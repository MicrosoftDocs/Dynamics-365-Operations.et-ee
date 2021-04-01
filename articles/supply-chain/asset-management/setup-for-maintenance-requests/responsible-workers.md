---
title: Vastutavad hooldustöötajad
description: Selles teemas selgitatakse, kuidas sätestada vastutavaid hooldustöötajaid varahalduses.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad6b1757952fb0e5b970f82f75d99919a7f0745e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5261161"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="cefbb-103">Vastutavad hooldustöötajad</span><span class="sxs-lookup"><span data-stu-id="cefbb-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="cefbb-104">Vastutavad hooldustöötajad võivad olla seotud vara tüüpide, varade, funktsionaalsete asukohtade, hooldustöö tüübi kategooriate, hooldustöö tüüpide, hooldustöö tüüpide variantide ja kaubandusega.</span><span class="sxs-lookup"><span data-stu-id="cefbb-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="cefbb-105">Neid saab kasutada töökäskudel ja hooldustaotlustel, et näidata eelistust hooldustöötajate osas, kes peaksid olema töökäsu eest vastutavad.</span><span class="sxs-lookup"><span data-stu-id="cefbb-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="cefbb-106">(Kuid need hooldustöötajad ei ole tingimata samad töötajad, kellele on ette nähtud töökäsk täita.) Selle funktsiooni kasutamine on valikuline.</span><span class="sxs-lookup"><span data-stu-id="cefbb-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="cefbb-107">Näiteks saab seda kasutada, et valida vastutavad töötajad või töötajate rühmad spetsiifiliste töö tüüpide või tööalade jaoks.</span><span class="sxs-lookup"><span data-stu-id="cefbb-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="cefbb-108">Töökösu elutsükli või hooldustaotluse elutsükli jooksul saab vastutavaid hooldustöötajaid muuta või värskendada.</span><span class="sxs-lookup"><span data-stu-id="cefbb-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="cefbb-109">Muutus või värskendus võib olla seotud näiteks hooldustaotluse elutsükli oleku või töökäsu elutsükli oleku muutusega.</span><span class="sxs-lookup"><span data-stu-id="cefbb-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="cefbb-110">Häälestust lehel **Vastutavad hooldustöötajad** *ei* kasutata töökäsu planeerimise ajal.</span><span class="sxs-lookup"><span data-stu-id="cefbb-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="cefbb-111">Varahalduses saate samuti sätestada *eelistatud* hooldustöötajaid, kes võivad olla eraldatud töökäskudele töökäsu planeerimise ajal.</span><span class="sxs-lookup"><span data-stu-id="cefbb-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="cefbb-112">Enne kui saate sätestada vastutavaid hooldustöötajaid, peate sätestama töötajad ja töötajate rühmad, mis peaksid valikuks saadava olema.</span><span class="sxs-lookup"><span data-stu-id="cefbb-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="cefbb-113">Lisateavet töötajate ja töötajate rühmade sätestamiseks vt teemast [Hooldustöötajad ja töötajate rühmad](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="cefbb-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="cefbb-114">Vastutavate hooldustöötajate sätestamine</span><span class="sxs-lookup"><span data-stu-id="cefbb-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="cefbb-115">Valige **Varahaldus**\>**Häälestus**\>**Töötajad**\>**Vastutavad hooldustöötajad**.</span><span class="sxs-lookup"><span data-stu-id="cefbb-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="cefbb-116">Valige **Uus**, et luua uus kirje.</span><span class="sxs-lookup"><span data-stu-id="cefbb-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="cefbb-117">Esmalt looge vaikimisi vastutava hooldustöötaja või vastutava töötajate rühma häälestus, kus sätestate üksnes välja **Vastutav töötajate rühm** ja/või välja **Vastutav töötaja**.</span><span class="sxs-lookup"><span data-stu-id="cefbb-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="cefbb-118">Ülejäänud väljad jätke tühjaks.</span><span class="sxs-lookup"><span data-stu-id="cefbb-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="cefbb-119">Seda vaikimisi häälestust kasutatakse töökäsu planeerimisel, kui teine spetsiifilisem kombinatsioon ei vasta töökäsu sisule.</span><span class="sxs-lookup"><span data-stu-id="cefbb-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cefbb-120">Kui vastutav hooldustöötaja või vastutavate hooldustöötajate rühm on hooldustaotluse loomise käigus valikuks saadaval lehel **Kõik hooldustaotlused**, vaatab varahaldus läbi kõik vastutavad hooldustöötaja kirjed, et leida võimalik vaste.</span><span class="sxs-lookup"><span data-stu-id="cefbb-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="cefbb-121">Varahaldus kontrollib alati kõige spetsiifilisemat kombinatsiooni esimesena.</span><span class="sxs-lookup"><span data-stu-id="cefbb-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="cefbb-122">Teisisõnu kontrollib varahaldus esmalt vastet väljale **Kaubandus**.</span><span class="sxs-lookup"><span data-stu-id="cefbb-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="cefbb-123">Kui vastet ei leita, otsib see vastet väljale **Hooldustöö tüübi variant**.</span><span class="sxs-lookup"><span data-stu-id="cefbb-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="cefbb-124">Kui vastet ei leita, otsib see vastet väljale **Hooldustöö tüüp** jne.</span><span class="sxs-lookup"><span data-stu-id="cefbb-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="cefbb-125">Nagu näete lehe kujundusest, tähendab selline käitumine, et kõige spetsiifilisema kombinatsiooni leidmiseks otsib varahaldus kirjeid vaste leidmiseks paremalt vasakule (esmalt **Kaubandus**, seejärel **Hooldustöö tüübi variant**, seejäel **Hooldustöö tüüp**, seejärel **Hooldustöö tüübi kategooria**, seejärel **Funktsionaalne asukoht**, seejärel **Vara** ja viimaks **Vara tüüp**).</span><span class="sxs-lookup"><span data-stu-id="cefbb-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="cefbb-126">Kui vastet ei leita, kasutatakse vaikimisi kirjet, mille valikutes pole kasutatud ühtegi neist väljast.</span><span class="sxs-lookup"><span data-stu-id="cefbb-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="cefbb-127">Järgnev illustratsioon näitab lehe **Vastutavad hooldustöötajad** näidet.</span><span class="sxs-lookup"><span data-stu-id="cefbb-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![Vastutavate hooldustöötajate leht](media/08-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]