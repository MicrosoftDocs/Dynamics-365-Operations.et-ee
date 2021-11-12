---
title: Finantsperioodi sulgemise tööruum
description: Selles artiklis antakse ülevaade finantsperioodi sulgemise tööruumist ja sellega seotud konfiguratsioonist.
author: kweekley
ms.date: 11/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ab203a18229cd426f8483ed6d0483c98614af9c
ms.sourcegitcommit: 4f8465729d7ae0bf5150a2785a6140c984c7030e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/31/2021
ms.locfileid: "7727060"
---
# <a name="financial-period-close-workspace"></a>Finantsperioodi sulgemise tööruum

[!include [banner](../includes/banner.md)]

Selles artiklis antakse ülevaade **finantsperioodi sulgemise** tööruumist ja sellega seotud konfiguratsioonist.

Finantsperioodi sulgemise tööruum

Tööruum **Finantsperioodi sulgemine** võimaldab teil jälgida oma rahalise sulgemise protsessi ettevõtete, alade ja inimeste alusel. Olenevalt teie vaatest selle tööruumi **Finantsperioodi sulgemine** kohta, näete kas kõiki sulgemise graafiku ülesandeid ja olekuid või ainult teile määratud ülesandeid. 

Esmalt peate valima tööruumi ülaosas oleva sulgemise graafiku. Kõik tööruumis ilmuvad andmed filtritakse seejärel valitud sulgemise graafiku järgi.

### <a name="summary-tiles"></a>Kokkuvõttepaanid

Jaotise **Kokkuvõte** paanid annavad ülevaate protsessist ja näidikud aitavad teil sulgemise protsessi jälgida. Näete tähtaja ületanud ülesandeid, tänase puhul järelejäänud ülesandeid, tänase tähtajaga, kuid sõltuvuste tõttu blokeeritud ülesandeid ja kõiki protsessi ülejäänud ülesandeid. See teave puudutab kõiki valitud sulgemise graafikusse kaasatud ettevõtteid.

### <a name="tasks-and-status-section"></a>Ülesannete ja oleku jaotis

Jaotises **Ülesanded ja olek** jaotub üldise sulgemisgraafiku olek mitmel viisil: olek ettevõtte järgi, olek piirkonna järgi ja olek vastutava isiku järgi. Saate vaadata olekut sulgemise graafiku kõigi ülesannete, ainult tänase tähtajaga ülesannete või tähtaja ületanud ülesannete puhul, muutes kaardi loendi ülaosas oleva filtri. Konkreetse ettevõtte oleku vaatamiseks saate valida ka ettevõtte filtri. Iga oleku vahekaart annab jaotuse nii lõpetatud ülesannete protsendi kui ka järelejäävate ülesannete arvu järgi. Ülesannete üksikasjaliku loendi filtrimiseks valitud kaardi järgi klõpsake kaarti või tegevust **Kuva üksikasjad**. 

Viimane vahekaart on ülesannete üksikasjalikuks loendiks. See loend kuvab täieliku ülesannete loendi ja seda saab filtrida nii, et see kuvaks ainult ülesanded, millest olete huvitatud. Saate loendit filtrida mitmel viisil. Näiteks saate filtrida ülesande tähtaja, seotud ettevõtte ja seotud ala järgi. Saate valida ka lõpetatud ülesannete kuvamise või peitmise ülesannete loendis. 

Ülesannete puhul kasutatakse kahte järgmist näidikut.

-   Hüüumärgi ikoon näitab, et ülesanne on tähtaja ületanud. Tähtaja ületanud ülesannete puhul on tähtaeg ka punasega esile tõstetud.
-   Tabaluku ikoon näitab, et ülesanne sõltub teistest ülesannetest, mis pole veel lõpetatud. Sõltuvustega blokeeritud ülesannet ei saa lõpetatuks märkida. Saate ülesande sõltuvusi seadistada, kasutades tegevust **Sea sõltuvus**.

Ülesande nimi on hüperlink lehele, kuhu kasutaja peab töö lõpuleviimiseks minema. Saate selle hüperlingi seada, kasutades ülesande redigeerimisel või loomisel välja **Ülesande link**. 

