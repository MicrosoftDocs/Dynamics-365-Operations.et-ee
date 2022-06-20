---
title: Eksperimendi seadistamine
description: See artikkel kirjeldab, kuidas seadistada katsetus kolmanda osapoole teenuses.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946162"
---
# <a name="set-up-an-experiment"></a>Eksperimendi seadistamine

Pärast [hüpoteesi määratlemist ja eksperimendi edumõõdikute kindlaks määramist](experimentation-identify.md) peate oma eksperimendi seadistama kolmanda osapoole teenuses. Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce. Lisa sammud on kaetud eraldi artikliga.

[ ![Eksperimendi kasutaja teekond – seadistamine.](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Eksperimendi seadistamine kolmanda osapoole teenuses
Nüüdseks peaks teil olema valitud kolmanda osapoole teenus oma eksperimendi käitamiseks ja jälgimiseks ning eksperimendi konnektori seadistamiseks. Need eeltingimused on loetletud teemas [Eksperimenteerimine rakenduses Dynamics 365 Commerce](experimentation-overview.md).

Järgige samme, mis on vajalikud eksperimendi loomiseks kolmanda osapoole teenuses. Kui konnektor on õigesti konfigureeritud, siis kuvatakse kolmanda osapoole teenuses seadistatud eksperimentide täielik loend Commerce'i saidiehitajas umbes viie minuti jooksul.

## <a name="set-up-your-success-metrics"></a>Edumõõdikute seadistamine
Iga eksperiment vajab mõõdikuid variatsioonide mõju mõõtmiseks ja hüpoteesi kontrollimiseks. Järgige alltoodud samme, et lubada mõõdikute arvutamine kolmanda osapoole teenuses, kasutades reaalajas telemeetriasündmusi rakendusest Dynamics 365 Commerce.

Oma eduka mõõdikute seadistamiseks boksist väljas moodulitele järgige neid samme.

1. Valige Commerce'i saidiehitajas vasakpoolselt navigeerimispaanilt vahekaart **Lehed** ja seejärel valige leht, mille jaoks soovite mõõdikuid koguda. 
1. Avage jaotis **Jälgitavad sündmuse ID-d** jälgitava lehe või mooduli parempoolselt atribuudipaanilt.
1. Valige suvand **Kuva**. Kuvatakse kõigi klõpsamise sündmuse-ID-de loend. Kopeerige sündmus, mida soovite jälgida, ja kleepige sündmuse võti kolmanda osapoole teenuses määratud asukohta. Kui vajate rohkem kui üht sündmust, kopeerige võtmed ükshaaval. 
1. Kasutage lehekülje vaadete SHA-256 lehenime väärtust saidikonstruktoris, mis on lisatud `.PageView`. Näiteks sündmuse ID oleks `Homepage.PageView``e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9`.
1. Kui kolmanda osapoole teenuses on vaja mõõdikute jälgimiseks veel midagi teha, tehke seda.

Kohandatud mooduli klõpsamiseks järgige neid samme klõpsamissündmuste vahendina:

1. Valmistage ette **TelemetryContent** objekt mooduli jaoks, kasutades allolevat funktsiooni. See funktsioon võtab sisendina lehe nime, mooduli nime ja SDK-antud vaikimisi telemeetriaobjekti.

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    Näide: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. Looge lastiandmed, mis sisaldavad teavet selle kohta, mida on vaja hõivata. Nuppude ja muude staatiliste juhtelementide jaoks saate kaasata **teksti** nagu "Ost kohe" või "Otsing". Ja komponentide jaoks, millel klõpsake näiteks tootekaardil klõpsamist, saate saata RecID **,** mis on toote kirje ID või toote ID.

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    Staatiliste juhtelementide näitena läbige nupu tekstistring, nagu allpool näidatud:

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    Tootek klõpsamise näitena läbige toote recordId, nagu allpool näidatud.

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. Sündmuse registreerimiseks **kutsuge funktsioon OnClick**.

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    Näide:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>Eelmine etapp
[Hüpoteesi tuvastamine ja eksperimendi mõõdikute määramine](experimentation-identify.md) 


## <a name="next-step"></a>Järgmine etapp
[Eksperimendi ühendamine ja redigeerimine](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
