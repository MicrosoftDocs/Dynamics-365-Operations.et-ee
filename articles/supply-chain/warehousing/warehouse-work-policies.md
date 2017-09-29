---
title: "Lao tööpoliitikad"
description: "Laotöö poliitikad juhivad seda, kas laotöö luuakse tootmises laoprotsessidega töötellimuse tüübi, varude asukoha ja toote põhjal."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ec7dd3b91851729e866bc90ca85a118839f9d71d
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="warehouse-work-policies"></a><span data-ttu-id="cac87-103">Lao tööpoliitikad</span><span class="sxs-lookup"><span data-stu-id="cac87-103">Warehouse work policies</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cac87-104">Laotöö poliitikad Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis juhivad seda, kas laotöö luuakse tootmises laoprotsessidega töötellimuse tüübi, varude asukoha ja toote põhjal.</span><span class="sxs-lookup"><span data-stu-id="cac87-104">Warehouse work policies in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="cac87-105">See tööpoliitika kontrollib, kas laotöö luuakse tootmises laoprotsesside jaoks.</span><span class="sxs-lookup"><span data-stu-id="cac87-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="cac87-106">Saate seadistada tööpoliitika, kasutades **töötellimuse tüüpide**, **lao asukoha** ja **toote** kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="cac87-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="cac87-107">Näiteks toode L0101 teatatakse väljundasukohas 001 lõpetatuks.</span><span class="sxs-lookup"><span data-stu-id="cac87-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="cac87-108">Lõpetatud kaupa tarbitakse hiljem teises tootmistellimuses väljastuskohaga 001.</span><span class="sxs-lookup"><span data-stu-id="cac87-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="cac87-109">Sellisel juhul saate seadistada tööpoliitika, et takistada lõpetatud kaupade kõrvalepaneku jaoks töö loomist, kui teatate toote L0101 väljastuskohas 001 lõpetatuks.</span><span class="sxs-lookup"><span data-stu-id="cac87-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="cac87-110">Tööpoliitika on individuaalne üksus, mida saab kirjeldada järgmise teabe kaudu.</span><span class="sxs-lookup"><span data-stu-id="cac87-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="cac87-111">**Tööpoliitika nimi**(tööpoliitika kordumatu identifikaator)</span><span class="sxs-lookup"><span data-stu-id="cac87-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="cac87-112">**Töötellimuse tüübid** ja **Töö loomise meetod**</span><span class="sxs-lookup"><span data-stu-id="cac87-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="cac87-113">**Lao asukohad**</span><span class="sxs-lookup"><span data-stu-id="cac87-113">**Inventory locations**</span></span>
-   <span data-ttu-id="cac87-114">**tooted.**</span><span class="sxs-lookup"><span data-stu-id="cac87-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="cac87-115">Töötellimuse tüübid</span><span class="sxs-lookup"><span data-stu-id="cac87-115">Work order types</span></span>
<span data-ttu-id="cac87-116">Saate valida järgmised töötellimuse tüübid.</span><span class="sxs-lookup"><span data-stu-id="cac87-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="cac87-117">Lõpetatud kaupade kõrvalepanek</span><span class="sxs-lookup"><span data-stu-id="cac87-117">Finished goods put away</span></span>
-   <span data-ttu-id="cac87-118">Kaastoodete ja kõrvalsaaduste kõrvalepanek</span><span class="sxs-lookup"><span data-stu-id="cac87-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="cac87-119">Toormaterjalide komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="cac87-119">Raw material picking</span></span>