Saate lisada ülesandele faile, märkuseid, pilte ja URL-e, kasutades tegevust **Manused**. Näiteks saate viidata selle ülesande osana kasutatavatele töölehe numbritele, lisada kindla ülesande kohta kommentaare või manustada ülesande puhul prinditud aruande faili. Ikoon kuvatakse manuse olemasolul ülesande veerus **Manus**. 

Suvand **Ülesanne on lõpetatud** tuleb pärast ülesande lõpetamist käsitsi valida. Kui ülesanne on lõpetatuks märgitud, värskendatakse väli **Lõpetamise kuupäev** automaatselt praegusele kuupäevale ja kellaajale. Vajaduse korral värskendatakse ka sõltuvuse näitajaid.

## <a name="all-financial-period-close-tasks-list-page"></a>Kõigi finantsperioodi sulgemisülesannete loendi leht
Saate vaadata kõiki praeguse ja eelmise perioodi sulgemise ülesandeid loendilehelt **Kõik finantsperioodi sulgemisülesanded**. Seda loendilehte on kõige parem kasutada sulgemisprotsessi ajaloo analüüsimiseks, kuna see sisaldab teavet plaanitud tähtaja, tegeliku lõpetamise kuupäeva ja ülesande lõpetanud isiku kohta. Selle loendilehe teavet saate aruandluseks ja auditeerimiseks eksportida hõlpsalt Microsoft Excelisse.

## <a name="financial-period-close-configuration-page"></a>Finantsperioodi sulgemiskonfiguratsiooni leht
Enne kui saate tööruumi **Finantsperioodi sulgemine** kasutada, peate protsessi konfigureerima, kasutades lehte **Finantsperioodi sulgemiskonfiguratsioon**. (Klõpsake valikuid **Pearaamat** &gt; **Perioodi sulgemine** &gt; **Finantsperioodi sulgemiskonfiguratsioon**.)

### <a name="resources"></a>Ressursid

Vahekaardil **Ressursid** saate määratleda sulgemisprotsessidesse kaasatud inimesed. Iga sulgemisülesande eest vastutav töötaja tuleb esmalt siin määrata. Peate määrama ka töötaja tööruumi vaate. Valikud on järgmised:

-   **Ainult määratud ülesanded** – kasutaja näeb ainult talle määratud ülesandeid.
-   **Kõik ülesanded ja olek** – kasutaja näeb kõiki sulgemisülesandeid ja üldise protsessi olekut.

Kasutajad, kellel on õigus vaadata ainult neile määratud ülesandeid, ei saa ülesandeid ülesannete loendisse lisada, neid redigeerida ega ülesannete loendist eemaldada.

### <a name="task-areas"></a>Ülesande alad

Kasutate ülesande alasid sulgemisülesannete grupeerimiseks teie organisatsiooni omandiõiguse loogilistesse aladesse. Näiteks võib ülesande aladena kasutada suvandeid Ostureskontro, Müügireskontro või Pearaamat.

### <a name="calendars"></a>Kalendrid

Saate luua ja redigeerida finantsilise sulgemise kalendreid, kasutades vahekaarti Kalendrid. Seal määratlete sulgemisprotsesside tööpäevad ja seda kasutatakse sulgemisülesannete plaanimisel.  Saate luua uue kalendri ja näidata ülesannete plaanimiseks kasutatavad tööpäevad.  Kalender on mõistlik luua pikaks ajaks, näiteks aastaks või mitmeks aastaks, kuna seda saab pärast loomist redigeerida.  Pärast kalendri loomist klõpsake kalendri kindlate päevade, nt pühade, värskendamiseks nuppu Redigeeri.  Sulgemisülesanded plaanitakse päevadele, mil valiku Kontroll väärtuseks on seatud Avatud.  Kui sulgemisülesandeid ei tohiks kindlale päevale plaanida, peaks selle päeva puhul valiku Kontroll väärtuseks olema seatud Suletud.

### <a name="templates"></a>Mallid

