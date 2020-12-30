---
title: Varad ja töökäsud
description: Selles teemas kirjeldatakse varasid ja töökäskusid varahalduses.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c2500a695fcffe0d60ac13b1b74cda4322b0e14
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426300"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="f7817-103">Varad ja töökäsud</span><span class="sxs-lookup"><span data-stu-id="f7817-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f7817-104">Selles teemas kirjeldatakse varasid ja töökäskusid varahalduses.</span><span class="sxs-lookup"><span data-stu-id="f7817-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="f7817-105">Varad ja töökäsud on varahalduse kesksed osad.</span><span class="sxs-lookup"><span data-stu-id="f7817-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="f7817-106">*Vara* on masin või masina osa, mis nõuab pidevat hooldust ja teenindust.</span><span class="sxs-lookup"><span data-stu-id="f7817-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="f7817-107">Varasid saab luua hierarhilises struktuuris ja need võivad olla seotud funktsionaalsete asukohtadega.</span><span class="sxs-lookup"><span data-stu-id="f7817-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="f7817-108">Hooldustöid saab kavandada varade kõikidel tasanditel.</span><span class="sxs-lookup"><span data-stu-id="f7817-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="f7817-109">Igale varale seadistatakse mitmesugused andmed, näiteks tooteteave ja vara täpsustus ning nõutavad hooldusplaanid.</span><span class="sxs-lookup"><span data-stu-id="f7817-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="f7817-110">Järgmisel joonisel on ülevaade vara andmetest ja varade kuuluvusest töö tüüpides.</span><span class="sxs-lookup"><span data-stu-id="f7817-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="f7817-111">Punast teksti kasutatakse näidete puhul, mis näitavad päritolu ja sõltuvused.</span><span class="sxs-lookup"><span data-stu-id="f7817-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![Töö tüüpidega seotud vara andmeid kuvav diagramm](media/05-overview-image.png)

<span data-ttu-id="f7817-113">Igal töökäsul on töökäsu tüüp, ennetav hooldus, korrigeeriv hooldus või kontroll.</span><span class="sxs-lookup"><span data-stu-id="f7817-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="f7817-114">Töökäsk sisaldab ühte või mitut töökäsu tööd.</span><span class="sxs-lookup"><span data-stu-id="f7817-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="f7817-115">Iga töökäsu töö määratleb töö, mis tuleb sooritada vara ja seotud töö tüübiga.</span><span class="sxs-lookup"><span data-stu-id="f7817-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="f7817-116">Seotud töö tüüpide hulgas on 10 000 km, 50 000 km, 1-aastane ülevaatus ja ohutusinspektsioon.</span><span class="sxs-lookup"><span data-stu-id="f7817-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="f7817-117">Üks töökäsk võib olla seotud mitme varaga.</span><span class="sxs-lookup"><span data-stu-id="f7817-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="f7817-118">Järgmine illustratsioon näitab töökäsu põhiandmete ülevaadet.</span><span class="sxs-lookup"><span data-stu-id="f7817-118">The following illustration shows an overview of the key data in a work order.</span></span>

![Töökäsu põhiandmeid kuvav diagramm](media/06-overview-image.png)

<span data-ttu-id="f7817-120">Töökäsk võib olla seotud mõne muu töökäsuga ja töö tüübid võivad sisaldada töökäsu loomiseks järeltöid.</span><span class="sxs-lookup"><span data-stu-id="f7817-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="f7817-121">Üldiselt ei ole töökäskude vahel sõltuvusi.</span><span class="sxs-lookup"><span data-stu-id="f7817-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="f7817-122">Seetõttu saavad nad muuta oma töökäskude elutsükli olekut ja neid saab planeerida üksteisest sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="f7817-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="f7817-123">Töökäskusid saab luua erinevatel viisidel, mis on seotud korrigeeriva, ennetava või reaktiivse hooldusega.</span><span class="sxs-lookup"><span data-stu-id="f7817-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="f7817-124">Saate töökäske luua ka käsitsi.</span><span class="sxs-lookup"><span data-stu-id="f7817-124">You can also create work orders manually.</span></span> <span data-ttu-id="f7817-125">Järgmine illustratsioon näitab ülevaadet töökäskude automaatse või käsitsi loomise protsessist.</span><span class="sxs-lookup"><span data-stu-id="f7817-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![Töökäskude automaatset või käsitsi loomist kuvav diagramm](media/07-overview-image.png)

<span data-ttu-id="f7817-127">Töökäsu hooldustöö plaanimisel ja käitamisel tuleb täita mitu etappi.</span><span class="sxs-lookup"><span data-stu-id="f7817-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="f7817-128">Järgmine illustratsioon näitab töötlemine ülevaadet.</span><span class="sxs-lookup"><span data-stu-id="f7817-128">The following illustration shows an overview of the processing for a work order.</span></span>

![Töökäsu töötlemise ülevaadet kuvav diagramm](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="f7817-130">Kui töötate rakenduses Dynamics 365 Supply Chain Management ja moodulis **Varahaldus** valite uue kirje loomiseks **Uus**, valige **Redigeeri** olemasoleva kirje värskendamiseks ja valige **Salvesta** uute või redigeeritud andmete salvestamiseks.</span><span class="sxs-lookup"><span data-stu-id="f7817-130">In general, when you work in Dynamics 365 Supply Chain Management and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>
