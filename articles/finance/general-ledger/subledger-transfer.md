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
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: de9328f69938151c5558d41263d36b873d117e4b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975479"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Alampearaamatu ülekandmine pearaamatusse

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse rakenduse Microsoft Dynamics 365 Finance võimalusi, mis on seotud alampearaamatu töölehtede kirjete pakettide edastamise reeglitega.

Versioonis 8.1 tehti muudatusi, et lubada reeglite edastamine, mis võimaldas **Sünkroonsel** valikul iganeda. Lisateavet vt teemast [Rakenduse Finance and Operations eemaldatud või aegunud funktsioonid](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).

Alampearaamatu partiide edastamiseks on saadaval järgmised valikud. 

 - Asünkroonne – see valik ajastab kohe alampearaamatu raamatupidamiskirjete edastamise pearaamatusse. Pearaamatu kanne salvestatakse kohe, kui ressursid on vabad seda taotlust serveris töötlema. 

- Plaanitud partii – see valik lisab alampearaamatu raamatupidamiskirjed, mis edastatakse pearaamatu töötlemise järjekorda, kus kandeid töödeldakse saabumise järjekorras. Pearaamatu kanne salvestatakse planeeritud ajal, kui ressursid on vabad seda pakett-tööd serveris töötlema. 
 
Versioonil 10.0.8 tehti parandusi asünkroonse valiku jõudluse suurendamiseks. See funktsioon on lubatud selle funktsiooni nimega **Alampearaamatu edastamine pearaamatu jõudluse optimeerimiseks**. 
 
See funktsioon parandab andmeedastust alampearaamatust pearaamatusse. See võimaldab protsessi tõhustada ja see rühmitab edastamiseks väiksemate kannete kogumid. See võimaldab pakktöötlusserveri tõhusamat kasutamist. Selle funktsiooni kasutamiseks peab pakktöötlusserver olema seadistatud, võrgus ja toimima, et asünkroonse edastamise valik töötaks. 
