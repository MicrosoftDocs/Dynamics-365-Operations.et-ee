---
title: Tagastatud kauba sissetuleku registreerimine
description: "Võite registreerida tagastatud kaupade sissetuleku, kasutades saabumise ülevaate vormi või registreerimisvormi."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverview, InventTransRegister
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 2be628d312e623e8ea6d92eb5edce12334190d9e
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---


# <a name="register-the-receipt-of-returned-items"></a><span data-ttu-id="b4af8-103">Tagastatud kauba sissetuleku registreerimine</span><span class="sxs-lookup"><span data-stu-id="b4af8-103">Register the receipt of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b4af8-104">Tagastatud kaupade sissetuleku registreerimiseks on kaks meetodi.</span><span class="sxs-lookup"><span data-stu-id="b4af8-104">There are two methods for registering the receipt of returned items.</span></span> <span data-ttu-id="b4af8-105">Esimene meetod on lao kättesaamisprotsess, mis kasutab vormi **Saabumise ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-105">The first method is a warehouse receiving process that uses the **Arrival overview** form.</span></span> <span data-ttu-id="b4af8-106">Teine kasutab vormi **Registreerimine**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-106">The second uses the **Registration** form.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-arrival-overview-form"></a><span data-ttu-id="b4af8-107">Tagastatud kaupade saatelehe registreerimine saabumise ülevaate vormis</span><span class="sxs-lookup"><span data-stu-id="b4af8-107">Register the receipt of returned items in the Arrival overview form</span></span>

<span data-ttu-id="b4af8-108">Saate kasutada vormi **Saabumise ülevaade**, et tuvastada tagastussaadetis selle tagastatud kauba (RMA) koodi järgi.</span><span class="sxs-lookup"><span data-stu-id="b4af8-108">You can use the **Arrival overview** form to identify a return shipment by its Return Material Authorization (RMA) number.</span></span> <span data-ttu-id="b4af8-109">Kui töölehe nimi on määratletud vahekaardil **Seadistamine** ja on olemas töölehe read, mis vastavad vormis **Saabumise ülevaade** valitud ridadele, luuakse uus töölehe päis, kui klõpsate nuppu **Alusta saabumistöölehte**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-109">If a journal name is defined on the **Setup** tab, and journal lines that correspond to the lines selected on the **Arrival overview** form exist, a new journal header is created when you click **Start arrival**.</span></span>

1.  <span data-ttu-id="b4af8-110">Klõpsake valikuid **Varud** \> **Perioodiline** \> **Saabumisülevaade**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-110">Click **Inventory management** \> **Periodic** \> **Arrival overview**.</span></span>

2.  <span data-ttu-id="b4af8-111">Valige väljas **Seadistuse nimi** suvand **Tagastustellimus** ja klõpsake käsku **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-111">In the **Setup name** field, select **Return order**, and then click **Update**.</span></span>
    

    > [!TIP]
    > <P><span data-ttu-id="b4af8-112">Saate otsingutulemuste täpsustamiseks kasutada välju <STRONG>Vahemik</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b4af8-112">You can use the <STRONG>Range</STRONG> fields to narrow the search results.</span></span> <span data-ttu-id="b4af8-113">Täpse tulemuse saamiseks saate tippida või valida tagastuskoodi väljal <STRONG>RMA number</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b4af8-113">You can type or select the RMA number in the <STRONG>RMA number</STRONG> field for an exact result.</span></span> <span data-ttu-id="b4af8-114">Selliste filtrite kogumi määratlemiseks ja salvestamiseks, mis määravad, milliseid sissetulevaid saabumisi kuvatakse, klõpsake vahekaarti <STRONG>Seadistamine</STRONG>. Saadaolevad filtrid sisaldavad tüüpe, ladusid ja alasid.</span><span class="sxs-lookup"><span data-stu-id="b4af8-114">To define and save a set of filters that will restrict which incoming arrivals are displayed, click the <STRONG>Setup</STRONG> tab. The available filters include types, warehouses, and docks.</span></span></P>

    

    > [!WARNING]
    > <P><span data-ttu-id="b4af8-115">Tagastustellimusi ei saa segada muude saabumise tüüpidega vormis <STRONG>Saabumise ülevaade</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b4af8-115">Return orders cannot be mixed with other arrival types in the <STRONG>Arrival overview</STRONG> form.</span></span> <span data-ttu-id="b4af8-116">Seetõttu on viide alati müügitellimus, kuid ühtki müügitellimuse ID-d ei määrata töölehe päises.</span><span class="sxs-lookup"><span data-stu-id="b4af8-116">Therefore, the reference will always be sales order, but no sales order ID will be specified on the journal header.</span></span></P>



