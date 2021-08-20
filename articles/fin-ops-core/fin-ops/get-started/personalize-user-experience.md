---
title: Kasutuskogemuse isikupärastamine
description: Selles teemas selgitatakse, kuidas isikupärastada rakendust.
author: jasongre
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 62363
ms.assetid: 57b445d7-3e9e-4228-8728-f63b9dbd77a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f71a94a6a5780f8a59590008f6370cb6897fa644e7fd826bacd0fb6206d159c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719297"
---
# <a name="personalize-the-user-experience"></a>Kasutuskogemuse isikupärastamine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas saate rakendust isikupärastada, ning see hõlmab järgmisi teemasid. 

- **Kogu süsteemi hõlmavad suvandid** – need isikupärastamise suvandid on saadaval seadistuslehel kõigile kasutajatele. Näiteks võib tuua värvikujunduse ja ajavööndi. 
- **Piiratud juurdepääs isikupärastamisele** – sellel juurdepääsutasemel salvestab rakendus automaatselt kasutaja tegevused, mis on seotud tüüpilise lehekasutusega, ja need taastatakse järgmine kord, kui te lehte külastate. Näiteks talletab rakendus ruudustiku veerulaiused, kui neid korrigeerite, ja kiirkaartide laiendatud või ahendatud oleku. 
- **Täielik juurdepääs isikupärastamisele** – sellel juurdepääsutasemel on kasutajatel juurdepääs kõigile rakenduse isikupärastamise võimalustele. Eelkõige on neil juurdepääs tööriistaribale **Isikupärastamine**. 
- **Isikupärastamiste jagamine** – kasutajad, kellel on täielik juurdepääs isikupärastamisele, saavad eksportida oma lehe isikupärastamisi ja jagada neid teiste kasutajatega.
- **Isikupärastamiste haldamine** – selle õigusega kasutajatel on juurdepääs halduslehele **Isikupärastamine**, et hallata kõiki isikupärastamisi organisatsioonitasemel. 

## <a name="system-wide-options-for-the-current-user"></a>Süsteemiülesed suvandid praegusele kasutajale

Leht **Kasutaja suvandid** sisaldab mitut süsteemiülest sätet praegusele kasutajale. Need suvandid on saadaval kõigile kasutajatele, isegi neile, kellele ei ole isikupärastamisele juurdepääsu antud. Lehe **Kasutaja suvandid** avamiseks valige navigeerimisribal nupp **Sätted** ja siis valige **Kasutaja suvandid**. Lehel **Kasutaja suvandid** on neli vahekaarti erinevate kasutajasätetega.

- **Visuaalne** – saate valida lehtede värvikujunduse ja elementide vaikesuurused.
- **Eelistused** – saate valida vaikeväärtused, mida kasutatakse iga kord, kui süsteemi avate. Väärtused hõlmavad vaikeettevõtet, esialgset lehte ja kuvamise/redigeerimise vaikerežiimi. (Kuva-/redigeerimisrežiim määrab, kas leht on vaatamiseks lukus või avaneb iga kord redigeerimiseks, kui selle avate.) Sellel vahekaardil on ka suvandid keele, ajavööndi ning kuupäeva-, kellaaja- ja numbrivormingute valimiseks. Samuti sisaldab see vahekaart mitmesuguseid eelistusi, mis erinevad olenevalt väljaandest.
- **Konto** – vaadake või kohandage oma kasutajanime ja muid kontoga seotud suvandeid.
- **Töövoog** – saate valida seotud suvandeid.

Lisaks oma kasutajasätete muutmisele saate oma kasutusandmeid ja isikupärastamisi vaadata ning kustutada lehel **Kasutaja suvandid**. Oma kasutusandmete vaatamiseks valige toimingupaanil **Kasutusandmed**. Süsteemi lehtedel tehtud isiklikke muudatusi võimaldab teil vaadata ja hallata vahekaart **Isikupärastamine**. Sellel vahekaardil saate lähtestada ka funktsiooni viiktekstid (st hüpikaknad, mis tutvustavad uusi süsteemifunktsioone). Seejärel teavitatakse teid uuesti eelnevatest funktsioonidest.

> [!NOTE]
> Kui funktsioon [Salvestatud vaated](saved-views.md) on sisse lülitatud, saate isikupärastamisi vaadata ja hallata, kui valite lehe **Kasutaja valikud** tegumiribal **Isikupärastamine**.

## <a name="restricted-personalization-access-formerly-implicit-personalizations"></a>Piiratud juurdepääs isikupärastamisele (varem kaudsed isikupärastamised)

**Piiratud juurdepääsutasemel isikupärastamisele** salvestab rakendus automaatselt kasutaja tegevused, mis on seotud tüüpilise lehekasutusega, ja need taastatakse järgmine kord, kui te lehte külastate. Eraldi salvestamine pole vajalik. 

Siin on loend tegevustest, mis kuuluvad tüüpilise lehekasutuse ja seega piiratud juurdepääsu alla isikupärastamisele. 

