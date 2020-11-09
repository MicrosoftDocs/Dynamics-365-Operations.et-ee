---
title: Paindliku laotaseme dimensiooni reserveerimise poliitika
description: See teema kirjeldab varude reserveerimise poliitikat, mis võimaldab partiijälgimisega tooteid müüvatel ettevõtetel käitada nende logistikat, nagu WMS-i toega toimingud, kindlatel partiidel kliendi müügitellimuste jaoks. Seda ka siis, kui tootega seostatud reserveerimise hierarhia ei luba kindlaid partiisid reserveerida.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy, WHSWorkTrans, WHSWorkInventTrans, WHSInventTableReservationHierarchy, WHSReservationHierarchyCreate, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b9bd4e67ed64218f9c4ac87bd143f73680af9ac4
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017640"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="92563-103">Paindliku laotaseme dimensiooni reserveerimise poliitika</span><span class="sxs-lookup"><span data-stu-id="92563-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92563-104">Kui varude reserveerimise hierarhia tüüp „partii-alla\[asukoha\]” on seotud toodetega, siis ei saa ettevõtted, mis müüvad partiijälgimisega tooteid ja käitavad nende logistikat, mis on lubatud Microsoft Dynamics 365 laohaldusesüsteemi (WMS) jaoks, reserveerida nende toodete kindlaid partiisid kliendi müügitellimustele.</span><span class="sxs-lookup"><span data-stu-id="92563-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="92563-105">Sarnaselt ei saa kindlaid litsentsiplaate reserveerida müügitellimustes olevate toodete jaoks, kui need tooted on seotud reserveerimise vaikehierarhiaga.</span><span class="sxs-lookup"><span data-stu-id="92563-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="92563-106">Selles teemas kirjeldatakse varude reserveerimise poliitikat, mis võimaldab nendel ettevõtetel kindlaid partiisid või litsentsiplaate reserveerida isegi siis, kui tooted on seotud reserveerimise hierarhia üksusega „partii-alla\[asukoht\]”.</span><span class="sxs-lookup"><span data-stu-id="92563-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="92563-107">Varude reserveerimise hierarhia</span><span class="sxs-lookup"><span data-stu-id="92563-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="92563-108">See jaotis võtab kokku olemasoleva varude reserveerimise hierarhia.</span><span class="sxs-lookup"><span data-stu-id="92563-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="92563-109">Varude reserveerimise hierarhia näitab, et laoala dimensioonidega seotud ulatuses on nõudetellimus seotud asukoha kohustuslike dimensioonide, lao ja varude olekuga, samas kui lao loogika vastutab nõutud koguste jaoks asukoha määramise ja selle reserveerimise eest.</span><span class="sxs-lookup"><span data-stu-id="92563-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="92563-110">Teisisõnu, nõudetellimuse ja laotoimingute vahelises suhtluses eeldatakse, et nõudetellimus määrab selle, kust tellimus tuleb saata (st millisest asukohast ja laost).</span><span class="sxs-lookup"><span data-stu-id="92563-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="92563-111">Seejärel toetub ladu laoruumidest nõutava koguse leidmisel oma loogikale.</span><span class="sxs-lookup"><span data-stu-id="92563-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="92563-112">Kuid selleks, et kajastada äritegevuse mudelit, on jälgimisdimensioonid (partii- ja seerianumbrid) siiski paindlikumad.</span><span class="sxs-lookup"><span data-stu-id="92563-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="92563-113">Varude reserveerimise hierarhia võib hõlmata stsenaariume, mille puhul kehtivad järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="92563-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="92563-114">Ettevõte tugineb oma laotoimingutele, et hallata partii- või seerianumbritega koguste komplekteerimist pärast seda, kui ladustamisruumis on kogused leitud.</span><span class="sxs-lookup"><span data-stu-id="92563-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="92563-115">Sellele mudelile viidatakse sageli kui *partii-alla\[asukoht\]*.</span><span class="sxs-lookup"><span data-stu-id="92563-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="92563-116">Seda kasutatakse tavaliselt siis, kui toote partii- või seerianumbri ID ei ole klientidele oluline, kuna nad suunavad nõudluse müügiettevõttele.</span><span class="sxs-lookup"><span data-stu-id="92563-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="92563-117">Kui partii- või seerianumbrid on osa kliendi tellimuse täpsustusest ja need kirjendatakse nõudetellimusel, on laos olevaid koguseid leidnud toimingud piiratud konkreetsete nõutud numbritega ja neid ei tohi muuta.</span><span class="sxs-lookup"><span data-stu-id="92563-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="92563-118">Sellele mudelile viidatakse sageli kui *partii-üles\[asukoht\]*.</span><span class="sxs-lookup"><span data-stu-id="92563-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="92563-119">Nende stsenaariumide puhul on probleemiks, et igale väljastatud tootele saab määrata ainult ühe varude reserveerimise hierarhia.</span><span class="sxs-lookup"><span data-stu-id="92563-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="92563-120">Seetõttu ei saa WMS pärast seda, kui hierarhia määramine on määratlenud, millal partii või seerianumber tuleb reserveerida (kas siis, kui nõudetellimus on tehtud, või lao komplekteerimise ajal), jälgitud üksuste käsitsemisel ajastust ad-hoc-alusel muuta.</span><span class="sxs-lookup"><span data-stu-id="92563-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="92563-121">Partiijälgimisega kaupade paindlik reserveerimine</span><span class="sxs-lookup"><span data-stu-id="92563-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="92563-122">Äristsenaarium</span><span class="sxs-lookup"><span data-stu-id="92563-122">Business scenario</span></span>

