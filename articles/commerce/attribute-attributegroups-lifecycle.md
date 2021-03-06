---
title: Atribuutide ja atribuudigruppide haldamine
description: Selles teemas kirjeldatakse, kuidas kasutada atribuute, et võimaldada kasutaja määratletud väljade kaudu toote ja selle omaduste kirjeldamist.
author: ashishmsft
ms.date: 04/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategoryAttribute, EcoResProductEntityAttributeTableFieldAssociation, EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResAttributeType, EcoResAttributeValue, EcoResCategoryAttributeGroup, EcoResCategoryFriendlyName
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.openlocfilehash: a49a0d05a55e72b5dae17933d38d03287a01d5ee
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936800"
---
# <a name="manage-attributes-and-attribute-groups"></a>Atribuutide ja atribuudigruppide haldamine

[!include [banner](includes/banner.md)]

*Atribuudid* võimaldavad täpsemalt kirjeldada toodet ja selle omadusi kasutaja määratud väljade kaudu (nagu **mälu suurus**, **kõvaketta maht**, **vastavus energiatähisele** jne). Atribuute saab seostada erinevate Commerce'i üksustega, nagu tootekategooriad ja kanalid, ning neile saab määrata vaikeväärtused. Tooted pärivad seejärel atribuudid ja atribuutide vaikeväärtused, kui need seostatakse tootekategooriate või kanalitega. Vaikeväärtusi saab alistada üksiku toote tasemel, kanali tasemel või kataloogis.


Näiteks võivad tavapärasel teleril olla järgmised atribuudid.

| Kategooria   | Atribuut                | Lubatud väärtused          | Vaikeväärtus |
|------------|--------------------------|-----------------------------|---------------|
| Teler ja video | Tootemark                    | Mis tahes kehtiv kaubamärgi väärtus       | None          |
| Teler         | Ekraani suurus              | 20–80 tolli                | None          |
|            | Vertikaallahendus      | 480i, 720p, 1080i või 1080p | 1080p         |
|            | Ekraani värskendussagedus      | 60 Hz, 120 Hz või 240 Hz       | 60 Hz          |
|            | HDMI-sisendid              | 0–10                        | 3             |
|            | DVI-sisendid               | 0–10                        | 1             |
|            | Koondsisendid         | 0–10                        | 2             |
|            | Komponendi sisendid         | 0–10                        | 1             |
| LCD        | 3D-valmidus                 | Jah või Ei                   | Jah           |
|            | 3D lubatud               | Jah või Ei                   | Ei            |
| Plasma     | Töötemperatuur alates      | 32–110 kraadi              | 32            |
|            | Töötemperatuur kuni        | 32–110 kraadi              | 100           |
| Projektsioon | Projektsioonitoru garantii | 6, 12 või 18 kuud         | 12            |
|            | Projektsioonitorude \#   | 1–5                         | 3             |

## <a name="attributes-and-attribute-types"></a>Atribuudid ja atribuuditüübid

Atribuudid põhinevad *atribuuditüüpidel*. Atribuudi tüüp tuvastab andmete tüübi, mida saab konkreetse atribuudi jaoks sisestada. Kasutatakse järgmisi toetatud atribuudi tüüpe.

- **Valuuta** – see tüüp toetab valuuta väärtust. Seda saab piirata (see tähendab, et see toetab väärtuste vahemikku) või jätta lahtiseks.
- **Kuupäev ja kellaaeg** – see tüüp toetab kuupäeva ja kellaaja väärtust. Seda saab piirata või jätta avatuks.
- **Kümnendkoht** – see tüüp toetab kümnendkohti sisaldavaid arvväärtusi. See toetab ka mõõtühikut. Seda saab piirata või jätta avatuks.
- **Täisarv** – see tüüp toetab arvväärtust. See toetab ka mõõtühikut. Seda saab piirata või jätta avatuks.
- **Tekst** – see tüüp toetab tekstväärtust. See toetab ka eelmääratletud võimalike väärtuste kogumit (st *loetelu*).
- **Kahendmuutuja** – see tüüp toetab binaarset väärtust (**tõene** või **väär**).
- **Viide** – see tüüp viitab teistele atribuutidele.

