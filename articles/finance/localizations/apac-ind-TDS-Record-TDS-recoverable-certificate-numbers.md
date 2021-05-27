---
title: TDS-i tagastatava sertifikaadi numbrite kirjendamine
description: See teema selgitab, kuidas kasutada tagasisaadav sertide lehte, et kirjendada sertide numbreid ja kuupäevi allika (TDS) sertide jaoks, mis on vastu võetud kindla hankija, kliendi või pearaamatu jaoks.
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023164"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="49590-103">TDS-i tagastatava sertifikaadi numbrite kirjendamine</span><span class="sxs-lookup"><span data-stu-id="49590-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49590-104">See teema selgitab, kuidas kasutada **tagasisaadavat sertide** lehte, et kirjendada sertide numbreid ja kuupäevi allika (TDS) sertide jaoks, mis on vastu võetud kindla hankija, kliendi või pearaamatu jaoks.</span><span class="sxs-lookup"><span data-stu-id="49590-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="49590-105">TDS-i serdi numbrite ja kuupäevade värskendamiseks, mis on kirjendatud TDS-i kannete jaoks sellel leheküljel, kasutage **Uuenda serti** lehte (**Pearaamat \> Perioodiline \> Kinnipeetava maksu \> Serdi värskendamine**).</span><span class="sxs-lookup"><span data-stu-id="49590-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="49590-106">Pärast TDS-i serdinumbrite värskendamist sulgege need.</span><span class="sxs-lookup"><span data-stu-id="49590-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="49590-107">Järgige neid samme TDS-i serdi numbrite ja kuupäevade salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="49590-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="49590-108">Avage **Maks \> Kaudsed maksud \> Kinnipeetav maks \> taastatavad serdid**.</span><span class="sxs-lookup"><span data-stu-id="49590-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="49590-109">[![Taastatavate sertide leht](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="49590-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="49590-110">Valige **taastatavad serid** lehel, **maksutüübi** väljal valige **TDS**.</span><span class="sxs-lookup"><span data-stu-id="49590-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="49590-111">Valige **Uus**, et luua uus kirje.</span><span class="sxs-lookup"><span data-stu-id="49590-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="49590-112">Väljale **Serdinumber** sisestage TDS-i kontsessiooniserdi number.</span><span class="sxs-lookup"><span data-stu-id="49590-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="49590-113">Valige **Kontotüübi** väljal konto tüüp, mille kohta TDS-sert on saadud: **Hanija**, **klient**, või **pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="49590-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="49590-114">Sõltuvalt **Konto** väljast valige hankija-, kliendi-või pearaamatukonto number, sõltuvalt valitud kontotüübist.</span><span class="sxs-lookup"><span data-stu-id="49590-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="49590-115">Väljal **Nimi** kuvatakse hankija, kliendi või pearaamatukonto nimi.</span><span class="sxs-lookup"><span data-stu-id="49590-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="49590-116">Väljal **Serte kokku** sisestage digitaalsete sertifikaatide kogus.</span><span class="sxs-lookup"><span data-stu-id="49590-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="49590-117">Väljale **Kuupäev** sisestage TDS-i kontsessiooniserdi numbri kuupäev.</span><span class="sxs-lookup"><span data-stu-id="49590-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="49590-118">Valige **Päringud** et avada **Serdi kannete** leht, kus saate vaadata TDS-i kandeid, mille jaoks on TDS-tunnistuse number ja kuupäev uuendatud.</span><span class="sxs-lookup"><span data-stu-id="49590-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="49590-119">Seda teavet saab uuendada **Serdi värskendamine** lehel (**Maks \> Deklaratsioonid \> Kinnipeetav maks \> Värskenda sert**).</span><span class="sxs-lookup"><span data-stu-id="49590-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="49590-120">**Serdi uuendamise** lehel kuvatakse TDS-kande kohta järgmine teave:</span><span class="sxs-lookup"><span data-stu-id="49590-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="49590-121">**Kuupäev** – TDS kannete sisestuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="49590-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="49590-122">**Kviitung** - kuvatakse TDS tehingukande kviitungi number.</span><span class="sxs-lookup"><span data-stu-id="49590-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="49590-123">**Allikas** - moodul, kus TDS-kanne loodi.</span><span class="sxs-lookup"><span data-stu-id="49590-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="49590-124">**Konto** – hankija-, kliendi- või pearaamatukonto number, mille jaoks TDS-kanne loodi.</span><span class="sxs-lookup"><span data-stu-id="49590-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="49590-125">**Nimi** – hankija-, kliendi- või pearaamatukonto number, mille jaoks TDS-kanne loodi.</span><span class="sxs-lookup"><span data-stu-id="49590-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="49590-126">**Summa** - arvele sisestatud summa, mida TDS on arvutanud.</span><span class="sxs-lookup"><span data-stu-id="49590-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="49590-127">**Maksusumma** – TDS-i maksusumma, mis kande jaoks arvutatud.</span><span class="sxs-lookup"><span data-stu-id="49590-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="49590-128">**Serdi kuupäev** – TDS-i serdi kuupäev, mis uuendati TDS-kande jaoks.</span><span class="sxs-lookup"><span data-stu-id="49590-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="49590-129">**Serdi number** – TDS-i serdi number, mis uuendati TDS-kande jaoks.</span><span class="sxs-lookup"><span data-stu-id="49590-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="49590-130">Lehel **Taastatavad serdid** valige märkeruut **Suletud** et sulgeda TDS-i serdi number pärast seda, kui olete selle TDS-kannete värskendamise lõpetanud **Värskenda sertifikaat** lehel.</span><span class="sxs-lookup"><span data-stu-id="49590-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="49590-131">Kõigi leheküljel kirjete jaoks **Suletud** märkeruudu märkimiseks valige **Märgi kõik**.</span><span class="sxs-lookup"><span data-stu-id="49590-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="49590-132">TDS-i serdinumbrid, mille jaoks on valitud märkeruut **Suletud**, pole saadaval **serdi värskendamise** lehel.</span><span class="sxs-lookup"><span data-stu-id="49590-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
