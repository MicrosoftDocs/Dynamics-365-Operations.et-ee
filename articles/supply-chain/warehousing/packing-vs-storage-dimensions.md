---
title: Pakkimiseks ja ladustamiseks erinevate dimensioonide määramine
description: See teema näitab, kuidas määrata, millise protsessi (pakkimine, ladustamine või pesastatud pakkimine) jaoks iga määratud dimensiooni kasutatakse.
author: mirzaab
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: aa5cbf807e809238489c539d3ad8c0bc34421774
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501290"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a><span data-ttu-id="d7c49-103">Pakkimiseks ja ladustamiseks erinevate dimensioonide määramine</span><span class="sxs-lookup"><span data-stu-id="d7c49-103">Set different dimensions for packing and storage</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d7c49-104">Mõned kaubad on pakitud või ladustatud nii, et teil võib tekkida vajadus jälgida füüsilisi dimensioone iga erineva protsessi puhul teisiti.</span><span class="sxs-lookup"><span data-stu-id="d7c49-104">Some items are packed or stored in such a way that you may need to track physical dimensions differently for each of several different processes.</span></span> <span data-ttu-id="d7c49-105">Funktsiooni *Pakendatava toote dimensioonid* abil saate igale tootele seadistada ühe või mitut tüüpi mõõtmeid.</span><span class="sxs-lookup"><span data-stu-id="d7c49-105">The *Packaging product dimensions* feature lets you set up one or several types of dimensions for each product.</span></span> <span data-ttu-id="d7c49-106">Iga dimensiooni tüüp tagab füüsiliste mõõtmiste kogumi (kaal, laius, sügavus ja kõrgus) ning määrab nende füüsiliste mõõtmise väärtuste rakendumise protsessi.</span><span class="sxs-lookup"><span data-stu-id="d7c49-106">Each dimension type provides a set of physical measurements (weight, width, depth, and height), and establishes the process where those physical measurement values apply.</span></span> <span data-ttu-id="d7c49-107">Kui see funktsioon on lubatud, toetab süsteem järgmisi dimensiooni tüüpe.</span><span class="sxs-lookup"><span data-stu-id="d7c49-107">When this feature is enabled, your system will support the following types of dimensions:</span></span>

- <span data-ttu-id="d7c49-108">*Ladustamine* – laoala dimensioone kasutatakse koos asukoha mahuliste mõõtmetega, et määrata, kui palju iga kaupa saab erinevates lao asukohtades ladustada.</span><span class="sxs-lookup"><span data-stu-id="d7c49-108">*Storage* - Storage dimensions are used along with location volumetrics to determine how many of each item can be stored in various warehouse locations.</span></span>
- <span data-ttu-id="d7c49-109">*Pakkimine* – pakkimise dimensioone kasutatakse konteineritesse pakkimisel ja käsitsi pakkimise protsessi käigus, et määrata, kui palju iga kaupa erinevatesse konteineritüüpidesse mahub.</span><span class="sxs-lookup"><span data-stu-id="d7c49-109">*Packing* - Packing dimensions are used during containerization and the manual packing process to determine how many of each item will fit in various container types.</span></span>
- <span data-ttu-id="d7c49-110">*Pesastatud pakkimine* – pesastatud pakkimise dimensioone kasutatakse siis, kui pakkimisprotsess sisaldab mitut taset.</span><span class="sxs-lookup"><span data-stu-id="d7c49-110">*Nested packing* - Nested packing dimensions are used when the packing process contains multiple levels.</span></span>

<span data-ttu-id="d7c49-111">*Ladustamise* dimensioone toetatakse isegi juhul, kui funktsioon *Pakendatava toote dimensioonid* pole lubatud.</span><span class="sxs-lookup"><span data-stu-id="d7c49-111">*Storage* dimensions are supported even when the *Packaging product dimensions* feature isn't enabled.</span></span> <span data-ttu-id="d7c49-112">Häälestate need rakenduse Supply Chain Management lehte **Füüsiline dimensioon** kasutades.</span><span class="sxs-lookup"><span data-stu-id="d7c49-112">You set these up using the **Physical dimension** page in Supply Chain Management.</span></span> <span data-ttu-id="d7c49-113">Neid dimensioone kasutavad kõik protsessid, kus pakkimise ja pesastatud pakkimise dimensioonid on määramata.</span><span class="sxs-lookup"><span data-stu-id="d7c49-113">These dimensions are used by all processes where the packing and nested packing dimensions aren't specified.</span></span>