### <a name="set-up-attribute-types"></a>Saate häälestada atribuuditüüpe.

1. Logige sisse varukontori klienti tootejuhina.
2. Minge jaotisse **Tooteteabe haldus** &gt; **Seadistus** &gt; **Kategooriad ja atribuudid** &gt; **Atribuuditüübid**.
3. Looge kaks atribuuditüüpi, mille tüüp on **tekst**, määrake suvand **Fikseeritud loend** väärtusele **Jah** ja lisage väärtuste loend.

    - Andke ühele atribuuditüübile nimeks **Läätse kuju** ja lisage järgmised väärtused: **Ovaalne**, **Ruudukujuline** ja **Ristkülikukujuline**.
    - Andke teisele atribuuditüübile nimeks **Päikeseprillide kaubamärk** ja lisage järgmised väärtused: **Ray ban**, **Aviator** ja **Oakley**.

![Atribuuditüübid](media/AttributeType.png)

### <a name="set-up-an-attribute"></a>Saate häälestada atribuudi.

1. Logige sisse varukontori klienti tootejuhina.
2. Minge jaotisse **Tooteteabe haldus** &gt; **Seadistus** &gt; **Kategooriad ja atribuudid** &gt; **Atribuudid**.
3. Looge atribuut nimega **Lääts**.
4. Määrake välja **Atribuudi tüüp** väärtuseks **Läätse kuju**.

![Atribuudid](media/Attribute.png)

## <a name="attribute-metadata"></a>Atribuudi metaandmed

*Atribuudi metaandmed* võimaldavad teil valida suvandid, mis määravad, kuidas iga toote atribuudid peaksid toimima. Näiteks saate määrata, kas atribuudid on vajalikud, kas neid saab kasutada otsinguteks ja kas neid kasutada filtrina.

Toodete korral saab atribuudi metaandmete sätteid allutada kanali tasemel. Seda võimalust käsitletakse selles teemas allpool.

Võite märgata, et leht **Atribuudid** sisaldab suvandeid, mis on seotud atribuudi metaandmetega. Jaotises **POSi atribuudi metaandmed** mõjutab üks suvand nimega **Saab täpsustada** atribuudiväärtuste käitumist kassas või viisi, kuidas süsteem neid atribuudiväärtusi töötleb. Ainult atribuudid, mille jaoks saab suvandi **Saab täpsustada** määrata väärtusele **Jah**, kuvatakse kassas toodete täiustamise või filtreerimise jaoks.

Siin on ülejäänud atribuudi metaandmete suvandid lehel **Atribuudid**:

- Otsitav
- Saab tuua
- Saab päringusse kaasata
- Sorditav
- Mitme väärtuse lubamine
- Suurtähtede ja vormingu eiramine
- Täielik vaste

Need suvandid olid algselt ette nähtud veebipoe fassaadi otsingufunktsiooni täiustamiseks. Kuigi Commerce ei sisalda valmiskujul veebipoe fassaadi, sisaldab see lahendust eCommerce Publishing Software Development Kit (SDK). Kliendid saavad seda SDK-d kasutada toodete panemiseks enda valitud otsinguindeksisse. Kuigi tooteandmed imporditakse, peaksid kliendid siiski saama eristada otsitavaid andmeid, andmeid, mille kohta saab esitada päringuid jne. Sel viisil saavad nad luua optimaalse indeksi veendumaks, et nad indekseerivad ainult atribuute, mida *nende hinnangul* tuleb indekseerida.

Teavet ülejäänud suvandite otstarbe kohta vt teemast [SharePoint Server 2013 otsinguskeemi ülevaade](/SharePoint/search/search-schema-overview).

