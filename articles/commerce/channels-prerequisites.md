---
title: Kanali seadistamise eeltingimused
description: Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce kanalite seadistamise eeltingimustest.
author: samjarawan
manager: annbe
ms.date: 02/21/2020
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
ms.openlocfilehash: 0da0457240cf12686fff2fa929c7fb510c11f242
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113778"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="29157-103">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="29157-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="29157-104">Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce kanali seadistamise eeltingimustest.</span><span class="sxs-lookup"><span data-stu-id="29157-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="29157-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="29157-105">Overview</span></span>

<span data-ttu-id="29157-106">Enne Dynamics 365 Commerce'i kanali loomist tuleb täita mitu eeltingimuseks olevat ülesannet.</span><span class="sxs-lookup"><span data-stu-id="29157-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="29157-107">Järgmised eeltingimuseks olevate ülesannete loendid on korraldatud kanali tüübi järgi.</span><span class="sxs-lookup"><span data-stu-id="29157-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="29157-108">Mõned dokumendid on veel kirjutamisel ja lingid uuendatakse uue sisu avaldamisel.</span><span class="sxs-lookup"><span data-stu-id="29157-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="29157-109">Lähtestamine</span><span class="sxs-lookup"><span data-stu-id="29157-109">Initialization</span></span>

- [<span data-ttu-id="29157-110">Algandmete lähtestamine</span><span class="sxs-lookup"><span data-stu-id="29157-110">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="29157-111">Kõigi kanalitüüpide jaoks nõutavad globaalsed eeltingimused</span><span class="sxs-lookup"><span data-stu-id="29157-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="29157-112">Juriidilise isiku struktuuri määratlemine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="29157-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="29157-113">Organisatsiooni hierarhia konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="29157-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="29157-114">Lao seadistamine</span><span class="sxs-lookup"><span data-stu-id="29157-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="29157-115">Käibemaksu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="29157-115">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="29157-116">Meiliteatiste profiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="29157-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="29157-117">Numbriseeriate häälestamine</span><span class="sxs-lookup"><span data-stu-id="29157-117">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="29157-118">Vaikekliendi ja aadressiraamatu seadistamine</span><span class="sxs-lookup"><span data-stu-id="29157-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="29157-119">Jaemüügikanali eeltingimused</span><span class="sxs-lookup"><span data-stu-id="29157-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="29157-120">Teabekoodid ja teabekoodide grupid</span><span class="sxs-lookup"><span data-stu-id="29157-120">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="29157-121">Jaemüügi funktsiooniprofiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="29157-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="29157-122">Töötaja aadressiraamatu seadistamine</span><span class="sxs-lookup"><span data-stu-id="29157-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="29157-123">Ekraanipaigutuse häälestamine</span><span class="sxs-lookup"><span data-stu-id="29157-123">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="29157-124">Riistvarajaama seadistamine</span><span class="sxs-lookup"><span data-stu-id="29157-124">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="29157-125">Kõnekeskuse kanali eeltingimused</span><span class="sxs-lookup"><span data-stu-id="29157-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="29157-126">Kõnekeskuse parameetrid</span><span class="sxs-lookup"><span data-stu-id="29157-126">Call center parameters</span></span>
- [<span data-ttu-id="29157-127">Kõnekeskuse tellimise ja tagasimakse makseviisid</span><span class="sxs-lookup"><span data-stu-id="29157-127">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="29157-128">Kõnekeskuse tarneviisid ja tasud</span><span class="sxs-lookup"><span data-stu-id="29157-128">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="29157-129">Võrgukanali eeltingimused</span><span class="sxs-lookup"><span data-stu-id="29157-129">Online channel prerequisites</span></span>

- [<span data-ttu-id="29157-130">Funktsiooniprofiili loomine võrgus</span><span class="sxs-lookup"><span data-stu-id="29157-130">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="29157-131">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="29157-131">Additional resources</span></span>

[<span data-ttu-id="29157-132">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="29157-132">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="29157-133">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="29157-133">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="29157-134">Organisatsiooni hierarhiate seadistamine</span><span class="sxs-lookup"><span data-stu-id="29157-134">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="29157-135">Juriidiliste isikute loomine</span><span class="sxs-lookup"><span data-stu-id="29157-135">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="29157-136">Jaemüügikanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="29157-136">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="29157-137">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="29157-137">Set up an online channel</span></span>](channel-setup-online.md)
