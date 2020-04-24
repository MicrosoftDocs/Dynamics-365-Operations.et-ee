---
title: Paindliku laotaseme dimensiooni reserveerimise poliitika
description: See teema kirjeldab varude reserveerimise poliitikat, mis võimaldab partiijälgimisega tooteid müüvatel ettevõtetel käitada nende logistikat, nagu WMS-i toega toimingud, kindlatel partiidel kliendi müügitellimuste jaoks. Seda ka siis, kui tootega seostatud reserveerimise hierarhia ei luba kindlaid partiisid reserveerida.
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0fe9ed9f2bebe8683f3b8bb37b33e8a63b9521f6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205663"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="fde70-103">Paindliku laotaseme dimensiooni reserveerimise poliitika</span><span class="sxs-lookup"><span data-stu-id="fde70-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fde70-104">Kui varude reserveerimise hierarhia tüüp „partii-alla\[asukoha\]” on seotud toodetega, siis ei saa ettevõtted, mis müüvad partiijälgimisega tooteid ja käitavad nende logistikat, mis on lubatud Microsoft Dynamics 365 laohaldusesüsteemi (WMS) jaoks, reserveerida nende toodete kindlaid partiisid kliendi müügitellimustele.</span><span class="sxs-lookup"><span data-stu-id="fde70-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="fde70-105">See teema kirjeldab varude reserveerimise poliitikat, mis võimaldab nendel ettevõtetel kindlaid partiisid reserveerida isegi siis, kui tooted on seotud reserveerimise hierarhia üksusega „partii-alla\[asukoht\]”.</span><span class="sxs-lookup"><span data-stu-id="fde70-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="fde70-106">Varude reserveerimise hierarhia</span><span class="sxs-lookup"><span data-stu-id="fde70-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="fde70-107">See jaotis võtab kokku olemasoleva varude reserveerimise hierarhia.</span><span class="sxs-lookup"><span data-stu-id="fde70-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="fde70-108">See keskendub viisile, kuidas käsitsetakse partii- ja seeriajälgimisega üksusi.</span><span class="sxs-lookup"><span data-stu-id="fde70-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="fde70-109">Varude reserveerimise hierarhia näitab, et laoala dimensioonidega seotud ulatuses on tellimuse nõudlus seotud asukoha kohustuslike dimensioonide, lao ja varude olekuga, samas kui lao loogika vastutab nõutud koguste jaoks asukoha määramise ja selle reserveerimise eest.</span><span class="sxs-lookup"><span data-stu-id="fde70-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="fde70-110">Teisisõnu, nõudluse ja laotoimingute vahelises suhtluses eeldatakse, et nõudluse järjekord määrab selle, kuhu tellimus tuleb saata (st millisesse asukohta ja lattu).</span><span class="sxs-lookup"><span data-stu-id="fde70-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="fde70-111">Seejärel toetub ladu laoruumidest nõutava koguse leidmisel oma loogikale.</span><span class="sxs-lookup"><span data-stu-id="fde70-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="fde70-112">Kuid selleks, et kajastada äritegevuse mudelit, on jälgimisdimensioonid (partii- ja seerianumbrid) siiski paindlikumad.</span><span class="sxs-lookup"><span data-stu-id="fde70-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="fde70-113">Varude reserveerimise hierarhia võib hõlmata stsenaariume, mille puhul kehtivad järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="fde70-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="fde70-114">Ettevõte tugineb oma laotoimingutele, et hallata partii- või seerianumbritega koguste komplekteerimist pärast seda, kui ladustamisruumis on kogused leitud.</span><span class="sxs-lookup"><span data-stu-id="fde70-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="fde70-115">Sellele mudelile viidatakse sageli kui *partii-alla\[asukoht\]*.</span><span class="sxs-lookup"><span data-stu-id="fde70-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="fde70-116">Seda kasutatakse tavaliselt siis, kui toote partii- või seerianumbri ID ei ole klientidele oluline, kuna nad suunavad nõudluse müügiettevõttele.</span><span class="sxs-lookup"><span data-stu-id="fde70-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="fde70-117">Kui partii- või seerianumbrid on osa kliendi tellimuse täpsustusest ja need kirjendatakse nõudlustellimusele, on laos olevaid koguseid leidnud toimingud piiratud konkreetsete nõutud numbritega ja neid ei tohi muuta.</span><span class="sxs-lookup"><span data-stu-id="fde70-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="fde70-118">Sellele mudelile viidatakse sageli kui *partii-üles\[asukoht\]*.</span><span class="sxs-lookup"><span data-stu-id="fde70-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="fde70-119">Nende stsenaariumide puhul on probleemiks, et igale väljastatud tootele saab määrata ainult ühe varude reserveerimise hierarhia.</span><span class="sxs-lookup"><span data-stu-id="fde70-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="fde70-120">Seetõttu ei saa WMS pärast seda, kui hierarhia määramine on määratlenud, millal partii või seerianumber tuleb reserveerida (kas siis, kui nõude tellimus on tehtud, või lao komplekteerimise ajal), jälgitud üksuste käsitsemisel ajastust ad-hoc-alusel muuta.</span><span class="sxs-lookup"><span data-stu-id="fde70-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="fde70-121">Partiijälgimisega kaupade paindlik reserveerimine</span><span class="sxs-lookup"><span data-stu-id="fde70-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="fde70-122">Äristsenaarium</span><span class="sxs-lookup"><span data-stu-id="fde70-122">Business scenario</span></span>

