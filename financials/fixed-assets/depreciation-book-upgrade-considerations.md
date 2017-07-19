---
title: "Kulumiraamatu täiendamise ülevaade"
description: "Varasemates väljalasetes on põhivarade jaoks kaks hindamiskontseptsiooni: väärtusmudelid ja kulumiraamatud. Rakenduses Microsoft Dynamics 365 for Operations (1611) on väärtusmudeli ja kulumiraamatu funktsioonid ühendatud üheks kontseptsiooniks, mis on tuntud kui raamat. Selles teemas antakse mõned asjad, mida täiendamisel arvestada."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 116f9e8fbf8ed6ecbd2a1163f17e52ba80061694
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="depreciation-book-upgrade-overview"></a>Kulumiraamatu täiendamise ülevaade

[!include[banner](../includes/banner.md)]


Varasemates väljalasetes on põhivarade jaoks kaks hindamiskontseptsiooni: väärtusmudelid ja kulumiraamatud. Rakenduses Microsoft Dynamics 365 for Operations (1611) on väärtusmudeli ja kulumiraamatu funktsioonid ühendatud üheks kontseptsiooniks, mis on tuntud kui raamat. Selles teemas antakse mõned asjad, mida täiendamisel arvestada. 

Täiendusprotsess liigutab teie olemasoleva seadistuse ja kõik olemasolevad kanded uude raamatu struktuuri. Väärtusmudelid jäävad selliseks, nagu need praegu on ehk raamatuks, mis sisestab pearaamatusse. Kulumiraamatud liigutatakse raamatusse, millel on valik **Pearaamatusse sisestamine** määratud sättele **Ei**. Kulumiraamatu töölehe nimed liigutatakse pearaamatu töölehele, mille nimel on sisestamiskiht määratud sättele **Pole**. Kulumiraamatu kanded teisaldatakse jaotisse Põhivara kanded. 

Enne andmete täiendamise käivitamist peate mõistma kahte suvandit, mis on saadaval kulumiraamatu tööleheridade täiendamiseks kanneteks, ja numbriseeriat, mida kasutatakse kande seeria jaoks. 

Suvand 1:  **Süsteemi määratletud numbriseeria** – see on vaikesuvand täiendamise jõudluse optimeerimiseks. Täiendamine ei kasutada numbriseeriate raamistikku, vaid eraldab selleasemel kanded kogumipõhise lähenemisega. Pärast täiendamist luuakse uus numbriseeria, mille parameeter **Järgmine numbrikomplekt** põhineb asjakohaselt täiendatud kandel. Vaikimisi on kasutatava numbriseeria vorming FADBUpgr\#\#\#\#\#\#\#\#\#. Seda lähenemist kasutades saate vormingut korrigeerida järgmiste parameetrite abil.

-   **Numbriseeria kood** – kood numbriseeria tuvastamiseks. Seda numbriseeria koodi ei saa eksisteerida, kuna see luuakse täiendamisega.
    -   Püsinimi: **NumberSequenceDefaultCode**
    -   Vaikeväärtus: "FADBUpgr"
-   **Eesliide** – püsistringi väärtus, mida kasutatakse kande numbrite jaoks eesliitena.
    -   Püsinimi: **NumberSequenceDefaultParameterPrefix**
    -   Vaikeväärtus: "FADBUpgr"
-   **Tähtnumbriline pikkus** – numbriseeria tähtnumbrilise segmendi pikkus.
    -   Püsinimi: **NumberSequenceDefaultParameterAlpanumericLength **
    -   Vaikeväärtus: 9
-   **Algusnumber** – esimene numbriseerias kasutatav number.
    -   Püsinimi: **NumberSequenceDefaultParameterStartNumber  **
    -   Vaikeväärtus: 1

2. valik: **Olemasolev kasutaja määratletud numbriseeria** – see valik võimaldab määratleda täiendamiseks kasutatava numbriseeria. Kaaluge selle valiku kasutamist, kui vajate täpsemat numbriseeria konfigureerimist. Numbriseeria kasutamiseks peate muutma täiendusklassi ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans järgmise teabega.

-   **Numbriseeria kood** – numbriseeria kood.
    -   Püsinimi: **NumberSequenceExistingCode **
    -   Vaikeväärtus: vaikesäte puudub, seda tuleb värskendada numbriseeria koodi järgi.
-   **Ühiskasutuses numbriseeria** – kahendmuutuja väärtus, et tuvastada numbriseeria ulatus. Kasutage kõigis ettevõtetes ühiskasutuses numbriseeriate jaoks „tõene” ja ettevõttespetsiifilise ulatuse jaoks „väär”. Väärtuse „väär” kasutamisel peab määratud nimega numbriseeria eksisteerima igas ettevõttes, mis sisaldab kulumiraamatu kandeid. Ühiskasutatud numbriseeriad eksisteerivad igas sektsioonis, mis sisaldab kulumiraamatu kandeid.
    -   Püsinimi: **NumberSequenceExistingIsShared **
    -   Vaikeväärtus: tõene

Parameetrid asuvad klassi ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans alguses. 

*// Määrake kannete eraldamise eelistatav lähenemisviis* 
*// tõene, kui soovite kasutada olemasoleva numbriseeria koodi* 
*// väär, kui soovite kasutada süsteemi määratletud numbriseeriat (vaikimisi)* const boolean NumberSequenceUseExistingCode = väär;  

*// Süsteemi määratletud numbriseeria lähenemisviisi kasutamisel määrake numbriseeria parameetrid.*
*// Nende parameetritega luuakse uus numbriseeria.* const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*// Olemasoleva numbriseeria lähenemisviisi kasutamisel määrake olemasoleva numbriseeria kood.* 
*// Kande eraldamine läheb olemasoleva numbriseeria puhul rea haaval.* const str NumberSequenceExistingCode = ''; *// Määrake olemasoleva numbriseeria koodi ulatus* 
*// tõene, kui määratud numbriseeria on ühiskasutuses* 
*// väär, kui määratud numbriseeria on ettevõtte kohta* 
*// Vaikimisi süsteemi määratletud numbriseeriat kasutatakse, kui määratud ulatusega numbriseeria koodi ei leita.* const boolean NumberSequenceExistingIsShared = true; 

Ehitage uuesti projekt, mis sialdab klassi, kui konstandid on modifitseeritud. 

Süsteemi loodud numbriseeria lähenemise (1. valik) kasutamisel kasutab täiendamine kogumipõhist töötlemist, et eraldada kande numbrid, nagu on määratud täiendamisskripti parameetrites. See loob pärast eraldamist ka määratud parameetritega uue numbriseeria. 

Kasutaja määratletud olemasoleva numbriseeria lähenemise (suvand 2) kasutamisel kontrollib täiendus, kas määratud ulatusega numbriseeria on andmebaasis olemas iga kulumiraamatu kannetega sektsiooni ja ettevõtte jaoks. See on olemas, kasutab täiendus rea haaval töötlemist, et eraldada kandenumbrid, nagu on määratud numbriseeriaga, mis kasutab numbriseeria raamistikku. Kui määratud ulatusega numbriseeriat ei ole, kasutab täiendus kandenumbrite eraldamiseks süsteemi määratletud numbriseeria vaike-lähenemisviisi ja loob pärast eraldamist määratud vaikeparameetritega uue numbriseeria.

Mõlema lähenemisega kasutab andmete täiendamisskript ka numbriseeriat uue pearaamatu töölehe nimedel oleva välja **Voucher series** jaoks, mis on loodud endiste kulumiraamatu töölehenimede jaoks.




