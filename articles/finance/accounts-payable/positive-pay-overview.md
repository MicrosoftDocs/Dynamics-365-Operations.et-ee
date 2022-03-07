---
title: Positiivse makse ülevaade
description: See artikkel sisaldab teavet positiivse makse kohta, mida kasutatakse pangale edastatava elektroonilise tšekkide loendi loomiseks.
author: panolte
ms.date: 08/22/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "88463"
- intro-internal
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 5f36230b68986cffc985353a7130ba429dabd10e
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7984048"
---
# <a name="positive-pay-overview"></a>Positiivse makse ülevaade

[!include [banner](../includes/banner.md)]

See artikkel sisaldab teavet positiivse makse kohta, mida kasutatakse pangale edastatava elektroonilise tšekkide loendi loomiseks. 

Positiivset makset kasutatakse pangale edastatava elektroonilise tšekkide loendi loomiseks. Positiivsete maksete failid aitavad pankadel tšekipettusi vältida. Saate seadistada positiivse makse elektroonilise tšekkide loendi koostamiseks iga kord, kui tšekke prinditakse. Tšeki esitamisel pangale võrdleb pank seda siis eelnevalt esitatud tšekkide loendiga. Kui tšekk vastab loendis olevale tšekile, maksab pank selle välja. Kui tšekk ei vasta ühelegi loendis olevale tšekile, võtab pank selle ülevaatamiseks enda kätte.

Positiivse makse teine nimetus on SafePay. 

Positiivse makse failides võib olla tundliku loomuga teavet maksesaajate ja tšekisummade kohta. Seetõttu kasutage kindlasti vajalikke turvameetmeid alates failide loomise hetkest kuni nende panka saabumiseni. Positiivsete maksete failid laaditakse alla veebibrauseri allalaadimisjuhiste kohaselt. 

Positiivse makse failid luuakse andmeüksuste abil. Enne positiivsete maksete faili koostamist tuleb seadistada XML-i jaoks teisendusvormingud, mis teisendavad andmed pangale sobivasse vormingusse. 

Iga pangakonto puhul, millele soovite positiivset makseteavet luua, tuleb määrata positiivse makse vorming. Pärast maksete loomist saate luua positiivse maksefaili üksikule juriidilisele isikule ja üksikule pangakontole. Teine võimalus on positiivsete maksete failide loomine juriidiliste isikute ja pangakontode jaoks üheaegselt. 

Kui positiivses maksefailis loetletud tšekid on tasutud, saate pangast kinnituskoodi. Seejärel saate süsteemis kinnitada positiivse maksefaili. 

Kui peate positiivse makse faili muutma, saate selle tagasi kutsuda. Siis lähtestatakse igas positiivse makse failis oleva tšeki puhul väli, mis näitab, kas see tšekk on olnud positiivse makse faili lisatud.

Lisateavet vt jaotisest [Positiivse makse failide seadistamine ja loomine](set-up-generate-positive-pay-files.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]