---
title: Dimensioonihierarhia
description: Teema sisaldab teavet dimensioonihierarhiate kohta. Dimensioonihierarhiat saab kasutada aruandlusstruktuuri, kulupoliitikate ja turbeseadistuse määratlemiseks kuluarvestuses.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionHierarchy,
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 71ba02fc6be4ab9a7871c10a9f95c474e52ae765
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442283"
---
# <a name="dimension-hierarchy"></a>Dimensioonihierarhia

[!include [banner](../includes/banner.md)]

Teema sisaldab teavet dimensioonihierarhiate kohta. Dimensioonihierarhiat saab kasutada aruandlusstruktuuri, kulupoliitikate ja turbeseadistuse määratlemiseks kuluarvestuses.  

## <a name="overview"></a>Ülevaade

Dimensioonihierarhiaid kasutatakse kuluarvestuses mitmesugustes kohtades. Dimensioonihierarhia võimaldab määratleda järgmised andmed.

-  Aruandluse struktuur, mis sobib organisatsiooni vajadustega
-  Kulupoliitikad
-  Turvalisuse seadistus

Siin on dimensioonihierarhia näide.

![Dimensioonihierarhia näide](./media/dimension-hierarchy.png)

Dimensioonihierarhia saab luua järgmistele dimensioonitüüpidele.

-  Kuluelemendi dimensioonid
-  Kuluobjekti dimensioonid
-  Statistilised dimensioonid

> [!NOTE]
> - Kui on vaja erinevaid perspektiive, võite luua samale dimensioonile mitu dimensioonihierarhiat.
> - Dimensioonihierarhia saab seostada ainult ühe dimensiooniga.
> - Dimensioonihierarhia struktuuris võib olla piiramatu arv tasandeid. Kõik tasandid on saadaval **kulujuhtimise** tööruumis. Kui kasutate aruandluseks Microsoft Excelit või Microsoft Power BI-d, siis eksporditakse ainult esimesed 15 dimensioonihierarhia taset. See piirang on sellepärast, et nii Excel kui ka Power BI nõuavad fikseeritud skeemi.
> - Dimensioonihierarhia ei sõltu kuupäevast. Seega salvestatakse dimensioonihierarhia muudatused kohe kirje juurde ja varasemat ning hilisemat kuupäeva ei saa võrrelda.

## <a name="dimension-hierarchy-type"></a>Dimensiooni hierarhia tüüp

Uue dimensioonihierarhia loomisel tuleb valida hierarhia tüüp. Avage **Kuluarvestus** > **Dimensioonid** > **Dimensioonihierarhiad**. Klõpsake nuppu **Uus** ja valige dimensioonihierarhia tüüp. Võite valida **Dimensiooni kategoriseerimishierarhia** või **Dimensiooni klassifitseerimishierarhia**.

### <a name="dimension-categorization-hierarchy"></a>Dimensiooni kategoriseerimishierarhia

Tüüpi **Dimensiooni kategoriseerimishierarhia** kasutatakse aruandluseks. See toetab ainult kuluelemendi dimensioone. Kui valite selle tüübi, kehtivad järgmised reeglid.

-  Dimensiooniliikme saab seostada hierarhia struktuuris mitu korda.
-  Kuluelemendi dimensiooniliikme saab paigutada erinevatesse sõlmedesse, määrates lehe sõlmele kulukäitumise.

### <a name="dimension-classification-hierarchy"></a>Dimensiooni klassifitseerimishierarhia

Tüüpi **Dimensiooni klassifitseerimishierarhia** kasutatakse reeglite määratlemiseks ja aruandluseks. See toetab kõiki dimensioone, nt kuluobjekte, kuluelemente ja statistilisi dimensioone. Kui valite selle tüübi, saab dimensiooniliikme seostada hierarhia struktuuris ainult ühe korra.

## <a name="create-and-maintain-a-dimension-hierarchy"></a>Dimensioonihierarhia loomine ja haldamine

Dimensioonihierarhia luuakse puustruktuurina, millel on sõlme ja lehesõlme seosed.

-  Sõlmel võib olla 1:_n_ alamsõlme.
-  Sõlmele ei saa olla määratud nii alamsõlmi kui ka lehesõlmi.
-  Lehesõlme saab määrata hierarhias ainult madalaimale tasandile.

### <a name="example"></a>Näide

