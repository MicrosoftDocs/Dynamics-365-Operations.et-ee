---
title: Mis on uut või muudetud Warehouse Management laohalduse mobiilirakenduses
description: Selles teemas loetletakse Microsoft Dynamics 365 Supply Chain Management iga Warehouse Management mobiilirakenduse väljastatud versiooni uued ja muudetud funktsioonid.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261772"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>Mis on uut või muudetud Warehouse Management laohalduse mobiilirakenduses

[!include [banner](../includes/banner.md)]

Selles teemas loetletakse Microsoft Dynamics 365 Supply Chain Management iga Warehouse Management mobiilirakenduse väljastatud versiooni uued funktsioonid, parandused, täiustused ja teadaolevad vead.

## <a name="version-2060"></a>Versioon 2.0.6.0

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>Uued funktsioonid, parandused ja täiustused versioonis 2.0.6.0

See versioon tutvustab järgmisi uusi funktsioone, parandusi ja täiustusi:

- Demorežiim kuvab nüüd kõik sildid seadme keeles.
- Vähem tõenäoline, et saate järgmise tõrketeate: "Määratud suuruse jaoks ei leia sobivat vaadet."
- Töökaartide minimaalne kõrgus on suurenenud (juhul, kui tööloendis on konfigureeritud kolm või vähem välju).
- Üksikasjade kaartide allosas on veerised (fade out) parandatud.
- Serveriga vahetatud XML-failide kehtetuid sümboleid käsitsetakse nüüd graatsiliselt. (Näiteks mitteprinditavaid tähemärke käsitsetakse nüüd graafiliselt ega põhjusta enam rakenduse hangumist.)
- HTTP-tõrkeid (nt "tõrge 503") serveri nõude esitamise korral käsitsetakse nüüd graatsiliselt.
- Tõrke kuvamisel ei kuvata valikute loendit enam liitboksi juhtelementide puhul automaatselt.
- Rakendus ei lõpeta enam vastamist kasutaja sätetes valitud kuvapaigutuse tõttu.
- Tootepilti näidatakse nüüd iseteeninduskeskkonnas. (See muudatus rakendub ainult madala resolutsiooniga versioonidele. Failihalduse teenus ei toeta täissuurusega pilte iseteeninduskeskkonnas.)
- Probleem, mis hõlmas nullkoguse lühikesi valikuid on parandatud.
- Rakendus ei hangu enam, kui üksikasjakaart näitab mitut identset välja.

### <a name="known-issues-in-version-2060"></a>Teadaolevad probleemid versioonis 2.0.6.0

Selles versioonis on järgmised teadaolevad probleemid.

- Rakendus (eriti tööloend) muutub aja jooksul aeglasemaks.
- **Windowsi versioon:** kui USB-vidinat kasutatakse Windowsi skannimiseks, põhjustavad ebaühtlased tulemused skannitud sümbolite sassimineku.

## <a name="version-2050"></a>Versioon 2.0.5.0

See versioon tutvustab järgmisi uusi funktsioone, parandusi ja täiustusi:

- Kliendi saladus ei ole enam ühenduse sätete häälestamises peidetud.
- Selle täielikuks nägemiseks võite nüüd teksti pikalt vajutada.
- Veateade, kui ladustamiõigused puuduvad, on täiustatud.
- Teatud voogude jaoks on lisatud uued kontrolliseeriad.
- Edastamisnupp ei muutu enam akna suuruse tõttu kättesaadavaks.
- Suuremate nuppude kasutamisel saavad liugurid väiksematele ekraanidele edasi minna.
- Nelja nupuga ülekatet ei katkestata enam.
- Klaviatuur toetab nüüd kustutusnuppu.
- Ereduse probleem, mis võib tekkida klaviatuuri klahvi vajutamisel, on parandatud.
- Mitmed demoandmete probleemid on parandatud.
- Probleem, mis mõjutas numbrivälju üksikasjade lehel, on parandatud.
- Ekraani klaviatuur aeg-ajalt mõnes seadmes enam ei kao.
- Erinevad kasutajaliidese (UI) vead on fikseeritud, nt vead, mis mõjutasid taustavärvi ja paigutamist.
- Venekeelne kasutajaliides on täiustatud.
- Mitmed probleemid, mis põhjustasid süsteemi hangumise, on parandatud.
- Kalkulaatori taasavamisega seotud probleem on parandatud.
- **Android versioon:** probleem, mis põhjustas Android 4.4 hangumise, on parandatud.
- **Android versioon:** minimaalset skaleerimist on vähendatud 50 protsendini.

## <a name="version-2040"></a>Versioon 2.0.4.0

Versiooni 2.0.4.0 oli Warehouse Management laohalduse mobiilirakenduse esimene üldiselt saadaolev väljaanne.

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>Uued funktsioonid, parandused ja täiustused versioonis 2.0.4.0

See versioon sisaldab järgmisi uusi funktsioone, parandusi ja täiustusi, mis polnud eelvaate versioonis saadaval.

- Kui üksikasjade kaart sisaldab kahte sama andmesildiga silti, on üks siltidest peidetud.
- Erimärgid on nüüd vaikimisi kuvatud ja nende peitmise suvand on kasutaja sätetest eemaldatud.
- Keelatud esitamisnupud kuvatakse nüüd kompaktses käeshoitavas vaates kättesaamatuna.
- Juhtimisseadmete järjestuse loogika muutmine tagab sujuvama skaleerimise seadmete vahel. Seega on vaja fontide või nuppude taastmist vähem korrigeerida.
- Värvi vaikekujundus on muudetud *Tumedaks*.
- Lindivaatesse on lisatud keelatud edastamisnupu puuduv ikoon.
- Aegunud erandid viivad teid nüüd ühenduse lehele, selle asemel et kuvada viga real.
- Kui ühtegi edastamistegevust pole saadaval (nt **OK**, **Jah**, **Aktsepteeri**, **Valmis** või **Lõpetatud**), siis edastamise nupp on keelatud.
- Rakenduse stabiilsust on parandatud.
- Turvalisuse ületuskontrolli [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).
- **Windowsi versioon:** Windowsi probleem, kus menüüd ei reageerinud pärast akna suuruse muutust, on parandatud.

### <a name="known-issue-in-version-2040"></a>Teadaolev probleem versioonis 2.0.4.0

Selles versioonis on järgmine teadaolev probleem:

- Sellel versioonil on probleem seadmetega, mis kasutavad Androidi versiooni 4.4. Rakenduse kasutamisel võib sellel Androidi versioonil tekkida probleeme.
