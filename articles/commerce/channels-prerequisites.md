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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0705efac4659f96ebca1c67f6f0ab8d23c99d81e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997696"
---
# <a name="channel-setup-prerequisites"></a>Kanali seadistamise eeltingimused


[!include [banner](includes/banner.md)]

Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce kanali seadistamise eeltingimustest.

## <a name="overview"></a>Ülevaade

Enne Dynamics 365 Commerce'i kanali loomist tuleb täita mitu eeltingimuseks olevat ülesannet. Järgmised eeltingimuseks olevate ülesannete loendid on korraldatud kanali tüübi järgi.

> [!NOTE]
> Mõned dokumendid on veel kirjutamisel ja lingid uuendatakse uue sisu avaldamisel.

## <a name="initialization"></a>Lähtestamine

- [Algandmete lähtestamine](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Kõigi kanalitüüpide jaoks nõutavad globaalsed eeltingimused

- [Juriidilise isiku struktuuri määratlemine ja konfigureerimine](channels-legal-entities.md) 
- [Organisatsiooni hierarhia konfigureerimine](channels-org-hierarchies.md)
- [Lao seadistamine](channels-setup-warehouse.md)
- [Käibemaksu konfigureerimine](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [Meiliteatiste profiili seadistamine](email-notification-profiles.md)
- [Numbriseeriate häälestamine](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [Vaikekliendi ja aadressiraamatu seadistamine](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Jaemüügikanali eeltingimused

- [Teabekoodid ja teabekoodide grupid](info-codes-retail.md)
- [Jaemüügi funktsiooniprofiili seadistamine](retail-functionality-profile.md)
- [Töötaja aadressiraamatu seadistamine](new-address-book.md)
- [Ekraanipaigutuse häälestamine](pos-screen-layouts.md)
- [Riistvarajaama seadistamine](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>Kõnekeskuse kanali eeltingimused

- Kõnekeskuse parameetrid
- [Kõnekeskuse tellimise ja tagasimakse makseviisid](work-with-payments.md)
- [Kõnekeskuse tarneviisid ja tasud](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>Võrgukanali eeltingimused

- [Funktsiooniprofiili loomine võrgus](online-functionality-profile.md)

## <a name="additional-resources"></a>Lisaressursid

[Kanalite ülevaade](channels-overview.md)

[Organisatsioonide ja organisatsioonihierarhiate ülevaade](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organisatsiooni hierarhiate seadistamine](channels-org-hierarchies.md)

[Juriidiliste isikute loomine](channels-legal-entities.md)

[Jaemüügikanali seadistamine](channel-setup-retail.md)
    
[Veebikanali häälestamine](channel-setup-online.md)
