--- 
title: "Toodete ristlaadimine vastuvõtvast laost kauplustesse"
description: "See protseduur tutvustab, kuidas luua ja töödelda ristplatvormi toodete laialisaatmiseks ostutellimuse vastuvõtukohast ühte või mitmesse kauplusesse."
author: BibiSp
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: daa42bb83d6b988e8fd18db6ad8386c67fd3e6e5
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="bdbf0-103">Toodete ristlaadimine vastuvõtvast laost kauplustesse</span><span class="sxs-lookup"><span data-stu-id="bdbf0-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bdbf0-104">See protseduur tutvustab, kuidas luua ja töödelda ristplatvormi toodete laialisaatmiseks ostutellimuse vastuvõtukohast ühte või mitmesse kauplusesse.</span><span class="sxs-lookup"><span data-stu-id="bdbf0-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="bdbf0-105">Kasutaja saab määrata mitu konfiguratsiooni ja lasta süsteemil soovitada, kuidas tooted laiali saata, või käsitsi sisestada, kuhu tooted saadetakse ja kui suure koguse iga kauplus saab.</span><span class="sxs-lookup"><span data-stu-id="bdbf0-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="bdbf0-106">See protseduur ei sisalda andmete seadistust, mida saab kasutada ristplatvormil, näiteks täiendamise reegleid, organisatsiooni hierarhiaid ega kauplusekaale.</span><span class="sxs-lookup"><span data-stu-id="bdbf0-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="bdbf0-107">See protseduur kasutab USRT-demofirmat.</span><span class="sxs-lookup"><span data-stu-id="bdbf0-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="bdbf0-108">Avage valik Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="bdbf0-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="bdbf0-109">Valige loendist ostutellimus ja klõpsake tellimuse avamiseks lingil.</span><span class="sxs-lookup"><span data-stu-id="bdbf0-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="bdbf0-110">Klõpsake tegevuspaneelil valikut Retail (Jaemüük).</span><span class="sxs-lookup"><span data-stu-id="bdbf0-110">On the Action Pane, click Retail.</span></span>
4. <span data-ttu-id="bdbf0-111">Klõpsake valikut Cross docking (Ristlaadimine).</span><span class="sxs-lookup"><span data-stu-id="bdbf0-111">Click Cross docking.</span></span>
5. <span data-ttu-id="bdbf0-112">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="bdbf0-112">Click Edit.</span></span>
    * <span data-ttu-id="bdbf0-113">Kategooriat saab kasutada kirjete filtreerimiseks jaotises Lines (Read).</span><span class="sxs-lookup"><span data-stu-id="bdbf0-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="bdbf0-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bdbf0-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="bdbf0-115">Sisestage väljale Cross docking quantity (Ristlaadimise kogus) väärtus, et täpsustada, kui suur osa valitud toote kodusest tuleks laiali saata.</span><span class="sxs-lookup"><span data-stu-id="bdbf0-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="bdbf0-116">Sisestage väljale Additional cross docking quantity (Lisa-ristlaadimise kogus) väärtus laialisaatmiskoguste määramiseks saadaolevatele ostetavatele toodetele</span><span class="sxs-lookup"><span data-stu-id="bdbf0-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="bdbf0-117">Sisestage väljale Distribution (Jaotus) asukoha kaal.</span><span class="sxs-lookup"><span data-stu-id="bdbf0-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="bdbf0-118">Saate teisi tüüpe valida jaotise jaoks teistsuguste reeglite kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="bdbf0-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="bdbf0-119">Sisestage väljale Täiendamise hierarhia väärtus.</span><span class="sxs-lookup"><span data-stu-id="bdbf0-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="bdbf0-120">Valige Jah väljal Respect assortments (Sortimendi tunnustamine).</span><span class="sxs-lookup"><span data-stu-id="bdbf0-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="bdbf0-121">Klõpsake valikut Arvuta kogused.</span><span class="sxs-lookup"><span data-stu-id="bdbf0-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="bdbf0-122">Klõpsake valikut Create order (Loo tellimus).</span><span class="sxs-lookup"><span data-stu-id="bdbf0-122">Click Create order.</span></span>
14. <span data-ttu-id="bdbf0-123">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="bdbf0-123">Click Yes.</span></span>
15. <span data-ttu-id="bdbf0-124">Leidke loendist ladu, mis tooted vastu võttis ja valige see</span><span class="sxs-lookup"><span data-stu-id="bdbf0-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="bdbf0-125">Klõpsake valitud lao jaoks loodud tellimuste vaatamiseks valikut Order (Tellimus)</span><span class="sxs-lookup"><span data-stu-id="bdbf0-125">Click Order to view the orders that got created for the selected warehouse</span></span>


