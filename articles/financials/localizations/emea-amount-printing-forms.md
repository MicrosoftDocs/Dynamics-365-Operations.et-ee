---
title: "Aruannetel ja dokumentidel summade kuvamisviisi värskendamine"
description: "Selles teemas antakse teavet aruannetel ja muudel dokumentidel summade kuvamisviisi värskendamiseks Eesti, Leedu, Poola, Tšehhi Vabariigi, Ungaris ja Venemaa puhul."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 264254
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 226eecd49fb5c4daeb701fbb019f402519999610
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a><span data-ttu-id="0bb3a-103">Aruannetel ja dokumentidel summade kuvamisviisi värskendamine</span><span class="sxs-lookup"><span data-stu-id="0bb3a-103">Update how amounts are displayed on reports and documents</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0bb3a-104">Selles teemas antakse teavet aruannetel ja muudel dokumentidel summade kuvamisviisi värskendamiseks Eesti, Leedu, Poola, Tšehhi Vabariigi, Ungaris ja Venemaa puhul.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-104">This topic provides information about how to update how amounts are displayed on reports and other documents for Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia.</span></span>

<span data-ttu-id="0bb3a-105">Juriidiliste isikute puhul Eestis, Lätis, Leedus, Poolas, Tšehhi Vabariigis, Ungaris ja Venemaal saate seadistada valuutaühikute ning allühikute jaoks täielikud ja lühinimed.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-105">For legal entities in Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia, you can set up full names and short names for currency units and subunits.</span></span> <span data-ttu-id="0bb3a-106">Neid nimesid saab kasutada dokumentidel ja aruannetes summade kuvamisviisi määramiseks.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-106">These names can be used to transform how amounts are represented on documents and reports.</span></span> <span data-ttu-id="0bb3a-107">Näiteks kuvatakse summa **LTL 100,20** arvetes või aruannetes kui **100 Litas 20 Centas**.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-107">For example: The amount **LTL 100.20** can be displayed as **100 Litas 20 Centas**.</span></span>

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a><span data-ttu-id="0bb3a-108">Valuutaühikute ja allühikute täielike ning lühinimede seadistamine</span><span class="sxs-lookup"><span data-stu-id="0bb3a-108">Set up full and short names for currency units and subunits</span></span>
<span data-ttu-id="0bb3a-109">Valuutaühikute ja allühikute täielike ning lühinimede seadistamiseks valitud keele puhul tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-109">To set up full and short names for currency units and subunits for a language, complete the following steps:</span></span>

