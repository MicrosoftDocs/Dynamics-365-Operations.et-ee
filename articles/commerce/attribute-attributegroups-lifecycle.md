---
title: Atribuutide ja atribuudigruppide haldamine
description: See artikkel kirjeldab, kuidas hallata atribuute ja atribuudigruppe, et kirjeldada tooteid ja nende omadusi Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.openlocfilehash: aad448ea733aabdff3dc4438dcb682d49e0665c0
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/31/2022
ms.locfileid: "9386968"
---
# <a name="manage-attributes-and-attribute-groups"></a>Atribuutide ja atribuudigruppide haldamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas hallata atribuute ja atribuudigruppe, et kirjeldada tooteid ja nende omadusi Microsoft Dynamics 365 Commerce.

*Atribuudid on* viis kirjeldada tooteid ja nende omadusi kasutaja määratletud väljade kaudu. Näited hõlmavad mälu mahtu, kõvaketta mahtu ja Energy Stari vastavust.

Atribuute saab seostada erinevate Commerce'i üksustega, nagu tootekategooriad ja kanalid, ning neile saab määrata vaikeväärtused. Kui atribuudid on seotud tootekategooriate või kanalitega, pärivad tooted need atribuudid ja vaikeväärtused. Atribuudi vaikeväärtused saab alistada üksiku toote tasemel, kanali tasemel või kataloogis.

Näiteks võivad tavapärasel teleril olla järgmised atribuudid.

| Kategooria   | Atribuut           | Lubatud väärtused                        | Vaikeväärtus |
|------------|---------------------|-------------------------------------------|---------------|
| Teler ja video | Tootemark               | Mis tahes kehtiv kaubamärgi väärtus                     | Pole          |
| TV         | Ekraani suurus         | 20–85 tolli                              | 55 tolli     |
|            | Vertikaallahendus | 4K (2160p), Full HD (1080p) või HD (720p) | 4K (2160p)    |
|            | Ekraani värskendussagedus | 60 Hz, 120 Hz või 240 Hz                     | 60 Hz          |
|            | HDMI-sisendid         | 0–10                                      | 3             |

## <a name="attributes-and-attribute-types"></a>Atribuudid ja atribuuditüübid

Atribuudid põhinevad *atribuuditüüpidel*. Atribuudi tüüp tuvastab andmetüübi, mida saab kindlale atribuudile sisestada. Commerce toetab järgmisi atribuuditüüpe:

- **Valuuta** – see tüüp toetab valuuta väärtust. Seda saab piirata (see tähendab, et see toetab väärtuste vahemikku) või jätta lahtiseks.
- **Kuupäev ja kellaaeg** – see tüüp toetab kuupäeva ja kellaaja väärtust. Seda saab piirata või jätta avatuks.
- **Kümnendkoht** – see tüüp toetab kümnendkohti sisaldavaid arvväärtusi. See toetab ka mõõtühikut. Seda saab piirata või jätta avatuks.
- **Täisarv** – see tüüp toetab arvväärtust. See toetab ka mõõtühikut. Seda saab piirata või jätta avatuks.
- **Tekst** – see tüüp toetab tekstväärtust. See toetab ka võimalike väärtuste eelmääratletud kogumeid, kui fikseeritud **loendi** säte on lubatud.
- **Kahendmuutuja** – see tüüp toetab binaarset väärtust (**tõene** või **väär**).
- **Viide** – see tüüp viitab teistele atribuutidele.

> [!NOTE]
> Azure’i [otsinguindeksi piirangute tõttu](/rest/api/searchservice/data-type-map-for-indexers-in-azure-search)**ei** toetata kümnendkoha atribuudi tüüpi pilve toetatud otsingukogemuste puhul. Azure’i cotive otsing **ei** **toeta kümnendkoha atribuuditüüpide teisendamist Edm-ks.Topeltsihtindeksi** väljatüübid, kuna see teisendamine vähendaks täpsust.

### <a name="set-up-attribute-types"></a>Saate häälestada atribuuditüüpe.

