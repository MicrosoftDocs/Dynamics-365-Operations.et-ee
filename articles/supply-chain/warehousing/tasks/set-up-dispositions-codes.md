---
title: Likvideerimiskoodide seadistamine
description: See protseduur keskendub likvideerimiaskoosdi loomisele, mida saab kasutada mobiilses seadmes tagastustellimuse vastuvõtmisprotsessi puhul.
author: ShylaThompson
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16458f709788e538d036cc4d3b3239f4ffa3c42e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830925"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="de389-103">Likvideerimiskoodide seadistamine</span><span class="sxs-lookup"><span data-stu-id="de389-103">Set up dispositions codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de389-104">See protseduur keskendub likvideerimiaskoosdi loomisele, mida saab kasutada mobiilses seadmes tagastustellimuse vastuvõtmisprotsessi puhul.</span><span class="sxs-lookup"><span data-stu-id="de389-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="de389-105">Likvideerimiskoodid on kogumik reegleid, mida saab kasutada kaupade vastuvõtmisel.</span><span class="sxs-lookup"><span data-stu-id="de389-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="de389-106">Näiteks kui töö kasutaja kasutab kahjustatud kaupade vastuvõtmiseks mobiilset seadet, peab ta skannima kahjustatud kaupade likvideerimiskoodi.</span><span class="sxs-lookup"><span data-stu-id="de389-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="de389-107">Vastuvõetud kaupade varude oleku, töömalli ja asukohakorralduse saab määratleda skannitud likvideerimiskoodi alusel.</span><span class="sxs-lookup"><span data-stu-id="de389-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="de389-108">Ostutellimuse vastuvõtmisprotsessi ja tootmisetellimuse lõpetatuna teatamisel on likvideerimiskoodi kasutamine valikuline.</span><span class="sxs-lookup"><span data-stu-id="de389-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="de389-109">Kui müügitellimuse tagastuse vastuvõtmisprotsessi puhul registreeritakse kaubad mobiilse seadme abil, on likvideerimiskoodi kasutamine kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="de389-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="de389-110">Selle juhendi loomisel kasutati demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="de389-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="de389-111">See protseduur on mõeldud laohaldurile.</span><span class="sxs-lookup"><span data-stu-id="de389-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="de389-112">Tehke valik Laohaldus > Seadistus > Mobiilne seade > Likvideerimiskoodid.</span><span class="sxs-lookup"><span data-stu-id="de389-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="de389-113">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="de389-113">Click New.</span></span>
    * <span data-ttu-id="de389-114">Saate luua kliendi tagastuste puhul kasutamiseks uue likvideerimiskoodi.</span><span class="sxs-lookup"><span data-stu-id="de389-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="de389-115">Sisestage väärtus väljale Likvideerimiskood.</span><span class="sxs-lookup"><span data-stu-id="de389-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="de389-116">Valige väljal Varude olek see varude olek, kus esineb varude blokeerimine.</span><span class="sxs-lookup"><span data-stu-id="de389-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="de389-117">USMF-i kasutamisel valige suvand Blokeerimine.</span><span class="sxs-lookup"><span data-stu-id="de389-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="de389-118">Saate lisada varude olekule likvideerimiskoodi, et tühistada selle vaikeolek tellimuseridadel.</span><span class="sxs-lookup"><span data-stu-id="de389-118">You can add an inventory status to the disposition code to override the default status that's on the order lines.</span></span>  
5. <span data-ttu-id="de389-119">Sisestage väärtus väljale Töömall.</span><span class="sxs-lookup"><span data-stu-id="de389-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="de389-120">Valikuline: saate valida tagastustellimusega seostatud töömalli koodi.</span><span class="sxs-lookup"><span data-stu-id="de389-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="de389-121">Kui ühtegi väärtust pole esitatud, lahendatakse töömall teie süsteemis konfigureeritud standardreeglitega.</span><span class="sxs-lookup"><span data-stu-id="de389-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="de389-122">Töömalli valimine piirab protsesse, millega seda likvideerimiskoodi saab kasutada.</span><span class="sxs-lookup"><span data-stu-id="de389-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="de389-123">Näiteks kui likvideerimiskoodil on töömall, mille töötellimuse olek on Ostutellimus, ei saa seda kasutada klientide tagastatud kaupade registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="de389-123">For example, if a disposition code has a work template with a work order of type purchase order, it can't be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="de389-124">Sisestage väärtus väljale Tagastamise likvideerimiskood.</span><span class="sxs-lookup"><span data-stu-id="de389-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="de389-125">Tagastuse likvideerimiskood määratleb ülejäänud tagastustellimuse protsessi registreeritud kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="de389-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="de389-126">Selles näites peaks klient saama kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="de389-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="de389-127">Lisage tagastuste likvideerimiskood, mis sisaldab tegevust Kreedit.</span><span class="sxs-lookup"><span data-stu-id="de389-127">Add a returns disposition code that contains an action Credit.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]