---
title: Eksperimendi eelversioon ja avaldamine
description: Selles teemas kirjeldatakse, kuidas vaadata rakendusest Dynamics 365 Commerce pärit eksperimendi eelversiooni ja seda avaldada.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f1a565917ab7a048d4d455bc0a0fbd9316237aeb
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/22/2020
ms.locfileid: "4411812"
---
# <a name="preview-and-publish-an-experiment"></a>Eksperimendi eelversioon ja avaldamine

Selles teemas kirjeldatakse, kuidas vaadata rakenduses Dynamics 365 Commerce oma eksperimendi eelversiooni ning seda avaldada pärast seda, kui olete [oma eksperimendi ühendanud ja oma variatsioone redigeerinud](experimentation-connect-edit.md). Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce. Täiendavad etapid on toodud eraldi teemades.

[ ![Eksperimendi kasutaja teekond – eelversioon ja avaldamine](./media/experimentation_preview_publish.svg) ](./media/experimentation_preview_publish.svg#lightbox)

## <a name="preview-your-experiment-variations"></a>Eksperimendi variatsioonide eelversiooni vaatamine
Saate vaadata oma variatsioonide eelversiooni ja jätkata nende redigeerimist, kuni need näevad välja nii, nagu te tahate.

Oma eksperimendi variatsioonide eelversiooni kuvamiseks Commerce'i saidiehitajaga, toimige järgmiselt.

1. Valige saidiehitajas käsuriba all asuvast variatsioonide rippmenüüst sisu, mille eelversiooni te kuvada soovite. 
1. Klõpsake käsuribal käsul **Eelvaade**. Kuvatakse eelversioon sellest, kuidas sisu avaldamise korral välja näeks.
1. Teistsuguse variatsiooni eelversiooni kuvamiseks valige see variatsioonide rippmenüüst ning valige uuesti **Eelversioon**.

## <a name="publish-your-experiment"></a>Eksperimendi avaldamine
Kui te ei kasuta avaldamisrühma, et ajastada seda, millal teie eksperiment kasutusele võetakse, ja soovite selle kohe avaldada, valige käsuribal suvand **Avalda**. Avaldatakse kõik eksperimenti kuuluvad variatsioonid.
    
> [!IMPORTANT]
> Kui lehel on avaldamata URL, peate esmalt URL-i avaldama, muidu ei ole see teie veebisaidi kasutajatele nähtav. Üksikasjad leiate teemast [Lehe salvestamine, eelversioon ja avaldamine](save-preview-publish-page.md).
    
### <a name="use-publish-groups-to-schedule-when-your-experiment-goes-live"></a>Avaldamisrühmade kasutamine eksperimendi kasutuselevõtu ajastamiseks
Saidiehitajas loodud variatsioonide avaldamist saab ajastada avaldamisrühma kaudu. Saate avaldamisrühma kaudu ühendada oma eksperimendiga lehe või fragmendi, valides vasakpoolsel navigeerimispaanil **Eksperimendid**. Samuti saate teha seda, kui valite **Lehed** või **Fragmendid** ja järgite juhiseid jaotises [Eksperimendi ühendamine ja variatsioonide redigeerimine](experimentation-connect-edit.md). Lisateavet avaldamisrühmade kohta leiate teemast [Avaldamisrühmadega töötamine](publish-groups.md).

Kui kasutate eksperimentidega koos avaldamisrühmi, tuleb arvestada mõnda olulist asja.
- Kui lisate avaldamisrühma lehe või fragmendi, milles on aktiivne eksperiment, eemaldatakse eksperiment avaldamisrühmas lehelt või fragmendist.
- Eksperimendid, mis on ühendatud aktiivse saidi lehtedega, ei ole avaldamisrühma lehtedele kättesaadavad ning sama kehtib vastupidi. Samamoodi ei ole aktiivse saidi lehed, millel on aktiivsed eksperimendid, kättesaadavad muudele avaldamisrühmades olevatele eksperimentidele ning sama kehtib vastupidi.
- Kui avaldate või ajastate avaldamisrühma, avaldatakse kogu rühmas olev sisu hoolimata sellest, kas avaldamisrühmaga on seotud mõni eksperiment.
- Kuna avaldamisrühm jääb alles ka pärast selle avaldamist aktiivsel saidil, jäävad alles ka avaldamisrühmas olevad eksperimendid. Seetõttu ei saa te sama lehe või fragmendiga teisi eksperimente seostada. Selle piirangu vältimiseks kustutage kõik avaldamisrühmad, mis sisaldavad eksperimente. Kui soovite kustutada aktiivselt saidilt eksperimendi, mis sisaldub ka avaldamisrühmas, kustutage see esmalt avaldamisrühmast.

## <a name="previous-step"></a>Eelmine etapp
[Eksperimendi ühendamine ja redigeerimine](experimentation-connect-edit.md)

## <a name="next-step"></a>Järgmine etapp
[Eksperimendi käitamine ja jälgimine](experimentation-run-monitor.md)
