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
ms.search.form: Currency
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264254
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: daa9443c5676189a771dc3af745e7d26aa0b32f3
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a><span data-ttu-id="6ede0-103">Aruannetel ja dokumentidel summade kuvamisviisi värskendamine</span><span class="sxs-lookup"><span data-stu-id="6ede0-103">Update how amounts are displayed on reports and documents</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="6ede0-104">Selles teemas antakse teavet aruannetel ja muudel dokumentidel summade kuvamisviisi värskendamiseks Eesti, Leedu, Poola, Tšehhi Vabariigi, Ungaris ja Venemaa puhul.</span><span class="sxs-lookup"><span data-stu-id="6ede0-104">This topic provides information about how to update how amounts are displayed on reports and other documents for Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia.</span></span>

<span data-ttu-id="6ede0-105">Juriidiliste isikute puhul Eestis, Lätis, Leedus, Poolas, Tšehhi Vabariigis, Ungaris ja Venemaal saate seadistada valuutaühikute ning allühikute jaoks täielikud ja lühinimed.</span><span class="sxs-lookup"><span data-stu-id="6ede0-105">For legal entities in Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia, you can set up full names and short names for currency units and subunits.</span></span> <span data-ttu-id="6ede0-106">Neid nimesid saab kasutada dokumentidel ja aruannetes summade kuvamisviisi määramiseks.</span><span class="sxs-lookup"><span data-stu-id="6ede0-106">These names can be used to transform how amounts are represented on documents and reports.</span></span> <span data-ttu-id="6ede0-107">Näiteks kuvatakse summa **LTL 100,20** arvetes või aruannetes kui **100 Litas 20 Centas**.</span><span class="sxs-lookup"><span data-stu-id="6ede0-107">For example: The amount **LTL 100.20** can be displayed as **100 Litas 20 Centas**.</span></span>

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a><span data-ttu-id="6ede0-108">Valuutaühikute ja allühikute täielike ning lühinimede seadistamine</span><span class="sxs-lookup"><span data-stu-id="6ede0-108">Set up full and short names for currency units and subunits</span></span>
<span data-ttu-id="6ede0-109">Valuutaühikute ja allühikute täielike ning lühinimede seadistamiseks valitud keele puhul tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="6ede0-109">To set up full and short names for currency units and subunits for a language, complete the following steps:</span></span>