<span data-ttu-id="92563-123">Selle stsenaariumi puhul kasutab ettevõte varude strateegiat, mille puhul lõpetatud kaupu jälgitakse partii numbrite järgi.</span><span class="sxs-lookup"><span data-stu-id="92563-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="92563-124">See ettevõte kasutab ka WMS-i töökogust.</span><span class="sxs-lookup"><span data-stu-id="92563-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="92563-125">Kuna sellel töökogusel on hästivarustatud loogika lao komplekteerimise ja saatmise toimingute planeerimiseks ning käitamiseks partiis lubatud kaupade puhul, on enamik lõpetatud kaupadest seotud „partii-alla\[asukoht\]“ varude reserveerimise hierarhiaga.</span><span class="sxs-lookup"><span data-stu-id="92563-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="92563-126">Seda tüüpi toiminguseadistuse eeliseks on see, et partiide komplekteerimise ja laovaliku otsused (mis on tegelikult reserveerimise otsused) lükatakse edasi, kuni alustatakse lao komplekteerimise toimingutega.</span><span class="sxs-lookup"><span data-stu-id="92563-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="92563-127">Neid ei tehta kliendi tellimuse esitamise ajal.</span><span class="sxs-lookup"><span data-stu-id="92563-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="92563-128">Kuigi „partii-alla\[asukoht\]” reserveerimise hierarhia teenib ettevõtte ärieesmärke hästi, nõuavad paljud ettevõtte kliendid toodete uuesti tellimisel sama partiid, mida nad varem ostsid.</span><span class="sxs-lookup"><span data-stu-id="92563-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="92563-129">Seetõttu ootavad ettevõtted paindlikkust selle osas, kuidas partii reserveerimise reegleid käsitletakse, nii et olenevalt klientide nõudlusest sama kauba järele võivad ilmneda järgmised käitumismustrid.</span><span class="sxs-lookup"><span data-stu-id="92563-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="92563-130">Partii numbrit saab kirjendada ja reserveerida, kui volitatud töötleja on tellimuse vastu võtnud, ja seda ei saa muuta laotoimingute ajal ja/või muude nõudmiste tõttu.</span><span class="sxs-lookup"><span data-stu-id="92563-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="92563-131">Selline käitumine aitab tagada, et tellitud partiinumber saadetakse kliendile.</span><span class="sxs-lookup"><span data-stu-id="92563-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="92563-132">Kui partiinumber ei ole kliendile oluline, saab laotoimingute komplekteerimise käigus määrata partiinumbri pärast seda, kui müügitellimuse registreerimine ja reserveerimine on tehtud.</span><span class="sxs-lookup"><span data-stu-id="92563-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="92563-133">Müügitellimuse kindla partii reserveerimise lubamine</span><span class="sxs-lookup"><span data-stu-id="92563-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="92563-134">Selleks, et mahutada soovitud paindlikkus partii reserveerimise käitumises kaupadele, mis on seotud „partii-alla\[asukoht\]” varude reserveerimise hierarhiaga, peavad varude haldurid lehel **Varude reserveerimise hierarhiad** valima märkeruudu **Luba reserveerimine nõudetellimusel** valiku **Partiinumber** tasemel.</span><span class="sxs-lookup"><span data-stu-id="92563-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Varude reserveerimise hierarhia paindlikuks muutmine](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="92563-136">Kui hierarhias valitakse tase **Partiinumber** , valitakse automaatselt kõik seda taset ületavad dimensioonid kuni **Asukoha** tasemeni.</span><span class="sxs-lookup"><span data-stu-id="92563-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="92563-137">(Vaikimisi valitakse tasemest **Asukoht** üle olevad dimensioonid.) Selline käitumine peegeldab loogikat, kus kõik dimensioonid partiinumbri ja asukoha vahel on samuti automaatselt reserveeritud pärast seda, kui reserveerite tellimuse reale kindla partiinumbri.</span><span class="sxs-lookup"><span data-stu-id="92563-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="92563-138">Märkeruut **Luba reserveerimine nõudetellimusel** kehtib ainult reserveerimise hierarhia tasemete puhul, mis jäävad lao asukoha dimensioonist allapoole.</span><span class="sxs-lookup"><span data-stu-id="92563-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="92563-139">**Partiinumber** ja **Litsentsiplaat** on hierarhias ainsad tasemed, mida saab kasutada paindliku reserveerimise poliitikas.</span><span class="sxs-lookup"><span data-stu-id="92563-139">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="92563-140">Teisisõnu ei saa te valida märkeruutu **Luba reserveerimine nõudetellimusel** taseme **Asukoht** või **Seerianumber** jaoks.</span><span class="sxs-lookup"><span data-stu-id="92563-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="92563-141">Kui teie reserveerimise hierarhia sisaldab seerianumbri dimensiooni (mis peab alati olema väiksem kui tase **Partiinumber** ) ja kui olete pakktöötluse numbrile sisse lülitanud partii-spetsiifilise reserveerimise, jätkab süsteem seerianumbri reserveerimise ja komplekteerimise toiminguid, mis põhinevad reeglitel, mis kehtivad reserveerimise poliitika „Seeria-alla\[asukoht\]” puhul.</span><span class="sxs-lookup"><span data-stu-id="92563-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="92563-142">Igal ajahetkel saate lubada partii-spetsiifilist reserveerimist olemasolevale „partii-alla\[asukoht\]” reserveerimise hierarhiale teie juurutuses.</span><span class="sxs-lookup"><span data-stu-id="92563-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="92563-143">See muudatus ei mõjuta reserveeringuid ja avatud lao tööd, mis loodi enne muudatuse toimumist.</span><span class="sxs-lookup"><span data-stu-id="92563-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="92563-144">Kuid märkeruutu **Luba reserveerimine nõudetellimusel** ei saa tühjendada, kui **Reserveeritud tellitud** , **Reserveeritud füüsilise** või **Tellitud** probleemi tüübi laokanded on olemas ühe või mitme selle reserveerimise hierarhiaga seotud kauba puhul.</span><span class="sxs-lookup"><span data-stu-id="92563-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered** , **Reserved physical** , or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="92563-145">Kui kauba olemasoleva reserveerimise hierarhia ei luba tellimuse partii täpsustust, saate selle uuesti määrata reserveerimise hierarhiasse, mis lubab partii spetsifikatsioone, tingimusel et hierarhia taseme struktuur on mõlemas hierarhias sama.</span><span class="sxs-lookup"><span data-stu-id="92563-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="92563-146">Kasutage funktsiooni **Muuda reserveerimise hierarhiat kaupadele** ümbermääramiseks.</span><span class="sxs-lookup"><span data-stu-id="92563-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="92563-147">See muudatus võib olla oluline, kui soovite vältida partiis jälitatud kaupade alamhulga paindlikku partii reserveerimist, kuid lubada seda ülejäänud tooteportfellile.</span><span class="sxs-lookup"><span data-stu-id="92563-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="92563-148">Olenemata sellest, kas olete märkinud ruudu **Luba reserveerimine nõudetellimusel** , kui te ei soovi kindlat partiinumbrit kaubale tellimuse rea jaoks reserveerida, rakendatakse laotoimingute vaikeloogikat, mis kehtib „partii-alla\[asukoht\]” reserveerimise hierarhia puhul.</span><span class="sxs-lookup"><span data-stu-id="92563-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="92563-149">Kindla partiinumbri reserveerimine kliendi tellimuse jaoks</span><span class="sxs-lookup"><span data-stu-id="92563-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="92563-150">Pärast seda, kui partii jälgitud kauba „partii-alla\[asukoht\]” varude reserveerimise hierarhia on seadistatud lubama kindla partiinumbrite reserveerimist müügitellimustel, võivad müügitellimuse töötlejad võtta sama kauba kohta kliendi tellimusi ühel järgmistest viisidest, olenevalt kliendi nõudest.</span><span class="sxs-lookup"><span data-stu-id="92563-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="92563-151">**Sisestage tellimuse üksikasjad partiinumbrit täpsustamata** – seda lähenemist tuleks kasutada juhul, kui toote partii spetsifikatsioon ei ole kliendile oluline.</span><span class="sxs-lookup"><span data-stu-id="92563-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="92563-152">Kõik olemasolevad protsessid, mis on seotud selle tüübi tellimuse käsitsemisega, jäävad süsteemis muutmata.</span><span class="sxs-lookup"><span data-stu-id="92563-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="92563-153">Kasutajate osas ei nõuta täiendavaid kaalutlusi.</span><span class="sxs-lookup"><span data-stu-id="92563-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="92563-154">**Sisestage tellimuse üksikasjad ja reserveerige konkreetne partiinumber** – seda lähenemist tuleks kasutada siis, kui klient nõuab kindlat partiid.</span><span class="sxs-lookup"><span data-stu-id="92563-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="92563-155">Tavaliselt nõuavad kliendid kindlat partiid, kui nad tellivad varem ostetud toodet.</span><span class="sxs-lookup"><span data-stu-id="92563-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="92563-156">Seda tüüpi partii-spetsiifilist reserveerimist nimetatakse *tellimusega kooskõlastatud reserveerimiseks*.</span><span class="sxs-lookup"><span data-stu-id="92563-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="92563-157">Järgmised reeglid kehtivad koguste töötlemisel ja partiinumber on seotud kindla tellimusega.</span><span class="sxs-lookup"><span data-stu-id="92563-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="92563-158">Selleks et lubada kauba kindla partii numbri reserveerimist kauba puhul, mis on märgitud jaotises „partii-alla\[asukoht\]”, peab süsteem reserveerima kõik dimensioonid asukoha kaudu.</span><span class="sxs-lookup"><span data-stu-id="92563-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="92563-159">See vahemik sisaldab tavaliselt litsentsiplaadi dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="92563-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="92563-160">Asukoha direktiive ei kasutata, kui komplekteerimise töö on loodud müügirea jaoks, mis kasutab tellimusega seotud partii reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="92563-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="92563-161">Tellimusega seotud partiide töö laotöötluse ajal ei tohi ei kasutaja ega süsteem partii numbrit muuta.</span><span class="sxs-lookup"><span data-stu-id="92563-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="92563-162">(See töötlemine hõlmab erandite käsitlemist.)</span><span class="sxs-lookup"><span data-stu-id="92563-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="92563-163">Järgmises näites kuvatakse täielik töövoog.</span><span class="sxs-lookup"><span data-stu-id="92563-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="92563-164">Näidisstsenaarium: partiinumbri määramine</span><span class="sxs-lookup"><span data-stu-id="92563-164">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="92563-165">Selle näite jaoks peavad olema installitud demoandmed ja peate kasutama demoandmete ettevõtet **USMF**.</span><span class="sxs-lookup"><span data-stu-id="92563-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="92563-166">Varude reserveerimise hierarhia seadistamine partiile konkreetse reserveerimise lubamiseks</span><span class="sxs-lookup"><span data-stu-id="92563-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="92563-167">Avage **Laohaldus** \> **Seadistus** \> **Varud \> Reserveerimine hierarhiasse**.</span><span class="sxs-lookup"><span data-stu-id="92563-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="92563-168">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="92563-168">Select **New**.</span></span>
3. <span data-ttu-id="92563-169">Väljale **Nimi** sisestage nimi (nt **BatchFlex** ).</span><span class="sxs-lookup"><span data-stu-id="92563-169">In the **Name** field, enter a name (for example, **BatchFlex** ).</span></span>
4. <span data-ttu-id="92563-170">Väljale **Kirjeldus** sisestage kirjeldus (nt **Partii alla paindlikkuse** ).</span><span class="sxs-lookup"><span data-stu-id="92563-170">In the **Description** field, enter a description (for example, **Batch below flexible** ).</span></span>
5. <span data-ttu-id="92563-171">Väljal **Valitud** valige **Seerianumber** ja **Omanik** ning seejärel klõpsake vasakut nooleklahvi, et teisaldada need väljale **Saadaolev**.</span><span class="sxs-lookup"><span data-stu-id="92563-171">In the **Selected** field, select **Serial number** and **Owner** , and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="92563-172">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="92563-172">Select **OK**.</span></span>
7. <span data-ttu-id="92563-173">Märkige dimensioonitaseme real **Partiinumbri** ruut **Luba reserveerimine nõudetellimusel**.</span><span class="sxs-lookup"><span data-stu-id="92563-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="92563-174">Tasemed **Litsentsiplaat** ja **Asukoht** valitakse automaatselt ja nende märkeruute ei saa tühjendada.</span><span class="sxs-lookup"><span data-stu-id="92563-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="92563-175">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="92563-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="92563-176">Uue väljastatud toote loomine</span><span class="sxs-lookup"><span data-stu-id="92563-176">Create a new released product</span></span>

1. <span data-ttu-id="92563-177">Määrake toote kolm koondandmete parameetrit, kasutades neid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="92563-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="92563-178">Valige väljal **Laoala dimensioonigrupp** suvand **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="92563-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="92563-179">Valige väljal  **Jälgimisdimensiooni grupp** suvand **Batch-Phy**.</span><span class="sxs-lookup"><span data-stu-id="92563-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="92563-180">Valige väljal **Reserveeringu hierarhia** suvand **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="92563-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="92563-181">Looge kaks partiinumbrit, nt **B11** ja **B22**.</span><span class="sxs-lookup"><span data-stu-id="92563-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="92563-182">Lisage kauba kogused laoseisu, kasutades järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="92563-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="92563-183">Ladu</span><span class="sxs-lookup"><span data-stu-id="92563-183">Warehouse</span></span> | <span data-ttu-id="92563-184">Partii number</span><span class="sxs-lookup"><span data-stu-id="92563-184">Batch number</span></span> | <span data-ttu-id="92563-185">Koht</span><span class="sxs-lookup"><span data-stu-id="92563-185">Location</span></span> | <span data-ttu-id="92563-186">Litsentsiplaat</span><span class="sxs-lookup"><span data-stu-id="92563-186">License plate</span></span> | <span data-ttu-id="92563-187">Kogus</span><span class="sxs-lookup"><span data-stu-id="92563-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="92563-188">24</span><span class="sxs-lookup"><span data-stu-id="92563-188">24</span></span>        | <span data-ttu-id="92563-189">B11</span><span class="sxs-lookup"><span data-stu-id="92563-189">B11</span></span>          | <span data-ttu-id="92563-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="92563-190">BULK-001</span></span> | <span data-ttu-id="92563-191">Puudub</span><span class="sxs-lookup"><span data-stu-id="92563-191">None</span></span>          | <span data-ttu-id="92563-192">10</span><span class="sxs-lookup"><span data-stu-id="92563-192">10</span></span>       |
    | <span data-ttu-id="92563-193">24</span><span class="sxs-lookup"><span data-stu-id="92563-193">24</span></span>        | <span data-ttu-id="92563-194">B11</span><span class="sxs-lookup"><span data-stu-id="92563-194">B11</span></span>          | <span data-ttu-id="92563-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="92563-195">FL-001</span></span>   | <span data-ttu-id="92563-196">LP11</span><span class="sxs-lookup"><span data-stu-id="92563-196">LP11</span></span>          | <span data-ttu-id="92563-197">10</span><span class="sxs-lookup"><span data-stu-id="92563-197">10</span></span>       |
    | <span data-ttu-id="92563-198">24</span><span class="sxs-lookup"><span data-stu-id="92563-198">24</span></span>        | <span data-ttu-id="92563-199">B22</span><span class="sxs-lookup"><span data-stu-id="92563-199">B22</span></span>          | <span data-ttu-id="92563-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="92563-200">FL-002</span></span>   | <span data-ttu-id="92563-201">LP22</span><span class="sxs-lookup"><span data-stu-id="92563-201">LP22</span></span>          | <span data-ttu-id="92563-202">10</span><span class="sxs-lookup"><span data-stu-id="92563-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="92563-203">Müügitellimuse üksikasjade sisestamine</span><span class="sxs-lookup"><span data-stu-id="92563-203">Enter sales order details</span></span>

1. <span data-ttu-id="92563-204">Avage **Müük ja turundus** \> **Müügitellimused** \> **Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="92563-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="92563-205">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="92563-205">Select **New**.</span></span>
3. <span data-ttu-id="92563-206">Müügitellimuse päise väljale **Kliendi konto** sisestage **US-003**.</span><span class="sxs-lookup"><span data-stu-id="92563-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="92563-207">Lisage uue üksuse jaoks rida ja sisestage koguseks **10**.</span><span class="sxs-lookup"><span data-stu-id="92563-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="92563-208">Veenduge, et välja **Ladu** väärtuseks oleks määratud **24**.</span><span class="sxs-lookup"><span data-stu-id="92563-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="92563-209">Kiirkaardil **Müügitellimuse read** valige väärtus **Varud** ja seejärel jaotises **Haldamine** suvand **Partii reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="92563-209">On the **Sales order lines** FastTab, select **Inventory** , and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="92563-210">Leht **Partii reserveerimine** näitab tellimuse rea reserveerimiseks saadaolevate partiide loendit.</span><span class="sxs-lookup"><span data-stu-id="92563-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="92563-211">Selles näites näitab see kogust **20** partiinumbri **B11** ja kogust **10** partiinumbri **B22** jaoks.</span><span class="sxs-lookup"><span data-stu-id="92563-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="92563-212">Pange tähele, et lehele **Partii reserveerimine** ei pääse realt juurde, kui sellel real olev üksus on seotud väärtusega „partii-alla\[asukoht\]”, kui see pole seadistatud lubama partiiga seotud reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="92563-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="92563-213">Kindla partii reserveerimiseks müügitellimusele tuleb kasutada lehte **Partii reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="92563-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="92563-214">Kui sisestate partii numbri otse müügitellimuse reale, käitub süsteem nii, nagu sisestasite kindla partii väärtuse üksusele, mille suhtes kehtib „partii-alla\[asukoht\]” reserveerimise poliitika.</span><span class="sxs-lookup"><span data-stu-id="92563-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="92563-215">Rea salvestamisel kuvatakse hoiatusteade.</span><span class="sxs-lookup"><span data-stu-id="92563-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="92563-216">Kui kinnitate, et partiinumber tuleb määrata otse tellimuse reale, ei käsitleta rida tavalise laohalduse loogikaga.</span><span class="sxs-lookup"><span data-stu-id="92563-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="92563-217">Kui reserveerite koguse lehelt **Reserveerimine** , ei reserveerita ühtegi kindlat partiid ja selle rea laotegevuse käitamine järgib reegleid, mis on rakendatavad „partii-alla\[asukoht\]” reserveerimise poliitika alusel.</span><span class="sxs-lookup"><span data-stu-id="92563-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="92563-218">See lehekülg töötab ja on seotud samal viisil, nagu see toimib ja on seotud üksuste puhul, millel on seostatud reserveerimise hierarhia tüübiga „partii-üle\[asukoha\]”.</span><span class="sxs-lookup"><span data-stu-id="92563-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="92563-219">Siiski kehtivad järgmised erandid.</span><span class="sxs-lookup"><span data-stu-id="92563-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="92563-220">Kiirkaart **Lähtereale määratud partiinumbrid** kuvab tellimuserea jaoks reserveeritud partiinumbrid.</span><span class="sxs-lookup"><span data-stu-id="92563-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="92563-221">Ruudustikus olevad partiiväärtused kuvatakse kogu tellimuserea täitmise tsüklis, sh laotöötluse etappides.</span><span class="sxs-lookup"><span data-stu-id="92563-221">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="92563-222">Seevastu kiirkaart **Ülevaade** , korrapärase tellimuse rea reserveerimine (s.t reserveerimine, mida tehakse **Asukoha** taseme kohal olevate dimensioonide puhul), kuvatakse ruudustikus kuni laotöö loomiseni.</span><span class="sxs-lookup"><span data-stu-id="92563-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="92563-223">Tööüksus võtab seejärel rea reserveerimise üle ja rea reserveeringut ei kuvata enam leheküljel.</span><span class="sxs-lookup"><span data-stu-id="92563-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="92563-224">Kiirkaart **Lähtereale määratud partiinumbrid** aitab tagada, et müügitellimuse töötleja saab vaadata kliendi tellimusele määratud partiinumbreid mis tahes tööetapis kuni arveldamiseni.</span><span class="sxs-lookup"><span data-stu-id="92563-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="92563-225">Peale konkreetse partii reserveerimise saab kasutaja valida käsitsi partii kindla asukoha ja litsentsiplaadi, selle asemel et lasta süsteemil need automaatselt valida.</span><span class="sxs-lookup"><span data-stu-id="92563-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="92563-226">See võimalus on seotud tellimuse sooritatud partii reserveerimise mehhanismi kujundusega.</span><span class="sxs-lookup"><span data-stu-id="92563-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="92563-227">Nagu varem mainitud, tuleb selleks, et lubada kindla partii numbri reserveerimist üksuse puhul, mis on märgitud jaotises „partii-alla\[asukoht\]”, peab süsteem reserveerima kõik dimensioonid asukoha kaudu.</span><span class="sxs-lookup"><span data-stu-id="92563-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="92563-228">Seetõttu teeb lao töö samu ladustamise dimensioone, mis olid reserveeritud tellimustega töötavate kasutajate poolt, ja see ei pruugi alati kajastada kauba ladustamise paigutust, mis on mugav või isegi võimalik komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="92563-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="92563-229">Kui tellimuse töötlejad on lao piirangutest teadlikud, võivad nad partii reserveerimisel käsitsi valida kindlad asukohad ja litsentsiplaadid.</span><span class="sxs-lookup"><span data-stu-id="92563-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="92563-230">Sellisel juhul peab kasutaja kasutama lehekülje päises funktsiooni **Kuva dimensioonid** ja lisama asukoha ja litsentsiplaadi kiirkaardi **Ülevaade** ruudustikus.</span><span class="sxs-lookup"><span data-stu-id="92563-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="92563-231">Valige lehel **Partii reserveerimine** partii **B11** jaoks rida ja seejärel käsk **Reserveeri rida**.</span><span class="sxs-lookup"><span data-stu-id="92563-231">On the **Batch reservation** page, select the line for batch **B11** , and then select **Reserve line**.</span></span> <span data-ttu-id="92563-232">Automaatsel reserveerimisel ei ole asukohtade ja litsentsiplaadi määramiseks loogikat määratud.</span><span class="sxs-lookup"><span data-stu-id="92563-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="92563-233">Koguse saate sisestada käsitsi väljale **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="92563-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="92563-234">Pange tähele, et kiirkaardi **Lähtereale määratud partiinumbrid** partii **B11** kuvatakse kui **Sooritatud**.</span><span class="sxs-lookup"><span data-stu-id="92563-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Kindla partiinumbri määramine müügitellimuse reale partii reserveerimise lehel](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="92563-236">Müügitellimuse rea koguse reserveerimist saab teha mitmel partiil.</span><span class="sxs-lookup"><span data-stu-id="92563-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="92563-237">Sama partii reserveerimist saab teha ka mitme asukoha ja litsentsiplaadi alusel (kui nende asukohtade puhul on lubatud litsentsiplaadid).</span><span class="sxs-lookup"><span data-stu-id="92563-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="92563-238">Kindla partii reserveerimine müügitellimuse real oleva koguse jaoks võib olla ka osaline.</span><span class="sxs-lookup"><span data-stu-id="92563-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="92563-239">Näiteks 100 ühiku kogukogust saab reserveerida nii, et kindel partii on pühendunud 20 ühikule, samas kui 80 ühikut on reserveeritud saidi ja lao tasemetele mis tahes saadaoleva partii jaoks.</span><span class="sxs-lookup"><span data-stu-id="92563-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="92563-240">Sel juhul kasutab WMS komplekteerimislehe töötlemisel kaht eraldiseisvat töörida.</span><span class="sxs-lookup"><span data-stu-id="92563-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="92563-241">Avage **Tooteteabe haldus** \> **Tooted** \> **Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="92563-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="92563-242">Valige üksus ja seejärel **Varude haldamine** \> **Kuva** \> **Kanded**.</span><span class="sxs-lookup"><span data-stu-id="92563-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Tellimusega kooskõlastatud reserveerimine laokande tüübina](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="92563-244">Vaadake üle kauba varude kanded, mis on seotud müügitellimuse rea reserveerimisega.</span><span class="sxs-lookup"><span data-stu-id="92563-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="92563-245">Kanne, mille välja **Viide** väärtuseks on seatud **Müügitellimus** ja välja **Väljaminek** väärtuseks on seatud **Reserveeritud füüsiline** , näitab tellimuse rea reserveerimist varude dimensioonide jaoks, mis on üle taseme **Asukoht**.</span><span class="sxs-lookup"><span data-stu-id="92563-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="92563-246">Kauba varude reserveerimise hierarhia kohaselt on need dimensioonid saidi, lao ja varude olek.</span><span class="sxs-lookup"><span data-stu-id="92563-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="92563-247">Kanne, mille välja **Viide** väärtuseks on seatud **Tellimuse tehtud reserveerimine** ja välja **Väljaminek** väärtuseks on seatud **Reserveeritud füüsiline** , näitab tellimuse rea reserveerimist kindlat partiid ja kõiki varude dimensioone üle selle.</span><span class="sxs-lookup"><span data-stu-id="92563-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="92563-248">Kauba varude reserveerimise hierarhia kohaselt on need dimensioonid partiinumber ja asukoht.</span><span class="sxs-lookup"><span data-stu-id="92563-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="92563-249">Selles näites on asukoht **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="92563-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="92563-250">Valige müügitellimuse päises suvandid **Ladu** \> **Tegevused** \> **Laost vabastamine**.</span><span class="sxs-lookup"><span data-stu-id="92563-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="92563-251">Tellimuse rida on nüüd moodustatud ja töö on loodud.</span><span class="sxs-lookup"><span data-stu-id="92563-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="92563-252">Tellitud partiinumbritega laotööde ülevaatamine ja töötlemine</span><span class="sxs-lookup"><span data-stu-id="92563-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="92563-253">Kiirkaardil **Müügitellimuse read** valige **Ladu**\>**Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="92563-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="92563-254">Tööl, mis tegeleb müügitellimuse reale pühendunud partii koguste komplekteerimisega, on järgmised omadused.</span><span class="sxs-lookup"><span data-stu-id="92563-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="92563-255">Töö loomiseks kasutab süsteem töömalle, kuid mitte asukoha direktiive.</span><span class="sxs-lookup"><span data-stu-id="92563-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="92563-256">Kõik töömallide jaoks määratletud kindlad sätted, nt maksimaalne komplekteerimise read või kindel mõõtühik, rakendatakse uute tööde loomisel määramiseks.</span><span class="sxs-lookup"><span data-stu-id="92563-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="92563-257">Siiski ei arvestata reegleid, mis on seotud asukoha direktiividega komplekteerimise asukohtade tuvastamiseks, kuna tellimusega kooskõlastatud reserveeringuga on juba määratud kõik varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="92563-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="92563-258">Need varude dimensioonid sisaldavad dimensioone lao ladustamise tasemel.</span><span class="sxs-lookup"><span data-stu-id="92563-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="92563-259">Seetõttu pärib töö need dimensioonid, ilma et peaksite konsulteerima asukoha direktiividega.</span><span class="sxs-lookup"><span data-stu-id="92563-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="92563-260">Partiinumbrit ei kuvata komplekteerimise real (nagu näiteks töörea puhul, mis luuakse kaubale, millel on seostatud „partii-üle\[-asukoht\]” reserveerimise hierarhia). Selle asemel kuvatakse seotud laokannete põhjal viidatud töökandes partiinumber ja kõik muud varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="92563-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Tellimusega kooskõlastatud reserveeringust pärinev lao laokande töö](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="92563-262">Kui töö on loodud, eemaldatakse välja **Viide** väärtusega **Tellimusele kooskõlastatud reserveerimine** kauba laokanne.</span><span class="sxs-lookup"><span data-stu-id="92563-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="92563-263">Laokannete puhul, mille välja **Viide** väärtuseks on seatud **Töö** , on nüüd füüsiline reserveerimine määratud kõigi koguse varude dimensioonide jaoks.</span><span class="sxs-lookup"><span data-stu-id="92563-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="92563-264">Laotoimingud võivad jätkata töö töötlemist tavalisel viisil.</span><span class="sxs-lookup"><span data-stu-id="92563-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="92563-265">Kuid mobiilseade juhendab töötajat valima kindlat partiinumbrit.</span><span class="sxs-lookup"><span data-stu-id="92563-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="92563-266">Lao keskkondades, kus asukohti kontrollitakse litsentsiplaadiga pärast seda, kui töötaja jõuab asukohani, mis talletab sama partii mitmele litsentsiplaadile, saab ta valida mis tahes litsentsiplaadi, mis pole veel reserveeritud (nt teine tellimusega kooskõlastatud reserveering või töö, mis pärineb seda tüüpi reserveeringust.)</span><span class="sxs-lookup"><span data-stu-id="92563-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="92563-267">Kui tööreal määratud asukohast komplekteerimine osutub ebaotstarbekaks, saavad laooperaatorid kasutada üht järgmistest toimingutest, et suunata kindla partii komplekteerimine mugavamasse asukohta.</span><span class="sxs-lookup"><span data-stu-id="92563-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="92563-268">Mobiilseadme tavatoiming **Asukoha alistamine** (eeldusel, et lao töötaja säte **Luba valitud asukoha alistamine** on lubatud)</span><span class="sxs-lookup"><span data-stu-id="92563-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="92563-269">Toiming **Muuda asukohta** lehel **Tööloendi üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="92563-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="92563-270">Lõpetage mobiilseadmes komplekteerimine ja töö sisestamine.</span><span class="sxs-lookup"><span data-stu-id="92563-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="92563-271">Kogus **10** on nüüd partiinumbri **B11** jaoks müügireale komplekteeritud ja asukohta **Baydoor** pandud.</span><span class="sxs-lookup"><span data-stu-id="92563-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="92563-272">Sel hetkel on see veokile laadimiseks ja kliendi aadressile lähetamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="92563-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="92563-273">Paindlik litsentsiplaadi reserveerimine</span><span class="sxs-lookup"><span data-stu-id="92563-273">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="92563-274">Äristsenaarium</span><span class="sxs-lookup"><span data-stu-id="92563-274">Business scenario</span></span>

<span data-ttu-id="92563-275">Selles stsenaariumis kasutab ettevõte laohaldust ja töö töötlemist ning planeerib koormaid üksikute kaubaaluste/konteinerite alusel väljaspool Supply Chain Managementi enne töö loomist.</span><span class="sxs-lookup"><span data-stu-id="92563-275">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="92563-276">Neid konteinereid esindavad varude dimensioonides litsentsiplaadid.</span><span class="sxs-lookup"><span data-stu-id="92563-276">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="92563-277">Selleks toiminguks tuleb seetõttu konkreetsed litsentsiplaadid enne komplekteerimistöö lõpetamist määrata müügitellimuse ridadele.</span><span class="sxs-lookup"><span data-stu-id="92563-277">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="92563-278">Ettevõte soovib, et litsentsiplaadi reserveerimise reeglite käsitsemine oleks paindlik, et juhtuksid järgmised asjad.</span><span class="sxs-lookup"><span data-stu-id="92563-278">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="92563-279">Litsentsiplaati saab kirjendada ja reserveerida, kui volitatud töötleja võtab tellimuse vastu, ning muud nõuded ei saa seda endale võtta.</span><span class="sxs-lookup"><span data-stu-id="92563-279">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="92563-280">Selline käitumine aitab tagada, et planeeritud litsentsiplaat saadetakse kliendile.</span><span class="sxs-lookup"><span data-stu-id="92563-280">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="92563-281">Kui litsentsiplaat ei ole juba müügitellimuse reale määratud, saab laotöötaja valida litsentsiplaadi komplekteerimise ajal, pärast müügitellimuse registreerimist ja reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="92563-281">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="92563-282">Paindliku litsentsiplaadi reserveerimise sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="92563-282">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="92563-283">Enne paindliku litsentsiplaadi reserveerimise kasutamist peate oma süsteemis sisse lülitama kaks funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="92563-283">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="92563-284">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsioonide olekut ja need vajadusel sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="92563-284">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="92563-285">Peate funktsioonid sisse lülitama järgmises järjekorras.</span><span class="sxs-lookup"><span data-stu-id="92563-285">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="92563-286">**Funktsiooni nimi:** *Paindlik dimensiooni reserveerimine laotasemel*</span><span class="sxs-lookup"><span data-stu-id="92563-286">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="92563-287">**Funktsiooni nimi:** *Paindlik tellimusega seotud litsentsiplaadi reserveerimine*</span><span class="sxs-lookup"><span data-stu-id="92563-287">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="92563-288">Kindla litsentsiplaadi reserveerimine müügitellimusel</span><span class="sxs-lookup"><span data-stu-id="92563-288">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="92563-289">Selleks, et lubada litsentsiplaadi reserveerimine tellimusel, peate valima lehel **Varude reserveerimise hierarhiad** märkeruudu **Luba reserveerimine nõudetellimusel** tasemel **Litsentsiplaat** hierarhia jaoks, mis on seotud asjaomase kaubaga.</span><span class="sxs-lookup"><span data-stu-id="92563-289">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![Varude reserveerimise hierarhialeht paindliku litsentsiplaadi reserveerimise hierarhia jaoks](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="92563-291">Saate lubada litsentsiplaadi reserveerimise tellimusel juurutuse käigus igal ajal.</span><span class="sxs-lookup"><span data-stu-id="92563-291">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="92563-292">See muudatus ei mõjuta reserveeringuid ega avatud laotöid, mis loodi enne muudatuse toimumist.</span><span class="sxs-lookup"><span data-stu-id="92563-292">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="92563-293">Kuid te ei saa märkeruutu **Luba reserveerimine nõudetellimusel** tühjendada, kui reserveerimise hierarhiaga seotud ühel või mitmel kaubal on avatud väljaminevate varude kandeid, mille väljamineku olek on *Tellimusel* , *Reserveeritud tellitud* või *Füüsiliselt reserveeritud*.</span><span class="sxs-lookup"><span data-stu-id="92563-293">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order* , *Reserved ordered* , or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="92563-294">Isegi kui märkeruut **Luba reserveerimine nõudetellimusel** on tasemel **Litsentsiplaat** valitud, *ei ole* siiski võimalik kindlat litsentsiplaati tellimusel reserveerida.</span><span class="sxs-lookup"><span data-stu-id="92563-294">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="92563-295">Sel juhul rakendub laotoimingute vaikeloogika, mis kehtib selle reserveerimise hierarhia puhul.</span><span class="sxs-lookup"><span data-stu-id="92563-295">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="92563-296">Konkreetse litsentsiplaadi reserveerimiseks peate kasutama [avatud andmeprotokolli (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) protsessi. Rakenduses saate teha reserveeringu otse müügitellimusel, kasutades käsu **Ava Excelis** valikut **Tellimusega seotud reserveeringud litsentsiplaadi kohta**.</span><span class="sxs-lookup"><span data-stu-id="92563-296">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="92563-297">Te peate sisestama Exceli lisandmoodulis avanenud üksuse andmetes järgmised reserveeringuga seotud andmed ja valima seejärel **Avalda** , et saata andmed tagasi Supply Chain Managementi.</span><span class="sxs-lookup"><span data-stu-id="92563-297">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="92563-298">Viide (toetatud on ainult väärtus *Müügitellimus*.)</span><span class="sxs-lookup"><span data-stu-id="92563-298">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="92563-299">Tellimuse number (väärtust saab tuletada partiist.)</span><span class="sxs-lookup"><span data-stu-id="92563-299">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="92563-300">Saatepartii ID</span><span class="sxs-lookup"><span data-stu-id="92563-300">Lot ID</span></span>
- <span data-ttu-id="92563-301">Litsentsiplaat</span><span class="sxs-lookup"><span data-stu-id="92563-301">License plate</span></span>
- <span data-ttu-id="92563-302">Kogus</span><span class="sxs-lookup"><span data-stu-id="92563-302">Quantity</span></span>

<span data-ttu-id="92563-303">Kui teil on vaja reserveerida kindlat litsentsiplaati partiijälgimisega kauba jaoks, kasutage lehte **Partii reserveerimine** , nagu on kirjeldatud jaotises [Müügitellimuse üksikasjade sisestamine](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="92563-303">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="92563-304">Kui laotoimingud töötlevad müügitellimuse rida, mis kasutab tellimusega seotud litsentsiplaadi reserveerimist, ei kasutata asukohakorraldusi.</span><span class="sxs-lookup"><span data-stu-id="92563-304">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="92563-305">Kui laotöö kaup koosneb ridadest, mis moodustavad täieliku kaubaaluse ja millel on litsentsiplaadiga seotud kogused, saate optimeerida komplekteerimisprotsessi, kasutades mobiilse seadme menüükäsku, mille puhul on suvandi **Käitle litsentsiplaadi põhjal** väärtuseks seatud *Jah*.</span><span class="sxs-lookup"><span data-stu-id="92563-305">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="92563-306">Selle asemel, et skannida töö kaupasid ühekaupa, saab laotöötaja seejärel komplekteerimise lõpule viimiseks litsentsiplaadi skannida.</span><span class="sxs-lookup"><span data-stu-id="92563-306">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![Mobiilse seadme menüükäsk, mille puhul on suvandi „Käitle litsentsiplaadi põhjal” väärtuseks seatud „Jah”](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="92563-308">Kuna funktsioon **Käitle litsentsiplaadi põhjal** ei toeta mitut kaubaalust hõlmavaid töid, siis on parem, kui eri litsentsiplaatide jaoks on eraldi tööüksus.</span><span class="sxs-lookup"><span data-stu-id="92563-308">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="92563-309">Selle meetodi kasutamiseks lisage väli **Tellimusega seotud litsentsiplaadi ID** tööpäise piirina lehel **Töömall**.</span><span class="sxs-lookup"><span data-stu-id="92563-309">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

> [!NOTE]
> <span data-ttu-id="92563-310">Tellimusega kooskõlastatud töö loomise protsessi puhul määratakse komplekteerimise tööridadele väärtus „tellimusega kooskõlastatud varude dimensioon” ja litsentsiplaadi väärtust pole otse võimalik vaadata.</span><span class="sxs-lookup"><span data-stu-id="92563-310">For the order-committed work creation process, an "order-committed inventory dimension" value will be assigned to the picking work lines, and it won't be possible to view the license plate value directly.</span></span> <span data-ttu-id="92563-311">Mobiilse seadme menüükäsu seadistamisel toetatakse ainult *kasutaja juhitud* protsessi.</span><span class="sxs-lookup"><span data-stu-id="92563-311">Only the *User directed* process is supported when setting up a mobile device menu item.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="92563-312">Näidisstsenaarium: tellimusega seotud litsentsiplaadi reserveerimise seadistamine ja töötlemine</span><span class="sxs-lookup"><span data-stu-id="92563-312">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="92563-313">Selles stsenaariumis näidatakse, kuidas seadistada ja töödelda tellimusega seotud litsentsiplaadi reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="92563-313">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="92563-314">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="92563-314">Make demo data available</span></span>

<span data-ttu-id="92563-315">Selles stsenaariumis viidatakse väärtustele ja kirjetele, mis kuuluvad Supply Chain Managementis esitatud standardsete demoandmete hulka.</span><span class="sxs-lookup"><span data-stu-id="92563-315">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="92563-316">Kui soovite stsenaariumi läbida siin toodud väärtuseid kasutades, peate kasutama keskkonda, kuhu demoandmed on installitud.</span><span class="sxs-lookup"><span data-stu-id="92563-316">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="92563-317">Lisaks seadke enne alustamist juriidilise isiku väärtuseks **USMF**.</span><span class="sxs-lookup"><span data-stu-id="92563-317">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="92563-318">Varude reserveerimise hierarhia loomine, mis lubab litsentsiplaate reserveerida</span><span class="sxs-lookup"><span data-stu-id="92563-318">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="92563-319">Avage **Laohaldus \> Seadistus \> Varud \> Reserveerimise hierarhia**.</span><span class="sxs-lookup"><span data-stu-id="92563-319">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="92563-320">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="92563-320">Select **New**.</span></span>
1. <span data-ttu-id="92563-321">Sisestage väljale **Nimi** väärtus (nt *FlexibleLP* ).</span><span class="sxs-lookup"><span data-stu-id="92563-321">In the **Name** field, enter a value (for example, *FlexibleLP* ).</span></span>
1. <span data-ttu-id="92563-322">Sisestage väljale **Kirjeldus** väärtus (nt *Paindlik LP reserveerimine* ).</span><span class="sxs-lookup"><span data-stu-id="92563-322">In the **Description** field, enter a value (for example, *Flexible LP reservation* ).</span></span>
1. <span data-ttu-id="92563-323">Valige loendis **Valitud** suvandid **Partiinumber** , **Seerianumber** ja **Omanik**.</span><span class="sxs-lookup"><span data-stu-id="92563-323">In the **Selected** list, select **Batch number** , **Serial number** , and **Owner**.</span></span>
1. <span data-ttu-id="92563-324">Valige nupp **Eemalda** ![vasakule osutav nool](media/backward-button.png), et teisaldada valitud kirjed loendisse **Saadaval**.</span><span class="sxs-lookup"><span data-stu-id="92563-324">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="92563-325">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="92563-325">Select **OK**.</span></span>
1. <span data-ttu-id="92563-326">Märkige dimensioonitaseme **Litsentsiplaat** real märkeruut **Luba reserveerimine nõudetellimusel**.</span><span class="sxs-lookup"><span data-stu-id="92563-326">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="92563-327">Tase **Asukoht** valitakse automaatselt ja selle märkeruutu ei saa tühjendada.</span><span class="sxs-lookup"><span data-stu-id="92563-327">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="92563-328">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="92563-328">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="92563-329">Kahe väljastatud toote loomine</span><span class="sxs-lookup"><span data-stu-id="92563-329">Create two released products</span></span>

1. <span data-ttu-id="92563-330">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="92563-330">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="92563-331">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="92563-331">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="92563-332">Seadke dialoogiboksis **Uus väljastatud toode** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="92563-332">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="92563-333">**Tootenumber:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="92563-333">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="92563-334">**Kaubakood:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="92563-334">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="92563-335">**Kauba mudeligrupp:** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="92563-335">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="92563-336">**Kaubagrupp:** *Audio*</span><span class="sxs-lookup"><span data-stu-id="92563-336">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="92563-337">**Laoala dimensiooni grupp:** *Ladu*</span><span class="sxs-lookup"><span data-stu-id="92563-337">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="92563-338">**Jälgimisdimensioonigrupp:** *Puudub*</span><span class="sxs-lookup"><span data-stu-id="92563-338">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="92563-339">**Reserveerimise hierarhia:** *FlexibleLP*</span><span class="sxs-lookup"><span data-stu-id="92563-339">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="92563-340">Valige toote loomiseks ja dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="92563-340">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="92563-341">Uus toode avatakse.</span><span class="sxs-lookup"><span data-stu-id="92563-341">The new product is opened.</span></span> <span data-ttu-id="92563-342">Seadke kiirkaardil **Ladu** välja **Ühiku seeriagrupi ID** väärtuseks *ea*.</span><span class="sxs-lookup"><span data-stu-id="92563-342">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="92563-343">Korrake eelmisi samme, et luua teine toode, millel on samad sätted, kuid seadke väljade **Tootenumber** ja **Kaubakood** väärtuseks *Item2*.</span><span class="sxs-lookup"><span data-stu-id="92563-343">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="92563-344">Valige toimingupaani vahekaardi **Varude haldamine** grupis **Kuva** suvand **Vaba kaubavaru**.</span><span class="sxs-lookup"><span data-stu-id="92563-344">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="92563-345">Seejärel valige **Koguse korrigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="92563-345">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="92563-346">Korrigeerige uute kaupade vaba kaubavaru järgmises tabelis täpsustatud viisil.</span><span class="sxs-lookup"><span data-stu-id="92563-346">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="92563-347">Üksus</span><span class="sxs-lookup"><span data-stu-id="92563-347">Item</span></span>  | <span data-ttu-id="92563-348">Ladu</span><span class="sxs-lookup"><span data-stu-id="92563-348">Warehouse</span></span> | <span data-ttu-id="92563-349">Koht</span><span class="sxs-lookup"><span data-stu-id="92563-349">Location</span></span> | <span data-ttu-id="92563-350">Litsentsiplaat</span><span class="sxs-lookup"><span data-stu-id="92563-350">License plate</span></span> | <span data-ttu-id="92563-351">Kogus</span><span class="sxs-lookup"><span data-stu-id="92563-351">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="92563-352">Item1</span><span class="sxs-lookup"><span data-stu-id="92563-352">Item1</span></span> | <span data-ttu-id="92563-353">24</span><span class="sxs-lookup"><span data-stu-id="92563-353">24</span></span>        | <span data-ttu-id="92563-354">FL-010</span><span class="sxs-lookup"><span data-stu-id="92563-354">FL-010</span></span>   | <span data-ttu-id="92563-355">LP01</span><span class="sxs-lookup"><span data-stu-id="92563-355">LP01</span></span>          | <span data-ttu-id="92563-356">10</span><span class="sxs-lookup"><span data-stu-id="92563-356">10</span></span>       |
    | <span data-ttu-id="92563-357">Item1</span><span class="sxs-lookup"><span data-stu-id="92563-357">Item1</span></span> | <span data-ttu-id="92563-358">24</span><span class="sxs-lookup"><span data-stu-id="92563-358">24</span></span>        | <span data-ttu-id="92563-359">FL-011</span><span class="sxs-lookup"><span data-stu-id="92563-359">FL-011</span></span>   | <span data-ttu-id="92563-360">LP02</span><span class="sxs-lookup"><span data-stu-id="92563-360">LP02</span></span>          | <span data-ttu-id="92563-361">10</span><span class="sxs-lookup"><span data-stu-id="92563-361">10</span></span>       |
    | <span data-ttu-id="92563-362">Item2</span><span class="sxs-lookup"><span data-stu-id="92563-362">Item2</span></span> | <span data-ttu-id="92563-363">24</span><span class="sxs-lookup"><span data-stu-id="92563-363">24</span></span>        | <span data-ttu-id="92563-364">FL-010</span><span class="sxs-lookup"><span data-stu-id="92563-364">FL-010</span></span>   | <span data-ttu-id="92563-365">LP01</span><span class="sxs-lookup"><span data-stu-id="92563-365">LP01</span></span>          | <span data-ttu-id="92563-366">5</span><span class="sxs-lookup"><span data-stu-id="92563-366">5</span></span>        |
    | <span data-ttu-id="92563-367">Item2</span><span class="sxs-lookup"><span data-stu-id="92563-367">Item2</span></span> | <span data-ttu-id="92563-368">24</span><span class="sxs-lookup"><span data-stu-id="92563-368">24</span></span>        | <span data-ttu-id="92563-369">FL-011</span><span class="sxs-lookup"><span data-stu-id="92563-369">FL-011</span></span>   | <span data-ttu-id="92563-370">LP02</span><span class="sxs-lookup"><span data-stu-id="92563-370">LP02</span></span>          | <span data-ttu-id="92563-371">5</span><span class="sxs-lookup"><span data-stu-id="92563-371">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="92563-372">Peate looma need kaks litsentsiplaati ja kasutama asukohti, mis lubavad segakaupu, nt *FL-010* ja *FL-011*.</span><span class="sxs-lookup"><span data-stu-id="92563-372">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="92563-373">Müügitellimuse loomine ja kindla litsentsiplaadi reserveerimine</span><span class="sxs-lookup"><span data-stu-id="92563-373">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="92563-374">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="92563-374">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="92563-375">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="92563-375">Select **New**.</span></span>
1. <span data-ttu-id="92563-376">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="92563-376">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="92563-377">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="92563-377">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="92563-378">**Ladu:** *24*</span><span class="sxs-lookup"><span data-stu-id="92563-378">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="92563-379">Valige **OK** , et sulgeda dialoogiboks **Müügitellimuse loomine** ja avada uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="92563-379">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="92563-380">Lisage kiirkaardil **Müügitellimuse read** järgmiste sätetega rida.</span><span class="sxs-lookup"><span data-stu-id="92563-380">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="92563-381">**Kaubakood:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="92563-381">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="92563-382">**Kogus:** *10*</span><span class="sxs-lookup"><span data-stu-id="92563-382">**Quantity:** *10*</span></span>

1. <span data-ttu-id="92563-383">Lisage teine järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="92563-383">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="92563-384">**Kaubakood:** *Item2*</span><span class="sxs-lookup"><span data-stu-id="92563-384">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="92563-385">**Kogus:** *5*</span><span class="sxs-lookup"><span data-stu-id="92563-385">**Quantity:** *5*</span></span>

1. <span data-ttu-id="92563-386">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="92563-386">Select **Save**.</span></span>
1. <span data-ttu-id="92563-387">Avage kiirkaardil **Rea üksikasjad** vahekaart **Seadistus** ja märkige üles iga rea **Partii ID** väärtus.</span><span class="sxs-lookup"><span data-stu-id="92563-387">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="92563-388">Neid väärtuseid on vaja kindlate litsentsiplaatide reserveerimisel.</span><span class="sxs-lookup"><span data-stu-id="92563-388">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="92563-389">Kindla litsentsiplaadi reserveerimiseks peate kasutama andmeüksust **Tellimusega seotud reserveeringud litsentsiplaadi kohta**.</span><span class="sxs-lookup"><span data-stu-id="92563-389">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="92563-390">Kindlas litsentsiplaadis partiijälgimisega kauba reserveerimiseks saate kasutada ka lehte **Partii reserveerimine** , nagu on kirjeldatud jaotises [Müügitellimuse üksikasjade sisestamine](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="92563-390">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="92563-391">Kui sisestate litsentsiplaadi otse müügitellimuse real ja kinnitate selle süsteemi, ei kasutata selle rea puhul laohalduse töötlemist.</span><span class="sxs-lookup"><span data-stu-id="92563-391">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="92563-392">Valige **Ava Microsoft Office'is** , valige **Tellimusega seotud reserveeringud litsentsiplaadi kohta** ja laadige fail alla.</span><span class="sxs-lookup"><span data-stu-id="92563-392">Select **Open in Microsoft Office** , select **Order-committed reservations per license plate** , and download the file.</span></span>
1. <span data-ttu-id="92563-393">Avage allalaaditud fail Excelis ja valige **Luba redigeerimine** , et lubada Exceli lisandmooduli käivitamine.</span><span class="sxs-lookup"><span data-stu-id="92563-393">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="92563-394">Kui käivitate Exceli lisandmooduli esimest korda, valige käsk **Usalda seda lisandmoodulit**.</span><span class="sxs-lookup"><span data-stu-id="92563-394">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="92563-395">Kui teil palutakse sisse logida, valige **Logi sisse** ja seejärel logige sisse, kasutades sama identimisteavet, mida kasutasite rakendusse Supply Chain Management sisselogimisel.</span><span class="sxs-lookup"><span data-stu-id="92563-395">If you're prompted to sign in, select **Sign in** , and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="92563-396">Kauba reserveerimiseks kindlas litsentsiplaadis valige Exceli lisandmoodulis **Uus** , et lisada reserveerimisrida ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="92563-396">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="92563-397">**Partii ID:** sisestage **Partii ID** väärtus, mille leidsite kauba *Item1* müügitellimuse realt.</span><span class="sxs-lookup"><span data-stu-id="92563-397">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="92563-398">**Litsentsiplaat:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="92563-398">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="92563-399">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="92563-399">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="92563-400">Valige **Uus** , et lisada uus reserveerimisrida ja määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="92563-400">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="92563-401">**Partii ID:** sisestage **Partii ID** väärtus, mille leidsite kauba *Item2* müügitellimuse realt.</span><span class="sxs-lookup"><span data-stu-id="92563-401">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="92563-402">**Litsentsiplaat:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="92563-402">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="92563-403">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="92563-403">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="92563-404">Valige Exceli lisandmoodulis **Avalda** , et saata andmed tagasi Supply Chain Managementi.</span><span class="sxs-lookup"><span data-stu-id="92563-404">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="92563-405">Reserveerimisrida kuvatakse süsteemis ainult juhul, kui avaldamine on tõrgeteta lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="92563-405">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="92563-406">Minge tagasi Supply Chain Managementi.</span><span class="sxs-lookup"><span data-stu-id="92563-406">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="92563-407">Kauba reserveeringu läbivaatamiseks valige kiirkaardil **Müügitellimuse read** menüüst **Varud** suvand **Halda \> Reserveering**.</span><span class="sxs-lookup"><span data-stu-id="92563-407">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="92563-408">Pange tähele, et kauba *Item1* müügitellimuse rea puhul on reserveeritud kogus *10* ja kauba *Item2* müügitellimuse rea puhul on kogus *5*.</span><span class="sxs-lookup"><span data-stu-id="92563-408">Notice that, for the sales order line for *Item1* , inventory of *10* is reserved, and for the sales order line for *Item2* , inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="92563-409">Müügitellimuse rea reserveeringuga seotud laokannete ülevaatamiseks valige kiirkaardil **Müügitellimuse read** menüüst **Varud** suvand **Kuva \> Kanded**.</span><span class="sxs-lookup"><span data-stu-id="92563-409">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="92563-410">Pange tähele, et reserveeringuga on seotud kaks kannet: üks, mille välja **Viide** väärtuseks on seatud *Müügitellimus* , ja üks, mille välja **Viide** väärtuseks on seatud *Tellimusega seotud reserveering*.</span><span class="sxs-lookup"><span data-stu-id="92563-410">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="92563-411">Kanne, mille välja **Viide** väärtuseks on seatud *Müügitellimus* , näitab tellimuse rea reserveeringut varude dimensioonide jaoks, mis on üle taseme **Asukoht** (sait, ladu ja varude olek).</span><span class="sxs-lookup"><span data-stu-id="92563-411">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="92563-412">Kanne, mille välja **Viide** väärtuseks on seatud *Tellimusega seotud reserveering* , näitab konkreetse litsentsiplaadi ja asukoha tellimuse rea reserveeringut.</span><span class="sxs-lookup"><span data-stu-id="92563-412">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="92563-413">Müügitellimuse vabastamiseks valige toimingupaanil vahekaardi **Ladu** grupist **Tegevused** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="92563-413">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="92563-414">Määratud tellimusega seotud litsentsiplaatidega laotöö ülevaatamine ja töötlemine</span><span class="sxs-lookup"><span data-stu-id="92563-414">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="92563-415">Valige kiirkaardil **Müügitellimuse read** menüüst **Ladu** suvand **Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="92563-415">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="92563-416">Litsentsiplaadi reserveerimist kasutava müügitellimuse jaoks tööd luues ei kasuta süsteem asukohakorraldusi, nagu ka siis, kui reserveerimine toimub kindla partii raames.</span><span class="sxs-lookup"><span data-stu-id="92563-416">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="92563-417">Kuna tellimusega seotud reserveeringus on täpsustatud kõik varude dimensioonid, sealhulgas asukoht, ei pea kasutama asukohakorraldusi, kuna need varude dimensioonid sisestatakse lihtsalt töösse.</span><span class="sxs-lookup"><span data-stu-id="92563-417">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="92563-418">Need kuvatakse jaotises **Varude dimensioonidest** lehel **Töö laokanded**.</span><span class="sxs-lookup"><span data-stu-id="92563-418">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="92563-419">Pärast töö loomist eemaldatakse kauba laokanne, mille välja **Viide** väärtus on *Tellimusega seotud reserveering*.</span><span class="sxs-lookup"><span data-stu-id="92563-419">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="92563-420">Laokannete puhul, mille välja **Viide** väärtuseks on seatud *Töö* , on nüüd füüsiline reserveering määratud koguse kõigi varude dimensioonide jaoks.</span><span class="sxs-lookup"><span data-stu-id="92563-420">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="92563-421">Lõpetage mobiilses seadmes komplekteerimine ja töö sisestamine menüükäsu abil, mille märkeruut **Käitle litsentsiplaadi põhjal** on valitud.</span><span class="sxs-lookup"><span data-stu-id="92563-421">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="92563-422">Funktsioon **Käitle litsentsiplaadi põhjal** aitab teil töödelda kogu litsentsiplaati.</span><span class="sxs-lookup"><span data-stu-id="92563-422">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="92563-423">Kui peate töötlema vaid osa litsentsiplaadist, ei saa te seda funktsiooni kasutada.</span><span class="sxs-lookup"><span data-stu-id="92563-423">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="92563-424">Soovitame iga litsentsiplaadi jaoks luua eraldi töö.</span><span class="sxs-lookup"><span data-stu-id="92563-424">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="92563-425">Selle tulemuse saavutamiseks kasutage funktsiooni **Tööpäise piirid** , mis asub lehel **Töömall**.</span><span class="sxs-lookup"><span data-stu-id="92563-425">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="92563-426">Litsentsiplaat *LP02* on nüüd müügitellimuse ridadele komplekteeritud ja pandud asukohta *Laadimisuks*.</span><span class="sxs-lookup"><span data-stu-id="92563-426">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="92563-427">Nüüd on see laadimiseks ja kliendile lähetamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="92563-427">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="92563-428">Tellitud ja kooskõlastatud partiinumbritega laotööde ülevaatamise ja töötlemise erandid</span><span class="sxs-lookup"><span data-stu-id="92563-428">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="92563-429">Laotöö komplekteerimiseks tellitud partii numbrite suhtes kehtivad samad standardse lao erandi käsitlemise protsessid ja toimingud, mis tavatöö puhul.</span><span class="sxs-lookup"><span data-stu-id="92563-429">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="92563-430">Üldiselt saab avatud töö või töörea tühistada ja katkestada, kui kasutaja asukoht on täis, see võib olla lühike-komplekteeritud ja seda saab liikumise tõttu uuendada.</span><span class="sxs-lookup"><span data-stu-id="92563-430">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="92563-431">Samuti saab vähendada juba lõpetatud töö komplekteeritud kogust või seda tööd muuta.</span><span class="sxs-lookup"><span data-stu-id="92563-431">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="92563-432">Järgmist põhireeglit rakendatakse kõigile nende erandite käsitlemise toimingutele: kliendile reserveeritud partiinumbrit ei saa kunagi asendada teise partii numbriga, kuid selle ladustamise dimensioone (asukoht ja litsentsiplaat) saab muuta, selleks peab kasutaja seda käsitsi värskendama või süsteem automaatselt uuendama.</span><span class="sxs-lookup"><span data-stu-id="92563-432">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="92563-433">Automaatne värskendamine põhineb samadel juhusliku määramisega ladustamise dimensioonidel, mida rakendatakse, kui kindel partii on automaatselt reserveeritud, kuid ladustamise dimensioone ei määratud.</span><span class="sxs-lookup"><span data-stu-id="92563-433">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="92563-434">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="92563-434">Example scenario</span></span>

<span data-ttu-id="92563-435">Selle stsenaariumi näide on olukord, kus varem lõpetatud töö on funktsiooni **Vähenda komplekteeritud kogust** kasutamisel komplekteerimata.</span><span class="sxs-lookup"><span data-stu-id="92563-435">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="92563-436">Selles näites eeldatakse, et olete juba lõpetanud sammud, mida kirjeldatakse jaotises [Näidisstsenaarium: partiinumbri määramine](#Example-batch-allocation).</span><span class="sxs-lookup"><span data-stu-id="92563-436">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="92563-437">Tegevus jätkub pärast toda näidet.</span><span class="sxs-lookup"><span data-stu-id="92563-437">It continues from that example.</span></span>

1. <span data-ttu-id="92563-438">Avage **Laohaldus** \> **Koormad** \> **Aktiivsed koormad**.</span><span class="sxs-lookup"><span data-stu-id="92563-438">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="92563-439">Valige koorem, mis loodi seoses teie müügitellimuse saadetisega.</span><span class="sxs-lookup"><span data-stu-id="92563-439">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="92563-440">Kiirkaardilt **Koorma tellimuse read** valige käsk **Vähenda komplekteeritud kogust**.</span><span class="sxs-lookup"><span data-stu-id="92563-440">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="92563-441">Valige lehel **Vähenda komplekteeritud kogust** välja **Teisalda asukohta** väärtuseks **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="92563-441">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="92563-442">Väljal **Teisalda litsentsiplaadile** valige väärtus **LP33**.</span><span class="sxs-lookup"><span data-stu-id="92563-442">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="92563-443">Sisestage ruudustiku väljale **Varude kogus väljale komplekteerimata** väärtus **10**.</span><span class="sxs-lookup"><span data-stu-id="92563-443">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="92563-444">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="92563-444">Select **OK**.</span></span>

<span data-ttu-id="92563-445">Siin on komplekteerimise tegevuse tulemused.</span><span class="sxs-lookup"><span data-stu-id="92563-445">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="92563-446">Varem suletud töö olek on seatud väärtusele **Tühistatud**.</span><span class="sxs-lookup"><span data-stu-id="92563-446">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="92563-447">Tüübi **Varude liikumine** uus töö luuakse komplekteerimata kogusega **10** partiinumbri **B11** jaoks.</span><span class="sxs-lookup"><span data-stu-id="92563-447">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="92563-448">See töö näitab liikumist asukohast **Baydoor** litsentsiplaadile **LP33** asukohas **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="92563-448">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="92563-449">Olek on seatud väärtusele **Suletud**.</span><span class="sxs-lookup"><span data-stu-id="92563-449">The status is set to **Closed**.</span></span>
- <span data-ttu-id="92563-450">Süsteem reserveerib algselt tellitud partiinumbri uuesti ja määrab asukoha ja litsentsiplaadi ID-d.</span><span class="sxs-lookup"><span data-stu-id="92563-450">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="92563-451">(See protsess on samaväärne funktsiooni **Reserveeri rida** käitamisega antud partiinumbri puhul).</span><span class="sxs-lookup"><span data-stu-id="92563-451">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="92563-452">Selle tulemusel näidatakse partii **B11** määratuna kiirkaardi **Lähtereale kinnitatud partiinumbrid** lehele **Partii reserveerimine** ja väli **Reserveerimine** sisaldab kogust **10** partiinumbri **B11** jaoks.</span><span class="sxs-lookup"><span data-stu-id="92563-452">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="92563-453">Lisaks on välja **Asukoht** väärtuseks **FL-001** ja välja **Litsentsiplaat** väärtuseks on seatud **LP11**.</span><span class="sxs-lookup"><span data-stu-id="92563-453">Additionally, the **Location** field is set to **FL-001** , and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="92563-454">(Kui neid ei ole näha, saate need väljad ruudustikku lisada.)</span><span class="sxs-lookup"><span data-stu-id="92563-454">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="92563-455">Järgmised tabelid annavad ülevaate sellest, kuidas süsteem käsitleb kindla lao tegevuste tellimusega kooskõlastatud partii reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="92563-455">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="92563-456">Tabelite sisu tõlgendamiseks oletame, et iga laotoiming käivitatakse tellimusega seotud partii reserveerimisest tuleneva olemasoleva laotöö kontekstis või et iga laotoimingu käivitamine mõjutab seda tüüpi tööd.</span><span class="sxs-lookup"><span data-stu-id="92563-456">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="92563-457">Neis tabelites näitab veerg Partii kogus on saadaval, kas partii kogus on saadaval lisaks kogusele, mis on juba reserveeritud praeguse tellimusega seotud reserveeringutele, või on juba reserveeritud laotööst, mis pärineb selle tüübi reserveeringutest.</span><span class="sxs-lookup"><span data-stu-id="92563-457">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="92563-458">Avatud tööde komplekteerimise asukoha alistamine</span><span class="sxs-lookup"><span data-stu-id="92563-458">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92563-459">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="92563-459">Key setup parameter</span></span></th>
<th><span data-ttu-id="92563-460">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="92563-460">Batch quantity is available</span></span></th>
<th><span data-ttu-id="92563-461">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="92563-461">Key user steps</span></span></th>
<th><span data-ttu-id="92563-462">Laotöö</span><span class="sxs-lookup"><span data-stu-id="92563-462">Warehouse work</span></span></th>
<th><span data-ttu-id="92563-463">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="92563-463">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="92563-464">Suvand <strong>Luba komplekteerimise asukoha alistamine</strong> on töötajale lubatud.</span><span class="sxs-lookup"><span data-stu-id="92563-464">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="92563-465">Jah</span><span class="sxs-lookup"><span data-stu-id="92563-465">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-466">Valige suvand <strong>Alista asukoht</strong> laorakenduses, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="92563-466">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="92563-467">Valige <strong>Soovita</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-467">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="92563-468">Kinnitage uus asukoht, mis on soovitatud partii koguse kättesaadavuse alusel.</span><span class="sxs-lookup"><span data-stu-id="92563-468">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="92563-469">Praeguse töö puhul toimuvad järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="92563-469">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="92563-470">Komplekteerimise real olev asukoht uuendatakse uude asukohta.</span><span class="sxs-lookup"><span data-stu-id="92563-470">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="92563-471">(Kui asukoha määrab litsentsiplaat, on töölao kandele määratud juhuslik litsentsiplaat ja töötaja saab valida mis tahes saadaoleva kogusega litsentsiplaadi.)</span><span class="sxs-lookup"><span data-stu-id="92563-471">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="92563-472">Kui kogus leitakse uues asukohas rohkem kui ühel litsentsiplaadil, jaotatakse algse komplekteerimise rida mitmeks reaks, et see vastaks igale litsentsiplaadile.</span><span class="sxs-lookup"><span data-stu-id="92563-472">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="92563-473">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="92563-473">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-474">Ei</span><span class="sxs-lookup"><span data-stu-id="92563-474">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-475">Valige suvand <strong>Alista asukoht</strong> laorakenduses, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="92563-475">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="92563-476">Sisestage asukoht käsitsi.</span><span class="sxs-lookup"><span data-stu-id="92563-476">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="92563-477">Toiming <strong>Asukoha alistamine</strong> pole võimalik.</span><span class="sxs-lookup"><span data-stu-id="92563-477">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="92563-478">See nurjub ja kuvatakse tõrge.</span><span class="sxs-lookup"><span data-stu-id="92563-478">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="92563-479">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="92563-479">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="92563-480">Nupp Täis – jaotab töörea kasutaja asukoha ületäitumise tõttu</span><span class="sxs-lookup"><span data-stu-id="92563-480">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92563-481">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="92563-481">Key setup parameter</span></span></th>
<th><span data-ttu-id="92563-482">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="92563-482">Batch quantity is available</span></span></th>
<th><span data-ttu-id="92563-483">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="92563-483">Key user steps</span></span></th>
<th><span data-ttu-id="92563-484">Laotöö</span><span class="sxs-lookup"><span data-stu-id="92563-484">Warehouse work</span></span></th>
<th><span data-ttu-id="92563-485">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="92563-485">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="92563-486">Valik <strong>Luba töö jaotamine</strong> on lubatud mobiilseadme menüükäsul.</span><span class="sxs-lookup"><span data-stu-id="92563-486">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="92563-487">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="92563-487">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-488">Valige laorakenduses menüüsuvand <strong>Täis</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="92563-488">Select the <strong>Full</strong> menu item on the warehouse app when you process picking work.</span></span></li>
<li><span data-ttu-id="92563-489">Sisestage väljale <strong>Komplekteeri kogus</strong> nõutava komplekteerimise osaline kogus, et näidata kogu võimsust.</span><span class="sxs-lookup"><span data-stu-id="92563-489">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="92563-490">Praeguse töö puhul uuendatakse kogus järelejäänud kogusele, mis tuleb komplekteerida.</span><span class="sxs-lookup"><span data-stu-id="92563-490">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="92563-491">Komplekteeritud koguse uus töö luuakse ja suletakse.</span><span class="sxs-lookup"><span data-stu-id="92563-491">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="92563-492">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="92563-492">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="92563-493">Lõpetatud töö komplekteeritud koguse vähendamine (koormast)</span><span class="sxs-lookup"><span data-stu-id="92563-493">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92563-494">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="92563-494">Key setup parameter</span></span></th>
<th><span data-ttu-id="92563-495">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="92563-495">Batch quantity is available</span></span></th>
<th><span data-ttu-id="92563-496">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="92563-496">Key user steps</span></span></th>
<th><span data-ttu-id="92563-497">Laotöö</span><span class="sxs-lookup"><span data-stu-id="92563-497">Warehouse work</span></span></th>
<th><span data-ttu-id="92563-498">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="92563-498">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="92563-499">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="92563-499">Not applicable</span></span></td>
<td><span data-ttu-id="92563-500">Jah</span><span class="sxs-lookup"><span data-stu-id="92563-500">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-501">Avage koorma realt leht <strong>Komplekteeritud koguse vähendamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-501">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="92563-502">Sisestage kogu kogus, mis ei lähe komplekteerimisele.</span><span class="sxs-lookup"><span data-stu-id="92563-502">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="92563-503">Valige teisaldamiseks asukoht/litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="92563-503">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="92563-504">Koorma reaga seotud töö on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="92563-504">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="92563-505">Varude teisaldamiseks luuakse uus töö ja suletakse.</span><span class="sxs-lookup"><span data-stu-id="92563-505">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="92563-506">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="92563-506">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="92563-507">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="92563-507">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-508">Ei</span><span class="sxs-lookup"><span data-stu-id="92563-508">No</span></span></td>
<td><span data-ttu-id="92563-509">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="92563-509">See the previous row.</span></span></td>
<td><span data-ttu-id="92563-510">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="92563-510">See the previous row.</span></span></td>
<td><span data-ttu-id="92563-511">Kogus reserveeritakse samale partiile samas asukohas ja litsentsiplaadiga (kui asukoht on litsentsiplaadi kontrollitud), mis sisestati komplekteerimise ajal.</span><span class="sxs-lookup"><span data-stu-id="92563-511">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="92563-512">Kauba teisaldamine laos</span><span class="sxs-lookup"><span data-stu-id="92563-512">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="92563-513">See laotoiming rakendub ainult tüübi **Töö loomise protsess** teisaldamistele, mitte malli alusel teisaldamistele.</span><span class="sxs-lookup"><span data-stu-id="92563-513">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92563-514">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="92563-514">Key setup parameter</span></span></th>
<th><span data-ttu-id="92563-515">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="92563-515">Batch quantity is available</span></span></th>
<th><span data-ttu-id="92563-516">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="92563-516">Key user steps</span></span></th>
<th><span data-ttu-id="92563-517">Laotöö</span><span class="sxs-lookup"><span data-stu-id="92563-517">Warehouse work</span></span></th>
<th><span data-ttu-id="92563-518">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="92563-518">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="92563-519">Töötaja saab <strong>lubada seotud töö varude teisaldamist</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-519">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="92563-520">Jah</span><span class="sxs-lookup"><span data-stu-id="92563-520">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-521">Alustage teisaldamist laorakenduses.</span><span class="sxs-lookup"><span data-stu-id="92563-521">Start a movement on the warehouse app.</span></span></li>
<li><span data-ttu-id="92563-522">Sisestage alg- ja lõppasukohad.</span><span class="sxs-lookup"><span data-stu-id="92563-522">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="92563-523">Kõigi olemasolevate tööde puhul, mida teisaldamine mõjutab, uuendatakse komplekteerimise asukoht uude asukohta.</span><span class="sxs-lookup"><span data-stu-id="92563-523">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="92563-524">Varude teisaldamiseks luuakse uus töö ja suletakse.</span><span class="sxs-lookup"><span data-stu-id="92563-524">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="92563-525">Kõik olemasolevad reserveeringud, mis mõjutavad koguse liikumist antud asukohast, reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="92563-525">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="92563-526">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="92563-526">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-527">Ei</span><span class="sxs-lookup"><span data-stu-id="92563-527">No</span></span></td>
<td><span data-ttu-id="92563-528">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="92563-528">See the previous row.</span></span></td>
<td><span data-ttu-id="92563-529">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="92563-529">See the previous row.</span></span></td>
<td><span data-ttu-id="92563-530">Kõik olemasolevad reserveeringud, mis mõjutavad koguse liikumist antud asukohast, reserveeritakse uuesti sama partii ja uue asukoha ning litsentsiplaadi jaoks (kui asukoht on litsentsiplaadi kontrollitud).</span><span class="sxs-lookup"><span data-stu-id="92563-530">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="92563-531">Lõpetatud töö komplekteeritud koguse vähendamine (koormast või voost)</span><span class="sxs-lookup"><span data-stu-id="92563-531">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92563-532">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="92563-532">Key setup parameter</span></span></th>
<th><span data-ttu-id="92563-533">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="92563-533">Batch quantity is available</span></span></th>
<th><span data-ttu-id="92563-534">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="92563-534">Key user steps</span></span></th>
<th><span data-ttu-id="92563-535">Laotöö</span><span class="sxs-lookup"><span data-stu-id="92563-535">Warehouse work</span></span></th>
<th><span data-ttu-id="92563-536">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="92563-536">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="92563-537">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="92563-537">Not applicable</span></span></td>
<td><span data-ttu-id="92563-538">Jah</span><span class="sxs-lookup"><span data-stu-id="92563-538">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-539">Avage leht <strong>Tühistatud töö</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-539">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="92563-540">Taotlemise lehel märkige ruut <strong>Jäta kaubad praegusesse asukohta</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-540">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="92563-541">Koorma reaga seotud kõik tööd on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="92563-541">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="92563-542">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="92563-542">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="92563-543">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="92563-543">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-544">Ei</span><span class="sxs-lookup"><span data-stu-id="92563-544">No</span></span></td>
<td><span data-ttu-id="92563-545">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="92563-545">See the previous row.</span></span></td>
<td><span data-ttu-id="92563-546">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="92563-546">See the previous row.</span></span></td>
<td><span data-ttu-id="92563-547">Kogus reserveeritakse samale partiile ja asukohale ning litsentsiplaadile, kuhu kogus tühistamisel jäeti.</span><span class="sxs-lookup"><span data-stu-id="92563-547">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-548">Jah</span><span class="sxs-lookup"><span data-stu-id="92563-548">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-549">Avage leht <strong>Tühistatud töö</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-549">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="92563-550">Taotlemise lehel märkige ruut <strong>Määra kaubad sellesse asukohta</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-550">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="92563-551">Praegune töö on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="92563-551">The current work is canceled.</span></span></li>
<li><span data-ttu-id="92563-552">Varude teisaldamiseks luuakse uus töö ja suletakse.</span><span class="sxs-lookup"><span data-stu-id="92563-552">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="92563-553">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="92563-553">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="92563-554">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="92563-554">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-555">Ei</span><span class="sxs-lookup"><span data-stu-id="92563-555">No</span></span></td>
<td><span data-ttu-id="92563-556">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="92563-556">See the previous row.</span></span></td>
<td><span data-ttu-id="92563-557">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="92563-557">See the previous row.</span></span></td>
<td><span data-ttu-id="92563-558">Kogus reserveeritakse samale partiile ja asukohale ning litsentsiplaadile, kuhu kogus tühistamisel määrati.</span><span class="sxs-lookup"><span data-stu-id="92563-558">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-559">Jah/ei</span><span class="sxs-lookup"><span data-stu-id="92563-559">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-560">Avage leht <strong>Tühistatud töö</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-560">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="92563-561">Taotlemise lehel märkige ruut <strong>Teisalda kaubad sellesse asukohta</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-561">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="92563-562">Tühistamist ei toetata.</span><span class="sxs-lookup"><span data-stu-id="92563-562">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="92563-563">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="92563-563">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-564">Jah/ei</span><span class="sxs-lookup"><span data-stu-id="92563-564">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-565">Avage leht <strong>Tühistatud töö</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-565">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="92563-566">Taotlemise lehel märkige ruut <strong>Teisalda kaubad asukoha direktiivi kohaselt</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-566">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="92563-567">Tühistamist ei toetata.</span><span class="sxs-lookup"><span data-stu-id="92563-567">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="92563-568">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="92563-568">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="92563-569">Koguse lühiajaline komplekteerimine – registreerige kogus komplekteerimise ajal asukohas/litsentsiplaadil kui füüsiliselt leidmata.</span><span class="sxs-lookup"><span data-stu-id="92563-569">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92563-570">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="92563-570">Key setup parameter</span></span></th>
<th><span data-ttu-id="92563-571">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="92563-571">Batch quantity is available</span></span></th>
<th><span data-ttu-id="92563-572">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="92563-572">Key user steps</span></span></th>
<th><span data-ttu-id="92563-573">Laotöö</span><span class="sxs-lookup"><span data-stu-id="92563-573">Warehouse work</span></span></th>
<th><span data-ttu-id="92563-574">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="92563-574">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="92563-575">Töö erandi tüübiks on seadistatud<strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>puudub</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-575">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="92563-576">Jah</span><span class="sxs-lookup"><span data-stu-id="92563-576">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-577">Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="92563-577">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="92563-578">Sisestage väljale <strong>Komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="92563-578">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="92563-579">Väljale <strong>Põhjus</strong> sisestage väärtus <strong>Ümberjaotamine puudub</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-579">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="92563-580">Praegune töö on suletud ja komplekteeritud kogus on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="92563-580">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="92563-581">Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</span><span class="sxs-lookup"><span data-stu-id="92563-581">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="92563-582">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="92563-582">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="92563-583">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="92563-583">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-584">Ei</span><span class="sxs-lookup"><span data-stu-id="92563-584">No</span></span></td>
<td><span data-ttu-id="92563-585">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="92563-585">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="92563-586">Lühikese komplekteerimise toiming nurjub ja kuvatakse tõrge.</span><span class="sxs-lookup"><span data-stu-id="92563-586">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="92563-587">Praegune töö jääb avatuks.</span><span class="sxs-lookup"><span data-stu-id="92563-587">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="92563-588">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="92563-588">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="92563-589">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Puudub</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-589">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="92563-590">Jah</span><span class="sxs-lookup"><span data-stu-id="92563-590">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-591">Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="92563-591">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="92563-592">Sisestage väljale <strong>Komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="92563-592">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="92563-593">Väljale <strong>Põhjus</strong> sisestage väärtus <strong>Ümberjaotamine puudub</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-593">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="92563-594">Praegune töö on suletud ja komplekteeritud kogus on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="92563-594">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="92563-595">Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</span><span class="sxs-lookup"><span data-stu-id="92563-595">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="92563-596">Kõik olemasolevad reserveeringud, mis mõjutavad koguse kohandamist lühikese komplekteerimise asukohast, reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="92563-596">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="92563-597">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="92563-597">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-598">Ei</span><span class="sxs-lookup"><span data-stu-id="92563-598">No</span></span></td>
<td><span data-ttu-id="92563-599">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="92563-599">See the previous row.</span></span></td>
<td><span data-ttu-id="92563-600">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="92563-600">See the previous row.</span></span></td>
<td><span data-ttu-id="92563-601">Kõik olemasolevad reserveeringud, mis mõjutavad koguse kohandamist lühikese komplekteerimise asukohast, eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="92563-601">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-602">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Käsitsi</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah/ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-602">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="92563-603">Lisaks saavad töötajad kasutada suvandit <strong>Luba kauba käsitsi ümberjaotamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-603">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="92563-604">Jah</span><span class="sxs-lookup"><span data-stu-id="92563-604">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-605">Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="92563-605">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="92563-606">Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="92563-606">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="92563-607">Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos käsitsi ümberjaotamisega</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-607">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="92563-608">Valige loendist asukoht/litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="92563-608">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="92563-609">Praeguse töö puhul toimuvad järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="92563-609">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="92563-610">Praegune komplekteerimise rida on suletud ja komplekteeritud kogus on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="92563-610">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="92563-611">Asetusrida on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="92563-611">The put line is canceled.</span></span></li>
<li><span data-ttu-id="92563-612">Luuakse uus komplekteerimise rida.</span><span class="sxs-lookup"><span data-stu-id="92563-612">A new pick line is created.</span></span> <span data-ttu-id="92563-613">See kasutab kasutaja valitud asukohta/litsentsiplaati.</span><span class="sxs-lookup"><span data-stu-id="92563-613">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="92563-614">Luuakse uus asetusrida.</span><span class="sxs-lookup"><span data-stu-id="92563-614">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="92563-615">Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</span><span class="sxs-lookup"><span data-stu-id="92563-615">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="92563-616">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="92563-616">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-617">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Käsitsi</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-617">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="92563-618">Lisaks saavad töötajad kasutada suvandit <strong>Luba kauba käsitsi ümberjaotamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-618">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="92563-619">Ei</span><span class="sxs-lookup"><span data-stu-id="92563-619">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-620">Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="92563-620">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="92563-621">Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="92563-621">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="92563-622">Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos käsitsi ümberjaotamisega</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-622">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="92563-623">Lühikese komplekteerimise toiming nurjub ja kuvatakse tõrge.</span><span class="sxs-lookup"><span data-stu-id="92563-623">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="92563-624">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="92563-624">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-625">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Käsitsi</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-625">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="92563-626">Lisaks saavad töötajad kasutada suvandit <strong>Luba kauba käsitsi ümberjaotamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-626">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="92563-627">Ei</span><span class="sxs-lookup"><span data-stu-id="92563-627">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-628">Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="92563-628">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="92563-629">Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="92563-629">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="92563-630">Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos käsitsi ümberjaotamisega</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-630">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="92563-631">Valige loendist asukoht/litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="92563-631">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="92563-632">Praeguse töö puhul toimuvad järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="92563-632">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="92563-633">Praegune komplekteerimise rida on suletud ja komplekteeritud kogus on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="92563-633">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="92563-634">Asetusrida on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="92563-634">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="92563-635">Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</span><span class="sxs-lookup"><span data-stu-id="92563-635">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="92563-636">Kõik olemasolevad reserveeringud, mis mõjutavad koguse kohandamist lühikese komplekteerimise asukohast/litsentsiplaadilt, eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="92563-636">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-637">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Automaatne</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah/ei</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah/ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-637">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="92563-638">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="92563-638">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-639">Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="92563-639">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="92563-640">Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="92563-640">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="92563-641">Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos automaatse ümberjaotamisega</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-641">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="92563-642">Lühiajalist komplekteerimist, mis hõlmab automaatset ümberjaotamist, ei toetata.</span><span class="sxs-lookup"><span data-stu-id="92563-642">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="92563-643">Lühiajalist komplekteerimist, mis hõlmab automaatset ümberjaotamist, ei toetata.</span><span class="sxs-lookup"><span data-stu-id="92563-643">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="92563-644">Muuda varude olekut</span><span class="sxs-lookup"><span data-stu-id="92563-644">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="92563-645">Seda laotoimingut saab sooritada mitmest kirjest.</span><span class="sxs-lookup"><span data-stu-id="92563-645">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="92563-646">Siin kuvatud näites kasutatakse toimingut **Varude oleku muutmine** lehe **Vaba asukoht** alusel.</span><span class="sxs-lookup"><span data-stu-id="92563-646">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="92563-647">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="92563-647">Key setup parameter</span></span></th>
<th><span data-ttu-id="92563-648">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="92563-648">Batch quantity is available</span></span></th>
<th><span data-ttu-id="92563-649">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="92563-649">Key user steps</span></span></th>
<th><span data-ttu-id="92563-650">Laotöö</span><span class="sxs-lookup"><span data-stu-id="92563-650">Warehouse work</span></span></th>
<th><span data-ttu-id="92563-651">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="92563-651">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="92563-652">Vahekaardil <strong>Ladu</strong>, kirjes <strong>Ladu</strong> on välja <strong>Eemalda reserveeringud ja märgised</strong> väärtuseks määratud <strong>Reserveeringud</strong> või <strong>Märgistused ja reserveeringud</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-652">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="92563-653">Jah</span><span class="sxs-lookup"><span data-stu-id="92563-653">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-654">Valige kindel asukoht.</span><span class="sxs-lookup"><span data-stu-id="92563-654">Select a specific location.</span></span></li>
<li><span data-ttu-id="92563-655">Valige rida, millel on kindel kaup, asukoht ja litsentsiplaat (kui asukoht on litsentsiplaadi kontrollitud).</span><span class="sxs-lookup"><span data-stu-id="92563-655">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="92563-656">Valige <strong>Varude oleku muutmine</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-656">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="92563-657">Seadke välja <strong>Varude olek</strong> väärtuseks <strong>Blokeerimine</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-657">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="92563-658">Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="92563-658">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="92563-659">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="92563-659">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="92563-660">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="92563-660">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="92563-661">Tüübi <strong>Varude oleku muutmine</strong> kaks laokannet luuakse selleks, et tähistada varude oleku dimensiooni muutumist.</span><span class="sxs-lookup"><span data-stu-id="92563-661">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="92563-662">Tüübi <strong>Varude blokeerimine</strong> ja probleemitüübi <strong>Reserveeritud füüsiline</strong> luuakse selleks, et tähistada blokeeritud koguse reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="92563-662">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="92563-663">Ei</span><span class="sxs-lookup"><span data-stu-id="92563-663">No</span></span></td>
<td><span data-ttu-id="92563-664">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="92563-664">See the previous row.</span></span></td>
<td><span data-ttu-id="92563-665">Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="92563-665">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="92563-666">Reserveering eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="92563-666">The reservation is removed.</span></span></li>
<li><span data-ttu-id="92563-667">Tüübi <strong>Varude oleku muutmine</strong> kaks laokannet luuakse selleks, et tähistada varude oleku dimensiooni muutumist.</span><span class="sxs-lookup"><span data-stu-id="92563-667">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="92563-668">Tüübi <strong>Varude blokeerimine</strong> ja probleemitüübi <strong>Reserveeritud füüsiline</strong> luuakse selleks, et tähistada blokeeritud koguse reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="92563-668">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="92563-669">Vahekaardil <strong>Ladu</strong>, kirjes <strong>Ladu</strong> on välja <strong>Eemalda reserveeringud ja märgised</strong> väärtuseks määratud <strong>Puudub</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-669">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="92563-670">Jah</span><span class="sxs-lookup"><span data-stu-id="92563-670">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="92563-671">Valige kindel asukoht.</span><span class="sxs-lookup"><span data-stu-id="92563-671">Select a specific location.</span></span></li>
<li><span data-ttu-id="92563-672">Valige rida, millel on kindel kaup, asukoht ja litsentsiplaat (kui asukoht on litsentsiplaadi kontrollitud).</span><span class="sxs-lookup"><span data-stu-id="92563-672">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="92563-673">Valige <strong>Varude oleku muutmine</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-673">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="92563-674">Seadke välja <strong>Varude olek</strong> väärtuseks <strong>Blokeerimine</strong>.</span><span class="sxs-lookup"><span data-stu-id="92563-674">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="92563-675">Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="92563-675">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="92563-676">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="92563-676">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="92563-677">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="92563-677">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="92563-678">Ei</span><span class="sxs-lookup"><span data-stu-id="92563-678">No</span></span></td>
<td><span data-ttu-id="92563-679">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="92563-679">See the previous row.</span></span></td>
<td><span data-ttu-id="92563-680">Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="92563-680">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="92563-681">Varude oleku muudatused pole lubatud.</span><span class="sxs-lookup"><span data-stu-id="92563-681">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="92563-682">Kitsendused</span><span class="sxs-lookup"><span data-stu-id="92563-682">Limitations</span></span>

- <span data-ttu-id="92563-683">Paindliku lao taseme dimensiooni reserveerimise funktsionaalsus ei toeta järgmisi funktsioone.</span><span class="sxs-lookup"><span data-stu-id="92563-683">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="92563-684">Tegeliku kaalu haldus</span><span class="sxs-lookup"><span data-stu-id="92563-684">Catch weight management</span></span>
    - <span data-ttu-id="92563-685">Füüsiline negatiivne laovaru</span><span class="sxs-lookup"><span data-stu-id="92563-685">Physical negative inventory</span></span>
    - <span data-ttu-id="92563-686">Tellitud tarnete reserveerimine</span><span class="sxs-lookup"><span data-stu-id="92563-686">Reservation against ordered supply</span></span>
    - <span data-ttu-id="92563-687">Üleviimistellimuste ja toormaterjalide komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="92563-687">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="92563-688">Konteineri konsolideerimise reeglil on direktiivi ühiku alusel pakkimisel piirangud.</span><span class="sxs-lookup"><span data-stu-id="92563-688">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="92563-689">Tellimusega kooskõlastatud reserveeringute puhul on soovitatav mitte kasutada konteineri loomise malle, mille puhul väli **Pakk direktiiviühiku järgi** on lubatud.</span><span class="sxs-lookup"><span data-stu-id="92563-689">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="92563-690">Praeguses kujunduses ei kasutata asukoha direktiive laotöö loomisel.</span><span class="sxs-lookup"><span data-stu-id="92563-690">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="92563-691">Seetõttu rakendatakse konteinerite voo etapis ainult madalaimat ühikut ühikute seeriagrupis (laoühikutes).</span><span class="sxs-lookup"><span data-stu-id="92563-691">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