- **Ruudustiku veergude laiused** – saate korrigeerida veeru laiust ruudustikus, valides veerupäisest vasakul või paremal oleva suuruse muutmise riba ja libistades seda vasakule või paremale, kuni veerg on soovitud laiusega. Rakendus salvestab veeru jaoks valitud laiuse. Seejärel muudetakse järgmine kord, kui lehe avate, veeru laius selleks laiuseks.
- **Ruudustiku jalus ja veergude summad** – *(saadaval ainult siis, kui uus ruudustiku juhtelement on sisse lülitatud)* saate otsustada, kas ruudustiku numbreid sisaldava veergude allosas tuleks näidata summat ning kas ruudustiku jalus peaks nähtav olema. Rakendus talletab need eelistused ja rakendab need järgmisel korral, kui avate lehe. Lisateavet vt jaotisest [Ruudustiku võimalused](grid-capabilities.md). 
- **Kiirkaardid** – mõnel lehel on laiendatavad jaotised, mida nimetatakse *kiirkaartideks*. Rakendus salvestab teabe laiendatud või ahendatud kiirkaartide kohta. Samad kiirkaadid laiendatakse või ahendatakse järgmisel korral, kui lehe avate, võttes aluseks teie viimast tegevust lehel. Mõnel juhul saate kiirkaardi ahendamisega aidata süsteemi jõudlust parandada, sest rakendus ei pea kiirkaartide teavet tooma, kuni neid ei laiendata. Nagu hiljem selles teemas selgitatakse, saate muuta ka kiirkaartide järjestust lehel.
- **Kiirinfo** – mõnel lehel on paan **Seotud teave**, millel kuvatakse lehe praeguse teemaga seotud kirjutuskaitstud teave. Igat paani **Seotud teave** jaotist nimetatakse *Kiirinfoks*. Saate kogu paani **Seotud teave** laiendada või ahendada, samuti laiendada või ahendada üksikuid kiirinfo jaotisi. Rakendus salvestab need eelistused. Teie viimast tegevust lehel arvesse võttes laiendatakse või ahendatakse paani **Seotud teave** ja üksikuid kiirinfo jaotisi järgmine kord, kui lehe avate. Mõnel juhul saate paani **Seotud teave** või kiirinfo ahendamisega aidata süsteemi jõudlust parandada, sest rakendus ei pea kiirinfo jaotiste teavet tooma, kuni neid ei laiendata.
- **Toimingupaanid** – *toimingupaan* kuvatakse enamiku lehtede ülaserva lähedal. Toimingupaan sisaldab nuppe paljudeks tegevusteks, mida praegusel lehel saate teha. Need nupud on sageli korraldatud vahekaartidele. Saate kogu toimingupaani avatuks *kinnitada* või hoida seda vaikimisi ahendatuna. Toimingupaan avatakse või ahendatakse järgmisel korral, kui lehe avate, võttes aluseks teie viimast tegevust lehel. Kui olete toimingupaani kinnitanud, kuvatakse viimati kasutatud vahekaart.
- **Kiirfiltrid** – *kiirfilter* kuvatakse paljude ruudustike kohal. Kiirfiltriga saate ruudustikku filtreerida ühe valitud veeru põhjal. Rakendus salvestab filtreeritud veeru valiku. Seejärel filtreeritakse ruudustik vaikimisi sama veeru järgi, kui selle lehe järgmine kord avate. Siiski saate valida erineva veeru, mille alusel ruudustikku filtreerida.
- **Veerupäisefiltrid** – kui filtreerite ruudustiku *veerupäisefiltrite* abil, saate soovitud andmete leidmiseks muuta filtri operaatorit soovitud viisil. Näiteks saate valida tehtemärgi **algab väärtusega** asemel tehtemärgi **on täpselt**. Iga kord, kui kasutate veerupäisefiltrit ja muudate filtri tehtemärki, salvestab rakendus muudatuse. Seejärel taastab see filtri tehtemärgi järgmine kord, kui selle veeru alusel filtreerite.
- **Navigeerimispaan** – saate avada *navigeerimispaani*, valides mistahes lehe vasakul paanil nupu **Laienda navigeerimispaani**. (_**Menüü** nuppu_, nimetatakse mõnikord *hamburgeriks*, *hamburgerimenüük* s või *hamburgerinupuks*.) Saate kinnitada navigeerimispaani avatuna või hoida selle vaikimisi ahendatuna. Kui olete navigeerimispaani avatuna kinnitanud, hoiab rakendus seda lahti, kuni selle ahendate.

## <a name="full-personalization-access-formerly-explicit-personalizations"></a>Täielik juurdepääs isikupärastamisele (varem otsesed isikupärastamised)

