---
title: Reeglid
description: See teema kirjeldab, kuidas seadistada reegleid, et määrata, kuidas kulusid peaks Global Inventory Accounting teenuses arvesse võtma.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 74d99d3eefdcaaa7f6551668990b702396b32ffc
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273144"
---
# <a name="conventions"></a><span data-ttu-id="f7312-103">Reeglid</span><span class="sxs-lookup"><span data-stu-id="f7312-103">Conventions</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="f7312-104">Reeglid on konteiner poliitikate komplektile, mis mõjutavad süsteemi käitumist.</span><span class="sxs-lookup"><span data-stu-id="f7312-104">A convention is a container for a set of policies that affect system behavior.</span></span> <span data-ttu-id="f7312-105">Äritegevuse nõuetele toetudes peate määrama reeglid kasutades erinevate poliitikate kombinatsiooni, mis määravad, kuidas tuleb kulusid teenuses Global Inventory Accounting arvestada.</span><span class="sxs-lookup"><span data-stu-id="f7312-105">Based on your business requirements, you must define conventions by using a combination of the various policies that establish how costs should be accounted in Global Inventory Accounting.</span></span> <span data-ttu-id="f7312-106">Kõikide pearaamatute puhul rakendatud raamatupidamispoliitikate ühtsuse tagamiseks saate iga reegli seostada ühe või mitme pearaamatuga.</span><span class="sxs-lookup"><span data-stu-id="f7312-106">You can associate each convention with one or more ledgers to ensure consistency in accounting policies that are applied across ledgers.</span></span>

<span data-ttu-id="f7312-107">Oma reeglite seadistamiseks minge **Globaalne laoarvestus \> Seadistamine \> Reeglid**.</span><span class="sxs-lookup"><span data-stu-id="f7312-107">To set up your conventions, go to **Global inventory accounting \> Setup \> Conventions**.</span></span> <span data-ttu-id="f7312-108">Määrake igale reeglile järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="f7312-108">For each convention, set the following fields:</span></span>

- <span data-ttu-id="f7312-109">**Nimi** – sisestage reegli nimi.</span><span class="sxs-lookup"><span data-stu-id="f7312-109">**Name** – Enter the name of the convention.</span></span>
- <span data-ttu-id="f7312-110">**Kirjeldus** – sisestage reegli kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="f7312-110">**Description** – Enter a description of the convention.</span></span>
- <span data-ttu-id="f7312-111">**Kuluobjekti poliitika** – valige kuluobjekti poliitika.</span><span class="sxs-lookup"><span data-stu-id="f7312-111">**Cost Object policy** – Select a cost object policy.</span></span> <span data-ttu-id="f7312-112">Need põhimõtted määratlevad granulaarsuse taseme, mida süsteem laoväärtuse arvutamisel ja säilitamiseks kohaldab.</span><span class="sxs-lookup"><span data-stu-id="f7312-112">These policies determine the level of granularity that the system applies to calculate and maintain the inventory value.</span></span> <span data-ttu-id="f7312-113">Saadaval on järgmised eelmääratud valikud:</span><span class="sxs-lookup"><span data-stu-id="f7312-113">The following predefined options are available:</span></span>

    - <span data-ttu-id="f7312-114">Toode</span><span class="sxs-lookup"><span data-stu-id="f7312-114">Product</span></span>
    - <span data-ttu-id="f7312-115">Toode – Koht</span><span class="sxs-lookup"><span data-stu-id="f7312-115">Product – Site</span></span>
    - <span data-ttu-id="f7312-116">Toode – Koht – Ladu</span><span class="sxs-lookup"><span data-stu-id="f7312-116">Product – Site – Warehouse</span></span>

    <span data-ttu-id="f7312-117">Näiteks kui valite *Toode – Koht*, siis iga lao liikumise (sissevool või väljavool) jaoks arvutab ja haldab süsteem iga toote laokulu koha tasemel.</span><span class="sxs-lookup"><span data-stu-id="f7312-117">For example, if you select *Product – Site*, for every inventory movement (inflow or outflow), the system calculates and maintains the inventory cost of each product at the site level.</span></span> <span data-ttu-id="f7312-118">Seetõttu ei mõjuta lao liikumised madalamatel tasemetel (nt laotasemel) laoväärtust.</span><span class="sxs-lookup"><span data-stu-id="f7312-118">Therefore, inventory movements at lower levels, such as the warehouse level, don't affect the inventory value.</span></span> <span data-ttu-id="f7312-119">(Laotaseme ülekanne on näiteks kauba ülekanne ühel laokohal kahe lao vahel) Samamoodi ei saa te varude maksumust vaadata madalamal tasemel, näiteks laotasemel.</span><span class="sxs-lookup"><span data-stu-id="f7312-119">(An example of a warehouse-level transfer is an item transfer between two warehouses in one site.) Likewise, you can't view the inventory cost at a lower level, such as the warehouse level.</span></span>