## <a name="filter-settings-for-attributes"></a>Atribuutide filtrisätted

Atribuutide filtrisätted võimaldavad teil määratleda, kuidas kuvatakse kassas atribuutide filtreid. Atribuudi filtrisätetele juurdepääsemiseks valige lehel **Atribuudid** atribuut ja seejärel valige toimingupaanil suvand **Filtrisätted**.

Leht **Filtri kuvamise eelistused** sisaldab järgmisi välju.

- **Nimi** – vaikimisi on see väli seadistatud atribuudi nime jaoks. Kuid te saate selle väärtust muuta.
- **Kuvamissuvand** – saadaval on järgmised suvandid.

    - **Üksik väärtus** – see suvand on saadaval järgmiste atribuuditüüpide jaoks: **kahendmuutuja**, **valuuta**, **kümnendkoht**, **täisarv** ja **tekst**. See suvand lubab kliendis piiritlemise eesmärgil nende atribuutide jaoks valida üksikväärtuse.
    - **Mitme väärtusega** – see suvand on saadaval järgmiste atribuuditüüpide jaoks: **valuuta**, **kümnendkoht**, **täisarv** ja **tekst**. See suvand lubab kliendis piiritlemise eesmärgil selle atribuudi jaoks valida mitu väärtust.

- **Kuva juhtelement** – saadaval on järgmised suvandid.

    - **Loend** – see suvand on saadaval kõigi atribuuditüüpide jaoks.
    - **Vahemik** – see suvand on saadaval järgmiste atribuuditüüpide jaoks: **valuuta**, **kümnendkoht** ja **täisarv**.
    - **Liugur** – see suvand on saadaval järgmiste atribuuditüüpide jaoks: **valuuta**, **kümnendkoht** ja **täisarv**.
    - **Ribadega liugur** – see suvand on saadaval järgmiste atribuuditüüpide jaoks: **valuuta**, **kümnendkoht** ja **täisarv**.

- **Läveväärtus** – see säte on vajalik, kui valite kuva juhtelemendi tüübiks **Vahemik**. Saate väärtuste määratlemiseks eraldajana kasutada semikoolonit (;).

    Näteks, filtri **Koti maht** jaoks saab läveväärtus olla **10; 20; 50; 100; 200; 500; 1000; 5000**. Sel juhul kuvab kassa järgmised vahemikud. Kõik vahemikud, millel pole tulemikomplektis ühtegi toodet, kuvatakse tuhmina.

    - Vähem kui 10
    - 10–20
    - 20–50
    - 50–100
    - 100–200
    - 200–500
    - 500 või rohkem

