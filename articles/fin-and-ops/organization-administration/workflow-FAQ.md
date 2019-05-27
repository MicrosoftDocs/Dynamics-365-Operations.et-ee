---
title: Töövoo KKK
description: Teemas on toodud vastused korduma kippuvatele küsimustele rakenduse Microsoft Dynamics 365 for Finance and Operations töövoo süsteemi kohta.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509287"
---
# <a name="workflow-system"></a><span data-ttu-id="79c47-103">Töövoo süsteem</span><span class="sxs-lookup"><span data-stu-id="79c47-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79c47-104">Teemas on toodud vastused korduma kippuvatele küsimustele rakenduse Microsoft Dynamics 365 for Finance and Operations töövoo süsteemi kohta.</span><span class="sxs-lookup"><span data-stu-id="79c47-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="79c47-105">Teatised</span><span class="sxs-lookup"><span data-stu-id="79c47-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="79c47-106">Miks võetakse tööüksuse tagasilükkamisel vastu mitu teatist?</span><span class="sxs-lookup"><span data-stu-id="79c47-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="79c47-107">Tööüksuse tagasilükkamisel viiakse see tööüksus tagasilükatuna lõpuni.</span><span class="sxs-lookup"><span data-stu-id="79c47-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="79c47-108">Algatajale luuakse ja määratakse teine tööüksus.</span><span class="sxs-lookup"><span data-stu-id="79c47-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="79c47-109">See tähendab, et algataja saab teatise tagasilükatud tööüksuse kohta ja kasutaja, kellele määrati uus „taotletakse muudatust” tööüksus, saab eraldi teatise.</span><span class="sxs-lookup"><span data-stu-id="79c47-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="79c47-110">Iga teatis on erineva tööüksuse jaoks, kuid nende sarnasus võib põhjustada segadust.</span><span class="sxs-lookup"><span data-stu-id="79c47-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="79c47-111">Otsime võimalusi selle tulevases väljaandes parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="79c47-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="79c47-112">Miks minu töövoo eksport nurjub?</span><span class="sxs-lookup"><span data-stu-id="79c47-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="79c47-113">Praegu on töövoo ekspordi funktsioonil piirang, milles töövoo nimede pikkus ei tohi ületada 48 märki.</span><span class="sxs-lookup"><span data-stu-id="79c47-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="79c47-114">Kasutades nime, mis on pikem kui 48 märki võib põhjustada tõrke "Server ei saanud taotlust autentida" ja/või takistada faili eksportimist failitüübita.</span><span class="sxs-lookup"><span data-stu-id="79c47-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="79c47-115">Järgmine ajaveebipostitus sisaldab üksikasju [Töövoo ekspordi tõrkeotsingu](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting) kohta.</span><span class="sxs-lookup"><span data-stu-id="79c47-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>
