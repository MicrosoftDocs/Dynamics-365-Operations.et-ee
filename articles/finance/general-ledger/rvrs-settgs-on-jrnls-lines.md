---
title: Storno seaded töölehtedel ja ridadel
description: Selles teemas käsitletakse, miks üldisele töölehele sisestatud stornokannet ei pruugi olla kaasatud sisestatud kandesse.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028558"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="4430a-103">Storno seaded töölehtedel ja ridadel</span><span class="sxs-lookup"><span data-stu-id="4430a-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4430a-104">Selles teemas käsitletakse, miks üldisele töölehele sisestatud stornokannet ei pruugi olla kaasatud sisestatud kandesse.</span><span class="sxs-lookup"><span data-stu-id="4430a-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="4430a-105">Sümptom</span><span class="sxs-lookup"><span data-stu-id="4430a-105">Symptom</span></span>

<span data-ttu-id="4430a-106">Päevane tööleht sisaldab stornokannet ja tühistuskuupäeva töölehel.</span><span class="sxs-lookup"><span data-stu-id="4430a-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="4430a-107">Töölehe sisestamisel ei tühistata ühtki kannet.</span><span class="sxs-lookup"><span data-stu-id="4430a-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="4430a-108">Miks see juhtub?</span><span class="sxs-lookup"><span data-stu-id="4430a-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="4430a-109">Lahendus</span><span class="sxs-lookup"><span data-stu-id="4430a-109">Resolution</span></span>

<span data-ttu-id="4430a-110">Töölehe sisestamisel vaatab tühistamisprotsess ainult kande jaotise **Read** seadeid **Stornokanne** ja **Tühistamiskuupäev**.</span><span class="sxs-lookup"><span data-stu-id="4430a-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="4430a-111">See lähenemine võimaldab töölehele lisada mõned kanded, mis on märgitud tühistamiseks, ja teised, mis pole.</span><span class="sxs-lookup"><span data-stu-id="4430a-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="4430a-112">Töölehe väärtusi kasutatakse vaikeväärtustena ainult *uute* ridade lisamisel.</span><span class="sxs-lookup"><span data-stu-id="4430a-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="4430a-113">Väärtuste muutmine töölehel ei mõjuta olemasolevaid ridu.</span><span class="sxs-lookup"><span data-stu-id="4430a-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="4430a-114">Selles näites sisestati esmalt kanderead.</span><span class="sxs-lookup"><span data-stu-id="4430a-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="4430a-115">Kui sisestate rea üksikasjad enne töölehe tühistatavaks määramist, ei kohaldata stornokandeks ja tühistamiskuupäevaks määramist ühelegi olemasolevale reale.</span><span class="sxs-lookup"><span data-stu-id="4430a-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="4430a-116">Stornokande või tühistamiskuupäeva muutmisel olemasoleval real rakendatakse see muudatus ka sama kande muudele ridadele.</span><span class="sxs-lookup"><span data-stu-id="4430a-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="4430a-117">Jõudluse optimeerimiseks ei värskendata ruudustikku pärast muudatuste rakendamist muudele ridadele.</span><span class="sxs-lookup"><span data-stu-id="4430a-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="4430a-118">Uuendatud väärtusi saab kuvada ruudustiku värskendamisega.</span><span class="sxs-lookup"><span data-stu-id="4430a-118">You can display the updated values by refreshing the grid.</span></span>


