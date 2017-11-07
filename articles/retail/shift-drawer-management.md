---
title: Vahetuse ja sularahasahtli haldamine
description: "Selles artiklis selgitatakse, kuidas seadistada ja kasutada kahte tüüpi jaemüügikassa vahetust – ühist ja eraldiseisvat. Ühiseid vahetusi saab kasutada mitu kasutajat mitmes kohas, samas kui eraldi vahetusi saab kasutada korraga ainult üks töötaja."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 72f73404f99330c3ff8b23dabed78477a0cd30cd
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="shift-and-cash-drawer-management"></a>Vahetuse ja sularahasahtli haldamine

[!include[banner](includes/banner.md)]


Selles artiklis selgitatakse, kuidas seadistada ja kasutada kahte tüüpi jaemüügikassa vahetust – ühist ja eraldiseisvat. Ühiseid vahetusi saab kasutada mitu kasutajat mitmes kohas, samas kui eraldi vahetusi saab kasutada korraga ainult üks töötaja.

Jaemüügikassa (POS) vahetusi on kahte tüüpi: eraldi ja ühine. Eraldi vahetusi saab kasutada korraga ainult üks töötaja. Ühiseid vahetusi saab kasutada mitu kasutajat mitmes kohas. Seetõttu loovad need tõhusalt ühe vahetuse mitme kaupluse töötaja jaoks.

## <a name="standalone-shifts"></a>Eraldiseisvad vahetused
Eraldiseisvaid vahetusi kasutatakse tavapärastes, fikseeritud kassa stsenaariumides, kus kassat tasakaalustatakse iga kassaregistri kohta eraldi. Näiteks toidukaupluse seadistuses on tavaliselt mitu fikseeritud kassaregistrit ja igale registrile on määratud kassiir. Sel juhul kasutab iga register tõenäoliselt eraldiseisvat vahetust ja kassiir vastutab kassasahtli sisu või selles registris oleva füüsilise sularaha eest. Eraldi vahetus hõlmab kõiki selle registri tegevusi kassiiri töövahetuse ajal. Tegevused võivad sisaldada kassasahtlis olevat avasummat, kõiki sularaha väljavõtmisi ja lisamisi toimingute kaudu nagu raha hoiustamine panka ja sularaha sissemakse ning päevakassa vahetuse lõpus.

### <a name="set-up-a-stand-alone-shift"></a>Eraldiseisva vahetuse seadistamine

Eraldiseisev vahetus määratakse kassasahtli tasandil. See protseduur selgitab, kuidas seadistada kassaregistris eraldiseisvat vahetust.

1.  Klõpsake valikuid **Jaemüük** &gt; **Kanali häälestus** &gt; **Kassa häälestus** &gt; **Kassaprofiilid** &gt; **Riistvaraprofiilid**.
2.  Valige riistvaraprofiil, mida eraldiseisva vahetuse puhul kasutada.
3.  Kinnitage kiirkaardil **Sahtel**, et valiku **Ühise vahetuse sahtel** väärtuseks oleks määratud **Ei**.
4.  Klõpsake käsku **Salvesta**.
5.  Klõpsake valikuid **Jaemüük** &gt; **Kanali häälestus** &gt; **Kassa häälestus** &gt; **Registrid**.
6.  Valige register, mis nõuab eraldi vahetust, ja klõpsake siis käsku **Redigeeri**.
7.  Valige väljalt **Riistvaraprofiil** 2. etapis valitud riistvaraprofiil.
8.  Klõpsake käsku **Salvesta**.
9.  Klõpsake valikut **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafik**.
10. Valige jaotusgraafik **1090** ja klõpsake siis käsku **Käivita kohe** kassa muudatuste sünkroonimiseks.

### <a name="use-a-stand-alone-shift"></a>Eraldiseisva vahetuse kasutamine

1.  Logige kassasse sisse.
2.  Kui pole ühtegi avatud vahetust, siis valige **Ava uus vahetus**.
3.  Minge toimingu **Deklareeri algsumma** juurde ja määrake sularahasumma, mis kassasahtlisse tööpäeva alustamiseks pannakse.
4.  Tehke mõned kanded.
5.  Päeva lõpus valige **Päevakassa tegemine** sularahasahtlisse jääva sularaha hulga kinnitamiseks.
6.  Sisestage sularahasumma ja klõpsake siis käsku **Salvesta** päevakassa salvestamiseks.
7.  Vahetuse sulgemiseks valige **Sule vahetus**.

