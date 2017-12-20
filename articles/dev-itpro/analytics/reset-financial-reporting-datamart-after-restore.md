---
title: "Finantsaruandluse andmevaka lähtestamine"
description: "Selles teemas kirjeldatakse, kuidas lähtestada finantsaruandluse andmevakka."
author: aolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0786d3377b914791106ef30455d676e5ab2ae03d
ms.openlocfilehash: c708fa18b8676d8ff57c26b3176a36d86df29387
ms.contentlocale: et-ee
ms.lasthandoff: 12/07/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="e699d-103">Finantsaruandluse andmevaka lähtestamine</span><span class="sxs-lookup"><span data-stu-id="e699d-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e699d-104">Selles teemas kirjeldatakse, kuidas lähtestada finantsaruandluse andmevakka järgmistes versioonides.</span><span class="sxs-lookup"><span data-stu-id="e699d-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="e699d-105">Rakenduse Microsoft Dynamics 365 for Finance and Operations finantsaruandluse väljaanne 7.2.6.0 ja uuem</span><span class="sxs-lookup"><span data-stu-id="e699d-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="e699d-106">Rakenduse Microsoft Dynamics 365 for Finance and Operations finantsaruandluse väljaanne 7.0.10000.4 ja uuem</span><span class="sxs-lookup"><span data-stu-id="e699d-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="e699d-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (kohapealne)</span><span class="sxs-lookup"><span data-stu-id="e699d-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="e699d-108">Rakenduse Finance and Operations finantsaruandluse väljaande 7.2.6.0 hankimiseks saate laadida alla teabebaasi artikli nr 4052514 aadressilt <https://support.microsoft.com/en-us/help/4052514>.</span><span class="sxs-lookup"><span data-stu-id="e699d-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://support.microsoft.com/en-us/help/4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="e699d-109">Rakenduse Finance and Operations finantsaruandluse väljaande 7.2.6.0 ja uuema finantsaruandluse andmevaka lähtestamine</span><span class="sxs-lookup"><span data-stu-id="e699d-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="e699d-110">Aruande koostaja finantsaruandluse andmevaka lähtestamine</span><span class="sxs-lookup"><span data-stu-id="e699d-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="e699d-111">Selle protsessi etappe toetatakse rakenduse Finance and Operations finantsaruandluse väljaandes 7.2.6.0 ja uuemas.</span><span class="sxs-lookup"><span data-stu-id="e699d-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="e699d-112">Kui teil on varasem väljaanne, pöörduge abi saamiseks tugimeeskonna poole.</span><span class="sxs-lookup"><span data-stu-id="e699d-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="e699d-113">Teatud juhtudel võib olla vajalik finantsaruandluse andmevaka lähtestamine.</span><span class="sxs-lookup"><span data-stu-id="e699d-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="e699d-114">Saate selle ülesande täita aruande koostaja kliendis.</span><span class="sxs-lookup"><span data-stu-id="e699d-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="e699d-115">Allpool on esitatud mõned stsenaariumid, mille korral võib olla vajalik andmevaka lähtestamine.</span><span class="sxs-lookup"><span data-stu-id="e699d-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="e699d-116">Rakenduse Finance and Operations andmebaas taastati, kuid andmevaka andmebaasi ei taastatud.</span><span class="sxs-lookup"><span data-stu-id="e699d-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="e699d-117">Perioodi kohta kuvatakse valed andmed.</span><span class="sxs-lookup"><span data-stu-id="e699d-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="e699d-118">Tugimeeskond juhendab teid, kuidas lähtestada andmevakka tõrkeotsingu sammu osana.</span><span class="sxs-lookup"><span data-stu-id="e699d-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="e699d-119">Andmevakka tuleks lähtestada ainult aegadel, mil töötlemise hulk andmebaasis on väike.</span><span class="sxs-lookup"><span data-stu-id="e699d-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="e699d-120">Finantsaruandluse pole lähtestamise ajal saadaval.</span><span class="sxs-lookup"><span data-stu-id="e699d-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="e699d-121">Andmevaka lähtestamine</span><span class="sxs-lookup"><span data-stu-id="e699d-121">Reset the data mart</span></span>

