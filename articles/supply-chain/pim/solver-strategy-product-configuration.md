---
title: Lahendaja strateegia toote konfiguratsiooni jaoks
description: "Selles teemas kirjeldatakse, kuidas kasutada lahendaja strateegiat toote konfiguratsiooni jõudluse parandamiseks."
author: cvocph
manager: AnnBe
ms.date: 01/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8075abccdcdde21df967dcc9948a738895f35cef
ms.openlocfilehash: 035103b183c637dcce454686d44535a6fa07c745
ms.contentlocale: et-ee
ms.lasthandoff: 01/25/2018

---

# <a name="solver-strategy-for-product-configuration"></a>Lahendaja strateegia toote konfiguratsiooni jaoks

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas kasutada lahendaja strateegiat toote konfiguratsiooni jõudluse parandamiseks.

Lahendaja strateegia mõiste võeti esimest korda kasutusele rakenduse Microsoft Dynamics AX 2012 R2 kumulatiivses värskenduses 7 (CU7). Seda laiendati rakenduste Microsoft Dynamics AX 2012 R3 ja Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 kumulatiivses värskenduses 8 (CU8).

Lahendaja strateegia mõiste hõlmab nüüd järgmisi strateegiaid.

- Vaikimisi
- Minimaalsed domeenid kõigepealt
- Ülevalt alla
- Z3

## <a name="solver-strategy"></a>Lahendaja strateegia 

Toote konfiguratsioonimudeli on [piirangu rahulolu probleem](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf). Microsoft Solver Foundation (MSF) pakub toote konfiguratsioonimudelite kaudu kasutatavate piirangu rahuldamise probleemide lahendamiseks kahte tüüpi lahendaja strateegiaid. Need lahendaja strateegiad sõltuvad [heuristikast](https://techterms.com/definition/heuristic), mida kasutatakse probleemi lahendamisel piirandu rahuldamise probleemide muutujate järjekorra kindlaks määramiseks. Heuristika võib oluliselt mõjutada probleemi või probleemide klassi lahendamise jõudlust.

Rakenduses Finance and Operations määrab toote konfiguratsioonimudelite lahendaja strateegia selle, millist lahendajat heuristikas kasutatakse. Strateegiad **Vaikimisi**, **Minimaalsed domeenid kõigepealt** ja **Ülevalt alla** kasutavad kahte MSF-i lahendajat, kusjuures strateegia **Z3** kasutab lahendajat Z3. 

Tõelised kliendijuurutamisuuringud on näidanud, et toote konfiguratsioonimudeli lahendaja strateegiate muutmine võib vähendada reageerimisaega minutitelt millisekunditele. Seetõttu on tasub toote konfiguratsioonimudeli tõhusaimi strateegia leidmiseks proovida eri lahendaja strateegiaid.

## <a name="change-the-settings-for-the-solver-strategy"></a>Lahendaja strateegia sätete muutmine

Lahendaja strateegia muutmiseks tehke lehe **Toote konfiguratsioonimudelid** toimingupaanil valik **Mudeli atribuudid**. Seejärel valige dialoogiboksis **Mudeli üksikasjade redigeerimine** lahendaja strateegia.

[![Lahendaja strateegia muutmine](./media/solver-strategy.png)](./media/solver-strategy.png)

Praegu ei ole olemas loogikat, mis tuvastaks automaatselt, milline lahendaja strateegia on piirangupõhiste toote konfiguratsioonimudelite jaoks kõige tõhusam. Seetõttu tuleb proovida lahendaja strateegiaid ükshaaval.

Järgmine tabel pakub soovitusi lahendaja strateegia kasutamiseks eri stsenaariumide korral.

| Lahendaja strateegia      | Stsenaarium, milles strateegiat saab kasutada |
|----------------------|-----------------------------------|
| Vaikimisi              | Strateegia **Vaikimisi** on optimeeritud lahendama mudeleid, mis sõltuvad tabeli piirangutest. Kliendijuurutamisuuringud on näidanud, et see strateegia on kõige tõhusam stsenaariumides, kus tabeli piiranguid kasutatakse ulatuslikult. |
| Minimaalne domeen kõigepealt | Strateegiad **Minimaalne domeen kõigepealt** ja **Ülalt alla** on omavahel tihedalt seotud. Kliendijuurutamisuuringud on näidanud, et CUB-s kasutusele võetud strateegia **Ülalt alla** on strateegiast **Minimaalne domeen kõigepealt** tõhusam. Strateegiat **Minimaalne domeen kõigepealt** hoitakse tootes tagasiühilduvuseks. Mõlemad lahendaja strateegiad on tõhusamad selliste mudelite lahendamises, mis sisaldavad mitut aritmeetilist avaldist, kus ei kasutata tabelipiiranguid. Mõnel juhul on aga strateegia **Vaikimisi** neist kahest tõhusam. Seetõttu on oluline proovida kõiki strateegiaid. |
| Ülevalt alla             | Strateegiad **Minimaalne domeen kõigepealt** ja **Ülalt alla** on omavahel tihedalt seotud. Kliendijuurutamisuuringud on näidanud, et CUB-s kasutusele võetud strateegia **Ülalt alla** on strateegiast **Minimaalne domeen kõigepealt** tõhusam. Strateegiat **Minimaalne domeen kõigepealt** hoitakse tootes tagasiühilduvuseks. Mõlemad lahendaja strateegiad on tõhusamad selliste mudelite lahendamises, mis sisaldavad mitut aritmeetilist avaldist, kus ei kasutata tabelipiiranguid. Mõnel juhul on aga strateegia **Vaikimisi** neist kahest tõhusam. Seetõttu on oluline proovida kõiki strateegiaid. |
| Z3                   | Strateegiat **Z3** soovitame kasutada lahendaja vaikestrateegiana. Kui muretsete jõudluse ja mastaabitavuse pärast, saate hinnata teisi strateegiaid. |

## <a name="additional-resources"></a>Lisaressursid

[Toote konfiguratsioonimudeli koostamine](build-product-configuration-model.md)

[Heuristika](https://techterms.com/definition/heuristic)

[Piirangu rahuldamise probleem](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)