Atribuuditüüpide häälestamiseks järgige selle näidisprotseduuri samme.

1. Tootejuhina Commerce Headquartersi sisselogimine.
1. Minge tooteteabe **halduse häälestuskategooriate \>\> ja atribuutide atribuutide \> tüüpidele**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage **atribuudi tüübi nime** väljale koti **tüüp**.
1. Väljal **Tüüp** valige **Tekst**.
1. Seadke suvandi **Fikseeritud loend** väärtuseks **Jah**.
1. Valige väärtuste **kiirkaardil** käsk **Lisa**.
1. Sisestage uue rea väljale **Väärtus** **Sat sisestamist**.
1. Lisage veel viis rida. Iga väärtuse **väljale** sisestage erinev väärtus: **Clutch**, Purse **,** Backpack **,** **Messenger** või **Messenger**.
1. Valige toimingupaanil nupp **Salvesta**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage **atribuudi tüübi nime** väljale Firma **kaubamärk**.
1. Väljal **Tüüp** valige **Tekst**.
1. Seadke suvandi **Fikseeritud loend** väärtuseks **Jah**.
1. Valige väärtuste **kiirkaardil** käsk **Lisa**.
1. Sisestage uue rea väljale **Väärtus** **Konto keelamine**.
1. Lisage veel kaks rida. Iga väärtuse **väljale** sisestage erinev väärtus: **Aviator või** **Sisestusklahv**.
1. Valige toimingupaanil nupp **Salvesta**.

![Atribuuditüüpide leht.](media/AttributeType_2022Series.png)

### <a name="set-up-an-attribute"></a>Saate häälestada atribuudi.

Atribuudi häälestamiseks järgige selle näidisprotseduuri samme.

1. Tootejuhina Commerce Headquartersi sisselogimine.
1. Minge tooteteabe **halduse häälestuskategooriatele \>\> ja atribuutidele \>**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage **väljale** Nimi koti **tüüp**.
1. **Atribuudi tüübi väljal** valige koti **tüüp**.
1. Valige toimingupaanil nupp **Salvesta**.

![Atribuutide leht.](media/Attribute_2022Series.png)

## <a name="attribute-metadata"></a>Atribuudi metaandmed

*Atribuudi metaandmed* võimaldavad teil valida suvandid, mis määravad, kuidas iga toote atribuudid peaksid toimima. Näiteks saate määrata, kas atribuudid on vajalikud, kas neid saab kasutada otsinguteks ja kas neid kasutada filtrina.

Toodete korral saab atribuudi metaandmete sätteid allutada kanali tasemel.

Atribuudi atribuutide leht sisaldab **mitmeid** atribuudi metaandmetega seotud valikuid. Näiteks **kui** **·** **seadistate** valiku Saab täpsustada valikule Jah jaotises Ärikanalite atribuudi metaandmed, näidatakse atribuuti toodete täpsustamiseks või filtreerimiseks otsingutulemustes ja kategooriate sirvimise lehtedel. Atribuudi konfigureerimiseks piiritletavaks peate esmalt valima **tegevuspaanil** filtri sätted ja kinnitama atribuudi filtrisätted.

## <a name="filter-settings-for-attributes"></a>Atribuutide filtrisätted

Atribuutide filtrite sätted määravad, kuidas atribuudi filtreid kassas näidatakse. Atribuudi filtrisätetele juurdepääsemiseks valige tegevuspaanil **atribuudi** atribuutide lehel Suvand Filtri **sätted**.

Filtri **sätete leht** sisaldab järgmisi välju:

