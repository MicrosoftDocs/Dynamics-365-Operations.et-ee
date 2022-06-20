---
title: Plaanitud ristlaadimine
description: See artikkel kirjeldab täpsemat planeeritud ristlaadimist, kus tellimuseks nõutav varude kogus suunatakse otse sissetulekust või loomisest õigesse väljastusalasse või ladustamisalasse. Kõik järelejäänud sissetulevast allikast pärinevad varud suunatakse õigesse ladustamiskohta, kasutades tavalist ladustamise protsessi.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 28ebf1b4fb966fd6801e75e7b3a6c8741114938d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863675"
---
# <a name="planned-cross-docking"></a>Plaanitud ristlaadimine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab täpsemat planeeritud ristlaadimist. Ristlaadimine on laoprotsess, kus tellimuse jaoks nõutav varude kogus suunatakse sissetulekust või loomisest otse õigesse väljaminevasse väljastus- või koondusalasse. Kõik järelejäänud sissetulevast allikast pärinevad varud suunatakse õigesse ladustamiskohta, kasutades tavalist ladustamise protsessi.

Ristlaadimine võimaldab töötajatel jätta vahele juba väljaminevasse tellimusse märgitud varude sissetulevat ladustamist ja väljaminevat komplekteerimist. Selle abil vähendatakse varude liigutamise kordade arvu, kus see on võimalik. Lisaks, kuna süsteemiga suheldakse vähem, säästetakse rohkem lao kaupluse korrusel olevat aega ja ruumi.

Enne ristlaadimise käivitamist peate konfigureerima uue ristlaadimise malli, kus on määratud ristlaadimise tarneallikas ja muud nõuete kogumid. Kui väljaminev tellimus on loodud, tuleb rida tähistada sissetuleva tellimusega, mis sisaldab sama kaupa. Ristlaadimise mallil saate valida direktiivi koodi välja sarnaselt täiendamise ja ostutellimuste seadistamise viisile.

Sissetuleva tellimuse vastuvõtmise ajal tuvastab ristlaadimise seadistus automaatselt ristlaadimise vajaduse ning loob vajaliku koguse jaoks liikumise töö, mis põhineb asukohakorralduse seadistusel.

> [!NOTE]
> Lao kandeid *ei* jäeta registreerimata ristlaadimise tühistamisel, isegi kui selle võimaluse säte on laohalduse parameetrites sisse lülitatud.

## <a name="turn-on-the-planned-cross-docking-features"></a>Plaanitud ristilaadimise funktsioonide sisselülitamine

Kui teie süsteem ei kaasa juba selles artiklis kirjeldatud funktsioone, [minge](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) Funktsioonihaldusse ja lülitage järgmised funktsioonid sisse järgmises järjekorras:

1. *Plaanitud ristlaadimine*
1. *Asukohadirektiividega ristiliaadimismallid*
    > [!NOTE]
    > See funktsioon võimaldab määrata ristlaadimise mallil **direktiivi tähise** välja sarnaselt täiendusmallide seadistamise viisiga. Selle funktsiooni lubamine takistab teil lõpliku *put*-rea ristlaadimise töömalli ridadele direktiivi koodi lisamist. See tagab, et lõpliku asukoha saab määrata töö loomise ajal enne töömallide kaalumist.

## <a name="setup"></a>Seadistus

### <a name="regenerate-load-posting-methods"></a>Koorma sisestamise meetodite uuesti loomine

Plaanitud ristlaadimine rakendatakse koormuse sisestamise meetodina. Pärast funktsiooni sisselülitamist tuleb meetodid uuesti luua.

1. Avage jaotis **Laohaldus \> Seadistus \> Koormuse sisestamise meetodid**.
1. Valige toimingupaanil suvand **Meetodite uuesti loomine**.

    Kui uuesti loomine on lõpule viidud, peaksite nägema meetodit, mille suvandi **Meetodi nimi** väärtus on *planCrossDocking*.

1. Sulgege leht.

### <a name="create-a-cross-docking-template"></a>Ristlaadimise malli loomine

