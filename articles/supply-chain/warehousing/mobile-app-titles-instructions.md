---
title: Mobiilirakenduse Warehouse Management etapipealkirjade ja juhiste kohandamine
description: See teema kirjeldab, kuidas luua ja näidata kohandatud juhiseid iga ülesandevoo etapi kohta, mille mobiilirakendusele Warehouse Management seadistate.
author: MarkusFogelberg
ms.date: 08/11/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-08-11
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 112f4ab1d4ed6081ca14e93c3767139ccf95c9f7
ms.sourcegitcommit: 3d05bb2a423fe130700686ff73daa355d15b0e09
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386143"
---
# <a name="customize-step-titles-and-instructions-for-the-warehouse-management-mobile-app"></a>Mobiilirakenduse Warehouse Management etapipealkirjade ja juhiste kohandamine

> [!IMPORTANT]
> Selles teemas kirjeldatud funktsioonid kehtivad ainult uue mobiilirakenduse Warehouse Management kohta. Need ei mõjuta vana laorakendust, mis on nüüdseks iganenud.

See teema kirjeldab, kuidas luua ja näidata kohandatud juhiseid iga ülesandevoo etapi kohta, mille mobiilirakendusele Warehouse Management seadistate. Kui laotöötajad saavad hästi kirjutatud juhised, saavad nad alustada uute voogude kasutamist ilma eelnevat väljaõpet vajamata. See funktsioon pakub järgmisi eeliseid.

- **Valmistab töölised kiiremini ette, lastes neil järgida ülesande iga etapi kohta käivaid lihtsaid juhiseid.** Iga voo samm annab juhised, mis võimaldavad eesliini töötajatel ülesannet mõista.
- **Sisestage juhised, mis vastavad teie enda protsessidele.** Kirjutage oma juhised teie äri- ja laoprotsessidele vastavalt. Näiteks võite sobitada terminoloogia teie füüsilisele asukohale ja kohalikele lühenditele vastavaks.

## <a name="turn-on-the-warehouse-app-step-instructions-feature"></a>Lülitage laorakenduse etapiviisiliste juhiste funktsioon sisse

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *laorakenduse etapiviisilised juhised*

## <a name="step-titles-and-step-instructions-in-the-app"></a>Etappide pealkirjad ja etappide juhised rakenduses

Ülesandevoo iga etapp tuvastatakse mobiilirakenduses Warehouse Management etapi ID-ga. Lisaks on igal etapil pealkiri, ikoon ja juhised. (Lisateavet vt [Mobiilirakendusele Warehouse Management etappide ikoonide ja pealkirjade määramine](step-icons-titles.md).)

### <a name="step-titles"></a>Etappide pealkirjad

*Etapi pealkiri* on lühikirjeldus sellest, mida töötaja peaks etapi jooksul tegema. See kuvatakse ekraani ülaosas suure tekstina, nii nagu näidatud järgmisel joonisel.

![Etapi pealkirja näide mobiilirakenduses Warehouse Management](media/wma-step-title.png "Etapi pealkirja näide mobiilirakenduses Warehouse Management")

> [!TIP]
> Suure kirjasuuruse tõttu peaksite proovima hoida etappide pealkirjad võimalikult lühikesed. Vastasel juhul võib tekst olla äralõigatud. Ent pikemate pealkirjade puhul saavad töötajad pealkirja siiski vajutada ja all hoida, et avada dialoogiboks, kus kuvatakse täistekst.

### <a name="step-instructions"></a>Etapi juhised

*Etapi juhis* on pikem kirjeldus, mis annab rohkem teavet selle kohta, mida töötaja etapi jooksul peaks tegema. See ilmub hüpikaknas, nagu järgmisel joonisel näha.

![Etapi juhise näide mobiilirakenduses Warehouse Management](media/wma-step-instructions.png "Etapi juhise näide mobiilirakenduses Warehouse Management")

Etapi juhis kuvatakse automaatselt etapi avamisel. Töötajad saavad seda eirata, puudutades ükskõik millist kohta väljaspool dialoogiboksi. Lisaks on dialoogiboksis märkeruut **Ära näita uuesti**, mille töötajad saavad valida, et vältida juhise kuvamist järgmisel korral sama ülesande täitmisel.

## <a name="load-the-default-setup"></a>Vaikehäälestuse laadimine

Kui funktsiooni *Laorakenduse etappide juhised* esmakordselt sisse lülitate, ei sisalda teie süsteem kohandatavaid etappide pealkirju või juhiseid. Seega tuleb kõigepealt laadida vaikeseadistus. Vaikeseadistus sisaldab tekste kõigi saadaolevate etappide ID-de jaoks igas toetatud keeles. Vaikeseadistuse laadimiseks toimige järgmiselt.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme etapid**.
1. Valige toimingupaanilt suvand **Loo vaikeseadistus**. Leht täidetakse standardetappidega.

## <a name="customize-step-titles-and-instructions"></a>Etappide pealkirjade ja juhiste kohandamine

