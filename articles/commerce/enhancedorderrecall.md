---
title: Tellimuse tagasikutsumise toiming kassas
description: Selles teemas selgitatakse funktsioonivõimalusi, mis on saadaval kassas täiustatud tellimuse tagasikutsumise lehtedel.
author: hhainesms
manager: annbe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 174821fce4baf81e4298da4b066f855bfec98ca5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585126"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="ee9b5-103">Tellimuse tagasikutsumise toiming kassas</span><span class="sxs-lookup"><span data-stu-id="ee9b5-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ee9b5-104">**Tellimuse tagasikutsumise** toiming rakenduse Commerce kassas (POS) pakub värskendatud tellimuste otsimise ja filtreerimise funktsioone ning tellimusespetsiifilist teavet.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="ee9b5-105">See funktsioon on saadaval rakenduse Commerce versioonis 10.0.15 ja uuemates.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="ee9b5-106">Selle funktsiooni lubamiseks lülitage sisse funktsioon **Täiustatud tellimuse tagasikutsumise toiming kassas**, mis asub rakenduse Commerce peakontoris tööruumis **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="ee9b5-107">Pärast funktsiooni lubamist kaaluge kassas oma [kuvapaigutuste](pos-screen-layouts.md) värskendamist, et kasutada ära mõningaid muudetud võimalusi.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="ee9b5-108">Toimingu **Tellimuse tagasikutsumine** nupp võimaldab organisatsioonidel teha toimingut eelnevalt määratletud kuva kaudu.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Nupuruudustiku konfiguratsioon](media/recallorderbuttongrid.png)

<span data-ttu-id="ee9b5-110">Kuvasuvandid on järgmised.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-110">The display options are as follows.</span></span>
- <span data-ttu-id="ee9b5-111">**Puudub** – see suvand käivitab toimingu ilma kindla kuvata.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="ee9b5-112">Kui kasutaja avab toimingu selle konfiguratsiooniga, palutakse neil tellimusi otsida ja leida või valida eelnevalt määratud tellimuse filtri seast.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="ee9b5-113">**Täidetavad tellimused** – kui kasutaja käivitab toimingu, käivitub päring automaatselt, et otsida üles ja kuvada loend tellimustest, mille kauplus peab täitma.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the user's current store.</span></span> <span data-ttu-id="ee9b5-114">Need tellimused on konfigureeritud kaupluses pealevõtmiseks või kauplusest lähetamiseks ning nende tellimuste ridu pole veel peale võetud ega pakitud.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="ee9b5-115">**Pealevõetavad tellimused** – kui kasutaja käivitab toimingu, käivitub päring automaatselt, et otsida üles ja kuvada loend tellimustest, mis on konfigureeritud kaupluses pealevõtmiseks kasutaja praeguses kaupluses.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="ee9b5-116">**Lähetatavad tellimused** – kui kasutaja käivitab toimingu, käivitub päring automaatselt, et otsida üles ja kuvada loend tellimustest, mis on konfigureeritud lähetamiseks kasutaja praegusest kauplusest.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="ee9b5-117">Kui kassas käivitatakse toiming **Tellimuse tagasikutsumine** ja kuva väärtuseks on konfigureeritud **Puudub**, saab kasutaja tellimusi otsida ja leida ühel järgmistest viisidest.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="ee9b5-118">Skannige tellimuse vöötkoodid.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-118">Scan order barcodes.</span></span> <span data-ttu-id="ee9b5-119">See otsib vasteid tellimuse numbri, kanali viite ja sissetuleku ID väljadelt.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="ee9b5-120">Valige rakenduseribalt ikoon **Otsi tellimusi** või **Otsi ja filtreeri**, et kasutada kriteeriumidele vastavate tellimuste leidmiseks filtreerimist.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="ee9b5-121">Valige eelmääratletud filtri kaudu rippmenüüst **Kuva tellimused** (täidetavad tellimused, pealevõetavad tellimused või lähetatavad tellimused).</span><span class="sxs-lookup"><span data-stu-id="ee9b5-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="ee9b5-123">Pärast otsingukriteeriumide rakendamist kuvatakse rakenduses ühtivate müügitellimuste loend.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span> <span data-ttu-id="ee9b5-124">Otsingu-/filtrisuvandite kasutamisel ei pea toodud tellimused olema kasutaja praeguse kauplusega lingitud tellimused.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-124">It's important to note that when using the search/filter options, the orders retrieved do not have to be orders linked to the user's current store.</span></span> <span data-ttu-id="ee9b5-125">See otsinguprotsess toob ja kuvab kõik otsingukriteeriumitele vastavad klienditellimused, isegi kui tellimus on loodud või seatud täidetuks teise kaupluse/kanali või lao asukoha poolt.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-125">This search process will retrieve and display any customer order that matches the search criteria, even if the order was created or set to be fulfilled by another store/channel or warehouse location.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="ee9b5-127">Kasutaja saab valida loendist tellimuse, et vaadata täiendavaid üksikasju.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-127">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="ee9b5-128">Ekraani paremas servas oleval teabepaanil kuvatakse valitud tellimuse üksikasjad, sh tellimuse rea üksikasjad, tarne üksikasjad ja täitmise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-128">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="ee9b5-129">Rakendusepaanilt saab kasutaja valida toimingu.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-129">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="ee9b5-130">Sõltuvalt tellimuse olekust ei pruugi kindlad toimingud lubatud olla.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-130">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="ee9b5-131">**Tagastus** – käivitab valitud klienditellimusel arveldatud toodete tagastuse loomise protsessi.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-131">**Return** – Initiates the process of creating a return for any of the invoiced products on the selected customer order.</span></span>