3.  <span data-ttu-id="b4af8-117">Leidke ruudustikus **Kviitungid** rida, mis sobib tagastatava kaubaga, ja märkige seejärel ruut veerus **Vali saabumise jaoks**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-117">In the **Receipts** grid, locate the line that matches the item being returned, and then select the check box in the **Select for arrival** column.</span></span>

4.  <span data-ttu-id="b4af8-118">Selleks et tagastatud sissetulekust välistada kindlad read, nt algse tellimuse kaubad, mida tagastatud saadetises ei olnud, tühjendage nendega seotud märkeruudud **Vali saabumise jaoks** vormi alumisel osal olevas tabelis **Read**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-118">To exclude certain lines from the return receipt, such as items from the original order that were not included in the return shipment, clear the associated **Select for arrival** check boxes in the **Lines** table in the lower part of the form.</span></span>

5.  <span data-ttu-id="b4af8-119">Klõpsake nuppu **Alusta saabumistöölehte** saabumise töölehe loomiseks.</span><span class="sxs-lookup"><span data-stu-id="b4af8-119">Click the **Start arrival** button to create an arrival journal.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="b4af8-120">Saate valida mitu tagastustellimust ja kaasata need kõik ühte saabumisprotsessi.</span><span class="sxs-lookup"><span data-stu-id="b4af8-120">You can select multiple return orders and include them all in a single arrival process.</span></span> <span data-ttu-id="b4af8-121">Kõik tagastustellimuse read kopeeritakse kauba saabumistöölehe vastavatele ridadele.</span><span class="sxs-lookup"><span data-stu-id="b4af8-121">Each return order line will be copied into a corresponding item arrival journal line.</span></span></P>

    

    > [!NOTE]
    > <P><span data-ttu-id="b4af8-122">Samuti saate käsitsi luua saabumistöölehte, kasutades vormi <STRONG>Kauba saabumine</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b4af8-122">You can also manually create an arrival journal by using the <STRONG>Item arrival</STRONG> form.</span></span> 



6.  <span data-ttu-id="b4af8-123">Klõpsake valikuid **Laohaldus** \> **Töölehed** \> **Kauba saabumine** \> **Kauba saabumine**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-123">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>

7.  <span data-ttu-id="b4af8-124">Valige värskelt loodud saabumistööleht ja klõpsake nuppu **Read**, et avada vorm **Töölehe read, asukohad**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-124">Select the arrival journal that you just created and then click **Lines** to open the **Journal lines, locations** form.</span></span>

8.  <span data-ttu-id="b4af8-125">Vahekaardil **Üldine** kohandage numbrit väljal **Kogus**, kui see on nõutav, ja määrake seejärel likvideerimiskood väljal **Likvideerimiskood**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-125">On the **General** tab, adjust the number in the **Quantity** field, if it is required, and then assign a disposition code in the **Disposition code** field.</span></span>
    
    <span data-ttu-id="b4af8-126">Teise võimalusena saate märkida ruudu **Vahelao haldus**, et tagastatud kaubad läbiksid kontrollimisprotsessi vahelaoorderi kontekstis.</span><span class="sxs-lookup"><span data-stu-id="b4af8-126">Alternatively, you can select the **Quarantine management** check box to have the returned items sent through an inspection process in the context of a quarantine order.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="b4af8-127">Kui saadate tagastatud kaubad vahelao kaudu, ei saa likvideerimiskoode määrata.</span><span class="sxs-lookup"><span data-stu-id="b4af8-127">If you send the returned items through quarantine, you cannot specify a disposition code.</span></span></P>



