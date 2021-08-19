---
title: Saadetise automaatne vabastamine ristlaadimiseks
description: See teemas kirjeldatakse ristlaadimise strateegiat, mille abil saate automaatselt vabastada nõudlustellimuse lattu, kui tootmistellimus, mis tarnib nõudluskoguse, on kinnitatud lõpetatuks, nii et kogus teisaldatakse otse toodangu vabastamise asukohast väljaminevasse asukohta.
author: omulvad
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 74e26953fc964a3cfdee182433a017bb53fa45d62beab442b2c224e8365adef0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755950"
---
# <a name="auto-release-shipment-for-cross-docking"></a>Saadetise automaatne vabastamine ristlaadimiseks

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse ristlaadimise strateegiat, mille abil saate automaatselt vabastada nõudlustellimuse lattu, kui tootmistellimus, mis tarnib nõudluskoguse, on kinnitatud lõpetatuks. Sel viisil teisaldatakse nõudlustellimuse täitmiseks vajalik kogus toodangu väljastuskohast otse väljaminevasse asukohta.

Ristlaadimine on laohaldusvoog, kus väljamineva tellimuse täitmiseks vajalik kogus suunatakse tellimuse väljastusalale või koondusalale asukohast, kus sissetulev tellimus saadi. (Sissetulev tellimus võib olla ostutellimus, üleviimistellimus või tootmistellimus). Kui täpsem ristlaadimise funktsioon toetab kõiki tarne- ja nõudlustellimusi ning nõuab, et väljaminev nõudlus väljastatakse enne ristlaadimise tuvastamist, siis saadetise automaatse vabastamise funktsioonil on järgmised omadused:

- See toetab ainult tootmistellimusi kui pakkumist ning ainult müügitellimusi ja üleviimistellimusi kui nõudlust.
- Ristlaadimistoimingu saab käivitada ka siis, kui nõudlustellimust ei vabastatud lattu enne tarne vastuvõtmise registreerimist (st enne tootmise lõpetamise kinnitamist).

Sellel ristlaadimise funktsioonil on kaks eelist:

- Laotoimingud võivad vahele jätta lõpetatud kaupade koguse ladustamise tavapärasesse ladustamisalasse, kui need kogused võetakse uuesti välja väljamineva tellimuse täitmiseks. Selle asemel saab kogused teisaldada ühe korra väljastamiskohast kuni pakkimis-/saatmiskohani. Sel viisil aitab funktsioon vähendada laovarude käsitsemiskordade arvu ja lõppkokkuvõttes aitab suurendada aja ja ruumi kokkuhoidu laos.
- Laotoimingute abil saab müügitellimuste ja üleviimistellimuste vabastamist lattu edasi lükata seni, kuni tootmistellimusse kuuluvate lõpetatud kaupade väljastus on lõpetatuna kinnitatud. See eelis võib olla eriti asjakohane tellimuse järgi tootmise keskkondades, kus tootmise täitmisajad kipuvad olema pikemad kui lattutootmise keskkondades.

## <a name="prerequisites"></a>Eeltingimused

| Eeltingimus | Kirjeldus |
|---|---|
| Üksus | Kauba puhul peavad olema lubatud laohaldusprotsessid.<p>**Märkus.** Tegeliku kaaluga kaupu ei saa kaasata ristlaadimise protsessidesse.</p> |
| Ladu | Laos peavad olema lubatud laohaldusprotsessid. |
| Ristlaadimismallid | Antud lao jaoks peab olema seadistatud vähemalt üks ristlaadimismall, mis kasutab nõudluse vabastamise poliitikat **Tarne vastuvõtmisel**. |
| Töö klass | Töötellimuse tüübi **Ristlaadimine** jaoks tuleb luua ristlaadimise tööklassi ID. |
| Töömallid | Töötellimuse tüübi **Ristlaadimine** töömallid on vajalikud ristlaadimise komplekteerimis- ja asetamistöö loomiseks. |
| Asukohakorraldus | Töötellimuse tüübi **Ristlaadimine** asukohakorraldused on vajalikud, et suunata asetamistöö asukohtadesse, kus müügitellimuse kogused pakitakse ja saadetakse välja. |
| Nõudlustellimuse ja tootmistellimuse vaheline märgistus | Laosüsteem võib käivitada väljamineva tellimuse saadetise automaatse vabastamise ja luua ristlaadimise töö väljastuskohast lõpetatuna märkimise tegevuse käigus ainult siis, kui müügitellimused ja üleviimistellimused on reserveeritud ja märgitud võrreldes tootmistellimusega. |

