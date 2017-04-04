---
title: "Töölehe ridade ja Exceli dokumente"
description: "See teema selgitab, kuidas sisestada ja avaldada üldist Microsoft Exceli töölehtede read. See sisaldab teavet erinevate Mallid, mille abil saab, sõltuvalt tehingute sisestamise."
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

# <a name="publish-journal-lines-and-documents-from-excel"></a>Töölehe ridade ja Exceli dokumente

See teema selgitab, kuidas sisestada ja avaldada üldist Microsoft Exceli töölehtede read. See sisaldab teavet erinevate Mallid, mille abil saab, sõltuvalt tehingute sisestamise.

Kasutajad saavad sisestada ja avaldada finants Microsoft Exceli töölehtede read. Pärast seda, kui kasutaja loob žurnaali, mille **ridade Excelis avada** nuppu kuvatakse saadaolevaid malle. Malle on teatud olukordades, mitte aga iga liigi kombinatsioon toetab ajakirja toetada. Järgmine tabel näitab saadaolevaid malle ja need toetavad kontotüüpide.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Template**             | **Toetatud tüübid**                                                                                             | **Kuidas on võimalik saada Mall**                                                          |
| Pearaamatu töölehe read     | Konto: Pearaamatu, kliendi, hankija, panga korvata konto: pearaamatu, kliendi, hankija, panga IC on toetatud.       | Päevaraamat                                                                         |
| Arveregister         | Konto: Hankija vastaskonto: pearaamatu IC ei toetata.                                                    | AP arve register                                                                     |
| Arve tööleht          | Ettevõtted: Hankija vastaskonto: pearaamatu IC on toetatud.                                                      | AP arve tööleht                                                                      |
| Hankija arve           |                                                                                                                         | Hankija arve                                                                          |
| Kliendiarvete tööleht | : Konto kliendi nihe: pearaamatu IC on toetatud.                                                     | Päevaraamat                                                                         |
| Vabas vormis arve        |                                                                                                                         | Kohta ning **vabas vormis arve** klõpsake valikul **Excelis avatud** (Microsoft Office ikoon). |
| Põhivarade tööleht     | Vara pearaamatu, panga, kliendi või hankija. IC ei toetata.                                               | Põhivara tööleht                                                                     |
| Hankija maksetööleht   | Konto: Hankija vastaskonto: pearaamatu, panga IC on toetatud.                                                 | Hankija maksetööleht                                                                  |
| Kliendimaksete tööleht | : Konto kliendi nihe: pearaamatu, panga IC on toetatud.                                               | Kliendimaksete tööleht                                                                |
| Projektikulu tööleht  | Konto: Projekti, pearaamatu, kliendi, hankija vastaskonto kontole: projekti, pearaamatu, kliendi, hankija IC on toetatud. | Peažurnaali kulu (all projektihaldus ja raamatupidamine)                       |

Ridade avaldamisel andmed on kinnitatud tagada nende vastavus seatud rahalist töölehtedel eeskirju. Pärast seda, kui avaldatakse read, kasutajad saavad redigeerida või sisestada kandeid Microsoft Dynamics 365 toiminguteks. 

Lisamiseks mallile finantsdimensioonide nõutakse täiendavaid muudatusi. Lisateabe saamiseks vaadake [mõõtmed lisamine Microsoft Exceli malli](\dev-itpro\financial-dimensions\add-dimensions-excel-templates). Kui ettevõte on lisatud dimensioonid, on saadaval Excel disainer ja saab lisada malli.




