---
title: Protsessid ja operatsioonid
description: "See teema annab teavet protsesside ja operatsioonide kohta. Protsess määratleb toote või tootevariandi tootmise protsessi. See kirjeldab tootmisprotsessi iga etappi (operatsiooni) ja nende etappide läbimise järjekorda. Iga etapi puhul määratleb protsess ka vajalikud operatsiooniressursid, vajaliku seadistamise aja ja käitusaja ning kulu arvutamise viisi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 556b9859d0b162b11f0bcbfc6552f6fd9a900596
ms.lasthandoff: 03/31/2017


---

# <a name="routes-and-operations"></a>Protsessid ja operatsioonid

[!include[banner](../includes/banner.md)]


See teema annab teavet protsesside ja operatsioonide kohta. Protsess määratleb toote või tootevariandi tootmise protsessi. See kirjeldab tootmisprotsessi iga etappi (operatsiooni) ja nende etappide läbimise järjekorda. Iga etapi puhul määratleb protsess ka vajalikud operatsiooniressursid, vajaliku seadistamise aja ja käitusaja ning kulu arvutamise viisi.

<a name="overview"></a>Ülevaade
--------

Protsess kirjeldab operatsioonide järjekorda, mis on toote või tootevariandi tootmiseks vajalik. Iga operatsiooni puhul määratleb protsess ka vajalikud operatsiooniressursid, operatsiooni seadistamiseks ja sooritamiseks vajaliku aja ja kulu arvutamise viisi. Sama protsessi saab kasutada mitme toote tootmiseks või määratleda iga toote või tootevariandi jaoks kordumatu protsessi. Ka sama toote jaoks võib olla mitu protsessi. Sellisel juhul on kasutatav protsess erinev, olenevalt teguritest nagu toodetav kogus. Rakenduse Microsoft Dynamics 365 for Operations protsessi määratlus koosneb neljast eraldi elemendist, mis kirjeldavad üheskoos tootmisprotsessi.

-   **Protsess** – protsess määratleb tootmisprotsessi struktuuri. Teisisõnu määratleb see operatsioonide järjekorra.
-   **Operatsioon** – operatsioon tähistab protsessi nimelist etappi, nt **Koostamine**. Sama operatsioon võib toimuda mitmes protsessis ja sellel võivad olla erinevad operatsiooni numbrid.
-   **Operatsiooni seos** – operatsiooni seos määratleb operatsiooni tööatribuudid nagu seadistusaja ja käitusaja, kulukategooriad, tarbimisparameetrid ja ressursivajadused. Operatsiooni seos võimaldab erinevaid operatsiooni tööatribuute, olenevalt protsessist, mille alusel operatsiooni kasutatakse, või valmistatavatest toodetest.
-   **Protsessi versioon** – protsessi versioon määratleb protsessi, mida toote või tootevariandi valmistamiseks kasutatakse. Protsessiversioonid võimaldavad protsesside uuesti kasutamist toodete lõikes või nende muutmist aja jooksul. Samuti võimaldavad need erinevate protsesside kasutamist sama toote valmistamiseks. Sellisel juhul oleneb kasutatav protsess teguritest nagu asukoht või toodetav kogus.

## <a name="routes"></a>Protsessid
Protsess kirjeldab operatsioonide järjekorda, mida toote või tootevariandi tootmiseks kasutatakse. Igale operatsioonile määratakse operatsiooni number ja järgnev operatsioon. Operatsioonide järjekord moodustab protsessivõrgu, mida saab kujutada juhitud diagrammiga, millel on vähemalt üks alguspunkt ja üks lõpp-punkt. Dynamics 365 for Operationsis eristatakse protsesse struktuuri tüübi põhjal. Kaks protsessitüüpi on lihtsad protsessid ja protsessivõrgud. Tootmise juhtimise parameetrites saate määrata, kas kasutada saab ainult lihtsaid protsesse või keerukamais protsessivõrke.

### <a name="simple-routes"></a>Lihtsad protsessid

