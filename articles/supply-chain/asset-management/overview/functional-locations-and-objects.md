---
title: Funktsionaalsed asukohad ja varad
description: Selles teemas kirjeldatakse funktsionaalseid asukohti ja varasid varahalduses. Varahaldus on täpsem moodul varade ja hooldustööde haldamiseks rakenduses Dynamics 365 Supply Chain Management.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5271b673d758608cae8e43d72b7e75b259d5f142
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024610"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="5529d-104">Funktsionaalsed asukohad ja varad</span><span class="sxs-lookup"><span data-stu-id="5529d-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="5529d-105">Selles teemas kirjeldatakse funktsionaalseid asukohti ja varasid varahalduses.</span><span class="sxs-lookup"><span data-stu-id="5529d-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="5529d-106">Varahaldus on täpsem moodul varade ja hooldustööde haldamiseks rakenduses Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5529d-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="5529d-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="5529d-107">Overview</span></span>

<span data-ttu-id="5529d-108">Varahaldus on integreeritud sujuvalt mitme mooduliga rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5529d-108">Asset Management is integrated seamlessly with several modules in Finance and Operations.</span></span> <span data-ttu-id="5529d-109">Järgmisel joonisel on kujutatud liidesed teiste moodulitega.</span><span class="sxs-lookup"><span data-stu-id="5529d-109">The following illustration shows the interfaces with other modules.</span></span>

![Joonis 1](media/01-overview-image.png)

<span data-ttu-id="5529d-111">Varahaldus võimaldab teil tõhusalt hallata ja sooritada kõiki ülesandeid, mis on seotud teie ettevõtte mitut tüüpi seadmete haldamise ja hooldamisega.</span><span class="sxs-lookup"><span data-stu-id="5529d-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="5529d-112">See varustus hõlmab masinaid, tootmisseadmeid ja sõidukeid.</span><span class="sxs-lookup"><span data-stu-id="5529d-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="5529d-113">Varahaldus toetab lahendusi paljudes tööstusharudes.</span><span class="sxs-lookup"><span data-stu-id="5529d-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="5529d-114">Järgmisel joonisel on ülevaade varahalduse põhifunktsioonidest.</span><span class="sxs-lookup"><span data-stu-id="5529d-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![Joonis 2](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="5529d-116">Funktsionaalsed asukohad ja varad</span><span class="sxs-lookup"><span data-stu-id="5529d-116">Functional locations and assets</span></span>

<span data-ttu-id="5529d-117">Funktsionaalseid asukohti kasutatakse varade haldamiseks asukohtades.</span><span class="sxs-lookup"><span data-stu-id="5529d-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="5529d-118">See haldus hõlmab varade kulude jälgimist funktsionaalsetes asukohtades.</span><span class="sxs-lookup"><span data-stu-id="5529d-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="5529d-119">Funktsionaalsed asukohad on struktureeritud hierarhiliselt ja asukohtadel võivad olla alamasukohad.</span><span class="sxs-lookup"><span data-stu-id="5529d-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="5529d-120">Funktsionaalsete asukohtade struktuur on staatiline.</span><span class="sxs-lookup"><span data-stu-id="5529d-120">The structure of functional locations is static.</span></span> <span data-ttu-id="5529d-121">Teisisõnu, asukohad ei saa muuta kohti.</span><span class="sxs-lookup"><span data-stu-id="5529d-121">In other words, locations can't change place.</span></span> <span data-ttu-id="5529d-122">Varasid saab paigaldada funktsionaalsetele asukohtadele ja vajaduse korral saab neid hiljem installida ka muudesse funktsionaalsetele asukohtadesse.</span><span class="sxs-lookup"><span data-stu-id="5529d-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="5529d-123">Varakulud järgivad alati vara asukohta.</span><span class="sxs-lookup"><span data-stu-id="5529d-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="5529d-124">Teisisõnu, kui installite vara uuele funktsionaalsele asukohale, kasutab vara automaatselt finantsdimensioone, mis on seotud uue funktsionaalse asukohaga.</span><span class="sxs-lookup"><span data-stu-id="5529d-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="5529d-125">Seetõttu on vara kulud alati seotud funktsionaalse asukohaga, kuhu vara on praegu installitud.</span><span class="sxs-lookup"><span data-stu-id="5529d-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="5529d-126">See finantsdimensioonide automaatne käsitlemine aitab tagada kulude täieliku jälgimise, kui teie ettevõte teeb projekti juhtimise ja aruandluse funktsionaalsetes asukohtades.</span><span class="sxs-lookup"><span data-stu-id="5529d-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="5529d-127">Funktsionaalsete asukohtade hierarhia ehitamine sõltub teie ettevõtte nõuetest sisemise varustuse hoidmise või kliendiseadmete teenindamise jaoks.</span><span class="sxs-lookup"><span data-stu-id="5529d-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="5529d-128">Järgmisel joonisel on näide funktsionaalsetest asukohtadest, mis põhinevad geograafilistel asukohtadel.</span><span class="sxs-lookup"><span data-stu-id="5529d-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![Joonis 3](media/03-overview-image.png)

<span data-ttu-id="5529d-130">Järgmisel joonisel on näide funktsionaalsetest asukohtadest, mis põhinevad kliendid.</span><span class="sxs-lookup"><span data-stu-id="5529d-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![Joonis 4](media/04-overview-image.png)
