---
title: Eksperimendi ühendamine ja variatsioonide redigeerimine
description: Selles teemas kirjeldatakse, kuidas ühendada kolmanda osapoole teenuses olev eksperiment rakendusega Dynamics 365 Commerce ja redigeerida eksperimendi variatsioone.
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
ms.openlocfilehash: 030640ba8907ae52c198ac96ad2c243b533d8c53
ms.sourcegitcommit: 7592c2dec0428d56843ab395d2a52c89f77f99b5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096963"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Eksperimendi ühendamine ja variatsioonide redigeerimine

Selles teemas kirjeldatakse, kuidas ühendada oma eksperiment rakenduses Commerce ning variatsioone muuta, et need ühtiks teie hüpoteesiga. 

Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce. Täiendavad etapid on toodud eraldi teemades.

[ ![Eksperimendi kasutaja teekond – ühendamine ja redigeerimine](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Kui olete kolmanda osapoole teenuses [oma eksperimendi seadistanud](experimentation-setup.md), ühendate eksperimendi rakendusega Dynamics 365 Commerce ja redigeerite eksperimendi variatsioone.

## <a name="planning-considerations"></a>Plaanimine

Enne kui ühendate oma eksperimendi rakenduses Commerce, peate tegema mõne otsuse, mis mõjutavad seda, kuidas Commerce teie sisu haldab.

### <a name="determine-the-scope-of-your-experiment"></a>Oma eksperimendi ulatuse määratlemine
Eksperimendi ühendamisel palutakse teil määratleda eksperimendi ulatus. Eksperimentide ulatus võib olla **osaline** või **terve**.
- Valige **osaline** , kui soovite teha eksperimenti lehe kindla osa põhjal. Selle suvandi valimisel peate määrama, millised moodulid eksperimenti kaasatakse. Eksperimendiga mitteseotud vaikelehe või fragmendi osade muudatused sünkroonitakse automaatselt kõikides variatsioonides.
- Valige **terve** , kui soovite eksperimendis kasutada tervet lehte või fragmenti. Luuakse vaikelehe või fragmendi eraldi koopiad. Te ei pea valima, millised moodulid on eksperimenti kaasatud, kuna kogu redigeerimispind on muutmiseks saadaval. Saate mooduleid lisada, kustutada või järjekorda seada nii, nagu on vaja. Kui aga muudetakse eksperimendiga seotud vaikelehte või fragmenti, tuleb need muudatused kõigis variatsioonides käsitsi sünkroonida.

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> Kui seostate oma eksperimendi lehega, mis kasutab paigutust, saate määrata eksperimendi ulatuseks ainult **terve**.

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a>Otsustamine, kas soovite ajastada seda, millal teie eksperiment avaldatakse
Kui soovite ajastada seda, millal teie eksperiment aktiivsel saidil avaldatakse, veenduge *enne* eksperimendi ühendamist, et eksperimendiga seostatav sisu on saadaval avaldamisrühmas. 

Lisateavet avaldamisrühmade kohta leiate teemast [Avaldamisrühmadega töötamine](publish-groups.md).


## <a name="connect-your-experiment"></a>Eksperimendi ühendamine
Oma eksperimendi ühendamiseks käivitate viisardi **Eksperimendi ühendamine**. Viisardist leiate oma eksperimendi ühendamiseks vajalikud sammud. Kui viisard on lõpule jõudnud, on teie eksperiment ühendatud ja luuakse muudatused, mis on redigeerimiseks valmis.

Oma eksperimendi ühendamise alustamiseks Commerce'i saidiehitajaga, toimige järgmiselt.

1. Viisardi **Eksperimendi ühendamine** käivitamiseks valige vasakpoolselt paanilt **Eksperimendid** ja seejärel valige **Ühenda**. Teine võimalus viisardile juurde pääsemiseks lehe või fragmendi redaktori kaudu, on selle redigeerimine ja suvandi **Eksperimendi ühendamine** valimine käsureal.

    > [!NOTE]
    > Lehe saab korraga ühendada ainult ühe eksperimendiga. Lehe ühendamiseks teise eksperimendiga kustutage esiteks see eksperiment, millega leht on praegu ühendatud.

1. Valige leht või fragment, mida soovite eksperimendis kasutada.
1. Seadistage eksperimendi ulatus **osaliseks** või **terveks** , lähtudes valikust, mille tegite ülaltoodud jaotises [Oma eksperimendi ulatuse määratlemine](#determine-the-scope-of-your-experiment).
    > [!NOTE]
    > Funktsiooni **Lehtede või fragmentide kasutamine eksperimentides** lipp peab olema lubatud, kui soovite eksperimendis kasutada tervet lehte või fragmenti. Lisateavet leiate teemast [Eksperimenteerimine rakenduses Dynamics 365 Commerce](experimentation-overview.md).
    
1. Viisardi viimases etapis valige **Loo variatsioonid ja välju viisardist**. Eksperimendi jaoks luuakse variatsioonid. 

## <a name="edit-your-variations"></a>Variatsioonide redigeerimine
Viisardist väljumisel luuakse teie jaoks variatsioonid. 

Seejärel redigeerige variatsioone nii, et need peegeldaksid valikuid, mida te peate eksperimendi hüpoteesis kontrollima. Valige üks järgmistest meetoditest, mis vastab teie eksperimendi ulatusele, mille valisite ülaltoodud teemas [Oma eksperimendi ulatuse määratlemine](#determine-the-scope-of-your-experiment).

### <a name="edit-variations-for-experiments-with-partial-scope"></a>Variatsioonide redigeerimine osalise ulatusega eksperimentide puhul
Kui määrasite viisardis **Eksperimendi ühendamine** oma eksperimendi ulatuseks **osaline** , toimige järgmiselt.

1. Kasutage redaktoris käsuriba all asuvat variatsioonide rippmenüüd, et redigeerida iga variatsiooni oma algse hüpoteesi alusel. Samuti võite tahta luua kontroll- või baasvariatsiooni, jättes ühe variatsiooni muutmata.
1. Valige moodul, mida eksperimendis kasutada, valige kolmikpunkt (...) ja seejärel valige **Lisa eksperimendile**.

### <a name="edit-variations-for-experiments-with-entire-scope"></a>Variatsioonide redigeerimine täisulatusega eksperimentide puhul
Kui määrasite viisardis **Eksperimendi ühendamine** oma eksperimendi ulatuseks **terve** , kasutage käsuriba all olevat variatsioonide rippmenüüd, et redigeerida iga variatsiooni algse hüpoteesi alusel. 

> [!NOTE]
> Mõlemal juhul võite tahta ka luua kontroll- või baasvariatsiooni, jättes ühe variatsiooni muutmata.

## <a name="previous-step"></a>Eelmine etapp
[Eksperimendi seadistamine](experimentation-setup.md) 


## <a name="next-step"></a>Järgmine etapp
[Eksperimendi eelversioon ja avaldamine](experimentation-preview-publish.md)
