---
title: Allhange
description: See teema aitab teil koostada rakenduses Dynamics 365 Supply Chain Management tootmise allhanke juhiseid.
author: christophernread
manager: tfehr
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: f771c15d98abe3689054d43cc8b33632121522a3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255537"
---
# <a name="subcontracting"></a><span data-ttu-id="481bd-103">Allhange</span><span class="sxs-lookup"><span data-stu-id="481bd-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="481bd-104">See teema aitab teil koostada rakenduses Microsoft Dynamics 365 Supply Chain Management tootmise allhanke juhiseid.</span><span class="sxs-lookup"><span data-stu-id="481bd-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="481bd-105">Teema esimeses osas kirjeldatakse andmete seadistamist.</span><span class="sxs-lookup"><span data-stu-id="481bd-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="481bd-106">Teises osas läbite juhise etapid.</span><span class="sxs-lookup"><span data-stu-id="481bd-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="481bd-107">Sihtpublik</span><span class="sxs-lookup"><span data-stu-id="481bd-107">Target audience</span></span>

<span data-ttu-id="481bd-108">Selles teemas saate teada, kuidas seadistada allhanget tootmises.</span><span class="sxs-lookup"><span data-stu-id="481bd-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="481bd-109">Allhanke tegevusvoo põhiseadistamiseks kasutate olemasolevaid andmeid juriidilises isikus HQUS.</span><span class="sxs-lookup"><span data-stu-id="481bd-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="481bd-110">Demoandmed juriidilises isikus HQUS sisaldavad eelmääratud seadistusparameetreid, mis toetavad juhendi etappides.</span><span class="sxs-lookup"><span data-stu-id="481bd-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="481bd-111">Kuigi juhend käsitleb peamisi valupunkte ja väljakutseid erinevate rollide puhul, saab selle lõpule viia süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="481bd-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="481bd-112">Demostsenaarium</span><span class="sxs-lookup"><span data-stu-id="481bd-112">Demo scenario</span></span>

<span data-ttu-id="481bd-113">Juriidilises isikus HQUS toodetakse kvaliteetkõlareid.</span><span class="sxs-lookup"><span data-stu-id="481bd-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="481bd-114">Tootmisprotsessi käigus läbivad kõlarid kolme järgmist toimingut.</span><span class="sxs-lookup"><span data-stu-id="481bd-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="481bd-115">**Eelkooste** – kõlarikorpuse kokkupanek.</span><span class="sxs-lookup"><span data-stu-id="481bd-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="481bd-116">Korpuse materjal komplekteeritakse materjalilaost enne toimingu käivitamist.</span><span class="sxs-lookup"><span data-stu-id="481bd-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="481bd-117">**Katmine** – pärast kõlarikorpuse kokkupanekut tuleb see katta.</span><span class="sxs-lookup"><span data-stu-id="481bd-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="481bd-118">Selle toimingu viib lõpule hankija (alltöövõtja).</span><span class="sxs-lookup"><span data-stu-id="481bd-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="481bd-119">Eelnevalt kokkupandud kõlarikorpus tarnitakse katmise alltöövõtjale koos kahe materjaliga.</span><span class="sxs-lookup"><span data-stu-id="481bd-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="481bd-120">**Lõpetamine** – pärast seda, kui alltöövõtja on eelnevalt kokkupandud kõlarikorpuse katnud, tagastatakse see juriidilisele isikule HQUS, et kõlar lõplikulkt kokku panna.</span><span class="sxs-lookup"><span data-stu-id="481bd-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="481bd-121">Järgmisel joonisel on kujutatud kolm toimingut ja materjalid, mida neis tarbitakse.</span><span class="sxs-lookup"><span data-stu-id="481bd-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![Eelkooste, katmine ja lõpetamine ning materjalid, mida neis tarbitakse.](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="481bd-123">Seadistamine</span><span class="sxs-lookup"><span data-stu-id="481bd-123">Setup</span></span>

<span data-ttu-id="481bd-124">Enne selle juhendiga alustamist peate seadistama andmed.</span><span class="sxs-lookup"><span data-stu-id="481bd-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="481bd-125">Valmistoote seadistamine</span><span class="sxs-lookup"><span data-stu-id="481bd-125">Set up the finished product</span></span>

