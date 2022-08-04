---
title: Tsüklilise inventuuri näidisstsenaariumid
description: See artikkel annab kogumi stsenaariume, mis uurivad Microsofti tsüklilise inventuuri funktsioone Dynamics 365 Supply Chain Management.
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4f6f3f2db6efcc4d4d6ae3d278751a230fca9a64
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068592"
---
# <a name="cycle-counting-example-scenarios"></a>Tsüklilise inventuuri näidisstsenaariumid

[!include [banner](../includes/banner.md)]

See artikkel annab kogumi stsenaariume, mis uurivad Microsofti tsüklilise inventuuri funktsioone Dynamics 365 Supply Chain Management. Kõigepealt kirjeldab see nõudeid oma olemasolevale Supply Chain Management keskkonnale. Seejärel selgitab see, kuidas konfigureerida tsüklilist inventuuri ja kirjeldab kõiki tsüklilise inventuuri etappe. Kui olete lõpetanud, peaks teil olema hea arusaam tsüklilise inventuuri, sealhulgas juhendatud tsüklilise inventuuri, pimetsüklilise inventuuri, punkttsüklilise inventuuri, tsüklilise inventuuri lävede ja tsüklilise inventuuri plaanidest.

## <a name="prerequisites"></a>Eeltingimused

### <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Iga stsenaarium selles artiklis viitab väärtustele ja kirjetele, mis sisalduvad tarneahela halduse standardsetes demoandmetes. Kui soovite kasutada siin esitatud väärtusi stsenaariumidega töötamise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks (ettevõte) **USMF**.

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a>Mobiilirakenduse Warehouse Management toe sisselülitamine

