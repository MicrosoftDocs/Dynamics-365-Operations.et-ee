---
title: Saadetise automaatvärskendused
description: See teema annab ülevaate saadetise automaatvärskenduse funktsioonidest.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e42e7f19311adee7cc48f0ad0b59a4d0d54df9aa
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773539"
---
# <a name="shipment-auto-updates"></a><span data-ttu-id="b9d05-103">Saadetise automaatvärskendused</span><span class="sxs-lookup"><span data-stu-id="b9d05-103">Shipment auto-updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9d05-104">Saadetise automaatvärskenduse funktsioon uuendab automaatselt koormusreal olevaid saadetisega seotud koguseid (nii suurendab kui ka vähendab) pärast koorma vabastamist lattu.</span><span class="sxs-lookup"><span data-stu-id="b9d05-104">The auto-update shipment functionality automatically updates quantities (both increases and decreases) on a load line that is associated with a shipment, after the load has been released to a warehouse.</span></span> <span data-ttu-id="b9d05-105">See funktsioon on sisse lülitatud seni, kuni saadetise või koormuse koormusrida läbib töötlusvoo.</span><span class="sxs-lookup"><span data-stu-id="b9d05-105">This functionality remains turned on until the load line on the shipment or load is processed on a wave.</span></span> <span data-ttu-id="b9d05-106">Selle kasutamisel saavad tellimuse värskendused käsitsi sekkumata lao automaatselt läbida kuni laotöö loomiseni.</span><span class="sxs-lookup"><span data-stu-id="b9d05-106">When it's used, order updates can automatically flow through to the warehouse, without requiring manual intervention, until warehouse work is created.</span></span>

<span data-ttu-id="b9d05-107">Kui saadetise automaatvärskenduse funktsiooni ei kasutata, väheneb automaatselt ainult kogus kuni laotöö loomiseni.</span><span class="sxs-lookup"><span data-stu-id="b9d05-107">When the auto-update shipment functionality isn't used, only quantity decreases automatically flow until warehouse work is created.</span></span> <span data-ttu-id="b9d05-108">Kasutajad peavad ridu käsitsi uuendama või kustutama ning seejärel uuesti vabastama, kui suurendatakse tellimuse koguseid või lisatakse uusi tellimuse ridu.</span><span class="sxs-lookup"><span data-stu-id="b9d05-108">Users must manually update or delete lines, and they must then re-release lines if order quantities are increased or new order lines are added.</span></span> <span data-ttu-id="b9d05-109">Saadetise automaatvärskenduse funktsiooni kasutamisel saavad ettevõtted vaevatult ladu värskendada, muretsemata, et seotud saadetised ja koormused ei vasta tellimusrea uuendustele.</span><span class="sxs-lookup"><span data-stu-id="b9d05-109">By using the auto-update shipment functionality, businesses can seamlessly provide updates to the warehouse without having to worry that related shipments and loads won't reflect order line updates.</span></span>

<span data-ttu-id="b9d05-110">Saadetise automaatvärskenduse funktsioon rakendub nii müügitellimuse kui ka edastamise ridadele ja see on sisse lülitatud kindla lao jaoks.</span><span class="sxs-lookup"><span data-stu-id="b9d05-110">The auto-update shipment functionality applies to both sales order lines and transfer order lines, and it's turned on for a specific warehouse.</span></span> <span data-ttu-id="b9d05-111">Tänu sellele saavad ettevõtted vastavalt vajadusele rakendada ladudes erinevaid saadetise automaatvärskenduse poliitikaid.</span><span class="sxs-lookup"><span data-stu-id="b9d05-111">Therefore, companies can apply different auto-update shipment policies across warehouses, as they require.</span></span> <span data-ttu-id="b9d05-112">Vaikimisi rakendub koguse vähenemise saadetise automaatvärskenduse poliitika kõikidele ladudele, mis kasutavad laohalduse protsesse.</span><span class="sxs-lookup"><span data-stu-id="b9d05-112">By default, the auto-update shipment policy for quantity decreases is applied for all warehouses that use warehouse management processes.</span></span> <span data-ttu-id="b9d05-113">Kui kasutusel on see vaikepoliitika, väheneb automaatselt ainult saadetise ja koormuse kogus kuni laotöö loomiseni.</span><span class="sxs-lookup"><span data-stu-id="b9d05-113">When this default policy setting is used, only quantity decreases automatically flow through to a shipment and load until warehouse work is created.</span></span> <span data-ttu-id="b9d05-114">See sarnaneb käitumisele, mida kasutati enne saadetise automaatvärskenduse funktsiooni kasutuselevõttu.</span><span class="sxs-lookup"><span data-stu-id="b9d05-114">This behavior resembles the behavior that was used before the auto-update shipment functionality was introduced.</span></span>

