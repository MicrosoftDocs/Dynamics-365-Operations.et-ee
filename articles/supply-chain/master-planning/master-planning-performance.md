---
title: Koondplaneerimise jõudluse parandamine
description: Selles teemas kirjeldatakse mitmesuguseid võimalusi, mis võivad aidata parandada koondplaneerimise või probleemide tõrkeotsingu jõudlust.
author: t-benebo
manager: tfehr
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 01db8a02e57c61daf940e2f459124a857ced68cb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213603"
---
# <a name="improve-master-planning-performance"></a>Koondplaneerimise jõudluse parandamine

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse mitmesuguseid võimalusi, mis võivad aidata parandada koondplaneerimise või probleemide tõrkeotsingu jõudlust. See sisaldab teavet nii parameetrite ja sätete kohta kui ka soovituslikke konfiguratsioone ja tegevusi. Kaasatud on ka kokkuvõte kõikidest olulistest parameetritest, mida peaksite kaaluma pikaajaliste koondplaneerimise tööde korral.

See teema on mõeldud süsteemiadministraatoritele või IT-kasutajatele, kes saavad teha tõrkeotsingut. See on mõeldud ka tootmise või tarnimise plaanijatele, kuna see sisaldab teavet parameetrite kohta, mis on seotud ettevõtte plaanimise nõuetega. 

## <a name="parameters-related-to-master-planning-performance"></a>Koondplaneerimise jõudlusega seotud parameetrid

Mitmesugused parameetrid mõjutavad koondplaneerimise töötamise aega ja neid tuleb arvesse võtta.

### <a name="number-of-threads"></a>Lõimede arv

Parameeter **Lõimede arv** võimaldab kohandada koondplaneerimise protsessi, et aidata parandada konkreetse andmekogumi jõudlust. See parameeter määrab lõimede koguarvu, mida kasutatakse koondplaneerimise käivitamiseks. See põhjustab koondplaneerimise käivitamise paralleelimise, mis aitab vähendada töötamise aega. 

Saate seadistada parameetri **Lõimede arv** dialoogiaknas **Koondplaneerimise käitus**. Selle dialoogiakna avamiseks valige suvandid **Koondplaneerimine \> Koondplaneerimine \> Käivita \> Koondplaneerimine** või valige käsk **Käivita** tööruumis **Koondplaneerimine**. Selle parameetri parima väärtuse leidmiseks peate kasutama katse ja eksituse meetodit. Kuid algse väärtuse arvutamiseks võite kasutada järgmiseid valemeid.

- **Kui teie ettevõte on tootja:** (lõimede arv) = (plaanitud tellimuste arv ÷ 1000)
- **Muu:** (lõimede arv) = (kaupade arv ÷ 1000)

Koondplaneerimisel kasutatavate abiliste arv peab olema vähem kui või võrdne lõimede maksimaalse arvuga, mis on pakktöötlusserveris lubatud. Kui abiliste arv ületab lõimede arvu pakktöötlusserveris, siis täiendavad lõimed ei tööta.

> [!NOTE]
> Parameetri **Lõimede arv** seadmine väärtusele **0** (null) pikendab koondplaneerimise töötamise aega. Seetõttu soovitame alati määrata väärtuse, mis on suurem kui 0.

### <a name="number-of-tasks-in-helper-task-bundle"></a>Ülesannete arv abilise ülesannete kogumis

Muutes sätet **Ülesannete arv ülesannete kogumis** (ehk kogumi suurus), võib olla võimalik töötamise aega lühendada. See säte reguleerib kaupade arvu, mis on plaanitud koos ühe abilisega.

Parameetri **Ülesannete arv ülesannete kogumis** saate määrata jaotises **Jõudlus** vahekaardil **Üldine** lehel **Koondplaneerimise parameetrid** (**Koondplaneerimine \> Seadistamine \> Koondplaneerimise parameetrid**). Selle parameetri parim väärtus oleneb teie andmetest. Seetõttu soovitame alustada väärtusest **1** ning kasutada katse ja eksituse meetodit teie seadistuse jaoks parima väärtuse määramiseks.

Üldiselt soovitame suurendada ülesannete arvu, kui kaupade arv on väga suur (sadades tuhandetes). Muidu peaksite ülesannete arvu vähendama. Järgmiste konkreetsete majandusharude jaoks kaaluge järgmisi soovitusi.

