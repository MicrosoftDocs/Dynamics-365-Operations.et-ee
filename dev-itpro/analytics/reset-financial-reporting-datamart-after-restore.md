---
title: "Finantsaruandluse andmevaka lähtestamine pärast andmebaasi taastamist"
description: "Selles teemas kirjeldatakse, kuidas lähtestada finantsaruandluse andmevakka pärast Microsoft Dynamics 365 for Finance and Operationsi andmebaasi taastamist."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: et-ee
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Finantsaruandluse andmevaka lähtestamine pärast andmebaasi taastamist

[!include[banner](../includes/banner.md)]


Selles teemas kirjeldatakse, kuidas lähtestada finantsaruandluse andmevakka pärast Microsoft Dynamics 365 for Finance and Operationsi andmebaasi taastamist.

Kui taastate oma rakenduse Finance and Operations andmebaasi varukoopia põhjal või kopeerite mõnest muust keskkonnast pärit andmebaasi, peate järgima selles teemas toodud juhiseid tagamaks, et finantsaruandluse andmevakk kasutab taastatud andmebaasi õigesti. 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> Selle protsessi etappe toetatakse rakenduse Dynamics 365 for Operations 2016. aasta mai väljaandes (rakenduse järgus 7.0.1265.23014 ja finantsaruandluse järgus 7.0.10000.4) ja uuemates väljaannetes. Kui teil on rakenduse Finance and Operations varasem väljaanne, siis pöörduge abi saamiseks meie tugiteenuse töörühma poole.

## <a name="export-report-definitions"></a>Aruande definitsioonide eksportimine
Kõigepealt eksportige aruandekoosturis paiknevad aruandekujundused, tehes järgmist.

1.  Minge aruandekoosturis jaotisse **Ettevõte** &gt; **Koosteüksuste grupid**.
2.  Valige eksportimiseks koosteüksuste grupp ja klõpsake nuppu **Ekspordi**. 
    > [!Note] 
    > Finance and Operationsi puhul toetatakse ainult ühte koosteüksuste gruppi: **Vaikeväärtus**.
3.  Valige eksportimiseks aruande definitsioonid.
    -   Kõikide aruande definitsioonide ja seotud koosteüksuste eksportimiseks klõpsake suvandit **Vali kõik**.
    -   Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite eksportimiseks klõpsake vastavat vahekaarti ja valige eksporditavad üksused. Vahekaardil mitme üksuse valimiseks vajutage ja hoidke all klahvi Ctrl. Eksporditavate aruannete valimisel valitakse seotud read, veerud, puud ja dimensioonikogumid.

4.  Klõpsake nuppu **Ekspordi**.
5.  Sisestage faili nimi ja valige turvaline asukoht, kuhu soovite eksporditud aruande definitsioonid salvestada.
6.  Klõpsake käsku **Salvesta**.

Faili saab kopeerida või laadida üles turvalisse asukohta, et selle saaks muul ajal teistsugusesse keskkonda importida. Teavet Microsoft Azure’i salvestuskonto kohta leiate jaotisest [Andmeedastus käsurea utiliidiga AzCopy](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). 
> [!NOTE]
> Microsoft ei paku Finance and Operationsi lepingu raames salvestuskontot. Peate ostma salvestuskonto või kasutama eraldi Azure’i tellimuse salvestuskontot. 
> [!WARNING]
> Olge kursis Azure’i virtuaalarvutite D-ketta käitumisega. Ärge hoidke sellel pidevalt eksporditud koosteüksuste gruppe. Lisateavet ajutiste ketaste kohta leiate jaotisest [Ajutine ketas Windows Azure’i virtuaalarvutites](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Teenuste peatamine
Kasutage kaugarvutit ühenduse loomiseks kõigi arvutitega keskkonnas ja peatage faili services.msc abil järgmised Windowsi teenused:

-   ülemaailmse veebi avaldamisteenus (kõigil AOS-i arvutitel)
-   Microsoft Dynamics 365 for Finance and Operationsi pakett-tööde halduse teenus (ainult mitteprivaatsetel AOS-i arvutitel)
-   Management Reporter 2012 protsessiteenus (ainult BI-arvutitel)

Nendel teenustel on avatud ühendus Finance and Operationsi andmebaasiga.

## <a name="reset"></a>Lähtestamine
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a>Otsige üles ja laadige alla kõige uusim pakett MinorVersionDataUpgrade.zip

Otsige üles uusim pakett MinorVersionDataUpgrade.zip, kasutades juhiseid jaotises [Uusima andmeuuenduse juurutuspaketi allalaadimine](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package). Juhistes selgitatakse, kuidas leida ja alla laadida õige andmetäienduse paketi väljaanne. Paketi MinorVersionDataUpgrade.zip alla laadimiseks ei ole vaja uuendust. Paketi MinorVersionDataUpgrade.zip koopia alla laadimiseks peate täitma ainult teemas „Uusima andmeuuenduse juurutuspaketi allalaadimine“ toodud juhised, ilma ülejäänud spikriartiklis toodud juhiseid täitmata.

#### <a name="execute-scripts-against-finance-and-operations-database"></a>Käivitage skriptid Finance and Operationsi andmebaasi suhtes

Käivitage järgmised skriptid Finance and Operationsi andmebaasi suhtes (mitte finantsaruandluse andmebaasi suhtes).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Need skriptid tagavad õiged kasutajad, rollid ja muudatuste jälgimise sätted.

#### <a name="execute-powershell-command-to-reset-database"></a>Käivitage andmebaasi lähtestamiseks PowerShelli käsk

Käivitage järgmine käsk otse AOS-i arvutil, et lähtestada Finance and Operationsi ja finantsaruandluse integratsioon.

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
-   Microsoft Dynamics 365 for Finance and Operationsi pakett-tööde halduse teenus (ainult mitteprivaatsetel AOS-i arvutitel)
-   Management Reporter 2012 protsessiteenus (ainult BI-arvutitel)

## <a name="import-report-definitions"></a>Aruande definitsioonide importimine
Importige aruande kujundused aruandekoosturist, kasutades eksportimise ajal loodud faili.

1.  Minge aruandekoosturis jaotisse **Ettevõte** &gt; **Koosteüksuste grupid**.
2.  Valige eksportimiseks koosteüksuste grupp ja klõpsake nuppu **Ekspordi**. 

    > [!NOTE]
    > Finance and Operationsi puhul toetatakse ainult ühte koosteüksuste gruppi: **Vaikeväärtus**.
    
3.  Valige koosteüksus **Vaikeväärtus** ja klõpsake nuppu **Impordi**.
4.  Valige eksporditud aruande definitsioone sisaldav fail ja klõpsake nuppu **Ava**.
5.  Valige dialoogiboksist Import imporditavad aruande definitsioonid.
    -   Kõikide aruande definitsioonide ja seotud koosteüksuste importimiseks klõpsake valikut **Vali kõik**.
    -   Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite importimiseks valige imporditavad aruanded, read, veerud, puud või dimensioonikogumid.

6.  Klõpsake nuppu **Impordi**.