## <a name="main-elements-of-the-functionality"></a><span data-ttu-id="b9d05-115">Funktsiooni põhielemendid</span><span class="sxs-lookup"><span data-stu-id="b9d05-115">Main elements of the functionality</span></span>

<span data-ttu-id="b9d05-116">Saadetise automaatvärskenduse funktsioon toetub määramisel, kas koormusreal olevat kogust tuleks muuta siis, kui muudatus tehakse müügitellimuse või edastamise real, peamiselt saadetise olekule.</span><span class="sxs-lookup"><span data-stu-id="b9d05-116">The auto-update shipment functionality relies primarily on the shipment status to determine whether the quantity on a load line should be changed when a change is made on a sales order line or transfer order line.</span></span> <span data-ttu-id="b9d05-117">Samuti toetub see määramisel, millal luua automaatselt uus koormusrida olemasolevasse koormusse, peamiselt saadetise olekule.</span><span class="sxs-lookup"><span data-stu-id="b9d05-117">It also relies primarily on the shipment status to determine when a new load line should automatically be added to an existing load.</span></span> <span data-ttu-id="b9d05-118">Kui saadetise olekuks on **Voog moodustatud** või kõrgem, siis automaatset uuendamist ei toimu.</span><span class="sxs-lookup"><span data-stu-id="b9d05-118">When the shipment status is **Waved** or higher, no automatic update occurs.</span></span>

<span data-ttu-id="b9d05-119">Voogude olekut arvestatakse ka automaatvärskenduse puhul.</span><span class="sxs-lookup"><span data-stu-id="b9d05-119">Wave status is also considered for automatic updates.</span></span> <span data-ttu-id="b9d05-120">Kui koormusreaga seotud vool on olekuks **Peatatud**, **Teostamine**, **Vabastatud**, **Komplekteeritud** või **Saadetud** ja kui kasutaja püüab vähendada koormust koormusreal (müügitellimuse või edastamise rea koguse vähenemisega) kuvatakse järgmine tõrketeade: "Reserveeringuid ei saa eemaldada, kuna on loodud töö, mis sõtlub nendest reserveeringutest."</span><span class="sxs-lookup"><span data-stu-id="b9d05-120">When the wave that is related to the load line has a status of **Held**, **Executing**, **Released**, **Picked**, or **Shipped**, if a user tries to reduce the quantity on a load line (via a quantity decrease on the sales order line or transfer order line), the following error message is shown: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span> <span data-ttu-id="b9d05-121">Lisaks, kui vool on üks eelnevalt mainitud voo olekutest, ei suurene koormusrea kogus automaatselt, kui kasutaja püüab müügitellimuse või edastamise rea koguse vähendamisega kaudselt suurendada koormusrea kogust.</span><span class="sxs-lookup"><span data-stu-id="b9d05-121">Additionally, when the wave has one of the previously mentioned wave statuses, if a user tries to indirectly increase the load line quantity by decreasing the quantity on the sales order line or transfer order line, the quantity on the load line isn't automatically increased.</span></span> <span data-ttu-id="b9d05-122">Sel juhul tuleb koormusrida käsitsi uuendada.</span><span class="sxs-lookup"><span data-stu-id="b9d05-122">In this case, the load line must be manually updated.</span></span>

## <a name="scenarios"></a><span data-ttu-id="b9d05-123">Stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="b9d05-123">Scenarios</span></span>

<span data-ttu-id="b9d05-124">Saadetise automaatvärskenduse funktsioon toetab nelja stsenaariumi: uue tellimuserea lisamine, tellimusrea koguse suurendamine, tellimusrea koguse vähendamine ja tellimusrea eemaldamine.</span><span class="sxs-lookup"><span data-stu-id="b9d05-124">The auto-update shipment functionality supports four scenarios: adding a new order line, increasing the quantity on an order line, decreasing the quantity on an order line, and removing an order line.</span></span>

