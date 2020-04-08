---
title: Hankijate ja hankija pangakontode seadistamine ISO20022 kreeditkorralduste jaoks
description: See protseduur näitab, kuidas seadistada hankija ja hankijakohase pangakonto teavet, mis on nõutav ISO20022 kreeditülekande või mis tahes muu hankija maksefaili loomiseks.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4809a352f87cc3d88429461a06dfe36189ed5f31
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138965"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="ce8b8-103">Hankijate ja hankija pangakontode seadistamine ISO20022 kreeditkorralduste jaoks</span><span class="sxs-lookup"><span data-stu-id="ce8b8-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ce8b8-104">See protseduur näitab, kuidas seadistada hankija ja hankijakohase pangakonto teavet, mis on nõutav ISO20022 kreeditülekande või mis tahes muu hankija maksefaili loomiseks.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="ce8b8-105">Selle protseduuri loomiseks kasutatav demoandmete ettevõte on DEMF.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="ce8b8-106">See on neljas viiest protseduurist, mis illustreerib hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="ce8b8-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="ce8b8-108">Panga üksikasjade seadistamine</span><span class="sxs-lookup"><span data-stu-id="ce8b8-108">Set up bank details</span></span>
1. <span data-ttu-id="ce8b8-109">Minge jaotisse Ostureskontrod > Hankijad > Kõik hankijad.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="ce8b8-110">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ce8b8-111">Näiteks saate filtrida välja Hankija konto väärtuse DE-001 järgi.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="ce8b8-112">Hankija üksikasjade avamiseks klõpsake DE-001.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="ce8b8-113">Klõpsake toimingupaanil suvandit Hankija.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="ce8b8-114">Klõpsake valikut Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="ce8b8-115">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-115">Click Edit.</span></span>
    * <span data-ttu-id="ce8b8-116">Kui ühtegi pangakontot pole saadaval, peate looma uue.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="ce8b8-117">Sisestage väljale SWIFT-kood väärtus COBADEFFXXX.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="ce8b8-118">Sisestage väljale IBAN väärtus DE36200400000628808808.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="ce8b8-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="ce8b8-120">Hankija makseviisi seadistamine</span><span class="sxs-lookup"><span data-stu-id="ce8b8-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="ce8b8-121">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-121">Click Edit.</span></span>
2. <span data-ttu-id="ce8b8-122">Laiendage või ahendage jaotist Makse.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="ce8b8-123">Klõpsake väljal Makseviis otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ce8b8-124">Klõpsake loendis valitud real SEPA CT olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="ce8b8-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ce8b8-125">Click Save.</span></span>

