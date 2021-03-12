---
title: Kaupluse valija moodul
description: See teema hõlmab kaupluse valija moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 74dbad4cb348f19b51ba8b84a1cd41fc5049708e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006331"
---
# <a name="store-selector-module"></a>Kaupluse valija moodul

[!include [banner](includes/banner.md)]

See teema hõlmab kaupluse valija moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Kliendid saavad kasutada kaupluse valija moodulit, et komplekteerida toode valitud poes pärast Internetis ostlemist. Commerce versioonis 10.0.13 sisaldab kaupluse valija moodul ka täiendavaid võimalusi, mis võivad näidata lehekülge **Leia kauplus**, mis näitab lähedalasuvate kauplusi.

Kaupluse valija moodul võimaldab kasutajatel sisestada asukoha (linn, maakond, aadress jne), et otsida kauplusi otsinguraadiuse piires. Mooduli esmakordsel avamisel kasutab see kaupluste otsimiseks kliendi brauseri asukohta (kui nõusolek on saadud).

## <a name="store-selector-module-usage-in-e-commerce"></a>Kaupluse valija mooduli kasutamine e-kaubanduses

- Kaupluse valija moodulit saab kasutada toote üksikasjade lehel (PDP), et valida kauplus järele tulemiseks.
- Kaupluse valija moodulit saab kasutada ostukorvi lehel, et valida kauplus järele tulemiseks.
- Kaupluse valija moodulit saab kasutada eraldiseisval lehel, kus kuvatakse kõik saadaolevad kauplused.

## <a name="bing-maps-integration"></a>Bing Maps integratsioon