<span data-ttu-id="d7c49-114">*Pakkimise* ja *pesastatud pakkimise* dimensioonid häälestatakse, kasutades lehte **Toote füüsilised dimensioonid**, mis lisatakse, kui lubate funktsiooni *Pakendatava toote dimensioonid*.</span><span class="sxs-lookup"><span data-stu-id="d7c49-114">*Packing* and *nested packing* dimensions are set up using the **Physical product dimensions** page, which is added when you enable the *Packaging product dimensions* feature.</span></span>
<span data-ttu-id="d7c49-115">See teema sisaldab stsenaariumit, mis kirjeldab selle funktsiooni kasutamist.</span><span class="sxs-lookup"><span data-stu-id="d7c49-115">This topic provides a scenario that illustrates how to use this feature.</span></span>

## <a name="turn-on-the-packaging-product-dimensions-feature"></a><span data-ttu-id="d7c49-116">Lülitage pakendatavate toodete dimensioonide funktsioon sisse.</span><span class="sxs-lookup"><span data-stu-id="d7c49-116">Turn on the packaging product dimensions feature</span></span>

<span data-ttu-id="d7c49-117">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="d7c49-117">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="d7c49-118">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="d7c49-118">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d7c49-119">Seega on funktsioon loetletud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="d7c49-119">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d7c49-120">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="d7c49-120">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d7c49-121">**Funktsiooni nimi:** *Pakendatavate toodete mõõtmed*</span><span class="sxs-lookup"><span data-stu-id="d7c49-121">**Feature name:** *Packaging product dimensions*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="d7c49-122">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="d7c49-122">Example scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="d7c49-123">Stsenaariumi seadistamine</span><span class="sxs-lookup"><span data-stu-id="d7c49-123">Set up the scenario</span></span>

<span data-ttu-id="d7c49-124">Enne kui käivitate näidisstsenaariumi, peate oma süsteemi selles jaotises kirjeldatud viisil ette valmistama.</span><span class="sxs-lookup"><span data-stu-id="d7c49-124">Before you can run the example scenario, you must prepare your system as described in this section.</span></span>

#### <a name="enable-demo-data"></a><span data-ttu-id="d7c49-125">Demoandmete lubamine</span><span class="sxs-lookup"><span data-stu-id="d7c49-125">Enable demo data</span></span>

<span data-ttu-id="d7c49-126">Selle stsenaariumi kasutamiseks siin määratud demokirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="d7c49-126">To work through this scenario using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="d7c49-127">Enne alustamist peate valima ka juriidilise isiku *USMF*.</span><span class="sxs-lookup"><span data-stu-id="d7c49-127">Additionally, you must select the *USMF* legal entity before you begin.</span></span>

#### <a name="add-a-new-physical-dimension-to-a-product"></a><span data-ttu-id="d7c49-128">Tootele uue füüsilise dimensiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="d7c49-128">Add a new physical dimension to a product</span></span>

<span data-ttu-id="d7c49-129">Lisage tootele uus füüsiline dimensioon, tehes järgmist:</span><span class="sxs-lookup"><span data-stu-id="d7c49-129">Add a new physical dimension for a product by doing the following:</span></span>

