---
title: "Automaatne tasakaalustus ja prioriteetide kindlaksmääramisel"
description: "See artikkel kirjeldab, kuidas kandeid tasakaalustatakse, kui teete lehel Müügireskontro parameetrid valiku Automaatne tasakaalustamine. Samuti selgitab see, kuidas automaatset tasakaalustamist saab koos makse prioriteediga kasutada."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: a751973b49febd6925267d00fb1d2c72114f86b0
ms.lasthandoff: 03/31/2017


---

# <a name="automatic-settlement-and-prioritization"></a>Automaatne tasakaalustus ja prioriteetide kindlaksmääramisel

See artikkel kirjeldab, kuidas kandeid tasakaalustatakse, kui teete lehel Müügireskontro parameetrid valiku Automaatne tasakaalustamine. Samuti selgitab see, kuidas automaatset tasakaalustamist saab koos makse prioriteediga kasutada.

Maksete tasakaalustamisel arvete ja muude kannetega on kaks võimalust. Valige käsitsi tehingute arveldamiseks või Microsoft Dynamics 365 operatsioonid saab valida kandeid automaatselt automaatne tasakaalustus funktsiooni abil. Saate kohandada ka automaatsete tasakaalustuste töötlemise viisi, kasutades suvandit **Tasakaalustuse prioriseerimine**. Kõik need valikud on osa tasakaalustuse parameetreid, mis on määratletud nende **Müügireskontro parameetrid** lehel. Kannete automaatse tasakaalustamise viis võib erineda, sõltuvalt meetodist, mida automaatseks tasakaalustamiseks kasutate. Saadaval on järgmised meetodid:

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
| Viivisearve | 15. oktoober  | 7,00   |                     |                    | Käesolev huvi on arve 1 ja arve 2. Summa arvutatakse 2% intressi summad, mis on 30 või enam päeva üle tähtaja. Näide: 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="userdefined-settlement-priority"></a>Userdefined lahendamise prioriteet
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
| Arve 3     | 10/15/2015 |         | 500,00                         | 350.00           | 150.00  | USA dollar      |
| Viivisearve | 10/15/2015 |         | 7,00                           | 0,00             | 0,00    | USA dollar      |




