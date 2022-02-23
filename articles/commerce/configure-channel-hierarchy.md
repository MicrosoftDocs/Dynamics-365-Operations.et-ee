---
title: Kanali konfigureerimine kanali navigeerimishierarhia kasutamiseks
description: Selles teemas kirjeldatakse, kuidas konfigureerida rakenduses Microsoft Dynamics 365 Commerce kanal kasutama kanali navigeerimishierarhiat.
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
ms.openlocfilehash: 7b5041d35d310125c314ab2cb77d3cc40cdb7113
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411578"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a>Kanali konfigureerimine kanali navigeerimishierarhia kasutamiseks


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas konfigureerida rakenduses Microsoft Dynamics 365 Commerce kanal kasutama kanali navigeerimishierarhiat.

## <a name="overview"></a>Ülevaade

Kanali navigeerimishierarhiad korraldavad tooteid kategooriatesse, nii et tooteid saab sirvida e-poes või kassas. Jaemüügi- ja võrgukanalid peavad olema konfigureeritud kanali navigeerimishierarhiatega.

## <a name="configure-the-channel"></a>Kanali konfigureerimine

Kanal konfigureerimiseks kanali navigatsioonihierarhiat kasutama toimige järgmiselt.

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Kanali seadistus \> Kanali kategooriad ja toote atribuudid**.
1. Valige konfigureerimiseks kanal.
1. Valige toimingupaanil suvand **Atribuudi metaandmete häälestamine**.
1. Valige ripploendis **Kategooriahierarhia** sobiv kanali navigeerimishierarhia.
1. Valige toimingupaanil nupp **Salvesta**.
1. Lisage jaotisesse **Atribuudigrupp** kõik atribuutide grupid, mis on kõigi sõlmede globaalsed atribuudid.

Järgmine pilt näitab kuidas konfigureerida kanalit kasutama kanali navigatsioonihierarhiat.

![Kanali konfiguratsiooni näide](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a>Atribuudi metaandmete häälestamine

Atribuudi metaandmete häälestamine võimaldab iga sõlme atribuutide konfigureerimist.

Atribuudi metaandmete seadistamiseks toimige järgmiselt.

1. Valige toimingupaanil suvand **Atribuudi metaandmete häälestamine**.
1. Iga sõlme puhul valige **Kanali toote atribuudid**.
1. Seadke suvand **Kuva kanalil atribuuti** väärtusele **Jah** ja suvand **Saab täpsustada** väärtusele **Jah**, et lubada sellel kanalil täpsustamisi.
1. Pärast iga sõlme konfigureerimist vastavalt soovile, valige **Tegevuspaanil** salvestamiseks nupp **Salvesta**.
1. Valige ülevalt parempoolsest nurgast **X**, et väljuda sellelt kuvalt tagasi lehele **Kanali kategooriad ja tooteatribuudid**.

Järgmine pilt näitab näidet kanali tooteatribuutide konfigureerimisest kanali kategooria sõlmel.

![Kanali atribuudid kanali kategooria sõlmel](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a>Muudatuste avaldamine

Muudatuste jõustumiseks tuleb muudatused avaldada.

Muudatuste avaldamiseks tehke järgmist.

1. Valige toimingupaanil **Avalda kanali värskendused**.
1. Valige paanil **Avalda kanali värskendused** nupp **OK**.

Järgmine pilt näitab, kuidas kanali värskendusi avaldada.

![Kanalivärskenduste avaldamine](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a>Lisaressursid

[Kanali navigeerimishierarhia loomine](create-channel-hierarchy.md)


