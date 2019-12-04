---
title: Kliendi maksetasude määramine
description: Looge kliendimaksete maksetasud.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5b94578e077834ce73c921dca18ad6e38c37659
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177390"
---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="1781e-103">Kliendi maksetasude määramine</span><span class="sxs-lookup"><span data-stu-id="1781e-103">Establish customer payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1781e-104">Looge kliendimaksete maksetasud.</span><span class="sxs-lookup"><span data-stu-id="1781e-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="1781e-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="1781e-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="1781e-106">**Navigeerimispaanil** avage **Moodulid > Müügireskontro > Maksete seadistamine > Makse maks**.</span><span class="sxs-lookup"><span data-stu-id="1781e-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Payment fee**.</span></span>
2. <span data-ttu-id="1781e-107">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1781e-107">Click **New**.</span></span>
3. <span data-ttu-id="1781e-108">Sisestage väljale **Maksu ID** maksu ID.</span><span class="sxs-lookup"><span data-stu-id="1781e-108">In the **Fee ID** field, enter a Fee ID.</span></span> <span data-ttu-id="1781e-109">Tasu ID kuvatakse makse töölehtedel, mistõttu muutke see kirjeldavaks, et aru saada, millist tasu hinnatakse.</span><span class="sxs-lookup"><span data-stu-id="1781e-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="1781e-110">Sisestage väljale **Nimi** makse nimi.</span><span class="sxs-lookup"><span data-stu-id="1781e-110">In the **Name** field, enter a fee name.</span></span>
5. <span data-ttu-id="1781e-111">Kirjeldage makset väljal **Makse kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="1781e-111">In the **Fee description** field, enter a description for the fee.</span></span>
6. <span data-ttu-id="1781e-112">Väljal **Kulu** vali, kas kulu võetakse kliendi või pearaamatu kontolt.</span><span class="sxs-lookup"><span data-stu-id="1781e-112">In the **Charge** field, select whether the fee will be charged to the Customer or a Ledger account.</span></span> <span data-ttu-id="1781e-113">Kui hinnatakse kliendi tasu, valige suvand Klient.</span><span class="sxs-lookup"><span data-stu-id="1781e-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="1781e-114">Kui tasu hinnatakse teie organisatsiooni kuluna, valige Pearaamat.</span><span class="sxs-lookup"><span data-stu-id="1781e-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="1781e-115">Selle ülesande puhul valige Klient.</span><span class="sxs-lookup"><span data-stu-id="1781e-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="1781e-116">Valige väljas **Päeviku tüüp** seda makse maksu kasutada saav päeviku tüüp.</span><span class="sxs-lookup"><span data-stu-id="1781e-116">In the **Journal type** field, select the type of journal that can use this payment fee.</span></span> <span data-ttu-id="1781e-117">Nende tasude kasutamisel kliendimakseteks on töölehe tüübiks tõenäoliselt Kliendimakse.</span><span class="sxs-lookup"><span data-stu-id="1781e-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="1781e-118">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1781e-118">Click **Save**.</span></span>
9. <span data-ttu-id="1781e-119">Klõpsake **Makse maksu seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="1781e-119">Click **Payment fee setup**.</span></span> <span data-ttu-id="1781e-120">Makse tasu seadistust kasutatakse kriteeriumide määratlemiseks, mil maksetasu hinnatakse.</span><span class="sxs-lookup"><span data-stu-id="1781e-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="1781e-121">Näiteks saate määrata, et tasu arvutatakse, kui pangakontoks on USMF OPER ja makseviisiks on tšekk.</span><span class="sxs-lookup"><span data-stu-id="1781e-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="1781e-122">Selleks, et hinnata, millisele pangakontole see maks läheb, valige väljal **Rühmitamine** „Tabel“, „Rühm“ või „Kõik“.</span><span class="sxs-lookup"><span data-stu-id="1781e-122">In the **Groupings** field, select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span> <span data-ttu-id="1781e-123">Kui valite suvandi Kõik, võidakse seda tasu hinnata kõigil pangakontodel.</span><span class="sxs-lookup"><span data-stu-id="1781e-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="1781e-124">Valides suvandi Tabel, võidakse seda tasu hinnata ainult teie valitud pangakontol.</span><span class="sxs-lookup"><span data-stu-id="1781e-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="1781e-125">Suvandi Grupp valimisel võidakse seda tasu hinnata ainult valitud pangagrupi pangakontodel.</span><span class="sxs-lookup"><span data-stu-id="1781e-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="1781e-126">Valige väljas **Panga seos** panga rühm või pangakonto.</span><span class="sxs-lookup"><span data-stu-id="1781e-126">In the **Bank relation** field, select either a bank group or a bank account.</span></span> <span data-ttu-id="1781e-127">Suvandi Tabel valimisel kuvab otsing pangakontod.</span><span class="sxs-lookup"><span data-stu-id="1781e-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="1781e-128">Suvandi Grupp valimisel kuvab otsing pangagrupid.</span><span class="sxs-lookup"><span data-stu-id="1781e-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="1781e-129">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="1781e-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="1781e-130">Väljas **Makseviis** valige, millisele makseviisile see maks kehtib.</span><span class="sxs-lookup"><span data-stu-id="1781e-130">In the **Mehtod of payment** field, select the Method of payment for which this fee will be assessed.</span></span> <span data-ttu-id="1781e-131">Näiteks võite määrata tasu klientidele, kui nad saadavad makseid pigem tšekina kui elektroonilise maksena.</span><span class="sxs-lookup"><span data-stu-id="1781e-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="1781e-132">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="1781e-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="1781e-133">Vajadusel sisestage välja **Makse valuuta** makse valuuta.</span><span class="sxs-lookup"><span data-stu-id="1781e-133">If relevant, in the **Payment currency** field, enter a payment currency.</span></span> <span data-ttu-id="1781e-134">Makse valuutat kasutatakse tasu määramise täiendavate kriteeriumidena.</span><span class="sxs-lookup"><span data-stu-id="1781e-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="1781e-135">Näiteks võib teie pank nõuda lisatasu USA dollarites saadud maksete eest, kuna nad teevad üldjuhul tehinguid ainult eurodes.</span><span class="sxs-lookup"><span data-stu-id="1781e-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="1781e-136">Valige, kas tasu on protsent, summa või intervall.</span><span class="sxs-lookup"><span data-stu-id="1781e-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="1781e-137">Sisestage välja **Protsent/summa**, kas maksu protsent või summa.</span><span class="sxs-lookup"><span data-stu-id="1781e-137">In the **Percentage/Amount field**, enter either percentage or amount of the fee.</span></span> <span data-ttu-id="1781e-138">Kui välja Protsent/summa väärtuseks on Protsent, on siin sisestatud väärtus protsent.</span><span class="sxs-lookup"><span data-stu-id="1781e-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="1781e-139">Kui välja Protsent/summa väärtuseks on Summa, on siin sisestatud väärtus summa.</span><span class="sxs-lookup"><span data-stu-id="1781e-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="1781e-140">Kui välja Protsent/summa väärtuseks on Intervall, kasutage kihtide määratlemiseks vahekaarti Intervall.</span><span class="sxs-lookup"><span data-stu-id="1781e-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="1781e-141">Valige väljas **Maksu valuuta** maksu valuuta.</span><span class="sxs-lookup"><span data-stu-id="1781e-141">In the **Fee currency** field, select the currency of the fee.</span></span> <span data-ttu-id="1781e-142">See on valuuta, milles tasu luuakse.</span><span class="sxs-lookup"><span data-stu-id="1781e-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="1781e-143">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1781e-143">Click **Save**.</span></span>