- **Nimi** – vaikimisi on see väli seadistatud atribuudi nime jaoks. Kuid te saate selle väärtust muuta.
- **Kuvamissuvand** – saadaval on järgmised suvandid.

    - **Üksik väärtus** – see suvand on saadaval järgmiste atribuuditüüpide jaoks: **kahendmuutuja**, **valuuta**, **kümnendkoht**, **täisarv** ja **tekst**. See võimaldab toodete loendilehtedel (nt kategooriate sirvimise ja tooteotsingu tulemuste lehekülgedel) määrata täpsustajatele ainult ühe väärtuse.
    - **Mitme väärtusega** – see suvand on saadaval järgmiste atribuuditüüpide jaoks: **valuuta**, **kümnendkoht**, **täisarv** ja **tekst**. See lubab täpsustamiseks valida kliendile atribuudi jaoks mitu väärtust.

- **Kuva juhtelement** – saadaval on järgmised suvandid.

    - **Loend** – see valik on saadaval kõigi atribuuditüüpide puhul.
    - **Vahemik** – see suvand on saadaval järgmiste atribuuditüüpide jaoks: **valuuta**, **kümnendkoht** ja **täisarv**.
    - **Liugur** – see suvand on saadaval järgmiste atribuuditüüpide jaoks: **valuuta**, **kümnendkoht** ja **täisarv**.
    - **Ribadega liugur** – see suvand on saadaval järgmiste atribuuditüüpide jaoks: **valuuta**, **kümnendkoht** ja **täisarv**.

- **Läveväärtus** – see säte on vajalik, kui valite kuva juhtelemendi tüübiks **Vahemik**. Saate väärtuste määratlemiseks eraldajana kasutada semikoolonit (;).

    Näiteks koti mahu atribuudi puhul, **·** **mille atribuudi tüüp on Täisarv**, **võib läviväärtus olla 10; 20; 50; 100; 200; 500; 1000; 1000; 5000**. Sel juhul kuvab kassa järgmised vahemikud. Vahemikud, kus tulemustekomplektis pole tooteid, kuvatakse tuhmina.

    - Vähem kui 10
    - 10–20
    - 20–50
    - 50–100
    - 100–200
    - 200–500
    - 500 või rohkem

Atribuutide filtrisätted on rakendatavad ainult toote atribuutidele ning neid saab kasutada tooteotsingu ja kategooriate sirvimise tulemuste piiritlemiseks. Need ei kehti kliendi otsingu või tellimuse otsingu kohta, kuigi samu atribuute saab kasutada kliendi- või tellimuseteabe rikastamiseks.

Ärimoodulite vaikesätetes ei ole Kuva **juhtelementide** **filtrisätete** (Vahemik, **Slaider** **ja Slaidur) jaoks saadaval ühtki boksist väljas tugi koos ribadega.** Kassalahenduste puhul toetatakse endiselt vahemiku ja slaidaja sätteid, **·** **samas kui ribadega slaididega säte on rakendatav pärandi võrgupoes ja on saadaval ka kolmanda osapoole integreerimise ja kohandatud stsenaariumite puhul.** **·** SharePoint

Soovitame, **·** **et** täpsustuse atribuutidel oleks atribuut Tekst, kus on lubatud suvand Fikseeritud loend, ning et seda loendit hallatakse (kuni 100–200 kordumatut väärtust). Kui täpsustajal on 1000 või rohkem kordumatut väärtust, on sobivam kasutada selle tekstitüübi atribuuti, **·** **mille** puhul on valik Fikseeritud loend keelatud.

Tõlked on atribuudinimede ja nende väärtuste jaoks kriitilise tähtsusega. Atribuutide jaoks, mille teksti **tüüp** on lubatud fikseeritud **loendi** suvandiga, saate atribuudiväärtuste jaoks määratleda tõlked atribuuditüübi **all**. Iga muu atribuuditüübi jaoks saate määratleda tõlked lehel, kus saate atribuudiväärtused määratleda. Näiteks atribuudi puhul, mille tüüp **on** Tekst, saate määratleda vaikeväärtuse tõlked atribuudi atribuutide **lehel**. Kuid kui alistate vaikeväärtuse tootetasemel, saate määratleda atribuudi tõlked toote atribuutide **lehel**.

