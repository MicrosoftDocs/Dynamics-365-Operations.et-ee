---
title: Juriidiliste isikute loomine
description: See teema kirjeldab, kuidas luua Microsofti Dynamics 365 Commerce'is juriidilisi isikuid, mis tulevad enne kanalite loomist luua ja konfigureerida.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 28cbcc42505f1dc90c420adc812735841541c8e0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411638"
---
# <a name="create-legal-entities"></a><span data-ttu-id="23af1-103">Juriidiliste isikute loomine</span><span class="sxs-lookup"><span data-stu-id="23af1-103">Create legal entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="23af1-104">See teema kirjeldab, kuidas luua Microsofti Dynamics 365 Commerce'is juriidilisi isikuid, mis tulevad enne kanalite loomist luua ja konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="23af1-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

## <a name="overview"></a><span data-ttu-id="23af1-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="23af1-105">Overview</span></span>

<span data-ttu-id="23af1-106">Juriidiline isik on registreeritud või õigusliku struktuuriga organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="23af1-106">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="23af1-107">Juriidilised isikud võivad sõlmida juriidilisi lepinguid ja on kohustatud koostama oma tegevuse kohta aruandeid.</span><span class="sxs-lookup"><span data-stu-id="23af1-107">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="23af1-108">Ettevõte on juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="23af1-108">A company is a type of legal entity.</span></span> <span data-ttu-id="23af1-109">Ettevõtted on praegu ainsad juriidilised isikud, mida saate luua, ja iga juriidiline isik on seostatud ettevõtte ID-ga.</span><span class="sxs-lookup"><span data-stu-id="23af1-109">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="23af1-110">See seos on olemas, kuna mõni programmi funktsioonivaldkond kasutab oma andmemudelis ettevõtte ID-d või atribuuti *DataAreaId*.</span><span class="sxs-lookup"><span data-stu-id="23af1-110">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="23af1-111">Neis funktsioonivaldkondades kasutatakse ettevõtteid andmeturbe piirina.</span><span class="sxs-lookup"><span data-stu-id="23af1-111">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="23af1-112">Kasutajad pääsevad juurde ainult selle ettevõtte andmetele, millesse nad parasjagu sisse on loginud.</span><span class="sxs-lookup"><span data-stu-id="23af1-112">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="23af1-113">Kanali loomisel peate määrama, millise juriidilise isiku juurde kanal kuulub.</span><span class="sxs-lookup"><span data-stu-id="23af1-113">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="23af1-114">Uue juriidilise isiku loomine</span><span class="sxs-lookup"><span data-stu-id="23af1-114">Create a new legal entity</span></span>

<span data-ttu-id="23af1-115">Uue juriidilise isiku loomiseks Dynamics 365 Commerce'is toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="23af1-115">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="23af1-116">Avage navigatsioonipaneelil **Moodulid \> Peakontori seadistus \> Juriidilised isikud**.</span><span class="sxs-lookup"><span data-stu-id="23af1-116">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="23af1-117">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="23af1-117">On the action pane, select **New**.</span></span> <span data-ttu-id="23af1-118">Paan **Uus juriidiline isik** kuvatakse paremal.</span><span class="sxs-lookup"><span data-stu-id="23af1-118">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="23af1-119">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="23af1-119">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="23af1-120">Sisestage väärtus väljale **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="23af1-120">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="23af1-121">Sisestage või valige väärtus väljale **Riik/regioon**.</span><span class="sxs-lookup"><span data-stu-id="23af1-121">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="23af1-122">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="23af1-122">Select **OK**.</span></span> 

   ![Juriidilise isiku loomine](media/legal-entities.png)

