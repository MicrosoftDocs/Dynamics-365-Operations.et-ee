---
title: Kastiaruannete loomine ja nende lõppemine
description: Kasutage seda tegevuse juhist valmisaruannete käitamiseks Headquartersis erinevatest tööruumidest ja asukohas Päringud ja Müügiaruanded, mis asuvad rakenduses Commerce.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailCategoryAndProductWorkspace, RetailOrgHierarchyTreeLookup, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d3dd941eb4e682e61c8b3d10ef0ccd14239f090c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232709"
---
# <a name="generate-and-run-out-of-box-reports"></a>Kastiaruannete loomine ja nende lõppemine

[!include [banner](../includes/banner.md)]

Kasutage seda tegevuse juhist valmisaruannete käitamiseks Headquartersis erinevatest tööruumidest ja asukohas Päringud ja Müügiaruanded, mis asuvad rakenduses Commerce.

Selle salvestise loomisel kasutati demoettevõtte USRT-i andmeid. See salvestis on mõeldud süsteemiadministraatori rollile.

## <a name="launch-reports-from-workspaces"></a>Aruannete käivitamine tööruumidest
1. Avage Jaemüük ja kaubandus > Tooted ja kategooriad > Kategooria- ja tootehaldus.
2. Klõpsake noolt jaotise Aruanded laiendamiseks või ahendamiseks.
3. Klõpsake suvandit Peamiste toodete aruanne.
4. Sisestage kuupäev väljale Alguskuupäev.
5. Sisestage kuupäev väljale Lõpukuupäev.
6. Klõpsake väljal Kanal otsingu avamiseks ripploendi nuppu.
7. Valige puul suvand Contoso Retail\Contoso Retail USA\Central\Houston.
    * See näitab organisatsiooni vaikehierarhiat Commerce’i aruandluseks.   Minge jaotisse Organisatsioonihaldus > Organisatsioonid > Organisatsioonihierarhia eesmärgid, valige suvand Kaubanduse aruandlus ja kontrollige jaotises Määratud hierarhiad hierarhia nime, mille puhul on veerg Vaikimisi märgitud. Selle tegevuse salvestise jaoks kasutatud demoandmete osana märkate, et aruandluse jaoks on organisatsiooni vaikehierarhiaks valitud Kauplused piirkonniti.     
8. Klõpsake nuppu OK.
9. Valige suvand väljal Kuva.
10. Valige suvand väljal Alus.
11. Klõpsake nuppu OK.

## <a name="launch-reports-from-the-inquiries-and-sales-reports"></a>Aruannete käivitamine päringutest ja müügiaruannetest
1. Avage Jaemüük ja kaubandus > Päringud ja aruanded > Müügiaruanded > Kategooria müügiaruanded.
2. Sisestage kuupäev väljale Alguskuupäev.
3. Sisestage kuupäev väljale Lõpukuupäev.
4. Klõpsake väljal Kanal otsingu avamiseks ripploendi nuppu.
5. Valige puul suvand Contoso Retail\Contoso Retail USA\West\Seattle.
    * See näitab organisatsiooni vaikehierarhiat Commerce’i aruandluseks. Minge jaotisse Organisatsioonihaldus > Organisatsioonid > Organisatsioonihierarhia eesmärgid, valige suvand Kaubanduse aruandlus ja kontrollige jaotises Määratud hierarhiad hierarhia nime, mille puhul on veerg Vaikimisi märgitud. Selle tegevuse salvestise jaoks kasutatud demoandmete osana märkate, et aruandluse jaoks on organisatsiooni vaikehierarhiaks valitud Kauplused piirkonniti.     
6. Klõpsake nuppu OK.
7. Klõpsake nuppu OK.

## <a name="export-an-hq-reports"></a>HQ aruannete eksportimine
1. Avage Jaemüük ja kaubandus > Päringud ja aruanded > Müügiaruanded > Organisatsiooni müügiaruanded.
2. Sisestage kuupäev väljale Alguskuupäev.
3. Sisestage kuupäev väljale Lõpukuupäev.
4. Klõpsake nuppu OK.
5. Klõpsake suvandit Ekspordi.
6. Klõpsake suvandit PDF.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]