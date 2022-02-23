---
title: Kliendimaksete ülevaade
description: Sellest tegevusejuhisest leiate ülevaate klindimaksete sisestamiseks kasutatavate eri meetodite kohta.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9196bedcea26a0024b3eabbbcb9c58a0155a7490
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442350"
---
# <a name="customer-payment-overview"></a>Kliendimaksete ülevaade

[!include [banner](../../includes/banner.md)]

Sellest tegevusejuhisest leiate ülevaate klindimaksete sisestamiseks kasutatavate eri meetodite kohta. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Maksed > Maksete töölehed**.
2. Klõpsake valikut **Uus**.
3. Valige maksetööleht, millele kliendi maksed salvestatakse.
4. Valige tööleht või sisestage see käsitsi.
5. **Toimingupaanil** klõpsake **Kliendi maksete sisestamine**. Valikut Sisesta kliendimaksed kasutatakse ühe kliendimakse kirjendamiseks korraga. Makseteabe sisestate lehe ülaossa ja seejärel saate sama lehe kaudu märkida kõik maksega tasutud arved.  
6. Sisestage klient, kellelt makse saite. Kui te ei tea klienti, kuid teate makstud kannet, saate makse sisestamiseks kasutada välja Kanne. Sisestage või valige arve väljal Kanne. Klient tuuakse pärast kande valimist vaikimisi automaatselt.
7. Sisestage makseviide väljale **Makseviide**. Makseviide võib olla kliendi tšekinumber või kliendi elektroonilise makse viide. Makseviide on vajalik vaid juhul, kui märgite makse kaasamise deposiidikviitungile.  
8. Valige väljal **Deposiitkviitung**, kas makse kaasatakse deposiitkviitungile. 
9. Sisestage kliendi maksesumma väljale **Kreedit**. Maksesummat ei tooda vaikimisi. See tuleb käsitsi sisestada. 
10. Märkige kliendi makstud arved. Kui makse on ettemaks, ei pea te tasakaalustamiseks märkima ühtegi arvet. Makse saab siiski salvestada ja sisestada. Arve tasakaalustamine võib toimuda hiljem.
11. Sisestage maksesumma, mis tuleks märgitud arvel tasakaalustada. Seda välja saab kasutada, kui makse on osamakseks. Kui te summat ei sisesta, määratakse tasakaalustatav summa automaatselt teie eest.
12. Klõpsake käsku **Salvesta töölehel**. Enne makse töölehele salvestamist veenduge, et vastaskonto oleks määratletud. Käsuga **Salvesta töölehel** salvestatakse makse ja teisaldatakse see töölehele. Seejärel saate jätkata järgmise makse sisestamist.
13. Sulgege leht.
14. Klõpsake paanil **Toimingupaan** suvandit Read. Ridade avamisel näete kõiki lehele **Kliendimaksete sisestamine** ja töölehele salvestatud makseid. Saate seda lehte kasutada ka uute kliendimaksete sisestamiseks või enne sisestamist olemasoleva kliendimakse redigeerimiseks.
15. Teise makse loomiseks klõpsake nuppu **Uus**. 
16. Valige klient, kellelt makse saite. Kui te klienti ei tea, kuid teate maksega tasutud arvet, kasutage arve käsitsi sisestamiseks või valimiseks välja Arve. Klient tuuakse vaikimisi pärast arve valimist.  
17. Klõpsake tasutud arvete märkimiseks **Kannete tasakaalustamine**. Te ei pea makset mis tahes arvetel tasakaalustama. Kui tegemist on ettemaksuga või kui te ei tea, milline arve on tasutud, saate makse sisestada. Makse saab arvel tasakaalustada hiljem.  
18. Märkige maksega tasutud arved. 
19. Väljale **Summa** sisestage maksesumma, mis arvel tasakaalustatakse.
20. Klõpsake valikut **OK**.
21. Sisestage makseviide väljale **Makseviide**. Makseviide on vajalik vaid juhul, kui märgite makse kaasamise deposiidikviitungile.  
22. Kliendi maksete sisestamiseks klõpsake **Toimingupaanil** valikut **Sisesta**. 

