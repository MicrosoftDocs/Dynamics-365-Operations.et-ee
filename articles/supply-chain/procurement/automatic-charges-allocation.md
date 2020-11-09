---
title: Tasude automaatne eraldamine
description: Microsoft Dynamics 365 Supply Chain Managementi tasude funktsiooni abil saate automaatselt eraldada tasusid ostutellimustele või müügitellimustele.
author: dasani-madipalli
manager: tfehr
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 818affc7591577b69309928eb9b0e71130884cec
ms.sourcegitcommit: 3feccc9facb33e3dee18f04e202f7b20785df0a8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998872"
---
# <a name="automatic-allocation-of-charges"></a><span data-ttu-id="fd5d3-103">Tasude automaatne eraldamine</span><span class="sxs-lookup"><span data-stu-id="fd5d3-103">Automatic allocation of charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd5d3-104">Sõltuvalt kliendist, kellega töötate, või müüdavast kaubast, võite soovida rakendada kindlaid lisatasusid.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-104">Based on the customer that you're working with or the item that you're selling, you might want to apply specific additional charges.</span></span> <span data-ttu-id="fd5d3-105">Microsoft Dynamics 365 Supply Chain Managementi *tasude* funktsiooni abil saate automaatselt eraldada tasusid ostutellimustele või müügitellimustele.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-105">The *charges* feature in Microsoft Dynamics 365 Supply Chain Management helps you automatically allocate charges to purchase orders or sales orders.</span></span>

<span data-ttu-id="fd5d3-106">Automaatsed tasud või autom. tasud, rakendatakse automaatselt, kui loote müügitellimuse või ostutellimuse.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-106">Automatic charges, or auto charges, are automatically applied when you create a sales order or a purchase order.</span></span> <span data-ttu-id="fd5d3-107">Automaatsed tasud saate määratleda kindlate hankijate, klientide hankija- või kaubagruppide kohta.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-107">You can define auto charges for specific vendors, customers, groups of vendors, or items.</span></span> <span data-ttu-id="fd5d3-108">Saate määratleda ka automaatsed tasud, mis kehtivad kõigi hankijate, klientide või kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-108">You can also define auto charges that apply to all vendors, customers, or items.</span></span>

## <a name="set-up-charges-codes"></a><span data-ttu-id="fd5d3-109">Tasukoodide häälestus</span><span class="sxs-lookup"><span data-stu-id="fd5d3-109">Set up charges codes</span></span>

<span data-ttu-id="fd5d3-110">Tasude eraldamiseks peate esmalt määratlema tasukoodid.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-110">To allocate charges, you must first define charges codes.</span></span>

1. <span data-ttu-id="fd5d3-111">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-111">Follow one of these steps:</span></span>

    - <span data-ttu-id="fd5d3-112">Ostutellimuste puhul avage **Ostureskontro \> Tasude seadistamine \> Tasukood**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-112">For purchase orders: Go to **Accounts payable \> Charges setup \> Charges code**.</span></span>
    - <span data-ttu-id="fd5d3-113">Müügitellimuste puhul avage **Müügireskontro \> Tasude seadistamine \> Tasukood**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-113">For sales orders: Go to **Accounts receivable \> Charges setup \> Charges code**.</span></span>