**Märkus.** Vahetuse ajal on saadaval muud toimingud, olenevalt kehtivatest äriprotsessidest. Raha eemaldamiseks kassasahtlist päeva kestel või enne vahetuse sulgemist võib kasutada toiminguid **Seifi viidav raha**, **Raha hoiustamine panka** ja **Väljamakse**. Kui kassasahtlis jääb sularaha väheks, võib sinna sularaha lisamiseks kasutada toimingut **Sularaha sissemakse**.

## <a name="shared-shifts"></a>Ühised vahetused
Ühist vahetust kasutatakse keskkonnas, kus mitmel kassiiril on tööpäeva jooksul ühine sularahasahtel või sularahasahtlite kogum. Tavaliselt kasutatakse ühist vahetust mobiilse kassa keskkondades. Mobiilses keskkonnas ei määrata igale kassiirile ühte sularahasahtlit ning ta ei vastuta selle eest. Selle asemel peavad kõik kassiirid saama registreerida müüki ja lisada sularaha, endale lähimat kassasahtlit kasutades. Selle stsenaariumi puhul kuuluvad kassiiride ühised sularahasahtlid ühisesse vahetusse. Kõik ühise vahetuse sularahasahtlid kuuluvad selle vahetuse sularahahalduse tegevustega seoses samasse vahetusse. Seetõttu peaks vahetuse algsumma sisaldama kõigi ühisesse vahetusse kuuluvate sularahasahtlite sularahasummat. Samamoodi on päevakassa kõigi ühisesse vahetusse kuuluvate sularahasahtlite sularahasumma. **Märkus.** Korraga saab igas kaupluses olla avatud ainult üks ühine vahetus. Samas kaupluses saab kasutada ühiseid vahetusi ja eraldi vahetusi.

### <a name="set-up-a-shared-shift"></a>Ühise vahetuse seadistamine

1.  Klõpsake valikuid **Jaemüük** &gt; **Kanali häälestus** &gt; **Kassa häälestus** &gt; **Kassaprofiilid** &gt; **Riistvaraprofiilid**.
2.  Valige riistvaraprofiil, mida ühise vahetuse puhul kasutada.
3.  Määrake kiirkaardil **Sahtel** valiku **Ühise vahetuse sahtel** väärtuseks **Jah**.
4.  Klõpsake käsku **Salvesta**.
5.  Klõpsake valikuid **Jaemüük** &gt; **Kanali häälestus** &gt; **Kassa häälestus** &gt; **Registrid**.
6.  Valige register, mis nõuab ühist vahetust, ja klõpsake siis käsku **Redigeeri**.
7.  Valige väljalt **Riistvaraprofiil** 2. etapis valitud riistvaraprofiil.
8.  Klõpsake käsku **Salvesta**.
9.  Klõpsake valikut **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafik**.
10. Valige jaotusgraafik **1090** ja klõpsake siis käsku **Käivita kohe** kassa muudatuste sünkroonimiseks.

### <a name="use-a-shared-shift"></a>Ühise vahetuse kasutamine

1.  Logige kassasse sisse.
2.  Kui kassa pole veel riistvarajaamaga ühendatud, siis valige **Kassaväline toiming** ja seejärel **Riistvarajaama valimine**, et muuta riistvarajaam ühise vahetuse puhul aktiivseks. See samm on vajalik üksnes esimesel korral, kui register ühise vahetuse keskkonda lisatakse.
3.  Logige kassast välja ja siis uuesti sisse.
4.  Valige käsk **Loo uus vahetus**.
5.  Valige käsk **Deklareeri algsumma**.
6.  Sisestage kõigi kassasahtlite arv kaupluses, mis ühisesse vahetusse kuuluvad, ja klõpsake siis käsku **Salvesta**.
    -   Algsumma osa lisamiseks igasse järgmisse kassasahtlisse kasutage toimingut **Riistvarajaama valimine** riistvarajaama aktiveerimiseks.
    -   Kassasahtli sisu lisamiseks konkreetsesse kassasahtlisse kasutage toimingut **Ava sahtel**.
    -   Jätkake, kuni kõigis ühise vahetuse kassasahtlites on osa algsummast.

7.  Päeva lõpus avage iga kassasahtel ja võtke sularaha välja.
8.  Kui olete viimasest sularahasahtlist raha välja võtnud, lugege üle kõigi kassasahtlite raha.
9.  Kasutage toimingut **Päevakassa tegemine** kõigis ühise vahetuse sularahasahtlites olnud sularahasumma kinnitamiseks.
10. Ühise vahetuse sulgemiseks kasutage toimingut **Sule vahetus**.





