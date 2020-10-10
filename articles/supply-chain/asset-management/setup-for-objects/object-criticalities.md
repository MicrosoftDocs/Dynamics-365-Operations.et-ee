---
title: Varade kriitilisuse tüübid
description: Teemas selgitatakse varade kriitilisuse tüüpe varahalduses.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b7d6e3dea1b3c1ef47490df678f639c036cdd5c
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889813"
---
# <a name="asset-criticality-types"></a><span data-ttu-id="b1e61-103">Varade kriitilisuse tüübid</span><span class="sxs-lookup"><span data-stu-id="b1e61-103">Asset criticality types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b1e61-104">Teemas selgitatakse varade kriitilisuse tüüpe varahalduses.</span><span class="sxs-lookup"><span data-stu-id="b1e61-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="b1e61-105">Varade kriitilisus on seotud varaga ja kantakse töötellimustele üle.</span><span class="sxs-lookup"><span data-stu-id="b1e61-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="b1e61-106">Töötellimuse puhul ei saa seda muuta.</span><span class="sxs-lookup"><span data-stu-id="b1e61-106">It can't be changed on a work order.</span></span> <span data-ttu-id="b1e61-107">Varade kriitilisust kasutatakse töökäsu kriitilisuse arvutamiseks töötellimuse planeerimisel.</span><span class="sxs-lookup"><span data-stu-id="b1e61-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="b1e61-108">Teisisõnu kasutatakse seda arvutamiseks, millises ulatuses mõjutab vara hooldustöö tootmisgraafikut ja tootlikkust teie ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="b1e61-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="b1e61-109">Lisateabe saamiseks häälestuse kohta, mis on seotud töötellimuse planeerimisel reitingusummade arvutamisega, vt teemat [Varahalduse parameetrid](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b1e61-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="b1e61-110">Kriitilisuse seadistamiseks looge esmalt kriitilisuse tüübid, mida tuleks kasutada vara seadistuses.</span><span class="sxs-lookup"><span data-stu-id="b1e61-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="b1e61-111">Seejärel seadistage vara kriitilisused.</span><span class="sxs-lookup"><span data-stu-id="b1e61-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="b1e61-112">Kriitilisuse tüüpide häälestamine</span><span class="sxs-lookup"><span data-stu-id="b1e61-112">Set up criticality types</span></span>

