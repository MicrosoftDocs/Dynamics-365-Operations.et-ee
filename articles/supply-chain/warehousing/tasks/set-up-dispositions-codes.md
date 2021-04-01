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
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8eeba07aafbcbc327aa5e28a10d10c16b0e0f43
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236538"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="c798c-103">Likvideerimiskoodide seadistamine</span><span class="sxs-lookup"><span data-stu-id="c798c-103">Set up dispositions codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c798c-104">See protseduur keskendub likvideerimiaskoosdi loomisele, mida saab kasutada mobiilses seadmes tagastustellimuse vastuvõtmisprotsessi puhul.</span><span class="sxs-lookup"><span data-stu-id="c798c-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="c798c-105">Likvideerimiskoodid on kogumik reegleid, mida saab kasutada kaupade vastuvõtmisel.</span><span class="sxs-lookup"><span data-stu-id="c798c-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="c798c-106">Näiteks kui töö kasutaja kasutab kahjustatud kaupade vastuvõtmiseks mobiilset seadet, peab ta skannima kahjustatud kaupade likvideerimiskoodi.</span><span class="sxs-lookup"><span data-stu-id="c798c-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="c798c-107">Vastuvõetud kaupade varude oleku, töömalli ja asukohakorralduse saab määratleda skannitud likvideerimiskoodi alusel.</span><span class="sxs-lookup"><span data-stu-id="c798c-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="c798c-108">Ostutellimuse vastuvõtmisprotsessi ja tootmisetellimuse lõpetatuna teatamisel on likvideerimiskoodi kasutamine valikuline.</span><span class="sxs-lookup"><span data-stu-id="c798c-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="c798c-109">Kui müügitellimuse tagastuse vastuvõtmisprotsessi puhul registreeritakse kaubad mobiilse seadme abil, on likvideerimiskoodi kasutamine kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="c798c-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="c798c-110">Selle juhendi loomisel kasutati demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="c798c-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="c798c-111">See protseduur on mõeldud laohaldurile.</span><span class="sxs-lookup"><span data-stu-id="c798c-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="c798c-112">Tehke valik Laohaldus > Seadistus > Mobiilne seade > Likvideerimiskoodid.</span><span class="sxs-lookup"><span data-stu-id="c798c-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="c798c-113">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="c798c-113">Click New.</span></span>
    * <span data-ttu-id="c798c-114">Saate luua kliendi tagastuste puhul kasutamiseks uue likvideerimiskoodi.</span><span class="sxs-lookup"><span data-stu-id="c798c-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="c798c-115">Sisestage väärtus väljale Likvideerimiskood.</span><span class="sxs-lookup"><span data-stu-id="c798c-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="c798c-116">Valige väljal Varude olek see varude olek, kus esineb varude blokeerimine.</span><span class="sxs-lookup"><span data-stu-id="c798c-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="c798c-117">USMF-i kasutamisel valige suvand Blokeerimine.</span><span class="sxs-lookup"><span data-stu-id="c798c-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="c798c-118">Saate lisada varude olekule likvideerimiskoodi, et tühistada selle vaikeolek tellimuseridadel.</span><span class="sxs-lookup"><span data-stu-id="c798c-118">You can add an inventory status to the disposition code to override the default status that's on the order lines.</span></span>  
5. <span data-ttu-id="c798c-119">Sisestage väärtus väljale Töömall.</span><span class="sxs-lookup"><span data-stu-id="c798c-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="c798c-120">Valikuline: saate valida tagastustellimusega seostatud töömalli koodi.</span><span class="sxs-lookup"><span data-stu-id="c798c-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="c798c-121">Kui ühtegi väärtust pole esitatud, lahendatakse töömall teie süsteemis konfigureeritud standardreeglitega.</span><span class="sxs-lookup"><span data-stu-id="c798c-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="c798c-122">Töömalli valimine piirab protsesse, millega seda likvideerimiskoodi saab kasutada.</span><span class="sxs-lookup"><span data-stu-id="c798c-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="c798c-123">Näiteks kui likvideerimiskoodil on töömall, mille töötellimuse olek on Ostutellimus, ei saa seda kasutada klientide tagastatud kaupade registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="c798c-123">For example, if a disposition code has a work template with a work order of type purchase order, it can't be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="c798c-124">Sisestage väärtus väljale Tagastamise likvideerimiskood.</span><span class="sxs-lookup"><span data-stu-id="c798c-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="c798c-125">Tagastuse likvideerimiskood määratleb ülejäänud tagastustellimuse protsessi registreeritud kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="c798c-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="c798c-126">Selles näites peaks klient saama kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="c798c-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="c798c-127">Lisage tagastuste likvideerimiskood, mis sisaldab tegevust Kreedit.</span><span class="sxs-lookup"><span data-stu-id="c798c-127">Add a returns disposition code that contains an action Credit.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]