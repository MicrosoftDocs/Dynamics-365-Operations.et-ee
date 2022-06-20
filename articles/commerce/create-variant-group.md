---
title: Variandigrupi loomine
description: See artikkel kirjeldab, kuidas luua tootele suuruse, stiili või värvi variandi gruppi moodulis Microsoft Dynamics 365 Commerce
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: a46dc9fd5cdb848818964e771d373924b217147a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874957"
---
# <a name="create-a-variant-group"></a>Variandigrupi loomine


[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas luua tootele suuruse, stiili või värvi variandi gruppi moodulis Microsoft Dynamics 365 Commerce

## <a name="overview"></a>Ülevaade

Dynamics 365 Commerce toetab mitmeid toodete variante. See on ideaalne erinevate tootekategooriate jaoks variandigruppide seadistamiseks. Näiteks saab t-särkide puhul luua suuruse grupi suurustega XS, S, M, L ja XL või värvigrupi, mis sisaldaks toote kõiki saadaolevaid värve. Variandigrupid tuleb lisada enne toodete lisamist.

Selles artiklis luuakse ja konfigureeritakse suuruse grupp. Sarnase toiminguga saab lisada ja konfigureerida ka stiili- ja värvigruppe.

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

![Suuruse grupi loomine.](media/create-variant-group.png)

## <a name="additional-resources"></a>Lisaressursid

[Tooteteabe ülevaade](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Jaemüügitoodete häälestamine](set-up-retail-products.md)

[Tootedimensioonid](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]