1. <span data-ttu-id="fd5d3-114">Tasukoodi loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-114">On the Action Pane, select **New** to create a charges code.</span></span>
1. <span data-ttu-id="fd5d3-115">Määrake uue kirje päises järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-115">In the header of the new record, set the following fields:</span></span>

    - <span data-ttu-id="fd5d3-116">**Tasukood** – sisestage tasukood.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-116">**Charges code** – Enter a code for the charges.</span></span>
    - <span data-ttu-id="fd5d3-117">**Kirjeldus** – sisestage tasude kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-117">**Description** – Enter a description of the charges.</span></span>
    - <span data-ttu-id="fd5d3-118">**Kauba käibemaksugrupp** – valige kauba käibemaksugrupp (kui see on olemas).</span><span class="sxs-lookup"><span data-stu-id="fd5d3-118">**Item sales tax group** – Select an item sales tax group, if applicable.</span></span>
    - <span data-ttu-id="fd5d3-119">**Proportsionaalne jaotumine** – määrake suvandi väärtuseks *Jah* , kui soovite tasusid proportsionaalselt jaotada.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-119">**Prorate** – Set this option to *Yes* if you want to prorate your charges.</span></span> <span data-ttu-id="fd5d3-120">See suvand on saadaval ainult müügitellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-120">This option is available only for sales orders.</span></span>
    - <span data-ttu-id="fd5d3-121">**Maksimaalne summa** – sisestage maksimaalne summa, mis selle tasukoodi puhul lubatud on.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-121">**Maximum amount** – Enter the maximum amount that is allowed for the charges code.</span></span> <span data-ttu-id="fd5d3-122">Seda välja kasutatakse hankija arvete tasude kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-122">This field is used to validate charges for vendor invoices.</span></span> <span data-ttu-id="fd5d3-123">See on saadaval ainult ostutellimustele.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-123">It's available only for purchase orders.</span></span>

        > [!NOTE]
        > <span data-ttu-id="fd5d3-124">Ostutellimuste tasude kinnitamise funktsiooni sisselülitamiseks avage **Ostureskontro \> Seadistus \> Ostureskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-124">To turn on the functionality for validating charges for purchase orders, go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span> <span data-ttu-id="fd5d3-125">Määrake kiirkaardi **Arve kinnitamine** jaotises **Arve kinnitamine** suvandi **Luba arvete võrdlemise kinnitamine** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-125">On the **Invoice validation** FastTab, in the **Invoice validation** section, set the **Enable invoice matching validation** option to *Yes*.</span></span>

1. <span data-ttu-id="fd5d3-126">Kiirkaart **Sisestamine** sisaldab jaotiseid **Deebet** ja **Krediit**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-126">The **Posting** FastTab includes **Debit** and **Credit** sections.</span></span> <span data-ttu-id="fd5d3-127">Määrake järgmised väljad, sõltuvalt pearaamatust, kuhu soovite tasud sisestada.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-127">Set the following fields, depending on the ledger that you want to post the charges to:</span></span>

    - <span data-ttu-id="fd5d3-128">**Tüüp** – valige konto tüüp, kuhu sisestate ( *Pearaamat* , *Klient* või *Kaup* ).</span><span class="sxs-lookup"><span data-stu-id="fd5d3-128">**Type** – Select the type of account that you're posting to ( *Ledger* , *Customer* , or *Item* ).</span></span>
    - <span data-ttu-id="fd5d3-129">**Sisestamine** – valige loodavate sisestuste tüüp (nt *Peatöövõtja tasu* või *Kliendi tasakaalustamine* ).</span><span class="sxs-lookup"><span data-stu-id="fd5d3-129">**Posting** – Select the type of postings to create (such as *Broker fee* or *Customer settlement* ).</span></span>
    - <span data-ttu-id="fd5d3-130">**Konto** – valige konto, mille eest tasu sisestate.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-130">**Account** – Select the account to post the charge for.</span></span>

1. <span data-ttu-id="fd5d3-131">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-charge-groups"></a><span data-ttu-id="fd5d3-132">Tasugruppide loomine</span><span class="sxs-lookup"><span data-stu-id="fd5d3-132">Create charge groups</span></span>

<span data-ttu-id="fd5d3-133">Tasugrupid eraldavad kindlaid klientide või hankijate grupi tasusid automaatselt.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-133">Charge groups automatically allocate specific charges to a group of customers or vendors.</span></span> <span data-ttu-id="fd5d3-134">Järgmised alamjaotised kirjeldavad, kuidas luua ja määrata neid tasugruppe.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-134">The following subsections describe how to create and assign these charge groups.</span></span>

