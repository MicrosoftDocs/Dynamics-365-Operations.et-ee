---
title: TDS-i maksete tasakaalustamine TDS-i halduri hankijatele ja TDS-i challani loomine
description: See teema kirjeldab, kuidas tasakaalustada allika (TDS) maksetes maha arvatud maksu TDS-i halduri hankijatele.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023185"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a><span data-ttu-id="a4fe0-103">TDS-i maksete tasakaalustamine TDS-i halduri hankijatele ja TDS-i challani loomine</span><span class="sxs-lookup"><span data-stu-id="a4fe0-103">Settle TDS payments to TDS authority vendors and generate TDS challan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4fe0-104">See teema kirjeldab, kuidas tasakaalustada allika (TDS) maksetes maha arvatud maksu TDS-i halduri hankijatele.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-104">This topic explains how to settle Tax Deducted at Source (TDS) payments to TDS authority vendors.</span></span>

1. <span data-ttu-id="a4fe0-105">Avage **Ostureskontro \> Maksed \> Hankija maksete tööleht**.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-105">Go to **Accounts payable \> Payments \> Vendor payment journal**.</span></span>

    <span data-ttu-id="a4fe0-106">[![Hankija maksetööleht](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span><span class="sxs-lookup"><span data-stu-id="a4fe0-106">[![Vendor payment journal page](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span></span>

2. <span data-ttu-id="a4fe0-107">Valige **Hankija makse tööleherea** lehel **Uus** et luua töölehel uus rida.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-107">On the **Vendor payment journal** page, select **New** to create a journal line.</span></span>
3. <span data-ttu-id="a4fe0-108">Valige **Konto** väljal TDS-i asutuse hankija, kellelt TDS-maksed tasakaalustada.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-108">In the **Account** field, select the TDS authority vendor to settle TDS payments to.</span></span>
4. <span data-ttu-id="a4fe0-109">Valige **Tasakaalustuskanded** et avada **Tasakaalustuskanded** leht, kus saate vaadata TDS-i kandeid TDS-i autoriseeritud hankijate jaoks.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-109">Select **Settlement transactions** to open the **Settlement transactions** page, where you can view the settled TDS transactions for the TDS authority vendor.</span></span>

    <span data-ttu-id="a4fe0-110">Tasakaalustusperioodi tasakaalustatud TDS-kanded kuvatakse järgmisel viisil:</span><span class="sxs-lookup"><span data-stu-id="a4fe0-110">The settled TDS transactions for a settlement period are shown in the following way:</span></span>

    - <span data-ttu-id="a4fe0-111">TDS-kanded, mille hinnangukategooria olemus on **Ettevõte** kuvatakse ühe kandereana.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-111">TDS transactions where the nature of assessee category is **Company** are shown as one transaction line.</span></span>
    - <span data-ttu-id="a4fe0-112">TDS-kanded, mille hindamiskategooria olemus on **HUF**, **Firma**, **individduaal**, **AOP**, **BOI**, **Kohalik asutus**, või **Teised** kuvatakse ühe kandereana.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-112">TDS transactions where the nature of assessee category is **HUF**, **Firm**, **Individual**, **AOP**, **BOI**, **Local authority**, or **Others** are shown as one transaction line.</span></span>
    - <span data-ttu-id="a4fe0-113">Väljal **Summa** kuvatakse TDS-i kogusumma, mis tuleb tasuda TDS-i asutuse hankijale.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-113">The **Amount** field shows the total TDS amount that is due to be paid to the TDS authority vendor.</span></span>

5. <span data-ttu-id="a4fe0-114">Valige **Kinnipeetava maksu kanded**, et vaadata erinevaid TDS-i kandeid, mis kaasatakse tasakaalustuskirjesse.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-114">Select **Withholding tax transactions** to view the different TDS transactions that are included for the settlement record.</span></span> <span data-ttu-id="a4fe0-115">Saate vaadata kõigi sellel lehel oleva tasakaalustusperioodi tasakaalustusprotsessi kaasatud TDS-kannete tükeldamist.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-115">You can view the split of each TDS transaction that has been included in the settlement process for the settlement period on this page.</span></span>
6. <span data-ttu-id="a4fe0-116">Märkige **Ülevaade** vahekaardil märkeruut **Märk** TDS-kannete tasakaalustamiseks TDS-i asutuse hankijaga.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-116">On the **Overview** tab, select the **Mark** check box for the TDS transactions to settle to the TDS authority vendor.</span></span>

    <span data-ttu-id="a4fe0-117">Vahekaarddil **Ülevaade** kuvatakse iga avatud TDS-kande kohta järgmine teave:</span><span class="sxs-lookup"><span data-stu-id="a4fe0-117">The **Overview** tab shows the following information for each open TDS transaction:</span></span>

    - <span data-ttu-id="a4fe0-118">**Kuupäev** – lisage kande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-118">**Date** – The TDS transaction date.</span></span>
    - <span data-ttu-id="a4fe0-119">**Kviitung** – Kviitungi number.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-119">**Voucher** – The voucher number.</span></span>
    - <span data-ttu-id="a4fe0-120">**Allikas** – Moodul, kus TDS-kanne loodi.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-120">**Source** – The module that the TDS transaction is posted in.</span></span>
    - <span data-ttu-id="a4fe0-121">**Hankija/klient** – hankija- või kliendikood, millest TDS maha arvatakse.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-121">**Vendor/Customer** – The vendor or customer account number that the TDS is deducted from.</span></span>
    - <span data-ttu-id="a4fe0-122">**Mahaarvatud isiku/osapoole nimi** – selle hankija või kliendi nimi, kellelt TDS maha arvatakse.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-122">**Name of deductee/party** – The name of the vendor or customer that the TDS is deducted from.</span></span>
    - <span data-ttu-id="a4fe0-123">**Hindaja olemus** – selle hinnangukategooria olemus, kuhu mahaarvatav kuulub.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-123">**Nature of assessee** – The nature of assessee category that the deductee belongs to.</span></span>
    - <span data-ttu-id="a4fe0-124">**Summa** - arvele sisestatud summa, mida TDS on arvutanud.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-124">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="a4fe0-125">**Maksusumma** – TDS-i maksusumma, mis kande jaoks arvutatud.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-125">**Tax amount** – The TDS amount that was calculated for the transaction.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4fe0-126">Tühjendage **Märke** ruut kõikide TDS-kannete puhul, mida ei peaks TDS-i asutuse hankijaga tasakaalustama.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-126">Clear the **Mark** check box for any TDS transactions that should not be settled to the TDS authority vendor.</span></span>

    <span data-ttu-id="a4fe0-127">Vahekaardil **Üldine** kuvatakse **PAN** väljal mahaarvatud kauba püsikonto number (PAN).</span><span class="sxs-lookup"><span data-stu-id="a4fe0-127">On the **General** tab, the **PAN** field shows the permanent account number (PAN) of the deductee.</span></span> <span data-ttu-id="a4fe0-128">Väljal **Kuupäev** kuvatakse TDS-i arvutuse kuupäev ja väljal **Väärtus** kuvatakse kogu protsent, mida kasutati TDS-i arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-128">The **Date** field shows the date of the TDS calculation, and the **Value** field shows the total percentage that was used for the TDS calculation.</span></span>

7. <span data-ttu-id="a4fe0-129">Valige **Kanne** et vaaddata TDS-kande kandekirjeid.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-129">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
8. <span data-ttu-id="a4fe0-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-130">Close the page.</span></span>
10. <span data-ttu-id="a4fe0-131">Valige **Kinnipeetava maksu komponendid** et avada **kinnipeetava maksu komponentide** leht, kus saate vaadataTDS-i, mis arvutati konkreetse TDS-i maksukoodi kohta.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-131">Select **Withholding tax components** to open the **Withholding tax components** page, where you can view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>

    <span data-ttu-id="a4fe0-132">Vahekaardil **Ülevaade** näitab **maksukomponendi** väljal TDS-i maksukomponenti, mida kandes kasutati.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-132">On the **Overview** tab, the **Tax component** field shows the TDS tax component that was used for the transaction.</span></span> <span data-ttu-id="a4fe0-133">Väljal **Summa** kuvatakse TDS-i summa, mis arvutati TDS-i maksukomponendi jaoks baasvaluutas.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-133">The **Amount** field shows the TDS amount that was calculated for the TDS tax component, in the base currency.</span></span> <span data-ttu-id="a4fe0-134">Väljal **Akumuleeritud summa** kuvatakse kõigi tasakaalustatud kannete TDS-i maksukomponendi jaoks arvutatud TDS-i kogusumma.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-134">The **Accumulated amount** field shows the total TDS amount that was calculated for the TDS tax component for all settled transactions.</span></span>

    <span data-ttu-id="a4fe0-135">Vahekaardil **Summa** jaotises **Vaikevaluuta** kuvatakse TDS-i maksukomponendi jaoks arvutatud TDS-summa vaikevaluutas.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-135">On the **Amount** tab, the **Default currency** section shows the TDS amount that was calculated for the TDS tax component, in the default currency.</span></span> <span data-ttu-id="a4fe0-136">Jaotises **Paralleelvaluuta** kuvatakse summa paralleelvaluutas.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-136">The **Secondary currency** section shows the amount in the secondary currency.</span></span>

11. <span data-ttu-id="a4fe0-137">Sulgege **Kinnipeetava maksu komponentide** leht.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-137">Close the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="a4fe0-138">**Avatud kande redigeerimise** lehel **Summa** väljal pange tähele, et tasakaalustusperioodiks TDS-i asutuse hankijaga tasakaalustatav kogusumma uuendatakse.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-138">On the **Open transaction editing** page, in the **Amount** field, notice that the total amount to settle to the TDS authority vendor for the settlement period is updated.</span></span>
13. <span data-ttu-id="a4fe0-139">Erinevate TDS-i tasakaalustusperioodide TDS-i tasakaalustuskannete tasakaalustamiseks TDS-i asutuse hankijaga märkige **Märgi** ruut kannete jaoks.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-139">To settle the TDS transactions of different TDS settlement periods to the TDS authority vendor, select the **Mark** check box for the transactions.</span></span>
14. <span data-ttu-id="a4fe0-140">Sulgege **Avatud kannete redigeerimine** leht.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-140">Close the **Open transaction editing** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4fe0-141">Kui kinnipeetava maksu kannete lehel on tasakaalustamiseks valitud vaid mõned kanded, uuendatakse valitud kannete TDS-i kogusumma **Kinnipeetava maksu kanded** **Redigeerimise** lehel **Aavatud kande redigeerimise** lehel.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-141">If only a few transactions are selected for settlement on the **Withholding tax transactions** page, the total TDS amount of the selected transactions is updated in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="a4fe0-142">Parandussumma uuendatakse töölehe real ja avatud **Töölehe kande** lehel ja **Avatud kannete redigeerimine** leht on suletud.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-142">The correction amount is updated on the journal line on the **Journal voucher** page, and the **Open transaction editing** page is closed.</span></span>

    <span data-ttu-id="a4fe0-143">**Töölehe kande** lehel näitab **Deebet** väli TDS-i asutuse hankijale makstavat kogusummat.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-143">On the **Journal voucher** page, the **Debit** field shows the total amount to pay to the TDS authority vendor.</span></span>

15. <span data-ttu-id="a4fe0-144">Sisestage vastaskonto üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-144">Enter the offset account details.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a4fe0-145">Kui TDS-kannetel on erinevad maksukonto numbrid (TAN-id), luuakse tööleheread TAN kohta **töölehe kande** lehel.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-145">If TDS transactions have different Tax Account Numbers (TANs), journal lines are created per TAN on the **Journal voucher** page.</span></span>

16. <span data-ttu-id="a4fe0-146">**Maksetasu** vahekaardil **Tasu ID** väljal valige tasu ID, mille tasu tüüp on **Intress** või **Teised** et nõuda maksetasu hilinenud maksete eest, mis on tehtud TDS-i asutuse hankijale.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-146">On the **Payment fee** tab, in the **Fee ID** field, select a fee ID that has a fee type of **Interest** or **Others** to charge the payment fee for delayed payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="a4fe0-147">Vahekaardi **Maksuteave** jaotises **Ettevõtte teave** väljal kuvatakse **Nimi** väljal ettevõtte nimi.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-147">On the **Tax information** tab, in the **Company information** section, the **Name** field shows the company name.</span></span> <span data-ttu-id="a4fe0-148">Jaotises **Kinnipeetav maks** kuvatakse väljal **Maksukonto number (TAN)** kandereaga seotud kinnipeetava maksu kood.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-148">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the TAN that is attached to the transaction line.</span></span>

17. <span data-ttu-id="a4fe0-149">Kinnitage ja sisestage tööleht.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-149">Validate and post the journal.</span></span>
18. <span data-ttu-id="a4fe0-150">Valige **Kinnipeetav maks \> Challani teave** kande challani üksikasjade sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-150">Select **Withholding tax \> Challan information** to enter the challan details for the transaction.</span></span>

    <span data-ttu-id="a4fe0-151">Väljal **Kviitung** kuvatakse TDS tehingukande kviitungi number.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-151">The **Voucher** field shows the voucher number of the transaction.</span></span>
    
19. <span data-ttu-id="a4fe0-152">Valige **TDS deponeeritud raamatukanne** märkeruut, kui TDS-i summa hoiustatakse raamatukirjet kasutades.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-152">Select the **TDS deposited by book entry** check box if the TDS amount is deposited by using book entry.</span></span>
20. <span data-ttu-id="a4fe0-153">Sisestage **Challani numbri** väljale chalani number, mida kasutatakse makse maksmiseks TDS-i maksu hankijale.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-153">In the **Challan number** field, enter the challan number that is used to make the payment to the TDS authority vendor.</span></span>
21. <span data-ttu-id="a4fe0-154">Väljale **Kuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-154">In the **Date** field, enter the challan date.</span></span>
22. <span data-ttu-id="a4fe0-155">Valige väljal **Panga nimi** panga nimi, mille kohta tuleb TDS-i maksu hankijale makstav TDS-i summa deponeerida.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-155">In the **Bank name** field, select the name of the bank that the TDS amount that is payable to the TDS authority vendor should be deposited to.</span></span> <span data-ttu-id="a4fe0-156">See väli loetleb kõik pangakontod, mis seadistati TDS-i asutuse hankija jaoks väljal **Ostureskontro \> Kõik hankijad \> Seadista \> Pangakontod**.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-156">This field lists all the bank accounts that were set up for the TDS authority vendor at **Accounts payable \> All vendors \> Set up \> Bank accounts**.</span></span>
23. <span data-ttu-id="a4fe0-157">Väljale **BSR-kood** sisestage panga basic Statistical Return (BSR) kood.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-157">In the **BSR code** field, enter the Basic Statistical Return (BSR) code of the bank.</span></span>
24. <span data-ttu-id="a4fe0-158">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-158">Close the page.</span></span>

### <a name="example"></a><span data-ttu-id="a4fe0-159">Näide</span><span class="sxs-lookup"><span data-stu-id="a4fe0-159">Example</span></span>

<span data-ttu-id="a4fe0-160">Periood 04/01/2009 tasakaalustatakse **Rent** TDS-i komponendigrupi jaoks perioodilise TDS-i tasakaalustusprotsessi abil.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-160">The period 04/01/2009 is settled for the **Rent** TDS component group by using the periodic TDS settlement process.</span></span> <span data-ttu-id="a4fe0-161">TDS-i kogusumma 141 625.00 sisestatakse TDS-i tasakaalustusperioodi jooksul TDS-i hankija kontole.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-161">The total TDS amount of 141,625.00 is posted to the TDS vendor authority account for the TDS settlement period.</span></span> <span data-ttu-id="a4fe0-162">Seda summat saate vaadata **Kogusumma** väljal **Avatud kannete redigeerimise** TDS-i asutuse hankija lehel.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-162">You can view this amount in the **Amount** field on the **Open transaction editing** page for the TDS authority vendor.</span></span>

<span data-ttu-id="a4fe0-163">Kui valite **kinnipeetava maksu kanded** et vaadata erinevaid TDS-i kandeid, mis perioodi jooksul tasakaalustati, kuvatakse järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-163">If you select **Withholding tax transactions** to view the different TDS transactions that were settled for the period, the following information is shown.</span></span>

| <span data-ttu-id="a4fe0-164">TDS summa</span><span class="sxs-lookup"><span data-stu-id="a4fe0-164">TDS amount</span></span> |
|------------|
| <span data-ttu-id="a4fe0-165">16,995.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-165">16,995.00</span></span>  |
| <span data-ttu-id="a4fe0-166">22,660.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-166">22,660.00</span></span>  |
| <span data-ttu-id="a4fe0-167">28,325.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-167">28,325.00</span></span>  |
| <span data-ttu-id="a4fe0-168">16,995.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-168">16,995.00</span></span>  |
| <span data-ttu-id="a4fe0-169">28,325.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-169">28,325.00</span></span>  |
| <span data-ttu-id="a4fe0-170">16,995.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-170">16,995.00</span></span>  |
| <span data-ttu-id="a4fe0-171">11,330.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-171">11,330.00</span></span>  |

<span data-ttu-id="a4fe0-172">Valige **Kinnipeetava maksu komponendid** et avada kinnipeetava maksu komponentide leht, kus saate vaadataTDS-i, mis arvutati konkreetse TDS-i maksukoodi kohta.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-172">For a specific TDS amount, you can select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span> <span data-ttu-id="a4fe0-173">Näiteks valite **Kinnipeetava maksu komponentide** TDS-i summa jaoks 16 995.00.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-173">For this example, you select **Withholding tax components** for the TDS amount 16,995.00.</span></span> <span data-ttu-id="a4fe0-174">Kuvatakse kande komponendi kohta arvutatud maksusumma.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-174">The tax amount that was calculated per component for the transaction is shown.</span></span>

| <span data-ttu-id="a4fe0-175">Maksukomponent</span><span class="sxs-lookup"><span data-stu-id="a4fe0-175">Tax component</span></span> | <span data-ttu-id="a4fe0-176">Summa</span><span class="sxs-lookup"><span data-stu-id="a4fe0-176">Amount</span></span>    | <span data-ttu-id="a4fe0-177">Akumuleeritud summa</span><span class="sxs-lookup"><span data-stu-id="a4fe0-177">Accumulated amount</span></span> |
|---------------|-----------|--------------------|
| <span data-ttu-id="a4fe0-178">TDS</span><span class="sxs-lookup"><span data-stu-id="a4fe0-178">TDS</span></span>           | <span data-ttu-id="a4fe0-179">1,5000.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-179">1,5000.00</span></span> | <span data-ttu-id="a4fe0-180">125,000.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-180">125,000.00</span></span>         |
| <span data-ttu-id="a4fe0-181">Lisatasu</span><span class="sxs-lookup"><span data-stu-id="a4fe0-181">Surcharge</span></span>     | <span data-ttu-id="a4fe0-182">1,500.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-182">1,500.00</span></span>  | <span data-ttu-id="a4fe0-183">12,500.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-183">12,500.00</span></span>          |
| <span data-ttu-id="a4fe0-184">PE-Cess</span><span class="sxs-lookup"><span data-stu-id="a4fe0-184">PE-Cess</span></span>       | <span data-ttu-id="a4fe0-185">330.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-185">330.00</span></span>    | <span data-ttu-id="a4fe0-186">2,750.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-186">2,750.00</span></span>           |
| <span data-ttu-id="a4fe0-187">SHE Cess</span><span class="sxs-lookup"><span data-stu-id="a4fe0-187">SHE Cess</span></span>      | <span data-ttu-id="a4fe0-188">165.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-188">165.00</span></span>    | <span data-ttu-id="a4fe0-189">1,375.00</span><span class="sxs-lookup"><span data-stu-id="a4fe0-189">1,375.00</span></span>           |

<span data-ttu-id="a4fe0-190">Kui valisite ainult TDS summa 16 995.00, 22 660.00, ja 2 8325.00 tasakaalustamiseks, kuvatakse **Kinnipeetava maksu kannete lehel** tasakaalustuse kogusumma **67 980.00** lehe **Parandus** väljal **Avatud kande redigeerimise**.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-190">If you selected only the TDS amounts 16,995.00, 22,660.00, and 2,8325.00 for settlement on the **Withholding tax transactions** page, the total amount for settlement is shown as **67,980.00** in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="a4fe0-191">Kui see kanne on tasakaalustamiseks märgitud ja **avatud kannete redigeerimise** leht on suletud, kuvatakse **67 980.00** väljal **Deebet** **Töölehe kande** lehel.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-191">If this transaction is marked for settlement, and the **Open transaction editing** page is closed, the amount **67,980.00** is shown in the **Debit** field on the **Journal voucher** page.</span></span>

<span data-ttu-id="a4fe0-192">Nüüd saate sisestada töölehe ja luua TDS-challani.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-192">You can now post the journal and generate the TDS challan.</span></span>

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a><span data-ttu-id="a4fe0-193">TDS-i asutusele hankijatele tehtud ettemaksete korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="a4fe0-193">Adjustment of advance payments that are made to TDS authority vendors</span></span>

<span data-ttu-id="a4fe0-194">TDS-i asutuse hankijale tegelikuks makseks tehtud ettemakse korrigeerimiseks minge hankijatele **Ostureskonto \> Hankijad \> Kõik hankijad \> Kannete redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-194">To adjust an advance payment that was made to the TDS authority vendor to an actual payment, go to **Accounts payable \> Vendors \> All vendors \> Transactions editing**.</span></span> <span data-ttu-id="a4fe0-195">Kui tegelik makse, mis tehakse, ületab ettemaksu, luuakse kande jaoks kaks challani numbrit.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-195">If the actual payment that is made exceeds the advance payment, two challan numbers are generated for the transaction.</span></span> <span data-ttu-id="a4fe0-196">Kuid TDS-päringus näidatakse ainult esimest chalani numbrit.</span><span class="sxs-lookup"><span data-stu-id="a4fe0-196">However, only the first challan number is shown in the TDS inquiry.</span></span>