Kui atribuut on märgitud kanali jaoks täpsemaks, ei tohiks atribuuditüüpi uuendada. Vastasel juhul mõjutate tooteandmete avaldamist otsinguindeksis. Soovitame selle asemel luua uue atribuudi uuele täpsustustüübile ja eemaldada eelmine atribuut teistest atribuudigruppidest.

Otsi atribuutide järgi on toetatud, kuid toob ainult otsingusõnade täpsed vasted. Näiteks kanga atribuudi **väärtus** on Cashmere **.** Kui klient otsib nime "Sularaha", ei **tooda ühtki toodet, mille kangaks on Cashmere ning mille kangaks on Cashmere**. Kui klient otsib siiski otsides "Cashmere", "Ekvivalendid" või "CashmereEkvivalendid", laaditakse tooted, **mille kangaks on Cashmere** riie.

### <a name="additional-attribute-metadata-options"></a>Atribuudi metaandmete lisasuvandid

> [!NOTE]
> Need atribuudi metaandmete suvandid on rakendatavad ainult pärandi SharePoint võrgupoes ja välisele integratsioonile. Lisateavet nende atribuutide metaandmete valikute kohta vt [Serveri 2013 otsinguskeemi SharePoint ülevaadet](/SharePoint/search/search-schema-overview).

Atribuutide lehel on saadaval ka järgmised lisaatribuudi **metaandmete** suvandid:

- Otsitav
- Saab tuua
- Saab päringusse kaasata
- Sorditav
- Suurtähtede ja vormingu eiramine
- Täielik vaste

Need suvandid olid algselt mõeldud pärandipõhiste võrgukaustade SharePoint otsingufunktsioonide täiustamiseks. Need ei pruugi kehtida commerce’i e-äri veebisaitide ega kassaterminalide puhul. Kuna peakontori integreerimist jätkatakse, on need suvandid saadaval atribuudi metaandmete eksportimiseks Commerce’i tarkvara arenduskomplekti (SDK) abil. Commerce SDK abil saate tooted panna kohandatud, optimeeritud välise otsingu indeksisse. Sel viisil saate tagada, et indekseeritakse ainult indekseeritud atribuudid.

## <a name="attribute-groups"></a>Atribuudigrupid

Atribuudigruppi *kasutatakse* komponendi või alamkomponendi üksikute atribuutide grupeerimiseks toote konfiguratsioonimudelis. Atribuudi saab lisada rohkem kui ühte atribuudigruppi. Atribuudigrupid saavad aidata kasutajatel tooteid konfigureerida, sest erinevad valikud on paigutatud kindlasse konteksti. Atribuudigruppe saab määrata kategooriatesse või kanalitele. Atribuudigrupis saate atribuutidele seadistada ka vaikeväärtused.

![Atribuudigruppide leht.](media/AttributeGroup_2022Series.png)

### <a name="create-an-attribute-group"></a>Looge atribuudigrupp

Atribuudigrupi loomiseks järgige selle näidisprotseduuri samme.

1. Tootejuhina Commerce Headquartersi sisselogimine.
1. Minge tooteteabe **halduse häälestuskategooriatesse \>\> ja atribuutide \> gruppidesse**.
1. Looge atribuudigrupp nimega **Särkide särk.**
1. Lisage järgmised atribuudid: **CleaningMethod,Type** **,** Collection **ja** **Design**.

> [!NOTE]
> Atribuudigrupi atribuutide kuvamisjärjestuse väärtused ei mõjuta või rakendu otsingu- ja kategooria sirvimistulemustes täpsustuste järjekorrale. Need on rakendatavad ainult stsenaariumi "tellimuse atribuudid" korral.

### <a name="assign-attribute-groups-to-categories"></a>Atribuudigruppide määramine kategooriatele

Üht või mitut atribuudigruppi saab kategooriasõlmedega seostada järgmiste kategooriahierarhiate tüüpides:

- Kaubanduse tootehierarhia
- Kanali navigeerimiskategooria hierarhia
- Täiendav tootekategooria hierarhia

