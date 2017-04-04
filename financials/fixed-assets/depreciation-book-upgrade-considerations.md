---
title: "Põhivara uuendamise kokkuvõtte lisaleht"
description: "Varasemates väljaannetes oli kahe hindamise mõiste põhivarade - väärtusmudelid ja kulumiraamatud. Rakenduse Microsoft Dynamics 365 for Operations versioonis 1611 on väärtusmudeli ja kulumiraamatu funktsioonid ühendatud üheks kontseptsiooniks, mis on tuntud kui raamat. Selles teemas antakse mõned asjad, mida täiendamisel arvestada."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: d29cb7bc5acc29be93332b4211adebc4486a7a25
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-book-upgrade-overview"></a>Põhivara uuendamise kokkuvõtte lisaleht

Varasemates väljaannetes oli kahe hindamise mõiste põhivarade - väärtusmudelid ja kulumiraamatud. Rakenduse Microsoft Dynamics 365 for Operations versioonis 1611 on väärtusmudeli ja kulumiraamatu funktsioonid ühendatud üheks kontseptsiooniks, mis on tuntud kui raamat. Selles teemas antakse mõned asjad, mida täiendamisel arvestada. 

Täiendusprotsess liigutab teie olemasoleva seadistuse ja kõik olemasolevad kanded uude raamatu struktuuri. Väärtusmudelid jäävad selliseks, nagu need praegu on ehk raamatuks, mis sisestab pearaamatusse. Kulumiraamatud liigutatakse raamatusse, millel on valik **Pearaamatusse sisestamine** määratud sättele **Ei**. Kulumiraamatu töölehenimede üle Pearaamatu töölehe nimi sisestuskiht seatud **pole**. Kulumiraamatukannete teisaldatakse teostada. 

Enne andmete täiendamise käivitamist peate mõistma kahte suvandit, mis on saadaval kulumiraamatu tööleheridade täiendamiseks kanneteks, ja numbriseeriat, mida kasutatakse kande seeria jaoks. 

Suvand 1:  **Süsteemi määratletud numbriseeria** – see on vaikesuvand täiendamise jõudluse optimeerimiseks. Täiendamine ei kasutada numbriseeriate raamistikku, vaid eraldab selleasemel kanded kogumipõhise lähenemisega. Pärast versiooniuuendust, luuakse uus numbriseeria kirjelduse ning **järgmise määra** nõuetekohaselt täiendatud tehingute põhjal. Vaikimisi kasutatav numbriseeria on selle FADBUpgr\#\#\#\#\#\#\#\#\# formaadis. Mõned parameetrid on saadaval vormi muuta, kasutades seda lähenemisviisi:

-   **Dokumendinumber numbriseeria koodi** – tuvastamiseks numbriseeria tähis. Selle numbriseeria koodi ei saa eksisteerida sest see loovad täiendamist.
    -   Püsinimi: **NumberSequenceDefaultCode**
    -   Vaikeväärtus: "FADBUpgr"
-   **Eesliide** – püsistringi väärtus, mida kasutatakse kande numbrite jaoks eesliitena.
    -   Püsinimi: **NumberSequenceDefaultParameterPrefix**
    -   Vaikeväärtus: "FADBUpgr"
-   **Tähtnumbriline pikkus** – numbriseeria tähtnumbrilise segmendi pikkus.
    -   Püsiv: ** NumberSequenceDefaultParameterAlpanumericLength **
    -   Vaikeväärtus: 9
-   **Algusnumber** – esimene numbriseerias kasutatav number.
    -   Püsiv: ** NumberSequenceDefaultParameterStartNumber **
    -   Vaikeväärtus: 1

Variant 2: **olemasolev kasutaja määratletud numbriseeria** -see valik võimaldab teil määrata soovite seda täiendust kasutada. Võite kasutada seda võimalust, kui vajate arenenud numbrite jada konfiguratsiooni. Numbriseeria kasutamiseks peate muutma uuendamise klassi ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans järgmised andmed:

-   **Numbriseeria kood** – numbriseeria kood.
    -   Püsiv: ** NumberSequenceExistingCode **
    -   Vaikeväärtus: vaikesäte puudub, seda tuleb värskendada numbriseeria koodi järgi.
-   **Ühiskasutuses numbriseeria** – kahendmuutuja väärtus, et tuvastada numbriseeria ulatus. Kasutage kõigis ettevõtetes ühiskasutuses numbriseeriate jaoks „tõene” ja ettevõttespetsiifilise ulatuse jaoks „väär”. Kasutades "vale", kuuluma iga ettevõte, mis sisaldab kulumiraamatu kannete numbriseeria nimi. Jagatud Numbriseeriad olemas kulumiraamatukannete iga sektsiooni.
    -   Püsiv: ** NumberSequenceExistingIsShared **
    -   Vaikeväärtus: tõene

Parameetrid on alguses on ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans klassi. 

*Saate määrata kannete jaotamise parem lähenemine*<ph id="t1">
</ph>*/ / tõene, kui soovite kasutada mõne olemasoleva numbriseeria koodi*<ph id="t2">
</ph>*/ / vale, kui kasutate süsteemi määratletud numbriseeria (vaikimisi)* konstant Boole'i NumberSequenceUseExistingCode = false;  

*Kui süsteemi määratletud numbrite jada lähenemine, määrata parameetrid numbriseeria. *<ph id="t3">
</ph>*/ / Uus numbriseeria on loodud nende parameetritega.* Const str NumberSequenceDefaultCode = "FADBUpgr"; const str NumberSequenceDefaultParameterPrefix = "FADBUpgr"; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*Vana number jada meetodi kasutamisel saate määrata olemasoleva numbriseeria koodi. *<ph id="t4">
</ph>*/ / Kande eraldamise läheb ridahaaval olemasolevate numbriseeriatele.* Const str NumberSequenceExistingCode = ''; */ / Ulatuse, olemasolevate numbriseeria koodi*<ph id="t5">
</ph>*/ / tõene, kui määratud numbriseeria jagatakse*<ph id="t6">
</ph>*/ / valede, kui määratud numbriseeria on iga ettevõtte*<ph id="t7">
</ph>*/ / vaikimisi süsteemi määratletud numbriseeria kasutatakse kui numbriseeria kood koos määratud ulatust ei leitud.* const boolean NumberSequenceExistingIsShared = true; 

Ehitage uuesti projekt, mis sialdab klassi, kui konstandid on modifitseeritud. 

Süsteemi genereeritud number jada lähenemine (variant 1) kasutamisel kasutab täiendamist komplekt töötlemine kandenumbrite uuendamise skripti parameetrid määratletud eraldada. See loob ka uue numbriseeria määratud parameetritega pärast. 

Kasutaja määratletud olemasoleva numbriseeria lähenemise (suvand 2) kasutamisel kontrollib täiendus, kas määratud ulatusega numbriseeria on andmebaasis olemas iga kulumiraamatu kannetega sektsiooni ja ettevõtte jaoks. Kui see olemas, kasutab täiendamist-ridahaaval töötlemise kandenumbrite nagu määratud numbriseeria numbrite jada raamistiku abil eraldada. Kui numbriseeriat pole määratud ulatust, täiendamist kasutab vaikimisi süsteemi määratletud numbrite jada lähenemine kandenumbrite eraldada ja luua uue numbriseeria määratud vaikimisi parameetritega pärast.

Mõlema lähenemisega kasutab andmete täiendamisskript ka numbriseeriat uue pearaamatu töölehe nimedel oleva välja **Voucher series** jaoks, mis on loodud endiste kulumiraamatu töölehenimede jaoks.


