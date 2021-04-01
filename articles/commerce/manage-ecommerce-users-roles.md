---
title: E-kaubanduse kasutajate ja rollide haldamine
description: See teema selgitab, kuidas anda kasutajatele juurdepääs teie Microsoft Dynamics 365 Commerce’i saidi autorluse keskkonnale.
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a2235a43fd69adddeaba4c29305435db0fa39d64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255915"
---
# <a name="manage-e-commerce-users-and-roles"></a><span data-ttu-id="c536e-103">E-kaubanduse kasutajate ja rollide haldamine</span><span class="sxs-lookup"><span data-stu-id="c536e-103">Manage e-Commerce users and roles</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c536e-104">See teema selgitab, kuidas anda kasutajatele juurdepääs teie Microsoft Dynamics 365 Commerce’i saidi autorluse keskkonnale.</span><span class="sxs-lookup"><span data-stu-id="c536e-104">This topic explains how to grant users access to the authoring environment for your Microsoft Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="c536e-105">Et aidata kontrollida kasutajate juurdepääsu ja anda kasutajatele luba konkreetsete ülesannete täitmiseks, kasutab saidi autorluse keskkond rakenduses Microsoft Azure Active Directory (Azure AD) loodud turvagruppe.</span><span class="sxs-lookup"><span data-stu-id="c536e-105">To help control user access and grant users permission to perform specific tasks, the site authoring environment uses security groups that you create in Microsoft Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="c536e-106">Kõigepealt määrate autorluse keskkonnas igale rollile Azure AD-st uue või olemasoleva turvagrupi.</span><span class="sxs-lookup"><span data-stu-id="c536e-106">You first assign a new or existing security group from Azure AD to each role in the authoring environment.</span></span> <span data-ttu-id="c536e-107">Seejärel annate või tühistate individuaalsete kasutajate load, lisades need kasutajad vastavasse turvagruppi või eemaldades need turvarühmast.</span><span class="sxs-lookup"><span data-stu-id="c536e-107">You then grant or revoke permissions for individual users by either adding those users to an appropriate security group or removing them from a security group.</span></span>

## <a name="overview-of-roles-in-the-authoring-environment"></a><span data-ttu-id="c536e-108">Autorluse keskkonna rollide ülevaade</span><span class="sxs-lookup"><span data-stu-id="c536e-108">Overview of roles in the authoring environment</span></span>

<span data-ttu-id="c536e-109">Rakenduse Dynamics 365 for Commerce autorluse keskkond toetab järgmisi rolle.</span><span class="sxs-lookup"><span data-stu-id="c536e-109">The Dynamics 365 for Commerce authoring environment supports the following roles.</span></span>

| <span data-ttu-id="c536e-110">Roll</span><span class="sxs-lookup"><span data-stu-id="c536e-110">Role</span></span>                 | <span data-ttu-id="c536e-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c536e-111">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="c536e-112">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="c536e-112">System Administrator</span></span> | <span data-ttu-id="c536e-113">Selle rolliga kasutajatel on kõik õigused kõigi tööriistade ja kõigi hinnangute ning arvustuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="c536e-113">Users who have this role have all privileges for all tools, and for all ratings and reviews.</span></span> <span data-ttu-id="c536e-114">Nad saavad luua ka saite.</span><span class="sxs-lookup"><span data-stu-id="c536e-114">They can also create sites.</span></span> |
| <span data-ttu-id="c536e-115">Administraator</span><span class="sxs-lookup"><span data-stu-id="c536e-115">Administrator</span></span>   | <span data-ttu-id="c536e-116">Selle rolliga kasutajad omavad kõiki privileege kõikide antud saidi struktuuri tööriistadele ja RnR-ile.</span><span class="sxs-lookup"><span data-stu-id="c536e-116">Users who have this role have all privileges for all tools and RnR in a given site structure.</span></span> |
| <span data-ttu-id="c536e-117">Veebitootja</span><span class="sxs-lookup"><span data-stu-id="c536e-117">Web Producer</span></span>         | <span data-ttu-id="c536e-118">Selle rolliga kasutajad saavad luua lehti, fragmente ja malle, laadida üles ja hallata varasid ning rikastada tooteid ja kategooriaid.</span><span class="sxs-lookup"><span data-stu-id="c536e-118">Users who have this role can create pages, fragments and templates, upload and manage assets, and enrich products and categories.</span></span> |
| <span data-ttu-id="c536e-119">Lugeja</span><span class="sxs-lookup"><span data-stu-id="c536e-119">Reader</span></span>               | <span data-ttu-id="c536e-120">Selle rolliga kasutajad saavad vaadata lehti, malle, varasid, fragmente, paigutusi ja sätteid, kuid ei tohi teha muudatusi.</span><span class="sxs-lookup"><span data-stu-id="c536e-120">Users who have this role can view pages, templates, assets, fragments, layouts and settings, but may not make changes.</span></span> |
| <span data-ttu-id="c536e-121">RnR-i moderaator</span><span class="sxs-lookup"><span data-stu-id="c536e-121">RnR Moderator</span></span>        | <span data-ttu-id="c536e-122">Selle rolliga kasutajad saavad hallata toote arvustusi.</span><span class="sxs-lookup"><span data-stu-id="c536e-122">Users who have this role can moderate product reviews.</span></span> |