### <a name="charge-groups-for-purchase-orders"></a><span data-ttu-id="fd5d3-135">Ostutellimuste tasugrupid</span><span class="sxs-lookup"><span data-stu-id="fd5d3-135">Charge groups for purchase orders</span></span>

<span data-ttu-id="fd5d3-136">Ostutellimuste jaoks tasugruppide loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-136">To create charge groups for purchase orders, follow these steps.</span></span>

1. <span data-ttu-id="fd5d3-137">Avage **Ostureskontro \> Tasude seadistus \> Hankija tasugrupp**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-137">Go to **Accounts payable \> Charges setup \> Vendor charges group**.</span></span>
1. <span data-ttu-id="fd5d3-138">Valige toimingupaanil **Uus** , et lisada rida jaotise ruudustikku ja seejärel määrake järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-138">On the Action Pane, select **New** to add a row to the grid, and then set the following fields:</span></span>

    - <span data-ttu-id="fd5d3-139">**Tasugrupp** – sisestage tasugrupi nimi.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-139">**Charges group** – Enter the name of the charge group.</span></span>
    - <span data-ttu-id="fd5d3-140">**Kirjeldus** – sisestage tasugrupi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-140">**Description** – Enter a description of the charge group.</span></span>

1. <span data-ttu-id="fd5d3-141">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-141">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="fd5d3-142">Avage **Ostureskontro \> Hankijad \> Kõik hankijad** ja avage olemasolev hankija või looge uus hankija.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-142">Go to **Accounts payable \> Vendors \> All vendors** , and either open an existing vendor or create a new vendor.</span></span>
1. <span data-ttu-id="fd5d3-143">Määrake kiirkaardi **Ostutellimuse vaikeväärtused** jaotise **Ostutellimus** väljale **Tasugrupp** äsja loodud tasugrupp.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-143">On the **Purchase order defaults** FastTab, in the **Purchase order** section, set the **Charges group** field to the charge group that you just created.</span></span>

### <a name="charge-groups-for-sales-orders"></a><span data-ttu-id="fd5d3-144">Müügitellimuste tasugrupid</span><span class="sxs-lookup"><span data-stu-id="fd5d3-144">Charge groups for sales orders</span></span>

<span data-ttu-id="fd5d3-145">Müügitellimuste jaoks tasugruppide loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-145">To create charge groups for sales orders, follow these steps.</span></span>

1. <span data-ttu-id="fd5d3-146">Minge jaotisse **Müügireskontro \> Tasude seadistus \> Kliendi tasugrupid**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-146">Go to **Accounts receivable \> Charges setup \> Customer charge groups**.</span></span>
1. <span data-ttu-id="fd5d3-147">Valige toimingupaanil **Uus** , et lisada rida jaotise ruudustikku ja seejärel määrake järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-147">On the Action Pane, select **New** to add a row to the grid, and then set the following fields:</span></span>

    - <span data-ttu-id="fd5d3-148">**Tasugrupp** – sisestage tasugrupi nimi.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-148">**Charges group** – Enter the name of the charge group.</span></span>
    - <span data-ttu-id="fd5d3-149">**Kirjeldus** – sisestage tasugrupi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-149">**Description** – Enter a description of the charge group.</span></span>

1. <span data-ttu-id="fd5d3-150">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-150">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="fd5d3-151">Avage **Müügireskontro \> Kliendid \> Kõik kliendid** ja avage olemasolev klient või looge uus klient.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-151">Go to **Accounts receivable \> Customers \> All customers** , and either open an existing customer or create a new customer.</span></span>
1. <span data-ttu-id="fd5d3-152">Määrake kiirkaardi **Ostutellimuse vaikeväärtused** jaotise **Müügitellimus** väljale **Tasugrupp** äsja loodud tasugrupp.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-152">On the **Purchase order defaults** FastTab, in the **Sales order** section, set the **Charges group** field to the charge group that you just created.</span></span>

## <a name="define-auto-charges"></a><span data-ttu-id="fd5d3-153">Automaatsete tasude määratlemine</span><span class="sxs-lookup"><span data-stu-id="fd5d3-153">Define auto charges</span></span>

