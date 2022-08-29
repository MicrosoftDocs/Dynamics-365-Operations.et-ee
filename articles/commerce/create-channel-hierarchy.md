---
title: Looge kanali navigeerimishierarhia
description: See artikkel kirjeldab, kuidas luua kanali navigeerimishierarhiat Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/27/2021
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
ms.openlocfilehash: c3b28dd29bf444a75e5aa0a2a105d8a03fcacb0d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270260"
---
# <a name="create-a-channel-navigation-hierarchy"></a>Looge kanali navigeerimishierarhia


[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas luua kanali navigeerimishierarhiat Microsoft Dynamics 365 Commerce.

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

![Juursõlme näide.](media/create-channel-hierarchy-1.png)

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

![Kanali hierarhia näide.](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>Toodete lisamine kategooria sõlmedesse

Toodete lisamiseks kategooria sõlmedesse toimige järgmiselt.

1. Valige kategooria sõlm.
1. Valige jaotises **Tooted** suvand **Lisa**.
1. Leidke uued tooted, mida soovite lisada, kasutades toote numbrit või nime, ja seejärel valige **OK**.
1. Valige toimingupaanil nupp **Salvesta**.

> [!NOTE]
> Toodete lisamisest sõlmele kanali navigeerimise hierarhia sees ei piisa selleks, et tooted kuvataks valitud kanalis, tooted peavad olema ka kanalile määratud. Sortimentide kohta lisateabe saamiseks vt [sortimendi haldust](assortments.md).

Järgmine pilt näitab lisatud toodetega sõlme näidet.

![Kategooria sõlme lisatud tooted.](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>Toote atribuutide gruppide lisamine kategooria sõlmedesse

> [!NOTE]
> Atribuutide grupid tuleb luua enne, kui saate need kanali navigeerimise hierarhias sõlmele lisada.

Tootele kategooria sõlme atribuudigrupi lisamiseks toimige järgmiselt.

1. Valige kategooria sõlm.
1. Valige jaotises **Toote atribuudigrupp** suvand **Lisa**.
1. Leidke lisatavad atribuutide grupid ja seejärel valige **OK**.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab sõlme näidist koos lisatud toote atribuudigruppidega.

![Sõlme toote atribuudigrupid.](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>Lisaressursid

[Sortimentide häälestamine](set-up-assortments.md)

[Atribuutide ja atribuudigruppide haldamine](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
