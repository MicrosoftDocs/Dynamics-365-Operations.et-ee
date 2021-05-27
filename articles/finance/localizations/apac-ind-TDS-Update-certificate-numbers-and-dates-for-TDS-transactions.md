---
title: TDS-i kannete sertifikaadinumbrite ja kuupäevade uuendamine
description: See teema selgitab, kuidas kasutada tagasisaadava sertide lehte, et kirjendada sertide numbreid ja kuupäevi allika (TDS) sertide jaoks, mis on vastu võetud kindla hankija, kliendi või pearaamatu jaoks.
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023174"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a><span data-ttu-id="88268-103">TDS-i kannete sertifikaadinumbrite ja kuupäevade uuendamine</span><span class="sxs-lookup"><span data-stu-id="88268-103">Update certificate numbers and dates for TDS transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88268-104">See teema selgitab, kuidas kasutada tagasisaadava sertide lehte, et kirjendada sertide numbreid ja kuupäevi allika (TDS) sertide jaoks, mis on vastu võetud kindla hankija, kliendi või pearaamatu jaoks.</span><span class="sxs-lookup"><span data-stu-id="88268-104">This topic explains how to update the recoverable certificate numbers and dates that were recorded for vendor, customer, and ledger accounts for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="88268-105">TDS-kannete serte saate vaadata lehel **Taastatavad serdid**.</span><span class="sxs-lookup"><span data-stu-id="88268-105">You can view the certificates for TDS transactions on the **Recoverable certificates** page.</span></span> <span data-ttu-id="88268-106">Saate serte uuendada, kasutades **Sertide värskendamine** lehte.</span><span class="sxs-lookup"><span data-stu-id="88268-106">You can update the certificates by using the **Update Certificates** page.</span></span>

<span data-ttu-id="88268-107">TDS-tehingute sertifikaatide numbrite ja kuupäevade värskendamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="88268-107">Follow these steps to update certificate numbers and dates for TDS transactions.</span></span>