Kui tooted on kategooriasse liigitatud kategooriates, mis on seotud atribuudigruppidega, pärivad need atribuudid, mis on nendesse atribuudigruppidesse kaasatud.

![Toote atribuudigruppide FastTab poe tootehierarhia lehel](media/AGRetailProdHierarchy_2022Series.png)

Atribuudigruppide määramiseks kategooriatele Commerce’i tootehierarhias järgige selle näidisprotseduuri samme.

1. Tootejuhina Commerce Headquartersi sisselogimine.
1. Avage **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Kaubanduse tootehierarhia**.
1. Valige mood **navigeerimishierarhia**.
1. Valige **Mens põhivarade** **all kategooria Plaanimine** **ja** seejärel lisage toote atribuudigruppide kiirkaardile **atribuudigrupp nimega Mehed.**
1. Valige kategooria **Moekad päikeseprillid** ja kinnitage uued atribuudid atribuudigrupis **Moekad päikeseprillid**, valides suvandi **Kuva atribuudid**. Atribuudigrupis peaksid olema uued atribuudid **Läätse kuju** ja **Päikeseprillide kaubamärk**.
1. Valige kategooria **Lisa** ja kontrollige meeste atribuudigrupi **atribuute**, valides Vaate **atribuudid**. Atribuudigrupp peaks sisaldama atribuute **Meeste vöö kaubamärk**, **Vöö materjal** ja **Vöö suurus**.

Sama põhiprotseduuri saab kasutada ka atribuudigruppide määramiseks kategooriatele kanali navigeerimiskategooria hierarhias ja täiendavale tootekategooria hierarhiale. Kasutage 2. sammus siiski ühte järgmistest teedest, sõltuvalt hierarhiast, millele soovite atribuudigrupid määrata:

- **Kanali navigeerimiskategooria hierarhia: minge** jaemüügi ja **äri kategooria ning \> tootehalduse kanali navigeerimiskategooriatesse \>**.
- **Täiendav tootekategooria hierarhia: minge** jaemüügi ja **äri kategooriasse \> ja tootehalduse täiendavad \> tootekategooriad**.

> [!NOTE]
> Veenduge, et seostate atribuudigrupid ainult kategooriahierarhias toote atribuudigruppide **kiirkaardiga, mitte kategooria** atribuudi väärtuste kiirkaardil **.** Kui atribuudid kuvatakse kiirkaardil **Kategooria atribuudiväärtused**, valige **tegevuspaanil** suvand Redigeeri kategooriahierarhiat. Seejärel valige kategooria atribuudigruppide **kiirkaardil** kategooria sõlm ja valige käsk **Eemalda**. Commerce Scale Uniti kaudu atribuutide toomist kategooria alusel ei toetata.

## <a name="identify-viewable-and-refinable-attributes-for-commerce-channels-for-the-default-product-collection"></a>Ärikanalite jaoks vaikimisi tootekogumi jaoks kuvatavate ja määratletavate atribuutide tuvastamine

Pärast erinevate hierarhiate kategooriatega erinevate atribuudigruppide seostamist (Commerce product hierarchy või channel navigation categories) ja määranud iga toote atribuudiväärtused kategooriaseose põhjal, peate lubama atribuudi Näita atribuuti kanali lipul, **et** need atribuudid oleks kindlas kanalis näha.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kanali kategooriad ja toote atribuudid**.
1. Valige **set atribuudi metaandmed** ja seejärel valige atribuut vasakul navigeerimispaanil.
1. Määrake kanali **toote atribuutide kiirkaardil** (mitte **kategooria atribuutide kiirkaart)** **·** **suvandi Kuva atribuut kanalil** väärtusele Jah, et atribuut oleks vaatatav.
1. Kui soovite, et atribuut oleks ka täpsustada, määrake suvandi **Saab täpsustada väärtuseks** Jah **·**.

### <a name="control-visibility-of-dimension-based-refiners-such-as-size-style-and-color"></a>Dimensioonipõhiste täpsustamiste nähtavuse (nt suurus, stiil ja värv) nähtavuse juhtimine

