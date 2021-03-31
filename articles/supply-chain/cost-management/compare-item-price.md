---
title: Kaubahindade võrdluse talletuse aruanne
description: Saage teada, kuidas luua kaubahindade võrdluse talletuse aruannet ja seejärel tulemusi sirvida ja/või eksportida.
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f40faa7919e6fb5ce0de2594b3d2f264fe42fa1a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222917"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="fd3ed-103">Kaubahindade võrdluse talletuse aruanne</span><span class="sxs-lookup"><span data-stu-id="fd3ed-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd3ed-104">Selles teemas selgitatakse, kuidas käivitada aruanne **Kaubahindade võrdluse talletus** ja muuta väljund digitaalselt kättesaadavaks kas interaktiivse lehena rakenduses Dynamics 365 Supply Chain Management või eksporditud dokumendina ühes paljudest vormingutest.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="fd3ed-105">Aruande brauseris vaatamisel reguleeritakse veerge ja koondsaldosid dünaamiliselt olenevalt konfigureeritud paigutusele.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="fd3ed-106">Saate sortida tulemusi, filtreerida neid, minna andmetesse süvitsi ja muud.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="fd3ed-107">Aruande tulemused talletatakse andmeüksuses **Kaubahindade võrdlus**, mis võimaldab teil tulemusi filtreerida ja eksportida vormingus, nagu CSV või Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="fd3ed-108">Aruanne **Kaubahindade võrdluse talletus** on kasulik juhtudel, kui väljund sisaldab palju ridu.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="fd3ed-109">Näiteks sisaldab väljund palju ridu, kui teil on enam kui 40 000 üksusel kuluversioonis ootel kauba hind.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="fd3ed-110">Kaubahindade võrdluse talletuse lubamine</span><span class="sxs-lookup"><span data-stu-id="fd3ed-110">Enable compare item prices storage</span></span>

