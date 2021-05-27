---
title: TDS-i arvutamine arvetel töölehtede abil
description: Selles teemas loetletakse töölehtedel allikalt (TDS) maha arvatud maksu arvutamise sammud.
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
ms.openlocfilehash: d68e1b3a4dc31823ec56a525149f16bdc23c0883
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023192"
---
# <a name="calculate-tds-on-invoices-using-journals"></a><span data-ttu-id="20694-103">TDS-i arvutamine arvetel töölehtede abil</span><span class="sxs-lookup"><span data-stu-id="20694-103">Calculate TDS on invoices using journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="20694-104">Selles teemas loetletakse töölehtedel allikalt (TDS) maha arvatud maksu arvutamise sammud.</span><span class="sxs-lookup"><span data-stu-id="20694-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on journals.</span></span>

<span data-ttu-id="20694-105">Alustage lehekülje **Üldised töölehed** avamisega (**Pearaamat > Töölehe sisestused > Üldtöölehed**).</span><span class="sxs-lookup"><span data-stu-id="20694-105">Begin by opening the **General journals** page (**General ledger > Journal entries > General journals**).</span></span>

<span data-ttu-id="20694-106">[![Päevaraamatud](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span><span class="sxs-lookup"><span data-stu-id="20694-106">[![General journals](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)</span></span>

1. <span data-ttu-id="20694-107">Looge tööleheread tabelis loetletud töölehevormide abil.</span><span class="sxs-lookup"><span data-stu-id="20694-107">Create journal lines using the journal forms that are listed in the table.</span></span> <span data-ttu-id="20694-108">Valige konto tüüp ja vastaskonto tüüp ning sisestage kandele summa.</span><span class="sxs-lookup"><span data-stu-id="20694-108">Select the account type and offset account type and enter the amount for the transaction.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="20694-109">Valige **Arve kinnitamise tööleht** lehel suvand **Otsi kandeid** ja valige arved, mille kohta TDS arvutada.</span><span class="sxs-lookup"><span data-stu-id="20694-109">On the **Invoice approval journal** page, select **Find vouchers** and select invoices to calculate TDS on.</span></span> <span data-ttu-id="20694-110">Saate vaadata loodud arveid **Arveregistri** lehel või **Otsi kandeid** lehel.</span><span class="sxs-lookup"><span data-stu-id="20694-110">View the invoices created in the **Invoice register** page or the **Find vouchers** page.</span></span>  

2. <span data-ttu-id="20694-111">Vahekaardil **Üldine** lehel **Töölehe kanded** vaadake või muutke hankijale või kliendile määratud TDS-i vaikegruppi **TDS grupp** väljal.</span><span class="sxs-lookup"><span data-stu-id="20694-111">On the **General** tab of the **Journal voucher** page, view or modify the default TDS group defined for the vendor or customer, in the **TDS group** field.</span></span> <span data-ttu-id="20694-112">Töölehe ridadel arvutatud TDS-i summa põhineb **TDS-i grupi** väljal loetletud TDS-i maksukoodide jaoks määratletud valemil.</span><span class="sxs-lookup"><span data-stu-id="20694-112">The TDS amount that's calculated on journal lines is based on the formula defined for the TDS tax codes listed in the **TDS group** field.</span></span> 

   > [!NOTE]
   > <span data-ttu-id="20694-113">Väli **Kinnipeetava maksu grupp** ja väli **TCS-i grupp** muutuvad kättesaamatuks, kui valite TDS-grupi **TDS-grupp** väljal.</span><span class="sxs-lookup"><span data-stu-id="20694-113">The **Withholding tax group**  field and the **TCS group** field become unavailable when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="20694-114">**Kinnipeetava maksu grupi** väli on saadaval ainult lehel **Üldised töölehed** lehel.</span><span class="sxs-lookup"><span data-stu-id="20694-114">The **Withholding tax group** field is available only on the **General journal** page.</span></span> <span data-ttu-id="20694-115">TDS arvutatakse ainult siis, kui on märgitud **Arvuta kinnipeetav maks** ruut kas **Kõik hankijad** või **Kõik kliendid** lehel.</span><span class="sxs-lookup"><span data-stu-id="20694-115">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** pages.</span></span>   

3. <span data-ttu-id="20694-116">Valige **Maksuteabe** vahekaart. Valige ettevõttele sellel väljal seadistatud alternatiivsed aadressid, kui vaja.</span><span class="sxs-lookup"><span data-stu-id="20694-116">Select the **Tax information** tab. Select the alternate addresses of a company that's set up for the company in this field, if required.</span></span> <span data-ttu-id="20694-117">Ettevõtte nime saate vaadata väljal **Nimi**, mis on **Ettevõtte teave** väljagrupis.</span><span class="sxs-lookup"><span data-stu-id="20694-117">You can view the company name in the **Name** field, which is under the **Company information** field group.</span></span> 

4. <span data-ttu-id="20694-118">Vaadake hankija või kliendi hinnalepete kategooria olemust **Hinna hindamise** väljal, mis on **Kinnipeetava maksu** väljagrupis.</span><span class="sxs-lookup"><span data-stu-id="20694-118">View the nature of assessee category of the vendor or customer in the **Nature of assessee** field, which is under the **Withholding tax** field group.</span></span> <span data-ttu-id="20694-119">Vaadake **Maksukonto number** (**TAN**) väljal kuvatava ettevõtte nime valitud maksude maksukontot.</span><span class="sxs-lookup"><span data-stu-id="20694-119">In the **Tax Account Number** (**TAN**) field, view the TAN of the selected company name that's displayed.</span></span>  

5. <span data-ttu-id="20694-120">Valige **Kinnipeetav maks** menüüst **Kinnipeetav maks** et avada **Ajutised kinnipeetava maksu kanded** leht.</span><span class="sxs-lookup"><span data-stu-id="20694-120">Select **Withholding tax** in **Withholding tax** menu to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="20694-121">Järgmised väljad kuvatakse ülemisel paanil **Ajutise kinnipeetava maksu kannete** lehel.</span><span class="sxs-lookup"><span data-stu-id="20694-121">The following fields are displayed on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="20694-122">**Kinnipeetava maksu summa kokku** - TDS-grupi kande jaoks arvutatud TDS-i kogusumma.</span><span class="sxs-lookup"><span data-stu-id="20694-122">**Withholding tax amount in total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="20694-123">Väljal **Väärtus** - Kuvatakse kande TDS-i arvutamiseks kasutatav koguprotsent.</span><span class="sxs-lookup"><span data-stu-id="20694-123">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="20694-124">Koguprotsent põhineb valemil, mis on määratud TDS-grupiga seotud TDS-i maksukoodide jaoks.</span><span class="sxs-lookup"><span data-stu-id="20694-124">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="20694-125">**Korrigeeritud kinnipeetava maksu summa kokku** - TDS-i grupi kõikide maksukoodide korrigeeritud TDS-i kogusumma.</span><span class="sxs-lookup"><span data-stu-id="20694-125">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="20694-126">**TDS** - Kui see on valitud, lisatakse kandele TDS-grupp.</span><span class="sxs-lookup"><span data-stu-id="20694-126">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

  <span data-ttu-id="20694-127">Välja **Ülevaade**, **Üldine**, ja **Kohandamine** vahekaardil **Kinnipeetava maksu kannete** lehel kuvatakse TDS-summa ja korrigeeritud TDS-i summa TDS-i grupiga seotud TDS-i maksukoodi kohta.</span><span class="sxs-lookup"><span data-stu-id="20694-127">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

6. <span data-ttu-id="20694-128">Valige **Lävend** valimine lehe **Lävendd** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="20694-128">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="20694-129">Vaadake sellel leheküljel konkreetse TDS-i maksukoodiga seotud TDS-i maksukomponendi jaoks määratletud läve limiiti ja erandi läve limiiti.</span><span class="sxs-lookup"><span data-stu-id="20694-129">View the threshold limit and exception threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

   <span data-ttu-id="20694-130">Valige **Valemikoostur** et avada **Valemikoosturi** vorm.</span><span class="sxs-lookup"><span data-stu-id="20694-130">Select **Formula designer** to open the **Formula designer** form.</span></span> <span data-ttu-id="20694-131">Vaadake sellel leheküljel konkreetse TDS-i maksukoodi jaoks määratletud valemit.</span><span class="sxs-lookup"><span data-stu-id="20694-131">View the formula defined for a specific TDS tax code in this page.</span></span> <span data-ttu-id="20694-132">Sulgege **valemikoostur** ja **Ajutise kinnipeetava maksu kannete** lehed et naasta **Töölehe kande** lehele.</span><span class="sxs-lookup"><span data-stu-id="20694-132">Close the **Formula designer** and **Temporary withholding tax transactions** pages to return to the **Journal voucher** page.</span></span>

8. <span data-ttu-id="20694-133">Sisestage kõik vajalikud üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="20694-133">Enter the other required details.</span></span> <span data-ttu-id="20694-134">Kinnitage ja sisestage tööleht.</span><span class="sxs-lookup"><span data-stu-id="20694-134">Validate and post the journal.</span></span> <span data-ttu-id="20694-135">Ostuarvetel arvutatud TDS-i summa sisestatakse tasumisele kuuluvale kontole.</span><span class="sxs-lookup"><span data-stu-id="20694-135">The TDS amount that's calculated on purchase invoices is posted to the payable account.</span></span> <span data-ttu-id="20694-136">Müügiarvetel arvutatud TDS-summa sisestatakse tasumisele kuuluvale kontole, mis on määratud igale TDS-i maksukoodile TDS-grupis.</span><span class="sxs-lookup"><span data-stu-id="20694-136">The TDS amount that's calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="20694-137">TDS-i maksukoodide ostureskontro või müügireskontrod määratletakse **Kinnipeetava maksu koodide** lehel.</span><span class="sxs-lookup"><span data-stu-id="20694-137">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

9. <span data-ttu-id="20694-138">Valige **Sisestatud kinnipeetav maks**, et avada **Kinnipeetava** **maksu** **kannete** leht.</span><span class="sxs-lookup"><span data-stu-id="20694-138">Select **Posted withholding tax** to open the **Withholding** **tax** **transactions** page.</span></span> <span data-ttu-id="20694-139">Väljal **Väärtus** kuvatakse kande TDS-i arvutamiseks kasutatav koguprotsent.</span><span class="sxs-lookup"><span data-stu-id="20694-139">In the **Value** field, the total percentage used to calculate TDS for the transaction is displayed.</span></span>

   <span data-ttu-id="20694-140">Välja **Ülevaade**, **Üldine**, ja **Summa** vahekaardil kinnipeetava maksu kannete lehel kuvatakse TDS-summa ja korrigeeritud TDS-i summa TDS-i grupiga seotud TDS-i maksukoodi kohta.</span><span class="sxs-lookup"><span data-stu-id="20694-140">The fields on the **Overview**, **General**, and **Amount** tabs in the Withholding tax transactions page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>