Väikeettevõttel on järgmine organisatsiooni struktuur, kus finantsosakond ja personaliosakond on halduse alla kuuluvad osakonnad ja komplekteerimine ning pakkumine on tootmise alla kuuluvad osakonnad.

![Organisatsiooni struktuuri näide](./media/dimension-hierarchy-org.png)

Kuluobjekti dimensioon kajastab kõik organisatsiooni kulukeskusi.

- Kuluobjekti dimensioon
    - Kulukeskused

Kuluobjekti dimensiooni, mis kajastab kõiki kulukeskusi, saab seadistada siin näidatud viisil.

| Kulukeskused | Kirjeldus |
|--------------|-------------|
| CC001        | Personaliosakond          |
| CC002        | Finantsid     |
| CC003        | Maks         |
| CC007        | AR/AP       |
| CC005        | Assembler    |
| CC006        | Pakendamine   |

Kuluelemendi dimensioon kajastab kõik organisatsiooni kuluelemente.

- Kuluelemendi dimensioon
    - Kuluelemendid

Kuluelemendi dimensiooni, mis kajastab kõiki kuluelemente, saab seadistada siin näidatud viisil.

| Kuluelemendid | Kirjeldus |
|---------------|-------------|
| 10001         | Elektrienergia |
| 10010         | Koristamine    |
| 10011         | Küte     |
| 40001         | COGS        |

Dimensioonihierarhia, mis rahuldab organisatsiooni aruandlusvajadused, saab seadistada siin näidatud viisil.

**Dimensioonihierarhia üksikasjad**

| Dimensioonihierarhia nimi | Dimensioon    | Dimensiooni hierarhia tüübi nimi      | Juurdepääsuloendi hierarhia |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisatsioon             | Kulukeskused | Dimensiooni klassifitseerimishierarhia | Ei                    |

Aruandluse jaoks saab dimensioonihierarhia seadistada siin näidatud viisil.

|                   | Dimensiooniliikmete vahemikud   |                         |
|-------------------|---------------------------|-------------------------|
| **Sõlmed**         | **Lähtedimensiooni liige** | **Sihtdimensiooni liige** |
| Organisatsioon      |                           |                         |
| &nbsp;&nbsp;Administraator         |                           |                         |
|&nbsp;&nbsp;&nbsp;&nbsp;Finantsid   | CC002                     | CC003                   |
|                   | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personaliosakond        | CC001                     | CC001                   |
| &nbsp;&nbsp;Tootmine    |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakendamine | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Assembler  | CC006                     | CC006                   |

Dimensioonihierarhia, mis täidab poliitika nõude, saab seadistada siin näidatud viisil.

**Dimensioonihierarhia üksikasjad**

| Dimensioonihierarhia nimi | Dimensioon     | Dimensiooni hierarhia tüübi nimi      |
|--------------------------|---------------|------------------------------------|
| Kulukäitumine            | Kuluelemendid | Dimensiooni klassifitseerimishierarhia |

Poliitika jaoks saab dimensioonihierarhia seadistada siin näidatud viisil.

|                   | Dimensiooniliikmete vahemikud   |                         |
|-------------------|---------------------------|-------------------------|
| **Sõlmed**         | **Lähtedimensiooni liige** | **Sihtdimensiooni liige** |
| Kulukäitumine     |                           |                         |
| &nbsp;&nbsp;Fikseeritud kulu    | 10001                     | 10011                   |
|&nbsp;&nbsp;Muutuv kulu | 40001                     | 40010                   |

> [!NOTE]
> Jaotises **Dimensiooniliikmete vahemikud** võib sõlm sisaldada 1:_n_ dimensiooniliikmete vahemikku. Saate sisestada dimensiooniliikme ID-d, mida ei ole veel dimensiooni liikmetena olemas. See lähenemine muudab hierarhia tulevikku silmas pidades paindlikuks.  

### <a name="copy-a-hierarchy"></a>Hierarhia kopeerimine

Saate kopeerida praeguse dimensioonihierarhia uue dimensioonihierarhia lähtepunktiks. Selline lähenemine võib olla abiks, kui soovite võrrelda eelmist dimensioonihierarhiat uue dimensioonihierarhiaga.

### <a name="rearrange-nodes-in-a-hierarchy"></a>Sõlmede ümberpaigutamine hierarhias

Sõlme saab struktuuri praegusel tasemel üles ja alla liigutada. Sel viisil saate sõlmede järjestust tööruumis **Kulujuhtimine** aruandluse jaoks ümber korraldada.

