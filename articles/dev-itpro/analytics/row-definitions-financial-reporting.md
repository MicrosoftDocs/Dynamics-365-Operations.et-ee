---
title: Readefinitsioonid finantsaruande koosturis
description: "Readefinitsioon on aruande komponent (koosteüksus), mis määrab finantsaruandel iga rea sisu. Readefinitsiooni saab kombineerida veerudefinitsioonide, aruandluspuu definitsioonide ja aruande definitsioonidega koosteüksuste grupi loomiseks, mida saavad kasutada mitu ettevõtet."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: c829af1da1b3109f4687c9a2536dd156339d5c76
ms.contentlocale: et-ee
ms.lasthandoff: 08/13/2018

---

# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="f9434-104">Readefinitsioonid finantsaruande koosturis</span><span class="sxs-lookup"><span data-stu-id="f9434-104">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9434-105">Readefinitsioon on aruande komponent (koosteüksus), mis määrab finantsaruandel iga rea sisu.</span><span class="sxs-lookup"><span data-stu-id="f9434-105">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="f9434-106">Readefinitsiooni saab kombineerida veerudefinitsioonide, aruandluspuu definitsioonide ja aruande definitsioonidega koosteüksuste grupi loomiseks, mida saavad kasutada mitu ettevõtet.</span><span class="sxs-lookup"><span data-stu-id="f9434-106">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="f9434-107">Readefinitsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="f9434-107">Create a row definition</span></span>

