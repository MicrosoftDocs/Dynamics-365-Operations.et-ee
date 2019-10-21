---
title: LinkedIni ja rakekenduse Microsoft Dynamics 365 Talent – Attract integreerimise tõrkeotsing
description: Selles teemas kirjeldatakse tõrkeotsingut, kui proovite sisestada töid rakendusest Microsoft Dynamics 365 Talent– Attract LinkedIni.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 79f138ad9aeb203bce19cc93237fca96bffd015f
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008216"
---
# <a name="troubleshoot-integration-with-linkedin"></a><span data-ttu-id="9d7f1-103">LinkedIniga integreerimise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="9d7f1-103">Troubleshoot integration with LinkedIn</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d7f1-104">Järgmise teabe abil saate tõrkeotsingut teha probleemide korral, mis võivad tekkida, kui proovite sisestada tööpakkumisi rakendusest Microsoft Dynamics 365 Talent: Attract LinkedIni.</span><span class="sxs-lookup"><span data-stu-id="9d7f1-104">Use the following information to help troubleshoot issues that you might have when you try to post jobs to LinkedIn from Microsoft Dynamics 365 Talent: Attract.</span></span>

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a><span data-ttu-id="9d7f1-105">Te ei saa Attractist LinkedIni sisse logida</span><span class="sxs-lookup"><span data-stu-id="9d7f1-105">You can't sign in to LinkedIn from Attract</span></span>

<span data-ttu-id="9d7f1-106">Kui teil on probleeme Attractist LinkedIni sisselogimisega, proovige järgmist.</span><span class="sxs-lookup"><span data-stu-id="9d7f1-106">If you're having trouble signing in to LinkedIn from Attract, try these steps:</span></span>

1. <span data-ttu-id="9d7f1-107">Kontrollige, kas Attracti sisestatud LinkedIni mandaadid on kehtivad ja õiged.</span><span class="sxs-lookup"><span data-stu-id="9d7f1-107">Verify that the LinkedIn credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="9d7f1-108">Kui mandaadid on kehtivad ja õiged, võtke ühendust [LinkedIni toega](https://www.linkedin.com/help/linkedin).</span><span class="sxs-lookup"><span data-stu-id="9d7f1-108">If the credentials are valid and correct, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>
3. <span data-ttu-id="9d7f1-109">Kui probleem ei lahene, võtke ühendust [Microsofti toega](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="9d7f1-109">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a><span data-ttu-id="9d7f1-110">Tööpakkumisi Attractist ei kuvata LinkedInis</span><span class="sxs-lookup"><span data-stu-id="9d7f1-110">Job posts from Attract don't appear on LinkedIn</span></span>

<span data-ttu-id="9d7f1-111">Kui teie tööpakkumine pole pärast 24 tunni möödumist LinkedInis ilmunud, proovige järgmist.</span><span class="sxs-lookup"><span data-stu-id="9d7f1-111">If your job hasn't appeared on LinkedIn after 24 hours, try these steps:</span></span>

1. <span data-ttu-id="9d7f1-112">Veenduge, et teie LinkedIni ettevõtte ID viiks teie LinkedIni ettevõtte lehele ja oleks õigesti sisestatud Attract Admin centerisse.</span><span class="sxs-lookup"><span data-stu-id="9d7f1-112">Make sure that your LinkedIn Company ID maps to your LinkedIn company page and is correctly entered in the Attract Admin center.</span></span> <span data-ttu-id="9d7f1-113">Lisateavet LinkedIni seadete muutmise kohta administreerimiskeskuses leiate teemast [Integreerimise häälestamine LinkedIniga](attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="9d7f1-113">For more information about how to change LinkedIn settings in the Admin center, see [Set up integration with LinkedIn](attract-admin-linkedin.md).</span></span> <span data-ttu-id="9d7f1-114">Lisateavet LinkedIni ettevõtte ID kohta leiate teemast [LinkedIni ettevõtte ID sidumine LinkedIni töölauaga – korduma kippuvad küsimused](https://www.linkedin.com/help/linkedin/answer/98972).</span><span class="sxs-lookup"><span data-stu-id="9d7f1-114">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>
2. <span data-ttu-id="9d7f1-115">Kontrollige LinkedIni tööpakkumise üksikasju ja veenduge, et aadress oleks täielik.</span><span class="sxs-lookup"><span data-stu-id="9d7f1-115">Check the job details on LinkedIn to make sure that the address is complete.</span></span> <span data-ttu-id="9d7f1-116">Tööpakkumise edukaks sisestamiseks vajab LinkedIn vähemalt tööpakkumise linna ja riiki või regiooni.</span><span class="sxs-lookup"><span data-stu-id="9d7f1-116">To post a job successfully, LinkedIn needs at least the city and country or region of the job.</span></span>
3. <span data-ttu-id="9d7f1-117">Veenduge, et tööpakkumine ei dubleeriks teist tööpakkumist, mis on LinkedIni sisestatud.</span><span class="sxs-lookup"><span data-stu-id="9d7f1-117">Make sure that the job doesn't duplicate another job that has been posted on LinkedIn.</span></span> <span data-ttu-id="9d7f1-118">LinkedIn ei postita töid, mis on kas LinkedIn Premium tööpakkumise või mõne muu allika piiratud loendite duplikaadid.</span><span class="sxs-lookup"><span data-stu-id="9d7f1-118">LinkedIn won't post jobs that are duplicates of either LinkedIn Premium Job Slots or Limited Listings from another source.</span></span> <span data-ttu-id="9d7f1-119">Kontrollige, kas mõni teine isik teie ettevõttest ei ole juba tööpakkumist käsitsi sisestanud.</span><span class="sxs-lookup"><span data-stu-id="9d7f1-119">Verify that another person at your company didn't already post the job manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d7f1-120">Vt ka</span><span class="sxs-lookup"><span data-stu-id="9d7f1-120">See also</span></span>

[<span data-ttu-id="9d7f1-121">LinkedIn-i KKK</span><span class="sxs-lookup"><span data-stu-id="9d7f1-121">LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="9d7f1-122">Tööde sisestamine Attractist LinkedIn-i</span><span class="sxs-lookup"><span data-stu-id="9d7f1-122">Post jobs to LinkedIn from Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="9d7f1-123">Kandidaatide hankimine teenuse LinkedIn Recruiter abil</span><span class="sxs-lookup"><span data-stu-id="9d7f1-123">Source candidates with LinkedIn Recruiter</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="9d7f1-124">Tööpakkumiste loomine</span><span class="sxs-lookup"><span data-stu-id="9d7f1-124">Create jobs</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="9d7f1-125">LinkedIniga integreerimise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="9d7f1-125">Troubleshoot integration with LinkedIn</span></span>](./attract-troubleshoot-linkedin.md)