<span data-ttu-id="cac87-120">Väljal **Töö loomise meetod** on väärtus **Mitte kunagi**.</span><span class="sxs-lookup"><span data-stu-id="cac87-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="cac87-121">See väärtus näitab, et tööpoliitika takistab laotöö loomist valitud töötellimuse tüübi jaoks.</span><span class="sxs-lookup"><span data-stu-id="cac87-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="cac87-122">Lao asukohad</span><span class="sxs-lookup"><span data-stu-id="cac87-122">Inventory locations</span></span>
<span data-ttu-id="cac87-123">Saate valida asukoha, millele tööpoliitika rakendub.</span><span class="sxs-lookup"><span data-stu-id="cac87-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="cac87-124">Kui tööpoliitikaga ei seostu ühtki asukohta, siis ei rakendu tööpoliitika ühelegi protsessile.</span><span class="sxs-lookup"><span data-stu-id="cac87-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="cac87-125">Lehel **Asukohad** saate ka valida või tühistada tööpoliitika valimise teatud asukohas.</span><span class="sxs-lookup"><span data-stu-id="cac87-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="cac87-126">Tooted</span><span class="sxs-lookup"><span data-stu-id="cac87-126">Products</span></span>
<span data-ttu-id="cac87-127">Saate valida toote, millele tööpoliitika rakendub.</span><span class="sxs-lookup"><span data-stu-id="cac87-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="cac87-128">Saate rakendada tööpoliitika kõikidele toodetele või valitud toodetele.</span><span class="sxs-lookup"><span data-stu-id="cac87-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="cac87-129">Näide</span><span class="sxs-lookup"><span data-stu-id="cac87-129">Example</span></span>
<span data-ttu-id="cac87-130">Järgmises näites on kaks tootmistellimust: PRD-001 ja PRD-00*2*.</span><span class="sxs-lookup"><span data-stu-id="cac87-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="cac87-131">Tootmistellimusel PRD-001 on toiming nimega **Assembler**, kus toode SC1 on teatatud lõpetatuks asukohale O1.</span><span class="sxs-lookup"><span data-stu-id="cac87-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="cac87-132">Tootmistellimusel PRD-002 on toiming nimega **Värvimine** ja tarbib toodet SC1 asukohast O1.</span><span class="sxs-lookup"><span data-stu-id="cac87-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="cac87-133">Tootmistellimus PRD-002 tarbib ka toormaterjali RM1 asukohast O1.</span><span class="sxs-lookup"><span data-stu-id="cac87-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="cac87-134">RM1-d hoitakse laoasukohas BULK-001 ja komplekteeritakse asukohale O1 laotööga toormaterjali komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="cac87-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="cac87-135">Komplekteerimistöö luuakse tootmise PRD-002 väljastamisel.</span><span class="sxs-lookup"><span data-stu-id="cac87-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="cac87-136">[![Lao tööpoliitikad](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="cac87-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="cac87-137">Kui plaanite selle stsenaariumi jaoks konfigureerida lao tööpoliitika, peaksite arvestama järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="cac87-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="cac87-138">Laotöö pole lõpetatud kaupade kõrvalepanekuks vajalik, kui teatate toote SC1 lõpetatuks tootmistellimusest PRD-001 asukohale O1.</span><span class="sxs-lookup"><span data-stu-id="cac87-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="cac87-139">Seda seetõttu, et tootmistellimuse PRD-002 toiming **Värvimine** tarbib samas asukohas SC1.</span><span class="sxs-lookup"><span data-stu-id="cac87-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="cac87-140">Laotöö on toormaterjali komplekteerimiseks vajalik, et liigutada toormaterjali RM1 laoasukohast BULK-001 asukohta O1.</span><span class="sxs-lookup"><span data-stu-id="cac87-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="cac87-141">Siin on näide tööpoliitikast, mida saate nende kaalutluste põhjal seadistada.</span><span class="sxs-lookup"><span data-stu-id="cac87-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
|<span data-ttu-id="cac87-142">**Tööpoliitika nimi**</span><span class="sxs-lookup"><span data-stu-id="cac87-142">**Work policy name**</span></span><br>                 |<span data-ttu-id="cac87-143">**Töökäsu tüübid**</span><span class="sxs-lookup"><span data-stu-id="cac87-143">**Work order types**</span></span><br>                               |
| <span data-ttu-id="cac87-144">Kõrvalepanekuta 01     \`</span><span class="sxs-lookup"><span data-stu-id="cac87-144">No put away 01     \`</span></span>                    |<span data-ttu-id="cac87-145">- Lõpetatud kaupade kõrvalepanek</span><span class="sxs-lookup"><span data-stu-id="cac87-145">- Finished good put away</span></span><br>                           |
|                                         |<span data-ttu-id="cac87-146">**Asukohad**</span><span class="sxs-lookup"><span data-stu-id="cac87-146">**Locations**</span></span><br>                                      |
|                                         |<span data-ttu-id="cac87-147">- O1</span><span class="sxs-lookup"><span data-stu-id="cac87-147">- O1</span></span>   |                                               |
|                                         |<span data-ttu-id="cac87-148">**Tooted**</span><span class="sxs-lookup"><span data-stu-id="cac87-148">**Products**</span></span> <br>                                      |
|                                         |<span data-ttu-id="cac87-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="cac87-149">- SC1</span></span>                                                  |

<span data-ttu-id="cac87-150">Järgmised protseduurid annavad etapiviisilise juhise, kuidas seadistada selle stsenaarium jaoks laotöö poliitikat.</span><span class="sxs-lookup"><span data-stu-id="cac87-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="cac87-151">Samuti on kirjeldatud näidisseadistust, mis näitab, kuidas teatada tootmistellimus lõpetatuks asukohale, mis pole litsentsiplaadiga kontrollitav.</span><span class="sxs-lookup"><span data-stu-id="cac87-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="cac87-152">Lao tööpoliitika seadistamine</span><span class="sxs-lookup"><span data-stu-id="cac87-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="cac87-153">Laotoimingud ei hõlma alati laotööd.</span><span class="sxs-lookup"><span data-stu-id="cac87-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="cac87-154">Tööpoliitika määratlemisel saate vältida töö loomist toormaterjali komplekteerimise puhul ja lõpetatud kaupade ladustamist toodete kogumi puhul kindlates asukohtades.</span><span class="sxs-lookup"><span data-stu-id="cac87-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="cac87-155">Selle protseduuri loomiseks kasutati demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="cac87-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="cac87-156">ETAPID (21)</span><span class="sxs-lookup"><span data-stu-id="cac87-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="cac87-157">1.</span><span class="sxs-lookup"><span data-stu-id="cac87-157">1.</span></span>  | <span data-ttu-id="cac87-158">Minge asukohta Laohaldus &gt; Seadistus &gt; Töö &gt; Tööpoliitikad.</span><span class="sxs-lookup"><span data-stu-id="cac87-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="cac87-159">2.</span><span class="sxs-lookup"><span data-stu-id="cac87-159">2.</span></span>  | <span data-ttu-id="cac87-160">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cac87-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="cac87-161">3.</span><span class="sxs-lookup"><span data-stu-id="cac87-161">3.</span></span>  | <span data-ttu-id="cac87-162">Tippige välja Tööpoliitika nimi väärtus Ladustamitööd ei ole.</span><span class="sxs-lookup"><span data-stu-id="cac87-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="cac87-163">4.</span><span class="sxs-lookup"><span data-stu-id="cac87-163">4.</span></span>  | <span data-ttu-id="cac87-164">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="cac87-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="cac87-165">5.</span><span class="sxs-lookup"><span data-stu-id="cac87-165">5.</span></span>  | <span data-ttu-id="cac87-166">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cac87-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="cac87-167">6.</span><span class="sxs-lookup"><span data-stu-id="cac87-167">6.</span></span>  | <span data-ttu-id="cac87-168">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="cac87-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="cac87-169">7.</span><span class="sxs-lookup"><span data-stu-id="cac87-169">7.</span></span>  | <span data-ttu-id="cac87-170">Tehke väljal Töötellimuse tüüp valik Lõpetatud kaupade kõrvalepanek.</span><span class="sxs-lookup"><span data-stu-id="cac87-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="cac87-171">8.</span><span class="sxs-lookup"><span data-stu-id="cac87-171">8.</span></span>  | <span data-ttu-id="cac87-172">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cac87-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="cac87-173">9.</span><span class="sxs-lookup"><span data-stu-id="cac87-173">9.</span></span>  | <span data-ttu-id="cac87-174">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="cac87-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="cac87-175">10.</span><span class="sxs-lookup"><span data-stu-id="cac87-175">10.</span></span> | <span data-ttu-id="cac87-176">Tehke välja Töötellimuse tüüp valik Kaastoodete ja kõrvalsaaduste kõrvalepanek.</span><span class="sxs-lookup"><span data-stu-id="cac87-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="cac87-177">11.</span><span class="sxs-lookup"><span data-stu-id="cac87-177">11.</span></span> | <span data-ttu-id="cac87-178">Laiendage jaotist Lao asukohad.</span><span class="sxs-lookup"><span data-stu-id="cac87-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="cac87-179">12.</span><span class="sxs-lookup"><span data-stu-id="cac87-179">12.</span></span> | <span data-ttu-id="cac87-180">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cac87-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="cac87-181">13.</span><span class="sxs-lookup"><span data-stu-id="cac87-181">13.</span></span> | <span data-ttu-id="cac87-182">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="cac87-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="cac87-183">14.</span><span class="sxs-lookup"><span data-stu-id="cac87-183">14.</span></span> | <span data-ttu-id="cac87-184">Sisestage loendisse Ladu väärtus 51.</span><span class="sxs-lookup"><span data-stu-id="cac87-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="cac87-185">15.</span><span class="sxs-lookup"><span data-stu-id="cac87-185">15.</span></span> | <span data-ttu-id="cac87-186">Sisestage või valige väljal Asukoht väärtus 001.</span><span class="sxs-lookup"><span data-stu-id="cac87-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="cac87-187">16.</span><span class="sxs-lookup"><span data-stu-id="cac87-187">16.</span></span> | <span data-ttu-id="cac87-188">Laiendage jaotist Tooted.</span><span class="sxs-lookup"><span data-stu-id="cac87-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="cac87-189">17.</span><span class="sxs-lookup"><span data-stu-id="cac87-189">17.</span></span> | <span data-ttu-id="cac87-190">Tehk väljal Toote valimine valik Valitud.</span><span class="sxs-lookup"><span data-stu-id="cac87-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="cac87-191">18.</span><span class="sxs-lookup"><span data-stu-id="cac87-191">18.</span></span> | <span data-ttu-id="cac87-192">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="cac87-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="cac87-193">19.</span><span class="sxs-lookup"><span data-stu-id="cac87-193">19.</span></span> | <span data-ttu-id="cac87-194">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="cac87-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="cac87-195">20.</span><span class="sxs-lookup"><span data-stu-id="cac87-195">20.</span></span> | <span data-ttu-id="cac87-196">Sisestage või valige väljal Kaubakood väärtus L0101.</span><span class="sxs-lookup"><span data-stu-id="cac87-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="cac87-197">21.</span><span class="sxs-lookup"><span data-stu-id="cac87-197">21.</span></span> | <span data-ttu-id="cac87-198">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="cac87-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="cac87-199">Teatage tootmistellimus lõpetatuks asukohale, mis pole litsentsiplaadiga kontrollitud</span><span class="sxs-lookup"><span data-stu-id="cac87-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="cac87-200">Selles protseduuris esitatakse näide lõpetatuks kuulutamisest mittelitsentsiplaadiga kontrollitava asukoha jaoks.</span><span class="sxs-lookup"><span data-stu-id="cac87-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="cac87-201">Selle ülesande eeltingimus on kehtiv tööpoliitika.</span><span class="sxs-lookup"><span data-stu-id="cac87-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="cac87-202">Eelmine protseduur näitab tööpoliitika seadistust.</span><span class="sxs-lookup"><span data-stu-id="cac87-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="cac87-203">ETAPID (25)</span><span class="sxs-lookup"><span data-stu-id="cac87-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="cac87-204"><strong>Alamülesanne: väljundi asukoha seadistamine.</strong></span><span class="sxs-lookup"><span data-stu-id="cac87-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="cac87-205">Avage Organisatsiooni haldus &gt; Ressursid &gt; Ressursigrupid.</span><span class="sxs-lookup"><span data-stu-id="cac87-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="cac87-206">Valige loendist ressursigrupp 5102.</span><span class="sxs-lookup"><span data-stu-id="cac87-206">In the list, select resource group '5102'.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="cac87-207">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="cac87-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="cac87-208">Sisestage väljale Väljastusladu väärtus 51.</span><span class="sxs-lookup"><span data-stu-id="cac87-208">In the Output warehouse field, enter '51'.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="cac87-209">Sisestage väljale Väljundi asukoht väärtus 001.</span><span class="sxs-lookup"><span data-stu-id="cac87-209">In the Output location field, enter '001'.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="cac87-210">Asukoht 001 pole litsentsiplaadiga juhitav asukoht.</span><span class="sxs-lookup"><span data-stu-id="cac87-210">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="cac87-211">Saate seadistada mittelitsentsiplaadi väljundi asukoha ainult siis, kui asukohale on olemas vastav tööpoliitika.</span><span class="sxs-lookup"><span data-stu-id="cac87-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="cac87-212"><strong>Alamülesanne: tootmistellimuse loomine ja selle lõpetatuna kinnitamine.</strong></span><span class="sxs-lookup"><span data-stu-id="cac87-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="cac87-213">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="cac87-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="cac87-214">Avage Tootmise juhtimine &gt; Tootmistellimused &gt; Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="cac87-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="cac87-215">Klõpsake valikut Uus tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="cac87-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="cac87-216">Sisestage väljale Kauba kood väärtus L0101.</span><span class="sxs-lookup"><span data-stu-id="cac87-216">In the Item number field, enter 'L0101'.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="cac87-217">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="cac87-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="cac87-218">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="cac87-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="cac87-219">Klõpsake suvandit Hinnang.</span><span class="sxs-lookup"><span data-stu-id="cac87-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="cac87-220">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cac87-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="cac87-221">Klõpsake käsku Käivita.</span><span class="sxs-lookup"><span data-stu-id="cac87-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="cac87-222">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="cac87-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="cac87-223">Tehke väljal Automaatne koosluse tarbimine valik Mitte kunagi.</span><span class="sxs-lookup"><span data-stu-id="cac87-223">In the Automatic BOM consumption field, select 'Never'.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="cac87-224">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cac87-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="cac87-225">Klõpsake valikut Kinnita lõpetamine.</span><span class="sxs-lookup"><span data-stu-id="cac87-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="cac87-226">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="cac87-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="cac87-227">Tehke väljal Aktsepteeri viga valik Jah.</span><span class="sxs-lookup"><span data-stu-id="cac87-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="cac87-228">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cac87-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="cac87-229">Klõpsake toimingupaanil valikut Ladu.</span><span class="sxs-lookup"><span data-stu-id="cac87-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="cac87-230">Klõpsake suvandit Töö üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="cac87-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="cac87-231">Kui tootmistellimus on lõpetatuks kuulutatud, pole ladustamiseks tööd loodud.</span><span class="sxs-lookup"><span data-stu-id="cac87-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="cac87-232">See ilmneb, kuna määratletud on tööpoliitika, mis takistab töö loomist, kui toode L0101 kuulutatakse lõpetatuks asukohale 001.</span><span class="sxs-lookup"><span data-stu-id="cac87-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>




