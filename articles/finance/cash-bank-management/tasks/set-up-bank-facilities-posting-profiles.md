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
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6da3b9358192997de1d0231e5c9c8eaba92a23b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976262"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="f7aab-103">Pangateenuste ja garantiikirjade sisestusreeglite seadistamine</span><span class="sxs-lookup"><span data-stu-id="f7aab-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7aab-104">Selle ülesandega luuakse panga süsteemiteenus ja sisestusreegel, mis on vajalik garantiikirja töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="f7aab-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="f7aab-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="f7aab-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="f7aab-106">Pearaamatu parameeter</span><span class="sxs-lookup"><span data-stu-id="f7aab-106">General ledger parameter</span></span>
1. <span data-ttu-id="f7aab-107">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha- ja pangahalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="f7aab-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="f7aab-108">Laiendage jaotist Pangadokument.</span><span class="sxs-lookup"><span data-stu-id="f7aab-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="f7aab-109">Valige suvand Garantiikirja lubamine.</span><span class="sxs-lookup"><span data-stu-id="f7aab-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="f7aab-110">Klõpsake väljal Kande tööleht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f7aab-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f7aab-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f7aab-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="f7aab-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f7aab-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f7aab-113">Klõpsake vahekaarti Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="f7aab-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="f7aab-114">Numbriseeria määratlemine garantiikirja numbri ja garantiikirja kandeviidete jaoks</span><span class="sxs-lookup"><span data-stu-id="f7aab-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="f7aab-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f7aab-115">Click Save.</span></span>
9. <span data-ttu-id="f7aab-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7aab-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="f7aab-117">Panga süsteemiteenuse loomine</span><span class="sxs-lookup"><span data-stu-id="f7aab-117">Create Bank facility</span></span>
1. <span data-ttu-id="f7aab-118">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Panga süsteemiteenused.</span><span class="sxs-lookup"><span data-stu-id="f7aab-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="f7aab-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f7aab-119">Click New.</span></span>
3. <span data-ttu-id="f7aab-120">Sisestage väljale Süsteemiteenuste grupp garantiikirja kande jaoks panga süsteemiteenuste grupi nimi.</span><span class="sxs-lookup"><span data-stu-id="f7aab-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="f7aab-121">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="f7aab-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f7aab-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f7aab-122">Click Save.</span></span>
6. <span data-ttu-id="f7aab-123">Klõpsake vahekaarti Süsteemiteenuste tüübid.</span><span class="sxs-lookup"><span data-stu-id="f7aab-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="f7aab-124">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f7aab-124">Click New.</span></span>
8. <span data-ttu-id="f7aab-125">Sisestage väljale Süsteemiteenuste tüüp panga süsteemiteenuse leppega seotud panga süsteemiteenuste tüübi nimi.</span><span class="sxs-lookup"><span data-stu-id="f7aab-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="f7aab-126">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="f7aab-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="f7aab-127">Klõpsake väljal Süsteemiteenuste grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f7aab-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="f7aab-128">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f7aab-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="f7aab-129">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f7aab-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="f7aab-130">Valige suvand väljal Süsteemiteenuse olemus.</span><span class="sxs-lookup"><span data-stu-id="f7aab-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="f7aab-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f7aab-131">Click Save.</span></span>
15. <span data-ttu-id="f7aab-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7aab-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="f7aab-133">Panga sisestusreegel</span><span class="sxs-lookup"><span data-stu-id="f7aab-133">Bank posting profile</span></span>
1. <span data-ttu-id="f7aab-134">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Pangadokumentide sisestusreegel.</span><span class="sxs-lookup"><span data-stu-id="f7aab-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="f7aab-135">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f7aab-135">Click New.</span></span>
3. <span data-ttu-id="f7aab-136">Klõpsake väljal Konto/grupi nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f7aab-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f7aab-137">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f7aab-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f7aab-138">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f7aab-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f7aab-139">Valige väljal Tasakaalustuskonto tasakaalustuseks põhikonto.</span><span class="sxs-lookup"><span data-stu-id="f7aab-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="f7aab-140">Valige väljal Tasude konto kulukannete konto.</span><span class="sxs-lookup"><span data-stu-id="f7aab-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="f7aab-141">Valige väljal Kasumikonto marginaalkande jaoks konto.</span><span class="sxs-lookup"><span data-stu-id="f7aab-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="f7aab-142">Valige väljal Likvideerimiskonto garantiikirja kande likvideerimiskonto.</span><span class="sxs-lookup"><span data-stu-id="f7aab-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="f7aab-143">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f7aab-143">Click Save.</span></span>
11. <span data-ttu-id="f7aab-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7aab-144">Close the page.</span></span>

