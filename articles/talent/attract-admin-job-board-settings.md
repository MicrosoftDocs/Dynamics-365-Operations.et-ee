---
title: Luba Broadbeani integreerimine rakenduses Microsoft Dynamics 365 for Talent - Attract
description: Selles teemas selgitatakse, kuidas konfigureerida Microsoft Dynamics 365 for Talent - Attract postitama töid välistele töölaudadele (nt Broadbean).
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 2334c2bd0edccf3000f8d91651afafd4619ad0b8
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739675"
---
# <a name="enable-broadbean-integration"></a><span data-ttu-id="dc9d1-103">Luba Broadbeani integreerimine</span><span class="sxs-lookup"><span data-stu-id="dc9d1-103">Enable Broadbean integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="dc9d1-104">Soovite, et teave teie vabadest ametikohtadest jõuaks võimalikult paljude kvalifitseeritud kandidaatideni.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="dc9d1-105">Värbamissaidid nagu Broadbean aitavad teil seda eesmärki saavutada.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="dc9d1-106">Microsoft Dynamics 365 for Talent: Attract võimaldab teil töökuulutusi Broadbeani sisestada ja Microsoft teeb selles vallas pidevalt uusi pakkumisi.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-106">Microsoft Dynamics 365 for Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="dc9d1-107">Töökuulutuste sisestamiseks välistele veebisaitidele peab teil olema [tervikliku värbamise lisandmoodul](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="dc9d1-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="dc9d1-108">Tööde sisestamiseks Broadbeani Attracti kaudu peab teil olema Broadbeani kordustellimus.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="dc9d1-109">See funktsioon on praegu eelvaateversioonis.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-109">This feature is currently in preview.</span></span> <span data-ttu-id="dc9d1-110">Kui soovite seda proovida, peate [selle sisse lülitama Attracti administraatori sätetega](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="dc9d1-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="dc9d1-111">Broadbeani integreerimise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="dc9d1-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="dc9d1-112">Attracti administraatorina sisse logimine.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="dc9d1-113">Valige lehe paremast ülanurgast nupp **Sätted** (hammasrattasümbol) ja seejärel valige **Administreerimiskeskus**.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="dc9d1-114">Looge Broadbeaniga ühendus ja sisestage oma andmed väljadele **Kasutajanimi**, **Kliendi ID** ja **Krüptimise luba**.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="dc9d1-115">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="dc9d1-116">Teie Broadbeani mandaadid on tundlikud ja konfidentsiaalsed.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="dc9d1-117">Seega talletage ja jagage neid vastutustundlikult.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="dc9d1-118">Mandaadid on nähtavad kõigile, kellel on Attractis administraatori roll.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="dc9d1-119">Microsoft ja Attract ei ole nende väärtuste loomise ning haldamisega seotud.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="dc9d1-120">Mandaatide Attractis ajakohasena hoidmine ja nendega seotud võimalike probleemide lahendamine Broadbeanis on teie vastutus.</span><span class="sxs-lookup"><span data-stu-id="dc9d1-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>