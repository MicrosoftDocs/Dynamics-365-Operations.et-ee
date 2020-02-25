---
title: Kanali seadistamise eeltingimused
description: Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce kanalite seadistamise eeltingimustest.
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
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002285"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="c3b9a-103">Kanali seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="c3b9a-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c3b9a-104">Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce kanali seadistamise eeltingimustest.</span><span class="sxs-lookup"><span data-stu-id="c3b9a-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c3b9a-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="c3b9a-105">Overview</span></span>

<span data-ttu-id="c3b9a-106">Enne Dynamics 365 Commerce'i kanali loomist tuleb täita mitu eeltingimuseks olevat ülesannet.</span><span class="sxs-lookup"><span data-stu-id="c3b9a-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="c3b9a-107">Järgmised eeltingimuseks olevate ülesannete loendid on korraldatud kanali tüübi järgi.</span><span class="sxs-lookup"><span data-stu-id="c3b9a-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="c3b9a-108">Mõned dokumendid on veel kirjutamisel ja lingid uuendatakse uue sisu avaldamisel.</span><span class="sxs-lookup"><span data-stu-id="c3b9a-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="c3b9a-109">Lähtestamine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-109">Initialization</span></span>

- [<span data-ttu-id="c3b9a-110">Algandmete lähtestamine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-110">Initialize seed data</span></span>](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="c3b9a-111">Kõigi kanalitüüpide jaoks nõutavad globaalsed eeltingimused</span><span class="sxs-lookup"><span data-stu-id="c3b9a-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="c3b9a-112">Juriidilise isiku struktuuri määratlemine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="c3b9a-113">Organisatsiooni hierarhia konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="c3b9a-114">Lao seadistamine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="c3b9a-115">Käibemaksu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-115">Configure sales tax</span></span>](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c3b9a-116">Meiliteatiste profiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="c3b9a-117">Numbriseeriate häälestamine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-117">Set up number sequences</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c3b9a-118">Vaikekliendi ja aadressiraamatu seadistamine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="c3b9a-119">Jaemüügikanali eeltingimused</span><span class="sxs-lookup"><span data-stu-id="c3b9a-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="c3b9a-120">Teabekoodid ja teabekoodide grupid</span><span class="sxs-lookup"><span data-stu-id="c3b9a-120">Info codes and info code groups</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c3b9a-121">Jaemüügi funktsiooniprofiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="c3b9a-122">Töötaja aadressiraamatu seadistamine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="c3b9a-123">Ekraanipaigutuse häälestamine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-123">Set up a screen layout</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c3b9a-124">Riistvarajaama seadistamine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-124">Set up a hardware station</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="c3b9a-125">Kõnekeskuse kanali eeltingimused</span><span class="sxs-lookup"><span data-stu-id="c3b9a-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="c3b9a-126">Kõnekeskuse parameetrid</span><span class="sxs-lookup"><span data-stu-id="c3b9a-126">Call center parameters</span></span>
- <span data-ttu-id="c3b9a-127">Kõnekeskuse tagasimakseviisid</span><span class="sxs-lookup"><span data-stu-id="c3b9a-127">Call center refund methods</span></span>
- <span data-ttu-id="c3b9a-128">Rentimise tüübid</span><span class="sxs-lookup"><span data-stu-id="c3b9a-128">Rental types</span></span>
- <span data-ttu-id="c3b9a-129">Makseteenused</span><span class="sxs-lookup"><span data-stu-id="c3b9a-129">Payment services</span></span>
- <span data-ttu-id="c3b9a-130">Tellimuse ooteloleku koodid</span><span class="sxs-lookup"><span data-stu-id="c3b9a-130">Order hold codes</span></span>

## <a name="online-channel-prerequisites"></a><span data-ttu-id="c3b9a-131">Veebikanali eeltingimused</span><span class="sxs-lookup"><span data-stu-id="c3b9a-131">Online channel prerequisites</span></span>

- [<span data-ttu-id="c3b9a-132">Veebipõhise funktsiooniprofiili loomine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-132">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="c3b9a-133">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c3b9a-133">Additional resources</span></span>

[<span data-ttu-id="c3b9a-134">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="c3b9a-134">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c3b9a-135">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="c3b9a-135">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c3b9a-136">Organisatsiooni hierarhiate seadistamine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="c3b9a-137">Juriidiliste isikute loomine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-137">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="c3b9a-138">Jaemüügikanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-138">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="c3b9a-139">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="c3b9a-139">Set up an online channel</span></span>](channel-setup-online.md)