---
title: Allhange
description: See teema aitab teil koostada rakenduses Dynamics 365 Supply Chain Management tootmise allhanke juhiseid.
author: christophernread
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 053dff19da6e51d23383d667c340c49f3eff1b27
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825178"
---
# <a name="subcontracting"></a><span data-ttu-id="3f18b-103">Allhange</span><span class="sxs-lookup"><span data-stu-id="3f18b-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f18b-104">See teema aitab teil koostada rakenduses Microsoft Dynamics 365 Supply Chain Management tootmise allhanke juhiseid.</span><span class="sxs-lookup"><span data-stu-id="3f18b-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3f18b-105">Teema esimeses osas kirjeldatakse andmete seadistamist.</span><span class="sxs-lookup"><span data-stu-id="3f18b-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="3f18b-106">Teises osas läbite juhise etapid.</span><span class="sxs-lookup"><span data-stu-id="3f18b-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="3f18b-107">Sihtpublik</span><span class="sxs-lookup"><span data-stu-id="3f18b-107">Target audience</span></span>

<span data-ttu-id="3f18b-108">Selles teemas saate teada, kuidas seadistada allhanget tootmises.</span><span class="sxs-lookup"><span data-stu-id="3f18b-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="3f18b-109">Allhanke tegevusvoo põhiseadistamiseks kasutate olemasolevaid andmeid juriidilises isikus HQUS.</span><span class="sxs-lookup"><span data-stu-id="3f18b-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="3f18b-110">Demoandmed juriidilises isikus HQUS sisaldavad eelmääratud seadistusparameetreid, mis toetavad juhendi etappides.</span><span class="sxs-lookup"><span data-stu-id="3f18b-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="3f18b-111">Kuigi juhend käsitleb peamisi valupunkte ja väljakutseid erinevate rollide puhul, saab selle lõpule viia süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="3f18b-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="3f18b-112">Demostsenaarium</span><span class="sxs-lookup"><span data-stu-id="3f18b-112">Demo scenario</span></span>

<span data-ttu-id="3f18b-113">Juriidilises isikus HQUS toodetakse kvaliteetkõlareid.</span><span class="sxs-lookup"><span data-stu-id="3f18b-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="3f18b-114">Tootmisprotsessi käigus läbivad kõlarid kolme järgmist toimingut.</span><span class="sxs-lookup"><span data-stu-id="3f18b-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="3f18b-115">**Eelkooste** – kõlarikorpuse kokkupanek.</span><span class="sxs-lookup"><span data-stu-id="3f18b-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="3f18b-116">Korpuse materjal komplekteeritakse materjalilaost enne toimingu käivitamist.</span><span class="sxs-lookup"><span data-stu-id="3f18b-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="3f18b-117">**Katmine** – pärast kõlarikorpuse kokkupanekut tuleb see katta.</span><span class="sxs-lookup"><span data-stu-id="3f18b-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="3f18b-118">Selle toimingu viib lõpule hankija (alltöövõtja).</span><span class="sxs-lookup"><span data-stu-id="3f18b-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="3f18b-119">Eelnevalt kokkupandud kõlarikorpus tarnitakse katmise alltöövõtjale koos kahe materjaliga.</span><span class="sxs-lookup"><span data-stu-id="3f18b-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="3f18b-120">**Lõpetamine** – pärast seda, kui alltöövõtja on eelnevalt kokkupandud kõlarikorpuse katnud, tagastatakse see juriidilisele isikule HQUS, et kõlar lõplikulkt kokku panna.</span><span class="sxs-lookup"><span data-stu-id="3f18b-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="3f18b-121">Järgmisel joonisel on kujutatud kolm toimingut ja materjalid, mida neis tarbitakse.</span><span class="sxs-lookup"><span data-stu-id="3f18b-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![Eelkooste, katmine ja lõpetamine ning materjalid, mida neis tarbitakse.](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="3f18b-123">Seadistamine</span><span class="sxs-lookup"><span data-stu-id="3f18b-123">Setup</span></span>

