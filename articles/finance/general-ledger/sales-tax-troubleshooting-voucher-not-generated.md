---
title: Kviitungit pole loodud
description: See teema pakub tõrkeotsingu teavet, mis võib aidata, kui kviitung peaks loodama, aga ei looda.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ba23b597b1d7d283b99638fb7d5d91da00afb09c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018753"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="4f745-103">Kviitungit pole loodud</span><span class="sxs-lookup"><span data-stu-id="4f745-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f745-104">Kui kviitung tuleb luua, kuid **Kviitungi kande** leht ei näita ühtegi kviitungit, järgige selle probleemi tõrkeotsinguks vajalikke etappe järgmistes jaotistes.</span><span class="sxs-lookup"><span data-stu-id="4f745-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="4f745-105">[![Kviitungite kandeleht kus pole kviitungeid](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="4f745-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="4f745-106">Kontrollige maksu kohaldatavust</span><span class="sxs-lookup"><span data-stu-id="4f745-106">Check the tax applicability</span></span>

1. <span data-ttu-id="4f745-107">Mine **Maks** \> **Perioodilised ülesanded** \> **Arveraamatu alamtöölehe kirjeid pole veel üle kantud**.</span><span class="sxs-lookup"><span data-stu-id="4f745-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="4f745-108">Kui päevaraamatu kirje on olemas, valige see ja seejärel valige **Kanna kohe üle**.</span><span class="sxs-lookup"><span data-stu-id="4f745-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="4f745-109">[![Kanna üle nupp Arveraamatu alamtöölehe kanded ei ole veel üle kantud leht](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="4f745-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="4f745-110">Avage **Kviitungi kanded** leht uuesti, et näha, kas kviitung loodi.</span><span class="sxs-lookup"><span data-stu-id="4f745-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="4f745-111">Kohanduse olemasolu tuvastamine</span><span class="sxs-lookup"><span data-stu-id="4f745-111">Determine whether customization exists</span></span>

<span data-ttu-id="4f745-112">Kui olete eelmistes jaotistes kirjeldatud toimingud teinud, kuid pole probleemi lahendada õnnestunud, tehke kindlaks, kas kohandamine on võimalik.</span><span class="sxs-lookup"><span data-stu-id="4f745-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="4f745-113">Kui kohandust ei ole, looge Microsofti teenusetaotlus edasise toe saamiseks.</span><span class="sxs-lookup"><span data-stu-id="4f745-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