- Jaemüügis ja levitamises, kus on palju sõltumatuid kaupasid, kasutage palju abilisi, kuna kaupade vahel puudub sõltuvus. 
- Tootmises, kus on palju kooslusi ja jagatud alamkomponente, kasutage vähem abilisi, kuna sõltuvused kaupade vahel võivad põhjustada ooteaegu.

> [!TIP]
> Kui teil on probleeme jõudlusega, soovitame vähendada sätte **Abiliste arv ülesannete kogumis** väärtusele **1**. Saate alustada katse ja eksituse meetodiga, et leida oma seadistusele parim väärtus. Üldiselt tekivad jõudlusprobleemid, kui ühe kauba töötlemine võtab rohkem aega kui ülejäänud kaupade töötlemine. Sellisel juhul näete, et kahe järgneva ülesande, mille olek koondplaneerimises on **Laovarud**, käitamisele kulub hoopis erinev hulk aega. Äärmuslikel juhtudel võib see erinevus olla isegi 30 minutit. Ülesannete käitamisele kuluvat aega saab tuletada, vaadates iga ülesande kestust.

### <a name="use-of-cache"></a>Vahemälu kasutamine

Parameetriga **Vahemälu kasutamine** saate kohandada koondplaneerimise protsessi, et see toimiks konkreetsel andmekogumil paremini. Näiteks saate kohandada selle saavutama järgmised tulemused.

- Kui toimub rohkem vahemällu salvestamist, kogutakse andmete mällu rohkem andmeid. Eeldus on, et andmeid kasutatakse hiljem uuesti. Kui andmed on mälus, võite salvestada andmebaasi taotlusi. Kuid rohkem vahemällu salvestades kasvavad nõudmised mälule.
- Kui toimub vähem vahemällu salvestamist, võib vajalik olla samade andmete sagedasem toomine andmebaasist. Peale selle salvestab rakendusobjektide server (AOS) protsessi käigus mällu vähe andmeid.

Keeruline on ennustada, kumb variant on parem, kuna iga juhtum oleneb mitte ainult andmetest, aga ka riistvarast. Näiteks kuna vähem vahemällu salvestamist tekitab andmebaasi serverile lisakoormust, ei ole selle variandi kasutamine ilmselt hea mõte, kui andmebaasi server on juba üle koormatud.

Parameetri **Vahemälu kasutamine** saate määrata jaotises **Jõudlus** vahekaardil **Üldine** lehel **Koondplaneerimise parameetrid** (**Koondplaneerimine \> Seadistamine \> Koondplaneerimise parameetrid**). Vahemällu salvestamise tõhusus oleneb suuresti kliendiandmetest. Näiteks kui vahemällu salvestatud andmeid pole kunagi vaja, siis raiskate mälumahtu, kui hoiate andmeid alles plaanimisprotsessi lõpuni. Kui sellisel juhul konfigureerite vähem vahemällu salvestamist, võib jõudlus paraneda, kuna AOS nõuab vähem mälu ja serveriressursid vabastatakse muude ülesannete jaoks.

> [!TIP]
> Üldiselt soovitame seada parameetri **Vahemälu kasutamine** väärtusele **Maksimum**, kuna see parameeter on mõeldud jõudlust parandama. Soovitame seada parameetri väärtusele **Miinimum**, kui töötate kohapeal ja mälu maht on piiratud (umbes 2 gigabaiti \[GB\]).

### <a name="number-of-orders-in-firming-bundle"></a>Kinnituskogumi tellimuste arv

Parameeter **Kinnituskogumi tellimuste arv** määrab tellimuste koguarvu, mida töödeldakse korraga igas lõimes/partiis. See põhjustab automaatkinnitamise protsessi paralleelimise.

Parameetri **Kinnituskogumi tellimuste arv** saate määrata jaotises **Jõudlus** vahekaardil **Üldine** lehel **Koondplaneerimise parameetrid** (**Koondplaneerimine \> Seadistamine \> Koondplaneerimise parameetrid**). Automaatkinnitamise paralleelimine põhineb tellimustel, mida tuleb koos töödelda. Näiteks kui see parameeter on seatud väärtusele **50**, võtab iga lõim või pakktöötlus korraga 50 tellimust ja töötleb neid koos. Parima väärtuse leidmiseks soovitame kasutada katse ja eksituse meetodit. Kuid algse väärtuse arvutamiseks võite kasutada järgmist valemit.

(Tellimuste arv kogumi kohta) = (nõutud kaupade arv ÷ lõimede arv)

