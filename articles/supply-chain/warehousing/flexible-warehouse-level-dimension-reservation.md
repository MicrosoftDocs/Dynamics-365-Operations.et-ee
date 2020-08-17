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
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 65304216b579b8def493d1e4218174cb9617013d
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652175"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="1ab92-103">Paindliku laotaseme dimensiooni reserveerimise poliitika</span><span class="sxs-lookup"><span data-stu-id="1ab92-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ab92-104">Kui varude reserveerimise hierarhia tüüp „partii-alla\[asukoha\]” on seotud toodetega, siis ei saa ettevõtted, mis müüvad partiijälgimisega tooteid ja käitavad nende logistikat, mis on lubatud Microsoft Dynamics 365 laohaldusesüsteemi (WMS) jaoks, reserveerida nende toodete kindlaid partiisid kliendi müügitellimustele.</span><span class="sxs-lookup"><span data-stu-id="1ab92-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span>

<span data-ttu-id="1ab92-105">Sarnaselt ei saa kindlaid litsentsiplaate reserveerida müügitellimustes olevate toodete jaoks, kui need tooted on seotud reserveerimise vaikehierarhiaga.</span><span class="sxs-lookup"><span data-stu-id="1ab92-105">In a similar way, specific license plates can't be reserved for products on sales orders when those products are associated with the default reservation hierarchy.</span></span>

<span data-ttu-id="1ab92-106">Selles teemas kirjeldatakse varude reserveerimise poliitikat, mis võimaldab nendel ettevõtetel kindlaid partiisid või litsentsiplaate reserveerida isegi siis, kui tooted on seotud reserveerimise hierarhia üksusega „partii-alla\[asukoht\]”.</span><span class="sxs-lookup"><span data-stu-id="1ab92-106">This topic describes the inventory reservation policy that lets these businesses reserve specific batches or license plates, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="1ab92-107">Varude reserveerimise hierarhia</span><span class="sxs-lookup"><span data-stu-id="1ab92-107">Inventory reservation hierarchy</span></span>

<span data-ttu-id="1ab92-108">See jaotis võtab kokku olemasoleva varude reserveerimise hierarhia.</span><span class="sxs-lookup"><span data-stu-id="1ab92-108">This section summarizes the existing inventory reservation hierarchy.</span></span>

<span data-ttu-id="1ab92-109">Varude reserveerimise hierarhia näitab, et laoala dimensioonidega seotud ulatuses on nõudetellimus seotud asukoha kohustuslike dimensioonide, lao ja varude olekuga, samas kui lao loogika vastutab nõutud koguste jaoks asukoha määramise ja selle reserveerimise eest.</span><span class="sxs-lookup"><span data-stu-id="1ab92-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="1ab92-110">Teisisõnu, nõudetellimuse ja laotoimingute vahelises suhtluses eeldatakse, et nõudetellimus määrab selle, kust tellimus tuleb saata (st millisest asukohast ja laost).</span><span class="sxs-lookup"><span data-stu-id="1ab92-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="1ab92-111">Seejärel toetub ladu laoruumidest nõutava koguse leidmisel oma loogikale.</span><span class="sxs-lookup"><span data-stu-id="1ab92-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="1ab92-112">Kuid selleks, et kajastada äritegevuse mudelit, on jälgimisdimensioonid (partii- ja seerianumbrid) siiski paindlikumad.</span><span class="sxs-lookup"><span data-stu-id="1ab92-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="1ab92-113">Varude reserveerimise hierarhia võib hõlmata stsenaariume, mille puhul kehtivad järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="1ab92-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="1ab92-114">Ettevõte tugineb oma laotoimingutele, et hallata partii- või seerianumbritega koguste komplekteerimist pärast seda, kui ladustamisruumis on kogused leitud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="1ab92-115">Sellele mudelile viidatakse sageli kui *partii-alla\[asukoht\]*.</span><span class="sxs-lookup"><span data-stu-id="1ab92-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="1ab92-116">Seda kasutatakse tavaliselt siis, kui toote partii- või seerianumbri ID ei ole klientidele oluline, kuna nad suunavad nõudluse müügiettevõttele.</span><span class="sxs-lookup"><span data-stu-id="1ab92-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="1ab92-117">Kui partii- või seerianumbrid on osa kliendi tellimuse täpsustusest ja need kirjendatakse nõudetellimusel, on laos olevaid koguseid leidnud toimingud piiratud konkreetsete nõutud numbritega ja neid ei tohi muuta.</span><span class="sxs-lookup"><span data-stu-id="1ab92-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="1ab92-118">Sellele mudelile viidatakse sageli kui *partii-üles\[asukoht\]*.</span><span class="sxs-lookup"><span data-stu-id="1ab92-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="1ab92-119">Nende stsenaariumide puhul on probleemiks, et igale väljastatud tootele saab määrata ainult ühe varude reserveerimise hierarhia.</span><span class="sxs-lookup"><span data-stu-id="1ab92-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="1ab92-120">Seetõttu ei saa WMS pärast seda, kui hierarhia määramine on määratlenud, millal partii või seerianumber tuleb reserveerida (kas siis, kui nõudetellimus on tehtud, või lao komplekteerimise ajal), jälgitud üksuste käsitsemisel ajastust ad-hoc-alusel muuta.</span><span class="sxs-lookup"><span data-stu-id="1ab92-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="1ab92-121">Partiijälgimisega kaupade paindlik reserveerimine</span><span class="sxs-lookup"><span data-stu-id="1ab92-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="1ab92-122">Äristsenaarium</span><span class="sxs-lookup"><span data-stu-id="1ab92-122">Business scenario</span></span>

<span data-ttu-id="1ab92-123">Selle stsenaariumi puhul kasutab ettevõte varude strateegiat, mille puhul lõpetatud kaupu jälgitakse partii numbrite järgi.</span><span class="sxs-lookup"><span data-stu-id="1ab92-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="1ab92-124">See ettevõte kasutab ka WMS-i töökogust.</span><span class="sxs-lookup"><span data-stu-id="1ab92-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="1ab92-125">Kuna sellel töökogusel on hästivarustatud loogika lao komplekteerimise ja saatmise toimingute planeerimiseks ning käitamiseks partiis lubatud kaupade puhul, on enamik lõpetatud kaupadest seotud „partii-alla\[asukoht\]“ varude reserveerimise hierarhiaga.</span><span class="sxs-lookup"><span data-stu-id="1ab92-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="1ab92-126">Seda tüüpi toiminguseadistuse eeliseks on see, et partiide komplekteerimise ja laovaliku otsused (mis on tegelikult reserveerimise otsused) lükatakse edasi, kuni alustatakse lao komplekteerimise toimingutega.</span><span class="sxs-lookup"><span data-stu-id="1ab92-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="1ab92-127">Neid ei tehta kliendi tellimuse esitamise ajal.</span><span class="sxs-lookup"><span data-stu-id="1ab92-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="1ab92-128">Kuigi „partii-alla\[asukoht\]” reserveerimise hierarhia teenib ettevõtte ärieesmärke hästi, nõuavad paljud ettevõtte kliendid toodete uuesti tellimisel sama partiid, mida nad varem ostsid.</span><span class="sxs-lookup"><span data-stu-id="1ab92-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="1ab92-129">Seetõttu ootavad ettevõtted paindlikkust selle osas, kuidas partii reserveerimise reegleid käsitletakse, nii et olenevalt klientide nõudlusest sama kauba järele võivad ilmneda järgmised käitumismustrid.</span><span class="sxs-lookup"><span data-stu-id="1ab92-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="1ab92-130">Partii numbrit saab kirjendada ja reserveerida, kui volitatud töötleja on tellimuse vastu võtnud, ja seda ei saa muuta laotoimingute ajal ja/või muude nõudmiste tõttu.</span><span class="sxs-lookup"><span data-stu-id="1ab92-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="1ab92-131">Selline käitumine aitab tagada, et tellitud partiinumber saadetakse kliendile.</span><span class="sxs-lookup"><span data-stu-id="1ab92-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="1ab92-132">Kui partiinumber ei ole kliendile oluline, saab laotoimingute komplekteerimise käigus määrata partiinumbri pärast seda, kui müügitellimuse registreerimine ja reserveerimine on tehtud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="1ab92-133">Müügitellimuse kindla partii reserveerimise lubamine</span><span class="sxs-lookup"><span data-stu-id="1ab92-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="1ab92-134">Selleks, et mahutada soovitud paindlikkus partii reserveerimise käitumises kaupadele, mis on seotud „partii-alla\[asukoht\]” varude reserveerimise hierarhiaga, peavad varude haldurid lehel **Varude reserveerimise hierarhiad** valima märkeruudu **Luba reserveerimine nõudetellimusel** valiku **Partiinumber** tasemel.</span><span class="sxs-lookup"><span data-stu-id="1ab92-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Varude reserveerimise hierarhia paindlikuks muutmine](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="1ab92-136">Kui hierarhias valitakse tase **Partiinumber**, valitakse automaatselt kõik seda taset ületavad dimensioonid kuni **Asukoha** tasemeni.</span><span class="sxs-lookup"><span data-stu-id="1ab92-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="1ab92-137">(Vaikimisi valitakse tasemest **Asukoht** üle olevad dimensioonid.) Selline käitumine peegeldab loogikat, kus kõik dimensioonid partiinumbri ja asukoha vahel on samuti automaatselt reserveeritud pärast seda, kui reserveerite tellimuse reale kindla partiinumbri.</span><span class="sxs-lookup"><span data-stu-id="1ab92-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="1ab92-138">Märkeruut **Luba reserveerimine nõudetellimusel** kehtib ainult reserveerimise hierarhia tasemete puhul, mis jäävad lao asukoha dimensioonist allapoole.</span><span class="sxs-lookup"><span data-stu-id="1ab92-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="1ab92-139">**Partiinumber** ja **Litsentsiplaat** on hierarhias ainsad tasemed, mida saab kasutada paindliku reserveerimise poliitikas.</span><span class="sxs-lookup"><span data-stu-id="1ab92-139">**Batch number** and **License plate** are the only levels in the hierarchy that are open for the flexible reservation policy.</span></span> <span data-ttu-id="1ab92-140">Teisisõnu ei saa te valida märkeruutu **Luba reserveerimine nõudetellimusel** taseme **Asukoht** või **Seerianumber** jaoks.</span><span class="sxs-lookup"><span data-stu-id="1ab92-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location** or **Serial number** level.</span></span>
>
> <span data-ttu-id="1ab92-141">Kui teie reserveerimise hierarhia sisaldab seerianumbri dimensiooni (mis peab alati olema väiksem kui tase **Partiinumber**) ja kui olete pakktöötluse numbrile sisse lülitanud partii-spetsiifilise reserveerimise, jätkab süsteem seerianumbri reserveerimise ja komplekteerimise toiminguid, mis põhinevad reeglitel, mis kehtivad reserveerimise poliitika „Seeria-alla\[asukoht\]” puhul.</span><span class="sxs-lookup"><span data-stu-id="1ab92-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="1ab92-142">Igal ajahetkel saate lubada partii-spetsiifilist reserveerimist olemasolevale „partii-alla\[asukoht\]” reserveerimise hierarhiale teie juurutuses.</span><span class="sxs-lookup"><span data-stu-id="1ab92-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="1ab92-143">See muudatus ei mõjuta reserveeringuid ja avatud lao tööd, mis loodi enne muudatuse toimumist.</span><span class="sxs-lookup"><span data-stu-id="1ab92-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="1ab92-144">Kuid märkeruutu **Luba reserveerimine nõudetellimusel** ei saa tühjendada, kui **Reserveeritud tellitud**, **Reserveeritud füüsilise** või **Tellitud** probleemi tüübi laokanded on olemas ühe või mitme selle reserveerimise hierarhiaga seotud kauba puhul.</span><span class="sxs-lookup"><span data-stu-id="1ab92-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="1ab92-145">Kui kauba olemasoleva reserveerimise hierarhia ei luba tellimuse partii täpsustust, saate selle uuesti määrata reserveerimise hierarhiasse, mis lubab partii spetsifikatsioone, tingimusel et hierarhia taseme struktuur on mõlemas hierarhias sama.</span><span class="sxs-lookup"><span data-stu-id="1ab92-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="1ab92-146">Kasutage funktsiooni **Muuda reserveerimise hierarhiat kaupadele** ümbermääramiseks.</span><span class="sxs-lookup"><span data-stu-id="1ab92-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="1ab92-147">See muudatus võib olla oluline, kui soovite vältida partiis jälitatud kaupade alamhulga paindlikku partii reserveerimist, kuid lubada seda ülejäänud tooteportfellile.</span><span class="sxs-lookup"><span data-stu-id="1ab92-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="1ab92-148">Olenemata sellest, kas olete märkinud ruudu **Luba reserveerimine nõudetellimusel**, kui te ei soovi kindlat partiinumbrit kaubale tellimuse rea jaoks reserveerida, rakendatakse laotoimingute vaikeloogikat, mis kehtib „partii-alla\[asukoht\]” reserveerimise hierarhia puhul.</span><span class="sxs-lookup"><span data-stu-id="1ab92-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="1ab92-149">Kindla partiinumbri reserveerimine kliendi tellimuse jaoks</span><span class="sxs-lookup"><span data-stu-id="1ab92-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="1ab92-150">Pärast seda, kui partii jälgitud kauba „partii-alla\[asukoht\]” varude reserveerimise hierarhia on seadistatud lubama kindla partiinumbrite reserveerimist müügitellimustel, võivad müügitellimuse töötlejad võtta sama kauba kohta kliendi tellimusi ühel järgmistest viisidest, olenevalt kliendi nõudest.</span><span class="sxs-lookup"><span data-stu-id="1ab92-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="1ab92-151">**Sisestage tellimuse üksikasjad partiinumbrit täpsustamata** – seda lähenemist tuleks kasutada juhul, kui toote partii spetsifikatsioon ei ole kliendile oluline.</span><span class="sxs-lookup"><span data-stu-id="1ab92-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="1ab92-152">Kõik olemasolevad protsessid, mis on seotud selle tüübi tellimuse käsitsemisega, jäävad süsteemis muutmata.</span><span class="sxs-lookup"><span data-stu-id="1ab92-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="1ab92-153">Kasutajate osas ei nõuta täiendavaid kaalutlusi.</span><span class="sxs-lookup"><span data-stu-id="1ab92-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="1ab92-154">**Sisestage tellimuse üksikasjad ja reserveerige konkreetne partiinumber** – seda lähenemist tuleks kasutada siis, kui klient nõuab kindlat partiid.</span><span class="sxs-lookup"><span data-stu-id="1ab92-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="1ab92-155">Tavaliselt nõuavad kliendid kindlat partiid, kui nad tellivad varem ostetud toodet.</span><span class="sxs-lookup"><span data-stu-id="1ab92-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="1ab92-156">Seda tüüpi partii-spetsiifilist reserveerimist nimetatakse *tellimusega kooskõlastatud reserveerimiseks*.</span><span class="sxs-lookup"><span data-stu-id="1ab92-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="1ab92-157">Järgmised reeglid kehtivad koguste töötlemisel ja partiinumber on seotud kindla tellimusega.</span><span class="sxs-lookup"><span data-stu-id="1ab92-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="1ab92-158">Selleks et lubada kauba kindla partii numbri reserveerimist kauba puhul, mis on märgitud jaotises „partii-alla\[asukoht\]”, peab süsteem reserveerima kõik dimensioonid asukoha kaudu.</span><span class="sxs-lookup"><span data-stu-id="1ab92-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="1ab92-159">See vahemik sisaldab tavaliselt litsentsiplaadi dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="1ab92-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="1ab92-160">Asukoha direktiive ei kasutata, kui komplekteerimise töö on loodud müügirea jaoks, mis kasutab tellimusega seotud partii reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="1ab92-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="1ab92-161">Tellimusega seotud partiide töö laotöötluse ajal ei tohi ei kasutaja ega süsteem partii numbrit muuta.</span><span class="sxs-lookup"><span data-stu-id="1ab92-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="1ab92-162">(See töötlemine hõlmab erandite käsitlemist.)</span><span class="sxs-lookup"><span data-stu-id="1ab92-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="1ab92-163">Järgmises näites kuvatakse täielik töövoog.</span><span class="sxs-lookup"><span data-stu-id="1ab92-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario-batch-number-allocation"></a><span data-ttu-id="1ab92-164">Näidisstsenaarium: partiinumbri määramine</span><span class="sxs-lookup"><span data-stu-id="1ab92-164">Example scenario: Batch number allocation</span></span>

