---
title: Organisatsiooni hierarhia kavandamine
description: "Enne organisatsioonide ja organisatsiooni hierarhiate seadistamist peate kindlasti mõistma, kuidas oma ettevõtte mudelit kõige paremini kujundada."
author: sericks007
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 17404
ms.assetid: babde0c6-bb5d-45ae-95ca-2af75a0ea292
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 45a00f03519679f07c95a669727ecd2fa1a91c41
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="plan-your-organizational-hierarchy"></a>Organisatsiooni hierarhia kavandamine

[!include[banner](../includes/banner.md)]


Organisatsioonide ja organisatsiooni hierarhiate seadistamiseks rakenduses Microsoft Dynamics 365 for Finance and Operations plaanige kindlasti oma ettevõtte mudel. Organisatsioonimudelil on rakenduse Dynamics 365 for Finance and Operations juurutamisele ja äriprotsessidele oluline mõju. 

Organisatsioonihierarhiad kajastavad ettevõtte koosseisu kuuluvate organisatsioonide seoseid. Seetõttu on organisatsioonimudeli loomisel kõige tähtsam arvestada teie ettevõtte struktuuri. Soovitame määratleda organisatsioonistruktuurid tippjuhtkonnalt ja osakondade (nt finants- ja raamatupidamis-, personali-, operatsiooni-, ostu- ning müügi- ja turundusosakond) juhtivatelt töötajatelt pärineva tagasiside põhjal. 

Hierarhiate planeerimisel on oluline arvestada ka organisatsiooni hierarhia ja finantsdimensioonide vahelist seost. Ettevõtte erinevate vaatepunktide tähistamiseks saab seadistada mitu organisatsiooni hierarhiat. Finantsdimensioonide abil saab luua nendel vaatepunktidel põhinevaid aruandeid. Looge koostöös oma rakenduse Microsoft Dynamics 365 for Finance and Operations partneriga hierarhiaid, mis rahuldavad nii organisatsiooni vajadusi kui ka seadusjärgset aruandlusvajadust. 

> [!Note]
> Ehkki saate kasutada finantsdimensioone juriidiliste isikute kajastamiseks rakenduses Dynamics 365 for Finance and Operations juriidilisi isikuid loomata, pole finantsdimensioonid mõeldud juriidiliste isikute tegevus- või ärivajaduste rahuldamiseks. Üksustevaheline raamatupidamisfunktsioon rakenduses Finance and Operations on mõeldud ainult iga kande loodavate raamatupidamiskirjete käsitlemiseks. 

> [!Caution]
> Organisatsioonide mudeli koostamisel ei tohiks lähtuda ainult selle artikli teabest. See dokumentatsioon on juhend. Lisajuhiseid saate oma rakenduse Finance and Operations partnerilt. Teie rakenduse Finance and Operations partneril on kogemusi mitmesugustes valdkondades ja kogu kliendibaasi lõikes.

## <a name="decide-whether-to-model-internal-organizations-as-legal-entities-or-operating-units"></a>Otsustage, kas siseorganisatsioonid on mudelis juriidilised isikud või tootmisüksused

Ettevõttel peab olema rakenduses Finance and Operations vähemalt üks juriidiline isik. Juriidiline isik võib sõlmida seaduslikke lepinguid ja on kohustatud koostama oma tegevuse kohta finantsaruandeid. 

Rakenduses Finance and Operations saab juriidilisi isikuid kasutada ärikanneteks või konsolideerimiseks. See tähendab, et juriidiline isik rakenduses Finance and Operations ei pruugi kajastada tingimata teie ettevõtte tegelikku üksust. Näiteks võib kannetes osalevale ettevõttele kuuluda allettevõtete juriidilisi isikuid. Selle stsenaariumi puhul on kannete jaoks vajalik juriidiline isik ja allettevõtete juriidiliste isikute tulemuste ja saldode konsolideerimiseks on vajalik virtuaalne juriidiline isik. 

Ettevõtte siseorganisatsioone (nt piirkondlikke kontoreid) saab kajastada täiendavate juriidiliste isikute või peamise juriidilise isiku tootmisüksustena. Tootmisüksus ei pea olema juriidiliselt määratletud organisatsioon. Tootmisüksusi kasutatakse ettevõtte majandusressursside ja tööprotsesside juhtimiseks. Näiteks osakonnad ja kulukeskused on tootmisüksused. 

