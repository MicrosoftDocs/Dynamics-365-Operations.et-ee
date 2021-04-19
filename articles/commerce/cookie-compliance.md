---
title: Küpsise vastavus
description: Selles teemas kirjeldatakse küpsise vastavuse ja Microsoft Dynamics 365 Commerce'is sisalduva vaikepoliitika kaalutlusi.
author: BrianShook
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2cc2089bc3052c0c59cb0414f8301123a9a30df2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796023"
---
# <a name="cookie-compliance"></a><span data-ttu-id="4b6cc-103">Küpsise vastavus</span><span class="sxs-lookup"><span data-stu-id="4b6cc-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4b6cc-104">Selles teemas kirjeldatakse küpsise vastavuse ja Microsoft Dynamics 365 Commerce'is sisalduva vaikepoliitika kaalutlusi.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4b6cc-105">Privaatsus on oluline tegur, kui e-kaubanduse kliente mõjutavad jälgimistehnoloogiad.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-105">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="4b6cc-106">Eraelu puutumatuse standardite, nagu üldise andmekaitse määruse (GDPR) tõttu Euroopa Liidus (EL), tuleb arvesse võtta elektroonilisi privaatsuspõhimõtted, mis on tänapäeval aktiivsed.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-106">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="4b6cc-107">Kuna paljud e-kaubanduse saidid on globaalselt juurdepääsetavad vaikimisi, on oluline vaadata üle oma e-kaubanduse saidi vastavuse standardid.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-107">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="4b6cc-108">Lisateavet Microsoft kasutavate üldpõhimõtete kohta leiate [Microsofti usalduskeskusest.](https://www.microsoft.com/trust-center)</span><span class="sxs-lookup"><span data-stu-id="4b6cc-108">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="4b6cc-109">Sellel saidil saate ka lisateavet vastavuse ja privaatsuse valdkondade kohta.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-109">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="4b6cc-110">Järgmises tabelis on toodud Dynamics 365 Commerce'i saitide asetatud küpsiste kehtiv viiteloend.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-110">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="4b6cc-111">Küpsise nimi</span><span class="sxs-lookup"><span data-stu-id="4b6cc-111">Cookie name</span></span>                               | <span data-ttu-id="4b6cc-112">Kasutus</span><span class="sxs-lookup"><span data-stu-id="4b6cc-112">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="4b6cc-113">.AspNet.Cookies</span><span class="sxs-lookup"><span data-stu-id="4b6cc-113">.AspNet.Cookies</span></span>                             | <span data-ttu-id="4b6cc-114">Talletage Microsoft Azure Active Directory (Azure AD) autentimisküpsised ühekordse sisselogimise (SSO) jaoks.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-114">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="4b6cc-115">Talletab kasutaja kohta krüptitud põhiteavet (nimi, perekonnanimi, e-post).</span><span class="sxs-lookup"><span data-stu-id="4b6cc-115">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="4b6cc-116">&#95;msdyn365___cart&#95;</span><span class="sxs-lookup"><span data-stu-id="4b6cc-116">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="4b6cc-117">Talletab ostukorvi ID, mida kasutatakse ostukorvi eksemplari lisatud toodete loendi hankimiseks.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-117">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="4b6cc-118">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="4b6cc-118">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="4b6cc-119">Küpsise vastavuse nõusoleku jälgimine.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-119">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="4b6cc-120">ai_session</span><span class="sxs-lookup"><span data-stu-id="4b6cc-120">ai_session</span></span>                                  | <span data-ttu-id="4b6cc-121">Tuvastab, mitu kasutajategevuse seanssi on hõlmanud konkreetseid rakenduse lehti ja funktsioone.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-121">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="4b6cc-122">ai_user</span><span class="sxs-lookup"><span data-stu-id="4b6cc-122">ai_user</span></span>                                     | <span data-ttu-id="4b6cc-123">Tuvastab, mitu inimest kasutas rakendust ja selle funktsioone.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-123">Detects how many people used the app and its features.</span></span> <span data-ttu-id="4b6cc-124">Kasutajaid loendatakse anonüümsete ID-de abil.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-124">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="4b6cc-125">b2cru</span><span class="sxs-lookup"><span data-stu-id="4b6cc-125">b2cru</span></span>                                       | <span data-ttu-id="4b6cc-126">Talletab ümbersuunamise URL-i dünaamiliselt.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-126">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="4b6cc-127">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="4b6cc-127">JSESSIONID</span></span>                                  | <span data-ttu-id="4b6cc-128">Maksekonnektor Adyen kasutab seda kasutaja seansi talletamiseks.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-128">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="4b6cc-129">OpenIdConnect.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="4b6cc-129">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="4b6cc-130">Autentimine</span><span class="sxs-lookup"><span data-stu-id="4b6cc-130">Authentication</span></span>                                               |
| <span data-ttu-id="4b6cc-131">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="4b6cc-131">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="4b6cc-132">Kasutatakse päringu oleku säilitamiseks.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-132">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="4b6cc-133">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="4b6cc-133">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="4b6cc-134">Päringuvõltsingu (CRSF) talong, mida kasutatakse päringuvõltsingu eest kaitsmiseks.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-134">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="4b6cc-135">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="4b6cc-135">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="4b6cc-136">Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-136">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="4b6cc-137">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="4b6cc-137">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="4b6cc-138">Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-138">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="4b6cc-139">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="4b6cc-139">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="4b6cc-140">Kasutatakse selleks, et suunata päringuid sobivasse tootmise autentimisserveri eksemplari.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-140">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="4b6cc-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="4b6cc-141">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="4b6cc-142">Kasutatakse SSO seansi haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-142">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="4b6cc-143">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="4b6cc-143">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="4b6cc-144">Kasutatakse toimingute, sealhulgas praeguse toimingu, jälgimiseks (avatud vahekaartide arv, mis autendivad ettevõtte ja tarbija vahelist (B2C) saiti).</span><span class="sxs-lookup"><span data-stu-id="4b6cc-144">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="4b6cc-145">Saidi kasutaja küpsise nõusolek e-kaubanduse saidil</span><span class="sxs-lookup"><span data-stu-id="4b6cc-145">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="4b6cc-146">Kui e-kaubanduse saidi funktsioon või moodul kasutab ebaolulist küpsist, tuleb enne küpsise jälitamist hankida saidi kasutaja nõusolek.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-146">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="4b6cc-147">Selleks et saidi kasutajad saaksid e-kaubanduse saidil anda küpsise nõusoleku, peab saidi autor lisama ja konfigureerima lehe päisemoodulisse küpsistega nõustumise mooduli, et tagada nõusoleku küsimine ja vastuvõtmine.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-147">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="4b6cc-148">Saidi kasutaja peab andma nõusoleku, et saidi lehel oleks võimalik renderdada ebaolulist küpsist kasutavat funktsiooni või moodulit.</span><span class="sxs-lookup"><span data-stu-id="4b6cc-148">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4b6cc-149">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4b6cc-149">Additional resources</span></span>

[<span data-ttu-id="4b6cc-150">Hõlbustusfunktsioonid ja -võimalused</span><span class="sxs-lookup"><span data-stu-id="4b6cc-150">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="4b6cc-151">Vastavuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="4b6cc-151">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="4b6cc-152">Privaatsuspoliitika lehe lisamine</span><span class="sxs-lookup"><span data-stu-id="4b6cc-152">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="4b6cc-153">Jälgitud sisumuudatustega seostatud kasutaja ID-de asendamine</span><span class="sxs-lookup"><span data-stu-id="4b6cc-153">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="4b6cc-154">Küpsistega nõustumise moodul</span><span class="sxs-lookup"><span data-stu-id="4b6cc-154">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="4b6cc-155">Päisemoodul</span><span class="sxs-lookup"><span data-stu-id="4b6cc-155">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