Sõlme saab hierarhias uude kohta viia, valides sihtsõlme. Sõlme teisaldamiseks on kaks võimalust.

- **Nihuta alla** – saate valitud sõlme selle asukohast hierarhias eemaldada ja lisada valitud sihtsõlme **alla**.
- **Nihuta järele** – saate valitud sõlme selle asukohast hierarhias eemaldada ja lisada valitud sihtsõlme **järele** selle hierarhiatasandil.

> [!NOTE] 
> Sõlmede järjekorda ei säilitata, kui ekspordite andmed Excelisse või Power BI-sse, kuna need tööriistad kasutavad vaikimisi tähtedest ja numbritest koosnevat sortimisjärjestust. Järjekord tuleb käsitsi ümber korraldada.

## <a name="define-dimension-hierarchies-for-reporting"></a>Dimensioonihierarhiate määratlemine aruandluseks

Dimensioonihierarhiad on aruandluseks olulised. Nende abil saate määratleda kindla struktuuri, mis sobib eraldi organisatsioonile. Dimensioonihierarhia sõlme tasandil toimuvad liitmised võimaldavad organisatsiooni igasuguse tasandi sidusrühmadel näha igasuguse tasandi andmeid.

Dimensioonihierarhiad on saadaval järgmistes aruandlustööriistades. See lähenemine aitab tagada aruandlusstruktuuri järjepidevuse.

- **Kulujuhtimise** tööruum (klient):

    - kontrollitakse konfiguratsiooniga.

- **Kulujuhtimise** tööruum (mobiilirakendus):

    - kontrollitakse konfiguratsiooniga.

- Excel

    - annab võimaluse valida konkreetsed dimensioonihierarhiad ekspordidefinitsiooni kohta.

        - Üks kuluelemendi dimensioonihierarhia (kohustuslik)
        - Üks kuluobjekti dimensioonihierarhia (valikuline)
        - Üks statistiline dimensioonihierarhia (valikuline)

- Power BI:

    - saadaval on kõik dimensioonihierarhiad.
    
Kui koostate Exceli või Power BI abil aruandeid, siis eksporditakse ainult esimesed 15 dimensioonihierarhiate taset. See piirang on sellepärast, et nii Excelis kui ka Power BI-s on vaja fikseeritud skeemi. Kui hierarhias on üle 15 taseme, siis rohkem tasemeid ei ekspordita. Normeeritud tabel sisaldab kirjet iga dimensiooniliikme kohta hierarhias. Seetõttu toimub automaatne liitmine. See aitab tagada, et saldod kõigil 15 olemasoleval hierarhiatasandil on õiged.

Järgmises näites näidatakse, milline dimensioonihierarhia aruandlusstruktuuris välja võib näha.

| Kuluobjekti dimensioonihierarhia – tase 1 | Kuluobjekti dimensioonihierarhia – tase 2 | Kuluobjekti dimensioonihierarhia – tase 3 | Kuluobjekti dimensioonihierarhia – tase 4 | Kuluobjekti dimensioonihierarhia – tase 15 |
|-------------------------------------------|-------------------------------------------|-------------------------------------------|-------------------------------------------|--------------------------------------------|
| Organisatsioon                              | Administraator                                     | Finantsid                                   | CC002                                     |                                            |
| Organisatsioon                              | Administraator                                     | Finantsid                                   | CC003                                     |                                            |
| Organisatsioon                              | Administraator                                     | Finantsid                                   | CC007                                     |                                            |
| Organisatsioon                              | Administraator                                     | Personaliosakond                                        | CC001                                     |                                            |
| Organisatsioon                              | Tootmine                                | Pakendamine                                 | CC005                                     |                                            |
| Organisatsioon                              | Tootmine                                | Assembler                                  | CC006                                     |                                            |

### <a name="update-the-dimension-hierarchies-that-are-used-for-reporting"></a>Aruandluses kasutatavate dimensioonihierarhiate uuendamine 

Aja jooksul tuleb eespool mainitud aruandlustööriistades kasutatavaid dimensioonihierarhiaid uuendada. Dimensioonihierarhiaid saab uuendada, uuendades klienti.

- **Kulujuhtimise** tööruum (klient)
- **Kulujuhtimise** tööruum (mobiilirakendus)