Mõned funktsioonid rakenduses Finance and Operations toimivad erinevalt, sõltuvalt sellest, kas organisatsioon on juriidiline isik või tootmisüksus. Otsustamisel kaaluge hoolikalt allpool kirjeldatud funktsioone. 


### <a name="master-data"></a>Koondandmed
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik      
Mõned koondandmed (nt kliendid, maksetingimused, maksuamet ja laoalapõhine varude tellimine) tuleb seadistada iga juriidilise isiku jaoks. Mõned koondandmed (nt kasutajad, tooted ja suurem osa personaliandmeid) on kõigi juriidiliste isikute vahel ühiskasutuses. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Koondandmed on tootmisüksuste vahel ühiskasutuses. 

### <a name="module-parameters"></a>Mooduliparameetrid
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik    
Moodulite nagu ostureskontro, müügireskontro ning sularaha- ja pangahalduse parameetrid tuleb määrata juriidilise isiku kohta. Kuna igale juriidilisele isikule seadistatakse moodul eraldi, saab iga allettevõtte järgida kohalikke nõudeid ja äripraktikaid. Näiteks professionaalsete teenuste juriidilisel isikul ja tootmise juriidilisel isikul võivad olla erinevad mooduliparameetrid, isegi kui nad alluvad samale emaettevõttele. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Mooduliparameetrid on tootmisüksuste vahel ühiskasutuses. 

### <a name="data-security"></a>Andmeturve
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik    
Enamik andmeid on automaatselt ettevõtte ID-ga kaitstud. Ettevõtte ID on juriidilise isikuga seostatud andmete kordumatu identifikaator. Ettevõte võib olla seostatud ainult ühe juriidilise isikuga ja juriidiline isik võib olla seostatud ainult ühe ettevõttega. Kasutaja pääseb juurde ainult nende ettevõtete andmetele, millele tal on juurdepääs. Andmete kaitsmiseks ettevõtte ID-ga ei pea rakendust Finance and Operations kohandama. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Andmeid saab kaitsta tootmisüksuste kaupa, luues kohandatud andmeturbepoliitikad. Andmetele juurdepääsu piiramiseks kasutatakse andmeturbepoliitikaid. Näiteks oletame, et kasutajal on lubatud luua ainult kindla tootmisüksuse ostutellimusi. Et kasutaja ei pääseks juurde ühegi muu tootmisüksuse ostutellimuse andmetele, saab luua andmeturbepoliitikad. Kannete maht ja turbepoliitikate arv võib jõudlust mõjutada. Turbepoliitikate koostamisel tuleb jõudlust silmas pidada. 

### <a name="ledgers"></a>Pearaamatud
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik    
Iga juriidiline isik vajab pearaamatut, milles on kontoplaan, arvestusvaluuta, aruandlusvaluuta ja rahanduskalender. Bilansi saab koostada ainult juriidilisele isikule. Põhikontosid, dimensioone, konto struktuure, kontoplaane ja konto reegleid saab kasutada rohkem kui üks juriidiline isik.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Tootmisüksusel ei saa olla oma pearaamatuteavet. Kui teie siseorganisatsioonid ei nõua kordumatuid pearaamatuid, saate kasutada nende puhul tootmisüksuste mudelit. Pearaamatu teave seadistatakse hierarhia peamisele juriidilisele isikule. Kasumiaruannet saab luua juriidilise isiku tootmisüksustele või peamisele juriidilisele isikule. 

### <a name="fiscal-calendars"></a>Rahandussaasta kalendrid 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik    
Igal juriidilisel isikul on oma rahanduskalender. Kui teie siseorganisatsioonid kasutavad erinevaid rahandusaastaid ja rahanduskalendreid, peate kasutama nende organisatsioonide puhul juriidiliste isikute mudelit. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Tootmisüksustel peab olema ühine rahanduskalender. Kui teie siseorganisatsioonid saavad kasutada samu rahandusaastaid ja rahanduskalendreid, saate kasutada nende organisatsioonide puhul tootmisüksuste mudelit. 

### <a name="consolidation"></a>Konsolideerimine
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik    
Piirkondlike kontorite finantstulemused tuleb finantsaruannete koostamiseks konsolideerida ühte konsolideeritud ettevõttesse. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Konsolideerimine pole nõutav, kuna andmed on juba tootmisüksuste vahel ühiskasutuses. 

