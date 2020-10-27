---
title: Variatsiooni esiletõstmine ja eksperimendi lõpuleviimine
description: See teema kirjeldab, kuidas rakenduses Dynamics 365 Commerce edukat variatsiooni esile tõsta ja eksperimenti lõpule viia.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
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
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930176"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Variatsiooni esiletõstmine ja eksperimendi lõpuleviimine

Selles teemas kirjeldatakse, kuidas tõsta esile variatsiooni, mis sai teie eksperimendis parima tulemuse, ja kuidas eksperimenti lõpule viia. Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce. Täiendavad etapid on toodud eraldi teemades.

[ ![Eksperimendi kasutaja teekond – ülevaatamine ja lõpetamine](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)

Kui olete [oma eksperimendi käivitanud](experimentation-run-monitor.md) ja kogunud piisavalt andmeid, et määrata, millist variatsiooni te oma aktiivsel saidil kasutada soovite, tõstate variatsiooni esile ja lõpetate eksperimendi.

## <a name="promote-a-variation"></a>Variatsiooni esiletõstmine
Kasutage kolmanda osapoole teenuses oleva eksperimendiga seotud andmeid ja analüüsi, et otsustada, millise variatsiooni tulemused olid parimad. Et asendada aktiivsel saidil olev praegune sisu parima variatsiooniga, et see oleks saadaval kõigile teie veebisaidi kasutajatele, tehke järgmist. 

1. Avage saidiehitajas vahekaart **Eksperimendid** ja valige eksperiment.
1. Valige ülemisel ribal suvand **Lõpeta eksperiment**.
1. Valige dialoogimenüüs **Eksperimendi lõpetamine** suvand **Vaata eksperimendi andmed läbi**. Avaneb kolmanda osapoole teenus, kus saate mõõdikuid kontrollida ja teha kindlaks, milline variatsioon oli parim.
1. Valige saidiehitaja dialoogimenüüs **Eksperimendi lõpetamine** parim variatsioon ja seejärel valige **Edasi**.
1. Avage kolmanda osapoole teenus ja peatage eksperiment.
1. Valige saidiehitajas suvand **Lõpeta**, et kirjutada üle originaalne aktiivne leht ja avaldada parim variatsioon nii, et see on saadaval kõigile teie veebisaidi kasutajatele. 

> [!NOTE]
> Kui otsustate praegust aktiivset lehte säilitada ja variatsiooni mitte avaldada, valige **Avalda originaalne leht uuesti**.

## <a name="delete-your-experiment"></a>Eksperimendi kustutamine
Kuigi te ei pea lõpetatud eksperimenti rakenduses Commerce kustutama, võite selle kustutada, et säästa ruumi või puhastada oma tööruumi. Eksperimendi kustutamiseks tehke järgmist.

1. Avage saidiehitajas vahekaart **Eksperimendid** ja valige eksperiment. 
    > [!NOTE]
    > Kui eksperiment on ikka aktiivne, peatage eksperiment enne jätkamist kolmanda osapoole teenuses.
1. Valige käsuribalt **Tühista avaldamine**, et eemaldada variatsiooni sisu aktiivselt saidilt.
1. Valige käsuribalt **Kustuta**, et eksperiment kustutada.

## <a name="previous-step"></a>Eelmine etapp
[Eksperimendi käitamine ja jälgimine](experimentation-run-monitor.md)
