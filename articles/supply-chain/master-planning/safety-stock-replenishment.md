---
title: Kaupade puhvervaru täitmine
description: Selles teemas käsitletakse kaupade puhvervaru täitmist ja puhvervarukoguse seadistamist.
author: t-benebo
ms.date: 8/23/2021
ms.topic: article
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended, ReqSafetyKeyDefaultDataWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: c539b804198ddc5d5dac52c958a851ee55116711
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672062"
---
# <a name="safety-stock-fulfillment-for-items"></a>Kaupade puhvervaru täitmine

[!include [banner](../includes/banner.md)]

Puhvervaru näitab kauba laost otsa saamise riski vähendamiseks laos hoitavat kauba lisakogust. Puhvervaru kasutatakse, et tagada turvaline puhver juhuks, kui müügitellimusi tuleb, kuid tarnija ei suuda kliendi soovitud lähetuskuupäevaks lisakaupu tarnida. Kui puhvervaru kasutatakse müügitellimuse täitmiseks, siis seda vähendatakse. Koondplaneerimisega saate varudele automaatselt piisava puhvri tagasi arvestada.

## <a name="set-up-safety-stock-levels-for-items"></a>Kaupade puhvervaru tasemete seadistamine

Puhvervaru seadistatakse kauba laovarude osana lehel **Kauba laovarud**, avades **Väljastatud tooted \> Planeerimine \> Laovarud**.

Sisestage puhvervaru tase, mida soovite kauba kohta säilitada, väljale **Miinimum**. Väärtus on väljendatud laoühikutes. Kui jätate välja tühjaks, on vaikeväärtuseks null. See väli on saadaval, kui valite loendist **Planeerimise kood** kas valiku **Periood**, **Vajadus** või **Min/max**. Puhvervaru taseme kvoot kehtib saadaolevatele varudele, mis tähendab, et reserveerimised ja märgistused võivad põhjustada puhvervarude täiendamise enne, kui kauba füüsiline kogus väheneb alla määratud minimaalse taseme.

> [!NOTE]
> Enne kui saate määrata välja **Miinimum** dimensioonid, peate määrama kõik teised laovarude plaanimise dimensioonid. See takistab koondplaneerimise käigus kehtetu kirje kasutamist. Selline olukord võib tekkida, kui näiteks dimensioonigruppi on laiendatud täiendava laovarude plaanimise dimensiooniga, mille jaoks ei ole veel määratud minimaalseid ja maksimaalseid varude koguseid.

Nõudluse hooajaliste kõikumiste arvestamiseks saate kasutada varunormide kordajaid. Näiteks saate hooajavälisel ajal kaubavarude minimaalset taset alandada ja seejärel seda muudel kuudel järk-järgult tõsta. Miinimum kordaja loomiseks avage **Koondplaneerimine \> Seadistamine \> Laovarud \> Miinimum/maksimum võti**. Hooajalise puhvervaru taseme korrigeerimiseks määrake varunormide kordaja väljal **Varunormide kordaja** lehel **Kauba laovarud**.

## <a name="example-minimum-key"></a>Näide: varunormide kordaja

Järgnev toiming on näide selle kohta, kuidas seadistada miinimumvõtit, mis kuvab suurenenud hooajalise nõudluse hooaja- ja suvekuudel.

1. Valige **Koondplaneerimine \> Seadistus \> Laovarud \> Miinimum/maksimum võtmed**.
1. Miinimum/maksimum võtme loomiseks valige **Uus**.
1. Sisestage väljale **Miinimum- või maksimumvõti** võtme ID. Sisestage võtme nimi väljale **Nimi**.
1. Seadistage suvand **Kasuta kehtivuskuupäeva** väärtusele *Jah* ja jätke väli **Kehtivuskuupäev** tühjaks, et muuta võti kehtivaks alates praeguse aasta esimesest päevast.

    > [!NOTE]
    > Sätete **Kasuta jõustumiskuupäeva** ja **Efektiivse kuupäeva** kombineerimine määratleb kuupäeva, millest alates võti kehtib.
    >
    > - Kui suvand **Kasuta jõustumiskuupäeva** on seatud valikule *Ei*, kehtib võti alates praegusest kuupäevast või süsteemikuupäevast.
    > - Kui suvand **Kasuta jõustumiskuupäeva** on seatud väärtusele *Jah*, kehtib võti alates kuupäevast, mis on määratletud väljal **Efektiivne kuupäev**.

