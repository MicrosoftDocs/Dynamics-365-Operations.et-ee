---
title: Eksperimenteerimine rakenduses Dynamics 365 Commerce
description: Eksperimenteerimine võimaldab saidiehitajas luua, redigeerida ja hallata lehe paigutust ning sisukäsitlusi. Terviklik eksperimenteerimise tugi on lubatud e-kaubanduse lehtede ja lehel olevate üksuste jaoks.
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
ms.openlocfilehash: 85eb7a661cc66c42699797cca4fa6820941de7c0
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/22/2020
ms.locfileid: "4097135"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Eksperimenteerimine rakenduses Dynamics 365 Commerce
Eksperimenteerige rakenduses Dynamics 365 Commerce, et kinnitada hüpoteese oma e-kaubanduse lehtede tõhususe kohta ja langetada otsuseid andmetel põhineva kindlustundega. Commerce toetab lehtede, moodulite ja fragmentide A/B-testimist ning võimaldab teil mõõta väljapakutud muudatuste mõju oma veebisaidile.

Saate luua, redigeerida ning hallata lehe- ja sisukäsitlusi, mida nimetatakse Commerce'i saidiehitajas **variatsioonideks**. Commerce integreerub kolmanda osapoole teenustega, mida saate kasutada eksperimentide loomiseks ja käsitluste määramiseks. Commerce'is jäädvustatud reaalajas sündmuste vood võimaldavad teha analüüse, mis määravad eksperimendi tulemused kolmanda osapoole teenuses. Seejärel saate neid analüüse kasutada, et oma hüpoteesi toetada või ümber lükata.

## <a name="set-up-prerequisites"></a> Seadistuse eeltingimused
1. **Hankige Commerce'i õige versioon** – värskendage oma mooduliteek, veebikanali laiendatavuse tarkvara arenduse komplekt (SDK) ja Commerce Scale Unit rakenduse Commerce'i versioonile 10.0.13 või uuemale.
1. **Eksperimendi konnektori seadistamine** – eksperimendi konnektor võimaldab rakendusel Commerce ühenduda kolmanda osapoole teenustega, et hankida eksperimentide loend ja teha kindlaks, millal kasutajale eksperimenti näidata. Saate osta kolmanda osapoole konnektori siit: [AppSource](https://appsource.microsoft.com). Järgige avaldaja installijuhiseid. Saate teise võimalusena kasutada näidistestkonnektorit rakenduses Commerce, et testida eksperimenteerimistöövoogu ilma, et peaksite välist teenust konfigureerima. Lisateavet leiate teemast [Konnektorite konfigureerimine ja lubamine](e-commerce-extensibility/connectors.md). 
1. **Lülitage sisse eksperimenteerimisfunktsiooni lipud rakenduses Commerce** – saate lubada eksperimenteerimise rentnikutasemel, avades **Rentniku sätted > Funktsioonid** , või saiditasemel kohas **Sätted > Funktsioonid**.
    - Lubage **Eksperimenteerimise** lipp, et luua lehel moodulite eksperimendivariatsioonid ilma eksperimenti mittekuuluvat sisu muutmata või kopeerimata. See tagab, et jätkuvad sisuvärskendused väljaspool eksperimenti on eksperimendi elutsükli jooksul sünkroonitud. Selle lipu keelamise korral ei näidata kasutajatele ühtki eksperimente ja eemaldatakse saidiehitajast kõik redigeerimisfunktsioonid.
    - Lubage lipp **Lehtede või fragmentide kasutamine eksperimentides** , et kasutada lehte või fragmenti eksperimendis. See loob lehel või fragmendis olevate kõikide moodulite puhul terve lehe või fragmendi täieliku koopia. Kasutage seda režiimi, kui soovite testida sisu suuri muudatusi või juhul, kui jätkuvate sisumuudatuste sünkroniseerimine kõikides eksemplarides pole oluline. Selle lipu keelamine takistab uute eksperimentide loomist ja redigeerimist lehtedel ning fragmentides.
    > [!NOTE]
    > Lipp **Eksperimenteerimine** peab olema samuti lubatud, et töötaks funktsioon **Lehtede või fragmentide kasutamine eksperimentides**.
    
## <a name="experimentation-lifecycle"></a>Eksperimenteerimise elutsükkel
Eksperimendi seadistamine, variatsioonide loomine ja eksperimendi käitamine on iteratiivne protsess. Allolev diagramm illustreerib eksperimendi elutsüklit rakenduses Commerce ja kolmanda osapoole teenuses. 

[ ![Eksperimenteerimise elutsükkel](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Lisateavet iga eksperimenteerimisprotsessi etapi kohta leiate järgmistest teemadest.
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
