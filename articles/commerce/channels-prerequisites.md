---
title: Kanali seadistamise eeltingimused
description: Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce kanalite seadistamise eeltingimustest.
author: samjarawan
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 33fcead6c0b08db17f24b638376a23b8b6024a5b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800515"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="09e4f-103">Kanali häälestuse eeltingimused</span><span class="sxs-lookup"><span data-stu-id="09e4f-103">Channel setup prerequisites</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="09e4f-104">Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce kanalite seadistamise eeltingimustest.</span><span class="sxs-lookup"><span data-stu-id="09e4f-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="09e4f-105">Enne Dynamics 365 Commerce'i kanali loomist tuleb täita mitu eeltingimuseks olevat ülesannet.</span><span class="sxs-lookup"><span data-stu-id="09e4f-105">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="09e4f-106">Järgmised eeltingimuseks olevate ülesannete loendid on korraldatud kanali tüübi järgi.</span><span class="sxs-lookup"><span data-stu-id="09e4f-106">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="09e4f-107">Mõned dokumendid on veel kirjutamisel ja lingid uuendatakse uue sisu avaldamisel.</span><span class="sxs-lookup"><span data-stu-id="09e4f-107">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="09e4f-108">Lähtestamine</span><span class="sxs-lookup"><span data-stu-id="09e4f-108">Initialization</span></span>

- [<span data-ttu-id="09e4f-109">Algandmete lähtestamine</span><span class="sxs-lookup"><span data-stu-id="09e4f-109">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="09e4f-110">Kõigi kanalitüüpide jaoks nõutavad globaalsed eeltingimused</span><span class="sxs-lookup"><span data-stu-id="09e4f-110">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="09e4f-111">Juriidilise isiku struktuuri määratlemine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="09e4f-111">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="09e4f-112">Organisatsiooni hierarhia konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="09e4f-112">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="09e4f-113">Lao seadistamine</span><span class="sxs-lookup"><span data-stu-id="09e4f-113">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="09e4f-114">Käibemaksu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="09e4f-114">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="09e4f-115">Meiliteatiste profiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="09e4f-115">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="09e4f-116">Numbriseeriate häälestamine</span><span class="sxs-lookup"><span data-stu-id="09e4f-116">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="09e4f-117">Vaikekliendi ja aadressiraamatu seadistamine</span><span class="sxs-lookup"><span data-stu-id="09e4f-117">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="09e4f-118">Jaemüügikanali eeltingimused</span><span class="sxs-lookup"><span data-stu-id="09e4f-118">Retail channel prerequisites</span></span>

- [<span data-ttu-id="09e4f-119">Teabekoodid ja teabekoodide grupid</span><span class="sxs-lookup"><span data-stu-id="09e4f-119">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="09e4f-120">Jaemüügi funktsiooniprofiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="09e4f-120">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="09e4f-121">Töötaja aadressiraamatu seadistamine</span><span class="sxs-lookup"><span data-stu-id="09e4f-121">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="09e4f-122">Ekraanipaigutuse häälestamine</span><span class="sxs-lookup"><span data-stu-id="09e4f-122">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="09e4f-123">Riistvarajaama seadistamine</span><span class="sxs-lookup"><span data-stu-id="09e4f-123">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="09e4f-124">Kõnekeskuse kanali eeltingimused</span><span class="sxs-lookup"><span data-stu-id="09e4f-124">Call Center channel prerequisites</span></span>

- <span data-ttu-id="09e4f-125">Kõnekeskuse parameetrid</span><span class="sxs-lookup"><span data-stu-id="09e4f-125">Call center parameters</span></span>
- [<span data-ttu-id="09e4f-126">Kõnekeskuse tellimise ja tagasimakse makseviisid</span><span class="sxs-lookup"><span data-stu-id="09e4f-126">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="09e4f-127">Kõnekeskuse tarneviisid ja tasud</span><span class="sxs-lookup"><span data-stu-id="09e4f-127">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="09e4f-128">Võrgukanali eeltingimused</span><span class="sxs-lookup"><span data-stu-id="09e4f-128">Online channel prerequisites</span></span>

- [<span data-ttu-id="09e4f-129">Funktsiooniprofiili loomine võrgus</span><span class="sxs-lookup"><span data-stu-id="09e4f-129">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="09e4f-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="09e4f-130">Additional resources</span></span>

[<span data-ttu-id="09e4f-131">Kanalite ülevaade</span><span class="sxs-lookup"><span data-stu-id="09e4f-131">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="09e4f-132">Organisatsioonide ja organisatsioonihierarhiate ülevaade</span><span class="sxs-lookup"><span data-stu-id="09e4f-132">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="09e4f-133">Organisatsiooni hierarhiate seadistamine</span><span class="sxs-lookup"><span data-stu-id="09e4f-133">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="09e4f-134">Juriidiliste isikute loomine</span><span class="sxs-lookup"><span data-stu-id="09e4f-134">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="09e4f-135">Jaemüügikanali seadistamine</span><span class="sxs-lookup"><span data-stu-id="09e4f-135">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="09e4f-136">Veebikanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="09e4f-136">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
