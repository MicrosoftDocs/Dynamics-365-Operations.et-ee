---
title: Automaatne tasakaalustus ja prioritiseerimine
description: See artikkel kirjeldab, kuidas kandeid tasakaalustatakse, kui teete lehel Müügireskontro parameetrid valiku Automaatne tasakaalustamine. Samuti selgitab see, kuidas automaatset tasakaalustamist saab koos makse prioriteediga kasutada.
author: ShivamPandey-msft
ms.date: 01/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd5b894c82beb1b5d69ad6bf485161ab9c91a806
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855516"
---
# <a name="automatic-settlement-and-prioritization"></a>Automaatne tasakaalustus ja prioritiseerimine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas kandeid tasakaalustatakse, kui teete lehel Müügireskontro parameetrid valiku Automaatne tasakaalustamine. Samuti selgitab see, kuidas automaatset tasakaalustamist saab koos makse prioriteediga kasutada.

Maksete tasakaalustamisel arvete ja muude kannetega on kaks võimalust. Saate valida tasakaalustatavad kanded käsitsi või süsteem võib valida kanded automaatselt, kasutades automaatse tasakaalustamise funktsiooni. Saate kohandada ka automaatsete tasakaalustuste töötlemise viisi, kasutades suvandit **Tasakaalustuse prioriseerimine**. Kõik need suvandid on osa tasakaalustuse parameetritest, mis on määratletud lehel **Müügireskontro parameetrid**. Kannete automaatse tasakaalustamise viis võib erineda, sõltuvalt meetodist, mida automaatseks tasakaalustamiseks kasutate. Saadaval on järgmised meetodid:

-   Kasutaja määratletud tasakaalustuse prioriteet
-   Vaikimisi automaatne tasakaalustus

Järgmised jaotised kirjeldavad, kuidas iga meetodi puhul kandeid tasakaalustatakse.

## <a name="example-transactions"></a>Näidiskanded
Selles artiklis allpool toodud tasakaalustuste näited põhinevad järgmistel kannetel. Kõik kanded on kliendi 2050 kohta.

| Kanne   | Kuupäev        | Summa | Skonto tingimused | Skonto kuupäev | Kommentaarid                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Arve 1     | 15. august   | 100,00 | 2%14, neto 30        | 29. august          |                                                                                                                                                                                               |
| Arve 2     | 1. september | 250,00 | 2%14, neto 30        | 15. september       |                                                                                                                                                                                               |
| Arve 3     | 15. oktoober  | 500,00 | 2% 14/neto 30        | 29. oktoober         |                                                                                                                                                                                               |
| Viivisearve | 15. oktoober  | 7,00   |                     |                    | Viivisearve on 1. ja 2. arve kohta. Summa arvutatakse kaheprotsendilise intressina summadelt, mis on vähemalt 30 päeva üle tähtaja. Näide: 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="user-defined-settlement-priority"></a>Kasutaja määratletud tasakaalustuse prioriteet
Kui valite lehel **Müügireskontro parameetrid** suvandi **Kasuta automaatseteks tasakaalustusteks prioriteeti** sätteks **Jah**, kasutatakse kannete automaatseks tasakaalustamiseks valimisel tasakaalustusprioriteeti, mille määratlete lehel **Tasakaalustuse prioriteet**. Selle näite puhul on määratletud järgmine tasakaalustusprioriteet.

1.  Kande tüüp
    -   Maksetasu
    -   Märgukirjad
    -   Viivisearved
    -   Arved

2.  Kande kuupäev kasvavalt
3.  Kanne

Kui sisestate 25. oktoobril makse summas 700,00, tasakaalustatakse makse kannetele järgmises järjestuses.

| Kanne       | Kuupäev       | Arve | Summa kandevaluutas | Tasakaalustatav summa | Saldo | Valuuta |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Viivisearve | 10/15/2015 |         | 7,00                           | 7,00             | 0,00    | USA dollar      |
| Arve 1     | 8/15/2015  | 10001   | 100,00                         | 100,00           | 0,00    | USA dollar      |
| Arve 2     | 9/1/2015   | 10002   | 250,00                         | 250,00           | 0,00    | USA dollar      |
| Arve 3     | 10/15/2015 |         | 500,00                         | 343.00           | 157.00  | USA dollar      |

## <a name="default-automatic-settlement"></a>Vaikimisi automaatne tasakaalustus
Kui kasutaja määratletud tasakaalustuse prioriteet puudub, valitakse kanded tasakaalustuseks automaatselt tähtaja alusel. Tasakaalustatud kannetel peab olema sama valuuta, nagu kandel, millega nad tasakaalustatakse. Kui sisestate 25. oktoobril makse summas 700,00, valitakse tasakaalustamiseks järgmised kanded.

| Kanne       | Kuupäev       | Arve | Summa kandevaluutas | Tasakaalustatav summa | Saldo | Valuuta |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Arve 1     | 8/15/2015  | 10001   | 100,00                         | 100,00           | 0,00    | USA dollar      |
| Arve 2     | 9/1/2015   | 10002   | 250,00                         | 250,00           | 0,00    | USA dollar      |
| Arve 3     | 10/15/2015 |         | 500.00                         | 350.00           | 150.00  | USA dollar      |
| Viivisearve | 10/15/2015 |         | 7.00                           | 0,00             | 7.00    | USA dollar      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