1. Avage **Laohaldus \> Seadistus \> Töö \> Ristlaadimismallid**.
1. Malli loomiseks valige toimingupaanilt suvand **Uus**.
1. Määrake päises järgmised väärtused.

    - **Järjestus:** *1*

        See väli määratleb mallide hindamise järjekorra.

    - **Ristlaadimismalli ID:** *51*
    - **Kirjeldus:** *Ladu 51*
    - **Nõudluse vabastamise poliitika:** *Enne tarne vastuvõtmist*
    - **Ladu:** *51*

1. Kiirkaardi **Planeerimine** seadistus juhib kuidas mall töötab. Määrake järgmised väärtused.

    - **Nõudluse nõuded:** *Puudub*

        See väli määratleb nõudluse varude nõuded. Kui nõudlus peab olema seotud tarnega enne vabastamist, valige *Märkimine*. Kui nõudmine tuleb enne vabastamist reserveerida vastavalt tellimusele, valige *Tellimuse reserveerimine*.

    - **Tüübi leidmine:** *Saadetise asukohad*

        See väli määratleb, kas ristlaadimise töö peaks kasutama saadetise ajastamise/koormuse asukohti või kas see peaks kasutama asukohakorraldusi oma ajastamise/koormuse asukohtade leidmiseks.

    - **Töömall:** jätke see väli tühjaks.

        See väli määratleb töömalli, mida tuleks kasutada ristlaadimise töö loomisel.

    - **Uuesti kinnitamine tarne vastuvõtmisel:** *Ei*

        See suvand määratleb, kas tarnet tuleb vastuvõtmise ajal uuesti kinnitada. Kui selle suvandi väärtuseks on seatud *Jah*, kontrollitakse nii maksimaalset ajavahemikku kui ka aegumiskuupäevade vahemikku.

    - **Korralduse kood:** jätke see väli tühjaks

        Selle suvandi lubavad *asukohadirektiivide funktsiooniga ristlaadimismallid*. Süsteem kasutab asukohakorraldusi, et aidata määrata parim asukoht ristlaadimise varude teisaldamiseks. Selle seadistamiseks määrake igale asjakohasele ristlaadimise mallile korralduse kood. Kui määratakse direktiivikood, otsib süsteem töö loomisel asukohadirektiive direktiivikoodi järgi. Sel viisil saate piirata asukohajuhiseid, mida kasutatakse konkreetse ristlaadimise malli puhul.

    - **Kinnita maksimaalne ajavahemik:** *Jah*

        See suvand määratleb, kas maksimaalset ajavahemikku tuleb hinnata tarneallika valimisel. Kui selle suvandi väärtuseks on seatud *Jah*, siis muutuvad maksimaalse ja minimaalse ajavahemiku väljad kättesaadavaks.

    - **Maksimaalne ajavahemik** *5*

        See väli määratleb maksimaalse lubatud ajavahemiku, mis on lubatud tarne saabumise ja nõudluse väljamineku vahel.

    - **Maksimaalse ajavahemiku ühik:** *Päevad*
    - **Minimaalne ajavahemik:** *0*

        See väli määratleb minimaalse lubatud ajavahemiku, mis on lubatud tarne saabumise ja nõudluse väljamineku vahel.

    - **Minimaalse ajavahemiku ühik:** *Päevad*
    - **Aegumiskuupäevade vahemik** *0*

        *Esimesena aegunud esimesena välja (FEFO) kriteerium:* see väli määratleb maksimaalse päevade arvu, mis jääb praegu laos oleva partii esimesena aeguva aegumiskuupäeva ja vastuvõetava partii vahele.

1. Kiirkaardil **Tarneallikad** saate määrata selle malli jaoks kehtivad tarnetüübid. Valige **Uus** ja seejärel seadke järgmised väärtused.

    - **Järjekorranumber:** *1*
    - **Tarneallikas:** *Ostutellimus*

