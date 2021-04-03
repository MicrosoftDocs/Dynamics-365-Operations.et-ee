---
title: Kauba asendamise tellimuse loomine
description: Kauba asendustellimused luuakse tavaliselt pärast toote tagastamist ja kontrollimist.
author: josaw1
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnReplaceItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0932c34cc6b3604afbea7c8a18620640c00d928
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257995"
---
# <a name="create-an-item-replacement-order"></a><span data-ttu-id="d060d-103">Kauba asendamise tellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="d060d-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d060d-104">Kauba asendustellimused luuakse tavaliselt pärast toote tagastamist ja kontrollimist.</span><span class="sxs-lookup"><span data-stu-id="d060d-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="d060d-105">Kui kaup tuleb siiski asendada enne tagastamist või kui originaalkaupa ei tagastata, saate luua kauba asendustellimuse kohe pärast tagastustellimuse loomist.</span><span class="sxs-lookup"><span data-stu-id="d060d-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="d060d-106">Looge asendustellimus pärast tagastatava kauba kättesaamist.</span><span class="sxs-lookup"><span data-stu-id="d060d-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="d060d-107">Klõpsake valikuid **Müük ja turundus** \> **Üldine** \> **Tagastustellimused** \> **Kõik tagastustellimused**.</span><span class="sxs-lookup"><span data-stu-id="d060d-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="d060d-108">Looge uus tagastustellimus või valige tagastustellimus loendist, et avada vorm **Tagastustellimus – RMA-kood: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="d060d-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="d060d-109">Klõpsake valikut **Tagastusrida** ja valige seejärel **Asenduskaup**.</span><span class="sxs-lookup"><span data-stu-id="d060d-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="d060d-110">Valige kirje, millega tagastatud kaup asendada.</span><span class="sxs-lookup"><span data-stu-id="d060d-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="d060d-111">Sisestage kauba täpsustused ja klõpsake seejärel **Rakenda**.</span><span class="sxs-lookup"><span data-stu-id="d060d-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="d060d-112">Tagastustellimusele saatelehe loomiseks klõpsake valikut **Saateleht**.</span><span class="sxs-lookup"><span data-stu-id="d060d-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="d060d-113">Müügitellimus luuakse valitud asenduskaubale.</span><span class="sxs-lookup"><span data-stu-id="d060d-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="d060d-114">Pärast müügitellimuse loomist asenduskaubale otsitakse müügilepinguid automaatselt ja kui on kehtiv müügileping, rakendatakse see müügitellimusele.</span><span class="sxs-lookup"><span data-stu-id="d060d-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="d060d-115">Asendustellimuse loomine enne tagastatava kauba kättesaamist</span><span class="sxs-lookup"><span data-stu-id="d060d-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="d060d-116">Klõpsake valikuid **Müük ja turundus** \> **Üldine** \> **Tagastustellimused** \> **Kõik tagastustellimused**.</span><span class="sxs-lookup"><span data-stu-id="d060d-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="d060d-117">Looge uus tagastustellimus või valige tagastustellimus loendist, et avada vorm **Tagastustellimus – RMA-kood: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="d060d-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="d060d-118">Klõpsake valikut **Otsi müügitellimust**, kui soovite tuvastada tagastatud kauba müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="d060d-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="d060d-119">Täitke vorm **Otsi müügitellimust** ja klõpsake seejärel **OK**, et vorm sulgeda ja naasta vormile **Tagastustellimus – RMA-kood: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="d060d-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="d060d-120">Tagastatud kauba müügitellimuse rida kopeeritakse tagastustellimusse.</span><span class="sxs-lookup"><span data-stu-id="d060d-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="d060d-121">klõpsake vormi **Loo müügitellimus** avamiseks valikut **Asendustellimus**.</span><span class="sxs-lookup"><span data-stu-id="d060d-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="d060d-122">Märkige ruut **Kopeeri tagastustellimuse read**, et kanda üle üksikasjad tagastustellimuselt, mille te selle müügitellimuse juurde vormil **Tagastustellimus – RMA number: %1, %2** valisite.</span><span class="sxs-lookup"><span data-stu-id="d060d-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="d060d-123">Sisestage või muutke üksikasju vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="d060d-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="d060d-124">Kui tuvastasite müügitellimuse 3. etapis ja kui tagastatud kauba müügitellimuse rida on lingitud müügilepinguga, kuvatakse väljal **Müügilepingu ID** automaatselt kauba asendustellimuse kehtiva müügilepingu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="d060d-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="d060d-125">Klõpsake **OK**, et sulgeda vorm **Müügitellimuse loomine**, ja avage vorm **Müügitellimus**, kus saate jätkata uue müügitellimuse teabe sisestamist.</span><span class="sxs-lookup"><span data-stu-id="d060d-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="d060d-126">Mis tahes kehtiva tagastustellimuse read kopeeritakse uude müügitellimusse.</span><span class="sxs-lookup"><span data-stu-id="d060d-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="d060d-127">Kui müügilepingu identifikaator kuvatakse automaatselt väljal **Müügilepingu ID**, siis on müügileping kauba asendustellimuse puhul müügitellimuse päisega lingitud.</span><span class="sxs-lookup"><span data-stu-id="d060d-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="d060d-128">Kui müügilepingus on kehtiv kohustus, mis pole veel täidetud, ja müügitellimus luuakse enne müügilepingu aegumist, luuakse müügilepingu ja müügitellimuse ridade vahel link.</span><span class="sxs-lookup"><span data-stu-id="d060d-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="d060d-129">Seetõttu kopeeritakse müügilepingu teave, nagu kaubahind, uuele müügitellimuse reale.</span><span class="sxs-lookup"><span data-stu-id="d060d-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]