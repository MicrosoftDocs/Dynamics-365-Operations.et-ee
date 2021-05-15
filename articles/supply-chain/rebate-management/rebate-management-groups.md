---
title: Tagasimaksehalduse grupid
description: Selles teemas kirjeldatakse, kuidas seadistada tagasimaksehalduse gruppi. Tagasimaksehalduse gruppe saab kasutada tagasimakse arvutuste ajal ja neid saab siduda koondkirjega.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: cef7abbbf2a94e26b6b9e66492cd7347d3b4d1f2
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920057"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="08f6a-104">Tagasimaksehalduse grupid</span><span class="sxs-lookup"><span data-stu-id="08f6a-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08f6a-105">Tagasimakse ja mahaarvamise arvutused võivad olla seotud gruppidega.</span><span class="sxs-lookup"><span data-stu-id="08f6a-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="08f6a-106">Tagasimakse haldusgruppe saab luua klientidele, hankijatele ja üksustele.</span><span class="sxs-lookup"><span data-stu-id="08f6a-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="08f6a-107">Neid saab siduda koondkirjega.</span><span class="sxs-lookup"><span data-stu-id="08f6a-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="08f6a-108">Tagasimaksehalduse kliendigrupid</span><span class="sxs-lookup"><span data-stu-id="08f6a-108">Rebate management customer groups</span></span>

<span data-ttu-id="08f6a-109">Arvutused klientide grupi jaoks luuakse sageli ettevõtete ketile, näiteks supermarketite ketile või frantsiisifirmale.</span><span class="sxs-lookup"><span data-stu-id="08f6a-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="08f6a-110">Seda tüüpi kalkulatsioon on tavaliselt seotud tagasimaksega.</span><span class="sxs-lookup"><span data-stu-id="08f6a-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="08f6a-111">Mahaarvamist arvutatakse sageli ilma, et arvestatakse, kellele kvalifitseerumistellimus müüdi.</span><span class="sxs-lookup"><span data-stu-id="08f6a-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="08f6a-112">Siiski on erandeid.</span><span class="sxs-lookup"><span data-stu-id="08f6a-112">However, there are exceptions.</span></span> <span data-ttu-id="08f6a-113">Näiteks võib litsentsisaaja luua mahaarvamisskeemi, kus kliendigrupp A saab 4 protsenti, kuid kliendigrupp B saab ainult 3 protsenti.</span><span class="sxs-lookup"><span data-stu-id="08f6a-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="08f6a-114">Saate häälestada kliendigruppe.</span><span class="sxs-lookup"><span data-stu-id="08f6a-114">Set up customer groups</span></span>

<span data-ttu-id="08f6a-115">Tagasimaksehalduse kliendigruppidega töötamiseks minge **Tagasimaksehaldus \> Tagasimaksehalduse gruppide seadistamine \> Kliendigrupid**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="08f6a-116">Toimingupaani nuppude abil saate gruppe lisada ja eemaldada vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="08f6a-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="08f6a-117">Määrake igale grupile järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="08f6a-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="08f6a-118">**Tagasimaksehalduse grupp** – sisestage unikaalne grupi nimi.</span><span class="sxs-lookup"><span data-stu-id="08f6a-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="08f6a-119">**Kirjeldus** : sisestage grupi kirjeldus, et pakkuda lisateavet selle kohta, kuidas seda tuleks kasutada.</span><span class="sxs-lookup"><span data-stu-id="08f6a-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="08f6a-120">Kliendigrupi määrangute haldamine</span><span class="sxs-lookup"><span data-stu-id="08f6a-120">Manage customer group assignments</span></span>

