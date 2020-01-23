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
ms.openlocfilehash: ec095642f556b8d0087dd22f35097671a30047a6
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898499"
---
# <a name="troubleshoot-integration-with-linkedin-and-attract"></a><span data-ttu-id="30b4a-103">LinkedIni ja rakenduse Attract integreerimise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="30b4a-103">Troubleshoot integration with LinkedIn and Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="30b4a-104">Järgmise teabe abil saate tõrkeotsingut teha probleemide korral, mis võivad tekkida, kui proovite sisestada tööpakkumisi rakendusest Microsoft Dynamics 365 Talent: Attract LinkedIni.</span><span class="sxs-lookup"><span data-stu-id="30b4a-104">Use the following information to help troubleshoot issues that you might have when you try to post jobs to LinkedIn from Microsoft Dynamics 365 Talent: Attract.</span></span>

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a><span data-ttu-id="30b4a-105">Te ei saa Attractist LinkedIni sisse logida</span><span class="sxs-lookup"><span data-stu-id="30b4a-105">You can't sign in to LinkedIn from Attract</span></span>

<span data-ttu-id="30b4a-106">Kui teil on probleeme Attractist LinkedIni sisselogimisega, proovige järgmist.</span><span class="sxs-lookup"><span data-stu-id="30b4a-106">If you're having trouble signing in to LinkedIn from Attract, try these steps:</span></span>

1. <span data-ttu-id="30b4a-107">Kontrollige, kas Attracti sisestatud LinkedIni mandaadid on kehtivad ja õiged.</span><span class="sxs-lookup"><span data-stu-id="30b4a-107">Verify that the LinkedIn credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="30b4a-108">Kui mandaadid on kehtivad ja õiged, võtke ühendust [LinkedIni toega](https://www.linkedin.com/help/linkedin).</span><span class="sxs-lookup"><span data-stu-id="30b4a-108">If the credentials are valid and correct, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>
3. <span data-ttu-id="30b4a-109">Kui probleem ei lahene, võtke ühendust [Microsofti toega](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="30b4a-109">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a><span data-ttu-id="30b4a-110">Tööpakkumisi Attractist ei kuvata LinkedInis</span><span class="sxs-lookup"><span data-stu-id="30b4a-110">Job posts from Attract don't appear on LinkedIn</span></span>

<span data-ttu-id="30b4a-111">Kui teie tööpakkumine pole pärast 24 tunni möödumist LinkedInis ilmunud, proovige järgmist.</span><span class="sxs-lookup"><span data-stu-id="30b4a-111">If your job hasn't appeared on LinkedIn after 24 hours, try these steps:</span></span>

1. <span data-ttu-id="30b4a-112">Veenduge, et teie LinkedIni ettevõtte ID viiks teie LinkedIni ettevõtte lehele ja oleks õigesti sisestatud Attract Admin centerisse.</span><span class="sxs-lookup"><span data-stu-id="30b4a-112">Make sure that your LinkedIn Company ID maps to your LinkedIn company page and is correctly entered in the Attract Admin center.</span></span> <span data-ttu-id="30b4a-113">Lisateavet Admin Centeris LinkedIni sätete muutmise kohta leiate teemast [Rakendusega LinkedIn for Microsoft Dynamics 365 Talent – Attract integreerimise seadistamine](attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="30b4a-113">For more information about how to change LinkedIn settings in the Admin center, see [Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract](attract-admin-linkedin.md).</span></span> <span data-ttu-id="30b4a-114">Lisateavet LinkedIni ettevõtte ID kohta leiate teemast [LinkedIni ettevõtte ID sidumine LinkedIni töölauaga – korduma kippuvad küsimused](https://www.linkedin.com/help/linkedin/answer/98972).</span><span class="sxs-lookup"><span data-stu-id="30b4a-114">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>
2. <span data-ttu-id="30b4a-115">Kontrollige LinkedIni tööpakkumise üksikasju ja veenduge, et aadress oleks täielik.</span><span class="sxs-lookup"><span data-stu-id="30b4a-115">Check the job details on LinkedIn to make sure that the address is complete.</span></span> <span data-ttu-id="30b4a-116">Tööpakkumise edukaks sisestamiseks vajab LinkedIn vähemalt tööpakkumise linna ja riiki või regiooni.</span><span class="sxs-lookup"><span data-stu-id="30b4a-116">To post a job successfully, LinkedIn needs at least the city and country or region of the job.</span></span>
3. <span data-ttu-id="30b4a-117">Veenduge, et tööpakkumine ei dubleeriks teist tööpakkumist, mis on LinkedIni sisestatud.</span><span class="sxs-lookup"><span data-stu-id="30b4a-117">Make sure that the job doesn't duplicate another job that has been posted on LinkedIn.</span></span> <span data-ttu-id="30b4a-118">LinkedIn ei postita töid, mis on kas LinkedIn Premium tööpakkumise või mõne muu allika piiratud loendite duplikaadid.</span><span class="sxs-lookup"><span data-stu-id="30b4a-118">LinkedIn won't post jobs that are duplicates of either LinkedIn Premium Job Slots or Limited Listings from another source.</span></span> <span data-ttu-id="30b4a-119">Kontrollige, kas mõni teine isik teie ettevõttest ei ole juba tööpakkumist käsitsi sisestanud.</span><span class="sxs-lookup"><span data-stu-id="30b4a-119">Verify that another person at your company didn't already post the job manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="30b4a-120">Vt ka</span><span class="sxs-lookup"><span data-stu-id="30b4a-120">See also</span></span>

[<span data-ttu-id="30b4a-121">Attracti integreerimine LinkedIni KKK-ga</span><span class="sxs-lookup"><span data-stu-id="30b4a-121">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="30b4a-122">Rakendusest Microsoft Dynamics 365 Talent – Attract LinkedIni postitamine</span><span class="sxs-lookup"><span data-stu-id="30b4a-122">Post jobs to LinkedIn from Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="30b4a-123">LinkedIn Recruiteriga allikakandidaadid rakenduses Microsoft Dynamics 365 Talent – Attract.</span><span class="sxs-lookup"><span data-stu-id="30b4a-123">Source candidates with LinkedIn Recruiter in Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="30b4a-124">Tööde loomine, kinnitamine ja sisestamine Attractis</span><span class="sxs-lookup"><span data-stu-id="30b4a-124">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="30b4a-125">Rakendusega Microsoft Dynamics 365 Talent – Attract ja LinkedIniga integreerimise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="30b4a-125">Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-troubleshoot-linkedin.md)
