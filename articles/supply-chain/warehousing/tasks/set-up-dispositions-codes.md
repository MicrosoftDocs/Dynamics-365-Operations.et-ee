---
title: Likvideerimiskoodide seadistamine
description: See protseduur keskendub likvideerimiaskoosdi loomisele, mida saab kasutada mobiilses seadmes tagastustellimuse vastuvõtmisprotsessi puhul.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d84699e8e4323792ac67b69236d264e33eeaf28
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017035"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="d8396-103">Likvideerimiskoodide seadistamine</span><span class="sxs-lookup"><span data-stu-id="d8396-103">Set up dispositions codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8396-104">See protseduur keskendub likvideerimiaskoosdi loomisele, mida saab kasutada mobiilses seadmes tagastustellimuse vastuvõtmisprotsessi puhul.</span><span class="sxs-lookup"><span data-stu-id="d8396-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="d8396-105">Likvideerimiskoodid on kogumik reegleid, mida saab kasutada kaupade vastuvõtmisel.</span><span class="sxs-lookup"><span data-stu-id="d8396-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="d8396-106">Näiteks kui töö kasutaja kasutab kahjustatud kaupade vastuvõtmiseks mobiilset seadet, peab ta skannima kahjustatud kaupade likvideerimiskoodi.</span><span class="sxs-lookup"><span data-stu-id="d8396-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="d8396-107">Vastuvõetud kaupade varude oleku, töömalli ja asukohakorralduse saab määratleda skannitud likvideerimiskoodi alusel.</span><span class="sxs-lookup"><span data-stu-id="d8396-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="d8396-108">Ostutellimuse vastuvõtmisprotsessi ja tootmisetellimuse lõpetatuna teatamisel on likvideerimiskoodi kasutamine valikuline.</span><span class="sxs-lookup"><span data-stu-id="d8396-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="d8396-109">Kui müügitellimuse tagastuse vastuvõtmisprotsessi puhul registreeritakse kaubad mobiilse seadme abil, on likvideerimiskoodi kasutamine kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="d8396-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="d8396-110">Selle juhendi loomisel kasutati demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="d8396-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="d8396-111">See protseduur on mõeldud laohaldurile.</span><span class="sxs-lookup"><span data-stu-id="d8396-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="d8396-112">Tehke valik Laohaldus > Seadistus > Mobiilne seade > Likvideerimiskoodid.</span><span class="sxs-lookup"><span data-stu-id="d8396-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="d8396-113">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d8396-113">Click New.</span></span>
    * <span data-ttu-id="d8396-114">Saate luua kliendi tagastuste puhul kasutamiseks uue likvideerimiskoodi.</span><span class="sxs-lookup"><span data-stu-id="d8396-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="d8396-115">Sisestage väärtus väljale Likvideerimiskood.</span><span class="sxs-lookup"><span data-stu-id="d8396-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="d8396-116">Valige väljal Varude olek see varude olek, kus esineb varude blokeerimine.</span><span class="sxs-lookup"><span data-stu-id="d8396-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="d8396-117">USMF-i kasutamisel valige suvand Blokeerimine.</span><span class="sxs-lookup"><span data-stu-id="d8396-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="d8396-118">Saate lisada varude olekule likvideerimiskoodi, et tühistada selle vaikeolek tellimuseridadel.</span><span class="sxs-lookup"><span data-stu-id="d8396-118">You can add an inventory status to the disposition code to override the default status that's on the order lines.</span></span>  
5. <span data-ttu-id="d8396-119">Sisestage väärtus väljale Töömall.</span><span class="sxs-lookup"><span data-stu-id="d8396-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="d8396-120">Valikuline: saate valida tagastustellimusega seostatud töömalli koodi.</span><span class="sxs-lookup"><span data-stu-id="d8396-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="d8396-121">Kui ühtegi väärtust pole esitatud, lahendatakse töömall teie süsteemis konfigureeritud standardreeglitega.</span><span class="sxs-lookup"><span data-stu-id="d8396-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="d8396-122">Töömalli valimine piirab protsesse, millega seda likvideerimiskoodi saab kasutada.</span><span class="sxs-lookup"><span data-stu-id="d8396-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="d8396-123">Näiteks kui likvideerimiskoodil on töömall, mille töötellimuse olek on Ostutellimus, ei saa seda kasutada klientide tagastatud kaupade registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="d8396-123">For example, if a disposition code has a work template with a work order of type purchase order, it can't be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="d8396-124">Sisestage väärtus väljale Tagastamise likvideerimiskood.</span><span class="sxs-lookup"><span data-stu-id="d8396-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="d8396-125">Tagastuse likvideerimiskood määratleb ülejäänud tagastustellimuse protsessi registreeritud kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="d8396-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="d8396-126">Selles näites peaks klient saama kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="d8396-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="d8396-127">Lisage tagastuste likvideerimiskood, mis sisaldab tegevust Kreedit.</span><span class="sxs-lookup"><span data-stu-id="d8396-127">Add a returns disposition code that contains an action Credit.</span></span>  