- <span data-ttu-id="b9d05-125">**Uue tellimuserea lisamine** – kui väli **Saadetise automaatvärskendus** kiirkaardil **Ladu** lehel **Laod** (**Laohaldus \> Seadistus \> Ladu \> Laod**) on seatud olekusse **Alati**, ei värskendata olemasolevat koormust, kui tellimuse saadetis on olemas ja müügitellimusele või edastamise tellimusele lisatakse uus tellimusrida pärast müügitellimusele koormuse loomist.</span><span class="sxs-lookup"><span data-stu-id="b9d05-125">**Add a new order line** – When the **Auto update shipment** field on the **Warehouse** FastTab of the **Warehouses** page (**Warehouse management \> Setup \> Warehouse \> Warehouses**) is set to **Always**, if a shipment exists for the order, and a new order line is added to a sales order or transfer order after a load has already been created for the sales order, the existing load isn't updated.</span></span> <span data-ttu-id="b9d05-126">Luuakse uus koormusrida, millel puudub viide olemasoleva koormusega, ja seostatakse olemasoleva saadetisega.</span><span class="sxs-lookup"><span data-stu-id="b9d05-126">A new load line that has no reference to the existing load is created and associated with the existing shipment.</span></span> <span data-ttu-id="b9d05-127">Koormusele lisatakse uus rida ja vabastatakse.</span><span class="sxs-lookup"><span data-stu-id="b9d05-127">The new line is added to the load and released.</span></span>
- <span data-ttu-id="b9d05-128">**Tellimusrea koguse suurendamine** – kui välja **Saadetise automaatvärskendus** väärtuseks on seatud **Alati**, suurendatakse koormusrida tellimusreaga sama koguse võrra, kui tellimuse saadetis on olemas ja olemasoleva müügitellimuse või edastamise rea kogust suurendatakse pärast seda, kui müügitellimusele on koormus juba loodud.</span><span class="sxs-lookup"><span data-stu-id="b9d05-128">**Increase the quantity on an order line** – When the **Auto update shipment** field is set to **Always**, if a shipment exists for the order, and the quantity on an existing sales order line or transfer order line is increased after a load has already been created for the sales order, the load line is increased by the same quantity as the order line.</span></span> <span data-ttu-id="b9d05-129">Kui koormus vabastati, kuid tööd ei loodud, suurendatakse koormusrida tellimusreaga sama koguse võrra.</span><span class="sxs-lookup"><span data-stu-id="b9d05-129">If the load was released, but no work was created, the load line is increased by the same quantity as the order line.</span></span>
- <span data-ttu-id="b9d05-130">**Tellimusrea koguse vähendamine** – kui välja **Saadetise automaatvärskendus** väärtuseks on seatud **Alati** või **Koguse vähendamisel**, uuendatakse seostatud koormusrea kogus võrdväärseks, kui tellimuse saadetis on olemas ja olemasoleva müügitellimuse või edastamise rea kogust vähendatakse pärast seda, kui müügitellimusele on koormus juba loodud, juhul, kui selle koormusrea kogus ei ole juba võrdne või väiksem kui tellimusrea uus kogus.</span><span class="sxs-lookup"><span data-stu-id="b9d05-130">**Decrease the quantity on an order line** – When the **Auto update shipment** field is set to **Always** or **On quantity decrease**, if a shipment exists for the order, and the quantity on an existing sales order line or transfer order line is decreased after a load has already been created for the sales order, the quantity on the associated load line is updated to match, unless the quantity on that load line already equals or is less than the new quantity on the order line.</span></span> <span data-ttu-id="b9d05-131">Sel juhul see ei mõjuta koormusrida.</span><span class="sxs-lookup"><span data-stu-id="b9d05-131">In that case, the load line isn't affected.</span></span> <span data-ttu-id="b9d05-132">Kui koormus vabastati, kuid tööd ei loodud, uuendatakse seostatud koormusrea kogus võrdväärseks, välja arvatud juhul, kui koormusrea kogus on juba võrdne või väiksem kui tellimusrea uus kogus.</span><span class="sxs-lookup"><span data-stu-id="b9d05-132">If the load was released, but no work was created, the quantity on the associated load line is updated to match, unless the quantity on the load line already equals or is less than the new quantity on the order line.</span></span> <span data-ttu-id="b9d05-133">Sel juhul see mõjutab koormusrida.</span><span class="sxs-lookup"><span data-stu-id="b9d05-133">In that case, the load line is affected.</span></span>
- <span data-ttu-id="b9d05-134">**Tellimusrea eemaldamine**– kui välja **Saadetise automaatvärskenduse** väärtuseks on seatud **Alati** või **Koguse vähendamisel**, kuvatakse tõrketeade, kui kasutaja püüab eemaldada tellimusrida, mille koormusrida on juba olemas.</span><span class="sxs-lookup"><span data-stu-id="b9d05-134">**Remove an order line** – When the **Auto update shipment** field is set to **Always** or **On quantity decrease**, if the user tries to remove an order line that a load line exists for, an error message is shown.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="b9d05-135">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="b9d05-135">Example scenario</span></span>