![Atribuudi filtrisätted](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a>Atribuudigrupid

Kui atribuudid on määratletud, saab need määrata atribuudigruppidesse. *Atribuudigruppi* kasutatakse individuaalsete atribuutide grupeerimiseks toote konfiguratsioonimudeli komponendi või alamkomponendi jaoks. Atribuudi saab lisada rohkem kui ühte atribuudigruppi. Atribuudigrupid saavad aidata kasutajatel tooteid konfigureerida, sest erinevad valikud on paigutatud kindlasse konteksti. Atribuudigruppe saab määrata kategooriatesse või kanalitele.

Saate ka määrata vaikeväärtusi atribuutidele, mis kuuluvad atribuudigruppi. Näiteks saate atribuudigruppi lisada värvi atribuudi ja valida atribuudi vaikeväärtuseks **Sinine**. Sel juhul, kui atribuudigrupp lisatakse tootele, mis sisaldab ühe atribuudina värvi, on selle toote vaikevärv **sinine**.

![Atribuudigrupid](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a>Looge atribuudigrupp

1. Logige sisse varukontori klienti tootejuhina.
2. Minge jaotisse **Tooteteabe haldus** &gt; **Seadistus** &gt; **Kategooriad ja atribuudid** &gt; **Atribuudigrupid**.
3. Looge atribuudigrupp, mille nimi on **Moekad päikeseprillid**.
4. Lisage järgmised atribuudid: **Läätse kuju** ja **Päikeseprillide kaubamärk**.

### <a name="assign-attribute-groups-to-categories"></a>Atribuudigruppide määramine kategooriatele

Järgmist tüüpi kategooriahierarhiates saab kategooriasõlmedega seostada ühe või mitu atribuudigruppi: Commerce'i tootehierarhia, kanali navigeerimiskategooria hierarhia ja täiendav tootekategooria hierarhia. Seejärel pärivad tooted kategoriseerimisel atribuudigruppidesse kaasatud atribuudid.

![Tootehierarhia – toote atribuudigrupid](media/AGRetailProdHierarchy.PNG)

Järgige neid samme, et määrata atribuudigruppe Commerce'i tootehierarhias gruppidesse.

1. Logige sisse varukontori klienti tootejuhina.
2. Avage **Jaemüük ja kaubandus** &gt; **Kategooria- ja tootehaldus** &gt; **Commerce'i tootehierarhia**.
3. Valige **Moe navigeerimishierarhia**.
4. Jaotises **Meeste rõivad** valige kategooria **Püksid** ja seejärel kiirkaardil **Toote atribuudigrupid** lisage atribuudigrupp nimega **Meeste vöö**.
5. Valige kategooria **Moekad päikeseprillid** ja kinnitage uued atribuudid atribuudigrupis **Moekad päikeseprillid**, valides suvandi **Kuva atribuudid**.

    Atribuudigrupis peaksid olema uued atribuudid **Läätse kuju** ja **Päikeseprillide kaubamärk**.

6. Jaotises **Meeste rõivad** valige kategooria **Püksid** ja kinnitage atribuudigrupi **Meeste vöö** atribuudid, valides suvandi **Kuva atribuudid**.

    Atribuudigrupp peaks sisaldama atribuute **Meeste vöö kaubamärk**, **Vöö materjal** ja **Vöö suurus**.

> [!NOTE]
> Seda toimingut saab kasutada ka atribuudigruppide määramiseks kategooriatesse kanali navigeerimiskategooria hierarhias ja täiendavas tootekategooria hierarhias. 2. etapis kasutage järgmisi navigeerimisteid:
>
> - Jaemüük ja kaubandus &gt; Kategooria ja toote haldus &gt; Kanali navigeerimiskategooriad
> - Jaemüük ja kaubandus &gt; Kategooria ja toote haldus &gt; Täiendavad tootekategooriad

### <a name="assign-attribute-groups-to-stores"></a>Atribuudigruppide määramine kauplustele

Kaupluse hierarhia ühe või mitme kauplusega saab seostada ühe või mitu atribuudigruppi. Seejärel, kui tooteid rikastatakse kindlate Kaupluste jaoks, pärivad need atribuudigruppidesse kaasatud atribuudid.

1. Logige sisse varukontori klienti tootejuhina.
2. Avage **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kanali kategooriad ja toote atribuudid**.
3. Määrake atribuudigrupid kanalile Houston:

    1. Valige kanal **Houston**.
    2. Kiirkaardil **Atribuudigrupp** valige **Lisa** ja seejärel väljal **Nimi** valige **SharePointProvisionedProductAttributeGroup**.
    3. Valige uuesti **Lisa** ja seejärel väljal **Nimi** valige **Meeste vöö**.
    4. Valige uuesti **Lisa** ja seejärel väljal **Nimi** valige **Moekad päikeseprillid**.

        > [!NOTE]
        > Suvand võimaldab teil määrata, et see kanal peaks pärima atribuudigrupid oma emakanalilt hierarhias. Kui määrate suvandi **Päri** väärtuseks **Jah**, pärib alamkanali sõlm kõik atribuudigrupid ja nendes atribuudigruppides olevad atribuudid.

4. Lubage atribuudid, et need oleksid saadaval kanalil Houston:

    1. Valige tegumiribal suvand **Atribuudi metaandmete häälestamine**.
    2. Valige kategooriasõlm **Mood** ja seejärel valige kiirkaardil **Kanali toote atribuudid** iga atribuudi jaoks suvand **Atribuudi kaasamine**.
    3. Valige kategooriasõlm **Moeaksessuaarid**, valige kategooria **Moekad päikeseprillid** ja seejärel valige kiirkaardil **Kanali toote atribuudid** iga atribuudi jaoks suvand **Atribuudi kaasamine**.
    4. Valige kategooriasõlm **Meeste rõivad**, valige kategooria **Püksid** ja seejärel valige kiirkaardil **Kanali toote atribuudid** iga atribuudi jaoks suvand **Atribuudi kaasamine**.

![Kanali kategooriad ja toote atribuudid – atribuudigrupid](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a>Atribuudi väärtuste alistamine

Atribuutide vaikeväärtused saab toote tasemel individuaalsete toodete puhul alistada. Vaikeväärtused saab ka kindlatele kanalitele sihitud kindlates kataloogides olevate üksikute toodete puhul alistada.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Individuaalse toote atribuudiväärtuste alistamine

1. Logige sisse varukontori klienti tootejuhina.
2. Avage **Jaemüük ja kaubandus** &gt; **Kategooria ja toote haldus** &gt; **Väljastatud tooted kategooriate alusel**.
3. Valige kategooriasõlm **Mood** &gt; **Moeaksessuaarid** &gt; **Moekad päikeseprillid**.
4. Valige ruudustikust nõutav toode. Seejärel tehke tegumiriba vahekaardil **Toode** grupis **Häälesta** valik **Toote atribuudid**.
5. Valige vasakpoolsel paanil atribuut ja seejärel värskendage parempoolsel paanil selle väärtust.

![Toote üksikasjade leht – toote atribuudigrupid](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a>Kataloogis olevate toodete atribuudiväärtuste alistamine

1. Logige sisse varukontori klienti tootejuhina.
2. Avage **Jaemüük ja kaubandus** &gt; **Tootekataloogi haldus** &gt; **Kõik kataloogid**.
3. Valige kataloog **Fabrikam Base Catalog**.
4. Valige kategooriasõlm **Mood** &gt; **Moeaksessuaarid** &gt; **Moekad päikeseprillid**.
5. Kiirkaardil **Tooted** valige nõutav toode ja seejärel valige tooteruudustiku kohal suvand **Atribuudid**.
6. Järgmistel kiirkaartidel värskendage nõutavate atribuutide väärtusi:

    - Ühiskasutuses tootemeedium
    - Ühised toote atribuudid
    - Kanali meedium
    - Kanali toote atribuudid

    > [!NOTE]
    > Kui luuakse ühiskasutuses tootemeedium ja ühised toote atribuudid, kehtivad need kõigile toodetele.

![Kataloogi toote atribuudigrupid](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a>Kanalil olevate toodete atribuudiväärtuste alistamine

1. Logige sisse varukontori klienti tootejuhina.
2. Avage **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kanali kategooriad ja toote atribuudid**.
3. Valige kanal **Houston**.
4. Kiirkaardil **Tooted** valige nõutav toode ja seejärel valige tooteruudustiku kohal suvand **Atribuudid**.

    > [!NOTE]
    > Kui tooteid pole saadaval, lisage tooteid, valides kiirkaardil **Tooted** suvandi **Lisa** ja seejärel valides nõutavad tooted dialoogiboksis **Lisa tooted**.

5. Järgmistel kiirkaartidel värskendage nõutavate atribuutide väärtusi:

    - Ühiskasutuses tootemeedium
    - Ühised toote atribuudid
    - Kanali meedium
    - Kanali toote atribuudid

    > [!NOTE]
    > Kui luuakse ühiskasutuses tootemeedium ja ühised toote atribuudid, kehtivad need kõigile toodetele.


[!INCLUDE[footer-include](../includes/footer-banner.md)]