<span data-ttu-id="481bd-126">See protseduur aitab teil seadistada väljastatud toote D8100 – kaetud korpus.</span><span class="sxs-lookup"><span data-stu-id="481bd-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="481bd-127">Valige **Tooteteabe haldus \> Tooted \> Väljastatud tooted**, et avada leht **Väljastatud toote üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="481bd-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="481bd-128">Sisestage kiirfiltri väljale **D8100** olemasoleva väljastatud toote leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="481bd-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![Väljastatud toote D8100 filtreerimine lehel Väljastatud toote üksikasjad](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="481bd-130">Valige toimingupaani vahekaardil **Insener** suvand **Protsess**, et avada leht **Protsess**.</span><span class="sxs-lookup"><span data-stu-id="481bd-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="481bd-131">Lehel **Protsess** kuvatakse väljastatud toote D8100 kaheksa protsessiversiooni.</span><span class="sxs-lookup"><span data-stu-id="481bd-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="481bd-132">Kaheksa protsessiversiooni on jaotatud nelja protsessi vahel saidil 1 ja saidil 5.</span><span class="sxs-lookup"><span data-stu-id="481bd-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="481bd-133">Protsessi 000400 kasutatakse kuluarvutuseks, protsessi 00041 kasutatakse siis, kui katmistoiming on sisemine, ja protsessi 00042 kasutatakse siis, kui katmistoiming on väline.</span><span class="sxs-lookup"><span data-stu-id="481bd-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![Kaheksa protsessiversiooni lehel Protsess](./media/subcontract03_route-page.png)

