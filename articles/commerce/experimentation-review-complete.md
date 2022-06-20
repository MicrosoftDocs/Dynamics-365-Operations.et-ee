---
title: Variatsiooni esiletõstmine ja eksperimendi lõpuleviimine
description: See artikkel kirjeldab, kuidas propageerida edukat variatsiooni ja lõpetada katsetus selles Dynamics 365 Commerce.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 3e9a978551622bbb14d9213f607d9dfabe42672a
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942733"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Variatsiooni esiletõstmine ja eksperimendi lõpuleviimine

See artikkel kirjeldab, kuidas propageerida variatsiooni, mis oli teie katsetuskatsel parim, ja kuidas katse lõpule viia. Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce. Lisa sammud on kaetud eraldi artikliga.

[ ![Eksperimendi kasutaja teekond – ülevaatamine ja lõpetamine.](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Kui olete [oma eksperimendi käivitanud](experimentation-run-monitor.md) ja kogunud piisavalt andmeid, et määrata, millist variatsiooni te oma aktiivsel saidil kasutada soovite, tõstate variatsiooni esile ja lõpetate eksperimendi.

## <a name="promote-a-variation"></a>Variatsiooni esiletõstmine
Kasutage kolmanda osapoole teenuses oleva eksperimendiga seotud andmeid ja analüüsi, et otsustada, millise variatsiooni tulemused olid parimad. Seejärel saate seda reklaamida, asendades aktiivsel saidil oleva praeguse sisu parima variatsiooniga, et see oleks saadaval kõigile teie veebisaidi kasutajatele.

Parima variatsiooni reklaamimiseks toimige järgmiselt. 

1. Valige Commerce'i saidiehitaja vasakpoolsel navigeerimispaanil **Eksperimendid** ja seejärel valige eksperiment.
1. Valige käsuribal **Eksperimendi lõpule viimine**.
1. Valige dialoogiboksis **Eksperimendi lõpule viimine** suvand **Vaata eksperimendi andmed läbi**. Avaneb kolmanda osapoole teenus, kus saate mõõdikuid kontrollida ja teha kindlaks, milline variatsioon oli parim.
1. Valige dialoogiboksis **Eksperimendi lõpule viimine** parim variatsioon ja seejärel valige **Edasi**.
1. Avage kolmanda osapoole teenus ja peatage eksperiment.
1. Valige saidiehitajas suvand **Lõpeta**, et kirjutada üle originaalne aktiivne leht ja avaldada parim variatsioon nii, et see on saadaval kõigile teie veebisaidi kasutajatele. 

> [!NOTE]
> Kui otsustate praegust aktiivset lehte säilitada ja variatsiooni mitte avaldada, valige **Avalda originaalne leht uuesti**.

## <a name="delete-your-experiment"></a>Eksperimendi kustutamine
Kuigi te ei pea lõpetatud eksperimenti rakenduses Commerce kustutama, võite selle kustutada, et säästa ruumi või puhastada oma tööruumi. 

Ärisaidilooja lõpetatud katse kustutamiseks järgige neid samme.

1. Valige vasakpoolsel navigeerimispaanil **Eksperimendid** ja seejärel valige eksperiment. 
    > [!NOTE]
    > Kui eksperiment on ikka aktiivne, peatage eksperiment enne jätkamist kolmanda osapoole teenuses.
1. Valige käsuribalt **Tühista avaldamine**, et eemaldada variatsiooni sisu aktiivselt saidilt.
1. Eksperimendi kustutamiseks valige **Kustuta**.

## <a name="previous-step"></a>Eelmine etapp
[Katse käitamine ja jälgimine](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