> [!NOTE]
> Saate seadistada päringu, et juhtida konkreetse ristdokkimise malli kasutamist. Ristlaadimise mallide päringus on ainult *InventTable*'i (kaubad) tabel ja sisemiselt ühendatud *WHSInventTable'i* (WHS-kaupade) tabel. Kui soovite päringule teisi tabeleid lisada, saate nendega liituda, kasutades ainult *olemas olnud liitmised* või *ei ole olemas liitmised*. Kui filtreerite ühendatud tabeleid, laaditakse põhitabelist kirje iga tabeli sobiva kirje kohta. Kui liitmistüüp *on olemas liitmine*, lõpeb otsing pärast esimese vaste leidmist. Näiteks kui te liidate müügitellimuse rea tabeliga kaupade tabeliga, kontrollib ja tagastab süsteem kaubad, mille kohta on määratud tingimus vähemalt ühel müügitellimuse real. Andmed on toodud ematabelist (kaubad), mitte alamtabelist (müügitellimuse rida). Seega ei saa lähtedokumentide (nt müügitellimuse ridade või klientide) alusel filtreerimist teha väljast.

### <a name="create-a-work-class"></a>Tööklassi loomine

1. Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töö klassid**.
1. Tööklassi loomiseks valige toimingupaanilt suvand **Uus**.
1. Määrake järgmised väärtused.

    - **Töö klassi ID:** *CrossDock*
    - **Kirjeldus:** *Ristlaadima*
    - **Töökäsu tüüp:** *Ristlaadimine*

### <a name="create-a-work-template"></a>Töömalli loomine

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Määrake välja **Töökäsu tüüp** väärtuseks *Ristlaadimine*.
1. Valige toimingupaanil suvand **Uus**, et lisada vahekaardile rida **Ülevaade**.
1. Määrake uuel real järgmised väärtused.

    - **Järjekorranumber:** *1*
    - **Töömall:** *51 ristlaadimine*
    - **Töömalli kirjeldus:** *51 ristlaadimine*

1. Valige **Salvesta**, et muuta kiirkaart **Töömalli üksikasjad** kättesaadavaks.
1. Valige kiirkaardil **Töömalli üksikasjad** suvand **Uus**, et lisada rida ruudustikku.
1. Määrake uuel real järgmised väärtused.

    - **Töö tüüp:** *Komplekteerimine*
    - **Töö klassi ID:** *CrossDock*

1. Valige **Uus**, et lisada uus rida ja määrake sellele järgmised väärtused.

    - **Töö tüüp:** *Ladustamine*
    - **Töö klassi ID:** *CrossDock*

1. Valige **Salvesta** ja kinnitage, et malli *51 ristlaadimine* on valitud märkeruut **Kehtiv**.
1. Valikuline: valige suvand **Redigeeri päringut**, kui soovite seada töömalli kasutamisel soovitud kriteeriumid.

    Saate seadistada päringu, et juhtida, millal konkreetset töömalli kasutatakse. Näiteks saate määrata, et malli saab kasutada tööks ainult konkreetses asukohas. Kui soovite, et ristlaadimise töö mall rakendati kindlas asukohas, peate filtreerima väljal **Alustamise asukoht**, mitte väljal **Asukoht**, sest sissetulevate protsesside (ost, ristlaadimine ja laadimine) töö loomine algab panemisrealt. Töö loomisel seadistab asukoha tähis **Asukoht** välja panemiskohaks. Kuid valimiskoht salvestatakse väljale **Alguskoht**.

> [!NOTE]
> Töötüübid *Komplekteerimine* ja *Ladustamine* peavad olema samad.

### <a name="create-location-directives"></a>Asukohakorralduste loomine

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Määrake vasakpoolse paani välja **Töökäsu tüüp** suvandiks *Ristlaadimine*.
1. Valige toimingupaanil **Uus** ja seejärel seadke järgmised väärtused.

    - **Järjekorranumber:** *1*
    - **Nimi:** *51 ladustamine ristlaadimisel*
    - **Töö tüüp:** *Ladustamine*
    - **Tegevuskoht:** *5*
    - **Ladu:** *51*

1. Valige **Salvesta**, et muuta kiirkaart **Read** kättesaadavaks.
1. Valige kiirkaardil **Read** suvand **Uus**, et lisada rida ruudustikku.
1. Määrake uuel real järgmised väärtused.

    - **Alates kogusest:** *1*
    - **Koguseni:** *1000000*