<span data-ttu-id="3f18b-124">Enne selle juhendiga alustamist peate seadistama andmed.</span><span class="sxs-lookup"><span data-stu-id="3f18b-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="3f18b-125">Valmistoote seadistamine</span><span class="sxs-lookup"><span data-stu-id="3f18b-125">Set up the finished product</span></span>

<span data-ttu-id="3f18b-126">See protseduur aitab teil seadistada väljastatud toote D8100 – kaetud korpus.</span><span class="sxs-lookup"><span data-stu-id="3f18b-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="3f18b-127">Valige **Tooteteabe haldus \> Tooted \> Väljastatud tooted**, et avada leht **Väljastatud toote üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="3f18b-128">Sisestage kiirfiltri väljale **D8100** olemasoleva väljastatud toote leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="3f18b-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![Väljastatud toote D8100 filtreerimine lehel Väljastatud toote üksikasjad](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="3f18b-130">Valige toimingupaani vahekaardil **Insener** suvand **Protsess**, et avada leht **Protsess**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="3f18b-131">Lehel **Protsess** kuvatakse väljastatud toote D8100 kaheksa protsessiversiooni.</span><span class="sxs-lookup"><span data-stu-id="3f18b-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="3f18b-132">Kaheksa protsessiversiooni on jaotatud nelja protsessi vahel saidil 1 ja saidil 5.</span><span class="sxs-lookup"><span data-stu-id="3f18b-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="3f18b-133">Protsessi 000400 kasutatakse kuluarvutuseks, protsessi 00041 kasutatakse siis, kui katmistoiming on sisemine, ja protsessi 00042 kasutatakse siis, kui katmistoiming on väline.</span><span class="sxs-lookup"><span data-stu-id="3f18b-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![Kaheksa protsessiversiooni lehel Protsess](./media/subcontract03_route-page.png)

4. <span data-ttu-id="3f18b-135">Valige ülemisel paanil ruudustikus **Versioonid** protsessiversioon **00042** saidile **5**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="3f18b-136">Valige alumisel paanil vahekaardil **Ülevaade** ruudustikust toiming **20** (**Cbnt CtSc**).</span><span class="sxs-lookup"><span data-stu-id="3f18b-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![Valitud on toiming 20 protsessiversiooni 00042 puhul saidile 5](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="3f18b-138">Valige vahekaart **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-138">Select the **General** tab.</span></span>

    <span data-ttu-id="3f18b-139">Pange tähele, et välja **Protsessi tüüp** väärtus on **Hankija**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="3f18b-140">See väärtus näitab, et toiming 20 (Cbnt CtSc) on alltöövõtu toiming.</span><span class="sxs-lookup"><span data-stu-id="3f18b-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![Vahekaardil Üldine on välja Protsessi tüüp väärtuseks seatud Hankija](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="3f18b-142">Valige vahekaart **Ressursinõuded**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="3f18b-143">Võimalusi kasutatakse tootmise plaanimisel rakendatava ressursi leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="3f18b-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="3f18b-144">Toimingu 20 (Cbnt CtSc) puhul pange tähele, et nõutav on ressurss, millel on kaks võimalust: **Katmine** ja **Kaetud korpused**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![Võimalused Katmine ja Kaetud korpused vahekaardil Ressursinõuded](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="3f18b-146">Valige suvand **Rakendatavad ressursid**, et avada dialoogiboks **Rakendatavad ressurssid**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="3f18b-147">Leiti kolm ressurssi, mis vastavad toimingu ressursinõuetele.</span><span class="sxs-lookup"><span data-stu-id="3f18b-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="3f18b-148">Pange tähele, et ressursside 8851 ja 8852 tüüp on **Hankija**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![Kolm sobivat ressurssi dialoogiboksis Rakendatavad ressurssid](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="3f18b-150">Valige **OK**, et sulgeda dialoogiboks **Rakendatavad ressurssid** ja naasta lehele **Protsess**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="3f18b-151">Sulgege leht **Protsess**, et naasta lehele **Väljastatud toote üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![Leht Väljastatud toodete üksikasjad](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="3f18b-153">Valige toimingupaani vahekaardil **Insener** suvand **Koosluse versioonid**, et avada leht **Koosluse versioonid**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="3f18b-154">Lehel **Koosluse versioonid** kuvatakse väljastatud toote D8100 neli koosluse (BOM) versiooni.</span><span class="sxs-lookup"><span data-stu-id="3f18b-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="3f18b-155">Kooslust 000040 kasutatakse kuluarvutuseks ja plaanimiseks, kooslust 000041 kasutatakse siis, kui katmistoiming tehakse ettevõttesiseselt ning kooslusi 000042 ja 000043 kasutatakse siis, kui katmistoiming hangitakse.</span><span class="sxs-lookup"><span data-stu-id="3f18b-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="3f18b-156">Pange tähele, et kaup S8050 on toode kaubatüübiga **Teenus**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="3f18b-157">See kaup kujutab alltöövõtulepinguga tööd.</span><span class="sxs-lookup"><span data-stu-id="3f18b-157">This item represents the subcontracted work.</span></span>

    ![Neli koosluseversiooni lehel Koosluse versioonid](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="3f18b-159">Valige kiirkaardil **Koosluse read** suvand **Redigeeri**, et avada dialoogiboks **Koosluserea redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="3f18b-160">Kui tootmistellimus on loodud ja väljastatud toote D8100 puhul hinnatud, luuakse kaubale S8050 automaatselt ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="3f18b-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="3f18b-161">See ostutellimus seotakse tootmistellimusega.</span><span class="sxs-lookup"><span data-stu-id="3f18b-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="3f18b-162">Ostutellimuste automaatseks loomiseks tuleb välja **Rea tüüp** väärtuseks seada **Hankija** ja valida tuleb alltöövõtja hankija konto.</span><span class="sxs-lookup"><span data-stu-id="3f18b-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="3f18b-163">Selles näites on hankija konto US-801.</span><span class="sxs-lookup"><span data-stu-id="3f18b-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="3f18b-164">Pange tähele, et koosluse rida on ühendatud katmistoiminguga toimingu numbri (antud juhul 20) kaudu.</span><span class="sxs-lookup"><span data-stu-id="3f18b-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![Dialoogiboks Koosluserea redigeerimine](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="3f18b-166">Laotöölistele parooli loomine</span><span class="sxs-lookup"><span data-stu-id="3f18b-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="3f18b-167">Peate määratlema pihuseadet kasutavatele laotöötajatele parooli.</span><span class="sxs-lookup"><span data-stu-id="3f18b-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="3f18b-168">Valige **Laohaldus \> Seadistus \> Töötaja**, et avada leht **Töö kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="3f18b-169">Valige kiirkaardil **Kasutajad** rida kasutajale **51**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![Leht Töö kasutajad](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="3f18b-171">Valige suvand **Parooli lähtestamine**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="3f18b-172">Sisestage väljadele **Parool** ja **Parooli kinnitus** väärtus **1**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="3f18b-173">Valige suvand **Sea parool**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="3f18b-174">Üksikasjalik juhend</span><span class="sxs-lookup"><span data-stu-id="3f18b-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="3f18b-175">**Stsenaarium ja taust**</span><span class="sxs-lookup"><span data-stu-id="3f18b-175">**Scenario and background**</span></span>

<span data-ttu-id="3f18b-176">Tootele D8100, kaetud korpus, luuakse tootmistellimus 10 ühikuga.</span><span class="sxs-lookup"><span data-stu-id="3f18b-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="3f18b-177">Korpuste katmine on alltöövõtulepinguga toiming, mille teeb hankija US-801, Perfect Coating Solutions.</span><span class="sxs-lookup"><span data-stu-id="3f18b-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="3f18b-178">Tootmistellimuse hõlmab kolme toimingut.</span><span class="sxs-lookup"><span data-stu-id="3f18b-178">The production order consists of three operations.</span></span> <span data-ttu-id="3f18b-179">Esimeses toimingus pannakse korpus ettevõttesisese toiminguna eelnevalt kokku.</span><span class="sxs-lookup"><span data-stu-id="3f18b-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="3f18b-180">Eelkooste jaoks vajalik materjal väljastatakse toormaterjali laost komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="3f18b-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="3f18b-181">Kui eelkooste on lõpule viidud, saadetakse eelnevalt kokkupandud korpus Perfect Coating Solutionsile koos kahe katmistoimingu jaoks vajaliku materjaliga.</span><span class="sxs-lookup"><span data-stu-id="3f18b-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="3f18b-182">Kui kaetud korpus saadetakse hankijalt tagasi, läbib see lõpliku ettevõttesisese koostetoimingu, enne kui see lõpetatuna kinnitatakse.</span><span class="sxs-lookup"><span data-stu-id="3f18b-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="3f18b-183">Valige suvandid **Tootmise juhtimine \> Tootmistellimused \> Kõik tootmistellimused**, et avada leht **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="3f18b-184">Valige toimingupaanil suvand **Uus tootmistellimus**, et avada dialoogiboks **Tootmistellimuse loomine**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![Dialoogiboks Tootmistellimuse loomine](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="3f18b-186">Valige väljal **Kaubakood** väärtus **D8100**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="3f18b-187">Kaubakoodi valimisel kuvatakse varude dimensioonide väljad.</span><span class="sxs-lookup"><span data-stu-id="3f18b-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="3f18b-188">Valige väljal **Värv** väärtus **Kroom**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="3f18b-189">Ilmub teateaken küsimusega, kas sisestada tuleks koosluse ja protsessi aktiivsed versioonid.</span><span class="sxs-lookup"><span data-stu-id="3f18b-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![Teateaken](./media/subcontract13_message-box.png)

5. <span data-ttu-id="3f18b-191">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-191">Select **Yes**.</span></span> 

    <span data-ttu-id="3f18b-192">Dialoogiboksis **Tootmistellimuse loomine** on väljadel **Koosluse number** ja **Protsessi kood** automaatselt valitud vastavalt toote D8100 koosluse ja protsessi aktiivsed versioonid.</span><span class="sxs-lookup"><span data-stu-id="3f18b-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="3f18b-193">Praegusel juhul on valitud kooslus **000040** ja protsess **000040**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="3f18b-194">Nii koosluse kui ka protsessi puhul kasutatakse kuluarvutuseks ja plaanimiseks versiooni 000040.</span><span class="sxs-lookup"><span data-stu-id="3f18b-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="3f18b-195">Valige väljal **Tegevuskoht** väärtus **5**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="3f18b-196">Valige väljal **Ladu** väärtus **51**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="3f18b-197">Muutke väljadel **Koosluse number** ja **Protsessi kood** väärtust, milleks on automaatselt valitud **000042**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3f18b-198">Nii koosluse kui ka protsessi puhul kasutatakse versiooni 000042 korpuse katmiseks alltöövõtulepinguga hankijaga US-801.</span><span class="sxs-lookup"><span data-stu-id="3f18b-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![Dialoogiboksis Tootmistellimuse loomine määratud väärtused](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="3f18b-200">Valige käsk **Loo**, et luua tootmistellimus ja naasta lehele **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![Uus tootmistellimus lehel Kõik tootmistellimused](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="3f18b-202">Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Hinnang**, et avada dialoogiboks **Hinnang**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![Dialoogiboks Hinnang](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="3f18b-204">Valige **OK**, et kinnitada hinnang ja naasta lehele **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3f18b-205">Kui tootmistellimus on hinnatud, luuakse teenusüksuse S8050 jaoks hankijale US-801 tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="3f18b-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="3f18b-206">Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Kooslus**, et avada leht **Kooslus**, kus saate vaadata tootmistellimuse koosluseridu.</span><span class="sxs-lookup"><span data-stu-id="3f18b-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="3f18b-207">Teenuseüksuse S8050 puhul pange tähele, et seal on viide ostutellimusele, mis loodi tootmistellimuse hindamisel.</span><span class="sxs-lookup"><span data-stu-id="3f18b-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![Tootmistellimuse koosluse read lehel Kooslus](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="3f18b-209">Sulgege leht **Kooslus**, et naasta lehele **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="3f18b-210">Valige toimingupaani vahekaardil **Ajakava** suvand **Tööde planeerimine**, et avada dialoogiboks **Töö planeerimine**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="3f18b-211">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3f18b-211">Specify the following values:</span></span>

    - <span data-ttu-id="3f18b-212">Valige väljal **Plaanimissuund** suvand **Edasi homsest**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="3f18b-213">Valige suvandi **Piiratud võimsus** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![Dialoogiboks Tööde planeerimine](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="3f18b-215">Valige **OK**, et sulgeda dialoogiboks **Tööde planeerimine** ja naasta lehele **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="3f18b-216">Valige toimingupaani vahekaardil **Ajakava** suvand **Gantt**, et avada leht **Gantti diagramm – ressursivaade**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="3f18b-217">Gantti diagramm annab visuaalse ülevaate tootmistööde ajakavast ressurssidel.</span><span class="sxs-lookup"><span data-stu-id="3f18b-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="3f18b-218">Pange tähele, et väline katmistöö koosneb kolmest tööst: protsessitöö, transporditöö ja ooteajatöö.</span><span class="sxs-lookup"><span data-stu-id="3f18b-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![Gantti diagramm lehel Gantti diagramm – ressursivaade](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="3f18b-220">Sulgege leht **Gantti diagramm – ressursivaade**, et naasta lehele **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="3f18b-221">Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Väljastamine**, et avada dialoogiboks **Väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![Dialoogiboks Väljastamine](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="3f18b-223">Valige dialoogiboksi **Väljastamine** sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="3f18b-224">Valige suvandid **Tootmise juhtimine \> Perioodilised ülesanded \> Väljasta lattu \> Koosluse- ja valemiridade automaatne väljastamine**, et avada dialoogiboks **Koosluse- ja valemiridade automaatne väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![Dialoogiboks Koosluse- ja valemiridade automaatne väljastamine](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="3f18b-226">Valige koosluse- ja valemiridade töö automaatse väljastamise töö käitamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="3f18b-227">See töö väljastab lattu toormaterjalide komplekteerimistöö.</span><span class="sxs-lookup"><span data-stu-id="3f18b-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="3f18b-228">Valige suvandid **Tootmise juhtimine \> Tootmistellimused \> Kõik tootmistellimused**, et avada leht **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="3f18b-229">Valige kiirfiltri abil tootmistellimus, millega olete töötanud.</span><span class="sxs-lookup"><span data-stu-id="3f18b-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="3f18b-230">Valige toimingupaani vahekaardil **Ladu** suvand **Töö üksikasjad**, et avada leht **Töö**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="3f18b-231">Pange tähele, et lehel kuvatakse toormaterjali komplekteerimise kohta kaks töökomplekti.</span><span class="sxs-lookup"><span data-stu-id="3f18b-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="3f18b-232">Esimene töö on materjalide M8100 ja M8101 kohta.</span><span class="sxs-lookup"><span data-stu-id="3f18b-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="3f18b-233">Neid materjale tarbib toiming 10.</span><span class="sxs-lookup"><span data-stu-id="3f18b-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="3f18b-234">Teine töö on materjalide M8202 ja M8250 kohta.</span><span class="sxs-lookup"><span data-stu-id="3f18b-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="3f18b-235">Neid materjale tarbib toiming 20, mis tehakse alltöövõtulepinguga.</span><span class="sxs-lookup"><span data-stu-id="3f18b-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![Kaks toormaterjali komplekteerimise töökomplekti lehel Töö](./media/subcontract22_work-page.png)

26. <span data-ttu-id="3f18b-237">Käivitage mobiilirakendus Warehouse Management laotöö töötlemiseks toimingu 10 puhul.</span><span class="sxs-lookup"><span data-stu-id="3f18b-237">Start the Warehouse Management mobile app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="3f18b-238">Valige suvandid **Tootmise juhtimine \> Tootmistellimused \> Kõik tootmistellimused**, et avada leht **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="3f18b-239">Valige kiirfiltri abil tootmistellimus, millega olete töötanud.</span><span class="sxs-lookup"><span data-stu-id="3f18b-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="3f18b-240">Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Alusta**, et avada dialoogiboks **Alustamine**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="3f18b-241">Määrake vahekaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3f18b-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="3f18b-242">Valige väljal **Toimingust nr**</span><span class="sxs-lookup"><span data-stu-id="3f18b-242">In the **From Oper. No.**</span></span> <span data-ttu-id="3f18b-243">väärtus **10**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-243">field, select **10**.</span></span>
    - <span data-ttu-id="3f18b-244">Valige väljal **Toiminguni nr**</span><span class="sxs-lookup"><span data-stu-id="3f18b-244">In the **To Oper. No.**</span></span> <span data-ttu-id="3f18b-245">väärtus **10**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-245">field, select **10**.</span></span>

    ![Vahekaardil 1 Üldine määratud väärtused](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="3f18b-247">Valige **OK**, et sulgeda dialoogiboks **Alustamine** ja naasta lehele **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="3f18b-248">Pange tähele, et tootmistellimuse olek on nüüd **Alustatud**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="3f18b-249">Toimingu 10 materjale tarbib komplekteerimislehe töölehe automaatne sisestamine.</span><span class="sxs-lookup"><span data-stu-id="3f18b-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="3f18b-250">Aja tarbimist toimingu 10 puhul võtab arvesse protsessikaardi töölehe automaatne sisestamine.</span><span class="sxs-lookup"><span data-stu-id="3f18b-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="3f18b-251">Käivitage mobiilirakendus Warehouse Management laotöö töötlemiseks toimingu 20 puhul.</span><span class="sxs-lookup"><span data-stu-id="3f18b-251">Start the Warehouse Management mobile app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="3f18b-252">Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Alusta**, et avada dialoogiboks **Alustamine**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="3f18b-253">Määrake vahekaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="3f18b-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="3f18b-254">Valige väljal **Toimingust nr**</span><span class="sxs-lookup"><span data-stu-id="3f18b-254">In the **From Oper. No.**</span></span> <span data-ttu-id="3f18b-255">väärtus **20**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-255">field, select **20**.</span></span>
    - <span data-ttu-id="3f18b-256">Valige väljal **Toiminguni nr**</span><span class="sxs-lookup"><span data-stu-id="3f18b-256">In the **To Oper. No.**</span></span> <span data-ttu-id="3f18b-257">väärtus **20**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-257">field, select **20**.</span></span>
    - <span data-ttu-id="3f18b-258">Sisestage väljale **Kogus** väärtus **10**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="3f18b-259">Valige väljal **Sisesta komplekteerimisleht kohe** suvand **Ei**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-259">Set the **Post picking list now** option to **No**.</span></span>

    ![Vahekaardil 2 Üldine määratud väärtused](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="3f18b-261">Valige **OK**, et sulgeda dialoogiboks **Alustamine** ja naasta lehele **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="3f18b-262">Komplekteerimisleht luuakse materjalide jaoks, mida kasutatakse katmistoimingu puhul, ja teenusüksuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="3f18b-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="3f18b-263">Teenusüksus kujutab alltöövõtulepinguga toimingut.</span><span class="sxs-lookup"><span data-stu-id="3f18b-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="3f18b-264">Valige toimingupaani vahekaardil **Vaade** suvand **Komplekteerimisleht**, et avada leht **Komplekteerimisleht**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="3f18b-265">Valige komplekteerimisleht, mis pole sisestatud, ja seejärel valige töölehe number töölehe ridade kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="3f18b-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![Töölehe read lehel Komplekteerimisleht](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="3f18b-267">Valige toimingupaanil suvandid **Printimine** \> **Komplekteerimislehe aruanne**, et avada dialoogiboks **Komplekteerimislehe aruanne**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="3f18b-268">Seadke suvandi **Kasuta tarneteate paigutust** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![Dialoogiboks Komplekteerimislehe aruanne](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="3f18b-270">Valige aruande **Komplekteerimisleht** loomiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="3f18b-271">Selles näites prinditakse hankija tarneteade tootmise komplekteerimislehe töölehelt.</span><span class="sxs-lookup"><span data-stu-id="3f18b-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="3f18b-272">Tarneteade määrab katmistoimingut tegevale hankijale tarnitavad materjalid.</span><span class="sxs-lookup"><span data-stu-id="3f18b-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![Komplekteerimislehe aruanne](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="3f18b-274">Sulgege aruanne **Komplekteerimisleht**, et naasta lehele **Komplekteerimisleht**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="3f18b-275">Valige toiminguribal suvand **Sisestamine**, et avada dialoogiboks **Töölehe sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![Dialoogiboks Töölehe sisestamine](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="3f18b-277">Valige dialoogiboksi **Töölehe sisestamine** sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="3f18b-278">Avage ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="3f18b-278">Open the purchase order.</span></span>

    ![Leht Ostutellimus](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="3f18b-280">Valige toimingupaani vahekaardil **Ostmine** suvand **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="3f18b-281">Valige dialoogiboksi **Töölehe sisestamine** avamiseks käsk **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="3f18b-282">Valige **OK**, et sulgeda dialoogiboks **Töölehe sisestamine** ja naasta lehele **Ostutellimus**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="3f18b-283">Muutke ühiku hinnaks **33** asemel **40**.</span><span class="sxs-lookup"><span data-stu-id="3f18b-283">Change the unit price from **33** to **40**.</span></span>

    ![Lehel Ostutellimus muudetud ühiku hind](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="3f18b-285">Kinnitage ostutellimus uuesti.</span><span class="sxs-lookup"><span data-stu-id="3f18b-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="3f18b-286">Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="3f18b-286">Product receipt.</span></span>

    ![Dialoogiboks Toote sissetuleku sisestamine](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="3f18b-288">Ostuarve.</span><span class="sxs-lookup"><span data-stu-id="3f18b-288">Purchase invoice.</span></span>
52. <span data-ttu-id="3f18b-289">Värskendage vastendamise olekut.</span><span class="sxs-lookup"><span data-stu-id="3f18b-289">Update the match status.</span></span>

    ![Leht Hankija arve](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="3f18b-291">Kinnita lõpetamine.</span><span class="sxs-lookup"><span data-stu-id="3f18b-291">Report as finished.</span></span>

    ![Dialoogiboks Lõpetatuna kinnitamine](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="3f18b-293">Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="3f18b-293">End.</span></span>

    ![Dialoogiboks Lõpetamine](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="3f18b-295">Kuluvõrdlus.</span><span class="sxs-lookup"><span data-stu-id="3f18b-295">Cost comparison.</span></span>

    ![Kuluvõrdluse diagrammid](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="3f18b-297">Puuduv seadistus andmetes.</span><span class="sxs-lookup"><span data-stu-id="3f18b-297">Missing setup in data.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]