<span data-ttu-id="fde70-123">Selle stsenaariumi puhul kasutab ettevõte varude strateegiat, mille puhul lõpetatud kaupu jälgitakse partii numbrite järgi.</span><span class="sxs-lookup"><span data-stu-id="fde70-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="fde70-124">See ettevõte kasutab ka WMS-i töökogust.</span><span class="sxs-lookup"><span data-stu-id="fde70-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="fde70-125">Kuna sellel töökogusel on hästivarustatud loogika lao komplekteerimise ja saatmise toimingute planeerimiseks ning käitamiseks partiis lubatud kaupade puhul, on enamik lõpetatud kaupadest seotud „partii-alla\[asukoht\]“ varude reserveerimise hierarhiaga.</span><span class="sxs-lookup"><span data-stu-id="fde70-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="fde70-126">Seda tüüpi toiminguseadistuse eeliseks on see, et partiide komplekteerimise ja laovaliku otsused (mis on tegelikult reserveerimise otsused) lükatakse edasi, kuni alustatakse lao komplekteerimise toimingutega.</span><span class="sxs-lookup"><span data-stu-id="fde70-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="fde70-127">Neid ei tehta kliendi tellimuse esitamise ajal.</span><span class="sxs-lookup"><span data-stu-id="fde70-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="fde70-128">Kuigi „partii-alla\[asukoht\]” reserveerimise hierarhia teenib ettevõtte ärieesmärke hästi, nõuavad paljud ettevõtte kliendid toodete uuesti tellimisel sama partiid, mida nad varem ostsid.</span><span class="sxs-lookup"><span data-stu-id="fde70-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="fde70-129">Seetõttu ootavad ettevõtted paindlikkust selle osas, kuidas partii reserveerimise reegleid käsitletakse, nii et olenevalt klientide nõudlusest sama kauba järele võivad ilmneda järgmised käitumismustrid.</span><span class="sxs-lookup"><span data-stu-id="fde70-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="fde70-130">Partii numbrit saab kirjendada ja reserveerida, kui volitatud töötleja on tellimuse vastu võtnud, ja seda ei saa muuta laotoimingute ajal ja/või muude nõudmiste tõttu.</span><span class="sxs-lookup"><span data-stu-id="fde70-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="fde70-131">Selline käitumine aitab tagada, et tellitud partiinumber saadetakse kliendile.</span><span class="sxs-lookup"><span data-stu-id="fde70-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="fde70-132">Kui partiinumber ei ole kliendile oluline, saab laotoimingute komplekteerimise käigus määrata partiinumbri pärast seda, kui müügitellimuse registreerimine ja reserveerimine on tehtud.</span><span class="sxs-lookup"><span data-stu-id="fde70-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="fde70-133">Müügitellimuse kindla partii reserveerimise lubamine</span><span class="sxs-lookup"><span data-stu-id="fde70-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="fde70-134">Selleks, et mahutada soovitud paindlikkus partii reserveerimise käitumises kaupadele, mis on seotud „partii-alla\[asukoht\]” varude reserveerimise hierarhiaga, peavad varude haldurid lehel **Varude reserveerimise hierarhiad** valima märkeruudu **Luba reserveerimine nõudmisel tellimusele** valiku **Partiinumber** tasemel.</span><span class="sxs-lookup"><span data-stu-id="fde70-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Varude reserveerimise hierarhia paindlikuks muutmine](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="fde70-136">Kui hierarhias valitakse tase **Partiinumber**, valitakse automaatselt kõik seda taset ületavad dimensioonid kuni **Asukoha** tasemeni.</span><span class="sxs-lookup"><span data-stu-id="fde70-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="fde70-137">(Vaikimisi valitakse tasemest **Asukoht** üle olevad dimensioonid.) Selline käitumine peegeldab loogikat, kus kõik dimensioonid partiinumbri ja asukoha vahel on samuti automaatselt reserveeritud pärast seda, kui reserveerite tellimuse reale kindla partiinumbri.</span><span class="sxs-lookup"><span data-stu-id="fde70-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="fde70-138">Märkeruut **Luba reserveerimine nõudmisel tellimusele** kehtib ainult reserveerimise hierarhia tasemete puhul, mis jäävad lao asukoha dimensioonist allapoole.</span><span class="sxs-lookup"><span data-stu-id="fde70-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="fde70-139">**Partiinumber** on paindliku reserveerimise poliitika jaoks avatud hierarhia ainus tase.</span><span class="sxs-lookup"><span data-stu-id="fde70-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="fde70-140">Teisisõnu ei saa te märkida ruutu **Luba reserveerimine nõudmisel tellimusele** taseme **Asukoht**, **Litsentsiplaat** või **Seerianumber** jaoks.</span><span class="sxs-lookup"><span data-stu-id="fde70-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="fde70-141">Kui teie reserveerimise hierarhia sisaldab seerianumbri dimensiooni (mis peab alati olema väiksem kui tase **Partiinumber**) ja kui olete pakktöötluse numbrile sisse lülitanud partii-spetsiifilise reserveerimise, jätkab süsteem seerianumbri reserveerimise ja komplekteerimise toiminguid, mis põhinevad reeglitel, mis kehtivad reserveerimise poliitika „Seeria-alla\[asukoht\]” puhul.</span><span class="sxs-lookup"><span data-stu-id="fde70-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="fde70-142">Igal ajahetkel saate lubada partii-spetsiifilist reserveerimist olemasolevale „partii-alla\[asukoht\]” reserveerimise hierarhiale teie juurutuses.</span><span class="sxs-lookup"><span data-stu-id="fde70-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="fde70-143">See muudatus ei mõjuta reserveeringuid ja avatud lao tööd, mis loodi enne muudatuse toimumist.</span><span class="sxs-lookup"><span data-stu-id="fde70-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="fde70-144">Kuid märkeruutu **Luba reserveerimine nõudmisel tellimusele** ei saa tühjendada, kui **Reserveeritud tellitud**, **Reserveeritud füüsilise** või **Tellitud** probleemi tüübi laokanded on olemas ühe või mitme selle reserveerimise hierarhiaga seotud kauba puhul.</span><span class="sxs-lookup"><span data-stu-id="fde70-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="fde70-145">Kui kauba olemasoleva reserveerimise hierarhia ei luba tellimuse partii täpsustust, saate selle uuesti määrata reserveerimise hierarhiasse, mis lubab partii spetsifikatsioone, tingimusel et hierarhia taseme struktuur on mõlemas hierarhias sama.</span><span class="sxs-lookup"><span data-stu-id="fde70-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="fde70-146">Kasutage funktsiooni **Muuda reserveerimise hierarhiat kaupadele** ümbermääramiseks.</span><span class="sxs-lookup"><span data-stu-id="fde70-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="fde70-147">See muudatus võib olla oluline, kui soovite vältida partiis jälitatud kaupade alamhulga paindlikku partii reserveerimist, kuid lubada seda ülejäänud tooteportfellile.</span><span class="sxs-lookup"><span data-stu-id="fde70-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="fde70-148">Olenemata sellest, kas olete märkinud ruudu **Luba reserveerimine nõudmisel tellimusele**, kui te ei soovi kindlat partiinumbrit kaubale tellimuse rea jaoks reserveerida, rakendatakse laotoimingute vaikeloogikat, mis kehtib „partii-alla\[asukoht\]” reserveerimise hierarhia puhul.</span><span class="sxs-lookup"><span data-stu-id="fde70-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="fde70-149">Kindla partiinumbri reserveerimine kliendi tellimuse jaoks</span><span class="sxs-lookup"><span data-stu-id="fde70-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="fde70-150">Pärast seda, kui partii jälgitud kauba „partii-alla\[asukoht\]” varude reserveerimise hierarhia on seadistatud lubama kindla partiinumbrite reserveerimist müügitellimustel, võivad müügitellimuse töötlejad võtta sama kauba kohta kliendi tellimusi ühel järgmistest viisidest, olenevalt kliendi nõudest.</span><span class="sxs-lookup"><span data-stu-id="fde70-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="fde70-151">**Sisestage tellimuse üksikasjad partiinumbrit täpsustamata** – seda lähenemist tuleks kasutada juhul, kui toote partii spetsifikatsioon ei ole kliendile oluline.</span><span class="sxs-lookup"><span data-stu-id="fde70-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="fde70-152">Kõik olemasolevad protsessid, mis on seotud selle tüübi tellimuse käsitsemisega, jäävad süsteemis muutmata.</span><span class="sxs-lookup"><span data-stu-id="fde70-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="fde70-153">Kasutajate osas ei nõuta täiendavaid kaalutlusi.</span><span class="sxs-lookup"><span data-stu-id="fde70-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="fde70-154">**Sisestage tellimuse üksikasjad ja reserveerige konkreetne partiinumber** – seda lähenemist tuleks kasutada siis, kui klient nõuab kindlat partiid.</span><span class="sxs-lookup"><span data-stu-id="fde70-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="fde70-155">Tavaliselt nõuavad kliendid kindlat partiid, kui nad tellivad varem ostetud toodet.</span><span class="sxs-lookup"><span data-stu-id="fde70-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="fde70-156">Seda tüüpi partii-spetsiifilist reserveerimist nimetatakse *tellimusega kooskõlastatud reserveerimiseks*.</span><span class="sxs-lookup"><span data-stu-id="fde70-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="fde70-157">Järgmised reeglid kehtivad koguste töötlemisel ja partiinumber on seotud kindla tellimusega.</span><span class="sxs-lookup"><span data-stu-id="fde70-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="fde70-158">Selleks et lubada kauba kindla partii numbri reserveerimist kauba puhul, mis on märgitud jaotises „partii-alla\[asukoht\]”, peab süsteem reserveerima kõik dimensioonid asukoha kaudu.</span><span class="sxs-lookup"><span data-stu-id="fde70-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="fde70-159">See vahemik sisaldab tavaliselt litsentsiplaadi dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="fde70-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="fde70-160">Asukoha direktiive ei kasutata, kui komplekteerimise töö on loodud müügirea jaoks, mis kasutab tellimusega seotud partii reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="fde70-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="fde70-161">Tellimusega seotud partiide töö laotöötluse ajal ei tohi ei kasutaja ega süsteem partii numbrit muuta.</span><span class="sxs-lookup"><span data-stu-id="fde70-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="fde70-162">(See töötlemine hõlmab erandite käsitlemist.)</span><span class="sxs-lookup"><span data-stu-id="fde70-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="fde70-163">Järgmises näites kuvatakse täielik töövoog.</span><span class="sxs-lookup"><span data-stu-id="fde70-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="fde70-164">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="fde70-164">Example scenario</span></span>

<span data-ttu-id="fde70-165">Selle näite jaoks peavad olema installitud demoandmed ja peate kasutama demoandmete ettevõtet **USMF**.</span><span class="sxs-lookup"><span data-stu-id="fde70-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="fde70-166">Varude reserveerimise hierarhia seadistamine partiile konkreetse reserveerimise lubamiseks</span><span class="sxs-lookup"><span data-stu-id="fde70-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="fde70-167">Avage **Laohaldus** \> **Seadistus** \> **Varud \> Reserveerimine hierarhiasse**.</span><span class="sxs-lookup"><span data-stu-id="fde70-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="fde70-168">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fde70-168">Select **New**.</span></span>
3. <span data-ttu-id="fde70-169">Väljale **Nimi** sisestage nimi (nt **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="fde70-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="fde70-170">Väljale **Kirjeldus** sisestage kirjeldus (nt **Partii alla paindlikkuse**).</span><span class="sxs-lookup"><span data-stu-id="fde70-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="fde70-171">Väljal **Valitud** valige **Seerianumber** ja **Omanik** ning seejärel klõpsake vasakut nooleklahvi, et teisaldada need väljale **Saadaolev**.</span><span class="sxs-lookup"><span data-stu-id="fde70-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="fde70-172">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="fde70-172">Select **OK**.</span></span>
7. <span data-ttu-id="fde70-173">Märkige dimensioonitaseme real **Partiinumbri** ruut **Luba reserveerimine nõudmisel tellimusele**.</span><span class="sxs-lookup"><span data-stu-id="fde70-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="fde70-174">Tasemed **Litsentsiplaat** ja **Asukoht** valitakse automaatselt ja nende märkeruute ei saa tühjendada.</span><span class="sxs-lookup"><span data-stu-id="fde70-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="fde70-175">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fde70-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="fde70-176">Uue väljastatud toote loomine</span><span class="sxs-lookup"><span data-stu-id="fde70-176">Create a new released product</span></span>

1. <span data-ttu-id="fde70-177">Määrake toote kolm koondandmete parameetrit, kasutades neid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="fde70-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="fde70-178">Valige väljal **Laoala dimensioonigrupp** suvand **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="fde70-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="fde70-179">Valige väljal  **Jälgimisdimensiooni grupp** suvand **Batch-Phy**.</span><span class="sxs-lookup"><span data-stu-id="fde70-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="fde70-180">Valige väljal **Reserveeringu hierarhia** suvand **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="fde70-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="fde70-181">Looge kaks partiinumbrit, nt **B11** ja **B22**.</span><span class="sxs-lookup"><span data-stu-id="fde70-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="fde70-182">Lisage kauba kogused laoseisu, kasutades järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="fde70-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="fde70-183">Ladu</span><span class="sxs-lookup"><span data-stu-id="fde70-183">Warehouse</span></span> | <span data-ttu-id="fde70-184">Partii number</span><span class="sxs-lookup"><span data-stu-id="fde70-184">Batch number</span></span> | <span data-ttu-id="fde70-185">Koht</span><span class="sxs-lookup"><span data-stu-id="fde70-185">Location</span></span> | <span data-ttu-id="fde70-186">Litsentsiplaat</span><span class="sxs-lookup"><span data-stu-id="fde70-186">License plate</span></span> | <span data-ttu-id="fde70-187">Kogus</span><span class="sxs-lookup"><span data-stu-id="fde70-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="fde70-188">24</span><span class="sxs-lookup"><span data-stu-id="fde70-188">24</span></span>        | <span data-ttu-id="fde70-189">B11</span><span class="sxs-lookup"><span data-stu-id="fde70-189">B11</span></span>          | <span data-ttu-id="fde70-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="fde70-190">BULK-001</span></span> | <span data-ttu-id="fde70-191">Puudub</span><span class="sxs-lookup"><span data-stu-id="fde70-191">None</span></span>          | <span data-ttu-id="fde70-192">10</span><span class="sxs-lookup"><span data-stu-id="fde70-192">10</span></span>       |
    | <span data-ttu-id="fde70-193">24</span><span class="sxs-lookup"><span data-stu-id="fde70-193">24</span></span>        | <span data-ttu-id="fde70-194">B11</span><span class="sxs-lookup"><span data-stu-id="fde70-194">B11</span></span>          | <span data-ttu-id="fde70-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="fde70-195">FL-001</span></span>   | <span data-ttu-id="fde70-196">LP11</span><span class="sxs-lookup"><span data-stu-id="fde70-196">LP11</span></span>          | <span data-ttu-id="fde70-197">10</span><span class="sxs-lookup"><span data-stu-id="fde70-197">10</span></span>       |
    | <span data-ttu-id="fde70-198">24</span><span class="sxs-lookup"><span data-stu-id="fde70-198">24</span></span>        | <span data-ttu-id="fde70-199">B22</span><span class="sxs-lookup"><span data-stu-id="fde70-199">B22</span></span>          | <span data-ttu-id="fde70-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="fde70-200">FL-002</span></span>   | <span data-ttu-id="fde70-201">LP22</span><span class="sxs-lookup"><span data-stu-id="fde70-201">LP22</span></span>          | <span data-ttu-id="fde70-202">10</span><span class="sxs-lookup"><span data-stu-id="fde70-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="fde70-203">Müügitellimuse üksikasjade sisestamine</span><span class="sxs-lookup"><span data-stu-id="fde70-203">Enter sales order details</span></span>

1. <span data-ttu-id="fde70-204">Avage **Müük ja turundus** \> **Müügitellimused** \> **Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="fde70-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="fde70-205">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fde70-205">Select **New**.</span></span>
3. <span data-ttu-id="fde70-206">Müügitellimuse päise väljale **Kliendi konto** sisestage **US-003**.</span><span class="sxs-lookup"><span data-stu-id="fde70-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="fde70-207">Lisage uue üksuse jaoks rida ja sisestage koguseks **10**.</span><span class="sxs-lookup"><span data-stu-id="fde70-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="fde70-208">Veenduge, et välja **Ladu** väärtuseks oleks määratud **24**.</span><span class="sxs-lookup"><span data-stu-id="fde70-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="fde70-209">Kiirkaardil **Müügitellimuse read** valige väärtus **Varud** ja seejärel jaotises **Haldamine** suvand **Partii reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="fde70-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="fde70-210">Leht **Partii reserveerimine** näitab tellimuse rea reserveerimiseks saadaolevate partiide loendit.</span><span class="sxs-lookup"><span data-stu-id="fde70-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="fde70-211">Selles näites näitab see kogust **20** partiinumbri **B11** ja kogust **10** partiinumbri **B22** jaoks.</span><span class="sxs-lookup"><span data-stu-id="fde70-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="fde70-212">Pange tähele, et lehele **Partii reserveerimine** ei pääse realt juurde, kui sellel real olev üksus on seotud väärtusega „partii-alla\[asukoht\]”, kui see pole seadistatud lubama partiiga seotud reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="fde70-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fde70-213">Kindla partii reserveerimiseks müügitellimusele tuleb kasutada lehte **Partii reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="fde70-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="fde70-214">Kui sisestate partii numbri otse müügitellimuse reale, käitub süsteem nii, nagu sisestasite kindla partii väärtuse üksusele, mille suhtes kehtib „partii-alla\[asukoht\]” reserveerimise poliitika.</span><span class="sxs-lookup"><span data-stu-id="fde70-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="fde70-215">Rea salvestamisel kuvatakse hoiatusteade.</span><span class="sxs-lookup"><span data-stu-id="fde70-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="fde70-216">Kui kinnitate, et partiinumber tuleb määrata otse tellimuse reale, ei käsitleta rida tavalise laohalduse loogikaga.</span><span class="sxs-lookup"><span data-stu-id="fde70-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="fde70-217">Kui reserveerite koguse lehelt **Reserveerimine**, ei reserveerita ühtegi kindlat partiid ja selle rea laotegevuse käitamine järgib reegleid, mis on rakendatavad „partii-alla\[asukoht\]” reserveerimise poliitika alusel.</span><span class="sxs-lookup"><span data-stu-id="fde70-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="fde70-218">See lehekülg töötab ja on seotud samal viisil, nagu see toimib ja on seotud üksuste puhul, millel on seostatud reserveerimise hierarhia tüübiga „partii-üle\[asukoha\]”.</span><span class="sxs-lookup"><span data-stu-id="fde70-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="fde70-219">Siiski kehtivad järgmised erandid.</span><span class="sxs-lookup"><span data-stu-id="fde70-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="fde70-220">Kiirkaart **Lähtereale määratud partiinumbrid** kuvab tellimuserea jaoks reserveeritud partiinumbrid.</span><span class="sxs-lookup"><span data-stu-id="fde70-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="fde70-221">Ruudustikus olevad partiiväärtused kuvatakse kogu tellimuserea täitmise tsüklis, sh laotöötluse etappides.</span><span class="sxs-lookup"><span data-stu-id="fde70-221">The batch values in the grid will be shown throughout the fulfilment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="fde70-222">Seevastu kiirkaart **Ülevaade**, korrapärase tellimuse rea reserveerimine (s.t reserveerimine, mida tehakse **Asukoha** taseme kohal olevate dimensioonide puhul), kuvatakse ruudustikus kuni laotöö loomiseni.</span><span class="sxs-lookup"><span data-stu-id="fde70-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="fde70-223">Tööüksus võtab seejärel rea reserveerimise üle ja rea reserveeringut ei kuvata enam leheküljel.</span><span class="sxs-lookup"><span data-stu-id="fde70-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="fde70-224">Kiirkaart **Lähtereale määratud partiinumbrid** aitab tagada, et müügitellimuse töötleja saab vaadata kliendi tellimusele määratud partiinumbreid mis tahes tööetapis kuni arveldamiseni.</span><span class="sxs-lookup"><span data-stu-id="fde70-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="fde70-225">Peale konkreetse partii reserveerimise saab kasutaja valida käsitsi partii kindla asukoha ja litsentsiplaadi, selle asemel et lasta süsteemil need automaatselt valida.</span><span class="sxs-lookup"><span data-stu-id="fde70-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="fde70-226">See võimalus on seotud tellimuse sooritatud partii reserveerimise mehhanismi kujundusega.</span><span class="sxs-lookup"><span data-stu-id="fde70-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="fde70-227">Nagu varem mainitud, tuleb selleks, et lubada kindla partii numbri reserveerimist üksuse puhul, mis on märgitud jaotises „partii-alla\[asukoht\]”, peab süsteem reserveerima kõik dimensioonid asukoha kaudu.</span><span class="sxs-lookup"><span data-stu-id="fde70-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="fde70-228">Seetõttu teeb lao töö samu ladustamise dimensioone, mis olid reserveeritud tellimustega töötavate kasutajate poolt, ja see ei pruugi alati kajastada kauba ladustamise paigutust, mis on mugav või isegi võimalik komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="fde70-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="fde70-229">Kui tellimuse töötlejad on lao piirangutest teadlikud, võivad nad partii reserveerimisel käsitsi valida kindlad asukohad ja litsentsiplaadid.</span><span class="sxs-lookup"><span data-stu-id="fde70-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="fde70-230">Sellisel juhul peab kasutaja kasutama lehekülje päises funktsiooni **Kuva dimensioonid** ja lisama asukoha ja litsentsiplaadi kiirkaardi **Ülevaade** ruudustikus.</span><span class="sxs-lookup"><span data-stu-id="fde70-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="fde70-231">Valige lehel **Partii reserveerimine** partii **B11** jaoks rida ja seejärel käsk **Reserveeri rida**.</span><span class="sxs-lookup"><span data-stu-id="fde70-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="fde70-232">Automaatsel reserveerimisel ei ole asukohtade ja litsentsiplaadi määramiseks loogikat määratud.</span><span class="sxs-lookup"><span data-stu-id="fde70-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="fde70-233">Koguse saate sisestada käsitsi väljale **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="fde70-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="fde70-234">Pange tähele, et kiirkaardi **Lähtereale määratud partiinumbrid** partii **B11** kuvatakse kui **Sooritatud**.</span><span class="sxs-lookup"><span data-stu-id="fde70-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Kindla partiinumbri määramine müügitellimuse reale partii reserveerimise lehel](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="fde70-236">Müügitellimuse rea koguse reserveerimist saab teha mitmel partiil.</span><span class="sxs-lookup"><span data-stu-id="fde70-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="fde70-237">Sama partii reserveerimist saab teha ka mitme asukoha ja litsentsiplaadi alusel (kui nende asukohtade puhul on lubatud litsentsiplaadid).</span><span class="sxs-lookup"><span data-stu-id="fde70-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="fde70-238">Kindla partii reserveerimine müügitellimuse real oleva koguse jaoks võib olla ka osaline.</span><span class="sxs-lookup"><span data-stu-id="fde70-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="fde70-239">Näiteks 100 ühiku kogukogust saab reserveerida nii, et kindel partii on pühendunud 20 ühikule, samas kui 80 ühikut on reserveeritud saidi ja lao tasemetele mis tahes saadaoleva partii jaoks.</span><span class="sxs-lookup"><span data-stu-id="fde70-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="fde70-240">Sel juhul kasutab WMS komplekteerimislehe töötlemisel kaht eraldiseisvat töörida.</span><span class="sxs-lookup"><span data-stu-id="fde70-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="fde70-241">Avage **Tooteteabe haldus** \> **Tooted** \> **Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="fde70-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="fde70-242">Valige üksus ja seejärel **Varude haldamine** \> **Kuva** \> **Kanded**.</span><span class="sxs-lookup"><span data-stu-id="fde70-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Tellimusega kooskõlastatud reserveerimine laokande tüübina](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="fde70-244">Vaadake üle kauba varude kanded, mis on seotud müügitellimuse rea reserveerimisega.</span><span class="sxs-lookup"><span data-stu-id="fde70-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="fde70-245">Kanne, mille välja **Viide** väärtuseks on seatud **Müügitellimus** ja välja **Väljaminek** väärtuseks on seatud **Reserveeritud füüsiline**, näitab tellimuse rea reserveerimist varude dimensioonide jaoks, mis on üle taseme **Asukoht**.</span><span class="sxs-lookup"><span data-stu-id="fde70-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="fde70-246">Kauba varude reserveerimise hierarhia kohaselt on need dimensioonid saidi, lao ja varude olek.</span><span class="sxs-lookup"><span data-stu-id="fde70-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="fde70-247">Kanne, mille välja **Viide** väärtuseks on seatud **Tellimuse tehtud reserveerimine** ja välja **Väljaminek** väärtuseks on seatud **Reserveeritud füüsiline**, näitab tellimuse rea reserveerimist kindlat partiid ja kõiki varude dimensioone üle selle.</span><span class="sxs-lookup"><span data-stu-id="fde70-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="fde70-248">Kauba varude reserveerimise hierarhia kohaselt on need dimensioonid partiinumber ja asukoht.</span><span class="sxs-lookup"><span data-stu-id="fde70-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="fde70-249">Selles näites on asukoht **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="fde70-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="fde70-250">Valige müügitellimuse päises suvandid **Ladu** \> **Tegevused** \> **Laost vabastamine**.</span><span class="sxs-lookup"><span data-stu-id="fde70-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="fde70-251">Tellimuse rida on nüüd moodustatud ja töö on loodud.</span><span class="sxs-lookup"><span data-stu-id="fde70-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="fde70-252">Tellitud partiinumbritega laotööde ülevaatamine ja töötlemine</span><span class="sxs-lookup"><span data-stu-id="fde70-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="fde70-253">Kiirkaardil **Müügitellimuse read** valige **Ladu**\>**Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="fde70-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="fde70-254">Tööl, mis tegeleb müügitellimuse reale pühendunud partii koguste komplekteerimisega, on järgmised omadused.</span><span class="sxs-lookup"><span data-stu-id="fde70-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="fde70-255">Töö loomiseks kasutab süsteem töömalle, kuid mitte asukoha direktiive.</span><span class="sxs-lookup"><span data-stu-id="fde70-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="fde70-256">Kõik töömallide jaoks määratletud kindlad sätted, nt maksimaalne komplekteerimise read või kindel mõõtühik, rakendatakse uute tööde loomisel määramiseks.</span><span class="sxs-lookup"><span data-stu-id="fde70-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="fde70-257">Siiski ei arvestata reegleid, mis on seotud asukoha direktiividega komplekteerimise asukohtade tuvastamiseks, kuna tellimusega kooskõlastatud reserveeringuga on juba määratud kõik varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="fde70-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="fde70-258">Need varude dimensioonid sisaldavad dimensioone lao ladustamise tasemel.</span><span class="sxs-lookup"><span data-stu-id="fde70-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="fde70-259">Seetõttu pärib töö need dimensioonid, ilma et peaksite konsulteerima asukoha direktiividega.</span><span class="sxs-lookup"><span data-stu-id="fde70-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="fde70-260">Partiinumbrit ei kuvata komplekteerimise real (nagu näiteks töörea puhul, mis luuakse kaubale, millel on seostatud „partii-üle\[-asukoht\]” reserveerimise hierarhia). Selle asemel kuvatakse seotud laokannete põhjal viidatud töökandes partiinumber ja kõik muud varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="fde70-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Tellimusega kooskõlastatud reserveeringust pärinev lao laokande töö](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="fde70-262">Kui töö on loodud, eemaldatakse välja **Viide** väärtusega **Tellimusele kooskõlastatud reserveerimine** kauba laokanne.</span><span class="sxs-lookup"><span data-stu-id="fde70-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="fde70-263">Laokannete puhul, mille välja **Viide** väärtuseks on seatud **Töö**, on nüüd füüsiline reserveerimine määratud kõigi koguse varude dimensioonide jaoks.</span><span class="sxs-lookup"><span data-stu-id="fde70-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="fde70-264">Laotoimingud võivad jätkata töö töötlemist tavalisel viisil.</span><span class="sxs-lookup"><span data-stu-id="fde70-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="fde70-265">Kuid mobiilseade juhendab töötajat valima kindlat partiinumbrit.</span><span class="sxs-lookup"><span data-stu-id="fde70-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="fde70-266">Lao keskkondades, kus asukohti kontrollitakse litsentsiplaadiga pärast seda, kui töötaja jõuab asukohani, mis talletab sama partii mitmele litsentsiplaadile, saab ta valida mis tahes litsentsiplaadi, mis pole veel reserveeritud (nt teine tellimusega kooskõlastatud reserveering või töö, mis pärineb seda tüüpi reserveeringust.)</span><span class="sxs-lookup"><span data-stu-id="fde70-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="fde70-267">Kui tööreal määratud asukohast komplekteerimine osutub ebaotstarbekaks, saavad laooperaatorid kasutada üht järgmistest toimingutest, et suunata kindla partii komplekteerimine mugavamasse asukohta.</span><span class="sxs-lookup"><span data-stu-id="fde70-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="fde70-268">Mobiilseadme tavatoiming **Asukoha alistamine** (eeldusel, et lao töötaja säte **Luba valitud asukoha alistamine** on lubatud)</span><span class="sxs-lookup"><span data-stu-id="fde70-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="fde70-269">Toiming **Muuda asukohta** lehel **Tööloendi üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="fde70-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="fde70-270">Lõpetage mobiilseadmes komplekteerimine ja töö sisestamine.</span><span class="sxs-lookup"><span data-stu-id="fde70-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="fde70-271">Kogus **10** on nüüd partiinumbri **B11** jaoks müügireale komplekteeritud ja asukohta **Baydoor** pandud.</span><span class="sxs-lookup"><span data-stu-id="fde70-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="fde70-272">Sel hetkel on see veokile laadimiseks ja kliendi aadressile lähetamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="fde70-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a><span data-ttu-id="fde70-273">Tellitud ja kooskõlastatud partiinumbritega laotööde ülevaatamise ja töötlemise erandid</span><span class="sxs-lookup"><span data-stu-id="fde70-273">Exception handling of warehouse work thas has order-committed batch numbers</span></span>

<span data-ttu-id="fde70-274">Laotöö komplekteerimiseks tellitud partii numbrite suhtes kehtivad samad standardse lao erandi käsitlemise protsessid ja toimingud, mis tavatöö puhul.</span><span class="sxs-lookup"><span data-stu-id="fde70-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="fde70-275">Üldiselt saab avatud töö või töörea tühistada ja katkestada, kui kasutaja asukoht on täis, see võib olla lühike-komplekteeritud ja seda saab liikumise tõttu uuendada.</span><span class="sxs-lookup"><span data-stu-id="fde70-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="fde70-276">Samuti saab vähendada juba lõpetatud töö komplekteeritud kogust või seda tööd muuta.</span><span class="sxs-lookup"><span data-stu-id="fde70-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="fde70-277">Järgmist põhireeglit rakendatakse kõigile nende erandite käsitlemise toimingutele: kliendile reserveeritud partiinumbrit ei saa kunagi asendada teise partii numbriga, kuid selle ladustamise dimensioone (asukoht ja litsentsiplaat) saab muuta, selleks peab kasutaja seda käsitsi värskendama või süsteem automaatselt uuendama.</span><span class="sxs-lookup"><span data-stu-id="fde70-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="fde70-278">Automaatne värskendamine põhineb samadel juhusliku määramisega ladustamise dimensioonidel, mida rakendatakse, kui kindel partii on automaatselt reserveeritud, kuid ladustamise dimensioone ei määratud.</span><span class="sxs-lookup"><span data-stu-id="fde70-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="fde70-279">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="fde70-279">Example scenario</span></span>

<span data-ttu-id="fde70-280">Selle stsenaariumi näide on olukord, kus varem lõpetatud töö on funktsiooni **Vähenda komplekteeritud kogust** kasutamisel komplekteerimata.</span><span class="sxs-lookup"><span data-stu-id="fde70-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="fde70-281">See näide jätkab selle teema eelmist näidet.</span><span class="sxs-lookup"><span data-stu-id="fde70-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="fde70-282">Avage **Laohaldus** \> **Koormad** \> **Aktiivsed koormad**.</span><span class="sxs-lookup"><span data-stu-id="fde70-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="fde70-283">Valige koorem, mis loodi seoses teie müügitellimuse saadetisega.</span><span class="sxs-lookup"><span data-stu-id="fde70-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="fde70-284">Kiirkaardilt **Koorma tellimuse read** valige käsk **Vähenda komplekteeritud kogust**.</span><span class="sxs-lookup"><span data-stu-id="fde70-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="fde70-285">Valige lehel **Vähenda komplekteeritud kogust** välja **Teisalda asukohta** väärtuseks **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="fde70-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="fde70-286">Väljal **Teisalda litsentsiplaadile** valige väärtus **LP33**.</span><span class="sxs-lookup"><span data-stu-id="fde70-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="fde70-287">Sisestage ruudustiku väljale **Varude kogus väljale komplekteerimata** väärtus **10**.</span><span class="sxs-lookup"><span data-stu-id="fde70-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="fde70-288">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="fde70-288">Select **OK**.</span></span>

<span data-ttu-id="fde70-289">Siin on komplekteerimise tegevuse tulemused.</span><span class="sxs-lookup"><span data-stu-id="fde70-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="fde70-290">Varem suletud töö olek on seatud väärtusele **Tühistatud**.</span><span class="sxs-lookup"><span data-stu-id="fde70-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="fde70-291">Tüübi **Varude liikumine** uus töö luuakse komplekteerimata kogusega **10** partiinumbri**B11** jaoks.</span><span class="sxs-lookup"><span data-stu-id="fde70-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="fde70-292">See töö näitab liikumist asukohast **Baydoor** litsentsiplaadile **LP33** asukohas **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="fde70-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="fde70-293">Olek on seatud väärtusele **Suletud**.</span><span class="sxs-lookup"><span data-stu-id="fde70-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="fde70-294">Süsteem reserveerib algselt tellitud partiinumbri uuesti ja määrab asukoha ja litsentsiplaadi ID-d.</span><span class="sxs-lookup"><span data-stu-id="fde70-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="fde70-295">(See protsess on samaväärne funktsiooni **Reserveeri rida** käitamisega antud partiinumbri puhul).</span><span class="sxs-lookup"><span data-stu-id="fde70-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="fde70-296">Selle tulemusel näidatakse partii **B11** määratuna kiirkaardi **Lähtereale kinnitatud partiinumbrid** lehele **Partii reserveerimine** ja väli **Reserveerimine** sisaldab kogust **10** partiinumbri **B11** jaoks.</span><span class="sxs-lookup"><span data-stu-id="fde70-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="fde70-297">Lisaks on välja **Asukoht** väärtuseks **FL-001** ja välja **Litsentsiplaat** väärtuseks on seatud **LP11**.</span><span class="sxs-lookup"><span data-stu-id="fde70-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="fde70-298">(Kui neid ei ole näha, saate need väljad ruudustikku lisada.)</span><span class="sxs-lookup"><span data-stu-id="fde70-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="fde70-299">Järgmised tabelid annavad ülevaate sellest, kuidas süsteem käsitleb kindla lao tegevuste tellimusega kooskõlastatud partii reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="fde70-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="fde70-300">Tabelite sisu tõlgendamiseks oletame, et iga laotoiming käivitatakse tellimusega seotud partii reserveerimisest tuleneva olemasoleva laotöö kontekstis või et iga laotoimingu käivitamine mõjutab seda tüüpi tööd.</span><span class="sxs-lookup"><span data-stu-id="fde70-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="fde70-301">Neis tabelites näitab veerg Partii kogus on saadaval, kas partii kogus on saadaval lisaks kogusele, mis on juba reserveeritud praeguse tellimusega seotud reserveeringutele, või on juba reserveeritud laotööst, mis pärineb selle tüübi reserveeringutest.</span><span class="sxs-lookup"><span data-stu-id="fde70-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="fde70-302">Avatud tööde komplekteerimise asukoha alistamine</span><span class="sxs-lookup"><span data-stu-id="fde70-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fde70-303">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="fde70-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="fde70-304">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="fde70-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="fde70-305">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="fde70-305">Key user steps</span></span></th>
<th><span data-ttu-id="fde70-306">Laotöö</span><span class="sxs-lookup"><span data-stu-id="fde70-306">Warehouse work</span></span></th>
<th><span data-ttu-id="fde70-307">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="fde70-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="fde70-308">Suvand <strong>Luba komplekteerimise asukoha alistamine</strong> on töötajale lubatud.</span><span class="sxs-lookup"><span data-stu-id="fde70-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="fde70-309">Jah</span><span class="sxs-lookup"><span data-stu-id="fde70-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-310">Valige suvand <strong>Alista asukoht</strong> lao mobiilirakenduses (WMA), kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="fde70-310">Select the <strong>Override location</strong> menu item on the Warehouse Mmobile App (WMA) when you start picking work.</span></span></li>
<li><span data-ttu-id="fde70-311">Valige <strong>Soovita</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="fde70-312">Kinnitage uus asukoht, mis on soovitatud partii koguse kättesaadavuse alusel.</span><span class="sxs-lookup"><span data-stu-id="fde70-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="fde70-313">Praeguse töö puhul toimuvad järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="fde70-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="fde70-314">Komplekteerimise real olev asukoht uuendatakse uude asukohta.</span><span class="sxs-lookup"><span data-stu-id="fde70-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="fde70-315">(Kui asukoha määrab litsentsiplaat, on töölao kandele määratud juhuslik litsentsiplaat ja töötaja saab valida mis tahes saadaoleva kogusega litsentsiplaadi.)</span><span class="sxs-lookup"><span data-stu-id="fde70-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="fde70-316">Kui kogus leitakse uues asukohas rohkem kui ühel litsentsiplaadil, jaotatakse algse komplekteerimise rida mitmeks reaks, et see vastaks igale litsentsiplaadile.</span><span class="sxs-lookup"><span data-stu-id="fde70-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="fde70-317">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="fde70-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-318">Ei</span><span class="sxs-lookup"><span data-stu-id="fde70-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-319">Valige suvand <strong>Alista asukoht</strong> lao mobiilirakenduses (WMA), kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="fde70-319">Select the <strong>Override location</strong> menu item on the WMA when you start picking work.</span></span></li>
<li><span data-ttu-id="fde70-320">Sisestage asukoht käsitsi.</span><span class="sxs-lookup"><span data-stu-id="fde70-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="fde70-321">Toiming <strong>Asukoha alistamine</strong> pole võimalik.</span><span class="sxs-lookup"><span data-stu-id="fde70-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="fde70-322">See nurjub ja kuvatakse tõrge.</span><span class="sxs-lookup"><span data-stu-id="fde70-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="fde70-323">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="fde70-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="fde70-324">Nupp Täis – jaotab töörea kasutaja asukoha ületäitumise tõttu</span><span class="sxs-lookup"><span data-stu-id="fde70-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fde70-325">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="fde70-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="fde70-326">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="fde70-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="fde70-327">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="fde70-327">Key user steps</span></span></th>
<th><span data-ttu-id="fde70-328">Laotöö</span><span class="sxs-lookup"><span data-stu-id="fde70-328">Warehouse work</span></span></th>
<th><span data-ttu-id="fde70-329">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="fde70-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fde70-330">Valik <strong>Luba töö jaotamine</strong> on lubatud mobiilseadme menüükäsul.</span><span class="sxs-lookup"><span data-stu-id="fde70-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="fde70-331">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="fde70-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-332">Valige lao mobiilirakenduses (WMA) menüüsuvand <strong>Täis</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="fde70-332">Select the <strong>Full</strong> menu item on the WMA when you process picking work.</span></span></li>
<li><span data-ttu-id="fde70-333">Sisestage väljale <strong>Komplekteeri kogus</strong> nõutava komplekteerimise osaline kogus, et näidata kogu võimsust.</span><span class="sxs-lookup"><span data-stu-id="fde70-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="fde70-334">Praeguse töö puhul uuendatakse kogus järelejäänud kogusele, mis tuleb komplekteerida.</span><span class="sxs-lookup"><span data-stu-id="fde70-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="fde70-335">Komplekteeritud koguse uus töö luuakse ja suletakse.</span><span class="sxs-lookup"><span data-stu-id="fde70-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="fde70-336">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="fde70-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="fde70-337">Lõpetatud töö komplekteeritud koguse vähendamine (koormast)</span><span class="sxs-lookup"><span data-stu-id="fde70-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fde70-338">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="fde70-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="fde70-339">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="fde70-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="fde70-340">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="fde70-340">Key user steps</span></span></th>
<th><span data-ttu-id="fde70-341">Laotöö</span><span class="sxs-lookup"><span data-stu-id="fde70-341">Warehouse work</span></span></th>
<th><span data-ttu-id="fde70-342">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="fde70-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="fde70-343">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="fde70-343">Not applicable</span></span></td>
<td><span data-ttu-id="fde70-344">Jah</span><span class="sxs-lookup"><span data-stu-id="fde70-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-345">Avage koorma realt leht <strong>Komplekteeritud koguse vähendamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="fde70-346">Sisestage kogu kogus, mis ei lähe komplekteerimisele.</span><span class="sxs-lookup"><span data-stu-id="fde70-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="fde70-347">Valige teisaldamiseks asukoht/litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="fde70-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="fde70-348">Koorma reaga seotud töö on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="fde70-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="fde70-349">Varude teisaldamiseks luuakse uus töö ja suletakse.</span><span class="sxs-lookup"><span data-stu-id="fde70-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="fde70-350">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="fde70-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="fde70-351">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="fde70-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-352">Ei</span><span class="sxs-lookup"><span data-stu-id="fde70-352">No</span></span></td>
<td><span data-ttu-id="fde70-353">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="fde70-353">See the previous row.</span></span></td>
<td><span data-ttu-id="fde70-354">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="fde70-354">See the previous row.</span></span></td>
<td><span data-ttu-id="fde70-355">Kogus reserveeritakse samale partiile samas asukohas ja litsentsiplaadiga (kui asukoht on litsentsiplaadi kontrollitud), mis sisestati komplekteerimise ajal.</span><span class="sxs-lookup"><span data-stu-id="fde70-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="fde70-356">Kauba teisaldamine laos</span><span class="sxs-lookup"><span data-stu-id="fde70-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="fde70-357">See laotoiming rakendub ainult tüübi **Töö loomise protsess** teisaldamistele, mitte malli alusel teisaldamistele.</span><span class="sxs-lookup"><span data-stu-id="fde70-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fde70-358">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="fde70-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="fde70-359">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="fde70-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="fde70-360">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="fde70-360">Key user steps</span></span></th>
<th><span data-ttu-id="fde70-361">Laotöö</span><span class="sxs-lookup"><span data-stu-id="fde70-361">Warehouse work</span></span></th>
<th><span data-ttu-id="fde70-362">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="fde70-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="fde70-363">Töötaja saab <strong>lubada seotud töö varude teisaldamist</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="fde70-364">Jah</span><span class="sxs-lookup"><span data-stu-id="fde70-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-365">Alustage teisaldamist WMA-ga.</span><span class="sxs-lookup"><span data-stu-id="fde70-365">Start a movement on the WMA.</span></span></li>
<li><span data-ttu-id="fde70-366">Sisestage alg- ja lõppasukohad.</span><span class="sxs-lookup"><span data-stu-id="fde70-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="fde70-367">Kõigi olemasolevate tööde puhul, mida teisaldamine mõjutab, uuendatakse komplekteerimise asukoht uude asukohta.</span><span class="sxs-lookup"><span data-stu-id="fde70-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="fde70-368">Varude teisaldamiseks luuakse uus töö ja suletakse.</span><span class="sxs-lookup"><span data-stu-id="fde70-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="fde70-369">Kõik olemasolevad reserveeringud, mis mõjutavad koguse liikumist antud asukohast, reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="fde70-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="fde70-370">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="fde70-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-371">Ei</span><span class="sxs-lookup"><span data-stu-id="fde70-371">No</span></span></td>
<td><span data-ttu-id="fde70-372">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="fde70-372">See the previous row.</span></span></td>
<td><span data-ttu-id="fde70-373">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="fde70-373">See the previous row.</span></span></td>
<td><span data-ttu-id="fde70-374">Kõik olemasolevad reserveeringud, mis mõjutavad koguse liikumist antud asukohast, reserveeritakse uuesti sama partii ja uue asukoha ning litsentsiplaadi jaoks (kui asukoht on litsentsiplaadi kontrollitud).</span><span class="sxs-lookup"><span data-stu-id="fde70-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="fde70-375">Lõpetatud töö komplekteeritud koguse vähendamine (koormast või voost)</span><span class="sxs-lookup"><span data-stu-id="fde70-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fde70-376">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="fde70-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="fde70-377">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="fde70-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="fde70-378">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="fde70-378">Key user steps</span></span></th>
<th><span data-ttu-id="fde70-379">Laotöö</span><span class="sxs-lookup"><span data-stu-id="fde70-379">Warehouse work</span></span></th>
<th><span data-ttu-id="fde70-380">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="fde70-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="fde70-381">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="fde70-381">Not applicable</span></span></td>
<td><span data-ttu-id="fde70-382">Jah</span><span class="sxs-lookup"><span data-stu-id="fde70-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-383">Avage leht <strong>Tühistatud töö</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="fde70-384">Taotlemise lehel märkige ruut <strong>Jäta kaubad praegusesse asukohta</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="fde70-385">Koorma reaga seotud kõik tööd on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="fde70-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="fde70-386">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="fde70-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="fde70-387">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="fde70-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-388">Ei</span><span class="sxs-lookup"><span data-stu-id="fde70-388">No</span></span></td>
<td><span data-ttu-id="fde70-389">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="fde70-389">See the previous row.</span></span></td>
<td><span data-ttu-id="fde70-390">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="fde70-390">See the previous row.</span></span></td>
<td><span data-ttu-id="fde70-391">Kogus reserveeritakse samale partiile ja asukohale ning litsentsiplaadile, kuhu kogus tühistamisel jäeti.</span><span class="sxs-lookup"><span data-stu-id="fde70-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-392">Jah</span><span class="sxs-lookup"><span data-stu-id="fde70-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-393">Avage leht <strong>Tühistatud töö</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="fde70-394">Taotlemise lehel märkige ruut <strong>Määra kaubad sellesse asukohta</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="fde70-395">Praegune töö on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="fde70-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="fde70-396">Varude teisaldamiseks luuakse uus töö ja suletakse.</span><span class="sxs-lookup"><span data-stu-id="fde70-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="fde70-397">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="fde70-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="fde70-398">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="fde70-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-399">Ei</span><span class="sxs-lookup"><span data-stu-id="fde70-399">No</span></span></td>
<td><span data-ttu-id="fde70-400">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="fde70-400">See the previous row.</span></span></td>
<td><span data-ttu-id="fde70-401">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="fde70-401">See the previous row.</span></span></td>
<td><span data-ttu-id="fde70-402">Kogus reserveeritakse samale partiile ja asukohale ning litsentsiplaadile, kuhu kogus tühistamisel määrati.</span><span class="sxs-lookup"><span data-stu-id="fde70-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-403">Jah/ei</span><span class="sxs-lookup"><span data-stu-id="fde70-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-404">Avage leht <strong>Tühistatud töö</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="fde70-405">Taotlemise lehel märkige ruut <strong>Teisalda kaubad sellesse asukohta</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="fde70-406">Tühistamist ei toetata.</span><span class="sxs-lookup"><span data-stu-id="fde70-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="fde70-407">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="fde70-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-408">Jah/ei</span><span class="sxs-lookup"><span data-stu-id="fde70-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-409">Avage leht <strong>Tühistatud töö</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="fde70-410">Taotlemise lehel märkige ruut <strong>Teisalda kaubad asukoha direktiivi kohaselt</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="fde70-411">Tühistamist ei toetata.</span><span class="sxs-lookup"><span data-stu-id="fde70-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="fde70-412">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="fde70-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="fde70-413">Koguse lühiajaline komplekteerimine – registreerige kogus komplekteerimise ajal asukohas/litsentsiplaadil kui füüsiliselt leidmata.</span><span class="sxs-lookup"><span data-stu-id="fde70-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fde70-414">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="fde70-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="fde70-415">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="fde70-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="fde70-416">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="fde70-416">Key user steps</span></span></th>
<th><span data-ttu-id="fde70-417">Laotöö</span><span class="sxs-lookup"><span data-stu-id="fde70-417">Warehouse work</span></span></th>
<th><span data-ttu-id="fde70-418">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="fde70-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="fde70-419">Töö erandi tüübiks on seadistatud<strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>puudub</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="fde70-420">Jah</span><span class="sxs-lookup"><span data-stu-id="fde70-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-421">Valige lao mobiilirakenduses (WMA) menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="fde70-421">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="fde70-422">Sisestage väljale <strong>Komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="fde70-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="fde70-423">Väljale <strong>Põhjus</strong> sisestage väärtus <strong>Ümberjaotamine puudub</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="fde70-424">Praegune töö on suletud ja komplekteeritud kogus on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fde70-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="fde70-425">Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</span><span class="sxs-lookup"><span data-stu-id="fde70-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="fde70-426">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="fde70-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="fde70-427">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="fde70-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-428">Ei</span><span class="sxs-lookup"><span data-stu-id="fde70-428">No</span></span></td>
<td><span data-ttu-id="fde70-429">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="fde70-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="fde70-430">Lühikese komplekteerimise toiming nurjub ja kuvatakse tõrge.</span><span class="sxs-lookup"><span data-stu-id="fde70-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="fde70-431">Praegune töö jääb avatuks.</span><span class="sxs-lookup"><span data-stu-id="fde70-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="fde70-432">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="fde70-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="fde70-433">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Puudub</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="fde70-434">Jah</span><span class="sxs-lookup"><span data-stu-id="fde70-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-435">Valige lao mobiilirakenduses (WMA) menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="fde70-435">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="fde70-436">Sisestage väljale <strong>Komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="fde70-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="fde70-437">Väljale <strong>Põhjus</strong> sisestage väärtus <strong>Ümberjaotamine puudub</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="fde70-438">Praegune töö on suletud ja komplekteeritud kogus on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fde70-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="fde70-439">Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</span><span class="sxs-lookup"><span data-stu-id="fde70-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="fde70-440">Kõik olemasolevad reserveeringud, mis mõjutavad koguse kohandamist lühikese komplekteerimise asukohast, reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="fde70-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="fde70-441">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="fde70-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-442">Ei</span><span class="sxs-lookup"><span data-stu-id="fde70-442">No</span></span></td>
<td><span data-ttu-id="fde70-443">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="fde70-443">See the previous row.</span></span></td>
<td><span data-ttu-id="fde70-444">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="fde70-444">See the previous row.</span></span></td>
<td><span data-ttu-id="fde70-445">Kõik olemasolevad reserveeringud, mis mõjutavad koguse kohandamist lühikese komplekteerimise asukohast, eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="fde70-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-446">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Käsitsi</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah/ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="fde70-447">Lisaks saavad töötajad kasutada suvandit <strong>Luba kauba käsitsi ümberjaotamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="fde70-448">Jah</span><span class="sxs-lookup"><span data-stu-id="fde70-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-449">Valige lao mobiilirakenduses (WMA) menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="fde70-449">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="fde70-450">Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="fde70-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="fde70-451">Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos käsitsi ümberjaotamisega</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="fde70-452">Valige loendist asukoht/litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="fde70-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="fde70-453">Praeguse töö puhul toimuvad järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="fde70-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="fde70-454">Praegune komplekteerimise rida on suletud ja komplekteeritud kogus on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fde70-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="fde70-455">Asetusrida on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="fde70-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="fde70-456">Luuakse uus komplekteerimise rida.</span><span class="sxs-lookup"><span data-stu-id="fde70-456">A new pick line is created.</span></span> <span data-ttu-id="fde70-457">See kasutab kasutaja valitud asukohta/litsentsiplaati.</span><span class="sxs-lookup"><span data-stu-id="fde70-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="fde70-458">Luuakse uus asetusrida.</span><span class="sxs-lookup"><span data-stu-id="fde70-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="fde70-459">Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</span><span class="sxs-lookup"><span data-stu-id="fde70-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="fde70-460">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="fde70-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-461">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Käsitsi</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="fde70-462">Lisaks saavad töötajad kasutada suvandit <strong>Luba kauba käsitsi ümberjaotamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="fde70-463">Ei</span><span class="sxs-lookup"><span data-stu-id="fde70-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-464">Valige lao mobiilirakenduses (WMA) menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="fde70-464">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="fde70-465">Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="fde70-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="fde70-466">Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos käsitsi ümberjaotamisega</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="fde70-467">Lühikese komplekteerimise toiming nurjub ja kuvatakse tõrge.</span><span class="sxs-lookup"><span data-stu-id="fde70-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="fde70-468">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="fde70-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-469">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Käsitsi</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="fde70-470">Lisaks saavad töötajad kasutada suvandit <strong>Luba kauba käsitsi ümberjaotamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="fde70-471">Ei</span><span class="sxs-lookup"><span data-stu-id="fde70-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-472">Valige lao mobiilirakenduses (WMA) menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="fde70-472">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="fde70-473">Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="fde70-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="fde70-474">Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos käsitsi ümberjaotamisega</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="fde70-475">Valige loendist asukoht/litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="fde70-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="fde70-476">Praeguse töö puhul toimuvad järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="fde70-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="fde70-477">Praegune komplekteerimise rida on suletud ja komplekteeritud kogus on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fde70-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="fde70-478">Asetusrida on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="fde70-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="fde70-479">Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</span><span class="sxs-lookup"><span data-stu-id="fde70-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="fde70-480">Kõik olemasolevad reserveeringud, mis mõjutavad koguse kohandamist lühikese komplekteerimise asukohast/litsentsiplaadilt, eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="fde70-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-481">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Automaatne</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah/ei</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah/ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="fde70-482">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="fde70-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-483">Valige lao mobiilirakenduses (WMA) menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="fde70-483">Select the <strong>Shortpick</strong> menu item on the WMA when you run picking work.</span></span></li>
<li><span data-ttu-id="fde70-484">Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="fde70-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="fde70-485">Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos automaatse ümberjaotamisega</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="fde70-486">Lühiajalist komplekteerimist, mis hõlmab automaatset ümberjaotamist, ei toetata.</span><span class="sxs-lookup"><span data-stu-id="fde70-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="fde70-487">Lühiajalist komplekteerimist, mis hõlmab automaatset ümberjaotamist, ei toetata.</span><span class="sxs-lookup"><span data-stu-id="fde70-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="fde70-488">Muuda varude olekut</span><span class="sxs-lookup"><span data-stu-id="fde70-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="fde70-489">Seda laotoimingut saab sooritada mitmest kirjest.</span><span class="sxs-lookup"><span data-stu-id="fde70-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="fde70-490">Siin kuvatud näites kasutatakse toimingut **Varude oleku muutmine** lehe **Vaba asukoht** alusel.</span><span class="sxs-lookup"><span data-stu-id="fde70-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="fde70-491">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="fde70-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="fde70-492">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="fde70-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="fde70-493">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="fde70-493">Key user steps</span></span></th>
<th><span data-ttu-id="fde70-494">Laotöö</span><span class="sxs-lookup"><span data-stu-id="fde70-494">Warehouse work</span></span></th>
<th><span data-ttu-id="fde70-495">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="fde70-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="fde70-496">Vahekaardil <strong>Ladu</strong>, kirjes <strong>Ladu</strong> on välja <strong>Eemalda reserveeringud ja märgised</strong> väärtuseks määratud <strong>Reserveeringud</strong> või <strong>Märgistused ja reserveeringud</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="fde70-497">Jah</span><span class="sxs-lookup"><span data-stu-id="fde70-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-498">Valige kindel asukoht.</span><span class="sxs-lookup"><span data-stu-id="fde70-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="fde70-499">Valige rida, millel on kindel kaup, asukoht ja litsentsiplaat (kui asukoht on litsentsiplaadi kontrollitud).</span><span class="sxs-lookup"><span data-stu-id="fde70-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="fde70-500">Valige <strong>Varude oleku muutmine</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="fde70-501">Seadke välja <strong>Varude olek</strong> väärtuseks <strong>Blokeerimine</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="fde70-502">Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="fde70-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="fde70-503">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="fde70-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="fde70-504">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="fde70-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="fde70-505">Tüübi <strong>Varude oleku muutmine</strong> kaks laokannet luuakse selleks, et tähistada varude oleku dimensiooni muutumist.</span><span class="sxs-lookup"><span data-stu-id="fde70-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="fde70-506">Tüübi <strong>Varude blokeerimine</strong> ja probleemitüübi <strong>Reserveeritud füüsiline</strong> luuakse selleks, et tähistada blokeeritud koguse reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="fde70-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="fde70-507">Ei</span><span class="sxs-lookup"><span data-stu-id="fde70-507">No</span></span></td>
<td><span data-ttu-id="fde70-508">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="fde70-508">See the previous row.</span></span></td>
<td><span data-ttu-id="fde70-509">Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="fde70-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="fde70-510">Reserveering eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="fde70-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="fde70-511">Tüübi <strong>Varude oleku muutmine</strong> kaks laokannet luuakse selleks, et tähistada varude oleku dimensiooni muutumist.</span><span class="sxs-lookup"><span data-stu-id="fde70-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="fde70-512">Tüübi <strong>Varude blokeerimine</strong> ja probleemitüübi <strong>Reserveeritud füüsiline</strong> luuakse selleks, et tähistada blokeeritud koguse reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="fde70-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="fde70-513">Vahekaardil <strong>Ladu</strong>, kirjes <strong>Ladu</strong> on välja <strong>Eemalda reserveeringud ja märgised</strong> väärtuseks määratud <strong>Puudub</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="fde70-514">Jah</span><span class="sxs-lookup"><span data-stu-id="fde70-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="fde70-515">Valige kindel asukoht.</span><span class="sxs-lookup"><span data-stu-id="fde70-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="fde70-516">Valige rida, millel on kindel kaup, asukoht ja litsentsiplaat (kui asukoht on litsentsiplaadi kontrollitud).</span><span class="sxs-lookup"><span data-stu-id="fde70-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="fde70-517">Valige <strong>Varude oleku muutmine</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="fde70-518">Seadke välja <strong>Varude olek</strong> väärtuseks <strong>Blokeerimine</strong>.</span><span class="sxs-lookup"><span data-stu-id="fde70-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="fde70-519">Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="fde70-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="fde70-520">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="fde70-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="fde70-521">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="fde70-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="fde70-522">Ei</span><span class="sxs-lookup"><span data-stu-id="fde70-522">No</span></span></td>
<td><span data-ttu-id="fde70-523">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="fde70-523">See the previous row.</span></span></td>
<td><span data-ttu-id="fde70-524">Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="fde70-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="fde70-525">Varude oleku muudatused pole lubatud.</span><span class="sxs-lookup"><span data-stu-id="fde70-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="fde70-526">Kitsendused</span><span class="sxs-lookup"><span data-stu-id="fde70-526">Limitations</span></span>

- <span data-ttu-id="fde70-527">Paindliku lao taseme dimensiooni reserveerimise funktsionaalsus ei toeta järgmisi funktsioone.</span><span class="sxs-lookup"><span data-stu-id="fde70-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="fde70-528">Tegeliku kaalu haldus</span><span class="sxs-lookup"><span data-stu-id="fde70-528">Catch weight management</span></span>
    - <span data-ttu-id="fde70-529">Füüsiline negatiivne laovaru</span><span class="sxs-lookup"><span data-stu-id="fde70-529">Physical negative inventory</span></span>
    - <span data-ttu-id="fde70-530">Tellitud tarnete reserveerimine</span><span class="sxs-lookup"><span data-stu-id="fde70-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="fde70-531">Üleviimistellimuste ja toormaterjalide komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="fde70-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="fde70-532">Konteineri konsolideerimise reeglil on direktiivi ühiku alusel pakkimisel piirangud.</span><span class="sxs-lookup"><span data-stu-id="fde70-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="fde70-533">Tellimusega kooskõlastatud reserveeringute puhul on soovitatav mitte kasutada konteineri loomise malle, mille puhul väli **Pakk direktiiviühiku järgi** on lubatud.</span><span class="sxs-lookup"><span data-stu-id="fde70-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="fde70-534">Praeguses kujunduses ei kasutata asukoha direktiive laotöö loomisel.</span><span class="sxs-lookup"><span data-stu-id="fde70-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="fde70-535">Seetõttu rakendatakse konteinerite voo etapis ainult madalaimat ühikut ühikute seeriagrupis (laoühikutes).</span><span class="sxs-lookup"><span data-stu-id="fde70-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
