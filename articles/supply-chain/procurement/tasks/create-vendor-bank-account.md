---
title: Hankija pangakonto loomine
description: Selles protseduuris kirjeldatakse, kuidas luua hankijale pangakontot.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deb3587667ac13b95617ec219995bfef931df00c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "360620"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="f4185-103">Hankija pangakonto loomine</span><span class="sxs-lookup"><span data-stu-id="f4185-103">Create a vendor bank account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4185-104">Selles protseduuris kirjeldatakse, kuidas luua hankijale pangakontot.</span><span class="sxs-lookup"><span data-stu-id="f4185-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="f4185-105">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="f4185-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="f4185-106">Tehke valik Hanked > Hankijad > Kõik hankijad.</span><span class="sxs-lookup"><span data-stu-id="f4185-106">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="f4185-107">Valige hankija, kellele soovite pangakontot luua, ja klõpsake siis hankija konto ID linki.</span><span class="sxs-lookup"><span data-stu-id="f4185-107">Select the vendor that you want to create a bank account for, and then click the link on the Vendor account ID.</span></span>
3. <span data-ttu-id="f4185-108">Klõpsake toimingupaanil suvandit Hankija.</span><span class="sxs-lookup"><span data-stu-id="f4185-108">On the Action Pane, click Vendor.</span></span>
4. <span data-ttu-id="f4185-109">Klõpsake valikut Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="f4185-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="f4185-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f4185-110">Click New.</span></span>
6. <span data-ttu-id="f4185-111">Sisestage väärtus väljale Pangakonto.</span><span class="sxs-lookup"><span data-stu-id="f4185-111">In the Bank account field, type a value.</span></span>
    * <span data-ttu-id="f4185-112">Seda ID-d kasutatakse hankija kirje pangakonto tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="f4185-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="f4185-113">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f4185-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="f4185-114">Sisestage väärtus väljale Pangagrupid või valige see.</span><span class="sxs-lookup"><span data-stu-id="f4185-114">In the Bank groups field, enter or select a value.</span></span>
9. <span data-ttu-id="f4185-115">Tehke valik väljal Protsessikoodi tüüp.</span><span class="sxs-lookup"><span data-stu-id="f4185-115">In the Routing number type field, select an option.</span></span>
    * <span data-ttu-id="f4185-116">See on protsessikoodi tüüp, mida kasutatakse rahvusvaheliste maksete puhul.</span><span class="sxs-lookup"><span data-stu-id="f4185-116">This is the type of routing number that’s used for international payments.</span></span>  
10. <span data-ttu-id="f4185-117">Sisestage väärtus väljale Pangakonto number.</span><span class="sxs-lookup"><span data-stu-id="f4185-117">In the Bank account number field, type a value.</span></span>
11. <span data-ttu-id="f4185-118">Sisestage väärtus väljale SWIFT-kood.</span><span class="sxs-lookup"><span data-stu-id="f4185-118">In the SWIFT code field, type a value.</span></span>
12. <span data-ttu-id="f4185-119">Sisestage väärtus väljale IBAN.</span><span class="sxs-lookup"><span data-stu-id="f4185-119">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="f4185-120">IBAN-number peab olema õiges vormingus.</span><span class="sxs-lookup"><span data-stu-id="f4185-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="f4185-121">Näiteks võite kasutada numbrit DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="f4185-121">For example, you could use DE89370400440532013000.</span></span>  
    * <span data-ttu-id="f4185-122">Pangakonto olek on Aktiivne, kui aktiveerimiskuupäev on kätte jõudnud ja aegumiskuupäeva pole ületatud.</span><span class="sxs-lookup"><span data-stu-id="f4185-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="f4185-123">See on aktiivne ka juhul, kui väljad Aktiveerimiskuupäev ja Aegumiskuupäev on mõlemad tühjad.</span><span class="sxs-lookup"><span data-stu-id="f4185-123">It’s also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="f4185-124">Kui nii välja Aktiveerimiskuupäev kui ka välja Aegumiskuupäev kuupäevad on tulevikus, ei ole elektroonilised maksed võimalikud.</span><span class="sxs-lookup"><span data-stu-id="f4185-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="f4185-125">Muud makseviisid on kättesaadavad ja pangakonto on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="f4185-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="f4185-126">Laiendage jaotist Seadistus.</span><span class="sxs-lookup"><span data-stu-id="f4185-126">Expand the Setup section.</span></span>
14. <span data-ttu-id="f4185-127">Sisestage väärtus väljale Teksti kood.</span><span class="sxs-lookup"><span data-stu-id="f4185-127">In the Text code field, type a value.</span></span>
    * <span data-ttu-id="f4185-128">Sellel väljal on määratud kood, mis kuvatakse saaja pangaväljavõttel.</span><span class="sxs-lookup"><span data-stu-id="f4185-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="f4185-129">Sisestage väärtus väljale Teade pangale.</span><span class="sxs-lookup"><span data-stu-id="f4185-129">In the Message to bank field, type a value.</span></span>
16. <span data-ttu-id="f4185-130">Tippige väärtus väljale Vahetuskursi viide.</span><span class="sxs-lookup"><span data-stu-id="f4185-130">In the Exchange reference field, type a value.</span></span>
    * <span data-ttu-id="f4185-131">See on mis tahes edaspidise või fikseeritud tähtajaga vahetuskursi viitenumber.</span><span class="sxs-lookup"><span data-stu-id="f4185-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>  
17. <span data-ttu-id="f4185-132">Valige või sisestage väärtus väljal Valuuta.</span><span class="sxs-lookup"><span data-stu-id="f4185-132">In the Currency field, enter or select a value.</span></span>
    * <span data-ttu-id="f4185-133">Eelpäringute väljastamisel annab see jaotis ülevaate nende olekust (ootel või kinnitatud).</span><span class="sxs-lookup"><span data-stu-id="f4185-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="f4185-134">Laiendage jaotist Aadress.</span><span class="sxs-lookup"><span data-stu-id="f4185-134">Expand the Address section.</span></span>
19. <span data-ttu-id="f4185-135">Laiendage jaotist Eelpäringud.</span><span class="sxs-lookup"><span data-stu-id="f4185-135">Expand the Prenotes section.</span></span>
20. <span data-ttu-id="f4185-136">Laiendage jaotist Kontaktteave.</span><span class="sxs-lookup"><span data-stu-id="f4185-136">Expand the Contact information section.</span></span>
21. <span data-ttu-id="f4185-137">Sisestage väärtus väljale Telefon.</span><span class="sxs-lookup"><span data-stu-id="f4185-137">In the Telephone field, type a value.</span></span>
22. <span data-ttu-id="f4185-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f4185-138">Close the page.</span></span>
23. <span data-ttu-id="f4185-139">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="f4185-139">Click Edit.</span></span>
24. <span data-ttu-id="f4185-140">Laiendage jaotist Makse.</span><span class="sxs-lookup"><span data-stu-id="f4185-140">Expand the Payment section.</span></span>
25. <span data-ttu-id="f4185-141">Valige väljalt Pangakonto äsja loodud konto.</span><span class="sxs-lookup"><span data-stu-id="f4185-141">In the Bank  account field, select the account that you’ve just created.</span></span>
26. <span data-ttu-id="f4185-142">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f4185-142">Click Save.</span></span>
    * <span data-ttu-id="f4185-143">Aadress võib pärineda pangagrupist, kui see on määratud, või võite selle siin lisada.</span><span class="sxs-lookup"><span data-stu-id="f4185-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  

