---
title: Domeeninime konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida rakenduse Microsoft Dynamics 365 e-kaubanduse saidi domeeni nime.
author: psimolin
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8b7bc322b1a42190d5eec99f89a34025c34ba09f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220482"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="d60e2-103">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d60e2-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d60e2-104">Selles teemas selgitatakse, kuidas konfigureerida rakenduse Microsoft Dynamics 365 e-kaubanduse saidi domeeni nime.</span><span class="sxs-lookup"><span data-stu-id="d60e2-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="d60e2-105">Domeenide lisamine e-kaubanduse lähtestamise ajal</span><span class="sxs-lookup"><span data-stu-id="d60e2-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="d60e2-106">Domeenide seostamiseks enda Dynamics 365 Commerce'i e-kaubanduse keskkonnaga lähtestage e-kaubandus, nagu on kirjeldatud teemas [Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="d60e2-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="d60e2-107">Lähtestamise ajal palutakse teil anda teavet, mida kasutatakse teie e-kaubanduse keskkonna ettevalmistamiseks.</span><span class="sxs-lookup"><span data-stu-id="d60e2-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="d60e2-108">Lisage väljale **Toetatud hostinimed** kõik domeenid, mida kavatsete selle keskkonnaga kasutada.</span><span class="sxs-lookup"><span data-stu-id="d60e2-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="d60e2-109">Mitu domeeni tuleb eraldada semikooloniga.</span><span class="sxs-lookup"><span data-stu-id="d60e2-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="d60e2-110">Sel viisil on domeenid konfigureeritud kõikides vajalikes kaubanduse komponentides ja need on kasutusvalmis, kui suunate liikluse sisuedastusvõrgust (CDN) või veebiserverist e-kaubanduse eesserveritesse.</span><span class="sxs-lookup"><span data-stu-id="d60e2-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="d60e2-111">Domeenide lisamine pärast e-kaubanduse lähtestamist</span><span class="sxs-lookup"><span data-stu-id="d60e2-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="d60e2-112">Uute domeenide seostamiseks enda e-kaubanduse keskkonnaga pärast e-kaubanduse lähtestamist peate esitama teenusetaotluse.</span><span class="sxs-lookup"><span data-stu-id="d60e2-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d60e2-113">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d60e2-113">Additional resources</span></span>

[<span data-ttu-id="d60e2-114">Uue e-kaubanduse rentniku juurutamine</span><span class="sxs-lookup"><span data-stu-id="d60e2-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="d60e2-115">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="d60e2-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="d60e2-116">Dynamics 365 Commerce'i saidi seostamine võrgukanaliga</span><span class="sxs-lookup"><span data-stu-id="d60e2-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="d60e2-117">Robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="d60e2-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="d60e2-118">Üleslaadimise URL suunab ümber hulgi</span><span class="sxs-lookup"><span data-stu-id="d60e2-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="d60e2-119">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="d60e2-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="d60e2-120">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="d60e2-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="d60e2-121">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="d60e2-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="d60e2-122">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="d60e2-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="d60e2-123">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="d60e2-123">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]