Etapi pealkirja ja/või juhise kohandamiseks ükskõik mitmes keeles toimige järgmiselt.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme etapid**.

    Lehekülg **Mobiilse seadme etapid** loetleb kõik etapid, mis on teie süsteemis saadaval. Iga etapi ID-d saab ühiskasutada mistahes arvu mobiilsete seadmete menüüelementidega. Kui etapi ID on mitme menüüelemendi vahel ühiskasutuses, kuvatakse kõikidele neile menüüelementidele sama pealkiri ja juhised. Kuid saate luua ülekirjutusi, et kohandada konkreetsete menüüelementide pealkirja ja juhiseid. (Lisateabe saamiseks vt järgmist jaotist.)

    Ruudustik sisaldab järgmisi veerge.

    - **Menüüelemendi nimi** – read, kus see veerg on tühi, kasutavad etapi vaikepealkirja ja -juhiseid, mis kehtivad kõigi mobiilse seadme menüüelementide kohta, mille jaoks ülekirjutust määratletud ei ole. Ridadel, kus selle veeru väärtuseks on seatud menüüelemendi nimi, on ülekirjutused, mis kehtivad ainult konkreetsele menüüelemendile.
    - **Etapi ID** – etapi kordumatu ID.
    - **Sisendi pealkiri** – pealkiri, mis kuvatakse, kui rakendus taotleb uut teavet. Tavaliselt on lehekülje väljad tühjad (st neil pole eelseadistatud väärtusi).
    - **Kinnituse pealkiri** – pealkiri, mis kuvatakse, kui rakendus taotleb kinnitust väärtusele, mis on juba süsteemis talletatud. Tavaliselt on lehekülje väljadel eelseadistatud väärtused.

1. Leidke **Etapi ID** ja **menüüelemendi nime** nende väärtuste kombinatsioon, mida soovite redigeerida, ja valige väärtus veerus **Etapi ID**. Avanev lehekülg loetleb kõik saadaolevad valitud etapi pealkirja ja juhiste tõlked.
1. Teksti kohandamiseks mis tahes keele jaoks järgige ühte järgmistest sammudest. Mõlema valiku abil saate redigeerida olemasolevate keelte tekste. Kuid ainult esimene valik võimaldab teil lisada tekste uutesse keeltesse, samas kui ainult teine valik võimaldab teil vaadata ja redigeerida kõigi olemasolevate menüüspetsiifiliste valitud keele ülekirjutuste tekste.

    - Valige tööriistaribal käsk **Lisa**, et avada dialoogiboks, kus saate iga toetatud keele jaoks tekste lisada või redigeerida. Seadke väli **Viitekeel** sellele keelele, mille väärtusi soovite vaadata. Väärtused kuvatakse vasakul veerus. Seadke väli **Tõlgete keel** sellele keelele, mida soovite lisada või kohandada. Redigeerige parempoolses veerus vajadusel väljade **Sisendi pealkiri**, **Sisendi juhis**, **Kinnituse pealkiri** ja **Kinnituse juhis** väärtuseid. Seejärel valige **OK**.
    - Otsige ja valige ruudustikus rida, kus väli **Keel** oleks määratud keelele, mida soovite redigeerida. Valige tööriistaribal **Vaata &lt;keel&gt; selle etapi tõlked**, et avada dialoogiboks, kus saate redigeerida valitud keele kõigi saadaolevate ülekirjutuste tekste. Dialoogiboks sisaldab ruudustikku, milles on read nii standardtekstidele (kus väli **Menüüelemendi nimi** on tühi) kui ka igale saadaolevale ülekirjutuse tekstile (kus väli **Menüüelemendi nimi** on seadistatud sellele menüüelemendi nimele, mille kohta ülekirjutus kehtib). Redigeerige vajadusel väljade **Sisendi pealkiri**, **Sisendi juhis**, **Kinnituse pealkiri** ja **Kinnituse juhis** väärtuseid. Seejärel valige **OK**.

1. Jätkake tööd seni, kuni olete määratlenud iga vajaliku pealkirja ja juhise iga vajaliku keele kohta.

## <a name="add-menu-specific-overrides"></a>Menüüpõhiste ülekirjutuste lisamine

Nagu eelmises jaotises mainitud, saate igale etapi ID-le luua mis tahes arvu menüüpõhiseid ülekirjutusi. Seda võimalust saate kasutada juhiste redigeerimiseks ja muutmiseks, et see sobiks paremini teie kohaliku äriprotsessiga konkreetse menüüelemendi jaoks. Näiteks müügi komplekteerimise korral, kui teie ettevõte annab tavaliselt töötajatele töö ID-d trükitud dokumendina, saate and vihje, et töötajad peaksid alustama töö ID skannimisest.

Iga ülekirjutamine rakendub konkreetsele mobiilseadme menüüelemendile ja võib sisaldada mis tahes arvu tõlkeid. Kui menüüelemendi kohta pole ühtegi ülekirjutust, kasutab menüüelement standardtekste. Kui keele jaoks ei ole määratletud ühtegi tõlget, kasutatakse standardtekste isegi menüüelementide korral, mille puhul on teiste keelte jaoks määratud ülekirjutus.

Ülekirjutuse loomiseks ja konfigureerimiseks toimige järgmiselt.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme etapid**.
1. Leidke ja valige ruudustikust rida, mille jaoks ülekirjutus luua.
1. Valige toimingupaanilt suvand **Lisa etapi konfiguratsioon**.
1. Seadistage ripploendis **Lisa etapi konfiguratsioon** välja **Menüüelement** väärtuseks selle mobiiliseadme menüüelemendi nimi, mille kohta teie ülekirjutus kehtib. Seejärel valige **OK**.
1. Kuvataval leheküljel kuvatakse kõik uue ülekirjutuse jaoks saadaolevad tekstid. Algselt luuakse ainult üks keel. Kui te ei lisa neid keeli siia, jätkavad kõik teised keeled standardtekstide kasutamist. Redigeerige tekste ja lisage vastavalt vajadusele uued keeled, nagu eelmises jaotises kirjeldatud.
