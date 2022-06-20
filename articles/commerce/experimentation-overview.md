---
title: Eksperimenteerimine rakenduses Dynamics 365 Commerce
description: Eksperimenteerimine võimaldab saidiehitajas luua, redigeerida ja hallata lehe paigutust ning sisukäsitlusi. Terviklik eksperimenteerimise tugi on lubatud e-kaubanduse lehtede ja lehel olevate üksuste jaoks.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: overview
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1ef877072ba7ffe1b0326cf8d526b512b5ab30b8
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946200"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Eksperimenteerimine rakenduses Dynamics 365 Commerce
Eksperimenteerige rakenduses Dynamics 365 Commerce, et kinnitada hüpoteese oma e-kaubanduse lehtede tõhususe kohta ja langetada otsuseid andmetel põhineva kindlustundega. Commerce toetab lehtede, moodulite ja fragmentide A/B-testimist ning võimaldab teil mõõta väljapakutud muudatuste mõju oma veebisaidile.

Saate luua, redigeerida ning hallata lehe- ja sisukäsitlusi, mida nimetatakse Commerce'i saidiehitajas **variatsioonideks**. Commerce integreerub kolmanda osapoole teenustega, mida saate kasutada eksperimentide loomiseks ja käsitluste määramiseks. Commerce'is jäädvustatud reaalajas sündmuste vood võimaldavad teha analüüse, mis määravad eksperimendi tulemused kolmanda osapoole teenuses. Seejärel saate neid analüüse kasutada, et oma hüpoteesi toetada või ümber lükata.

## <a name="set-up-prerequisites"></a> Seadistuse eeltingimused

1. **Hankige Commerce'i õige versioon** – värskendage oma mooduliteek, veebikanali laiendatavuse tarkvara arenduse komplekt (SDK) ja Commerce Scale Unit rakenduse Commerce'i versioonile 10.0.13 või uuemale.
1. **Eksperimendi konnektori seadistamine** – eksperimendi konnektor võimaldab rakendusel Commerce ühenduda kolmanda osapoole teenustega, et hankida eksperimentide loend ja teha kindlaks, millal kasutajale eksperimenti näidata. Saate osta kolmanda osapoole konnektori siit: [AppSource](https://appsource.microsoft.com). Järgige avaldaja installijuhiseid. Saate teise võimalusena kasutada näidistestkonnektorit rakenduses Commerce, et testida eksperimenteerimistöövoogu ilma, et peaksite välist teenust konfigureerima. Lisateavet leiate teemast [Konnektorite konfigureerimine ja lubamine](e-commerce-extensibility/connectors.md). 
1. **Lülitage proovimise funktsiooni lipp** äris sisse – **\>** võite lubada katsetuse rentniku tasemel, **lülitudes rentniku sätete funktsioonidele või saidi tasemel, lülitudes saidi sätete funktsioonidele.\>** Lülitage katsetuse **lipp mooduli** variatsioonide loomiseks sisse. Selle lipu keelamise korral ei näidata kasutajatele ühtki eksperimente ja eemaldatakse saidiehitajast kõik redigeerimisfunktsioonid.
    
## <a name="experimentation-lifecycle"></a>Eksperimenteerimise elutsükkel

Eksperimendi seadistamine, variatsioonide loomine ja eksperimendi käitamine on iteratiivne protsess. Allolev diagramm illustreerib eksperimendi elutsüklit rakenduses Commerce ja kolmanda osapoole teenuses. 

[ ![Eksperimenteerimise elutsükkel.](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Lisateavet iga katsetusprotsessi sammu kohta leiate järgmistest artiklitest.
- [Hüpoteesi tuvastamine ja eksperimendi mõõdikute määramine](experimentation-identify.md)
- [Katse seadistamine](experimentation-setup.md)
- [Katse ühendamine ja redigeerimine](experimentation-connect-edit.md)
- [Katse eelversioon ja avaldamine](experimentation-preview-publish.md)
- [Eksperimendi käitamine ja jälgimine](experimentation-run-monitor.md)
- [Variatsiooni soodustamine ja katse lõpuleviimine](experimentation-review-complete.md)

> [!NOTE]
> Et saada teada, kus eksperiment elutsüklis on, valige saidiehitaja vasakpoolsel paanil **Eksperimendid**. Kuvatakse eksperimentide loend koos iga eksperimendi olekuga nii rakenduses Commerce kui ka kolmanda osapoole teenuses. Lisateavet leiate teemast [Eksperimendi oleku ülevaatamine](experimentation-status.md).

## <a name="next-step"></a>Järgmine etapp
[Hüpoteesi tuvastamine ja eksperimendi edumõõdikute määramine](experimentation-identify.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
