---
title: Variandigrupi loomine
description: See artikkel kirjeldab, kuidas luua tootele suuruse, stiili või värvi variandi gruppi moodulis Microsoft Dynamics 365 Commerce
author: samjarawan
ms.date: 01/27/2020
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
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
ms.openlocfilehash: 507076259c2d9dfe97a0e24d253b5ac0a8325fe2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270096"
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

![Suuruse grupi loomine.](media/Size-Groups.png)

## <a name="additional-resources"></a>Lisaressursid

[Tooteteabe ülevaade](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[Jaemüügitoodete häälestamine](set-up-retail-products.md)

[Tootedimensioonid](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
