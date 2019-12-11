---
title: Ostukasti moodul
description: See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e86b1881e6829ccc33f36ada453af20c1815a2fa
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811137"
---
# <a name="buy-box-module"></a>Ostukasti moodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Mõiste *ostukast* viitab tavaliselt toote üksikasjade lehe alale, mis on lehe kuvatav osa ehk „above the fold” ja mis sisaldab kõige olulisemat teavet, mis on toote ostu tegemiseks vajalik. (Ala, mida nimetatakse inglise keeles „above the fold”, on nähtav, kui leht esmakordselt laeb, ilma et kasutaja peaks hiirega selle nägemiseks kerima.)

Ostukasti moodul on spetsiaalne konteiner, mida kasutatakse kõigi moodulite majutamiseks, mis on toote üksikasjade lehe ostukasti alal näidatud.

Toote üksikasjade lehe URL sisaldab toote ID-d. Kogu teave, mis on vajalik ostukasti mooduli renderdamiseks, tuletatakse sellest toote ID-st. Kui toote ID-d ei ole, siis ostukasti moodulit ei renderdata lehel õigesti. Seetõttu ei saa ostukasti moodulit kasutada ühelgi lehel, millel puudub toote kontekst (nt avaleht või turunduse leht).

## <a name="buy-box-module-properties-and-slots"></a>Ostukasti mooduli atribuudid ja pesad 

Konteinerina kontrollib ostukasti moodul osasid põhiatribuute, nagu laius. Laiuse säte määratleb, kas konteineri sees olevad moodulid peavad mahtuma sellesse konteinerisse või kas need saavad täita ekraani.

Toote üksikasjade lehel on ostukast jaotatud kaheks piirkonnaks: meediumipiirkond vasakul ja sisupiirkond paremal. Need kaks piirkonda on ostukasti moodulis esindatud pesadena. Iga pesa on eelkonfigureeritud aktsepteerima ainult kindlaid pesa poolt toetatud mooduleid. Näiteks toetab pesa **Meedia** ainult meediumigalerii moodulit.

Vaikimisi on meediumipiirkonna ja sisupiirkonna veeru laiuse suhe 2 : 1. Samas võib teema veergude laiuse allutada. Lisaks on mobiilsetel seadmetel kaks piirkonda virnastatud, nii et üks piirkond ilmub teise piirkonna all.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moodulid, mida saab ostukasti moodulis kasutada

- **Meediumigalerii** – seda moodulit kasutatakse toote üksikasjade lehel toote piltide näitamiseks. See võib toetada ühte kuni mitu pilti. See toetab ka pisipilte. Pisipildid saab paigutada kas horisontaalselt (reana pildi all) või vertikaalselt (veeruna pildi kõrval). Meediumigalerii mooduli saab lisada ostukasti mooduli pesale **Meedia**. Hetkel toetab see ainult pilte ja videoid.
- **Toote pealkiri** – see moodul näitab toote üksikasjade lehel toote pealkirja. Vaikimisi kasutatakse pealkirja silti **H1**, kuid pealkirja silti saab vajadusel muuta.
- **Toote hinnang** – selles moodulis kuvatakse kliendi tootele antud hinnangute alusel tärnhinnangud. Ostukasti moodul toob iga toote jaoks hinnangu teenusest toote hinnangud.
- **Toote hind** – see moodul kuvab toote hinna. Hind hõlmab läbikriipsutatud hindu ja allahindlusi.
- **Toote kirjeldus** – see moodul kuvab toote kirjelduse.
- **Toote konfiguratsioon** – see moodul näitab toote suurust, stiili ja mõõtmeid. Mõõtmete valijaid saab virnastada vertikaalselt või need võivad esineda kõrvuti. Kui tootevariant on valitud, värskendatakse ostukasti teisi atribuute (nt toote kirjeldus ja pildid), et näidata variandi teavet.
- **Toote kogus** – seda moodulit kasutatakse toote koguse konfigureerimiseks. Säte piirab toote või variandi kogust, mida saab ostukorvi lisada.
- **Lisa ostukorvi** – seda moodulit kasutatakse toimingu „Lisa ostukorvi” sooritamiseks. Ostukorvi saab lisada ainult toote või variandi. Teisisõnu ei saa põhitoodet ostukorvi lisada. Moodulil on atribuut **Navigeeri ostukorvi**, mille saidi autor saab määrata. Kui see atribuut on seatud väärtusele **Tõene**, võidakse kasutaja viia ostukorvi lehele iga kord, kui toiming „Lisa ostukorvi” käivitatakse. Kui see väärtus on seatud väärtusele **Väär**, saab klient jätkata toote üksikasjade lehe sirvimist pärast kaupade ostukorvi lisamist.
- **Lisa soovinimekirja** – seda moodulit kasutatakse kauba kliendi soovinimekirja lisamiseks. Soovinimekirja saab lisada ainult toote või variandi. Lisaks peab klient olema saidile sisse logitud. Moodul sisaldab tõrketöötluse loogikat tagamaks, et mõlemad tingimused on täidetud.
- **Otsing poes** – see moodul käivitab voo „osta veebis, käi poes järel”.
- **Kättesaamine poest** – see moodul kuvab lähedalasuvate poodide loendi, kus kaup on kohapeal olemas. Vaikimisi kuvab see moodul poed, mis jäävad kliendi asukohast 50 miili raadiusse. Samas saab otsingu raadiust selles moodulis kohandada. Iga poe jaoks teostatakse varude kontroll, kui varude kontrolli funktsioon on sisse lülitatud, ja kuvatakse vastav laos olemas või laost otsas teade.
- **Poodide otsing Bingi kaartidel** – seda moodulit saab kasutada poes kättesaamise mooduli sees. See võimaldab klientidel otsida poode sisestades asukoha. Bingi kaartide geokodeerimise rakenduse programmeerimisliidest (API) kasutatakse konkreetse asukoha teisendamiseks laius- ja pikkuskraadideks. Selle mooduli kasutamisel kuvatakse ainult kliendi praeguse asukoha lähedal asuvad poed ja klient ei saa teist asukohta otsida.
- **Sisurikas plokk** – see moodul võib näidata sõnumit, mida saidi autor või jaemüüja soovib ostukastis reklaamida, näiteks „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-FABRIKAM” või „Üle 100 euro maksvad tellimused saadetakse tasuta”. Sõnumeid juhib sisuhaldussüsteem (CMS).