<span data-ttu-id="fd5d3-154">Pärast tasukoodide seadistamist tehke automaatsete tasude määratlemiseks järgmist.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-154">After your charges codes are set up, follow these steps to define the auto charges.</span></span>

1. <span data-ttu-id="fd5d3-155">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-155">Follow one of these steps:</span></span>

    - <span data-ttu-id="fd5d3-156">Ostutellimuste puhul avage **Hanked \> Seadistus \> Tasud \> Automaatsed tasud**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-156">For purchase orders: Go to **Procurement and sourcing \> Setup \> Charges \> Automatic charges**.</span></span>
    - <span data-ttu-id="fd5d3-157">Müügitellimuste puhul avage **Müügireskontro \> Seadistus \> Tasude seadistamine \> Automaatsed tasud**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-157">For sales orders: Go to **Accounts receivable \> Setup \> Charges setup \> Auto charges**.</span></span>

1. <span data-ttu-id="fd5d3-158">Valige loendipaani väljal **Tase** tase, mille puhul rakendub teie automaatne tasu.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-158">In the list pane, in the **Level** field, select the level where your auto charge applies:</span></span>

    - <span data-ttu-id="fd5d3-159">*Peamine* – tasud rakendatakse tellimuse päisele.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-159">*Main* – Apply charges to the order header.</span></span>
    - <span data-ttu-id="fd5d3-160">*Rida* – tasud rakendatakse tellimuse ridadele.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-160">*Line* – Apply charges to the order lines.</span></span>

1. <span data-ttu-id="fd5d3-161">Valige olemasolev automaatne tasu selle redigeerimiseks või valige **Uus** uue automaatse tasu määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-161">Select an existing auto charge to edit it, or select **New** to define a new auto charge.</span></span>
1. <span data-ttu-id="fd5d3-162">Valige loendist **Konto kood** üks järgmistest väärtustest, et määrata mõjutatud kontode ulatus.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-162">In the **Account code** list, select one of the following values to specify the scope of accounts that will be affected:</span></span>

    - <span data-ttu-id="fd5d3-163">*Tabel* – tasud määratakse kindlale kliendile või hankijale.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-163">*Table* – Assign charges to a specific customer or vendor.</span></span>
    - <span data-ttu-id="fd5d3-164">*Grupp* – tasud määratakse lisatasude grupile.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-164">*Group* – Assign charges to a miscellaneous charges group.</span></span>
    - <span data-ttu-id="fd5d3-165">*Kõik* – tasud määratakse kõigile klientidele või hankijatele.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-165">*All* – Assign charges to all customers or vendors.</span></span>

1. <span data-ttu-id="fd5d3-166">Valige väljal **Kliendi seos** või **Hankija seos** kindel klient või hankija, kui tegite väljal **Konto kood** valiku *Tabel*.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-166">In the **Customer relation** or **Vendor relation** field, select a specific customer or vendor if you set the **Account code** field to *Table*.</span></span> <span data-ttu-id="fd5d3-167">Kui tegite väljal **Konto kood** valiku *Grupp* , valige kliendi või hankija tasugrupp.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-167">If you set the **Account code** field to *Group* , select a customer or vendor charges group.</span></span>
1. <span data-ttu-id="fd5d3-168">Valige väljal **Kauba kood** üks järgmistest väärtustest, et määrata mõjutatud kaupade ulatus.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-168">In the **Item code** field, select one of the following values to specify the scope of items that will be affected.</span></span> <span data-ttu-id="fd5d3-169">Kauba koodi saate valida ainult siis, kui määratlete automaatsed tasud reatasemel.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-169">You can select an item code only when you define auto charges at the line level.</span></span>

    - <span data-ttu-id="fd5d3-170">*Tabel* – tasud määratakse kindlale kaubale.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-170">*Table* – Assign charges to a specific item.</span></span>
    - <span data-ttu-id="fd5d3-171">*Grupp* – tasud määratakse kauba tasugrupile.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-171">*Group* – Assign charges to an item charges group.</span></span>
    - <span data-ttu-id="fd5d3-172">*Kõik* – tasud määratakse kõigile kaupadele.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-172">*All* – Assign charges to all items.</span></span>

