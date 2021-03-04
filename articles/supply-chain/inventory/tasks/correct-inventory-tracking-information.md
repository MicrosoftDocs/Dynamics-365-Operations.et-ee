---
title: Varude jälgimisteabe korrigeerimine
description: See protseduur juhib teid läbi varude üleviimistöölehe koostamise ja sisestamise protsessi, et parandada varude jälgimise teavet.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8a488d4c30923445b3ebc2626a79b8fa45012c7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426526"
---
# <a name="correct-inventory-tracking-information"></a>Varude jälgimisteabe korrigeerimine

[!include [banner](../../includes/banner.md)]

See protseduur juhib teid läbi varude üleviimistöölehe koostamise ja sisestamise protsessi, et parandada varude jälgimise teavet. Selles näites muudame partiiga kontrollitava kauba teavet, muutes valesti registreeritud partii teiseks partiiks. Saate selle protseduuriga tutvuda demoettevõtte USPI või oma andmeid kasutades. Kui kasutate oma andmeid, peab teil olema lubatud partiiga kaup ja see ei tohi olla asukoha järgi kontrollitav. Samuti peate seadistama varude üleviimiste jaoks varude töölehe nime. Neid ülesandeid täidab üldjuhul laotöötaja.


## <a name="create-an-inventory-transfer-journal"></a>Lao üleviimistöölehe loomine
1. Minge jaotisse Ülekanne.
2. Klõpsake valikut Uus.
3. Sisestage või valige väärtus väljal Nimi.
4. Klõpsake nuppu OK.

## <a name="create-journal-lines"></a>Tööleheridade loomine
1. Klõpsake valikut Uus.
2. Sisestage või valige väärtus väljal Kaubakood.
    * Kui kasutate USPI-d, võite valida üksuse M5003.  
3. Sisestage arv väljale Kogus.
4. Klõpsake vahekaarti Varude dimensioonid.
5. Sisestage või valige väärtus väljal Partii number.
6. Sisestage või valige väärtus väljal Koht.
7. Sisestage või valige väärtus väljal Ladu.
8. Sisestage või valige väärtus väljal Partii number.

## <a name="post-the-journal"></a>Töölehe sisestamine
1. Klõpsake valikut Sisesta.
2. Klõpsake nuppu OK.

## <a name="check-tracing-information"></a>Jälgimisteabe vaatamine
1. Klõpsake Ladu.
2. Klõpsake käsku Jälgi.
3. Klõpsake nuppu OK.
    * Selle jälgimisteabe kasutamisel saate välja selgitada, millisest partiist varusid parandasite.  Võite kasutada selle teabe vaatamiseks ka kauba jälgimise lehte.  
4. Sulgege leht.

## <a name="check-inventory-transactions"></a>Laokannete kontrollimine
1. Klõpsake Ladu.
2. Klõpsake suvandit Kanded.
    * Siin näete kandeid, mis loodi, kui oma töölehe sisestasite.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]