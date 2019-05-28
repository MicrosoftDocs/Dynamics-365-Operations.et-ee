---
title: Märgukirjade töötlemine
description: See protseduur kirjeldab märgukirjade loomist, printimist ja sisestamist.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8a3f74d2891c050294e089eae14ba2386449d7c9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549625"
---
# <a name="process-collection-letters"></a>Märgukirjade töötlemine

[!include [banner](../../includes/banner.md)]

See protseduur kirjeldab märgukirjade loomist, printimist ja sisestamist. See ülesanne kasutab demoettevõtte USMF andmeid.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Märgukirjaseeria häälestamine sisestusreeglis
1. Avage **Krediit ja sissenõuded > Seadistus > Kliendi sisestusreeglid**.
2. Klõpsake valikut **Redigeeri**.
3. Valige ripploendist märgukirjaseeria. Kui te ei soovi luua kannete jaoks märgukirju selle sisestusreegliga, jätke väli tühjaks.  
4. Tabeli piirangu vahekaardil saate laiendada seda, kuidas sissenõudekirju töödeldakse. Kui väli on seatud olekusse **Jah**, luuakse märgukirjad selle sisestusreegli jaoks.  

## <a name="create-collection-letters"></a>Sissenõude märgukirjade loomine
1. Avage jaotis **Krediit ja sissenõuded > Märgukiri > Märgukirjade loomine**.
2. Valige kandetüübid, mille jaoks märgukirjad luuakse. Kõik seda tüüpi avatud kanded kaasatakse kalkulatsiooni.  
2. Valige üks suvand väljalt **Märgukiri**.
3. Sisestage märgukirja kuupäev.
4. Valige sisestusreegel, kui määrasite suvandi **Kasuta sisestusreegleid** olekusse **Vali**. Sisestusreegli jaoks kaks võimalust:   
   - **Konto** – kasutab iga viivisearve kohta kliendi kontole määratud sisestusreeglit.   
   - **Vali** – kasutage sisestusreeglit, mille valite väljal **Sisestusreegel**.  
5. Jaotise kaasamiseks laiendage valikut **Kirjed**.
6. Klõpsake käsku **Filtreeri**.
7. Sisestage kliendi ID väljale **Kriteeriumid**. Sisestage näiteks US-001.
8. Klõpsake nupul **OK**.
9. Klõpsake nupul **OK**.

## <a name="print-collection-letters"></a>Märgukirjade printimine
1. Avage jaotis **Krediit ja sissenõuded > Märgukiri > Märgukirjade ülevaatamine ja töötlemine**.
2. Valige väljal **Olek** suvand **Loodud**.
3. Valige väljal **Prinditud** suvand **Printimata**.
4. Klõpsake **Prindi**.
5. Klõpsake suvandit **Märgukirja märkus**.
6. Jaotise kaasamiseks laiendage valikut **Kirjed**.
7. Sisestage sisestamiste äralõikekuupäev.
8. Märgukirja printimiseks klõpsake **OK**.
9. Märgukirja sisestamine.
   1. Klõpsake käsku **Sisesta**.
   2. Sisestage märgukirja sisestuskuupäev.
   3. Jaotise kaasamiseks laiendage valikut **Kirjed**.
   4. Klõpsake nupul **OK**.
   5. Valige väljal **Olek** suvand **Sisestatud**.
   6. Valige suvand väljal **Prinditud**.

## <a name="control-collection-letters-at-the-customer-level"></a>Märgukirjade kontrollimine kliendi tasemel
Saate ka seadistada märgukirjad kliendi tasemel nii, et iga kande märgukirjakoodi jälgitakse, kuid märgukirja töötlemine põhineb ühe märgukirja tasemel, mis on kliendi jaoks talletatud. Üks märgukiri sisaldab kõiki kandeid, mis on kliendi tähtaja ületanud. Ajapikenduse päeva jälgitakse nüüd kliendi tasemel, järgmist märgukirja ei saadeta enne ajapikenduse päevade arvu möödumist enne järgmise märgukirja saatmise tähtaega, kuigi pärast viimase märgukirja saatmist on kannete tähtaeg ületatud. See suvand vähendab kliendi kohta saadetavate märgukirjade arvu. 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Märgukirjade kontrollimise seadistamine kliendi tasemel
1.  Avage **Krediit ja kollektsioonid > Seadistus > Müügireskontro parameetrid** ja klõpsake vahekaardil **Sissenõuded**. 
2.  Muutke suvandi **Loomine märgukirja kohta** väärtuseks **Klient**. 
3.  Avage jaotis **Krediit ja sissenõuded > Märgukiri > Märgukirjade ülevaatamine ja töötlemine**. Kõikide tähtaja ületanud kannete kohta luuakse kliendile ainult üks märgukiri.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Eira märgukirja koodi arvutamisel makseid ja kreeditarveid
Kui kaasate maksed ja kreeditarved märgukirjas kaasatavatesse kannetesse, võivad maksed või kreeditarved käivitada märgukirja. Saate määrata, kuidas maksed ja kreeditarved kontrollivad märgukirja koodi, muutes väärtust **Ignoreerida maksete ja kreeditarvete märgukirjakoodi arvutamisel** parameetrit. 

Märgukirja koodi arvutamisel maksete ja kreeditarvete eiramiseks tehke järgmist.
1. Avage **Krediit ja kollektsioonid > Seadistus > Müügireskontro parameetrid** ja klõpsake vahekaardil **Sissenõuded**. 
2. Muutke suvandi **Märgukirja koodi arvutamisel maksete ja kreeditarvete eiramine** väärtuseks **Jah**.