Kõige sagedamini kasutatavad spetsifikatsioonid on tootedimensioonid (nt suurus, stiil ja värv). Et need tootedimensioonid oleksid täpsemad, peaksite seostama kanali tasemel atribuudigrupi, mis sisaldab viidet atribuuditüübile, mis pärib automaatselt tootedimensiooni väärtuste väärtused.

Saate määrata, et tootedimensioonid on vaadatavad ja määratletavad, uuendades lippe **kanali kategooriate ja toote atribuutide** lehel. Valige navigeerimispaanil juursõlm ja **seadke seejärel kanali toote atribuutide kiirkaardil** **·** **suvandi** Kuva atribuut kanalis **väärtusele Jah atribuutide Suurus**, **·** **Stiil** ja Värv puhul. Kui soovite, et need atribuudid oleks ka täpsustatavad, määrake suvandi **Saab täpsustada väärtuseks** **Jah** iga puhul.

![Atribuudi metaandmete seadmine dimensioonide täpsustajatele.](./media/ProductDimensionRefinersMetadataSetup_2022Series.png)

Atribuutide lubamiseks nii, et need on saadaval demoandmepõhises Kanalis, järgige selle näidisprotseduuri samme.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kanali kategooriad ja toote atribuudid**.
1. Valige kanal **Houston**.
1. Valige tegumiribal suvand **Atribuudi metaandmete häälestamine**.
1. Valige kategooriasõlm **Mood** ja seejärel valige kiirkaardil **Kanali toote atribuudid** iga atribuudi jaoks suvand **Atribuudi kaasamine**.
1. Valige kategooriasõlm **Moeaksessuaarid**, valige kategooria **Moekad päikeseprillid** ja seejärel valige kiirkaardil **Kanali toote atribuudid** iga atribuudi jaoks suvand **Atribuudi kaasamine**.
1. Valige kategooriasõlm **Meeste rõivad**, valige kategooria **Püksid** ja seejärel valige kiirkaardil **Kanali toote atribuudid** iga atribuudi jaoks suvand **Atribuudi kaasamine**.
1. Pärast kavandatud atribuutide ja täpsustamiste atribuudi metaandmete värskendamist veenduge, et salvestate oma muudatused ja käivitate kanalivärskenduste **avaldamise** töö. Seejärel pärast uuenduste avaldamist peate käivitama järgmised tööd: 1070 (kanali konfiguratsioon), **1040** (**Tooted**) **ja 1150** (**kataloog**).**·** **·**

> [!NOTE]
> - Kui teie ettevõtte jaoks on vaja sageli lisada või eemaldada navigeerimishierarhiast tooteid või teha muudatusi, nt kuvada tellimuse väärtusi, lisada uusi kategooriaid ja lisada kategooriatele uusi atribuudigruppe, on soovitatav konfigureerida kanali uuenduste avaldamine nii, **et** see töötaks sagedase pakett-tööna. Teise võimalusena **käivitage** käsitsi kanali uuenduste avaldamise töö ja Commerce Data Exchange seejärel järgmised (CDX) tööd: **1070** (**Kanali** konfiguratsioon), **1040** (**Tooted**) ja **1150** (**kataloog**).
> - Päriluse **suvand** võimaldab teil määrata, et kanal peaks hierarhias atribuudigrupid oma emakanalist tuletama. Kui määrate suvandi **Päri** väärtuseks **Jah**, pärib alamkanali sõlm kõik atribuudigrupid ja nendes atribuudigruppides olevad atribuudid.
> - Kui tegevuspaanil **ei ole saadaval nupp Atribuudi metaandmete kogumi kogumi, veenduge,** **et navigeerimishierarhia on seostatud teie kanaliga kiirkaardil** **Üldine**.
> - Te ei tohi seostada ühtegi atribuudigruppi, **·** **välja arvatud dimensioonipõhised atribuudigrupid kanali tasemel (nt atribuudigruppide all kanali kategooriate ja toote atribuutide** lehel).
> - Pärast kliendispetsiifiliste ettevõtete (B2B) kataloogide toe sissejuhatust äriversioonis 10.0.27 soovite eeldatavalt tuvastada iga B2B kataloogi täpsustaja ja atribuutide seadistused samamoodi, nagu selles artiklis kirjeldatud.

