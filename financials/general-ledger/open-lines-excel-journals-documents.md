---
title: "Tööleheridade ja dokumentide avaldamine Excelist"
description: "See teema selgitab, kuidas sisestada ja avaldada päevaraamatute ridasid Microsoft Excelist. See sisaldab ka teavet mitmesuguste mallide kohta, mida sisestatava kande tüübist olenevalt kasutada saate."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 087339cb3002b42bcb985c2ccfc2d97c752a817c
ms.lasthandoff: 03/31/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Tööleheridade ja dokumentide avaldamine Excelist

See teema selgitab, kuidas sisestada ja avaldada päevaraamatute ridasid Microsoft Excelist. See sisaldab ka teavet mitmesuguste mallide kohta, mida sisestatava kande tüübist olenevalt kasutada saate.

Kasutajad saavad sisestada ja avaldada finantstöölehtede ridu Microsoft Excelist. Pärast töölehe loomist kuvab nupp **Ava read Excelis** saadaolevad mallid. Mallid on mõeldud konkreetsete stsenaariumide toetamiseks, kuid töölehel ei toetata iga kontotüübi kombinatsiooni. Järgmises tabelis on näidatud saadaolevad mallid ja kontotüübid, mida need toetavad.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Mall**             | **Toetatud kontotüübid**                                                                                             | **Mallile juurdepääsemise viis**                                                          |
| Pearaamatu töölehe read     | Toetatakse järgmisi. Konto: Pearaamat, Klient, Hankija, Pank Vastaskonto: Pearaamat, Klient, Hankija, Kontsernisisene pank.       | Päevaraamat                                                                         |
| Arveregister         | Ei toetata järgmisi. Konto: Hankija Vastaskonto: Kontsernisisene pearaamat.                                                    | AP-arveregister                                                                     |
| Arve tööleht          | Toetatakse järgmisi. Kontod: Hankija Vastaskonto: Kontsernisisene pearaamat.                                                      | AP arve tööleht                                                                      |
| Hankija arve           |                                                                                                                         | Hankija arve                                                                          |
| Kliendiarvete tööleht | Toetatakse järgmisi. Konto: Kliendi Vastaskonto: Kontsernisisene pearaamat.                                                     | Päevaraamat                                                                         |
| Vabas vormis arve        |                                                                                                                         | Klõpsake lehel **Vabas vormis arve** valikut **Ava Excelis** (Microsoft Office’i ikoon). |
| Põhivarade tööleht     | Pearaamatu, panga, kliendi või hankija vara. Kontsernisisest ei toetata.                                               | Põhivara tööleht                                                                     |
| Hankija maksetööleht   | Toetatakse järgmisi. Konto: Hankija Vastaskonto: Pearaamat, Kontsernisisene pank.                                                 | Hankija maksetööleht                                                                  |
| Kliendimaksete tööleht | Toetatakse järgmisi. Konto: Kliendi Vastaskonto: Pearaamat, Kontsernisisene pank.                                               | Kliendimaksete tööleht                                                                |
| Projektikulu tööleht  | Toetatakse järgmisi. Konto: Projekt, Pearaamat, Klient, Hankija Vastaskonto: Projekt, Pearaamat, Klient, Hankija, Kontsernisisene. | Päevaraamatu kulu (jaotises Projektihaldus ja raamatupidamine).                       |

Kui read on avaldatud, siis neid kontrollitakse, veendumaks, et need vastavad finantstöölehtedel seadistatud reeglitele. Pärast ridade avaldamist saavad kasutajad redigeerida või sisestada kandeid Microsoft Dynamics 365 for Operationsist. 

Finantsdimensioonide lisamiseks mallile on vajalikud täiendavad muudatused. Lisateavet leiate jaotisest [Dimensioonide lisamine Microsoft Exceli mallile](\dev-itpro\financial-dimensions\add-dimensions-excel-templates). Pärast seda, kui üksusele on dimensioonid lisatud, on need Exceli kujundajas saadaval ja neid saab mallile lisada.