9.  <span data-ttu-id="b4af8-128">Klõpsake nuppu **Kontrolli**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-128">Click the **Validate** button.</span></span>

10. <span data-ttu-id="b4af8-129">Kui kinnitamise protsessis tõrkeid ei esine, klõpsake käsku **Postita**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-129">If there are no errors in the validation process, click **Post**.</span></span>

## <a name="register-the-receipt-of-returned-items-in-the-registration-form"></a><span data-ttu-id="b4af8-130">Tagastatud kaupade saatelehe registreerimine registreerimisvormis</span><span class="sxs-lookup"><span data-stu-id="b4af8-130">Register the receipt of returned items in the Registration form</span></span>

<span data-ttu-id="b4af8-131">Vormi **Saabumise ülevaade** kasutamise alternatiivina võite kasutada vormi **Registreerimine**, et registreerida tagastatud kaupade saabumine.</span><span class="sxs-lookup"><span data-stu-id="b4af8-131">As an alternative to using the **Arrival overview** form, you can use the **Registration** form to register the arrival of returned items.</span></span>

1.  <span data-ttu-id="b4af8-132">Klõpsake valikuid **Müük ja turundus** \> **Üldine** \> **Tagastustellimused** \> **Kõik tagastustellimused**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-132">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span> <span data-ttu-id="b4af8-133">Looge uus tagastustellimus või avage loendist tagastustellimus.</span><span class="sxs-lookup"><span data-stu-id="b4af8-133">Create a new return order or open the return order from the list.</span></span> <span data-ttu-id="b4af8-134">Kiirkaardil **Read** valige tagastustellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="b4af8-134">On the **Lines** FastTab, select the return order line.</span></span> <span data-ttu-id="b4af8-135">Klõpsake käsku **Värskenda rida** ja seejärel valikut **Registreerimine**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-135">Click **Update line**, and then click **Registration**.</span></span>

2.  <span data-ttu-id="b4af8-136">Määrake likvideerimiskood väljal **Likvideerimiskood** ja klõpsake seejärel nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-136">Assign a disposition code in the **Disposition code** field, and then click **OK**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="b4af8-137">Ei ole võimalik saata kaupa kontrollimiseks vahelaoorderina, kasutades vormi <STRONG>Registreerimine</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="b4af8-137">It is not possible to send the item for inspection as a quarantine order using the <STRONG>Registration</STRONG> form.</span></span></P>



3.  <span data-ttu-id="b4af8-138">Ruudustikus **Kanded** valige registreeritav kanne.</span><span class="sxs-lookup"><span data-stu-id="b4af8-138">In the **Transactions** grid, select the transaction to be registered.</span></span>

4.  <span data-ttu-id="b4af8-139">Klõpsake ruudustikus **Registreeri kohe** käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-139">In the **Register now** grid, click **Add**.</span></span> <span data-ttu-id="b4af8-140">Korrake kahte eelmist etappi, kuni kõik tagastatud kaubad kuvatakse ruudustikus **Registreeri kohe**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-140">Repeat the previous two steps until all of the returned items appear in the **Register now** grid.</span></span>

5.  <span data-ttu-id="b4af8-141">Klõpsake käsku **Postita kõik**.</span><span class="sxs-lookup"><span data-stu-id="b4af8-141">Click **Post all**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4af8-142">Vt ka</span><span class="sxs-lookup"><span data-stu-id="b4af8-142">See also</span></span>

<span data-ttu-id="b4af8-143">[Saabumise ülevaade (vorm)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="b4af8-143">[Arrival overview (form)](https://technet.microsoft.com/en-us/library/hh227654\(v=ax.60\))</span></span>

  