<span data-ttu-id="fd3ed-111">Enne selle funktsiooni kasutamist peate selle oma süsteemis lubama.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="fd3ed-112">Administraatorid saavad kasutada [funktsioonide halduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajaduse korral see lubada.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="fd3ed-113">Siin on funktsioon loetletud järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="fd3ed-114">**Moodul** – kuluhaldus</span><span class="sxs-lookup"><span data-stu-id="fd3ed-114">**Module** - Cost management</span></span>
- <span data-ttu-id="fd3ed-115">**Funktsiooni nimi** – kaubahinna võrdluse talletus</span><span class="sxs-lookup"><span data-stu-id="fd3ed-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="fd3ed-116">Kaubahindade võrdluse talletuse aruande loomine</span><span class="sxs-lookup"><span data-stu-id="fd3ed-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="fd3ed-117">Aruande **Kaubahindade võrdluse talletus** loomiseks ja salvestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="fd3ed-118">Avage **Kuluhaldus > Päringud ja aruanded > Eelmääratud kulude aruanded > Kaubahindade võrdluse talletus**.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="fd3ed-119">Valige suvand **Uus**, et avada paan **Kaubahindade võrdlus**.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="fd3ed-120">Määrake järgmised valikud, et määratleda, milliseid hindu teie aruandes võrreldakse.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="fd3ed-121">Kiirkaardil **Parameetrid** andke aruandele kordumatu **nimi** ja kasutage väljasid jaotistes **Võrreldavad ootel hinnad** ja **Võrdluses kasutatavad hinnad**, et määratleda, milliseid hindu ja kuupäevi võrrelda.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="fd3ed-122">Seadistage kiirkardil **Kaasatavad kirjed** filtrid ja piirangud, et määratleda, millised andmed aruandesse kaasata.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="fd3ed-123">Seadistage kiirkaardil **Käivita taustal** aruannete loomise viis, aeg ja sagedus.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="fd3ed-124">See aruanne käivitatakse alati pakett-töö osana.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="fd3ed-125">Valige **OK**, et rakendada oma sätted ja sulgeda paan.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="fd3ed-126">Kui pakett-töö on lõpetatud, loetletakse see lehel **Kaubahindade võrdluse talletus**.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="fd3ed-127">Aruande nägemiseks võib olla vajalik lehe värskendamine.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="fd3ed-128">Kaubahindade võrdluse talletuse aruandega tutvumine</span><span class="sxs-lookup"><span data-stu-id="fd3ed-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="fd3ed-129">Pärast aruande loomist saate igal ajal seda vaadata ja sellega tutvuda järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="fd3ed-130">Avage **Kuluhaldus > Päringud ja aruanded > Eelmääratud kulude aruanded > Kaubahindade võrdluse talletus**.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="fd3ed-131">Valige loendist aruanne.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-131">Select a report from the list.</span></span>

1. <span data-ttu-id="fd3ed-132">Tehke üht järgmistest valikutest.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-132">Do one of the following:</span></span>

    - <span data-ttu-id="fd3ed-133">Aruande tulemustest ülevaate saamiseks valige suvand **Ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="fd3ed-134">Aruande üksikajalikuma kuva saamiseks valige suvand **Kuva üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="fd3ed-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="fd3ed-135">Pärast valitud vaate avamist saate teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="fd3ed-136">Valige peaaegu mis tahes veerupäis, et sortida või filtreerida tabelit selle veeru väärtuste järgi, nagu enamike standardete vormidega Supply Chain Managementis.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="fd3ed-137">Pange tähele, et te ei saa sortida ega filtreerida veergu **Netomuutuse hinna %**, kuna see on arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="fd3ed-138">Valige suvand **Dimensiooni kuvamine**, et avada paan, kus saate valida, milline dimensiooni veerg vormile kaasata.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="fd3ed-139">Määrake suvand **Salvesta seadistus** olekule **Jah**, kui soovite need seadistused salvestada, et need oleksid alles järgmine kord, kui aruande avate.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="fd3ed-140">Valige **OK**, et rakendada oma sätted ja sulgeda.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="fd3ed-141">Valige vormil mis tahes rida ja seejärel valige **Kuva üksikasjad**, et näha valitud üksuse kohta rohkem teavet.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="fd3ed-142">Saate siin andmetesse süvitsi minna.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="fd3ed-143">Valige vormil mis tahes rida ja seejärel valige **Kuva võrdlusdiagramm**, et näha oma tulemuste interaktiivset graafilist esitust, nagu need teie valitud üksusega seonduvad.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="fd3ed-144">Saate neid tulemusi uurida, valides diagrammil ja diagrammi legendis erinevaid graafilisi elemente.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="fd3ed-145">Valige vormil mis tahes rida ja seejärel valige **Kuva arvutuse üksikasjad**, et näha valitud üksusega seotud arvutuste kohta rohkem teavet.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="fd3ed-146">Saate siin andmetesse süvitsi minna.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="fd3ed-147">Kaubahindade võrdluse talletuse aruande eksportimine</span><span class="sxs-lookup"><span data-stu-id="fd3ed-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="fd3ed-148">Iga loodud aruanne talletatakse andmeüksuses **Kaubahindade võrdlus**.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="fd3ed-149">Saate kasutada Supply Chain Managementi standardseid andmekogumise funktsioone, et eksportida selle üksuse andmed mis tahes toetatud vormingusse, sh CSV või Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="fd3ed-150">Järgnev on näide selle kohta, kuidas aruannet **Kaubahindade võrdluse talletus** eksportida.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="fd3ed-151">Avage **Süsteemihaldus > Tööruumid > Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="fd3ed-152">Valige nupp **Ekspordi** jaotises **Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="fd3ed-153">Avaneb leht **Eksport**, mida kasutate eksportimistöö seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="fd3ed-154">Alustage sellega, et annate oma tööle **grupi nime**.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="fd3ed-155">Jaotises **Valitud olemid** valige suvand **Lisa olem**, et avada dialoogiaken, kus saate määrata järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="fd3ed-156">**Olemi nimi** – valige **Kaubahindade võrdlus**.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="fd3ed-157">**Sihtüksuse vorming** – valige vorming, mille soovite eksportida.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="fd3ed-158">Valige käsk **Lisa**, et lisada uus rida, ja seejärel klõpsake nuppu **Sulge**, et sulgeda dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="fd3ed-159">Tavaliselt ekspordite ühe aruande korraga.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="fd3ed-160">Selle tegemiseks seadistage **Filter** rea jaoks, mille äsja paanile **Päring** lisasite.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="fd3ed-161">See võimaldab teil määratleda, milliseid aruandeid üksusest **Kaubahindade võrdlus** soovite oma eksporti kaasata.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="fd3ed-162">Ühe aruande eksportimiseks seadke järgmised filtri valikud.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="fd3ed-163">Vahekaardil **vahemik** valige käsk **Lisa**, et lisada uus rida.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="fd3ed-164">Määrake suvad **Tabel** valikule **Kaubahindade võrdlus**.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="fd3ed-165">Määrake suvad **Tuletatud tabel** valikule **Kaubahindade võrdlus**.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="fd3ed-166">Määrake suvand **Väli** väljale, mille alusel soovite filtreerida.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="fd3ed-167">Tavaliselt kasutate suvandit **Täimise nimi** või **Täitmise kellaaeg**.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="fd3ed-168">Seadke suvand **kriteeriumid** valitud välja väärtusele, mida soovite otsida (kas aruande nimi või aruande loomise kellaaeg).</span><span class="sxs-lookup"><span data-stu-id="fd3ed-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="fd3ed-169">Vajadusel lisage tabelisse **Vahemik** veel ridu, kuni olete otsitava aruande üheselt identifitseerinud.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="fd3ed-170">Valige **OK**, et salvestada oma sätted ja sulgeda.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="fd3ed-171">Oma ekspordi seadistuse salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="fd3ed-172">Avage vahekaart **Eksportimise suvandid** ja valige suvand **Ekspordi kohe**, et luua eksportimise fail.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="fd3ed-173">Avaneb leht **Käivitamise kokkuvõtte** kokkuvõte, kus saate vaadata oma ekspordi töö olekut ja eksporditud üksuste loendit.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="fd3ed-174">Valige üksus **Kaubahindade võrdlus**, mis on loetletud alal **Üksuse töötlemise olek**, ja seejärel valige suvand **Laadi fail alla**, et laadida alla sellest olemist eksporditud andmed.</span><span class="sxs-lookup"><span data-stu-id="fd3ed-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="fd3ed-175">Lisateavet andmete eksportimiseks andmehalduse kasutamise kohta vt [Andmete importimis- ja eksportimistööde ülevaade](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="fd3ed-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]