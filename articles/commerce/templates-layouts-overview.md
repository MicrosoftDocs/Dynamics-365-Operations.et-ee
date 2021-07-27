---
title: Mallide ja paigutuste ülevaade
description: Selles teemas räägitakse mallidest ja paigutustest rakenduses Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 62cc0bb9d62b0ab90e212b03e6c4efd9734dadec
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347412"
---
# <a name="templates-and-layouts-overview"></a>Mallide ja paigutuste ülevaade


[!include [banner](includes/banner.md)]

Mallid on rakenduse Microsoft Dynamics 365 Commerce lehemudeli põhielemendid. Kui teie eesmärk on muuta saidi loomise töövood võimalikult tõhusaks ja järjepidevaks, on oluline, et teaksite, kuidas malle oma veebisaidil ära kasutada. Varased otsused malli struktuuri kohta on olulised ning võivad oluliselt mõjutada igapäevaste, hooajaliste ja saidiüleste kaubamärgi värskenduste kulu ja kiirust. Hea struktuuriga mallidel on teisigi eeliseid. Näiteks aitavad need parandada saidiülese otsingumootori optimeerimise (SEO) skoore ja minimeerivad vigade esinemissagedust.

Hea võimalus mallidega alustamiseks on mõista mallide ja paigutuste funktsionaalseid eeliseid, nendevahelisi erinevusi ning hierarhiat.

Järgmisel joonisel on näha lehemudeli hierarhia renderdatud veebilehe taga.

![Lehemudeli diagramm.](../commerce/media/page-model-diagram.png)

| Üksus        | Põhifunktsioonid |
|---------------|----------------|
| Mall      | Mallid määravad mooduli suvandid ning paigutuste ja lehekülje eksemparide kogumi üldehituse. |
| Kujundus        | Paigutused määravad moodulite lõpliku valiku ja asetuse lehel või lehtede kogumil. |
| Lehekülge eksemplar | Lehekülje eksemplarid määravad konkreetsete lehtede andmed ja sisu. |

## <a name="templates"></a>Mallid

Mallid on rakenduse Dynamics 365 Commerce lehemudeli hierarhias kõige üleval ja need on saidi konfigureerimisel väga olulised. Põhimõtteliselt aitavad mallid kontrollida järjepidevust alampaigutuste ja -lehtede rühmas, määratledes alusstruktuuri ning luues suvandid järgmise paigutuse ja lehe loomise töövoogude jaoks. Mallid võivad muuta lihtsamaks sisu loomise protsessi eelmääratletud keskselt hallatavate elementide (nagu päised ja jalused) ja juhendatud loomisvoogude kaudu, mis aitavad tagada, et mooduli konfigureerimisvalikud oleksid kaubamärgile vastavad.

### <a name="controlling-consistency"></a>Järjepidevuse kontrollimine

Malli kujundades on tähtsaim äriotsus, mille peate langetama, see, kui palju kontrollib mall lehe loomise protsessi. Lihtsaim loodav malli tüüp on selline, mis jätab kõik lahtiseks järgmisele autorile, kuid sellel võivad olla pikaajalised tagajärjed mallist loodud lehtede hooldamises. Hästi kirjutatud mall toetab ja tagab sujuva loomiskogemuse, ent annab autoritele siiski piisavalt vabadust toimingu lõpetamiseks. Kõik need aspektid olenevad kontrollitasemest, mis mallile on antud.

Mallid võivad aidata sisu autoritel teha tõhusamat tööd ja püsida kaubamärgi juures järgmiselt.

- Mallid piiravad mooduleid, mida lehel saab kasutada.
- Soovitavad vaikemooduleid ja konfigureerimisvalikuid.
- Panevad paika mõned mooduli- ja konfigureerimisvalikud, mida kontrollitakse malli tasandil. Seda protsessi nimetatakse ka sätte *lukustamiseks*.

Järgmisel joonisel on näha, kuidas saab konfigureerida üldmalli (mall X).

