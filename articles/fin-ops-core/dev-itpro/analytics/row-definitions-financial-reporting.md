---
title: Readefinitsioonid finantsaruande koosturis
description: Readefinitsioon on aruande komponent (koosteüksus), mis määrab finantsaruandel iga rea sisu.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: dfce0f1622d45dcf77d91b71abbe9e33e8c91ad0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564027"
---
# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="25375-103">Readefinitsioonid finantsaruande koosturis</span><span class="sxs-lookup"><span data-stu-id="25375-103">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25375-104">Readefinitsioon on aruande komponent (koosteüksus), mis määrab finantsaruandel iga rea sisu.</span><span class="sxs-lookup"><span data-stu-id="25375-104">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="25375-105">Readefinitsiooni saab kombineerida veerudefinitsioonide, aruandluspuu definitsioonide ja aruande definitsioonidega koosteüksuste grupi loomiseks, mida saavad kasutada mitu ettevõtet.</span><span class="sxs-lookup"><span data-stu-id="25375-105">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="25375-106">Readefinitsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="25375-106">Create a row definition</span></span>

1. <span data-ttu-id="25375-107">Klõpsake aruandekoosturis navigeerimispaanil suvandit **Readefinitsioonid**.</span><span class="sxs-lookup"><span data-stu-id="25375-107">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="25375-108">Klõpsake menüüs **Fail** valikut **Uus** ja seejärel valikut **Readefinitsioon**.</span><span class="sxs-lookup"><span data-stu-id="25375-108">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="25375-109">Lisateabe saamiseks iga lahtri sisu kohta vt osa [Readefinitsiooni lahtrite muutmine](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="25375-109">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="25375-110">Readefinitsiooni avamine</span><span class="sxs-lookup"><span data-stu-id="25375-110">Open a row definition</span></span>
1. <span data-ttu-id="25375-111">Klõpsake aruandekoosturis navigeerimispaanil suvandit **Readefinitsioonid**.</span><span class="sxs-lookup"><span data-stu-id="25375-111">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="25375-112">Avamiseks topeltklõpsake readefinitsiooni nime.</span><span class="sxs-lookup"><span data-stu-id="25375-112">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="25375-113">Mis tahes readefinitsiooniga seostatud koosteüksuse vaatamiseks paremklõpsake readefinitsiooni ja seejärel valige **Seosed**.</span><span class="sxs-lookup"><span data-stu-id="25375-113">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="25375-114"> Readefinitsiooni sisu</span><span class="sxs-lookup"><span data-stu-id="25375-114">Contents of a row definition</span></span>
<span data-ttu-id="25375-115">Readefinitsioon võib sisaldada kuni 20 000 finantsdimensiooni rida ja võib sisaldada järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="25375-115">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="25375-116">Kirjeldav tekst, mis lisab aruandele tähenduse, luues jaotise päiseid, ridu ja tühikuid, nt **Sularaha** või **Kogutulu**</span><span class="sxs-lookup"><span data-stu-id="25375-116">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="25375-117">Lingid finantsandmete juurde, mille hulka võivad kuuluda Microsoft Dynamics 365 Financei dimensiooniväärtused</span><span class="sxs-lookup"><span data-stu-id="25375-117">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 Finance</span></span>

    > [!NOTE]
    > <span data-ttu-id="25375-118">Saate readefinitsiooni nii seadistada, et see võtab iga kord, kui aruanne luuakse, finantsdimensiooni süsteemist andmeid.</span><span class="sxs-lookup"><span data-stu-id="25375-118">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="25375-119">Ridade kogusummad ja valemid, mis põhinevad lingitud finantsandmetel</span><span class="sxs-lookup"><span data-stu-id="25375-119">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="25375-120">Üldjuhul sisaldab iga readefinitsioon üht järgmist tüüpi teavet.</span><span class="sxs-lookup"><span data-stu-id="25375-120">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="25375-121">Viited finantsdimensioonide süsteemile</span><span class="sxs-lookup"><span data-stu-id="25375-121">References to the financial dimensions system</span></span>
- <span data-ttu-id="25375-122">Andmetel põhinevad kogusummad või arvutused</span><span class="sxs-lookup"><span data-stu-id="25375-122">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="25375-123">Vormindus</span><span class="sxs-lookup"><span data-stu-id="25375-123">Formatting</span></span>

<span data-ttu-id="25375-124">Readefinitsiooni teabe sisestamiseks on kaks viisi.</span><span class="sxs-lookup"><span data-stu-id="25375-124">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="25375-125">Rea teabe käsitsi sisestamine uude readefinitsiooni.</span><span class="sxs-lookup"><span data-stu-id="25375-125">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="25375-126">Lisateabe saamiseks vt osa [Readefinitsiooni lahtrite muutmine](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="25375-126">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="25375-127">Kasutage aruandekoosturit rea teabe toomiseks otse finantsdimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="25375-127">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="25375-128">Lisateavet leiate jaotisest Seotud valemid/read/üksused osas [Readefinitsiooni lahtrite muutmine](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="25375-128">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="25375-129"> Dimensioonide lisamine readefinitsioonis</span><span class="sxs-lookup"><span data-stu-id="25375-129">Add dimensions in a row definition</span></span>
<span data-ttu-id="25375-130">Dimensioon on andmete ja väärtuste ühisosa.</span><span class="sxs-lookup"><span data-stu-id="25375-130">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="25375-131">Aruandekoosturis saab andmeid ja väärtusi rühmitada.</span><span class="sxs-lookup"><span data-stu-id="25375-131">You can group data and values in report designer.</span></span> <span data-ttu-id="25375-132">Seejärel saab kandeid üksikasjalikumalt liigitada ja analüüsida.</span><span class="sxs-lookup"><span data-stu-id="25375-132">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="25375-133">Saate kasutada dialoogiboksi **Ridade sisestamine dimensioonidest**, et lisada readefinitsiooni korraga mitu rida.</span><span class="sxs-lookup"><span data-stu-id="25375-133">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="25375-134">Dialoogiboksis kuvatakse iga dimensiooni puhul üks veerg.</span><span class="sxs-lookup"><span data-stu-id="25375-134">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="25375-135">Järgmine tabel kirjeldab teavet, mida saab iga dimensiooni kohta määrata.</span><span class="sxs-lookup"><span data-stu-id="25375-135">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="25375-136">Suvand</span><span class="sxs-lookup"><span data-stu-id="25375-136">Option</span></span>                | <span data-ttu-id="25375-137">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="25375-137">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="25375-138">Dimensioon</span><span class="sxs-lookup"><span data-stu-id="25375-138">Dimension</span></span>             | <span data-ttu-id="25375-139">Muster, mis tuvastab readefinitsiooni lisatava dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="25375-139">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="25375-140">See muster sisaldab ühte ampersandi (&) või numbrimärki (\#) iga koha puhul dimensioonides.</span><span class="sxs-lookup"><span data-stu-id="25375-140">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="25375-141">Üldiselt kasutatakse kõiki ampersande põhikonto dimensiooni ja kõiki numbrimärke muude dimensioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="25375-141">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="25375-142">Dimensioonivahemiku algus</span><span class="sxs-lookup"><span data-stu-id="25375-142">Dimension Range Start</span></span> | <span data-ttu-id="25375-143">Readefinitsiooni lisatava dimensiooni esimene väärtus.</span><span class="sxs-lookup"><span data-stu-id="25375-143">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="25375-144">Dimensioonivahemiku lõpp</span><span class="sxs-lookup"><span data-stu-id="25375-144">Dimension Range End</span></span>   | <span data-ttu-id="25375-145">Viimane selle dimensiooni puhul readefinitsiooni lisatav väärtus.</span><span class="sxs-lookup"><span data-stu-id="25375-145">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="25375-146">Readefinitsiooni dimensioonide lisamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="25375-146">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="25375-147">Klõpsake aruandekoosturis valikut **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="25375-147">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="25375-148">Klõpsake menüüs **Redigeeri** suvandit **Sisesta read dimensioonidest**.</span><span class="sxs-lookup"><span data-stu-id="25375-148">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="25375-149">Valige dialoogiboksist **Ridade lisamine dimensioonidest** real **Dimensioonid** readefinitsiooni teisaldatava dimensiooni lahter ja seejärel klõpsake valikut **Kõik &&&**.</span><span class="sxs-lookup"><span data-stu-id="25375-149">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="25375-150">Readefinitsiooni piiramiseks dimensiooniväärtuste kindlasse vahemikku sisestage alguse dimensiooniväärtus lahtrisse **Dimensioonivahemiku algus** ja seejärel sisestage lõpu dimensiooniväärtus lahtrisse **Dimensioonivahemiku lõpp**.</span><span class="sxs-lookup"><span data-stu-id="25375-150">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="25375-151">Kõikide valitud dimensiooni väärtuste kaasamiseks jätke need lahtrid tühjaks.</span><span class="sxs-lookup"><span data-stu-id="25375-151">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25375-152">Kui dimensioonivahemikes on metamärke (\* ?), ei pruugi te olenevalt sellest, kuidas ERP andmebaas andmeid sordib, kõiki soovitud tulemusi saada.</span><span class="sxs-lookup"><span data-stu-id="25375-152">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="25375-153">Määrake väljal **Algrea kood** readefinitsiooni lisatava esimese dimensiooniväärtuse reakood.</span><span class="sxs-lookup"><span data-stu-id="25375-153">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="25375-154">Määrake väljal **Iga rea juurdekasv** järjestikuste reakoodide vahe.</span><span class="sxs-lookup"><span data-stu-id="25375-154">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="25375-155">Näiteks kui esimene reakood on 100 ja juurdekasvu väärtus on 30, on esimeste uute ridade koodideks 100, 130, 160, 190 ja 220.</span><span class="sxs-lookup"><span data-stu-id="25375-155">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="25375-156">Kasutage juurdekasvu väärtust, mis annab piisavalt ruumi uute vormingu ja valemi ridade lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="25375-156">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="25375-157">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="25375-157">Click **OK**.</span></span> <span data-ttu-id="25375-158">Readefinitsiooni lisatakse iga valitud dimensiooniväärtuse kohta üks rida.</span><span class="sxs-lookup"><span data-stu-id="25375-158">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="25375-159"> Readefinitsiooni ümardamise korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="25375-159">Adjust rounding in a row definition</span></span>
<span data-ttu-id="25375-160">Ümardatud summadega bilansi puhul ei pruugi kogusummad tasakaalus olla.</span><span class="sxs-lookup"><span data-stu-id="25375-160">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="25375-161">See probleem võib ilmneda, kui kasutate bilansiaruandes ümardamist ja aruande definitsioon määrab samuti ümardamise.</span><span class="sxs-lookup"><span data-stu-id="25375-161">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="25375-162">Võite kasutada valikut **Ümardamise korrigeerimine** readefinitsioonis bilansside summade tasakaalustamiseks.</span><span class="sxs-lookup"><span data-stu-id="25375-162">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="25375-163">Ümardamise saab välja lülitada või muuta seda aruandedefinitsiooni vahekaardil **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="25375-163">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="25375-164">Järgmises tabelis näidatakse, kuidas summasid ümardatakse.</span><span class="sxs-lookup"><span data-stu-id="25375-164">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="25375-165">Selles tabelis erinevad ridade 100 ja 200 kogusummad, kui ümardamine on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="25375-165">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="25375-166">Rea kood</span><span class="sxs-lookup"><span data-stu-id="25375-166">Row code</span></span> | <span data-ttu-id="25375-167">Summad ümardamata</span><span class="sxs-lookup"><span data-stu-id="25375-167">Amounts without rounding</span></span> | <span data-ttu-id="25375-168">Summa tuhandikeni ümardatuna</span><span class="sxs-lookup"><span data-stu-id="25375-168">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="25375-169">100</span><span class="sxs-lookup"><span data-stu-id="25375-169">100</span></span>      | <span data-ttu-id="25375-170">3,600</span><span class="sxs-lookup"><span data-stu-id="25375-170">3,600</span></span>                    | <span data-ttu-id="25375-171">4</span><span class="sxs-lookup"><span data-stu-id="25375-171">4</span></span>                                       |
| <span data-ttu-id="25375-172">200</span><span class="sxs-lookup"><span data-stu-id="25375-172">200</span></span>      | <span data-ttu-id="25375-173">3,700</span><span class="sxs-lookup"><span data-stu-id="25375-173">3,700</span></span>                    | <span data-ttu-id="25375-174">4</span><span class="sxs-lookup"><span data-stu-id="25375-174">4</span></span>                                       |
| <span data-ttu-id="25375-175">Kokku</span><span class="sxs-lookup"><span data-stu-id="25375-175">Total</span></span>    | <span data-ttu-id="25375-176">7,300</span><span class="sxs-lookup"><span data-stu-id="25375-176">7,300</span></span>                    | <span data-ttu-id="25375-177">8</span><span class="sxs-lookup"><span data-stu-id="25375-177">8</span></span>                                       |

<span data-ttu-id="25375-178">Bilansi ümardamise korrigeerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="25375-178">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="25375-179">Klõpsake aruande kujundajas suvandit **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="25375-179">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="25375-180">Klõpsake menüüs **Redigeeri** suvandit **Ümardusparandus**.</span><span class="sxs-lookup"><span data-stu-id="25375-180">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="25375-181">Sisestage dialoogiboksi **Ümardamise korrigeerimised** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="25375-181">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="25375-182">**Ümardamise korrigeerimise rida** – bilansi tasakaalustamiseks korrigeeritava rea reakood.</span><span class="sxs-lookup"><span data-stu-id="25375-182">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="25375-183">**Koguvarade rida** – bilansis koguvarasid sisaldava rea reakood.</span><span class="sxs-lookup"><span data-stu-id="25375-183">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="25375-184">**Kogu kohustuste ja omakapitali rida** – bilansis kogu kohustusi ja omakapitali sisaldava rea reakood.</span><span class="sxs-lookup"><span data-stu-id="25375-184">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="25375-185">**Korrigeerimissumma limiit** – positiivne täisarv, mis määrab automaatsete korrigeerimiste limiidi.</span><span class="sxs-lookup"><span data-stu-id="25375-185">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="25375-186">Seda summat võrreldakse tegeliku ümardamise erinevuse absoluutväärtusega.</span><span class="sxs-lookup"><span data-stu-id="25375-186">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25375-187">Need reakoodid tuleb teie finantsandmetega siduda.</span><span class="sxs-lookup"><span data-stu-id="25375-187">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="25375-188">Teisisõnu peab real olema lahtris **Link finantsdimensioonidele** dimensiooniväärtus.</span><span class="sxs-lookup"><span data-stu-id="25375-188">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="25375-189">**Ärge** viidake kirjelduse (**DESC**), arvutatud (**CALC**) või summeeritud (**TOT**) reale.</span><span class="sxs-lookup"><span data-stu-id="25375-189">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="25375-190">Teie bilansi summad tasakaalustatakse nüüd ümardamise sisselülitamisel võrdselt.</span><span class="sxs-lookup"><span data-stu-id="25375-190">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="25375-191">Korrigeerimise piirangut kohaldatakse aruande definitsiooni puhul määratud suvandi **Ümardamistäpsus** põhjal.</span><span class="sxs-lookup"><span data-stu-id="25375-191">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="25375-192">Näiteks kui valite aruande ümardamise tuhandikeni ja sisestate arvu **2** väljale **Korrigeerimissumma limiit**, kuvatakse hoiatusteade, kui välja **Ümardamise korrigeerimise rida** väärtus suureneb või väheneb rohkem kui 2,000.</span><span class="sxs-lookup"><span data-stu-id="25375-192">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="25375-193">Ridade ja veergude teksti vormindamine</span><span class="sxs-lookup"><span data-stu-id="25375-193">Format row and column text</span></span>
<span data-ttu-id="25375-194">Saate kohandada aruannete ilmet fontide muutmise ja teksti vormindamise teel.</span><span class="sxs-lookup"><span data-stu-id="25375-194">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="25375-195">Järgmistes jaotistes selgitatakse, kuidas aruannetes ridade ja veergude ilmet vormindada.</span><span class="sxs-lookup"><span data-stu-id="25375-195">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="25375-196">Kirjatüüpide haldamine</span><span class="sxs-lookup"><span data-stu-id="25375-196">Manage font styles</span></span>

<span data-ttu-id="25375-197">Saate aruande fondilaade luua ja muuta.</span><span class="sxs-lookup"><span data-stu-id="25375-197">You can create and modify font styles for your report.</span></span> <span data-ttu-id="25375-198">Seejärel saab rakendada need laadid dokumendile või aruande konkreetsele reale või veerule.</span><span class="sxs-lookup"><span data-stu-id="25375-198">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="25375-199"><strong>Kirjatüübi loomine</strong></span><span class="sxs-lookup"><span data-stu-id="25375-199"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="25375-200">Klõpsake aruande kujundaja menüüs <strong>Vorming </strong>suvandit <strong>Laadid ja vorming</strong>.</span><span class="sxs-lookup"><span data-stu-id="25375-200">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="25375-201">Klõpsake dialoogiboksis <strong>Laadid ja vormindamine</strong> suvandit <strong>Uus</strong> ning seejärel sisestage uuele laadile kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="25375-201">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="25375-202">Tehke fondivalikud ja seejärel klõpsake suvandit <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="25375-202">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="25375-203"><strong>Fondi laadi muutmine</strong></span><span class="sxs-lookup"><span data-stu-id="25375-203"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="25375-204">Klõpsake aruande kujundaja menüüs <strong>Vorming </strong>suvandit <strong>Laadid ja vorming</strong>.</span><span class="sxs-lookup"><span data-stu-id="25375-204">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="25375-205">Valige muudetav laad dialoogiboksist <strong>Laadid ja vormindamine</strong> ja klõpsake seejärel suvandit <strong>Muuda</strong>.</span><span class="sxs-lookup"><span data-stu-id="25375-205">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="25375-206">Tehke fondivalikud ja seejärel klõpsake suvandit <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="25375-206">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="25375-207"><strong>Kirjatüübi rakendamine</strong></span><span class="sxs-lookup"><span data-stu-id="25375-207"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="25375-208">Valige aruandekoosturi definitsioonis või veeru definitsioonis või päistes ja jalustes vähemalt üks lahter.</span><span class="sxs-lookup"><span data-stu-id="25375-208">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="25375-209">Valige tööriistaribal olevast loendist <strong>Laad</strong> fondi laad.</span><span class="sxs-lookup"><span data-stu-id="25375-209">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="25375-210">Rea teksti vormindamine</span><span class="sxs-lookup"><span data-stu-id="25375-210">Format row text</span></span>

<span data-ttu-id="25375-211">Readefinitsioonis määratud vorming alistab veeru- ja aruande definitsioonis määratud vormingu.</span><span class="sxs-lookup"><span data-stu-id="25375-211">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="25375-212">Saate tekstivormingut muuta, kasutades vormindamise tööriistariba nuppe.</span><span class="sxs-lookup"><span data-stu-id="25375-212">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="25375-213">Tegemist on Microsoft Windowsi standardsete juhtelementidega.</span><span class="sxs-lookup"><span data-stu-id="25375-213">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="25375-214">Avage aruandekoosturis muudetav readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="25375-214">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="25375-215">Valige vormindatavad lahtrid.</span><span class="sxs-lookup"><span data-stu-id="25375-215">Select the cells to format.</span></span> <span data-ttu-id="25375-216">Mitme lahtri valimiseks hoidke lahtri valimisel all klahvi Ctrl.</span><span class="sxs-lookup"><span data-stu-id="25375-216">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="25375-217">Vormingu rakendamiseks klõpsake tööriistariba nuppu.</span><span class="sxs-lookup"><span data-stu-id="25375-217">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="25375-218">Näiteks rea taandamiseks valige rida ja seejärel klõpsake tööriistariba ikooni **Suurenda taanet** ![Suurenda taanet](media/indent.gif "Suurenda taanet").</span><span class="sxs-lookup"><span data-stu-id="25375-218">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](media/indent.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="25375-219">Veergude korrigeerimine aruannete kujundamisel</span><span class="sxs-lookup"><span data-stu-id="25375-219">Adjust columns while you design reports</span></span>

<span data-ttu-id="25375-220">Nende veergude vaatamise lihtsustamiseks, mille kallal readefinitsioonis töötate, saate korrigeerida veeru laiust ning samuti peita (minimeerida) või kuvada veerge vaatepaanil.</span><span class="sxs-lookup"><span data-stu-id="25375-220">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="25375-221">Tehtavad muudatused mõjutavad ainult veergude ilmet ekraanil.</span><span class="sxs-lookup"><span data-stu-id="25375-221">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="25375-222">Need ei mõjuta veeru vormindust aruannetes.</span><span class="sxs-lookup"><span data-stu-id="25375-222">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="25375-223">Veeru laiuse muutmine vaatepaanil</span><span class="sxs-lookup"><span data-stu-id="25375-223">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="25375-224">Avage aruande kujundajas muudetav readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="25375-224">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="25375-225">Valige menüüs **Vorming** suvand **Veeru laius**.</span><span class="sxs-lookup"><span data-stu-id="25375-225">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="25375-226">Sisestage dialoogiboksi **Veeru laius** väärtus ja klõpsake siis nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="25375-226">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="25375-227">Teine võimalus on lohistada veeru laiuse muutmiseks veeru päise lahtri paremat äärt.</span><span class="sxs-lookup"><span data-stu-id="25375-227">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="25375-228">Veergude peitmine vaatepaanil</span><span class="sxs-lookup"><span data-stu-id="25375-228">Hide columns in the view pane</span></span>

1. <span data-ttu-id="25375-229">Avage aruande kujundajas muudetav readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="25375-229">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="25375-230">Valige minimeeritav(ad) veerg (veerud).</span><span class="sxs-lookup"><span data-stu-id="25375-230">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="25375-231">Paremklõpsake ja seejärel klõpsake suvandit **Peida**.</span><span class="sxs-lookup"><span data-stu-id="25375-231">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="25375-232">Kõikide peidetud veergude kuvamine vaatepaanil</span><span class="sxs-lookup"><span data-stu-id="25375-232">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="25375-233">Avage aruande kujundajas muudetav readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="25375-233">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="25375-234">Paremklõpsake kuvatavat minimeeritud veergu ja klõpsake seejärel valikut **Kuva**.</span><span class="sxs-lookup"><span data-stu-id="25375-234">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="25375-235">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="25375-235">Additional resources</span></span>

[<span data-ttu-id="25375-236">Finantsaruandlus</span><span class="sxs-lookup"><span data-stu-id="25375-236">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]