Finantsilise sulgemise malli abil saate määratleda kõik sulgemisprotsessi kuuluvad ülesanded. Sulgemisülesanne on korduv tööpanus, mis on määratud isikule lõpetamiseks iga sulgemisprotsessi osana. Mallis tuleb iga sulgemisülesande puhul määratleda suhteline tähtaeg. Suhteline tähtaeg on päevade arv enne või pärast määratletud perioodi lõppkuupäeva, millal on igal perioodil ülesande tähtaeg. Igale ülesandele määratakse ka tähtaja kellaaeg. Tähtaja kellaaeg seatakse teie ajavööndis ja teisendatakse iga kasutaja ajatsooni puhul. 

Saate määrata mallis oleva ülesande ühele või mitmele ettevõttele, kus ülesanne kehtib. Kui selle tööpanust on igas ettevõttes lõpetama määratud eri isik, võib osutuda kasulikuks sama tööpanuse puhul mitme ülesande loomine. Looge iga ettevõtte puhul üks ülesanne. 

Menüüelement **Ülesande link** on seostatud ülesande tööpanusega ja seda saab kasutada tööruumis ülesande lingilt otse seotud lehele liikumiseks. Näiteks saab valuuta ümberarvutamise protsessi käivitava sulgemisülesande ostureskontro puhul siduda seostatud lehega **Välisvaluuta ümberarvutamine**. Saate siduda ka välise URL-iga. 

> [!TIP]
> Kui soovite siduda kindla halduse aruandja aruande finantsperioodi sulgemisülesandega, saate kasutada aruande URL-i. Aruande URL-i juurde pääsemiseks avage aruandekujundaja ja klõpsake seejärel aruande avamiseks veebibrauseris suvandit **Fail** &gt; **Kuva aruanne**. Seejärel saate brauseri aadressiribalt URL-i kopeerida ja kleepida selle väljale **Ülesande link** **URL**. 

Saate määratleda malli ülesande sõltuvusi. Kui ülesanne on seadistatud sõltuma ühest või mitmest ülesandest, ei saa seda ülesannet lõpetatuks märkida, kuni kõik sõltuvused on lõpule viidud. 

Saate luua mitu finantsilise sulgemise malli. Seejärel saate kasutada eri malle sulgemisprotsesside jälgimiseks eri periooditüüpide puhul, nagu kuu või aasta lõpp, või erinevaid sulgemisprotsesse kasutavate ettevõtete jälgimiseks. Pärast ühe malli loomist saate selle kopeerida uude malli ja teha vajalikud muudatused. Saate igale sulgemise graafikule määrata ainult ühe malli.

### <a name="closing-schedules"></a>Sulgemisgraafikud

Saate kasutada sulgemise graafikut finantsilise sulgemise malli määramiseks kindlale finantsperioodile, mis tuleb sulgeda. Ülesanded luuakse mallist seejärel automaatselt määratud perioodi puhul ja uus sulgemise graafik lisatakse tööruumi. Uue sulgemise graafiku loomisel kasutatakse välja **Perioodi lõppkuupäev** sulgemisülesannete tegelike tähtaegade määramiseks finantsilise sulgemise mallis määratud suhtelise tähtaja põhjal. 

Määrake sulgemise graafiku puhul sobiv kalender, näitamaks ülesande plaanimisel kasutatavaid tööpäevi. Kui te konkreetset kalendrit ei määratle, kasutavad ülesande tähtaja kuupäevad kõiki nädalapäevi. 

Peate määratlema ka ettevõtted, mis sulgemise graafikuga seostatakse. Kui malli ülesanded on määratud mitmele ettevõttele, luuakse iga sulgemise graafikus oleva ettevõtte puhul eraldi ülesanded ja määratakse malli ülesandele. 

Pärast sulgemise graafiku lõpetamist valige selle puhul suvand **Suletud**. Ülesande ajalugu on endiselt saadaval loendilehel **Kõik finantsperioodi sulgemisülesanded**, kuid sulgemise graafik eemaldatakse tööruumist. Pärast sulgemise graafiku märkimist valikule **Suletud** ei saa te sellele ülesandeid lisada, ülesandeid redigeerida ega ülesandeid sellelt eemaldada.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
