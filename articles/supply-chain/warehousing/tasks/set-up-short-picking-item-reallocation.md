--- 
title: "Kiirelt komplekteeritava kauba ümberjaotamise seadistamine"
description: "See protseduur näitab, kuidas lubada laotöötajatel kiiresti alternatiivseid asukohti leida, kui selles asukohas, kuhu nad suunati, pole piisavalt varusid."
author: YuyuScheller
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 593b4ddb1442d77fd8a29e9d9b161936505f1fb3
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="7cb0d-103">Kiirelt komplekteeritava kauba ümberjaotamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="7cb0d-103">Set up short picking item reallocation</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7cb0d-104">See protseduur näitab, kuidas lubada laotöötajatel kiiresti alternatiivseid asukohti leida, kui selles asukohas, kuhu nad suunati, pole piisavalt varusid.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> <span data-ttu-id="7cb0d-105">Võimalik on kasutada automaatset ümberjaotamise protsessi, mis kasutab kaupade toomiseks asukohakorraldusi, kui need on teises asukohas olemas.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-105">It’s possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they’re available at another location.</span></span> <span data-ttu-id="7cb0d-106">Teise võimalusena näidatakse käsitsi ümberjaotamise kasutamisel mobiilsel seadmel loendit saadaoleva kogusega asukohtadest, mis võimaldab laotöötajal valida, millise asukoha varusid kasutada.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="7cb0d-107">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="7cb0d-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="7cb0d-109">Tööerandite häälestamine</span><span class="sxs-lookup"><span data-stu-id="7cb0d-109">Set up work exceptions</span></span>
1. <span data-ttu-id="7cb0d-110">Avage Laohaldus > Seadistus > Töö > Tööerandid.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-110">Go to Warehouse management > Setup > Work > Work exceptions.</span></span>
2. <span data-ttu-id="7cb0d-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-111">Click New.</span></span>
    * <span data-ttu-id="7cb0d-112">Määratleda saab mitu tööerandit erinevate kauba ümberjaotamise poliitikatega, et laotöötaja saaks valida neist ühe töödeldava saadetise vajaduste põhjal.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-112">It’s possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="7cb0d-113">Tippige väärtus väljale Tööerandi kood.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-113">In the Work exception code field, type a value.</span></span>
    * <span data-ttu-id="7cb0d-114">Andke tööerandile pealkiri, mis näitaks, milleks seda kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-114">Give the work exception a title to indicate what it’s used for.</span></span> <span data-ttu-id="7cb0d-115">Näiteks Puuduva käsitsi valimine.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="7cb0d-116">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-116">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7cb0d-117">Tehke väljal Erandi tüüp valik Puuduva valimine.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-117">In the Exception type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="7cb0d-118">Märkige ruut Varude korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-118">Select the Adjust inventory check box.</span></span>
    * <span data-ttu-id="7cb0d-119">See valik tähendab, et varud reguleeritakse puuduva valimise asukohas automaatselt väärtusele 0.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="7cb0d-120">Valige või sisestage väärtus väljal Vaikimisi korrigeerimistüübi kood.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-120">In the Default adjustment type code field, enter or select a value.</span></span>
    * <span data-ttu-id="7cb0d-121">Näiteks ettevõtte USMF puhul võite teha valiku Remove Res Adj Out.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="7cb0d-122">Tehke väljal Kauba ümberjaotamine valik Käsitsi.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-122">In the Item reallocation field, select 'Manual'.</span></span>
    * <span data-ttu-id="7cb0d-123">Kui teete valiku Käsitsi või Automaatne ja Käsitsi, peab laotöötajale olema antud võimalus kasutada käsitsi ümberjaotamist.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="7cb0d-124">Töötaja seadistamine käsitsi kauba ümberjaotamist kasutama</span><span class="sxs-lookup"><span data-stu-id="7cb0d-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="7cb0d-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-125">Close the page.</span></span>
2. <span data-ttu-id="7cb0d-126">Avage Laohaldus > Seadistus > Töötaja.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-126">Go to Warehouse management > Setup > Worker.</span></span>
3. <span data-ttu-id="7cb0d-127">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-127">Click Edit.</span></span>
4. <span data-ttu-id="7cb0d-128">Valige loendist töötaja 24.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="7cb0d-129">Laiendage jaotist Töö.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-129">Expand the Work section.</span></span>
6. <span data-ttu-id="7cb0d-130">Tehke väljal Luba käsitsi kauba ümberjaotamine valik Jah.</span><span class="sxs-lookup"><span data-stu-id="7cb0d-130">Select Yes in the Allow manual item reallocation field.</span></span>


