---
title: "Kassa rakenduse ja kasutaja keelesätted"
description: "Selles teemas kirjeldatakse Retail Modern POS-i (MPOS) ja pilve kassa keelesätete muutmist."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cabb63aea0da4b264aec8e0cc4d43b3e1014e71b
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="pos-application-and-user-language-settings"></a><span data-ttu-id="a35ad-103">Kassa rakenduse ja kasutaja keelesätted</span><span class="sxs-lookup"><span data-stu-id="a35ad-103">POS application and user language settings</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a35ad-104">Selles teemas kirjeldatakse Retail Modern POS-i (MPOS) ja pilve kassa keelesätete muutmist.</span><span class="sxs-lookup"><span data-stu-id="a35ad-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

<a name="overview"></a><span data-ttu-id="a35ad-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="a35ad-105">Overview</span></span>
========

<span data-ttu-id="a35ad-106">Retail Modern POS (MPOS) ja pilve kassa toetavad keskkondi, kus kaupluse ja kasutaja keelesätted ja tõlked võivad erineda.</span><span class="sxs-lookup"><span data-stu-id="a35ad-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="a35ad-107">Näiteks asub kauplus piirkonnas, kus enamik kliente kasutab inglise keelt, kuid mõned töötajad eelistavad prantsuskeelse tõlkega rakendust kasutada.</span><span class="sxs-lookup"><span data-stu-id="a35ad-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="a35ad-108">Andmete keel</span><span class="sxs-lookup"><span data-stu-id="a35ad-108">Data language</span></span>
<span data-ttu-id="a35ad-109">Olenemata kasutaja sätetest kasutavad Retail Modern POS ja pilve kassa andmete tõlkimiseks kaupluse sätetes määratud keelt.</span><span class="sxs-lookup"><span data-stu-id="a35ad-109">Regardless of the user’s settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="a35ad-110">See tagab kõigile kasutajatele ja klientidele sama kogemuse.</span><span class="sxs-lookup"><span data-stu-id="a35ad-110">This will ensure that all users and customers will have a consistent experience.</span></span>  <span data-ttu-id="a35ad-111">Andmete näidete hulka kuuluvad:</span><span class="sxs-lookup"><span data-stu-id="a35ad-111">Examples of data include:</span></span>

-   <span data-ttu-id="a35ad-112">Tooted</span><span class="sxs-lookup"><span data-stu-id="a35ad-112">Products</span></span>
-   <span data-ttu-id="a35ad-113">atribuudid ja väärtused,</span><span class="sxs-lookup"><span data-stu-id="a35ad-113">Attributes and values</span></span>
-   <span data-ttu-id="a35ad-114">kategooriate nimed,</span><span class="sxs-lookup"><span data-stu-id="a35ad-114">Category names</span></span>
-   <span data-ttu-id="a35ad-115">prinditud või meilitsi saadetud kannete sissetulekud,</span><span class="sxs-lookup"><span data-stu-id="a35ad-115">Printed or emailed transaction receipts</span></span>
-   <span data-ttu-id="a35ad-116">makseviiside nimed,</span><span class="sxs-lookup"><span data-stu-id="a35ad-116">Payment method names</span></span>
-   <span data-ttu-id="a35ad-117">rea kuvateated.</span><span class="sxs-lookup"><span data-stu-id="a35ad-117">Line display messages</span></span>

<span data-ttu-id="a35ad-118">Kaupluse keelt kasutatakse ka kassa peamises sisselogimisaknas, kuna kasutaja ei ole enne sisselogimist teada.</span><span class="sxs-lookup"><span data-stu-id="a35ad-118">The store’s language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="a35ad-119">Kui kaupluse keele jaoks pole tõlget saadaval, ennistatakse kassasse ettevõtte keel.</span><span class="sxs-lookup"><span data-stu-id="a35ad-119">If a translation is not available for the store’s language, the POS will revert to the company’s language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="a35ad-120">Kaupluse keelesätte konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a35ad-120">Configuring the store’s language setting</span></span>

