---
title: Tegevuskoha jaoks graafiku loomine
description: See protseduur selgitab, kuidas ajastada tootmistellimusi, mida ei ole tegevuskoha jaoks veel alustatud.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0db5095020bc14d56ae3680e7d0caa68789180e
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469278"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]