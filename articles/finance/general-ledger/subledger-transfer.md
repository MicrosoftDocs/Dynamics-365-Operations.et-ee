---
title: Alampearaamatu ülekandmine pearaamatusse
description: Selles teemas kirjeldatakse rakendusega Microsoft Dynamics 365 Finance seotud võimalusi alampearaamatu ülekandmiseks pearaamatusse.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1ae10f406148e213fd0272d1387f15606233be27
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000443"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Alampearaamatu ülekandmine pearaamatusse

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse rakenduse Microsoft Dynamics 365 Finance võimalusi, mis on seotud alampearaamatu töölehtede kirjete pakettide edastamise reeglitega.

Versioonis 8.1 tehti muudatusi, et lubada reeglite edastamine, mis võimaldas sünkroonsel valikul aeguda. Lisateavet vt teemast [Rakenduse Finance and Operations eemaldatud või aegunud funktsioonid](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).

Alampearaamatu partiide edastamiseks on saadaval järgmised valikud. 

 - Asünkroonne – see valik ajastab kohe alampearaamatu raamatupidamiskirjete edastamise pearaamatusse. Pearaamatu kanne salvestatakse kohe, kui ressursid on vabad seda taotlust serveris töötlema. 

- Plaanitud partii – see valik lisab alampearaamatu raamatupidamiskirjed, mis edastatakse pearaamatu töötlemise järjekorda, kus kandeid töödeldakse saabumise järjekorras. Pearaamatu kanne salvestatakse planeeritud ajal, kui ressursid on vabad seda pakett-tööd serveris töötlema. 
 
Versiooni 10.0.8 tehti parandusi asünkroonse valiku jõudluse suurendamiseks. See funktsioon on lubatud selle funktsiooni nimega **Alampearaamatu edastamine pearaamatu jõudluse optimeerimiseks**. 
 
See funktsioon parandab andmeedastust alampearaamatust pearaamatusse. See võimaldab protsessi tõhustada ja see rühmitab edastamiseks väiksemate kannete kogumid. See võimaldab pakktöötlusserveri tõhusamat kasutamist. Selle funktsiooni kasutamiseks peab pakktöötlusserver olema seadistatud, võrgus ja toimima, et asünkroonse edastamise valik töötaks. 
