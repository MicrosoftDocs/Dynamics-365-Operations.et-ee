---
title: Kliendi jaoks mahakandmise töölehe loomine
description: See ülesande juhend näitab, kuidas seadistada mahakandmiste parameetreid ja seejärel kandeid lehelt Sissenõuded, Kliendiarvete avamine ja Klient maha kanda.
author: ShivamPandey-msft
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e810badf9b43a3b0e57390b05247113021e26b6a0242cf29022274307c5fd56
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771796"
---
# <a name="create-a-write-off-journal-for-a-customer"></a>Kliendi jaoks mahakandmise töölehe loomine

[!include [banner](../../includes/banner.md)]

See ülesande juhend näitab, kuidas seadistada mahakandmiste parameetreid ja seejärel kandeid lehelt Sissenõuded, Kliendiarvete avamine ja Klient maha kanda. See ülesanne kasutab demoettevõtte USMF andmeid.


## <a name="set-up-the-write-off-parameters"></a>Mahakandmise parameetrite seadistamine
1. Avage **Navigeerimispaan > Moodulid > Krediidihaldus ja võlanõuded > Seadistus > Müügireskontro parameetrid**.
2. Klõpsake vahekaarti **Võlanõuded**.
3. Laiendage või ahendage jaotis **Mahakandmine**.
    - **Mahakandmise tööleht** on päevaraamat, mis hoiustab teie loodud mahakandmiskandeid.  
    - Saate lisada igale mahakandmisele põhjusekoodi. Saate selle vaikeväärtuse mahakandmisel alistada.  
    - Seadke suvandi **Eralda käibemaks** väärtuseks Jah, kui soovite eraldada käibemaksu algsest kandest mahakandmisel.  
4. Sulgege leht.
5. Avage **Krediit ja sissenõuded > Seadistus > Kliendi sisestusreeglid**. Mahakandmise kontot kasutatakse kulukontona või reservi kohandamiseks pearaamatus.
6. Sulgege leht.

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a>Kliendi saldo mahakandmine aegunud saldode lehelt
1. Avage **Krediit ja sissenõudmised > Sissenõudmised > Aegunud kliendisaldod**.
2. Märkige kliendi puhul rida, mille soovite maha kanda. Näiteks märkige rida, millel on ettevõte Birch Company.
3. Paanil **Toimingupaan** klõpsake **Võta vastu**.
4. Klõpsake **Kanna maha**.
5. Klõpsake valikut **OK**.
6. Sulgege leht.
7. Avage **Navigeerimispaan > Moodulid > Pearaamat > Töölehe kanded > Päevaraamatud**.
8. Valige töölehe partiinumber töölehe puhul, mis sisaldab teie mahakandmist. Kliendi saldo tühistamiseks luuakse üks rida. Üks või mitu rida luuakse mahakandmise sisestamiseks mahakandmiskontole.  
9. Sulgege leht.
10. Sulgege leht.

## <a name="write-off-transactions-from-the-collections-form"></a>Kannete mahakandmine sissenõuete vormilt.
1. Avage **Krediit ja sissenõudmised > Sissenõudmised > Aegunud kliendisaldod**.
2. Valige kliendi nimi, kelle kandeid soovite maha kanda. Näiteks valige Cave Wholesales (US-004).
3. Märkige esimese kande rida.
4. Märkige teise kande rida.
5. Klõpsake **Kanna maha**.
6. Väljale **Põhjuse kommentaar** sisestage "Halvad võlad".
7. Klõpsake valikut **OK**.
8. Sulgege leht.
9. Sulgege leht.
10. Avage **Pearaamat > Töölehe kanded > Päevaraamatud**.
11. Valige töölehe partiinumber töölehe puhul, mis sisaldab teie mahakandmist. Kliendi saldo tühistamiseks luuakse üks rida. Üks või mitu rida luuakse mahakandmise sisestamiseks mahakandmiskontole.  
12. Sulgege leht.
13. Sulgege leht.

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a>Arve mahakandmine lehelt Klientide arvete avamine
1. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Arved > Avatud kliendiarved**.
2. Märkige arve rida. Näiteks, märkige rida CIV-000667 jaoks.
3. Paanil **Toimingupaan** klõpsake **Arve**.
4. Klõpsake **Kanna maha**.
5. Klõpsake valikut **OK**.
6. Sulgege leht.

## <a name="write-off-a-customer-balance-from-the-customer-page"></a>Kliendi saldo mahakandmine kliendi lehelt
1. Avage **Müügireskontro > Kliendid > Kõik kliendid**.
2. Valige kliendi konto. Näiteks, valige US-001 (Contoso Jaemüük San Diego).
3. Paanil **Toimingupaan** klõpsake **Võta vastu**.
4. Klõpsake **Kanna maha**.
5. Klõpsake valikut **OK**.
6. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]