1. <span data-ttu-id="d7c49-130">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="d7c49-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="d7c49-131">Valige toote **kaubakoodiga** *A0001*.</span><span class="sxs-lookup"><span data-stu-id="d7c49-131">Select the product with **Item number** *A0001*.</span></span>
1. <span data-ttu-id="d7c49-132">Avage toimingupaani vahekaart **Varude haldamine** ja valige grupis **Ladu** suvand **Füüsilised toote dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="d7c49-132">On the Action Pane, open the **Manage inventory** tab and, from the **Warehouse** group, select **Physical product dimensions**.</span></span>
1. <span data-ttu-id="d7c49-133">Avaneb leht **Füüsilised toote dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="d7c49-133">The **Physical product dimensions** page opens.</span></span> <span data-ttu-id="d7c49-134">Valige tegevuspaanil suvand **Uus**, et lisada ruudustikku uus dimensioon koos järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="d7c49-134">On the Action Pane, select **New** to add a new dimension to the grid with the following settings:</span></span>
    - <span data-ttu-id="d7c49-135">**Füüsilise dimensiooni tüüp** - *Pakkimine*</span><span class="sxs-lookup"><span data-stu-id="d7c49-135">**Physical dimension type** - *Packing*</span></span>
    - <span data-ttu-id="d7c49-136">**Füüsiline ühik** - *tk*</span><span class="sxs-lookup"><span data-stu-id="d7c49-136">**Physical unit** - *pcs*</span></span>
    - <span data-ttu-id="d7c49-137">**Kaal** - *4*</span><span class="sxs-lookup"><span data-stu-id="d7c49-137">**Weight** - *4*</span></span>
    - <span data-ttu-id="d7c49-138">**Massiühik** - *kg*</span><span class="sxs-lookup"><span data-stu-id="d7c49-138">**Weight unit** - *kg*</span></span>
    - <span data-ttu-id="d7c49-139">**Sügavus** - *3*</span><span class="sxs-lookup"><span data-stu-id="d7c49-139">**Depth** - *3*</span></span>
    - <span data-ttu-id="d7c49-140">**Kõrgus** - *4*</span><span class="sxs-lookup"><span data-stu-id="d7c49-140">**Height** - *4*</span></span>
    - <span data-ttu-id="d7c49-141">**Laius** - *3*</span><span class="sxs-lookup"><span data-stu-id="d7c49-141">**Width** - *3*</span></span>
    - <span data-ttu-id="d7c49-142">**Pikkus** - *cm*</span><span class="sxs-lookup"><span data-stu-id="d7c49-142">**Length** - *cm*</span></span>
    - <span data-ttu-id="d7c49-143">**Mahuühik** - *cm3*</span><span class="sxs-lookup"><span data-stu-id="d7c49-143">**Volume unit** - *cm3*</span></span>

<span data-ttu-id="d7c49-144">Väli **Maht** arvutatakse automaatselt teie sätete **Sügavus**, **Kõrgus** ja **Laius** põhjal.</span><span class="sxs-lookup"><span data-stu-id="d7c49-144">The **Volume** field is automatically calculated based on your **Depth**, **Height**, and **Width** settings.</span></span>

#### <a name="create-a-new-container-type"></a><span data-ttu-id="d7c49-145">Uue konteineri tüübi loomine</span><span class="sxs-lookup"><span data-stu-id="d7c49-145">Create a new container type</span></span>

<span data-ttu-id="d7c49-146">Avage suvand **Laohaldus \> Seadistus \> Konteinerid \> Konteineri tüübid** ja looge uus kirje järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="d7c49-146">Go to **Warehouse management \> Setup \> Containers \> Container types** and create a new record with the following settings:</span></span>

- <span data-ttu-id="d7c49-147">**Konteineri tüübi kood** - *lühike kast*</span><span class="sxs-lookup"><span data-stu-id="d7c49-147">**Container type code** - *Short Box*</span></span>
- <span data-ttu-id="d7c49-148">**Kirjeldus** - *lühike kast*</span><span class="sxs-lookup"><span data-stu-id="d7c49-148">**Description** - *Short Box*</span></span>
- <span data-ttu-id="d7c49-149">**Maksimaalne netokaal** - *50*</span><span class="sxs-lookup"><span data-stu-id="d7c49-149">**Maximum net weight** - *50*</span></span>
- <span data-ttu-id="d7c49-150">**Maht** - *144*</span><span class="sxs-lookup"><span data-stu-id="d7c49-150">**Volume** - *144*</span></span>
- <span data-ttu-id="d7c49-151">**Pikkus** - *6*</span><span class="sxs-lookup"><span data-stu-id="d7c49-151">**Length** - *6*</span></span>
- <span data-ttu-id="d7c49-152">**Laius** - *6*</span><span class="sxs-lookup"><span data-stu-id="d7c49-152">**Width** - *6*</span></span>
- <span data-ttu-id="d7c49-153">**Kõrgus** - *4*</span><span class="sxs-lookup"><span data-stu-id="d7c49-153">**Height** - *4*</span></span>

