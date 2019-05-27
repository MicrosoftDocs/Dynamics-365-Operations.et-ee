---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (14. veebruar 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1db7d032eade3f996e0554e64d6ea0704a347ed8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517778"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a><span data-ttu-id="533bd-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (14. veebruar 2019)</span><span class="sxs-lookup"><span data-stu-id="533bd-103">What's new or changed in Dynamics 365 for Talent (February 14, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="533bd-104">Selles teemas kirjeldatakse Talenti uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="533bd-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="533bd-105">Muutused Attractis</span><span class="sxs-lookup"><span data-stu-id="533bd-105">Changes in Attract</span></span>
<span data-ttu-id="533bd-106">See versioon sisaldab väikesi veaparandusi.</span><span class="sxs-lookup"><span data-stu-id="533bd-106">There are minor bug fixes included with this release.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="533bd-107">Muutused kasutuselevõtus</span><span class="sxs-lookup"><span data-stu-id="533bd-107">Changes in Onboarding</span></span>
<span data-ttu-id="533bd-108">See versioon sisaldab väikesi veaparandusi.</span><span class="sxs-lookup"><span data-stu-id="533bd-108">There are minor bug fixes included with this release.</span></span>
 
## <a name="changes-in-core-hr"></a><span data-ttu-id="533bd-109">Core HR-i muudatused</span><span class="sxs-lookup"><span data-stu-id="533bd-109">Changes in Core HR</span></span> 
<span data-ttu-id="533bd-110">**Järk 8.1.2146**</span><span class="sxs-lookup"><span data-stu-id="533bd-110">**Build 8.1.2146**</span></span>

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a><span data-ttu-id="533bd-111">Töövõtja põhipalga üksus ei ekspordi kõiki kirjeid</span><span class="sxs-lookup"><span data-stu-id="533bd-111">Employee fixed compensation entity doesn't export all records</span></span>
<span data-ttu-id="533bd-112">Selle muudatusega ekspordib üksus **Töövõtja põhipalk** nüüd kõik kirjed.</span><span class="sxs-lookup"><span data-stu-id="533bd-112">With this change, the **Employee fixed compensation** entity will now export all records.</span></span> <span data-ttu-id="533bd-113">Üksust saab kasutada olemasolevate põhipalga kirjete loomiseks ja värskendamiseks töövõtjate jaoks.</span><span class="sxs-lookup"><span data-stu-id="533bd-113">The entity can be used to create and update existing fixed compensation records for employees.</span></span> 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a><span data-ttu-id="533bd-114">Töösuhte lõppkuupäev ei arvesta töövõtja eelistatud ajavööndi sätteid</span><span class="sxs-lookup"><span data-stu-id="533bd-114">Employment end date doesn't honor employee preferred time zone settings</span></span>
<span data-ttu-id="533bd-115">Töösuhte lõppkuupäevad arvestavad nüüd ettevõttega töösuhte loomisel või lõpetamisel kasutaja eelistatud ajavööndit.</span><span class="sxs-lookup"><span data-stu-id="533bd-115">Employment end dates are now honoring the user-preferred time zone when creating or ending employment with a company.</span></span>
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a><span data-ttu-id="533bd-116">Ühendkuningriigi aadresse kuvatakse lehel Analüütika Ida-Šveitsi aadressidena</span><span class="sxs-lookup"><span data-stu-id="533bd-116">UK addresses display in Analytics as Eastern Switzerland addresses</span></span>
<span data-ttu-id="533bd-117">Selles versioonis on tehtud muudatus, mis parandab aadresside joondusvea jaotise **Personalihaldus** aruandes Töötajate arv asukoha järgi.</span><span class="sxs-lookup"><span data-stu-id="533bd-117">In this release, a change has been made to correct misalignment in addresses in the **Personnel Management** "Headcount by location" report.</span></span>
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a><span data-ttu-id="533bd-118">Lõpetamise kood pole ametikoha lõpetamisel töötaja ametikoha määramiskirjes täidetud</span><span class="sxs-lookup"><span data-stu-id="533bd-118">Termination code is not populated on the worker position assignment record when ending the position</span></span>
<span data-ttu-id="533bd-119">Tehti muudatus, mis seab töötaja ametikoha määramise lõpetamisel vaikeväärtuseks koodi Lõpetamise põhjus.</span><span class="sxs-lookup"><span data-stu-id="533bd-119">A change has been made to default the "Termination reason" code when ending the employees position assignment.</span></span>

### <a name="new-entity-created-for-job-compensation-levels"></a><span data-ttu-id="533bd-120">Töö hüvitustasemete jaoks loodud uus kirje</span><span class="sxs-lookup"><span data-stu-id="533bd-120">New entity created for job compensation levels</span></span>
<span data-ttu-id="533bd-121">Loodi uus andmehaldusraamistiku (DMF) üksus.</span><span class="sxs-lookup"><span data-stu-id="533bd-121">A new data management framework (DMF) entity was created.</span></span> <span data-ttu-id="533bd-122">Üksus tagab iga süsteemis määratletud töö hüvitustasemete, turuväärtuste ja uuringuteabe loomise ja värskendamise.</span><span class="sxs-lookup"><span data-stu-id="533bd-122">The entity provides for creation and updates to compensation levels, market values, and survey information for each job defined in the system.</span></span>
