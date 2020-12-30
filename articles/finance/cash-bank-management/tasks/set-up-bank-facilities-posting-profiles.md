---
title: Pangateenuste ja garantiikirjade sisestusreeglite seadistamine
description: Selle ülesandega luuakse panga süsteemiteenus ja sisestusreegel, mis on vajalik garantiikirja töötlemiseks.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff5402b11cd2ccdfde2881268d9cd936947cd77e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442432"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="664a3-103">Pangateenuste ja garantiikirjade sisestusreeglite seadistamine</span><span class="sxs-lookup"><span data-stu-id="664a3-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="664a3-104">Selle ülesandega luuakse panga süsteemiteenus ja sisestusreegel, mis on vajalik garantiikirja töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="664a3-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="664a3-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="664a3-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="664a3-106">Pearaamatu parameeter</span><span class="sxs-lookup"><span data-stu-id="664a3-106">General ledger parameter</span></span>
1. <span data-ttu-id="664a3-107">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha- ja pangahalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="664a3-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="664a3-108">Laiendage jaotist Pangadokument.</span><span class="sxs-lookup"><span data-stu-id="664a3-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="664a3-109">Valige suvand Garantiikirja lubamine.</span><span class="sxs-lookup"><span data-stu-id="664a3-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="664a3-110">Klõpsake väljal Kande tööleht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="664a3-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="664a3-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="664a3-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="664a3-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="664a3-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="664a3-113">Klõpsake vahekaarti Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="664a3-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="664a3-114">Numbriseeria määratlemine garantiikirja numbri ja garantiikirja kandeviidete jaoks</span><span class="sxs-lookup"><span data-stu-id="664a3-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="664a3-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="664a3-115">Click Save.</span></span>
9. <span data-ttu-id="664a3-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="664a3-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="664a3-117">Panga süsteemiteenuse loomine</span><span class="sxs-lookup"><span data-stu-id="664a3-117">Create Bank facility</span></span>
1. <span data-ttu-id="664a3-118">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Panga süsteemiteenused.</span><span class="sxs-lookup"><span data-stu-id="664a3-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="664a3-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="664a3-119">Click New.</span></span>
3. <span data-ttu-id="664a3-120">Sisestage väljale Süsteemiteenuste grupp garantiikirja kande jaoks panga süsteemiteenuste grupi nimi.</span><span class="sxs-lookup"><span data-stu-id="664a3-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="664a3-121">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="664a3-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="664a3-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="664a3-122">Click Save.</span></span>
6. <span data-ttu-id="664a3-123">Klõpsake vahekaarti Süsteemiteenuste tüübid.</span><span class="sxs-lookup"><span data-stu-id="664a3-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="664a3-124">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="664a3-124">Click New.</span></span>
8. <span data-ttu-id="664a3-125">Sisestage väljale Süsteemiteenuste tüüp panga süsteemiteenuse leppega seotud panga süsteemiteenuste tüübi nimi.</span><span class="sxs-lookup"><span data-stu-id="664a3-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="664a3-126">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="664a3-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="664a3-127">Klõpsake väljal Süsteemiteenuste grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="664a3-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="664a3-128">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="664a3-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="664a3-129">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="664a3-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="664a3-130">Valige suvand väljal Süsteemiteenuse olemus.</span><span class="sxs-lookup"><span data-stu-id="664a3-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="664a3-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="664a3-131">Click Save.</span></span>
15. <span data-ttu-id="664a3-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="664a3-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="664a3-133">Panga sisestusreegel</span><span class="sxs-lookup"><span data-stu-id="664a3-133">Bank posting profile</span></span>
1. <span data-ttu-id="664a3-134">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Pangadokumentide sisestusreegel.</span><span class="sxs-lookup"><span data-stu-id="664a3-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="664a3-135">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="664a3-135">Click New.</span></span>
3. <span data-ttu-id="664a3-136">Klõpsake väljal Konto/grupi nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="664a3-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="664a3-137">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="664a3-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="664a3-138">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="664a3-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="664a3-139">Valige väljal Tasakaalustuskonto tasakaalustuseks põhikonto.</span><span class="sxs-lookup"><span data-stu-id="664a3-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="664a3-140">Valige väljal Tasude konto kulukannete konto.</span><span class="sxs-lookup"><span data-stu-id="664a3-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="664a3-141">Valige väljal Kasumikonto marginaalkande jaoks konto.</span><span class="sxs-lookup"><span data-stu-id="664a3-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="664a3-142">Valige väljal Likvideerimiskonto garantiikirja kande likvideerimiskonto.</span><span class="sxs-lookup"><span data-stu-id="664a3-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="664a3-143">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="664a3-143">Click Save.</span></span>
11. <span data-ttu-id="664a3-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="664a3-144">Close the page.</span></span>