1. Looge jaotises **Perioodid** 12 rida ja seadke neile järgmised väärtused:

    - **Muutmine** - Määrake igale reale kordumatu number 1-st 12-ni. See väli näitab järkjärgulist muutust ajaühikus, mille määrab väli **Ühik**.
    - **Ühik** - Valige *Kuud* iga rea jaoks.
    - **Alguskuupäev**, **Lõpkuupäev** ja **Kuud** - Need väljad seatakse automaatselt **Muutuse** ja **Ühik** sätete alusel. Igakuised perioodid algavad käesoleva aasta esimesest päevast.
    - **Tegur** - Sisestage väljale väärtused, mida kirjeldatakse järgmises tabelis. See väli määratleb teguri, millega soovite minimaalset laovaru korrutada.

        | Rida (Muutus) | Tegur | Tulemus |
        |---|---|---|
        | 1–3 | 1 | Minimaalsed varud põhinevad lehel **Kauba laovarud** jaanuarist märtsini määratud seadistusel. |
        | 4–5 | 2 | Aprilli ja mai puhul korrutatakse minimaalne kaubavaru teguriga 2. |
        | 6–8 | 2.5 | Minimaalne kaubavaru korrutatakse teguriga 2,5 perioodi juuni kuni august puhul. |
        | 9–12 | 1 | Perioodiks septembrist detsembrini pöördub minimaalne kaubavaru tagasi seadistuse juurde lehel **Kauba laovarud**. |

    Teie sätted peaksid nüüd sarnanema järgmise illustratsiooni sätetega.

    ![Minimaalsed või maksimaalsed võtmeperioodid.](media/min-max-key-periods.png "Minimaalsed või maksimaalsed võtmeperioodid")

> [!NOTE]
> Minimaalse/maksimaalse võtme loomiseks võite kasutada ka viisardit. **Minimaalse/maksimaalse võtmete** lehel toimingupaanil valige **viisard** et avada viisardi **Miinimum/maksimumvõtmed**. Viisard juhendab teid samm-sammult läbi miinimum-/maksimumvõtme loomise ja seadistamise protsessi.

Kui laovarude kood on *Min/max*, saate määrata ka maksimaalse varude koguse, mida soovite kauba puhul säilitada. Väärtus on väljendatud ka laoühikutes. Kui plaanitud saadaolev laovaru langeb alla minimaalse koguse, luuakse koondplaneerimisel – pärast mis tahes teiste avatud vajaduste täitmist – plaanitud tellimus laotaseme tõstmiseks määratud maksimaalse koguseni. Nii nagu minimaalse varude koguse seadistamisel, peate enne välja **Maksimaalne** seadmist määrama kõik muud planeeritud laovarude dimensioonid.

## <a name="example-minmax-coverage-code"></a>Näide: min/max kattekood

Miinimumkogus on 10 ja maksimumkogus on 15. Praegune vaba kaubavaru on 4. Seega on minimaalne nõutav kogus 6. Ent kuna maksimaalne kogus on 15, loob koondplaneerimine plaanitud tellimuse 11 kaubaühikuga.

Hooajalisest nõudlusest olenevate kaupade puhul peate säilitama eri maksimaalsed tasemed. Selleks peate määrama **Maksimaalse võtme** minnes **Koondplaneerimine \> Seadistamine \> Laovarud \> Miinimum/maksimum võtmed**. Täitke väli **Varunormide kordaja** lehel **Kauba laovarud**. Varunormide kordajate kaudu määratud puhvervaru tasemete kohta saate teavet lehe **Kauba laovarud** vahekaardilt **Min/max**. Veenduge, et teatud perioodiks määratud miinimum- ja maksimumväärtused oleks sünkroonitud.

## <a name="safety-stock-fulfillment"></a>Puhvervaru täitmine

Parameetriga **Täida minimaalselt** saate valida kuupäeva või ajavahemiku, mille puhul laovarude tase peab vastama väljal **Miinimum** määratud kogusele. See väli on saadaval, kui valite loendist **Planeerimise kood** kas valiku **Periood**, **Vajadus** või **Min/max**.

Kui kasutate **varunormide kordajaid**, märkige ruut **Miinimumperioodid** minimaalse laovarude taseme täitmiseks kõigil varunormide kordaja kohta seadistatud perioodidel. Kui jätate selle ruudu tühjaks, täidetakse minimaalne laovaru ainult praeguseks perioodiks.

Alljärgnev stsenaarium näitab, kuidas see parameeter töötab ja millised on selle väärtuste vahelised erinevused.

> [!NOTE]
> Kõigi selles teemas toodud graafikute x-telg tähistab varusid, y-telg päevi, tulbad varude taset, nooled kandeid, nagu näiteks müügitellimuse read, ostutellimuse read, või plaanitud tellimused.

[![Tavastsenaarium kaupade puhvervaru täitmiseks.](media/Scenario1.png)](media/Scenario1.png)

**Minimaalse täitmise** parameetri väärtused võivad olla järgmised:

### <a name="todays-date"></a>Tänane kuupäev

Määratud miinimumkogus saavutatakse koondplaneerimise käitamise kuupäeval. Süsteem püüab puhvervaru kvoodi võimalikult kiiresti täita, kuigi see võib täitmisaja tõttu ebarealistlik olla.

[![Tänase kuupäeva nõue.](media/TodayReq.png)](media/TodayReq.png)

Tänase kuupäevaga vajadus Plaanitud tellimus P1 luuakse tänase kuupäevaga, et saadaolevad varud ületaks puhvervaru taseme sellel kuupäeval. Müügitellimuse read S1–S3 vähendavad endiselt kaubavarude taset. Koondplaneerimises luuakse plaanitud tellimused P2–P4, et taastada pärast iga müügitellimuse vajaduse täitmist varude tase puhvri kvoodini.

Kui kasutate kattekoodi **Vajadus**, luuakse mitu plaanitud tellimust. Nõutumate kaupade ja materjalide täiendamiste koondamiseks on soovitatav kasutada kas kattekoodi **Periood** või **Min/max**. Alljärgnev graafik illustreerib kattekoodi **Periood** kasutamist.

[![Periood. Tänane kuupäev.](media/TodayPeriod.png)](media/TodayPeriod.png)

Alljärgneval graafikul on näidatud kattekoodi **Min/max** näide.

[![Min/Max. Tänane kuupäev.](media/TodayMinMax.png)](media/TodayMinMax.png)

### <a name="todays-date--procurement-time"></a>Tänane kuupäev + tarneaeg

Määratud miinimumkogus saavutatakse kuupäeval, mis saadakse, kui lisada koondplaneerimise käituskuupäevale ostu või tootmise täitmisaeg. See aeg sisaldab mis tahes ohutuspiire. Kui kauba kohta on olemas kaubanduslepe ja lehel **Koondplaneerimise parameetrid** on märgitud ruut **Otsi kaubandusleppeid**, siis kaubandusleppe tarne täitmisaega ei arvestata. Täitmisajad võetakse kauba laovarude sätetest või kaubalt.

See täitmisrežiim loob plaane, milles on vähem viivitusi ja plaanitud tellimusi, olenemata kaubale määratud laovarude grupist.

Alljärgneval graafikul on kujutatud plaani tulemusi, kui kattekood on kas **Vajadus** või **Periood**.

[![Vajadus või Periood. Tänane kuupäev ja täitmisaeg.](media/TodayPLTReq.png)](media/TodayPLTReq.png)

Alljärgneval graafikul on kujutatud plaani tulemusi, kui kattekood on **Min/max**.

[![Min/max. Tänane kuupäev ja täitmisaeg.](media/TodayPLTMinMax.png)](media/TodayPLTMinMax.png)

### <a name="first-issue"></a>Esimene väljaminek

Määratud miinimumkogus saavutatakse kuupäeval, kui saadaolevad laovarud vähenevad alla minimaalse taseme, nagu on näha alljärgneval graafikul. Isegi kui saadaolevad varud on koondplaneerimise käituskuupäeval minimaalsest tasemest madalamad, ei püüa funktsioon **Esimene väljaminek** varusid enne järgmise vajaduse tulekut katta.

Alljärgneval graafikul on näidatud kattekoodi **Vajadus** kasutamist.

[![Kauba planeerimine kattekoodiga Vajadus ja Esimene väljaminek täitmisega.](media/FirstIssueReq.png)](media/FirstIssueReq.png)

Alljärgnev graafik illustreerib kattekoodi **Periood** kasutamist.

[![Kauba planeerimine kattekoodiga periood ja esimese väljamineku täitmisega.](media/FirstIssuePeriod.png)](media/FirstIssuePeriod.png)

Alljärgneval graafikul on näidatud kattekoodi **Min/max** näide.

[![Kauba planeerimine kattekoodiga MinMax ja esimese väljamineku täitmisega.](media/FirstIssueMinMax.png)](media/FirstIssueMinMax.png)

Kui saadaolevad varud on koondplaneerimise käituskuupäeval allpool puhvervaru kvooti, käitavad funktsioonid **Tänane kuupäev** ja **Tänane kuupäev + tarneaeg** kohe varude täiendamise. Funktsioon **Esimene väljaminek** ootab kauba muu väljaminekukandeni, nagu müügitellimuse ja kooslusrea nõue, ning käitab täiendamise sel kuupäeval.

Kui koondplaneerimise käituskuupäeval on saadaolevad varud allpool puhvervaru kvooti, annavad funktsioonid **Tänane kuupäev** ja **Esimene väljaminek** täpselt sama tulemuse, nagu on näidatud järgmisel graafikul.

