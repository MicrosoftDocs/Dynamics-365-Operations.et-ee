---
title: Vöötkoodide häälestamine
description: Selles artiklis kirjeldatakse vöötkoodide kasutamist rakenduses Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 52801e0d09b1d7da50719966700ca45275d702f7
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057274"
---
# <a name="set-up-bar-codes"></a><span data-ttu-id="47758-103">Vöötkoodide häälestamine</span><span class="sxs-lookup"><span data-stu-id="47758-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="47758-104">Selles artiklis kirjeldatakse vöötkoodide kasutamist rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="47758-104">This article describes how to use bar codes in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="47758-105">Vöötkoode saate kasutada toodete ostmiseks ja müümiseks, tootevariantide jälgimiseks ning klientide ja töötajate seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="47758-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="47758-106">Samuti saate vöötkoodide abil väljastada ja heaks kiita kuponge, kinkekaarte ja kreeditarveid.</span><span class="sxs-lookup"><span data-stu-id="47758-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="47758-107">Saate seadistada tooteid, et neil oleks standardsed või kohandatud ettevõttesisesed vöötkoodid.</span><span class="sxs-lookup"><span data-stu-id="47758-107">You can set up products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="47758-108">Toodetel võib olla rohkem kui üks vöötkood.</span><span class="sxs-lookup"><span data-stu-id="47758-108">Products can have more than one bar code.</span></span> <span data-ttu-id="47758-109">Näiteks võib tootel olla mitu vöötkoodi, kui tegemist on erinevate tootjate toodetega või kui sellel on suuruse, stiili või värvi alusel eristatavaid variante.</span><span class="sxs-lookup"><span data-stu-id="47758-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="47758-110">Vöötkoodid võivad sisaldada toote kaalu või hinda.</span><span class="sxs-lookup"><span data-stu-id="47758-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="47758-111">Vöötkoodide maskid on mallid vöötkoodide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="47758-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="47758-112">Kui määrate igale variandi kombinatsioonile kordumatu vöötkoodi, saate vöötkoodi kassaaparaadis skannida ja lasta programmil määrata, millist toote varianti müüakse.</span><span class="sxs-lookup"><span data-stu-id="47758-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="47758-113">Samuti saate müügistatistikat variandi kaupa koguda ja kuvada.</span><span class="sxs-lookup"><span data-stu-id="47758-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="47758-114">Igale suuruse, värvi ja stiili grupile saab määrata kordumatu numbri, mis selle grupi vöötkoodis tuvastab.</span><span class="sxs-lookup"><span data-stu-id="47758-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="47758-115">Commerce kasutab vöötkoodi maski vöötkoodide automaatseks loomiseks igale variandikombinatsioonile.</span><span class="sxs-lookup"><span data-stu-id="47758-115">Commerce uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="47758-116">Kui suurusi, värve ja stiile on palju, võib see funktsioon kasulik olla, kuna kombinatsioonide arv suureneb oluliselt iga lisatud variandikoodiga.</span><span class="sxs-lookup"><span data-stu-id="47758-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="47758-117">Kui seda funktsiooni ei kasutata, tuleb vöötkoodid määrata igale toote varianti tähistavale kombinatsioonile käsitsi.</span><span class="sxs-lookup"><span data-stu-id="47758-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="47758-118">Vöötkoode saate luua käsitsi või automaatselt.</span><span class="sxs-lookup"><span data-stu-id="47758-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="47758-119">Vöötkoodide loomiseks tehke järgmised tegevused loetletud järjekorras.</span><span class="sxs-lookup"><span data-stu-id="47758-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="47758-120">[Vöötkoodi maski tähemärkide seadistamine](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="47758-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="47758-121">[Vöötkoodi maskide seadistamine](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="47758-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="47758-122">Konfigureerige vöötkoodi seadistused.</span><span class="sxs-lookup"><span data-stu-id="47758-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="47758-123">Looge vöötkoodid kindlatele toodetele.</span><span class="sxs-lookup"><span data-stu-id="47758-123">Create bar codes for products.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47758-124">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="47758-124">Additional resources</span></span>

[<span data-ttu-id="47758-125">Vöötkoodi maskide häälestamine</span><span class="sxs-lookup"><span data-stu-id="47758-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)
