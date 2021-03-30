---
title: Valuuta ümberarvutamine konsolideeritavas ettevõttes
description: Selles teemas kirjeldatakse valuuta ümberhindamist konsolideeritud ettevõttes.
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81de31ee75b4be38256505bc7b875dc15473c75a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212225"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a>Valuuta ümberarvutamine konsolideeritavas ettevõttes

[!include [banner](../includes/banner.md)]

Kui konsolodeerite andmeid ühelt arveldusvaluutalt teisele, peate siiski käivitama valuuta ümberarvestamise, kui vahetuskurssides on muutusi, et teie konto saldo arvestataks õigesti ümber. Kasutage algsel andmete konsolideerimisel vahekaarti **Valuuta teisendamine**, et valida algsed vahetuskursid ümberarvestamiseks konsolideerimisprotsessi käigus. Pärast uue vahetuskursi sisestamist (näiteks järgmisel kuul) peate konto saldo ümber arvutama. Realiseerimata kasumeid või kahjumeid värskendatakse vastavalt uue vahetuskursi ja kuupäeva alusel. Järgnev näide illustreerib raamatupidamiskandeid, mis luuakse protsessi ajal.

## <a name="company-setup"></a>Ettevõtte seadistus
-   **Lähte-/töötav ettevõte (USMF)** – USA dollareid (USD) kasutatakse arvestus- ja aruandlusvaluutana.
-   **Konsolideeritud ettevõte (CON)** – eurosid (EUR) kasutatakse arvestus- ja aruandlusvaluutana.
    -   **Realiseeritud kasum** – pearaamatukonto 801500
    -   **Realiseeritud kahjum** – pearaamatukonto 801600
    -   **Realiseerimata kasum** – pearaamatukonto 801600
    -   **Realiseerimata kahjum** – pearaamatukonto 801400

## <a name="original-transactions"></a>Algsed kanded
### <a name="cash-receipt-transactions-in-usmf"></a>Kassaorderi kanded USMF-is

| Kuupäev       | Pearaamatu konto               | Valuuta | Summa |
|------------|------------------------------|----------|--------|
| 11.10.2015 | 110110 – sularaha                | USA dollar      | 500    |
| 11.10.2015 | 130100 – müügireskontro | USA dollar      | –500   |

## <a name="exchange-rates"></a>Vahetuskursid

| Valuutast | Valuutaks | Alguskuupäev | Vahetuskurss |
|---------------|-------------|------------|---------------|
|  eurot           | USA dollar         | 1.10.2015  | 200           |
|  eurot           | USA dollar         | 1.11.2015  | 150           |
|  eurot           | USA dollar         | 1.12.2012  | 100           |

## <a name="perform-the-consolidation-for-october-2015"></a>2015. aasta oktoobri konsolideerimine
### <a name="balances-in-the-consolidation-company"></a>Konsolideeritava ettevõtte saldod

| Pearaamatu konto | Valuuta | Summa | Arvutus    |
|----------------|----------|--------|----------------|
| 110110         |  eurot      | 250    | 500 USD × 50%  |
| 130100         |  eurot      | –250   | –500 USD × 50% |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a>Perioodi 1. oktoober 2015 kuni 30. november 2015 kontode valuuta ümberarvutamine
### <a name="balances-in-the-consolidation-company"></a>Konsolideeritava ettevõtte saldod

| Pearaamatu konto | Valuuta | Summa  | Arvutus                        |
|----------------|----------|---------|------------------------------------|
| 110110         |  eurot      | 333,33  | Algne summa 500 × 66,6667%  |
| 130100         |  eurot      | –333,33 | Algne summa –500 × 66,6667% |
| 801400         |  eurot      | 83,33   | 333,33 – 250                       |
| 801600         |  eurot      | –83,33  | –333,33 – (–250)                   |

Näete aruandlusvaluuta summade puhul lisakandeid.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a>Perioodi 1. oktoober 2015 kuni 31. detsember 2015 kontode valuuta ümberarvutamine
### <a name="balances-in-the-consolidation-company"></a>Konsolideeritava ettevõtte saldod

| Pearaamatu konto | Valuuta | Summa  | Arvutus                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         |  eurot      | 500,00  | Algne summa 500 × 1                           |
| 130100         |  eurot      | –500,00 | Algne summa –500 × 1                          |
| 801400         |  eurot      | 250     | 500 – 333,33 = 166,67 166,67 + 83,33 = 250           |
| 801600         |  eurot      | –250    | –500 – (–333,33) = –166,67 –166,67 + (–83,33) = –250 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]