- Kõikidel malli X alampaigutustel peavad olema päise konteiner, sisu konteiner ja jaluse konteiner.
- Mallis X on päise konteineri konfiguratsioon lukustatud ja seda saab muuta vaid mallis X. Kõikidel alampaigutustel ja -lehtedel on alati see päis.
- Sisu konteineri jaoks on vaja vähemalt üht ja kuni kümmet moodulit. Need moodulid määratakse järgmiste paigutuste ja lehtedega.
- Sisu konteineri jaoks on saadaval pannoo-, funktsiooni-, karussell- ja ribareklaami moodul.
- Jaluse konteiner konfigureeritakse mallis X, aga seda saab üle kirjutada järgmiste paigutuste ja lehtedega.

Selle näite mall määratleb lihtsa struktuuri ja suvandite kogumi järgmiste sisu autorite jaoks. Pange tähele, et mõni lehe osa (praegusel juhul päis) on täielikult määratletud ja mallis lukustatud ning neid ei saa järgmised autorid muuta. Muid osasid (praegusel juhul sisu) saavad järgmised autorid määratleda konkreetsete juhiste järgi (praegusel juhul konkreetset tüüpi moodulite minimaalne ja maksimaalne arv). Ja muud osad (praegusel juhul jalus) määratletakse mallis, aga neid saavad üle kirjutada järgmised autorid.

Oluline esimene samm saidi ja kaubamärgi administraatorite jaoks on määrata õige tasakaal alampaigutuse ning lehe autorite piirangute ja paindlikkuse vahel. Malle kasutades on see tasakaal täielikult konfigureeritav. See mõjutab, kas leheelemente värskendatakse keskselt (mallis lukustatud) või jäetakse need alamtasemetele, mis jäävad lehe hierarhias allapoole.

Mallide kasutamisega alustamiseks vt teemat [Mallidega töötamine](work-with-templates.md).

## <a name="layouts"></a>Paigutused

Paigutused on lehemudeli hierarhias järgmisel tasemel, mallide järel. Kui mall määrab kõik moodulid, mis lehel lubatud on, siis paigutus konkreetne valik mooduleid. Lehed on lehemudeli hierarhias järgmisel tasemel, paigutuste järel. Need määravad paigutusse valitud moodulite lokaliseeritud sisu.

Järgmises näites tuginetakse mallile eelmisest jaotisest ja näidatakse, kuidas saab konfigureerida põhipaigutust.

- Paigutuse ülemmall nõuab, et sisu konteineris oleks üks kuni kümme moodulit. Need võivad olla pannoo-, funktsiooni-, karussell- ja ribareklaami moodulid. Seega saab paigutus määrata järgmise moodulite valiku ja asetuse.

    - Sisu konteineri esimene moodul on ribareklaami moodul, millele järgnevad pannoomoodul ja kaks funktsioonimoodulit.
    - Esimene funktsioonimoodul on vasakjoondusega ja teine paremjoondusega.

- Kuigi ülemmallist päritakse vaikejalus, jättis malli autor jaluse lukustamata. Seega saab paigutus selle üle kirjutada, määratledes teistsuguse jaluse fragmendi.

Selle näite paigutus määratleb moodulite lõpliku asetuse alamlehtedel. Nagu malliga, saab ka paigutusega määratleda vaike- või lukustatud mooduli atribuute, mis edastatakse alati alamlehtedele (nt funktsioonimoodulite joondus). Paigutuse iga mooduli tegelik sisu või andmed määratletakse seejärel hierarhias veel madalamal, alamlehe igas eksemplaris. Oluline on eristada, et paigutused ei sisalda otseselt lokaliseeritavad sisu, nende alamlehed aga sisaldavad. Paigutuse peamine funktsioon on määratleda moodulite lõplik asetus ja vaikekonfiguratsioon alamlehtede jaoks.

