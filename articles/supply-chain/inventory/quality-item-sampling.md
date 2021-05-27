---
title: Kvaliteedijuhtimise kauba valim
description: Selles teemas kirjeldatakse, kuidas seadistada kauba valimeid.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022224"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="1ead4-103">Kvaliteedijuhtimise kauba valim</span><span class="sxs-lookup"><span data-stu-id="1ead4-103">Quality management item sampling</span></span>

<span data-ttu-id="1ead4-104">Kauba valimit kasutatakse kvaliteediseose osana.</span><span class="sxs-lookup"><span data-stu-id="1ead4-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="1ead4-105">See määratleb praeguse füüsilise laovaru summa, mida tuleb kontrollida.</span><span class="sxs-lookup"><span data-stu-id="1ead4-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="1ead4-106">Valimi aluseks võib olla fikseeritud kogus, protsent või terve litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="1ead4-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="1ead4-107">Kauba valimi seadistamine</span><span class="sxs-lookup"><span data-stu-id="1ead4-107">Set up item sampling</span></span>

<span data-ttu-id="1ead4-108">Kauba valimi seadistamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="1ead4-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="1ead4-109">Avage **Varude haldus \> Seadistus \> Kvaliteedijuhtimine \> Kauba valim**.</span><span class="sxs-lookup"><span data-stu-id="1ead4-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="1ead4-110">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1ead4-110">Select **New**.</span></span>
1. <span data-ttu-id="1ead4-111">Sisestage väärtus väljale **Kauba valim**.</span><span class="sxs-lookup"><span data-stu-id="1ead4-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="1ead4-112">Sisestage väärtus väljal **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="1ead4-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="1ead4-113">Sisestage arv väljale **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="1ead4-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="1ead4-114">See väärtus on seotud külgneval väljal valitud koguse spetsifikatsiooni väärtusega.</span><span class="sxs-lookup"><span data-stu-id="1ead4-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="1ead4-115">Jaotises **Protsess** valige märkeruut **Täielik blokeerimine**, kui testi ebaõnnestumisel tuleks kogu partii või tellimisrea kogus blokeerida.</span><span class="sxs-lookup"><span data-stu-id="1ead4-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="1ead4-116">Kui see ruut tühjendatakse, blokeeritakse testi ebaõnnestumisel ainult kvaliteeditellimuses olevad kaubad.</span><span class="sxs-lookup"><span data-stu-id="1ead4-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="1ead4-117">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="1ead4-117">Select **Save**.</span></span>
1. <span data-ttu-id="1ead4-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1ead4-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="1ead4-119">Funktsioon *Kvaliteedijuhtimine laoprotsesside jaoks* pakub täiendavaid kauba valimi määramise võimalusi.</span><span class="sxs-lookup"><span data-stu-id="1ead4-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="1ead4-120">See lisab *Kauba valimi ulatus* kontseptsiooni ja võimaldab määratleda koguse spetsifikatsioonina täieliku litsentsi plaadi.</span><span class="sxs-lookup"><span data-stu-id="1ead4-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="1ead4-121">Kui olete selle funktsiooni lubanud, vaadake jaotist [Kvaliteedijuhtimine laoprotsesside jaoks](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="1ead4-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
