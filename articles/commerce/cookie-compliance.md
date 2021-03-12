---
title: Küpsise vastavus
description: Selles teemas kirjeldatakse küpsise vastavuse ja Microsoft Dynamics 365 Commerce'is sisalduva vaikepoliitika kaalutlusi.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 95c5801e69396b21a36c4ae12ce17801e6f7fd88
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993496"
---
# <a name="cookie-compliance"></a><span data-ttu-id="0c4e5-103">Küpsise vastavus</span><span class="sxs-lookup"><span data-stu-id="0c4e5-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0c4e5-104">Selles teemas kirjeldatakse küpsise vastavuse ja Microsoft Dynamics 365 Commerce'is sisalduva vaikepoliitika kaalutlusi.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0c4e5-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="0c4e5-105">Overview</span></span>

<span data-ttu-id="0c4e5-106">Privaatsus on oluline tegur, kui e-kaubanduse kliente mõjutavad jälgimistehnoloogiad.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="0c4e5-107">Eraelu puutumatuse standardite, nagu üldise andmekaitse määruse (GDPR) tõttu Euroopa Liidus (EL), tuleb arvesse võtta elektroonilisi privaatsuspõhimõtted, mis on tänapäeval aktiivsed.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="0c4e5-108">Kuna paljud e-kaubanduse saidid on globaalselt juurdepääsetavad vaikimisi, on oluline vaadata üle oma e-kaubanduse saidi vastavuse standardid.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="0c4e5-109">Lisateavet Microsoft kasutavate üldpõhimõtete kohta leiate [Microsofti usalduskeskusest.](https://www.microsoft.com/trust-center)</span><span class="sxs-lookup"><span data-stu-id="0c4e5-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="0c4e5-110">Sellel saidil saate ka lisateavet vastavuse ja privaatsuse valdkondade kohta.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="0c4e5-111">Järgmises tabelis on toodud Dynamics 365 Commerce'i saitide asetatud küpsiste kehtiv viiteloend.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="0c4e5-112">Küpsise nimi</span><span class="sxs-lookup"><span data-stu-id="0c4e5-112">Cookie name</span></span>                               | <span data-ttu-id="0c4e5-113">Kasutus</span><span class="sxs-lookup"><span data-stu-id="0c4e5-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="0c4e5-114">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="0c4e5-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="0c4e5-115">Talletage Microsoft Azure Active Directory (Azure AD) autentimisküpsised ühekordse sisselogimise (SSO) jaoks.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="0c4e5-116">Talletab kasutaja kohta krüptitud põhiteavet (nimi, perekonnanimi, e-post).</span><span class="sxs-lookup"><span data-stu-id="0c4e5-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="0c4e5-117">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="0c4e5-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="0c4e5-118">Talletab ostukorvi ID, mida kasutatakse ostukorvi eksemplari lisatud toodete loendi hankimiseks.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="0c4e5-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="0c4e5-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="0c4e5-120">Küpsise vastavuse nõusoleku jälgimine.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="0c4e5-121">ai_session</span><span class="sxs-lookup"><span data-stu-id="0c4e5-121">ai_session</span></span>                                  | <span data-ttu-id="0c4e5-122">Tuvastab, mitu kasutajategevuse seanssi on hõlmanud konkreetseid rakenduse lehti ja funktsioone.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="0c4e5-123">ai_user</span><span class="sxs-lookup"><span data-stu-id="0c4e5-123">ai_user</span></span>                                     | <span data-ttu-id="0c4e5-124">Tuvastab, mitu inimest kasutas rakendust ja selle funktsioone.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="0c4e5-125">Kasutajaid loendatakse anonüümsete ID-de abil.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="0c4e5-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="0c4e5-126">b2cru</span></span>                                       | <span data-ttu-id="0c4e5-127">Talletab ümbersuunamise URL-i dünaamiliselt.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="0c4e5-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="0c4e5-128">JSESSIONID</span></span>                                  | <span data-ttu-id="0c4e5-129">Maksekonnektor Adyen kasutab seda kasutaja seansi talletamiseks.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="0c4e5-130">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="0c4e5-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="0c4e5-131">Autentimine</span><span class="sxs-lookup"><span data-stu-id="0c4e5-131">Authentication</span></span>                                               |
| <span data-ttu-id="0c4e5-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="0c4e5-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="0c4e5-133">Kasutatakse päringu oleku säilitamiseks.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="0c4e5-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="0c4e5-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="0c4e5-135">Päringuvõltsingu (CRSF) talong, mida kasutatakse päringuvõltsingu eest kaitsmiseks.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="0c4e5-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="0c4e5-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="0c4e5-137">Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="0c4e5-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="0c4e5-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="0c4e5-139">Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="0c4e5-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="0c4e5-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="0c4e5-141">Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="0c4e5-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="0c4e5-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="0c4e5-143">Kasutatakse SSO seansi haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="0c4e5-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="0c4e5-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="0c4e5-145">Kasutatakse toimingute, sealhulgas praeguse toimingu, jälgimiseks (avatud vahekaartide arv, mis autendivad ettevõtte ja tarbija vahelist (B2C) saiti).</span><span class="sxs-lookup"><span data-stu-id="0c4e5-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="0c4e5-146">Saidi kasutaja küpsise nõusolek e-kaubanduse saidil</span><span class="sxs-lookup"><span data-stu-id="0c4e5-146">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="0c4e5-147">Kui e-kaubanduse saidi funktsioon või moodul kasutab ebaolulist küpsist, tuleb enne küpsise jälitamist hankida saidi kasutaja nõusolek.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-147">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="0c4e5-148">Selleks et saidi kasutajad saaksid e-kaubanduse saidil anda küpsise nõusoleku, peab saidi autor lisama ja konfigureerima lehe päisemoodulisse küpsistega nõustumise mooduli, et tagada nõusoleku küsimine ja vastuvõtmine.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-148">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="0c4e5-149">Saidi kasutaja peab andma nõusoleku, et saidi lehel oleks võimalik renderdada ebaolulist küpsist kasutavat funktsiooni või moodulit.</span><span class="sxs-lookup"><span data-stu-id="0c4e5-149">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c4e5-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0c4e5-150">Additional resources</span></span>

[<span data-ttu-id="0c4e5-151">Hõlbustusfunktsioonid ja -võimalused</span><span class="sxs-lookup"><span data-stu-id="0c4e5-151">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="0c4e5-152">Vastavuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="0c4e5-152">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="0c4e5-153">Privaatsuspoliitika lehe lisamine</span><span class="sxs-lookup"><span data-stu-id="0c4e5-153">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="0c4e5-154">Jälgitud sisumuudatustega seostatud kasutaja ID-de asendamine</span><span class="sxs-lookup"><span data-stu-id="0c4e5-154">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="0c4e5-155">Küpsistega nõustumise moodul</span><span class="sxs-lookup"><span data-stu-id="0c4e5-155">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="0c4e5-156">Päisemoodul</span><span class="sxs-lookup"><span data-stu-id="0c4e5-156">Header module</span></span>](author-header-module.md)