1. <span data-ttu-id="f9434-108">Klõpsake aruandekoosturis navigeerimispaanil suvandit **Readefinitsioonid**.</span><span class="sxs-lookup"><span data-stu-id="f9434-108">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="f9434-109">Klõpsake menüüs **Fail** valikut **Uus** ja seejärel valikut **Readefinitsioon**.</span><span class="sxs-lookup"><span data-stu-id="f9434-109">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="f9434-110">Lisateabe saamiseks iga lahtri sisu kohta vt osa [Readefinitsiooni lahtrite muutmine](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="f9434-110">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="f9434-111">Readefinitsiooni avamine</span><span class="sxs-lookup"><span data-stu-id="f9434-111">Open a row definition</span></span>
1. <span data-ttu-id="f9434-112">Klõpsake aruandekoosturis navigeerimispaanil suvandit **Readefinitsioonid**.</span><span class="sxs-lookup"><span data-stu-id="f9434-112">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="f9434-113">Avamiseks topeltklõpsake readefinitsiooni nime.</span><span class="sxs-lookup"><span data-stu-id="f9434-113">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="f9434-114">Mis tahes readefinitsiooniga seostatud koosteüksuse vaatamiseks paremklõpsake readefinitsiooni ja seejärel valige **Seosed**.</span><span class="sxs-lookup"><span data-stu-id="f9434-114">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="f9434-115"> Readefinitsiooni sisu</span><span class="sxs-lookup"><span data-stu-id="f9434-115">Contents of a row definition</span></span>
<span data-ttu-id="f9434-116">Readefinitsioon võib sisaldada kuni 20 000 finantsdimensiooni rida ja võib sisaldada järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="f9434-116">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="f9434-117">Kirjeldav tekst, mis lisab aruandele tähenduse, luues jaotise päiseid, ridu ja tühikuid, nt **Sularaha** või **Kogutulu**</span><span class="sxs-lookup"><span data-stu-id="f9434-117">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="f9434-118">Lingid finantsandmete juurde, mille hulka võivad kuuluda Microsoft Dynamics 365 for Finance and Operationsi dimensiooniväärtused</span><span class="sxs-lookup"><span data-stu-id="f9434-118">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 for Finance and Operations</span></span>

    > [!NOTE]
    > <span data-ttu-id="f9434-119">Saate readefinitsiooni nii seadistada, et see võtab iga kord, kui aruanne luuakse, finantsdimensiooni süsteemist andmeid.</span><span class="sxs-lookup"><span data-stu-id="f9434-119">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="f9434-120">Ridade kogusummad ja valemid, mis põhinevad lingitud finantsandmetel</span><span class="sxs-lookup"><span data-stu-id="f9434-120">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="f9434-121">Üldjuhul sisaldab iga readefinitsioon üht järgmist tüüpi teavet.</span><span class="sxs-lookup"><span data-stu-id="f9434-121">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="f9434-122">Viited finantsdimensioonide süsteemile</span><span class="sxs-lookup"><span data-stu-id="f9434-122">References to the financial dimensions system</span></span>
- <span data-ttu-id="f9434-123">Andmetel põhinevad kogusummad või arvutused</span><span class="sxs-lookup"><span data-stu-id="f9434-123">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="f9434-124">Vormindus</span><span class="sxs-lookup"><span data-stu-id="f9434-124">Formatting</span></span>

<span data-ttu-id="f9434-125">Readefinitsiooni teabe sisestamiseks on kaks viisi.</span><span class="sxs-lookup"><span data-stu-id="f9434-125">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="f9434-126">Rea teabe käsitsi sisestamine uude readefinitsiooni.</span><span class="sxs-lookup"><span data-stu-id="f9434-126">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="f9434-127">Lisateabe saamiseks vt osa [Readefinitsiooni lahtrite muutmine](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="f9434-127">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="f9434-128">Kasutage aruandekoosturit rea teabe toomiseks otse finantsdimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="f9434-128">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="f9434-129">Lisateavet leiate jaotisest Seotud valemid/read/üksused osas [Readefinitsiooni lahtrite muutmine](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="f9434-129">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="f9434-130"> Dimensioonide lisamine readefinitsioonis</span><span class="sxs-lookup"><span data-stu-id="f9434-130">Add dimensions in a row definition</span></span>
<span data-ttu-id="f9434-131">Dimensioon on andmete ja väärtuste ühisosa.</span><span class="sxs-lookup"><span data-stu-id="f9434-131">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="f9434-132">Aruandekoosturis saab andmeid ja väärtusi rühmitada.</span><span class="sxs-lookup"><span data-stu-id="f9434-132">You can group data and values in report designer.</span></span> <span data-ttu-id="f9434-133">Seejärel saab kandeid üksikasjalikumalt liigitada ja analüüsida.</span><span class="sxs-lookup"><span data-stu-id="f9434-133">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="f9434-134">Saate kasutada dialoogiboksi **Ridade sisestamine dimensioonidest**, et lisada readefinitsiooni korraga mitu rida.</span><span class="sxs-lookup"><span data-stu-id="f9434-134">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="f9434-135">Dialoogiboksis kuvatakse iga dimensiooni puhul üks veerg.</span><span class="sxs-lookup"><span data-stu-id="f9434-135">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="f9434-136">Järgmine tabel kirjeldab teavet, mida saab iga dimensiooni kohta määrata.</span><span class="sxs-lookup"><span data-stu-id="f9434-136">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="f9434-137">Suvand</span><span class="sxs-lookup"><span data-stu-id="f9434-137">Option</span></span>                | <span data-ttu-id="f9434-138">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f9434-138">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="f9434-139">Dimensioon</span><span class="sxs-lookup"><span data-stu-id="f9434-139">Dimension</span></span>             | <span data-ttu-id="f9434-140">Muster, mis tuvastab readefinitsiooni lisatava dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="f9434-140">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="f9434-141">See muster sisaldab ühte ampersandi (&) või numbrimärki (\#) iga koha puhul dimensioonides.</span><span class="sxs-lookup"><span data-stu-id="f9434-141">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="f9434-142">Üldiselt kasutatakse kõiki ampersande põhikonto dimensiooni ja kõiki numbrimärke muude dimensioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="f9434-142">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="f9434-143">Dimensioonivahemiku algus</span><span class="sxs-lookup"><span data-stu-id="f9434-143">Dimension Range Start</span></span> | <span data-ttu-id="f9434-144">Readefinitsiooni lisatava dimensiooni esimene väärtus.</span><span class="sxs-lookup"><span data-stu-id="f9434-144">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="f9434-145">Dimensioonivahemiku lõpp</span><span class="sxs-lookup"><span data-stu-id="f9434-145">Dimension Range End</span></span>   | <span data-ttu-id="f9434-146">Viimane selle dimensiooni puhul readefinitsiooni lisatav väärtus.</span><span class="sxs-lookup"><span data-stu-id="f9434-146">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="f9434-147">Readefinitsiooni dimensioonide lisamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="f9434-147">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="f9434-148">Klõpsake aruandekoosturis valikut **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="f9434-148">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="f9434-149">Klõpsake menüüs **Redigeeri** suvandit **Sisesta read dimensioonidest**.</span><span class="sxs-lookup"><span data-stu-id="f9434-149">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="f9434-150">Valige dialoogiboksist **Ridade lisamine dimensioonidest** real **Dimensioonid** readefinitsiooni teisaldatava dimensiooni lahter ja seejärel klõpsake valikut **Kõik &&&**.</span><span class="sxs-lookup"><span data-stu-id="f9434-150">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="f9434-151">Readefinitsiooni piiramiseks dimensiooniväärtuste kindlasse vahemikku sisestage alguse dimensiooniväärtus lahtrisse **Dimensioonivahemiku algus** ja seejärel sisestage lõpu dimensiooniväärtus lahtrisse **Dimensioonivahemiku lõpp**.</span><span class="sxs-lookup"><span data-stu-id="f9434-151">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="f9434-152">Kõikide valitud dimensiooni väärtuste kaasamiseks jätke need lahtrid tühjaks.</span><span class="sxs-lookup"><span data-stu-id="f9434-152">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f9434-153">Kui dimensioonivahemikes on metamärke (\* ?), ei pruugi te olenevalt sellest, kuidas ERP andmebaas andmeid sordib, kõiki soovitud tulemusi saada.</span><span class="sxs-lookup"><span data-stu-id="f9434-153">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="f9434-154">Määrake väljal **Algrea kood** readefinitsiooni lisatava esimese dimensiooniväärtuse reakood.</span><span class="sxs-lookup"><span data-stu-id="f9434-154">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="f9434-155">Määrake väljal **Iga rea juurdekasv** järjestikuste reakoodide vahe.</span><span class="sxs-lookup"><span data-stu-id="f9434-155">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="f9434-156">Näiteks kui esimene reakood on 100 ja juurdekasvu väärtus on 30, on esimeste uute ridade koodideks 100, 130, 160, 190 ja 220.</span><span class="sxs-lookup"><span data-stu-id="f9434-156">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="f9434-157">Kasutage juurdekasvu väärtust, mis annab piisavalt ruumi uute vormingu ja valemi ridade lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="f9434-157">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="f9434-158">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9434-158">Click **OK**.</span></span> <span data-ttu-id="f9434-159">Readefinitsiooni lisatakse iga valitud dimensiooniväärtuse kohta üks rida.</span><span class="sxs-lookup"><span data-stu-id="f9434-159">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="f9434-160"> Readefinitsiooni ümardamise korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="f9434-160">Adjust rounding in a row definition</span></span>
<span data-ttu-id="f9434-161">Ümardatud summadega bilansi puhul ei pruugi kogusummad tasakaalus olla.</span><span class="sxs-lookup"><span data-stu-id="f9434-161">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="f9434-162">See probleem võib ilmneda, kui kasutate bilansiaruandes ümardamist ja aruande definitsioon määrab samuti ümardamise.</span><span class="sxs-lookup"><span data-stu-id="f9434-162">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="f9434-163">Võite kasutada valikut **Ümardamise korrigeerimine** readefinitsioonis bilansside summade tasakaalustamiseks.</span><span class="sxs-lookup"><span data-stu-id="f9434-163">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="f9434-164">Ümardamise saab välja lülitada või muuta seda aruandedefinitsiooni vahekaardil **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="f9434-164">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="f9434-165">Järgmises tabelis näidatakse, kuidas summasid ümardatakse.</span><span class="sxs-lookup"><span data-stu-id="f9434-165">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="f9434-166">Selles tabelis erinevad ridade 100 ja 200 kogusummad, kui ümardamine on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="f9434-166">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="f9434-167">Rea kood</span><span class="sxs-lookup"><span data-stu-id="f9434-167">Row code</span></span> | <span data-ttu-id="f9434-168">Summad ümardamata</span><span class="sxs-lookup"><span data-stu-id="f9434-168">Amounts without rounding</span></span> | <span data-ttu-id="f9434-169">Summa tuhandikeni ümardatuna</span><span class="sxs-lookup"><span data-stu-id="f9434-169">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="f9434-170">100</span><span class="sxs-lookup"><span data-stu-id="f9434-170">100</span></span>      | <span data-ttu-id="f9434-171">3,600</span><span class="sxs-lookup"><span data-stu-id="f9434-171">3,600</span></span>                    | <span data-ttu-id="f9434-172">4</span><span class="sxs-lookup"><span data-stu-id="f9434-172">4</span></span>                                       |
| <span data-ttu-id="f9434-173">200</span><span class="sxs-lookup"><span data-stu-id="f9434-173">200</span></span>      | <span data-ttu-id="f9434-174">3,700</span><span class="sxs-lookup"><span data-stu-id="f9434-174">3,700</span></span>                    | <span data-ttu-id="f9434-175">4</span><span class="sxs-lookup"><span data-stu-id="f9434-175">4</span></span>                                       |
| <span data-ttu-id="f9434-176">Kokku</span><span class="sxs-lookup"><span data-stu-id="f9434-176">Total</span></span>    | <span data-ttu-id="f9434-177">7,300</span><span class="sxs-lookup"><span data-stu-id="f9434-177">7,300</span></span>                    | <span data-ttu-id="f9434-178">8</span><span class="sxs-lookup"><span data-stu-id="f9434-178">8</span></span>                                       |

<span data-ttu-id="f9434-179">Bilansi ümardamise korrigeerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="f9434-179">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="f9434-180">Klõpsake aruande kujundajas suvandit **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="f9434-180">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="f9434-181">Klõpsake menüüs **Redigeeri** suvandit **Ümardusparandus**.</span><span class="sxs-lookup"><span data-stu-id="f9434-181">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="f9434-182">Sisestage dialoogiboksi **Ümardamise korrigeerimised** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f9434-182">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="f9434-183">**Ümardamise korrigeerimise rida** – bilansi tasakaalustamiseks korrigeeritava rea reakood.</span><span class="sxs-lookup"><span data-stu-id="f9434-183">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="f9434-184">**Koguvarade rida** – bilansis koguvarasid sisaldava rea reakood.</span><span class="sxs-lookup"><span data-stu-id="f9434-184">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="f9434-185">**Kogu kohustuste ja omakapitali rida** – bilansis kogu kohustusi ja omakapitali sisaldava rea reakood.</span><span class="sxs-lookup"><span data-stu-id="f9434-185">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="f9434-186">**Korrigeerimissumma limiit** – positiivne täisarv, mis määrab automaatsete korrigeerimiste limiidi.</span><span class="sxs-lookup"><span data-stu-id="f9434-186">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="f9434-187">Seda summat võrreldakse tegeliku ümardamise erinevuse absoluutväärtusega.</span><span class="sxs-lookup"><span data-stu-id="f9434-187">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f9434-188">Need reakoodid tuleb teie finantsandmetega siduda.</span><span class="sxs-lookup"><span data-stu-id="f9434-188">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="f9434-189">Teisisõnu peab real olema lahtris **Link finantsdimensioonidele** dimensiooniväärtus.</span><span class="sxs-lookup"><span data-stu-id="f9434-189">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="f9434-190">**Ärge** viidake kirjelduse (**DESC**), arvutatud (**CALC**) või summeeritud (**TOT**) reale.</span><span class="sxs-lookup"><span data-stu-id="f9434-190">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="f9434-191">Teie bilansi summad tasakaalustatakse nüüd ümardamise sisselülitamisel võrdselt.</span><span class="sxs-lookup"><span data-stu-id="f9434-191">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="f9434-192">Korrigeerimise piirangut kohaldatakse aruande definitsiooni puhul määratud suvandi **Ümardamistäpsus** põhjal.</span><span class="sxs-lookup"><span data-stu-id="f9434-192">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="f9434-193">Näiteks kui valite aruande ümardamise tuhandikeni ja sisestate arvu **2** väljale **Korrigeerimissumma limiit**, kuvatakse hoiatusteade, kui välja **Ümardamise korrigeerimise rida** väärtus suureneb või väheneb rohkem kui 2,000.</span><span class="sxs-lookup"><span data-stu-id="f9434-193">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="f9434-194">Ridade ja veergude teksti vormindamine</span><span class="sxs-lookup"><span data-stu-id="f9434-194">Format row and column text</span></span>
<span data-ttu-id="f9434-195">Saate kohandada aruannete ilmet fontide muutmise ja teksti vormindamise teel.</span><span class="sxs-lookup"><span data-stu-id="f9434-195">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="f9434-196">Järgmistes jaotistes selgitatakse, kuidas aruannetes ridade ja veergude ilmet vormindada.</span><span class="sxs-lookup"><span data-stu-id="f9434-196">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="f9434-197">Kirjatüüpide haldamine</span><span class="sxs-lookup"><span data-stu-id="f9434-197">Manage font styles</span></span>

<span data-ttu-id="f9434-198">Saate aruande fondilaade luua ja muuta.</span><span class="sxs-lookup"><span data-stu-id="f9434-198">You can create and modify font styles for your report.</span></span> <span data-ttu-id="f9434-199">Seejärel saab rakendada need laadid dokumendile või aruande konkreetsele reale või veerule.</span><span class="sxs-lookup"><span data-stu-id="f9434-199">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="f9434-200"><strong>Kirjatüübi loomine</strong></span><span class="sxs-lookup"><span data-stu-id="f9434-200"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="f9434-201">Klõpsake aruande kujundaja menüüs <strong>Vorming </strong>suvandit <strong>Laadid ja vorming</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9434-201">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="f9434-202">Klõpsake dialoogiboksis <strong>Laadid ja vormindamine</strong> suvandit <strong>Uus</strong> ning seejärel sisestage uuele laadile kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="f9434-202">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="f9434-203">Tehke fondivalikud ja seejärel klõpsake suvandit <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9434-203">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="f9434-204"><strong>Fondi laadi muutmine</strong></span><span class="sxs-lookup"><span data-stu-id="f9434-204"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="f9434-205">Klõpsake aruande kujundaja menüüs <strong>Vorming </strong>suvandit <strong>Laadid ja vorming</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9434-205">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="f9434-206">Valige muudetav laad dialoogiboksist <strong>Laadid ja vormindamine</strong> ja klõpsake seejärel suvandit <strong>Muuda</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9434-206">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="f9434-207">Tehke fondivalikud ja seejärel klõpsake suvandit <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="f9434-207">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="f9434-208"><strong>Kirjatüübi rakendamine</strong></span><span class="sxs-lookup"><span data-stu-id="f9434-208"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="f9434-209">Valige aruandekoosturi definitsioonis või veeru definitsioonis või päistes ja jalustes vähemalt üks lahter.</span><span class="sxs-lookup"><span data-stu-id="f9434-209">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="f9434-210">Valige tööriistaribal olevast loendist <strong>Laad</strong> fondi laad.</span><span class="sxs-lookup"><span data-stu-id="f9434-210">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="f9434-211">Rea teksti vormindamine</span><span class="sxs-lookup"><span data-stu-id="f9434-211">Format row text</span></span>

<span data-ttu-id="f9434-212">Readefinitsioonis määratud vorming alistab veeru- ja aruande definitsioonis määratud vormingu.</span><span class="sxs-lookup"><span data-stu-id="f9434-212">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="f9434-213">Saate tekstivormingut muuta, kasutades vormindamise tööriistariba nuppe.</span><span class="sxs-lookup"><span data-stu-id="f9434-213">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="f9434-214">Need juhtelemendid on standardsed Microsoft Windowsi juhtelemendid.</span><span class="sxs-lookup"><span data-stu-id="f9434-214">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="f9434-215">Avage aruande kujundajas muudetav readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="f9434-215">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="f9434-216">Valige vormindatavad lahtrid.</span><span class="sxs-lookup"><span data-stu-id="f9434-216">Select the cells to format.</span></span> <span data-ttu-id="f9434-217">Mitme lahtri valimiseks hoidke lahtri valimisel all klahvi Ctrl.</span><span class="sxs-lookup"><span data-stu-id="f9434-217">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="f9434-218">Vormingu rakendamiseks klõpsake tööriistariba nuppu.</span><span class="sxs-lookup"><span data-stu-id="f9434-218">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="f9434-219">Näiteks rea taandamiseks valige rida ja seejärel klõpsake tööriistariba ikooni **Suurenda taanet** ![Suurenda taanet](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Suurenda taanet").</span><span class="sxs-lookup"><span data-stu-id="f9434-219">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="f9434-220">Veergude korrigeerimine aruannete kujundamisel</span><span class="sxs-lookup"><span data-stu-id="f9434-220">Adjust columns while you design reports</span></span>

<span data-ttu-id="f9434-221">Nende veergude vaatamise lihtsustamiseks, mille kallal readefinitsioonis töötate, saate korrigeerida veeru laiust ning samuti peita (minimeerida) või kuvada veerge vaatepaanil.</span><span class="sxs-lookup"><span data-stu-id="f9434-221">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="f9434-222">Tehtavad muudatused mõjutavad ainult veergude ilmet ekraanil.</span><span class="sxs-lookup"><span data-stu-id="f9434-222">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="f9434-223">Need ei mõjuta veeru vormindust aruannetes.</span><span class="sxs-lookup"><span data-stu-id="f9434-223">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="f9434-224">Veeru laiuse muutmine vaatepaanil</span><span class="sxs-lookup"><span data-stu-id="f9434-224">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="f9434-225">Avage aruande kujundajas muudetav readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="f9434-225">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="f9434-226">Valige menüüs **Vorming** suvand **Veeru laius**.</span><span class="sxs-lookup"><span data-stu-id="f9434-226">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="f9434-227">Sisestage dialoogiboksi **Veeru laius** väärtus ja klõpsake siis nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9434-227">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="f9434-228">Teine võimalus on lohistada veeru laiuse muutmiseks veeru päise lahtri paremat äärt.</span><span class="sxs-lookup"><span data-stu-id="f9434-228">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="f9434-229">Veergude peitmine vaatepaanil</span><span class="sxs-lookup"><span data-stu-id="f9434-229">Hide columns in the view pane</span></span>

1. <span data-ttu-id="f9434-230">Avage aruande kujundajas muudetav readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="f9434-230">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="f9434-231">Valige minimeeritav(ad) veerg (veerud).</span><span class="sxs-lookup"><span data-stu-id="f9434-231">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="f9434-232">Paremklõpsake ja seejärel klõpsake suvandit **Peida**.</span><span class="sxs-lookup"><span data-stu-id="f9434-232">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="f9434-233">Kõikide peidetud veergude kuvamine vaatepaanil</span><span class="sxs-lookup"><span data-stu-id="f9434-233">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="f9434-234">Avage aruande kujundajas muudetav readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="f9434-234">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="f9434-235">Paremklõpsake kuvatavat minimeeritud veergu ja klõpsake seejärel valikut **Kuva**.</span><span class="sxs-lookup"><span data-stu-id="f9434-235">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="f9434-236">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f9434-236">Additional resources</span></span>

[<span data-ttu-id="f9434-237">Finantsaruandlus</span><span class="sxs-lookup"><span data-stu-id="f9434-237">Financial reporting</span></span>](financial-reporting-intro.md)

