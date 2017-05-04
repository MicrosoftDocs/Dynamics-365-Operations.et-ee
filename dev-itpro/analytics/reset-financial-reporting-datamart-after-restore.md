---
title: "Finantsaruandluse andmevaka lähtestamine pärast andmebaasi taastamist"
description: "Selles teemas kirjeldatakse, kuidas lähtestada finantsaruandluse andmevakka pärast Microsoft Dynamics 365 for Operationsi andmebaasi taastamist."
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

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Finantsaruandluse andmevaka lähtestamine pärast andmebaasi taastamist

Selles teemas kirjeldatakse, kuidas lähtestada finantsaruandluse andmevakka pärast Microsoft Dynamics 365 for Operationsi andmebaasi taastamist. 

On mitu stsenaariumi, mille korral võib olla vaja Dynamics 365 for Operationsi andmebaas varukoopiast taastada või kopeerida andmebaas teisest keskkonnast. Kui nii juhtub, siis tuleb teha sobivad toimingud tagamiseks, et finantsaruandluse andmevakk kasutaks taastatud Microsoft Dynamics 365 for Operationsi andmebaasi õigesti. Kui teil on küsimusi finantsaruandluse andmevaka lähtestamise kohta muul põhjusel peale Dynamics 365 for Operationsi andmebaasi taastamise, siis vaadake lisateavet jaotisest [Management Reporteri andmevaka lähtestamine](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/). Pange tähele, et selle protsessi etappe toetatakse Dynamics 365 for Operationsi 2016. aasta mai väljaandes (rakenduse järgus 7.0.1265.23014 ja finantsaruandluse järgus 7.0.10000.4) ja uuemates väljaannetes. Kui teil on Dynamics 365 for Operationsi varasem väljaanne, siis pöörduge abi saamiseks meie tugiteenuse töörühma poole.

## <a name="export-report-definitions"></a>Aruande definitsioonide eksportimine
Kõigepealt eksportige aruandekoosturis paiknevad aruandekujundused, tehes järgmist.

1.  Minge aruandekoosturis jaotisse **Ettevõte** &gt; **Koosteüksuste grupid**.
2.  Valige eksportimiseks koosteüksuste grupp ja klõpsake nuppu **Ekspordi**. **Märkus.** Dynamics 365 for Operationsi puhul toetatakse ainult ühte koosteüksuste gruppi: **Vaikeväärtus**.
3.  Valige eksportimiseks aruande definitsioonid.
    -   Kõikide aruande definitsioonide ja seotud koosteüksuste eksportimiseks klõpsake suvandit **Vali kõik**.
    -   Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite eksportimiseks klõpsake vastavat vahekaarti ja valige eksporditavad üksused. Vahekaardil mitme üksuse valimiseks vajutage ja hoidke all klahvi Ctrl. Eksporditavate aruannete valimisel valitakse seotud read, veerud, puud ja dimensioonikogumid.

4.  Klõpsake nuppu **Ekspordi**.
5.  Sisestage faili nimi ja valige turvaline asukoht, kuhu soovite eksporditud aruande definitsioonid salvestada.
6.  Klõpsake käsku **Salvesta**.

