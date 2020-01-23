---
title: Dokumendi olekud ja töötsükkel
description: Selles teemas käsitletakse rakenduse Microsoft Dynamics 365 Commerce leheelementide erinevaid dokumendi olekuid.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: edb81efc45fc5e7eed32cb7d9b8fda5ade987dd4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914883"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="2fa89-103">Dokumendi olekud ja töötsükkel</span><span class="sxs-lookup"><span data-stu-id="2fa89-103">Document states and lifecycle</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2fa89-104">Selles teemas käsitletakse rakenduse Microsoft Dynamics 365 Commerce leheelementide erinevaid dokumendi olekuid.</span><span class="sxs-lookup"><span data-stu-id="2fa89-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="2fa89-105">Dokumendi oleku kirjeldused</span><span class="sxs-lookup"><span data-stu-id="2fa89-105">Document state descriptions</span></span>

<span data-ttu-id="2fa89-106">Teema [lehekülje elemendid](page-elements-overview.md) loetleb erinevate dokumentide tüübid sisu haldamise süsteemis (CMS).</span><span class="sxs-lookup"><span data-stu-id="2fa89-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="2fa89-107">Nendel dokumenditüüpidel võib autorluse tööriistas olla mitu olekut.</span><span class="sxs-lookup"><span data-stu-id="2fa89-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="2fa89-108">Dokumendi olekud aitavad ennetada andmekonflikte ja jõustada versiooni kontrollimist.</span><span class="sxs-lookup"><span data-stu-id="2fa89-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="2fa89-109">Need määratlevad, kes saavad dokumente muuta, millal dokumente saab muuta ja millal võivad teised inimesed muudatusi näha.</span><span class="sxs-lookup"><span data-stu-id="2fa89-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="2fa89-110">Järgmises tabelis on toodud Commerce’i leheelementide võimalikud dokumentide olekud.</span><span class="sxs-lookup"><span data-stu-id="2fa89-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="2fa89-111">Dokumendi olek</span><span class="sxs-lookup"><span data-stu-id="2fa89-111">Document state</span></span> | <span data-ttu-id="2fa89-112">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2fa89-112">Description</span></span> |
|---|---|
| <span data-ttu-id="2fa89-113">Väljaregistreeritud</span><span class="sxs-lookup"><span data-stu-id="2fa89-113">Checked out</span></span> | <span data-ttu-id="2fa89-114">Kui CMS-i üksus on teile välja registreeritud, ei saa ükski teine volitatud süsteemi kasutaja seda redigeerida.</span><span class="sxs-lookup"><span data-stu-id="2fa89-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="2fa89-115">Mis tahes üksusele tehtavad muudatused on nähtavad ainult teile.</span><span class="sxs-lookup"><span data-stu-id="2fa89-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="2fa89-116">Sisseregistreeritud</span><span class="sxs-lookup"><span data-stu-id="2fa89-116">Checked in</span></span> | <span data-ttu-id="2fa89-117">Kui CMS-i üksus on registreeritud, on kõik muudatused teistele volitatud süsteemi kasutajatele nähtavad ja need kasutajad saavad seejärel üksuse välja registreerida ja seda redigeerida.</span><span class="sxs-lookup"><span data-stu-id="2fa89-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="2fa89-118">Iga registreerimine loob üksuse ajaloos dokumendi versiooni kirje.</span><span class="sxs-lookup"><span data-stu-id="2fa89-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="2fa89-119">Avaldatud</span><span class="sxs-lookup"><span data-stu-id="2fa89-119">Published</span></span> | <span data-ttu-id="2fa89-120">Kui CMS-i üksus on avaldatud, suunatakse see teie reaalajas saidile ja see muutub mitte volitatud välistele kasutajatele internetis leitavaks.</span><span class="sxs-lookup"><span data-stu-id="2fa89-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="2fa89-121">Üksuseid saab avaldada ainult siis, kui need on registreeritud.</span><span class="sxs-lookup"><span data-stu-id="2fa89-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="2fa89-122">Salvestatud</span><span class="sxs-lookup"><span data-stu-id="2fa89-122">Saved</span></span> | <span data-ttu-id="2fa89-123">Väljaregistreeritud CMS-i üksusele tehtud muudatused saab salvestada CMS-i enne, kui üksus registreeritakse või avaldatakse.</span><span class="sxs-lookup"><span data-stu-id="2fa89-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="2fa89-124">Need salvestatud muudatused ei ole teistele autenditud süsteemi kasutajatele nähtavad enne, kui üksus on registreeritud.</span><span class="sxs-lookup"><span data-stu-id="2fa89-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="2fa89-125">Need ei ole välistele kasutajatele nähtavad enne, kuni üksus on avaldatud.</span><span class="sxs-lookup"><span data-stu-id="2fa89-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="2fa89-126">Loobutud väljaregistreerimine</span><span class="sxs-lookup"><span data-stu-id="2fa89-126">Discarded check out</span></span> | <span data-ttu-id="2fa89-127">Kui väljaregistreeritud CMS-i üksusest loobutakse, kustutatakse kõik salvestatud muudatused ja üksus naaseb versioonile, mis oli viimati registreeritud.</span><span class="sxs-lookup"><span data-stu-id="2fa89-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="2fa89-128">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2fa89-128">Additional resources</span></span>

[<span data-ttu-id="2fa89-129">Sisu lisamise viisid</span><span class="sxs-lookup"><span data-stu-id="2fa89-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="2fa89-130">Lehe mudeli sõnastik</span><span class="sxs-lookup"><span data-stu-id="2fa89-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="2fa89-131">Avaldamisrühmadega töötamine</span><span class="sxs-lookup"><span data-stu-id="2fa89-131">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="2fa89-132">Moodulitega töötamine</span><span class="sxs-lookup"><span data-stu-id="2fa89-132">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="2fa89-133">Fragmentidega töötamine</span><span class="sxs-lookup"><span data-stu-id="2fa89-133">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="2fa89-134">Mallide ja paigutuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="2fa89-134">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="2fa89-135">Saidil navigeerimise kohandamine</span><span class="sxs-lookup"><span data-stu-id="2fa89-135">Customize site navigation</span></span>](customize-site-navigation.md)
