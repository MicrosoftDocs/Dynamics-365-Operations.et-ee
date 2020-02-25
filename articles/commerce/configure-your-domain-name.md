---
title: Domeeninime konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida rakenduse Microsoft Dynamics 365 e-kaubanduse saidi domeeni nime.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4db774783dba4b1cea9552da3cff29a9528bd496
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002170"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="ceb19-103">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ceb19-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ceb19-104">Selles teemas selgitatakse, kuidas konfigureerida rakenduse Microsoft Dynamics 365 e-kaubanduse saidi domeeni nime.</span><span class="sxs-lookup"><span data-stu-id="ceb19-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="ceb19-105">Domeenide lisamine e-kaubanduse lähtestamise ajal</span><span class="sxs-lookup"><span data-stu-id="ceb19-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="ceb19-106">Domeenide seostamiseks e-kaubanduse keskkonnaga, lähtestage e-kaubandus, nagu on kirjeldatud teemas [Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="ceb19-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="ceb19-107">Lähtestamise ajal palutakse teil anda teavet, mida kasutatakse teie e-kaubanduse keskkonna ettevalmistamiseks.</span><span class="sxs-lookup"><span data-stu-id="ceb19-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="ceb19-108">Lisage väljale **Toetatud hostinimed** kõik domeenid, mida kavatsete selle keskkonnaga kasutada.</span><span class="sxs-lookup"><span data-stu-id="ceb19-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="ceb19-109">Mitu domeeni tuleb eraldada semikooloniga.</span><span class="sxs-lookup"><span data-stu-id="ceb19-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="ceb19-110">Sel viisil on domeenid konfigureeritud kõikides vajalikes e-kaubanduse komponentides ja need on kasutusvalmis, kui vahetate liikluse sisuedastusvõrgust (CDN) või veebiserverist ja suunate selle e-kaubanduse eesserveritesse.</span><span class="sxs-lookup"><span data-stu-id="ceb19-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="ceb19-111">Domeenide lisamine pärast e-kaubanduse lähtestamist</span><span class="sxs-lookup"><span data-stu-id="ceb19-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="ceb19-112">E-kaubanduse keskkonnaga uute domeenide seostamiseks pärast e-kaubanduse lähtestamist, peate esitama teenusetaotluse.</span><span class="sxs-lookup"><span data-stu-id="ceb19-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ceb19-113">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ceb19-113">Additional resources</span></span>

[<span data-ttu-id="ceb19-114">Uue e-kaubanduse saidi juurutamine</span><span class="sxs-lookup"><span data-stu-id="ceb19-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="ceb19-115">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="ceb19-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="ceb19-116">Veebisaidi seostamine kanaliga</span><span class="sxs-lookup"><span data-stu-id="ceb19-116">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="ceb19-117">Robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="ceb19-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="ceb19-118">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="ceb19-118">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="ceb19-119">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="ceb19-119">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="ceb19-120">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="ceb19-120">Enable location-based store detection</span></span>](enable-store-detection.md)