1. Valige **Salvesta**, et muuta kiirkaart **Asukohakorralduse toimingud** kättesaadavaks.
1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et lisada rida ruudustikku.
1. Määrake uuel real järgmised väärtused.

    - **Nimi:** *Baydoor*
    - **Fikseeritud asukoha kasutus:** *Fikseeritud ja mittefikseeritud asukohad*

1. Valige **Salvesta**, et muuta tööriistariba **Asukohakorralduse toimingud** nupp **Päringu redigeerimine** kättesaadavaks.
1. Valige päringuredaktori avamiseks **Päringu redigeerimine**.
1. Veenduge vahekaardil **Vahemik**, et järgmised kaks rida oleksid konfigureeritud.

    - Rida 1:

        - **Tabel:** *Asukohad*
        - **Tuletatud tabel:** *Asukohad*
        - **Väli:** *Ladu*
        - **Kriteeriumid:** *51*

    - Rida 2:

        - **Tabel:** *Asukohad*
        - **Tuletatud tabel:** *Asukohad*
        - **Väli:** *Asukoht*
        - **Kriteeriumid:** *Baydoor*

1. Päringuredaktori sulgemiseks valige **OK**.

### <a name="create-a-mobile-device-menu-item"></a>Mobiilse seadme menüü-üksuse loomine

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Valige vasakpoolse paani menüü-üksuste loendist **Ostu ladustamine**.
1. Valige suvand **Redigeeri**.
1. Valige kiirkaardil **Tööklassid** suvand **Uus**, et lisada rida ruudustikku.
1. Määrake uuel real järgmised väärtused.

    - **Töö klassi ID:** *CrossDock*
    - **Töökäsu tüüp:** *Ristlaadimine*

1. Valige käsk **Salvesta**.

## <a name="scenario"></a>Stsenaarium

### <a name="create-a-purchase-order"></a>Ostutellimuse loomine

Järgige neid etappe ostutellimuse loomiseks tarneallikana.

1. Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiboksis **Ostutellimuse loomine** määrake järgmised väärtused.

    - **Hankija konto:** *104*
    - **Ladu:** *51*

1. Valige **OK** ja märkige tellimuse number üles.
1. Kiirkaardile **Ostutellimuse read** lisatakse uus rida. Määrake sellel real järgmised väärtused.

    - **Kauba kood:** *A0001*
    - **Kogus:** *5*

### <a name="create-a-sales-order"></a>Loo müügitellimus

Järgige neid etappe müügitellimuse loomiseks nõudluse allikana.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Kliendi konto:** *US-002*
    - **Ladu:** *51*

1. Valige nupp **OK**.
1. Kiirkaardile **Müügitellimuse read** lisatakse uus rida. Määrake sellel real järgmised väärtused.

    - **Kauba kood:** *A0001*
    - **Kogus:** *3*

### <a name="create-planned-cross-docking"></a>Plaanitud ristlaadimise loomine

Järgige neid etappe osturellimusest plaanitud ristlaadimise loomiseks.

1. Valige äsja loodud müügitellimuse lehe **Müügitellimuse üksikasjad** toimingupaani vahekaardil **Ladu** grupis **Toimingud** suvand **Vabasta lattu**.

    Lattu vabastamine loob saadetise ja koormusrea müügitellimuse rea jaoks ning püüab eraldada varusid.
    
    Teile kuvatakse teade. Kuvatakse ka järgmine hoiatusteade: „Voo XXXX jaoks ei loodud ühtegi tööd. Lisateavet leiate töö loomise ajaloo logist.” Seda käitumist eeldatakse, kuna laos pole varusid.

1. Valige ruudustiku kohal oleva menüü **Ladu** kiirkaardilt **Müügitellimuse read** suvand **Saadetise üksikasjad**.

    Kuvatakse leht **Saadetise üksikasjad**, mis kuvab müügirea jaoks loodud saadetise.

1. Pange tähele, et kiirkaardil **Koormusread** on välja **Plaanitud ristlaadimise kogus** väärtuseks seatud *3*. Kuna laos polnud varusid saadaval, kuid kehtiv tarneallikas saabub ristlaadimismallis määratletud ajavahemikus, loodi ristlaadimise kogus.
1. Valige kiirkaardil **Koormusread** suvand **Plaanitud ristlaadimine**, et vaadata loodud ristlaadimise üksikasju.

