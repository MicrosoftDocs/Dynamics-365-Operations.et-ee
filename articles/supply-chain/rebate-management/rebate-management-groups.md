---
title: Tagasimaksehalduse grupid
description: Selles teemas kirjeldatakse, kuidas seadistada tagasimaksehalduse gruppi. Tagasimaksehalduse gruppe saab kasutada tagasimakse arvutuste ajal ja neid saab siduda koondkirjega.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271073"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="ada68-104">Tagasimakse halduse grupid</span><span class="sxs-lookup"><span data-stu-id="ada68-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ada68-105">Tagasimaksehalduse arvutused võivad olla seotud gruppidega.</span><span class="sxs-lookup"><span data-stu-id="ada68-105">Rebate management calculations can be driven by groups.</span></span> <span data-ttu-id="ada68-106">Tagasimakse haldusgruppe saab luua klientidele, hankijatele ja üksustele.</span><span class="sxs-lookup"><span data-stu-id="ada68-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="ada68-107">Neid saab siduda koondkirjega.</span><span class="sxs-lookup"><span data-stu-id="ada68-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="ada68-108">Tagasimaksehalduse kliendigrupid</span><span class="sxs-lookup"><span data-stu-id="ada68-108">Rebate management customer groups</span></span>

<span data-ttu-id="ada68-109">Arvutused klientide grupi jaoks luuakse sageli ettevõtete ketile, näiteks supermarketite ketile või frantsiisifirmale.</span><span class="sxs-lookup"><span data-stu-id="ada68-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="ada68-110">Seda tüüpi kalkulatsioon on tavaliselt seotud tagasimaksega.</span><span class="sxs-lookup"><span data-stu-id="ada68-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="ada68-111">Mahaarvamist arvutatakse sageli ilma, et arvestatakse, kellele kvalifitseerumistellimus müüdi.</span><span class="sxs-lookup"><span data-stu-id="ada68-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="ada68-112">Siiski on erandeid.</span><span class="sxs-lookup"><span data-stu-id="ada68-112">However, there are exceptions.</span></span> <span data-ttu-id="ada68-113">Näiteks võib litsentsisaaja luua mahaarvamisskeemi, kus kliendigrupp A saab 4 protsenti, kuid kliendigrupp B saab ainult 3 protsenti.</span><span class="sxs-lookup"><span data-stu-id="ada68-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="ada68-114">Saate häälestada kliendigruppe.</span><span class="sxs-lookup"><span data-stu-id="ada68-114">Set up customer groups</span></span>

<span data-ttu-id="ada68-115">Tagasimaksehalduse kliendigruppidega töötamiseks minge **Tagasimaksehaldus \> Tagasimaksehalduse gruppide seadistamine \> Kliendigrupid**.</span><span class="sxs-lookup"><span data-stu-id="ada68-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="ada68-116">Toimingupaani nuppude abil saate gruppe lisada ja eemaldada vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="ada68-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="ada68-117">Määrake igale grupile järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="ada68-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="ada68-118">**Tagasimaksehalduse grupp** – sisestage unikaalne grupi nimi.</span><span class="sxs-lookup"><span data-stu-id="ada68-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="ada68-119">**Kirjeldus** : sisestage grupi kirjeldus, et pakkuda lisateavet selle kohta, kuidas seda tuleks kasutada.</span><span class="sxs-lookup"><span data-stu-id="ada68-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="ada68-120">Kliendigrupi määrangute haldamine</span><span class="sxs-lookup"><span data-stu-id="ada68-120">Manage customer group assignments</span></span>

