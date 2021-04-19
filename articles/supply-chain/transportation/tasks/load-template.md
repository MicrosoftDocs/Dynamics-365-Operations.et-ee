---
title: Koorma mallid
description: Teemas kirjeldatakse koormamallide häälestamist ja koormamalli seostamist uue koormaga.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 175c8017b14cc298cdaa00031f8450015a747786
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831502"
---
# <a name="load-templates"></a><span data-ttu-id="70669-103">Koorma mallid</span><span class="sxs-lookup"><span data-stu-id="70669-103">Load templates</span></span>

<span data-ttu-id="70669-104">Uue koorma loomisel saate määrata koormamalli.</span><span class="sxs-lookup"><span data-stu-id="70669-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="70669-105">Koorma mallis on teave seadmete ja selliste mõõtmete kohta nagu koorma kõrgus, laius, sügavus ja maht.</span><span class="sxs-lookup"><span data-stu-id="70669-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="70669-106">Teemas kirjeldatakse koormamallide häälestamist ja koormamalli seostamist uue koormaga.</span><span class="sxs-lookup"><span data-stu-id="70669-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="70669-107">Koormamalli häälestamine</span><span class="sxs-lookup"><span data-stu-id="70669-107">Set up a load template</span></span>

1. <span data-ttu-id="70669-108">Valige **Transpordihaldus \> Häälestus \> Koorma koostamine \> Koormamall**.</span><span class="sxs-lookup"><span data-stu-id="70669-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="70669-109">Uue malli lisamiseks valige toimingupaanil nupp **Uus** või valige nupp **Redigeerimi**, et redigeerida olemasolevat malli.</span><span class="sxs-lookup"><span data-stu-id="70669-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="70669-110">Määrake uue või olemasoleva malli real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="70669-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="70669-111">**Koormamalli ID** – sisestage koormamalli jaoks kordumatu identifikaator (ID).</span><span class="sxs-lookup"><span data-stu-id="70669-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="70669-112">**Seadmed** – valige seadmed, mida tuleks kasutada koorma saatmiseks.</span><span class="sxs-lookup"><span data-stu-id="70669-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="70669-113">**Koorma kõrgus**, **koorma laius** ja **Koorma sügavus** – sisestage koorma mõõtmed.</span><span class="sxs-lookup"><span data-stu-id="70669-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="70669-114">**Koorma max lubatud maht** ja **Koorma max lubatud kaal** – sisestage koorma suurim lubatud maht ja kaal.</span><span class="sxs-lookup"><span data-stu-id="70669-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="70669-115">**Maksimaalne lubatud brutokaal** – sisestage koorma suurim lubatud brutokaal.</span><span class="sxs-lookup"><span data-stu-id="70669-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="70669-116">Koorma brutokaal hõlmab nii omakaalu kui ka koormakaalu.</span><span class="sxs-lookup"><span data-stu-id="70669-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="70669-117">**Koorma maksimaalne lubatud veokoguste arv** – sisestage maksimaalne arv veokoguseid, mida koorem võib sisaldada.</span><span class="sxs-lookup"><span data-stu-id="70669-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="70669-118">**Koorma laadimine põramdale virna** – valige see märkeruut, et kasutada koorma põrandale laadimist.</span><span class="sxs-lookup"><span data-stu-id="70669-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="70669-119">Põranda laadimise stsenaariumi puhul virnastatakse kastid põrandast laeni ja seinast seinani, et konteineri mahtu parimal moel ära kasutada.</span><span class="sxs-lookup"><span data-stu-id="70669-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="70669-120">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="70669-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="70669-121">Koormamalli seostamine uue koormaga</span><span class="sxs-lookup"><span data-stu-id="70669-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="70669-122">**Avage Transpordihaldus \> Plaanimine \> Koorma plaanimise töölaud.**</span><span class="sxs-lookup"><span data-stu-id="70669-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="70669-123">Valige lehe ülemises osas üks järgmistest vahekaartidest, sõltuvalt sellest, millist tüüpi lähtedokumendi puhul koormust luuakse: **Saadetised**, **Müügiread**, **Üleviimistellimuse read** või **Ostutellimuse read**.</span><span class="sxs-lookup"><span data-stu-id="70669-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="70669-124">Valige kindel dokument, mille jaoks koormat planeerida.</span><span class="sxs-lookup"><span data-stu-id="70669-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="70669-125">Valige toimingupaani vahekaardi **Pakkumine ja nõudlus** grupis **Lisa** suvand **Uuele koormusele**.</span><span class="sxs-lookup"><span data-stu-id="70669-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="70669-126">Valige dialoogiboksi **Koormamall** väljal **Koormamalli ID** rakendatav mall.</span><span class="sxs-lookup"><span data-stu-id="70669-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="70669-127">Malli rakendamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="70669-127">Select **OK** to apply the template.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]