<span data-ttu-id="b9d05-136">Sellisel juhul peavad teil olema installitud demoandmed ja peate kasutama **USMF** demoandmete ettevõtet.</span><span class="sxs-lookup"><span data-stu-id="b9d05-136">For this scenario, you must have demo data installed, and you must use the **USMF** demo data company.</span></span>

### <a name="turn-on-the-auto-update-shipment-functionality"></a><span data-ttu-id="b9d05-137">Saadetise automaatvärskenduse funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="b9d05-137">Turn on the auto-update shipment functionality</span></span>

<span data-ttu-id="b9d05-138">Saadetise automaatvärskenduse funktsiooni sisselülitamine toimub järgmiste toimingute abil.</span><span class="sxs-lookup"><span data-stu-id="b9d05-138">To turn on the auto-update shipment functionality, follow these steps.</span></span>

1. <span data-ttu-id="b9d05-139">Avage **Laohaldus \> Seadistus \> Ladu \> Laod**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-139">Go to **Warehouse management \> Setup \> Warehouse \> Warehouses**.</span></span>
2. <span data-ttu-id="b9d05-140">Valige ladu **24**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-140">Select warehouse **24**.</span></span>
3. <span data-ttu-id="b9d05-141">Muutke kiirkaardil **Ladu** välja **Saadetise automaatvärskendus** väärtus olekust **Koguse vähendamisel** olekusse **Alati**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-141">On the **Warehouse** FastTab, in the **Auto update shipment** field, change the value from **On quantity decrease** to **Always**.</span></span>

<span data-ttu-id="b9d05-142">Väärtuse muutmisel olekusse **Alati**, kajastuvad valitud ladude saadetistes ja koormustes kõik müügitellimuse ja edastamise ridadel tehtavad koguste suurendamised ja vähendamised ning uute ridade lisamised eespool nimetatud kitsenduste põhjal.</span><span class="sxs-lookup"><span data-stu-id="b9d05-142">After you change the value to **Always**, any increases or decreases in the quantities on sales order lines and transfer order lines, and any additions of new lines, are reflected on shipments and loads for the selected warehouse, given the previously mentioned update constraints.</span></span>

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a><span data-ttu-id="b9d05-143">Voomalli muutmine selliselt, et koormusridu ei töödeldaks automaatselt</span><span class="sxs-lookup"><span data-stu-id="b9d05-143">Change the wave template so that load lines aren't automatically processed</span></span>

<span data-ttu-id="b9d05-144">Selleks, et konfigureerida voomalli nii, et see ei töötleks koormusridu automaatselt, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b9d05-144">To configure the wave template so that it doesn't automatically process load lines, follow these steps.</span></span>

1. <span data-ttu-id="b9d05-145">Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-145">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="b9d05-146">Valige voomall **24 Saadetise vaikemall**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-146">Select wave template **24 Shipping default**.</span></span>
3. <span data-ttu-id="b9d05-147">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-147">Select **Edit**.</span></span>
4. <span data-ttu-id="b9d05-148">Muutke kiirkaardil **Üldine** valik **Voo automaatne loomine** olekusse **Jah** ja veenduge, et teised valikud oleksid seatud olekusse **Ei**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-148">On the **General** FastTab, set the **Automate wave creation** option to **Yes**, and make sure that all other options are set to **No**.</span></span>

