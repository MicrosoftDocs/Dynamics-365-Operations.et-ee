---
title: Ohtlike materjalide seadistamine
description: Selles teemas selgitatakse, kuidas häälestada andmeid, mis on nõutavad kauba liigitamiseks ohtlike materjalidena. Kui loote müügitellimuse, mis sisaldab kaupa, mis on liigitatud ohtlikuks materjaliks, genereerib süsteem müügitellimuse saatmisel selle müügitellimuse jaoks ohtliku materjali dokumentatsiooni.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: db0d78c7a6fa69aa4e0c4c82f92c33daabda073f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983337"
---
# <a name="set-up-hazardous-materials"></a>Ohtlike materjalide seadistamine

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Ohtlike materjalide funktsiooni kasutamiseks peate esmalt häälestama andmed, mis on vajalikud kaupade liigitamiseks ohtlike materjalidena. Seejärel, kui loote müügitellimuse, mis sisaldab kaupa, mis on liigitatud ohtlikuks materjaliks, genereerib süsteem müügitellimuse saatmisel selle müügitellimuse jaoks ohtliku materjali dokumentatsiooni.

## <a name="turn-on-the-hazardous-materials-feature-for-your-system"></a>Süsteemi ohtlike materjalide funktsiooni sisselülitamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *Tooteteabe haldus*
- **Funktsiooni nimi:** *Toote ohtlike materjalide teave ja saatmisdokumentatsioon*

## <a name="hazardous-material-regulations"></a>Ohtliku materjali määrused

Ohtlike materjalide protsesside kasutamiseks peate esmalt looma määruse. Määrused määratlevad, kuidas kauba jaoks luuakse saadetisse prinditav tekst. Samuti määratletakse nendega seotud tarneviisid.

Siin on mõned ühised määrused:

- **ADR** – määrused, mis on seotud ohtlike kaupade rahvusvahelise autoveoga
- **CFR 49** – Ameerika Ühendriikide määrused ohtlike kaupade veo kohta
- **IMDG** – rahvusvaheline ohtlike kaupade (IMDG) kood
- **IATA** – Rahvusvahelise Lennutranspordi Assotsiatsiooni (IATA) ohtlike kaupade määrused

Need määrused aitavad määratleda, milline teave tuleb kuvada, kui prindite kaubasaadetise teksti. Saate määratleda nii palju määrusi, kui peate järgima.

> [!IMPORTANT]
> Ohtlike materjalidega seotud teabekoodide häälestamise funktsioon ei vii teie ettevõtet määrustega vastavusse. See on ainult tööriist, mis aitab teil oma ettevõtte jaoks protsesse luua.

Tavaliselt on määrus saadaval kindla transpordiliigi, näiteks mere-, maantee- või õhutranspordi jaoks. Seetõttu saate iga määruse seostada tarneviisiga. Tarneviisi kasutatakse, kui laohalduses prinditakse kindlaid dokumente. Laohalduses on iga saadetis lingitud lähetuse vedaja ja vedaja teenusega, mis on häälestatud moodulis **Transport**. Tarneviis on seostatud saadetise vedaja ja vedaja teenusega. Aruande käivitamisel kasutatakse tarneviisi, et leida väljastatud kaubaga seostatud saadetise prinditava tekstiga.

Need häälestusandmed pole spetsiifilised iga juriidilise isiku (ettevõtte) jaoks. Seetõttu võib teil olla ohtlike materjalide teabe ühine kogum, mis on jagatud kõigi teie juriidiliste isikute vahel.

Iga määruse jaoks saate määratleda materjalide loendi ja kasutada seda mallina, mis on seotud väljastatud kaupadega. Iga määruse puhul saate määratleda ka printimishäälestuse. Printimishäälestus võimaldab teil määratleda, kuidas koostada kauba saatmisteksti. Printimishäälestust kasutatakse väljastatud kauba saadetisse prinditava teksti koostamiseks.