## <a name="override-attribute-values"></a>Atribuudiväärtuste alistamine

Atribuutide vaikeväärtused saab toote tasemel individuaalsete toodete puhul alistada. Samuti saab neid alistada üksikute toodete puhul kindlates kataloogides, mis on mõeldud kindlatele kanalitele.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Individuaalse toote atribuudiväärtuste alistamine

Üksiku toote atribuudiväärtuste alistamiseks järgige selle näidisprotseduuri samme.

1. Tootejuhina Commerce Headquartersi sisselogimine.
1. Minge jaemüügi ja **äri kategooriasse \> ja tootehaldusesse Väljastatud \> tooted kategooriate alusel**.
1. Valige **moe lisad \>\>: mood, matid**.
1. Valige ruudustikust nõutav toode. Seejärel tehke tegumiriba vahekaardil **Toode** grupis **Häälesta** valik **Toote atribuudid**.
1. Valige vasakpoolsel paanil atribuut ja seejärel värskendage parempoolsel paanil selle väärtust.

![Toote atribuudiväärtuste leht.](media/ProdDetailsProdAttrValues_2022Series.png)

### <a name="override-the-attribute-values-of-all-products-in-a-catalog"></a>Alista kataloogi kõikide toodete atribuudiväärtused

Kataloogi kõikide toodete atribuudiväärtuste alistamiseks järgige selle näite protseduuri samme.

1. Tootejuhina Commerce Headquartersi sisselogimine.
1. Minge jaemüügi **ja ärikataloogi \> haldusse \> Kõik kataloogid**.
1. Valige kataloog **Fabrikam Base Catalog**.
1. Valige **moe lisad \>\>: mood, matid**.
1. Kiirkaardil **Tooted** valige nõutav toode ja seejärel valige tooteruudustiku kohal suvand **Atribuudid**.
1. Järgmistel kiirkaartidel värskendage nõutavate atribuutide väärtusi:

    - Ühiskasutuses tootemeedium
    - Ühised toote atribuudid
    - Kanali meedium
    - Kanali toote atribuudid

### <a name="override-the-attribute-values-of-all-products-in-a-channel"></a>Alista kõigi kanali toodete atribuudiväärtused

Kõigi kanali toodete atribuudiväärtuste alistamiseks järgige selle näite protseduuri samme.

1. Tootejuhina Commerce Headquartersi sisselogimine.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kanali kategooriad ja toote atribuudid**.
1. Valige kanal **Houston**.
1. Kiirkaardil **Tooted** valige nõutav toode ja seejärel valige tooteruudustiku kohal suvand **Atribuudid**.
1. Kui ühtki toodet pole **saadaval**, valige kiirkaardil **Tooted** suvand Lisa ja valige seejärel dialoogiboksis **Toodete lisamine vajalikud** tooted.
1. Järgmistel kiirkaartidel värskendage nõutavate atribuutide väärtusi:

    - Ühiskasutuses tootemeedium
    - Ühised toote atribuudid
    - Kanali meedium
    - Kanali toote atribuudid

### <a name="define-variant-specific-attribute-values-and-define-multiple-values-for-product-attributes"></a>Määratlege variandipõhised atribuudiväärtused ja määratlege toote atribuutidele mitu väärtust.

Variandispetsiifiliste atribuudiväärtuste määratlemiseks ja toote atribuutide mitme väärtuse määratlemiseks järgige selle näidisprotseduuri samme.

