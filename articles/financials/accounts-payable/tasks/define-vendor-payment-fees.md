---
title: Hankija maksetasude määratlemine
description: Hankija maksetasude seadistus.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 399291a98ddc6b01fb08f7a5c629ec7a6f8acfbf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "363196"
---
# <a name="define-vendor-payment-fees"></a><span data-ttu-id="6b2ee-103">Hankija maksetasude määratlemine</span><span class="sxs-lookup"><span data-stu-id="6b2ee-103">Define vendor payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b2ee-104">Hankija maksetasude seadistus.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-104">Set up vendor payment fees.</span></span> <span data-ttu-id="6b2ee-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="6b2ee-106">Avage Ostureskontro > Makse seadistus > Maksetasu.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-106">Go to Accounts payable > Payment setup > Payment fee.</span></span>
2. <span data-ttu-id="6b2ee-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-107">Click New.</span></span>
3. <span data-ttu-id="6b2ee-108">Sisestage väärtus väljale Tasu ID.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-108">In the Fee ID field, type a value.</span></span>
    * <span data-ttu-id="6b2ee-109">Tasu ID peaks kirjeldama, millal seda tasu kasutatakse, näiteks EFT_Tasu.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-109">The Fee ID should describe when this fee will be used, such as "EFT_Fee".</span></span>  
4. <span data-ttu-id="6b2ee-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="6b2ee-111">Sisestage väärtus väljale Tasu kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-111">In the Fee description field, type a value.</span></span>
    * <span data-ttu-id="6b2ee-112">Lisage kirjeldus lisateabe pakkumiseks selle kohta, millal tasu määratakse.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-112">Add a description to provide more detail on when the fee is assessed.</span></span>  
6. <span data-ttu-id="6b2ee-113">Valige väljal Tasu kas suvand Hankija või Pearaamat.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-113">In the Charge field, select either Vendor or Ledger.</span></span>
    * <span data-ttu-id="6b2ee-114">Pearaamatut kasutatakse, kui tasu kantakse teie organisatsiooni kuludesse.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-114">Ledger is used when the fee will be expensed to your organization.</span></span>  <span data-ttu-id="6b2ee-115">Hankijat kasutatakse, kui tasu määratakse hankijale.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-115">Vendor is used when the fee will be assessed to the vendor.</span></span>  
7. <span data-ttu-id="6b2ee-116">Sisestage põhikonto, mille kuludesse tasu läheb.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-116">Enter a main account for where the fee will be expensed.</span></span>
    * <span data-ttu-id="6b2ee-117">See suvand on kasutatav ainult juhul, kui suvandi Tasu puhul on valitud Pearaamat.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-117">This option is only available when selecting Ledger as the Charge option.</span></span>  
8. <span data-ttu-id="6b2ee-118">Sisestage tööleht, millel seda tasu saab kasutada.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-118">Select the journal on which this fee can be used.</span></span> 
    * <span data-ttu-id="6b2ee-119">Hankija maksetasu puhul valiksite töölehe Maksed hankijale.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-119">For a vendor payment fee, you would select the journal 'Vendor disbursement.'</span></span>  
9. <span data-ttu-id="6b2ee-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-120">Click Save.</span></span>
10. <span data-ttu-id="6b2ee-121">Klõpsake suvandit Maksetasu seadistus.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-121">Click Payment fee setup.</span></span>
    * <span data-ttu-id="6b2ee-122">Jätkake maksetasu seadistusega, et määratleda, millal tuleks tasu teie valitud töölehele vaikimisi lisada.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-122">Continue to the Payment fee setup to define when the fee should default onto the journal you selected.</span></span>  
11. <span data-ttu-id="6b2ee-123">Valige kas suvand Tabel, Grupp või Kõik.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-123">Select either Table, Group or All.</span></span>
    * <span data-ttu-id="6b2ee-124">Tabelit kasutatakse ühe pangakonto valimiseks, gruppi kasutatakse pangagrupi valimiseks ja suvandit Kõik selle tasu seadistuse kasutamiseks kõigi pangakontode puhul</span><span class="sxs-lookup"><span data-stu-id="6b2ee-124">Table is used to select a single bank account, Group is used to select a bank group, and All is to use this fee setup for all bank accounts</span></span>  
12. <span data-ttu-id="6b2ee-125">Valige kas pangagrupp või pangakonto.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-125">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="6b2ee-126">Otsing näitab pangagruppi, kui valisite suvandi Grupp ja pangakontosid, kui valisite suvandi Tabel.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-126">The lookup will show bank group if you selected Group, and will show bank accounts if you selected Table.</span></span>  
13. <span data-ttu-id="6b2ee-127">Valige makseviis, mis selle tasu puhul määratakse.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-127">Select the method of payment for when this fee will be assessed.</span></span>
14. <span data-ttu-id="6b2ee-128">Valige valitud makseviisi puhul suvand Makse täpsustus.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-128">Select the Payment specification for the selected method of payment.</span></span>
    * <span data-ttu-id="6b2ee-129">Suvandit Makse täpsustus kasutatakse elektroonilise ülekande makseviisidega.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-129">The Payment specification is used with electronic fund transfer methods of payment.</span></span>  
15. <span data-ttu-id="6b2ee-130">Valige, kas tasu on protsent, summa või intervall.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-130">Select whether the fee is a percentage, amount or interval.</span></span>
16. <span data-ttu-id="6b2ee-131">Sisestage tasu protsent või summa.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-131">Enter the percentage or amount of the fee.</span></span>
    * <span data-ttu-id="6b2ee-132">Kui tasuks on protsent, sisestage protsent.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-132">If the Fee is a percentage, enter the percentage.</span></span> <span data-ttu-id="6b2ee-133">Kui tasuks on summa, sisestage tasu summa.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-133">If the Fee is an amount, enter the amount of the fee.</span></span> <span data-ttu-id="6b2ee-134">Kui tasuks on intervall, kasutage mitmetasandiliste tasude määratlemiseks vahekaarti Intervall.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-134">If the Fee is an interval, use the Interval tab to defined the tiered fees.</span></span>  
17. <span data-ttu-id="6b2ee-135">Valige väljal Tasu valuuta see valuuta, milles tasu määratakse.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-135">In the Fee currency field, select the currency in which the fee will be assessed.</span></span>
    * <span data-ttu-id="6b2ee-136">See on tasu valuutakood.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-136">This currency is for the fee.</span></span> <span data-ttu-id="6b2ee-137">Makse valuutat kasutatakse määratlemaks, millal tasu reeglit tuleks määrata makse valuuta põhjal.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-137">The payment currency is used to define when the fee rule should be assessed based on the payment's currency.</span></span> <span data-ttu-id="6b2ee-138">Näiteks võib teie pank nõuda tasu, kui makse on tehtud eurodes, kuid kõikidele muudele maksetele pole tasu määratud.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-138">For example, your bank may charge a fee when a payment is made in EUR, but all other payments aren't assessed a fee.</span></span>  
18. <span data-ttu-id="6b2ee-139">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6b2ee-139">Click Save.</span></span>

