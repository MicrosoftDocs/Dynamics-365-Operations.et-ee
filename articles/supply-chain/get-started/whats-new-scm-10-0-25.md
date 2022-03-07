---
title: Dynamics 365 Supply Chain Management 10.0.25 (aprill 2022) eelversioon
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Supply Chain Management 10.0.25 uusi või muutunud funktsioone.
author: kamaybac
ms.date: 02/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 0ce9bc4685542cf691d862c0fec76f3f7b40c6b6
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087316"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10025-april-2022"></a>Dynamics 365 Supply Chain Management 10.0.25 (aprill 2022) eelversioon

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles teemas loetletakse rakenduse Microsoft Dynamics 365 Supply Chain Management eelversiooni 10.0.25 uued või muutunud funktsioonid. Selle versiooni number on 10.0.1149 ja see on saadaval järgmiselt:

- **Väljaande eelversioon:** veebruar 2022
- **Väljalaske üldine kättesaadavus (iseseisev värskendamine):** märts 2022
- **Väljalaske üldine kättesaadavus (automaatne värskendamine):** aprill 2022

## <a name="features-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selles versioonis sisalduvad funktsioonid. Võime värskendada seda teemat, et lisada sellesse funktsioone, mis on loodud pärast selle esialgset avaldamist tehtud veaparandusi.

| Funktsiooniala | Funktsioon | Lisateave | Lubaja:   |
|---|---|---|---|
| Varud&nbsp;ja&nbsp;logistika | Ohtlike materjalide täiustused | Need täiustused tuginevad olemasolevatele ohtlike materjalide funktsionaalsusele, et aidata ettevõtetel ohtlike materjalide transportimisel eri geograafilistes piirkondades paremini järgida kohalikke eeskirju. <!-- KFM: Update to 2022w1 link when published -->| Funktsioonide haldus:<br>*Ohtlike materjalide täiustused* |
| Varud&nbsp;ja&nbsp;logistika | Pakkimistöö pakkimisjaamade jaoks | See funktsioon parandab oluliselt pakkimis- ja saatmistoimingute paindlikkust ja paindlikkust. Pakkimisprotsessi käigus saavad laotöötajad nüüd pakkida ja saata üksikuid pakke, mis on seotud sama saadetise ja koormusega. Tellimuse read, mis on osa samast saadetisest, ei pea tingimata koos lähetama, kui mõned kaubad on kohe saatmiseks valmis. Ühe tellimuse saab pakkida ja saata mitmesse pakki erinevatel saatmisaegadel, vähendades seeläbi ooteaegu ja lisades agility.<!-- KFM: Update to 2022w1 link when published --> | Funktsioonide haldus:<br>*Pakkimistöö pakkimisjaamade jaoks* |
| Varud&nbsp;ja&nbsp;logistika | [Skannige vöötkoode laos, kasutades GS1-vormingu standardeid](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/scan-barcodes-warehouse-using-gs1-format-standards) <!-- KFM: Update to 2022w1 link when published --> | [GS1 vöötkoodid ja QR-koodid](../warehousing/gs1-barcodes.md) | Funktsioonide haldus:<br>*GS1 vöötkoodide skannimine* |
| Tootmine | [Materjali tarbimine ja reserveeringud tootmispõranda täitmise liideses](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/material-consumption-reservations-production-floor-execution-interface) | [Kuidas töötajad kasutavad tootmisosakonna käivitusliidest](../production-control/production-floor-execution-use.md) | Funktsioonide haldus:<br>*(Eelvaade) Materjalikulu registreerimine tootmisosakonna käivitusliideses (WMS-loaga)* |
| Tootmine | [Materjali tarbimise registreerimine skaalaühikutes](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/register-material-consumption-scale-units) | [Tootmise täideviimise töökoormused pilv- ja perimeeterskaalaüksuste jaoks](../cloud-edge/cloud-edge-workload-manufacturing.md) | Funktsioonide haldus:<br>*Materjalikulu registreerimine mobiilirakenduse skaalaüksuses* |
| Planeerimine | [Plaani optimeerimise soovitused olemasoleva pakkumise optimeerimiseks](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planning-optimization-suggestions-optimize-existing-supply) | [Tegevusteated](../master-planning/action-messages.md) | Vaikimisi lubatud |
| Planeerimine | Plaanitud tellimuste lihtsustamine | [Plaanitud tellimuste lihtsustamine](../master-planning/planning-optimization/planned-orders-simplified.md ) | Funktsioonide haldus:<br>*Plaanitud tellimuste lihtsustamine* |