## <a name="example-cross-docking-flow"></a>Ristlaadimise voo näide

Tüüpiline ristlaadimise voog koosneb järgmistest põhietappidest.

1. Müügitellimuse vastuvõtja loob müügitellimuse tellimuse järgi tehtud toote kohta. Tavaliselt ei ole taotletud kogus käepärast ja see tuleb esmalt toota.
2. Müügitellimuse vastuvõtja loob tootmistellimuse otse müügitellimuse realt. Sel viisil reserveerib ja märgib müügitellimuse vastuvõtja müügitellimuse koguse võrreldes tootmistellimuse kogusega. 

    Teise võimalusena määrab tootmise plaanija, et märkimist tuleb uuendada plaanitud tellimuste kinnitamisel.

3. Tootmistellimus läbib järgmised etapid:

    1. Tootmise plaanija hindab tootmistellimust ja väljastab selle. (Hinnang sisaldab toormaterjali reserveerimist ja väljastamine hõlmab lattu väljastamist.)
    2. Laotöötaja alustab ja lõpetab toormaterjali komplekteerimise ladustamiskohast tootmissisendi asukohta vastavalt toodangu komplekteerimistööle.
    3. Tööde operaator käivitab tootmistellimuse.
    4. Viimase toimingu käigus annab masinaoperaator mobiilse seadme abil teada tootmistellimuse lõpulejõudmisest.

4. Süsteem kasutab seadistust, et tuvastada kahe lingitud tellimuse puhul ristlaadimise sündmus, ja seejärel täidab need ülesanded:

    1. Seotud müügitellimuse automaatne vabastamine lattu saadetise loomiseks.
    2. Ristlaadimistöö automaatne loomine, millel on juhised komplekteerida lõpetatud kaubad väljastamiskohast ja teisaldada need väljaminevasse asukohta, mille ristlaadimise asukohakorraldused määrasid müügitellimusele.
    3. Käsk masinaoperaatorile lõpetada ristlaadimistöö kohe pärast tootmistellimuse lõpetatuna kinnitamist.

5. Pärast ristlaadimistöö lõpetamist ja koguste laadimist sõidukile kinnitab väljamineva lao plaanija müügisaadetise.

## <a name="example-scenario"></a>Näidisstsenaarium

Sellisel juhul peavad teil olema installitud demoandmed ja peate kasutama **USMF** demoandmete ettevõtet.

### <a name="set-up-cross-docking-that-uses-the-auto-release-shipment-feature"></a>Saadetise automaatse vabastamise funktsiooni kasutava ristlaadimise seadistamine

#### <a name="cross-docking-template"></a>Ristlaadimismall

1. Avage **Laohaldus** \> **Seadistus** \> **Töö** \> **Ristlaadimismallid**.
2. Valige suvand **Uus**.
3. Sisestage väljale **Järjekorranumber** väärtus **1**.
4. Sisestage väljale **Ristlaadimismalli ID** nimi, näiteks **XDock\_RAF**.
5. Valige väljal **Nõudluse vabastamise poliitika** väärtus **Tarne vastuvõtmisel**.
6. Sisestage väljale **Ladu** lao number, kus soovite ristlaadimisprotsessi seadistada. Selles näites valige **51**.

    > [!NOTE]
    > Niipea kui valite malli nõudluse vabastamise poliitikaks **Tarne vastuvõtmisel**, muutuvad kõik muud selle lehe väljad mittekättesaadavaks. Samuti ei saa määrata ühtegi tarneallikat. Selline käitumine ilmneb seetõttu, et ristlaadimine, mis kasutab saadetise automaatse vabastamise funktsiooni, toetab tarneallikatena ainult tootmistellimusi ja see nõuab, et müügitellimuste ja tootmistellimuste vahel oleks märgistus. Kui valite nõudluse vabastamise poliitikaks **Enne tarne vastuvõtmist**, on vahekaartide **Plaanimine** ja **Tarneallikad** väljad saadaval ja neid saab redigeerida.

