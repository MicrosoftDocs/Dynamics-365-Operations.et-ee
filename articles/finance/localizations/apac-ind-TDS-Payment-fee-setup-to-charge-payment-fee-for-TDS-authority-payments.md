---
title: Maksetasude häälestamine TDS-i halduri maksete jaoks
description: See teema kirjeldab, kuidas seadistada maksetasusid, mida arvatakse maha allika (TDS) maksuameti maksetes.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023193"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="09d77-103">Maksetasude häälestamine TDS-i halduri maksete jaoks</span><span class="sxs-lookup"><span data-stu-id="09d77-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09d77-104">See teema kirjeldab, kuidas seadistada maksetasusid, mida arvatakse maha allika (TDS) maksuameti maksetes.</span><span class="sxs-lookup"><span data-stu-id="09d77-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="09d77-105">Avage **Ostureskontro \> Makse seadistus \> Maksetasu**.</span><span class="sxs-lookup"><span data-stu-id="09d77-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="09d77-106">[![Maksetasu leht](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="09d77-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="09d77-107">Klõpsake valikut **Uus**, et luua maksetööleht, ja sisestage seejärel nõutavad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="09d77-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="09d77-108">Valige **Makse tüüp** väljal tüüp, et valida makse tüüpi:</span><span class="sxs-lookup"><span data-stu-id="09d77-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="09d77-109">**None**</span><span class="sxs-lookup"><span data-stu-id="09d77-109">**None**</span></span>
    - <span data-ttu-id="09d77-110">**Viivis** – viivist võetakse TDS-i maksu hankijale tehtud hilinenud maksetelt.</span><span class="sxs-lookup"><span data-stu-id="09d77-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="09d77-111">**Teised** –Teised maksed võetakse TDS-i maksu hankijale tehtud hilinenud maksetelt.</span><span class="sxs-lookup"><span data-stu-id="09d77-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="09d77-112">Kui valite **Intress** või **Muud**, **Tasu** väljal väärtuseks automaatselt **Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="09d77-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="09d77-113">Kui valisite väljal **Intress** või **Teised** väljal **Välja tüüp**, väljal **Põhikonto**, valige pearaamatukonto, et sisestada viivist või muid makse.</span><span class="sxs-lookup"><span data-stu-id="09d77-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="09d77-114">Sisestage kõik vajalikud üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="09d77-114">Enter the other required details.</span></span>