4. <span data-ttu-id="481bd-135">Valige ülemisel paanil ruudustikus **Versioonid** protsessiversioon **00042** saidile **5**.</span><span class="sxs-lookup"><span data-stu-id="481bd-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="481bd-136">Valige alumisel paanil vahekaardil **Ülevaade** ruudustikust toiming **20** (**Cbnt CtSc**).</span><span class="sxs-lookup"><span data-stu-id="481bd-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![Valitud on toiming 20 protsessiversiooni 00042 puhul saidile 5](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="481bd-138">Valige vahekaart **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="481bd-138">Select the **General** tab.</span></span>

    <span data-ttu-id="481bd-139">Pange tähele, et välja **Protsessi tüüp** väärtus on **Hankija**.</span><span class="sxs-lookup"><span data-stu-id="481bd-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="481bd-140">See väärtus näitab, et toiming 20 (Cbnt CtSc) on alltöövõtu toiming.</span><span class="sxs-lookup"><span data-stu-id="481bd-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![Vahekaardil Üldine on välja Protsessi tüüp väärtuseks seatud Hankija](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="481bd-142">Valige vahekaart **Ressursinõuded**.</span><span class="sxs-lookup"><span data-stu-id="481bd-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="481bd-143">Võimalusi kasutatakse tootmise plaanimisel rakendatava ressursi leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="481bd-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="481bd-144">Toimingu 20 (Cbnt CtSc) puhul pange tähele, et nõutav on ressurss, millel on kaks võimalust: **Katmine** ja **Kaetud korpused**.</span><span class="sxs-lookup"><span data-stu-id="481bd-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![Võimalused Katmine ja Kaetud korpused vahekaardil Ressursinõuded](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="481bd-146">Valige suvand **Rakendatavad ressursid**, et avada dialoogiboks **Rakendatavad ressurssid**.</span><span class="sxs-lookup"><span data-stu-id="481bd-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="481bd-147">Leiti kolm ressurssi, mis vastavad toimingu ressursinõuetele.</span><span class="sxs-lookup"><span data-stu-id="481bd-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="481bd-148">Pange tähele, et ressursside 8851 ja 8852 tüüp on **Hankija**.</span><span class="sxs-lookup"><span data-stu-id="481bd-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![Kolm sobivat ressurssi dialoogiboksis Rakendatavad ressurssid](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="481bd-150">Valige **OK**, et sulgeda dialoogiboks **Rakendatavad ressurssid** ja naasta lehele **Protsess**.</span><span class="sxs-lookup"><span data-stu-id="481bd-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="481bd-151">Sulgege leht **Protsess**, et naasta lehele **Väljastatud toote üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="481bd-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![Leht Väljastatud toodete üksikasjad](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="481bd-153">Valige toimingupaani vahekaardil **Insener** suvand **Koosluse versioonid**, et avada leht **Koosluse versioonid**.</span><span class="sxs-lookup"><span data-stu-id="481bd-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="481bd-154">Lehel **Koosluse versioonid** kuvatakse väljastatud toote D8100 neli koosluse (BOM) versiooni.</span><span class="sxs-lookup"><span data-stu-id="481bd-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="481bd-155">Kooslust 000040 kasutatakse kuluarvutuseks ja plaanimiseks, kooslust 000041 kasutatakse siis, kui katmistoiming tehakse ettevõttesiseselt ning kooslusi 000042 ja 000043 kasutatakse siis, kui katmistoiming hangitakse.</span><span class="sxs-lookup"><span data-stu-id="481bd-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="481bd-156">Pange tähele, et kaup S8050 on toode kaubatüübiga **Teenus**.</span><span class="sxs-lookup"><span data-stu-id="481bd-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="481bd-157">See kaup kujutab alltöövõtulepinguga tööd.</span><span class="sxs-lookup"><span data-stu-id="481bd-157">This item represents the subcontracted work.</span></span>

    ![Neli koosluseversiooni lehel Koosluse versioonid](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="481bd-159">Valige kiirkaardil **Koosluse read** suvand **Redigeeri**, et avada dialoogiboks **Koosluserea redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="481bd-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="481bd-160">Kui tootmistellimus on loodud ja väljastatud toote D8100 puhul hinnatud, luuakse kaubale S8050 automaatselt ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="481bd-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="481bd-161">See ostutellimus seotakse tootmistellimusega.</span><span class="sxs-lookup"><span data-stu-id="481bd-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="481bd-162">Ostutellimuste automaatseks loomiseks tuleb välja **Rea tüüp** väärtuseks seada **Hankija** ja valida tuleb alltöövõtja hankija konto.</span><span class="sxs-lookup"><span data-stu-id="481bd-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="481bd-163">Selles näites on hankija konto US-801.</span><span class="sxs-lookup"><span data-stu-id="481bd-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="481bd-164">Pange tähele, et koosluse rida on ühendatud katmistoiminguga toimingu numbri (antud juhul 20) kaudu.</span><span class="sxs-lookup"><span data-stu-id="481bd-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![Dialoogiboks Koosluserea redigeerimine](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="481bd-166">Laotöölistele parooli loomine</span><span class="sxs-lookup"><span data-stu-id="481bd-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="481bd-167">Peate määratlema pihuseadet kasutavatele laotöötajatele parooli.</span><span class="sxs-lookup"><span data-stu-id="481bd-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="481bd-168">Valige **Laohaldus \> Seadistus \> Töötaja**, et avada leht **Töö kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="481bd-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="481bd-169">Valige kiirkaardil **Kasutajad** rida kasutajale **51**.</span><span class="sxs-lookup"><span data-stu-id="481bd-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![Leht Töö kasutajad](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="481bd-171">Valige suvand **Parooli lähtestamine**.</span><span class="sxs-lookup"><span data-stu-id="481bd-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="481bd-172">Sisestage väljadele **Parool** ja **Parooli kinnitus** väärtus **1**.</span><span class="sxs-lookup"><span data-stu-id="481bd-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="481bd-173">Valige suvand **Sea parool**.</span><span class="sxs-lookup"><span data-stu-id="481bd-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="481bd-174">Üksikasjalik juhend</span><span class="sxs-lookup"><span data-stu-id="481bd-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="481bd-175">**Stsenaarium ja taust**</span><span class="sxs-lookup"><span data-stu-id="481bd-175">**Scenario and background**</span></span>

<span data-ttu-id="481bd-176">Tootele D8100, kaetud korpus, luuakse tootmistellimus 10 ühikuga.</span><span class="sxs-lookup"><span data-stu-id="481bd-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="481bd-177">Korpuste katmine on alltöövõtulepinguga toiming, mille teeb hankija US-801, Perfect Coating Solutions.</span><span class="sxs-lookup"><span data-stu-id="481bd-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="481bd-178">Tootmistellimuse hõlmab kolme toimingut.</span><span class="sxs-lookup"><span data-stu-id="481bd-178">The production order consists of three operations.</span></span> <span data-ttu-id="481bd-179">Esimeses toimingus pannakse korpus ettevõttesisese toiminguna eelnevalt kokku.</span><span class="sxs-lookup"><span data-stu-id="481bd-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="481bd-180">Eelkooste jaoks vajalik materjal väljastatakse toormaterjali laost komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="481bd-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="481bd-181">Kui eelkooste on lõpule viidud, saadetakse eelnevalt kokkupandud korpus Perfect Coating Solutionsile koos kahe katmistoimingu jaoks vajaliku materjaliga.</span><span class="sxs-lookup"><span data-stu-id="481bd-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="481bd-182">Kui kaetud korpus saadetakse hankijalt tagasi, läbib see lõpliku ettevõttesisese koostetoimingu, enne kui see lõpetatuna kinnitatakse.</span><span class="sxs-lookup"><span data-stu-id="481bd-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="481bd-183">Valige suvandid **Tootmise juhtimine \> Tootmistellimused \> Kõik tootmistellimused**, et avada leht **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="481bd-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="481bd-184">Valige toimingupaanil suvand **Uus tootmistellimus**, et avada dialoogiboks **Tootmistellimuse loomine**.</span><span class="sxs-lookup"><span data-stu-id="481bd-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![Dialoogiboks Tootmistellimuse loomine](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="481bd-186">Valige väljal **Kaubakood** väärtus **D8100**.</span><span class="sxs-lookup"><span data-stu-id="481bd-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="481bd-187">Kaubakoodi valimisel kuvatakse varude dimensioonide väljad.</span><span class="sxs-lookup"><span data-stu-id="481bd-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="481bd-188">Valige väljal **Värv** väärtus **Kroom**.</span><span class="sxs-lookup"><span data-stu-id="481bd-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="481bd-189">Ilmub teateaken küsimusega, kas sisestada tuleks koosluse ja protsessi aktiivsed versioonid.</span><span class="sxs-lookup"><span data-stu-id="481bd-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![Teateaken](./media/subcontract13_message-box.png)

5. <span data-ttu-id="481bd-191">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="481bd-191">Select **Yes**.</span></span> 

    <span data-ttu-id="481bd-192">Dialoogiboksis **Tootmistellimuse loomine** on väljadel **Koosluse number** ja **Protsessi kood** automaatselt valitud vastavalt toote D8100 koosluse ja protsessi aktiivsed versioonid.</span><span class="sxs-lookup"><span data-stu-id="481bd-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="481bd-193">Praegusel juhul on valitud kooslus **000040** ja protsess **000040**.</span><span class="sxs-lookup"><span data-stu-id="481bd-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="481bd-194">Nii koosluse kui ka protsessi puhul kasutatakse kuluarvutuseks ja plaanimiseks versiooni 000040.</span><span class="sxs-lookup"><span data-stu-id="481bd-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="481bd-195">Valige väljal **Tegevuskoht** väärtus **5**.</span><span class="sxs-lookup"><span data-stu-id="481bd-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="481bd-196">Valige väljal **Ladu** väärtus **51**.</span><span class="sxs-lookup"><span data-stu-id="481bd-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="481bd-197">Muutke väljadel **Koosluse number** ja **Protsessi kood** väärtust, milleks on automaatselt valitud **000042**.</span><span class="sxs-lookup"><span data-stu-id="481bd-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="481bd-198">Nii koosluse kui ka protsessi puhul kasutatakse versiooni 000042 korpuse katmiseks alltöövõtulepinguga hankijaga US-801.</span><span class="sxs-lookup"><span data-stu-id="481bd-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![Dialoogiboksis Tootmistellimuse loomine määratud väärtused](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="481bd-200">Valige käsk **Loo**, et luua tootmistellimus ja naasta lehele **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="481bd-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![Uus tootmistellimus lehel Kõik tootmistellimused](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="481bd-202">Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Hinnang**, et avada dialoogiboks **Hinnang**.</span><span class="sxs-lookup"><span data-stu-id="481bd-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![Dialoogiboks Hinnang](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="481bd-204">Valige **OK**, et kinnitada hinnang ja naasta lehele **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="481bd-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="481bd-205">Kui tootmistellimus on hinnatud, luuakse teenusüksuse S8050 jaoks hankijale US-801 tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="481bd-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="481bd-206">Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Kooslus**, et avada leht **Kooslus**, kus saate vaadata tootmistellimuse koosluseridu.</span><span class="sxs-lookup"><span data-stu-id="481bd-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="481bd-207">Teenuseüksuse S8050 puhul pange tähele, et seal on viide ostutellimusele, mis loodi tootmistellimuse hindamisel.</span><span class="sxs-lookup"><span data-stu-id="481bd-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![Tootmistellimuse koosluse read lehel Kooslus](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="481bd-209">Sulgege leht **Kooslus**, et naasta lehele **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="481bd-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="481bd-210">Valige toimingupaani vahekaardil **Ajakava** suvand **Tööde planeerimine**, et avada dialoogiboks **Töö planeerimine**.</span><span class="sxs-lookup"><span data-stu-id="481bd-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="481bd-211">Määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="481bd-211">Specify the following values:</span></span>

    - <span data-ttu-id="481bd-212">Valige väljal **Plaanimissuund** suvand **Edasi homsest**.</span><span class="sxs-lookup"><span data-stu-id="481bd-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="481bd-213">Valige suvandi **Piiratud võimsus** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="481bd-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![Dialoogiboks Tööde planeerimine](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="481bd-215">Valige **OK**, et sulgeda dialoogiboks **Tööde planeerimine** ja naasta lehele **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="481bd-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="481bd-216">Valige toimingupaani vahekaardil **Ajakava** suvand **Gantt**, et avada leht **Gantti diagramm – ressursivaade**.</span><span class="sxs-lookup"><span data-stu-id="481bd-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="481bd-217">Gantti diagramm annab visuaalse ülevaate tootmistööde ajakavast ressurssidel.</span><span class="sxs-lookup"><span data-stu-id="481bd-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="481bd-218">Pange tähele, et väline katmistöö koosneb kolmest tööst: protsessitöö, transporditöö ja ooteajatöö.</span><span class="sxs-lookup"><span data-stu-id="481bd-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![Gantti diagramm lehel Gantti diagramm – ressursivaade](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="481bd-220">Sulgege leht **Gantti diagramm – ressursivaade**, et naasta lehele **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="481bd-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="481bd-221">Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Väljastamine**, et avada dialoogiboks **Väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="481bd-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![Dialoogiboks Väljastamine](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="481bd-223">Valige dialoogiboksi **Väljastamine** sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="481bd-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="481bd-224">Valige suvandid **Tootmise juhtimine \> Perioodilised ülesanded \> Väljasta lattu \> Koosluse- ja valemiridade automaatne väljastamine**, et avada dialoogiboks **Koosluse- ja valemiridade automaatne väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="481bd-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![Dialoogiboks Koosluse- ja valemiridade automaatne väljastamine](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="481bd-226">Valige koosluse- ja valemiridade töö automaatse väljastamise töö käitamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="481bd-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="481bd-227">See töö väljastab lattu toormaterjalide komplekteerimistöö.</span><span class="sxs-lookup"><span data-stu-id="481bd-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="481bd-228">Valige suvandid **Tootmise juhtimine \> Tootmistellimused \> Kõik tootmistellimused**, et avada leht **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="481bd-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="481bd-229">Valige kiirfiltri abil tootmistellimus, millega olete töötanud.</span><span class="sxs-lookup"><span data-stu-id="481bd-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="481bd-230">Valige toimingupaani vahekaardil **Ladu** suvand **Töö üksikasjad**, et avada leht **Töö**.</span><span class="sxs-lookup"><span data-stu-id="481bd-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="481bd-231">Pange tähele, et lehel kuvatakse toormaterjali komplekteerimise kohta kaks töökomplekti.</span><span class="sxs-lookup"><span data-stu-id="481bd-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="481bd-232">Esimene töö on materjalide M8100 ja M8101 kohta.</span><span class="sxs-lookup"><span data-stu-id="481bd-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="481bd-233">Neid materjale tarbib toiming 10.</span><span class="sxs-lookup"><span data-stu-id="481bd-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="481bd-234">Teine töö on materjalide M8202 ja M8250 kohta.</span><span class="sxs-lookup"><span data-stu-id="481bd-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="481bd-235">Neid materjale tarbib toiming 20, mis tehakse alltöövõtulepinguga.</span><span class="sxs-lookup"><span data-stu-id="481bd-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![Kaks toormaterjali komplekteerimise töökomplekti lehel Töö](./media/subcontract22_work-page.png)

26. <span data-ttu-id="481bd-237">Käivitage laorakendus laotöö töötlemiseks toimingu 10 puhul.</span><span class="sxs-lookup"><span data-stu-id="481bd-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="481bd-238">Valige suvandid **Tootmise juhtimine \> Tootmistellimused \> Kõik tootmistellimused**, et avada leht **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="481bd-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="481bd-239">Valige kiirfiltri abil tootmistellimus, millega olete töötanud.</span><span class="sxs-lookup"><span data-stu-id="481bd-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="481bd-240">Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Alusta**, et avada dialoogiboks **Alustamine**.</span><span class="sxs-lookup"><span data-stu-id="481bd-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="481bd-241">Määrake vahekaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="481bd-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="481bd-242">Valige väljal **Toimingust nr**</span><span class="sxs-lookup"><span data-stu-id="481bd-242">In the **From Oper. No.**</span></span> <span data-ttu-id="481bd-243">väärtus **10**.</span><span class="sxs-lookup"><span data-stu-id="481bd-243">field, select **10**.</span></span>
    - <span data-ttu-id="481bd-244">Valige väljal **Toiminguni nr**</span><span class="sxs-lookup"><span data-stu-id="481bd-244">In the **To Oper. No.**</span></span> <span data-ttu-id="481bd-245">väärtus **10**.</span><span class="sxs-lookup"><span data-stu-id="481bd-245">field, select **10**.</span></span>

    ![Vahekaardil Üldine määratud väärtused](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="481bd-247">Valige **OK**, et sulgeda dialoogiboks **Alustamine** ja naasta lehele **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="481bd-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="481bd-248">Pange tähele, et tootmistellimuse olek on nüüd **Alustatud**.</span><span class="sxs-lookup"><span data-stu-id="481bd-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="481bd-249">Toimingu 10 materjale tarbib komplekteerimislehe töölehe automaatne sisestamine.</span><span class="sxs-lookup"><span data-stu-id="481bd-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="481bd-250">Aja tarbimist toimingu 10 puhul võtab arvesse protsessikaardi töölehe automaatne sisestamine.</span><span class="sxs-lookup"><span data-stu-id="481bd-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="481bd-251">Käivitage laorakendus laotöö töötlemiseks toimingu 20 puhul.</span><span class="sxs-lookup"><span data-stu-id="481bd-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="481bd-252">Valige toimingupaani vahekaardil **Tootmistellimus** suvand **Alusta**, et avada dialoogiboks **Alustamine**.</span><span class="sxs-lookup"><span data-stu-id="481bd-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="481bd-253">Määrake vahekaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="481bd-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="481bd-254">Valige väljal **Toimingust nr**</span><span class="sxs-lookup"><span data-stu-id="481bd-254">In the **From Oper. No.**</span></span> <span data-ttu-id="481bd-255">väärtus **20**.</span><span class="sxs-lookup"><span data-stu-id="481bd-255">field, select **20**.</span></span>
    - <span data-ttu-id="481bd-256">Valige väljal **Toiminguni nr**</span><span class="sxs-lookup"><span data-stu-id="481bd-256">In the **To Oper. No.**</span></span> <span data-ttu-id="481bd-257">väärtus **20**.</span><span class="sxs-lookup"><span data-stu-id="481bd-257">field, select **20**.</span></span>
    - <span data-ttu-id="481bd-258">Sisestage väljale **Kogus** väärtus **10**.</span><span class="sxs-lookup"><span data-stu-id="481bd-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="481bd-259">Valige väljal **Sisesta komplekteerimisleht kohe** suvand **Ei**.</span><span class="sxs-lookup"><span data-stu-id="481bd-259">Set the **Post picking list now** option to **No**.</span></span>

    ![Vahekaardil Üldine määratud väärtused](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="481bd-261">Valige **OK**, et sulgeda dialoogiboks **Alustamine** ja naasta lehele **Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="481bd-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="481bd-262">Komplekteerimisleht luuakse materjalide jaoks, mida kasutatakse katmistoimingu puhul, ja teenusüksuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="481bd-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="481bd-263">Teenusüksus kujutab alltöövõtulepinguga toimingut.</span><span class="sxs-lookup"><span data-stu-id="481bd-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="481bd-264">Valige toimingupaani vahekaardil **Vaade** suvand **Komplekteerimisleht**, et avada leht **Komplekteerimisleht**.</span><span class="sxs-lookup"><span data-stu-id="481bd-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="481bd-265">Valige komplekteerimisleht, mis pole sisestatud, ja seejärel valige töölehe number töölehe ridade kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="481bd-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![Töölehe read lehel Komplekteerimisleht](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="481bd-267">Valige toimingupaanil suvandid **Printimine** \> **Komplekteerimislehe aruanne**, et avada dialoogiboks **Komplekteerimislehe aruanne**.</span><span class="sxs-lookup"><span data-stu-id="481bd-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="481bd-268">Seadke suvandi **Kasuta tarneteate paigutust** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="481bd-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![Dialoogiboks Komplekteerimislehe aruanne](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="481bd-270">Valige aruande **Komplekteerimisleht** loomiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="481bd-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="481bd-271">Selles näites prinditakse hankija tarneteade tootmise komplekteerimislehe töölehelt.</span><span class="sxs-lookup"><span data-stu-id="481bd-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="481bd-272">Tarneteade määrab katmistoimingut tegevale hankijale tarnitavad materjalid.</span><span class="sxs-lookup"><span data-stu-id="481bd-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![Komplekteerimislehe aruanne](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="481bd-274">Sulgege aruanne **Komplekteerimisleht**, et naasta lehele **Komplekteerimisleht**.</span><span class="sxs-lookup"><span data-stu-id="481bd-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="481bd-275">Valige toiminguribal suvand **Sisestamine**, et avada dialoogiboks **Töölehe sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="481bd-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![Dialoogiboks Töölehe sisestamine](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="481bd-277">Valige dialoogiboksi **Töölehe sisestamine** sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="481bd-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="481bd-278">Avage ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="481bd-278">Open the purchase order.</span></span>

    ![Leht Ostutellimus](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="481bd-280">Valige toimingupaani vahekaardil **Ostmine** suvand **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="481bd-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="481bd-281">Valige dialoogiboksi **Töölehe sisestamine** avamiseks käsk **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="481bd-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="481bd-282">Valige **OK**, et sulgeda dialoogiboks **Töölehe sisestamine** ja naasta lehele **Ostutellimus**.</span><span class="sxs-lookup"><span data-stu-id="481bd-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="481bd-283">Muutke ühiku hinnaks **33** asemel **40**.</span><span class="sxs-lookup"><span data-stu-id="481bd-283">Change the unit price from **33** to **40**.</span></span>

    ![Lehel Ostutellimus muudetud ühiku hind](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="481bd-285">Kinnitage ostutellimus uuesti.</span><span class="sxs-lookup"><span data-stu-id="481bd-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="481bd-286">Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="481bd-286">Product receipt.</span></span>

    ![Dialoogiboks Toote sissetuleku sisestamine](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="481bd-288">Ostuarve.</span><span class="sxs-lookup"><span data-stu-id="481bd-288">Purchase invoice.</span></span>
52. <span data-ttu-id="481bd-289">Värskendage vastendamise olekut.</span><span class="sxs-lookup"><span data-stu-id="481bd-289">Update the match status.</span></span>

    ![Leht Hankija arve](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="481bd-291">Kinnita lõpetamine.</span><span class="sxs-lookup"><span data-stu-id="481bd-291">Report as finished.</span></span>

    ![Dialoogiboks Lõpetatuna kinnitamine](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="481bd-293">Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="481bd-293">End.</span></span>

    ![Dialoogiboks Lõpetamine](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="481bd-295">Kuluvõrdlus.</span><span class="sxs-lookup"><span data-stu-id="481bd-295">Cost comparison.</span></span>

    ![Kuluvõrdluse diagrammid](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="481bd-297">Puuduv seadistus andmetes.</span><span class="sxs-lookup"><span data-stu-id="481bd-297">Missing setup in data.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]