1. <span data-ttu-id="fd5d3-173">Valige väljal **Kauba seos** kindel kaup, kui tegite väljal **Kauba kood** valiku *Tabel*.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-173">In the **Item relation** field, select a specific item if you set the **Item code** field to *Table*.</span></span> <span data-ttu-id="fd5d3-174">Kui tegite väljal **Kauba kood** valiku *Grupp* , valige kauba tasugrupp.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-174">If you set the **Item code** field to *Group* , select an item charges group.</span></span>
1. <span data-ttu-id="fd5d3-175">**Ainult müügitellimuste puhul:** valige väljal **Tarneviisi kood** üks järgmistest väärtustest, et määrata tarneviiside ulatus, mis on mõjutatud.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-175">**For sales orders only:** In the **Mode of delivery code** field, select one of the following values to specify the scope of delivery modes that will be affected:</span></span>

    - <span data-ttu-id="fd5d3-176">*Tabel* – tasud määratakse konkreetsele tarneviisile.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-176">*Table* – Assign charges to a specific mode of delivery.</span></span>
    - <span data-ttu-id="fd5d3-177">*Grupp* – tasud määratakse konkreetsele tarnegrupile.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-177">*Group* – Assign charges to a mode of delivery group.</span></span>
    - <span data-ttu-id="fd5d3-178">*Kõik* – tasud määratakse kõigile tarneviisidele.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-178">*All* – Assign charges to all modes of delivery.</span></span>