### <a name="centralized-payments"></a>Tsentraliseeritud maksed
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik 
Tsentraliseeritud maksed tuleb seadistada nii, et kõigi allüksuste juriidiliste isikute arveid saab maksta (või makseid vastu võtta) üks peamine juriidiline isik. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Tsentraliseeritud maksed pole nõutavad, kuna kõik arved kajastatakse ühe juriidilise isiku juures.

### <a name="intercompany-transactions"></a>Kontsernisisesed kanded
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik 
Kontsernisiseseid müügitellimusi, ostutellimusi, makseid või sissetulekuid saab üksteisele rakendada. Töölehekandeid ei pea kasutama. Saate vaadata kontsernisiseseid kandeid alammooduli tasandil (müügireskontro, ostureskontro). Järgmised näited illustreerivad kontsernisiseste kannete käsitsemist. 

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Näide 1: peakontor osutab piirkondlikele kontoritele teenuseid ja peab esitama nende teenuste kulude eest piirkondlikele kontoritele arve.
Kui piirkondliku kontori mudel on juriidiline isik, on teil järgmised võimalused. 
- Peakontor loob töölehekande piirkondlikule kontorile kulu eest arve esitamiseks. Kanded ei aegu.
- Peakontor saadab teenuste kohta piirkondlikule kontorile ostutellimuse. Juriidilises isikus luuakse piirkondlikule kontorile automaatselt kontsernisisese alammooduli kannetega müügitellimus. 

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Näide 2: peakontor ostab piirkondlikule kontorile osutatava teenuse ja maksab selle eest
Kui piirkondliku kontori mudel on juriidiline isik, on teil järgmised võimalused. 
- arve ja makse vastavad peakontori regulatiivsetele nõuetele. Peakontor saab luua töölehekande piirkondlikule kontorile kulu eest arve esitamiseks. Kanded ei aegu. 
- arve ja makse vastavad peakontori regulatiivsetele nõuetele. Peakontor saab luua kontsernisisese alammooduli kande.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Kontsernisiseseid kandeid tootmisüksuste vahel toetatakse ainult töölehekannete kaudu. Tootmisüksus ei saa sama juriidilise isiku teisele tootmisüksusele ostutellimust, müügitellimust ega arvet väljastada ega seda sellelt vastu võtta. Te ei saa vaadata kontsernisiseseid kandeid alammooduli tasandil (müügireskontro, ostureskontro). Järgmised näited illustreerivad kontsernisiseste kannete käsitsemist. 

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Näide 1: peakontor osutab piirkondlikele kontoritele teenuseid ja peab esitama nende teenuste kulude eest piirkondlikele kontoritele arve.
Kui piirkondliku kontori puhul kasutatakse tootmisüksuse mudelit, sisestab peakontor kulukande ja kodeerib selle piirkondlikule kontorile. 

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Näide 2: peakontor ostab piirkondlikule kontorile osutatava teenuse ja maksab selle eest.
Kui kasutate piirkondliku kontori puhul tootmisüksuse mudelit, järgivad arve ja makse peakontori regulatiivseid nõudeid. Arve saab kodeerida piirkondlikule kontorile. Kasutage kasumiaruandes piirkondliku kontori kulude kajastamiseks tasakaalustavat finantsdimensiooni.

### <a name="local-tax-requirements"></a>Kohalikud maksunõuded
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik
Juriidilisele isikule kehtivad juriidilise isiku registreerimise riigis/piirkonnas tegutseva maksuameti maksuseadused. Näiteks kehtivad Taanis registreeritud juriidilisele isikule Taani maksuseadused ja -eeskirjad. Finance and Operationsis võib juriidiline isik kuuluda ainult ühte riiki/piirkonda. Juriidilise isiku peamise aadressi jaoks valitud riik/piirkond juhib riigi-/piirkonnapõhiseid funktsioone, mis on selle juriidilise isiku jaoks saadaval. Näiteks kui juriidilise isiku peamine aadress on Taanis, muutuvad kättesaadavaks funktsioonid, mis on seotud Taani maksuseaduste ja -eeskirjadega. Seega, kui teie organisatsioonid on erinevates riikides/piirkondades ja nõuavad erinevaid kohalikke maksusuvandeid, tuleb need organisatsioonid seadistada eraldi juriidiliste isikutena.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Tootmisüksused kasutavad peamise juriidilise isiku riigi konteksti. Sama juriidilise isiku tootmisüksustel ei saa olla erinevad riigi-/piirkonnapõhised nõuded. Kui teie organisatsioonid on samas riigis/piirkonnas ja kasutavad samu maksusuvandeid, saate seadistada need tootmisüksustena.


