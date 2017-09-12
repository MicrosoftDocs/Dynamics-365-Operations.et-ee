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

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="c6bfc-103">Finantsaruandluse andmevaka lähtestamine pärast andmebaasi taastamist</span><span class="sxs-lookup"><span data-stu-id="c6bfc-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c6bfc-104">Selles teemas kirjeldatakse, kuidas lähtestada finantsaruandluse andmevakka pärast Microsoft Dynamics 365 for Finance and Operationsi andmebaasi taastamist.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="c6bfc-105">Kui taastate oma rakenduse Finance and Operations andmebaasi varukoopia põhjal või kopeerite mõnest muust keskkonnast pärit andmebaasi, peate järgima selles teemas toodud juhiseid tagamaks, et finantsaruandluse andmevakk kasutab taastatud andmebaasi õigesti.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> <span data-ttu-id="c6bfc-106">Selle protsessi etappe toetatakse rakenduse Dynamics 365 for Operations 2016. aasta mai väljaandes (rakenduse järgus 7.0.1265.23014 ja finantsaruandluse järgus 7.0.10000.4) ja uuemates väljaannetes.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="c6bfc-107">Kui teil on rakenduse Finance and Operations varasem väljaanne, siis pöörduge abi saamiseks meie tugiteenuse töörühma poole.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="c6bfc-108">Aruande definitsioonide eksportimine</span><span class="sxs-lookup"><span data-stu-id="c6bfc-108">Export report definitions</span></span>
<span data-ttu-id="c6bfc-109">Kõigepealt eksportige aruandekoosturis paiknevad aruandekujundused, tehes järgmist.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="c6bfc-110">Minge aruandekoosturis jaotisse **Ettevõte** &gt; **Koosteüksuste grupid**.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="c6bfc-111">Valige eksportimiseks koosteüksuste grupp ja klõpsake nuppu **Ekspordi**.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-111">Select the building block group to export, and click **Export**.</span></span> 
    > [!Note] 
    > <span data-ttu-id="c6bfc-112">Finance and Operationsi puhul toetatakse ainult ühte koosteüksuste gruppi: **Vaikeväärtus**.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
3.  <span data-ttu-id="c6bfc-113">Valige eksportimiseks aruande definitsioonid.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="c6bfc-114">Kõikide aruande definitsioonide ja seotud koosteüksuste eksportimiseks klõpsake suvandit **Vali kõik**.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="c6bfc-115">Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite eksportimiseks klõpsake vastavat vahekaarti ja valige eksporditavad üksused.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="c6bfc-116">Vahekaardil mitme üksuse valimiseks vajutage ja hoidke all klahvi Ctrl.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-116">Press and hold the Ctrl key to select multiple items in a tab.</span></span> <span data-ttu-id="c6bfc-117">Eksporditavate aruannete valimisel valitakse seotud read, veerud, puud ja dimensioonikogumid.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-117">When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="c6bfc-118">Klõpsake nuppu **Ekspordi**.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-118">Click **Export**.</span></span>
5.  <span data-ttu-id="c6bfc-119">Sisestage faili nimi ja valige turvaline asukoht, kuhu soovite eksporditud aruande definitsioonid salvestada.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-119">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="c6bfc-120">Klõpsake käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-120">Click **Save**.</span></span>

