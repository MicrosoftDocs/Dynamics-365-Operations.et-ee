---
title: Kliendi jaoks mahakandmise töölehe loomine
description: See ülesande juhend näitab, kuidas seadistada mahakandmiste parameetreid ja seejärel kandeid lehelt Sissenõuded, Kliendiarvete avamine ja Klient maha kanda.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cd576458bab1e4654d21773b581a5b0f726c928
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545508"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>Kliendi jaoks mahakandmise töölehe loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See ülesande juhend näitab, kuidas seadistada mahakandmiste parameetreid ja seejärel kandeid lehelt Sissenõuded, Kliendiarvete avamine ja Klient maha kanda. See ülesanne kasutab demoettevõtte USMF andmeid.


## <a name="set-up-the-write-off-parameters"></a>Mahakandmise parameetrite seadistamine
1. Tehke valik Krediit ja sissenõuded > Seadistus > Ostureskontro parameetrid.
2. Klõpsake vahekaarti Sissenõuded.
3. Laiendage või ahendage jaotist Mahakandmine.
    * Mahakandmise tööleht on peažurnaal, millel on teie loodud mahakandmise kanded.  
    * Saate lisada igale mahakandmisele põhjusekoodi. Saate selle vaikeväärtuse mahakandmisel alistada.  
    * Kui soovite mahakandmisel käibemaksu algsest kandest eristada, määrake see suvandile Jah.  
4. Sulgege leht.
5. Avage Krediit ja sissenõuded > Seadistus > Kliendi sisestusreeglid.
    * Mahakandmiskontot kasutatakse peažurnaalil kulu kontona või korrigeerimise reserveerimiseks   
6. Sulgege leht.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Kliendi saldo mahakandmine aegunud saldode lehelt
1. Tehke valik Krediit ja sissenõuded > Sissenõuded > Aegunud saldod.
2. Märkige kliendi puhul rida, mille soovite maha kanda. Näiteks märkige rida, millel on ettevõte Birch Company.
3. Klõpsake toimingupaanil suvandit Sissenõudmine.
4. Klõpsake valikut Mahakandmine.
5. Klõpsake nuppu OK.
6. Sulgege leht.
7. Avage Pearaamat > Töölehe sisestused > Päevaraamatud.
8. Valige töölehe partiinumber töölehe puhul, mis sisaldab teie mahakandmist.
    * Kliendi saldo tühistamiseks luuakse üks rida. Üks või mitu rida luuakse mahakandmise sisestamiseks mahakandmiskontole.  
9. Sulgege leht.
10. Sulgege leht.

## <a name="write-off-transactions-from-the-collections-form"></a>Kannete mahakandmine sissenõuete vormilt.
1. Tehke valik Krediit ja sissenõuded > Sissenõuded > Aegunud saldod.
2. Valige kliendi nimi, kelle kandeid soovite maha kanda. Näiteks valige Cave Wholesales (US-004).
3. Märkige esimese kande rida.
4. Märkige teise kande rida.
5. Klõpsake valikut Mahakandmine.
6. Sisestage väljale Põhjuse kommentaar suvand Halvad võlad.
7. Klõpsake nuppu OK.
8. Sulgege leht.
9. Sulgege leht.
10. Avage Pearaamat > Töölehe sisestused > Päevaraamatud.
11. Valige töölehe partiinumber töölehe puhul, mis sisaldab teie mahakandmist.
    * Kliendi saldo tühistamiseks luuakse üks rida. Üks või mitu rida luuakse mahakandmise sisestamiseks mahakandmiskontole.  
12. Sulgege leht.
13. Sulgege leht.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Arve mahakandmine lehelt Klientide arvete avamine
1. Avage Müügireskontro > Arved > Kliendiarvete avamine.
2. Märkige arve rida. Näiteks, märkige rida CIV-000667 jaoks.
3. Klõpsake toimingupaanil valikut Arve.
4. Klõpsake valikut Mahakandmine.
5. Klõpsake nuppu OK.
6. Sulgege leht.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Kliendi saldo mahakandmine kliendi lehelt
1. Avage Müügireskontro > Kliendid > Kõik kliendid.
2. Valige kliendi konto. Näiteks valige US-001 (Contoso Retail San Diego).
3. Klõpsake toimingupaanil suvandit Sissenõudmine.
4. Klõpsake valikut Mahakandmine.
5. Klõpsake nuppu OK.
6. Sulgege leht.

