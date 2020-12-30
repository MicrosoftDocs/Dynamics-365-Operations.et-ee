---
title: Tellimuse tagasikutsumise toiming kassas
description: Selles teemas selgitatakse funktsioonivõimalusi, mis on saadaval kassas täiustatud tellimuse tagasikutsumise lehtedel.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 42b11ff16757d633b868dfdf248341193a44378f
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665294"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="830aa-103">Tellimuse tagasikutsumise toiming kassas</span><span class="sxs-lookup"><span data-stu-id="830aa-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="830aa-104">**Tellimuse tagasikutsumise** toiming rakenduse Commerce kassas (POS) pakub värskendatud tellimuste otsimise ja filtreerimise funktsioone ning tellimusespetsiifilist teavet.</span><span class="sxs-lookup"><span data-stu-id="830aa-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="830aa-105">See funktsioon on saadaval rakenduse Commerce versioonis 10.0.15 ja uuemates.</span><span class="sxs-lookup"><span data-stu-id="830aa-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="830aa-106">Selle funktsiooni lubamiseks lülitage sisse funktsioon **Täiustatud tellimuse tagasikutsumise toiming kassas**, mis asub rakenduse Commerce peakontoris tööruumis **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="830aa-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="830aa-107">Pärast funktsiooni lubamist kaaluge kassas oma [kuvapaigutuste](pos-screen-layouts.md) värskendamist, et kasutada ära mõningaid muudetud võimalusi.</span><span class="sxs-lookup"><span data-stu-id="830aa-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="830aa-108">Toimingu **Tellimuse tagasikutsumine** nupp võimaldab organisatsioonidel teha toimingut eelnevalt määratletud kuva kaudu.</span><span class="sxs-lookup"><span data-stu-id="830aa-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Nupuruudustiku konfiguratsioon](media/recallorderbuttongrid.png)

<span data-ttu-id="830aa-110">Kuvasuvandid on järgmised.</span><span class="sxs-lookup"><span data-stu-id="830aa-110">The display options are as follows.</span></span>
- <span data-ttu-id="830aa-111">**Puudub** – see suvand käivitab toimingu ilma kindla kuvata.</span><span class="sxs-lookup"><span data-stu-id="830aa-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="830aa-112">Kui kasutaja avab toimingu selle konfiguratsiooniga, palutakse neil tellimusi otsida ja leida või valida eelnevalt määratud tellimuse filtri seast.</span><span class="sxs-lookup"><span data-stu-id="830aa-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="830aa-113">**Täidetavad tellimused** – kui kasutaja käivitab toimingu, käivitub päring automaatselt, et otsida üles ja kuvada loend tellimustest, mille kauplus peab täitma.</span><span class="sxs-lookup"><span data-stu-id="830aa-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="830aa-114">Need tellimused on konfigureeritud kaupluses pealevõtmiseks või kauplusest lähetamiseks ning nende tellimuste ridu pole veel peale võetud ega pakitud.</span><span class="sxs-lookup"><span data-stu-id="830aa-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="830aa-115">**Pealevõetavad tellimused** – kui kasutaja käivitab toimingu, käivitub päring automaatselt, et otsida üles ja kuvada loend tellimustest, mis on konfigureeritud kaupluses pealevõtmiseks kasutaja praeguses kaupluses.</span><span class="sxs-lookup"><span data-stu-id="830aa-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="830aa-116">**Lähetatavad tellimused** – kui kasutaja käivitab toimingu, käivitub päring automaatselt, et otsida üles ja kuvada loend tellimustest, mis on konfigureeritud lähetamiseks kasutaja praegusest kauplusest.</span><span class="sxs-lookup"><span data-stu-id="830aa-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="830aa-117">Kui kassas käivitatakse toiming **Tellimuse tagasikutsumine** ja kuva väärtuseks on konfigureeritud **Puudub**, saab kasutaja tellimusi otsida ja leida ühel järgmistest viisidest.</span><span class="sxs-lookup"><span data-stu-id="830aa-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="830aa-118">Skannige tellimuse vöötkoodid.</span><span class="sxs-lookup"><span data-stu-id="830aa-118">Scan order barcodes.</span></span> <span data-ttu-id="830aa-119">See otsib vasteid tellimuse numbri, kanali viite ja sissetuleku ID väljadelt.</span><span class="sxs-lookup"><span data-stu-id="830aa-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="830aa-120">Valige rakenduseribalt ikoon **Otsi tellimusi** või **Otsi ja filtreeri**, et kasutada kriteeriumidele vastavate tellimuste leidmiseks filtreerimist.</span><span class="sxs-lookup"><span data-stu-id="830aa-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="830aa-121">Valige eelmääratletud filtri kaudu rippmenüüst **Kuva tellimused** (täidetavad tellimused, pealevõetavad tellimused või lähetatavad tellimused).</span><span class="sxs-lookup"><span data-stu-id="830aa-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="830aa-123">Pärast otsingukriteeriumide rakendamist kuvatakse rakenduses ühtivate müügitellimuste loend.</span><span class="sxs-lookup"><span data-stu-id="830aa-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="830aa-125">Kasutaja saab valida loendist tellimuse, et vaadata täiendavaid üksikasju.</span><span class="sxs-lookup"><span data-stu-id="830aa-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="830aa-126">Ekraani paremas servas oleval teabepaanil kuvatakse valitud tellimuse üksikasjad, sh tellimuse rea üksikasjad, tarne üksikasjad ja täitmise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="830aa-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="830aa-127">Rakendusepaanilt saab kasutaja valida toimingu.</span><span class="sxs-lookup"><span data-stu-id="830aa-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="830aa-128">Sõltuvalt tellimuse olekust ei pruugi kindlad toimingud lubatud olla.</span><span class="sxs-lookup"><span data-stu-id="830aa-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="830aa-129">**Tagasta** – käivitab valitud klienditellimusega seotud ühe või mitme arve tagastamise.</span><span class="sxs-lookup"><span data-stu-id="830aa-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="830aa-130">**Tühista** – tühistab valitud müügitellimuse täielikult.</span><span class="sxs-lookup"><span data-stu-id="830aa-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="830aa-131">**Täida** – viib kasutaja tellimuse täitmise lehele, mis on valitud tellimuse jaoks eelfiltreeritud.</span><span class="sxs-lookup"><span data-stu-id="830aa-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="830aa-132">Kuvatakse ainult tellimuse read, mida saab valitud tellimuse puhul kasutaja kaupluses täita.</span><span class="sxs-lookup"><span data-stu-id="830aa-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="830aa-133">**Redigeeri** – lubab kasutajatel valitud klienditellimust muuta.</span><span class="sxs-lookup"><span data-stu-id="830aa-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="830aa-134">**Pealevõtmine** – käivitab pealevõtmise voo, mis võimaldab kasutajal valida peale võtavad tooted ning loob pealevõtmise müügitehingu.</span><span class="sxs-lookup"><span data-stu-id="830aa-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>