#### <a name="work-classes"></a>Töö klassid

1. Avage **Laohaldus** \> **Seadistus** \> **Töö** \> **Töö klassid**.
2. Valige suvand **Uus**.
3. Sisestage väljale **Töö klassi ID** nimi, nt **CrossDock**.
4. Valige väljal **Töökäsu tüüp** suvand **Ristlaadimine**.

Selleks, et piirata asukohtade tüüpe, kuhu ristlaaditud lõpetatud kaupu saaks panna, saate määrata ühe või mitu sobivat asukohatüüpi.

#### <a name="work-templates"></a>Töömallid

1. Avage **Laohaldus** \> **Seadistus** \> **Töö** \> **Töömallid**.
2. Valige väljal **Töökäsu tüüp** suvand **Ristlaadimine**.
3. Valige suvand **Uus**.
4. Sisestage väljale **Järjekorranumber** väärtus **1**.
5. Sisestage väljale **Töömall** nimi, nt **CrossDock\_51**.
6. Valige käsk **Salvesta**.
7. Valige jaotises **Töömalli üksikasjad** valik **Uus**.
8. Valige uue rea jaoks väljal **Töö tüüp** väärtus **Komplekteerimine**. Valige väljal **Töö klassi ID** väärtus **CrossDock**.
9. Valige suvand **Uus**.
10. Valige uue rea jaoks väljal **Töö tüüp** väärtus **Ladustamine**. Valige väljal **Töö klassi ID** väärtus **CrossDock**.

#### <a name="location-directives"></a>Asukohakorraldus

Lõpetatud kaupade standardne ladustamisprotsess nõuab asukohakorraldust **Ladustamine**, et juhtida komplekteeritud toodangu koguste liikumist tavapärasesse salvestusruumi. Samuti peate seadistama ristlaadimise asukohakorralduse **Ladustamine**, et teha töö ülesandeks ladustada lõpetatud kogus määratud väljaminevasse asukohta, mis teenindab seotud müügitellimuse saadetist.

Ristlaadimise, nagu ka lõpetatud kaupade tavapärase ladustamise puhul, ei pea te komplekteerimise töötegevuse jaoks looma asukohakorraldust, sest väljaminev asukoht on antud. Lisaks eeldatakse, et see väljastamiskoht seadistatakse kas väljastamise vaikeasukohana ühes ressursiga seotud kirjetest (st ressurss, ressursigrupi seoste kogum või ressursigrupp) või lao tootmise lõpetatud kaupade vaikeasukohana.

1. Avage **Laohaldus** \> **Seadistus** \> **Asukohakorraldused**.
2. Valige väljal **Töökäsu tüüp** suvand **Ristlaadimine**.
3. Valige suvand **Uus**.
4. Sisestage väljale **Järjekorranumber** väärtus **1**.
5. Sisestage väljale **Nimi** nimi, nt **Baydoor**.
6. Väljal **Töö tüüp** valige **Paigal**.
7. Valige väljal **Tegevuskoht** väärtus **5**.
8. Valige väljal **Ladu** väärtus **51**.
9. Valige kiirkaardil **Read** suvand **Uus**.
10. Sisestage väljale **Koguseni** vahemiku maksimaalne kogus, nt **1000000**.
11. Valige käsk **Salvesta**.
12. Valige kiirkaardil **Asukohakorralduste tegevused** suvand **Uus**.
13. Sisestage väljale **Nimi** nimi, nt **Baydoor**.
14. Valige käsk **Salvesta**.
15. Saate kasutada standardset päringut, et piirata asukohtade paigutamist ühte või mitmesse kindlasse asukohta. Valige **Redigeeri päringut** ja seejärel valige tabeli **Asukohad** välja **Ladu** kriteeriumiks **51**.

### <a name="cross-dock-finished-goods-to-the-outbound-location"></a>Lõpetatud kaupade ristlaadimine väljaminevasse asukohta

Lõpetatud kauba koguse ristlaadimiseks seotud müügitellimuse väljaminevasse asukohta tehke järgmist.