<span data-ttu-id="b9d05-149">On oluline, et voo loomise protsessi osana ei loodaks ega vabastataks ühtki tööd automaatselt.</span><span class="sxs-lookup"><span data-stu-id="b9d05-149">It's important that no work be automatically created and released as part of the wave creation process.</span></span> <span data-ttu-id="b9d05-150">Pärast müügitellimuse rea jaoks loodud koormusreaga seotud töö loomist ei uuendata koormusrida enam automaatselt, kui müügitellimuse rea kogust muudetakse.</span><span class="sxs-lookup"><span data-stu-id="b9d05-150">After work is created that is related to the load line that was created for the sales order line, the load line is no longer automatically updated if the quantity on the sales order line is changed.</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="b9d05-151">Loo müügitellimus</span><span class="sxs-lookup"><span data-stu-id="b9d05-151">Create a sales order</span></span>

<span data-ttu-id="b9d05-152">Müügitellimuse loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b9d05-152">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="b9d05-153">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="b9d05-154">Valige klient **US-003**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-154">Select customer **US-003**.</span></span>
3. <span data-ttu-id="b9d05-155">Looge rida kauba numbrile **A0001**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-155">Create a line for item number **A0001**.</span></span>
4. <span data-ttu-id="b9d05-156">Sisestage kogus **10**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-156">Enter a quantity of **10**.</span></span> <span data-ttu-id="b9d05-157">(Veenduge, et kasutate ladu **24**.)</span><span class="sxs-lookup"><span data-stu-id="b9d05-157">(Make sure that you're using warehouse **24**.)</span></span>
5. <span data-ttu-id="b9d05-158">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-158">Select **Save**.</span></span>
6. <span data-ttu-id="b9d05-159">Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-159">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span> <span data-ttu-id="b9d05-160">Luuakse saadetis ja voog.</span><span class="sxs-lookup"><span data-stu-id="b9d05-160">A shipment and a wave are created.</span></span>

<span data-ttu-id="b9d05-161">Koormust ja tööd ei looda, sest muutsite eelmises protseduuris voomalli.</span><span class="sxs-lookup"><span data-stu-id="b9d05-161">Because you changed the wave template in the previous procedure, no load or work is created.</span></span> <span data-ttu-id="b9d05-162">Saadetis on olekus **Avatud** ja voog on olekus **Loodud**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-162">The shipment status is **Open**, and the wave status is **Created**.</span></span>

### <a name="decrease-the-quantity-on-a-sales-order-line"></a><span data-ttu-id="b9d05-163">Müügitellimuse rea koguse vähendamine</span><span class="sxs-lookup"><span data-stu-id="b9d05-163">Decrease the quantity on a sales order line</span></span>

<span data-ttu-id="b9d05-164">Müügitellimuse rea koguse vähendamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b9d05-164">To decrease the quantity on a sales order line, follow these steps.</span></span>

1. <span data-ttu-id="b9d05-165">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-165">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="b9d05-166">Valige äsja lattu vabastatud müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="b9d05-166">Select the sales order that you just released to the warehouse.</span></span>
3. <span data-ttu-id="b9d05-167">Valige müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="b9d05-167">Select the sales order line.</span></span> <span data-ttu-id="b9d05-168">Muutke välja **Kogus** väärtus **10** pealt **8** peale.</span><span class="sxs-lookup"><span data-stu-id="b9d05-168">In the **Quantity** field, change the value from **10** to **8**.</span></span>
4. <span data-ttu-id="b9d05-169">Müügitellimuse realt valige **Ladu \> Saadetise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-169">From the sales order line, select **Warehouse \> Shipment details**.</span></span> <span data-ttu-id="b9d05-170">Lehel **Saadetise üksikasjad** kiirkaardil **Koormusread** peegeldab kogus müügitellimuse rea muudatust.</span><span class="sxs-lookup"><span data-stu-id="b9d05-170">On the **Shipment details** page, on the **Load lines** FastTab, the quantity reflects the change on the sales order line.</span></span>

### <a name="increase-the-quantity-on-a-sales-order-line"></a><span data-ttu-id="b9d05-171">Müügitellimuse rea koguse suurendamine</span><span class="sxs-lookup"><span data-stu-id="b9d05-171">Increase the quantity on a sales order line</span></span>

<span data-ttu-id="b9d05-172">Müügitellimuse rea koguse suurendamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b9d05-172">To increase the quantity on a sales order line, follow these steps.</span></span>