6. <span data-ttu-id="09d77-115">Tegevuspaanil valige **Maksetasu seadistus**, et avada **Maksetasu seadistuse** leht, kus saate seadistada pankade, makseviiside, maksespetsifikatsioonide, valuutade ja ajaintervallide erinevate kombinatsioonide maksetasud.</span><span class="sxs-lookup"><span data-stu-id="09d77-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="09d77-116">[![Maksetasu seadistuse leht](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="09d77-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="09d77-117">Määrake vahekaardi **Ülevaade** väljal **Grupeerimised**, millistele pankadele maksetasu seadistate:</span><span class="sxs-lookup"><span data-stu-id="09d77-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="09d77-118">**Tabel""** – tasu kehtib konkreetse pangakonto kohta.</span><span class="sxs-lookup"><span data-stu-id="09d77-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="09d77-119">**Grupp** – tasu kehtib konkreetse pangak grupi kohta.</span><span class="sxs-lookup"><span data-stu-id="09d77-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="09d77-120">**Kõik** – tasu kehtib kõikide pangakontode puhul.</span><span class="sxs-lookup"><span data-stu-id="09d77-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="09d77-121">Kui valisite väljal **Tabel** või **Grupp** **Grupeerimised** väljal, valige **Pangaseose** väljal konkreetne pangakonto või pangagrupp, mille jaoks maksetasu seadistate.</span><span class="sxs-lookup"><span data-stu-id="09d77-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="09d77-122">Väljal **Maksemeetod** valige meetod, mida maksetasu maksmise puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="09d77-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="09d77-123">Väljal **Makse täpsustus** valige või sisestage makse täpsustuse kood, mis loodi **Makse täpsustuse** lehel.</span><span class="sxs-lookup"><span data-stu-id="09d77-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="09d77-124">Suvandit Makse täpsustus kasutatakse elektroonilise ülekande makseviisidega.</span><span class="sxs-lookup"><span data-stu-id="09d77-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="09d77-125">Valige väljal **Maksu valuuta** makse valuuta, mis aktiveerib tasu.</span><span class="sxs-lookup"><span data-stu-id="09d77-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="09d77-126">Tasu saab aktiveerida ainult valitud valuutat kasutavad kanded.</span><span class="sxs-lookup"><span data-stu-id="09d77-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="09d77-127">Kui jätate selle välja tühjaks, aktiveerivad tasu kõik valuutad.</span><span class="sxs-lookup"><span data-stu-id="09d77-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="09d77-128">Valige **Protsent/Summa** väljal arvutusmeetod.</span><span class="sxs-lookup"><span data-stu-id="09d77-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="09d77-129">Valikud on **Summa**, **Protsent** ja **Intervall**.</span><span class="sxs-lookup"><span data-stu-id="09d77-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="09d77-130">Väljal **Tasu summa** määrake tasu summa kas makse protsendina või ühe makse summana.</span><span class="sxs-lookup"><span data-stu-id="09d77-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="09d77-131">Valige väljas **Maksu valuuta** maksu valuuta.</span><span class="sxs-lookup"><span data-stu-id="09d77-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="09d77-132">Valige **Üldine** vahekaart valitud bangakonto üksikasjade vaatamiseks või muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="09d77-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="09d77-133">[![Vahekaart Üldine](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="09d77-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="09d77-134">Sisestage **Minimaalne** väljal minimaalne kandesumma, mis aktiveerib tasu.</span><span class="sxs-lookup"><span data-stu-id="09d77-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="09d77-135">Sisestage **Maksimaaalne** väljal maksimaalne kandesumma, mis aktiveerib tasu.</span><span class="sxs-lookup"><span data-stu-id="09d77-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="09d77-136">Väljadel **Alates** ja **Kuni kuupäevani** määratlege arvutamiseks kuupäevavahemik.</span><span class="sxs-lookup"><span data-stu-id="09d77-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="09d77-137">Väljal **Minimaalne tasu** määrake tasu summa kas makse protsendina või ühe makse summana.</span><span class="sxs-lookup"><span data-stu-id="09d77-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="09d77-138">Valige **Käibemaksugrupp** väljal käibemaksugrupp, mida kasutada tasusumma käibemaksu arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="09d77-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="09d77-139">Valige **Käibemaksugrupp** väljal käibemaksugrupp, mida kasutada tasusumma käibemaksu arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="09d77-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="09d77-140">Valige vahekaart **Intervall**.</span><span class="sxs-lookup"><span data-stu-id="09d77-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="09d77-141">[![Vahekaart Intervall](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="09d77-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="09d77-142">Väljal **Päevad** sisestage rahaülekande sisestuskuupäeva (allahindluskuupäeva) ja võlatähe tähtaja vahele jäävate päevade arv.</span><span class="sxs-lookup"><span data-stu-id="09d77-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="09d77-143">Valige **Protsent/Summa** väljal kas täpsustus on protsent või seatud summa.</span><span class="sxs-lookup"><span data-stu-id="09d77-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="09d77-144">Väljal **Minimaalne tasu** määrake tasu summa kas makse protsendina või ühe makse summana.</span><span class="sxs-lookup"><span data-stu-id="09d77-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="09d77-145">Sulgege **Maksetasu seadistuse** leht.</span><span class="sxs-lookup"><span data-stu-id="09d77-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="09d77-146">Sulgege **Maksetasu** leht.</span><span class="sxs-lookup"><span data-stu-id="09d77-146">Close the **Payment fee** page.</span></span>
