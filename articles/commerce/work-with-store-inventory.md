---
title: Kaupluse varude haldamine
description: Selles teemas kirjeldatakse dokumenditüüpe, mida saate kasutada varude haldamiseks.
author: rubencdelgado
manager: AnnBe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 3f7f228bbf312a2ccdc96d3e95287898bee01de4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022229"
---
# <a name="store-inventory-management"></a>Kaupluse varude haldamine

[!include [banner](includes/banner.md)]

Töötades varudega rakenduses Dynamics 365 Commerce ja kasutades kassarakendust, on oluline märkida, et kassa pakub piiratud tuge varude dimensioonidele ja teatud laokaubatüüpidele.

Kassalahendus ei toeta järgmiste kaupade konfiguratsioone.

- Kooslusekaubad (v.a komplekttooted, mis kasutavad koosluse raamistiku mõningaid komponente)
- Tegeliku kaaluga kaubad
- Partiiga juhitavad kaubad

Kassarakendus ei toeta praegu kassas järgmisi jälgimisdimensioone.

- Partii jälgimisdimensioon
- Omanikudimensioon

Kassalahendus pakub piiratud tuge järgmistele dimensioonidele. Piiratud tugi tähendab, et kassa võib lao/kaupluse seadistuse konfiguratsiooni põhjal mõne neist dimensioonidest varude kannetesse automaatselt vaikimisi määrata. Kassa ei toeta dimensioone täielikult samal viisil, nagu neid toetatakse müügikande käsitsi sisestamisel ERP-sse. 

- **Lao asukoht** – kasutajatel ei ole võimalik hallata vastuvõtva lao asukohta kaupade vastuvõtmisel kaupluse lattu, kui kauplus ei ole konfigureeritud kasutama laohalduse protsessi. Nende kaupade puhul kasutatakse kaupluse ladu vaikimisi määratletud vastuvõtva asukohana. Kui laohalduse protsess on kaupluses lubatud, siis käivitatakse piiratud tugi, mis palub kasutajal valida vastuvõttev asukoht kogu sissetuleku kohta. Poest müüdavaid kaupu müüakse alati kaupluse laoseadistuses vaikimisi määratletud asukohast. Tagastatava kauba lao asukoha haldamist saab kontrollida poe lao vaikimisi tagastatava asukoha definitsiooni alusel või tagastamise põhjusekoodide alusel, nagu on määratletud tagastamise asukoha poliitikas.
- **Litsentsiplaat** – litsentsiplaadid kohalduvad ainult siis, kui kauba ja kaupluselao puhul on lubatud suvand **Kasuta laohaldusprotsesse**. Kui Varud võetakse kaupluse lattu, kus laohalduse protsess on lubatud, ja kauba vastuvõtmiseks valitud asukoht on seotud asukoha profiiliga, mis nõuab litsentsiplaadi juhtimist, siis rakendus Kassa rakendab vastuvõtvale reale litsentsiplaati süstemaatiliselt. Kassa kasutajatel ei ole võimalust neid litsentsiplaadi andmeid muuta ega hallata. Kui on nõutav litsentsiplaadi täielik haldamine, soovitatakse kauplusel kasutada rakendusi WMS Mobile või ERP-i kontoriklienti nende kaupade vastuvõtmise haldamiseks.
- **Seerianumber** – rakendusel Kassa on piiratud tugi ühe seerianumbri jaoks, mis registreeritakse kande müügireal kassas loodud tellimuste alusel järjestatud kaupadele. Seda seerianumbrit ei kinnitata laos registreeritud seerianumbrite suhtes. Kui müügitellimus on loodud kõnekeskuse kanalis või on täidetud ERP-i kaudu ja mitu seerianumbrit on registreeritud ühel müügireal ERP-is täitmise protsessi käigus, siis neid seerianumbreid ei saa rakendada ega kinnitata, kui nende tellimuste puhul teostatakse kassas tagastust.
- **Lao olek** – kaupade puhul, mis kasutavad laohalduse protsessi ja nõuavad lao olekut, ei saa oleku välja määrata ega muuta rakenduse Kassa kaudu. Kaupluse lao konfiguratsioonis määratletud lao vaikimisi olekut kasutatakse kaupade lattu vastuvõtmisel.

> [!NOTE]
> Kõik organisatsioonid peavad kaubakonfiguratsioone kassa kaudu arendus- või katsekeskkonnas katsetama, enne kui need tootmisse juurutab. Katsetage oma kaupu, tehes nendega kassa kaudu regulaarseid sularahaga müügikandeid ja luues klienditellimusi (kohaldatavusel). Katsetamine peab hõlmama katsekeskkonnas täielikke väljavõtte sisestamise protsesse ja probleemide puudumise kontrollimist.
>
> Kaupade konfigureerimine viisil, mida kassarakendus ei toeta, ilma nõuetekohase katsetamiseta, võib põhjustada teie väljavõtete sisestamise protsessi nurjumist tootmises ilma probleemide hõlpsa lahendamise võimaluseta. Nende sisestusprotsesside õnnestumise võimaldamiseks võib kaaluda rakendusele partneri või kliendi kohanduste lubamist. Kui kohandused pole vajalikud, peab organisatsioon veenduma, et toodete tootekonfiguratsioon on tehtud viisil, mida toetab standardne kassarakenduse / tellimuse loomise / väljavõtte sisestamise protsess.

