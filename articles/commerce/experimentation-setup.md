---
title: Eksperimendi seadistamine
description: Selles teemas kirjeldatakse, kuidas seadistada eksperimenti kolmanda osapoole teenuses.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 9976ca461f7e988c32b81565fa2d084709e5ad6e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792506"
---
# <a name="set-up-an-experiment"></a>Eksperimendi seadistamine

Pärast [hüpoteesi määratlemist ja eksperimendi edumõõdikute kindlaks määramist](experimentation-identify.md) peate oma eksperimendi seadistama kolmanda osapoole teenuses. Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce. Täiendavad etapid on toodud eraldi teemades.

[ ![Eksperimendi kasutaja teekond – seadistamine](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Eksperimendi seadistamine kolmanda osapoole teenuses
Nüüdseks peaks teil olema valitud kolmanda osapoole teenus oma eksperimendi käitamiseks ja jälgimiseks ning eksperimendi konnektori seadistamiseks. Need eeltingimused on loetletud teemas [Eksperimenteerimine rakenduses Dynamics 365 Commerce](experimentation-overview.md).

Järgige samme, mis on vajalikud eksperimendi loomiseks kolmanda osapoole teenuses. Kui konnektor on õigesti konfigureeritud, siis kuvatakse kolmanda osapoole teenuses seadistatud eksperimentide täielik loend Commerce'i saidiehitajas umbes viie minuti jooksul.

## <a name="set-up-your-success-metrics"></a>Edumõõdikute seadistamine
Iga eksperiment vajab mõõdikuid variatsioonide mõju mõõtmiseks ja hüpoteesi kontrollimiseks. Järgige alltoodud samme, et lubada mõõdikute arvutamine kolmanda osapoole teenuses, kasutades reaalajas telemeetriasündmusi rakendusest Dynamics 365 Commerce.

Edumõõdikute häälestamiseks järgige neid toiminguid.

1. Valige Commerce'i saidiehitajas vasakpoolselt navigeerimispaanilt vahekaart **Lehed** ja seejärel valige leht, mille jaoks soovite mõõdikuid koguda. 
1. Avage jaotis **Jälgitavad sündmuse ID-d** jälgitava lehe või mooduli parempoolselt atribuudipaanilt.
1. Valige suvand **Kuva**. Kuvatakse kõigi sündmuse ID-de loend. Kopeerige sündmus, mida soovite jälgida, ja kleepige sündmusevõti selleks mõeldud kohta kolmanda osapoole teenuses. Kui vajate rohkem kui üht sündmust, kopeerige võtmed ükshaaval. 
    - Teavet selle kohta, kuidas vaadata kõiki saadaolevaid sündmusi ja atribuute, sh lehevaatamisi ja tulu, leiate teemast [Commerce'i komponentide sündmused diagnostika ja tõrkeotsingu jaoks](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).
1. Kui kolmanda osapoole teenuses on vaja mõõdikute jälgimiseks veel midagi teha, tehke seda.

## <a name="previous-step"></a>Eelmine etapp
[Hüpoteesi tuvastamine ja eksperimendi mõõdikute määramine](experimentation-identify.md) 


## <a name="next-step"></a>Järgmine etapp
[Eksperimendi ühendamine ja redigeerimine](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]