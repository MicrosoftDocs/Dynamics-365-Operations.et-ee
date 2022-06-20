---
title: Loo uus tootehierarhia
description: See artikkel kirjeldab, kuidas luua uus tootehierarhia Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
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
ms.openlocfilehash: 25cfd81e9163ae2da3cb916c88040204f31dc389
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887032"
---
# <a name="create-a-new-product-hierarchy"></a>Loo uus tootehierarhia


[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas luua uus tootehierarhia Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

Dynamics 365 Commerce toetab mitut jaemüügikanalit. Jaemüügikanalid hõlmavad võrgupoode, kõnekeskusi ja jaekauplusi (neid nimetatakse ka füüsilisteks kauplusteks). Igal kaupluse kanalil võivad olla oma makseviisid, hinnagrupid, kassaregistrid, tulu- ja kulukontod ning personal. Enne jaekaupluse kanali loomist tuleb seadistada kõik need elemendid. 

Commerce'i tootehierarhiat kasutatakse organisatsiooni üldise tootehierarhia määramiseks. Saate Commerce'i tootehierarhiat kasutada tootesündmuste, hinnakujunduse ja kampaaniate, aruandluse ning sortimendi planeerimise jaoks. Ühe organisatsiooni kohta saab määrata ainult ühe Commerce'i tootehierarhia.

## <a name="create-and-configure-a-product-hierarchy"></a>Tootehierarhia loomine ja konfigureerimine

Commerce'i tootehierarhia loomiseks ja konfigureerimiseks toimige järgmiselt.

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Tooted ja kategooriad \> Commerce'i tootehierarhia**.
1. Kui ühtegi hierachy pole veel olemas, valige **Tegevuspaanil** suvand **Uus**, et luua hierarhia juur.
1. Jaotises **Üldine**.
    1. Sisestage nimi väljale **Nimi**.
    1. Sisestage kirjeldus väljale **Kirjeldus**.
    1. Sisestage hüüdnimi väljale **Hüüdnimi**.
    1. Seadistage **Aktiivne** väärtusele **Jah**.

## <a name="add-hierarchy-nodes"></a>Hierarhiasõlmede lisamine

Hierarhiasõlmede lisamiseks toimige järgmiselt.

1. Valige toimingupaanil **Kategooriahierarhia muutmine**.
1. Valige peamine sõlm, millele soovite lisada uue sõlme, ja seejärel valige **Uus kategooria sõlm**.
1. Sisestage jaotises **Üldine** väärtused **Nimi**, **Kirjeldus**, **Hüüdnimi** ja **Märksõnad**.
1. Jaotises **Üldine**.
    1. Sisestage nimi väljale **Nimi**.
    1. Sisestage kirjeldus väljale **Kirjeldus**.
    1. Sisestage hüüdnimi väljale **Hüüdnimi**.
    1. Sisestage väljale **Märksõnad** asjakohased märksõnad.
    1. Sisestage väljale **Kuva järjekord** kuva järjekorda tähistav number (valikuline).
1. Valige toimingupaanil nupp **Salvesta**.
1. Täiendavate sõlmede lisamiseks korrake ülaltoodud samme.

Järgmine pilt näitab uue tootehierarhia sõlme loomist.

![Tootehierarhia loomine.](media/create-product-hierarchy.png)

## <a name="other-settings"></a>Muud sätted

Kategooria atribuudigruppe saab vajadusel määrata ka igale grupile.  

## <a name="additional-resources"></a>Lisaressursid

[Commerce’i hierarhiad](retail-hierarchies.md)

[Tootekategooriate ja toodete haldamine](category-management-product-creation.md)

[Kaubastatavate üksuste sortimisjärjestuse muutmine](custom-order-categories-nav-retail-prod-hierarchy.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]