[![Ei ole limiidi all.](media/ReqFirstIssue.png)](media/ReqFirstIssue.png)

Kui koondplaneerimise käituskuupäeval pole saadaolevad varud allpool puhvervaru kvooti, annab funktsioon **Tänane kuupäev + tarneaeg** järgmise tulemuse, kuna see lükkab täitmise hanke täitmisaja lõppu.

![Täitmine on edasi lükatud hanke täitmisaja lõpuni.](media/ReqTodayLT.png)

### <a name="coverage-time-fence"></a>Laovarude ajapiir

Määratud miinimumkogus saavutatakse väljal **Laovarude ajapiir** määratud ajaperioodi jooksul. See suvand on kasulik, kui koondplaneerimine ei luba puhvervaru taseme säilitamise eesmärgil saadaolevate varude kasutamist tegelike tellimuste, nt müügi või kannete puhul. Tulevases väljaandes pole seda täiendamisrežiimi siiski enam vaja ja see suvand aegub.

## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>„Esimesena aegunud esimesena välja” (FEFO) kaupade puhvervaru täiendamise planeerimine

Mis tahes hetkel kasutatakse tegeliku nõudluse, nagu müügiridade või kooslusridade FEFO („esimesena aegunud esimesena välja”) tellimuse täitmiseks hiliseima aegumiskuupäevaga puhvervaru.

Nägemaks, kuidas see töötab, vaadake järgmist stsenaariumit.

[![FEFO stsenaarium.](media/FEFOScenario.png)](media/FEFOScenario.png)

Planeerimise käitamisel katab see esimese müügitellimuse olemasolevast vabast kaubavarust ja täiendava ostutellimuse järelejäävast kogusest.

[![FEFO 1.](media/FEFO1.png)](media/FEFO1.png)

Luuakse plaanitud tellimus tagamaks, et saadaolevad varud ületavad puhvervaru kvoodi.

[![FEFO 2.](media/FEFO2.png)](media/FEFO2.png)

Kui plaanitakse teist müügitellimust, kasutakse selle koguse katmiseks varem loodud plaanitud tellimust, mis katab puhvervaru. Seega on puhvervaru pidevalt ringluses.

[![FEFO 3.](media/FEFO3.png)](media/FEFO3.png)

Lõpuks luuakse puhvervaru katmiseks teine plaanitud tellimus.

[![FEFO 4.](media/FEFO4.png)](media/FEFO4.png)

Kõik partiid aeguvad vastavalt ja puhvervaru uuesti täitmiseks luuakse pärast puhvervaru aegumist plaanitud tellimused.

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>Kuidas koondplaneerimine puhvervaru piirangut käsitleb?

Puhvervaru jälgitakse süsteemis vajaduse tüübina, nagu müügiridu või koosluse nõudeidki. Puhvervaru vajaduse rida näite lehel **Netonõuded**, kui eemaldate veerust **Nõude tüüp** vaikefiltri.

Puhvervaru nõudekande täitmine kaotab oma tähtsuse, kui süsteem tuvastab, et see põhjustab viivitusi tegeliku nõudluse täitmisel, nagu müügiridade, koosluse ridade, ülekandmisnõuete või nõudluse prognoosi ridade täitmisel. Muudel juhtudel on saadaolevate varude säilitamine ülalpool puhvervaru kogust samasuguse tähtsusega nagu teisedki vajaduse tüübid. See tagab viivitusteta tegelikud kanded ja aitab ennetada puhvervaru liigset ja varajast täiendamist.

Koondplaneerimise katvuse faasis ei deprioriseerita enam puhvervaru täiendamist. Enne mis tahes vajaduse tüüpi saab kasutada vaba kaubavaru. Viivituse arvutamisel lisatakse hilinenud müügiridade, kooslusridade nõuete ja kõigi muude nõudluse tüüpide ülevaatamisel uus loogika, et määrata, kas neid on võimalik puhvervaru kasutades õigeaegselt kätte toimetada. Kui süsteem tuvastab, et puhvervaru kasutamine võib viivitusi vähendada, siis asendatakse müügiridadel või koosluseridadel algne kate puhvervaruga ja süsteem käitab hoopis puhvervaru täiendamise.

Kui plaani või kauba jaoks pole seatud hilinemise arvutamist, siis on puhvervaru piirangul samasugune tähtsus nagu mis tahes muul nõudluse tüübil. See tähendab, et vaba kaubavaru ja muud saadaolevad varud on reserveeritud enne muid nõudluse tüüpe.

## <a name="additional-resources"></a>Lisaressursid

- [Puhvervaru abil üksuste minimaalse laovaru uuendamine](safety-stock-journal.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