See hierarhia on võimas kahel põhjusel. Esiteks, sama ülemmalli jagavaid paigutusi võetakse paigutuse vahetamise stsenaariumide jaoks sobivatena. Seega saab iga lehe paigutust vahetada muu paigutusega samast malli hierarhiast, ilma et selle lehetaseme sisu tuleks uuesti luua. Seda võib ära kasutada näiteks hooajaliste kujunduste värskendamiseks, katsetamiseks või saidi püsivaks ümberkujundamiseks. Teiseks pakuvad paigutused teist moodust lehtede grupi jagatud elementide keskseks muutmiseks, ilma et oleks vaja värskendada üksikuid lehti. Näiteks kui tootekategoorias on 1000 lehte, mis jagavad sama paigutust, saab mooduleid paigutuses ümber järjestada, ja see muudatus hakkab kohe kehtima kõigi 1000 alamlehel.

Seda hierarhiat tundes saate luua kiire ja tõhusa saidi struktuuri, mis aitab saidi arenedes aja jooksul vähendada kulusid, on skaleeritav ja annab paremaid tulemusi.

### <a name="preset-and-custom-layouts"></a>Eelseadistatud ja kohandatud paigutused

Teie saidi paigutused võivad olla kas *eelseadistatud* või *kohandatud*.

- **Eelseadistatud paigutused** sisaldavad lehe loomise töövoogu, kus kõik moodulid on juba valitud ja korraldatud ning vajalik on vaid sisestada andmed. See lähenemine võib aidata säästa aega, kui luua tuleb mitu lehte, millel on samad paigutuse nõudmised. Eelseadistatud paigutustel on alamlehtedega seos üks mitmele. Seetõttu saab üht eelseadistatud paigutust kasutada sadade või tuhandete alamlehtede mooduli korralduse keskseks kontrollimiseks.
- **Kohandatud paigutused** on põhimõtteliselt ühekordselt kasutatavad paigutused, mis juurutatakse ühele lehele. Neid pakuta valikuna uute lehtede loomisel või paigutuse vahetamise stsenaariumites. Selle lähenemise eelis on, et autor saab katsetada, luues kohandatud paigutust kasutava lehe. Kui autor soovib seejärel paigutust teistel lehtedel kasutada, saab selle hõlpsasti teisendada eelseadistatud paigutuseks. Uut eelseadistatud paigutust pakutakse seejärel valikuna lehe loomise töövoogudes ja paigutuse vahetuse stsenaariumites lehtedele samas malli hierarhias. Ka eelseadistatud paigutusi on võimalik muuta kohandatud paigutusteks. Nii saab autor lehe eelseadistatud paigutusest eraldada ja luua uue ühekordselt kasutatava paigutuse. (Sellele uuele kohandatud paigutusele kehtivad endiselt ülemmalli piirangud.)

Eelseadistatud ja kohandatud paigutusi redigeeritakse loomise tööriistakogumi eri osades. Kuna kohandatud paigutused ei olene teistest lehtedest, redigeeritakse neid otse lehe redigeerijas. Sellisel juhul on paigutuse olemasolu enamasti nähtav kasutajale ja see avaldatakse ainult lehetaseme atribuutides ning paigutuse suvandite toimingute kaudu. Kuid kuna eelseadistatud paigutuste muudatused võivad mõjutada paljusid alamlehti, tuleb neid redigeerida paigutuse redigeerijas, kus avaldamistoimingud võtavad arvesse täielikku mõju järgnevatele alamlehtedele.

Järgmisel joonisel on näha eelseadistatud ja kohandatud paigutused stsenaariumid.

![Eelseadistatud ja kohandatud paigutuse stsenaariumid.](../commerce/media/template-figure1.png)

Eelseadistatud paigutuste kasutamisega alustamiseks vt teemat [Eelseadistatud paigutustega töötamine](work-with-layouts.md).

## <a name="additional-resources"></a>Lisaressursid

[Mallidega töötamine](work-with-templates.md)

[Eelmääratud paigutustega töötamine](work-with-layouts.md)

[Avaldamisrühmadega töötamine](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]