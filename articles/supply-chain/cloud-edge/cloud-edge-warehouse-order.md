---
title: Laotellimused pilv- ja perimeeterskaalaüksuste jaoks
description: See teema annab teavet lao tellimuste võimaluse kohta, mida kasutatakse lao skaalaühiku töökoormuse osana.
author: perlynne
ms.date: 04/13/2021
ms.topic: article
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c24c08771c83453bb65312700cf994c7a800b7fd
ms.sourcegitcommit: 639175a39da38edd13e21eeb5a1a5ca62fa44d99
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/15/2021
ms.locfileid: "5899115"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="b91dd-103">Laotellimused pilv- ja perimeeterskaalaüksuste jaoks</span><span class="sxs-lookup"><span data-stu-id="b91dd-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="b91dd-104">Mitte kogu ettevõtte funktsionaalsus ei ole skaalaühikute töökoormuste kasutamisel avalikus eelvaates täielikult toetatud.</span><span class="sxs-lookup"><span data-stu-id="b91dd-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="b91dd-105">Kui kasutate skaalaühikuid, kasutage kindlasti ainult neid protsesse, mida see teema konkreetselt toetab.</span><span class="sxs-lookup"><span data-stu-id="b91dd-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="b91dd-106">Mis on laotellimused?</span><span class="sxs-lookup"><span data-stu-id="b91dd-106">What are warehouse orders?</span></span>

<span data-ttu-id="b91dd-107">*Laotellimused* on tellimuse tüüp, mis loodi keskuse ja skaalaüksuse lao juurutuste toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="b91dd-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="b91dd-108">Need võimaldavad teil lao töökoormuse skaalaühikus käitamisel võtta vastu varusid.</span><span class="sxs-lookup"><span data-stu-id="b91dd-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="b91dd-109">Neid kasutatakse praegu ainult ostutellimustega.</span><span class="sxs-lookup"><span data-stu-id="b91dd-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="b91dd-110">Laotellimusi kasutatakse laohalduse töötlemise osana, näiteks kui mobiilirakendust Warehouse Management kasutatakse sissetuleva ostutellimuse töötlemisel füüsilise vaba kaubavaru registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="b91dd-110">Warehouse orders are used as part of warehouse management processing, such as when the Warehouse Management mobile app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="b91dd-111">Laotellimused luuakse osana *lattu vabastamise* protsessist, mis on saadaval ostutellimustele, mis määratlevad kaaluühiku lao ja kaubad, mis on lubatud laohaldusprotsesside kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="b91dd-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b91dd-112">Laotellimused on saadaval ainult juurutustes, mis kasutavad [laohaldustöökoormusi pilv- ja perimeeterskaalaüksuste](cloud-edge-workload-warehousing.md) jaoks.</span><span class="sxs-lookup"><span data-stu-id="b91dd-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="b91dd-113">Laotellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="b91dd-113">Create a warehouse order</span></span>

<span data-ttu-id="b91dd-114">Laotellimuse loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b91dd-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="b91dd-115">Logige sisse keskuses töötavasse rakendusse Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b91dd-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="b91dd-116">(Peate käivitama protsessi *Vabasta lattu* ajal, kui olete keskusesse sisse logitud.)</span><span class="sxs-lookup"><span data-stu-id="b91dd-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="b91dd-117">Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="b91dd-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="b91dd-118">Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="b91dd-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="b91dd-119">Seotud laotellimuse ridade vaatamiseks avage vastav ostutellimus, valige jaotises **Ostutellimuse read** rida ja valige seejärel suvand **Ladu \> Laotellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="b91dd-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="b91dd-120">Kõigi ridade vaatamiseks avage **Laohaldus \> Päringud ja haldus \> Laotellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="b91dd-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

