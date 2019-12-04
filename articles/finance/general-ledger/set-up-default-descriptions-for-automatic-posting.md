---
title: Saate seadistada vaikekirjeldused automaatseks sisestamiseks
description: Selles teemas selgitatakse, kuidas seadistada vaiketeksti, mida kasutatakse automaatselt pearaamatusse sisestatavate raamatupidamiskirjete kirjeldamiseks kasutatavat vaiketeksti. Saate seadistada vaikimisi kirjeldusteksti, kasutades vabateksti või valides fikseeritud muutujad.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: eb89f50a3d227cad80226ce30f71c4f210129245
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622685"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="0d5ea-104">Saate seadistada vaikekirjeldused automaatseks sisestamiseks</span><span class="sxs-lookup"><span data-stu-id="0d5ea-104">Set up default descriptions for automatic posting</span></span>

<span data-ttu-id="0d5ea-105">Selles teemas selgitatakse, kuidas seadistada vaiketeksti, mida kasutatakse automaatselt pearaamatusse sisestatavate raamatupidamiskirjete kirjeldamiseks kasutatavat vaiketeksti.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="0d5ea-106">Saate seadistada vaikimisi kirjeldusteksti, kasutades vabateksti või valides fikseeritud muutujad.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="0d5ea-107">Teatud riikides või piirkondades saate mõne kandetüübi puhul kaasata ka teksti nende kandetüüpidega seotud väljadelt rakenduse Microsoft Dynamics AX andmebaasis.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="0d5ea-108">Kandetüüpide ning riikide ja regioonide loendi leiate selle teema jaotisest [Valikuline: muu teksti lisamine vaikekirjeldustele](#optional-add-other-text-to-default-descriptions).</span><span class="sxs-lookup"><span data-stu-id="0d5ea-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="0d5ea-109">Vaikekirjelduste seadistamine</span><span class="sxs-lookup"><span data-stu-id="0d5ea-109">Set up default descriptions</span></span>

1. <span data-ttu-id="0d5ea-110">Valige **Organisatsiooni haldus** \> **Seadistus** \> **Vaikekirjeldused**.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="0d5ea-111">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="0d5ea-112">Väljal **Kirjeldus** valige kandetüüp, mille jaoks vaikekirjeldus luuakse.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="0d5ea-113">Väljal **Keel** valige keel, millele see kirjeldus kehtib.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="0d5ea-114">Väljal **Tekst** sisestage vaikekirjeldus.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="0d5ea-115">Saate teksti tippida väljale või kasutada ühte või mitut järgmist vabas vormis muutujat.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="0d5ea-116">**%1** – lisage kande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="0d5ea-117">**%2** – lisage identifikaator, mis vastab pearaamatusse sisestatava dokumendi tüübile.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="0d5ea-118">Näiteks arvetega seotud kandetüüpide puhul lisab muutuja **%2** arvenumbri.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="0d5ea-119">**%3** – lisage identifikaator, mis on seotud pearaamatusse sisestatava dokumendi tüübiga.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="0d5ea-120">Näiteks arvetega seotud kandetüüpide puhul lisab muutuja **%3** kliendikonto numbri.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="0d5ea-121">Valikuline: muu teksti lisamine vaikekirjeldustele</span><span class="sxs-lookup"><span data-stu-id="0d5ea-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="0d5ea-122">Teatud riikides või piirkondades saate mõne kandetüübi puhul kasutada vaikekirjeldustes teksti, mis pärineb nende kandetüüpidega seotud andmete väljadelt.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="0d5ea-123">Järgmistes loendites on näidatud kandetüübid ning riigid ja piirkonnad, mille puhul see valik saadaval on.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="0d5ea-124">**Kandetüübid**</span><span class="sxs-lookup"><span data-stu-id="0d5ea-124">**Transaction types**</span></span>

<span data-ttu-id="0d5ea-125">Saate lisada muud teksti kandetüüpide vaikekirjeldustele, mis on seotud järgmiste dokumenditüüpidega.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="0d5ea-126">Kliendiarved</span><span class="sxs-lookup"><span data-stu-id="0d5ea-126">Customer invoices</span></span>
- <span data-ttu-id="0d5ea-127">Kliendi kreeditarved</span><span class="sxs-lookup"><span data-stu-id="0d5ea-127">Customer credit notes</span></span>
- <span data-ttu-id="0d5ea-128">Kliendi sularahamaksed</span><span class="sxs-lookup"><span data-stu-id="0d5ea-128">Customer cash payments</span></span>
- <span data-ttu-id="0d5ea-129">Müüja maksed</span><span class="sxs-lookup"><span data-stu-id="0d5ea-129">Vendor payments</span></span>
- <span data-ttu-id="0d5ea-130">Müügitellimused</span><span class="sxs-lookup"><span data-stu-id="0d5ea-130">Sales orders</span></span>
- <span data-ttu-id="0d5ea-131">Ostutellimused</span><span class="sxs-lookup"><span data-stu-id="0d5ea-131">Purchase orders</span></span>
- <span data-ttu-id="0d5ea-132">Laotöölehed</span><span class="sxs-lookup"><span data-stu-id="0d5ea-132">Inventory journals</span></span>
- <span data-ttu-id="0d5ea-133">Koondplaneerimine (MRP)</span><span class="sxs-lookup"><span data-stu-id="0d5ea-133">Master planning (MRP)</span></span>
- <span data-ttu-id="0d5ea-134">Põhivarad</span><span class="sxs-lookup"><span data-stu-id="0d5ea-134">Fixed assets</span></span>

<span data-ttu-id="0d5ea-135">**Riigid ja piirkonnad**</span><span class="sxs-lookup"><span data-stu-id="0d5ea-135">**Countries and regions**</span></span>

<span data-ttu-id="0d5ea-136">See valik on saadaval järgmistes riikides ja piirkondades:</span><span class="sxs-lookup"><span data-stu-id="0d5ea-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="0d5ea-137">Brasiilia</span><span class="sxs-lookup"><span data-stu-id="0d5ea-137">Brazil</span></span>
- <span data-ttu-id="0d5ea-138">Hiina</span><span class="sxs-lookup"><span data-stu-id="0d5ea-138">China</span></span>
- <span data-ttu-id="0d5ea-139">Tšehhi Vabariik</span><span class="sxs-lookup"><span data-stu-id="0d5ea-139">Czech Republic</span></span>
- <span data-ttu-id="0d5ea-140">Ida-Euroopa</span><span class="sxs-lookup"><span data-stu-id="0d5ea-140">Eastern Europe</span></span>
- <span data-ttu-id="0d5ea-141">Ungari</span><span class="sxs-lookup"><span data-stu-id="0d5ea-141">Hungary</span></span>
- <span data-ttu-id="0d5ea-142">India</span><span class="sxs-lookup"><span data-stu-id="0d5ea-142">India</span></span>
- <span data-ttu-id="0d5ea-143">Jaapan</span><span class="sxs-lookup"><span data-stu-id="0d5ea-143">Japan</span></span>
- <span data-ttu-id="0d5ea-144">Leedu</span><span class="sxs-lookup"><span data-stu-id="0d5ea-144">Lithuania</span></span>
- <span data-ttu-id="0d5ea-145">Läti</span><span class="sxs-lookup"><span data-stu-id="0d5ea-145">Latvia</span></span>
- <span data-ttu-id="0d5ea-146">Poola</span><span class="sxs-lookup"><span data-stu-id="0d5ea-146">Poland</span></span>
- <span data-ttu-id="0d5ea-147">Venemaa</span><span class="sxs-lookup"><span data-stu-id="0d5ea-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="0d5ea-148">Muu teksti lisamine vaikekirjeldustele</span><span class="sxs-lookup"><span data-stu-id="0d5ea-148">Add text to default descriptions</span></span>

<span data-ttu-id="0d5ea-149">Pärast selle teema varasemas jaotises [Vaikekirjelduste seadistamine](#set-up-default-descriptions) toodud sammude läbimist tehke vaikekirjeldustele muu teksti lisamiseks järgmist.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="0d5ea-150">Valige kiirkaardil **Parameetrid** valik **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="0d5ea-151">Valige väljal **Viitetabel** andmebaasi tabel, millest parameetriandmed kirjeldusse lisada.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="0d5ea-152">Valige väljal **Viiteväli** väli, millest parameetriandmed kirjeldusse lisada.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="0d5ea-153">Parameetrite lisamiseks korrake samme 1 kuni 3.</span><span class="sxs-lookup"><span data-stu-id="0d5ea-153">Repeat steps 1 through 3 to add more parameters.</span></span>