- <span data-ttu-id="ee9b5-132">**Tühista** – tühistab valitud müügitellimuse täielikult.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-132">**Cancel** – Issue a full cancellation of the selected sales order.</span></span> <span data-ttu-id="ee9b5-133">See valik pole kõnekeskuse kanali kaudu algatatud tellimuste puhul saadaval ja seda ei saa kasutada tellimuse osaliseks tühistamiseks.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-133">This option will not be available for orders initiated through a call center channel and cannot be used to partially cancel an order.</span></span>

- <span data-ttu-id="ee9b5-134">**Täida** – viib kasutaja tellimuse täitmise lehele, mis on valitud tellimuse jaoks eelfiltreeritud.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-134">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="ee9b5-135">Kuvatakse ainult tellimuse read, mida saab valitud tellimuse puhul kasutaja kaupluses täita.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-135">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="ee9b5-136">**Redigeeri** – lubab kasutajatel valitud klienditellimust muuta.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-136">**Edit** – Allows users to make changes to the selected customer order.</span></span> <span data-ttu-id="ee9b5-137">Tellimusi saab redigeerida ainult [teatud stsenaariumide puhul](customer-orders-overview.md#edit-an-existing-customer-order).</span><span class="sxs-lookup"><span data-stu-id="ee9b5-137">Orders are only editable in [certain scenarios](customer-orders-overview.md#edit-an-existing-customer-order).</span></span>

- <span data-ttu-id="ee9b5-138">**Pealeregistreerimine** – see suvand on saadaval, kui tellimusel on üks või mitu rida määratud kasutaja praegusesse kauplusesse järele.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-138">**Pick up** – This option will be available if the order has one or more lines designated for pickup at the user's current store.</span></span> <span data-ttu-id="ee9b5-139">Pealevõtmine – käivitab pealevõtmise voo, mis võimaldab kasutajal valida peale võtavad tooted ning loob pealevõtmise müügitehingu.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-139">This operation launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>

## <a name="add-notifications-to-the-recall-order-operation"></a><span data-ttu-id="ee9b5-140">Lisage teatised tagasikutsumistellimuse toimingusse</span><span class="sxs-lookup"><span data-stu-id="ee9b5-140">Add notifications to the recall order operation</span></span>

<span data-ttu-id="ee9b5-141">Versioonis 10.0.18 ja uuemates versioonides saate konfigureerida müügikoha teatised ja reaalajas paani teatised **tellimuse tagasikutsumise** toimingu jaoks, kui soovite.</span><span class="sxs-lookup"><span data-stu-id="ee9b5-141">In version 10.0.18 and later, you can configure POS notifications and live tile alerts for the **Order Recall** operation if desired.</span></span> <span data-ttu-id="ee9b5-142">Lisateavet vt [müügikohas tellimuse teatiste näitamiseks](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="ee9b5-142">For more information, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
