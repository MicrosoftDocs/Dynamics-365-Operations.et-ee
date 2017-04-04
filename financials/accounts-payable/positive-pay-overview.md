---
title: "Positiivse makse ülevaade"
description: "See artikkel sisaldab teavet positiivse makse kohta, mida kasutatakse pangale edastatava elektroonilise tšekkide loendi loomiseks."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 1fd606817b06a05b9abaaedf20ea9872bd7edd5d
ms.openlocfilehash: cb4806a1f023c1e60311ff9d8facb4ef5717ad94
ms.lasthandoff: 03/31/2017


---

# <a name="positive-pay-overview"></a>Positiivse makse ülevaade

See artikkel sisaldab teavet positiivse makse kohta, mida kasutatakse pangale edastatava elektroonilise tšekkide loendi loomiseks. 

Positiivset makset kasutatakse pangale edastatava elektroonilise tšekkide loendi loomiseks. Positiivsete maksete failid aitavad pankadel tšekipettusi vältida. Saate seadistada positiivse makse elektroonilise tšekkide loendi koostamiseks iga kord, kui tšekke prinditakse. Tšeki esitamisel pangale võrdleb pank seda siis eelnevalt esitatud tšekkide loendiga. Kui tšekk vastab loendis olevale tšekile, maksab pank selle välja. Kui tšekk ei vasta ühelegi loendis olevale tšekile, võtab pank selle ülevaatamiseks enda kätte.

Positiivse makse teine nimetus on SafePay. 

Positiivse makse failides võib olla tundliku loomuga teavet maksesaajate ja tšekisummade kohta. Seetõttu kasutage kindlasti vajalikke turvameetmeid alates failide loomise hetkest kuni nende panka saabumiseni. Positiivsete maksete failid laaditakse alla veebibrauseri allalaadimisjuhiste kohaselt. 

Positiivse makse failid luuakse andmeüksuste abil. Enne positiivsete maksete faili koostamist tuleb seadistada XML-i jaoks teisendusvormingud, mis teisendavad andmed pangale sobivasse vormingusse. 

Iga pangakonto puhul, millele soovite positiivset makseteavet luua, tuleb määrata positiivse makse vorming. Pärast maksete loomist saate luua positiivse maksefaili üksikule juriidilisele isikule ja üksikule pangakontole. Teine võimalus on positiivsete maksete failide loomine juriidiliste isikute ja pangakontode jaoks üheaegselt. 

Kui positiivses maksefailis loetletud tšekid on tasutud, saate pangast kinnituskoodi. Seejärel saate kinnitada positiivne makse fail Microsoft Dynamics 365 toiminguteks. 

Kui peate positiivse makse faili muutma, saate selle tagasi kutsuda. Siis lähtestatakse igas positiivse makse failis oleva tšeki puhul väli, mis näitab, kas see tšekk on olnud positiivse makse faili lisatud.

Lisateabe saamiseks vaadake [seada üles ja luua positiivne tasu faile](set-up-generate-positive-pay-files.md).


