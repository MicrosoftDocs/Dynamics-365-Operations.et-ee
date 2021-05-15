---
title: Kanali navigeerimishierarhia loomine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce navigatsiooni hierarhia.
author: samjarawan
ms.date: 04/27/2021
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
ms.openlocfilehash: 5df46de9dadfa0b7160a9b340ef36fdf963a0ad3
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951904"
---
# <a name="create-a-channel-navigation-hierarchy"></a>Looge kanali navigeerimishierarhia


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
> Toodete lisamisest sõlmele kanali navigeerimise hierarhia sees ei piisa selleks, et tooted kuvataks valitud kanalis, tooted peavad olema ka kanalile määratud. Sortimentide kohta lisateabe saamiseks vt [sortimendi haldust](assortments.md).

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