Laohalduse mobiilirakenduse kasutamiseks peavad uue *laorakenduse funktsiooni kasutajasätted,* ikoonid ja etapi pealkirjad olema süsteemis sisse lülitatud. Tarneahela halduse 10.0.25 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis on *vanem kui 10.0.25, saavad administraatorid selle funktsiooni sisse ja välja lülitada, otsides Kasutajasätteid, ikoone ja uue laorakenduse funktsiooni pealkirjad Funktsioonihalduse tööruumis*[...](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a>Stsenaariumite demoandmete ettevalmistamine

Järgige neid samme veendumaks, et kõik stsenaariumide jaoks vajalikud demoandmed on teie süsteemis USMF-i ettevõttes saadaval. Looge puuduvaid kirjeid või väärtusi.

1. Avage jaotis **Laohaldus \> Seadistus \> Töötaja**.
1. Valige loendi paanist **Julia Funderburk**.
1. Valige kiirkaardil **Kasutajad** järgmiste väärtustega rida. Kui need väärtused puuduvad, looge see.

    - **Kasutaja ID:** *61*
    - **Kasutajanimi:** *WH61*
    - **Vaikeladu:** *61*
    - **Menüü nimi:** *Peamine*

1. Seadke kiirkaardil **Töö** kasutajale *61* järgmised väärtused, kui neid ei ole veel seatud:

    - **On tsüklilise inventuuri ülevaataja:** *ei*
    - **Maksimaalne protsendi piirang:** *0*
    - **Maksimaalse koguse piirang:** *0*
    - **Maksimumväärtuse piirang:** *0*

1. Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töökaustad**.
1. Töökaustasid kasutatakse laotöö eraldamiseks töö (praegusel juhul tsüklilise inventuuri töö) tüübi alusel. Veenduge, et oleks olemas kirje järgmiste sätetega:

    - **Töökausta ID:** *CycleCount*
    - **Kirjeldus:** *tsükliline loendus*

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.
1. Valige loendipaanil kirje nimega *Tsükli loendus*. Kui see nimi pole olemasolevatel kirjetel, looge see. Kinnitage või määrake kirjele järgmised väärtused:

    - **Menüükäsu nimi:** *tsükli loendus*
    - **Pealkiri:** *juhendatud tsükli loendus*
    - **Režiim:** *töö*
    - **Kasuta olemasolevat tööd:** *Jah*
    - **Suunatud:** *süsteemi suunatud* (see väärtus näitab, et Supply Chain Management määrab töötajale tsüklilise inventuuri töö ID.)
    - **Kuva varude olek:** *Jah*

1. Valige toimingupaanil **Tsükliline inventuur**.
1. Kinnitage või määrake dialoogiboksis **Mobiilse seadme tsükliline inventuur** järgmised väärtused:

    - **Kuva kaubakood:** *jah*
    - **Kuva litsentsiplaat:** *jah*
    - **Katsete arv:** *1*

1. Valige dialoogiboksi sulgemiseks suvand **OK**.
1. Valige loendipaanil kirje nimega *Tsükliline pimeinventuur*. Kui see nimi pole olemasolevatel kirjetel, looge see. Kinnitage või määrake kirjele järgmised väärtused:

    - **Menüükäsu nimi:** *tsükliline pimeinventuur*
    - **Pealkiri:** *tsükliline pimeinventuur*
    - **Režiim:** *töö*
    - **Kasuta olemasolevat tööd:** *Jah*
    - **Juhatatud:** *Tsüklilise inventuuri rühmitamine* (see väärtus tähendab, et töötaja saab rühmitada asukoha, tsooni või töökausta tsüklilise inventuuri töö ID-d.)

1. Valige toimingupaanil **Tsükliline inventuur**.
1. Kinnitage või määrake dialoogiboksis **Mobiilse seadme tsükliline inventuur** järgmised väärtused:

    - **Kuva kaubakood:** *ei*
    - **Kuva litsentsiplaat:** *ei*
    - **Katsete arv:** *0*

1. Valige dialoogiboksi sulgemiseks suvand **OK**.
1. Valige loendipaanil kirje nimega *Punktinventuur*. Kui see nimi pole olemasolevatel kirjetel, looge see. Kinnitage või määrake kirjele järgmised väärtused:

    - **Menüükäsu nimi:** *punktinventuur*
    - **Pealkiri:** *punktinventuur*
    - **Režiim:** *töö*
    - **Kasuta olemasolevat tööd:** *Ei*
    - **Tööloomise protsess:** *punkttsükliline inventuur* (see väärtus näitab, et töötaja saab loendada kaupu lao asukohas igal ajal, tsüklilise inventuuri tööd loomata, sisestades asukoha ID. Punkttsüklilise inventuuri tegemiseks asukohas sisestab töötaja asukoha ID.)

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.
1. Valige loendipaanil kirje nimega *Laovarud*. Kui see nimi pole olemasolevatel kirjetel, looge see. Veenduge, et veerus **Menüüstruktuur** kuvatakse järgmised tsüklilise inventuuri menüü üksused:

    - Tsükliline inventuur
    - Tsükliline pimeinventuur
    - Punktinventuur

1. Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
1. Vahekaardil **Tsükliline inventuur** määrake järgmised väärtused.

    - **Tsüklilise inventuuri vaikimisi korrigeerimistüüp:** *tsükli inventuur* (see väli määrab töölehe tüübi, mis sisestatakse tsüklilise inventuuri korral.)
    - **Tsükli inventuuri tööklassi vaike-ID:** *CCount* (see väli määrab töö klassi, mida kasutatakse tsüklilise inventuuri jaoks.)
    - **Vaikimisi tsüklilise inventuuri töö prioriteet:** *50* (see väli seab prioriteedi, et tsüklilise inventuuri töö on seotud teist tüüpi tööga laos. Kui sisestate väiksema numbri kui muud tüüpi töödele sisestatud number, tõstate tsüklilise inventuuri töö prioriteeti.)

1. Avage jaotis **Laohaldus \> Seadistus \> Varud \> Korrigeerimistüübid**.
1. Leht **Korrigeerimistüübid** võimaldab luua koode erinevatele siss- ja välikorrigeerimistele, mis võivad ilmneda. Veenduge, et oleks olemas kirje järgmiste sätetega:

    - **Varude korrigeerimistüüp:** *tsükliline inventuur*
    - **Kirjeldus:** *tsükliline loendus*
    - **Nimi:** *ICnt*

1. Avage **Laohaldus \> Seadistus \> Lao seadistamine \> Laod**.
1. Valige loendi paanilt ladu *61*. Kui see nimi pole olemasolevatel kirjetel, looge see.
1. Kiirkaardil **Ladu** määrake järgmised väärtused.

    - **Kasuta laohalduse protsessi:** *Jah* (see väärtus võimaldab laohaldusprotsessidele (WMS)).
    - **Luba litsentsiplaadi liikumine tsüklilise inventuuri ajal:** *jah* (see väärtus võimaldab töötajatel teisaldada litsentsiplaate tsüklilise inventuuri ajal.)

## <a name="scenario-1-guided-cycle-counting"></a>1. stsenaarium: juhendatud tsükliline inventuur

Enne juhendatud tsüklilist inventuuri peate looma mõne töö. See töö juhendab määratud isikut läbi lao, asukohast asukohta, töös seadistatud loenduste lõpule viimiseks.

### <a name="create-cycle-counting-work-for-scenario-1"></a>1. stsenaariumi tsüklilise inventuuritöö loomine

Järgige neid samme, et luua tsüklilise inventuuri töö kauba asukohale *01A02R2S2B* (BULK-06) laos *61*.

1. Minge jaotisse **Laohaldus \> Tsükliline inventuur \> Tsüklilise inventuuri töö asukoha alusel**.
1. Seadke dialoogiboksis **Tsüklilise inventuuri töö loomine asukoha järgi** välja **Töökausta ID** väärtuseks *CycleCount*.
1. Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**.
1. Päringu redaktori dialoogiboksi vahekaardil **Vahemik** järgige järgmisi samme:

    - Rea puhul, kus välja **Väli** väärtuseks on seatud *Ladu*, seadke välja **Kriteeriumid** väärtuseks *61*.
    - Rea puhul, kus välja **Väli** väärtuseks on seatud *Asukoht*, seadke välja **Kriteeriumid** väärtuseks *01A02R2S2B*.

1. Päringuredaktori dialoogiboksi sulgemiseks valige **OK**.
1. Valige **OK**, et sulgeda dialoogiboks **Tsüklilise inventuuri töö loomine asukoha järgi**.

    Kui töö loomise protsess on lõpetatud, kuvatakse tegevuskeskuses sõnum.

1. Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.
1. Vastloodud töö leidmiseks seadistage filter veerule **Töökausta ID**, et leida kirjed, mille väärtus on *CycleCount*.

### <a name="do-cycle-counting-work-for-scenario-1"></a>1. stsenaariumi tsüklilise inventuuritöö teostamine

Pärast tsüklilise inventuuritöö loomist teete selle, loendades üksused laohoones ja seejärel mobiilseadme abil tulemuste sisestamiseks teenusesse Supply Chain Management. Järgige neid samme, et teha tsüklilise inventuuri töö mobiilirakenduses Warehouse Management.

1. Logige laohalduse mobiilirakenduse sisse töö kasutajana, [mille seadistasite selles artiklis varasema stsenaariumite](#prepare-demo-data) jaotises Demoandmete ettevalmistamine. Selles artikli näites on kasutaja nimeks *The Funderburk* ja seadistatud laole *61*. (USMF-i demoandmed peaksid lubama teil sisse logida selle töö kasutajana, sisestades *61* kasutaja ID-na ja *1* parooliks.)
1. Valige peamenüüs suvand **Laovarud**.
1. Valige **Laovarude** menüüs **Juhendatud tsükliline inventuur**.
1. Valige väli **Kogus**, sisestage *9* kasutades numbriklahvistikku ja valige seejärel **OK** (märkeruudu nupp).
1. Süsteem ootas, et sisestate selle kauba, asukoha ja numbrimärgi jaoks 10 tükki. Seetõttu palutakse teil uuesti lugeda. Valige väli **Kogus**, sisestage *9* uuesti kasutades numbriklahvistikku ja valige seejärel **OK** (märkeruudu nupp). Teisel katsel arvestatakse teie inventuuri tulemust.

    > [!NOTE]
    > Kui süsteem tuvastas erinevuse eeldatava vaba kaubavaru koguse ja sisestatud koguse vahel, palutakse teil teine kord loendada, kuna **juhendatud tsüklilise inventuuri** mobiilse seadme menüükäsu puhul on *katsete arvu* välja väärtuseks seatud **1**. Teid juhendati konkreetse kaubakoodi ja litsentsiplaadi numbriga, kuna nii suvand **Kuva kauba number** kui ka **Kuva litsentsiplaat** on mobiilse seadme menüü-üksuse puhul seatud väärtusele *Jah*.

1. Valige **OK** (märkenupp).

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a>Tsüklilise inventuuri erinevuste ülevaatamine stsenaariumi 1 puhul

Järgige neid samme tsüklilise inventuuri erinevuste ülevaatamiseks.

1. Naaske rakendusse Supply Chain Management.
1. Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.
1. Otsige ja valige tsüklilise inventuuri töö, mida varem vaatasite. (Näiteks seadistage filter veerul **Töökausta ID**, et leida kirjed, mille väärtus on *CycleCount*.) Pange tähele, et selle **töö oleku** väli on nüüd seatud olekule *Ootel ülevaade*.

    > [!NOTE]
    > Töö kasutajakonto puhul, mida kasutasite inventuuritöö jaoks, on **tsüklilise inventuuri ülevaataja** suvandiks *Ei* ja **maksimaalse protsendi piirang**, **maksimaalse koguse piirang** ja **maksimumväärtuse piirang** väljade väärtuseks on kõik seatud *0* (null). Seega peavad kõik inventuuri erinevused, mida see kasutajaaruanne käsitsi kinnitab ja seotud **töö oleku** väli on seatud olekusse *Ootel ülevaatus*. Kui loendatud väärtus jääb hälbe piiridesse (määratud lehel **Töö kasutajad** kas **maksimaalse protsendipiirangu** või **maksimaalse kogusepiirangu** väljadel), või kui **tsüklilise inventuuri ülevaataja** suvand on kasutajale seatud väärtusele *Jah*, oleks töö automaatselt suletud.

1. Toiminguriba vahekaardil **Töö** valige suvand **Tsükliline inventuur**.
1. Valige toimingupaanil **Kinnita inventuur**.

    Erinevus sisestatakse standardse inventuuri töölehe abil ja luuakse uus töötellimus.

1. Valige tegevuspaani lehel **Tsüklilise inventuuri kanded** suvand **Tuletatud töö**, et leida kinnitatud erinevuse jaoks loodud töö.

## <a name="scenario-2-blind-cycle-counting"></a>2. stsenaarium: tsükliline pimeinventuur

See stsenaarium nõuab, et teie süsteemis oleks 1. stsenaarium juba lõpetatud.

### <a name="create-cycle-counting-work-for-scenario-2"></a>2. stsenaariumi tsüklilise inventuuritöö loomine

Enne tsüklilist pimeinventuuri peate looma mõne töö. Järgige neid samme, et luua tsüklilise inventuuri töö kauba asukohale *01A02R2S2B* (BULK-06) laos *61*.

1. Minge jaotisse **Laohaldus \> Tsükliline inventuur \> Tsüklilise inventuuri töö kauba järgi**.
1. Seadke dialoogiboksis **Tsüklilise inventuuri töö loomine kauba järgi** välja **Töökausta ID** väärtuseks *CycleCount*.
1. Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**.
1. Lisage päringuredaktori dialoogiboksis vahekaardile **Vahemik** kolm rida, millel on järgmised sätted.

    - Rida 1:

        - **Tabel:** *Kaubad*
        - **Väli:** *Kaubakood*
        - **Kriteeriumid:** *L0101*

    - Rida 2:

        - **Tabel:** *Varude dimensioonid*
        - **Väli:** *Ladu*
        - **Kriteeriumid:** *61*

    - Rida 3:

        - **Tabel:** *Varude dimensioonid*
        - **Väli:** *Asukoht*
        - **Kriteeriumid:** *01A02R2S2B*

1. Päringuredaktori dialoogiboksi sulgemiseks valige **OK**.
1. Valige **OK**, et sulgeda dialoogiboks **Tsüklilise inventuuri töö loomine kauba järgi**.

    Kui töö loomise protsess on lõpetatud, kuvatakse teile teade.

### <a name="do-cycle-counting-work-for-scenario-2"></a>2. stsenaariumi tsüklilise inventuuritöö teostamine

Pärast tsüklilise inventuuri töö loomist järgige neid samme, et teha töö mobiilirakenduses Warehouse Management.

1. Logige laohalduse mobiilirakenduse sisse töö kasutajana, [mille seadistasite selles artiklis varasema stsenaariumite](#prepare-demo-data) jaotises Demoandmete ettevalmistamine. Selles artikli näites on kasutaja nimeks *The Funderburk* ja seadistatud laole *61*. (USMF-i demoandmed peaksid lubama teil sisse logida selle töö kasutajana, sisestades *61* kasutaja ID-na ja *1* parooliks.)
1. Valige peamenüüs suvand **Laovarud**.
1. Valige **Laovarude** menüüs **Tsükliline pimeinventuur**.
1. Valige väli **Tsooni ID**, sisestage *BULK06* ja seejärel valige **OK** (märkeruudu nupp).
1. Valige väli **Kaup**, sisestage *L0101* ja seejärel valige **OK** (märkeruudu nupp).
1. Valige väli **Litsentsiplaat**, sisestage *LP\_BULK\_06\_01* ja seejärel valige **OK** (märkeruudu nupp).
1. Valige väli **Kogus**, sisestage *10* ja seejärel valige **OK** (märkeruudu nupp).

    > [!NOTE]
    > Kuigi süsteem tuvastas erinevuse eeldatava vaba kaubavaru koguse ja skannitud koguse vahel, ei palutud teil teine kord loendada, kuna **tsükliline pimeinventuur** mobiilse seadme menüükäsu puhul on *katsete arvu* välja väärtuseks seatud **0** (null). Teid paluti skannida kaubakoodi number ja litsentsiplaat, kuna nii suvand **Kuva kauba number** kui ka **Kuva litsentsiplaat** on mobiilse seadme menüü-üksuse puhul seatud väärtusele *Ei*.

1. Valige **OK** (märkenupp).

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a>Tsüklilise inventuuri erinevuste ülevaatamine stsenaariumi 2 puhul

Järgige neid samme tsüklilise inventuuri erinevuste ülevaatamiseks.

1. Naaske rakendusse Supply Chain Management.
1. Minge **Laohaldus \> Tavaline \> Töö \> Ülevaatuse ootel tsüklilise inventuuri töö**.
1. Toiminguriba vahekaardil **Töö** valige suvand **Tsükliline inventuur**.
1. Valige toimingupaanil **Lükka inventuur tagasi**.

    Kuna inventuuri erinevus lükati tagasi, on töö suletud.

## <a name="scenario-3-spot-cycle-counting"></a>3. stsenaarium: tsükliline punktinventuur

Vaba kaubavaru kirjes on määratud, et kauba *L0101* vaba kogus on asukohas *01A02R2S2B*. Laotöötaja on asukohas *01A02R2S1B*. Kuigi see asukoht peab olema tühi, on see täis. Seega teeb laotöötaja kohe selle asukoha punktinventuuri.

### <a name="do-cycle-counting-work-for-scenario-3"></a>3. stsenaariumi tsüklilise inventuuritöö teostamine

Järgige neid samme, et teha tsüklilise inventuuri töö mobiilirakenduses Warehouse Management.

1. Logige laohalduse mobiilirakenduse sisse töö kasutajana, [mille seadistasite selles artiklis varasema stsenaariumite](#prepare-demo-data) jaotises Demoandmete ettevalmistamine. Selles artikli näites on kasutaja nimeks *The Funderburk* ja seadistatud laole *61*. (USMF-i demoandmed peaksid lubama teil sisse logida selle töö kasutajana, sisestades *61* kasutaja ID-na ja *1* parooliks.)
1. Valige peamenüüs suvand **Laovarud**.
1. Valige **Laovarude** menüüs **Tsükliline punktinventuur**.
1. Valige väli **Asukoht**, sisestage *01A02R2S1B* ja seejärel valige **OK** (märkeruudu nupp).

    Süsteem tuvastab, et asukoht on rakenduses Supply Chain Management tühi.

1. Valige käsk **Lisa LP või Kaup**.
1. Valige väli **Kaup**, sisestage *L0101* ja seejärel valige **OK** (märkeruudu nupp).
1. Valige väli **Litsentsiplaat**, sisestage *LP\_BULK\_06\_01* ja seejärel valige **OK** (märkeruudu nupp).
1. Valige väli **Kogus**, sisestage *9* ja seejärel valige **OK** (märkeruudu nupp).

    Kuna süsteem tuvastab, et määratud numbrimärk on rakenduse Supply Chain Management mõnes teises kohas juba saadaval, viiakse see numbrimärk praegusesse asukohta. Seetõttu palub süsteem teil kinnitada liikumise.

1. Valige **OK** (märkenupp).

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a>Tsüklilise inventuuri erinevuste ülevaatamine stsenaariumi 3 puhul

Järgige neid samme inventuuri tulemuste ülevaatamiseks.

1. Naaske rakendusse Supply Chain Management.
1. Avage jaotis **Laohaldus \> Tavaline \> Töö üksikasjad**.
1. Märkige ruudustiku ülaosas ruut **Kuva suletud**.
1. Seadke **töötellimuse tüübi** veeru filter väärtusele *Laovarude liikumine*.

    Süsteem tuvastas selle inventuuri automaatselt laovarude liikumisena. See liikumine on lubatud, kuna suvand **Tsüklilise inventuuri ajal litsentsiplaadi teisaldamise lubamine** on lehel *Laod* laole *61* määratud valikule **Jah**.

## <a name="scenario-4-define-cycle-count-thresholds"></a>4. stsenaarium: tsüklilise inventuuri lävede määratlemine

Üks viis tsüklilise inventuuri töö loomiseks on kasutada lävesid. Tsüklilise inventuuri lävi näitab laokaupade koguse või protsendi piirangut. Tsüklilise inventuuri töö luuakse läveni jõudmisel automaatselt.

Näiteks on 60 kaupa asukohas, mille tsüklilise inventuuri läve kogus on 40. Müügitellimuse kande käigus komplekteeritakse asukohast 25 kaupa ja need paigutatakse vaheasukohta. Kuna uus kaupade arv 35 on lävekogusest väiksem, luuakse asukohas automaatselt tsüklilise inventuuri töö.

Tsüklilise inventuuri lävede seadistamiseks toimige järgmiselt.

1. Avage **Laohaldus \> Seadistus \> Tsükliline inventuur \> Tsüklilise inventuuri läved**.
1. Valige toimingupaanil **Uus**, et luua lävi ja määrake sellele järgmised väärtused.

    - **Tsüklilise inventuuri läve ID:** *L0101*
    - **Kirjeldus:** *lävi L0101*
    - **Piirmäära kogus:** *2*
    - **Ühik:** *ea*
    - **Võimsuse lävi protsentuaalselt:** *0,00*
    - **Tsüklilise inventuuri läve tüüp:** *kogus*
    - **Töötle tsükli inventuuri koheselt:** *jah*
    - **Päevi tsükliliste inventuuride vahel:** *1*
    - **Töökausta ID:** *CycleCount*

1. Toimingupaanil valige käsk **Vali kaubad**.
1. Otsige päringu redaktori dialoogiboksi vahekaardil **Vahemik** üles rida, kus välja **Väli** väärtuseks on seatud *Kauba number*. Määrake selle rea välja **Kriteeriumid** väärtuseks *L0101*.
1. Päringuredaktori dialoogiboksi sulgemiseks valige **OK**.

    Olete nüüd määranud tsüklilise inventuuri läve kaubale *L0101*.

Tsükliline inventuur luuakse kaubale *L0101* igas asukohas, kui vaba kaubavaru kogus on väiksem kui 2 ja asukoha viimase tsüklilise inventuuri kuupäev pole täna.

## <a name="scenario-5-define-cycle-count-plans"></a>5. stsenaarium: tsüklilise inventuuri plaanide määratlemine

Tsüklilise inventuuri plaanid lasevad teil automatiseerida tsüklilise inventuuri töö loomist. Iga tsüklilise inventuuri plaani saate seadistada kindlate kauba- ja asukohapäringutega. Pakett-töö käitamisel loob see tsüklilise inventuuri töö kõigi asukohtade jaoks, mis vastavad kauba ja asukoha kriteeriumidele (plaani jaoks määratud maksimaalse inventuuride arvuni). Kui tsüklilise inventuuri töö on loodud, sisaldab inventuuri töö rida teavet inventuuri asukoha kohta, mille kohta peab inventuuri tegema. Selle asukohaga seotud vaba kaubavaru pole blokeeritud. Seetõttu on see saadaval reserveerimise ja väljamineva töötlemise jaoks, kuigi esineb avatud inventuuritöö.

Tsüklilise inventuuri plaani seadistamiseks toimige järgmiselt.

1. Avage **Laohaldus \> Seadistus \> Tsükliline inventuur \> Tsüklilise inventuuri plaanid**.
1. Valige toimingupaanil **Uus**, et lisada rida jaotise ruudustikku ja seejärel määrake sellele järgmised väärtused:

    - **Tsüklilise inventuuri plaani ID:** *BULK06*
    - **Kirjeldus:** *BULK06 asukoha loendamine*
    - **Töökausta ID:** *CycleCount*
    - **Tsükliliste inventuuride maksimumarv:** *10*
    - **Päevi tsükliliste inventuuride vahel:** *10*
    - **Tühjad asukohad:** *välja jätta tühjad*
    - **Töömall:** jätke see väli tühjaks.

1. Toimingupaanil valige käsk **Vali asukohad**.
1. Kuvatakse standardne päringu redaktori dialoogiaken. Lisage vahekaardil **Vahemik** rida ja määrake sellele järgmised väärtused:

    - **Tabel:** *Asukohad*
    - **Väli:** *Tsooni ID*
    - **Kriteeriumid:** *BULK06*

1. Päringuredaktori dialoogiboksi sulgemiseks valige **OK**.
1. Valige toimingupaanil **Tsüklilise inventuuri plaani protsessimine**.
1. Valige dialoogiboksis **Tsüklilise inventuuri plaanid** kiirkaardil **Käivita taustal** suvandi **Pakktöötlus** väärtuseks *Jah*.
1. Valige **kordumine**.
1. Seadistage dialoogiboksis **Kordumise määratlemine** pakett-töö nii, et see alustaks kohe ja käivituks kord iga minuti järel ning lõppkuupäev puudub.
1. Valige dialoogiboksi **Korduse defineerimine** sulgemiseks **OK**.
1. Valige dialoogiboksi **Tsüklilise inventuuri plaanid** sulgemiseks **OK**.

    Teade teavitab teid, et töö lisati pakett-töö järjekorda.

1. Minge **Laohaldus \> Üldine \> Tsüklilise inventuuri ajastamine**. Plaan algab kohe ja loob inventuuritöö. Kuna inventuuritöö on lõpetamata, on välja **Olek** väärtuseks seatud *Lõpetamata*. Ühe minuti pärast muutub veeru **Kogu tsükliline inventuur** väärtuseks *1*.

    > [!NOTE]
    > Tsüklilise inventuuri tööd ei looda, kui päevade arv pärast viimast tsükli inventuuri on väiksem kui väärtus, mis on seadistatud tsüklilise inventuuri plaani välja **Päevi tsüklilise inventuuri vahel**. Näiteks kui väljale **Päevi tsükliliste inventuuride vahel** sisestatud *5*, luuakse tsüklilisi inventuure iga viie päeva järel. Kuid kui tsüklilise inventuuri töö töödeldakse 3. päeval, luuakse järgmine tsüklilise inventuuri töö viis päeva pärast viimase tsüklilise inventuuri töö töötlemist, 8. päeval.

1. Tegevuspaanil valige **Töö** loodud inventuuritöö vaatamiseks.
