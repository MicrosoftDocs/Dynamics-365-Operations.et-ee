---
title: Pangateenuste ja akreditiivide sisestusreeglite seadistamine
description: See protseduur selgitab panga süsteemiteenuse loomist ja akreditiivi töötlemiseks vajalike sisestusreeglite sisestamist.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 945504cd73b743fb3711997274c537e51e5c6dec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834640"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="ecc94-103">Pangateenuste ja akreditiivide sisestusreeglite seadistamine</span><span class="sxs-lookup"><span data-stu-id="ecc94-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ecc94-104">See protseduur selgitab panga süsteemiteenuse loomist ja akreditiivi töötlemiseks vajalike sisestusreeglite sisestamist.</span><span class="sxs-lookup"><span data-stu-id="ecc94-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="ecc94-105">Ülesandes kasutatakse demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="ecc94-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="ecc94-106">Pearaamatu parameeter</span><span class="sxs-lookup"><span data-stu-id="ecc94-106">General ledger parameter</span></span>
1. <span data-ttu-id="ecc94-107">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha- ja pangahalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="ecc94-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="ecc94-108">Laiendage jaotist Pangadokument.</span><span class="sxs-lookup"><span data-stu-id="ecc94-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="ecc94-109">Valige suvand Impordi akreditiivi lubamine.</span><span class="sxs-lookup"><span data-stu-id="ecc94-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="ecc94-110">Valige suvand Ekspordi akreditiivi lubamine.</span><span class="sxs-lookup"><span data-stu-id="ecc94-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="ecc94-111">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ecc94-111">Click Save.</span></span>
6. <span data-ttu-id="ecc94-112">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ecc94-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="ecc94-113">Panga süsteemiteenuse loomine</span><span class="sxs-lookup"><span data-stu-id="ecc94-113">Create Bank facility</span></span>
1. <span data-ttu-id="ecc94-114">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Panga süsteemiteenused.</span><span class="sxs-lookup"><span data-stu-id="ecc94-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="ecc94-115">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ecc94-115">Click New.</span></span>
3. <span data-ttu-id="ecc94-116">Sisestage väljale Süsteemiteenuste tüüp panga süsteemiteenuste grupi nimi.</span><span class="sxs-lookup"><span data-stu-id="ecc94-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="ecc94-117">Sisestage väljale Kirjeldus panga süsteemiteenuste grupi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="ecc94-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="ecc94-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ecc94-118">Click Save.</span></span>
6. <span data-ttu-id="ecc94-119">Klõpsake vahekaarti Süsteemiteenuste tüübid.</span><span class="sxs-lookup"><span data-stu-id="ecc94-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="ecc94-120">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ecc94-120">Click New.</span></span>
8. <span data-ttu-id="ecc94-121">Sisestage ainuidentifikaator väljale Süsteemiteenuse tüüp.</span><span class="sxs-lookup"><span data-stu-id="ecc94-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="ecc94-122">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ecc94-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="ecc94-123">Klõpsake väljal Süsteemiteenuste grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ecc94-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ecc94-124">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ecc94-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="ecc94-125">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ecc94-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="ecc94-126">Valige väljal Süsteemiteenuste olemus panga süsteemiteenuste olemus.</span><span class="sxs-lookup"><span data-stu-id="ecc94-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="ecc94-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ecc94-127">Click Save.</span></span>
15. <span data-ttu-id="ecc94-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ecc94-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="ecc94-129">Panga sisestusreegel</span><span class="sxs-lookup"><span data-stu-id="ecc94-129">Bank posting profile</span></span>
1. <span data-ttu-id="ecc94-130">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Pangadokumentide sisestusreegel.</span><span class="sxs-lookup"><span data-stu-id="ecc94-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="ecc94-131">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ecc94-131">Click New.</span></span>
3. <span data-ttu-id="ecc94-132">Klõpsake väljal Konto/grupi nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ecc94-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ecc94-133">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ecc94-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ecc94-134">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ecc94-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ecc94-135">Valige tasakaalustuse põhikonto.</span><span class="sxs-lookup"><span data-stu-id="ecc94-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="ecc94-136">Seda kontot kasutatakse likviidsuse planeerimise arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="ecc94-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="ecc94-137">Valige väljal Tasude konto kulukannete konto.</span><span class="sxs-lookup"><span data-stu-id="ecc94-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="ecc94-138">Valige väljal Kasumikonto marginaalkannete konto.</span><span class="sxs-lookup"><span data-stu-id="ecc94-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="ecc94-139">Seda kontot debiteeritakse, kui avamarginaal sisestatakse ja krediteeritakse makse sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="ecc94-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="ecc94-140">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ecc94-140">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]