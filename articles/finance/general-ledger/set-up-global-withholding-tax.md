---
title: Globaalse kinnipeetava maksu häälestus
description: Selles teemas loetletakse müügi ja ostude globaalse kinnipeetava maksu seadistamise sammud.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 00c472e90f4926c52ffe9b19661e68cbfa6bd493
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204829"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="9ecbe-103">Globaalse kinnipeetava maksu häälestus</span><span class="sxs-lookup"><span data-stu-id="9ecbe-103">Set up global withholding tax</span></span>

<span data-ttu-id="9ecbe-104">Selles teemas loetletakse müügi ja ostude globaalse kinnipeetava maksu seadistamise sammud.</span><span class="sxs-lookup"><span data-stu-id="9ecbe-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="9ecbe-105">Kinnipeetava maksu haldurite seadistamine lehel **Kinnipeetava maksu haldurid**.</span><span class="sxs-lookup"><span data-stu-id="9ecbe-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="9ecbe-106">Kinnihoitava makse perioodide seadistamine lehel **Kinnipeetava maksu tasumise perioodid**.</span><span class="sxs-lookup"><span data-stu-id="9ecbe-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="9ecbe-107">Kinnipeetava pearaamatu sisestusgrupi seadistamine lehel **Kinnipeetav maks > Pearaamatu sisestusgrupp**.</span><span class="sxs-lookup"><span data-stu-id="9ecbe-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="9ecbe-108">**Kinnipeetava maksu** konto määratakse põhikontoga koos kinnipeetava maksu **Sisestustüübiga**.</span><span class="sxs-lookup"><span data-stu-id="9ecbe-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="9ecbe-109">**Kinnipeetava maksu vastaskonto** määratakse samuti põhikontoga koos **Sisestustüübiga** "Kinnipeetava maksu vastaskonto".</span><span class="sxs-lookup"><span data-stu-id="9ecbe-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="9ecbe-110">Avage **Pearaamat > Kontoplaan > Kontod > Põhikontod**, seadistage **Sisestustüüp** põhikontode alamvormil **Sisestuse kontrollimine**.</span><span class="sxs-lookup"><span data-stu-id="9ecbe-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="9ecbe-111">Kinnipeetava maksu koodide seadistamine lehel **Kinnipeetava maksu koodid**.</span><span class="sxs-lookup"><span data-stu-id="9ecbe-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="9ecbe-112">Kinnipeetava maksu gruppide seadistamine lehel **Kinnipeetava maksu grupid**.</span><span class="sxs-lookup"><span data-stu-id="9ecbe-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="9ecbe-113">Seadistage kinnipeetava maksu tulu tüübid lehel **Kinnipeetava maksu tulu** **tüübid**.</span><span class="sxs-lookup"><span data-stu-id="9ecbe-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="9ecbe-114">Kinnipeetava maksu gruppide seadistamine kauba või teenuse lehel **Üksus kinnipeetava maksu grupid**.</span><span class="sxs-lookup"><span data-stu-id="9ecbe-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="9ecbe-115">Seadistage **Minimaalne arve summa** lehel **Pearaamatu parameetrid > Kinnipeetav maks**.</span><span class="sxs-lookup"><span data-stu-id="9ecbe-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]