**Täielikul juurdepääsutasemel isikupärastamisele** on kasutajatel juurdepääs kõigile rakenduses pakutud isikupärastamise võimalustele. Kuna inimestel ja ettevõtetel on rakenduse kasutamisel erinevad vajadused, eriti kasutatavaid välju arvestades, pakub isikupärastamine tööriistasid, mis võimaldavad kasutajatel ning organisatsioonidel kohandada viisi, kuidas teavet rakenduses järjestatakse ja kasutatakse. Need võimalused on olulised, et pakkuda rakenduses lihtsustatud, optimeeritud kogemust, mis on kohandatud teie ja teie organisatsiooni jaoks. 

Kui funktsioon [Salvestatud vaated](saved-views.md) on sisse lülitatud, on vaja muudatused salvestada, et neid rakendataks kasutaja jaoks kindlas vaates püsivalt. Kui funktsioon **Salvestatud vaated** on välja lülitatud, salvestatakse need muudatused automaatselt.

Järgmistes jaotistes käsitletakse isikupärastamise võimalusi, mis on kasutajatele saadaval **täielikul juurdepääsutasemel isikupärastamisele**. Siin on mõned nendest võimalustest.

- Otseteemenüü suvandid
- **Isikupärastamise** tööriistariba
- Paanide, loendite ja linkide lisamine tööruumidesse
- Kokkuvõtte lisamine tööruumist armatuurlauale
- Armatuurlaua isikupärastamine

### <a name="shortcut-menu-options"></a>Otseteemenüü suvandid

Otseteemenüüd pakuvad ühte võimalust lehe kasutajaliidese muutmiseks, et see vastaks paremini teie enda või teie ettevõtte nõuetele. (Otseteemenüüd nimetatakse ka *paremklõpsuga avatavaks menüüks* või *kontekstimenüüks*.)

Mõned tüüpilisimad ja olulisimad muudatused, mille lehele saab teha, on saadaval otse, kasutades otseteemenüü suvandeid. Näiteks kui soovite lisada ruudustikku veerge või neid peita, lihtsalt paremklõpsake veerupäisel ja siis valige käsk **Sisesta veerge** või **Peida see veerg**.

Lisaks sellele on enamik isikupärastamistüüpe saadaval, kui paremklõpsate elemendil ja valite käsu **Isikupärastamine**. (Arvestage sellega, et kõiki lehel olevaid elemente ei saa isikupärastada.) Kui valite selle isikupärastamise viisi, ilmub elemendi *atribuudiaken*.

![Elemendi atribuutide isikupärastamine.](./media/cli-element-property-window.png)

Atribuudiakna kaudu on elemendi isikupärastamiseks järgmised võimalused.

- Elemendi sildi muutmine.
- Elemendi peitmine, nii et seda lehel ei kuvata. Väljal olevaid andmeid ei kustutata ega muudeta. Seda teavet lihtsalt ei kuvata enam lehel.
- Teabe lisamine kiirkaardi kokkuvõttejaotisse (kui element on kiirkaardil).
- Jätke väli vahele, et seda ei saaks kunagi fokusseerida, kui te tabuleerite läbi lehe.
- Saate väljal olevate andmete (mis tahes kirje puhul) redigeerimist takistada.
- Määrake andmesisestuse jaoks nõutav väli. Kui sellele väljale pole väärtust sisestatud, kuvatakse selle oleku tähistamiseks punane ääris ja tärn. See suvand on saadaval ainult alates versioonist 10.0.11, milles on sisse lülitatud funktsioonid [Salvestatud vaated](saved-views.md) ja **Väljade määramine vastavalt vajadusele isikupärastamise abil**.

Atribuudiaken võib sisaldada ka muid isikupärastamisvõimalusi olenevalt elemendist. Näiteks võib paani atribuudiaken lubada teil ülendada selle paani armatuurlauaks ning vaikearmatuurlaua elementide atribuudiaknad võib lubada teil luua uue kohandatud tööruumi.

### <a name="personalization-toolbar"></a>Isikupärastamise tööriistariba

Kui soovite teha lehel mitu muudatust või teha muudatusi, mis pole muude mehhanismide kaudu saadaval (nt kui soovite elemente ümber järjestada), saate kasutada tööriistariba **Isikupärastamine**. Tööriistariba **Isikupärastamine** avamiseks toimige järgmiselt.

- Vajutage **Ctrl+Shift+P** mis tahes lehel olevast elemendist.
- Avage elemendi atribuutide aknas **Isikupärasta seda lehte**.
- Valige mistahes lehe vahekaardi **Suvandid** jaotise **Isikupärastamine** tegumiribal **Isikupärasta seda lehte**.
- Valige navigeerimisribal nupp **Sätted** (hammasrattasümbol) ja valige **Isikupärasta**.

[![Isikupärastamise tööriistariba.](./media/restyledPersonalizationToolbar.png)](./media/restyledPersonalizationToolbar.png)

#### <a name="navigating-the-page"></a>Lehel liikumine