1. <span data-ttu-id="fd5d3-179">**Ainult müügitellimuste puhul** valige väljal **Tarneviisi seos** kindel tarneviis, kui tegite väljal **Tarneviisi kood** valiku *Tabel*.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-179">**For sales orders only:** In the **Mode of delivery relation** field, select a specific mode of delivery if you set the **Mode of delivery code** field to *Table*.</span></span> <span data-ttu-id="fd5d3-180">Kui tegite väljal **Tarneviisi kood** valiku *Grupp* , valige tarneviisi grupp.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-180">If you set the **Mode of delivery code** field to *Group* , select a mode of delivery group.</span></span>
1. <span data-ttu-id="fd5d3-181">Määratlege kiirkaardil **Read** tasud ja tasumäärad, mida kasutatakse praeguse automaatse tasu rakendamisel.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-181">On the **Lines** FastTab, define the charges and the charges rates that will be used when the current auto charge is applied.</span></span> <span data-ttu-id="fd5d3-182">Saate kasutada selle kiirkaardi tööriistariba nii paljude ridade lisamiseks, kui vajate.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-182">You can use the toolbar on this FastTab to add as many lines as you require.</span></span> <span data-ttu-id="fd5d3-183">Määrake igale reale järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-183">For each line, set the following fields:</span></span>

    - <span data-ttu-id="fd5d3-184">**Valuuta** – valige valuuta, mida tuleks kasutada tasu arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-184">**Currency** – Select the currency that should be used to calculate the charge.</span></span>
    - <span data-ttu-id="fd5d3-185">**Tasukood** – valige tasukood.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-185">**Charges code** – Select the code for the charge.</span></span>
    - <span data-ttu-id="fd5d3-186">**Kategooria** – valige üks järgmistest väärtustest.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-186">**Category** – Select one of the following values:</span></span>

        - <span data-ttu-id="fd5d3-187">*Fikseeritud* – tasu sisestatakse reale fikseeritud summana.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-187">*Fixed* – The charge is entered as a fixed amount on the line.</span></span> <span data-ttu-id="fd5d3-188">Fikseeritud tasusid saab kasutada tellimuse päises ja tellimuse ridadel olevate tasude puhul.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-188">Fixed charges can be used on charges both in the order header and on the order lines.</span></span>
        - <span data-ttu-id="fd5d3-189">*Tk* – tasu põhineb ühikul.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-189">*Pcs* – The charge is based on the unit.</span></span> <span data-ttu-id="fd5d3-190">Neid tasusid saab kasutada ainult tellimuse ridadel.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-190">These charges can be used only on order lines.</span></span> <span data-ttu-id="fd5d3-191">Need kuvatakse tellimuse kogusumma arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-191">They will appear when you calculate the order total.</span></span>
        - <span data-ttu-id="fd5d3-192">*Protsent* – tasu sisestatakse reale protsendina.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-192">*Percent* – The charge is entered as a percentage on the line.</span></span> <span data-ttu-id="fd5d3-193">Tasude protsente saab kasutada tellimuse päises ja tellimuse ridadel olevate tasude puhul.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-193">Percentage charges can be used on charges both in the order header and on the order lines.</span></span>
        - <span data-ttu-id="fd5d3-194">*Kontsernisisene protsent* – tasu sisestatakse kontsernisiseste tellimuste real protsendina.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-194">*Intercompany percent* – The charge is entered as a percentage on the line for intercompany orders.</span></span> <span data-ttu-id="fd5d3-195">Kontsernisisest protsenti saab kasutada ainult tellimuse ridadel.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-195">Intercompany percentage charges can be used only on order lines.</span></span>
        - <span data-ttu-id="fd5d3-196">*Väline* – tasu arvutatakse muu osapoole teenuse alusel, mis on seotud ühe või mitme kättetoimetajaga.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-196">*External* – The charge is calculated by a third-party service that is associated with one or more shipping carriers.</span></span>

    - <span data-ttu-id="fd5d3-197">**Tasu väärtus** – sisestage tasu väärtus, mis põhineb teie valitud kategoorial.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-197">**Charges value** – Enter the charge value, based on the category that you selected.</span></span>
    - <span data-ttu-id="fd5d3-198">**Tasu valuutakood** – määrake tasule valuuta, kui soovite kasutada väljal **Valuuta** määratletud valuutast erinevat valuutat.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-198">**Charges currency code** – Specify a currency for the charge if you want to use a currency other than the currency that you specified in the **Currency** field.</span></span> <span data-ttu-id="fd5d3-199">Saate kasutada teist valuutat juhul, kui valitud tasukoodile on väljal **Deebeti tüüp** või **Krediidi tüüp** määratud *Pearaamatukonto* või *Kaup*.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-199">You can use a different currency only if the **Debit type** or **Credit type** field is set to either *Ledger account* or *Item* for the selected charges code.</span></span>
    - <span data-ttu-id="fd5d3-200">**Alates summast** – määrake algsumma, millele automaatne tasu rakendada.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-200">**From amount** – Specify a starting amount to apply the auto charge to.</span></span> <span data-ttu-id="fd5d3-201">Summa tähendab selles kontekstis tellimuse kogusummat.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-201">In this context, the amount refers to the order total.</span></span>
    - <span data-ttu-id="fd5d3-202">**Kuni summani** – määrake lõppsumma, millele automaatne tasu rakendada.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-202">**To amount** – Specify the ending amount to apply the auto charge to.</span></span> <span data-ttu-id="fd5d3-203">Summa tähendab selles kontekstis tellimuse kogusummat.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-203">In this context, the amount refers to the order total.</span></span>
    - <span data-ttu-id="fd5d3-204">**Käibemaksugrupp** – määrake käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-204">**Sales tax group** – Specify a sales tax group.</span></span>
    - <span data-ttu-id="fd5d3-205">**Sait** ja **Ladu** – määrake sait ja ladu, kui tasud tuleb rakendada ainult konkreetsele saidile ja laole.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-205">**Site** and **Warehouse** – Specify a site and warehouse if charges should be applied only for a specific site and warehouse.</span></span>
    - <span data-ttu-id="fd5d3-206">**Säilita** – märkige see ruut tasukannete säilitamiseks pärast arve esitamise lõpule viimist, et tasu rakendataks iga kord, kui valitud kliendikontole uue arve loote.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-206">**Keep** – Select this check box to keep the charges transactions after invoicing is completed, so that the charge will be applied every time that you create a new invoice for the selected customer account.</span></span>