## <a name="buy-box-module-settings"></a>Ostukasti mooduli sätted

Ostukasti moodulitel saab konfigureerida kolme sätet.

- **Maksimaalne kogus** – iga kauba maksimaalne arv, mida saab ostukorvi lisada. Näiteks võib jaemüüja otsustada, et ühe tehinguga saab müüa iga toodet ainult 10 tükki.
- **Varude kontroll** – kui väärtus on satud suvandile **Tõene**, saab kauba lisada ostukorvi ainult pärast seda, kui ostukasti moodul on veendunud, et see oleks laos olemas. See varude kontroll tehakse nii stsenaariumide jaoks, kus kaup saadetakse, kui ka stsenaariumide jaoks, kus sellele tullakse poodi järele. Kui väärtuseks on seatud suvand **Väär**, siis enne kauba ostukorvi lisamist ja tellimuse esitamist varude kontrolli ei tehta.
- **Varude puhver** – varusid hallatakse reaalajas ja kui paljud kliendid esitavad tellimusi, võib täpse varude arvu säilitamine olla keeruline. Seega saab varude jaoks määrata puhvri. Kui varude kontroll on tehtud, siis kui varusid on vähem kui puhvri kogus, käsitletakse toodet kui laost otsas. Seega kui müük toimub kiiresti läbi mitme kanali, nii et varade arv pole täielikult sünkroonitud, on vähem ohtu, et müüakse kaup, mis on laost otsas.

## <a name="retail-server-interaction"></a>Jaemüügiserveri suhtlus

Ostukasti moodul toob toote teabe jaemüügiserveri API-de abil. Kogu teabe toomiseks kasutatakse toote ID-d toote üksikasjade lehel.

## <a name="add-a-buy-box-module-to-a-page"></a>Lehele ostukasti mooduli lisamine

Uuele lehele ostukasti mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Looge fragment nimega **ostukasti fragment** ja lisage sellele ostukasti moodul.
1. Lisage ostukasti mooduli pesas **Meedia** meediumigalerii moodul.
1. Ostukasti mooduli pesas **Sisu** lisage järgmised moodulid: toote pealkiri, tootehinnang, toote hind, toote kirjeldus, toote konfiguratsioon, ostukorvi lisamine, soovinimekirja lisamine ja otsing poes. Soovitud paigutuse saavutamiseks saate mooduleid pesas **Sisu** ümber korraldada.
1. Valige poes otsimise moodul. Selles moodulis olevas pesas lisage poes kättesaamise moodul.
1. Poes kättesaamise mooduli pesas lisage poe Bingi kaartidelt otsimise moodul.
1. Registreerige leht ja avaldage see.
1. Looge toote üksikasjade lehel jaoks mall ja pange sellele nimeks **PDP mall**.
1. Lisage vaikeleht.
1. Lisage vaikelehe pessa **Peamine** ostukasti fragment.
1. Salvestage mall, kontrollige seda ja avaldage see.
1. Kasutage äsja loodud malli, et luua leht, mille nimi on **PDP leht**.
1. Lisage uue lehe pessa **Peamine** ostukasti fragment.
1. Salvestage ja kuvage lehe eelvaade. Lisage eelvaatelehe URL-ile päringustringi parameeter **?productid=&lt;toote ID&gt;**. Sel viisil kasutatakse eelvaatelehe laadimiseks ja renderdamiseks toote konteksti.
1. Registreerige leht ja avaldage see. Toote üksikasjade lehele peaks ilmuma ostukast.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteinermoodul](add-container-module.md)

[Ostukorvi moodul](add-cart-module.md)

[Maksmise moodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