## <a name="system-administrator-role"></a><span data-ttu-id="c536e-123">Süsteemiadministraatori roll</span><span class="sxs-lookup"><span data-stu-id="c536e-123">System Administrator role</span></span>

<span data-ttu-id="c536e-124">Rakenduse Dynamics 365 Commerce ettevalmistamisel Microsoft Dynamicsi teenuse Lifecycle Services (LCS) keskkonnas, küsitakse teilt rolli **Süsteemiadministraator** jaoks turvagrupi määramist.</span><span class="sxs-lookup"><span data-stu-id="c536e-124">When you provision Dynamics 365 Commerce in the Microsoft Dynamics Lifecycle Services (LCS) environment, you're asked to provide a security group for the **System Administrator** role.</span></span> <span data-ttu-id="c536e-125">See roll rakendub seejärel automaatselt kõigile saitidele, mille konfigureeritavas keskkonnas loote.</span><span class="sxs-lookup"><span data-stu-id="c536e-125">This role is then automatically applied to all sites that you create in the environment that you're configuring.</span></span> <span data-ttu-id="c536e-126">Selle rolli turvagruppi saab uuendada ainult LCS-is.</span><span class="sxs-lookup"><span data-stu-id="c536e-126">The security group for this role can be updated only in LCS.</span></span> <span data-ttu-id="c536e-127">Kõikide saitide lehel **Saidihaldus** ilmub see kirjutuskaitstuna ja ainult teavitaval eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="c536e-127">On the **Site Administration** page for all sites, it appears as read-only and is for informational purposes only.</span></span>

## <a name="administrator-role"></a><span data-ttu-id="c536e-128">Administraatori roll</span><span class="sxs-lookup"><span data-stu-id="c536e-128">Administrator role</span></span>

<span data-ttu-id="c536e-129">Commerce’is uue saidi loomisel küsitakse teilt rolli **Administraator** jaoks turvagrupi määramist.</span><span class="sxs-lookup"><span data-stu-id="c536e-129">When you create a new site in Commerce, you're asked to provide a security group for the **Administrator** role.</span></span> <span data-ttu-id="c536e-130">Vaadake selles teemas eelnevalt toodud tabelit selle rolli antavate lubade ülevaateks.</span><span class="sxs-lookup"><span data-stu-id="c536e-130">See the table earlier in this topic for an overview of the permissions that this role grants.</span></span>

## <a name="add-or-update-security-groups"></a><span data-ttu-id="c536e-131">Turvagruppide lisamine või värskendamine</span><span class="sxs-lookup"><span data-stu-id="c536e-131">Add or update security groups</span></span>

<span data-ttu-id="c536e-132">Pärast saidi loomist pääsevad selle saidi autoriseerimise keskkonnale juurde ainult kasutajad, kes on turvagruppides, mis on seotud rollidega **Süsteemiadministraator** ja **Administraator**.</span><span class="sxs-lookup"><span data-stu-id="c536e-132">After your site is created, only users who are in the security groups that are associated with the **System Administrator** and **Administrator** roles can access the authoring environment for that site.</span></span> <span data-ttu-id="c536e-133">Kasutajatele rollide **Veebitootja**, **RnR-i moderaator** ja **Lugeja** määramiseks peate määrama nendele rollidele turvagrupid.</span><span class="sxs-lookup"><span data-stu-id="c536e-133">To assign users to the **Web Producer**, **RnR Moderator**, and **Reader** roles, you must assign security groups to those roles.</span></span> <span data-ttu-id="c536e-134">Rollile turvagrupi lisamiseks või hetkel rollile määratud turvagrupi uuendamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="c536e-134">To add a security group to a role, or to update a security group that is currently assigned to a role, follow these steps.</span></span>

1. <span data-ttu-id="c536e-135">Avage sait, mida soovite uuendada.</span><span class="sxs-lookup"><span data-stu-id="c536e-135">Go to the site that you want to update.</span></span>
1. <span data-ttu-id="c536e-136">Avage jaotises **Saidihaldus** leht **Turve**.</span><span class="sxs-lookup"><span data-stu-id="c536e-136">In **Site management**, open the **Security** page.</span></span>
1. <span data-ttu-id="c536e-137">Valige muutmiseks roll.</span><span class="sxs-lookup"><span data-stu-id="c536e-137">Select the role to modify.</span></span>
1. <span data-ttu-id="c536e-138">Lisage rollidele turvagrupid või eemaldage rollidelt turvagrupid.</span><span class="sxs-lookup"><span data-stu-id="c536e-138">Add security groups to roles, or remove security groups from roles.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c536e-139">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c536e-139">Additional resources</span></span>

[<span data-ttu-id="c536e-140">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="c536e-140">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="c536e-141">Saidi jaoks otsingumootori optimeerimise (SEO) kaalutlused</span><span class="sxs-lookup"><span data-stu-id="c536e-141">Search engine optimization (SEO) considerations for your site</span></span>](search-engine-optimization-considerations.md)

[<span data-ttu-id="c536e-142">Sisu turbepoliitika (CSP) haldamine</span><span class="sxs-lookup"><span data-stu-id="c536e-142">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]