Ohtlike materjalide määruste häälestamiseks avage **Tooteteabe halduse \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtlike materjalide määrus**. Lehel **Ohtlike materjalide määrus** saate luua suvalise arvu määrusi ja konfigureerida neid väljade abil, mida kirjeldatakse järgmistes alajaotustes.

### <a name="hazardous-material-regulation-header"></a>Ohtliku materjali määruse päis

Igal määrusel on kood ja kirjeldus. Järgmises tabelis on kirjeldatud päises olevaid välju.

| Field | Kirjeldus |
|---|---|
| Määruse kood | Saate sisestada koodi ohtliku materjali määruse kirje tuvastamiseks. |
| Kirjeldus | Saate sisestada ohtliku materjali määruse kirjelduse. |

### <a name="print-setup-fasttab"></a>Printimishäälestuse kiirkaart

Igal määrusel võib olla mistahes arv printimishäälestusi. Printimishäälestuse saate määratleda kiirkaardil **Printimishäälestus**. Järgmises tabelis kirjeldatakse igas printimishäälestuses saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Seeria | Saate määratleda järjekorra, milles väljadele saatmistekstis viidatakse. |
| Prindiväli | Valige väli, mida saatmisteksti kaasata. Printimiseks pole kõik ohtlike materjalide väljad saadaval. Saadaval on ainult ühised väljad, mida kasutatakse saatmisteksti määratlemiseks erinevates määrustes. Esimese prinditava välja peate määratlema välja eraldajana, mille väärtus **Järjestus** on *0* (null), et seda saaks kasutada eraldajana teiste väljade vahel. Nõutav on ainult üks viide väljaeraldajale.<p>Saadaval on järgmised väärtused:</p><ul></li><li>**Väljaeraldaja** – seda prindivälja kasutatakse teksti väljaeraldajana. Järjestuses on nõutav ainult üks viide väljaeraldajale. Tavaliselt peaksite selle prindivälja väärtuse **Järjestus** jaoks olema seatud väärtus *0* (null). Süsteem otsib väljaeraldajat ja kasutab esimest väljaeraldajat, mille ta loendist leiab. Stringis kasutatav tekstiväärtus pärineb väljalt **Prindi pärast**.</li><li>**ID** – see prindiväli seab prinditavale tekstile [ID ja/või kirjelduse](#identification).</li><li>**Klass** – see prindiväli seab prinditavale tekstile [klassi koodi ja/või kirjelduse](#classes).</li><li>**Jaotus** – see prindiväli seab prinditavale tekstile [jaotise koodi ja/või kirjelduse](#divisions).</li><li>**Pakkimisgrupp** – see prindiväli seab prinditavale tekstile [pakkimisgrupi koodi ja/või kirjelduse](#packing-group).</li><li>**Tunneli kood ja/või kirjeldus** – see prindiväli seab prinditavale tekstile [tunneli koodi ja/või kirjelduse](#tunnel).</li><li>**Õige saadetise nimi** – prindiväljal seatakse prinditavasse teksti [õige saadetise nimi](hazmat-items.md#hazmat-description).</li><li>**Tehniline nimi** – see prindiväli seab prinditavale tekstile [tehnilise nime ja/või kirjelduse](#technical-name).</li><li>**Transpordikategooria** – see prindiväli seab prinditavale tekstile [transpordikategooria koodi ja/või kirjelduse](#transport-category).</li><li>**Laadimine** – see prindiväli seab prinditavale tekstile [laadimiskoodi ja/või kirjelduse](#stowage).</li><li>**Fikseeritud tekst** – see prindiväli sisestab teksti, mis on määratletud selle rea väljal **Fikseeritud tekst**.</li><li>**Sildi kood ja/või kirjeldus** – see prindiväli seab prinditavale tekstile [sildi koodi ja/või kirjelduse](#label).</li><li>**Pakkimine lennuveoks** – see prindiväli seab prinditavale tekstile [lennuveoks pakkimise juhendi koodi ja/või kirjelduse](#packing-instruction).</li><li>**Piiratud kogus** – see prindiväli kontrollib, kas kaua märkeks on [piiratud kogusega kaup](hazmat-items.md#material-management) ja sel juhul sisestab teksti, mis on määratletud selle rea väljal **Fikseeritud tekst**.</li><li>**Pakkimiskirjeldus** – see prindiväli seab prinditavale tekstile [pakkimiskirjelduse](#packing-description).</li></ul> |
| Prindi enne | Saate sisestada teksti, mis tuleks printida enne sisu, mis on määratud sättega **Prindiväli**. |
| Prindi pärast | Saate sisestada teksti, mis tuleks printida pärast sisu, mis on määratud sättega **Prindiväli**. |
| Prindi koos eelmisega | Märkige see ruut, et vältida väljaeraldaja printimist eelmise välja ja selle välja vahel. Kasutage seda märkeruutu prindiväljadele, mis on kas valikulised või kaasatud mõne muu prindiväljaga. |
| Fikseeritud tekst | Kui määrate **prindiväljaks** väärtuse **Fikseeritud tekst** või **Piiratud kogus**, sisestage prinditav tekst. |
| Kaasa printimisel | Valige, millist väärtust või väärtusi valitud prindiväljalt tuleks selle rea puhul printida. Saate printida koodi, kirjelduse või nii koodi kui ka kirjelduse. |

### <a name="mode-of-delivery-fasttab"></a>Tarneviisi kiirkaart

Määrus on ühiskasutatav tabel ja see ei ole iga juriidilise isiku puhul spetsiifiline. Kuid tarneviisid on juriidilise isiku kohased. Seetõttu peate tarneviisi häälestamisel valima määruse, juriidilise isiku ja tarneviisi vahelise seose.

Järgmises tabelis on kirjeldatud kiirkaardil **Tarneviis** olevaid välju.

| Field | Kirjeldus |
|---|---|
| Ettevõte | Saate valida selle määrusega seostatud juriidilise isiku. |
| Tarneviis | Valitud juriidilise isiku põhjal saate valida määrusega seostatava tarneviisi. |

### <a name="country-fasttab"></a>Riigi kiirkaart

Võrdlemise eesmärgil saate loetleda riigid või regioonid, kus määrus on asjakohane. Kuid saadetise aruannete käitamisel kasutatakse määruse määramiseks ainult tarneviisi. Kui vaatate laosaadetise üle, puudub tarneviisi otselink. Saadetise saab seostada saadetise vedaja ja vedaja teenusega. Kui määrate vedaja teenuse, tuleb see seostada tarneviisiga. Seda seost kasutatakse saadetise aruannetes, näiteks veokirjas, et leida kaubasaadetisse prinditav tekst.

Järgmises tabelis kirjeldatakse kiirkaardil **Riik** olevaid välju.

| Field | Kirjeldus |
|---|---|
| Riik/regioon | Valige määrusega seostatav riik/regioon. |

## <a name="material-codes"></a><a name="hazmat-codes"></a>Materjalikoodid

Materjalikoodid määravad sätted, mis on seotud kindla ohtliku komponendiga, mis võidakse kaasata väljastatud tootesse. Iga materjalikood kuulub konkreetsele ohtlike materjalide määrusele ja selle määratlus peab vastama sellele määrusele. Kui rakendate väljastatud tootele materjalikoodi väljaga **Materjalikood**, rakendatakse selle toote puhul automaatselt kõiki materjalikoodi ohtlike materjalide sätteid. Seetõttu on väljastatud toodete häälestamine kiirem ja vähem aldis tõrketele.

Ohtlike materjalide määratluste haldamiseks toimige järgmiselt.

1. Avage **Tooteteabe halduse \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtlike materjalide määrus**.
2. Valige määrus ohtlike materjalide määratluse häälestamiseks.
3. Tehke vahekaardi **Häälestus** toimingupaanil valik **Ohtlikud materjalid**.
4. Sisestage väljale **Materjalikood** ohtliku materjali määratluse materjalikood. See väärtus valitakse materjalikoodi rakendamisel väljastatud tootele.

    Väli **Määruse kood** on kirjutuskaitstud ja seal kuvatakse määrus, mille valisite 2. etapis.

5. Kasutage selle lehe ülejäänud välju iga teie valitud määrusele kohalduva ohtliku materjali loomiseks ja häälestamiseks. Saadaolevad väljad on üksikute väljastatud toodete jaoks saadaolevad ohtlike materjalide väljade alamkogum. Lisateabe saamiseks vt [Ohtlikud materjalid toodetes, tellimustes, saadetistes ja koormates](hazmat-items.md).

## <a name="hazardous-material-classification-groups"></a><a name="classification-groups"></a>Ohtliku materjali klassifikatsioonigrupid

Iga ohtliku materjali klassifikatsioonigrupp määratleb väljaväärtuste grupi, mis määravad malli. Seda malli saate kasutada hiljem, kui häälestate väljastatud kauba ohtliku materjali andmed.

Kui määrate ohtliku materjali klassifikatsioonigrupi koodi väljastatud kaubale, kopeeritakse selle klassifikatsioonigrupiga seostatud teave kauba vastavatele väljadele. Seetõttu saate lihtsustada häälestustoiminguid, luues seotud väljaväärtuste kogumi, mida te sageli koos kasutate.

Need häälestusandmed pole spetsiifilised iga juriidilise isiku jaoks. Seetõttu võib teil olla ohtlike materjalide teabe ühine kogum, mis on jagatud kõigi teie juriidiliste isikute vahel.

Ohtlike materjalide klassifikatsioonigruppide häälestamiseks avage **Tooteteabe halduse \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtliku materjali klassifikatsioonigrupp**. Lehel **Ohtliku materjali klassifikatsioonigrupp** saate luua mistahes arvu gruppe ja konfigureerida neid väljade abil, mida kirjeldatakse järgmises tabelis.

| Field | Kirjeldus |
|---|---|
| Grupi kood | Saate sisestada grupi tuvastamise koodi. |
| Kirjeldus | Saate sisestada grupi kirjeldus. |
| Klassi kood | Saate grupiga seostada ohtliku materjali [klassi koodi](#classes). |
| Osakonna kood | Saate grupiga seostada ohtliku materjali [jaotuse koodi](#divisions). |
| Pakkimisgrupi kood | Saate grupiga seostada [pakendigrupi koodi](#packing-group). |
| Transpordikategooria kood | Saate grupiga seostada [transpordikategooria koodi](#transport-category). |
| Kordaja | Saate sisestada ohtliku materjali kordaja, mida kohaldatakse ohtlike materjalide klassi ja jaotuse suhtes vastavalt kehtivale määrusele. Seda kordajat kasutatakse valemi osana, mis arvutab koormasse või saadetisse kaasatud kõik *ohtliku materjali punktid*. Lisateavet ohtlike materjalide punktide ja selle kordaja kohta vt [kiirkaardilt Materjalihaldus](hazmat-items.md#material-management). |

## <a name="hazardous-material-classes"></a><a name="classes"></a>Ohtliku materjali klassid

Ohtliku materjali klass vastendatakse tavaliselt klasside loendiga, mis on esitatud määruses, millele te vastate. Näiteks USA määruse CFR 49 loendis on "klass 3" kergestisüttivad ja tuleohtlikud vedelikud. Saate häälestada klassid, mis puudutavad materjale, mida peate klassifitseerima.

Iga klass määratakse materjalide häälestusele materjaliloendis, mis on määrusega seotud. Määrate igale väljastatud kaubale klassi vastavalt vajadusele, et kirjeldada toote ohtlikku omadust.

Need häälestusandmed pole spetsiifilised iga juriidilise isiku jaoks. Seetõttu võib teil olla ohtlike materjalide teabe ühine kogum, mis on jagatud kõigi teie juriidiliste isikute vahel.

Ohtliku materjali klassid toimivad koos jaotuste, gruppide ja ühilduvusgruppidega järgmiselt.

- Kui määrate väljastatud kaubale ohtliku materjali klassi, peate määrama ka [ohtliku materjali jaotuse](#divisions).
- Ohtliku materjali klasse saate kasutada koos [ohtlike materjalide klassifikatsioonigruppidega](#classification-groups), et luua kaupade häälestamiseks koodide mall.
- Saate kasutada [ohtliku materjali ühilduvusgruppe](#compatibility-groups), et määrata, milliseid ohtlike materjalide klasse ja jaotusi saab koos tarnida.

Ohtliku materjali klasside häälestamiseks avage **Tooteteabe halduse \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtliku materjali klass**. Lehel **Ohtliku materjali klass** saate luua suvalise arvu klasse ja konfigureerida neid väljade abil, mida kirjeldatakse järgmises tabelis.

| Field | Kirjeldus |
|---|---|
| Klassi kood | Saate sisestada selle klassi tuvastamise koodi. Saate määratleda selle kauba koodi. Seejärel kasutatakse seda otsinguloendites, kui määrate väljastatud kaubale ohtliku materjali klassi. |
| Kirjeldus | Saate sisestada klassi kirjelduse. |

## <a name="hazardous-material-divisions"></a><a name="divisions"></a>Ohtliku materjali jaotused

Ohtlike materjalide jaotus on ohtliku materjali klassi alamkogum. Peate igale ohtlikku materjali sisaldavale tootele määrama nii jaotuse kui ka klassi.

Klasside puhul, millel pole ühtegi jaotust, looge jaotus koodiga *0*. Näiteks pole IATA määrustiku klassi-7 radioaktiivsetel materjalidel alajaotusi. Sel juhul saate luua jaotuse *0*, mille saate klassi määramisel seostada väljastatud tootega.

Need häälestusandmed pole spetsiifilised iga juriidilise isiku jaoks. Seetõttu võib teil olla ohtlike materjalide teabe ühine kogum, mis on jagatud kõigi teie juriidiliste isikute vahel.

Ohtliku materjali jaotused toimivad koos klasside, gruppide ja ühilduvusgruppidega järgmiselt.

- Kui määrate väljastatud kaubale ohtliku materjali jaotuse, peate määrama ka [ohtliku materjali klassi](#classes).
- Ohtliku materjali jaotusi saate kasutada koos [ohtlike materjalide klassifikatsioonigruppidega](#classification-groups), et luua kaupade häälestamiseks koodide mall.
- Saate kasutada [ohtliku materjali ühilduvusgruppe](#compatibility-groups), et määrata, milliseid ohtlike materjalide klasse ja jaotusi saab koos tarnida.

Ohtlike materjalide jaotuste häälestamiseks avage **Tooteteabe halduse \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtlike materjalide jaotus**. Lehel **Ohtliku materjali jaotus** saate luua suvalise arvu jaotusi ja konfigureerida neid väljade abil, mida kirjeldatakse järgmises tabelis.

| Field | Kirjeldus |
|---|---|
| Jaotus | Saate sisestada koodi, mida kasutada jaotuse viitenumbrina. |
| Kirjeldus | Sisestage jaotuse kirjeldus. |
| Klass | Otsige üles ja määrake klass, kuhu jaotus kuulub. |

## <a name="hazardous-material-compatibility-groups"></a><a name="compatibility-groups"></a>Ohtliku materjali ühilduvusgrupid

Ohtliku materjali ühilduvusgrupid määravad, milliseid ohtlike materjalide klasse ja jaotusi saab koos tarnida. Kui operaatorid loovad laokoormaid või saadetisi, saavad nad käitada ühilduvuskontrolli, mis väljastab hoiatuse, kui koorem või saadetis sisaldab kaupu, mis ei kuulu samasse ühilduvusgruppi.

Need häälestusandmed pole spetsiifilised iga juriidilise isiku jaoks. Seetõttu võib teil olla ohtlike materjalide teabe ühine kogum, mis on jagatud kõigi teie juriidiliste isikute vahel.

Ohtlike materjalide ühilduvusgruppide häälestamiseks avage **Tooteteabe halduse \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtliku materjali ühilduvusgrupp**. Lehel **Ohtliku materjali ühilduvusgrupp** saate luua mistahes arvu ühilduvusgruppe konfigureerida neid väljade abil, mida kirjeldatakse järgmistes alajaotustes.

### <a name="hazardous-material-compatibility-group-header"></a>Ohtliku materjali ühilduvusgrupi päis

Igal ühilduvusgrupil on kood ja kirjeldus. Järgmises tabelis on kirjeldatud päises olevaid välju.

| Field | Kirjeldus |
|---|---|
| Ühilduvusgrupp | Saate sisestada ühilduvusgrupi tuvastamise koodi. |
| Kirjeldus | Saate sisestada ühilduvusgrupi kirjelduse. |

### <a name="compatibility-group-details"></a>Ühilduvusgrupi üksikasjad

Iga ühilduvusgrupp määrab klasside ja jaotuste loendi ohtlike materjalide jaoks, mida saab koos tarnida.

| Field | Kirjeldus |
|---|---|
| Klass | Saate valida ohtliku materjali klassi, mis ühildub kõigi teiste klasside grupis. |
| Jaotus | Saate valida ohtliku materjali jaotuse, mis kuulub valitud klassi. |

## <a name="hazardous-material-specification-values"></a>Ohtliku materjali spetsifikatsiooni väärtused

Microsoft Dynamics 365 Supply Chain Management pakub mitut tüüpi ohtlike materjalide spetsifikatsioone. Iga tüübi puhul tuleb luua iga asjakohase välja jaoks keskne väärtuste kogum. Kasutajad saavad seejärel valida nende väärtuste seast, kui nad konfigureerivad ohtlike materjalide definitsioone või väljastatud tooteid. Supply Chain Management pakub lehtede kogumit, kus saate need väärtused luua. Iga leht on määratud ühte tüüpi spetsifikatsioonile. Iga saadaoleva spetsifikatsiooni kirjeldus ja teave selle kohta, kuidas luua selle jaoks saadaolevaid väärtusi, leiate järgmistest alajaotistest.

Üks ohtliku materjali spetsifikatsiooni näide on _laadimiskood_, mis määrab, kuidas antud materjali tuleb transportimise ajal ladustada. Kasutades selles jaotises sisalduvat teavet, saate luua laadimiskoodide keskse kogumi. See kogum kuvatakse seejärel kasutajatele ripploendis, kui nad määravad väljastatud tootele laadimiskoodi.

Need ohtlike materjalide spetsifikatsioonide väärtuse pole spetsiifilised iga juriidilise isiku kohta. Seetõttu võib teil olla ühiste väärtuste kogum, mida jagavad teie juriidilised isikud.

Saate kasutada [materjalikoode](#hazmat-codes), et luua iga spetsifikatsiooni jaoks sätete ühised kogumid, mis vastavad antud määrusele. Seejärel saate sobiva koodi rakendada igale väljastatud tootele vastavalt vajadusele. Lisateavet selle kohta, kuidas rakendada ohtliku materjali koodi konkreetsele väljastatud tootele ja kuidas konfigureerida selle toote üksikuid sätteid siin kirjeldatud spetsifikatsioonide kohta vt [Ohtlikud materjalid toodetes, tellimustes, saadetistes ja koormates](hazmat-items.md).

### <a name="hazardous-material-emergency-response"></a>Ohtliku materjali erakorraline vastus

Spetsifikatsioon *Ohtliku materjali erakorraline vastus* näitab, mida tuleks teha, kui midagi läheb valesti, kui transporditakse toodet, mis sisaldab antud ohtlikku materjali.

Selle spetsifikatsiooni väärtuste häälestamiseks avage **Tooteteabe haldus \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtliku materjali erakorraline vastus**. Lehel **Ohtliku materjali erakorraline vastus** saate luua mistahes arvu väärtusi ja konfigureerida igaühe neist klassifikatsioonikoodi ja lühikirjeldusega.

### <a name="hazardous-material-identification"></a><a name="identification"></a>Ohtliku materjali ID

Spetsifikatsioon *Ohtliku materjali ID* määratleb ohtliku materjali klassi või olemuse. Väärtus on tavaliselt kood, mis põhineb ÜRO standardil. Iga klass tuvastatakse koodi ja kirjeldusega ning see võib määrata transpordiviisi piirangud. Näiteks tuleohtliku kauba või materjali tuvastamiseks saate luua ohtliku materjali klassi, mis kasutab koodi *FL* ja kirjeldust *Tuleohtlik*. Samuti saate määrata, et klassi jaoks ei tohi kasutada õhutransporti.

Selle spetsifikatsiooni väärtuste häälestamiseks avage **Tooteteabe haldus \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtliku materjali ID**. Lehel **Ohtliku materjali ID** saate luua suvalise arvu väärtusi ja konfigureerida neid väljade abil, mida kirjeldatakse järgmises tabelis.

| Field | Kirjeldus |
|---|---|
| Identimine | Sisestage kood, mida kasutada viitenumbrina selle ohtliku materjali klassi tuvastamiseks. |
| Kirjeldus | Saate sisestada selle klassi kirjelduse. |
| Keela lennutransport | Märkige see ruut, et näidata, et seda ohtlike materjalide klassi jaoks ei tohi kasutada õhutransporti. |
| Keela meretransport | Märkige see ruut, et näidata, et seda ohtlike materjalide klassi jaoks ei tohi kasutada meretransporti. |

### <a name="hazardous-material-label"></a><a name="label"></a>Ohtliku materjali silt

Spetsifikatsioon *Ohtliku materjali silt* tuvastab ohtlike kaupade sildi, mida tuleb rakendada asjakohaste väljastatud toodete puhul. Sildid ise kirjeldavad, kuidas toodet käsitseda. Näiteks on teil toode, mis sisaldab mürgiseid gaase. Sel juhul häälestage sildi kood, mis tähistab mürgise gaasi silti. Samuti saate luua oma äriprotsessi nii, et see otsiks toodete tarnimise ajal üles selle väärtuse.

Selle spetsifikatsiooni väärtuste häälestamiseks avage **Tooteteabe haldus \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtliku materjali silt**. Lehel **Ohtliku materjali silt** saate luua mistahes arvu silte ja konfigureerida igaühe neist ID-koodi ja lühikirjeldusega.

### <a name="hazardous-material-packing-descriptions"></a><a name="packing-description"></a>Ohtliku materjali pakkimiskirjeldused

Spetsifikatsioon *Ohtliku materjali pakkimiskirjeldused* näitab, kuidas ohtlik kaup peab olema pakitud. Näiteks tuleks see pakkida kindlat tüüpi terasvaati või mõnda muud tüüpi spetsiaalsesse pakendisse.

Selle spetsifikatsiooni väärtuste häälestamiseks avage **Tooteteabe haldus \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtliku materjali pakkimiskirjeldused**. Lehel **Ohtliku materjali pakkimiskirjeldused** saate luua mistahes arvu pakkimiskirjeldusi ja konfigureerida igaühe neist ID-koodi ja lühikirjeldusega.

### <a name="hazardous-material-packing-group"></a><a name="packing-group"></a>Ohtliku materjali pakendigrupp

Spetsifikatsioon *Ohtliku materjali pakendigrupp* tuvastab ohtliku kauba pakendigrupi. Pakendigrupp võimaldab teil määratleda koodi ja kirjelduse, et näidata, kuidas ohtlikke materjale tuleks transportimise või saatmise ajal pakkida. Pakendigrupp määratakse kaubale kauba lehe **Kauba ohtlikud materjalid** kaudu.

Selle spetsifikatsiooni väärtuste häälestamiseks avage **Tooteteabe haldus \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtliku materjali pakendigrupp**. Lehel **Ohtliku materjali pakendigrupp** saate luua mistahes arvu pakendigruppe ja konfigureerida igaühe neist ID-koodi ja lühikirjeldusega.

### <a name="hazardous-material-packing-instruction"></a><a name="packing-instruction"></a>Ohtliku materjali pakkimisjuhend

Spetsifikatsioon *Ohtliku materjali pakkimisjuhend* määrab pakkimisejuhised, mida tuleb järgida, kui antud ohtlik kaup on ette valmistatud õhutranspordi jaoks.

Selle spetsifikatsiooni väärtuste häälestamiseks avage **Tooteteabe haldus \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtliku materjali pakkimisjuhend**. Lehel **Ohtliku materjali pakkimisjuhend** saate luua mistahes arvu pakkimisjuhendi ID-sid ja konfigureerida igaühe neist ID-koodi ja lühikirjeldusega.

### <a name="hazardous-material-stowage"></a><a name="stowage"></a>Ohtliku materjali laadimine

Spetsifikatsioon *Ohtliku materjali laadimine* näitab, kuidas toode tuleb ladustada laeval, kui kasutatakse meretransporti.

Selle spetsifikatsiooni väärtuste häälestamiseks avage **Tooteteabe haldus \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtliku materjali laadimine**. Lehel **Ohtliku materjali laadimine** saate luua mistahes arvu laadimis-ID-sid ja konfigureerida igaühe neist ID-koodi ja lühikirjeldusega.

### <a name="hazardous-material-transport-category"></a><a name="transport-category"></a>Ohtliku materjali transpordikategooria

Spetsifikatsiooni *Ohtliku materjali transpordikategooria* kasutatakse aruannetes tavaliselt sarnaste ohtlike toodete grupeerimiseks. Näiteks kasutatakse transpordikategooriaid aruandes **Saadetise kokkuvõte**, mille saate printida lao saadetisekirjest.

Selle spetsifikatsiooni väärtuste häälestamiseks avage **Tooteteabe haldus \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtliku materjali transpordikategooria**. Lehel **Ohtliku materjali transpordikategooria** saate luua mistahes arvu transpordikategooriaid ja konfigureerida igaühe neist kuvatava nime ja lühikirjeldusega.

### <a name="hazardous-material-technical-name"></a><a name="technical-name"></a>Ohtliku materjali tehniline nimi

Spetsifikatsiooni *Ohtliku materjali tehniline nimi* saate kasutada igat materjali kirjeldava üldkasutatava või sisemise ettevõttenime pakkumiseks.

Selle spetsifikatsiooni väärtuste häälestamiseks avage **Tooteteabe haldus \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtliku materjali tehniline nimi**. Lehel **Ohtliku materjali tehniline nimi** saate luua mistahes arvu tehnilisi nimesid ja konfigureerida igaühe neist kuvatava nime ja lühikirjeldusega.

### <a name="hazardous-material-tunnel"></a><a name="tunnel"></a>Ohtliku materjali tunnel

Spetsifikatsioon *Ohtliku materjali tunnel* piirab tunnelite tüüpe, mille kaudu saab ohtlikke materjale transportida, määratledes nende tunnelite tüübid, mida tuleb kasutada. Tunnelite kategooriad on kehtestatud ohtlike materjalide transpordi kehtivate määrustega. See spetsifikatsioon rakendub tavaliselt ainult maanteetranspordi puhul.

Selle spetsifikatsiooni väärtuste häälestamiseks avage **Tooteteabe haldus \> Häälestus \> Ohtlike materjalide saatmisdokumentatsioon \> Ohtliku materjali tunnel**. Lehel **Ohtliku materjali tunnel** saate luua mistahes arvu tunneli-ID-sid ja konfigureerida igaühe neist ID-koodi ja lühikirjeldusega.