<span data-ttu-id="e699d-122">Andmevaka lähtestamiseks avage Aruande koostaja ja valige menüüs **Tööriistad** suvand **Lähtesta andmevakk**.</span><span class="sxs-lookup"><span data-stu-id="e699d-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="e699d-123">Kuvatud dialoogiboksis on kaks jaotist: **Statistika** ja **Lähtestamine**.</span><span class="sxs-lookup"><span data-stu-id="e699d-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="e699d-124">[![Dialoogiboks Lähtesta andmevakk](./media/Statistics.png)](./media/Statistics.png)</span><span class="sxs-lookup"><span data-stu-id="e699d-124">[![Reset Data Mart dialog box](./media/Statistics.png)](./media/Statistics.png)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="e699d-125">Integratsioonikatsed</span><span class="sxs-lookup"><span data-stu-id="e699d-125">Integration attempts</span></span>

<span data-ttu-id="e699d-126">Ruudustik **Integratsioonikatsed** näitab, mitu korda süsteem on proovinud kandeid integreerida.</span><span class="sxs-lookup"><span data-stu-id="e699d-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="e699d-127">Kui esimesed paar katset ebaõnnestuvad, üritab süsteem valitud päevade jooksul andmeid uuesti integreerida.</span><span class="sxs-lookup"><span data-stu-id="e699d-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="e699d-128">Andmevakk tuleb lähtestada, kui katsete arv on 8 või enam ja dimensioonide kombinatsioone või kandekirjeid on palju.</span><span class="sxs-lookup"><span data-stu-id="e699d-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="e699d-129">Sellisel juhul ei esitata andmete kohta aruandeid.</span><span class="sxs-lookup"><span data-stu-id="e699d-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="e699d-130">Andmete olek</span><span class="sxs-lookup"><span data-stu-id="e699d-130">Data status</span></span>

<span data-ttu-id="e699d-131">Ruudustik **Andmete olek** annab hetkeülevaate andmevakas olevatest kannetest, vahetuskurssidest ja dimensiooniväärtustest.</span><span class="sxs-lookup"><span data-stu-id="e699d-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="e699d-132">Kui aegunud kirjeid on väga palju, näitab see, et eelmisi kirjeid on korduvalt värskendatud.</span><span class="sxs-lookup"><span data-stu-id="e699d-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="e699d-133">Selle tulemusena võib aruannete loomine minna aeglasemalt.</span><span class="sxs-lookup"><span data-stu-id="e699d-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="e699d-134">Valesti joondatud põhikonto kategooriad</span><span class="sxs-lookup"><span data-stu-id="e699d-134">Misaligned main account categories</span></span>

