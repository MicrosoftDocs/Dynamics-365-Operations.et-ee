---
title: Hinnanguprofiilid
description: Selles teemas kirjeldatakse, kuidas seadistada andmeid hinnangu gruppidele.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d359394ee0086edc5c8b9a3a0c48cf5933963ceb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828438"
---
# <a name="rating-profiles"></a><span data-ttu-id="ff8c5-103">Hinnanguprofiilid</span><span class="sxs-lookup"><span data-stu-id="ff8c5-103">Rating profiles</span></span>

<span data-ttu-id="ff8c5-104">Hinnangu profiil sarnaneb logistika lepingule (kuid mitte juriidilisele lepingule).</span><span class="sxs-lookup"><span data-stu-id="ff8c5-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="ff8c5-105">Seda kasutatakse koormate transpordi tariifide määramiseks.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="ff8c5-106">Iga hinnanguprofiil on vedaja puhul kordumatu.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="ff8c5-107">Hinnanguprofiilis seostatakse vedaja määra koondüksusega.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="ff8c5-108">Määra koondüksus defineerib määra aluse määrangu ja määra aluse.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="ff8c5-109">Määra alus määrab vedaja hinna.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="ff8c5-110">Saate seadistada hinnanguprofiili, kasutades üldist lehte, mis annab ülevaade kõigist olemasolevatest hinnanguprofiilidest.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="ff8c5-111">Alternatiivina saate seadistada hinnanguprofiili ka otse vedaja alt.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="ff8c5-112">Mõlemal juhul on hinnangu profiili jaoks seadistatud teave sama.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="ff8c5-113">Hinnangu profiili loomine või redigeerimine hinnangute profiilide lehel</span><span class="sxs-lookup"><span data-stu-id="ff8c5-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="ff8c5-114">Lehel **Hinnanguprofiilid** saate vaadata kõiki saadaolevaid hinnangu reegleid.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="ff8c5-115">Saate redigeerida ka olemasolevaid reegleid ja luua uusi profiile.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="ff8c5-116">Avage **Transpordihaldus \> Seadistus \> Hinnang \> Hinnanguprofiil**.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="ff8c5-117">Uue hinnanguprofiili lisamiseks ruudustikku valige tegumiribal nupp **Uus** või valige nupp **Redigeeri**, et redigeerida olemasolevat profiili.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="ff8c5-118">Määrake uue või olemasoleva hinnangu profiili real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="ff8c5-119">**Hinnanguprofiil** – Sisestage kordumatu identifikaator (ID) hinnanguprofiilile.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="ff8c5-120">**Nimi** – Sisestage hinnanguprofiili kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="ff8c5-121">**Saadetise vedaja** – Valige saadetise vedaja.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="ff8c5-122">Teie seadistatav hinnanguprofiil kuvatakse valitud vedaja kohta ka **Saadetise vedaja** lehel.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="ff8c5-123">**Sait** ja **Ladu** – Valige sait ja ladu.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="ff8c5-124">**Määra mootor** – Valige hinnanguprofiili määra mootor.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="ff8c5-125">**Määra koondüksus** – Valige hinnanguprofiili määra koondüksus.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="ff8c5-126">Määra koondüksuse abil saate määratleda määra aluse tüübi ja määra aluse.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="ff8c5-127">Lisateavet leiate teemast [Määra koondüksuse seadistamine](set-up-rate-masters.md).</span><span class="sxs-lookup"><span data-stu-id="ff8c5-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="ff8c5-128">**Transiidi aja mootor** – Valige hinnanguprofiili jaoks transiidi aja mootor.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="ff8c5-129">**Vedaja kütuseindeks** – Valige hinnanguprofiili jaoks vedaja kütuseindeks.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="ff8c5-130">**Teostamise alguskuupäev ja kellaaeg** ning **Teostamise lõppkuupäev ja-kellaaeg** – Määratlege periood, millal hinnanguprofiil peaks olema aktiivne.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="ff8c5-131">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="ff8c5-132">Hinnangu profiili loomine otse vedajate lehel</span><span class="sxs-lookup"><span data-stu-id="ff8c5-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="ff8c5-133">Avage jaotis **Transpordihaldus \> Seadistus \> Vedajad \> Kättetoimetajad**.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="ff8c5-134">Valige nimekirjast vedaja.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="ff8c5-135">Hinnanguprofiili loomiseks valige **Hinnanguprofiilide** FastTab-is **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="ff8c5-136">Seadistage uue hinnangu profiili väljad.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="ff8c5-137">Need väljad vastavad lehe **Hinnangu profiilid** väljadele, nagu on kirjeldatud selle teema eelmises jaotises.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="ff8c5-138">Lehel **Saadetise vedajad** loodud profiilid kuvatakse ka lehel **Hinnanguprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="ff8c5-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]