<span data-ttu-id="ada68-121">Iga klient võib kuuluda mis tahes erinevatesse tagasimakse haldusgruppidesse.</span><span class="sxs-lookup"><span data-stu-id="ada68-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="ada68-122">Grupi liikmete vaatamiseks ja määramiseks saate alustada kas grupi- või kliendiloendist.</span><span class="sxs-lookup"><span data-stu-id="ada68-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="ada68-123">Valitud grupi klientide vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ada68-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="ada68-124">Minge **Tagasimaksehalduse \> Tagasimaksehalduse gruppide seadistamine \> Kliendigrupid**.</span><span class="sxs-lookup"><span data-stu-id="ada68-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="ada68-125">Valige grupp, mida hallata.</span><span class="sxs-lookup"><span data-stu-id="ada68-125">Select the group to manage.</span></span>
1. <span data-ttu-id="ada68-126">Valige toimingupaanil **Kliendid**.</span><span class="sxs-lookup"><span data-stu-id="ada68-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="ada68-127">Kuvatakse leht **Tagasimakse halduse grupid** ja klientide loend, kes on juba valitud grupi liikmed.</span><span class="sxs-lookup"><span data-stu-id="ada68-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="ada68-128">Uue kliendi lisamiseks gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="ada68-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="ada68-129">Seejärel määrake uuel real järgmine väli.</span><span class="sxs-lookup"><span data-stu-id="ada68-129">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="ada68-130">**Kliendikonto** – valige kliendikonto ID.</span><span class="sxs-lookup"><span data-stu-id="ada68-130">**Customer account** – Select the customer account ID.</span></span>

1. <span data-ttu-id="ada68-131">Kliendi eemaldamiseks grupist valige klient ja seejärel valige tegevuspaanil käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="ada68-131">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="ada68-132">Valitud kliendi grupi määratluste vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ada68-132">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="ada68-133">Avage **Müügireskontro \> Kliendid \> Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="ada68-133">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="ada68-134">Valige klient, kellele töötada.</span><span class="sxs-lookup"><span data-stu-id="ada68-134">Select the customer to work with.</span></span>
1. <span data-ttu-id="ada68-135">Valige toimingupaani vahekaardil **Klient** grupis **Tagasimaksehaldus** suvand **Tagasimaksehalduse grupid**.</span><span class="sxs-lookup"><span data-stu-id="ada68-135">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="ada68-136">Kuvatakse leht **Tagasimakse halduse grupid** ja gruppide loend, kuhu valitud klient juba kuulub.</span><span class="sxs-lookup"><span data-stu-id="ada68-136">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="ada68-137">Kliendi lisamiseks uude gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="ada68-137">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="ada68-138">Seejärel määrake uuel real järgmine väli.</span><span class="sxs-lookup"><span data-stu-id="ada68-138">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="ada68-139">**Tagasimaksehalduse grupp** – valige grupp, kellele klient lisada.</span><span class="sxs-lookup"><span data-stu-id="ada68-139">**Rebate management group** – Select the group to add the customer to.</span></span>

1. <span data-ttu-id="ada68-140">Kliendi eemaldamiseks grupist valige grupp ja seejärel valige tegevuspaanil käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="ada68-140">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="ada68-141">Tagasimaksehalduse müüjagrupid</span><span class="sxs-lookup"><span data-stu-id="ada68-141">Rebate management vendor groups</span></span>

<span data-ttu-id="ada68-142">Müüja grupi kalkulatsioon luuakse sageli tarnepunktide grupile.</span><span class="sxs-lookup"><span data-stu-id="ada68-142">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="ada68-143">Seda tüüpi kalkulatsioon on tavaliselt seotud tagasimaksega.</span><span class="sxs-lookup"><span data-stu-id="ada68-143">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="ada68-144">Müüja gruppide häälestus</span><span class="sxs-lookup"><span data-stu-id="ada68-144">Set up vendor groups</span></span>

<span data-ttu-id="ada68-145">Tagasimaksehalduse müüjagruppidega töötamiseks minge **Tagasimaksehaldus \> Tagasimaksehalduse gruppide seadistamine \> Müüjagrupid**.</span><span class="sxs-lookup"><span data-stu-id="ada68-145">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="ada68-146">Toimingupaani nuppude abil saate gruppe lisada ja eemaldada vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="ada68-146">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="ada68-147">Määrake igale grupile järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="ada68-147">For each group, set the following fields:</span></span>

