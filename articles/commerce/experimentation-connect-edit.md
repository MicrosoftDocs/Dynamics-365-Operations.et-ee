---
title: Eksperimendi ühendamine ja variatsioonide redigeerimine
description: See artikkel kirjeldab, kuidas ühendada katsetus kolmanda osapoole Dynamics 365 Commerce teenuses ja kuidas redigeerida katsetusvariatsioone.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: dcdbd61976402ddd719ece184a86692fbc7c628d
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942818"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Eksperimendi ühendamine ja variatsioonide redigeerimine

See artikkel kirjeldab, kuidas ühendada oma ärikatseid ja teha muudatusi oma variatsioonides, nii et need ühtivad soovitud ärilahendustega. 

Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks eksperimendi seadistamise ja käivitamisega rakenduses Dynamics 365 Commerce. Lisa sammud on kaetud eraldi artikliga.

[ ![Eksperimendi kasutaja teekond – ühendamine ja redigeerimine.](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Kui olete kolmanda osapoole teenuses [oma eksperimendi seadistanud](experimentation-setup.md), ühendate eksperimendi rakendusega Dynamics 365 Commerce ja redigeerite eksperimendi variatsioone.

## <a name="connect-your-experiment"></a>Eksperimendi ühendamine
Oma eksperimendi ühendamiseks käivitate viisardi **Eksperimendi ühendamine**. Viisardist leiate oma eksperimendi ühendamiseks vajalikud sammud. Kui viisard on lõpule jõudnud, on teie eksperiment ühendatud ja luuakse muudatused, mis on redigeerimiseks valmis.

Oma eksperimendi ühendamise alustamiseks Commerce'i saidiehitajaga, toimige järgmiselt.

1. Viisardi **Eksperimendi ühendamine** käivitamiseks valige vasakpoolselt paanilt **Eksperimendid** ja seejärel valige **Ühenda**. Teine võimalus viisardile juurde pääsemiseks lehe või fragmendi redaktori kaudu, on selle redigeerimine ja suvandi **Eksperimendi ühendamine** valimine käsureal.

    > [!NOTE]
    > - Lehe saab korraga ühendada ainult ühe eksperimendiga. Lehe ühendamiseks teise eksperimendiga kustutage esiteks see eksperiment, millega leht on praegu ühendatud.
    > - Võite katsetada vaid kohandatud paigutusega lehtedel. Kui teie lehel on eelseadistatud paigutus, teisendage see esmalt kohandatud paigutuseks. Seda saate teha, kui valite käsuribalt Teisenda **kohandatud** paigutuseks. Lisateavet kavandite kohta vt eelseadistatud [ja kohandatud kavanditest](templates-layouts-overview.md#preset-and-custom-layouts). 

1. Kui loote ühenduse katsega **vahekaardi Katsetus, mis asub vasakus** navigeerimispaanis, valige kuvatavast loendist katsetusnimi.
1. Valige leht või tükk, millele soovite katsetada.
1. Viisardi viimases etapis valige **Loo variatsioonid ja välju viisardist**. Eksperimendi jaoks luuakse variatsioonid. 

> [!NOTE]
> Kui soovite ajastada seda, millal teie eksperiment aktiivsel saidil avaldatakse, veenduge *enne* eksperimendi ühendamist, et eksperimendiga seostatav sisu on saadaval avaldamisrühmas. Lisateavet avaldamisrühmade kohta leiate teemast [Avaldamisrühmadega töötamine](publish-groups.md).

## <a name="edit-your-variations"></a>Variatsioonide redigeerimine

Kui väljute Connecti **katseviisardist**, luuakse variatsioonid teie eest. Järgige alltoodud samme variatsioonide redigeerimiseks, et need kajastaksid valikuid, mida peate katsetada katsetuskontrolli käigus.

1. Kasutage redaktoris käsuriba all asuvat variatsioonide rippmenüüd, et redigeerida iga variatsiooni oma algse hüpoteesi alusel. Samuti võite tahta luua kontroll- või baasvariatsiooni, jättes ühe variatsiooni muutmata.
1. Valige moodul, mida eksperimendis kasutada, valige kolmikpunkt (...) ja seejärel valige **Lisa eksperimendile**.

> [!NOTE]
> Kaaluge juhtelemendi või baasmuutuse loomise, jättes ühe variatsioonist muutmata.

## <a name="previous-step"></a>Eelmine etapp
[Eksperimendi seadistamine](experimentation-setup.md) 


## <a name="next-step"></a>Järgmine etapp
[Eksperimendi eelversioon ja avaldamine](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
