---
title: Tööleheridade ja dokumentide avaldamine Excelist
description: See artikkel selgitab, kuidas sisestada ja avaldada ridu üldtöölehtede jaoks Microsoft Excel. See sisaldab ka teavet mitmesuguste mallide kohta, mida sisestatava kande tüübist olenevalt kasutada saate.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccb3e7a420f7f048ba93b6fadf5491e312e7ce33
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872466"
---
# <a name="publish-journal-lines-and-documents-from-excel"></a>Tööleheridade ja dokumentide avaldamine Excelist

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas sisestada ja avaldada ridu üldtöölehtede jaoks Microsoft Excel. See sisaldab ka teavet mitmesuguste mallide kohta, mida sisestatava kande tüübist olenevalt kasutada saate.

Kasutajad saavad sisestada ja avaldada finantstöölehtede ridu Microsoft Excelist. Pärast töölehe loomist kuvab nupp **Ava read Excelis** saadaolevad mallid. Mallid on mõeldud konkreetsete stsenaariumide toetamiseks, kuid töölehel ei toetata iga kontotüübi kombinatsiooni. Järgmises tabelis on näidatud saadaolevad mallid ja kontotüübid, mida need toetavad.

| Mall             | Toetatud kontotüübid | Mallile juurdepääsemise viis                                                          |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| Pearaamatu töölehe read     | Toetatakse järgmisi. Konto: Pearaamat, Klient, Hankija, Pank Vastaskonto: Pearaamat, Klient, Hankija, Kontsernisisene pank.       | Päevaraamat                                                                         |
| Arveregister         | Ei toetata järgmisi. Konto: Hankija Vastaskonto: Kontsernisisene pearaamat.                                                    | AP-arveregister                                                                     |
| Arve tööleht          | Toetatakse järgmisi. Kontod: Hankija Vastaskonto: Kontsernisisene pearaamat.                                                      | AP arve tööleht                                                                      |
| Hankija arve           |                                                                                                                         | Hankija arve                                                                          |
| Kliendiarvete tööleht | Toetatakse järgmisi. Konto: Kliendi Vastaskonto: Kontsernisisene pearaamat.                                                     | Päevaraamat                                                                         |
| Vabas vormis arve        |                                                                                                                         | Klõpsake lehel **Vabas vormis arve** käsku **Ava Excelis** (Microsoft Office’i ikoon). |
| Põhivarade tööleht     | Pearaamatu, panga, kliendi või hankija vara. Kontsernisisest ei toetata.                                               | Põhivara tööleht                                                                     |
| Hankija maksetööleht   | Toetatakse järgmisi. Konto: Hankija Vastaskonto: Pearaamat, Kontsernisisene pank.                                                 | Hankija maksetööleht                                                                  |
| Kliendimaksete tööleht | Toetatakse järgmisi. Konto: Kliendi Vastaskonto: Pearaamat, Kontsernisisene pank.                                               | Kliendimaksete tööleht                                                                |
| Projektikulu tööleht  | Toetatakse järgmisi. Konto: Projekt, Pearaamat, Klient, Hankija Vastaskonto: Projekt, Pearaamat, Klient, Hankija, Kontsernisisene. | Päevaraamatu kulu (jaotises Projektihaldus ja raamatupidamine).                       |

Kui read on avaldatud, siis neid kontrollitakse, veendumaks, et need vastavad finantstöölehtedel seadistatud reeglitele. Pärast ridade avaldamist saavad kasutajad Dynamics 365 Finance'i kandeid redigeerida või sisestada. 

Finantsdimensioonide lisamiseks mallile on vajalikud täiendavad muudatused. Lisateavet vt teemast [Dimensioonide lisamine Microsoft Exceli mallile](../../fin-ops-core/dev-itpro/financial/add-dimensions-excel-templates.md). Pärast seda, kui üksusele on dimensioonid lisatud, on need Exceli kujundajas saadaval ja neid saab mallile lisada.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
