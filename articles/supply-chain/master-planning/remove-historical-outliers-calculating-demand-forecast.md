---
title: Nõudluse prognoosi arvutamisel võõrväärtuste eemaldamine kandeandmete ajaloost
description: Selles artiklis kirjeldatakse, kuidas välistada võõrväärtusi ajaloolistest andmetest, mida kasutatakse nõudluse prognoosi arvutamiseks. Võõrväärtuste välistamisega saate parandada prognoosi täpsust.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup, ReqDemPlanOutlierQueryPreview
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df20a45707d3f6ff2ba963e3310194c1af830234
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187382"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Nõudluse prognoosi arvutamisel võõrväärtuste eemaldamine kandeandmete ajaloost

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas välistada võõrväärtusi ajaloolistest andmetest, mida kasutatakse nõudluse prognoosi arvutamiseks. Võõrväärtuste välistamisega saate parandada prognoosi täpsust.

Prognoosi täpsuse suurendamiseks saab võõrväärtused välistada. See on valikuline ülesanne. Siin on protsessi ülevaade.

1.  Klõpsake valikuid **Koondplaneerimine** &gt; **Seadistus** &gt; **Nõudluse prognoosimine** &gt; **Võõrväärtuse eemaldamine** lehe **Võõrväärtuse eemaldamine** avamiseks, kus saate välistatavate kannete valimiseks päringut kasutada.
2.  Valige ettevõte, millele päring kehtib, ja sisestage seejärel nimi ja kirjeldus. Väljale **Päringu kuupäev** lisatakse automaatselt praegune kuupäev.
3.  Märkige ruut **Aktiivne** päringu kaudu leitud kannete välistamiseks ajaloolistest andmetest. See säte jõustub alusprognoosi loomisel.
4.  Lehel **Võõrväärtuse eemaldamise päring** saate lisada, eemaldada ja valida kriteeriume, mis määravad, millised kanded välistatakse alusprognoosi arvutamisel. Valige näiteks kindel kaup või tellimuse kanne, mida välistada.
5.  Klõpsake valikut **Kuva kanded**. Lehel **Võõrväärtuse kanded** on esitatud kanded, mis täidavad päringus määratud kriteeriume ja mis välistatakse nõudluse prognoosi arvutamisel ajaloolistest andmetest.

**Märkus:** saate luua ka päringu, mis põhineb olemasoleval päringul. Valige kopeeritav päring ja klõpsake siis käsku **Dubleeri**. Väli **Päringu kuupäev** tuvastab versiooni. Võite kasutada päringut olemasoleval kujul või klõpsata kriteeriumide muutmiseks käsku **Redigeeri päringut**. Soovi korral saate muuta uue päringu nime ja kirjeldust.

## <a name="additional-resources"></a>Lisaressursid

[Nõudluse prognoosimise ülevaade](introduction-demand-forecasting.md)

[Prognoosi täpsuse jälgimine](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]