Dimensioonihierarhiate uuendused tuuakse eelnevalt vahemällu salvestatud töö puhul iga 24 tunni järel. Pärast eksporditud andmete uuendamist on uuendatud dimensioonihierarhiad saadaval järgmistes tööriistades.

- Excel
- Power BI

> [!NOTE] 
> Dimensioonihierarhia vahemälu uuenduse käsitsi käivitamiseks võite uuendatava dimensioonihierarhia või -hierarhiate puhul luua uue ekspordi Excelisse

## <a name="define-dimension-hierarchies-for-cost-policies"></a>Dimensioonihierarhiate määratlemine kulupoliitikate jaoks

Kuluarvestus koosneb mitmest poliitikast, milles on määratletud üksikasjalikud reeglid. Määratleda tuleb vähemalt üks dimensioonihierarhia järgmiste poliitikate jaoks.

- Kulukäitumine
- Kulu jaotus
- Kulude eraldamine
- Kulukomplekt

Dimensioonihierarhiad muudavad reeglite loomise lihtsaks. Et poleks vaja igale dimensiooniliikmele reegleid luua, võite kasutada dimensiooniliikmete kogumeid dimensioonihierarhia tasandite kaudu. Kui teil on kattuvad reeglid, peate määratlema konkreetsed reeglid, mida süsteem üldkulude arvutamisel arvestab.

### <a name="example-define-a-cost-behavior-policy"></a>Näide: kulukäitumise poliitika määratlemine

Luuakse uus kulukäitumise poliitika ja poliitikale määratakse siin näidatud viisil sobivad dimensioonihierarhiad.

**Kulukäitumise poliitika**

| Poliitika nimi   | Kuluelemendi dimensioonihierarhia | Kuluobjekti dimensioonihierarhia | Arvestusvaluuta |
|---------------|----------------------------------|---------------------------------|---------------------|
| Kulukäitumine | Kulukäitumine                    | Organisatsioon                    | USA dollar                 |

**Reeglid**

| Kuluelemendi dimensioonihierarhia sõlm | Kuluobjekti dimensioonihierarhia sõlm | Fikseeritud protsent | Fikseeritud summa | Kehtiv alates | Kehtiv kuni |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|----------|
| Fikseeritud kulu                            | Organisatsioon                         | 100,00           | 0,00         | 1/1/2017   | Mitte kunagi    |
| 10001                                 | Organisatsioon                         | 0,00             | 150.00       | 1/1/2017   | Mitte kunagi    |
| 10001 (\*)                             | Finantsid                              |                  | 50,00        | 1/1/2017   | Mitte kunagi    |
| Kulukäitumine või muutuvkulu (\*\*)   | Organisatsioon                         | 0,00             | 0,00         | 1/1/2017   | Mitte kunagi    |

\* Muutuvkulu sõlm pole nõutav. Kui kulu pole liigitatud fikseeritud kuluks, peab see olema muutuvkulu.

\*\* Luuakse üksikasjalik reegel kuluelemendi liikme 10001 ja kõigi finantside hierarhiatasandi alla koondatud kuluobjekti liikmete kombinatsioonile (CC002, CC003, CC007).

Eelnevad reeglid näitavad paindlikkust, mida dimensioonihierarhiad pakuvad. Kõrgetasemeliste reeglite määratlemisega saate hooldust vähendada. Seejärel saate määratleda üksikasjalikud reeglid, mis sobiksid konkreetse ärieesmärgiga.

Kui reeglites kasutatavaid dimensioonihierarhiaid muudetakse, toob süsteem need muudatused automaatselt esile.

Kui reeglite granulaarsuse tase pole enam vajalik, võib lasta reeglil aeguda.

Näiteks konkreetne kulukäitumise reegel finantside kuluobjekti dimensiooni hierarhiasõlmes pole enam vajalik. Sellisel juhul klõpsake reegli aeguda laskmiseks nuppu **Lase reeglil aeguda**.

| Kuluelemendi dimensioonihierarhia sõlm | Kuluobjekti dimensioonihierarhia sõlm | Fikseeritud protsent | Fikseeritud summa | Kehtiv alates | Kehtiv kuni  |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|-----------|
| Fikseeritud kulu                            | Organisatsioon                         | 100,00           | 0,00         | 1/1/2017   | Mitte kunagi     |
| 10001                                 | Organisatsioon                         | 0,00             | 150,00       | 1/1/2017   | Mitte kunagi     |
| 10001                                 | Finantsid                              |                  | 50,00        | 1/1/2017   | 20/1/2017 |
| Kulukäitumine või muutuvkulu        | Organisatsioon                         | 0,00             | 0,00         | 1/1/2017   | Mitte kunagi     |