<span data-ttu-id="b91dd-121">Pakett-töö kaudu saate käivitada ka *lattu väljastamise* protsessi, selleks avage **Laohaldus > Lattu väljastamine > Ostutellimuste automaatne väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="b91dd-121">You can also trigger the *Release to warehouse* process from a batch job by going to **Warehouse management > Release to warehouse > Automatic release of purchase orders**.</span></span> <span data-ttu-id="b91dd-122">Pakett-töö häälestamisel saate päringu põhjal valida konkreetsed ostutellimuse read.</span><span class="sxs-lookup"><span data-stu-id="b91dd-122">When setting up the batch job, you can select specific purchase order lines based on a query.</span></span> <span data-ttu-id="b91dd-123">Tavaline stsenaarium oleks häälestada korduv pakett-töö, millega väljastatakse kõik kinnitatud ostutellimuse read, mis saabuvad järgmisel päeval.</span><span class="sxs-lookup"><span data-stu-id="b91dd-123">A typical scenario would be to set up a recurrent batch job that releases all the confirmed purchase order lines expected to arrive the next day.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="b91dd-124">Laotellimuse tühistamine</span><span class="sxs-lookup"><span data-stu-id="b91dd-124">Cancel a warehouse order</span></span>

<span data-ttu-id="b91dd-125">Protsessi *Vabasta lattu* osana on ostutellimuse laokanded seotud laotellimustega ja keskuse poolt värskendamiseks lukus.</span><span class="sxs-lookup"><span data-stu-id="b91dd-125">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="b91dd-126">Kui vabastasite lattu ekslikult või kui teil on mõni muu põhjus laotellimuse ridade loomise tühistamiseks, saate taotleda laotellimuse ridade tühistamise.</span><span class="sxs-lookup"><span data-stu-id="b91dd-126">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="b91dd-127">Laotellimuse ridade tühistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b91dd-127">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="b91dd-128">Logige sisse keskuses töötavasse rakenduse Supply Chain Management eksemplari.</span><span class="sxs-lookup"><span data-stu-id="b91dd-128">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="b91dd-129">Avage **Laohaldus \> Päringud ja haldus \> Laotellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="b91dd-129">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="b91dd-130">Valige vastav rida.</span><span class="sxs-lookup"><span data-stu-id="b91dd-130">Select the relevant line.</span></span>
1. <span data-ttu-id="b91dd-131">Valige tegevuspaanil suvand **Tühista laotellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="b91dd-131">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="b91dd-132">Ridade tühistamise taotlus lükatakse tagasi kõikide ridade puhul, mis on juba tühistamise ootel või mida töödeldakse aktiivselt laos, mis käitab oma töökoormust skaalaüksusel.</span><span class="sxs-lookup"><span data-stu-id="b91dd-132">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="b91dd-133">Laotellimuse jälgimine</span><span class="sxs-lookup"><span data-stu-id="b91dd-133">Monitor a warehouse order</span></span>

<span data-ttu-id="b91dd-134">Vaates **Laotellimuse read** saate jälgida sissetuleva vastuvõtu edenemist, vaadates väärtuseid veerus **Vastuvõtmiseks järelejäänud kogus**.</span><span class="sxs-lookup"><span data-stu-id="b91dd-134">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="b91dd-135">Mobiilirakenduse Warehouse Management abil tehtud tööga seotud üksikasjade vaatamiseks järgige ühte järgmistest sammudest.</span><span class="sxs-lookup"><span data-stu-id="b91dd-135">To view details that are related to work that is done by using the Warehouse Management mobile app, follow one of these steps.</span></span>

- <span data-ttu-id="b91dd-136">Avage **Laohaldus \> Päringud ja aruanded \> Laotellimuse read** ja kasutage otsitavate ridade leidmiseks filtrit.</span><span class="sxs-lookup"><span data-stu-id="b91dd-136">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="b91dd-137">Avage **Hanked \> Ostutellimused \> Kõik ostutellimused** ja avage seotud ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="b91dd-137">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="b91dd-138">Jaotises **Ostutelimuse read** valige üks või mitu rida ja seejärel valige tööriistaribal **Ladu \> Lao sissetuleku kirjed**.</span><span class="sxs-lookup"><span data-stu-id="b91dd-138">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