## <a name="feature-enhancements-included-in-this-release"></a>Selles väljalaskes sisalduvad funktsioonid

Järgmises tabelis on loetletud selle väljalaske funktsioonide täiustused. Kõik need täiustused parandavad olemasolevat funktsiooni järk-järgult. Kuna need on ainult täiustused, siis neid ei loetleta [väljalaskeplaanis](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Kindlustamaks, et need täiustused ei satu vastuollu olemasolevate kohanduste või eelistustega, lülitatakse iga neist vaikimisi välja (kui pole märgitud teisiti).

Kui soovite mõnda neist funktsioonidest sisse või välja lülitada, peate seda funktsioonihalduses [tegema](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Moodul | Funktsiooni nimi funktsioonihalduses | Lisateave |
|---|---|---|
| Varude ja laohaldus | (Poola) Võimaldab siduda mitu SAD-arvet ühe ostutellimuse reaga ühes SAD-is | See funktsioon võimaldab teil jagada ostutellimuse read ja linkida need ühe haldusdokumendiga (SAD), kui need ostutellimuse read konteeriti mitme erineva arve jaoks (nt erinevate saadetiste puhul). |
| Hanked | Mitme ostutaotluse konsolideerimine üheks ostutellimuseks aruandluskuupäeva järgi | See funktsioon võimaldab konsolideerida mitu ostutaotlused ühte ostutellimusse, kui erinevatel ostutaotlustel on erinevad arvestuskuupäevad. Ostutellimuse loomise ja nõudluse konsolideerimise ostupoliitika reegleid saab seadistada, et automatiseerida otsus rekvireerimisridade rühmitamise kohta ostutellimuse taseme arvestuskuupäeva alusel. Ostutellimuse konsolideerimist arvestuskuupäeva järgi ei toetata, kui eelarve juhtimine on lubatud, kuna arvestuskuupäeva kasutatakse eelarve reserveerimiseks ja koormamiseks. Seetõttu tuleks see säilitada üleminekul ostutaotluselt ostutellimusele. |
| Hanked | Keela ostutaotluse jaotamise lähtestamise nupp | See funktsioon keelab **lehel Raamatupidamise jaotus** nupu **Lähtestamine** ülevaatamisel olevate ostutaotluste jaoks. |
| Hanked | Kuva pärandi vaikimisi pakkumiskutse vastuse välja sätted | See funktsioon taaskehtestab pärand vaikimisi pakkumiskutse (RFQ) vastusevälja sätted, mis olid varem kasutajaliidesest eemaldatud. Need sätted ei paku boksist välja funktsioone, kuid neid saab kohandada, et seda vastavalt vajadusele pakkuda. Lubage see funktsioon, kui teie asutus on pakkumiskutse vastuse vaikesätete jaoks juba lisanud funktsioone või kavatseb seda teha. Kui see funktsioon on lubatud, pääsete seadetele juurde, minnes **lehele Hange ja hankimisparameetrid**, avades **vahekaardi Pakkumiskutse** ja valides **väljad Vaikimisi pakkumiskutse vastus**. |
| Hanked | Hankija finantsdimensioonide ühendamine ostutellimuse aktiivse dimensioonilingi finantsdimensiooniga | See funktsioon võimaldab ühendada finantsdimensioonid aktiivse dimensioonilingi finantsdimensioonidega hankijatelt pärast ostutaotluse kinnitamist, kui seadistate seose finantsdimensiooni ja saidi varude dimensiooni vahel. Ostutellimuse loomise ja nõudluse konsolideerimise ostupoliitika reegleid saab seadistada, et juhtida otsust finantsdimensioonide ühendamise kohta hankijatelt, kellel on ostutellimuse päise tasemel aktiivse dimensioonilingi finantsdimensioon. |
| Tootmise juhtimine | (Venemaa) Tootmisvalemi/komplekti ja automaatse GTD reserveeringu/tarbimise vaikeasustuse lubamine tootmises | Funktsioon võimaldab täiendavaid tootmisvõimalusi imporditud toorainest (ainult Venemaa lokaliseerimine):<ul><li>Tootmisvalemite ja -koosluste automaatse vaikeasukoha seadmine nii ressursigruppides kui ka ladudes.</li><li>Tooraine automaatne reserveerimine GTD-numbri *dimensiooni järgi* WMS-aktiveeritud ladudes vastavalt mitte-WMS-i reserveerimise algoritmile. See kehtib juhul, kui tooraine komplekteerimise *tööpoliitika* on olemas, kui **töö loomise meetodiks** on seatud *Mitte kunagi* ning lao, asukoha ja kaubanumbri seadistus vastab tootmistellimuse (partii) laokannetele.</li><li>Tooraine automaatne tarbimine GTD-numbri *dimensiooni järgi* komplekteerimisloendi sisestamisel vastavalt eelnevalt kirjeldatud omandatud broneeringule.</li></ul> |
| Laohaldus | Keelake oodatud kviitungid kvaliteettellimustest, mille valim on blokeeritud varudes | See funktsioon takistab süsteemil luua eeldatavaid sissetulekukandeid kvaliteeditellimuste jaoks, mis proovivad blokeerimisolekuga varusid. Kuna blokeeritud varu pole saadaval, eemaldab see funktsioon eeldatavad sissetulekud. See aitab tagada, et varud ei lõpe mitme blokeerimisolekuga, mis võib põhjustada andmete terviklikkuse probleeme. |
| Laohaldus | (Eelvaade) Skaalaüksuse tugi sissetulevate ja väljaminevate laotellimuste jaoks | Selle funktsiooni tõttu loob süsteem väljaminevaid laotellimusi väljalaske-lattu protsessi käigus ja loob sissetulevad laotellimused, kui üleviimistellimused konteeritakse lähetatuna. Seejärel sünkroonib süsteem iga sissetuleva või väljamineva laotellimuse tellimuse saatmise või vastuvõtmise eest vastutava skaalaüksusega. Pange tähele, et pärast selle funktsiooni lubamist tuleb teie laokäitlemise töökoormust täiendada. Lisateavet vt [Laohalduse töökoormused pilv- ja perimeeterskaalaüksuste jaoks](../cloud-edge/cloud-edge-workload-warehousing.md).<br><br>See funktsioon nõuab *funktsiooni AsNite* lahtisidumise tööd ja võimaldab ülekandetellimusi vastu võtta, kasutades litsentsimärgi vastuvõtmise protsessi laohalduse mobiilirakenduses. |

## <a name="feature-state-changes-in-this-release"></a>Funktsiooni oleku muudatused selles väljaandes

Järgmises tabelis on loetletud funktsioonid, mis muutusid kohustuslikuks või vaikimisi sisse alates 10.0.25. Kõik need funktsioonid lülitatakse teie süsteemi jaoks automaatselt sisse kohe, kui värskendate versioonile 10.0.25. Kohustuslikke funktsioone ei saa välja lülitada, kuid funktsioonihalduse [abil](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) saab vaikefunktsioonid siiski välja lülitada.

Tabelis on loetletud ka funktsioonid, mis olid varem avalikus eelvaates, kuid on muutunud üldiselt kättesaadavaks 10.0.25, mis tähendab, et neid soovitatakse nüüd kasutada tootmiskeskkondades. Need funktsioonid on vaikimisi välja lülitatud, kui pole märgitud teisiti, seega peate nende lubamiseks kasutama [funktsioonihaldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kui soovite neid kasutada.

| Moodul | Funktsiooni nimi | Funktsiooni olek |
| --- | --- | --- |
| Varahaldus | Hoolduskava käitamise ajal töökäskude rühmitamise reeglite rakendamine | Üldiselt saadaval |
| Varahaldus | Loenduripõhised hoolduse täiustused | Üldiselt saadaval |
| Kuluhaldus | Kuluarvutuse tase | Üldiselt saadaval |
| Kuluhaldus | Luba kasutaja määratletud partiinumbri seadistamine varude sulgemise tühistamise jaoks | Üldiselt saadaval |
| Kuluhaldus | Varude sulgemise edenemise üksikasjad | Üldiselt saadaval |
| Kuluhaldus | Varude standardomahinna ümberhindamise finantsdimensioonide vaikimisi valikud | Üldiselt saadaval |
| Kuluhaldus | Laoväärtuse aruande andmete puhastamine | Vaikimisi sees |
| Kuluhaldus | Laoväärtuse aruannete talletamine | Vaikimisi sees |
| Kuluhaldus | Kuva varude sulgemislogi ruudustikuna | Vaikimisi sees |
| Tehnilise muudatuse haldamine | Luba olemasolevate toodete muudatuste haldamine | Vaikimisi sees |
| Tehnilise muudatuse haldamine | Tehnilise muudatuse haldamine | Vaikimisi sees |
| Tehnilise muudatuse haldamine | Tootmise tehnilised teatised | Vaikimisi sees |
| Tehnilise muudatuse haldamine | Paranenud tehnilise muudatuse halduse atribuudi pärimine | Vaikimisi sees |
| Tehnilise muudatuse haldamine | Valemite ja nende koostisosade muudatuste haldamine | Vaikimisi sees |
| Tehnilise muudatuse haldamine | Toote valmisoleku kontrollid | Vaikimisi sees |
| Tehnilise muudatuse haldamine | Tehnikatoodetele variantide loomine | Vaikimisi sees |
| Varude ja laohaldus | Koosluseridadelt koosluseversiooniga navigeerimine | Kohustuslik |
| Koondplaneerimine | Plaanitud hulgi- ja partiina tellimuste partiideks jaotatud kinnitamine ja konsolideerimine | Üldiselt saadaval |
| Koondplaneerimine | Ressursside koos hooldusega plaanimine | Üldiselt saadaval |
| Koondplaneerimine | Koondplaani häälestusviisardi funktsioonide lubamine | Kohustuslik |
| Koondplaneerimine | Prognoosimudeli valimine nõudluse prognoosi üksikasjades | Kohustuslik |
| Koondplaneerimine | Koondplaneerimise edenemise visualiseerimine | Kohustuslik |
| Koondplaneerimine | Plaanitud tellimuste paralleelne kinnitamine | Kohustuslik |
| Koondplaneerimine | Filtreerimisega plaanitud tellimuse kinnitamine | Vaikimisi sees |
| Koondplaneerimine | Plaanitud tellimuste salvestatud vaated | Vaikimisi sees |
| Hanked | Keela ostutaotluse jaotamise lähtestamise nupp | Üldiselt saadaval |
| Hanked | Luba hankega seotud töövoogude lähtestamine | Üldiselt saadaval |
| Hanked | Võimalus kinnitada hankijakoostööst aktsepteeritud ostutellimused partiina | Kohustuslik |
| Hanked | Ostulepingu suletud olek | Kohustuslik |
| Hanked | Ridade lisamine ostulepinguga seotud ostutellimuse arvetele | Vaikimisi sees |
| Hanked | Lisa väli „Tellitud kogus” lehele „Toote sissetuleku sisestamine” | Vaikimisi sees |
| Hanked | Lubage hankijatel taotleda hankekategooriaid hankijate koostöö kaudu | Vaikimisi sees |
| Hanked | Ostutellimuste alates ja kuni summade tasud | Vaikimisi sees |
| Hanked | Tasude seadistamine saidi ja laoga | Vaikimisi sees |
| Hanked | Luba ostulõivu arvutamine aastatariifi alusel | Vaikimisi sees |
| Hanked | Ostulepingu vastutav isik | Vaikimisi sees |
| Hanked | Ostutellimuste salvestatud vaated | Vaikimisi sees |
| Tooteteabe haldus | Vaiketellimuse koguste range kinnitamine | Kohustuslik |
| Tooteteabe haldus | Koosluse aruande eeltöötlus aegumise vältimiseks | Vaikimisi sees |
| Tooteteabe haldus | Jaota finantsdimensioonid kaubamalle kasutades vaikimisi eraldi | Vaikimisi sees |
| Tooteteabe haldus | Luba kaubamallide jaoks tootedimensioonigrupid | Vaikimisi sees |
| Tooteteabe haldus | Loo tootevariantide nimed nomenklatuuri alusel uuesti | Vaikimisi sees |
| Tooteteabe haldus | Variandi soovituste lehe täiustused | Vaikimisi sees |
| Tootmise juhtimine | Tegeliku kaalu koguse komplekteerimise paranenud tootlikkus | Üldiselt saadaval |
| Tootmise juhtimine | Töökaardi terminali lehele on lisatud uus nupp katkestuse peatamiseks | Kohustuslik |
| Tootmise juhtimine | Identifitseerimisnumbri automaatse genereerimise lubamine lõpetamisest teatamisel töökaardi vahendis | Kohustuslik |
| Tootmise juhtimine | Luba alltöövõtukaupade osaline vastuvõtmine ja lahendage probleem hankija tüüpi koosluseridade praagi arvutamisega. | Kohustuslik |
| Tootmise juhtimine | Funktsioon töökaardi seadme ja töökaardi terminali lukustamiseks, et neid saaks puhastada | Kohustuslik |
| Tootmise juhtimine | Täiustused dialoogides Kinnita ja Ülekandmistööd | Kohustuslik |
| Tootmise juhtimine | Töökaardi vahendile on lisatud lõpetatuks märkimise litsentsiplaat | Kohustuslik |
| Tootmise juhtimine | Sildi printimine töökaardi vahendilt | Kohustuslik |
| Tootmise juhtimine | Tootmisosakonna täideviimine | Kohustuslik |
| Tootmise juhtimine | Tootmisosakonna täideviimisliidese varahoolduse funktsioon | Vaikimisi sees |
| Tootmise juhtimine | Tootmisosakonna täideviimisliidese töö otsing | Vaikimisi sees |
| Tootmise juhtimine | Vaikimisi tootmisbroneeringu alistamine | Vaikimisi sees |
| Tootmise juhtimine | Kuva tootmisosakonna täideviimisliidese täielikud seeria-, partii- ja numbrimärginumbrid | Vaikimisi sees |
| Müük ja turundus | Müügitellimuse üksikasjade jõudlustäiustus | Üldiselt saadaval |
| Müük ja turundus | Müügipakkumise üksikasjade jõudlustäiustus | Üldiselt saadaval |
| Müük ja turundus | Müügitellimusele viitavate andmete ekspordipoliitika | Kohustuslik |
| Müük ja turundus | Müügitellimusest ostutellimuseni ridade kustutamise poliitika | Kohustuslik |
| Müük ja turundus | Müügipakkumisele viitavate andmete ekspordipoliitika | Kohustuslik |
| Müük ja turundus | Kontaktisiku andmeüksuse ekspordi optimeerimine | Vaikimisi sees |
| Müük ja turundus | Lubage müügipakkumise dokumendi sissejuhatuse ja dokumendi järelduste väljade otsing | Vaikimisi sees |
| Müük ja turundus | Parandage klientide aruande „100 esimest” jõudlust | Vaikimisi sees |
| Müük ja turundus | Prognoositava kliendisaldo ümberarvutamine | Vaikimisi sees |
| Müük ja turundus | Müügi tagastustellimuse rea registreerimine kümnendkoha täpsusega koos tegeliku kaaluga ja ilma selleta | Vaikimisi sees |
| Müük ja turundus | Müügi ja turunduse salvestatud vaated | Vaikimisi sees |
| Müük ja turundus | Ühe klõpsuga müügitellimuse kinnitus | Vaikimisi sees |
| Laohaldus | Asukohadirektiividega ristiliaadimismallid | Üldiselt saadaval |
| Laohaldus | Keelake oodatud kviitungid kvaliteettellimustest, mille valim on blokeeritud varudes | Üldiselt saadaval |
| Laohaldus | Litsentsiplaadi vastuvõtu ajalugu | Üldiselt saadaval |
| Laohaldus | Ümmarda kogused lattu väljastamiseks lähima müügiüksuseni | Üldiselt saadaval |
| Laohaldus | Laorakenduse tööloendite skaalaüksuse tugi | Üldiselt saadaval |
| Laohaldus | Saadetise voo sildi üksikasjad | Üldiselt saadaval |
| Laohaldus | Kasutage pakkimisjaamas konteinerite sulgemiseks / uuesti avamiseks kiiremat API-d | Üldiselt saadaval |
| Laohaldus | Kinnitage täiendamise tööde jaoks valitud mallid | Üldiselt saadaval |
| Laohaldus | Täiendamise malli lubamine, et kasutada olemasolevat viivitamatut täiendamise tööd (üksuste üleselt) | Kohustuslik |
| Laohaldus | GUID-ide automaatne määramine WHS-i kasutaja loomisel | Kohustuslik |
| Laohaldus | Jäädvusta lao rakenduses koorma kaupade vastuvõtmise ajal tootevariandid ja jälgimisdimensioonid | Kohustuslik |
| Laohaldus | Jälgimisdimensioonide kaudu juhitavate kaupade varude oleku muutmine | Kohustuslik |
| Laohaldus | Töö töökausta muutmine | Kohustuslik |
| Laohaldus | Kogumi positsioon on täis | Kohustuslik |
| Laohaldus | Kogumi kõrvalepaneku funktsioon | Kohustuslik |
| Laohaldus | Kinnitamine ja üleviimine | Kohustuslik |
| Laohaldus | Pakett-töös väljuvate saadetiste kinnitamine | Kohustuslik |
| Laohaldus | Saate kontrollida, kas mobiilsetes seadmetes kuvatakse vastuvõtu kokkuvõttelehte | Kohustuslik |
| Laohaldus | Varude käsitsi paigutamise toimingu edasilükatud töötlemine | Kohustuslik |
| Laohaldus | Ärge lubage luua koormusi, mis ei vasta lainekoormuse hoonemalli nõuetele | Kohustuslik |
| Laohaldus | Täiustatud litsentsiplaadi sildipaigutused | Kohustuslik |
| Laohaldus | Mitme SKU asukohakorralduste kõigi toimingute hindamine | Kohustuslik |
| Laohaldus | Peida koguväärtuse väli lehtedel "Kõik koormused" ja "Koormuse üksikasjad" | Kohustuslik |
| Laohaldus | Litsentsiplaadi sildi koostekonfiguratsioon | Kohustuslik |
| Laohaldus | Koorma rea käsitsi korrigeerimine administraatorile või sarnastele usaldusväärsetele kasutajatele | Kohustuslik |
| Laohaldus | Asukoha litsentsiplaadi paigutus | Kohustuslik |
| Laohaldus | Asukoha tootedimensioonide segamine | Kohustuslik |
| Laohaldus | Muuda mobiilse seadme varude liikumise varude oleku väli redigeeritavaks | Kohustuslik |
| Laohaldus | Käsitsi müügirea komplekteerimise teenus administraatorile või sarnastele usaldusväärsetele kasutajatele | Kohustuslik |
| Laohaldus | Üleviimistellimusega lähetatud litsentsiplaatide kasutamise takistamine kõikides teistes ladudes peale sihtlao | Kohustuslik |
| Laohaldus | Viip välja „Asukoht/litsentsiplaat” mitmetähenduslike väärtuste lahendamiseks | Kohustuslik |
| Laohaldus | Kvaliteedikontroll | Kohustuslik |
| Laohaldus | Uue laorakenduse kasutajasätted, ikoonid ja etappide pealkirjad | Kohustuslik |
| Laohaldus | Täiendav asukohatsoon | Vaikimisi sees |
| Laohaldus | Laorakenduses ülekandetellimuste loomine ja töötlemine | Vaikimisi sees |
| Laohaldus | Luba lao mobiilsete seadmete jaoks kiire kinnitamine | Vaikimisi sees |
| Laohaldus | Kauba konsolideerimise asukoha kasutamine | Vaikimisi sees |
| Laohaldus | Maksimaalne täitmisaeg laohalduse laoseisu kirjete puhastustööks | Vaikimisi sees |
| Laohaldus | Väljamineva töökoormuse visualiseerimine | Vaikimisi sees |
| Laohaldus | Laorakenduse sündmuste töötlemine | Vaikimisi sees |
| Laohaldus | Koorma planeerimise töölaua salvestatud vaade | Vaikimisi sees |
| Laohaldus | Töö üksikasjade lehe salvestatud vaade | Vaikimisi sees |
| Laohaldus | Voo töötlemise salvestatud vaade | Vaikimisi sees |
| Laohaldus | Koormuse töötlemise salvestatud vaated | Vaikimisi sees |
| Laohaldus | Saadetise töötlemise salvestatud vaated | Vaikimisi sees |
| Laohaldus | Voo pakett-töö üksikasjad | Vaikimisi sees |
| Laohaldus | Voo täitmise teatised | Vaikimisi sees |

## <a name="additional-resources"></a>Lisaressursid

### <a name="platform-updates-for-finance-and-operations-apps"></a>Rakenduse Finance and Operations platvormi värskendused

Microsoft Dynamics 365 Supply Chain Management 10.0.25 sisaldab platvormivärskendusi. Lisateavet leiate teemast [Finance and Operationsi rakenduste versiooni 10.0.25 platvormi värskendused (aprill 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-25.md).

### <a name="bug-fixes"></a>Veaparandused

Lisateabe saamiseks veaparanduste kohta, mis sisalduvad 10.0.25 uuendustes, logige sisse teenusesse Lifecycle Services (LCS) ja vaadake [KB artiklit](https://fix.lcs.dynamics.com/Issue/Details?bugId=654580&dbType=3&qc=3799fa965b008dd980d27cf740e4582e6384ec6601ae8a35b7eaec6f1287a868).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 1 plaan

Kas teile pakuvad huvi meie ärirakenduste või platvormi uued ja hiljuti väljaantud võimalused?

Vaadake [Dynamics 365 ja majandusharu pilved: 2022 väljalaskevoo 1 plaan](/dynamics365-release-plan/2022wave1/). Käsitleme ühes dokumendis kõiki üksikasju otsast lõpuni ja ülevalt alla, millest võite plaanide tegemisel lähtuda.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Eemaldatud ja aegunud Supply Chain Managementi funktsioonid

Teemas [Eemaldatud või aegunud Dynamics 365 Supply Chain Managementi funktsioonid](removed-deprecated-features-scm-updates.md) kirjeldatakse funktsioone, mis on eemaldatud või aegunud või kavandatakse eemaldada Supply Chain Managementist.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

Enne mis tahes funktsiooni eemaldamist tootest, teavitatakse aegumisest 12 kuud ette teemas [Eemaldatud või aegunud Dynamics 365 Supply Chain Managementi funktsioonid](removed-deprecated-features-scm-updates.md).

Murranguliste muudatuste puhul, mis mõjutavad ainult kompileerimise aega, kuid on binaarselt ühilduvad liivakasti- ja tootmiskeskkondadega, on aegumise aeg vähem kui 12 kuud. Need on tavaliselt funktsionaalsed uuendused, mida tuleb teha kompilaatori jaoks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
