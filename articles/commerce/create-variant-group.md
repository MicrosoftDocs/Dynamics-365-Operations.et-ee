---
title: Variandi grupi loomine
description: See teema kirjeldab, kuidas luua Microsoftis Dynamics 365 Commerce'is tootele suuruse-, stiili- või värvivariandi grupp.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5d9279e1076796bb455429e5ff004c89ec5829e7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411672"
---
# <a name="create-a-variant-group"></a>Variandi grupi loomine


[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas luua Microsoftis Dynamics 365 Commerce'is tootele suuruse-, stiili- või värvivariandi grupp.

## <a name="overview"></a>Ülevaade

Dynamics 365 Commerce toetab mitmeid toodete variante. See on ideaalne erinevate tootekategooriate jaoks variandigruppide seadistamiseks. Näiteks saab t-särkide puhul luua suuruse grupi suurustega XS, S, M, L ja XL või värvigrupi, mis sisaldaks toote kõiki saadaolevaid värve. Variandigrupid tuleb lisada enne toodete lisamist.

Selles teemas luuakse ja konfigureeritakse suuruse grupp. Sarnase toiminguga saab lisada ja konfigureerida ka stiili- ja värvigruppe.

## <a name="create-a-size-group"></a>Suuruse grupi loomine

Suuruse grupi loomiseks tehke järgmist.
 
1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Tooted ja kategooriad \> Variandi grupid \> Suuruse grupid**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage kasti **Suuruse grupp** suuruse grupile nimi.
1. Sisestage väljale **Kirjeldus** sobiv kirjeldus.
1. Valige toimingupaanil nupp **Salvesta**.

## <a name="add-attributes-to-the-size-group"></a>Atribuutide lisamine suuruse grupile

Suuruse grupile atribuutide lisamiseks toimige järgmiselt.

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Tooted ja kategooriad \> Variandi grupid \> Suuruse grupid**
1. Valige navigeerimispaanil suuruse grupp.
1. Valige jaotises **Suuruse grupi read** suvand **Lisa**.
1. Sisestage kasti **Suurus** suurust esindav string (näiteks "XL").
1. Sisestage väljale **Suuruse nimi** suuruse nimi (nt "Eriti suur").
1. Sisestage väljale **Täiendamise kaal** täiendamise kaalu tähistav number.
1. Sisestage väljale **Triipkoodi number** triipkoodi tähistav number.
1. Sisestage väljale **Kuva järjekord** kuva järjekorda tähistav number.
1. Kui olete suuruse lisamise lõpetanud, valige tegevuspaanilt **Salvesta**.

Järgmine pilt näitab "vabaajasärkide suuruste" suuruse grupi näidet.

![Suuruse grupi loomine](media/create-variant-group.png)

## <a name="additional-resources"></a>Lisaressursid

[Tooteteabe ülevaade](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Jaemüügitoodete häälestamine](set-up-retail-products.md)

[Tootedimensioonid](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]