1. <span data-ttu-id="b9d05-173">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-173">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="b9d05-174">Valige eelnevalt lattu vabastatud müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="b9d05-174">Select the sales order that you previously released to the warehouse.</span></span>
3. <span data-ttu-id="b9d05-175">Muutke rea kogus **8** pealt **12** peale.</span><span class="sxs-lookup"><span data-stu-id="b9d05-175">Change the line quantity from **8** to **12**.</span></span>
4. <span data-ttu-id="b9d05-176">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-176">Select **Save**.</span></span>
5. <span data-ttu-id="b9d05-177">Minge tagasi lehele **Kõik müügitellimused** ja valige müügitellimus uuesti.</span><span class="sxs-lookup"><span data-stu-id="b9d05-177">Go back to the **All sales orders** page, and select the sales order again.</span></span>
5. <span data-ttu-id="b9d05-178">Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Saadetise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-178">On the Action Pane, on the **Warehouse** tab, in the **Related information** group, select **Shipment details**.</span></span> <span data-ttu-id="b9d05-179">Lehel **Saadetise üksikasjad** kiirkaardil **Koormusread** peegeldab kogus müügitellimuse rea muudatust.</span><span class="sxs-lookup"><span data-stu-id="b9d05-179">On the **Shipment details** page, on the **Load lines** FastTab, the quantity reflects the change on the sales order line.</span></span>

<span data-ttu-id="b9d05-180">Kuigi koormusrea kogus tõusis 8-lt 12-ni, jääb reserveeringusse ainult kaheksa üksust, kui automaatset reserveerimist ei ole sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="b9d05-180">Although the quantity on the load line was increased from 8 to 12, only eight items remain reserved, unless automatic reservation is turned on.</span></span> <span data-ttu-id="b9d05-181">Kui olemasolevale saadetisele lisatud kogust ei reserveerita ja kui praegusel hetkel voogu töödelda ilma reserveeringuta, siis luuakse töö ainult eelnevalt reserveeritud kogusega.</span><span class="sxs-lookup"><span data-stu-id="b9d05-181">Because the quantity that was added to the existing shipment hasn't been reserved, if the wave is processed at this point, without reservation, work is created only for the quantity that has already been reserved.</span></span>

> [!NOTE]
> <span data-ttu-id="b9d05-182">Kui tellimuserea kogust vähendada, ei mõjuta see koormusrea kogust, kui see on juba võrdne või väiksem kui tellimusrea uus kogus.</span><span class="sxs-lookup"><span data-stu-id="b9d05-182">When the quantity on an order line is decreased, the quantity on the load line isn't affected if it already equals or is less than the new quantity on the order line.</span></span> <span data-ttu-id="b9d05-183">Kui tellimusrea kogust suurendada, suurendatakse koormusrea kogust sama koguse võrra kui tellimusrida.</span><span class="sxs-lookup"><span data-stu-id="b9d05-183">When the quantity on an order line is increased, the load line is increased by the same quantity as the order line.</span></span> <span data-ttu-id="b9d05-184">Kui tellimusreal olev kogus erineb koormusrea kogusest, jääb erinevus alles.</span><span class="sxs-lookup"><span data-stu-id="b9d05-184">If the quantity on the order line differs from the quantity on the load line, the difference remains.</span></span>

### <a name="add-a-sales-order-line"></a><span data-ttu-id="b9d05-185">Müügitellimusrea lisamine</span><span class="sxs-lookup"><span data-stu-id="b9d05-185">Add a sales order line</span></span>

<span data-ttu-id="b9d05-186">Müügitellimuse rea lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="b9d05-186">To add a sales order line, follow these steps.</span></span>

1. <span data-ttu-id="b9d05-187">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-187">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="b9d05-188">Valige eelnevalt lattu vabastatud müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="b9d05-188">Select the sales order that you previously released to the warehouse.</span></span>
3. <span data-ttu-id="b9d05-189">Looge rida kauba numbrile **A0002**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-189">Create a line for item number **A0002**.</span></span>
4. <span data-ttu-id="b9d05-190">Sisestage väljale **Kogus** väärtus **10**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-190">In the **Quantity** field, enter **10**.</span></span> <span data-ttu-id="b9d05-191">(Veenduge, et kasutate ladu **24**.) Uus rida lisatakse automaatselt olemasolevale saadetisele.</span><span class="sxs-lookup"><span data-stu-id="b9d05-191">(Make sure that you're using warehouse **24**.) The new line is automatically added to the existing shipment.</span></span>
5. <span data-ttu-id="b9d05-192">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-192">Select **Save**.</span></span>
6. <span data-ttu-id="b9d05-193">Minge tagasi lehele **Kõik müügitellimused** ja valige müügitellimus uuesti.</span><span class="sxs-lookup"><span data-stu-id="b9d05-193">Go back to the **All sales orders** page, and select the sales order again.</span></span>
7. <span data-ttu-id="b9d05-194">Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Saadetise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-194">On the Action Pane, on the **Warehouse** tab, in the **Related information** group, select **Shipment details**.</span></span> <span data-ttu-id="b9d05-195">Lehe **Saadetise üksikasjad** kiirkaardil **Koormusread** vaadake teist koormusrida.</span><span class="sxs-lookup"><span data-stu-id="b9d05-195">On the **Shipment details** page, on the **Load lines** FastTab, notice the second load line.</span></span>