#### <a name="create-a-container-group"></a><span data-ttu-id="d7c49-154">Konteinerigrupi loomine</span><span class="sxs-lookup"><span data-stu-id="d7c49-154">Create a container group</span></span>

<span data-ttu-id="d7c49-155">Avage suvand **Laohaldus \> Seadistus \> Konteinerid \> Konteinerigrupid** ja looge uus kirje järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="d7c49-155">Go to **Warehouse management \> Setup \> Containers \> Container groups** and create a new record with the following settings:</span></span>

- <span data-ttu-id="d7c49-156">**Konteinerigrupi ID** - *lühike kast*</span><span class="sxs-lookup"><span data-stu-id="d7c49-156">**Container group ID** - *Short Box*</span></span>
- <span data-ttu-id="d7c49-157">**Kirjeldus** - *lühike kast*</span><span class="sxs-lookup"><span data-stu-id="d7c49-157">**Description** - *Short Box*</span></span>

<span data-ttu-id="d7c49-158">Lisage uus rida jaotisse **Üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="d7c49-158">Add a new line to the **Details** section.</span></span> <span data-ttu-id="d7c49-159">Määrake **konteineri tüübiks** *Lühike kast*.</span><span class="sxs-lookup"><span data-stu-id="d7c49-159">Set the **Container type** to *Short Box*.</span></span>

#### <a name="set-up-a-container-build-template"></a><span data-ttu-id="d7c49-160">Konteineri koostemalli häälestamine</span><span class="sxs-lookup"><span data-stu-id="d7c49-160">Set up a container build template</span></span>

<span data-ttu-id="d7c49-161">Avage **Laohaldus \> Seadistus \> Konteinerid \> Konteinerite loomise mallid** ja valige **Kastid**.</span><span class="sxs-lookup"><span data-stu-id="d7c49-161">Go to **Warehouse management \> Setup \> Containers \> Container build templates** and select **Boxes**.</span></span> <span data-ttu-id="d7c49-162">Muutke **konteinerigrupi ID** valikule *lühike kast*.</span><span class="sxs-lookup"><span data-stu-id="d7c49-162">Change the **Container group ID** to *Short Box*.</span></span>

### <a name="run-the-scenario"></a><span data-ttu-id="d7c49-163">Käivitage stsenaarium</span><span class="sxs-lookup"><span data-stu-id="d7c49-163">Run the scenario</span></span>

<span data-ttu-id="d7c49-164">Pärast oma süsteemi ettevalmistamist eelmises jaotises kirjeldatud viisil olete valmis käivitama stsenaariumi nii, nagu on kirjeldatud järgmises jaotises.</span><span class="sxs-lookup"><span data-stu-id="d7c49-164">After you have prepared your system as described in the previous section, you are ready to run the scenario as described in the next section.</span></span>

#### <a name="create-a-sales-order-and-create-a-shipment"></a><span data-ttu-id="d7c49-165">Müügitellimuse ja saadetise loomine</span><span class="sxs-lookup"><span data-stu-id="d7c49-165">Create a sales order and create a shipment</span></span>

<span data-ttu-id="d7c49-166">Selles protsessis loote saadetise kauba *pakendamise* dimensioonide põhjal, mille kõrgus on alla 3.</span><span class="sxs-lookup"><span data-stu-id="d7c49-166">In this process you will create a shipment based on the item *packing* dimensions, for which the height is less than 3.</span></span>