<span data-ttu-id="c6bfc-121">Faili saab kopeerida või laadida üles turvalisse asukohta, et selle saaks muul ajal teistsugusesse keskkonda importida.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-121">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="c6bfc-122">Teavet Microsoft Azure’i salvestuskonto kohta leiate jaotisest [Andmeedastus käsurea utiliidiga AzCopy](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="c6bfc-122">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="c6bfc-123">Microsoft ei paku Finance and Operationsi lepingu raames salvestuskontot.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-123">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="c6bfc-124">Peate ostma salvestuskonto või kasutama eraldi Azure’i tellimuse salvestuskontot.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-124">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="c6bfc-125">Olge kursis Azure’i virtuaalarvutite D-ketta käitumisega.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-125">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="c6bfc-126">Ärge hoidke sellel pidevalt eksporditud koosteüksuste gruppe.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-126">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="c6bfc-127">Lisateavet ajutiste ketaste kohta leiate jaotisest [Ajutine ketas Windows Azure’i virtuaalarvutites](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="c6bfc-127">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="c6bfc-128">Teenuste peatamine</span><span class="sxs-lookup"><span data-stu-id="c6bfc-128">Stop services</span></span>
<span data-ttu-id="c6bfc-129">Kasutage kaugarvutit ühenduse loomiseks kõigi arvutitega keskkonnas ja peatage faili services.msc abil järgmised Windowsi teenused:</span><span class="sxs-lookup"><span data-stu-id="c6bfc-129">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="c6bfc-130">ülemaailmse veebi avaldamisteenus (kõigil AOS-i arvutitel)</span><span class="sxs-lookup"><span data-stu-id="c6bfc-130">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="c6bfc-131">Microsoft Dynamics 365 for Finance and Operationsi pakett-tööde halduse teenus (ainult mitteprivaatsetel AOS-i arvutitel)</span><span class="sxs-lookup"><span data-stu-id="c6bfc-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="c6bfc-132">Management Reporter 2012 protsessiteenus (ainult BI-arvutitel)</span><span class="sxs-lookup"><span data-stu-id="c6bfc-132">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="c6bfc-133">Nendel teenustel on avatud ühendus Finance and Operationsi andmebaasiga.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-133">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="c6bfc-134">Lähtestamine</span><span class="sxs-lookup"><span data-stu-id="c6bfc-134">Reset</span></span>
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="c6bfc-135">Otsige üles ja laadige alla kõige uusim pakett MinorVersionDataUpgrade.zip</span><span class="sxs-lookup"><span data-stu-id="c6bfc-135">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="c6bfc-136">Otsige üles uusim pakett MinorVersionDataUpgrade.zip, kasutades juhiseid jaotises [Uusima andmeuuenduse juurutuspaketi allalaadimine](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="c6bfc-136">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> <span data-ttu-id="c6bfc-137">Juhistes selgitatakse, kuidas leida ja alla laadida õige andmetäienduse paketi väljaanne.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-137">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="c6bfc-138">Paketi MinorVersionDataUpgrade.zip alla laadimiseks ei ole vaja uuendust.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-138">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="c6bfc-139">Paketi MinorVersionDataUpgrade.zip koopia alla laadimiseks peate täitma ainult teemas „Uusima andmeuuenduse juurutuspaketi allalaadimine“ toodud juhised, ilma ülejäänud spikriartiklis toodud juhiseid täitmata.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-139">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

#### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="c6bfc-140">Käivitage skriptid Finance and Operationsi andmebaasi suhtes</span><span class="sxs-lookup"><span data-stu-id="c6bfc-140">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="c6bfc-141">Käivitage järgmised skriptid Finance and Operationsi andmebaasi suhtes (mitte finantsaruandluse andmebaasi suhtes).</span><span class="sxs-lookup"><span data-stu-id="c6bfc-141">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="c6bfc-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="c6bfc-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="c6bfc-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="c6bfc-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="c6bfc-144">Need skriptid tagavad õiged kasutajad, rollid ja muudatuste jälgimise sätted.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-144">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="c6bfc-145">Käivitage andmebaasi lähtestamiseks PowerShelli käsk</span><span class="sxs-lookup"><span data-stu-id="c6bfc-145">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="c6bfc-146">Käivitage järgmine käsk otse AOS-i arvutil, et lähtestada Finance and Operationsi ja finantsaruandluse integratsioon.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-146">Execute the following command, directly on the AOS computer, to reset the integration between Finance and Operations and financial reporting:</span></span>

1.  <span data-ttu-id="c6bfc-147">Avage Windows PowerShell administraatorina.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-147">Open Windows PowerShell as Administrator.</span></span>
2.  <span data-ttu-id="c6bfc-148">Käivitage: F:</span><span class="sxs-lookup"><span data-stu-id="c6bfc-148">Execute: F:</span></span>
3.  <span data-ttu-id="c6bfc-149">Käivitage: cd F:\\MRApplicationService\\MRInstallDirectory</span><span class="sxs-lookup"><span data-stu-id="c6bfc-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span></span>
4.  <span data-ttu-id="c6bfc-150">Käivitage: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span><span class="sxs-lookup"><span data-stu-id="c6bfc-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span></span>
5.  <span data-ttu-id="c6bfc-151">Käivitage: Reset-DatamartIntegration -Reason OTHER -ReasonDetail „&lt;minu lähtestamise põhjus&gt;”</span><span class="sxs-lookup"><span data-stu-id="c6bfc-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span></span>
    -   <span data-ttu-id="c6bfc-152">Teil palutakse sisestada kinnitamiseks „Y”.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-152">You will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="c6bfc-153">Parameetrite selgitus.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-153">Explanation of parameters:</span></span>

-   <span data-ttu-id="c6bfc-154">Parameetri -Reason sobivad väärtused on SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-154">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="c6bfc-155">Parameeter -ReasonDetail on vaba tekst.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-155">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="c6bfc-156">Parameetrid reason ja reasonDetail salvestatakse jaotisse telemeetria / keskkonna jälgimine.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-156">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="c6bfc-157">Teenuste käivitamine</span><span class="sxs-lookup"><span data-stu-id="c6bfc-157">Start services</span></span>
<span data-ttu-id="c6bfc-158">Taaskäivitage faili services.msc abil eelnevalt peatatud teenused.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-158">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="c6bfc-159">ülemaailmse veebi avaldamisteenus (kõigil AOS-i arvutitel)</span><span class="sxs-lookup"><span data-stu-id="c6bfc-159">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="c6bfc-160">Microsoft Dynamics 365 for Finance and Operationsi pakett-tööde halduse teenus (ainult mitteprivaatsetel AOS-i arvutitel)</span><span class="sxs-lookup"><span data-stu-id="c6bfc-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="c6bfc-161">Management Reporter 2012 protsessiteenus (ainult BI-arvutitel)</span><span class="sxs-lookup"><span data-stu-id="c6bfc-161">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="c6bfc-162">Aruande definitsioonide importimine</span><span class="sxs-lookup"><span data-stu-id="c6bfc-162">Import report definitions</span></span>
<span data-ttu-id="c6bfc-163">Importige aruande kujundused aruandekoosturist, kasutades eksportimise ajal loodud faili.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-163">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="c6bfc-164">Minge aruandekoosturis jaotisse **Ettevõte** &gt; **Koosteüksuste grupid**.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-164">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="c6bfc-165">Valige eksportimiseks koosteüksuste grupp ja klõpsake nuppu **Ekspordi**.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-165">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="c6bfc-166">Finance and Operationsi puhul toetatakse ainult ühte koosteüksuste gruppi: **Vaikeväärtus**.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-166">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="c6bfc-167">Valige koosteüksus **Vaikeväärtus** ja klõpsake nuppu **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-167">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="c6bfc-168">Valige eksporditud aruande definitsioone sisaldav fail ja klõpsake nuppu **Ava**.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-168">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="c6bfc-169">Valige dialoogiboksist Import imporditavad aruande definitsioonid.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-169">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="c6bfc-170">Kõikide aruande definitsioonide ja seotud koosteüksuste importimiseks klõpsake valikut **Vali kõik**.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-170">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="c6bfc-171">Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite importimiseks valige imporditavad aruanded, read, veerud, puud või dimensioonikogumid.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-171">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="c6bfc-172">Klõpsake nuppu **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="c6bfc-172">Click **Import**.</span></span>





