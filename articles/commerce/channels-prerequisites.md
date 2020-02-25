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
# <a name="channel-setup-prerequisites"></a>Kanali seadistamise eeltingimused


[!include [banner](includes/banner.md)]

Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce kanali seadistamise eeltingimustest.

## <a name="overview"></a>Ülevaade

Enne Dynamics 365 Commerce'i kanali loomist tuleb täita mitu eeltingimuseks olevat ülesannet. Järgmised eeltingimuseks olevate ülesannete loendid on korraldatud kanali tüübi järgi.

> [!NOTE]
> Mõned dokumendid on veel kirjutamisel ja lingid uuendatakse uue sisu avaldamisel.

## <a name="initialization"></a>Lähtestamine

- [Algandmete lähtestamine](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Kõigi kanalitüüpide jaoks nõutavad globaalsed eeltingimused

- [Juriidilise isiku struktuuri määratlemine ja konfigureerimine](channels-legal-entities.md) 
- [Organisatsiooni hierarhia konfigureerimine](channels-org-hierarchies.md)
- [Lao seadistamine](channels-setup-warehouse.md)
- [Käibemaksu konfigureerimine](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [Meiliteatiste profiili seadistamine](email-notification-profiles.md)
- [Numbriseeriate häälestamine](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [Vaikekliendi ja aadressiraamatu seadistamine](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Jaemüügikanali eeltingimused

- [Teabekoodid ja teabekoodide grupid](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [Jaemüügi funktsiooniprofiili seadistamine](retail-functionality-profile.md)
- [Töötaja aadressiraamatu seadistamine](new-address-book.md)
- [Ekraanipaigutuse häälestamine](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [Riistvarajaama seadistamine](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a>Kõnekeskuse kanali eeltingimused

- Kõnekeskuse parameetrid
- Kõnekeskuse tagasimakseviisid
- Rentimise tüübid
- Makseteenused
- Tellimuse ooteloleku koodid

## <a name="online-channel-prerequisites"></a>Veebikanali eeltingimused

- [Veebipõhise funktsiooniprofiili loomine](online-functionality-profile.md)

## <a name="additional-resources"></a>Lisaressursid

[Kanalite ülevaade](channels-overview.md)

[Organisatsioonide ja organisatsioonihierarhiate ülevaade](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organisatsiooni hierarhiate seadistamine](channels-org-hierarchies.md)

[Juriidiliste isikute loomine](channels-legal-entities.md)

[Jaemüügikanali seadistamine](channel-setup-retail.md)
    
[Veebikanali häälestamine](channel-setup-online.md)