<span data-ttu-id="a35ad-121">Kaupluse keelt saab seadistada lehel **Jaekauplus** jaotises **Kõik jaekauplused**, valides **Üldine &gt; Regioonisätted &gt; Keel.</span><span class="sxs-lookup"><span data-stu-id="a35ad-121">The store’s language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language.</span></span> <span data-ttu-id="a35ad-122">**Iga kaupluste jaoks keele valimiseks kasutage rippmenüüd.</span><span class="sxs-lookup"><span data-stu-id="a35ad-122">**Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="a35ad-123">Kasutajaliidese keel</span><span class="sxs-lookup"><span data-stu-id="a35ad-123">User interface language</span></span>
<span data-ttu-id="a35ad-124">Kassa kasutaja keelesäte määrab rakenduse kasutajaliideses kasutatavad tõlked.</span><span class="sxs-lookup"><span data-stu-id="a35ad-124">The POS user’s language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="a35ad-125">See hõlmab kõiki silte, menüüsid ja loendeid, mida ei peeta andmeteks.</span><span class="sxs-lookup"><span data-stu-id="a35ad-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="a35ad-126">Erandiks on vaid kassa nupupaneelidel kuvatav tekst.</span><span class="sxs-lookup"><span data-stu-id="a35ad-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="a35ad-127">Nupupaneelid ei toeta tõlkeid, seega kuvatakse neil alati nupul määratletud tekst.</span><span class="sxs-lookup"><span data-stu-id="a35ad-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="a35ad-128">Tõlgitud nuppude toetamiseks tuleb kopeerida ja salvestada eraldi nupupaneelid ning määrata need vastavatele kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="a35ad-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="a35ad-129">Kasutaja keelesätte konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a35ad-129">Configuring the user’s language setting</span></span>

<span data-ttu-id="a35ad-130">Kassa kasutaja keelt saab seadistada lehel **Töötaja** jaotises **Kõik töötajad**, valides **Jaemüük &gt; Keel**.</span><span class="sxs-lookup"><span data-stu-id="a35ad-130">The POS user’s language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span>  <span data-ttu-id="a35ad-131">Seda ei seadistata vahekaardil Profiil. Kassa ei kasuta seda sätet.</span><span class="sxs-lookup"><span data-stu-id="a35ad-131">It is not set on the main Profile tab.  This setting is not used by POS.</span></span> <span data-ttu-id="a35ad-132">Kui kasutaja keelt ei määrata või määratakse mõni keel, millele ei ole tõlget saadaval, ennistatakse kassas kaupluse keel.</span><span class="sxs-lookup"><span data-stu-id="a35ad-132">If the user’s language is not set or it is set to a language where translations are not available, the POS will revert to the store’s language.</span></span>  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a35ad-133">** **</span><span class="sxs-lookup"><span data-stu-id="a35ad-133">** **</span></span>       | <span data-ttu-id="a35ad-134">**Kasutajaliidese keel** ** **</span><span class="sxs-lookup"><span data-stu-id="a35ad-134">**UI language** ** **</span></span>      | <span data-ttu-id="a35ad-135">**Andmete keel (tooted, kviitungi vormingud, rea kuva jne)**</span><span class="sxs-lookup"><span data-stu-id="a35ad-135">**Data language (products, receipt formats, line display, etc.)**</span></span> |
| <span data-ttu-id="a35ad-136">**Ettevõte**</span><span class="sxs-lookup"><span data-stu-id="a35ad-136">**Company**</span></span> | <span data-ttu-id="a35ad-137">Vaikimisi</span><span class="sxs-lookup"><span data-stu-id="a35ad-137">Default</span></span>                    | <span data-ttu-id="a35ad-138">Vaikimisi</span><span class="sxs-lookup"><span data-stu-id="a35ad-138">Default</span></span>                                                           |
| <span data-ttu-id="a35ad-139">**Kauplus**</span><span class="sxs-lookup"><span data-stu-id="a35ad-139">**Store**</span></span>   | <span data-ttu-id="a35ad-140">Tühistab ettevõtte</span><span class="sxs-lookup"><span data-stu-id="a35ad-140">Overrides company</span></span>          | <span data-ttu-id="a35ad-141">Tühistab ettevõtte</span><span class="sxs-lookup"><span data-stu-id="a35ad-141">Overrides company</span></span>                                                 |
| <span data-ttu-id="a35ad-142">**Kasutaja**</span><span class="sxs-lookup"><span data-stu-id="a35ad-142">**User**</span></span>    | <span data-ttu-id="a35ad-143">Tühistab kaupluse või ettevõtte</span><span class="sxs-lookup"><span data-stu-id="a35ad-143">Overrides store or company</span></span> | <span data-ttu-id="a35ad-144">Mitte kunagi</span><span class="sxs-lookup"><span data-stu-id="a35ad-144">Never</span></span>                                                             |