- <span data-ttu-id="ada68-148">**Tagasimaksehalduse grupp** – sisestage unikaalne grupi nimi.</span><span class="sxs-lookup"><span data-stu-id="ada68-148">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="ada68-149">**Kirjeldus** : sisestage grupi kirjeldus, et pakkuda lisateavet selle kohta, kuidas seda tuleks kasutada.</span><span class="sxs-lookup"><span data-stu-id="ada68-149">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="ada68-150">Müüjagrupi määrangute haldamine</span><span class="sxs-lookup"><span data-stu-id="ada68-150">Manage vendor group assignments</span></span>

<span data-ttu-id="ada68-151">Iga müüja võib kuuluda mis tahes erinevatesse tagasimakse haldusgruppidesse.</span><span class="sxs-lookup"><span data-stu-id="ada68-151">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="ada68-152">Grupi liikmete vaatamiseks ja määramiseks saate alustada kas grupi- või müüja loendist.</span><span class="sxs-lookup"><span data-stu-id="ada68-152">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="ada68-153">Valitud grupi müüjate vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ada68-153">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="ada68-154">Minge **Tagasimaksehalduse \> Tagasimaksehalduse gruppide seadistamine \> Müüjagrupid**.</span><span class="sxs-lookup"><span data-stu-id="ada68-154">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="ada68-155">Valige grupp, mida hallata.</span><span class="sxs-lookup"><span data-stu-id="ada68-155">Select the group to manage.</span></span>
1. <span data-ttu-id="ada68-156">Valige toimingupaanil **Müüjad**.</span><span class="sxs-lookup"><span data-stu-id="ada68-156">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="ada68-157">Kuvatakse leht **Tagasimakse halduse grupid** ja müüjate loend, kes on juba valitud grupi liikmed.</span><span class="sxs-lookup"><span data-stu-id="ada68-157">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="ada68-158">Müüja lisamiseks uude gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="ada68-158">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="ada68-159">Seejärel määrake uuel real järgmine väli.</span><span class="sxs-lookup"><span data-stu-id="ada68-159">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="ada68-160">**Müüja konto** – valige müüja konto ID.</span><span class="sxs-lookup"><span data-stu-id="ada68-160">**Vendor account** – Select the vendor account ID.</span></span>

1. <span data-ttu-id="ada68-161">Müüja eemaldamiseks grupist valige müüja ja seejärel valige tegevuspaanil käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="ada68-161">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="ada68-162">Valitud müüja grupi määratluste vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ada68-162">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="ada68-163">Avage **Ostureskonto \> Müüjad \> Kõik müüjad**.</span><span class="sxs-lookup"><span data-stu-id="ada68-163">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="ada68-164">Valige müüja, kellele töötada.</span><span class="sxs-lookup"><span data-stu-id="ada68-164">Select the vendor to work with.</span></span>
1. <span data-ttu-id="ada68-165">Valige toimingupaani vahekaardil **Müüja** grupis **Tagasimaksehaldus** suvand **Tagasimaksehalduse grupid**.</span><span class="sxs-lookup"><span data-stu-id="ada68-165">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="ada68-166">Kuvatakse leht **Tagasimakse halduse grupid** ja gruppide loend, kuhu valitud müüja juba kuulub.</span><span class="sxs-lookup"><span data-stu-id="ada68-166">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="ada68-167">Müüja lisamiseks uude gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="ada68-167">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="ada68-168">Seejärel määrake uuel real järgmine väli.</span><span class="sxs-lookup"><span data-stu-id="ada68-168">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="ada68-169">**Tagasimaksehalduse grupp** – valige grupp, kellele müüja lisada.</span><span class="sxs-lookup"><span data-stu-id="ada68-169">**Rebate management group** – Select the group to add the vendor to.</span></span>