1. <span data-ttu-id="23af1-124">Esitage jaotises **Üldine** juriidilise isiku kohta järgmised üldandmed.</span><span class="sxs-lookup"><span data-stu-id="23af1-124">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="23af1-125">Sisestage otsingunimi, kui otsingunimi on nõutav.</span><span class="sxs-lookup"><span data-stu-id="23af1-125">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="23af1-126">Otsingunimi on alternatiivne nimi, mida saab kasutada selle juriidilise isiku otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="23af1-126">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="23af1-127">Valige, kas seda juriidilist isikut kasutatakse konsolideeritud ettevõttena.</span><span class="sxs-lookup"><span data-stu-id="23af1-127">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="23af1-128">Valige, kas seda juriidilist isikut kasutatakse elimineerimise ettevõttena.</span><span class="sxs-lookup"><span data-stu-id="23af1-128">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="23af1-129">Valige üksusele **vaikekeel**.</span><span class="sxs-lookup"><span data-stu-id="23af1-129">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="23af1-130">Valige üksusele **ajavöönd**.</span><span class="sxs-lookup"><span data-stu-id="23af1-130">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="23af1-131">Tehke jaotises **Aadressid** valik **Muuda**, et sisestada aadressiteave, nagu tänavanimi, majanumber, sihtnumber ja linn.</span><span class="sxs-lookup"><span data-stu-id="23af1-131">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="23af1-132">Jaotisse **Kontaktteave** sisestage teave selliste sidepidamise viiside kohta nagu meiliaadressid, URL-id ja telefoninumbrid.</span><span class="sxs-lookup"><span data-stu-id="23af1-132">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="23af1-133">Sisestgae jaotisse **Seaduslik aruandlus** registreerimisnumbrid, mida kasutatakse seadusandlikuks aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="23af1-133">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="23af1-134">Sisestage jaotisse **Registreerimisnumbrid** mis tahes teave, mis on juriidilise isiku puhul nõutav.</span><span class="sxs-lookup"><span data-stu-id="23af1-134">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="23af1-135">Sisestage jaotisse **Pangakonto teave** juriidilise isiku pangakontod ja registreerimisnumbrid.</span><span class="sxs-lookup"><span data-stu-id="23af1-135">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="23af1-136">Sisestage jaotisesse **Väliskaubandus ja logistika** tarneteave juriidilise isiku kohta.</span><span class="sxs-lookup"><span data-stu-id="23af1-136">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="23af1-137">Jaotises **Numbriseeriad** saate vaadata numbriseeriaid, mis on seostatud juriidilise isikuga.</span><span class="sxs-lookup"><span data-stu-id="23af1-137">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="23af1-138">Alguses on see tühi.</span><span class="sxs-lookup"><span data-stu-id="23af1-138">This will be empty to start with.</span></span>
1. <span data-ttu-id="23af1-139">Jaotises **Armatuurlaua pilt** saate vaadata või muuta logo ja armatuurlaua pilti, mis on seostatud juriidilise isikuga.</span><span class="sxs-lookup"><span data-stu-id="23af1-139">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="23af1-140">Sisestage jaotisesse **Maksu registreerimine** registreerimisnumbrid, mida kasutatakse maksuhalduritele teatamiseks.</span><span class="sxs-lookup"><span data-stu-id="23af1-140">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="23af1-141">Sisestage jaotises **Maks 1099** juriidilisele isikule teave 1099.</span><span class="sxs-lookup"><span data-stu-id="23af1-141">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="23af1-142">Sisestage jaotisesse **Maksuteave** juriidilise isiku maksuteave.</span><span class="sxs-lookup"><span data-stu-id="23af1-142">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="23af1-143">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="23af1-143">Select **Save**.</span></span>

<span data-ttu-id="23af1-144">Järgmine pilt näitab näitliku juriidilise isiku üksikasju.</span><span class="sxs-lookup"><span data-stu-id="23af1-144">The following image shows details of an example legal entity.</span></span>

![Juriidilise isiku üldine jaotis](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="23af1-146">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="23af1-146">Additional resources</span></span>

[<span data-ttu-id="23af1-147">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="23af1-147">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="23af1-148">Organisatsioonihierarhia kavandamine</span><span class="sxs-lookup"><span data-stu-id="23af1-148">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="23af1-149">Organisatsiooni hierarhiad</span><span class="sxs-lookup"><span data-stu-id="23af1-149">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="23af1-150">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="23af1-150">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="23af1-151">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="23af1-151">Channel setup prerequisites</span></span>](channels-prerequisites.md)
