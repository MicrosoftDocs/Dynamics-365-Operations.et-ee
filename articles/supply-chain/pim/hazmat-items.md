---
title: Ohtlikud materjalid toodetes, tellimustes, saadetistes ja koormates
description: Selles teemas selgitatakse, kuidas määrata väljastatavate toodete ohtlike materjalide omadusi, kuidas panna ohtlikele kaupadele laovarude limiite ja kuidas kaasata ohtlikke materjale müügitellimusse, saadetisse või koormasse.
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
ms.openlocfilehash: 7e0564802bc53ce21236ffc6ed065bf6abac7c78
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243149"
---
# <a name="hazardous-materials-in-products-orders-shipments-and-loads"></a>Ohtlikud materjalid toodetes, tellimustes, saadetistes ja koormates

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles teemas selgitatakse, kuidas määrata väljastatavate toodete ohtlike materjalide omadusi, kuidas panna ohtlikele kaupadele laovarude limiite ja kuidas kaasata ohtlikke materjale müügitellimusse, saadetisse või koormasse.

## <a name="set-hazardous-material-specifications-for-products"></a>Toodete ohtlike materjalide spetsifikatsioonide määramine

Pärast ohtlike materjalide määruse määratlemist ja seotud viitekoodide häälestamist teemas [Ohtlike materjalide häälestamine](hazmat-setup.md) kirjeldatule vastavalt, saate selle teabe seostada väljastatud kaupadega. Saatmisdokumentide saatmistekst võetakse väljastatud kaupade ohtlike materjalide andmetest.

Väljastatud kauba ohtliku materjaliga seostamise osana peate määrama määruse koodi ja materjali. Kaubaga või seostada erinevaid määrusekoode olenevalt transpordivahendist ja iga kaubaga saab seostada mitu määrust ja materjalikoodi.

Väljastatud toote häälestamiseks ohtliku materjaliga toimige järgmiselt.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige või looge toode, et avada selle leht **Väljastatud toote üksikasjad**.
1. Määrake kiirkaardil **Varude haldus** suvandi **Ohtlik materjal** väärtuseks **Jah**. See säte tuvastab kauba ohtliku kaubana ja seda kasutatakse saatedokumentatsiooni printimisel.
1. Tehke grupi **Vastavus** vahekaardi **Varude haldus** toimingupaanil valik **Kauba ohtlik materjal**.
1. Täitke valitud kauba leht **Kauba ohtlik materjal** ja kasutage selleks välju, mis on kirjeldatud järgmistes alajaotistes.

### <a name="item-hazardous-materials-header"></a>Kauba ohtlikud materjalid päis

Järgmine tabel kirjeldab välju, mis on saadaval lehe **Kauba ohtlik materjal** ülaosas.

| Field | Kirjeldus |
|---|---|
| Kaubakood | Väljastatud toode, millega töötate. |
| Määruse kood | Valige tootele rakendatav ohtliku materjali määrus. Määrus määratleb, kuidas saadetisse prinditav tekst luuakse kauba ja seostatud tarneviiside jaoks. Pärast selle määramist ei saa koodi sellel lehel redigeerida. Siiski saate määrata uue määrusekoodi, valides väärtuse **Uus**. |
| Materjali kood | (Valikuline) Valige tootele rakendatav ohtliku materjali kood. Materjali kood annab malli, mis sisaldab selle lehe paljude teiste väljade vaikeväärtusi. Koodi valimisel kopeeritakse kõik selle ohtlike materjalide spetsifikatsioonid praegusele tootele. Kuid süsteem palub esmalt kinnitada, et kauba materjali andmed tuleb täita materjali koodist. |
| Grupi kood | (Valikuline) Saate valida tootele rakendatav ohtliku materjali klassifikatsioonigrupi kood. Välja **Materjalikood** koodi valimisel kopeeritakse kõik selle ohtlike materjalide spetsifikatsioonid praegusele tootele. Kuid süsteem palub esmalt kinnitada, et kaubaklassi grupi andmed tuleb täita grupikoodist. |

### <a name="descriptions-fasttab"></a><a name="hazmat-description"></a>Kiirkaart Kirjeldused

Järgmises tabelis kirjeldatakse kiirkaardil **Kirjeldused** olevaid välju.