1. <span data-ttu-id="ada68-170">Müüja eemaldamiseks grupist valige grupp ja seejärel valige tegevuspaanil käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="ada68-170">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="ada68-171">Kauba tagasimaksegrupid</span><span class="sxs-lookup"><span data-stu-id="ada68-171">Item rebate groups</span></span>

<span data-ttu-id="ada68-172">Kaupade grupeerimisel on teil tagasimaksete ja mahaarvamiste arvutamisel paindlikkust.</span><span class="sxs-lookup"><span data-stu-id="ada68-172">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="ada68-173">Selline lähenemine on sageli tõhusam viis seadistada klientidele ja hankijatele tagasimaksed ja mahaarvamised.</span><span class="sxs-lookup"><span data-stu-id="ada68-173">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="ada68-174">Saate häälestada kaubagruppe.</span><span class="sxs-lookup"><span data-stu-id="ada68-174">Set up item groups</span></span>

<span data-ttu-id="ada68-175">Tagasimaksehalduse kaubagruppidega töötamiseks minge **Tagasimaksehaldus \> Tagasimaksehalduse gruppide seadistamine \> Kaubagrupid**.</span><span class="sxs-lookup"><span data-stu-id="ada68-175">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="ada68-176">Toimingupaani nuppude abil saate gruppe lisada ja eemaldada vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="ada68-176">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="ada68-177">Määrake igale grupile järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="ada68-177">For each group, set the following fields:</span></span>

- <span data-ttu-id="ada68-178">**Tagasimaksehalduse grupp** – sisestage unikaalne grupi nimi.</span><span class="sxs-lookup"><span data-stu-id="ada68-178">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="ada68-179">**Kirjeldus** : sisestage grupi kirjeldus, et pakkuda lisateavet selle kohta, kuidas seda tuleks kasutada.</span><span class="sxs-lookup"><span data-stu-id="ada68-179">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="ada68-180">Kaubagrupi määrangute haldamine</span><span class="sxs-lookup"><span data-stu-id="ada68-180">Manage item group assignments</span></span>

<span data-ttu-id="ada68-181">Iga üksus võib kuuluda mis tahes erinevatesse tagasimakse haldusgruppidesse.</span><span class="sxs-lookup"><span data-stu-id="ada68-181">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="ada68-182">Grupi liikmete vaatamiseks ja määramiseks saate alustada kas grupi- või kauba loendist.</span><span class="sxs-lookup"><span data-stu-id="ada68-182">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="ada68-183">Saate lisada kaupu ka oma kategooriahierarhia alusel.</span><span class="sxs-lookup"><span data-stu-id="ada68-183">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="ada68-184">Valitud grupi kaupade vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ada68-184">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="ada68-185">Minge **Tagasimaksehalduse \> Tagasimaksehalduse gruppide seadistamine \> Kaubagrupid**.</span><span class="sxs-lookup"><span data-stu-id="ada68-185">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="ada68-186">Valige grupp, mida hallata.</span><span class="sxs-lookup"><span data-stu-id="ada68-186">Select the group to manage.</span></span>
1. <span data-ttu-id="ada68-187">Toimingupaanil valige käsk **Kaubad**.</span><span class="sxs-lookup"><span data-stu-id="ada68-187">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="ada68-188">Kuvatakse leht **Tagasimakse halduse grupid** ja kaupade loend, kes on juba valitud grupi liikmed.</span><span class="sxs-lookup"><span data-stu-id="ada68-188">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="ada68-189">Uue kauba lisamiseks gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="ada68-189">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="ada68-190">Seejärel määrake uuel real järgmine väli.</span><span class="sxs-lookup"><span data-stu-id="ada68-190">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="ada68-191">**Kaubakonto** – valige kaubakonto ID.</span><span class="sxs-lookup"><span data-stu-id="ada68-191">**Item account** – Select the item account ID.</span></span>

