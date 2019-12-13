---
title: Võrgukanali aruannete loomine
description: See teema kirjeldab, kuidas luua oma võrgukanali jaoks aruandeid rakenduses Microsoft Dynamics 365 Retail.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 77737c134df8f3ba598fe9026fa7c01ca9976733
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698046"
---
# <a name="generate-online-channel-reports"></a>Võrgukanali aruannete loomine

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas luua oma võrgukanali jaoks aruandeid rakenduses Microsoft Dynamics 365 Retail.

## <a name="overview"></a>Ülevaade

Saate luua ja vaadata Retailis mitu aruannet, et näha, kuidas võrgukanal toimib.

## <a name="channel-summary-report"></a>Kanali koondaruanne

Aruanne **Kanali kokkuvõte** kuvab valitud kanali järgmiste kannete kokkuvõtet.

- Müügikanded
- Maksekanded
- Maksukanded
- Allahinnatud kanded

Aruande **Kanali kokkuvõte** loomiseks toimige järgmiselt.

1. Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Kanali koondaruanne**.
1. Sisestage kuupäev väljale **Alates kuupäevast**.
1. Sisestage kuupäev väljale **Lõppkuupäev**.
1. Valige väljal **Kanal** võrgukanal.
1. Valige nupp **OK**.
 
## <a name="channel-sales-by-year-report"></a>Kanali müügiaruanne aastate alusel 

Aruanne **Kanali müük aastate alusel** näitab kindla poe müügi võrdlust aastate lõikes. Teie valite aasta, mille müüki võrrelda, ja aruanne võrdleb valitud aasta müüki eelmise aasta müügiga.

Aruande **Kanali müük aastate alusel** loomiseks toimige järgmiselt.

1. Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Kanali müügiaruanne aastate alusel**.
1. Sisestage väljale **Kalendriaastast** aasta.
1. Sisestage väljale **Kalendriaastani** aasta.
1. Valige väljal **Kanal** võrgukanal.
1. Valige nupp **OK**.

## <a name="channel-sales-by-hour-report"></a>Kanali müügiaruanne tundide alusel

Aruanne **Kanali müük tundide alusel** näitab valitud kanali või tootmisüksuse müügimõõdikuid tunni alusel.

Aruande **Kanali müük tundide alusel** loomiseks toimige järgmiselt.

1. Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Kanali müügiaruanne tundide alusel**.
1. Sisestage kuupäev väljale **Alates kuupäevast**.
1. Sisestage kuupäev väljale **Lõppkuupäev**.
1. Valige väljal **Kanal** võrgukanal.
1. Valige nupp **OK**.

## <a name="top-customers-report"></a>Parimate klientide aruanne

Aruanne **Parimad kliendid** näitab valitud kanali või tootmisüksuse parima *N* kliendi müügimõõdikuid. Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.

Aruande **Parimad kliendid** loomiseks toimige järgmiselt.

1. Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Parimate klientide aruanne**.
1. Sisestage kuupäev väljale **Alates kuupäevast**.
1. Sisestage kuupäev väljale **Lõppkuupäev**.
1. Valige väljal **Kanal** võrgukanal.
1. Valige nupp **OK**.

## <a name="top-discounts-report"></a>Peamiste allahindluste aruanne

Aruanne **Peamised allahindlused** näitab valitud kanali või tootmisüksuse peamise *N* allahindluse müügimõõdikuid. Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.

Aruande **Peamised allahindlused** loomiseks toimige järgmiselt.

1. Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Peamiste allahindluste aruanne**.
1. Sisestage kuupäev väljale **Alates kuupäevast**.
1. Sisestage kuupäev väljale **Lõppkuupäev**.
1. Valige väljal **Kanal** võrgukanal.
1. Valige nupp **OK**.

## <a name="top-products-report"></a>Peamiste toodete aruanne

Aruanne **Peamised tooted** näitab valitud kanali või tootmisüksuse peamise *N* toote müügimõõdikuid. Väärtus *N* on arv vahemikus 10 kuni 100 ja põhineb kasutaja valitud koondmõõdul.

Aruande **Peamised tooted** loomiseks toimige järgmiselt.

1. Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Peamiste toodete aruanne**.
1. Sisestage kuupäev väljale **Alates kuupäevast**.
1. Sisestage kuupäev väljale **Lõppkuupäev**.
1. Valige väljal **Kanal** võrgukanal.
1. Valige nupp **OK**.

## <a name="category-sales-report"></a>Kategooria müügiaruanne

Aruanne **Kategooria müük** näitab valitud kanali või tootmisüksuse kategooriahierarhia iga sõlme müügimõõdikuid valitud perioodi jooksul.

Aruande **Kategooria müük** loomiseks toimige järgmiselt.

1. Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Kategooria müügiaruanded**.
1. Sisestage kuupäev väljale **Alates kuupäevast**.
1. Sisestage kuupäev väljale **Lõppkuupäev**.
1. Valige väljal **Kanal** võrgukanal.
1. Valige nupp **OK**.

## <a name="organization-sales-report"></a>Organisatsiooni müügiaruanne

Aruanne **Organisatsiooni müük** näitab teie jaekaupluste jõudlust organisatsiooni üksuse järgi. See aruanne sisaldab müügikogust ja -summat poe kaupa ning iga poe kasumimarginaali. Organisatsiooni üksus põhineb vaikearuandluse hierarhial.

Aruande **Organisatsiooni müük** loomiseks toimige järgmiselt.

1. Avage **Jaemüük \> Päringud ja aruanded \> Müügiaruanded \> Organisatsiooni müügiaruanded**.
1. Sisestage kuupäev väljale **Alates kuupäevast**.
1. Sisestage kuupäev väljale **Lõppkuupäev**.
1. Valige nupp **OK**.

## <a name="additional-resources"></a>Lisaressursid

- [Abiressursid rakenduse Dynamics 365 Retail jaoks](../retail/index.md)
