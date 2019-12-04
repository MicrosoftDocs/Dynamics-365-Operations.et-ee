---
title: Valige teenindustase.
description: Selles teemas selgitatakse vara teenindustasemeid varahalduses.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6dad0cb480f69eac84df5ea9a67f2adb94e2f52c
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811799"
---
# <a name="asset-service-levels"></a><span data-ttu-id="e8302-103">Valige teenindustase.</span><span class="sxs-lookup"><span data-stu-id="e8302-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e8302-104">Selles teemas selgitatakse vara teenindustasemeid varahalduses.</span><span class="sxs-lookup"><span data-stu-id="e8302-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="e8302-105">Vara teenindustasemed on seotud varadega ja need kantakse üle hooldustaotlustele ja töökäskudele.</span><span class="sxs-lookup"><span data-stu-id="e8302-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="e8302-106">Neid kasutatakse töökäskude prioriteedi arvutamiseks töökäsu planeerimisel.</span><span class="sxs-lookup"><span data-stu-id="e8302-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="e8302-107">Vara teenindustasemeid saab vajaduse korral muuta.</span><span class="sxs-lookup"><span data-stu-id="e8302-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="e8302-108">Lisateabe saamiseks häälestuse kohta, mis on seotud töötellimuse planeerimisel reitingusummade arvutamisega, vt teemat [Varahalduse parameetrid](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e8302-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="e8302-109">Peate seadistama vähemalt ühe vaikekirje vara teenindustaseme jaoks.</span><span class="sxs-lookup"><span data-stu-id="e8302-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="e8302-110">Seda vaikekirjet kasutatakse juhul, kui töökäsu planeerimisel ei leita muud vastet.</span><span class="sxs-lookup"><span data-stu-id="e8302-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="e8302-111">**Näide 1:** vaikimisi teenindustase, mida kasutatakse, kui ühtegi muud vastet ei leita.</span><span class="sxs-lookup"><span data-stu-id="e8302-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="e8302-112">Selles kirjes saate valida ainult teenuse taseme.</span><span class="sxs-lookup"><span data-stu-id="e8302-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="e8302-113">**Näide 2:** kõrge teenindustase, mida kasutatakse Volvo veoauto mootori tööde planeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="e8302-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="e8302-114">Selles kirjes saate valida vastava vara tüübi (nt **veoauto mootor mootor**), tootja (**Volvo**) ja teenindustaseme.</span><span class="sxs-lookup"><span data-stu-id="e8302-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="e8302-115">Vara teenindustasemete seadistus</span><span class="sxs-lookup"><span data-stu-id="e8302-115">Set up asset service levels</span></span>

1. <span data-ttu-id="e8302-116">Valige **Varahaldus**\>**Häälestus**\>**Teenindustasemed**.</span><span class="sxs-lookup"><span data-stu-id="e8302-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="e8302-117">Valige **Uus**, et luua uus kirje.</span><span class="sxs-lookup"><span data-stu-id="e8302-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="e8302-118">Sõltuvalt vara teenindustaseme üksikasjalikkuse tasemest tehke asjakohased valikud väljadel **Funktsionaalne asukoht**, **Vara tüüp**, **Tootja**, **Mudel**, **Vara**, **Töökäsu tüüp** ja **Teenindustase**.</span><span class="sxs-lookup"><span data-stu-id="e8302-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e8302-119">Kui hooldustaotluste ja töökäskude puhul kasutatakse vara teenindustaset, vaatab varahaldus võimaliku vaste leidmiseks läbi kõik varade teenindustaseme kirjed.</span><span class="sxs-lookup"><span data-stu-id="e8302-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="e8302-120">Varahaldus kontrollib alati kõige spetsiifilisemat kombinatsiooni esimesena.</span><span class="sxs-lookup"><span data-stu-id="e8302-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="e8302-121">Teisisõnu kontrollib varahaldus esmalt **Töökäsu tüüp** väli.</span><span class="sxs-lookup"><span data-stu-id="e8302-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="e8302-122">Kui vastet ei leita, kontrollib see vastet väljale **Vara**.</span><span class="sxs-lookup"><span data-stu-id="e8302-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="e8302-123">Nagu näete lehe **Varahaldus** paigutuses, tähendab see käitumine, et kõige spetsiifilisema kombinatsiooni leidmiseks kontrollib varahaldus vaste leidmiseks iga kirjet paremalt vasakule.</span><span class="sxs-lookup"><span data-stu-id="e8302-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="e8302-124">Kui vastet ei leita, kasutatakse vaikimisi kirjet, mille valikutes pole kasutatud ühtegi neist seitsmest väljast.</span><span class="sxs-lookup"><span data-stu-id="e8302-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="e8302-125">Valige **väljal** hooldustase teenuse tase, mis näitab päringu kiireloomulisust.</span><span class="sxs-lookup"><span data-stu-id="e8302-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="e8302-126">Kui muudate vara teenindustaseme kirjet lehel **Vara teenindustase** pärast seda, kui olete seda töökäsul juba kasutanud, ei värskendata seda teenindustaset hooldustaotlustel ja töökäskudel vastavalt.</span><span class="sxs-lookup"><span data-stu-id="e8302-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>