1. <span data-ttu-id="ada68-192">Kauba eemaldamiseks grupist valige kauba ja seejärel valige tegevuspaanil käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="ada68-192">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="ada68-193">Valitud kauba grupi määratluste vaatamiseks, lisamiseks või eemaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ada68-193">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="ada68-194">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="ada68-194">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="ada68-195">Valige kaup, millega töötada.</span><span class="sxs-lookup"><span data-stu-id="ada68-195">Select the item to work with.</span></span>
1. <span data-ttu-id="ada68-196">Valige toimingupaani vahekaardil **Toode** grupis **Tagasimaksehaldus** suvand **Tagasimaksehalduse grupid**.</span><span class="sxs-lookup"><span data-stu-id="ada68-196">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="ada68-197">Kuvatakse leht **Tagasimakse halduse grupid** ja gruppide loend, kuhu valitud kaup juba kuulub.</span><span class="sxs-lookup"><span data-stu-id="ada68-197">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="ada68-198">Kauba lisamiseks uude gruppi valige tegevuspaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="ada68-198">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="ada68-199">Seejärel määrake uuel real järgmine väli.</span><span class="sxs-lookup"><span data-stu-id="ada68-199">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="ada68-200">**Tagasimaksehalduse grupp** – valige grupp, kellele kaupa lisada.</span><span class="sxs-lookup"><span data-stu-id="ada68-200">**Rebate management group** – Select the group to add the item to.</span></span>

1. <span data-ttu-id="ada68-201">Kauba eemaldamiseks grupist valige grupp ja seejärel valige tegevuspaanil käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="ada68-201">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="ada68-202">Oma kategooriahierarhial põhinevasse gruppi kaupade lisamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="ada68-202">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="ada68-203">Minge **Tagasimaksehalduse \> Tagasimaksehalduse gruppide seadistamine \> Kaubagrupid**.</span><span class="sxs-lookup"><span data-stu-id="ada68-203">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="ada68-204">Valige grupp, mida hallata.</span><span class="sxs-lookup"><span data-stu-id="ada68-204">Select the group to manage.</span></span>
1. <span data-ttu-id="ada68-205">Toimingupaanil valige käsk **Lisa kaubad**.</span><span class="sxs-lookup"><span data-stu-id="ada68-205">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="ada68-206">Valige dialoogiboksi **Lisa kaubad** väljal **Kategooriahierarhia** ülataseme kategooria.</span><span class="sxs-lookup"><span data-stu-id="ada68-206">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="ada68-207">Kauba hierarhia avatakse vasakul paanil.</span><span class="sxs-lookup"><span data-stu-id="ada68-207">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="ada68-208">Valige otsitav hierarhiatase.</span><span class="sxs-lookup"><span data-stu-id="ada68-208">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="ada68-209">Valitud hierarhia ja hierarhia taseme kaubad on nüüd loetletud parempoolsel paanil.</span><span class="sxs-lookup"><span data-stu-id="ada68-209">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="ada68-210">Paaniga töötamiseks järgige neid samme:</span><span class="sxs-lookup"><span data-stu-id="ada68-210">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="ada68-211">Märkige ruut iga kauba puhul, mille soovite lisada.</span><span class="sxs-lookup"><span data-stu-id="ada68-211">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="ada68-212">Ruudustiku päises kõikide loetletud kaupade valimiseks märkige see ruut.</span><span class="sxs-lookup"><span data-stu-id="ada68-212">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="ada68-213">Ruudustiku filtreerimiseks valige nupp **Kuva valitud**, nii et see näitab ainult seni valitud kaupu.</span><span class="sxs-lookup"><span data-stu-id="ada68-213">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="ada68-214">Täieliku loendi juurde naasmiseks valige nupp uuesti.</span><span class="sxs-lookup"><span data-stu-id="ada68-214">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="ada68-215">Valige **OK**, et rakendada oma kaubavalik valitud grupile.</span><span class="sxs-lookup"><span data-stu-id="ada68-215">Select **OK** to apply your item selection to the selected group.</span></span>