| Field | Kirjeldus |
|---|---|
| Õige saadetise nimi | Saate sisestada materjali tavakirjelduse, nagu on määratud kehtivas määruses. Selle väärtuse tõlkeid saate pakkuda kiirkaardil **Kauba saatmisteksti tõlge**, nagu on kirjeldatud järgmises jaotises. |
| Tehniline nimi | Saate valida materjali ühise või üldise nime. See nimi võib olla nimi, mida teie ettevõte kasutab materjali jaoks ettevõttesiseselt. |
| N.O.S. | Märkige see ruut, et näidata, kas väärtus **Õige saadetise nim** on kauba teisiti määratlemata (N.O.S.) saadetise nimi. N.O.S. saadetiste nimesid kasutatakse sarnaste kemikaalide ja kindla lõppkasutusega materjalide gruppide puhul, kuid seda ei pruugita loetleda nime järgi konkreetse määruse ohtlike materjalide tabelis. |

### <a name="item-ship-text-translation-fasttab"></a>Kauba saatmisteksti tõlke kiirkaart

Kiirkaart **Kauba saatmisteksti tõlge** sisaldab tabelit, mis näitab väärtuste **Õige saadetise nimi** tõlkeid, mis on määratletud kiirkaardi **Kirjeldused** esmase keele jaoks. Neid tõlkeid saab kasutada saadetisse prinditaval tekstil ühe või mitme täiendava keele jaoks.

Järgmises tabelis on kirjeldatud kiirkaardil **Kauba saatmisteksti tõlge** olevaid välju.


| Field | Kirjeldus |
|---|---|
| Keel | Selle keele kood, mida rida kasutab. Näiteks **pt-br** näitab portugali (Brasiilia) keelt. |
| Saadetise prinditav tekst | Tõlgitud väärtus **Õige saadetise nimi** keeles, mida rida kasutab. |

Tõlke lisamiseks või redigeerimiseks valige tabeli kohal **Tõlked**, et avada leht **Teksti tõlked**. Seejärel järgige üht neist sammudest.

- Uue tõlke lisamiseks tehke toimingupaanil valik **Lisa**. Valige lisatav keel ja seejärel sisestage tõlgitud tekst väljale **Tõlgitud tekst**.
- Olemasoleva tõlke redigeerimiseks valige sihtkeel väljal **Keel** ja vajaduse korral redigeerige tõlgitud teksti väljal **Tõlgitud tekst**.

### <a name="material-management-fasttab"></a><a name="material-management"></a>Kiirkaart Materjalihaldus

Järgmises tabelis kirjeldatakse kiirkaardil **Materjalihaldus** olevaid välju.

| Field | Kirjeldus |
|---|---|
| Klass | Saate valida ohtliku materjali klassi, kuhu toode kuulub, nagu see on määratletud määruses, millele te vastate. Peate igale ohtlikku materjali sisaldavale tootele määrama nii jaotuse kui ka klassi. |
| Kirjeldus | Kirjeldus, mis on määratletud väljal **Klass** valitud klassi jaoks. See väli on kirjutuskaitstud. |
| Jaotus | Saate valida ohtliku materjali jaotuse, kuhu toode kuulub, nagu see on määratletud määruses, millele te vastate. Jaotus on klassi alamkogum. Peate igale ohtlikku materjali sisaldavale tootele määrama nii jaotuse kui ka klassi. |
| Identimine | Saate valida ohtliku materjali ID. Tavaliselt põhineb see kood ÜRO standardil. |
| Pakkimisgrupp | Saate valida praeguse kauba kehtiva pakendigrupi. |
| Kirjeldus | Kirjeldus, mis on määratletud väljal **Pakendigrupp** valitud grupi jaoks. See väli on kirjutuskaitstud. |
| Pakkimiskirjeldused | Valige kohaldatav pakkimiskirjelduse kood. See kood viitab kirjeldusele, mis näitab, kuidas toode peab olema pakitud. |
| Ohtliku materjali sildid | Saate valida koodi, mis viitab kohaldatavale ohtlike kaupade sildile, mida tuleks tootele rakendada. |
| Piiratud kogus | Seadke see suvand väärtusele **Jah**, et teatada toote kaalust, mis sisaldub igas koormas ja igal koormareal. |
| Kogus | Saate sisestada toote ohtlike materjalide koguse määratud ühikus. Seda väärtust kasutatakse tootega hõlmatavate koormate ja saadetistega seotud ohtlike materjalide kogusumma arvutamiseks. |
| Kordaja | Saate sisestada kordaja, mida rakendatakse, kui ohtlikku materjali skoor arvutatakse iga koormarea jaoks, mis sisaldab toodet. See väärtus määratakse kohaldatava määrusega vastavalt tootes sisalduvale ohtliku materjali tüübile. |
| Ühik | Saate valida mõõtühiku, mis rakendub toote ohtliku materjali kogusele, nagu on määratud väljal **Kogus**. Seda väärtust kasutatakse tootega hõlmatavate koormate ja saadetistega seotud ohtlike materjalide kogusumma arvutamiseks. |