1. <span data-ttu-id="fd5d3-207">**Ainult müügitellimuste puhul:** kui soovite arvutada mitmetasandilisi tasusid, tutvuge teemaga [Müügitellimuste mitmetasandilised tasud](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders).</span><span class="sxs-lookup"><span data-stu-id="fd5d3-207">**For sales orders only:** If you want to calculate tiered charges, see [Tiered charges on sales orders](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-tiered-charges-on-sales-orders) for information.</span></span>

## <a name="allocate-charges-from-the-header-to-a-line"></a><span data-ttu-id="fd5d3-208">Tasude eraldamine päisest reale</span><span class="sxs-lookup"><span data-stu-id="fd5d3-208">Allocate charges from the header to a line</span></span>

<span data-ttu-id="fd5d3-209">Järgmises protseduuris näidatakse kuidas eraldada päisetaseme tasusid reale.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-209">The following procedure shows how to allocate header-level charges to a line.</span></span> <span data-ttu-id="fd5d3-210">Enne selle protseduuri alustamist peaks teil juba olema *fikseeritud summa* tüübiga päisetaseme tasu ja tellimus, mille puhul seda tasu rakendatakse.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-210">Before you start this procedure, you should already have a header-level charge of the *fixed amount* type and an order where that charge is applied.</span></span> <span data-ttu-id="fd5d3-211">Lisaks peab tellimus juba sisaldama vähemalt ühte reaüksust.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-211">Additionally, the order should already include at least one line item.</span></span>

1. <span data-ttu-id="fd5d3-212">Avage ostutellimus või tasutellimus.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-212">Open the purchase order or charge order.</span></span>
1. <span data-ttu-id="fd5d3-213">Järgige toimingupaanil ühte järgmistest etappidest.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-213">On the Action Pane, follow one of these steps:</span></span>

    - <span data-ttu-id="fd5d3-214">Ostutellimuste puhul: valige vahekaardil **Ost** grupis **Tasud** suvand **Tasude eraldamine**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-214">For purchase orders: On the **Purchase** tab, in the **Charges** group, select **Allocate charges**.</span></span>
    - <span data-ttu-id="fd5d3-215">Müügitellimuste puhul: valige vahekaardil **Müük** grupis **Tasud** suvand **Tasude eraldamine**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-215">For sales orders: On the **Sell** tab, in the **Charges** group, select **Allocate charges**.</span></span>

