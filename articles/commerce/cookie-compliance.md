---
title: Küpsise vastavus
description: Selles teemas kirjeldatakse küpsise vastavuse ja Microsoft Dynamics 365 Commerce'is sisalduva vaikepoliitika kaalutlusi.
author: BrianShook
manager: annbe
ms.date: 06/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e1fa016dc9f46b048220f0f83e4b0783087de91e
ms.sourcegitcommit: c66c4c67a21e7d7d3a94a3fd766c3184b6e65c4e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/12/2020
ms.locfileid: "3446909"
---
# <a name="cookie-compliance"></a><span data-ttu-id="03b26-103">Küpsise vastavus</span><span class="sxs-lookup"><span data-stu-id="03b26-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="03b26-104">Selles teemas kirjeldatakse küpsise vastavuse ja Microsoft Dynamics 365 Commerce'is sisalduva vaikepoliitika kaalutlusi.</span><span class="sxs-lookup"><span data-stu-id="03b26-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="03b26-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="03b26-105">Overview</span></span>

<span data-ttu-id="03b26-106">Privaatsus on oluline tegur, kui e-kaubanduse kliente mõjutavad jälgimistehnoloogiad.</span><span class="sxs-lookup"><span data-stu-id="03b26-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="03b26-107">Eraelu puutumatuse standardite, nagu üldise andmekaitse määruse (GDPR) tõttu Euroopa Liidus (EL), tuleb arvesse võtta elektroonilisi privaatsuspõhimõtted, mis on tänapäeval aktiivsed.</span><span class="sxs-lookup"><span data-stu-id="03b26-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="03b26-108">Kuna paljud e-kaubanduse saidid on globaalselt juurdepääsetavad vaikimisi, on oluline vaadata üle oma e-kaubanduse saidi vastavuse standardid.</span><span class="sxs-lookup"><span data-stu-id="03b26-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="03b26-109">Lisateavet Microsoft kasutavate üldpõhimõtete kohta leiate [Microsofti usalduskeskusest.](https://www.microsoft.com/trust-center)</span><span class="sxs-lookup"><span data-stu-id="03b26-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="03b26-110">Sellel saidil saate ka lisateavet vastavuse ja privaatsuse valdkondade kohta.</span><span class="sxs-lookup"><span data-stu-id="03b26-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="03b26-111">Järgmises tabelis on toodud Dynamics 365 Commerce'i saitide asetatud küpsiste kehtiv viiteloend.</span><span class="sxs-lookup"><span data-stu-id="03b26-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="03b26-112">Küpsise nimi</span><span class="sxs-lookup"><span data-stu-id="03b26-112">Cookie name</span></span>                               | <span data-ttu-id="03b26-113">Kasutus</span><span class="sxs-lookup"><span data-stu-id="03b26-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="03b26-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="03b26-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="03b26-115">Talletage Microsoft Azure Active Directory (Azure AD) autentimisküpsised ühekordse sisselogimise (SSO) jaoks.</span><span class="sxs-lookup"><span data-stu-id="03b26-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="03b26-116">Talletab kasutaja kohta krüptitud põhiteavet (nimi, perekonnanimi, e-post).</span><span class="sxs-lookup"><span data-stu-id="03b26-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="03b26-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="03b26-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="03b26-118">Talletab ostukorvi ID, mida kasutatakse ostukorvi eksemplari lisatud toodete loendi hankimiseks.</span><span class="sxs-lookup"><span data-stu-id="03b26-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="03b26-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="03b26-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="03b26-120">Küpsise vastavuse nõusoleku jälgimine.</span><span class="sxs-lookup"><span data-stu-id="03b26-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="03b26-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="03b26-121">ai_session</span></span>                                  | <span data-ttu-id="03b26-122">Tuvastab, mitu kasutajategevuse seanssi on hõlmanud konkreetseid rakenduse lehti ja funktsioone.</span><span class="sxs-lookup"><span data-stu-id="03b26-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="03b26-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="03b26-123">ai_user</span></span>                                     | <span data-ttu-id="03b26-124">Tuvastab, mitu inimest kasutas rakendust ja selle funktsioone.</span><span class="sxs-lookup"><span data-stu-id="03b26-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="03b26-125">Kasutajaid loendatakse anonüümsete ID-de abil.</span><span class="sxs-lookup"><span data-stu-id="03b26-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="03b26-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="03b26-126">b2cru</span></span>                                       | <span data-ttu-id="03b26-127">Talletab ümbersuunamise URL-i dünaamiliselt.</span><span class="sxs-lookup"><span data-stu-id="03b26-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="03b26-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="03b26-128">JSESSIONID</span></span>                                  | <span data-ttu-id="03b26-129">Maksekonnektor Adyen kasutab seda kasutaja seansi talletamiseks.</span><span class="sxs-lookup"><span data-stu-id="03b26-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="03b26-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="03b26-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="03b26-131">Autentimine</span><span class="sxs-lookup"><span data-stu-id="03b26-131">Authentication</span></span>                                               |
| <span data-ttu-id="03b26-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="03b26-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="03b26-133">Kasutatakse päringu oleku säilitamiseks.</span><span class="sxs-lookup"><span data-stu-id="03b26-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="03b26-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="03b26-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="03b26-135">Päringuvõltsingu (CRSF) talong, mida kasutatakse päringuvõltsingu eest kaitsmiseks.</span><span class="sxs-lookup"><span data-stu-id="03b26-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="03b26-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="03b26-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="03b26-137">Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari.</span><span class="sxs-lookup"><span data-stu-id="03b26-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="03b26-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="03b26-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="03b26-139">Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari.</span><span class="sxs-lookup"><span data-stu-id="03b26-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="03b26-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="03b26-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="03b26-141">Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari.</span><span class="sxs-lookup"><span data-stu-id="03b26-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="03b26-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="03b26-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="03b26-143">Kasutatakse SSO seansi haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="03b26-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="03b26-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="03b26-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="03b26-145">Kasutatakse toimingute, sealhulgas praeguse toimingu, jälgimiseks (avatud vahekaartide arv, mis autendivad ettevõtte ja tarbija vahelist (B2C) saiti).</span><span class="sxs-lookup"><span data-stu-id="03b26-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="03b26-146">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="03b26-146">Additional resources</span></span>

[<span data-ttu-id="03b26-147">Hõlbustusfunktsioonid ja -võimalused</span><span class="sxs-lookup"><span data-stu-id="03b26-147">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="03b26-148">Vastavuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="03b26-148">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="03b26-149">Privaatsuspoliitika lehe lisamine</span><span class="sxs-lookup"><span data-stu-id="03b26-149">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="03b26-150">Jälgitud sisumuudatustega seostatud kasutaja ID-de asendamine</span><span class="sxs-lookup"><span data-stu-id="03b26-150">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)
