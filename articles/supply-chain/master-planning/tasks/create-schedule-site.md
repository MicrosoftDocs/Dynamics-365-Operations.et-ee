---
title: Tegevuskoha jaoks graafiku loomine
description: See protseduur selgitab, kuidas ajastada tootmistellimusi, mida ei ole tegevuskoha jaoks veel alustatud.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1273297a7a48da11b1448f153a151c2a7b461d0
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148051"
---
# <a name="create-a-schedule-for-a-site"></a>Tegevuskoha jaoks graafiku loomine

[!include [banner](../../includes/banner.md)]

See protseduur selgitab, kuidas ajastada tootmistellimusi, mida ei ole tegevuskoha jaoks veel alustatud.  Selle protseduuri lõpuleviimiseks kasutatakse demoandmete ettevõtet USMF.


## <a name="identify-production-orders-that-are-not-started"></a>Käivitamata tootmistellimuste tuvastamine
1. Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.
2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks filtreerige väljal Tegevuskoht väärtusega 1.
    * 1 tähistab tegevuskohta USMF-is. Kui te ei kasuta USMF-i, valige tegevuskoht oma ettevõttest.  
3. Avage veeru Olek filter.
4. Rakendage filtrit väljal Olek koos väärtusega Plaanitud, kasutades filtrit väärtusega „on täpselt”.

## <a name="create-a-schedule"></a>Graafiku loomine
1. Märkige või tühjendage loendis kõik read.
2. Klõpsake tegumiribal valikut Graafik.
3. Klõpsake valikut Tööde plaanimine.
4. Valige väljal Planeerimissuund üksus Tarnekuupäevast tagasi.
5. Tehke väljal Piiratud võimsus valik Ei.
6. Tehke väljal Piiratud materjal valik Ei.
7. Klõpsake nuppu OK.
    * See võib veidi aega võtta.  

## <a name="view-the-result-of-scheduled-production-orders"></a>Plaanitud tootmistellimuste tulemite vaatamine
1. Märkige loendis valitud rida.
    * Saate märkida mis tahes rea.  
2. Klõpsake toimingupaanil valikut Tootmistellimus.
3. Klõpsake valikut Kõik tööd.
    * Sellel lehel saate vaadata tööde loendit. Vahekaardil Plaanimine saate vaadata töö algus- ja lõppkuupäeva.  
4. Klõpsake suvandit Materjalid.
    * Sellel lehel saate vaadata tootmistellimuse toimingute eeldatavat materjalikulu ja praegust saadaolevat kaubavaru.  