1. <span data-ttu-id="d7c49-167">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="d7c49-167">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d7c49-168">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d7c49-168">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d7c49-169">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d7c49-169">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d7c49-170">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="d7c49-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="d7c49-171">**Ladu:** *63*</span><span class="sxs-lookup"><span data-stu-id="d7c49-171">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="d7c49-172">Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7c49-172">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="d7c49-173">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="d7c49-173">The new sales order is opened.</span></span> <span data-ttu-id="d7c49-174">See peaks sisaldama uut tühja rida kiirkaardi **Müügitellimuse read** ruudustikus.</span><span class="sxs-lookup"><span data-stu-id="d7c49-174">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d7c49-175">Määrake sellel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="d7c49-175">On this line, set the following values:</span></span>

    - <span data-ttu-id="d7c49-176">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="d7c49-176">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d7c49-177">**Kogus:** *5*</span><span class="sxs-lookup"><span data-stu-id="d7c49-177">**Quantity:** *5*</span></span>

1. <span data-ttu-id="d7c49-178">Tehke kiirkaardil **Müügitellimuse read** valik **Varud \> Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="d7c49-178">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="d7c49-179">Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud.</span><span class="sxs-lookup"><span data-stu-id="d7c49-179">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="d7c49-180">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d7c49-180">Close the page.</span></span>
1. <span data-ttu-id="d7c49-181">Avage tegevuspaani vahekaart **Ladu** ja valige **Lattu väljastamine**, et luua lao jaoks töö.</span><span class="sxs-lookup"><span data-stu-id="d7c49-181">On the Action Pane, open the **Warehouse** tab and select **Release to warehouse** to create work for the warehouse.</span></span>
1. <span data-ttu-id="d7c49-182">Kiirkaardil **Müügitellimuse** read valige **Ladu \> Saadetise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="d7c49-182">On the **Sales order lines** FastTab, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="d7c49-183">Avage toimingupaanilt vahekaart **Transport** ja valige **Kuva konteinerid**.</span><span class="sxs-lookup"><span data-stu-id="d7c49-183">On the Action Pane, open the **Transportation** tab and select **View containers**.</span></span> <span data-ttu-id="d7c49-184">Kinnitage, et kaup pakiti konteineritesse, mis olid kaks *lühikese kasti* konteinerit.</span><span class="sxs-lookup"><span data-stu-id="d7c49-184">Confirm that the item was containerized into the two *Short Box* containers.</span></span>

#### <a name="place-an-item-into-storage"></a><span data-ttu-id="d7c49-185">Kauba lattu panemine</span><span class="sxs-lookup"><span data-stu-id="d7c49-185">Place an item into storage</span></span>

1. <span data-ttu-id="d7c49-186">Avage mobiilne seade, logige sisse lattu 63 ja avage **Varud \> Korrigeeri üksuses**.</span><span class="sxs-lookup"><span data-stu-id="d7c49-186">Open the mobile device, sign in to warehouse 63 and go to **Inventory \> Adjust In**.</span></span>
1. <span data-ttu-id="d7c49-187">Sisestage **Loc** = *SHORT-01*.</span><span class="sxs-lookup"><span data-stu-id="d7c49-187">Enter **Loc** = *SHORT-01*.</span></span> <span data-ttu-id="d7c49-188">Tehke uus registreerimismärk näitajatega **Kaup** = *A0001* ja **Kogus** = *1 tk*.</span><span class="sxs-lookup"><span data-stu-id="d7c49-188">Make a new license plate with **Item** = *A0001* and **Quantity** = *1 pcs*.</span></span>
1. <span data-ttu-id="d7c49-189">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d7c49-189">Select **OK**.</span></span> <span data-ttu-id="d7c49-190">Teile kuvatakse tõrge „Asukoha SHORT-01 valimine nurjus, sest kaup A0001 ei mahu asukoha määratud mõõtmesse.”</span><span class="sxs-lookup"><span data-stu-id="d7c49-190">You will receive the error "Location SHORT-01 failed because item A0001 does not fit in location's specified dimensions."</span></span> <span data-ttu-id="d7c49-191">Seda seetõttu, et toote tüübi *Ladu* dimensioonid on suuremad kui asukoha profiilis määratletud dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="d7c49-191">This is because the *Storage* type dimensions of the product are larger than the dimensions specified on the location profile.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]