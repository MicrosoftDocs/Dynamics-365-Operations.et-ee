---
title: Kaupluse varude haldamine
description: Selles teemas kirjeldatakse dokumenditüüpe, mida saate kasutada varude haldamiseks.
author: rubencdelgado
manager: AnnBe
ms.date: 01/18/2019
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
ms.openlocfilehash: 02f8afbe3bb6f94c66a8b5aa02531c219adc3963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "339230"
---
# <a name="store-inventory-management"></a>Kaupluse varude haldamine

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse dokumenditüüpe, mida saate kasutada varude haldamiseks.

Organisatsiooni varude haldamiseks saab kasutada järgmist tüüpi dokumente.

Töötades varudega rakenduses Dynamics 365 for Retail ja kasutades kassarakendust, on oluline märkida, et kassa pakub piiratud tuge varude dimensioonidele ja teatud laokaubatüüpidele.  

Kassalahendus ei toeta järgmiste kaupade konfiguratsioone.
- Kooslusekaubad (v.a komplekttooted, mis kasutavad koosluse raamistiku mõningaid komponente)
- Tegeliku kaaluga kaubad
- Partiiga juhitavad kaubad

Kassarakendus ei toeta praegu kassas järgmisi jälgimisdimensioone.
- Partii jälgimisdimensioon
- Omanikudimensioon

Kassalahendus pakub piiratud tuge järgmistele dimensioonidele. Piiratud tugi tähendab, et kassa võib lao/kaupluse seadistuse konfiguratsiooni põhjal mõne neist dimensioonidest varude kannetesse automaatselt vaikimisi määrata. Kassa ei toeta dimensioone täielikult samal viisil, nagu neid toetatakse müügikande käsitsi sisestamisel ERP-sse. 

- Koht
- Litsentsiplaat (kohaldub ainult siis, kui kauba ja kaupluselao puhul on lubatud suvand **Kasuta laohaldusprotsesse**)
- Seerianumber
- Lao olek

> [!NOTE]
> Kõik organisatsioonid peavad kaubakonfiguratsioone kassa kaudu arendus- või katsekeskkonnas katsetama, enne kui need tootmisse juurutab. Katsetage oma kaupu, tehes nendega kassa kaudu regulaarseid sularahaga müügikandeid ja luues klienditellimusi (kohaldatavusel). Katsetamine peab hõlmama katsekeskkonnas täielikke väljavõtte sisestamise protsesse ja probleemide puudumise kontrollimist.
> Kaupade konfigureerimine viisil, mida kassarakendus ei toeta, ilma nõuetekohase katsetamiseta, võib põhjustada teie väljavõtete sisestamise protsessi nurjumist tootmises ilma probleemide hõlpsa lahendamise võimaluseta. Nende sisestusprotsesside õnnestumise võimaldamiseks võib kaaluda rakendusele partneri või kliendi kohanduste lubamist. Kui kohandused pole vajalikud, peab organisatsioon veenduma, et toodete tootekonfiguratsioon on tehtud viisil, mida toetab standardne kassarakenduse / tellimuse loomise / väljavõtte sisestamise protsess.

## <a name="purchase-orders"></a>Ostutellimused

Ostutellimused koostatakse peakontoris. Kui ostutellimuse päisesse on kaasatud jaemüügiladu, saab tellimust vastu võtta kaupluses, kasutades rakenduses Microsoft Dynamics 365 for Retail Modern POS-i (MPOS) või pilvekassat. Pärast kaupluses vastuvõetud koguste sisestamist saab need kohalikult täiendavaks modifitseerimiseks salvestada. Teise võimalusena saab kogused kooskõlastada ja saata peakontorisse. Peakontoris kuvatakse kaupluses vastuvõetud kogused Dynamics 365 for Retailis ostutellimuse väljal **Kohe tarnitav**.

## <a name="transfer-orders"></a>Üleviimistellimused

Üleviimistellimuses saab määrata, et konkreetne kauplus on koht, kust kaupu saab teele panna. Sellisel juhul kuvatakse üleviimistellimus kaupluses MPOS-is või pilve POS-is komplekteerimistaotlusena. Pärast taotletud koguste komplekteerimist need kooskõlastatakse ja saadetakse peakontorisse. Peakontoris kuvatakse kaupluses komplekteeritud kogused Dynamics 365 for Retailis üleviimistellimuse väljal **Kohe saadetav**. Üleviimistellimuses saab määrata, et konkreetne kauplus on koht, kuhu kaupu saab saata. Sellisel juhul kuvatakse üleviimistellimus kaupluses MPOS-is või pilve POS-is vastuvõtmistaotlusena. Pärast kaupluses vastuvõetud koguste sisestamist saab need kohalikult täiendavaks modifitseerimiseks salvestada. Teise võimalusena saab kogused kooskõlastada ja saata peakontorisse. Peakontoris kuvatakse kaupluses vastuvõetud kogused Dynamics 365 for Retailis üleviimistellimuse väljal **Kohe tarnitav**.

## <a name="stock-counts"></a>Laoinventuurid

Laoinventuurid võivad olla plaanipärased või plaanivälised. Plaanitud laoinventuurid algatab peakontor, mis määrab ka loendatavad kaubad. Peakontor loob inventuuridokumendi, mida saab vastu võtta kaupluses, kus vaba laovaru kogused sisestatakse MPOS-is või pilve POS-is. Plaanimata laoinventuurid käivitatakse kaupluses ja vaba laoseisu koguseid värskendatakse MPOS-is või pilve POS-is. Erinevalt ajastatud laoinventuuridest puudub plaanimata laovarudel eelmääratletud kaupade loend. Mõlemat tüüpi laoinventuuri lõpetamisel see kooskõlastatakse ja saadetakse peakontorisse. Peakontoris inventuur kinnitatakse ja sisestatakse.

## <a name="inventory-lookup"></a>Otsing varudest

Jooksvat vaba tootekogust mitme kaupluse ja lao kohta saab vaadata varude otsingulehelt. Lisaks jooksvale vabale kaubavarule saab tulevasi lubamiseks saadaval (ATP) koguseid vaadata iga eraldi kaupluse kohta. Selleks valige kauplus, mille ATP-d soovite vaadata, ja seejärel klõpsake valikut **Kaupluse saadavuse kuvamine**.