Faili saab kopeerida või laadida üles turvalisse asukohta, et selle saaks muul ajal teistsugusesse keskkonda importida. Teavet Microsoft Azure’i salvestuskonto kohta leiate jaotisest [Andmeedastus käsurea utiliidiga AzCopy](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **Märkus.** Microsoft ei paku Dynamics 365 for Operationsi lepingu raames salvestuskontot. Peate ostma salvestuskonto või kasutama eraldi Azure’i tellimuse salvestuskontot. **Oluline!** Olge kursis Azure’i virtuaalarvutite D-ketta käitumisega. Ärge hoidke sellel pidevalt eksporditud koosteüksuste gruppe. Lisateavet ajutiste ketaste kohta leiate jaotisest [Ajutine ketas Windows Azure’i virtuaalarvutites](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Teenuste peatamine
Kasutage kaugarvutit ühenduse loomiseks kõigi arvutitega keskkonnas ja peatage faili services.msc abil järgmised Windowsi teenused:

-   ülemaailmse veebi avaldamisteenus (kõigil AOS-i arvutitel)
-   Microsoft Dynamics 365 for Operationsi pakett-tööde halduse teenus (ainult mitteprivaatsetel AOS-i arvutitel)
-   Management Reporter 2012 protsessiteenus (ainult BI-arvutitel)

Nendel teenustel on avatud ühendus Microsoft Dynamics 365 for Operationsi andmebaasiga.

## <a name="reset"></a>Lähtesta
#### <a name="locate-the-latest-dataupgradezip-package"></a>Otsige üles uusim pakett DataUpgrade.zip

Otsige üles uusim pakett DataUpgrade.zip, kasutades juhiseid jaotises [Skripti DataUpgrade.zip allalaadimine](..\migration-upgrade\upgrade-data-to-latest-update.md). Juhistes selgitatakse, kuidas leida oma keskkonna jaoks õige andmete versioonitäienduse pakett.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Käivitage skriptid Dynamics 365 for Operationsi andmebaasi suhtes

Käivitage järgmised skriptid Dynamics 365 for Operationsi andmebaasi suhtes (mitte finantsaruandluse andmebaasi suhtes).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Need skriptid tagavad õiged kasutajad, rollid ja muudatuste jälgimise sätted.

#### <a name="execute-powershell-command-to-reset-database"></a>Käivitage andmebaasi lähtestamiseks PowerShelli käsk

Käivitage järgmine käsk otse AOS-i arvutil, et lähtestada Dynamics 365 for Operationsi ja finantsaruandluse integratsioon.

1.  Avage Windows PowerShell administraatorina.
2.  Käivitage: F:
3.  Käivitage: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Käivitage: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1
5.  Käivitage: Reset-DatamartIntegration -Reason OTHER -ReasonDetail „&lt;minu lähtestamise põhjus&gt;”
    -   Teil palutakse sisestada kinnitamiseks „Y”.

Parameetrite selgitus.

-   Parameetri -Reason sobivad väärtused on SERVICING, BADDATA, OTHER.
-   Parameeter -ReasonDetail on vaba tekst.
-   Parameetrid reason ja reasonDetail salvestatakse jaotisse telemeetria / keskkonna jälgimine.

## <a name="start-services"></a>Teenuste käivitamine
Taaskäivitage faili services.msc abil eelnevalt peatatud teenused.

-   ülemaailmse veebi avaldamisteenus (kõigil AOS-i arvutitel)
-   Microsoft Dynamics 365 for Operationsi pakett-tööde halduse teenus (ainult mitteprivaatsetel AOS-i arvutitel)
-   Management Reporter 2012 protsessiteenus (ainult BI-arvutitel)

## <a name="import-report-definitions"></a>Aruande definitsioonide importimine
Importige aruande kujundused aruandekoosturist, kasutades eksportimise ajal loodud faili.

1.  Minge aruandekoosturis jaotisse **Ettevõte** &gt; **Koosteüksuste grupid**.
2.  Valige eksportimiseks koosteüksuste grupp ja klõpsake nuppu **Ekspordi**. **Märkus.** Dynamics 365 for Operationsi puhul toetatakse ainult ühte koosteüksuste gruppi: **Vaikeväärtus**.
3.  Valige koosteüksus **Vaikeväärtus** ja klõpsake nuppu **Impordi**.
4.  Valige eksporditud aruande definitsioone sisaldav fail ja klõpsake nuppu **Ava**.
5.  Valige dialoogiboksist Import imporditavad aruande definitsioonid.
    -   Kõikide aruande definitsioonide ja seotud koosteüksuste importimiseks klõpsake valikut **Vali kõik**.
    -   Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite importimiseks valige imporditavad aruanded, read, veerud, puud või dimensioonikogumid.

6.  Klõpsake nuppu **Impordi**.



