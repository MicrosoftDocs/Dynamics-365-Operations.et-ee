---
title: Funktsioonide haldamine
description: Saage teada, kuidas lülitada uusi funktsioone rakenduses Dynamics 365 Human Resources sisse või välja.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 84ff11e8237ce0669f7f6ac70c5b4411c5d4b466
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008721"
---
# <a name="manage-features"></a>Funktsioonide haldamine

Rakenduse Microsoft Dynamics 365 Human Resources pidevate uute võimaluste levitamise osana tahame, et kliendid saaksid proovida uusi funktsioone niipea kui võimalik. Pakume uusi eelvaatefunktsioone, mis on peaaegu valmis üldiseks kasutamiseks ja on läbinud põhjalikud kontrollid. Eelvaatefunktsioonide puhul soovime saada täiendavat kasutajate tagasidet ja kinnitust, enne kui funktsioonid üldiselt kättesaadavaks teeme.

Lisateavet Human Resourcesi uute funktsioonide kohta vt teemast [Mis on uut rakenduses Human Resources](hr-admin-whats-new.md) ja [Dynamics 365 ja Power Platformi väljalaskeplaan](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1).

Tööruumis **Funktsioonihaldus** on toodud loend igas väljaandes saadetud funktsioonidest. Vaikimisi on uued funktsioonid välja lülitatud. Saate kasutada tööruumi funktsioonide sisselülitamiseks ja nende dokumentatsiooni vaatamiseks. Lisateavet funktsioonihalduse kohta vt [Funktsioonihalduse ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Kõik uued funktsioonid jäävad vähemalt 30 päevaks eelvaatesse ja tavaliselt 30–60 päevaks. Peamised funktsioonid on tavaliselt saadaval eelvaate perioodile järgneva iga aasta oktoobris ja aprillis. Kohe kui näete tööruumis **Funktsioonihaldus** uusi võimalusi, saate need sisse lülitada. Mõned funktsioonid võivad olla vaikimisi sisse lülitatud.

Kui funktsioon on üldsusele saadaval, võib selle tootmiskeskkonnas sisse või välja lülitada. Tööruum **Funktsioonihaldus** näitab, millal muutub eelvaate funktsioon kohustuslikuks. See kuupäev on tavaliselt 1. oktoobril või 1. aprillil, et ühitada poolaasta väljalaskeplaanidega. Kohustuslikke funktsioone välja lülitada ei saa. Kuni see muutub kohustuslikuks, saate funktsiooni kõikides keskkondades sisse ja välja lülitada.

## <a name="enable-or-disable-preview-features"></a>Eelvaatefunktsioonide lubamine või keelamine

Eelvaatefunktsioonidele ligipääsemiseks peate kõigepealt need oma keskkonnas lubama. Eelvaatefunktsioonide lubamine või keelamine sõltub keskkonnast.

> [!IMPORTANT]
> Eelvaatefunktsioonid on saadaval ainult keskkondades **Liivakast**. Kui lülitate eelvaatefunktsiooni sisse, siis lubate selle kõikidele teie organisatsiooni kasutajatele, kes on selles keskkonnas. Kui lülitate eelvaatefunktsiooni välja, siis keelate selle ja teie kasutajatel pole sellele juurdepääsu. Eelvaatefunktsioonidel on rakenduses Human Resources piiratud tugi. Need võivad kasutada vähem privaatsus- ja turbemeetmeid ning pole hõlmatud teenuse Human Resources teenindustaseme lepingus (SLA). Eelvaatefunktsioone ei tohi kasutada isikuandmete (st igasugused andmed, mis võimaldavad isikut tuvastada) ega muude andmete töötlemiseks, millele kehtivad seaduste või regulatsioonide järgmise nõuded.

1. Valige rakenduses Human Resources suvand **Süsteemihaldus**.

2. Valige paan **Funktsioonihaldus**.

3. Eelvaatefunktsiooni lubamiseks valige see loendist ja seejärel valige käsk **Luba**. Eelvaatefunktsiooni keelamiseks valige see loendist ja seejärel valige käsk **Keela**.

## <a name="preview-feature-benefits-management"></a>Eelvaatefunktsioon: soodustuste haldus

Soodustuste haldus pakub paindlikku lahendust, mis toetab mitmesuguseid soodustuse võimalusi, koos hõlpsalt kasutatava töövõtja kogemusega, mis näitab teie pakkumisi. Lisateavet soodustuste halduse konfiguratsiooni ja kasutamise kohta vt teemast [Soodustuste halduse ülevaade](hr-benefits-management-overview.md).

Soodustuste haldus asendab funktsiooni tööruumis **Soodustused**. Kui lubate soodustuste halduse eelvaatefunktsiooni, ei saa te enam kasutada tööruumi **Soodustused** järgmisi vorme:

- **Soodustused**
- **Soodustuse elemendid**
- **Panuse arvutamise määrad**
- **Soodustuse registreerimise tulemused**
- **Soodustuse aegunuks märkimise ja pikendamise tulemused**
- **Soodustuskõlblikkuse poliitika reegli tüübid**
- **Soodustuse saamise õiguse eeskirjad**
- **Kõlblikkuse sündmused**

Saate kuvada nende vormi teabe ainult kirjutuskaitstud režiimis. Kui soovite teavet redigeerida, peake kõigepealt keelama soodustuste halduse eelvaatefunktsiooni.

### <a name="benefits-management-known-issues"></a>Soodustuste halduse teadaolevad probleemid

#### <a name="life-events"></a>Elusündmused

Elusündmuste töötlemisel kuvatakse kasutajale tõrge:

Kehtivusperioodi alguskuupäev peab olema vahemikus *plaani perioodi algus* kuni *plaani perioodi lõpp*. 

Elusündmuse töötlus jätkub ootuspäraselt.

#### <a name="eligibility-processing"></a>Sobivuse töötlemine

Kui käitate soodustusteks sobilikkust, mis kasutavad kindlustussummat 1–5 × palk, Protsent palgast ja Kindel summa, peab soodustuse kuupäev olema määratud töövõtja alguskuupäevaks **tööhõive ajaloos**, koos töötatud tundidega, maksesagedusega ja aastase soodustuste palga summaga. Kui töötaja jaoks on olemas põhipalk, sisestage töötatud tunnid koos maksesagedusega ja aastane palgasumma arvutatakse. Kui töövõtja on kuupalgaline, ei ole töötunnid vajalikud. Soovitame uute töötajate loomisel sisestada esmalt põhipalk. Soodustuse üksikasjade kirje värskendamine tehke järgmist. Navigeerige asukohta **Töötaja > Töötaja ajalugu > Tööhõive üksikasjad**. Muutke töötajate alustamiskuupäeva.

#### <a name="employee-self-service"></a>Töövõtja iseteenindus

Töötajad saavad valida plaani, mida nad ei ole kvalifitseeritud ja registreeruda välja. Näiteks: töötajal ei ole sõltuvaid, kuid nad võivad valida perekonna katvuse võimalusega meditsiiniplaani.

Töövõtja summat ei arvutata elukindlustuse katvussumma värskendamisel. Näiteks kui töövõtjale pakutakse elukindlustuse plaani, saavad nad valida katvuse kuni 50 000 dollarit hinnaga 0,36 dollarit 1000 dollari kohta.  Kui töövõtja uuendab katvussummat, jääb töövõtja seotud kulu nulli.

Soodustuse plaani jaoks, mis lubab ainult ühe selle plaani tüübi valiku, kuvatakse kasutajale viga, kui nad proovivad plaanist pärast plaani valimist loobuda. Näiteks valib kasutaja meditsiiniplaani ja lisab selle oma ostukorvi. Seejärel valib kasutaja teise meditsiiniplaani jaoks suvandi **Loobu**. Kasutajale kuvatakse viga.

## <a name="preview-features-in-leave-and-absence"></a>Puhkuste ja puudumiste eelvaatefunktsioonid

Puhkuste ja puudumiste eelvaatefunktsioonid hõlmavad järgnevat.

- **Puhkuste ja puudumiste kalender** – puhkuse ja puudumiste parameetrid liiguvad suvandist **Inimressursside parameetrid** uuele ekraanile, mille nimi **Puhkuste ja puudumiste parameetrid**. Uus ekraan sisaldab uut vahekaarti **Kalender**. See eelvaade võimaldab ainult parameetrite alamkogumit. Pääsete uuele ekraanile ligi vahekaardilt **Lingid** tööruumis **Puhkused ja puudumised**. Kalendrid hõlmavad järgmist.
  - **Ettevõtte kalender** – kuvab kõik töövõtja eemalolekuaja taotlused. Inimesed rolliga **Inimressursid** pääsevad sellele kalendrile ligi vahekaardilt **Lingid** tööruumis **Puhkused ja puudumised**.
  - **Halduri töörühma kalender** – kuvab kõik otseste alluvate eemalolekuaja taotlused. Haldurid pääsevad kalendrile ligi vahekaardilt **Minu töörühm** töövõtja iseteeninduse jaotises **Puhkused ja puudumise**. 

- **Puhkuste ja puudumiste puhkuse kalendrid** – puhkuste tüübid sisaldavad uut valikut **Puhkus**, mida kasutatakse koos tööaja kalendriga. Pühade ja sulgemiste määratletud päevad määratakse nüüd tööpäevade loomisel kui **Püha**. Lisandumiste töötlemisel tehakse kalendrile määratud töövõtjatele korrigeerimisi, et arvestada pühadega, mis langevad tööpäevadele.

- **Puhkuse lisandumise auditeerimine** – uus ekraan võimaldab teil vaadata üle, kui lisandumisi on töödeldud ja kustutatud, nii kõikide töövõtjate kui ka üksikute töövõtjate poolt. Pääsete sellele uuele ekraanile ligi vahekaardilt **Lingid** tööruumis **Puhkused ja puudumised**.

- **Puudumise lisandumise kustutamine** – saate nüüd kustutada konkreetsete puhkuseplaanide lisandumiste kirjed. Pääsete sellele uuele suvandile ligi vahekaardilt **Lingid** tööruumis **Puhkused ja puudumised**. Üksikute töövõtjate puhul kuvatakse see suvand töötaja profiili rühmituses **Puhkused ja puudumised**. 

- **Puhkuse lisandumise ümardamine** – suvandi **Puhkuse tüüp** uued valikud määratlevad, mis tüüpi ümardamise lisandumist tuleks kasutada, koos lisandumise protsessi ajal ümardamise kümnendkoha täpsusega. Lisandumiste töötlemisel rakendatakse lisandumise kirjetele ümardamist ja täpsust. 

- **Mitme puhkuse tüübi konfigureerimine ühes puhkuseplaanis** – puhkuse tüüpide puhkuse lisandumise graafiku uus veerg võimaldab teil määratleda puhkuse ja puudumise plaanis mitu puhkuse tüüpi erinevate lisandumise graafikutega. Eelmine väli **Puhkuse tüüp** on eemaldatud. Töövõtja registreerimisel kuvatakse puhkuse tüüpide saldod nüüd ekraani ülaosa asemel tabelis.

  > [!IMPORTANT]
  > Pärast selle lubamist ei saa seda funktsiooni välja lülitada.

- **Kasutaja lisandumise jaoks töövõtja täistööaja vastet (FTE)** – puhkuste lisandumise graafiku uus veerg võimaldab lisandumiseks kasutada täistööaja vastet. Lisandumiste töötlemisel kasutab rakendus töövõtja esmast ametikohta ja määratud täistööaja vastet, et määrata eelmääratud lisandumise summa.

  > [!NOTE]
  > See funktsioon on saadaval ainult juhul, kui lubate suvandi **Mitme puhkuse tüübi konfigureerimine puhkuseplaanis**. 

## <a name="feedback"></a>Tagasiside

Ootame teie tagasisidet teie kogemuse kohta nende eelvaatefunktsioonidega. Soovitame teil postitada tagasisidet nende või muude funktsioonide kasutamise kohta järgmistel saitidel.

- [Kogukonna foorum](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – sellel saidil on mitmeid ressursse ning kasutajad saavad arutada kasutusjuhtumeid, küsida küsimusi ja otsida kogukonnalt abi.
- Andke meile teada funktsioonidest, mida soovite tootes näha, või andke teada muudatustest, mida teie arvates oleks olemasolevates funktsioonides vaja. Pakkuge tooteideid asukohas [Rakenduse Human Resources ideed](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    
Ärge kasutage tagasisides ega tootearvustustes isikuandmeid (igasugused andmed, mis võimaldavad isikut tuvastada). Kogutud teavet võidakse põhjalikumalt analüüsida ja seda ei kasutata kohalduvate isikuandmete kaitse seaduste järgi taotluste täitmiseks. Isikuandmetele, mida kogutakse eraldi nende programmidega, kehtib [Microsofti privaatsusavaldus](https://privacy.microsoft.com/privacystatement).

## <a name="see-also"></a>Vt ka

- [Mis on rakenduses Human Resources uut?](hr-admin-whats-new.md)
- [Dynamics 365 ja Power Platformi väljalaskeplaan](https://docs.microsoft.com/dynamics365/release-plans/#pivot=products&panel=products1)