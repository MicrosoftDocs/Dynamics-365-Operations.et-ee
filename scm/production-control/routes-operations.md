---
title: Protsesside ja toimingute
description: "See teema pakub teavet protsesside ja operatsioonide. Marsruudi määratleb toote või toote variante tootmist. Selles kirjeldatakse tootmisprotsessi ja selleks, et neid samme tuleb teha iga samm (tegevus). Iga etapi protsessi määratleb vajalikud toimingud ressursid, nõutav Seadistusaeg ja Käitusaeg, ja kuidas kulusid arvutatakse."
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

# <a name="routes-and-operations"></a>Protsesside ja toimingute

See teema pakub teavet protsesside ja operatsioonide. Marsruudi määratleb toote või toote variante tootmist. Selles kirjeldatakse tootmisprotsessi ja selleks, et neid samme tuleb teha iga samm (tegevus). Iga etapi protsessi määratleb vajalikud toimingud ressursid, nõutav Seadistusaeg ja Käitusaeg, ja kuidas kulusid arvutatakse.

<a name="overview"></a>Ülevaade
--------

Marsruudi kirjeldatakse tekitamiseks toote või toote variante kuluvat toimingute järjekorda. Iga tegevuse jaoks protsessi määratleb operatsioonide ressursse, mis on vajalikud, et määratleda ja täita operatsiooni ja kuidas kulusid arvutatakse kuluvat aega. Kasutage samal liinil toota mitut toodet, või määratleda unikaalse marsruudi iga toote või toote variant. Sul võib olla isegi mitme marsruudi ühe toote kohta. Sel juhul erinev marsruut, mida kasutatakse sõltuvalt toodetava koguse. Marsruudi Microsoft Dynamics 365 toimingute määratlus hõlmab nelja eraldi elemente, mis koos, kirjeldada tootmisprotsessi:

-   **Marsruudi** – marsruudi määratleb tootmisprotsessi struktuuri. Teisisõnu määratleb operatsioonide järjekorra.
-   **Operatsiooni** – operatsiooni tuvastab nimega samm marsruudi, nagu **komplekti**. Sama operatsiooni võib esineda mitme marsruudi ja võib olla eri operatsioonide numbrid.
-   **Operatsiooni seos** – operatsiooni seos määratleb tegevuse atribuutide operatsioonist, nagu näiteks Seadistusaeg ja Käitusaeg, kategooriad, tarbimise parameetrite ja ressursivajaduse. Operatsiooni seos võimaldab tegevuse atribuutide operatsiooni erinevad sõltuvalt operatsiooni kasutatakse protsessi või tooteid, mis on toodetud.
-   **Protsessi versioon** – protsessiversioon määratleb marsruut, mida kasutatakse toote või toote variante. Protsessi versioonid võimaldavad taaskasutada tooteid või muuta aja jooksul liinidel. Need lubavad ka sama toote tootmiseks kasutatava teistmoodi. Sellisel juhul kasutatakse protsessi sõltub sellistest teguritest nagu asukoht või kogus, mille peab.

## <a name="routes"></a>Protsessid
Marsruudi kirjeldatakse toote või toote variant tootmiseks kasutatav operatsioonide järjekorra. Iga tegevus määrati operatsiooni number ja pärija operatsiooni. Toimingute järjekord moodustab liinivõrgu, milleks võib olla suunatud diagramm, mis on ühe või mitme lähtekohti ja ühe lõpp-punkti. Dynamics 365 toiminguteks, eristatakse tüüpi struktuur põhineb liinidel. Kaks marsruudid on lihtne liinidel ja marsruudi võrgud. Tootmise parameetrid, saate määrata kas ainult lihtne liinidel saab, või kas keerulisemate protsessi võrkude kasutamist.

### <a name="simple-routes"></a>Lihtne liinidel

Lihtne protsess on järjestikuste ja seal on ainult üks tee.  