## <a name="purchase-orders"></a>Ostutellimused

Ostutellimused koostatakse peakontoris. Kui ostutellimuse päisesse on kaasatud ladu, saab tellimust vastu võtta kaupluses, kasutades Modern POS-i (MPOS) või pilvekassat toimingu **Komplekteerimine ja vastuvõtmine** kaudu. Pärast seda, kui laos vastuvõetud kogused sisestatakse ostutellimuse dokumendi jaoks kassas väljale **Saa kohe**, saab neid salvestada kohalikult või kooskõlastatult. Selle teabe salvestamisel kohalikult eil ole mõju laovarule. Salvestamine peaks toimuma ainult juhul, kui kasutaja ei ole valmis sissetulekut sisestama HQ-sse ja vajab lihtsalt võimalust eelnevalt sisestatud andmed **Saa kohe** ajutiselt talletada. See salvestab nüüd andmed kohalikult kasutaja kanali andmebaasi. Pärast dokumendi töötlemist, kasutades suvandit **Kinnita**,saadetakse andmed **Saa kohe** HQ-sse ja ostutellimuse sissetulek sisestatakse. 

## <a name="transfer-orders"></a>Üleviimistellimused

Üleviimistellimusega saab määrata, et kindel kauplus on asukoht, kust kaupu saab lähetada või kuhu võetakse varusid vastu. Kui kassa kasutaja on üleviimistellimust lähetav ladu, saavad nad sisestada koguse **Läheta kohe** otse kassast. Lähetava kaupluse sisestatud andmeid saab salvestada kohalikult või kooskõlastatud. Kohalikult salvestamisel ei tehta üleviimistellimuse dokumendile HQ-s ühtegi värskendust. Salvestamine peaks toimuma ainult juhul, kui kasutaja ei ole valmis saadetist sisestama HQ-sse ja vajab lihtsalt võimalust eelnevalt sisestatud andmed **Läheta kohe** ajutiselt talletada. Kui kauplus on saadetise kinnitamiseks valmis, tuleb valida suvand **Kinnita**. See sisestab üleviimistellimuse saadetise HQ-sse, et vastuvõttev ladu saaks selle nüüd vastu vastu võtta. 

Kui kassa kasutaja on üleviimistellimust vastuvõttev ladu, saavad nad sisestada koguse **Saa kohe** otse kassast. Vastuvõtva kaupluse sisestatud andmeid saab salvestada kohalikult või kooskõlastatud. Salvestamine peaks toimuma ainult juhul, kui kasutaja ei ole valmis sissetulekut sisestama HQ-sse ja vajab võimalust eelnevalt sisestatud andmed **Saa kohe** ajutiselt talletada. See salvestab nüüd andmed kohalikult kasutaja kanali andmebaasi. Pärast dokumendi töötlemist, kasutades suvandit **Kinnita**, saadetakse andmed **Saa kohe** HQ-sse ja üleviimistellimuse sissetulek sisestatakse. On oluline, et vastuvõttev kauplus saab ainult kinnitada vastuvõetavaid kogused, mis on saadetud kogustega võrdsed või sellest väiksemad. Katse võtta vastu koguseid üleviimistellimusega, mida pole eelnevalt saadetud, põhjustab tõrkeid ja sissetulekut ei kinnitata HQ-s.

## <a name="stock-counts"></a>Laoinventuurid

Laoinventuurid võivad olla plaanipärased või plaanivälised. Plaanitud laoinventuurid algatab peakontor, mis määrab ka loendatavad kaubad. Peakontor loob inventuuridokumendi, mida saab vastu võtta kaupluses, kus vaba laovaru kogused sisestatakse MPOS-is või pilve POS-is. Plaanimata laoinventuurid käivitatakse kaupluses ja vaba laoseisu koguseid värskendatakse MPOS-is või pilve POS-is. Erinevalt ajastatud laoinventuuridest puudub plaanimata laovarudel eelmääratletud kaupade loend. Mõlemat tüüpi laoinventuuri lõpetamisel see kooskõlastatakse ja saadetakse peakontorisse. Peakontoris inventuur kinnitatakse ja sisestatakse eraldi etapina.

## <a name="inventory-lookup"></a>Otsing varudest

Jooksvat vaba tootekogust mitme kaupluse ja lao kohta saab vaadata lehelt **Otsing varudest**. Lisaks jooksvale vabale kaubavarule saab tulevasi lubamiseks saadaval (ATP) koguseid vaadata iga eraldi kaupluse kohta. Selleks valige kauplus, mille ATP-d soovite vaadata, ja seejärel klõpsake valikut **Kaupluse saadavuse kuvamine**.
