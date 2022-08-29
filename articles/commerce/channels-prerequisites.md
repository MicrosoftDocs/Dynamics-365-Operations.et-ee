---
title: Kanali häälestuse eeltingimused
description: Selles artiklis antakse ülevaade kanalite häälestamise eeltingimustest rakenduses Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 98ca2dc4691534853467c1680890199d08bc4e79
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282291"
---
# <a name="channel-setup-prerequisites"></a>Kanali häälestuse eeltingimused

[!include [banner](includes/banner.md)]

Selles artiklis antakse ülevaade kanali häälestuse eeltingimustest rakenduses Microsoft Dynamics 365 Commerce.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
