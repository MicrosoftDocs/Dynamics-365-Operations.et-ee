---
title: Eksperimendi käitamine ja jälgimine
description: See artikkel kirjeldab, kuidas käitada ja jälgida kolmanda osapoole teenuse katsetust. Selles kirjeldatakse ka, kuidas muuta variatsioone pärast eksperimendi alustamist.
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
ms.openlocfilehash: c9f62c97b46fa00791de52b2804dad5edde7f625
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909579"
---
# <a name="run-and-monitor-an-experiment"></a>Eksperimendi käitamine ja jälgimine

See artikkel kirjeldab, kuidas käitada ja jälgida katset kolmanda osapoole rakenduses ning vajadusel muudatusi muuta. Enne selle artikli sammude lõpule viimist peate esmalt avaldama katse [äris](experimentation-preview-publish.md). 

Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce. Lisa sammud on kaetud eraldi artikliga.

[ ![Eksperimendi kasutaja teekond – käitamine ja jälgimine.](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

Kui olete oma variatsioonid avaldanud, on lõpule viidud rakenduses Commerce kõik vajalikud sammud eksperimendi käitamiseks. Järgmine samm on määrata kindlaks, millist variatsiooni igale kasutajale lehe pärimisel näidata. Selle teeb kindlaks kolmanda osapoole teenus, kuid esmalt tuleb teil teenuses eksperiment aktiveerida. Kuna eksperimendi aktiveerimine varieerub iga teenuse puhul, peate järgima teenuse või pakkuja juhiseid. Kui eksperiment ei ole aktiveeritud, näevad kasutajad ainult lehe vaikeversiooni (ühtegi variatsiooni ei kuvata).

Peate eksperimenti piisavalt kaua töös hoidma, et koguda andmeid statistiliselt paikapidavate tulemuste jaoks. Kasutage kolmanda osapoole teenust, et jälgida eksperimendi käitamise ajal eksperimendiga seotud andmeid ja analüüsi.

## <a name="adjust-your-variations"></a>Variatsioonide kohandamine
Kui peate mingil põhjusel variatsioone muutma, järgige alltoodud samme.

> [!IMPORTANT]
> Kui muudate aktiivset eksperimenti rakenduses Commerce või kolmanda osapoole teenuses, võib see tulemusi oluliselt mõjutada. Võib-olla on parem lasta eksperimendil lõpuni jõuda ja seejärel suurte muudatuste jaoks uus eksperiment luua.

1. Valige Commerce'i saidiehitaja vasakpoolsel navigeerimispaanil **Eksperimendid** ja seejärel valige eksperiment. 
1. Valige rippmenüüst variatsioon, mida soovite värskendada.
1. Tehke kõik vajalikud muudatused ja seejärel vaadake variatsioonid üle ja avaldage need. Lisateavet leiate teemast [Eksperimendi eelversioon ja avaldamine](experimentation-preview-publish.md).
1. Minge kolmanda osapoole teenusesse, et muuta eksperimendi seadistust.
    
## <a name="previous-step"></a>Eelmine etapp
[Eksperimendi eelversioon ja avaldamine](experimentation-preview-publish.md)

## <a name="next-step"></a>Järgmine etapp
[Variatsiooni esiletõstmine ja eksperimendi lõpuleviimine](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]