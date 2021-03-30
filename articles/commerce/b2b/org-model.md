---
title: B2B organisatsioonidele organisatsiooni modelleerimise hierarhiate loomine.
description: Selles teemas kirjeldatakse, kuidas luua organisatsioonilised modelleerimishierarhiad ettevõtetevahelistele (B2B) organisatsioonidele.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 91cb01637faa69bd3c7fefefae69c60cb948510e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211221"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="f7cda-103">B2B organisatsioonidele organisatsiooni modelleerimise hierarhiate loomine.</span><span class="sxs-lookup"><span data-stu-id="f7cda-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7cda-104">Selles teemas kirjeldatakse, kuidas luua organisatsioonilised modelleerimishierarhiad ettevõtetevahelistele (B2B) organisatsioonidele rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f7cda-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f7cda-105">Äripartneri organisatsioone esindavad Commerce'i peakontoris klient ja kliendi hierarhia üksused.</span><span class="sxs-lookup"><span data-stu-id="f7cda-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="f7cda-106">Äripartneri organisatsioon ja selle kasutajad on esindatud klientidena ning kliendihierarhiaid kasutatakse nende klientide üksteisega seostamiseks.</span><span class="sxs-lookup"><span data-stu-id="f7cda-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="f7cda-107">Kui äripartneri taotlus B2B e-kaubanduse saidiga liitumiseks kinnitatakse, sooritatakse järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="f7cda-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="f7cda-108">Süsteemis luuakse kaks uut kliendikirjet: kliendikirje **Tüüp Organisatsioon** äripartneri organisatsioonile ja kliendikirje **Tüüp Isik** taotlejale (see on äripartneri kasutaja, kes taotluse esitas).</span><span class="sxs-lookup"><span data-stu-id="f7cda-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="f7cda-109">Uus kliendi hierarhia kirje luuakse jaotisesse **Klient \> Kliendi hierarhia**.</span><span class="sxs-lookup"><span data-stu-id="f7cda-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="f7cda-110">Kirjel on järgmised päise atribuudid.</span><span class="sxs-lookup"><span data-stu-id="f7cda-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="f7cda-111">**Kliendi hierarhia ID** - kliendi hierarhia kordumatu ID.</span><span class="sxs-lookup"><span data-stu-id="f7cda-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="f7cda-112">See ID kasutab numbriseeriat, mis on määratletud Commerce'i peakontori ühisparameetrites Commerce'i peakontoris.</span><span class="sxs-lookup"><span data-stu-id="f7cda-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="f7cda-113">**Nimi** - äripartneri organisatsiooni nimi, nagu on määratletud liitumistaotluses.</span><span class="sxs-lookup"><span data-stu-id="f7cda-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="f7cda-114">**Eesmärk** - see atribuut on seadistatud eelmääratletud väärtusele **B2B organisatsioon**.</span><span class="sxs-lookup"><span data-stu-id="f7cda-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="f7cda-115">**Organisatsioon** - äripartneri kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="f7cda-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="f7cda-116">Siin on kliendi hierarhia kirje üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="f7cda-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="f7cda-117">Taotleja kliendikirje on seotud kliendi hierarhiaga.</span><span class="sxs-lookup"><span data-stu-id="f7cda-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="f7cda-118">Administraatori roll on seotud taotlejaga.</span><span class="sxs-lookup"><span data-stu-id="f7cda-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="f7cda-119">Kui administraator lisab äripartneri organisatsioonile B2B-saidil veel kasutajaid, luuakse Commerce'i peakontoris igale loodud kasutajale uus kliendikirje.</span><span class="sxs-lookup"><span data-stu-id="f7cda-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="f7cda-120">See kliendikirje lisatakse ka äripartneri vastavale kliendi hierarhia kirjele ja sellel on roll "Kasutaja".</span><span class="sxs-lookup"><span data-stu-id="f7cda-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="f7cda-121">Enamasti peaksid hierarhia kõigi kliendikirjete vastavad atribuudi väärtused ühtima.</span><span class="sxs-lookup"><span data-stu-id="f7cda-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="f7cda-122">Näiteks, kuna kõik äripartneri kasutajad peaksid saama toodetele sarnaseid hindu, peavad nende hinnagrupp ja seotud konfiguratsioonid ühtima.</span><span class="sxs-lookup"><span data-stu-id="f7cda-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="f7cda-123">Süsteem ei jõusta siiski seda ühtsust.</span><span class="sxs-lookup"><span data-stu-id="f7cda-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="f7cda-124">Seetõttu vastutavad asjakohased Commerce'i peakontori kasutajad selle eest, et atribuudi väärtused ja konfiguratsioonid ühtiksid kõigi antud hierarhia klientidega.</span><span class="sxs-lookup"><span data-stu-id="f7cda-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="f7cda-125">Commerce peakontori kasutajad saavad hierarhia kõikide kliendikirjete atribuudi väärtusi vaadata kõrvuti vaates.</span><span class="sxs-lookup"><span data-stu-id="f7cda-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="f7cda-126">Valige soovitud kliendikirje atribuudid, valides rippmenüüst vahekaardi nimed.</span><span class="sxs-lookup"><span data-stu-id="f7cda-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="f7cda-127">Kasutajad saavad selle vaate kaudu otse atribuudi väärtusi vaadata ja redigeerida.</span><span class="sxs-lookup"><span data-stu-id="f7cda-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="f7cda-128">Teise võimalusena, kui soovite kõik administraatori kliendikirje väärtused rakendada ka kõigile kasutaja kliendikirjetele, valige kliendi hierarhia üksikasjade all valik **Alistamine**.</span><span class="sxs-lookup"><span data-stu-id="f7cda-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7cda-129">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f7cda-129">Additional resources</span></span>

[<span data-ttu-id="f7cda-130">B2B e-kaubanduse saidi seadistamine</span><span class="sxs-lookup"><span data-stu-id="f7cda-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="f7cda-131">Äripartnerist kasutajate haldamine B2B e-kaubanduse saitidel</span><span class="sxs-lookup"><span data-stu-id="f7cda-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="f7cda-132">Kliendikonto makseviisi konfigureerimine B2B e-kaubanduse saitide jaoks</span><span class="sxs-lookup"><span data-stu-id="f7cda-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="f7cda-133">Toote koguse piirangute määramine B2B e-kaubanduse saitide jaoks</span><span class="sxs-lookup"><span data-stu-id="f7cda-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]