1. <span data-ttu-id="6ede0-110">Avage leht **Valuutad**.</span><span class="sxs-lookup"><span data-stu-id="6ede0-110">Open the **Currencies** page.</span></span>
2. <span data-ttu-id="6ede0-111">Valige valuuta.</span><span class="sxs-lookup"><span data-stu-id="6ede0-111">Select a currency.</span></span>
3. <span data-ttu-id="6ede0-112">Klõpsake toimingupaanil valikut **Käänamine**.</span><span class="sxs-lookup"><span data-stu-id="6ede0-112">On the Action Pane, click **Declension**.</span></span>
4. <span data-ttu-id="6ede0-113">Keele jaoks täieliku ja lühinime lisamiseks klõpsake valikut **Uus** ja täitke järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="6ede0-113">To add full name and short name for a language, click **New** and complete the following fields.</span></span>

   |                                                                        |                                                                                                                                                                                                                                                                        |
   |------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |                         <span data-ttu-id="6ede0-114"><strong>Väli</strong></span><span class="sxs-lookup"><span data-stu-id="6ede0-114"><strong>Field</strong></span></span>                         |                                                                                                                      <span data-ttu-id="6ede0-115"><strong>Kirjeldus</strong></span><span class="sxs-lookup"><span data-stu-id="6ede0-115"><strong>Description</strong></span></span>                                                                                                                      |
   |                       <span data-ttu-id="6ede0-116"><strong>Keel</strong></span><span class="sxs-lookup"><span data-stu-id="6ede0-116"><strong>Language</strong></span></span>                        |                                                                                                               <span data-ttu-id="6ede0-117">Valige praeguse teksti keel.</span><span class="sxs-lookup"><span data-stu-id="6ede0-117">Select the language for the current text.</span></span>                                                                                                                |
   |    <span data-ttu-id="6ede0-118"><strong>Ainsuse nimetav (ühikunimede väljagrupp)</strong></span><span class="sxs-lookup"><span data-stu-id="6ede0-118"><strong>Singular nominative (Name of units field group)</strong></span></span>    |                                                                                       <span data-ttu-id="6ede0-119">Sisestage valuuta ainsusevorm.</span><span class="sxs-lookup"><span data-stu-id="6ede0-119">Enter the singular form of the currency.</span></span> <span data-ttu-id="6ede0-120">Näiteks on sõna Litas ainsuse nimetav vorm Litas.</span><span class="sxs-lookup"><span data-stu-id="6ede0-120">For example, the singular form of Litas is Litas.</span></span>                                                                                       |
   |     <span data-ttu-id="6ede0-121"><strong>Mitmuse nimetav (ühikunimede väljagrupp)</strong></span><span class="sxs-lookup"><span data-stu-id="6ede0-121"><strong>Plural nominative (Name of units field group)</strong></span></span>     | <span data-ttu-id="6ede0-122">Sisestage valuuta mitmusevorm.</span><span class="sxs-lookup"><span data-stu-id="6ede0-122">Enter the plural form of the currency.</span></span> <span data-ttu-id="6ede0-123">Näiteks sisestage Litai.</span><span class="sxs-lookup"><span data-stu-id="6ede0-123">For example, enter Litai.</span></span> <span data-ttu-id="6ede0-124"><strong>Märkus</strong>. Väljad <strong>Ainsuse omastav</strong> ja <strong>Mitmuse omastav</strong> on saadaval olenevalt väljal <strong>Keel</strong> valitud keelest.</span><span class="sxs-lookup"><span data-stu-id="6ede0-124"><strong>Note</strong>: The <strong>Singular genitive</strong> and <strong>Plural genitive</strong> fields are available based on the language that you select in the <strong>Language</strong> field.</span></span> |
   | <span data-ttu-id="6ede0-125"><strong>Ainsuse nimetav (allühiku nimede väljagruppi)</strong></span><span class="sxs-lookup"><span data-stu-id="6ede0-125"><strong>Singular nominative field (Name of parts field group)</strong></span></span> |                                                                                                        <span data-ttu-id="6ede0-126">Sisestage valuuta allühiku ainsusevorm.</span><span class="sxs-lookup"><span data-stu-id="6ede0-126">Enter the singular form of the subunit of the currency.</span></span>                                                                                                         |
   |     <span data-ttu-id="6ede0-127"><strong>Mitmuse nimetav (allühiku nimede väljagrupp)</strong></span><span class="sxs-lookup"><span data-stu-id="6ede0-127"><strong>Plural nominative (Name of parts field group)</strong></span></span>     |                                                                                                         <span data-ttu-id="6ede0-128">Sisestage valuuta allühiku mitmusevorm.</span><span class="sxs-lookup"><span data-stu-id="6ede0-128">Enter the plural form of the subunit of the currency.</span></span>                                                                                                          |
   |    <span data-ttu-id="6ede0-129"><strong>Ühikute lühinimi (Lühinime väljagrupp)</strong></span><span class="sxs-lookup"><span data-stu-id="6ede0-129"><strong>Shortcut name of units (Short name field group)</strong></span></span>    |                                                                                         <span data-ttu-id="6ede0-130">Sisestage valuutat tuvastav ISO-kood.</span><span class="sxs-lookup"><span data-stu-id="6ede0-130">Enter the ISO code to identify the currency.</span></span> <span data-ttu-id="6ede0-131">Näiteks littide tuvastamiseks sisestage LTL.</span><span class="sxs-lookup"><span data-stu-id="6ede0-131">For example, enter LTL to identify Litas.</span></span>                                                                                         |
   |   <span data-ttu-id="6ede0-132"><strong>Ühikute lühinimi (Lühinime väljagrupp)</strong></span><span class="sxs-lookup"><span data-stu-id="6ede0-132"><strong>Shortcut name for parts (Short name field group)</strong></span></span>    |                                                                                               <span data-ttu-id="6ede0-133">Sisestage valuuta allühiku üldnimetus.</span><span class="sxs-lookup"><span data-stu-id="6ede0-133">Enter the denomination of the currency subunit.</span></span> <span data-ttu-id="6ede0-134">Näiteks sisestage Centas.</span><span class="sxs-lookup"><span data-stu-id="6ede0-134">For example, enter Centas.</span></span>                                                                                               |
   |       <span data-ttu-id="6ede0-135"><strong>Sidesõna „ja” ühikute ja allühikute vahel</strong></span><span class="sxs-lookup"><span data-stu-id="6ede0-135"><strong>Conjunction 'and' between units and parts</strong></span></span>       |                                     <span data-ttu-id="6ede0-136">Märkige ruut , et printida ühikute ja allühikute vahel sidesõna „ja”.</span><span class="sxs-lookup"><span data-stu-id="6ede0-136">Select to print the conjunction “and” between the currency units and unit parts.</span></span> <span data-ttu-id="6ede0-137">Näiteks kuvatakse summa LTL 100,20 arvetel või aruannetes kui „100 Litas and 20 Centas”.</span><span class="sxs-lookup"><span data-stu-id="6ede0-137">For example, on invoices or reports, the amount for LTL 100.20 will be displayed as 100 Litas and 20 Centas.</span></span>                                      |


5. <span data-ttu-id="6ede0-138">Klõpsake käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="6ede0-138">Click **Save**.</span></span>