<span data-ttu-id="08f6a-121">Iga klient võib kuuluda mis tahes erinevatesse tagasimakse haldusgruppidesse.</span><span class="sxs-lookup"><span data-stu-id="08f6a-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="08f6a-122">Grupi liikmete vaatamiseks ja määramiseks saate alustada kas grupi- või kliendiloendist.</span><span class="sxs-lookup"><span data-stu-id="08f6a-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="08f6a-123">Valitud grupi klientide vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="08f6a-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="08f6a-124">Minge **Tagasimaksehalduse \> Tagasimaksehalduse gruppide seadistamine \> Kliendigrupid**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="08f6a-125">Valige grupp, mida hallata.</span><span class="sxs-lookup"><span data-stu-id="08f6a-125">Select the group to manage.</span></span>
1. <span data-ttu-id="08f6a-126">Valige toimingupaanil **Kliendid**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="08f6a-127">Kuvatakse leht **Tagasimakse halduse grupid** ja klientide loend, kes on juba valitud grupi liikmed.</span><span class="sxs-lookup"><span data-stu-id="08f6a-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="08f6a-128">Uue kliendi lisamiseks gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="08f6a-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="08f6a-129">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="08f6a-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="08f6a-130">**Kliendikonto** – valige kliendikonto ID.</span><span class="sxs-lookup"><span data-stu-id="08f6a-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="08f6a-131">**Nimi** – sisestage kliendi nimi ja/või kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="08f6a-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="08f6a-132">Kliendi eemaldamiseks grupist valige klient ja seejärel valige tegevuspaanil käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="08f6a-133">Valitud kliendi grupi määratluste vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="08f6a-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="08f6a-134">Avage **Müügireskontro \> Kliendid \> Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="08f6a-135">Valige klient, kellele töötada.</span><span class="sxs-lookup"><span data-stu-id="08f6a-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="08f6a-136">Valige toimingupaani vahekaardil **Klient** grupis **Tagasimaksehaldus** suvand **Tagasimaksehalduse grupid**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="08f6a-137">Kuvatakse leht **Tagasimakse halduse grupid** ja gruppide loend, kuhu valitud klient juba kuulub.</span><span class="sxs-lookup"><span data-stu-id="08f6a-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="08f6a-138">Kliendi lisamiseks uude gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="08f6a-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="08f6a-139">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="08f6a-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="08f6a-140">**Tagasimaksehalduse grupp** – valige grupp, kellele klient lisada.</span><span class="sxs-lookup"><span data-stu-id="08f6a-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="08f6a-141">**Kirjeldus** – sisestage grupi kirjeldus (nt selgitamaks, miks klient on grupi liige).</span><span class="sxs-lookup"><span data-stu-id="08f6a-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="08f6a-142">Kliendi eemaldamiseks grupist valige grupp ja seejärel valige tegevuspaanil käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="08f6a-143">Tagasimaksehalduse müüjagrupid</span><span class="sxs-lookup"><span data-stu-id="08f6a-143">Rebate management vendor groups</span></span>

<span data-ttu-id="08f6a-144">Müüja grupi kalkulatsioon luuakse sageli tarnepunktide grupile.</span><span class="sxs-lookup"><span data-stu-id="08f6a-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="08f6a-145">Seda tüüpi kalkulatsioon on tavaliselt seotud tagasimaksega.</span><span class="sxs-lookup"><span data-stu-id="08f6a-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="08f6a-146">Müüja gruppide häälestus</span><span class="sxs-lookup"><span data-stu-id="08f6a-146">Set up vendor groups</span></span>

<span data-ttu-id="08f6a-147">Tagasimaksehalduse müüjagruppidega töötamiseks minge **Tagasimaksehaldus \> Tagasimaksehalduse gruppide seadistamine \> Müüjagrupid**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="08f6a-148">Toimingupaani nuppude abil saate gruppe lisada ja eemaldada vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="08f6a-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="08f6a-149">Määrake igale grupile järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="08f6a-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="08f6a-150">**Tagasimaksehalduse grupp** – sisestage unikaalne grupi nimi.</span><span class="sxs-lookup"><span data-stu-id="08f6a-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="08f6a-151">**Kirjeldus** : sisestage grupi kirjeldus, et pakkuda lisateavet selle kohta, kuidas seda tuleks kasutada.</span><span class="sxs-lookup"><span data-stu-id="08f6a-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="08f6a-152">Müüjagrupi määrangute haldamine</span><span class="sxs-lookup"><span data-stu-id="08f6a-152">Manage vendor group assignments</span></span>