### <a name="statutory-reporting-for-a-countryregion"></a>Riigi/piirkonna seaduslik aruandlus 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik
Riikide/piirkondade puhul, mida Finance and Operations toetab, saab koostada enamikku seaduslikke aruandeid. Teavet selle kohta, millised aruanded iga riigi/piirkonna puhul saadaval on, leiate rakenduse Finance and Operations [Microsoft Dynamicsi lokaliseerimisportaalist](https://mbs.microsoft.com/customersource/global/ax/support/support-news/GFMLocalizationPortalMC). (Nõutav on CustomerSource’i sisselogimine.) 

> [!Note]
> Rakenduse Finance and Operations pearaamatu sisestamiskiht võimaldab teha korrigeerimiskirjeid emaettevõttele, mis kasutab tütarettevõttest erinevat raamatupidamisstandardit. Näiteks ettevõtte puhul, mis kasutab Ühendkuningriigis üldiselt aktsepteeritud raamatupidamispõhimõtteid (UK GAAP), saate teha korrigeerimiskirjeid sisestamiskihis. Need kirjed saab konsolideerida emaettevõttesse, mis kasutab Ameerika Ühendriikides üldiselt aktsepteeritud raamatupidamispõhimõtteid (GAAP). Korrigeerimiskirjed ei mõjuta UK GAAP aruandlust.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Kohustuslikud aruanded tuleb luua teise rakenduse abil. Peate veenduma, et andmed hõivatakse rakenduses Finance and Operations iga tootmisüksuse nõuete kohaselt, kui need peakontori nõuetest erinevad. 

### <a name="currency"></a>Valuuta
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik
Kui teie organisatsioonid peavad kasutama erinevaid tegevusvaluutasid, peate kasutama nende organisatsioonide puhul juriidiliste isikute mudelit. Funktsionaalsed valuutad seadistatakse juriidilise isiku kohta. Kuid saate sisestada kandeid ka mitmes valuutas. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Kui teie organisatsioonid võivad kasutada ühte tegevusvaluutat, saate kasutada organisatsioonide puhul tootmisüksuste mudelit. Tootmisüksustel peab olema ühine tegevusvaluuta. Kuid saate sisestada kandeid ja koostada aruandeid ka mitmes valuutas. 


### <a name="year-end-closing"></a>Rahandusaasta sulgemine
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik
Kui seadused ja raamatupidamistavad teie organisatsioonide asukohariikides/-piirkondades erinevad, võib olla vaja organisatsioonide puhul erinevaid rahandusaasta lõpetamise protseduure. See tähendab, et peate kasutama organisatsioonide puhul juriidiliste isikute mudelit. Igal juriidilisel isikul on oma aastalõpu protseduurid. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Kui seadused ja raamatupidamistavad teie organisatsioonide asukohariikides/-piirkondades on samad, võite kasutada ühesuguseid rahandusaasta lõpetamise protseduure. See tähendab, et saate kasutada organisatsioonide puhul tootmisüksuste mudelit. Kõik tootmisüksused peavad kasutama sama rahandusaasta sulgemise protseduuri. 
   
### <a name="number-sequences"></a>Numbriseeriad
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik
Mõne viite numbriseeriad saab seadistada juriidilise isiku kohta. Mõningaid numbriseeriaid saab kasutada ühiselt. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Mõne viite numbriseeriad saab seadistada tootmisüksuse kohta. Mõningaid numbriseeriaid saab kasutada ühiselt.

### <a name="products"></a>Tooted 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik
Tootedefinitsioonid on ühiskasutuses ja need tuleb väljastada üksikutele juriidilistele isikutele, enne kui neid saab kannetesse lisada. Igal juriidilisel isikul on oma väljastatud toodete komplekt, mille saab kandedokumentidesse kaasata. Kui teie siseorganisatsioonid peavad kasutama erinevaid tootekomplekte, peate kasutama nende organisatsioonide puhul juriidiliste isikute mudelit. 

> [!Note]
> Kuigi tootedefinitsioonid on ühiskasutuses, saate iga juriidilise isiku puhul, millele toode on väljastatud, määrata kaubale igas varude asukohas erinevad müügi, ostu ja ladustamise parameetrid. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Kõik tootmisüksused kasutavad sama tootekomplekti. Kui teie siseorganisatsioonid saavad kasutada sama tootekomplekti, saate kasutada nende organisatsioonide puhul tootmisüksuste mudelit. 

### <a name="inquiry-and-reporting"></a>Päringud ja aruandlus  
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Kui organisatsiooni mudel on juriidiline isik
Mitmes juriidilises isikus kannete sisestamiseks ja päringute tegemiseks peate ettevõtteid käsitsi vahetama. Andmeturbe piiride tõttu võib konsolideeritud päringute tegemine ja aruandlus olla ressursimahukas ja aeganõudev. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Kui organisatsiooni mudel on tootmisüksus 
Mitmest tootmisüksusest andmetele juurde pääsemiseks pole vaja ettevõtteid vahetada. Konsolideeritud päringute esitamine ja aruandlus ning üksiku piirkondliku päringu esitamine on lihtsam ja kiirem.

## <a name="best-practices-for-modeling-organizations-and-hierarchies"></a>Organisatsioonide ja hierarhiate mudelite loomise parimad praktikad
Arvestage organisatsiooni hierarhia juurutamisel järgmisi parimaid praktikaid.
-   Looge osakond juriidilise isiku ja äriüksuse vahelise ühisosa mudeli loomiseks. Seejärel saate koondada osakonna andmed kohustusliku aruandluse jaoks juriidilise isiku alla ja kontsernisiseseks aruandluseks äriüksuse alla. Osakonnad võivad toimida tulukeskustena. Osakondade kasutamisel pole vaja kasutada kontostruktuuris dimensioonidena juriidilisi isikuid ja äriüksusi. Võite kasutada dimensioonina lihtsalt osakondi. Kuid kui kulukeskusi kasutatakse ainult kulude koondamiseks ja osakondi tulu näitamiseks, tuleb kasutada kontostruktuuris dimensioonidena nii kulukeskusi kui ka osakondi.
-   Kui teil on kasumi ja kahjumi kajastamiseks keerukad nõuded, siis kasutage tootmisüksuste mudelis mitut hierarhiat.
-   Ärge kasutage ühe juriidilise isiku puhul samal hierarhia eesmärgil mitut hierarhiat.
-   Ärge looge hierarhiat iga eesmärgi jaoks. Tavaliselt saab ühte hierarhiat kasutada mitmel eesmärgil. Näiteks saab ühe tootmisüksuste hierarhia määrata kõigile poliitikaga seotud eesmärkidele.
-   Tasakaalustatud hierarhiate loomine. Hierarhias määratletakse kõik juursõlmest ühel kaugusel olevad sõlmed tasemena. Tasakaalustatud hierarhias saab igal tasemel olla ainult ühte tüüpi tootmisüksus ja kaugus juursõlmest iga tasemeni on ühesugune. Kui osakonna ja juriidilise isiku või äriüksuse vahel on vahepealseid tasemeid, võivad tasakaalustatud hierarhia loomiseks olla vajalikud kohatäiteorganisatsioonid.
-   Ärge kasutage eraldi tootmisüksuste hierarhiat, kui juriidiliste isikute struktuur on ka teie tegevusstruktuur. Juriidiliste isikute ja tootmisüksuste segahierarhia võib täita mõlemat eesmärki.
-   Enne suuremate ümberstruktureerimise stsenaariumide mudeli kasutuselevõttu kasutage hierarhia kehtivuskuupäevi mõju analüüsi ja kontrolltesti sooritamiseks.
-   Kasutage mustandirežiimi hierarhia muutmiseks enne tootmiskeskkonnas uue versiooni avaldamist.
-   Piirake inimeste arvu, kes tohivad organisatsioone tootmiskeskkonnas hierarhiasse lisada või neid sealt eemaldada. Väiksem arv vähendab kulukate eksimuste tekkimise ohtu ja vajadust paranduste järele.

