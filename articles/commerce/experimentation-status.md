---
title: Eksperimendi oleku ülevaatamine
description: See artikkel selgitab, milline on katsetuse olek katsetustsüklis Dynamics 365 Commerce.
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
ms.openlocfilehash: 818435a7c901d2a6b876b9c9db27faffc8b322fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877245"
---
# <a name="review-the-status-of-an-experiment"></a>Eksperimendi oleku ülevaatamine
Eksperimendi seadistamine ja käitamine rakenduses Dynamics 365 Commerce hõlmavad palju samme. Lisateavet eksperimendi elutsükli kohta leiate teemast [Eksperimenteerimine rakenduses Dynamics 365 Commerce](experimentation-overview.md).

Et saada teada, kus eksperiment elutsüklis on, valige Commerce'i saidiehitaja vasakpoolsel paanil **Eksperimendid**. Kuvatakse loend eksperimentidest, mille olek on toodud nii rakenduses Commerce kui ka kolmanda osapoole teenuses, mida kasutatakse eksperimentide loomise lubamiseks, variatsioonide määramiseks ja andmete analüüsimiseks.

Veerus **Commerce'i olek** võidakse kuvada järgmised väärtused. 
- **Mustand** – eksperiment on seotud lehe või fragmendiga rakenduses Commerce ning seda redigeeritakse.
- **Avaldatud** – eksperimendi variatsioonid on teie veebisaidil kuvamiseks valmis. Kui eksperimenti käitatakse kolmanda osapoole teenuses, näevad veebisaidi kasutajad lehe või fragmendi variatsiooni, mille valis kolmanda osapoole teenus.
- **Avaldamata** – eksperiment ei ole enam teie veebisaidil saadaval. Isegi kui eksperimenti käitatakse kolmanda osapoole teenuses, näevad veebisaidi kasutajad ainult lehe või fragmendi vaikeversiooni.
- **Lõpetatud** – eksperiment on oma rada kulgenud ja variatsioon tõsteti kõigi veebisaidi kasutajate jaoks esile.

Sarnaselt võidakse veerus **kolmanda osapoole olek** kuvada järgmiseid väärtusi, et näidata, millises olekus on eksperimendid kolmanda osapoole teenuses.
- **Mustand** – eksperiment on kolmanda osapoole teenuses seadistatud, kuid seda ei ole alustatud.
- **Käitamine** – eksperiment käivitati kolmanda osapoole teenuses ja kogub andmeid.
- **Peatatud** – eksperiment on peatatud ja andmeid ei koguta. Uuesti andmete kogumiseks peate eksperimenti jätkama.
- **Arhiivitud** – eksperiment on oma rada kulgenud ja salvestati kolmanda osapoole teenusesse hilisemaks vaatamiseks.

Allolevas diagrammis on toodud mõlemat olekute kogumid ja see, kuidas need üksteisega seotud on.

[ ![Eksperimenteerimise olekud.](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)


[!INCLUDE[footer-include](../includes/footer-banner.md)]