#### <a name="how-the-hazardous-material-score-is-calculated"></a>Ohtlike materjalide skoori arvutamine

Toote kiirkaardil **Materjalihaldus** määratud mitmeid väärtusi kasutatakse *ohtliku materjali skoori* arvutamiseks iga toodet sisaldava koormarea kohta. Skoori arvutamiseks kasutatakse järgmist valemit.

Ohtliku materjali skoor = *&lt;reakogus&gt;* × *&lt;ohtliku materjali kogus&gt;* × *&lt;ühikuteisendus&gt;* × *&lt;kordaja&gt;*

Siin on valemi võti.

- *&lt;Reakogus&gt;* on koormarea jaoks määratud toote kogus.
- *&lt;Ohtliku materjali kogus&gt;* on toote jaoks määratud ohtliku materjali kogus kiirkaardi **Materjalihaldus** väljal **Kogus**.
- *&lt;Ühikuteisendus&gt;* on teisendustegur, mida kasutatakse teisendamiseks koormarea koguse ühiku ja toote jaoks määratud ühiku vahel kiirkaardi **Materjalihaldus** väljal **Ühik**.
- *&lt;Kordaja&gt;* on toote jaoks määratud kordaja kiirkaardi **Materjalihaldus** väljal **Kordaja**.

See skoor esitatakse iga koormarea kohta, mis sisaldab toodet, milles need väärtused on määratud. Lisateavet lugege selle teema järgmisi jaotisi: [Ohtlikke materjale sisaldavad saadetised](#hazmat-shipments) ja [Ohtlikke materjale sisaldavad koormad](#hazmat-loads).

#### <a name="how-the-hazardous-material-weight-is-calculated"></a>Ohtlike materjalide kaalu arvutamine

Koormad ja koormaread, mis sisaldavad tooteid mille kiirkaardi **Materjalihaldus** suvandi **Piiratud kogus** väärtuseks on määratud **Jah**, kuvatakse ohtlike materjalide kogukaal, nagu on kirjeldatud selle teema järgnevates jaotistes [Ohtlikke materjale sisaldavad saadetised](#hazmat-shipments) ja [Ohtlikke materjale sisaldavad koormad](#hazmat-loads). Ohtlike materjalide kaalu arvutamiseks kasutatakse järgmist valemit.

Ohtliku materjali kaal = *&lt;Reakogus&gt;* × *&lt;Toote kaal&gt;* × *&lt;Ühikuteisendus&gt;*

Siin on valemi võti.

- *&lt;Reakogus&gt;* on koormarea jaoks määratud toote kogus.
- *&lt;Toote kaal&gt;* on toote jaoks määratud netokaal toote jaoks määratud laoühikutes.
- *&lt;Ühikuteisendus&gt;* on teisendustegur, mida kasutatakse koormarea koguse ühiku ja laoühiku teisendamiseks, mida kasutatakse *&lt;Toote kaalu&gt;* jaoks.

### <a name="transport-information-fasttab"></a>Kiirkaart Transporditeave

Järgmises tabelis kirjeldatakse kiirkaardil **Transporditeave** olevaid välju.

| Field | Kirjeldus |
|---|---|
| Transpordikategooria | Saate valida seotud transpordikategooria. |
| Tunnelikood | Saate valida kaubaga seotud tunneli piirangu koodi. |
| Ohtliku materjali laadimine | Saate valida viitekoodi, mida kasutatakse meretranspordi laadimise käitlemiseks, kui kaupa veetakse meretranspordiga. |
| Lennuki tüüp | Valige õhutranspordi piirang, mis kehtib materjali puhul, kui seda veetakse õhutranspordiga. |
| Pakkimine – ainult kaubalennukid | Väärtuse põhjal, mille valisite väljal **Lennuki tüüp**, valige pakkimisjuhendi kood, mis kehtib, kui toodet võib transportida ainult kaubalennukiga. |
| Pakkimine – reisija- ja kaubalennukid | Väärtuse põhjal, mille valisite väljal **Lennuki tüüp**, valige pakkimisjuhendi kood, mis kehtib, kui toodet võib transportida nii kaubalennuki kui ka reisilennukiga. |
| IATA tärn | Määrake selle suvandi väärtuseks **Jah**, et näidata, et sellele kiirkaardile sisestatud õhutranspordi spetsifikatsioonid on seotud Rahvusvahelise Lennutranspordi Assotsiatsiooni (IATA) ohtlike kaupade standardiga. Sellel väljal on ainult informatiivne eesmärk. |
| Erakorraline vastus | Saate valida koodi, mis viitab materjali käsitsemise juhistele hädaolukorras. |

### <a name="environmental-information-fasttab"></a>Kiirkaart Keskkonnateave

Järgmises tabelis kirjeldatakse kiirkaardil **Keskkonnateave** olevaid välju.

| Field | Kirjeldus |
|---|---|
| Oht keskkonnale | Määrake selle suvandi väärtuseks **Jah**, et näidata, et toode on keskkonnaohtlik. Kasutage seda välja oma aruandluse tarbeks. |
| Meresaaste | Määrake selle suvandi väärtuseks **Jah**, et näidata, et toode on meresaaste. Kasutage seda välja oma aruandluse tarbeks. |

## <a name="set-stock-limits-for-hazardous-products"></a><a name="stock-limits"></a>Ohtlike toodete ladustamispiirangute määramine

Ohutuse tagamiseks peate võib-olla piirama antud toote koguhulka, mida saab ladustada ühes asukohas. Väljastatud tootele ladustamispiirangute määramiseks toimige järgmiselt.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige toode, et avada selle leht **Väljastatud toote üksikasjad**.
1. Tehke grupi **Vastavus** vahekaardi **Varude haldus** toimingupaanil valik **Aruandluse üksikasjad**.
1. Määrake valitud toote õiged väärtused väljadel **Ohtliku materjali ladustamispiirang** ja **Ohtlik hoiatuse piirang**.

Aruanne **Ohtlike materjalide ladustamispiirang** võimaldab jälgida ohtlike materjalide varude tasemeid oma lao asukohtades, veendumaks, et need jäävad siin kehtestatud, ohututesse piiridesse. Lisateavet vt teemast [Ohtlike materjalide ladustamispiirangu aruanne](hazmat-reports.md#stock-limit-report).

## <a name="sales-order-transactions-that-include-hazardous-materials"></a>Ohtlikke materjale sisaldavad müügitellimuse kanded

Kui soovite lisada toote, mis on müügitellimusel klassifitseeritud kui ohtlik materjal, peate vastava kättetoimetaja seostama müügitellimusega. Avage müügitellimus ja seejärel määrake kiirkaardil **Tarne** väljad **Kättetoimetaja** ja **Vedaja teenus** vastavalt nõutule.

Kättetoimetaja on seostatud ka tarneviisiga. Seetõttu peate veenduma, et see teave oleks vastavuses ohtlike materjalide määrusega. Teisisõnu peab ohtliku materjali määruses määratud tarneviis vastama müügitellimuse päise spetsifikatsioonidele. Sel viisil on määrus, kättetoimetaja ja teenus ühendatud müügitellimusel kasutatavate saadetiste ridadega.

Pärast seda, kui müügitellimus on vormistatud ja saatmiseks valmis, saab selle lattu väljastada, et näidata müügi ja lao vahelisi ülekandeid.

## <a name="shipments-that-include-hazardous-materials"></a><a name="hazmat-shipments"></a>Saadetised, mis sisaldavad ohtlikke materjale

### <a name="view-hazardous-material-scores-for-each-shipment-line"></a>Saate kuvada iga saadetise rea ohtlike materjalide punktisummad

Saadetise lehel **Saadetise üksikasjad** kuvatakse ohtliku materjali kogukaas ja punktiväärtused, mis on arvutatud iga koormarea jaoks, mis on kaasatud sellesse saadetisse. Skooride ja kaalude vaatamiseks toimige järgmiselt.

1. Avage **Laohaldus \> Saadetised \> Kõik saadetised**.
1. Valige saadetis, et avada selle leht **Saadetise üksikasjad**.
1. Kontrolligeridu kiirkaardil **Koormaread**. Iga rea puhul näete ohtlike materjalide arvutusi järgmistel väljadel.

    - **Ohtliku materjali punktid** – sellel väljal kuvatakse koormarea ohtlike materjalide skoor. Väärtus arvutatakse vastavalt reeglitele ja väärtustele, mis on kehtestatud kohaldatava määruse jaoks ja väljastatud toote häälestuses. Arvutus võtab koormarea koguse ja viitab väljastatud toote kordajale [Materjalihalduse häälestuses](#material-management).
    - **Piiratud koguse netokaal** – toodete puhul, mis on märgitud piiratud kogusega toodetena nende ohtliku materjali sisu tõttu, kuvatakse sellel väljal koormareale kaasatud ohtliku sisu kogu netokaal. Arvutus põhineb toodetel, mis on märgitud ohtlikeks materjalideks väljastatud toote häälestuses. Kui kaup on märgitud piiratud kogusega kaubana, võtab arvutus iga koormarea koguse ja viitab väljastatud toote kaalule [Materjalihalduse häälestuses](#material-management).

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-shipment"></a>Saadetisse kaasatud ohtlike materjalide ühilduvuse kontrollimine

Süsteem saab hinnata, kas kõik saadetisse kaasatud ohtlikud materjalid sobivad saatmiseks koos. Ühilduvuse hindamiseks kontrollib süsteem iga saadetisse kaasatud tootele määratud ühilduvuse gruppi. Lisateavet vt teemast [Ohtlike materjalide ühilduvusgrupid](hazmat-setup.md#compatibility-groups).

Ühilduvusgrupi kontrolli käivitamiseks järgige neid toiminguid.

1. Avage **Laohaldus \> Saadetised \> Kõik saadetised**.
1. Valige saadetis, et avada selle leht **Saadetise üksikasjad**.
1. Tehke jaotise **Tegevused** vahekaardi **Saadetised** toimingupaanil valik **Ühilduvuskontroll**.

Kuvatakse teade, mis teavitab teid kontrolli tulemustest.

## <a name="loads-that-include-hazardous-materials"></a><a name="hazmat-loads"></a>Koormad, mis sisaldavad ohtlikke materjale

### <a name="view-hazardous-material-scores-for-each-load-line"></a>Saate kuvada iga koormarea ohtlike materjalide punktisummad

Koorma lehel **Koorma üksikasjad** kuvatakse ohtlike materjalide kogukaal ja punktiväärtused, mis on arvutatud selle koorma ja iga koormarea jaoks. Skooride ja kaalude vaatamiseks toimige järgmiselt.

1. Avage **Laohaldus \> Saadetised \> Kõik koormad**.
1. Valige koorem, et avada selle leht **Koorma üksikasjad**. (Koorma üksikasju saate avada ka seotud saadetise lingi valimisega.)
1. Kiirkaardil **Koorem** saate üle vaadata kogu koorma ohtlike materjalide koguskoori ja kaalud, kontrollides järgmisi välju.

    - **Ohtliku materjali punktid** – sellel väljal kuvatakse koorma ohtlike materjalide skoor. Väärtus arvutatakse vastavalt reeglitele ja väärtustele, mis on kehtestatud kohaldatava määruse jaoks ja väljastatud toote häälestuses. Arvutus võtab koormas sisalduva koguse ja viitab väljastatud toote kordajale [Materjalihalduse häälestuses](#material-management).
    - **Piiratud koguse netokaal** – toodete puhul, mis on märgitud piiratud kogusega toodetena nende ohtliku materjali sisu tõttu, kuvatakse sellel väljal koormasse kaasatud ohtliku sisu kogu netokaal. Arvutus põhineb toodetel, mis on märgitud ohtlikeks materjalideks väljastatud toote häälestuses. Kui kaup on märgitud piiratud kogusega kaubana, võtab arvutus iga koorma koguse ja viitab väljastatud toote kaalule [Materjalihalduse häälestuses](#material-management).

1. Üksikute ridade skooride ja kaalude ülevaatamiseks valige kiirkaart **Koormaread**. Iga rea kohta esitatud väärtused sarnanevad kogu koorma puhul esitatud väärtustele, nagu on kirjeldatud eelmises etapis.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-load"></a>Koormasse kaasatud ohtlike materjalide ühilduvuse kontrollimine

Süsteem saab hinnata, kas kõik koormasse kaasatud ohtlikud materjalid sobivad saatmiseks koos. Ühilduvuse hindamiseks kontrollib süsteem iga koormasse kaasatud tootele määratud ühilduvuse gruppi. Lisateavet vt teemast [Ohtlike materjalide ühilduvusgrupid](hazmat-setup.md#compatibility-groups).

Ühilduvusgrupi kontrolli käivitamiseks järgige neid toiminguid.

1. Avage **Laohaldus \> Saadetised \> Kõik koormad**.
1. Valige saadetis, et avada selle leht **Koorma üksikasjad**. (Koorma üksikasju saate avada ka seotud saadetise lingi valimisega.)
1. Tehke jaotise **Tegevused** vahekaardi **Koormad** toimingupaanil valik **Ühilduvuskontroll**.

Kuvatakse teade, mis teavitab teid kontrolli tulemustest.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]