Ükski üldkulude arvutus, mis tehakse pärast 20. jaanuari 2017, ei arvesta enam seda reeglit.

> [!NOTE] 
> Väljad **Kehtiv alates** ja **Kehtiv kuni** sõltuvad kuupäevast ja kellaajast. Saate lasta reeglil aeguda ja käivitada samal päeval uue üldkulude arvutuse.

## <a name="define-dimension-hierarchies-for-security-setup"></a>Dimensioonihierarhiate määratlemine turvalisuse seadistuse jaoks

Kuluarvestuse andmed tuleb teha kättesaadavaks kõigile aruandlusüksuse eest vastutavatele juhtidele. Kuluarvestuse terminoloogias kajastatakse aruandlusüksust kuluobjekti või kuluobjektide kogumina.

Kõigil juhtidel võib olla juurdepääs väga tundlikele äriandmetele, nt tuludele ja marginaalidele. Seetõttu on oluline seadistada turvalisus, et juhid näeksid ainult enda jaoks olulisi andmeid. Andmete turvalisuse kontrollimiseks saate määratleda dimensioonihierarhiad.

- Dimensioonihierarhiate kasutamine kehtib ainult siis, kui dimensioonihierarhia viites valitud dimensiooniväärtus on kuluobjekti dimensioon.
- Juurdepääsuloendi hierarhias saab kuluobjekti dimensioonil aktiveerida ainult ühe dimensioonihierarhia.

**Dimensioonihierarhia üksikasjad**

| Dimensioonihierarhia nimi | Dimensioon    | Dimensiooni hierarhia tüübi nimi      | Juurdepääsuloendi hierarhia |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisatsioon             | Kulukeskused | Dimensiooni klassifitseerimishierarhia | **Jah**               |

Hierarhiakujundajas saab kasutada uut kiirkaarti **Kasutajad**. Siin saate sisestada igasse hierarhiasõlme vähemalt ühe kasutaja ID.

|                 | Kasutajad            | Dimensiooniliikmete vahemikud   |                         |
|-----------------|------------------|---------------------------|-------------------------|
| **Sõlmed**       | **Kasutaja ID**      | **Lähtedimensiooni liige** | **Sihtdimensiooni liige** |
| Organisatsioon    | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Administraator         | aprill            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finantsid   | Alicia           | CC002                     | CC003                   |
|                 |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personaliosakond        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Tootmine    | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakendamine | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Assembler  | Chris            | CC006                     | CC006                   |

> [!NOTE] 
> Kuluarvestajad tuleks määrata hierarhia ülemisele tasandile, et nad näeksid kuluarvestuses kõiki kirjeid.

Juurdepääsuloendi hierarhia ja selle turbesätete lubamiseks avage **Kuluarvestus** > **Seadistus** > **Parameetrid** > **Üldine**. Valige parameeter **Luba kuvamise juurdepääs kuluobjekti dimensiooniliikmete jaoks**.

Juurdepääsuloendi hierarhia sätteid kasutatakse järgmistel aladel kuvatavate andmete juhtimiseks.

- **Kulujuhtimise** tööruum (klient):

    - Andmed vormidel, mida kasutatakse süvitsimineku stsenaariumide puhul

- **Kulujuhtimise** tööruum (mobiilirakendus):

    - Saldod kaartidel

- Power BI:

    - Power BI visualiseeringutel kuvatavad andmed
    - Dynamics 365 Financei klientrakendusse manustatud Power BI andmevisualiseeringud

> [!NOTE] 
> - Enne kui juurdepääsuloendi hierarhia saab Power BI-s olevaid andmeid mõjutada, tuleb juurdepääsuloendi hierarhia ja rea tasemel turve Power BI-s siduda. Lisateavet leiate teemast [Kuluarvestuse sisupaketi jaoks turbe seadistamine](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Juurdepääsuloendi hierarhia ei aita kaitsta andmete eksportimist Excelisse. Seetõttu peaksid seda aruandlustööriista kasutama ainult kuluarvestajad ja juhid, kellel on vaja andmete vaatamiseks täielikku juurdepääsu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]