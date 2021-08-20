---
title: Variatsiooni esiletõstmine ja eksperimendi lõpuleviimine
description: See teema kirjeldab, kuidas rakenduses Dynamics 365 Commerce edukat variatsiooni esile tõsta ja eksperimenti lõpule viia.
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
ms.openlocfilehash: 48d66e84ce52e77e83843853e3d528f9394a7676cadc4a4be5198065696dd10e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738742"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a>Variatsiooni esiletõstmine ja eksperimendi lõpuleviimine

Selles teemas kirjeldatakse, kuidas tõsta esile variatsiooni, mis sai teie eksperimendis parima tulemuse, ja kuidas eksperimenti lõpule viia. Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce. Täiendavad etapid on toodud eraldi teemades.

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

Eksperimendi kustutamiseks Commerce'i saidiehitajas, toimige järgmiselt.

1. Valige vasakpoolsel navigeerimispaanil **Eksperimendid** ja seejärel valige eksperiment. 
    > [!NOTE]
    > Kui eksperiment on ikka aktiivne, peatage eksperiment enne jätkamist kolmanda osapoole teenuses.
1. Valige käsuribalt **Tühista avaldamine**, et eemaldada variatsiooni sisu aktiivselt saidilt.
1. Eksperimendi kustutamiseks valige **Kustuta**.

## <a name="previous-step"></a>Eelmine etapp
[Katse käitamine ja jälgimine](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]