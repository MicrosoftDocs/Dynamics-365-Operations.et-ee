---
title: Kanali navigeerimishierarhia loomine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce navigatsiooni hierarhia.
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
ms.openlocfilehash: e83860667f142adcc85cd8542d521e18f16dbc2c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411570"
---
# <a name="create-a-channel-navigation-hierarchy"></a>Kanali navigeerimishierarhia loomine


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce navigatsiooni hierarhia.

## <a name="overview"></a>Ülevaade

Kanali navigatsiooni hierarhiat kasutatakse toodete grupeerimiseks ja korraldamiseks kategooriatesse, nii et tooteid saab sirvida võrgus või kassas.

## <a name="create-a-channel-navigation-hierarchy"></a>Kanali navigeerimishierarhia loomine

Kanali navigeerimishierarhia loomiseks toimige järgmiselt.

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Tooted ja kategooriad \> Kanali navigatsiooni kategooriad**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage nimi väljale **Nimi**.
1. Sisestage kirjeldus väljale **Kirjeldus**.
1. Valige **Loo**.
1. Valige toimingupaanilt suvand **Uus kategooria sõlm**, et luua juursõlm.
1. Sisestage nimi väljale **Nimi**.
1. Sisestage kirjeldus väljale **Kirjeldus**.
1. Sisestage hüüdnimi väljale **Hüüdnimi**.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab juursõlme näidet.

![Juursõlme näide](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a>Navigeerimiskategooria sõlmede loomine

Et luua täiendavaid navigeerimiskategooria sõlmi, mis tähistavad tootekategooriaid kanalis, toimige järgmiselt.

1. Valige navigeerimispaanil peamine sõlm, millele kategooria lisada.
1. Valige toimingupaanil nupp **Uus kategooria sõlm**.
1. Sisestage nimi väljale **Nimi**.
1. Sisestage kirjeldus väljale **Kirjeldus**.
1. Sisestage hüüdnimi väljale **Hüüdnimi**.
1. Sisestage väljale **Kuva järjekord** kuva järjekord (valikuline).
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab lõpuleviidud kanali navigeerimishierarhia näidet.

![Kanali hierarhia näide](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>Toodete lisamine kategooria sõlmedesse

Toodete lisamiseks kategooria sõlmedesse toimige järgmiselt.

1. Valige kategooria sõlm.
1. Valige jaotises **Tooted** suvand **Lisa**.
1. Leidke uued tooted, mida soovite lisada, kasutades toote numbrit või nime, ja seejärel valige **OK**.
1. Valige toimingupaanil nupp **Salvesta**.

> [!NOTE]
> Toodete lisamine sõlmele kanali navigeerimise hierarhia sees ei ole piisav, et tooted kuvataks valitud kanalis, tooted peavad olema ka tootele erinevad.

Järgmine pilt näitab lisatud toodetega sõlme näidet.

![Kategooria sõlme lisatud tooted](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>Toote atribuutide gruppide lisamine kategooria sõlmedesse

> [!NOTE]
> Atribuutide grupid tuleb luua enne, kui saate need kanali navigeerimise hierarhias sõlmele lisada.

Tootele kategooria sõlme atribuudigrupi lisamiseks toimige järgmiselt.

1. Valige kategooria sõlm.
1. Valige jaotises **Toote atribuudigrupp** suvand **Lisa**.
1. Leidke lisatavad atribuutide grupid ja seejärel valige **OK**.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab sõlme näidist koos lisatud toote atribuudigruppidega.

![Sõlme toote atribuudigrupid](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>Lisaressursid

[Sortimentide häälestamine](set-up-assortments.md)

[Atribuutide ja atribuudigruppide haldamine](attribute-attributegroups-lifecycle.md)
