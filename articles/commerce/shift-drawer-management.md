---
title: Vahetuse ja sularahasahtli haldamine
description: See artikkel selgitab, kuidas seadistada ja kasutada vahetusi Commerce pos-i kassas.
author: josaw1
ms.date: 05/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.industry: Retail
ms.search.form: RetailHardwareProfile, RetailTerminalTable
ms.openlocfilehash: effba19634ee26ddeb86b1cf01ad970daff07dae
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287453"
---
# <a name="shift-and-cash-drawer-management"></a>Vahetuse ja sularahasahtli haldamine

[!include [banner](includes/banner.md)]

See artikkel selgitab, kuidas seadistada ja kasutada vahetusi Commerce pos-i kassas.

Rakenduses Dynamics 365 Commerce kirjeldab termin *vahetus* kogumit kassa kandeandmetest ja tegevustest kahe ajahetke vahel. Iga vahetuse korral võrreldakse eeldatud rahasummat loendatud ja deklareeritud summaga.

Tavaliselt avatakse vahetused tööpäeva alguses. Sel hetkel deklareerib kasutaja algsumma, mis on sularahasahtlis. Seejärel tehakse kogu päeva jooksul müügikandeid. Päeva lõpus loetakse sahtel üle ja deklareeritakse sulgemissummad. Vahetus suletakse ja luuakse Z-aruanne. Z-aruanne näitab, kas esineb ülejääki või puudujääki.

## <a name="typical-shift-scenarios"></a>Tavalised vahetuse stsenaariumid

Commerce pakub erinevaid konfigureerimisvalikuid ja kassatoiminguid, et toetada kassas erinevaid päeva lõpetamise äriprotsesse. Selles jaotises kirjeldatakse mõningaid tavalisi vahetuse stsenaariume.

### <a name="fixed-till"></a>Fikseeritud kassasahtli sisu

Seda stsenaariumi on kasutatud kõige rohkem. Seda kasutatakse siiamaani väga palju. Vahetuses „Fikseeritud kassasahtli sisu” on vahetus ja kassasahtli sisu seostatud kindla kassaaparaadiga. Neid ei teisaldata ühest kassaaparaadist teise. Vahetust „Fikseeritud kassasahtli sisu” saab kasutada üksikkasutaja või seda saab jagada mitme kasutaja vahel. Vahetused „Fikseeritud kassasahtli sisu” ei nõua erilist konfiguratsiooni.

### <a name="floating-till"></a>Ujuv kassasahtli sisu

Vahetuses „Ujuv kassasahtli sisu” saab vahetust ja sularahasahtlit teisaldada ühest kassaaparaadist teise. Kuigi kassaaparaadil saab olla ainult üks aktiivne vahetus sularahasahtli kohta, saab vahetusi peatada ja seejärel hiljem või teises kassaaparaadis jätkata.

Näiteks on kauplusel kaks kassaaparaati. Iga kassaaparaat avatakse päeva alguses, kui kassapidaja avab uue vahetuse ja esitab algsumma. Kui üks kassapidaja on valmis pausi tegema, peatab ta oma vahetuse ja eemaldab kassasahtli sisu sularahasahtlist. Seejärel on kassaaparaat saadaval teiste kassapidajate jaoks. Teine kassapidaja saab kassaaparaadis sisse logida ja oma vahetuse avada. Kui esimese kassapidaja paus on lõppenud, saab see kassapidaja oma vahetust jätkata, kui üks teistest kassaaparaatidest vabaneb. Vahetused „Ujuv kassasahtli sisu” ei nõua erilist konfiguratsiooni või luba.

### <a name="single-user"></a>Üks kasutaja

Paljud jaemüüjad eelistavad lubada ainult üht kasutajat vahetuse kohta, et tagada kõrgeimal tasemel vastutavus sularahasahtlis oleva sularaha eest. Kui ainult ühel kasutajal on lubatud vahetusega seostatud kassasahtli sisu kasutada, on see kasutaja ainuisikuliselt vastutav võimalike lahknevuste eest. Kui vahetust kasutab mitu kasutajat, on raske kindlaks määrata, kes vea tegi või kes võib üritada kassasahtli sisu varastada.

### <a name="multiple-users"></a>Mitu kasutajat

Mõned jaemüüjad on valmis ohverdama ühe kasutaja vahetustega kaasneva vastutavuse ja lubavad rohkem kui ühe kasutaja vahetuse kohta. See lähenemisviis on tavaline, kui kasutajaid on rohkem kui saadaolevaid kassaaparaate ning vajadus paindlikkuse ja kiiruse järele kaalub potentsiaalse kahjumi üle. See on tavaline ka siis, kui kaupluste juhatajatel pole enda vahetusi, kuid nad saavad vajaduse korral kasutada oma kassapidajate vahetusi. Sisselogimiseks ja teise kasutaja avatud vahetuse kasutamiseks peab kasutajal olema kassaluba **Luba mitme vahetuse sisselogimine**.

### <a name="shared-shift"></a>Ühine vahetus