1. Tootejuhina Commerce Headquartersi sisselogimine.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kanali kategooriad ja toote atribuudid**.
1. Valige kanal **Houston**.
1. Valige kiirkaardil **Tooted** soovitud tootevariant ja seejärel valige atribuudid **tooteruudustiku** kohal.
1. Kui ühtki toodet pole **saadaval**, valige **kiirkaardil** Tooted suvand Lisa ja valige dialoogiaknas Toodete lisamine nõutavad **tootevariandid**.
1. Järgmistel kiirkaartidel värskendage nõutavate atribuutide väärtusi:

    - Ühiskasutuses tootemeedium
    - Ühised toote atribuudid
    - Kanali meedium
    - Kanali toote atribuudid

#### <a name="example-of-variant-specific-attribute-configuration"></a>Variandipõhise atribuudi konfiguratsiooni näide
        
Selles näites on P001-Master toode mitmekordne tegevus, **milles on kolm varianti:** Running,Avi **·** **ja** Trekking.**·** Iga variandi puhul soovite tegevuse atribuudi väärtuse kordumatult **määratleda**. **Kanali kategooriate** ja **toote** atribuutide lehe toodete kiirkaardil määrate variantide jaoks tegevuse atribuudi väärtuse, **nagu** näidatud järgmises tabelis.

| Variant     | Tegevuse atribuudi väärtus |
|-------------|--------------------------|
| P001-juht | Sport                   |
| P001-1 (üks)      | Töötab                  |
| Lk 2      | Jalutamine                  |
| Lk 3      | Trekking                 |

Kui kasutaja otsib otsingutulemustes sõna "jati", **ilmub otsingutulemustes P001-põhitoode**. Kui konfigureerite **tegevuse** atribuudi määratletavaks, **·** **loetleb tegevuse täpsustaja vaid määratletava väärtusena ainult Spordi**,**·** **sest see väärtus määratleti tegevuse atribuudile P001-Master toote** tasemel.

Vaikimisi on varianditaseme atribuudid mõeldud kasutamiseks ainult toote üksikasjade lehtedel (PDP-d). Kui valite PDP-s konkreetse tootevariandi, uuendatakse PDP toote spetsifikatsioone selle konkreetse variandi jaoks.

Et täpsustada atribuudiväärtusi, mis on määratletud tootevariandi tasemel, peate määratlema atribuudi tooteetribuudi tasemel, **valima** märkeruudu Luba mitu väärtust ja määrama atribuudi tüübiks **Tekst**.

Seejärel peate määratlema kõik võimalikud väärtused oma tootevariantide jaoks. Selles **näites** **kasutatud** tegevuse atribuudi puhul võivad võimalikud väärtused olla näiteks **Running** (Käivitatud),Kogunne (**Kogun** **·** **·** **) jaKogu**(Kogun) võiKogud (Kogu **) jaKogud** (Kogud).

Pärast seda, kui olete määratlenud variandiatribuudi väärtused, saate need määratleda tooteetribuudi tasemel, kasutades pipe-eraldatud väärtusi. Tegevuse atribuudi **jaoks** võite määratleda tooteetribuudi väärtuse tooteetribuudi väärtuseks Running **(Käivitatud| Väljaminev| Väljaminev| Trekk| Sma| Vesimärgid| Omased**

Seejärel saate iga variandi jaoks määrata atribuudiväärtused, sisestades kas pipe-eraldatud väärtused või üksikud väärtused. Tegevuse atribuudi **puhul** võite üksiku tootevariandi konfigureerida väärtuseks Running **(Käitamine| Väljaminev|,** jooksev **·**, **jooksev| Väljaminev| Vesimärgid** jne.

Kui olete variandi atribuudiväärtused määranud, **·** **·** **valige tegevuspaanil kanali kategooriate ja toote atribuutide lehel suvand Avalda kanali värskendused ning käivitage siis tööd 1150**, **1040** **ja 1070.**

Kui tööd on lõpetatud ja otsinguindeks on uuendatud, peaksid kõik eeldatavad väärtused ilmuma otsingutulemustes ja kategooriate sirvimise tulemustes.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