<span data-ttu-id="e699d-135">Kui kasutate varasemat väljaannet kui rakenduse Microsoft Dynamics 365 for Finance and Operations finantsaruandluse väljaanne 7.2.1, võib juhtuda, et peate andmevaka lähtestama, kui nimetate kontosid ümber ja teisaldate kontosid kontokategooriate vahel.</span><span class="sxs-lookup"><span data-stu-id="e699d-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="e699d-136">Nende tegevuste tagajärjeks võib olla põhikonto kategooriate valesti joondamine.</span><span class="sxs-lookup"><span data-stu-id="e699d-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="e699d-137">Seda, kas teil on see probleem, näitab väli **Valesti joondatud põhikonto kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="e699d-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="e699d-138">Andmevaka lähtestamine rakenduse Finance and Operations finantsaruandluse väljaandes 7.2.6.0</span><span class="sxs-lookup"><span data-stu-id="e699d-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="e699d-139">Andmevaka lähtestamiseks rakenduse Finance and Operations finantsaruandluse väljaandes 7.2.6.0 ja varasemas valige dialoogiboksis **Lähtesta andmevakk** märkeruut **Lähtesta andmevakk** ja seejärel klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="e699d-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="e699d-140">Soovitame andmevakka lähtestada ainult plaanitud seisakuajal.</span><span class="sxs-lookup"><span data-stu-id="e699d-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="e699d-141">[![Märkeruut Lähtesta andmevakk](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="e699d-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="e699d-142">Andmevaka lähtestamine ja põhjuse valimine rakenduse Microsoft Dynamics 365 for Finance and Operations finantsaruandluse väljaandes 7.3.0</span><span class="sxs-lookup"><span data-stu-id="e699d-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="e699d-143">Kui otsustate, et andmevaka lähtestamine on vajalik, valige märkeruut **Lähtesta andmevakk** ja valige väljal **Põhjus** lähtestamise põhjus.</span><span class="sxs-lookup"><span data-stu-id="e699d-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="e699d-144">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="e699d-144">The following options are available:</span></span>

- <span data-ttu-id="e699d-145">**Puuduvad või valed andmed** – tegite statistika põhjal kindlaks, et andmeid võib olla puudu.</span><span class="sxs-lookup"><span data-stu-id="e699d-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="e699d-146">Enne jätkamist soovitame teha koostööd tugimeeskonnaga, et selgitada välja juurpõhjus.</span><span class="sxs-lookup"><span data-stu-id="e699d-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="e699d-147">**Andmebaasi taastamine** – rakenduse Finance and Operations andmebaas taastati, kuid finantsaruandluse andmevaka andmebaasi ei taastatud.</span><span class="sxs-lookup"><span data-stu-id="e699d-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="e699d-148">**Muu** – lähtestate andmevakka mõnel muul põhjusel.</span><span class="sxs-lookup"><span data-stu-id="e699d-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="e699d-149">Kui usute, et ilmnenud on probleem, võtke selle tuvastamiseks ühendust toega.</span><span class="sxs-lookup"><span data-stu-id="e699d-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

> [!NOTE]
> <span data-ttu-id="e699d-150">Enne etappide lõpule viimist veenduge, et kõik olemasolevad ülesanded oleksid integreerimise lõpule viinud.</span><span class="sxs-lookup"><span data-stu-id="e699d-150">Verify that all existing tasks have finished integrating before you complete the steps.</span></span> <span data-ttu-id="e699d-151">Integreerimise oleku nägemiseks valige **Tööriistad** &gt; **Integreerimisolek**.</span><span class="sxs-lookup"><span data-stu-id="e699d-151">You can view the status of the integration by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="e699d-152">Eemalda kasutajad ja ettevõtted</span><span class="sxs-lookup"><span data-stu-id="e699d-152">Clear users and companies</span></span>

<span data-ttu-id="e699d-153">Valige märkeruut **Eemalda kasutajad ja ettevõtted**, kui taastasite oma andmebaasi, kuid muutsite seejärel kasutajaid või ettevõtteid.</span><span class="sxs-lookup"><span data-stu-id="e699d-153">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="e699d-154">Seda märkeruutu ei lähe tavaliselt vaja.</span><span class="sxs-lookup"><span data-stu-id="e699d-154">You should rarely have to select this check box.</span></span>

<span data-ttu-id="e699d-155">Kui olete valmis lähtestamist alustama, valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="e699d-155">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="e699d-156">Teil palutakse kinnitada, et olete valmis protsessi käivitama.</span><span class="sxs-lookup"><span data-stu-id="e699d-156">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="e699d-157">Pange tähele, et lähtestamise ning hiljem toimuva andmete esialgse integreerimise ajal pole finantsaruandlus saadaval.</span><span class="sxs-lookup"><span data-stu-id="e699d-157">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="e699d-158">Kui soovite saada integreerimise olekust ülevaate, valige **Tööriistad** &gt; **Integreerimisolek**, et näha, millal viimati integreerimine käivitati ja mis oli selle olek.</span><span class="sxs-lookup"><span data-stu-id="e699d-158">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="e699d-159">[![Integreerimise oleku vaatamine](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="e699d-159">[![View the status of the integration](./media/Integration.png)](./media/Integration.png)</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="e699d-160">Rakenduse Finance and Operations finantsaruandluse väljaande 7.0.10000.4 ja uuema finantsaruandluse andmevaka lähtestamine</span><span class="sxs-lookup"><span data-stu-id="e699d-160">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="e699d-161">Kui taastate oma rakenduse Finance and Operations andmebaasi varukoopia põhjal või kopeerite mõnest muust keskkonnast pärit andmebaasi, peate järgima selles jaotises toodud juhiseid tagamaks, et finantsaruandluse andmevakk kasutab taastatud Finance and Operationsi andmebaasi õigesti.</span><span class="sxs-lookup"><span data-stu-id="e699d-161">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="e699d-162">Selle protsessi etappe toetatakse Microsoft Dynamics AX-i rakenduse versioonis 7.0.1 (mai 2016) (rakenduse järgus 7.0.1265.23014 ja finantsaruandluse järgus 7.0.10000.4) ja uuemates.</span><span class="sxs-lookup"><span data-stu-id="e699d-162">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="e699d-163">Kui teil on rakenduse Finance and Operations varasem versioon, pöörduge abi saamiseks tugimeeskonna poole.</span><span class="sxs-lookup"><span data-stu-id="e699d-163">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="e699d-164">Aruande definitsioonide eksportimine</span><span class="sxs-lookup"><span data-stu-id="e699d-164">Export report definitions</span></span>

<span data-ttu-id="e699d-165">Esmalt järgige neid etappe, et eksportida aruande koostajast aruande kujundused.</span><span class="sxs-lookup"><span data-stu-id="e699d-165">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="e699d-166">Valige aruande koostajas suvandid **Ettevõte** &gt; **Koosteüksuste grupid**.</span><span class="sxs-lookup"><span data-stu-id="e699d-166">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="e699d-167">Valige eksportimiseks koosteüksuste grupp ja klõpsake nuppu **Ekspordi**.</span><span class="sxs-lookup"><span data-stu-id="e699d-167">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e699d-168">Finance and Operationsi puhul toetatakse ainult ühte koosteüksuste gruppi: **Vaikeväärtus**.</span><span class="sxs-lookup"><span data-stu-id="e699d-168">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="e699d-169">Valige eksportimiseks aruande definitsioonid.</span><span class="sxs-lookup"><span data-stu-id="e699d-169">Select the report definitions to export:</span></span>

    - <span data-ttu-id="e699d-170">Kõigi aruandedefinitsioonide ja seotud koosteüksuste eksportimiseks valige **Vali kõik**.</span><span class="sxs-lookup"><span data-stu-id="e699d-170">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="e699d-171">Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite eksportimiseks valige vastav vahekaart ja valige eksporditavad üksused.</span><span class="sxs-lookup"><span data-stu-id="e699d-171">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="e699d-172">Vahekaardil mitme üksuse valimiseks vajutage ja hoidke all klahvi Ctrl. Eksporditavate aruannete valimisel valitakse nendega seotud read, veerud, puud ja dimensioonikogumid.</span><span class="sxs-lookup"><span data-stu-id="e699d-172">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="e699d-173">Valige **Ekspordi**.</span><span class="sxs-lookup"><span data-stu-id="e699d-173">Select **Export**.</span></span>
5. <span data-ttu-id="e699d-174">Sisestage faili nimi ja valige turvaline asukoht, kuhu soovite eksporditud aruande definitsioonid salvestada.</span><span class="sxs-lookup"><span data-stu-id="e699d-174">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="e699d-175">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e699d-175">Select **Save**.</span></span>

<span data-ttu-id="e699d-176">Saate faili kopeerida või laadida üles turvalisse asukohta.</span><span class="sxs-lookup"><span data-stu-id="e699d-176">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="e699d-177">Sel viisil saab faili hiljem teise keskkonda importida.</span><span class="sxs-lookup"><span data-stu-id="e699d-177">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="e699d-178">Lisateavet Microsoft Azure’i salvestuskonto kasutamise kohta vt teemast [Andmeedastus käsurea utiliidiga AzCopy](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="e699d-178">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="e699d-179">Microsoft ei paku Finance and Operationsi lepingu raames salvestuskontot.</span><span class="sxs-lookup"><span data-stu-id="e699d-179">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="e699d-180">Peate ostma salvestuskonto või kasutama eraldi Azure’i tellimuse salvestuskontot.</span><span class="sxs-lookup"><span data-stu-id="e699d-180">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="e699d-181">Olge kursis Azure’i virtuaalarvutite D-ketta käitumisega.</span><span class="sxs-lookup"><span data-stu-id="e699d-181">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="e699d-182">Ärge talletage oma eksporditud koosteüksuste gruppe jäädavalt D-kettale. Lisateavet ajutiste ketaste kohta vt teemast [Ajutine ketas Windows Azure’i virtuaalarvutites](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="e699d-182">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="e699d-183">Teenuste peatamine</span><span class="sxs-lookup"><span data-stu-id="e699d-183">Stop services</span></span>

<span data-ttu-id="e699d-184">Järgmistel Microsofti Windowsi teenustel on avatud ühendus Finance and Operationsi andmebaasiga.</span><span class="sxs-lookup"><span data-stu-id="e699d-184">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="e699d-185">Seetõttu peate kasutama Microsofti kaugtöölauda ühenduse loomiseks kõigi arvutitega keskkonnas ja seejärel kasutama faili services.msc järgmiste teenuste peatamiseks.</span><span class="sxs-lookup"><span data-stu-id="e699d-185">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="e699d-186">Ülemaailmse veebi avaldamisteenus (kõigil rakendusobjekti serverite [AOS] arvutitel)</span><span class="sxs-lookup"><span data-stu-id="e699d-186">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="e699d-187">Microsoft Dynamics 365 for Finance and Operationsi pakett-tööde halduse teenus (ainult mitteprivaatsetel AOS-i arvutitel)</span><span class="sxs-lookup"><span data-stu-id="e699d-187">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="e699d-188">Management Reporter 2012 protsessiteenus (ainult äriteabe [BI] arvutitel)</span><span class="sxs-lookup"><span data-stu-id="e699d-188">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="e699d-189">Lähtestamine</span><span class="sxs-lookup"><span data-stu-id="e699d-189">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="e699d-190">Uusima paketi MinorVersionDataUpgrade.zip allalaadimine</span><span class="sxs-lookup"><span data-stu-id="e699d-190">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="e699d-191">Laadige alla uusim pakett MinorVersionDataUpgrade.zip.</span><span class="sxs-lookup"><span data-stu-id="e699d-191">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="e699d-192">Juhiste saamiseks selle kohta, kuidas leida üles ja laadida alla andmete täienduspaketi õige versioon, vt teemat [Uusima andmeuuenduse juurutuspaketi allalaadimine](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span><span class="sxs-lookup"><span data-stu-id="e699d-192">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages).</span></span> <span data-ttu-id="e699d-193">Paketi MinorVersionDataUpgrade.zip alla laadimiseks ei ole vaja uuendust.</span><span class="sxs-lookup"><span data-stu-id="e699d-193">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="e699d-194">Seega peate lihtsalt järgima selle teema jaotises „Uusima andmeuuenduse juurutuspaketi allalaadimine” olevaid etappe.</span><span class="sxs-lookup"><span data-stu-id="e699d-194">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="e699d-195">Võite kõik teised teemas olevad etapid vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="e699d-195">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="e699d-196">Skriptide käivitamine Finance and Operationsi andmebaasi suhtes</span><span class="sxs-lookup"><span data-stu-id="e699d-196">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="e699d-197">Käivitage järgmised skriptid Finance and Operationsi andmebaasi suhtes (mitte finantsaruandluse andmebaasi suhtes).</span><span class="sxs-lookup"><span data-stu-id="e699d-197">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="e699d-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="e699d-198">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="e699d-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="e699d-199">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="e699d-200">Need skriptid aitavad tagada õiged kasutajad, rollid ja muudatuste jälgimise sätted.</span><span class="sxs-lookup"><span data-stu-id="e699d-200">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="e699d-201">Windows PowerShelli käsu käivitamine andmebaasi lähtestamiseks</span><span class="sxs-lookup"><span data-stu-id="e699d-201">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="e699d-202">Käivitage AOS-i arvutis Microsoft Windows PowerShell administraatorina ja käivitage järgmised käsud, et lähtestada Finance and Operationsi ja finantsaruandluse integratsioon.</span><span class="sxs-lookup"><span data-stu-id="e699d-202">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="e699d-203">Siin on käsus **Reset-DatamartIntegration** olevate parameetrite selgitus.</span><span class="sxs-lookup"><span data-stu-id="e699d-203">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="e699d-204">Parameetri **-Reason** sobivad väärtused on **SERVICING**, **BADDATA** ja **OTHER**.</span><span class="sxs-lookup"><span data-stu-id="e699d-204">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="e699d-205">Parameeter **-ReasonDetail** on vaba tekst.</span><span class="sxs-lookup"><span data-stu-id="e699d-205">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="e699d-206">Põhjus ja põhjuse üksikasjad salvestatakse jaotisse telemeetria / keskkonna jälgimine.</span><span class="sxs-lookup"><span data-stu-id="e699d-206">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="e699d-207">Pärast käskude käivitamist palutakse teil sisestada **Y**, et kinnitada, et soovite andmebaasi lähtestada.</span><span class="sxs-lookup"><span data-stu-id="e699d-207">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="e699d-208">Teenuste taaskäivitamine</span><span class="sxs-lookup"><span data-stu-id="e699d-208">Restart services</span></span>

<span data-ttu-id="e699d-209">Taaskäivitage faili services.msc abil eelnevalt peatatud teenused.</span><span class="sxs-lookup"><span data-stu-id="e699d-209">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="e699d-210">ülemaailmse veebi avaldamisteenus (kõigil AOS-i arvutitel)</span><span class="sxs-lookup"><span data-stu-id="e699d-210">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="e699d-211">Microsoft Dynamics 365 for Finance and Operationsi pakett-tööde halduse teenus (ainult mitteprivaatsetel AOS-i arvutitel)</span><span class="sxs-lookup"><span data-stu-id="e699d-211">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="e699d-212">Management Reporter 2012 protsessiteenus (ainult BI-arvutitel)</span><span class="sxs-lookup"><span data-stu-id="e699d-212">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="e699d-213">Aruande definitsioonide importimine</span><span class="sxs-lookup"><span data-stu-id="e699d-213">Import report definitions</span></span>

<span data-ttu-id="e699d-214">Importige aruande kujundused aruande koostajast, kasutades eksportimise ajal loodud faili.</span><span class="sxs-lookup"><span data-stu-id="e699d-214">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="e699d-215">Valige aruande koostajas suvandid **Ettevõte** &gt; **Koosteüksuste grupid**.</span><span class="sxs-lookup"><span data-stu-id="e699d-215">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="e699d-216">Valige eksportimiseks koosteüksuste grupp ja klõpsake nuppu **Ekspordi**.</span><span class="sxs-lookup"><span data-stu-id="e699d-216">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e699d-217">Finance and Operationsi puhul toetatakse ainult ühte koosteüksuste gruppi: **Vaikeväärtus**.</span><span class="sxs-lookup"><span data-stu-id="e699d-217">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="e699d-218">Valige koosteüksus **Vaikeväärtus** ja seejärel valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="e699d-218">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="e699d-219">Valige eksporditud aruande definitsioone sisaldav fail ja seejärel valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="e699d-219">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="e699d-220">Valige dialoogiboksis **Importimine** imporditav aruandedefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="e699d-220">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="e699d-221">Kõigi aruandedefinitsioonide ja seotud koosteüksuste importimiseks valige **Vali kõik**.</span><span class="sxs-lookup"><span data-stu-id="e699d-221">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="e699d-222">Valige konkreetsete aruannete, ridade, veergude, puude või dimensioonikogumite importimiseks aruanded, read, veerud, puud või dimensioonikogumid.</span><span class="sxs-lookup"><span data-stu-id="e699d-222">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="e699d-223">Valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="e699d-223">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="e699d-224">Rakenduse Finance and Operations (kohapealne) finantsaruandluse andmevaka lähtestamine</span><span class="sxs-lookup"><span data-stu-id="e699d-224">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="e699d-225">Paluge kõigil kasutajatel aruande koostajast ja rakenduse Finance and Operations finantsaruandluse alalt väljuda.</span><span class="sxs-lookup"><span data-stu-id="e699d-225">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="e699d-226">Käivitage finantsaruandluse andmebaasi (MRDB) suhtes uuesti järgmine skript.</span><span class="sxs-lookup"><span data-stu-id="e699d-226">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="e699d-227">Lühendage või kustutage rakenduse Finance and Operations andmebaasis (AXDB) kõik kirjed tabelist FINANCIALREPORTS.</span><span class="sxs-lookup"><span data-stu-id="e699d-227">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="e699d-228">Lühendage või kustutage kõik kirjed tabelist FINANCIALREPORTVERSION, kui see tabel on rakenduse Finance and Operations andmebaasis olemas.</span><span class="sxs-lookup"><span data-stu-id="e699d-228">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="e699d-229">Kui rakenduse Finance and Operations andmebaasis pole seda tabelit, jätke see etapp vahele.</span><span class="sxs-lookup"><span data-stu-id="e699d-229">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="e699d-230">Käivitage finantsaruandluse andmebaasi suhtes uuesti skript **ResetDatamart.sql**.</span><span class="sxs-lookup"><span data-stu-id="e699d-230">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="e699d-231">See skript keelab andmevaka integreerimise, kustutab kõik andmevaka andmed ja seejärel lubab andmevaka integreerimise uuesti.</span><span class="sxs-lookup"><span data-stu-id="e699d-231">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="e699d-232">Pärast lähtestamist saate uuesti laaditud andmeid käsitsi kontrollida, käivitades finantsaruandluse andmebaasi suhtes järgmise päringu.</span><span class="sxs-lookup"><span data-stu-id="e699d-232">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="e699d-233">Kontrollige, et kõigi ridade väärtus oleks **LastRunTime** ja et suvand **StateType** oleks seatud väärtusele **5**.</span><span class="sxs-lookup"><span data-stu-id="e699d-233">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="e699d-234">Suvandi **StateType** väärtus **5** näitab, et andmete uuesti laadimine õnnestus.</span><span class="sxs-lookup"><span data-stu-id="e699d-234">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="e699d-235">Väärtus **7** näitab nurjunud olekut.</span><span class="sxs-lookup"><span data-stu-id="e699d-235">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="e699d-236">Mõnikord on organisatsiooni hierarhia kaardil selle esimesel käivitamisel see olek.</span><span class="sxs-lookup"><span data-stu-id="e699d-236">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="e699d-237">Kuid nurjunud oleku lahendamine peaks olema automaatne.</span><span class="sxs-lookup"><span data-stu-id="e699d-237">However, the faulted state but should be automatically resolved.</span></span>

