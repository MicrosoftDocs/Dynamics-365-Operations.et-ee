---
title: "Nõudluse prognoosi arvutamisel võõrväärtuste eemaldamine kandeandmete ajaloost"
description: "Selles artiklis kirjeldatakse, kuidas välistada võõrväärtusi ajaloolistest andmetest, mida kasutatakse nõudluse prognoosi arvutamiseks. Võõrväärtuste välistamisega saate parandada prognoosi täpsust."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 6f44e1ce566781f1586203528d55b13b28001a2c
ms.lasthandoff: 03/31/2017


---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Nõudluse prognoosi arvutamisel võõrväärtuste eemaldamine kandeandmete ajaloost

Selles artiklis kirjeldatakse, kuidas välistada võõrväärtusi ajaloolistest andmetest, mida kasutatakse nõudluse prognoosi arvutamiseks. Võõrväärtuste välistamisega saate parandada prognoosi täpsust.

Saate välistada võõrväärtuste prognoosi täpsuse parandamiseks. See on valikuline ülesanne. Siin on protsessi ülevaade.

1.  Klõpsake **kapten planeerimine**&gt;**Setup**&gt;**nõudluse prognoosimise**&gt;**tulemus eemaldamine** avamiseks ning **tulemus eemaldamine** lehele, kus saate päringu saate valida kanded välja jätta.
2.  Valige ettevõte, millele päring kehtib, ja sisestage seejärel nimi ja kirjeldus. Väljale **Päringu kuupäev** lisatakse automaatselt praegune kuupäev.
3.  Märkige ruut **Aktiivne** päringu kaudu leitud kannete välistamiseks ajaloolistest andmetest. See säte jõustub alusprognoosi loomisel.
4.  Lehel **Võõrväärtuse eemaldamise päring** saate lisada, eemaldada ja valida kriteeriume, mis määravad, millised kanded välistatakse alusprognoosi arvutamisel. Valige näiteks kindel kaup või tellimuse kanne, mida välistada.
5.  Klõpsake valikut **Kuva kanded**. Lehel **Võõrväärtuse kanded** on esitatud kanded, mis täidavad päringus määratud kriteeriume ja mis välistatakse nõudluse prognoosi arvutamisel ajaloolistest andmetest.

**Märkus:** saate luua ka päringu, mis põhineb olemasoleval päringul. Valige kopeeritav päring ja klõpsake siis käsku **Dubleeri**. Väli **Päringu kuupäev** tuvastab versiooni. Võite kasutada päringut olemasoleval kujul või klõpsata kriteeriumide muutmiseks käsku **Redigeeri päringut**. Soovi korral saate muuta uue päringu nime ja kirjeldust.

<a name="see-also"></a>Vt ka
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)