- <span data-ttu-id="f7312-120">**Sisendi mõõtmise aluspoliitika** – valige sisendi mõõtmise aluspoliitika.</span><span class="sxs-lookup"><span data-stu-id="f7312-120">**Input measurement basis policy** – Select an input measurement basis policy.</span></span> <span data-ttu-id="f7312-121">Need poliitikad määratlevad kulud, mis tuleks laokontole kanda ja kulud, mida tuleb nõuda.</span><span class="sxs-lookup"><span data-stu-id="f7312-121">These policies determine the costs that should flow into the inventory account and the costs that should be charged.</span></span> <span data-ttu-id="f7312-122">Kaubandusettevõtete jaoks on asjakohased järgmised valikud:</span><span class="sxs-lookup"><span data-stu-id="f7312-122">The following options are relevant for trading companies:</span></span>

    - <span data-ttu-id="f7312-123">**Tavaline ajalooline** – kõikide kulukomponentide voog laokontole.</span><span class="sxs-lookup"><span data-stu-id="f7312-123">**Normal historical** – All the cost components flow into the inventory account.</span></span>
    - <span data-ttu-id="f7312-124">**Standartne** : standardsed kuluvood laokontodesse ning erinevus rakendatud kulu ja tegelike kulude vahel kantakse dispersioonikontodele.</span><span class="sxs-lookup"><span data-stu-id="f7312-124">**Standard** – Standard cost flows into the inventory accounts, and the difference between the applied cost and the actual costs is charged to variance accounts.</span></span> <span data-ttu-id="f7312-125">Kui soovite luua *standardse* sisendi mõõtmise aluspoliitikat, peate esmalt looma hinnakirja, kus poliitika saab otsida kauba standardset kulu.</span><span class="sxs-lookup"><span data-stu-id="f7312-125">If you want to create a *Standard* input measurement basis policy, you must first create a price list where the policy can look up the item's standard cost.</span></span>
    - <span data-ttu-id="f7312-126">**Hinnakirjad** – Global Inventory Accounting teenus toetab kauba hindade toomist mitmest juriidilisest isikust.</span><span class="sxs-lookup"><span data-stu-id="f7312-126">**Price lists** – Global Inventory Accounting supports fetching item prices from multiple legal entities.</span></span> <span data-ttu-id="f7312-127">Saate määratleda hinnakirja, mida sisendi mõõtmise aluspoliitika hakkab kasutama.</span><span class="sxs-lookup"><span data-stu-id="f7312-127">You can define a price list that the input measurement basis policy will use.</span></span> <span data-ttu-id="f7312-128">Sel viisil saab süsteem teada, kust kauba hinda otsida.</span><span class="sxs-lookup"><span data-stu-id="f7312-128">In this way, the system will know where to look up the item price.</span></span> <span data-ttu-id="f7312-129">Hinnakirjade seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="f7312-129">Follow these steps to set up price lists:</span></span>

        1. <span data-ttu-id="f7312-130">Väljale **Nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="f7312-130">In the **Name** field, enter a name.</span></span>
        1. <span data-ttu-id="f7312-131">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="f7312-131">In the **Description** field, enter a description.</span></span>
        1. <span data-ttu-id="f7312-132">Väljal **Kulu tüüp** valige kulu tüüp (*Standardne kulu* või *Planeeritud kulu*).</span><span class="sxs-lookup"><span data-stu-id="f7312-132">In the **Costing type** field, select a costing type (*Standard cost* or *Planned cost*).</span></span>
        1. <span data-ttu-id="f7312-133">Valige väljal **Hinna tüüp** hinnatüüp (*Kulu*, *Ost* või *Müügihind*).</span><span class="sxs-lookup"><span data-stu-id="f7312-133">In the **Price type** field, select a price type (*Cost*, *Purchase*, or *Sales price*).</span></span>
        1. <span data-ttu-id="f7312-134">Kuluarvutue versiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="f7312-134">Add a costing version.</span></span>
        1. <span data-ttu-id="f7312-135">Tegevuspaanil valige **Hind**, et kinnitada kauba hinnad hinnakirjas.</span><span class="sxs-lookup"><span data-stu-id="f7312-135">On the Action Pane, select **Price** to validate the item prices on the price list.</span></span>