Kui tööriistariba **Isikupärastamine** on avatud, on aluseks olev leht kirjutuskaitstud (teiste sõnadega, te ei saa andmeid redigeerida), kuid see on siiski interaktiivne. Täpsemalt saate laiendada või ahendada paani **Seotud teave**, vahetada vahekaarte ja laiendada või ahendada jaotisi samamoodi, nagu teeksite neid toiminguid lehel. Isikupärastamismuudatuse rakendamiseks ahendatavale jaotisele või vahekaardile (nt kiirkaardi peitmine), käivitate vaid ahendatava jaotise või vahekaardi kõrval kuvatava nupu, kui sellele klaviatuuri või hiire abil liigute.

#### <a name="personalization-tools"></a>Isikupärastamise tööriistad

Tööriistaribal **Isikupärastamine** on saadaval järgmised tööriistad.

- Tööriistaga **Vali** saate valida ja muuta elemendi atribuute. Selle tööriista kasutamiseks valige tööriistaribal nupp **Vali** ja seejärel valige soovitud element. Kuvatakse elemendi atribuudiaken, kus te saate muuta selle elemendi kõiki atribuute. Saate protsessi selle lehe muude isikupärastatavate elementide puhul korrata. Võtke arvesse, et mõned isikupärastamise atribuudid ei pruugi mõne stsenaariumi puhul saadaval olla. Näiteks ei saa te nõutavat välja lukustada.
- Tööriistaga **Peida** saate elemendi lehel peita. Selle tööriista kasutamiseks valige tööriistaribal nupp **Peida** ja seejärel valige peidetav element. Tööriista **Peida** kasutamisel muudetakse kõik parasjagu peidetud elemendid nähtavaks, kuid need kuvatakse varjutatud konteineris. Elemendi saate nähtavaks muuta, kui valite selle. Selleks, et vaadata, milline leht välja näeb, kui elemendid on peidetud, aktiveerige muu isikupärastamistööriist või sulgege isikupärastamistööriist.
- Väljade lisamiseks oma lehele kasutage tööriista **Lisa välju**. Selle tööriista kasutamisel saate lisada ainult välju, mis on osa lehekülje määratlusest. Teavet selle kohta, kuidas luua uusi välju, mis ei ole osa praeguse lehe määratlusest, vt jaotisest [Kohandatud väljade loomine ja nendega töötamine](user-defined-fields.md). Nupu **Lisa välju** valimisel tööriistaribal peate esmalt valima ruudustiku või jaotise, kuhu soovite välja lisada. Dialoogiboksis kuvatakse valitud ruudustiku või jaotisega seotud väljade loend. Valige dialoogiboksis lisamiseks üks või mitu välja ja seejärel valige käsk **Värskenda**. Varem lisatud välja eemaldamiseks korrake protsessi, kuid tühjendage dialoogiboksis välja valik.
- Tööriistaga **Teisalda** saate nihutada elemendi praeguses elemendirühmas teise asukohta. Võtke arvesse, et elementi ei saa teisaldada emagrupist väljapoole. Selle tööriista kasutamiseks valige tööriistaribal nupp **Teisalda** ja seejärel valige teisaldatav element. Elemendi valimisel määratleb rakendus asukohad, kuhu elementi saab teisaldada. Neid asukohti tuntakse *pukseerimistsoonidena*. Elemendi lohistamisel praeguses rühmas kuvatakse iga pukseerimistsoon värvilisena ja paksu joonega selle ala kõrval, kuhu elemendi saab pukseerida.
- Tööriistaga **Jäta vahele** saate eemaldada elemendi lehe klaviatuuri vahekaardijärjestusest. Nupu **Jäta vahele** valimisel tööriistaribal kuvatakse kõik parasjagu vahelejäetud elemendid varjutatud konteineris. Välju saate interaktiivselt vahekaardi järjestusest eemaldada või neid sinna lisada.
- Tööriistaga **Kuva päis** saate kuvada välja kiirkaardi kokkuvõttejaotises. Tööriistariba nupu **Kuva päises** valimisel kuvatakse kõik kokkuvõtteväljadena valitud väljad varjutatud konteineris. Saate välju interaktiivselt kiirkaardi kokkuvõttesse lisada ja välju sealt eemaldada, valides soovitud väljad.
- Kasutage tööriista **Nõua**, et määrata element, nagu on nõutud andmesisestuse jaoks. Nupu **Nõua** valimisel tööriistaribal kuvatakse kõik nõutavad isikupärastatud elemendid varjutatud konteineris. Seejärel saate need uuesti mittenõutavaks muuta. See suvand on saadaval ainult versioonis 10.0.12 ja hilisemates versioonides, milles on sisse lülitatud funktsioon **Väljade määramine vastavalt vajadusele isikupärastamise abil**.
- Tööriistaga **Lukusta** saate märkida elemendi redigeeritavaks või mitteredigeeritavaks. Nupu **Lukusta** valimisel tööriistaribal kuvatakse kõik parasjagu mitteredigeeritavad elemendid varjutatud konteineris. Seejärel saate need uuesti redigeeritavaks muuta. Arvestage sellega, et mõned väljad on nõutavad ja neid ei saa mitteredigeeritavaks muuta. Nende väljade kõrval kuvatakse tabalukuikoon.
- Kasutage tööriista **Lisa rakendus Power Appsist**, et manustada lehel rakendus, mis loodi Microsoft Power Appsi kasutades. Üksikasjalikku teavet rakenduse Power Appsist lehele manustamise kohta vt teemast [Rakenduste manustamine Power Appsist](embed-power-apps.md). See suvand on saadaval ainult siis, kui funktsioon [Salvestatud vaated](saved-views.md) on väljalülitatud.
- Kasutage nuppu **Lisa rakendus**, et manustada lehele rakendus, mis loodi Microsoft Power Appsis või kolmanda poole poolt. See suvand on saadaval ainult siis, kui funktsioon [Salvestatud vaated](saved-views.md) on sisse lülitatud. 
- Kasutage tööriista **Eemaldamine** lehe lähtestamiseks vaikesätetele, installitud olekusse. Kõik praeguse lehe isikupärastamised kustutatakse. Seda tegevust ei saa tagasi võtta. Seetõttu kasutage seda tööriista ainult siis, kui soovite lehe lähtestada. Kui funktsioon **Salvestatud vaated** on sisse lülitatud, kustutab see tööriist praeguse vaate isikupärastamise.
- Tööriistaga **Importimine** saate laadida isikupärastamise failist, mille teie või keegi teine on lehe jaoks varem loonud. 

    - Kui funktsioon **Salvestatud vaated** on väljalülitatud, saate valida, kas lisada või asendada oma olemasolevad isikupärastamised lehe jaoks imporditavate isikupärastamistega. Seda tegevust ei saa tagasi võtta. Seetõttu peate pärast isikupärastamise importimist käsitsi eemaldama või tühistama kõik soovitud muudatused.
    - Kui funktsioon **Salvestatud vaated** on sisse lülitatud, muutuvad imporditud isikupärastamised lehe vaateks. Kui vaade on juba olemas, siis on teil võimalus importimine vahele jätta, asendada praegune vaade, millel on sama nimi, või nimetada imporditud vaade ümber.