Konfiguratsioon „Ühine vahetus” võimaldab jaemüüjatel kasutada üht vahetust mitmes kassaaparaadis, sularahasahtlis ja kasutajate vahel. Ühisel vahetusel on üks algsumma ja üks sulgemissumma, mis summeeritakse kõigist sularahasahtlitest. Ühised vahetused on kõige tavapärasemad mobiilsete seadmete kasutamisel. Selles stsenaariumis ei reserveerita iga kassaaparaadi jaoks eraldi sularahasahtlit. Selle asemel jagavad kõik kassaaparaadid üht sularahasahtlit.

Et kaupluses saaks kasutada ühiseid vahetusi, peab sularahasahtel olema konfigureeritud kui „Ühise vahetuse sahtel” valikus **Jaemüük ja kaubandus \> Kanali häälestus \> Kassa häälestus \> Kassa profiilid \> Riistvara profiilid \> Sahtel**. Lisaks peab kasutajatel olema üks või mõlemad ühise vahetuse load (Luba ühise vahetuse haldamine ja Luba ühise vahetuse kasutamine).

> [!NOTE]
> Korraga saab igas kaupluses olla avatud ainult üks ühine vahetus. Samas kaupluses saab kasutada ühiseid vahetusi ja eraldi vahetusi.

## <a name="shift-and-drawer-operations"></a>Vahetuse ja sahtli toimingud

Vahetuse oleku muutmiseks või sularahasahtlis oleva rahasumma suurendamiseks või vähendamiseks saab teha erinevaid toiminguid. Selles jaotises kirjeldatakse neid vahetusetoiminguid Modern POS-i ja pilvekassa puhul.

### <a name="open-shift"></a>Avatud vahetus

Kassa nõuab, et kasutajatel oleks aktiivne ja avatud vahetus, et teha toiminguid, mille tulemuseks on finantskanne, nagu müük, tagastus või klienditellimus.

Kui kasutaja logib kassasse sisse, kontrollib süsteem esmalt, kas aktiivne vahetus on praeguses kassaaparaadis selle kasutaja jaoks saadaval. Kui aktiivset vahetust pole saadaval, saab kasutaja seejärel olenevalt süsteemi konfiguratsioonist ja kasutaja lubadest avada uue vahetuse, jätkata olemasolevat vahetust või logida sisse kassavälises režiimis.

### <a name="declare-start-amount"></a>Deklareeri algsumma

See toiming on sageli esimene toiming, mida tehakse äsja avatud vahetuses. Selle toimingu jaoks määravad kasutajad vahetuse sularahakassas oleva sularaha algse koguse. See toiming on oluline, sest ülejäägi/puudujäägi arvutamisel, mis tehakse vahetuse sulgemisel, arvestatakse algsummat.

### <a name="float-entry"></a>Sularaha sissemakse

*Vahetusraha kirjed* on müügiga mitteseotud kanded, mis tehakse aktiivse vahetuse ajal, et suurendada sularahasahtlis oleva sularaha kogust. Vahetusraha kirje tavaliseks näiteks on kanne täiendava vahetusraha lisamiseks sahtlisse, kui vahetusraha on vähe.

### <a name="tender-removal"></a>Väljamakse

*Väljamaksed* on müügiga mitteseotud kanded, mis tehakse aktiivse vahetuse ajal, et vähendada sularahasahtlis oleva sularaha kogust. Seda toimingut kasutatakse kõige sagedamini koos vahetusraha kirje toiminguga muus vahetuses. Näiteks, kuna kassaaparaadis 1 on vähe vahetusraha, seetõttu teeb kassaaparaadi 2 kasutaja väljamakse, et vähendada tema sularahasahtlis olevat summat. Kassaaparaadi 1 kasutaja teeb seejärel vahetusraha kirje, et suurendada oma sularahasahtlis olevat summat.

### <a name="suspend-shift"></a>Peata vahetus

Kasutaja saab peatada oma aktiivse vahetuse, et vabastada praegune kassaaparaat muu kasutaja jaoks või et teisaldada oma vahetus teise registrisse (sel juhul nimetatakse seda sageli ujuvaks kassasahtli sisuks).

Vahetuse peatamine takistab uute kannete või muudatuste tegemist vahetuses kuni selle jätkamiseni.

### <a name="resume-shift"></a>Jätka vahetust

See toiming võimaldab kasutajatel jätkata eelnevalt peatatud vahetust kassaaparaadis, kus ei ole veel aktiivset vahetust.

### <a name="tender-declaration"></a>Päevakassa

See toiming võimaldab määrata praegu sularahasahtlis oleva kogusumma. Kasutajad teevad seda toimingut enamasti enne nende vahetuse sulgemist. Määratud summat võrreldakse eeldatud vahetuse summaga, et arvutada ülejäägi/puudujäägi summa.

### <a name="safe-drop"></a>Seifi viidav raha

Seifi viidava raha toimingu saab teostada aktiivses vahetuses igal ajal. See toiming eemaldab raha sularahasahtlist, et selle saaks üle kanda turvalisemasse asukohta, nagu tagaruumis asuv seif. Seifi viidava raha kogusumma kaasatakse vahetuse kogusummasse, kuid seda ei tule arvestada päevakassa osana.

