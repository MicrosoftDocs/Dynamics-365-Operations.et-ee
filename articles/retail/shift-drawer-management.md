---
title: Vahetuse ja sularahasahtli haldamine
description: "Selles artiklis selgitatakse, kuidas seadistada ja kasutada kahte tüüpi jaemüügikassa vahetust – ühist ja eraldiseisvat. Ühiseid vahetusi saab kasutada mitu kasutajat mitmes kohas, samas kui eraldi vahetusi saab kasutada korraga ainult üks töötaja."
author: rubencdelgado
manager: AnnBe
ms.date: 02/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailHardwareProfile, RetailTerminalTable
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
ms.sourcegitcommit: 8a24f8adc4f7886a1f942d83f7a4eb12e7034fcd
ms.openlocfilehash: c1483d3240d266845cea7789b70c038cb98fdfcc
ms.contentlocale: et-ee
ms.lasthandoff: 03/22/2018

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

## <a name="shift-operations"></a>Vahetuse toimingud
Vahetuse oleku muutmiseks või sahtlis oleva rahasumma suurendamiseks või vähendamiseks on mitu võimalust. Allolevas jaotises kirjeldatakse neid vahetuse toiminguid rakenduse Dynamics 365 for Retail tänapäevases kassas ja pilve kassas.

**Avatud vahetus**

Kassa nõuab, et kasutajal oleks aktiivne ja avatud vahetus, et teha toiminguid, mille tulemuseks on finantskanne, nagu müük, tagastus või klienditellimus.  

Kassasse sisselogimisel kontrollib süsteem esmalt, kas kasutajal on praeguses registris saadaval aktiivne vahetus. Kui ei, saab kasutaja seejärel olenevalt süsteemi konfiguratsioonist ja oma lubadest valida, kas ta soovib avada uue vahetuse, jätkata olemasolevat vahetust või jätkata sisselogimist kassavälises režiimis.

**Deklareeri algsumma**

See toiming on sageli esimene tegevus, mida tehakse äsja avatud vahetuses. Kasutajad määravad vahetuse kassas oleva sularaha algse koguse. See on oluline, sest vahetuse sulgemisel ilmnev üle-/vähemarvutamine moodustab osa selle summa kujunemisel.

**Vahetusraha kirje**

Vahetusraha kirjed on müügiga mitteseotud kanded, mis tehakse aktiivse vahetuse ajal ja mis suurendavad sahtlis oleva sularaha kogust. Vahetusraha kirje tavaliseks näiteks on täiendava vahetusraha lisamine sahtlisse, kui vahetusraha on vähe.

**Väljamakse**

Väljamaksed on müügiga mitteseotud kanded, mis tehakse aktiivse vahetuse ajal, et vähendada sahtlis oleva sularaha kogust. Seda kasutatakse kõige sagedamini koos vahetusraha kirjega muus vahetuses. Näiteks, registris 1 on vähe vahetusraha, seetõttu teeb registri 2 kasutaja väljamakse, et vähendada sahtlis olevat summat. Registri 1 kasutaja sisestab seejärel vahetusraha kirje, et suurendada enda summat.

**Peata vahetus**

Kasutaja saab peatada oma aktiivse vahetuse, et vabastada praegune register muu kasutaja jaoks või et teisaldada oma vahetus teise registrisse (seda nimetatakse sageli ujuvaks kassasahtli sisuks). 

Vahetuse peatamine takistab uute kannete või muudatuste tegemist vahetuses kuni selle jätkamiseni.

**Jätka vahetust**

See toiming võimaldab kasutajal jätkata eelnevalt peatatud vahetust registris, kus ei ole veel aktiivset vahetust.

**Päevakassa**

Päevakassa arvutamine on tegevus, mille kasutaja teeb, et täpsustada praegu kassas olev kogusumma, enamasti enne vahetuse sulgemist. See on väärtus, mida võrreldakse eeldatud vahetusega, et arvutada üleliigne/puuduv summa.

**Seifi viidav raha**

Seifi viidava raha toimingu saab teostada igal ajal aktiivses vahetuses. See toiming eemaldab raha sahtlist, nii et selle saaks üle kanda turvalisemasse asukohta, nagu tagaruumis asuv seif. Seifi viidava raha kogusumma kaasatakse endiselt vahetuse kogusummasse, kuid seda ei tule arvestada päevakassa osana.

**Raha hoiustamine panka**

Sarnaselt seifi viidava raha toimingule tehakse ka raha panka hoiustamise toimingut aktiivse vahetuse ajal. See toiming eemaldab raha vahetusest, et valmistada see ette pangadeposiidi jaoks.

**Pimedalt suletud vahetus**

Pimedalt suletud vahetus on vahetus, mis ei ole enam aktiivne, kuid pole veel täielikult suletud. Pimedalt suletud vahetusi ei saa jätkata, nagu peatatud vahetust, kuid toiminguid, nagu algsummade taotlemine ja päevakassa arvutamine saab teha ka hiljem või muust registrist.

Pimedalt suletud vahetusi kasutatakse sageli registri vabastamiseks uue kasutaja või vahetuse jaoks, ilma et eelnevalt tuleks seda vahetust täielikult loendada, vastavusse viia või sulgeda. 

**Sule vahetus**

See toiming arvutab vahetuse kogusummad ja üleliigse/puuduva summa ning seejärel viib aktiivse või pimedalt suletud vahetuse lõpule. Suletud vahetusi ei saa jätkata või muuta.  

**Vahetuste haldamine**

See toiming võimaldab kasutajatel vaadata kõiki kaupluse aktiivseid, peatatud ja pimedalt suletud vahetusi. Olenevalt oma lubadest saavad kasutajad teostada oma lõplikud sulgemise protseduurid, nagu päevakassa arvutamine ja pimedalt suletud vahetuste sulgemine. See toiming võimaldab ka kasutajatel vaadata ja kustutada kehtetuid vahetusi, kui peaks juhtuma, et vahetus on pärast ühenduseta ja ühendusega režiimide vahel lülitamist jäänud vigasesse olekusse. Need kehtetud vahetused ei sisalda vastavusseviimiseks vajalikku finantsteavet või kandeandmeid. 