- Tööriistaga **Eksportimine** saate oma lehe isikupärastamised failina salvestada. Saate seejärel oma isikupärastamisi teiste kasutajatega jagada. Need kasutajad peavad lihtsalt importima teie lehe isikupärastamisi sisaldava faili. Kui funktsioon **Salvestatud vaated** on sisse lülitatud, salvestab see tööriist praeguse vaate jagatavasse faili.
- Valige nupp **Sule**, kui soovite tööriistariba **Isikupärastamine** sulgeda ja lehe eelmise interaktiivse oleku taastada.

Traditsiooniliselt, kui kasutate tööriistariba **Isikupärastamine**, jõustuvad teie isikupärastamised kohe, kui need teete. Kui aga funktsioon [Salvestatud vaated](saved-views.md) on sisse lülitatud, peate isikupärastamised kindlasti salvestama valitud vaatesse.

Mõnel juhul kuvatakse tööriista valimisel elemendi kõrval tabalukuikoon. See ikoon näitab, et valitud tööriistaga seotud elemendi atribuute ei saa muuta, kuna nende atribuutide muutmine takistab lehe korralikku toimimist.

### <a name="adding-tiles-lists-and-links-to-a-workspace"></a>Paanide, loendite ja linkide lisamine tööruumi

Mõned lehed, milles on loendid, on isikupärastamisfunktsioon **Lisa tööruumi** saadaval tegumiriba vahekaardi **Suvandid** jaotises **Isikupärastamine**. Selle funktsiooni abil saate praegusest loendist lükata vastava teabe kindlasse tööruumi. Tööruumis kuvatav teave võib põhineda kas tervel loendil või loendi filtreeritud ja sorditud versioonis. Samuti saate määrata, kas teave kuvatakse tööruumis loendina, kokkuvõttepaanina, mis võib näidata loendis olevate üksuste arvu, või lingina.

> [!NOTE]
> Kui funktsioon [Salvestatud vaated](saved-views.md) on sisse lülitatud, on tööruumi lükatud sisu vaatega otse lingitud. Vaate päringut kasutatakse andmeid tööruumi tuua ning tööruumi asjaomane paan või link avab selle vaate lehe, nii et selle puhul rakendatakse vaate päring ja isikupärastamised. Kui vaadet uuendatakse, kohandatakse asjaomaseid tööruumi elemente uue vaate järgi.

[![Lisa tööruumi.](./media/personalization-addtoworkspace.png)](./media/personalization-addtoworkspace.png)