### <a name="bank-drop"></a>Raha hoiustamine panka

Sarnaselt seifi viidava raha toimingule tehakse ka raha panka hoiustamise toimingut aktiivse vahetuse ajal. See toiming eemaldab raha vahetusest, et valmistada see ette pangadeposiidi jaoks.

### <a name="blind-close-shift"></a>Pimedalt suletud vahetus

*Pimesi suletud vahetused* ei ole enam aktiivsed, kuid need ei ole täielikult suletud. Erinevalt peatatud vahetustest ei saa pimesi suletud vahetusi jätkata. Kuid nendega saab hiljem või teises kassaaparaadis teha toiminguid, nagu Deklareeri algsumma ja Päevakassa.

Pimedalt suletud vahetusi kasutatakse sageli registri vabastamiseks uue kasutaja või vahetuse jaoks, ilma et eelnevalt tuleks seda vahetust täielikult loendada, vastavusse viia või sulgeda.

### <a name="close-shift"></a>Sule vahetus

See toiming arvutab vahetuse kogusummad ja ülejäägi/puudujäägi summa ning seejärel viib aktiivse või pimedalt suletud vahetuse lõpule. Olenevalt kasutaja õigustest prinditakse vahetuse jaoks ka Z-aruanne. Suletud vahetusi ei saa jätkata või muuta.

### <a name="print-x"></a>Prindi X

See toiming loob ja prindib praeguse aktiivse vahetuse jaoks X-aruande.

### <a name="reprint-z"></a>Kordustrüki Z

See toiming prindib uuesti viimase Z-aruande, mille süsteem lõi vahetuse sulgemisel.

### <a name="manage-shifts"></a>Vahetuste haldamine

See toiming võimaldab kasutajatel vaadata kõiki kaupluse aktiivseid, peatatud ja pimedalt suletud vahetusi. Olenevalt oma lubadest saavad kasutajad teostada oma lõplikud sulgemise toimingud, nagu Päevakassa arvutamine ja Sule vahetus pimedalt suletud vahetuste jaoks. See toiming võimaldab ka kasutajatel vaadata ja kustutada kehtetuid vahetusi, kui peaks juhtuma, et vahetused on pärast ühenduseta ja ühendusega režiimide vahel lülitamist jäänud vigasesse olekusse. Need kehtetud vahetused ei sisalda vastavusseviimiseks vajalikku finantsteavet või kandeandmeid.

## <a name="shift-and-drawer-permissions"></a>Vahetuse ja sahtli load

Järgmised kassaload mõjutavad, mida kasutajad saavad ja ei saa erinevates stsenaariumides teha:

- **Luba pimedalt sulgemine**
- **Luba x-aruande printimine**
- **Luba z-aruande printimine**
- **Luba päevakassa**
- **Luba vahetusraha akt**
- **Ava sahtel ilma müügita**
- **Luba mitme vahetuse sisselogimine** – see õigus lubab kasutajal logida sisse ja kasutada teise kasutaja avatud vahetust. Kasutajad, kes ei ole seda õigust, saavad sisse logida ja kasutada ainult vahetusi, mille nad on ise avanud.
- **Luba ühise vahetuse haldamine** – kasutajatel peab olema see õigus ühise vahetuse avamiseks või sulgemiseks.
- **Luba ühise vahetuse kasutamine** – kasutajatel peab olema see õigus ühisesse vahetusse sisselogimiseks ja selle kasutamiseks.

## <a name="back-office-end-of-day-considerations"></a>Kontori päeva lõpetamise kaalutlused

Vahetuste ja sularahasahtli vastavusseviimise kasutamise viis kassas erineb viisist, kuidas kandeandmeid summeeritakse väljavõtete arvutamisel. On tähtis, et mõistaksite erinevust. Olenevalt teie konfiguratsioonist ja äriprotsessidest võivad vahetuse andmed kassas (Z-aruanne) ja arvutatud väljavõte kontoris anda erinevaid tulemusi. See erinevus ei tähenda tingimata, et vahetuse andmed või arvutatud väljavõte on valed või et andmetega on probleem. See tähendab lihtsalt seda, et esitatud parameetrid võivad sisaldada täiendavat kannet või vähem kandeid või et kanded on summeeritud erinevalt.

Kuigi igal jaemüüjal on erinevad ärinõuded, soovitame häälestada süsteemi järgmisel viisil, et vältida olukordi, kus esinevad seda tüüpi erinevused:

Avage **Jaemüük ja kaubandus \> Kanalid \> Kauplused \> Kõik kauplused \> Väljavõte/sulgemine** ja määrake iga kaupluse jaoks väli **Väljavõtte viis** ja **Sulgemisviis** olekule **Vahetus**.

See häälestus aitab tagada, et kontori väljevõtted sisaldavad samu kandeid, mis vahetused kassas ja et selle vahetuse andmed summeeritakse.

Lisateavet väljavõtte ja sulgemisviiside kohta vt [Jaemüügi väljavõtete kauplusekonfiguratsioonid](/dynamics365/unified-operations/retail/tasks/store-configurations-retail-statements).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
