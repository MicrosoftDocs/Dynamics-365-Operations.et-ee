---
title: Varude blokeerimise loomine ja haldamine
description: Selles teemas kirjeldatakse, kuidas vältida füüsilise vaba kaubavaru reserveerimist teiste väljaminevate lähtedokumentidega, kasutades varude blokeerimist.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956154"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="e6236-103">Varude blokeerimise loomine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="e6236-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6236-104">Selles teemas kirjeldatakse, kuidas vältida füüsilise vaba kaubavaru reserveerimist teiste väljaminevate lähtedokumentidega, kasutades varude blokeerimist.</span><span class="sxs-lookup"><span data-stu-id="e6236-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="e6236-105">Enne seda teemat puudutava protseduuri alustamist peab teil olema füüsilise vaba kaubavaruga kaup saadaval.</span><span class="sxs-lookup"><span data-stu-id="e6236-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="e6236-106">Blokeeri varud</span><span class="sxs-lookup"><span data-stu-id="e6236-106">Block inventory</span></span>

<span data-ttu-id="e6236-107">Varude blokeerimise kirje loomiseks selliselt, et inventar on blokeeritud, järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="e6236-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="e6236-108">Avage **Varude haldus \> Perioodilised ülesanded \> Inventari blokeerimine**.</span><span class="sxs-lookup"><span data-stu-id="e6236-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="e6236-109">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e6236-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e6236-110">Määrake uue blokeerimiskirje päises **kaubakoodi** väli kaubale, mida soovite blokeerida, ja sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e6236-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="e6236-111">Sisestage blokeeritavate kaupade arv kiirkaardi **Üldine** väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="e6236-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="e6236-112">Kiirkaardil **Varude dimensioonid** määrake sait ja ladu, kus asuvad kaubad, mida soovite blokeerida.</span><span class="sxs-lookup"><span data-stu-id="e6236-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="e6236-113">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e6236-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="e6236-114">Varude blokeerimise tingimuste värskendamine</span><span class="sxs-lookup"><span data-stu-id="e6236-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="e6236-115">Varude blokeerimise kirje uuendamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="e6236-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="e6236-116">Avage **Varude haldus \> Perioodilised ülesanded \> Inventari blokeerimine**.</span><span class="sxs-lookup"><span data-stu-id="e6236-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="e6236-117">Valige loendipaanil asjakohane blokeerimiskirje.</span><span class="sxs-lookup"><span data-stu-id="e6236-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="e6236-118">Redigeerige kandeid nii, nagu vaja.</span><span class="sxs-lookup"><span data-stu-id="e6236-118">Edit the record as required.</span></span> <span data-ttu-id="e6236-119">Näiteks võite muuta välja **Oodatav kuupäev** väärtust näitamaks, millal blokeeritud inventar jälle reserveerimiseks vabaks antakse.</span><span class="sxs-lookup"><span data-stu-id="e6236-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="e6236-120">Kui on valitud suvand **Oodatud sissetulekud**, kuvatakse kuupäev eeldataval kandel.</span><span class="sxs-lookup"><span data-stu-id="e6236-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="e6236-121">(Välja **Eeldatud sissetulekud** suvand valitakse vaikimisi blokeeriva kirje käsitsi loomisel.)</span><span class="sxs-lookup"><span data-stu-id="e6236-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="e6236-122">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e6236-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="e6236-123">Varude blokeeringu eemaldamine</span><span class="sxs-lookup"><span data-stu-id="e6236-123">Unblock inventory</span></span>

<span data-ttu-id="e6236-124">Varude blokeerimise kirje eemaldamiseks selliselt, et inventar ei oleks enam blokeeritud, järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="e6236-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="e6236-125">Avage **Varude haldus \> Perioodilised ülesanded \> Inventari blokeerimine**.</span><span class="sxs-lookup"><span data-stu-id="e6236-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="e6236-126">Valige loendipaanil asjakohane blokeerimiskirje.</span><span class="sxs-lookup"><span data-stu-id="e6236-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="e6236-127">Valige tegumiribal suvand **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="e6236-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="e6236-128">Teil pakutakse tegevus kinnitada.</span><span class="sxs-lookup"><span data-stu-id="e6236-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="e6236-129">Jätkamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e6236-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="e6236-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e6236-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
