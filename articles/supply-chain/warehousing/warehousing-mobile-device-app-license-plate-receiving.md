---
title: Identifitseerimisnumbri vastuvõtmine ladustamisrakenduse kaudu
description: Selles teemas selgitatakse, kuidas häälestada ladustamisrakendust, et toetada identifitseerimisnumbri vastuvõtmisprotsessi füüsiliste varude vastuvõtmiseks.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346372"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a><span data-ttu-id="712ec-103">Identifitseerimisnumbri vastuvõtmine ladustamisrakenduse kaudu</span><span class="sxs-lookup"><span data-stu-id="712ec-103">License plate receiving via the warehousing app</span></span>

<span data-ttu-id="712ec-104">Selles teemas selgitatakse, kuidas häälestada ladustamisrakendust, et see toetaks identifitseerimisnumbri vastuvõtmisprotsessi füüsiliste varude vastuvõtmiseks.</span><span class="sxs-lookup"><span data-stu-id="712ec-104">This topic explains how to set up the warehousing app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="712ec-105">Selle funktsiooni abil saate kiiresti kirjendada sissetulevate varude vastuvõtmist, mis on seotud saadetise eelteatisega (ASN).</span><span class="sxs-lookup"><span data-stu-id="712ec-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="712ec-106">Süsteem loob automaatselt ASN-i, kui üleviimistellimuse saatmiseks kasutatakse laohaldusprotsesse.</span><span class="sxs-lookup"><span data-stu-id="712ec-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="712ec-107">Ostutellimuse protsessi puhul saab ASN-i käsitsi kirjendada või automaatselt importida sissetuleva ASN-i andmeüksuse protsessi abil.</span><span class="sxs-lookup"><span data-stu-id="712ec-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="712ec-108">ASN-i andmed on seotud koormate ja saadetistega *pakkestruktuuride* kaudu, kus kaubaalused (peamised identifitseerimisnumbrid) võivad sisaldada kaste (pesastatud identifitseerimisnumbrid).</span><span class="sxs-lookup"><span data-stu-id="712ec-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="712ec-109">Selleks, et vähendada laokannete arvu, kui kasutatakse pesastatud identifitseerimisnumbreid, siis registreerib süsteem füüsilise vaba kaubavaru peamisele identifitseermisnumbrile.</span><span class="sxs-lookup"><span data-stu-id="712ec-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="712ec-110">Füüsiline vaba kaubavaru liikumise käivitamiseks pesastatud identifitseerimisnumbrilt peamisele identifitseerimisnumbrile pakkestruktuuri andmete põhjal, peab mobiilses seadmes olema menüü üksus, mis põhineb töö loomise protsessil *Pakena pesastatud identifitseerimisnumbritele*.</span><span class="sxs-lookup"><span data-stu-id="712ec-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="712ec-111">Kuva või jäta vastuvõtmise kokkuvõte leht</span><span class="sxs-lookup"><span data-stu-id="712ec-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="712ec-112">Saate kasutada funktsiooni *Kokkuvõtte lehe vastuvõtmise juhtimine mobiilses seadmes*, et kasutada täiendava üksikasjaliku ladustamisrakenduse voogu identifitseerimisnumbri vastuvõtmisprotsessi osana.</span><span class="sxs-lookup"><span data-stu-id="712ec-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed warehousing app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="712ec-113">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="712ec-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="712ec-114">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="712ec-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="712ec-115">Tööruumis **Funktsioonihaldus** loetletakse seda funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="712ec-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="712ec-116">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="712ec-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="712ec-117">**Funktsiooni nimi:** *kokkuvõtte lehe vastuvõtmise juhtimine mobiilses seadmes*</span><span class="sxs-lookup"><span data-stu-id="712ec-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="712ec-118">Kui see funktsioon on sisse lülitatud, annavad identifitseerimisnumbri vastuvõtmise või identifitseerimisnumbri vastuvõtmise ja ladustamise menüü üksused mobiilses seadmes sätte **Kuva vastuvõttev kokkuvõtte leht**.</span><span class="sxs-lookup"><span data-stu-id="712ec-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="712ec-119">Sellel sättel on järgmised suvandid.</span><span class="sxs-lookup"><span data-stu-id="712ec-119">This setting has the following options:</span></span>