- Tööruumile loendi lisamiseks tööruumi sortige või filtreerige esmalt lehel loend, et see kuvaks teavet nii, nagu soovite seda tööruumis kuvada. (Kui funktsioon **Salvestatud vaated** on sisse lülitatud, ei saa te jätkata enne, kui salvestate nende tingimustega vaate.) Seejärel valige **Lisa tööruumi**. Valige tööruum ja seejärel valige väljal **Esitlus** suvand **Loend**. Pärast suvandi **Konfigureeri** valimist ilmub dialoogiboks, kus saate valida veerud, mis peaks tööruumis loendis ilmuma. Saate ka määrata tööruumis olevale loendile sildi.
- Tööruumile paani lisamiseks filtreerige esmalt lehel loendit, et see kuvaks andmed, mida tuleks kokku võtta või millele soovite kiirelt juurdepääsu. (Kui funktsioon **Salvestatud vaated** on sisse lülitatud, ei saa te jätkata enne, kui salvestate nende tingimustega vaate.) Seejärel valige **Lisa tööruumi**. Valige tööruum ja seejärel valige väljal **Esitlus** suvand **Paan**. Kui olete valinud suvandi **Konfigureeri**, ilmub dialoogiboks, kus saate määrata tööruumis olevale paanile sildi. Saate ka määrata, kas paanil kuvatakse arv. Pärast seda, kui paan on tööruumi lisatud, saate selle valida praeguse lehe avamiseks tööruumist. Seejärel saate vaadata paaniga seotud filtreeritud loendit.
- Tööruumile lingi lisamiseks filtreerige esmalt lehel loend, nii et see kuvaks andmeid, millest olete huvitatud. (Kui funktsioon **Salvestatud vaated** on sisse lülitatud, ei saa te jätkata enne, kui salvestate nende tingimustega vaate.) Seejärel valige **Lisa tööruumi**. Valige tööruum ja seejärel valige väljal **Esitlus** suvand **Link**. Kui olete valinud suvandi **Konfigureeri**, ilmub dialoogiboks, kus saate määrata tööruumis olevale lingile sildi. Samuti saate valikuliselt määrata sildi uuele jaotisele, mis seda linki sisaldab.

Kui loend, paan või link on tööruumile lisatud, saate selle tööruumi avada ja elemendid soovitud viisil ümberkorraldada.

### <a name="adding-a-summary-from-a-workspace-to-a-dashboard"></a>Kokkuvõtte lisamine tööruumist armatuurlauale

Mõni tööruum sisaldab arvpaane (st paane, millel on arvud) ja teil on võimalik ka need paanid armatuurlaual kuvada. Tööruumis paremklõpsake inventuuripaani, valige **Isikupärasta** ja seejärel valige paani atribuutide aknas **Kinnita armatuurlauale**. Järgmine kord, kui te armatuurlaua avate ja seda värskendate, kuvatakse arv selle tööruumi navigeerimispaani all. Saate suunata selle arvu otse asjassepuutuvate andmete juurde.

### <a name="personalizing-your-dashboard"></a>Armatuurlaua isikupärastamine

Armatuurlaud on tihti esimene leht, mida näete rakenduse avamisel. Seda saab isikupärastada nagu kõiki süsteemi lehti, kasutades samu meetodeid, mida enne selles teemas kirjeldati. 

> [!WARNING]
> On oluline, et armatuurlaua sisu peitmisel valiksite te praegu otse paani, mitte selle ümber oleva ruumi. Kui peidate paani ümber oleva grupi, võivad tulemused olla ootamatud, kui hiljem lisatakse rohkem paane või kui süsteem lülitatakse mõnesse muusse keelde.

Üks armatuurlaual saadaolev ainulaadne isikupärastamise võimalus on võime lisada paane. 