Kaupluse valija moodul on integreeritud [Bing Maps REST-rakenduse programmeerimise liidestega (API)](https://docs.microsoft.com/bingmaps/rest-services/) Bingi geokodeerimise ja automaatse soovitamise funktsioonide kasutamiseks. Vajalik on Bing Maps kaartide API võti ja see tuleb lisada jagatud parameetrite lehele rakenduses Commerce peakontorid. Geokodeerimise API-d kasutatakse asukoha teisendamiseks laius-ja pikkuskraadideks. Autosuggest API-ga integreerimist kasutatakse otsingusoovituste näitamiseks, kui kasutajad sisestavad asukohad otsinguväljale.

Autosuggest REST API puhul peate tagama, et järgmised URL-id on lubatud saidi sisu turbepoliitikat (CSP) arvestades. Seadistus toimub Commerce'i saidiehitajas, lisades lubatud URL-id erinevatele saidi CSP-direktiividele (nt **img-src**). Lisateavet leiate teemast [Sisu turbepoliitika](manage-csp.md). 

- Lisage direktiivile **connect-src** väärtus **&#42;.bing.com**.
- Lisage direktiivile **img-src** väärtus **&#42;.virtualearth.net**.
- Lisage direktiivile **script-src** väärtused **&#42;.bing.com, &#42;.virtualearth.net**.
- Lisage direktiivile **script style-src** väärtus **&#42;.bing.com**.
 
## <a name="pickup-in-store-mode"></a>Järgi tulemine kauplusesse režiim

Kaupluse valijate moodul toetab **Järgi tulemine kauplusse** režiimis, mis kuvab kaupluste loendit, kus toode on järgi tulemuseks saadaval. See näitab ka kaupluse lahtioleku aegasid ja iga kaupluse toote laoseisu loendina. Kaupluse valija moodul eeldab toote sisu toote saadavuse kuvamiseks ja kasutaja toote ostukorvi lisamise lubamiseks, kui toote tarneviis on **järgitulemine** valitud kaupluses. Lisateavet vt teemast [Varude sätted](inventory-settings.md). 

Kaupluse valija moodulit saab lisada PDP-l ostukasti moodulisse, et kuvada kauplusi, kus toode on järele tulemiseks saadaval. Seda saab lisada ka ostukorvi moodulisse. Sellisel juhul on kaupluse valija moodulis näidatud järele tulemise suvandid iga ostukorvi rea kohta. Kauplise valija moodulit saab lisada ka teistele lehtedele või moodulitele laienduste ja kohanduste kaudu.

Selleks, et see stsenaarium töötaks, tuleb toodete tarneviisiks konfigureerida **järgi tulemine**. Vastasel juhul ei kuvata moodulit tootelehtedel. Lisateavet tarneviisi konfigureerimise kohta vaadake teemast [Tarneviiside häälestamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Järgmisel pildil on näide, kuidas kasutatakse kaupluse valija moodulit PDP-s.

![Kaupluse valija mooduli näide PDP-s](./media/BOPIS.PNG)

> [!NOTE]
> Versioonis 10.0.16 ja uuemates versioonides saab lubada uue funktsiooni, mis võimaldab organisatsioonil määratleda klientide jaoks mitu vastuvõtuviisi.  Kui see funktsioon on lubatud, täiustatakse kaupluse valijat ja teisi e-kaubanduse mooduleid, et võimaldada ostjal valida potentsiaalselt mitme pealevõtmise võimaluse vahel, kui see on konfigureeritud.  Lisateavet selle funktsiooni kohta leiate [sellest dokumentatsioonist](https://docs.microsoft.com/dynamics365/commerce/multiple-pickup-modes). 

## <a name="find-stores-mode"></a>Leia kauplused režiim

Kaupluse valija moodul toetab ka režiimi **Leia kauplused**. Seda režiimi saab kasutada kaupluse asukohtade lehe loomiseks, kus kuvatakse saadaolevad kauplused ja nende teave. Selles režiimis töötab kaupluse valija moodul toodete sisuga ja seda saab kasutada eraldiseisva moodulina mis tahes saidi lehel. Lisaks, kui asjakohased sätted on mooduli jaoks sisse lülitatud, saavad kasutajad valida kaupluse oma eelistatud kaupluseks. Kui kauplus on valitud kasutaja eelistatud kaupluseks, säilitatakse kaupluse ID brauseri küpsises. Seetõttu peab kasutaja küpsise nõusoleku teate aktsepteerima.

Järgmisel joonisel on kujutatud kaupluse valija mooduli näide, mida kasutatakse koos kaardi mooduliga kaupluse asukohtade lehel.

![Kaupluse valija mooduli ja kaardimooduli näide kaupluse asukohtade lehel](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a>Kaardi renderdamine

Kaupluse valija moodulit saab kasutada koos kaardi mooduliga, et näidata kaupluse asukohti kaardil. Kaardimooduli kohta lisateabe saamiseks vaadake teemat [Kaardimoodul](map-module.md)

## <a name="store-selector-module-properties"></a>Kaupluse valija mooduli atribuudid

| Atribuudi nimi | Väärtus | Kirjeldus |
|---------------|-------|-------------|
| Pealkiri | Tekst | Mooduli pealkiri. |
| Olek | **Leia kauplused** või **Järgi tulemine kauplusse** | **Leia kauplused** režiim kuvab saadaolevad kauplused. **Järgi tulemine kauplusse** võimaldab kasutajatel valida kaupluse, kuhu järgi minna. |
| Laad | **Dialoog** või **Tekstisisene** | Moodulit saab kuvada kas tekstisisesena või dialoogiaknas. |
| Määra eelistatud kaupluseks | **Tõene** või **Väär** | Kui see atribuut on seatud väärtusele **Tõene**, saavad kasutajad seada eelistatud kaupluse. Selle funktsiooni kasutamiseks peavad kasutajad nõustuma küpsise nõusoleku teatega. |
| Kuva kõik kauplused | **Tõene** või **Väär** | Kui see atribuut on seatud väärtusele **Tõene**, saavad kasutajad eirata atribuuti **Otsinguraadius** ja vaadata kõiki kauplusi. |
| Autosuggest valikud: maksimaalne tulemus | Number | See atribuut määratleb Autosuggest tulemuste maksimaalse arvu, mida saab kuvada Bingi Autosuggest API kaudu. |
| Otsinguraadius | Number | See atribuut määratleb kaupluste otsinguraadiuse miilides. Kui väärtust pole määratud, kasutatakse vaikimisi 50-miilist otsinguraadiust. |
| Teenusetingimused | URL |  See atribuut määrab teenusetingimuste URL-i, mis on vajalikud Bing Mapsi teenuse kasutamiseks. |

## <a name="add-a-store-selector-module-to-a-page"></a>Kaupluse valija mooduli lehele lisamine

**Järgi tulemine kauplusse** režiimis saab moodulit kasutada ainult PDP-l ja ostukorvi lehekülgedel. Selleks peab muutma režiimi **Järgi tulemine kauplusse** režiimiks mooduli atribuutide paanil.

- Lisateavet selle kohta, kuidas lisada kaupluse valija moodulit ostukasti moodulisse, vaadake teemast [Ostukasti moodul](add-buy-box.md). 
- Lisateavet selle kohta, kuidas lisada kaupluse valija moodulit ostukorvii moodulisse, vaadake teemast [Ostukorvi moodul](add-cart-module.md)

Kaupluse valija mooduli konfigureerimiseks, et näidata kaupluse asukohtade lehel saadaolevaid kauplusi (nagu joonisel, mis kuvatakse selles teemas) toimige järgmiselt.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Turundusmall** ja valige seejärel **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Valige dialoogiboksis **Vali mall** mall **Turundusmall**. Sisestage jaotises **Lehe nimi** väärtus **Poe asukohad** ja seejärel valige **OK**.
1. Uue lehe pesas **Peamine** valige kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.
1. Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Kahe veeruga konteiner** ja klõpsake seejärel **OK**.
1. Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**.
1. Määrake **X-väikese vaate pordi veeru konfiguratsiooni** väärtuseks **100%**.
1. Määrake **Väikese vaate pordi veeru konfiguratsiooni** väärtuseks **100%**.
1. Määrake **Keskmise vaate pordi veeru konfiguratsiooni** väärtuseks **33% 67%**.
1. Määrake **Suure vaate pordi veeru konfiguratsiooni** väärtuseks **33% 67%**.
1. Valige pesas **Kahe veeruga konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Kaupluse valija** ja klõpsake seejärel **OK**.
1. Seadke mooduli atribuutide paanil **Režiim** väärtuseks **Leia kauplused**.
1. Määrake **Otsinguraadius** väärtus miilides.
1. Määrake muud atribuudid, nt **Määrake eelistatud kaupluseks**, **Kuva kõik kauplused** ja **Luba automaatne soovitus** vastavalt vajadusele.
1. Valige pesas **Kahe veeruga konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Kaart** ja klõpsake seejärel **OK**.
1. Määrake mooduli atribuutide paanil kõik täiendavad atribuudid, mida vajate.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
 
## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Ostukastimoodul](add-buy-box.md)

[Ostukorvimoodul](add-cart-module.md)

[PDP lühiülevaade](quick-tour-pdp.md)

[Ostukorvi ja väljaregistreerimise lühiülevaade](quick-tour-cart-checkout.md)

[Tarneviiside häälestamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Organisatsiooni Bingi kaartide haldamine](dev-itpro/manage-bing-maps.md)

[Bing Maps REST API-d](https://docs.microsoft.com/bingmaps/rest-services/)

[Kaardimoodul](map-module.md)