Lihtne protsess on järjestikune ja protsessil on ainult üks alguspunkt.  

[![Lihtne protsess](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Kui aktiveerite tootmise juhtimise parameetrites ainult lihtsad protsessid, loob Dynamics 365 for Operations automaatselt operatsioonide numbrid (10, 20, 30 jne), kui protsessi määratlete.

### <a name="route-networks"></a>Protsessivõrgud

Kui aktiveerite tootmise juhtimise parameetrites keerukamad protsessivõrgud, saate määratleda protsessid, millel on mitu lähtepunkti ja toimingut, mis võivad töötada paralleelselt.  

[![Protsessivõrk](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Märkused.**

-   Igal operatsioonil võib olla ainult üks järglasoperatsioon ja kogu protsess peab lõppema ühe operatsiooniga.
-   Pole mingit garantiid, et mitu operatsiooni, millel on sama järglasoperatsioon (nt operatsioonid 30 ja 40 eelmisel illustratsioonil) töötaksid tegelikult paralleelselt. Operatsioonide plaanimisele võib seada piirangud ressursside saadavus ja maht.
-   Operatsiooni numbrina ei saa kasutada numbrit 0 (null). See number on reserveeritud ja seda kasutatakse määramiseks, et protsessi viimasel operatsioonil ei ole järglasoperatsiooni.

### <a name="parallel-operations"></a>Paralleelsed operatsioonid

Mõnikord on vaja operatsiooni sooritamiseks mitme erinevate omadustega operatsiooniressursi kombinatsiooni. Näiteks võib koostamisoperatsioon nõuda masinat, tööriista ja ühte töötajat iga kahe masina kohta, kes operatsiooni kontrolliks. Seda näidet saab modelleerida, kasutades paralleelseid operatsioone, kus üks operatsioon on mõeldud esmaseks operatsiooniks ja teised on teisesed.  

[![Protsess, millel on esmane ja teisesed operatsioonid](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Tavaliselt on kujutab esmane operatsioon endast kitsaskohana toimivat ressurssi ja dikteerib teiseste operatsioonide käitusaja. Kuid plaanimise ajal, mis hõlmab piiratud võimsust, peavad ressursid, mis on plaanitud nii esmase operatsiooni kui ka teiseste operatsioonide jaoks, olema kättesaadavad ja neil peab olema samal ajal vaba mahtu.  

Nii esmasel operatsioonil kui ka teisestel operatsioonidel peab olema sama operatsiooni number (30 eelmisel illustratsioonil).  

Eelnevas näites on esmase operatsiooni (30) ressursivajadus masin, samas kui teiseste operatsioonide (30' ja 30'') ressursivajadused on tööriist ja töötaja. Viiekümne protsendi suurune koormus aitab garanteerida, et plaanitud töötaja suudab korraga kahte masinat kontrollida.

### <a name="approval-of-routes"></a>Protsesside kinnitamine

Enne, kui protsessi plaanimises või tootmisprotsessis kasutada saab, tuleb see kinnitada. Kinnitamine näitab, et protsessi kujundamine on lõpetatud. Samal väljastatud tootel või väljastatud tootevariandil võib olla mitu kinnitatud protsessi. Tavaliselt kinnitatakse protsess või valem siis, kui kinnitatakse esimene vastav protsessi versioon. Kuid mõne äristsenaariumi puhul on protsessi ja protsessi versiooni kinnitamine erinevad tegevused, mis võivad hõlmata erinevaid protsessiomanikke.  

Iga protsessi saab eraldi kinnitada või sellelt kinnituse eemaldada. Kuid kui protsess on kinnitamata, on kinnitamata ka kõik seotud protsessiversioonid. Tootmise juhtimise parameetrites saate määrata, kas protsesside kinnitust saab eemaldada ja kas kinnitatud protsesse saab muuta.  

Kui teil on vaja säilitada logi, milles salvestatakse iga protsessi kinnitaja, võite nõuda protsessi kinnitamiseks digitaalallkirja. Siis peavad kasutajad kinnitama oma isiku, kasutades [digitaalallkirja](/dynamics365/operations/organization-administration/electronic-signature-overview).

## <a name="operations"></a>Toimingud
Operatsioon on tootmisprotsessi etapp. Dynamics 365 for Operationsis on igal operatsioonil ID ja lihtne kirjeldus. Järgmistes tabelites on toodud tüüpilised töökojaoperatsioonide näited.

| Toiming  | Kirjeldus        |
|------------|--------------------|
| PipeCut    | Torude lõikamine       |
| TIGweld    | TIG keevitamine        |
| JigAssy    | Rakiste koostamine       |
| Kontroll | Kvaliteedikontroll |

Operatsiooni tööatribuudid, nagu seadistusaeg ja käitusaeg, ressursivajadused, kuluarvestuse andmed ja tarbimise arvestus, määratakse operatsiooni seoses. (Lisateavet operatsiooni seoste kohta leiate järgmisest jaotisest.)

## <a name="operation-relations"></a>Toimingu seosed
Operatsiooni seoses hallatakse järgmisi operatsiooni tööatribuute.

-   Kulukategooriad
-   Tarbimisparameetrid
-   Töötlemisajad
-   Töötlemiskogused
-   Ressursi nõuded
-   Märkmed ja juhised

Samale operatsioonile saab määratleda mitu operatsiooni seost. Kuid iga operatsiooni seos on ühe operatsiooni põhine ja selles talletatakse atribuudid, mis on protsessi, väljastatud toote või kaubagrupiga seotud väljastatud toodete kogumi põhised. Seega saab sama operatsiooni kasutada mitmes protsessis, millel on erinevad tööatribuudid. Lisaks saab koondandmeid hõlpsamini hallata, kui kasutada standardoperatsioone, millel on samad tööatribuudid, olenemata kasutatavast protsessist ja valmistatavast tootest. Operatsiooni seose ulatus määratletakse atribuutide **Kaubakood**, **Kauba seos**, **Protsessi kood** ja **Protsessi seos** kaudu, nagu on näidatud järgmises tabelis.

| Kauba kood | Kauba seos         | Protsessi kood | Protsessi seos   | Operatsiooni seose ulatus                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabel     | &lt;Kauba ID&gt;       | Protsess      | &lt;Marsruudi ID&gt; | Operatsiooni tööatribuudid, kui seda kasutatakse protsessis, kus **Protsessi number**=&lt;protsessi ID&gt;, et valmistada väljastatud toode, kus **Kaubakood**=&lt;kauba ID&gt;.                                                                                                                        |
| Tabel     | &lt;Kauba ID&gt;       | Kõik        |                  | Operatsiooni vaike-tööatribuudid, kui seda kasutatakse väljastatud toote valmistamiseks, kus **Kaubakood**=&lt;kauba ID&gt;. Teisisõnu, need tööatribuudid rakenduvad siis, kui väljastatud tootel puudub protsessipõhine operatsiooni seos.                                     |
| Grupeeri     | &lt;Kaubagrupi ID&gt; | Protsess      | &lt;Marsruudi ID&gt; | Operatsiooni tööatribuudid, kui seda kasutatakse protsessis, kus **Protsessi number**=&lt;protsessi ID&gt; väljastatud toodete valmistamiseks, mis on seotud kaubagrupiga &lt;kaubagrupi ID&gt;, kui väljastatud tootel puudub protsessipõhine operatsiooni seos.                         |
| Grupeeri     | &lt;Kaubagrupi ID&gt; | Kõik        |                  | Operatsiooni vaike-tööatribuudid, kui seda kasutatakse väljastatud toodete valmistamiseks, mis on seotud kaubagrupiga &lt;kaubagrupi ID&gt;, kui puudub konkreetsem operatsiooni seos.                                                                                                  |
| Kõik       |                       | Protsess      | &lt;Marsruudi ID&gt; | Operatsiooni vaike-tööatribuudid, kui seda kasutatakse protsessis, kus **Protsessi kood**=&lt;protsessi ID&gt;. Teisisõnu, need tööatribuudid rakenduvad siis, kui sellel protsessil puudub operatsiooni seos, mis oleks väljastatud toote või sellega seotud kaubagrupi põhine. |
| Kõik       |                       | Kõik        |                  | Operatsiooni vaike-tööatribuudid. Need tööatribuudid rakenduvad siis, kui konkreetsemat operatsiooni seost pole.                                                                                                                                                                |

Samuti saate määrata, et operatsiooni seos on asukohapõhine. Sel viisil võivad operatsiooni tööatribuudid olla erinevad, olenevalt asukohast, kus operatsiooni tehakse. Konfigureeritud toodete puhul saate samuti määrata iga tootekonfiguratsiooni jaoks erinevad tööatribuudid.  

Operatsiooni seosed annavad protsesside määratlemisel palju paindlikkust. Lisaks aitab vaikeatribuutide määratlemise võimalus vähendada koondandmete hulka, mida tuleb hallata. Kuid see paindlikkus tähendab ka seda, et peate olema teadlik kontekstist, milles operatsiooni seost muudate.  

**Märkus.** Kuna operatsiooni atribuudid on salvestatud operatsiooni seostesse operatsiooni ja protsessi kohta, on kõigil sama operatsiooni juhtumitel (nt Koostamine) sama seadistusaeg, käitusaeg, ressursivajadused jne. Seega kui kaks operatsiooni juhtumit peavad toimuma samas protsessis, kuid olema erineva käitusajaga, siis tuleb luua kaks eraldi operatsiooni, nt Koostamine1 ja Koostamine2.

### <a name="modifying-product-specific-routes"></a>Tootepõhiste protsesside muutmine

Kui avate lehe **Protsess** lehelt **Väljastatud toote üksikasjad**, siis kuvatakse valitud väljastatud tootega seotud protsessiversioonid. Selles kontekstis näitab Dynamics 365 for Operations operatsiooni atribuudid sellest operatsiooni seosest, mis protsessi versiooniga kõige paremini sobib. Märkate, et operatsioonide loendis on atribuudid **Kaubakood** ja **Protsessi kood** operatsiooni seosest. Seega saate määrata, millist operatsiooni seost näidatakse.  

Lehel **Protsess** saate muuta operatsiooni tööatribuute, nt käitusaega või kulukategooriaid. Teie muudatused salvestatakse operatsiooni seosesse, mis põhinevad protsessil ja väljastatud tootel, millele selles protsessiversioonis viidatakse. Kui kuvatud operatsiooni seos ei põhine protsessil ja väljastatud tootel, siis teeb süsteem enne muudatuste salvestamist operatsiooni seosest koopia. See koopia *on* protsessi ja väljastatud toote põhine. Seega ei mõjuta teie muudatused teisi protsesse või väljastatud tooteid. Kontrollimiseks, millist operatsiooni seost lehel **Protsess** muudetakse, vaadake välju **Kaubakood** ja **Protsessi kood**.  

Saate luua ka käsitsi operatsiooni, mis on protsessi ja väljastatud toote põhine, kasutades funktsiooni **Seose kopeerimine ja redigeerimine**.  

**Märkus.** Kui lisate lehel **Protsess** protsessile uue operatsiooni, luuakse operatsiooni seos ainult praegusele väljastatud tootele. Seega kui protsessi kasutatakse ka teiste väljastatud toodete valmistamiseks, siis puudub nende väljastatud toodete jaoks kehtiv operatsioon ja protsessi ei saa enam nende väljastatud toodete jaoks kasutada.

### <a name="maintaining-operation-relations-per-route"></a>Operatsiooni seoste haldamine protsessi kohta

Kui avate lehe **Protsessi üksikasjad** loendilehelt **Protsessid**, kuvatakse kõigile protsessile kehtivate operatsiooni seoste loend. Seega saate hõlpsasti kontrollida, milliseid operatsiooni atribuute milliste toodete jaoks kasutatakse. Saate muuta nii vaikeatribuutide väärtusi kui ka tootepõhiseid atribuudiväärtusi.  

Kui lisate lehele **Protsessi üksikasjad** uue operatsiooni seose, määratakse väljale **Protsessi kood** automaatselt väärtus **Protsess** ja väljale **Protsessi seos** määratakse praeguse protsessi number.

### <a name="maintaining-operation-relations-per-operation"></a>Operatsiooni seoste haldamine operatsiooni kohta

Lehelt **Operatsioonid** saab avada lehe **Operatsiooni seosed**. Sellel lehel saate muuta kõiki konkreetse operatsiooni seoseid. Muuta saab isegi vaikeväärtusi sisaldavaid operatsiooni seoseid.  

Kui teie ettevõte kasutab standardoperatsioone ning kui tööparameetrid on kõigi toodete ja protsesside puhul samad, pakub leht **Operatsiooni seosed** mugavat võimalust nende operatsioonide vaike-tööparameetrite haldamiseks.

### <a name="applying-operation-relations"></a>Operatsiooni seoste rakendamine

Mõnikord peab Dynamics 365 for Operations operatsiooni jaoks tööatribuudid leidma. Näiteks ostutellimuse loomisel tuleb iga operatsiooni atribuudid kopeerida operatsiooni seostest tootmisprotsessiga. Nendes olukordades otsib Dynamics 365 for Operations vastavaid operatsiooni seoseid kõige konkreetsemast kombinatsioonist kõige vähem konkreetse kombinatsiooni suunas.  

Kui Dynamics 365 for Operations otsib väljastatud toote jaoks kõige asjakohasemat operatsiooni seost, eelistatakse operatsiooni seost, mis sobitab väljastatud toote kauba ID, operatsiooni seosele, mis sobitab kaubagrupi ID. Operatsiooni seost, mis vastab kaubagrupi ID-le, eelistatakse omakorda operatsiooni vaikeseosele. Otsimine toimub järgmises järjekorras.

1.  **Kaubakood**=**Tabel** ja **Kauba seos**=&lt;kauba ID&gt;
2.  **Kaubakood**=**Grupp** ja **Kauba seos**=&lt;kaubagrupi ID&gt;
3.  **Kaubakood**=**Kõik**
4.  **Protsessi kood**=**Protsess** ja **Protsessi seos**=&lt;protsessi ID&gt;
5.  **Protsessi kood**=**Kõik**
6.  **Konfiguratsioon**=&lt;konfiguratsiooni ID&gt;
7.  **Konfiguratsioon**=
8.  **Tegevuskoht**=&lt;tegevuskoha ID&gt;
9.  **Tegevuskoht**=

Seega tuleks operatsiooni kasutada iga protsessi puhul ainult üks kord. Kui operatsioon toimub samas protsessis mitu korda, on kõigil selle operatsiooni juhtumitel sama operatsiooni seos ja pole võimalik määrata igale juhtumile erinevaid atribuute (nt käitusaegu).

## <a name="route-versions"></a>Protsessi versioonid
Protsessiversioone kasutatakse toodete tootmisel tekkivate erinevuste säilitamiseks või tootmisprotsessi suurema juhtimise võimaldamiseks. Need määratlevad, millist protsessi peaks konkreetse väljastatud toote või väljastatud tootevariandi valmistamisel kasutama. Väljastatud tootele protsessi määratlemisel võib kasutada järgmisi piiranguid.

-   Tootedimensioonid (suurus, värv, stiil või konfiguratsioon)
-   Tootmiskogus
-   Tootmiskoht
-   Tootmise kuupäev

Kui valmistate toodet konkreetses tegevuskohas, konkreetses koguses või konkreetsel perioodil, võite määrata konkreetse protsessiversiooni protsessi vaikeversiooniks. Kuid pange tähele, et antud väljastatud tootele ja antud piirangute kogumile on lubatud ainult üks aktiivne protsess.  

Tootmise juhtimise parameetrites saate nõuda, et alati määrataks protsessi versiooni kehtivusperiood.

### <a name="approval-of-route-versions"></a>Protsessiversioonide kinnitamine

Enne, kui protsessiversiooni plaanimises või tootmisprotsessis kasutada saab, tuleb see kinnitada. Protsessiversiooni kinnitamisel võite kinnitada ka seotud protsessi. Kuid pange tähele, et protsessiversiooni saab kinnitada ainult juhul, kui kinnitatakse ka seotud protsess.

### <a name="activating-the-default-route-version"></a>Protsessi vaikeversiooni aktiveerimine

Kui protsessiversiooni aktiveerite, määrate selle protsessi vaikeversiooniks, mida kasutatakse koondplaneerimises või tootmistellimuste loomiseks. Antud piirangute kogumi (nt periood, laoala või kogus) kohta võib olla ainult üks aktiivne protsessiversioon. Kui versioon, mida püüate aktiveerida, satub konflikti juba aktiivse versiooniga, saate tõrketeate. Mitmetähendusliku aktiveerimise vältimiseks tuleb konflikti põhjustav versioon inaktiveerida või muuta protsessiversiooni piiranguid (tavaliselt perioodi).

### <a name="electronic-signatures"></a>Digitaalallkirjad

Kui teil on vaja säilitada logi, milles salvestatakse iga protsessiversiooni kinnitaja ja aktiveerija, võite nõuda nende toimingute jaoks digitaalallkirja. Siis peavad protsessiversioone kinnitavad ja aktiveerivad kasutajad kinnitama oma isiku, kasutades [digitaalallkirja](/dynamics365/operations/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Juhtumihaldust kasutav toote muutmine

Toote muutmise juhtum uute või muudetud protsesside ja protsessiversioonide kinnitamiseks ja aktiveerimiseks annab lihtsa võimaluse protsessiversiooni piirangute ülevaate kuvamiseks. Saate kinnitada ja aktiveerida ka kõiki protsesse, mis on seotud konkreetse muudatusega ühes operatsioonis, ja dokumenteerida tulemused toote muutmise juhtumis.

## <a name="maintaining-routes"></a>Protsesside haldamine
Olenevalt ettevõtte vajadustest võib teil olla võimalik protsessidefinitsioonide haldamisele kuuluvat pingutust vähendada.

### <a name="making-routes-independent-of-resources"></a>Protsesside sõltumatuks muutmine ressurssidest

Paljudes süsteemides tuleb protsessis määrata operatsiooniressurss või ressursigrupp, mis operatsiooni peaks läbi viima. Kuid Dynamics 365 for Operationsis saate määrata nõuete kogumi, millele operatsiooniressurss peab vastama, et seda saaks operatsioonis kasutada. Seetõttu ei tule konkreetset operatsiooniressurssi või ressursigruppi, mida peaks kasutama, määrata enne operatsiooni tegelikku plaanimist. See funktsioon on eriti kasulik, kui teil on palju töötajaid või masinaid, kes/mis saavad sama operatsiooni teha.  

Näiteks võite määrata, et operatsioon nõuab operatsiooniressurssi tüübiga **Masin**, mille võime **Stantsimine** on 20 tonni. Siis lahendab plaanimismootor need nõuded konkreetse operatsiooniressursi või ressursigrupi abil operatsiooni plaanimisel. Kuna teil on võimalus määrata ainult need nõuded, selle asemel et siduda operatsioon konkreetse masinaga, on teil palju rohkem paindlikkust. Lisaks on haldamine lihtsam, kui ressursse teisaldatakse või lisandub uusi ressursse.  

Lisateavet mitmesugust tüüpi ressursivajaduste ja nende kasutamise kohta leiate jaotistest Operatsiooni ressursivajadused ja [Ressursi võimalused](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Protsesside ühiskasutus tegevuskohtade lõikes

Kui valmistate sama toodet mitmes tootmiskohas ja kui toote valmistamise etapid on kõigis tootmiskohtades samad, siis võite sageli koostada ühise protsessi, mida kasutatakse kõigis tootmiskohtades. Ühise protsessi koostamiseks ärge määrake protsessis tegevuskohta. Kuid peate siiski looma protsessiversiooni, mis seostab ühise protsessi tootega igas tegevuskohas.  

Samuti peate veenduma, et protsessi iga operatsiooni ressursivajadused ei nõuaks konkreetseid operatsiooniressursse või ressursigruppe, vaid selle asemel väljendatakse neid vajalike ressursside omaduste kaudu. Siis saab plaanimismootor määrata sobivad operatsiooniressursid tegevuskohast, kus tootmine on plaanitud. Näiteks kui käitusajas on väikesed erinevused või kui teatud operatsiooni seadistusaeg on tegevuskohapõhine, saate määrata need andmed, lisades sellele tegevuskohale täiendava operatsiooni seose.  

Ühiste protsesside eeliste täiel määral kasutamiseks tuleks kasutada ka ressursside tarbimist vastaval kooslusel. Kui määrate koosluse real ressursitarbimise lipu, siis tuletatakse ladu ja koht, kust toormaterjale tuleks tarbida, operatsiooniressursist, millele operatsioon on plaanitud. Seetõttu ei tule ladu ja asukohta määrata enne tootmise tegelikku plaanimist. Sel viisil saate muuta nii koosluse kui ka protsessi sõltumatuks füüsilisest asukohast, kus toodet valmistatakse.

### <a name="standard-operation-relations"></a>Standardsed operatsiooniseosed

Kui teie ettevõte kasutab tootmises standarditud operatsioone ja kui seadistusajas, käitusajas, tarbimise arvutuses, kuluarvestuses jne on erinevused väikesed või puuduvad, siis võib olla abiks operatsiooni vaikeseoste loomine kõigile operatsioonidele. Sellisel juhul vältige protsessi- või väljastatud toote põhiste operatsiooniseoste loomist.  

Kui väljendate ka ressursivajadusi oskuste ja võimaluste näol ning muudate protsessid tegevuskohast sõltumatuks, võite aidata hoida äriprotsesside jooksva haldamise minimaalsena.  

Selle lähenemise kasutamisel muutub leht **Operatsiooniseosed** käitusaegade ja muude atribuutide haldamisel teie peamiseks sihtkohaks.

### <a name="resource-specific-process-times"></a>Ressursipõhised protsessiajad

Kui te operatsiooni ressursivajaduste hulgas operatsiooniressurssi või ressursigruppi ei määra, võivad vastavad ressursid tegutseda erineva kiirusega. Seega võib aeg, mida on operatsiooni töötlemiseks vaja, erinev olla. Selle probleemi lahendamiseks võib kasutada operatsiooni seose välja **Valem** määramiseks, kuidas protsessi aega arvutatakse. Valikud on järgmised:

-   **Standardne** – (vaikevalik) arvutus kasutab ainult operatsiooniseose välju ja korrutab määratud käitusaja tellimuse kogusega.
-   **Maht** – arvutus sisaldab operatsiooniressursi välja **Maht**. Seega on aeg ressursist sõltuv. Operatsiooniressursi juures määratud väärtus on maht tunni kohta. See väärtus korrutatakse tellimuse koguse ja operatsiooni seose väärtusega **Tegur**.
-   **Partii** – partii maht arvutatakse operatsiooni seose teabe abil. Siis saab arvutada tellimuse koguse põhjal partiide arvu ja protsessi aja.
-   **Ressursi partii** – see valik on põhimõtteliselt sama, mis valik **Partii**. Kuid arvutus sisaldab operatsiooniressursi välja **Partii maht**. Seega on aeg ressursist sõltuv.


<a name="see-also"></a>Vt ka
--------

[Kooslused ja valemid](bill-of-material-bom.md)

[Tootmisprotsessis kasutatud kulukategooriad](../cost-management/cost-categories-used-production-routings.md)

[Ressursi võimalused](resource-capabilities.md)

[Digitaalallkirja ülevaade](/dynamics365/operations/organization-administration/electronic-signature-overview)