- Kui funktsioon **Täisleheküljelised rakendused** on välja lülitatud, saate lisada uue paani, kui paremklõpsate armatuurlaua elemendil ja valite **Lisa tööruum**. Uus tööruumipaan luuakse armatuurlaua alaserva. Saate selle uue tööruumipaani soovitud viisil ümber nimetada. Samuti saate lisada tööruumi loendeid, paane ja linke, nagu on kirjeldatud selle teema jaotises [Paanide, loendite ja linkide lisamine tööruumi](personalize-user-experience.md#adding-tiles-lists-and-links-to-a-workspace).
- Kui funktsioon **Täisleheküljelised rakendused** on sisse lülitatud, saate lisada uue paani, kui paremklõpsate armatuurlaua elemendil ja valite **Lisa rakendus**. Valige dialoogiboksis, kas soovite lisada paani uue tööruumi jaoks või paani, mis sisaldab sisu Power Appsist või veebisaidilt. Seejärel järgige valitud suvandi konfigureerimiseks juhiseid. Uus paan luuakse armatuurlaua alaserva. 

## <a name="sharing-personalizations"></a>Isikupärastamiste ühiskasutamine

Pärast lehe isikupärastamist saate oma isikupärastatud lehte mitmel viisil teiste kasutajatega jagada. Järgmises loendis on meetodid korraldatud järjekorras kõige rohkem soovitatud meetodilt kuni kõige vähem soovitatud meetodile.

1. Avaldada kasutajatele vaated.
2. Kopeerige vaateid või isikupärastamiseid kasutajatele.
3. Eksportige ja importige vaated või isikupärastamiseid.

### <a name="publish-views-to-users"></a>Avaldage kasutajatele vaated

Kui [Salvestatud vaadete](saved-views.md) funktsioon on sisse lülitatud ja kui leht toetab vaateid, siis on parim viis isikupärastamiste jagamiseks teiste kasutajatega avaldada vaated kasutajatele, kel on üks või mitu turberolli. Lisateavet leiate teemast [avaldatud vaated](saved-views.md#publishing-views).

### <a name="copy-views-or-personalizations-to-users"></a>Kopeerige vaated või isikupärastamised kasutajatele

Kui [Salvestatud vaadete](saved-views.md) funktsioon on välja lülitatud või kui leht ei toeta vaatamisi, siis on soovituslik viis isikupärastamiste jagamiseks need kasutajate vahel kopeerida. See meetod on saadaval ainult privilegeeritud kasutajatele (nt süsteemi administraatoritele). Kuigi administraatorid võivad süsteemis otsida konkreetse kasutaja isikupärastamist (k.a kasutaja isiklik vaade, kui salvestatud vaated on lubatud) ja kopeerida konfiguratsiooni teistele kasutajatele.

Kui salvestatud vaated on lubatud, järgige isikupärastamise kopeerimiseks neid samme.

1. Minge **Süsteemi administratsioon \> Seadistus \> Isikustamine**.
2. Isiklike vaadete kopeerimiseks järgige neid samme:

    1. Valige **Isiklikud vaated**.
    2. Valige loendist soovitud vaated.
    3. Valige **Kopeeri kasutajatele**.
    4. Vaadete jaotamiseks valige kasutajad.

    Järgige neid samme isikupärastamise kopeerimiseks lehtedel, mis ei toeta vaateid.

    1. **Kasutajasätete valimine**.
    2. Valige kasutaja, kellel on isikupärastamine, mida soovite jaotada.
    3. Valige **Halda kõiki isikupärastamiseid**.
    4. Valige loendist soovitud isikustamised.
    5. Valige **Kopeeri kasutajatele**.
    6. Isikustamiste jaotamiseks valige kasutajad.

Kui salvestatud vaated ei ole lubatud, järgige isikupärastamise kopeerimiseks neid samme.

1. Minge **Süsteemi administratsioon \> Seadistus \> Isikustamine**.
2. Valige **Rakendamine**.
3. Isikustamiste jaotamiseks valige kasutajad.
4. Valige **Valige olemasolev isikupärastamine**.
5. Otsige ja valige (üksik) isikupärastamine, mida teid soovite.
6. Valige nupp **OK**.

### <a name="export-and-import-views-or-personalizations"></a>Eksportige ja importige vaateid või isikupärastamiseid

Teine viis isikupärastamise jagamiseks on läbi ekspordi ja impordi. Üksikud kasutajad või administraator, kes tegutseb enda nimel, saavad seda meetodit kasutada oma isikupärastamise või vaadete eksportimiseks ja seejärel anda eksporditud faili teistele kasutajatele importimiseks. Teise võimalusena saavad kasutajad anda eksporditud isikupärastamised haldusõigusi omavale kasutajale ja see kasutaja saab seejärel kasutada **Isikupärastamise** halduslehte et rakendada isikupärastamise fail paljudele kasutajatele samaaegselt.

#### <a name="export"></a>Eksport

Üldiselt saate eksportida ühe oma vaadetest või isikupärastamist, avades sobiva lehekülje, avades **isikupärastamise** tööriistariba ja valides seejärel **Ekspordi**. Lisateavet tööriistariba kohta vt [Tööriistariba isikupärastamise](#personalization-toolbar) jaotisest varasemalt selles teemas. Kui [salvestatud vaated](saved-views.md) on lubatud, saate minna ka **Sätted \> Kasutaja võimalused \> Isikustamine** et vaadata kõigi isikustamiste loendit süsteemis. Sealt saate valida eksportimiseks vaateid või isikupärastamiseid ja seejärel valida **Ekspordi**.

Lisaks saavad administraatorid eksportida teiste kasutajate isikupärastamiseid järgides neid samme.

1. Minge **Süsteemi administratsioon \> Seadistus \> Isikustamine**.
2. Vahekaardil **Kasutajad** valige soovitud kasutaja.
3. Otsige ja valige vaade või isikupärastamine, mida teid soovite.
4. Valige **Ekspordi**.

#### <a name="import"></a>Importimine

Vaate või isikupärastamise importimiseks avage **Isikupärastamise** tööriistariba ja valige **Impordi**. Lisaks saavad administraatorid faili importida ja anda selle kohe ühele või mitmele kasutajale.

Kui salvestatud vaated on lubatud, järgige neid samme.

1. Minge **Süsteemi administratsioon \> Seadistus \> Isikustamine**.
2. Toimingupaanil valige **Impordi vaated \> Kasutaja vaated**.
3. Valige impordimudel:

    - **Valige kindlad kasutajad** – Andke vaade või isikupärastamine valitud kasutajatele.
    - **Impordi vastavalt vajadusel** – importige vaade või isikupärastamine samale kasutajale, kes selle eksportis.

4. Valige **Sirvi** ja otsige ja valige isikustamine importimiseks.
5. Valige **Edasi**.
6. Kui valisite **Valige kindlad kasutajad** 3. sammus, valige kasutajad, kes isikupärastamise impordite.
7. Valige **Impordi**.
8. Lahenda konfliktid vastavalt vajadusele.

Kui salvestatud vaated ei ole lubatud, järgige neid samme.

1. Minge **Süsteemi administratsioon \> Seadistus \> Isikustamine**.
2. Valige **Rakendamine**.
3. Isikustamiste jaotamiseks valige kasutajad.
4. Valige **Impordi isikupärastamised failist**.
5. Valige **Sirvi** ja otsige ja valige isikustamine importimiseks.
6. Valige nupp **OK**.

## <a name="administration-of-personalizations"></a>Isikupärastamiste haldamine

Leht **Isikupärastamine** on isikupärastamiste organisatsiooni tasemel haldamise keskus. Lehe sisu ja võimalused sõltuvad sellest, kas funktsioon **Salvestatud vaated** on sisse lülitatud.

Kliendid, kes on sisse lülitanud funktsiooni **Salvestatud vaated**, näevad teemas [Salvestatud vaated](saved-views.md) jaotist „Vaadete globaalne haldamine“.

Klientidele, kes pole funktsiooni [Salvestatud vaated](saved-views.md) veel sisse lülitanud, on sellel lehel neli vahekaarti.

- **Rakenda** – saate importida või valida vähemalt ühe kasutaja isikupärastamise. Isikupärastamise rakendamiseks ühele või mitmele kasutajale valige esmalt roll ja selle rolliga kasutajad. Seejärel valige kas olemasolev isikupärastamine valitud kasutajatele rakendamiseks või importige isikupärastamise fail. Isikupärastamine kinnitatakse ja rakendatakse valitud kasutajatele järgmisel korral, kui nad valitud lehe avavad.

- **Eemalda** – saate eemaldada vähemalt ühe kasutaja lehe või tööruumi kõik isikupärastamised. Esmalt valige leht või tööruum, et näha seda isikupärastanud kasutajate loendit. Seejärel valige kasutajad, kelle isikupärastamised tuleb sellelt lehelt või sellest tööruumist eemaldada, ja valige käsk **Eemalda**. Kõik isikupärastamised, mille valitud kasutajad on valitud lehele või tööruumile rakendanud, kustutatakse. Seda tegevust ei saa tagasi võtta. Kui aga isikupärastamine on lehele või tööruumile salvestatud, saab selle isikupärastamise uuesti importida.

- **Kasutajad** – saate valida kasutaja, et kuvada loend lehtedest, mille kasutaja on isikupärastanud. Seejärel saate valitud kasutaja võimaluse kasutada isikupärastamisi kindlatel lehtedel või terves süsteemis sisse või välja lülitada. Samuti saate kasutaja jaoks isikupärastamise importida, eksportida või eemaldada. Lisaks saate lähtestada kasutaja funktsiooni viiktekstid. Sel juhul, kui kasutaja on varem välja lülitanud kõik hüpikaknad, mis juurutavad uusi funktsioone, kuvatakse need uuesti järgmisel korral, kui kasutaja nende funktsioonidega kokku puutub.

- **Süsteem** – saate ajutiselt välja lülitada süsteemis olevad kõigi kasutajate kõik isikupärastamised. Sel juhul kustutatakse kõik isikupärastamised kõigi kasutajate jaoks ja kõik lehed lähtestatakse nende vaikeolekusse. Kui lülitate isikupärastamise hiljem uuesti sisse, rakendatakse kõik isikupärastamised uuesti. Saate ka kõigi kasutajate isikupärastamised süsteemist jäädavalt kustutada. Kustutatud isikupärastamisi ei ole võimalik taastada. Seega veenduge enne seda ülesannet, et oleksite eksportinud kõik isikupärastamised, mida võite soovida hiljem importida.

## <a name="personalizing-inventory-dimensions"></a>Varude dimensioonide isikupärastamine

Lehel varude dimensioonide häälestuse isikupärastamisel võtke arvesse suvandi **Kuva dimensiooni** abil loodud sätteid. Näiteks saate isikupärastamise abil peita partiinumbri varude dimensiooni veeru, kuid veerg kuvatakse järgmine kord, kui leht avatakse. Selle põhjuseks on asjaolu, et suvandi **Dimensiooni kuvamine** sätted juhivad kuvatavaid varude dimensiooni veerge. **Dimensiooni kuva** sätted rakenduvad kõigile lehtede ja alistavad eraldi lehtedel varude dimensiooniväljade isikupärastatud sätted.

Seega, kui te eeltoodud näites ei soovi partiinumbri varude dimensiooni veergu lehel kuvada, peate selle dimensiooni selle lehe suvandi **Kuva dimensioonid** osana eemaldama.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