> [!NOTE]
> Kui seate parameetri **Kinnituskogumi tellimuste arv** väärtusele **0** (null), ei toimu automaatkinnitamise protsessi paralleelimist. Kogu protsess töötab ühes pakktöötluses ja selle töötamise aeg on kumulatiivne. Seetõttu pikeneb koondplaneerimise töötamise aeg. Sel põhjusel soovitame seada parameetri väärtusele, mis on suurem kui **0** (null).

### <a name="time-fences"></a>Ajapiirid

Ajapiirid määravad, kui kaugele tulevikus tuleb koondplaneerimisega kalkulatsioonid ja muud nõuded arvutada. Mida suurem on ajapiir, seda kauem kestab koondplaneerimine. Seetõttu määrake ajapiirid oma ärivajaduste järgi. Lisateavet ajapiiride kohta vt teemast [Koondplaneerimise seadistamine](master-planning-setup.md).

### <a name="actions"></a>Tegevused

Ajapiiride hulgast leiate ka parameetri **Tegevussoovitus**. Tegevussoovituste arvutamine põhjustab koondplaneerimise töötamise aja pikenemise. Kui tegevussoovitusi ei analüüsita ja rakendata korrapäraselt (iga päev, nädal jne), kaaluge arvutuse väljalülitamist koondplaneerimise töötamise ajaks. Arvutuse väljalülitamiseks seadke lehel **Koondplaanid** (**Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**) suvandi **Tegevussoovitus** ajapiir väärtusele **0** (null). Veenduge ka, et suvand **Tegevussoovitus** oleks välja lülitatud kõikide laovarude gruppide jaoks.

### <a name="futures"></a>Tulevased

Tulevaste arvutamine põhjustab koondplaneerimise töötamise aja pikenemise. Kui te ei plaani kooslusi või kui viivitusi ei tule levitada plaanimise ajal pakkumisest nõudlusesse, kaaluge tulevaste arvutamise väljalülitamist koondplaneerimise ajaks. Arvutuste väljalülitamiseks seadme suvandi **Tulevased** ajapiir väärtusele **0** (null) koondplaani jaoks, mida käitate. Veenduge ka, et suvand **Tulevased** oleks välja lülitatud kõikide laovarude gruppide jaoks.

## <a name="one-heavy-routine-at-a-time"></a>Üks mahukas töö korraga

Kui plaanite koondplaneerimist, ärge plaanige samale ajale muid pakett-töid. Eeskätt ärge plaanige samale ajale muid mahukaid töid, näiteks varude sulgemist.

## <a name="review-the-session-log"></a>Seansilogi läbivaatus

Süsteem võib koguda täiendavat teavet ülesannete kohta, mis töötavad koondplaneerimise ajal. Selleks et süsteem seda teavet koguks, lülitage sisse säte **Töötlemisaja jälgimine** dialoogiaknas **Koondplaneerimise käitus**. Kogutav teave võib aidata leida käituses kitsaskohti. Näiteks kui parameeter **Ülesannete arv abilise ülesannete kogumis** on seatud väärtusele **1**, saate tuvastada üksuse, millel on kõige pikem töötamise aeg. Saate ka võrrelda töötamise aegu eri lõimedel, mille olek on **Laovarud**, ja võrrelda iga ülesande kestust.

Süsteemi koondplaneerimise käituste läbi vaatamiseks järgige üht järgmistest etappidest.

- Valige tööruumis **Koondplaneerimine** ripploendist koondplaan ja seejärel paanilt **Koondplaneerimine** valige suvand **Ajalugu**. Valige töö, valige kiirkaardilt suvand **Päringud** ja seejärel suvand **Protsessiülesande kestus**.
- Lehel **Koondplaanid** valige vasakult paanilt plaan ja seejärel kiirkaardilt suvand **Ajalugu**. Valige töö, valige kiirkaardilt suvand **Päringud** ja seejärel suvand **Protsessiülesande kestus**.

Seansilogi ülevaatamisel arvestage järgnevaga.

- **Värskendamine** ei tohi kesta kaua (üldiselt peaks see kestma kuni 30 minutit), see on aga ühe lõimega
- **Plaani kopeerimine** ei tohi kesta kaua (see peaks kestma umbes minuti).
- **Automaatkinnitamine** kestab tavaliselt umbes 30 minutit. Kuid see võib kesta mitu tundi, olenevalt tellimuste arvust ja kaupade keerukusest.
- **Automaatkinnitamine** ei tohi kesta vähem kui **Laovarud**.
- **Laovarud** peaksid ülejäänuga võrreldes võtma kõige kauem aega.
- **Tegevus** ja **Tulevane sõnum** võivad kesta kaua, olenevalt andmetest ja koosluste arvust.