<span data-ttu-id="1ab92-165">Selle näite jaoks peavad olema installitud demoandmed ja peate kasutama demoandmete ettevõtet **USMF**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><a name="Example-batch-allocation"></a><span data-ttu-id="1ab92-166">Varude reserveerimise hierarhia seadistamine partiile konkreetse reserveerimise lubamiseks</span><span class="sxs-lookup"><span data-stu-id="1ab92-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="1ab92-167">Avage **Laohaldus** \> **Seadistus** \> **Varud \> Reserveerimine hierarhiasse**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="1ab92-168">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-168">Select **New**.</span></span>
3. <span data-ttu-id="1ab92-169">Väljale **Nimi** sisestage nimi (nt **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="1ab92-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="1ab92-170">Väljale **Kirjeldus** sisestage kirjeldus (nt **Partii alla paindlikkuse**).</span><span class="sxs-lookup"><span data-stu-id="1ab92-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="1ab92-171">Väljal **Valitud** valige **Seerianumber** ja **Omanik** ning seejärel klõpsake vasakut nooleklahvi, et teisaldada need väljale **Saadaolev**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="1ab92-172">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-172">Select **OK**.</span></span>
7. <span data-ttu-id="1ab92-173">Märkige dimensioonitaseme real **Partiinumbri** ruut **Luba reserveerimine nõudetellimusel**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="1ab92-174">Tasemed **Litsentsiplaat** ja **Asukoht** valitakse automaatselt ja nende märkeruute ei saa tühjendada.</span><span class="sxs-lookup"><span data-stu-id="1ab92-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="1ab92-175">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="1ab92-176">Uue väljastatud toote loomine</span><span class="sxs-lookup"><span data-stu-id="1ab92-176">Create a new released product</span></span>

1. <span data-ttu-id="1ab92-177">Määrake toote kolm koondandmete parameetrit, kasutades neid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="1ab92-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="1ab92-178">Valige väljal **Laoala dimensioonigrupp** suvand **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="1ab92-179">Valige väljal  **Jälgimisdimensiooni grupp** suvand **Batch-Phy**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="1ab92-180">Valige väljal **Reserveeringu hierarhia** suvand **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="1ab92-181">Looge kaks partiinumbrit, nt **B11** ja **B22**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="1ab92-182">Lisage kauba kogused laoseisu, kasutades järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="1ab92-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="1ab92-183">Ladu</span><span class="sxs-lookup"><span data-stu-id="1ab92-183">Warehouse</span></span> | <span data-ttu-id="1ab92-184">Partii number</span><span class="sxs-lookup"><span data-stu-id="1ab92-184">Batch number</span></span> | <span data-ttu-id="1ab92-185">Koht</span><span class="sxs-lookup"><span data-stu-id="1ab92-185">Location</span></span> | <span data-ttu-id="1ab92-186">Litsentsiplaat</span><span class="sxs-lookup"><span data-stu-id="1ab92-186">License plate</span></span> | <span data-ttu-id="1ab92-187">Kogus</span><span class="sxs-lookup"><span data-stu-id="1ab92-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="1ab92-188">24</span><span class="sxs-lookup"><span data-stu-id="1ab92-188">24</span></span>        | <span data-ttu-id="1ab92-189">B11</span><span class="sxs-lookup"><span data-stu-id="1ab92-189">B11</span></span>          | <span data-ttu-id="1ab92-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="1ab92-190">BULK-001</span></span> | <span data-ttu-id="1ab92-191">Puudub</span><span class="sxs-lookup"><span data-stu-id="1ab92-191">None</span></span>          | <span data-ttu-id="1ab92-192">10</span><span class="sxs-lookup"><span data-stu-id="1ab92-192">10</span></span>       |
    | <span data-ttu-id="1ab92-193">24</span><span class="sxs-lookup"><span data-stu-id="1ab92-193">24</span></span>        | <span data-ttu-id="1ab92-194">B11</span><span class="sxs-lookup"><span data-stu-id="1ab92-194">B11</span></span>          | <span data-ttu-id="1ab92-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="1ab92-195">FL-001</span></span>   | <span data-ttu-id="1ab92-196">LP11</span><span class="sxs-lookup"><span data-stu-id="1ab92-196">LP11</span></span>          | <span data-ttu-id="1ab92-197">10</span><span class="sxs-lookup"><span data-stu-id="1ab92-197">10</span></span>       |
    | <span data-ttu-id="1ab92-198">24</span><span class="sxs-lookup"><span data-stu-id="1ab92-198">24</span></span>        | <span data-ttu-id="1ab92-199">B22</span><span class="sxs-lookup"><span data-stu-id="1ab92-199">B22</span></span>          | <span data-ttu-id="1ab92-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="1ab92-200">FL-002</span></span>   | <span data-ttu-id="1ab92-201">LP22</span><span class="sxs-lookup"><span data-stu-id="1ab92-201">LP22</span></span>          | <span data-ttu-id="1ab92-202">10</span><span class="sxs-lookup"><span data-stu-id="1ab92-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><a name="sales-order-details"></a><span data-ttu-id="1ab92-203">Müügitellimuse üksikasjade sisestamine</span><span class="sxs-lookup"><span data-stu-id="1ab92-203">Enter sales order details</span></span>

1. <span data-ttu-id="1ab92-204">Avage **Müük ja turundus** \> **Müügitellimused** \> **Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="1ab92-205">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-205">Select **New**.</span></span>
3. <span data-ttu-id="1ab92-206">Müügitellimuse päise väljale **Kliendi konto** sisestage **US-003**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="1ab92-207">Lisage uue üksuse jaoks rida ja sisestage koguseks **10**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="1ab92-208">Veenduge, et välja **Ladu** väärtuseks oleks määratud **24**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="1ab92-209">Kiirkaardil **Müügitellimuse read** valige väärtus **Varud** ja seejärel jaotises **Haldamine** suvand **Partii reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="1ab92-210">Leht **Partii reserveerimine** näitab tellimuse rea reserveerimiseks saadaolevate partiide loendit.</span><span class="sxs-lookup"><span data-stu-id="1ab92-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="1ab92-211">Selles näites näitab see kogust **20** partiinumbri **B11** ja kogust **10** partiinumbri **B22** jaoks.</span><span class="sxs-lookup"><span data-stu-id="1ab92-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="1ab92-212">Pange tähele, et lehele **Partii reserveerimine** ei pääse realt juurde, kui sellel real olev üksus on seotud väärtusega „partii-alla\[asukoht\]”, kui see pole seadistatud lubama partiiga seotud reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="1ab92-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ab92-213">Kindla partii reserveerimiseks müügitellimusele tuleb kasutada lehte **Partii reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="1ab92-214">Kui sisestate partii numbri otse müügitellimuse reale, käitub süsteem nii, nagu sisestasite kindla partii väärtuse üksusele, mille suhtes kehtib „partii-alla\[asukoht\]” reserveerimise poliitika.</span><span class="sxs-lookup"><span data-stu-id="1ab92-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="1ab92-215">Rea salvestamisel kuvatakse hoiatusteade.</span><span class="sxs-lookup"><span data-stu-id="1ab92-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="1ab92-216">Kui kinnitate, et partiinumber tuleb määrata otse tellimuse reale, ei käsitleta rida tavalise laohalduse loogikaga.</span><span class="sxs-lookup"><span data-stu-id="1ab92-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="1ab92-217">Kui reserveerite koguse lehelt **Reserveerimine**, ei reserveerita ühtegi kindlat partiid ja selle rea laotegevuse käitamine järgib reegleid, mis on rakendatavad „partii-alla\[asukoht\]” reserveerimise poliitika alusel.</span><span class="sxs-lookup"><span data-stu-id="1ab92-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="1ab92-218">See lehekülg töötab ja on seotud samal viisil, nagu see toimib ja on seotud üksuste puhul, millel on seostatud reserveerimise hierarhia tüübiga „partii-üle\[asukoha\]”.</span><span class="sxs-lookup"><span data-stu-id="1ab92-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="1ab92-219">Siiski kehtivad järgmised erandid.</span><span class="sxs-lookup"><span data-stu-id="1ab92-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="1ab92-220">Kiirkaart **Lähtereale määratud partiinumbrid** kuvab tellimuserea jaoks reserveeritud partiinumbrid.</span><span class="sxs-lookup"><span data-stu-id="1ab92-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="1ab92-221">Ruudustikus olevad partiiväärtused kuvatakse kogu tellimuserea täitmise tsüklis, sh laotöötluse etappides.</span><span class="sxs-lookup"><span data-stu-id="1ab92-221">The batch values in the grid will be shown throughout the fulfillment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="1ab92-222">Seevastu kiirkaart **Ülevaade**, korrapärase tellimuse rea reserveerimine (s.t reserveerimine, mida tehakse **Asukoha** taseme kohal olevate dimensioonide puhul), kuvatakse ruudustikus kuni laotöö loomiseni.</span><span class="sxs-lookup"><span data-stu-id="1ab92-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="1ab92-223">Tööüksus võtab seejärel rea reserveerimise üle ja rea reserveeringut ei kuvata enam leheküljel.</span><span class="sxs-lookup"><span data-stu-id="1ab92-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="1ab92-224">Kiirkaart **Lähtereale määratud partiinumbrid** aitab tagada, et müügitellimuse töötleja saab vaadata kliendi tellimusele määratud partiinumbreid mis tahes tööetapis kuni arveldamiseni.</span><span class="sxs-lookup"><span data-stu-id="1ab92-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="1ab92-225">Peale konkreetse partii reserveerimise saab kasutaja valida käsitsi partii kindla asukoha ja litsentsiplaadi, selle asemel et lasta süsteemil need automaatselt valida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="1ab92-226">See võimalus on seotud tellimuse sooritatud partii reserveerimise mehhanismi kujundusega.</span><span class="sxs-lookup"><span data-stu-id="1ab92-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="1ab92-227">Nagu varem mainitud, tuleb selleks, et lubada kindla partii numbri reserveerimist üksuse puhul, mis on märgitud jaotises „partii-alla\[asukoht\]”, peab süsteem reserveerima kõik dimensioonid asukoha kaudu.</span><span class="sxs-lookup"><span data-stu-id="1ab92-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="1ab92-228">Seetõttu teeb lao töö samu ladustamise dimensioone, mis olid reserveeritud tellimustega töötavate kasutajate poolt, ja see ei pruugi alati kajastada kauba ladustamise paigutust, mis on mugav või isegi võimalik komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="1ab92-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="1ab92-229">Kui tellimuse töötlejad on lao piirangutest teadlikud, võivad nad partii reserveerimisel käsitsi valida kindlad asukohad ja litsentsiplaadid.</span><span class="sxs-lookup"><span data-stu-id="1ab92-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="1ab92-230">Sellisel juhul peab kasutaja kasutama lehekülje päises funktsiooni **Kuva dimensioonid** ja lisama asukoha ja litsentsiplaadi kiirkaardi **Ülevaade** ruudustikus.</span><span class="sxs-lookup"><span data-stu-id="1ab92-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="1ab92-231">Valige lehel **Partii reserveerimine** partii **B11** jaoks rida ja seejärel käsk **Reserveeri rida**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="1ab92-232">Automaatsel reserveerimisel ei ole asukohtade ja litsentsiplaadi määramiseks loogikat määratud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="1ab92-233">Koguse saate sisestada käsitsi väljale **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="1ab92-234">Pange tähele, et kiirkaardi **Lähtereale määratud partiinumbrid** partii **B11** kuvatakse kui **Sooritatud**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Kindla partiinumbri määramine müügitellimuse reale partii reserveerimise lehel](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="1ab92-236">Müügitellimuse rea koguse reserveerimist saab teha mitmel partiil.</span><span class="sxs-lookup"><span data-stu-id="1ab92-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="1ab92-237">Sama partii reserveerimist saab teha ka mitme asukoha ja litsentsiplaadi alusel (kui nende asukohtade puhul on lubatud litsentsiplaadid).</span><span class="sxs-lookup"><span data-stu-id="1ab92-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="1ab92-238">Kindla partii reserveerimine müügitellimuse real oleva koguse jaoks võib olla ka osaline.</span><span class="sxs-lookup"><span data-stu-id="1ab92-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="1ab92-239">Näiteks 100 ühiku kogukogust saab reserveerida nii, et kindel partii on pühendunud 20 ühikule, samas kui 80 ühikut on reserveeritud saidi ja lao tasemetele mis tahes saadaoleva partii jaoks.</span><span class="sxs-lookup"><span data-stu-id="1ab92-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="1ab92-240">Sel juhul kasutab WMS komplekteerimislehe töötlemisel kaht eraldiseisvat töörida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="1ab92-241">Avage **Tooteteabe haldus** \> **Tooted** \> **Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="1ab92-242">Valige üksus ja seejärel **Varude haldamine** \> **Kuva** \> **Kanded**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Tellimusega kooskõlastatud reserveerimine laokande tüübina](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="1ab92-244">Vaadake üle kauba varude kanded, mis on seotud müügitellimuse rea reserveerimisega.</span><span class="sxs-lookup"><span data-stu-id="1ab92-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="1ab92-245">Kanne, mille välja **Viide** väärtuseks on seatud **Müügitellimus** ja välja **Väljaminek** väärtuseks on seatud **Reserveeritud füüsiline**, näitab tellimuse rea reserveerimist varude dimensioonide jaoks, mis on üle taseme **Asukoht**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="1ab92-246">Kauba varude reserveerimise hierarhia kohaselt on need dimensioonid saidi, lao ja varude olek.</span><span class="sxs-lookup"><span data-stu-id="1ab92-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="1ab92-247">Kanne, mille välja **Viide** väärtuseks on seatud **Tellimuse tehtud reserveerimine** ja välja **Väljaminek** väärtuseks on seatud **Reserveeritud füüsiline**, näitab tellimuse rea reserveerimist kindlat partiid ja kõiki varude dimensioone üle selle.</span><span class="sxs-lookup"><span data-stu-id="1ab92-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="1ab92-248">Kauba varude reserveerimise hierarhia kohaselt on need dimensioonid partiinumber ja asukoht.</span><span class="sxs-lookup"><span data-stu-id="1ab92-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="1ab92-249">Selles näites on asukoht **Bulk-001**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="1ab92-250">Valige müügitellimuse päises suvandid **Ladu** \> **Tegevused** \> **Laost vabastamine**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="1ab92-251">Tellimuse rida on nüüd moodustatud ja töö on loodud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="1ab92-252">Tellitud partiinumbritega laotööde ülevaatamine ja töötlemine</span><span class="sxs-lookup"><span data-stu-id="1ab92-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="1ab92-253">Kiirkaardil **Müügitellimuse read** valige **Ladu**\>**Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="1ab92-254">Tööl, mis tegeleb müügitellimuse reale pühendunud partii koguste komplekteerimisega, on järgmised omadused.</span><span class="sxs-lookup"><span data-stu-id="1ab92-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="1ab92-255">Töö loomiseks kasutab süsteem töömalle, kuid mitte asukoha direktiive.</span><span class="sxs-lookup"><span data-stu-id="1ab92-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="1ab92-256">Kõik töömallide jaoks määratletud kindlad sätted, nt maksimaalne komplekteerimise read või kindel mõõtühik, rakendatakse uute tööde loomisel määramiseks.</span><span class="sxs-lookup"><span data-stu-id="1ab92-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="1ab92-257">Siiski ei arvestata reegleid, mis on seotud asukoha direktiividega komplekteerimise asukohtade tuvastamiseks, kuna tellimusega kooskõlastatud reserveeringuga on juba määratud kõik varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="1ab92-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="1ab92-258">Need varude dimensioonid sisaldavad dimensioone lao ladustamise tasemel.</span><span class="sxs-lookup"><span data-stu-id="1ab92-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="1ab92-259">Seetõttu pärib töö need dimensioonid, ilma et peaksite konsulteerima asukoha direktiividega.</span><span class="sxs-lookup"><span data-stu-id="1ab92-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="1ab92-260">Partiinumbrit ei kuvata komplekteerimise real (nagu näiteks töörea puhul, mis luuakse kaubale, millel on seostatud „partii-üle\[-asukoht\]” reserveerimise hierarhia). Selle asemel kuvatakse seotud laokannete põhjal viidatud töökandes partiinumber ja kõik muud varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="1ab92-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Tellimusega kooskõlastatud reserveeringust pärinev lao laokande töö](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="1ab92-262">Kui töö on loodud, eemaldatakse välja **Viide** väärtusega **Tellimusele kooskõlastatud reserveerimine** kauba laokanne.</span><span class="sxs-lookup"><span data-stu-id="1ab92-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="1ab92-263">Laokannete puhul, mille välja **Viide** väärtuseks on seatud **Töö**, on nüüd füüsiline reserveerimine määratud kõigi koguse varude dimensioonide jaoks.</span><span class="sxs-lookup"><span data-stu-id="1ab92-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="1ab92-264">Laotoimingud võivad jätkata töö töötlemist tavalisel viisil.</span><span class="sxs-lookup"><span data-stu-id="1ab92-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="1ab92-265">Kuid mobiilseade juhendab töötajat valima kindlat partiinumbrit.</span><span class="sxs-lookup"><span data-stu-id="1ab92-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="1ab92-266">Lao keskkondades, kus asukohti kontrollitakse litsentsiplaadiga pärast seda, kui töötaja jõuab asukohani, mis talletab sama partii mitmele litsentsiplaadile, saab ta valida mis tahes litsentsiplaadi, mis pole veel reserveeritud (nt teine tellimusega kooskõlastatud reserveering või töö, mis pärineb seda tüüpi reserveeringust.)</span><span class="sxs-lookup"><span data-stu-id="1ab92-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="1ab92-267">Kui tööreal määratud asukohast komplekteerimine osutub ebaotstarbekaks, saavad laooperaatorid kasutada üht järgmistest toimingutest, et suunata kindla partii komplekteerimine mugavamasse asukohta.</span><span class="sxs-lookup"><span data-stu-id="1ab92-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="1ab92-268">Mobiilseadme tavatoiming **Asukoha alistamine** (eeldusel, et lao töötaja säte **Luba valitud asukoha alistamine** on lubatud)</span><span class="sxs-lookup"><span data-stu-id="1ab92-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="1ab92-269">Toiming **Muuda asukohta** lehel **Tööloendi üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="1ab92-270">Lõpetage mobiilseadmes komplekteerimine ja töö sisestamine.</span><span class="sxs-lookup"><span data-stu-id="1ab92-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="1ab92-271">Kogus **10** on nüüd partiinumbri **B11** jaoks müügireale komplekteeritud ja asukohta **Baydoor** pandud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="1ab92-272">Sel hetkel on see veokile laadimiseks ja kliendi aadressile lähetamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="1ab92-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="flexible-license-plate-reservation"></a><span data-ttu-id="1ab92-273">Paindlik litsentsiplaadi reserveerimine</span><span class="sxs-lookup"><span data-stu-id="1ab92-273">Flexible license plate reservation</span></span>

### <a name="business-scenario"></a><span data-ttu-id="1ab92-274">Äristsenaarium</span><span class="sxs-lookup"><span data-stu-id="1ab92-274">Business scenario</span></span>

<span data-ttu-id="1ab92-275">Selles stsenaariumis kasutab ettevõte laohaldust ja töö töötlemist ning planeerib koormaid üksikute kaubaaluste/konteinerite alusel väljaspool Supply Chain Managementi enne töö loomist.</span><span class="sxs-lookup"><span data-stu-id="1ab92-275">In this scenario, a company uses warehouse management and work processing, and handles load planning at the level of individual pallets/containers outside Supply Chain Management before work is created.</span></span> <span data-ttu-id="1ab92-276">Neid konteinereid esindavad varude dimensioonides litsentsiplaadid.</span><span class="sxs-lookup"><span data-stu-id="1ab92-276">These containers are represented by license plates in the inventory dimensions.</span></span> <span data-ttu-id="1ab92-277">Selleks toiminguks tuleb seetõttu konkreetsed litsentsiplaadid enne komplekteerimistöö lõpetamist määrata müügitellimuse ridadele.</span><span class="sxs-lookup"><span data-stu-id="1ab92-277">Therefore, for this approach, specific license plates must be pre-assigned to sales order lines before picking work is done.</span></span> <span data-ttu-id="1ab92-278">Ettevõte soovib, et litsentsiplaadi reserveerimise reeglite käsitsemine oleks paindlik, et juhtuksid järgmised asjad.</span><span class="sxs-lookup"><span data-stu-id="1ab92-278">The company is looking for flexibility in the way that the license plate reservation rules are handled, so that the following behaviors occur:</span></span>

- <span data-ttu-id="1ab92-279">Litsentsiplaati saab kirjendada ja reserveerida, kui volitatud töötleja võtab tellimuse vastu, ning muud nõuded ei saa seda endale võtta.</span><span class="sxs-lookup"><span data-stu-id="1ab92-279">A license plate can be recorded and reserved when the order is taken by the sales processor, and it can't be taken by other demands.</span></span> <span data-ttu-id="1ab92-280">Selline käitumine aitab tagada, et planeeritud litsentsiplaat saadetakse kliendile.</span><span class="sxs-lookup"><span data-stu-id="1ab92-280">This behavior helps guarantee that the license plate that was planned is shipped to the customer.</span></span>
- <span data-ttu-id="1ab92-281">Kui litsentsiplaat ei ole juba müügitellimuse reale määratud, saab laotöötaja valida litsentsiplaadi komplekteerimise ajal, pärast müügitellimuse registreerimist ja reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="1ab92-281">If the license plate isn't already assigned to a sales order line, warehouse personnel can select a license plate during picking work, after sales order registration and reservation are completed.</span></span>

### <a name="turn-on-flexible-license-plate-reservation"></a><span data-ttu-id="1ab92-282">Paindliku litsentsiplaadi reserveerimise sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="1ab92-282">Turn on flexible license plate reservation</span></span>

<span data-ttu-id="1ab92-283">Enne paindliku litsentsiplaadi reserveerimise kasutamist peate oma süsteemis sisse lülitama kaks funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="1ab92-283">Before you can use flexible license plate reservation, two features must be turned on in your system.</span></span> <span data-ttu-id="1ab92-284">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsioonide olekut ja need vajadusel sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="1ab92-284">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="1ab92-285">Peate funktsioonid sisse lülitama järgmises järjekorras.</span><span class="sxs-lookup"><span data-stu-id="1ab92-285">You must turn on the features in the following order:</span></span>

1. <span data-ttu-id="1ab92-286">**Funktsiooni nimi:** *Paindlik dimensiooni reserveerimine laotasemel*</span><span class="sxs-lookup"><span data-stu-id="1ab92-286">**Feature name:** *Flexible warehouse-level dimension reservation*</span></span>
1. <span data-ttu-id="1ab92-287">**Funktsiooni nimi:** *Paindlik tellimusega seotud litsentsiplaadi reserveerimine*</span><span class="sxs-lookup"><span data-stu-id="1ab92-287">**Feature name:** *Flexible order-committed license plate reservation*</span></span>

### <a name="reserve-a-specific-license-plate-on-the-sales-order"></a><span data-ttu-id="1ab92-288">Kindla litsentsiplaadi reserveerimine müügitellimusel</span><span class="sxs-lookup"><span data-stu-id="1ab92-288">Reserve a specific license plate on the sales order</span></span>

<span data-ttu-id="1ab92-289">Selleks, et lubada litsentsiplaadi reserveerimine tellimusel, peate valima lehel **Varude reserveerimise hierarhiad** märkeruudu **Luba reserveerimine nõudetellimusel** tasemel **Litsentsiplaat** hierarhia jaoks, mis on seotud asjaomase kaubaga.</span><span class="sxs-lookup"><span data-stu-id="1ab92-289">To enable license plate reservation on an order, you must select the **Allow reservation on demand order** check box for the **License plate** level on the **Inventory reservation hierarchies** page for the hierarchy that is associated with the relevant item.</span></span>

![Varude reserveerimise hierarhialeht paindliku litsentsiplaadi reserveerimise hierarhia jaoks](media/Flexible-LP-reservation-hierarchy.png)

<span data-ttu-id="1ab92-291">Saate lubada litsentsiplaadi reserveerimise tellimusel juurutuse käigus igal ajal.</span><span class="sxs-lookup"><span data-stu-id="1ab92-291">You can enable license plate reservation on the order at any point in your deployment.</span></span> <span data-ttu-id="1ab92-292">See muudatus ei mõjuta reserveeringuid ega avatud laotöid, mis loodi enne muudatuse toimumist.</span><span class="sxs-lookup"><span data-stu-id="1ab92-292">This change won't affect any reservations or open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="1ab92-293">Kuid te ei saa märkeruutu **Luba reserveerimine nõudetellimusel** tühjendada, kui reserveerimise hierarhiaga seotud ühel või mitmel kaubal on avatud väljaminevate varude kandeid, mille väljamineku olek on *Tellimusel*, *Reserveeritud tellitud* või *Füüsiliselt reserveeritud*.</span><span class="sxs-lookup"><span data-stu-id="1ab92-293">However, you can't clear the **Allow reservation on demand order** check box if open outbound inventory transactions that have an issue status of *On order*, *Reserved ordered*, or *Reserved physical* exist for one or more items that are associated with that reservation hierarchy.</span></span>

<span data-ttu-id="1ab92-294">Isegi kui märkeruut **Luba reserveerimine nõudetellimusel** on tasemel **Litsentsiplaat** valitud, *ei ole* siiski võimalik kindlat litsentsiplaati tellimusel reserveerida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-294">Even if the **Allow reservation on demand order** check box is selected for the **License plate** level, it's still possible *not* to reserve a specific license plate on the order.</span></span> <span data-ttu-id="1ab92-295">Sel juhul rakendub laotoimingute vaikeloogika, mis kehtib selle reserveerimise hierarhia puhul.</span><span class="sxs-lookup"><span data-stu-id="1ab92-295">In this case, the default warehouse operations logic that is valid for the reservation hierarchy applies.</span></span>

<span data-ttu-id="1ab92-296">Konkreetse litsentsiplaadi reserveerimiseks peate kasutama [avatud andmeprotokolli (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) protsessi. Rakenduses saate teha reserveeringu otse müügitellimusel, kasutades käsu **Ava Excelis** valikut **Tellimusega seotud reserveeringud litsentsiplaadi kohta**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-296">To reserve a specific license plate, you must use an [Open Data Protocol (OData)](../../fin-ops-core/dev-itpro/data-entities/odata.md) process.In the application, you can do this reservation directly from a sales order by using the **Order-committed reservations per license plate** option of the **Open in Excel** command.</span></span> <span data-ttu-id="1ab92-297">Te peate sisestama Exceli lisandmoodulis avanenud üksuse andmetes järgmised reserveeringuga seotud andmed ja valima seejärel **Avalda**, et saata andmed tagasi Supply Chain Managementi.</span><span class="sxs-lookup"><span data-stu-id="1ab92-297">In the entity data that is opened in the Excel add-in, you must enter the following reservation-related data and then select **Publish** to send the data back to Supply Chain Management:</span></span>

- <span data-ttu-id="1ab92-298">Viide (toetatud on ainult väärtus *Müügitellimus*.)</span><span class="sxs-lookup"><span data-stu-id="1ab92-298">Reference (Only the *Sales order* value is supported.)</span></span>
- <span data-ttu-id="1ab92-299">Tellimuse number (väärtust saab tuletada partiist.)</span><span class="sxs-lookup"><span data-stu-id="1ab92-299">Order number (The value can be derived from the lot.)</span></span>
- <span data-ttu-id="1ab92-300">Saatepartii ID</span><span class="sxs-lookup"><span data-stu-id="1ab92-300">Lot ID</span></span>
- <span data-ttu-id="1ab92-301">Litsentsiplaat</span><span class="sxs-lookup"><span data-stu-id="1ab92-301">License plate</span></span>
- <span data-ttu-id="1ab92-302">Kogus</span><span class="sxs-lookup"><span data-stu-id="1ab92-302">Quantity</span></span>

<span data-ttu-id="1ab92-303">Kui teil on vaja reserveerida kindlat litsentsiplaati partiijälgimisega kauba jaoks, kasutage lehte **Partii reserveerimine**, nagu on kirjeldatud jaotises [Müügitellimuse üksikasjade sisestamine](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="1ab92-303">If you must reserve a specific license plate for a batch-tracked item, use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>

<span data-ttu-id="1ab92-304">Kui laotoimingud töötlevad müügitellimuse rida, mis kasutab tellimusega seotud litsentsiplaadi reserveerimist, ei kasutata asukohakorraldusi.</span><span class="sxs-lookup"><span data-stu-id="1ab92-304">When the sales order line that uses an order-committed license plate reservation is processed by warehouse operations, location directives aren't used.</span></span>

<span data-ttu-id="1ab92-305">Kui laotöö kaup koosneb ridadest, mis moodustavad täieliku kaubaaluse ja millel on litsentsiplaadiga seotud kogused, saate optimeerida komplekteerimisprotsessi, kasutades mobiilse seadme menüükäsku, mille puhul on suvandi **Käitle litsentsiplaadi põhjal** väärtuseks seatud *Jah*.</span><span class="sxs-lookup"><span data-stu-id="1ab92-305">If a warehouse work item consists of lines that equal a complete pallet and have license plate–committed quantities, you can optimize the picking process by using a mobile device menu item where the **Handle by license plate** option is set to *Yes*.</span></span> <span data-ttu-id="1ab92-306">Selle asemel, et skannida töö kaupasid ühekaupa, saab laotöötaja seejärel komplekteerimise lõpule viimiseks litsentsiplaadi skannida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-306">A warehouse worker can then scan a license plate to complete a pick instead of having to scan the items from the work one by one.</span></span>

![Mobiilse seadme menüükäsk, mille puhul on suvandi „Käitle litsentsiplaadi põhjal” väärtuseks seatud „Jah”](media/Handle-by-LP-menu-item.png)

<span data-ttu-id="1ab92-308">Kuna funktsioon **Käitle litsentsiplaadi põhjal** ei toeta mitut kaubaalust hõlmavaid töid, siis on parem, kui eri litsentsiplaatide jaoks on eraldi tööüksus.</span><span class="sxs-lookup"><span data-stu-id="1ab92-308">Because the **Handle by license plate** functionality doesn't support work that covers multiple pallets, it's better to have a separate work item for different license plates.</span></span> <span data-ttu-id="1ab92-309">Selle meetodi kasutamiseks lisage väli **Tellimusega seotud litsentsiplaadi ID** tööpäise piirina lehel **Töömall**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-309">To use this approach, add the **Order-committed license plate ID** field as a work header break on the **Work template** page.</span></span>

## <a name="example-scenario-set-up-and-process-an-order-committed-license-plate-reservation"></a><span data-ttu-id="1ab92-310">Näidisstsenaarium: tellimusega seotud litsentsiplaadi reserveerimise seadistamine ja töötlemine</span><span class="sxs-lookup"><span data-stu-id="1ab92-310">Example scenario: Set up and process an order-committed license plate reservation</span></span>

<span data-ttu-id="1ab92-311">Selles stsenaariumis näidatakse, kuidas seadistada ja töödelda tellimusega seotud litsentsiplaadi reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="1ab92-311">This scenario shows how to set up and process an order-committed license plate reservation.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="1ab92-312">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="1ab92-312">Make demo data available</span></span>

<span data-ttu-id="1ab92-313">Selles stsenaariumis viidatakse väärtustele ja kirjetele, mis kuuluvad Supply Chain Managementis esitatud standardsete demoandmete hulka.</span><span class="sxs-lookup"><span data-stu-id="1ab92-313">This scenario refers to values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="1ab92-314">Kui soovite stsenaariumi läbida siin toodud väärtuseid kasutades, peate kasutama keskkonda, kuhu demoandmed on installitud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-314">If you want to work through the scenario by using the values that are provided here, be sure to work on an environment where the demo data is installed.</span></span> <span data-ttu-id="1ab92-315">Lisaks seadke enne alustamist juriidilise isiku väärtuseks **USMF**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-315">Additionally, set the legal entity to **USMF** before you begin.</span></span>

### <a name="create-an-inventory-reservation-hierarchy-that-allows-for-license-plate-reservation"></a><span data-ttu-id="1ab92-316">Varude reserveerimise hierarhia loomine, mis lubab litsentsiplaate reserveerida</span><span class="sxs-lookup"><span data-stu-id="1ab92-316">Create an inventory reservation hierarchy that allows for license plate reservation</span></span>

1. <span data-ttu-id="1ab92-317">Avage **Laohaldus \> Seadistus \> Varud \> Reserveerimise hierarhia**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-317">Go to **Warehouse management \> Setup \> Inventory \> Reservation hierarchy**.</span></span>
1. <span data-ttu-id="1ab92-318">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-318">Select **New**.</span></span>
1. <span data-ttu-id="1ab92-319">Sisestage väljale **Nimi** väärtus (nt *FlexibleLP*).</span><span class="sxs-lookup"><span data-stu-id="1ab92-319">In the **Name** field, enter a value (for example, *FlexibleLP*).</span></span>
1. <span data-ttu-id="1ab92-320">Sisestage väljale **Kirjeldus** väärtus (nt *Paindlik LP reserveerimine*).</span><span class="sxs-lookup"><span data-stu-id="1ab92-320">In the **Description** field, enter a value (for example, *Flexible LP reservation*).</span></span>
1. <span data-ttu-id="1ab92-321">Valige loendis **Valitud** suvandid **Partiinumber**, **Seerianumber** ja **Omanik**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-321">In the **Selected** list, select **Batch number**, **Serial number**, and **Owner**.</span></span>
1. <span data-ttu-id="1ab92-322">Valige nupp **Eemalda** ![vasakule osutav nool](media/backward-button.png), et teisaldada valitud kirjed loendisse **Saadaval**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-322">Select the **Remove** button ![backward arrow](media/backward-button.png) to move the selected records to the **Available** list.</span></span>
1. <span data-ttu-id="1ab92-323">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-323">Select **OK**.</span></span>
1. <span data-ttu-id="1ab92-324">Märkige dimensioonitaseme **Litsentsiplaat** real märkeruut **Luba reserveerimine nõudetellimusel**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-324">In the row for the **License plate** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="1ab92-325">Tase **Asukoht** valitakse automaatselt ja selle märkeruutu ei saa tühjendada.</span><span class="sxs-lookup"><span data-stu-id="1ab92-325">The **Location** level is automatically selected, and you can't clear the check box for it.</span></span>
1. <span data-ttu-id="1ab92-326">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-326">Select **Save**.</span></span>

### <a name="create-two-released-products"></a><span data-ttu-id="1ab92-327">Kahe väljastatud toote loomine</span><span class="sxs-lookup"><span data-stu-id="1ab92-327">Create two released products</span></span>

1. <span data-ttu-id="1ab92-328">Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-328">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="1ab92-329">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-329">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="1ab92-330">Seadke dialoogiboksis **Uus väljastatud toode** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="1ab92-330">In the **New released product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1ab92-331">**Tootenumber:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="1ab92-331">**Product number:** *Item1*</span></span>
    - <span data-ttu-id="1ab92-332">**Kaubakood:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="1ab92-332">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="1ab92-333">**Kauba mudeligrupp:** *FIFO*</span><span class="sxs-lookup"><span data-stu-id="1ab92-333">**Item model group:** *FIFO*</span></span>
    - <span data-ttu-id="1ab92-334">**Kaubagrupp:** *Audio*</span><span class="sxs-lookup"><span data-stu-id="1ab92-334">**Item group:** *Audio*</span></span>
    - <span data-ttu-id="1ab92-335">**Laoala dimensiooni grupp:** *Ladu*</span><span class="sxs-lookup"><span data-stu-id="1ab92-335">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="1ab92-336">**Jälgimisdimensioonigrupp:** *Puudub*</span><span class="sxs-lookup"><span data-stu-id="1ab92-336">**Tracking dimension group:** *None*</span></span>
    - <span data-ttu-id="1ab92-337">**Reserveerimise hierarhia:** *FlexibleLP*</span><span class="sxs-lookup"><span data-stu-id="1ab92-337">**Reservation hierarchy:** *FlexibleLP*</span></span>

1. <span data-ttu-id="1ab92-338">Valige toote loomiseks ja dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-338">Select **OK** to create the product and close the dialog box.</span></span>
1. <span data-ttu-id="1ab92-339">Uus toode avatakse.</span><span class="sxs-lookup"><span data-stu-id="1ab92-339">The new product is opened.</span></span> <span data-ttu-id="1ab92-340">Seadke kiirkaardil **Ladu** välja **Ühiku seeriagrupi ID** väärtuseks *ea*.</span><span class="sxs-lookup"><span data-stu-id="1ab92-340">On the **Warehouse** FastTab, set the **Unit sequence group ID** field to *ea*.</span></span>
1. <span data-ttu-id="1ab92-341">Korrake eelmisi samme, et luua teine toode, millel on samad sätted, kuid seadke väljade **Tootenumber** ja **Kaubakood** väärtuseks *Item2*.</span><span class="sxs-lookup"><span data-stu-id="1ab92-341">Repeat the previous steps to create a second product that has the same settings, but set the **Product number** and **Item number** fields to *Item2*.</span></span>
1. <span data-ttu-id="1ab92-342">Valige toimingupaani vahekaardi **Varude haldamine** grupis **Kuva** suvand **Vaba kaubavaru**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-342">On the Action Pane, on the **Manage inventory** tab, in the **View** group, select **On-hand inventory**.</span></span> <span data-ttu-id="1ab92-343">Seejärel valige **Koguse korrigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-343">Then select **Quantity adjustment**.</span></span>
1. <span data-ttu-id="1ab92-344">Korrigeerige uute kaupade vaba kaubavaru järgmises tabelis täpsustatud viisil.</span><span class="sxs-lookup"><span data-stu-id="1ab92-344">Adjust the on-hand inventory of the new items as specified in the following table.</span></span>

    | <span data-ttu-id="1ab92-345">Üksus</span><span class="sxs-lookup"><span data-stu-id="1ab92-345">Item</span></span>  | <span data-ttu-id="1ab92-346">Ladu</span><span class="sxs-lookup"><span data-stu-id="1ab92-346">Warehouse</span></span> | <span data-ttu-id="1ab92-347">Koht</span><span class="sxs-lookup"><span data-stu-id="1ab92-347">Location</span></span> | <span data-ttu-id="1ab92-348">Litsentsiplaat</span><span class="sxs-lookup"><span data-stu-id="1ab92-348">License plate</span></span> | <span data-ttu-id="1ab92-349">Kogus</span><span class="sxs-lookup"><span data-stu-id="1ab92-349">Quantity</span></span> |
    |-------|-----------|----------|---------------|----------|
    | <span data-ttu-id="1ab92-350">Item1</span><span class="sxs-lookup"><span data-stu-id="1ab92-350">Item1</span></span> | <span data-ttu-id="1ab92-351">24</span><span class="sxs-lookup"><span data-stu-id="1ab92-351">24</span></span>        | <span data-ttu-id="1ab92-352">FL-010</span><span class="sxs-lookup"><span data-stu-id="1ab92-352">FL-010</span></span>   | <span data-ttu-id="1ab92-353">LP01</span><span class="sxs-lookup"><span data-stu-id="1ab92-353">LP01</span></span>          | <span data-ttu-id="1ab92-354">10</span><span class="sxs-lookup"><span data-stu-id="1ab92-354">10</span></span>       |
    | <span data-ttu-id="1ab92-355">Item1</span><span class="sxs-lookup"><span data-stu-id="1ab92-355">Item1</span></span> | <span data-ttu-id="1ab92-356">24</span><span class="sxs-lookup"><span data-stu-id="1ab92-356">24</span></span>        | <span data-ttu-id="1ab92-357">FL-011</span><span class="sxs-lookup"><span data-stu-id="1ab92-357">FL-011</span></span>   | <span data-ttu-id="1ab92-358">LP02</span><span class="sxs-lookup"><span data-stu-id="1ab92-358">LP02</span></span>          | <span data-ttu-id="1ab92-359">10</span><span class="sxs-lookup"><span data-stu-id="1ab92-359">10</span></span>       |
    | <span data-ttu-id="1ab92-360">Item2</span><span class="sxs-lookup"><span data-stu-id="1ab92-360">Item2</span></span> | <span data-ttu-id="1ab92-361">24</span><span class="sxs-lookup"><span data-stu-id="1ab92-361">24</span></span>        | <span data-ttu-id="1ab92-362">FL-010</span><span class="sxs-lookup"><span data-stu-id="1ab92-362">FL-010</span></span>   | <span data-ttu-id="1ab92-363">LP01</span><span class="sxs-lookup"><span data-stu-id="1ab92-363">LP01</span></span>          | <span data-ttu-id="1ab92-364">5</span><span class="sxs-lookup"><span data-stu-id="1ab92-364">5</span></span>        |
    | <span data-ttu-id="1ab92-365">Item2</span><span class="sxs-lookup"><span data-stu-id="1ab92-365">Item2</span></span> | <span data-ttu-id="1ab92-366">24</span><span class="sxs-lookup"><span data-stu-id="1ab92-366">24</span></span>        | <span data-ttu-id="1ab92-367">FL-011</span><span class="sxs-lookup"><span data-stu-id="1ab92-367">FL-011</span></span>   | <span data-ttu-id="1ab92-368">LP02</span><span class="sxs-lookup"><span data-stu-id="1ab92-368">LP02</span></span>          | <span data-ttu-id="1ab92-369">5</span><span class="sxs-lookup"><span data-stu-id="1ab92-369">5</span></span>        |

    > [!NOTE]
    > <span data-ttu-id="1ab92-370">Peate looma need kaks litsentsiplaati ja kasutama asukohti, mis lubavad segakaupu, nt *FL-010* ja *FL-011*.</span><span class="sxs-lookup"><span data-stu-id="1ab92-370">You must create the two license plates and use locations that allow for mixed items, such as *FL-010* and *FL-011*.</span></span>

### <a name="create-a-sales-order-and-reserve-a-specific-license-plate"></a><span data-ttu-id="1ab92-371">Müügitellimuse loomine ja kindla litsentsiplaadi reserveerimine</span><span class="sxs-lookup"><span data-stu-id="1ab92-371">Create a sales order and reserve a specific license plate</span></span>

1. <span data-ttu-id="1ab92-372">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-372">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="1ab92-373">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-373">Select **New**.</span></span>
1. <span data-ttu-id="1ab92-374">Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="1ab92-374">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="1ab92-375">**Kliendi konto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="1ab92-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="1ab92-376">**Ladu:** *24*</span><span class="sxs-lookup"><span data-stu-id="1ab92-376">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="1ab92-377">Valige **OK**, et sulgeda dialoogiboks **Müügitellimuse loomine** ja avada uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="1ab92-377">Select **OK** to close the **Create sales order** dialog box and open the new sales order.</span></span>
1. <span data-ttu-id="1ab92-378">Lisage kiirkaardil **Müügitellimuse read** järgmiste sätetega rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-378">On the **Sales order lines** FastTab, add a line that has the following settings:</span></span>

    - <span data-ttu-id="1ab92-379">**Kaubakood:** *Item1*</span><span class="sxs-lookup"><span data-stu-id="1ab92-379">**Item number:** *Item1*</span></span>
    - <span data-ttu-id="1ab92-380">**Kogus:** *10*</span><span class="sxs-lookup"><span data-stu-id="1ab92-380">**Quantity:** *10*</span></span>

1. <span data-ttu-id="1ab92-381">Lisage teine järgmiste sätetega müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-381">Add a second sales order line that has the following settings:</span></span>

    - <span data-ttu-id="1ab92-382">**Kaubakood:** *Item2*</span><span class="sxs-lookup"><span data-stu-id="1ab92-382">**Item number:** *Item2*</span></span>
    - <span data-ttu-id="1ab92-383">**Kogus:** *5*</span><span class="sxs-lookup"><span data-stu-id="1ab92-383">**Quantity:** *5*</span></span>

1. <span data-ttu-id="1ab92-384">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-384">Select **Save**.</span></span>
1. <span data-ttu-id="1ab92-385">Avage kiirkaardil **Rea üksikasjad** vahekaart **Seadistus** ja märkige üles iga rea **Partii ID** väärtus.</span><span class="sxs-lookup"><span data-stu-id="1ab92-385">On the **Line details** FastTab, on the **Setup** tab, make a note of the **Lot ID** value for each line.</span></span> <span data-ttu-id="1ab92-386">Neid väärtuseid on vaja kindlate litsentsiplaatide reserveerimisel.</span><span class="sxs-lookup"><span data-stu-id="1ab92-386">These values will be required during reservation of specific license plates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ab92-387">Kindla litsentsiplaadi reserveerimiseks peate kasutama andmeüksust **Tellimusega seotud reserveeringud litsentsiplaadi kohta**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-387">To reserve a specific license plate, you must use the **Order-committed reservations per license plate** data entity.</span></span> <span data-ttu-id="1ab92-388">Kindlas litsentsiplaadis partiijälgimisega kauba reserveerimiseks saate kasutada ka lehte **Partii reserveerimine**, nagu on kirjeldatud jaotises [Müügitellimuse üksikasjade sisestamine](#sales-order-details).</span><span class="sxs-lookup"><span data-stu-id="1ab92-388">To reserve a batch-tracked item on a specific license plate, you can also use the **Batch reservation** page, as described in the [Enter sales order details](#sales-order-details) section.</span></span>
    >
    > <span data-ttu-id="1ab92-389">Kui sisestate litsentsiplaadi otse müügitellimuse real ja kinnitate selle süsteemi, ei kasutata selle rea puhul laohalduse töötlemist.</span><span class="sxs-lookup"><span data-stu-id="1ab92-389">If you enter the license plate directly on the sales order line and confirm it to the system, warehouse management processing won't be used for the line.</span></span>

1. <span data-ttu-id="1ab92-390">Valige **Ava Microsoft Office'is**, valige **Tellimusega seotud reserveeringud litsentsiplaadi kohta** ja laadige fail alla.</span><span class="sxs-lookup"><span data-stu-id="1ab92-390">Select **Open in Microsoft Office**, select **Order-committed reservations per license plate**, and download the file.</span></span>
1. <span data-ttu-id="1ab92-391">Avage allalaaditud fail Excelis ja valige **Luba redigeerimine**, et lubada Exceli lisandmooduli käivitamine.</span><span class="sxs-lookup"><span data-stu-id="1ab92-391">Open the downloaded file in Excel, and select **Enable editing** to enable the Excel add-in to run.</span></span>
1. <span data-ttu-id="1ab92-392">Kui käivitate Exceli lisandmooduli esimest korda, valige käsk **Usalda seda lisandmoodulit**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-392">If you're running the Excel add-in for the first time, select **Trust this Add-in**.</span></span>
1. <span data-ttu-id="1ab92-393">Kui teil palutakse sisse logida, valige **Logi sisse** ja seejärel logige sisse, kasutades sama identimisteavet, mida kasutasite rakendusse Supply Chain Management sisselogimisel.</span><span class="sxs-lookup"><span data-stu-id="1ab92-393">If you're prompted to sign in, select **Sign in**, and then sign in by using the same credentials that you used to sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="1ab92-394">Kauba reserveerimiseks kindlas litsentsiplaadis valige Exceli lisandmoodulis **Uus**, et lisada reserveerimisrida ja seejärel seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="1ab92-394">To reserve an item on a specific license plate, in the Excel add-in, select **New** to add a reservation line, and then set the following values:</span></span>

    - <span data-ttu-id="1ab92-395">**Partii ID:** sisestage **Partii ID** väärtus, mille leidsite kauba *Item1* müügitellimuse realt.</span><span class="sxs-lookup"><span data-stu-id="1ab92-395">**Lot ID:** Enter the **Lot ID** value that you found for the sales order line for *Item1*.</span></span>
    - <span data-ttu-id="1ab92-396">**Litsentsiplaat:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="1ab92-396">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="1ab92-397">**ReservedInventoryQuantity:** *10*</span><span class="sxs-lookup"><span data-stu-id="1ab92-397">**ReservedInventoryQuantity:** *10*</span></span>

1. <span data-ttu-id="1ab92-398">Valige **Uus**, et lisada uus reserveerimisrida ja määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="1ab92-398">Select **New** to add another reservation line, and set the following values:</span></span>

    - <span data-ttu-id="1ab92-399">**Partii ID:** sisestage **Partii ID** väärtus, mille leidsite kauba *Item2* müügitellimuse realt.</span><span class="sxs-lookup"><span data-stu-id="1ab92-399">**Lot ID:** Enter the **Lot ID** value you found for the sales order line for *Item2*.</span></span>
    - <span data-ttu-id="1ab92-400">**Litsentsiplaat:** *LP02*</span><span class="sxs-lookup"><span data-stu-id="1ab92-400">**License plate:** *LP02*</span></span>
    - <span data-ttu-id="1ab92-401">**ReservedInventoryQuantity:** *5*</span><span class="sxs-lookup"><span data-stu-id="1ab92-401">**ReservedInventoryQuantity:** *5*</span></span>

1. <span data-ttu-id="1ab92-402">Valige Exceli lisandmoodulis **Avalda**, et saata andmed tagasi Supply Chain Managementi.</span><span class="sxs-lookup"><span data-stu-id="1ab92-402">In the Excel add-in, select **Publish** to send the data back to Supply Chain Management.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ab92-403">Reserveerimisrida kuvatakse süsteemis ainult juhul, kui avaldamine on tõrgeteta lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-403">The reservation line will appear in the system only if publishing is completed without errors.</span></span>

1. <span data-ttu-id="1ab92-404">Minge tagasi Supply Chain Managementi.</span><span class="sxs-lookup"><span data-stu-id="1ab92-404">Go back to Supply Chain Management.</span></span> 
1. <span data-ttu-id="1ab92-405">Kauba reserveeringu läbivaatamiseks valige kiirkaardil **Müügitellimuse read** menüüst **Varud** suvand **Halda \> Reserveering**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-405">To review the item's reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **Maintain \> Reservation**.</span></span> <span data-ttu-id="1ab92-406">Pange tähele, et kauba *Item1* müügitellimuse rea puhul on reserveeritud kogus *10* ja kauba *Item2* müügitellimuse rea puhul on kogus *5*.</span><span class="sxs-lookup"><span data-stu-id="1ab92-406">Notice that, for the sales order line for *Item1*, inventory of *10* is reserved, and for the sales order line for *Item2*, inventory of *5* is reserved.</span></span>
1. <span data-ttu-id="1ab92-407">Müügitellimuse rea reserveeringuga seotud laokannete ülevaatamiseks valige kiirkaardil **Müügitellimuse read** menüüst **Varud** suvand **Kuva \> Kanded**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-407">To review inventory transactions that are related to the sales order line reservation, on the **Sales order lines** FastTab, on the **Inventory** menu, select **View \> Transactions**.</span></span> <span data-ttu-id="1ab92-408">Pange tähele, et reserveeringuga on seotud kaks kannet: üks, mille välja **Viide** väärtuseks on seatud *Müügitellimus*, ja üks, mille välja **Viide** väärtuseks on seatud *Tellimusega seotud reserveering*.</span><span class="sxs-lookup"><span data-stu-id="1ab92-408">Notice that there are two transactions that are related to the reservation: one where the **Reference** field is set to *Sales order* and one where the **Reference** field is set to *Order-committed reservation*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ab92-409">Kanne, mille välja **Viide** väärtuseks on seatud *Müügitellimus*, näitab tellimuse rea reserveeringut varude dimensioonide jaoks, mis on üle taseme **Asukoht** (sait, ladu ja varude olek).</span><span class="sxs-lookup"><span data-stu-id="1ab92-409">A transaction where the **Reference** field is set to *Sales order* represents the order line reservation for inventory dimensions that are above the **Location** level (site, warehouse, and inventory status).</span></span> <span data-ttu-id="1ab92-410">Kanne, mille välja **Viide** väärtuseks on seatud *Tellimusega seotud reserveering*, näitab konkreetse litsentsiplaadi ja asukoha tellimuse rea reserveeringut.</span><span class="sxs-lookup"><span data-stu-id="1ab92-410">A transaction where the **Reference** field is set to *Order-committed reservation* represents the order line reservation for the specific license plate and location.</span></span>

1. <span data-ttu-id="1ab92-411">Müügitellimuse vabastamiseks valige toimingupaanil vahekaardi **Ladu** grupist **Tegevused** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-411">To release the sales order, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

### <a name="review-and-process-warehouse-work-with-order-committed-license-plates-assigned"></a><span data-ttu-id="1ab92-412">Määratud tellimusega seotud litsentsiplaatidega laotöö ülevaatamine ja töötlemine</span><span class="sxs-lookup"><span data-stu-id="1ab92-412">Review and process warehouse work with order-committed license plates assigned</span></span>

1. <span data-ttu-id="1ab92-413">Valige kiirkaardil **Müügitellimuse read** menüüst **Ladu** suvand **Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-413">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Work details**.</span></span>

    <span data-ttu-id="1ab92-414">Litsentsiplaadi reserveerimist kasutava müügitellimuse jaoks tööd luues ei kasuta süsteem asukohakorraldusi, nagu ka siis, kui reserveerimine toimub kindla partii raames.</span><span class="sxs-lookup"><span data-stu-id="1ab92-414">As when reservation is done for a specific batch, the system doesn't use location directives when it creates the work for the sales order that uses license plate reservation.</span></span> <span data-ttu-id="1ab92-415">Kuna tellimusega seotud reserveeringus on täpsustatud kõik varude dimensioonid, sealhulgas asukoht, ei pea kasutama asukohakorraldusi, kuna need varude dimensioonid sisestatakse lihtsalt töösse.</span><span class="sxs-lookup"><span data-stu-id="1ab92-415">Because the order-committed reservation specifies all the inventory dimensions, including the location, location directives don't have to be used, because those inventory dimensions are just entered in the work.</span></span> <span data-ttu-id="1ab92-416">Need kuvatakse jaotises **Varude dimensioonidest** lehel **Töö laokanded**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-416">They are shown in the **From inventory dimensions** section on the **Work inventory transactions** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ab92-417">Pärast töö loomist eemaldatakse kauba laokanne, mille välja **Viide** väärtus on *Tellimusega seotud reserveering*.</span><span class="sxs-lookup"><span data-stu-id="1ab92-417">After the work is created, the item's inventory transaction where the **Reference** field is set to *Order-committed reservation* is removed.</span></span> <span data-ttu-id="1ab92-418">Laokannete puhul, mille välja **Viide** väärtuseks on seatud *Töö*, on nüüd füüsiline reserveering määratud koguse kõigi varude dimensioonide jaoks.</span><span class="sxs-lookup"><span data-stu-id="1ab92-418">The inventory transaction where the **Reference** field is set to *Work* now holds the physical reservation for all the quantity's inventory dimensions.</span></span>

1. <span data-ttu-id="1ab92-419">Lõpetage mobiilses seadmes komplekteerimine ja töö sisestamine menüükäsu abil, mille märkeruut **Käitle litsentsiplaadi põhjal** on valitud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-419">On the mobile device, finish picking and putting the work by using a menu item where the **Handle by license plate** check box is selected.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1ab92-420">Funktsioon **Käitle litsentsiplaadi põhjal** aitab teil töödelda kogu litsentsiplaati.</span><span class="sxs-lookup"><span data-stu-id="1ab92-420">The **Handle by license plate** functionality helps you process the whole license plate.</span></span> <span data-ttu-id="1ab92-421">Kui peate töötlema vaid osa litsentsiplaadist, ei saa te seda funktsiooni kasutada.</span><span class="sxs-lookup"><span data-stu-id="1ab92-421">If you must process part of the license plate, you can't use this functionality.</span></span>
    >
    > <span data-ttu-id="1ab92-422">Soovitame iga litsentsiplaadi jaoks luua eraldi töö.</span><span class="sxs-lookup"><span data-stu-id="1ab92-422">We recommend that you have separate work generated for each license plate.</span></span> <span data-ttu-id="1ab92-423">Selle tulemuse saavutamiseks kasutage funktsiooni **Tööpäise piirid**, mis asub lehel **Töömall**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-423">To achieve this result, use the **Work header breaks** feature on the **Work template** page.</span></span>

    <span data-ttu-id="1ab92-424">Litsentsiplaat *LP02* on nüüd müügitellimuse ridadele komplekteeritud ja pandud asukohta *Laadimisuks*.</span><span class="sxs-lookup"><span data-stu-id="1ab92-424">License plate *LP02* is now picked for sales order lines and put to the *Baydoor* location.</span></span> <span data-ttu-id="1ab92-425">Nüüd on see laadimiseks ja kliendile lähetamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="1ab92-425">At this point, it's ready to be loaded and dispatched to the customer.</span></span>

## <a name="exception-handling-of-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="1ab92-426">Tellitud ja kooskõlastatud partiinumbritega laotööde ülevaatamise ja töötlemise erandid</span><span class="sxs-lookup"><span data-stu-id="1ab92-426">Exception handling of warehouse work that has order-committed batch numbers</span></span>

<span data-ttu-id="1ab92-427">Laotöö komplekteerimiseks tellitud partii numbrite suhtes kehtivad samad standardse lao erandi käsitlemise protsessid ja toimingud, mis tavatöö puhul.</span><span class="sxs-lookup"><span data-stu-id="1ab92-427">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="1ab92-428">Üldiselt saab avatud töö või töörea tühistada ja katkestada, kui kasutaja asukoht on täis, see võib olla lühike-komplekteeritud ja seda saab liikumise tõttu uuendada.</span><span class="sxs-lookup"><span data-stu-id="1ab92-428">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="1ab92-429">Samuti saab vähendada juba lõpetatud töö komplekteeritud kogust või seda tööd muuta.</span><span class="sxs-lookup"><span data-stu-id="1ab92-429">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="1ab92-430">Järgmist põhireeglit rakendatakse kõigile nende erandite käsitlemise toimingutele: kliendile reserveeritud partiinumbrit ei saa kunagi asendada teise partii numbriga, kuid selle ladustamise dimensioone (asukoht ja litsentsiplaat) saab muuta, selleks peab kasutaja seda käsitsi värskendama või süsteem automaatselt uuendama.</span><span class="sxs-lookup"><span data-stu-id="1ab92-430">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="1ab92-431">Automaatne värskendamine põhineb samadel juhusliku määramisega ladustamise dimensioonidel, mida rakendatakse, kui kindel partii on automaatselt reserveeritud, kuid ladustamise dimensioone ei määratud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-431">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="1ab92-432">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="1ab92-432">Example scenario</span></span>

<span data-ttu-id="1ab92-433">Selle stsenaariumi näide on olukord, kus varem lõpetatud töö on funktsiooni **Vähenda komplekteeritud kogust** kasutamisel komplekteerimata.</span><span class="sxs-lookup"><span data-stu-id="1ab92-433">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="1ab92-434">Selles näites eeldatakse, et olete juba lõpetanud sammud, mida kirjeldatakse jaotises [Näidisstsenaarium: partiinumbri määramine](#Example-batch-allocation).</span><span class="sxs-lookup"><span data-stu-id="1ab92-434">This example assumes that you've already completed the steps that are described in [Example scenario: Batch number allocation](#Example-batch-allocation).</span></span> <span data-ttu-id="1ab92-435">Tegevus jätkub pärast toda näidet.</span><span class="sxs-lookup"><span data-stu-id="1ab92-435">It continues from that example.</span></span>

1. <span data-ttu-id="1ab92-436">Avage **Laohaldus** \> **Koormad** \> **Aktiivsed koormad**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-436">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="1ab92-437">Valige koorem, mis loodi seoses teie müügitellimuse saadetisega.</span><span class="sxs-lookup"><span data-stu-id="1ab92-437">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="1ab92-438">Kiirkaardilt **Koorma tellimuse read** valige käsk **Vähenda komplekteeritud kogust**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-438">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="1ab92-439">Valige lehel **Vähenda komplekteeritud kogust** välja **Teisalda asukohta** väärtuseks **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-439">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="1ab92-440">Väljal **Teisalda litsentsiplaadile** valige väärtus **LP33**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-440">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="1ab92-441">Sisestage ruudustiku väljale **Varude kogus väljale komplekteerimata** väärtus **10**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-441">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="1ab92-442">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-442">Select **OK**.</span></span>

<span data-ttu-id="1ab92-443">Siin on komplekteerimise tegevuse tulemused.</span><span class="sxs-lookup"><span data-stu-id="1ab92-443">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="1ab92-444">Varem suletud töö olek on seatud väärtusele **Tühistatud**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-444">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="1ab92-445">Tüübi **Varude liikumine** uus töö luuakse komplekteerimata kogusega **10** partiinumbri**B11** jaoks.</span><span class="sxs-lookup"><span data-stu-id="1ab92-445">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="1ab92-446">See töö näitab liikumist asukohast **Baydoor** litsentsiplaadile **LP33** asukohas **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-446">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="1ab92-447">Olek on seatud väärtusele **Suletud**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-447">The status is set to **Closed**.</span></span>
- <span data-ttu-id="1ab92-448">Süsteem reserveerib algselt tellitud partiinumbri uuesti ja määrab asukoha ja litsentsiplaadi ID-d.</span><span class="sxs-lookup"><span data-stu-id="1ab92-448">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="1ab92-449">(See protsess on samaväärne funktsiooni **Reserveeri rida** käitamisega antud partiinumbri puhul).</span><span class="sxs-lookup"><span data-stu-id="1ab92-449">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="1ab92-450">Selle tulemusel näidatakse partii **B11** määratuna kiirkaardi **Lähtereale kinnitatud partiinumbrid** lehele **Partii reserveerimine** ja väli **Reserveerimine** sisaldab kogust **10** partiinumbri **B11** jaoks.</span><span class="sxs-lookup"><span data-stu-id="1ab92-450">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="1ab92-451">Lisaks on välja **Asukoht** väärtuseks **FL-001** ja välja **Litsentsiplaat** väärtuseks on seatud **LP11**.</span><span class="sxs-lookup"><span data-stu-id="1ab92-451">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="1ab92-452">(Kui neid ei ole näha, saate need väljad ruudustikku lisada.)</span><span class="sxs-lookup"><span data-stu-id="1ab92-452">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="1ab92-453">Järgmised tabelid annavad ülevaate sellest, kuidas süsteem käsitleb kindla lao tegevuste tellimusega kooskõlastatud partii reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="1ab92-453">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="1ab92-454">Tabelite sisu tõlgendamiseks oletame, et iga laotoiming käivitatakse tellimusega seotud partii reserveerimisest tuleneva olemasoleva laotöö kontekstis või et iga laotoimingu käivitamine mõjutab seda tüüpi tööd.</span><span class="sxs-lookup"><span data-stu-id="1ab92-454">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="1ab92-455">Neis tabelites näitab veerg Partii kogus on saadaval, kas partii kogus on saadaval lisaks kogusele, mis on juba reserveeritud praeguse tellimusega seotud reserveeringutele, või on juba reserveeritud laotööst, mis pärineb selle tüübi reserveeringutest.</span><span class="sxs-lookup"><span data-stu-id="1ab92-455">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="1ab92-456">Avatud tööde komplekteerimise asukoha alistamine</span><span class="sxs-lookup"><span data-stu-id="1ab92-456">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ab92-457">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="1ab92-457">Key setup parameter</span></span></th>
<th><span data-ttu-id="1ab92-458">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="1ab92-458">Batch quantity is available</span></span></th>
<th><span data-ttu-id="1ab92-459">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="1ab92-459">Key user steps</span></span></th>
<th><span data-ttu-id="1ab92-460">Laotöö</span><span class="sxs-lookup"><span data-stu-id="1ab92-460">Warehouse work</span></span></th>
<th><span data-ttu-id="1ab92-461">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="1ab92-461">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="1ab92-462">Suvand <strong>Luba komplekteerimise asukoha alistamine</strong> on töötajale lubatud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-462">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="1ab92-463">Jah</span><span class="sxs-lookup"><span data-stu-id="1ab92-463">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-464">Valige suvand <strong>Alista asukoht</strong> laorakenduses, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="1ab92-464">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="1ab92-465">Valige <strong>Soovita</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-465">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="1ab92-466">Kinnitage uus asukoht, mis on soovitatud partii koguse kättesaadavuse alusel.</span><span class="sxs-lookup"><span data-stu-id="1ab92-466">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1ab92-467">Praeguse töö puhul toimuvad järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="1ab92-467">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="1ab92-468">Komplekteerimise real olev asukoht uuendatakse uude asukohta.</span><span class="sxs-lookup"><span data-stu-id="1ab92-468">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="1ab92-469">(Kui asukoha määrab litsentsiplaat, on töölao kandele määratud juhuslik litsentsiplaat ja töötaja saab valida mis tahes saadaoleva kogusega litsentsiplaadi.)</span><span class="sxs-lookup"><span data-stu-id="1ab92-469">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="1ab92-470">Kui kogus leitakse uues asukohas rohkem kui ühel litsentsiplaadil, jaotatakse algse komplekteerimise rida mitmeks reaks, et see vastaks igale litsentsiplaadile.</span><span class="sxs-lookup"><span data-stu-id="1ab92-470">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1ab92-471">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="1ab92-471">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-472">Ei</span><span class="sxs-lookup"><span data-stu-id="1ab92-472">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-473">Valige suvand <strong>Alista asukoht</strong> laorakenduses, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="1ab92-473">Select the <strong>Override location</strong> menu item on the warehouse app when you start picking work.</span></span></li>
<li><span data-ttu-id="1ab92-474">Sisestage asukoht käsitsi.</span><span class="sxs-lookup"><span data-stu-id="1ab92-474">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1ab92-475">Toiming <strong>Asukoha alistamine</strong> pole võimalik.</span><span class="sxs-lookup"><span data-stu-id="1ab92-475">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="1ab92-476">See nurjub ja kuvatakse tõrge.</span><span class="sxs-lookup"><span data-stu-id="1ab92-476">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="1ab92-477">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="1ab92-477">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="1ab92-478">Nupp Täis – jaotab töörea kasutaja asukoha ületäitumise tõttu</span><span class="sxs-lookup"><span data-stu-id="1ab92-478">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ab92-479">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="1ab92-479">Key setup parameter</span></span></th>
<th><span data-ttu-id="1ab92-480">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="1ab92-480">Batch quantity is available</span></span></th>
<th><span data-ttu-id="1ab92-481">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="1ab92-481">Key user steps</span></span></th>
<th><span data-ttu-id="1ab92-482">Laotöö</span><span class="sxs-lookup"><span data-stu-id="1ab92-482">Warehouse work</span></span></th>
<th><span data-ttu-id="1ab92-483">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="1ab92-483">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1ab92-484">Valik <strong>Luba töö jaotamine</strong> on lubatud mobiilseadme menüükäsul.</span><span class="sxs-lookup"><span data-stu-id="1ab92-484">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="1ab92-485">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="1ab92-485">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-486">Valige laorakenduses menüüsuvand <strong>Täis</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="1ab92-486">Select the <strong>Full</strong> menu item on the warehouse app when you process picking work.</span></span></li>
<li><span data-ttu-id="1ab92-487">Sisestage väljale <strong>Komplekteeri kogus</strong> nõutava komplekteerimise osaline kogus, et näidata kogu võimsust.</span><span class="sxs-lookup"><span data-stu-id="1ab92-487">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="1ab92-488">Praeguse töö puhul uuendatakse kogus järelejäänud kogusele, mis tuleb komplekteerida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-488">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="1ab92-489">Komplekteeritud koguse uus töö luuakse ja suletakse.</span><span class="sxs-lookup"><span data-stu-id="1ab92-489">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="1ab92-490">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="1ab92-490">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="1ab92-491">Lõpetatud töö komplekteeritud koguse vähendamine (koormast)</span><span class="sxs-lookup"><span data-stu-id="1ab92-491">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ab92-492">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="1ab92-492">Key setup parameter</span></span></th>
<th><span data-ttu-id="1ab92-493">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="1ab92-493">Batch quantity is available</span></span></th>
<th><span data-ttu-id="1ab92-494">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="1ab92-494">Key user steps</span></span></th>
<th><span data-ttu-id="1ab92-495">Laotöö</span><span class="sxs-lookup"><span data-stu-id="1ab92-495">Warehouse work</span></span></th>
<th><span data-ttu-id="1ab92-496">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="1ab92-496">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="1ab92-497">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="1ab92-497">Not applicable</span></span></td>
<td><span data-ttu-id="1ab92-498">Jah</span><span class="sxs-lookup"><span data-stu-id="1ab92-498">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-499">Avage koorma realt leht <strong>Komplekteeritud koguse vähendamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-499">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="1ab92-500">Sisestage kogu kogus, mis ei lähe komplekteerimisele.</span><span class="sxs-lookup"><span data-stu-id="1ab92-500">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="1ab92-501">Valige teisaldamiseks asukoht/litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="1ab92-501">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="1ab92-502">Koorma reaga seotud töö on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-502">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="1ab92-503">Varude teisaldamiseks luuakse uus töö ja suletakse.</span><span class="sxs-lookup"><span data-stu-id="1ab92-503">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1ab92-504">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="1ab92-504">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="1ab92-505">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="1ab92-505">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-506">Ei</span><span class="sxs-lookup"><span data-stu-id="1ab92-506">No</span></span></td>
<td><span data-ttu-id="1ab92-507">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-507">See the previous row.</span></span></td>
<td><span data-ttu-id="1ab92-508">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-508">See the previous row.</span></span></td>
<td><span data-ttu-id="1ab92-509">Kogus reserveeritakse samale partiile samas asukohas ja litsentsiplaadiga (kui asukoht on litsentsiplaadi kontrollitud), mis sisestati komplekteerimise ajal.</span><span class="sxs-lookup"><span data-stu-id="1ab92-509">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="1ab92-510">Kauba teisaldamine laos</span><span class="sxs-lookup"><span data-stu-id="1ab92-510">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="1ab92-511">See laotoiming rakendub ainult tüübi **Töö loomise protsess** teisaldamistele, mitte malli alusel teisaldamistele.</span><span class="sxs-lookup"><span data-stu-id="1ab92-511">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ab92-512">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="1ab92-512">Key setup parameter</span></span></th>
<th><span data-ttu-id="1ab92-513">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="1ab92-513">Batch quantity is available</span></span></th>
<th><span data-ttu-id="1ab92-514">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="1ab92-514">Key user steps</span></span></th>
<th><span data-ttu-id="1ab92-515">Laotöö</span><span class="sxs-lookup"><span data-stu-id="1ab92-515">Warehouse work</span></span></th>
<th><span data-ttu-id="1ab92-516">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="1ab92-516">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="1ab92-517">Töötaja saab <strong>lubada seotud töö varude teisaldamist</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-517">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="1ab92-518">Jah</span><span class="sxs-lookup"><span data-stu-id="1ab92-518">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-519">Alustage teisaldamist laorakenduses.</span><span class="sxs-lookup"><span data-stu-id="1ab92-519">Start a movement on the warehouse app.</span></span></li>
<li><span data-ttu-id="1ab92-520">Sisestage alg- ja lõppasukohad.</span><span class="sxs-lookup"><span data-stu-id="1ab92-520">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="1ab92-521">Kõigi olemasolevate tööde puhul, mida teisaldamine mõjutab, uuendatakse komplekteerimise asukoht uude asukohta.</span><span class="sxs-lookup"><span data-stu-id="1ab92-521">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="1ab92-522">Varude teisaldamiseks luuakse uus töö ja suletakse.</span><span class="sxs-lookup"><span data-stu-id="1ab92-522">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1ab92-523">Kõik olemasolevad reserveeringud, mis mõjutavad koguse liikumist antud asukohast, reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="1ab92-523">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="1ab92-524">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="1ab92-524">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-525">Ei</span><span class="sxs-lookup"><span data-stu-id="1ab92-525">No</span></span></td>
<td><span data-ttu-id="1ab92-526">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-526">See the previous row.</span></span></td>
<td><span data-ttu-id="1ab92-527">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-527">See the previous row.</span></span></td>
<td><span data-ttu-id="1ab92-528">Kõik olemasolevad reserveeringud, mis mõjutavad koguse liikumist antud asukohast, reserveeritakse uuesti sama partii ja uue asukoha ning litsentsiplaadi jaoks (kui asukoht on litsentsiplaadi kontrollitud).</span><span class="sxs-lookup"><span data-stu-id="1ab92-528">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="1ab92-529">Lõpetatud töö komplekteeritud koguse vähendamine (koormast või voost)</span><span class="sxs-lookup"><span data-stu-id="1ab92-529">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ab92-530">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="1ab92-530">Key setup parameter</span></span></th>
<th><span data-ttu-id="1ab92-531">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="1ab92-531">Batch quantity is available</span></span></th>
<th><span data-ttu-id="1ab92-532">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="1ab92-532">Key user steps</span></span></th>
<th><span data-ttu-id="1ab92-533">Laotöö</span><span class="sxs-lookup"><span data-stu-id="1ab92-533">Warehouse work</span></span></th>
<th><span data-ttu-id="1ab92-534">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="1ab92-534">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="1ab92-535">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="1ab92-535">Not applicable</span></span></td>
<td><span data-ttu-id="1ab92-536">Jah</span><span class="sxs-lookup"><span data-stu-id="1ab92-536">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-537">Avage leht <strong>Tühistatud töö</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-537">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="1ab92-538">Taotlemise lehel märkige ruut <strong>Jäta kaubad praegusesse asukohta</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-538">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1ab92-539">Koorma reaga seotud kõik tööd on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-539">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="1ab92-540">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="1ab92-540">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="1ab92-541">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="1ab92-541">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-542">Ei</span><span class="sxs-lookup"><span data-stu-id="1ab92-542">No</span></span></td>
<td><span data-ttu-id="1ab92-543">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-543">See the previous row.</span></span></td>
<td><span data-ttu-id="1ab92-544">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-544">See the previous row.</span></span></td>
<td><span data-ttu-id="1ab92-545">Kogus reserveeritakse samale partiile ja asukohale ning litsentsiplaadile, kuhu kogus tühistamisel jäeti.</span><span class="sxs-lookup"><span data-stu-id="1ab92-545">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-546">Jah</span><span class="sxs-lookup"><span data-stu-id="1ab92-546">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-547">Avage leht <strong>Tühistatud töö</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-547">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="1ab92-548">Taotlemise lehel märkige ruut <strong>Määra kaubad sellesse asukohta</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-548">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="1ab92-549">Praegune töö on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-549">The current work is canceled.</span></span></li>
<li><span data-ttu-id="1ab92-550">Varude teisaldamiseks luuakse uus töö ja suletakse.</span><span class="sxs-lookup"><span data-stu-id="1ab92-550">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1ab92-551">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="1ab92-551">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="1ab92-552">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="1ab92-552">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-553">Ei</span><span class="sxs-lookup"><span data-stu-id="1ab92-553">No</span></span></td>
<td><span data-ttu-id="1ab92-554">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-554">See the previous row.</span></span></td>
<td><span data-ttu-id="1ab92-555">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-555">See the previous row.</span></span></td>
<td><span data-ttu-id="1ab92-556">Kogus reserveeritakse samale partiile ja asukohale ning litsentsiplaadile, kuhu kogus tühistamisel määrati.</span><span class="sxs-lookup"><span data-stu-id="1ab92-556">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-557">Jah/ei</span><span class="sxs-lookup"><span data-stu-id="1ab92-557">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-558">Avage leht <strong>Tühistatud töö</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-558">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="1ab92-559">Taotlemise lehel märkige ruut <strong>Teisalda kaubad sellesse asukohta</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-559">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1ab92-560">Tühistamist ei toetata.</span><span class="sxs-lookup"><span data-stu-id="1ab92-560">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="1ab92-561">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="1ab92-561">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-562">Jah/ei</span><span class="sxs-lookup"><span data-stu-id="1ab92-562">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-563">Avage leht <strong>Tühistatud töö</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-563">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="1ab92-564">Taotlemise lehel märkige ruut <strong>Teisalda kaubad asukoha direktiivi kohaselt</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-564">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1ab92-565">Tühistamist ei toetata.</span><span class="sxs-lookup"><span data-stu-id="1ab92-565">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="1ab92-566">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="1ab92-566">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="1ab92-567">Koguse lühiajaline komplekteerimine – registreerige kogus komplekteerimise ajal asukohas/litsentsiplaadil kui füüsiliselt leidmata.</span><span class="sxs-lookup"><span data-stu-id="1ab92-567">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ab92-568">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="1ab92-568">Key setup parameter</span></span></th>
<th><span data-ttu-id="1ab92-569">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="1ab92-569">Batch quantity is available</span></span></th>
<th><span data-ttu-id="1ab92-570">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="1ab92-570">Key user steps</span></span></th>
<th><span data-ttu-id="1ab92-571">Laotöö</span><span class="sxs-lookup"><span data-stu-id="1ab92-571">Warehouse work</span></span></th>
<th><span data-ttu-id="1ab92-572">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="1ab92-572">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="1ab92-573">Töö erandi tüübiks on seadistatud<strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>puudub</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-573">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="1ab92-574">Jah</span><span class="sxs-lookup"><span data-stu-id="1ab92-574">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-575">Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="1ab92-575">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="1ab92-576">Sisestage väljale <strong>Komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="1ab92-576">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="1ab92-577">Väljale <strong>Põhjus</strong> sisestage väärtus <strong>Ümberjaotamine puudub</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-577">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="1ab92-578">Praegune töö on suletud ja komplekteeritud kogus on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1ab92-578">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="1ab92-579">Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</span><span class="sxs-lookup"><span data-stu-id="1ab92-579">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1ab92-580">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="1ab92-580">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="1ab92-581">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="1ab92-581">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-582">Ei</span><span class="sxs-lookup"><span data-stu-id="1ab92-582">No</span></span></td>
<td><span data-ttu-id="1ab92-583">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-583">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1ab92-584">Lühikese komplekteerimise toiming nurjub ja kuvatakse tõrge.</span><span class="sxs-lookup"><span data-stu-id="1ab92-584">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="1ab92-585">Praegune töö jääb avatuks.</span><span class="sxs-lookup"><span data-stu-id="1ab92-585">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1ab92-586">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="1ab92-586">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="1ab92-587">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Puudub</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-587">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="1ab92-588">Jah</span><span class="sxs-lookup"><span data-stu-id="1ab92-588">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-589">Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="1ab92-589">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="1ab92-590">Sisestage väljale <strong>Komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="1ab92-590">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="1ab92-591">Väljale <strong>Põhjus</strong> sisestage väärtus <strong>Ümberjaotamine puudub</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-591">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="1ab92-592">Praegune töö on suletud ja komplekteeritud kogus on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1ab92-592">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="1ab92-593">Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</span><span class="sxs-lookup"><span data-stu-id="1ab92-593">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1ab92-594">Kõik olemasolevad reserveeringud, mis mõjutavad koguse kohandamist lühikese komplekteerimise asukohast, reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="1ab92-594">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="1ab92-595">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="1ab92-595">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-596">Ei</span><span class="sxs-lookup"><span data-stu-id="1ab92-596">No</span></span></td>
<td><span data-ttu-id="1ab92-597">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-597">See the previous row.</span></span></td>
<td><span data-ttu-id="1ab92-598">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-598">See the previous row.</span></span></td>
<td><span data-ttu-id="1ab92-599">Kõik olemasolevad reserveeringud, mis mõjutavad koguse kohandamist lühikese komplekteerimise asukohast, eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="1ab92-599">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-600">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Käsitsi</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah/ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-600">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="1ab92-601">Lisaks saavad töötajad kasutada suvandit <strong>Luba kauba käsitsi ümberjaotamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-601">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="1ab92-602">Jah</span><span class="sxs-lookup"><span data-stu-id="1ab92-602">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-603">Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="1ab92-603">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="1ab92-604">Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="1ab92-604">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="1ab92-605">Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos käsitsi ümberjaotamisega</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-605">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="1ab92-606">Valige loendist asukoht/litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="1ab92-606">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="1ab92-607">Praeguse töö puhul toimuvad järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="1ab92-607">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="1ab92-608">Praegune komplekteerimise rida on suletud ja komplekteeritud kogus on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1ab92-608">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="1ab92-609">Asetusrida on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-609">The put line is canceled.</span></span></li>
<li><span data-ttu-id="1ab92-610">Luuakse uus komplekteerimise rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-610">A new pick line is created.</span></span> <span data-ttu-id="1ab92-611">See kasutab kasutaja valitud asukohta/litsentsiplaati.</span><span class="sxs-lookup"><span data-stu-id="1ab92-611">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="1ab92-612">Luuakse uus asetusrida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-612">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1ab92-613">Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</span><span class="sxs-lookup"><span data-stu-id="1ab92-613">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1ab92-614">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="1ab92-614">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-615">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Käsitsi</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-615">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="1ab92-616">Lisaks saavad töötajad kasutada suvandit <strong>Luba kauba käsitsi ümberjaotamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-616">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="1ab92-617">Ei</span><span class="sxs-lookup"><span data-stu-id="1ab92-617">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-618">Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="1ab92-618">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="1ab92-619">Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="1ab92-619">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="1ab92-620">Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos käsitsi ümberjaotamisega</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-620">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1ab92-621">Lühikese komplekteerimise toiming nurjub ja kuvatakse tõrge.</span><span class="sxs-lookup"><span data-stu-id="1ab92-621">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="1ab92-622">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="1ab92-622">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-623">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Käsitsi</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-623">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="1ab92-624">Lisaks saavad töötajad kasutada suvandit <strong>Luba kauba käsitsi ümberjaotamine</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-624">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="1ab92-625">Ei</span><span class="sxs-lookup"><span data-stu-id="1ab92-625">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-626">Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="1ab92-626">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="1ab92-627">Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="1ab92-627">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="1ab92-628">Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos käsitsi ümberjaotamisega</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-628">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="1ab92-629">Valige loendist asukoht/litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="1ab92-629">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="1ab92-630">Praeguse töö puhul toimuvad järgmised tegevused.</span><span class="sxs-lookup"><span data-stu-id="1ab92-630">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="1ab92-631">Praegune komplekteerimise rida on suletud ja komplekteeritud kogus on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1ab92-631">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="1ab92-632">Asetusrida on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-632">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1ab92-633">Korrigeerimise tähistamiseks luuakse tüüpide <strong>Inventuur</strong> ja <strong>Müüdud</strong> väljamineku tüübi laokanded.</span><span class="sxs-lookup"><span data-stu-id="1ab92-633">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="1ab92-634">Kõik olemasolevad reserveeringud, mis mõjutavad koguse kohandamist lühikese komplekteerimise asukohast/litsentsiplaadilt, eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="1ab92-634">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-635">Töö erandi tüübiks on seadistatud <strong>Lühike komplekteerimine</strong>, kus <strong>Kauba ümberjaotamine</strong> = <strong>Automaatne</strong>, <strong>Varu korrigeerimine</strong> = <strong>Jah/ei</strong> ja <strong>Eemalda reserveeringud</strong> = <strong>Jah/ei</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-635">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="1ab92-636">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="1ab92-636">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-637">Valige laorakenduses menüüsuvand <strong>Lühike komplekteerimine</strong>, kui käivitate töö komplekteerimise.</span><span class="sxs-lookup"><span data-stu-id="1ab92-637">Select the <strong>Shortpick</strong> menu item on the warehouse app when you run picking work.</span></span></li>
<li><span data-ttu-id="1ab92-638">Sisestage väljale <strong>Lühikese komplekteerimise kogus</strong> väärtus <strong>0</strong> (null).</span><span class="sxs-lookup"><span data-stu-id="1ab92-638">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="1ab92-639">Valige väljal <strong>Põhjus</strong> suvand <strong>Lühike komplekteerimine koos automaatse ümberjaotamisega</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-639">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1ab92-640">Lühiajalist komplekteerimist, mis hõlmab automaatset ümberjaotamist, ei toetata.</span><span class="sxs-lookup"><span data-stu-id="1ab92-640">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="1ab92-641">Lühiajalist komplekteerimist, mis hõlmab automaatset ümberjaotamist, ei toetata.</span><span class="sxs-lookup"><span data-stu-id="1ab92-641">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="1ab92-642">Muuda varude olekut</span><span class="sxs-lookup"><span data-stu-id="1ab92-642">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="1ab92-643">Seda laotoimingut saab sooritada mitmest kirjest.</span><span class="sxs-lookup"><span data-stu-id="1ab92-643">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="1ab92-644">Siin kuvatud näites kasutatakse toimingut **Varude oleku muutmine** lehe **Vaba asukoht** alusel.</span><span class="sxs-lookup"><span data-stu-id="1ab92-644">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="1ab92-645">Võtmeseadistuse parameeter</span><span class="sxs-lookup"><span data-stu-id="1ab92-645">Key setup parameter</span></span></th>
<th><span data-ttu-id="1ab92-646">Partii kogus on saadaval</span><span class="sxs-lookup"><span data-stu-id="1ab92-646">Batch quantity is available</span></span></th>
<th><span data-ttu-id="1ab92-647">Võtmekasutaja sammud</span><span class="sxs-lookup"><span data-stu-id="1ab92-647">Key user steps</span></span></th>
<th><span data-ttu-id="1ab92-648">Laotöö</span><span class="sxs-lookup"><span data-stu-id="1ab92-648">Warehouse work</span></span></th>
<th><span data-ttu-id="1ab92-649">Tellimusega kooskõlastatud partii reserveerimine</span><span class="sxs-lookup"><span data-stu-id="1ab92-649">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="1ab92-650">Vahekaardil <strong>Ladu</strong>, kirjes <strong>Ladu</strong> on välja <strong>Eemalda reserveeringud ja märgised</strong> väärtuseks määratud <strong>Reserveeringud</strong> või <strong>Märgistused ja reserveeringud</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-650">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="1ab92-651">Jah</span><span class="sxs-lookup"><span data-stu-id="1ab92-651">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-652">Valige kindel asukoht.</span><span class="sxs-lookup"><span data-stu-id="1ab92-652">Select a specific location.</span></span></li>
<li><span data-ttu-id="1ab92-653">Valige rida, millel on kindel kaup, asukoht ja litsentsiplaat (kui asukoht on litsentsiplaadi kontrollitud).</span><span class="sxs-lookup"><span data-stu-id="1ab92-653">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="1ab92-654">Valige <strong>Varude oleku muutmine</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-654">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="1ab92-655">Seadke välja <strong>Varude olek</strong> väärtuseks <strong>Blokeerimine</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-655">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1ab92-656">Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-656">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1ab92-657">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="1ab92-657">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="1ab92-658">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="1ab92-658">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="1ab92-659">Tüübi <strong>Varude oleku muutmine</strong> kaks laokannet luuakse selleks, et tähistada varude oleku dimensiooni muutumist.</span><span class="sxs-lookup"><span data-stu-id="1ab92-659">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="1ab92-660">Tüübi <strong>Varude blokeerimine</strong> ja probleemitüübi <strong>Reserveeritud füüsiline</strong> luuakse selleks, et tähistada blokeeritud koguse reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="1ab92-660">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-661">Ei</span><span class="sxs-lookup"><span data-stu-id="1ab92-661">No</span></span></td>
<td><span data-ttu-id="1ab92-662">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-662">See the previous row.</span></span></td>
<td><span data-ttu-id="1ab92-663">Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-663">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="1ab92-664">Reserveering eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="1ab92-664">The reservation is removed.</span></span></li>
<li><span data-ttu-id="1ab92-665">Tüübi <strong>Varude oleku muutmine</strong> kaks laokannet luuakse selleks, et tähistada varude oleku dimensiooni muutumist.</span><span class="sxs-lookup"><span data-stu-id="1ab92-665">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="1ab92-666">Tüübi <strong>Varude blokeerimine</strong> ja probleemitüübi <strong>Reserveeritud füüsiline</strong> luuakse selleks, et tähistada blokeeritud koguse reserveerimist.</span><span class="sxs-lookup"><span data-stu-id="1ab92-666">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="1ab92-667">Vahekaardil <strong>Ladu</strong>, kirjes <strong>Ladu</strong> on välja <strong>Eemalda reserveeringud ja märgised</strong> väärtuseks määratud <strong>Puudub</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-667">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="1ab92-668">Jah</span><span class="sxs-lookup"><span data-stu-id="1ab92-668">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="1ab92-669">Valige kindel asukoht.</span><span class="sxs-lookup"><span data-stu-id="1ab92-669">Select a specific location.</span></span></li>
<li><span data-ttu-id="1ab92-670">Valige rida, millel on kindel kaup, asukoht ja litsentsiplaat (kui asukoht on litsentsiplaadi kontrollitud).</span><span class="sxs-lookup"><span data-stu-id="1ab92-670">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="1ab92-671">Valige <strong>Varude oleku muutmine</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-671">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="1ab92-672">Seadke välja <strong>Varude olek</strong> väärtuseks <strong>Blokeerimine</strong>.</span><span class="sxs-lookup"><span data-stu-id="1ab92-672">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="1ab92-673">Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-673">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="1ab92-674">Kogus reserveeritakse sama partii jaoks uuesti.</span><span class="sxs-lookup"><span data-stu-id="1ab92-674">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="1ab92-675">Süsteem määrab juhuslikult asukoha ja litsentsiplaadi (kui asukoht on litsentsiplaadi kontrollitud), kus kogus on saadaval.</span><span class="sxs-lookup"><span data-stu-id="1ab92-675">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1ab92-676">Ei</span><span class="sxs-lookup"><span data-stu-id="1ab92-676">No</span></span></td>
<td><span data-ttu-id="1ab92-677">Vt eelmist rida.</span><span class="sxs-lookup"><span data-stu-id="1ab92-677">See the previous row.</span></span></td>
<td><span data-ttu-id="1ab92-678">Varude oleku muudatused ei ole töö jaoks reserveeritud koguste puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-678">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="1ab92-679">Varude oleku muudatused pole lubatud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-679">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="1ab92-680">Kitsendused</span><span class="sxs-lookup"><span data-stu-id="1ab92-680">Limitations</span></span>

- <span data-ttu-id="1ab92-681">Paindliku lao taseme dimensiooni reserveerimise funktsionaalsus ei toeta järgmisi funktsioone.</span><span class="sxs-lookup"><span data-stu-id="1ab92-681">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="1ab92-682">Tegeliku kaalu haldus</span><span class="sxs-lookup"><span data-stu-id="1ab92-682">Catch weight management</span></span>
    - <span data-ttu-id="1ab92-683">Füüsiline negatiivne laovaru</span><span class="sxs-lookup"><span data-stu-id="1ab92-683">Physical negative inventory</span></span>
    - <span data-ttu-id="1ab92-684">Tellitud tarnete reserveerimine</span><span class="sxs-lookup"><span data-stu-id="1ab92-684">Reservation against ordered supply</span></span>
    - <span data-ttu-id="1ab92-685">Üleviimistellimuste ja toormaterjalide komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="1ab92-685">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="1ab92-686">Konteineri konsolideerimise reeglil on direktiivi ühiku alusel pakkimisel piirangud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-686">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="1ab92-687">Tellimusega kooskõlastatud reserveeringute puhul on soovitatav mitte kasutada konteineri loomise malle, mille puhul väli **Pakk direktiiviühiku järgi** on lubatud.</span><span class="sxs-lookup"><span data-stu-id="1ab92-687">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="1ab92-688">Praeguses kujunduses ei kasutata asukoha direktiive laotöö loomisel.</span><span class="sxs-lookup"><span data-stu-id="1ab92-688">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="1ab92-689">Seetõttu rakendatakse konteinerite voo etapis ainult madalaimat ühikut ühikute seeriagrupis (laoühikutes).</span><span class="sxs-lookup"><span data-stu-id="1ab92-689">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
