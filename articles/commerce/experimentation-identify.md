---
title: Hüpoteesi tuvastamine ja eksperimendi mõõdikute määramine
description: Selles teemas kirjeldatakse, kuidas tuvastada hüpoteesi ja edumõõdikuid eksperimendi jaoks, mille te käivitate e-kaubanduse veebisaidil rakenduses Dynamics 365 Commerce.
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
ms.openlocfilehash: a3f5d44e008e4092557d75c8f5d830d5ae36a091
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799039"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a>Hüpoteesi tuvastamine ja eksperimendi edumõõdikute määramine
Eksperimenteerimise elutsükli esimene etapp hõlmab eksperimendi hüpoteesi ning jälgitavate mõõdikute määramist edukuse hindamiseks. Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks [eksperimendi seadistamise ja käivitamisega](experimentation-overview.md) rakenduses Dynamics 365 Commerce. Täiendavad etapid on toodud eraldi teemades. 

[ ![Eksperimendi kasutaja teekond – tuvastamine](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)

Hüpotees on väide, millega te ennustate eksperimendi tulemust. Hüpotees määratletakse mitme teguri põhjal, näiteks kasutajate käitumisega seotud andmed ja veebisaidi andmed, mille olete kogunud. Hüpoteesiga määratlete oletuse või teooria, mida soovite oma eksperimendi abil kontrollida. Eksperimendi hüpoteesi näide võib olla „*valge T-särgi pilt minu avalehel paneb inimesi suvekuudel rohkem klõpsama kui sinine kampsun, sest inimesed tahavad kanda suvel midagi kerget ja heledat*”. Sellisel juhul loote variatsioonid, mis sisaldavad valget T-särki ja sinist kampsunit, ning avaldate mõlemad korraga.

Hüpoteesi kontrollimiseks peab eksperimendi edukus või nurjumine olema vahetult seotud kasutaja tegevusega. Näiteks kui veebisaidi kasutaja klõpsab lingile või nupule. Need toimingud peavad vastama sündmustele, mis edastatakse eksperimenti jälgivale kolmanda osapoole teenusele. Aja jooksul muudetakse tegevust tegevate kasutajate protsent mõõdikuks, mida saate kasutada aruannete loomiseks ning analüüsimiseks. Kõigi saadaolevate sündmuste ja atribuutide läbi vaatamiseks vt [Commerce'i komponentide sündmused diagnostika ja tõrkeotsingu jaoks](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).

## <a name="previous-step"></a>Eelmine etapp
[Eksperimenteerimine rakenduses Dynamics 365 Commerce](experimentation-overview.md)


## <a name="next-step"></a>Järgmine etapp
[Katse seadistamine](experimentation-setup.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]