1.  <span data-ttu-id="0bb3a-110">Avage leht **Valuutad**.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-110">Open the **Currencies** page.</span></span>
2.  <span data-ttu-id="0bb3a-111">Valige valuuta.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-111">Select a currency.</span></span>
3.  <span data-ttu-id="0bb3a-112">Klõpsake toimingupaanil valikut **Käänamine**.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-112">On the Action Pane, click **Declension**.</span></span>
4.  <span data-ttu-id="0bb3a-113">Keele jaoks täieliku ja lühinime lisamiseks klõpsake valikut **Uus** ja täitke järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-113">To add full name and short name for a language, click **New** and complete the following fields.</span></span>
    |                                                           |                                                                                                                                                                                                                    |
    |-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="0bb3a-114">**Väli**</span><span class="sxs-lookup"><span data-stu-id="0bb3a-114">**Field**</span></span>                                                 | <span data-ttu-id="0bb3a-115">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="0bb3a-115">**Description**</span></span>                                                                                                                                                                                                    |
    | <span data-ttu-id="0bb3a-116">**Keel**</span><span class="sxs-lookup"><span data-stu-id="0bb3a-116">**Language**</span></span>                                              | <span data-ttu-id="0bb3a-117">Valige praeguse teksti keel.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-117">Select the language for the current text.</span></span>                                                                                                                                                                          |
    | <span data-ttu-id="0bb3a-118">**Ainsuse nimetav (ühikunimede väljagrupp)**</span><span class="sxs-lookup"><span data-stu-id="0bb3a-118">**Singular nominative (Name of units field group)**</span></span>       | <span data-ttu-id="0bb3a-119">Sisestage valuuta ainsusevorm.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-119">Enter the singular form of the currency.</span></span> <span data-ttu-id="0bb3a-120">Näiteks on sõna Litas ainsuse nimetav vorm Litas.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-120">For example, the singular form of Litas is Litas.</span></span>                                                                                                                         |
    | <span data-ttu-id="0bb3a-121">**Mitmuse nimetav (ühikunimede väljagrupp)**</span><span class="sxs-lookup"><span data-stu-id="0bb3a-121">**Plural nominative (Name of units field group)**</span></span>         | <span data-ttu-id="0bb3a-122">Sisestage valuuta mitmusevorm.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-122">Enter the plural form of the currency.</span></span> <span data-ttu-id="0bb3a-123">Näiteks sisestage Litai.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-123">For example, enter Litai.</span></span> <span data-ttu-id="0bb3a-124">**Märkus**. Väljad **Ainsuse omastav** ja **Mitmuse omastav** on saadaval olenevalt väljal **Keel** valitud keelest.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-124">**Note**: The **Singular genitive** and **Plural genitive** fields are available based on the language that you select in the **Language** field.</span></span> |
    | <span data-ttu-id="0bb3a-125">**Ainsuse nimetav (allühiku nimede väljagruppi)**</span><span class="sxs-lookup"><span data-stu-id="0bb3a-125">**Singular nominative field (Name of parts field group)**</span></span> | <span data-ttu-id="0bb3a-126">Sisestage valuuta allühiku ainsusevorm.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-126">Enter the singular form of the subunit of the currency.</span></span>                                                                                                                                                            |
    | <span data-ttu-id="0bb3a-127">**Mitmuse nimetav (allühiku nimede väljagrupp)**</span><span class="sxs-lookup"><span data-stu-id="0bb3a-127">**Plural nominative (Name of parts field group)**</span></span>         | <span data-ttu-id="0bb3a-128">Sisestage valuuta allühiku mitmusevorm.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-128">Enter the plural form of the subunit of the currency.</span></span>                                                                                                                                                              |
    | <span data-ttu-id="0bb3a-129">**Ühikute lühinimi (Lühinime väljagrupp)**</span><span class="sxs-lookup"><span data-stu-id="0bb3a-129">**Shortcut name of units (Short name field group)**</span></span>       | <span data-ttu-id="0bb3a-130">Sisestage valuutat tuvastav ISO-kood.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-130">Enter the ISO code to identify the currency.</span></span> <span data-ttu-id="0bb3a-131">Näiteks littide tuvastamiseks sisestage LTL.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-131">For example, enter LTL to identify Litas.</span></span>                                                                                                                             |
    | <span data-ttu-id="0bb3a-132">**Ühikute lühinimi (Lühinime väljagrupp)**</span><span class="sxs-lookup"><span data-stu-id="0bb3a-132">**Shortcut name for parts (Short name field group)**</span></span>      | <span data-ttu-id="0bb3a-133">Sisestage valuuta allühiku üldnimetus.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-133">Enter the denomination of the currency subunit.</span></span> <span data-ttu-id="0bb3a-134">Näiteks sisestage Centas.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-134">For example, enter Centas.</span></span>                                                                                                                                         |
    | <span data-ttu-id="0bb3a-135">**Sidesõna „ja” ühikute ja allühikute vahel**</span><span class="sxs-lookup"><span data-stu-id="0bb3a-135">**Conjunction 'and' between units and parts**</span></span>             | <span data-ttu-id="0bb3a-136">Märkige ruut , et printida ühikute ja allühikute vahel sidesõna „ja”.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-136">Select to print the conjunction “and” between the currency units and unit parts.</span></span> <span data-ttu-id="0bb3a-137">Näiteks kuvatakse summa LTL 100,20 arvetel või aruannetes kui „100 Litas and 20 Centas”.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-137">For example, on invoices or reports, the amount for LTL 100.20 will be displayed as 100 Litas and 20 Centas.</span></span>                      |

5.  <span data-ttu-id="0bb3a-138">Klõpsake käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0bb3a-138">Click **Save**.</span></span>