[![Lihtne marsruut](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Ainult lihtne liinidel tootmisparameetrite kontrolli lubamisel Dynamics 365 operatsioonide loob automaatselt nende operatsioonide numbrid (10, 20, 30 ja nii edasi) kui määratlete marsruut.

### <a name="route-networks"></a>Liinivõrku

Keerulisemate protsessi võrkude tootmisparameetrite kontrolli lubamisel saate määratleda mitme algus punkti ja toimingud, mida saab käivitada paralleelselt liinidel.  

[![Route network](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Märkused.**

-   Ettevõtmise võib olla ainult üks järeltulija operatsiooni ning kogu marsruudi lõppema ühekorraga.
-   Ei ole kindel, mis tegelikult töötab mitu toimingud, mis on ühe pärija tegevuse (nt tegevusvaldkonnad 30 ja 40 eelmisel joonisel) samaaegselt. Olemasolu ja jõudlusega ressursside võib panna piirangud operatsioonid planeeritakse teel.
-   Te ei saa kasutada operatsiooni number 0 (null). See number on reserveeritud ja määrata protsessi viimase operatsiooni on ükski pärija tegevus.

### <a name="parallel-operations"></a>Paralleelsed operatsioonid

Mõnikord, koos mitme tegevuse ressursse, erinevate omadustega on vajalik töötamiseks. Näiteks kokkupanekut võib nõuda masin, vahend ja üks töötaja iga kaks masinat tegevuse üle järelevalve teostamiseks. See näide võib modelleerida abil samaaegseid operatsioone, kui operatsioonist on määratud esmase operatsiooni ja teised on teisejärgulised.  

[![Marsruudil, mis on esmane ja teisene](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Üldjuhul esmase operatsiooni esindab kitsaskoht ressursi ja dikteerib ka teisese operatsiooni Käitusaeg. Kuid planeerimisel rahalisel piiratud võimsus, esmase operatsiooni ja teiseste operatsioonide planeeritud vahendeid tuleb saadaval ja on samal ajal vaba võimsust.  

Esmane operatsioon ja teiseste operatsioonide peab olema sama operatsiooninumbrit (30 eelmisel joonisel).  

Eelmises näites esmase operatsiooni (30) ressursi vajadus on masin, teiseste operatsioonide (30' ja 30'') ressursivajaduse on tööriist ja töötaja. 50% - l koormus aitab tagada, et määratud töötaja saab jälgida kaks masinat korraga.

### <a name="approval-of-routes"></a>Protsesside kinnitamine

Marsruudi peab enne planeerimise või tootmise protsessi kasutamist olema kinnitatud. Kinnitamine näitab, et lennutee kujundamisega lõppemist. Sama välja toote või väljalastud toote variant võib olla mitme heakskiidetud marsruudi. Marsruudi heakskiitmine esineb tavaliselt, kui esimene asjakohaste protsessiversioon kinnitatud. Kuid mõned äri stsenaariumid, marsruudi ja protsessi versioon on eraldi tegevuste korraldamisse tootmisprotsessi eri omanikele.  

Igal marsruudil võib olla kinnitatud või kinnitamata eraldi. Pange tähele, kui protsess on kinnitamata, kõik seotud protsessi versioonid on ka kinnitamata. Tootmise parameetrid, saate määrata kas liinidel võib olla kinnitamata ja kinnitatud protsesside muudetavad.  

Kui peate Logi mis kirjeid, kes kinnitab iga liini, võib nõuda protsessi kinnitamine e-allkirja. Siis on kasutajad abil tõendada oma [digitaalallkirja](/dynamics365/operations/organization-administration/electronic-signature-overview).

## <a name="operations"></a>Toimingud
Operatsiooni on tootmisprotsessis. Dynamics 365 operatsioonideks, on iga toimingu ID ja lihtne kirjeldus. Järgmises tabelis on tüüpilised näited toimingud kohapeal pood.

| Toiming  | Kirjeldus        |
|------------|--------------------|
| PipeCut    | Toru lõikamine       |
| TIGweld    | TIG keevitus        |
| JigAssy    | Šabloon assamblee       |
| Kontroll | Kvaliteedi kontroll |

Tegevuse atribuutide operatsiooni, Seadistusaeg ja Käitusaeg, ressursivajadused, omahinna arvutamise teabe ja arvutamine, nagu on ära toodud operatsiooniseose. (Seoste lisateabe saamiseks vt järgmist jaotist.)

## <a name="operation-relations"></a>Toimingu seosed
Operatsiooni seos hoitakse töökorras laltki operatsiooni:

-   Kulukategooriad
-   Tarbimise näitajad
-   Töötlemise korda
-   Töötlemise kogused
-   Ressursi nõuded
-   Märkmeid ja juhiseid

Saate määratleda mitu seoste sama operatsiooni. Iga operatsiooni seos on seotud ühe toiminguga ja marsruudi, välja antud toodet või vabastatud toodete, mis on seotud kauba grupi kogum seotud atribuudid. Seega sama operatsiooni saab kasutada mitme marsruudi, et erineva töö omadustega. Lisaks saate kergemini säilitada põhiandmeid, et sama töö omadustega, sõltumata protsessi, mida kasutatakse ja toode, mille toodab toimingutega kasutamisel. Operatsiooni seos kohaldamisala on määratletud läbi selle **Tootekood**, **kirje seos**, **Route kood** ja **liinil seoses** omadused, nagu on näidatud järgmises tabelis.

| Kauba kood | Kauba seos         | Protsessi kood | Protsessi seos   | Operatsiooni seos ulatus                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabel     | &lt;Kauba ID&gt;       | Protsess      | &lt;Marsruudi ID&gt; | Tegevuse atribuutide kasutamisel protsessi operatsiooni kui **kood**=&lt;protsessi ID&gt; välja antud toote valmistamiseks kui **kaubakood**=&lt;kirje ID&gt;.                                                                                                                        |
| Tabel     | &lt;Kauba ID&gt;       | Kõik        |                  | Tegevuse vaikeatribuudid operatsiooni välja antud toote kasutamisel kui **kaubakood**=&lt;kirje ID&gt;. Teisisõnu, need tegevuse atribuudid rakendatakse, kui liinil konkreetse operatsiooni seose välja antud toote.                                     |
| Grupeeri     | &lt;Kauba kood&gt; | Protsess      | &lt;Marsruudi ID&gt; | Tegevuse atribuutide kasutamisel protsessi operatsiooni kui **kood**=&lt;protsessi ID&gt; vabastatud valmistamiseks, mis on seotud hooldusüksuse rühma &lt;kirje tunnus on&gt;, kui on välja antud toote marsruudi konkreetse operatsiooni seos.                         |
| Grupeeri     | &lt;Kauba kood&gt; | Kõik        |                  | Toimingu kasutamisel vabastatud valmistamiseks, mis on seotud hooldusüksuse rühma tegevuse atribuutide vaikesätete &lt;kirje tunnus on&gt;, kui konkreetseid operatsiooni seos on olemas.                                                                                                  |
| Kõik       |                       | Protsess      | &lt;Marsruudi ID&gt; | Tegevuse vaikeatribuudid operatsiooni, kui seda kasutatakse protsessi kui **kood**=&lt;protsessi ID&gt;. Tähendab, nende tegevuse atribuutide pöörduda operatsiooni seos puudub sellel liinil, oleneb kas väljalastud toote või sellega on seotud Kaubagrupp. |
| Kõik       |                       | Kõik        |                  | Tegevuse atribuutide vaikesätete operatsiooni. Nende tegevuse atribuudid rakendatakse, kui pole konkreetseid operatsiooni seos.                                                                                                                                                                |

Saate ka määrata, et operatsiooniseose keskkonnaseires. Nii tegevuse atribuutide operatsiooni võib varieeruda sõltuvalt asukohast (st sait) Kui toimingu. Konfigureeritud kaupade puhul saate määrata eri tegevuse omaduste iga toote konfiguratsiooni.  

Operatsiooniseosed teile paindlikult kõrguspiirang määratlemisel. Lisaks aitab määratleda vaikeatribuudid vähendada põhiandmed, mis tuleb säilitada. Aga see ka tähendab, et peab olema muutmist operatsiooniseose ja konteksti.  

**Märkus:** et tegevuse atribuute talletatakse operatsiooniseosed iga operatsiooni iga marsruudi, kõik korrad ühe tegevuse (nt assamblee) on sama Sisestusaeg, Käitusaeg, järele ja nii edasi. Seega, kui kahe esinemisjuhu operatsiooni tuleb esineda samal liinil on eri kulgema korda, loote kahe erineva tehinguni, nagu Assembly1 ja Assembly2.

### <a name="modifying-product-specific-routes"></a>Konkreetse ravimi marsruutide muutmine

Kui avate selle **liinil** lehekülg selle **välja toote üksikasjad** lehel kuvatakse protsessi versioonid, mis on seotud valitud väljalastud toote. Iga tegevuse puhul Dynamics 365 operatsioonide näitab tegevuse atribuute operatsiooniseose kõige paremini sobiva protsessiversiooni. Märkad, et toimingute loetelu sisaldab on **Tootekood** ja **marsruudi koodi** operatsiooniseose kohandatud atribuudid. Seetõttu saate määratleda, millised operatsiooni seos kuvatakse.  

Kohta ning **liinil** lehel operatsiooni Käitusaeg või kulukategooriaid nagu tegevuse atribuutide muutmist. Tehtud muudatused on salvestatud operatsiooniseose iseloomulikke marsruut ja väljalastud toote, mis on viidatud praeguse protsessiversiooni. Kui operatsiooni seos, mis on näidanud, ei ole konkreetselt välja antud toote ja protsessi enne tehtud muudatused on salvestatud, loob süsteem operatsiooniseose koopia. See eksemplar *on* liinil ja väljalastud toote. Seetõttu tehtud muudatused ei mõjuta teisi marsruute või vabastatud toodete. Kontrollimaks, millist operatsiooni seos muudetakse kohta ning **liinil** lehekülg, Vaata selle **Tootekood** ja **Route koodi** väljad.  

Saate luua ka käsitsi toiming, mis on seotud protsessi ja välja antud toote abil on **koopia ja muuta seoses** funktsiooni.  

**Märkus:** kui sa lisada uus operatsioon marsruut on **liinil** lehel operatsiooniseose luuakse praeguse välja antud toote. Seetõttu kui protsessi kasutatakse ka muude vabastatud toodete tootmiseks, ei ole kohaldatav operatsiooni seos eksisteerib vabastatud toodete ja marsruut sobib enam nende vabastatud toodete.

### <a name="maintaining-operation-relations-per-route"></a>Säilitades iga marsruudi operatsiooniseosed

Kui avate selle **marsruudi andmed** lehekülg selle **liinidel** loendi lehel on kõik operatsiooniseosed, mida kohaldatakse marsruudi loend. Seetõttu saate hõlpsasti kontrollida, mis tegevuse atribuute kasutatakse tooteid. Saate muuta atribuudi vaikeväärtused ja konkreetse ravimi atribuudiväärtused.  

Kui lisate uue operatsiooni seos on **marsruudi andmed** lehel on **Route koodi** välja väärtuseks automaatselt **liinil**, ja **liinil seoses** väärtuseks on praeguse protsessi protsessi koodi.

### <a name="maintaining-operation-relations-per-operation"></a>Säilitades iga operatsiooni operatsiooniseosed

: Selle **toimingute** lehe, saate avada selle **operatsiooniseosed** lehekülg. Sellel lehel saate muuta kõiki seoste konkreetse operatsiooni. Saate isegi muuta operatsiooniseosed, mis sisaldavad vaikimisi väärtused.  

Kui teie ettevõte kasutab toiminguid ja tööparameetritele on samad kõikide toodete ja protsesside, on **operatsiooniseosed** lehekülg pakub see mugav viis säilitada tegevuse vaikeatribuudid nende suhtes.

### <a name="applying-operation-relations"></a>Kohaldamise operatsiooniseosed

Mõnikord Dynamics 365 toimingute puhul tuleb leida tegevuse atribuutide operatsiooni. Näiteks, ostutellimuse loomisel iga tegevuse omadusi tuleb kopeerida: operation relations tootmisprotsessi. Sel juhul otsib Dynamics 365 operatsioonide vastava tegevuse seosed kaasnevaid kõige vähem kindla kombinatsioon.  

Kui Dynamics 365 tegevuse otsimise jaoks kõige olulisemad operatsiooniseose välja toote, mis vastab kauba ID välja antud toote operatsiooniseose on eelistada operatsiooniseose et vastet kaubagrupi ID. Mis vastab kauba grupi kood operatsiooniseose eelistatakse vaikimisi operatsiooni seos. Otsing sooritatakse järgmiselt:

1.  **Tootekood**=**tabeli** ja **kirje seos**=&lt;kirje ID&gt;
2.  **Tootekood**=**rühma** ja **kirje seos**=&lt;kirje kood&gt;
3.  **Tootekood**=**kõik**
4.  **Protsessi kood**=**liinil** ja **liinil seoses**=&lt;protsessi ID&gt;
5.  **Protsessi kood**=**kõik**
6.  **Konfiguratsiooni**=&lt;konfiguratsiooni ID.&gt;
7.  **Configuration**=
8.  **Saidi**=&lt;saidi ID&gt;
9.  **Site**=

Seetõttu operatsiooni võib kasutada ainult üks kord iga protsessi jaoks. Kui tehing tehti mitu korda sama protsessi, kõik korrad protseduuris on sama operatsiooni seos ja ei saa iga korra on erinevad omadused (näiteks korda).

## <a name="route-versions"></a>Protsessi versioonid
Protsessi versioonid kasutatakse tekkivate erinevuste säilitamiseks toodete või tootmisprotsessi suurema kontrolli. Nad määratlevad, kumba olema ettevaatlik eraldi välja toote või väljalastud toote variant on toodetud. Järgmistest abil saate määratleda, millise marsruudi kasutatakse väljalastud toote:

-   Toote mõõtmed (suurus, värv, stiil või konfiguratsiooni)
-   Tootmise kogus
-   Valmistamise koht
-   Tootmise kuupäev

Kui oled teatavas kohas, teatud koguses toodet tootva või teatud aja jooksul, saate määrata kindla protsessiversiooni vaikimisi protsessiversiooni. Pange tähele, et ainult üks aktiivne marsruut on lubatud välja antud toote ja kehtestada piiranguid.  

Tootmise parameetrid, saab nõuda kehtivusperiood protsessiversioon alati täpsustada.

### <a name="approval-of-route-versions"></a>Protsessiversiooni kinnitamine

Enne protsessiversioon kasutamist viia või tootmisprotsessi, see peab olema kinnitatud. Protsessiversiooni kinnitamisel saab ka seotud protsessi kinnitada. Pange tähele, et protsessiversiooni saab heaks kiita ainult juhul seotud protsessi ka vastu.

### <a name="activating-the-default-route-version"></a>Protsessiversiooni vaikimisi aktiveerimine

Kui aktiveerite protsessiversioon, määrate see kapten planeerimine vaikimisi protsessiversiooni kasutavad või mida kasutatakse tootmistellimuste loomisel. Sul võib olla ainult üks aktiivne protsessiversioon kehtestada piiranguid (näiteks punkti, saidi või koguse). Kui proovite aktiveerida konfliktide versioon versiooni mis on juba aktiivne, kuvatakse tõrketeade. Et ebamäärane aktiveerimist, peate seejärel inaktiveerida vastuolulist versiooni või muuta protsessi versioon piiranguid (tavaliselt perioodil).

### <a name="electronic-signatures"></a>Elektrooniliste allkirjade

Kui peate Logi mis kirjeid, kes kiidab heaks ja aktiveerib iga protsessi versioon, saate nõuda elektroonilisi allkirju nende ülesannete täitmise eest. Siis on kasutajad, kes saate kinnitada ja aktiveerida protsessiversioone abil tõendada oma [digitaalallkirja](/dynamics365/operations/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Toote muutuse, mis kasutab Juhtumikorraldamise

Toote Muuda täheregistrit heakskiitmist ja uute või muudetud marsruute ja protsessi versioonid annab sulle lihtne näha ülevaadet Marsruudi versiooni piiranguid. Saate kinnitada ja aktiveerida kõik protsessid, mis on seotud ühe tegevuse konkreetne muutus ja dokumenteerima toote muutmine juhul.

## <a name="maintaining-routes"></a>Säilitades liinidel
Sõltuvalt teie ettevõtte vajadusi, võimalik vähendada neid pingutusi, mida on vaja selleks, et säilitada oma protsessi määratlused.

### <a name="making-routes-independent-of-resources"></a>Muutes liinidel sõltumatut ressursside

Paljud süsteemid, toimingute ressursi või ressursirühma, mis tuleks sooritada toimingut peab olema määratud protsessi. Siiski saate määratleda Dynamics 365 operatsioonide, operatsioonide ressursi peavad vastama tegevuse suhtes nõuete kogum. Seetõttu pole eritoimingud ressursi või ressursirühma, mida tuleks kasutada määrata enne tegelikult planeeritakse operatsioon. See funktsioon on eriti kasulik, kui on palju töötajaid või masinad, mida saab täita sama operatsiooni.  

Näiteks saate määrata, et tegevuse puhul peab toimingute ressurss on **masin** tüüp, mis on saanud **stantsimine** võime 20 tonni. Ajastamise mootoriga siis lahendab need nõuded eritoimingud ressursi või ressursirühma kui määratletakse. Sest lihtsalt saate määrata nende nõuete asemel tegevuse sidumist kindla masina, teil on palju rohkem paindlikkust. Lisaks hooldus on lihtsam, kui lisatakse uusi vahendeid või ressursside viiakse.  

Vt lisateavet erinevate järele ja nende tegevuse järele ja [ressursi võimalusi](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Liinide jagamine saidid

Kui te toota sama toodet üle ühe tootmiskoha ja toote sammud on sama kõikides tegevuskohtades, saate kujundada sageli jagatud protsessi, mida kasutatakse üle kõik tootmiskohad. Et luua jagatud marsruut, ei määra saidi enda kohta. Aga peab ikka luua protsessi versioon, mis seostab jagatud liinil toote igas asukohas.  

Peab tegema, on protsessi iga operatsiooni täitmiseks ei sea eritoimingud. või ressursirühma, et selle asemel esitatud omadused vahendeid. Ajastamise mootoriga saab siis määrata asjakohased toimingud ressursside tootmiseks planeeritud linna kodulehekülg. Näiteks kui on väiksed erinevused Käitusaeg või mingi kindla tegevuse Seadistusaeg on kohaspetsiifiline, saate määrata selle teabe lisada täiendavaid operatsiooniseose saidi.  

Täielikult ära jagatud liinidel kasu, tuleks kasutada ka ressursside tarbimise vastava kooslusega seotud koosluse. Kui ressursside tarbimise lipu koosluserea, lao ja asukoha, et tooraine sisse võtta, saab tuletada toimingute ressurss, mis on planeeritud operatsiooni. Seetõttu pole lao ja asukoha määrata enne tootmise tegelikult planeeritud. Nii saate Koosluse ja protsessi kui toode on valmistatud asukohast sõltumatu.

### <a name="standard-operation-relations"></a>Standard operatsiooniseosed

Kui teie ettevõte kasutab standarditud toimingud kogu tootmine ja kui on vähe või üldse mitte muutus seadistusaeg, käitusaja, arvutamine, kulusid, ja nii edasi, võib osutuda kasulikuks vaikimisi kõik seoste loomine. Sellisel juhul Vältige operatsiooniseosed, mis on seotud mis tahes marsruudil või välja toote.  

Kui ka kiire järele oskusi ja võimeid, ja teha oma liinidel saidi sõltumatu, aitate hoida äritegevuse käigus Tootmispersonal miinimumini.  

Selle lähenemise kasutamine on **operatsiooniseosed** leht muutub oma peamiseks kasutajaks kulgema korda ja muude omaduste säilitamiseks.

### <a name="resource-specific-process-times"></a>Loodusvarade protsessi korda

Kui te ei määra tegevuse ressursi või ressursirühma ressursivajaduse operatsiooni osana, toimiks kohaldatavad vahendid erineva kiirusega. Seetõttu võib erineda operatsiooni menetlemiseks kuluvat aega. Probleemi lahendamiseks kasutage selle **valem** välja operatsiooniseose määrata protsessi arvutamine. Valikud on järgmised:

-   **Standard** – (vaikimisi valik) kasutab ainult välju operatsiooniseose ja korrutab määratud Käitusaeg tellimuse koguse arvutamiseks.
-   **Võimsus** – arvutus hõlmab selle **võimsus** välja operatsioonide ressursist. Seega on aeg ressursi sõltuv. Toimingute ressurss määratud väärtust ei tund. See väärtus korrutatakse tellimiskogus ja **tegur** operatsiooniseose väärtuse.
-   **Partii** – partii võimsus arvutatakse operatsiooniseose teave abil. Partiide ja seetõttu protsessi saab siis arvutatakse vastavalt tellimuse kogusele.
-   **Ressursi partii** – see valik on põhimõtteliselt sama, mis on **partii** võimalus. Kuid arvutus hõlmab selle **partii maht** välja operatsioonide ressursist. Seega on aeg ressursi sõltuv.


<a name="see-also"></a>Vt ka
--------

[Bills of materials and formulas](bill-of-material-bom.md)

[Cost categories used in production routing](../cost-management/cost-categories-used-production-routings.md)

[Resource capabilities](resource-capabilities.md)

[Electronic signature overview](/dynamics365/operations/organization-administration/electronic-signature-overview)


