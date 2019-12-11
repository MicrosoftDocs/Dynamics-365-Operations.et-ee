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
ms.openlocfilehash: 7a988f533757cc3f8555fcf4fb724a22a5b014f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770454"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="a78fa-103">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a78fa-103">Configure your domain name</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a78fa-104">Selles teemas selgitatakse, kuidas konfigureerida rakenduse Microsoft Dynamics 365 e-kaubanduse saidi domeeni nime.</span><span class="sxs-lookup"><span data-stu-id="a78fa-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="a78fa-105">Domeenide lisamine e-kaubanduse lähtestamise ajal</span><span class="sxs-lookup"><span data-stu-id="a78fa-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="a78fa-106">Domeenide seostamiseks e-kaubanduse keskkonnaga, lähtestage e-kaubandus, nagu on kirjeldatud teemas [Uue e-kaubanduse saidi juurutamine](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="a78fa-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="a78fa-107">Lähtestamise ajal palutakse teil anda teavet, mida kasutatakse teie e-kaubanduse keskkonna ettevalmistamiseks.</span><span class="sxs-lookup"><span data-stu-id="a78fa-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="a78fa-108">Lisage väljale **Toetatud hostinimed** kõik domeenid, mida kavatsete selle keskkonnaga kasutada.</span><span class="sxs-lookup"><span data-stu-id="a78fa-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="a78fa-109">Mitu domeeni tuleb eraldada semikooloniga.</span><span class="sxs-lookup"><span data-stu-id="a78fa-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="a78fa-110">Sel viisil on domeenid konfigureeritud kõikides vajalikes e-kaubanduse komponentides ja need on kasutusvalmis, kui vahetate liikluse sisuedastusvõrgust (CDN) või veebiserverist ja suunate selle e-kaubanduse eesserveritesse.</span><span class="sxs-lookup"><span data-stu-id="a78fa-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="a78fa-111">Domeenide lisamine pärast e-kaubanduse lähtestamist</span><span class="sxs-lookup"><span data-stu-id="a78fa-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="a78fa-112">E-kaubanduse keskkonnaga uute domeenide seostamiseks pärast e-kaubanduse lähtestamist, peate esitama teenusetaotluse.</span><span class="sxs-lookup"><span data-stu-id="a78fa-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a78fa-113">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a78fa-113">Additional resources</span></span>

[<span data-ttu-id="a78fa-114">E-poe ülevaade</span><span class="sxs-lookup"><span data-stu-id="a78fa-114">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="a78fa-115">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="a78fa-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="a78fa-116">Uue e-kaubanduse saidi juurutamine</span><span class="sxs-lookup"><span data-stu-id="a78fa-116">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a78fa-117">Veebisaidi seostamine kanaliga</span><span class="sxs-lookup"><span data-stu-id="a78fa-117">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a78fa-118">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="a78fa-118">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="a78fa-119">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="a78fa-119">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="a78fa-120">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="a78fa-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