<span data-ttu-id="b9d05-196">Kui olemasolevale saadetisele lisatud kogust ei reserveerita ja kui praegusel hetkel voogu töödelda, luuakse töö ainult esimese müügitellimuse rea ja esimese koormusrea koguse jaoks.</span><span class="sxs-lookup"><span data-stu-id="b9d05-196">Because the sales order line that you just added to the existing shipment hasn't been reserved, if the wave is processed at this point, work is created only for the quantity on the first sales order line and the first load line.</span></span>

### <a name="process-a-wave"></a><span data-ttu-id="b9d05-197">Töötle voogu</span><span class="sxs-lookup"><span data-stu-id="b9d05-197">Process a wave</span></span>

<span data-ttu-id="b9d05-198">Voo töötlemiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b9d05-198">To process the wave, follow these steps.</span></span>

1. <span data-ttu-id="b9d05-199">Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-199">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
2. <span data-ttu-id="b9d05-200">Valige varem loodud voog.</span><span class="sxs-lookup"><span data-stu-id="b9d05-200">Select the wave that you previously created.</span></span>
3. <span data-ttu-id="b9d05-201">Tehke tegumiriba vahekaardil **Voog** grupis **Voog** valik **Töötlus**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-201">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Process**.</span></span>

<span data-ttu-id="b9d05-202">Voog töödeldakse ja luuakse töö koormusrea reserveeritud kogustele.</span><span class="sxs-lookup"><span data-stu-id="b9d05-202">The wave is processed and creates work for the reserved quantities on the load lines.</span></span> <span data-ttu-id="b9d05-203">Saadetise olek värskendatakse olekust **Avatud** olekusse **Voog moodustatud**.</span><span class="sxs-lookup"><span data-stu-id="b9d05-203">The shipment status is updated from **Open** to **Waved**.</span></span> <span data-ttu-id="b9d05-204">Kuna saadetise olek on uuendatud olekusse **Voog moodustatud**, siis kõik toimuvad muudatused, nagu rea koguste vähendamine või suurendamine või müügitellimusele uute ridade lisamine, ei mõjuta see moodustatud vooga saadetise olemasolevaid koormusridu.</span><span class="sxs-lookup"><span data-stu-id="b9d05-204">As the shipment status is updated to **Waved**, any changes that occur, such as decreases or increases in line quantities, or the addition of new lines to the sales order, don't affect the existing load lines that are associated with the waved shipment.</span></span>

<span data-ttu-id="b9d05-205">Kui saadetise olekuks on **Voog moodustatud** või kõrgem, ei kajastu müügitellimuse rea koguse värskendused ega ole valideeritud selle saadetisega seostatud koormusrea suhtes.</span><span class="sxs-lookup"><span data-stu-id="b9d05-205">If a shipment has a status of **Waved** or higher, updates to the quantity on a sales order line aren't reflected on or validated against a load line that is associated with the shipment.</span></span> <span data-ttu-id="b9d05-206">Koormusrea koguse muudatused tuleb teha otse koormusreal.</span><span class="sxs-lookup"><span data-stu-id="b9d05-206">Changes to the quantity on a load line must be made directly on the load line.</span></span>

<span data-ttu-id="b9d05-207">Valideerimine toimub pärast koormusreale töö loomist ja reserveering on tehtud.</span><span class="sxs-lookup"><span data-stu-id="b9d05-207">Validation is done after work has been created for the load line and a reservation has been made.</span></span> <span data-ttu-id="b9d05-208">Müügitellimuse rea koguse vähendamine valideeritakse seejärel töörea reserveeringu suhtes.</span><span class="sxs-lookup"><span data-stu-id="b9d05-208">A decrease in the quantity on the sales order line is then validated against the work line reservation.</span></span>