## <a name="filtering-of-items"></a>Kaupade filtreerimine

Filtrid, mida rakendatakse dialoogiaknas **Koondplaneerimise käitus**, mõjutavad koondplaneerimise käituse kestust. Valige suvandid **Koondplaneerimine \> Koondplaneerimine \> Käivita \> Koondplaneerimine** või valige käsk **Käivita** tööruumis **Koondplaneerimine**. Kaupade välja jätmiseks käitusest soovitame filtreerida kauba töötsükli oleku järgi (mitte kaubakoodi järgi). Kui filtreerite töötsükli oleku järgi, kestab värskendamise protsess vähem aega kui kaubakoodide järgi filtreerides.

## <a name="automatically-filter-by-items-with-direct-demand"></a>Automaatselt otsenõudlusega kaupade alusel filtreerimine

Koondplaneerimise käitusaja parandamiseks saate valida ainult otsese nõudlusega kaupade kaasamise. Seda filtrit saab kasutada ainult täieliku koondplaneerimise käitamiseks, millel ei ole ühtegi muud filtrit väljal **Kaasatavad kirjed** rakendatud. Koondplaneerimise filtritega käivitamine ignoreerib seadistust **Automaatselt otsenõudlusega kaupade alusel filtreerimine**.

Väli **Automaatselt otsenõudlusega kaupade alusel filtreerimine** asub lehel **Koondplaneerimise parameetrid** ja seda saab kasutada nii eeltöötluse kui ka järeltöötluse seadistustega.

### <a name="pre-processing"></a>Eeltöötlemine
Parameeter **Eeltöötlus: automaatselt otsenõudlusega kaupade alusel filtreerimine** tagab, et koondplaneerimise eeltöötluse etapp hõlmab ainult kaupu, mis vastavad vähemalt ühele järgmistest tingimustest.
  - Kaubal on eeldatav sissetulek või väljaminek, nagu ostutellimus, müügitellimus, hinnapakkumine, üleviimistellimus või tootmistellimus. 
  - Kaubal on laovarud koos puhvervaruga (minimaalne kauba laoseis).
  - Kaubal on nõudluse prognoos pärast tänast.
  - Kaubal on pakkumise prognoos pärast tänast.
  - Kaup sisaldab kõiki järjepidevuse ridu kõnekeskuse moodulist, mis pole veel loodud.

> [!NOTE]
> Füüsiliselt saadaval laovaruga kaup ei kuva, ei nõudetehingut, kuna kaubale pole nõudlust.

### <a name="post-processing"></a>Järeltöötlus
Suvand **Järeltöötlus: automaatselt otsenõudlusega kaupade alusel filtreerimine** on asjakohane ainult siis, kui määrate oma laovarude gruppides suvandi **Koosluse versiooni vajadus**. Vastasel juhul ei pea te parameetrit lubama. 

Enne laovarude etapi käivitamist on laovarude eelne etapp, mille ajal töödeldakse kaubad, millel on laovarude säte **Koosluse versiooni vajadus** lubatud, uuesti. Seda tehakse tagamaks, et nõutava koosluse versiooni kaubad oleksid planeeritud. Kaubad, mille puhul arvatakse, et nendele pole töötlemise eel nõudlust, ei ole enam nõutud ja seetõttu tuleks need planeerimisest välja jätta.

## <a name="performance-checklist-summary"></a>Jõudluse kontroll-loendi kokkuvõte

- **Lõimede arv** – määrake väärtus, mis on suurem kui **0** (null).
- **Ülesannete arv abilise ülesannete kogumis** – määrake väärtus, mis on suurem kui **0** (null). (Kasutage selles teemas eespool toodud valemeid.)
- **Vahemälu kasutamine** – seadke väärtusele **Maksimum**, v.a siis, kui süsteemis on vähe vaba mäluruumi.
- **Kinnituskogumi tellimuste arv** – määrake väärtus, mis on suurem kui **0** (null). (Kasutage selles teemas eespool toodud valemit.)
- **Ajapiirid** – kohandage oma ärivajaduste järgi.
- **Tegevused ja tulevased** – keelake tegevused ja tulevased, kui te neid ei kasuta.
- **Üks mahukas töö korraga** – ärge käitage koondplaneerimist koos teiste mahukate töödega.
- **Seansilogi läbivaatus.**
- **Kaupade filtreerimine** – kasutage töötsükli olekut kaupade väljajätmiseks koondplaneerimise käitusest. (Ärge kasutage kaubakoode.)