1. Avage **Müük ja turundus** \> **Müügitellimused** \> **Kõik müügitellimused**.
2. Valige suvand **Uus**.
3. Müügitellimuse päise jaoks valige kliendikonto **US-001** ja ladu, mis on seadistatud ristlaadimiseks, mis kasutab saadetise automaatse vabastamise funktsiooni.
4. Lisage lõpetatud toote jaoks rida ja sisestage koguseks **10**.
5. Valige jaotises **Müügitellimuse read** suvandid **Toode ja tarnimine** \> **Tootmistellimus**.
6. Vadake dialoogiboksis **Tootmistellimuse loomine** üle vaikeväärtused ja seejärel valige **Loo**. Luuakse uus tootmistellimus ja lingitakse müügitellimusega (st reserveeritakse ja märgistatakse).
7. Valikuline: muutke välja **Kogus** väärtust nii, et see oleks suurem kui müügitellimuse täitmiseks vajalik väärtus. Kui toodangu kogus on lõpetatuna kinnitatud, loob süsteem märgistatud koguse kohta ristlaadimistöö ja ülejäänud koguse kohta ladustamistöö vastavalt lõpetatud kaupade ladustamise tavaprotseduurile.

    Nagu varem mainitud, peab müügitellimuse ja tootmistellimuse vahel olema märgistus. Vastasel juhul ristlaadimine ei toimi. Märkimise saab luua mitmel viisil:

    - Süsteem saab automaatselt luua märgistuse järgmistes olukordades:

        - Tootmistellimus luuakse käsitsi otse müügitellimuse realt (vt 6. samm).
        - Plaanitud tootmistellimused on kinnitatud ja välja **Märkimise värskendamine** väärtuseks on seatud **Standardne**.

    - Kasutaja saab märgistuse käsitsi luua, avades lehekülje **Märgistus** nõudlustellimuse realt.

    > [!NOTE]
    > Märkimist ei saa käsitsi luua kaupadele, mis on seadistatud kasutama laomudelina standardset ja kaalutud keskmist.

8. Valige lehe **Tootmistellimus** toimingupaani vahekaardi **Tootmistellimus** grupis **Protsess** üksus **Hinda** ja seejärel valige **OK**. Tellimust hinnatakse ja toormaterjali kogus reserveeritakse tootmiseks.
9. Valige toimingupaani vahekaardi **Tootmistellimus** grupis **Protsess** üksus **Vabasta** ja seejärel valige **OK**. Toormaterjalide jaoks luuakse lao komplekteerimistöö.
10. Avage töö ja vaadake see üle. Valige toimingupaani vahekaardil **Ladu** grupis **Seotud teave** üksus **Töö üksikasjad**. Märkige üles töö ID.
11. Logige sisse mobiilirakendusse Warehouse Management, et käivitada töö laos 51.
12. Avage **Tootmine** \> **Tootmise komplekteerimine**.
13. Sisestage töö ID, et alustada toormaterjali komplekteerimist ja viia see lõpule. 

    Pärast töö lõpetatuna kinnitamist on toormaterjalide kogus saadaval tootmissisendi asukohas (**005** USMF-i demoandmetes) ja tootmistellimuse täitmine saab alata.

14. Valige lehe **Tootmistellimus** toimingupaani vahekaardi **Tootmistellimus** grupis **Protsess** üksus **Alusta** ja seejärel valige **OK**.
15. Rakenduses avage **Tootmine** \> **RAF ja kõrvalepanek**.
16. Sisestage väljale **Prod ID** tootmistellimuse number ja muud kohustuslikud üksikasjad ning seejärel valige **OK**.

Pange tähele, et toimuvad järgmised sündmused:

- Lattu vabastamine käivitatakse lingitud müügitellimuse puhul.
- Vabastamise põhjal luuakse saadetis ja ristlaadimistöö. See töö käsib laooperaatoril komplekteerida müügitellimuse rea täitmiseks vajalikud kogused ja panna need väljaminevasse asukohta, mis on määratud ristlaadimise asukohakorralduses.
- Kui tootmistellimuse kogus on suurem kui müügitellimuse nõutav kogus, luuakse tavapärane paigutustöö. See töö teeb laooperaatorile ülesandeks komplekteerida lõpetatud kaupade kogus, mis jääb järele pärast ristlaadimist ja teisaldada see tavalisse lattu vastavalt asukohakorraldusele.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]