1. <span data-ttu-id="b1e61-113">Valige **Varadehaldus**\>**Häälestus**\>**Varad** \>**Kriitilisuse tüübid**.</span><span class="sxs-lookup"><span data-stu-id="b1e61-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="b1e61-114">Valige **Uus**, et luua uus kirje.</span><span class="sxs-lookup"><span data-stu-id="b1e61-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="b1e61-115">Väljale **Kriitilisus** sisestage number, mis näitab kriitilisust.</span><span class="sxs-lookup"><span data-stu-id="b1e61-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="b1e61-116">Väljale **Nimi** sisestage kriitilisuse tüübi nimi.</span><span class="sxs-lookup"><span data-stu-id="b1e61-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="b1e61-117">Väljale **Tegur** sisestage tegur.</span><span class="sxs-lookup"><span data-stu-id="b1e61-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="b1e61-118">Seda tegurit kasutatakse töökäsu plaanimise arvutamisel, et määrata kriitilisuse kirje, mida tuleks kasutada.</span><span class="sxs-lookup"><span data-stu-id="b1e61-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="b1e61-119">(Suurima teguriga kirjet kasutatakse alati.) See säte on asjakohane, juhul kui nagu on näidatud järgmisel joonisel, luuakse kriitilisuse read, millel on sama kriitilisuse väärtus.</span><span class="sxs-lookup"><span data-stu-id="b1e61-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![Kriitilisuse tüüpide leht](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="b1e61-121">Vara kriitilisuse häälestus</span><span class="sxs-lookup"><span data-stu-id="b1e61-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="b1e61-122">Valige **Varahaldus**\>**Häälestus**\>**Vara kriitilisus**.</span><span class="sxs-lookup"><span data-stu-id="b1e61-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="b1e61-123">Valige **Uus**, et luua uus kirje.</span><span class="sxs-lookup"><span data-stu-id="b1e61-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="b1e61-124">Sõltuvalt varade kriitilisuse nõutavast üksikasjade tasemest tehke asjakohased valikud väljadel **Funktsionaalne asukoht**, **Vara liik**, **Tootja**, **Mudel**, **Vara**, **Töö tüübi kategooria**, **Töö tüüp**, **Töö tüübi variant** ja **Töö vajadus**.</span><span class="sxs-lookup"><span data-stu-id="b1e61-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b1e61-125">Varade kriitilisuse valimisel vaatab varahaldus läbi kõik vara kriitilisuse kirjed, et kontrollida võimalikku vastet.</span><span class="sxs-lookup"><span data-stu-id="b1e61-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="b1e61-126">Varahaldus kontrollib alati kõige spetsiifilisemat kombinatsiooni esimesena.</span><span class="sxs-lookup"><span data-stu-id="b1e61-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="b1e61-127">Teisisõnu kontrollib varahaldus esmalt **Töö nõuet**.</span><span class="sxs-lookup"><span data-stu-id="b1e61-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="b1e61-128">Kui vastet ei leita, kontrollib see **Töö tüübi varianti**.</span><span class="sxs-lookup"><span data-stu-id="b1e61-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="b1e61-129">Kui vastet ei leita, kontrollib see **Töö tüübi** ja nii edasi.</span><span class="sxs-lookup"><span data-stu-id="b1e61-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="b1e61-130">Nagu näete lehe paigutuses, tähendab see käitumine, et kõige spetsiifilisema kombinatsiooni leidmiseks kontrollib varahaldus vaste leidmiseks iga kirjet paremalt vasakule.</span><span class="sxs-lookup"><span data-stu-id="b1e61-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="b1e61-131">Kui vastet ei leita, kasutatakse „vaikimisi“ kirjet, mille kohta pole valikuid tehtud.</span><span class="sxs-lookup"><span data-stu-id="b1e61-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="b1e61-132">Väljal **Kriitilisus** valige üks kriitilisuse väärtustest, mille olete eelneva protsessi käigus loonud.</span><span class="sxs-lookup"><span data-stu-id="b1e61-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="b1e61-133">Märkused kriitilisuse seadistuse kohta</span><span class="sxs-lookup"><span data-stu-id="b1e61-133">Notes about criticality setup</span></span>

- <span data-ttu-id="b1e61-134">Kui muudate selles seadistuses vara kriitilisust pärast seda, kui olete seda töökäsul juba kasutanud, ei värskendata selle töökäsu kriitilisust vastavalt.</span><span class="sxs-lookup"><span data-stu-id="b1e61-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="b1e61-135">Töökäsu kriitilisus arvutatakse ümber iga kord, kui töökäsu rida lisatakse või kustutatakse töökäsult.</span><span class="sxs-lookup"><span data-stu-id="b1e61-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="b1e61-136">Kui töökäsk sisaldab mitut töökäsu tööd, kasutatakse töökäsu puhul alati kõrgeimat kriitilisust vastavalt väljale **Faktor** lehel **Kriitilisuse tüübid**.</span><span class="sxs-lookup"><span data-stu-id="b1e61-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="b1e61-137">Üldiselt võib vara kriitilisus perioodi jooksul muutuda.</span><span class="sxs-lookup"><span data-stu-id="b1e61-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="b1e61-138">Kriitilisust võivad mõjutada uute seadmete ostmine, renoveerimine jne.</span><span class="sxs-lookup"><span data-stu-id="b1e61-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="b1e61-139">Kaaluge oma varade kriitilisuse ümberhindamist regulaarsete ajavahemike järel (näiteks kord aastas või igal teisel aastal), et veenduda, kas teie kriitilisuse määratlused vastavad teie praegusele tootmisseadistusele.</span><span class="sxs-lookup"><span data-stu-id="b1e61-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>
