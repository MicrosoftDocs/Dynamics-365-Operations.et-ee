---
title: "Lähtesta finants aruandluse andmete mart pärast andmebaasi taastamine"
description: "Selles teemas kirjeldatakse lähtestamine finants aruandluse andmete mart pärast taastamist Microsoft Dynamics 365 operatsioonide andmebaasi."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Lähtesta finants aruandluse andmete mart pärast andmebaasi taastamine

Selles teemas kirjeldatakse lähtestamine finants aruandluse andmete mart pärast taastamist Microsoft Dynamics 365 operatsioonide andmebaasi. 

On mitu põhjust, kui peate oma Dynamics 365 operatsioonide andmebaasi varukoopia põhjal taastada või kopeerida andmebaasi teise keskkonda. Sel juhul peate järgima asjakohaseid meetmeid selle tagamiseks, et raamatupidamise aruandluse andmete mart õigesti kasutab taastatud Dynamics 365 operatsioonide andmebaasi. Küsimuste finants aruandluse andmete mart lähtestamise põhjus väljaspool Dynamics 365 operatsioonide andmebaasi taastamise kohta, vaadake selle [lähtestamine juhtimise Reporter andmete mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) lisateabe saamiseks. Pange tähele, et samme selles protsessis on toetatud Dynamics 365 operatsiooni mai 2016 pressiteade (App ehitada 7.0.1265.23014 ja finants aruandluse build 7.0.10000.4) ja uuematesse versioonidesse. Kui teil on mõni varasem versioon Dynamics 365 toiminguteks, võtke ühendust meie klienditoega abi.

## <a name="export-report-definitions"></a>Ekspordi aruanded
Esiteks eksportida aruande kujunduse asub Aruandekujundaja, tehes järgmist:

1.  Aruandekujundaja, minge **ettevõtte**&gt;**koosteüksuse sõprade**.
2.  Valige koosteüksuse eksportida, ja klõpsake **eksportida**. **Märkus:** Dynamics 365 toiminguteks, on toetatud ainult üks koosteüksuse rühma, **vaikimisi**.
3.  Valige aruande definitsioonid eksportida:
    -   Kõikide aruande definitsioonide ja seotud koosteüksuste eksportimiseks klõpsake suvandit **Vali kõik**.
    -   Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite eksportimiseks klõpsake vastavat vahekaarti ja valige eksporditavad üksused. Vahekaardil mitme üksuse valimiseks vajutage ja hoidke all klahvi Ctrl. Aruandeid eksportida valimisel valitakse seotud read, veerud, puud ja Dimensioonikogumid.

4.  Klõpsake **eksportida**.
5.  Sisestage faili nimi ja valige turvalises kohas, kuhu soovite salvestada eksporditud aruande mõisted.
6.  Click **Save**.

Faili saab kopeerida ega üles laadida turvalisse, võimaldades importida teises keskkonnas muul ajal. Teave Microsoft Azure storage konto kasutamise kohta leiate [AzCopy käsurea Utility andmete edastamiseks](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **Märkus:** Microsoft ei paku ladustamise konto Dynamics 365 osana toimingud kokkuleppe. Peate osta ladustamise konto või kasutage ladustamise konto eraldi Azure'i tellimus. **Tähtis:** käitumist juhtida D Azure'i virtuaalarvutite kohta teadma. Eksporditud koosteüksuse pakuvad siin püsivalt hoida. Ajutine draivi kohta lisateabe saamiseks vt [mõista ajutisele draivile Windows Azure'i virtuaalarvutite kohta](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Peatamine
Kaugtöölaua abil saate ühendada kõik arvutid keskkonnas ja peatada Windows services services.msc abil:

-   Veebis avaldamine (numbril kõikidele arvutitele)
-   Microsoft Dynamics 365 toimingute partii haldusteenus (linna-ja erasektori arvutitele ainult)
-   Protsessi haldusteenus Reporter 2012 (arvutites BI ainult)

Need teenused on avatud ühendusi Dynamics 365 operatsioonide andmebaasi.

## <a name="reset"></a>Lähtesta
#### <a name="locate-the-latest-dataupgradezip-package"></a>Leidke Viimane DataUpgrade.zip pakett

Leidke Viimane DataUpgrade.zip pakett kasutades leida juhiseid [lae DataUpgrade.zip skripti](..\migration-upgrade\upgrade-data-to-latest-update.md). Juhised selgitavad, kuidas andmete uuendamise pakett keskkonna jaoks õige versiooni leidmiseks.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Käivitada operatsioonide andmebaasi vastu Dynamics 365 skriptid

Järgmine skripte vastuolus Dynamics 365 operatsioonide andmebaasi (ole vastu finants aruandluse andmebaasi).

-   DataUpgrade.zip\\AosService\\skripte\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\skripte\\GrantAzViewChangeTracking.sql

Need skriptid tagada, et kasutajad, rollid ja muutuste jälituse seaded on õiged.

#### <a name="execute-powershell-command-to-reset-database"></a>PowerShelli käsu taastada andmebaasi

Käivitada järgmine käsk otse AOS-i arvuti lähtestamiseks integratsiooni Dynamics 365 operatsioonide ja aruandlus:

1.  Avage Windows PowerShelli administraatorina.
2.  Execute: F:
3.  Täita: F: cd\\MRApplicationService\\MRInstallDirectory
4.  Käivita: Import-moodul. \\Server\\MRDeploy\\MRDeploy.psd1
5.  Käivita: Reset-DatamartIntegration-põhjus muud - ReasonDetail "&lt;minu põhjus lähtestamine&gt;"
    -   Küsitakse "Y", et siseneda.

Parameetrite selgitus:

-   -Sobivad väärtused põhjus on: hooldus, BADDATA, teised.
-   -ReasonDetail parameeter on vabas vormis.
-   Põhjus ja reasonDetail fikseeritakse telemeetria/keskkonna monitooring.

## <a name="start-services"></a>Teenuste käivitamiseks
Kasutage services.msc varem protsessiteave teenuste taaskäivitamine:

-   Veebis avaldamine (numbril kõikidele arvutitele)
-   Microsoft Dynamics 365 toimingute partii haldusteenus (linna-ja erasektori arvutitele ainult)
-   Protsessi haldusteenus Reporter 2012 (arvutites BI ainult)

## <a name="import-report-definitions"></a>Importida aruanded
Importida mustreid aruande Report Designer loodud ajal ekspordi faili abil:

1.  Aruandekujundaja, minge **ettevõtte**&gt;**koosteüksuse sõprade**.
2.  Valige koosteüksuse eksportida, ja klõpsake **eksportida**. **Märkus:** Dynamics 365 toiminguteks, on toetatud ainult üks koosteüksuse rühma, **vaikimisi**.
3.  Valige selle **vaikimisi** plokk ja klõpsa **impordi**.
4.  Valige väljale märge mõisteid sisaldav fail ja klõpsake **avatud**.
5.  Valige dialoogiboksist Import imporditavad aruande definitsioonid.
    -   Kõikide aruande definitsioonide ja seotud koosteüksuste importimiseks klõpsake valikut **Vali kõik**.
    -   Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite importimiseks valige imporditavad aruanded, read, veerud, puud või dimensioonikogumid.

6.  Click **Import**.