1. <span data-ttu-id="88268-108">Minge **Maks \> Deklaratsioonid \> Kinnipeetav maks \> Värskenda sertifikaat**.</span><span class="sxs-lookup"><span data-stu-id="88268-108">Go to **Tax \> Declarations \> Withholding tax \> Update certificate**.</span></span>

    <span data-ttu-id="88268-109">[![Serdilehe värskendamine](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span><span class="sxs-lookup"><span data-stu-id="88268-109">[![Update certificate page](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span></span>

2. <span data-ttu-id="88268-110">Valige **Serdi värskendamine** lehel **Vali** väljal **Maksu tüüp** **TDS**.</span><span class="sxs-lookup"><span data-stu-id="88268-110">On the **Update certificate** page, in the **Select** section, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="88268-111">Väljal **Sertifikaadi number** valige kliendi või hankija TDS-i serdi number.</span><span class="sxs-lookup"><span data-stu-id="88268-111">In the **Certificate number** field, select the customer's or vendor's TDS certificate number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="88268-112">**Serdi numbri** väli loetleb ainult TDS-i serdinumbreid, mille puhul on ruut **Suletud** tühjendatud **Taastatavad serdid** lehel.</span><span class="sxs-lookup"><span data-stu-id="88268-112">The **Certificate number** field lists only TDS certificate numbers that the **Closed** check box is cleared for on the **Recoverable certificates** page.</span></span>

    <span data-ttu-id="88268-113">Väljal **Serdi kuupäev** näidatakse serdi kuupäev.</span><span class="sxs-lookup"><span data-stu-id="88268-113">The **Certificate date** field shows the certificate date.</span></span> <span data-ttu-id="88268-114">Väljal **Kontotüüp** kuvatakse kontotüüp, mille kohta TDS-serdi number vastu võetakse, ning väljal **Nimi** kuvatakse konto nimi.</span><span class="sxs-lookup"><span data-stu-id="88268-114">The **Account type** field shows the type of account that the TDS certificate number is received for, and the **Name** field shows the name of the account.</span></span>

5. <span data-ttu-id="88268-115">Vahekaardil **Kuupäevast** ja **Kuupäevani** sisestage TDS kannete eelarveperioodi algus- ja lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="88268-115">In the **From date** and **To date** fields, select the start and end dates of the period to show the TDS transactions for.</span></span>
6. <span data-ttu-id="88268-116">Valige **Kuva andmed**, et vaadata valitud perioodi jooksul sisestatud TDS-i kandeid.</span><span class="sxs-lookup"><span data-stu-id="88268-116">Select **Show data** to view the TDS transactions that were posted during the selected period.</span></span>

    <span data-ttu-id="88268-117">Vahekaardi **Ülevaade** ülemisel paanil kuvatakse tabelil järgmine teave iga TDS-kande kohta, mis hankijale või kliendile valitud perioodi jooksul sisestati:</span><span class="sxs-lookup"><span data-stu-id="88268-117">On the **Overview** tab, the grid in the upper pane shows the following information about each TDS transaction that was posted for the vendor or customer during the selected period:</span></span>

    - <span data-ttu-id="88268-118">**Kviitung** - kuvatakse TDS tehingukande kviitungi number.</span><span class="sxs-lookup"><span data-stu-id="88268-118">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="88268-119">**Kuupäev** – TDS kannete kuupäev.</span><span class="sxs-lookup"><span data-stu-id="88268-119">**Date** – The date of the TDS transaction.</span></span>
    - <span data-ttu-id="88268-120">**Summa** - arvele sisestatud summa, mida TDS on arvutanud.</span><span class="sxs-lookup"><span data-stu-id="88268-120">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="88268-121">**Maksusumma** – TDS-i maksusumma, mis kande jaoks arvutatud.</span><span class="sxs-lookup"><span data-stu-id="88268-121">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>

7. <span data-ttu-id="88268-122">Kindlate TDS-kannete teisaldamiseks ülemisest ruudustikust alumisele ruudustikule valige kanded ja seejärel käsk **Kaasa**.</span><span class="sxs-lookup"><span data-stu-id="88268-122">To move specific TDS transactions from the upper grid to the lower grid, select the transactions, and then select **Include**.</span></span> <span data-ttu-id="88268-123">Teise võimalusena valige käsk **Kaasa kõik** et teisaldada kõik TDS-kanded ülemisest ruudustikust alumisele ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="88268-123">Alternatively, select **Include all** to move all TDS transactions from the upper grid to the lower grid.</span></span>

    <span data-ttu-id="88268-124">Kindlate TDS-kannete või kõikide TDS-kannete teisaldamiseks alumisest ruudustikust ülemisse ruudustikku kasutage nuppu **Välista** või **Välista kõik**.</span><span class="sxs-lookup"><span data-stu-id="88268-124">To move specific TDS transactions or all TDS transactions from the lower grid to the upper grid, use the **Exclude** or **Exclude all** button.</span></span>

8. <span data-ttu-id="88268-125">Valige **Värskenda** et värskendada **Serdi numbrit** ja **Serdi kuupäev** väljal TDS-kannete jaoks alumises ruudustikus.</span><span class="sxs-lookup"><span data-stu-id="88268-125">Select **Update** to update the **Certificate number** and **Certificate date** fields for TDS transactions in the lower grid.</span></span>
10. <span data-ttu-id="88268-126">Minge **Maks \> Kaudsed maksud \> Kinnipeetav maks \> Taastatav sert** ja valige **Päring**, et vaadata värskendatud kanderidu, milles on uus serdi number **Serdikannete** lehel.</span><span class="sxs-lookup"><span data-stu-id="88268-126">Go to **Tax \> Indirect taxes \> Withholding tax \> Recoverable certificate**, and select **Inquiry** to view the updated transaction lines that have the new certificate numbers on the **Certificate transactions** page.</span></span>

    <span data-ttu-id="88268-127">[![Serdi kannete leht](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span><span class="sxs-lookup"><span data-stu-id="88268-127">[![Certificate transactions page](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span></span>
