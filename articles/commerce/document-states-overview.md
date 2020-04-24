---
title: Dokumendi olekud ja töötsükkel
description: Selles teemas käsitletakse rakenduse Microsoft Dynamics 365 Commerce leheelementide erinevaid dokumendi olekuid.
author: phinneyridge
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4a00f1c363e5ecb0e3e64637a8f487c48df2df72
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261509"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="f595a-103">Dokumendi olekud ja töötsükkel</span><span class="sxs-lookup"><span data-stu-id="f595a-103">Document states and lifecycle</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f595a-104">Selles teemas käsitletakse rakenduse Microsoft Dynamics 365 Commerce leheelementide erinevaid dokumendi olekuid.</span><span class="sxs-lookup"><span data-stu-id="f595a-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="f595a-105">Dokumendi oleku kirjeldused</span><span class="sxs-lookup"><span data-stu-id="f595a-105">Document state descriptions</span></span>

<span data-ttu-id="f595a-106">Teema [lehekülje elemendid](page-elements-overview.md) loetleb erinevate dokumentide tüübid sisu haldamise süsteemis (CMS).</span><span class="sxs-lookup"><span data-stu-id="f595a-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="f595a-107">Nendel dokumenditüüpidel võib autorluse tööriistas olla mitu olekut.</span><span class="sxs-lookup"><span data-stu-id="f595a-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="f595a-108">Dokumendi olekud aitavad ennetada andmekonflikte ja jõustada versiooni kontrollimist.</span><span class="sxs-lookup"><span data-stu-id="f595a-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="f595a-109">Need määratlevad, kes saavad dokumente muuta, millal dokumente saab muuta ja millal võivad teised inimesed muudatusi näha.</span><span class="sxs-lookup"><span data-stu-id="f595a-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="f595a-110">Järgmises tabelis on toodud Commerce’i leheelementide võimalikud dokumentide olekud.</span><span class="sxs-lookup"><span data-stu-id="f595a-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="f595a-111">Dokumendi olek</span><span class="sxs-lookup"><span data-stu-id="f595a-111">Document state</span></span>      | <span data-ttu-id="f595a-112">Saidiehitaja tegevus</span><span class="sxs-lookup"><span data-stu-id="f595a-112">Site builder action</span></span>        | <span data-ttu-id="f595a-113">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f595a-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="f595a-114">Väljaregistreeritud</span><span class="sxs-lookup"><span data-stu-id="f595a-114">Checked out</span></span>         | <span data-ttu-id="f595a-115">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="f595a-115">Select **Edit**.</span></span>           | <span data-ttu-id="f595a-116">Kohaldatav dokument on teile välja registreeritud.</span><span class="sxs-lookup"><span data-stu-id="f595a-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="f595a-117">Kui dokument on selles olekus, ei saa teised autenditud süsteemi kasutajad seda muuta ja kõik dokumendis tehtud muudatused on nähtavad ainult teile.</span><span class="sxs-lookup"><span data-stu-id="f595a-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="f595a-118">Salvestatud</span><span class="sxs-lookup"><span data-stu-id="f595a-118">Saved</span></span>               | <span data-ttu-id="f595a-119">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f595a-119">Select **Save**.</span></span>           | <span data-ttu-id="f595a-120">Välja registreeritud dokumendis tehtud muudatused salvestatakse andmebaasi, kuid dokumenti pole veel registreeritud ega avaldatud.</span><span class="sxs-lookup"><span data-stu-id="f595a-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="f595a-121">Salvestatud muudatused ei ole teistele autenditud süsteemi kasutajatele nähtavad enne, kui autor on teinud valiku **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="f595a-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="f595a-122">Need ei ole välistele kasutajatele nähtavad enne, kuni üksus on avaldatud.</span><span class="sxs-lookup"><span data-stu-id="f595a-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="f595a-123">Loobutud väljaregistreerimine</span><span class="sxs-lookup"><span data-stu-id="f595a-123">Discarded check out</span></span> | <span data-ttu-id="f595a-124">Valige **Hülga redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="f595a-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="f595a-125">Kõik välja registreeritud dokumendis tehtud muudatused hüljatakse ja üksus taastab viimase registreeritud versiooni.</span><span class="sxs-lookup"><span data-stu-id="f595a-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="f595a-126">Sisseregistreeritud</span><span class="sxs-lookup"><span data-stu-id="f595a-126">Checked in</span></span>          | <span data-ttu-id="f595a-127">Valige **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="f595a-127">Select **Finish editing**.</span></span> | <span data-ttu-id="f595a-128">Redigeeritud dokument on registreeritud.</span><span class="sxs-lookup"><span data-stu-id="f595a-128">The edited document is checked in.</span></span> <span data-ttu-id="f595a-129">Kõik muudatused on teistele autenditud süsteemikasutajatele nähtavad ja need kasutajad saavad seejärel dokumenti redigeerida.</span><span class="sxs-lookup"><span data-stu-id="f595a-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="f595a-130">Iga registreerimine loob üksuse ajaloos dokumendi versiooni kirje.</span><span class="sxs-lookup"><span data-stu-id="f595a-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="f595a-131">Avaldatud</span><span class="sxs-lookup"><span data-stu-id="f595a-131">Published</span></span>           | <span data-ttu-id="f595a-132">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="f595a-132">Select **Publish**.</span></span>        | <span data-ttu-id="f595a-133">Dokument avaldatakse ja muudatused suunatakse teie reaalajas saidile ja need muutuvad süsteemivälistele kasutajatele leitavaks.</span><span class="sxs-lookup"><span data-stu-id="f595a-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="f595a-134">Üksusi saab avaldada ainult juhul, kui nad on esmalt registreeritud käsu **Lõpeta redigeerimine** abil.</span><span class="sxs-lookup"><span data-stu-id="f595a-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="f595a-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f595a-135">Additional resources</span></span>

[<span data-ttu-id="f595a-136">Sisu lisamise viisid</span><span class="sxs-lookup"><span data-stu-id="f595a-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="f595a-137">Lehe mudeli sõnastik</span><span class="sxs-lookup"><span data-stu-id="f595a-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="f595a-138">Avaldamisrühmadega töötamine</span><span class="sxs-lookup"><span data-stu-id="f595a-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="f595a-139">Moodulitega töötamine</span><span class="sxs-lookup"><span data-stu-id="f595a-139">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="f595a-140">Fragmentidega töötamine</span><span class="sxs-lookup"><span data-stu-id="f595a-140">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="f595a-141">Mallide ja paigutuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="f595a-141">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="f595a-142">Saidil navigeerimise kohandamine</span><span class="sxs-lookup"><span data-stu-id="f595a-142">Customize site navigation</span></span>](customize-site-navigation.md)
