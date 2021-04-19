---
title: Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade
description: Selles teemas antakse ülevaade Microsoft Dynamics 365 Commerce ja Microsoft Teams integratsioonist.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3b7872757815d4eec0393e8b1c8c6ff5467e9473
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842646"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="23fbc-103">Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade</span><span class="sxs-lookup"><span data-stu-id="23fbc-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="23fbc-104">Selles teemas antakse ülevaade Microsoft Dynamics 365 Commerce ja Microsoft Teams integratsioonist.</span><span class="sxs-lookup"><span data-stu-id="23fbc-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="23fbc-105">Dynamics 365 Commerce integreerub rakendusega Teams, et aidata kliente ja nende töötajaid, parandades tööviljakust kahe rakenduse vahelisi ülesandeid sünkroonides.</span><span class="sxs-lookup"><span data-stu-id="23fbc-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="23fbc-106">Rakenduse Commerce and Teams sujuvam ülesande haldus võimaldab kaupluste juhatajal ja töötajal luua ülesannete loendeid, määrata ülesandeid mitmele kauplusele ja jälgida toimingute olekut kauplustes olenemata millisest rakendusest seda tehti.</span><span class="sxs-lookup"><span data-stu-id="23fbc-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="23fbc-107">Commerce and Teamsi integreerimine on saadaval rakenduse Commerce versiooni 10.0.18 väljalaskest.</span><span class="sxs-lookup"><span data-stu-id="23fbc-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="23fbc-108">Võtmefunktsioonid</span><span class="sxs-lookup"><span data-stu-id="23fbc-108">Key features</span></span>

<span data-ttu-id="23fbc-109">Need on mõned Commerce ja Microsoft Teams integratsiooni põhifunktsioonid:</span><span class="sxs-lookup"><span data-stu-id="23fbc-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="23fbc-110">Kasutage rakendust Teams kasutades Commerce'is määratletud teavet, nagu organisatsiooniline struktuur ja teave kaupluste, töötajate, õiguste ja ärikonteksti kohta.</span><span class="sxs-lookup"><span data-stu-id="23fbc-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="23fbc-111">Saate hõlpsalt sünkroonida Commerce ja Teams vahelisi jooksvaid muudatusi (nt uute poodide lisamine või uute töötajate palkamine), kuid säilitada Commerce organisatsioonilist struktuuri andmete põhiallikana.</span><span class="sxs-lookup"><span data-stu-id="23fbc-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="23fbc-112">Integreerige Commerce ja Teams vahelisi ülesannete haldust, et aidata salvestada töötajaid, kaupluste juhatajaid, piirkonnajuhid ja kommunikatsioonijuhid ülesandehaldust ükskõik kummast rakendusest.</span><span class="sxs-lookup"><span data-stu-id="23fbc-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="23fbc-113">Integratsioonifunktsiooni kasutamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="23fbc-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="23fbc-114">Enne Microsoft Teams integratsioonifunktsiooni kasutamist peavad olema täidetud järgmised eeltingimused:</span><span class="sxs-lookup"><span data-stu-id="23fbc-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="23fbc-115">Microsoft 365 Business Standard litsents (see litsents sisaldab rakendust Teams.)</span><span class="sxs-lookup"><span data-stu-id="23fbc-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="23fbc-116">Azure Active Directory (Azure AD) kontod kõigile kaupluse juhatajatele ja töötajatele</span><span class="sxs-lookup"><span data-stu-id="23fbc-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="23fbc-117">Azure AD autentimisega konfigureeritud kassasüsteemid</span><span class="sxs-lookup"><span data-stu-id="23fbc-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="23fbc-118">Kontseptuaalne arhitektuur</span><span class="sxs-lookup"><span data-stu-id="23fbc-118">Conceptual architecture</span></span>

<span data-ttu-id="23fbc-119">Järgmine näide näitab kontseptuaalset Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülesehitust, kasutades näitena San Francisco kauplust.</span><span class="sxs-lookup"><span data-stu-id="23fbc-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="23fbc-120">Nii Teamsi kui ka Commerce kassarakendus kasutab hoidlana Microsoft Plannerit, nii et Teamsis avaldatud ülesanded ilmuvad kassarakenduses ja kassahaldurite loodud sihtülesanded ilmuvad Teamsis, mistõttu rakenduste vahel toimub tõrgeteta ülesannete haldus.</span><span class="sxs-lookup"><span data-stu-id="23fbc-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![Commerce ja Teamsi integratsiooni ülesehitus](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="23fbc-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="23fbc-122">Additional resources</span></span>

[<span data-ttu-id="23fbc-123">Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="23fbc-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="23fbc-124">Microsoft Teams sätted rakendusest Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="23fbc-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="23fbc-125">Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel</span><span class="sxs-lookup"><span data-stu-id="23fbc-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="23fbc-126">Kasutaja rollide haldamine rakenduses Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="23fbc-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="23fbc-127">Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="23fbc-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="23fbc-128">Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK</span><span class="sxs-lookup"><span data-stu-id="23fbc-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
