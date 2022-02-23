---
title: Märgukirjade töötlemine
description: See teema kirjeldab märgukirjade loomist, printimist ja sisestamist.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 2b8ce102086535a5462d3fa0e8ac76e9ec3dd15c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442301"
---
# <a name="process-collection-letters"></a>Märgukirjade töötlemine

[!include [banner](../../includes/banner.md)]

See teema kirjeldab märgukirjade loomist, printimist ja sisestamist. See ülesanne kasutab demoettevõtte USMF andmeid.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Märgukirjaseeria häälestamine sisestusreeglis
1. Minge **Navigeerimispaan > Moodulid > Kreedit ja sissenõuded > Häälestus > Kliendi postitusprofiil**.
2. Klõpsake valikut **Redigeeri**.
3. Valige ripploendist märgukirjaseeria. Kui te ei soovi luua kannete jaoks märgukirju selle sisestusreegliga, jätke väli tühjaks.  
4. Laiendage **Tabeli piirangut**, et muuta viisi, kuidas sissenõudekirju töödeldakse. Kui väli on seatud olekusse **Jah**, luuakse märgukirjad selle sisestusreegli jaoks.  

## <a name="create-collection-letters"></a>Sissenõude märgukirjade loomine
1. Minge **Navigatsioonipaan > Moodulid > Krediit ja sissenõuded > Sissenõudekiri > Sissenõudekirja loomine**.
2. Valige kandetüübid, mille jaoks märgukirjad luuakse. Kõik seda tüüpi avatud kanded kaasatakse kalkulatsiooni.  
3. Valige üks suvand väljalt **Märgukiri**.
4. Sisestage väljale **Sissenõudekirja kuupäev** sissenõudekirja kuupäev.
5. Valige sisestusreegel, kui määrasite suvandi **Kasuta sisestusreegleid** olekusse **Vali**. Sisestusreegli jaoks kaks võimalust:   

   - **Konto** – kasutab iga viivisearve kohta kliendi kontole määratud sisestusreeglit.   
   - **Vali** – kasutage sisestusreeglit, mille valite väljal **Sisestusreegel**.  

6. Jaotise kaasamiseks laiendage valikut **Kirjed**.
7. Valige **Filter**.
8. Sisestage kliendi ID väljale **Kriteeriumid**. Sisestage näiteks US-001.
9. Valige nupp **OK**.
10. Valige nupp **OK**.

## <a name="print-collection-letters"></a>Märgukirjade printimine
1. Minge **navigatsioonipaan > Moodulid > Krediit ja sissenõuded > Sissenõudekiri > Sissenõudekirjade ülevaade ja töötlemine**.
2. Valige väljal **Olek** suvand **Loodud**.
3. Valige väljal **Prinditud** suvand **Printimata**.
4. Valige **Prindi**.
5. Valige  **Sissenõudekiri**.
6. Sisestage moodulisse **Parameetrid** sisestuste sulgemiskuupäev.
7. Laiendage moodulit **Kirjed kaasamiseks** ja sisestage sissenõudekirja märkme üksikasjad.
8. Sissenõudekirja printimiseks klõpsake **OK**.
9. Märgukirja sisestamine.

    1. Valige **Sisesta**.
    1. Sisestage märgukirja sisestuskuupäev.
    1. Jaotise kaasamiseks laiendage valikut **Kirjed**.
    1. Valige nupp **OK**.
    1. Valige väljal **Olek** suvand **Sisestatud**.
    1. Valige suvand väljal **Prinditud**.

## <a name="control-collection-letters-at-the-customer-level"></a>Märgukirjade kontrollimine kliendi tasemel
Kui märgukirjad seadistatakse kandetasemel, võidakse luua mitu kirja kliendi kohta kande ajalise jaotuse põhjal. Kui kanded kuvatakse muus kirjade järjestuses, luuakse eraldi märgukirjad iga tähtaja ületanud kandegrupi jaoks kliendi kohta. Seetõttu võib üks klient saada näiteks ühe märgukirja 60 päeva tähtaja ületanud kannete kohta ja teise märgukirja 90 päeva tähtaja ületanud kannete kohta. 

Iga märgukiri on seostatud ka märgukirjakoodiga. Märgukirjakood seostatakse üksikute kannetega ja seda kasutatakse määratlemiseks, millal tuleks luua iga kande jaoks järgmine märgukiri. Näiteks kui kanne on 30 päeva tähtaja ületanud, määratleb märgukirjakood, et järgmine märgukiri saadetakse siis, kui kanne on 60 päeva üle tähtaja, kui seda pole selleks ajaks ära makstud. 

Märgukirju saab seadistada ka klienditasemel. Sellisel juhul iga kande märgukirjakoodi jälgitakse, kuid märgukirja töötlemine põhineb ühe märgukirja tasemel, mis on kliendi jaoks talletatud. Üks märgukiri sisaldab kõiki kandeid, mis on kliendi tähtaja ületanud. Ajapikenduse päeva jälgitakse nüüd kliendi tasemel, järgmist märgukirja ei saadeta enne ajapikenduse päevade arvu möödumist enne järgmise märgukirja saatmise tähtaega, kuigi pärast viimase märgukirja saatmist oli kannete tähtaeg ületatud. See suvand aitab vähendada iga kliendi kohta saadetavate märgukirjade arvu.

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Märgukirjade kontrollimise seadistamine kliendi tasemel
1.  Minge **Navigatsioonipaan > Moodulid > Krediit ja sissenõuded > Seadistus > Müügireskontro parameetrid** ja klõpsake vahekaardil **Sissenõuded**. 
2.  Muutke suvandi **Loomine märgukirja kohta** väärtuseks **Klient**. 
3.  Minge **navigatsioonipaan > Moodulid > Krediit ja sissenõuded > Sissenõudekiri > Sissenõudekirjade ülevaade ja töötlemine**. Kõikide tähtaja ületanud kannete kohta luuakse kliendile ainult üks märgukiri.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Eira märgukirja koodi arvutamisel makseid ja kreeditarveid
Kui kaasate maksed ja kreeditarved märgukirjas kaasatavatesse kannetesse, võivad maksed või kreeditarved käivitada märgukirja. Saate määrata, kuidas maksed ja kreeditarved kontrollivad märgukirja koodi, muutes väärtust **Ignoreerida maksete ja kreeditarvete märgukirjakoodi arvutamisel** parameetrit. 

Märgukirja koodi arvutamisel maksete ja kreeditarvete eiramiseks tehke järgmist.

1. Minge **Navigatsioonipaan > Moodulid > Krediit ja sissenõuded > Seadistus > Müügireskontro parameetrid** ja klõpsake vahekaardil **Sissenõuded**. 
2. Muutke suvandi **Märgukirja koodi arvutamisel maksete ja kreeditarvete eiramine** väärtuseks **Jah**.