1. <span data-ttu-id="fd5d3-216">Määrake dialoogiboksis **Tasude määramine tellimuseridadele** järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-216">In the **Allocate charges to order lines** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="fd5d3-217">**Tasude eraldamine** – valige üks järgmistest väärtustest, et määrata, kuidas tuleks tasusid eraldada.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-217">**Charges allocation** – Select one of the following values to specify how the charges should be allocated:</span></span>

        - <span data-ttu-id="fd5d3-218">*Netosumma* – eraldage tasud vastavalt iga rea summale kogu netosumma suhtes.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-218">*Net amount* – Allocate charges according to each line amount relative to the total net amount.</span></span>
        - <span data-ttu-id="fd5d3-219">*Kogus* – eraldage tasud vastavalt iga rea ühikute arvule, mis on seotud ühikute koguarvuga.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-219">*Quantity* – Allocate charges according to the number of units for each line relative to the total number of units.</span></span>
        - <span data-ttu-id="fd5d3-220">*Rea kohta* – eraldage tasud võrdselt ridade koguarvu vahel.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-220">*Per line* – Allocate charges equally among the total number of lines.</span></span>

    - <span data-ttu-id="fd5d3-221">**Tasude eraldamine ridadele** – valige väärtus, et määrata, kas tasud tuleks eraldada kõikidele ridadele, ainult positiivsetele ridadele või ainult negatiivsetele ridadele.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-221">**Allocate charges to lines** – Select a value to specify whether charges should be allocated to all lines, to positive lines only, or to negative lines only.</span></span>
    - <span data-ttu-id="fd5d3-222">**Eralda kõik** – märkige see ruut, et eraldada tasud ostutellimuse ridadele ka juhul, kui tasukoodil on muu deebettüüp kui *Kaup*.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-222">**Allocate all** – Select this check box to allocate charges to order lines even if the charges code has a debit type other than *Item*.</span></span>
    - <span data-ttu-id="fd5d3-223">**Vastuvõetud** – märkige see ruut, et eraldada tasud ainult saadud tellimuse ridadele.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-223">**Received** – Select this check box to allocate charges only to received order lines.</span></span>
    - <span data-ttu-id="fd5d3-224">**Ladustatud** – märkige see ruut, et eraldada tasud ainult inverteeritud tellimuse ridadele.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-224">**Stocked** – Select this check box to allocate charges to only inventoried order lines.</span></span>
    - <span data-ttu-id="fd5d3-225">**Suvandite kuvamine ja kindlate ridade tühjendamine** – märkige see ruut, et välistada sellest eraldamisest konkreetsed read.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-225">**Show selections and clear specific lines** – Select this check box to exclude specific lines from this allocation.</span></span> <span data-ttu-id="fd5d3-226">Kui märgite selle ruudu, siis avaneb ruudustik **Eraldamisest välja arvatud ridade valimine**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-226">When you select this check box, the **Choose lines to exclude from allocation** grid is opened.</span></span> <span data-ttu-id="fd5d3-227">See ruudustik sisaldab ainult sätetega **Rea tasude eraldamine** ja **Ladustatud** määratletud kriteeriumidele vastavaid ridu.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-227">This grid includes only lines that match the criteria that are defined by the **Allocate charges to lines** and **Stocked** settings.</span></span> <span data-ttu-id="fd5d3-228">Näiteks kui teete väljal **Rea tasude eraldamine** valiku *Positiivsed read* ja märgite ruudu **Ladustatud** , kuvatakse ruudustikus ainult need read, mis on positiivsed ja inventeeritud.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-228">For example, if you set the **Allocate charges to lines** field to *Positive lines* and select the **Stocked** check box, the grid shows only lines that are both positive and inventoried.</span></span> <span data-ttu-id="fd5d3-229">Lisaks filtreerib ruudustik automaatselt kõik read, millel on kogu kogus juba vastu võetud.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-229">In addition, the grid automatically filters out any lines that the full quantity has already been received for.</span></span> <span data-ttu-id="fd5d3-230">Kui ruudustik on avatud, tühjendage märkeruut **Kaasa** iga rea puhul, mis tuleks eraldamisel välistada.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-230">While the grid is open, clear the **Include** check box for each line that should be excluded from allocation.</span></span> 

        > [!IMPORTANT]
        > <span data-ttu-id="fd5d3-231">Kui töötate ruudustikuga **Eraldamisest välja arvatud ridade valimine** , jätke kindlasti ruudustik senikaua avatuks, kuni valite **Eralda**.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-231">When you work with the **Choose lines to exclude from allocation** grid, be sure to leave the grid open until you select **Allocate**.</span></span> <span data-ttu-id="fd5d3-232">Kui sulgete ruudustiku enne valiku **Eralda** tegemist, lähevad teie ruudustiku sätted kaotsi.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-232">If you close the grid before you select **Allocate** , your settings in the grid will be lost.</span></span> <span data-ttu-id="fd5d3-233">Seega tasud eraldatakse vastavalt eelnevalt määratletud kriteeriumitele.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-233">Therefore, charges will be allocated based on the criteria that you previously defined.</span></span>

1. <span data-ttu-id="fd5d3-234">Valige **Eralda** , et rakendada oma sätted ja sulgeda päringu dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="fd5d3-234">Select **Allocate** to apply your settings and close the dialog box.</span></span>