- <span data-ttu-id="712ec-120">**Kuva üksikasjalik kokkuvõte** – identifitseerimisnumbri vastuvõtmise ajal kuvatakse töötajatele täiendav leht, mis sisaldab täielikku ASN-i teavet.</span><span class="sxs-lookup"><span data-stu-id="712ec-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="712ec-121">**Jäta kokkuvõte vahele** – töötajatele ei kuvata täielikku ASN-i teavet.</span><span class="sxs-lookup"><span data-stu-id="712ec-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="712ec-122">Lao töötajad ei saa määrata ka likvideerimiskoodi või lisada erandeid vastuvõtu protsessi ajal.</span><span class="sxs-lookup"><span data-stu-id="712ec-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="712ec-123">Takista üleviimistellimuse – saadetud identifitseerimisnumbrite kasutamist muudes ladudes, mis ei ole sihtkoha ladu</span><span class="sxs-lookup"><span data-stu-id="712ec-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="712ec-124">Identifitseerimisnumbri vastuvõtmisprotsessi ei saa kasutada, kui ASN sisaldab juba olemasolevat identifitseerimisnumbri ID-d ja sellel on füüsiline vaba kaubavaru muus lao asukohas, kus identifitseerimisnumbri registreerimine toimub.</span><span class="sxs-lookup"><span data-stu-id="712ec-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="712ec-125">Üleviimistellimuste olukorras, kus transiitlaos ei jälgita identifitseerimisnumbreid (ja seega ei jälgita ka füüsilist vaba kaubavaru identifitseerimisnumbri kohta), saate kasutada funktsiooni *Takista üleviimistellimuse – saadetud identifitseerimisnumbrite kasutamist muudes ladudes, mis ei ole sihtkoha ladu*, et vältida transiidis olevate identifitseerimisnumbrite füüsilise vaba kaubavaru värskendamist.</span><span class="sxs-lookup"><span data-stu-id="712ec-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="712ec-126">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="712ec-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="712ec-127">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="712ec-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="712ec-128">Tööruumis **Funktsioonihaldus** loetletakse seda funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="712ec-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="712ec-129">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="712ec-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="712ec-130">**Funktsiooni nimi:** *Takista üleviimistellimuse saadetud identifitseerimisnumbrite kasutamist muudes ladudes, mis ei ole sihtkoha ladu*</span><span class="sxs-lookup"><span data-stu-id="712ec-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="712ec-131">Selle funktsiooni haldamiseks, kui see on saadaval, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="712ec-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="712ec-132">Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="712ec-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="712ec-133">Määrake vahekaardi **Üldine** kiirkaardil **Identifitseerimisnumbrid** väljale **Transiitlao identifitseerimisnumbri poliitika** üks järgmistest väärtustest.</span><span class="sxs-lookup"><span data-stu-id="712ec-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="712ec-134">**Luba mittejälitatud identifitseerimisnumbri taaskasutamine** – süsteem töötab samamoodi nagu siis, kui funktsioon *Takista üleviimistellimuse saadetud identifitseerimisnumbrite kasutamist muudes ladudes, mis ei ole sihtkoha ladu* pole saadaval.</span><span class="sxs-lookup"><span data-stu-id="712ec-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="712ec-135">See väärtus on vaikesäte funktsiooni esmakordsel aktiveerimisel.</span><span class="sxs-lookup"><span data-stu-id="712ec-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="712ec-136">**Takista mittejälitatud identifitseerimisnumbri korduvkasutamist** – sihtkoha laos on lubatud ainult need vaba kauvabaru värskendused, mis on seotud saadetud identifitseerimisnumbriga, kuni üleviimistellimus on vastu võetud.</span><span class="sxs-lookup"><span data-stu-id="712ec-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="712ec-137">Lisateave</span><span class="sxs-lookup"><span data-stu-id="712ec-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="712ec-138">Lisateavet mobiilse seadme menüü üksuste kohta vt teemast [Mobiilsete seadmete seadistamine laotöö jaoks](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="712ec-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
