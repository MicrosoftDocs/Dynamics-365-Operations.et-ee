---
title: Juriidiliste isikute loomine
description: See teema kirjeldab, kuidas luua Microsoft Dynamics 365 Commerce'is juriidilisi isikuid, mis tulevad enne kanalite loomist luua ja konfigureerida.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 016b67631a53139d12d65dfaf594f49b030326b1
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478208"
---
# <a name="create-legal-entities"></a><span data-ttu-id="2113a-103">Juriidiliste isikute loomine</span><span class="sxs-lookup"><span data-stu-id="2113a-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2113a-104">See teema kirjeldab, kuidas luua Microsoft Dynamics 365 Commerce'is juriidilisi isikuid, mis tulevad enne kanalite loomist luua ja konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="2113a-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="2113a-105">Juriidiline isik on registreeritud või õigusliku struktuuriga organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="2113a-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="2113a-106">Juriidilised isikud võivad sõlmida juriidilisi lepinguid ja on kohustatud koostama oma tegevuse kohta aruandeid.</span><span class="sxs-lookup"><span data-stu-id="2113a-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="2113a-107">Ettevõte on juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="2113a-107">A company is a type of legal entity.</span></span> <span data-ttu-id="2113a-108">Ettevõtted on praegu ainsad juriidilised isikud, mida saate luua, ja iga juriidiline isik on seostatud ettevõtte ID-ga.</span><span class="sxs-lookup"><span data-stu-id="2113a-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="2113a-109">See seos on olemas, kuna mõni programmi funktsioonivaldkond kasutab oma andmemudelis ettevõtte ID-d või atribuuti *DataAreaId*.</span><span class="sxs-lookup"><span data-stu-id="2113a-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="2113a-110">Neis funktsioonivaldkondades kasutatakse ettevõtteid andmeturbe piirina.</span><span class="sxs-lookup"><span data-stu-id="2113a-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="2113a-111">Kasutajad pääsevad juurde ainult selle ettevõtte andmetele, millesse nad parasjagu sisse on loginud.</span><span class="sxs-lookup"><span data-stu-id="2113a-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="2113a-112">Kanali loomisel peate määrama, millise juriidilise isiku juurde kanal kuulub.</span><span class="sxs-lookup"><span data-stu-id="2113a-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="2113a-113">Uue juriidilise isiku loomine</span><span class="sxs-lookup"><span data-stu-id="2113a-113">Create a new legal entity</span></span>

<span data-ttu-id="2113a-114">Uue juriidilise isiku loomiseks Dynamics 365 Commerce'is toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2113a-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="2113a-115">Avage navigatsioonipaneelil **Moodulid \> Peakontori seadistus \> Juriidilised isikud**.</span><span class="sxs-lookup"><span data-stu-id="2113a-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="2113a-116">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2113a-116">On the action pane, select **New**.</span></span> <span data-ttu-id="2113a-117">Paan **Uus juriidiline isik** kuvatakse paremal.</span><span class="sxs-lookup"><span data-stu-id="2113a-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="2113a-118">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="2113a-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="2113a-119">Sisestage väärtus väljale **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="2113a-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="2113a-120">Sisestage või valige väärtus väljale **Riik/regioon**.</span><span class="sxs-lookup"><span data-stu-id="2113a-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="2113a-121">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2113a-121">Select **OK**.</span></span> 

   ![Juriidilise isiku loomine](media/legal-entities.png)

1. <span data-ttu-id="2113a-123">Esitage jaotises **Üldine** juriidilise isiku kohta järgmised üldandmed.</span><span class="sxs-lookup"><span data-stu-id="2113a-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="2113a-124">Sisestage otsingunimi, kui otsingunimi on nõutav.</span><span class="sxs-lookup"><span data-stu-id="2113a-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="2113a-125">Otsingunimi on alternatiivne nimi, mida saab kasutada selle juriidilise isiku otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="2113a-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="2113a-126">Valige, kas seda juriidilist isikut kasutatakse konsolideeritud ettevõttena.</span><span class="sxs-lookup"><span data-stu-id="2113a-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="2113a-127">Valige, kas seda juriidilist isikut kasutatakse elimineerimise ettevõttena.</span><span class="sxs-lookup"><span data-stu-id="2113a-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="2113a-128">Valige üksusele **vaikekeel**.</span><span class="sxs-lookup"><span data-stu-id="2113a-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="2113a-129">Valige üksusele **ajavöönd**.</span><span class="sxs-lookup"><span data-stu-id="2113a-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="2113a-130">Tehke jaotises **Aadressid** valik **Muuda**, et sisestada aadressiteave, nagu tänavanimi, majanumber, sihtnumber ja linn.</span><span class="sxs-lookup"><span data-stu-id="2113a-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="2113a-131">Jaotisse **Kontaktteave** sisestage teave selliste sidepidamise viiside kohta nagu meiliaadressid, URL-id ja telefoninumbrid.</span><span class="sxs-lookup"><span data-stu-id="2113a-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="2113a-132">Sisestgae jaotisse **Seaduslik aruandlus** registreerimisnumbrid, mida kasutatakse seadusandlikuks aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="2113a-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="2113a-133">Sisestage jaotisse **Registreerimisnumbrid** mis tahes teave, mis on juriidilise isiku puhul nõutav.</span><span class="sxs-lookup"><span data-stu-id="2113a-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="2113a-134">Sisestage jaotisse **Pangakonto teave** juriidilise isiku pangakontod ja registreerimisnumbrid.</span><span class="sxs-lookup"><span data-stu-id="2113a-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="2113a-135">Sisestage jaotisesse **Väliskaubandus ja logistika** tarneteave juriidilise isiku kohta.</span><span class="sxs-lookup"><span data-stu-id="2113a-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="2113a-136">Jaotises **Numbriseeriad** saate vaadata numbriseeriaid, mis on seostatud juriidilise isikuga.</span><span class="sxs-lookup"><span data-stu-id="2113a-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="2113a-137">Alguses on see tühi.</span><span class="sxs-lookup"><span data-stu-id="2113a-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="2113a-138">Jaotises **Armatuurlaua pilt** saate vaadata või muuta logo ja armatuurlaua pilti, mis on seostatud juriidilise isikuga.</span><span class="sxs-lookup"><span data-stu-id="2113a-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="2113a-139">Sisestage jaotisesse **Maksu registreerimine** registreerimisnumbrid, mida kasutatakse maksuhalduritele teatamiseks.</span><span class="sxs-lookup"><span data-stu-id="2113a-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="2113a-140">Sisestage jaotises **Maks 1099** juriidilisele isikule teave 1099.</span><span class="sxs-lookup"><span data-stu-id="2113a-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="2113a-141">Sisestage jaotisesse **Maksuteave** juriidilise isiku maksuteave.</span><span class="sxs-lookup"><span data-stu-id="2113a-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="2113a-142">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2113a-142">Select **Save**.</span></span>

<span data-ttu-id="2113a-143">Järgmine pilt näitab näitliku juriidilise isiku üksikasju.</span><span class="sxs-lookup"><span data-stu-id="2113a-143">The following image shows details of an example legal entity.</span></span>

![Juriidilise isiku üldine jaotis](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="2113a-145">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2113a-145">Additional resources</span></span>

[<span data-ttu-id="2113a-146">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="2113a-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="2113a-147">Organisatsioonihierarhia kavandamine</span><span class="sxs-lookup"><span data-stu-id="2113a-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="2113a-148">Organisatsiooni hierarhiad</span><span class="sxs-lookup"><span data-stu-id="2113a-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="2113a-149">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="2113a-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="2113a-150">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="2113a-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
