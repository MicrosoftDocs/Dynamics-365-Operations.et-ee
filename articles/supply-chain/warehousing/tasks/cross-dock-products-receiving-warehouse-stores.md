---
title: Toodete ristlaadimine vastuvõtvast laost kauplustesse
description: See protseduur tutvustab, kuidas luua ja töödelda ristplatvormi toodete laialisaatmiseks ostutellimuse vastuvõtukohast ühte või mitmesse kauplusesse.
author: ShylaThompson
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f297a9bbb8ad5d1cd701626783e7db75c94fa842
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148373"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a>Toodete ristlaadimine vastuvõtvast laost kauplustesse

[!include [banner](../../includes/banner.md)]

See protseduur tutvustab, kuidas luua ja töödelda ristplatvormi toodete laialisaatmiseks ostutellimuse vastuvõtukohast ühte või mitmesse kauplusesse. Kasutaja saab määrata mitu konfiguratsiooni ja lasta süsteemil soovitada, kuidas tooted laiali saata, või käsitsi sisestada, kuhu tooted saadetakse ja kui suure koguse iga kauplus saab. See protseduur ei sisalda andmete seadistust, mida saab kasutada ristplatvormil, näiteks täiendamise reegleid, organisatsiooni hierarhiaid ega kauplusekaale. See protseduur kasutab USRT-demofirmat.

1. Avage valik Kõik ostutellimused.
2. Valige loendist ostutellimus ja klõpsake tellimuse avamiseks lingil.
3. Klõpsake toimingupaanil suvandit Jaemüük ja Kaubandus.
4. Klõpsake valikut Cross docking (Ristlaadimine).
5. Klõpsake nuppu Redigeeri.
    * Kategooriat saab kasutada kirjete filtreerimiseks jaotises Lines (Read).  
6. Otsige loendist ja valige soovitud kirje.
7. Sisestage väljale Cross docking quantity (Ristlaadimise kogus) väärtus, et täpsustada, kui suur osa valitud toote kodusest tuleks laiali saata.
8. Sisestage väljale Additional cross docking quantity (Lisa-ristlaadimise kogus) väärtus laialisaatmiskoguste määramiseks saadaolevatele ostetavatele toodetele
9. Sisestage väljale Distribution (Jaotus) asukoha kaal.
    * Saate teisi tüüpe valida jaotise jaoks teistsuguste reeglite kasutamiseks.  
10. Sisestage väljale Täiendamise hierarhia väärtus.
11. Valige Jah väljal Respect assortments (Sortimendi tunnustamine).
12. Klõpsake valikut Arvuta kogused.
13. Klõpsake valikut Create order (Loo tellimus).
14. Klõpsake nuppu Jah.
15. Leidke loendist ladu, mis tooted vastu võttis ja valige see
16. Klõpsake valitud lao jaoks loodud tellimuste vaatamiseks valikut Order (Tellimus)