- <span data-ttu-id="f7312-136">**Kuluvoo eelduse poliitika** – valige kuluvoo eelduse poliitika.</span><span class="sxs-lookup"><span data-stu-id="f7312-136">**Cost flow assumption policy** – Select a cost flow assumption policy.</span></span> <span data-ttu-id="f7312-137">Need poliitikad määratlevad, kuidas eemaldatakse kulud varudest ja esitatakse müüdud kaupade maksumusena.</span><span class="sxs-lookup"><span data-stu-id="f7312-137">These policies determine how costs are removed from inventory and reported as the cost of goods sold.</span></span> <span data-ttu-id="f7312-138">Saadaval on järgmised eelmääratud valikud:</span><span class="sxs-lookup"><span data-stu-id="f7312-138">The following predefined options are available:</span></span>

    - <span data-ttu-id="f7312-139">Keskmine</span><span class="sxs-lookup"><span data-stu-id="f7312-139">Average</span></span>
    - <span data-ttu-id="f7312-140">Konkreetne – partii</span><span class="sxs-lookup"><span data-stu-id="f7312-140">Specific – Batch</span></span>

    > [!NOTE]
    > <span data-ttu-id="f7312-141">Global Inventory Accounting on tähtajatu laovarude süsteem.</span><span class="sxs-lookup"><span data-stu-id="f7312-141">Global Inventory Accounting is a perpetual inventory system.</span></span> <span data-ttu-id="f7312-142">Süsteem jälgib laoväärtust kannete kaupa.</span><span class="sxs-lookup"><span data-stu-id="f7312-142">Therefore, the system tracks the inventory value on a transaction-by-transaction basis.</span></span>

- <span data-ttu-id="f7312-143">**Kuluelemendi poliitika** – saate määrata kuluelemendi poliitikad ja siduda need selle väljaga.</span><span class="sxs-lookup"><span data-stu-id="f7312-143">**Cost element policy** – You can define cost element policies and link them to this field.</span></span> <span data-ttu-id="f7312-144">*Kuluelement* on sündmuse tarbitava ressursi kulu.</span><span class="sxs-lookup"><span data-stu-id="f7312-144">A *cost element* is the cost of a resource that is consumed by an event.</span></span> <span data-ttu-id="f7312-145">Kuluelemente saate kasutada kulude jälgimiseks ja kategoriseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="f7312-145">You can use cost elements to track and categorize costs.</span></span> <span data-ttu-id="f7312-146">Kuluelemendi poliitikate loomiseks sisestage teave järgmistesse kohtadesse:</span><span class="sxs-lookup"><span data-stu-id="f7312-146">To create cost element policies, enter information in the following places:</span></span>

    - <span data-ttu-id="f7312-147">**Nimi** väli</span><span class="sxs-lookup"><span data-stu-id="f7312-147">**Name** field</span></span>
    - <span data-ttu-id="f7312-148">**Kirjelduse** väli</span><span class="sxs-lookup"><span data-stu-id="f7312-148">**Description** field</span></span>
    - <span data-ttu-id="f7312-149">**Kuluelementide** loend</span><span class="sxs-lookup"><span data-stu-id="f7312-149">**Cost element** list</span></span>
    - <span data-ttu-id="f7312-150">**Reeglite** ruudustik</span><span class="sxs-lookup"><span data-stu-id="f7312-150">**Rules** grid</span></span>

    <span data-ttu-id="f7312-151">Kui te ei soovi laoväärtust veelgi täpsemaks muuta, peate looma kuluelemendi loendi, kus on üks kuluelement.</span><span class="sxs-lookup"><span data-stu-id="f7312-151">If you don't want to break down the inventory value further, you must still create a cost element list that has a single cost element.</span></span> <span data-ttu-id="f7312-152">Seejärel peate looma kuluelemendi poliitika, et vastendada kõik asjakohased mõõtmise tüübid (kulukomponendid) selle kuluelemendiga.</span><span class="sxs-lookup"><span data-stu-id="f7312-152">You must then create a cost element policy to map all the relevant measurement types (cost components) to that cost element.</span></span>