## <a name="process-the-cross-docking"></a>Ristlaadimise töötlemine

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a>Ostutellimuse vastuvõtmine ladustamise mobiilirakendusega

Süsteem võtab ostutellimuselt vastu koguse 5 vastuvõtvasse asukohta ja loob kaks tööd.

Esimese loodud töö ID suvandi **Töötellimuse tüüp** väärtus on *Ristlaadimine* ja see on seotud müügitellimusega. Selle kogus on 3 ja see suunatakse saatmise lõplikku saatmisasukohta, et seda saaks kohe välja saata.

Teine loodud töö ID suvandi **Töötellimuse tüüp** väärtus on *Ostutellimused* ja see on seotud ostutellimusega. Sellel on järelejäänud kogus 2, mida ei ristlaaditud ja mis on suunatud lattu ladustamiseks.

1. Logige mobiilsesse seadmesse lao *51* kasutajana sisse.
1. Avage jaotis **Sissetulev \> Vastuvõetud ost**.
1. Sisestage väljale **PONum** oma ostutellimuse number.
1. Sisestage väljale **Kogus** väärtus *5*.
1. Valige nupp **OK**.
1. Järgmisel lehel määrake välja **Kaup** väärtuseks *A0001*.
1. Valige nupp **OK**.
1. Kinnitage järgmisel lehel väärtused **PONum**, **Kaup** ja **Kogus**, valides **OK**.

    Teile kuvatakse teade „Töö lõpule viidud”.

1. Väljumiseks valige **Tühista**.

### <a name="put-away-to-cross-docking-and-bulk"></a>Ristlaadimiseks ja hulgi ladustamine

Praegu on mõlemal töö ID-l sama sihtkoha identifitseerimisnumber. Järgmiste etappide lõpule viimiseks peate hankima töö ID ja sihtkoha identifitseerimisnumbri ID. Selle teabe saate hankida ostutellimuse rea ja müügitellimuse rea töö üksikasjadest. Saate minna ka jaotisse **Laohaldus \> Töö \> Töö üksikasjad** ja filtreerida töö jaoks, kus suvandi **Ladu** väärtus on *51*.

1. Avage mobiilsel seadmel **Sissetulev \> Ostude ladustamine** ja sisestage töö jaoks sihtidentifitseerimisnumber.
1. Sisestage väljale **ID** töö üksikasjadest saadud sihtidentifitseerimisnumbri ID.

    Lehel ristlaadimise komplekteerimine kuvatakse komplekteerimise asukoht (*RECV*), sihtidentifitseerimisnumber (*identifitseerimisnumber*), kaup (*A0001*) ja kogus (*3*).

1. Valige nupp **OK**.
1. Sisestage väljale **Siht-LP** sihtidentifitseerimisnumber selle identifitseerimisnumbri ID jaoks, mis tuleks ladustada (ristlaadida) saatmise asukohta. Saate valida mis tahes soovitud identifitseerimisnumbri ID.
1. Valige nupp **OK**.
1. Sisestage järgmisel lehel väljale **ID** sihtidentifitseerimisnumbri ID.
1. Valige nupp **OK**.
1. Kinnitage töö järelejäänud koguse 2 komplekteerimiseks ja seejärel valige **OK**.
1. Järgmisel lehel valige **Valmis** komplekteerimise toimingu lõpetamiseks ja alustage ladustamise protsessi.

    Mobiilirakendus annab teile nende jaoks asukoha ja identifitseerimisnumbri.

1. Kinnitage hulgiladustamine **Ladustamine**, valides **OK**.
1. Järgmisel lehel kinnitage ristlaadimine **Ladustamine**, valides **OK**.

    Teile kuvatakse teade „Töö lõpule viidud”.

1. Väljumiseks valige **Tühista**.

Järgmine illustratsioon näitab, kuidas lõpule viidud ristlaadimise tööd kuvatakse Microsoftis Dynamics 365 Supply Chain Managementis.

![Lõpule viidud ristlaadimise töö.](media/PlannedCrossDockingWork.png "Lõpule viidud ristlaadimise töö")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