<span data-ttu-id="08f6a-153">Iga müüja võib kuuluda mis tahes erinevatesse tagasimakse haldusgruppidesse.</span><span class="sxs-lookup"><span data-stu-id="08f6a-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="08f6a-154">Grupi liikmete vaatamiseks ja määramiseks saate alustada kas grupi- või müüja loendist.</span><span class="sxs-lookup"><span data-stu-id="08f6a-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="08f6a-155">Valitud grupi müüjate vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="08f6a-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="08f6a-156">Minge **Tagasimaksehalduse \> Tagasimaksehalduse gruppide seadistamine \> Müüjagrupid**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="08f6a-157">Valige grupp, mida hallata.</span><span class="sxs-lookup"><span data-stu-id="08f6a-157">Select the group to manage.</span></span>
1. <span data-ttu-id="08f6a-158">Valige toimingupaanil **Müüjad**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="08f6a-159">Kuvatakse leht **Tagasimakse halduse grupid** ja müüjate loend, kes on juba valitud grupi liikmed.</span><span class="sxs-lookup"><span data-stu-id="08f6a-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="08f6a-160">Müüja lisamiseks uude gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="08f6a-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="08f6a-161">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="08f6a-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="08f6a-162">**Müüja konto** – valige müüja konto ID.</span><span class="sxs-lookup"><span data-stu-id="08f6a-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="08f6a-163">**Nimi** – sisestage müüja nimi ja/või kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="08f6a-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="08f6a-164">Müüja eemaldamiseks grupist valige müüja ja seejärel valige tegevuspaanil käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="08f6a-165">Valitud müüja grupi määratluste vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="08f6a-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="08f6a-166">Avage **Ostureskonto \> Müüjad \> Kõik müüjad**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="08f6a-167">Valige müüja, kellele töötada.</span><span class="sxs-lookup"><span data-stu-id="08f6a-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="08f6a-168">Valige toimingupaani vahekaardil **Müüja** grupis **Tagasimaksehaldus** suvand **Tagasimaksehalduse grupid**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="08f6a-169">Kuvatakse leht **Tagasimakse halduse grupid** ja gruppide loend, kuhu valitud müüja juba kuulub.</span><span class="sxs-lookup"><span data-stu-id="08f6a-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="08f6a-170">Müüja lisamiseks uude gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="08f6a-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="08f6a-171">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="08f6a-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="08f6a-172">**Tagasimaksehalduse grupp** – valige grupp, kellele müüja lisada.</span><span class="sxs-lookup"><span data-stu-id="08f6a-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="08f6a-173">**Kirjeldus** – sisestage grupi kirjeldus (nt selgitamaks, miks müüja on grupi liige).</span><span class="sxs-lookup"><span data-stu-id="08f6a-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="08f6a-174">Müüja eemaldamiseks grupist valige grupp ja seejärel valige tegevuspaanil käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="08f6a-175">Kauba tagasimaksegrupid</span><span class="sxs-lookup"><span data-stu-id="08f6a-175">Item rebate groups</span></span>

<span data-ttu-id="08f6a-176">Kaupade grupeerimisel on teil tagasimaksete ja mahaarvamiste arvutamisel paindlikkust.</span><span class="sxs-lookup"><span data-stu-id="08f6a-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="08f6a-177">Selline lähenemine on sageli tõhusam viis seadistada klientidele ja hankijatele tagasimaksed ja mahaarvamised.</span><span class="sxs-lookup"><span data-stu-id="08f6a-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="08f6a-178">Saate häälestada kaubagruppe.</span><span class="sxs-lookup"><span data-stu-id="08f6a-178">Set up item groups</span></span>

<span data-ttu-id="08f6a-179">Tagasimaksehalduse kaubagruppidega töötamiseks minge **Tagasimaksehaldus \> Tagasimaksehalduse gruppide seadistamine \> Kaubagrupid**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="08f6a-180">Toimingupaani nuppude abil saate gruppe lisada ja eemaldada vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="08f6a-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="08f6a-181">Määrake igale grupile järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="08f6a-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="08f6a-182">**Tagasimaksehalduse grupp** – sisestage unikaalne grupi nimi.</span><span class="sxs-lookup"><span data-stu-id="08f6a-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="08f6a-183">**Kirjeldus** : sisestage grupi kirjeldus, et pakkuda lisateavet selle kohta, kuidas seda tuleks kasutada.</span><span class="sxs-lookup"><span data-stu-id="08f6a-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="08f6a-184">Kaubagrupi määrangute haldamine</span><span class="sxs-lookup"><span data-stu-id="08f6a-184">Manage item group assignments</span></span>

<span data-ttu-id="08f6a-185">Iga üksus võib kuuluda mis tahes erinevatesse tagasimakse haldusgruppidesse.</span><span class="sxs-lookup"><span data-stu-id="08f6a-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="08f6a-186">Grupi liikmete vaatamiseks ja määramiseks saate alustada kas grupi- või kauba loendist.</span><span class="sxs-lookup"><span data-stu-id="08f6a-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="08f6a-187">Saate lisada kaupu ka oma kategooriahierarhia alusel.</span><span class="sxs-lookup"><span data-stu-id="08f6a-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="08f6a-188">Valitud grupi kaupade vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="08f6a-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="08f6a-189">Minge **Tagasimaksehalduse \> Tagasimaksehalduse gruppide seadistamine \> Kaubagrupid**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="08f6a-190">Valige grupp, mida hallata.</span><span class="sxs-lookup"><span data-stu-id="08f6a-190">Select the group to manage.</span></span>
1. <span data-ttu-id="08f6a-191">Toimingupaanil valige käsk **Kaubad**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="08f6a-192">Kuvatakse leht **Tagasimakse halduse grupid** ja kaupade loend, kes on juba valitud grupi liikmed.</span><span class="sxs-lookup"><span data-stu-id="08f6a-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="08f6a-193">Uue kauba lisamiseks gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="08f6a-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="08f6a-194">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="08f6a-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="08f6a-195">**Kaubakonto** – valige kaubakonto ID.</span><span class="sxs-lookup"><span data-stu-id="08f6a-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="08f6a-196">**Toote nimi** – sisestage kauba nimi ja/või kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="08f6a-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="08f6a-197">Kauba eemaldamiseks grupist valige kauba ja seejärel valige tegevuspaanil käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="08f6a-198">Valitud kauba grupi määratluste vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="08f6a-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="08f6a-199">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="08f6a-200">Valige kaup, millega töötada.</span><span class="sxs-lookup"><span data-stu-id="08f6a-200">Select the item to work with.</span></span>
1. <span data-ttu-id="08f6a-201">Valige toimingupaani vahekaardil **Toode** grupis **Tagasimaksehaldus** suvand **Tagasimaksehalduse grupid**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="08f6a-202">Kuvatakse leht **Tagasimakse halduse grupid** ja gruppide loend, kuhu valitud kaup juba kuulub.</span><span class="sxs-lookup"><span data-stu-id="08f6a-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="08f6a-203">Kauba lisamiseks uude gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="08f6a-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="08f6a-204">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="08f6a-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="08f6a-205">**Tagasimaksehalduse grupp** – valige grupp, kellele kaupa lisada.</span><span class="sxs-lookup"><span data-stu-id="08f6a-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="08f6a-206">**Kirjeldus** – sisestage grupi kirjeldus (nt selgitamaks, miks kaup on grupi liige).</span><span class="sxs-lookup"><span data-stu-id="08f6a-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="08f6a-207">Kauba eemaldamiseks grupist valige grupp ja seejärel valige tegevuspaanil käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="08f6a-208">Oma kategooriahierarhial põhinevasse gruppi kaupade lisamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="08f6a-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="08f6a-209">Minge **Tagasimaksehalduse \> Tagasimaksehalduse gruppide seadistamine \> Kaubagrupid**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="08f6a-210">Valige grupp, mida hallata.</span><span class="sxs-lookup"><span data-stu-id="08f6a-210">Select the group to manage.</span></span>
1. <span data-ttu-id="08f6a-211">Toimingupaanil valige käsk **Lisa kaubad**.</span><span class="sxs-lookup"><span data-stu-id="08f6a-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="08f6a-212">Valige dialoogiboksi **Lisa kaubad** väljal **Kategooriahierarhia** ülataseme kategooria.</span><span class="sxs-lookup"><span data-stu-id="08f6a-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="08f6a-213">Kauba hierarhia avatakse vasakul paanil.</span><span class="sxs-lookup"><span data-stu-id="08f6a-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="08f6a-214">Valige otsitav hierarhiatase.</span><span class="sxs-lookup"><span data-stu-id="08f6a-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="08f6a-215">Valitud hierarhia ja hierarhia taseme kaubad on nüüd loetletud parempoolsel paanil.</span><span class="sxs-lookup"><span data-stu-id="08f6a-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="08f6a-216">Paaniga töötamiseks järgige neid samme:</span><span class="sxs-lookup"><span data-stu-id="08f6a-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="08f6a-217">Märkige ruut iga kauba puhul, mille soovite lisada.</span><span class="sxs-lookup"><span data-stu-id="08f6a-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="08f6a-218">Ruudustiku päises kõikide loetletud kaupade valimiseks märkige see ruut.</span><span class="sxs-lookup"><span data-stu-id="08f6a-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="08f6a-219">Ruudustiku filtreerimiseks valige nupp **Kuva valitud**, nii et see näitab ainult seni valitud kaupu.</span><span class="sxs-lookup"><span data-stu-id="08f6a-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="08f6a-220">Täieliku loendi juurde naasmiseks valige nupp uuesti.</span><span class="sxs-lookup"><span data-stu-id="08f6a-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="08f6a-221">Valige **OK**, et rakendada oma kaubavalik valitud grupile.</span><span class="sxs-lookup"><span data-stu-id="08f6a-221">Select **OK** to apply your item selection to the selected group.</span></span>
