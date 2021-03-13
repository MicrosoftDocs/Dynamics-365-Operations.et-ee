---
title: BYOD ajastatud pakett-tööde optimeerimine
description: Selles teemas selgitatakse, kuidas optimeerida jõudlust, kui kasutate teenuses Microsoft Dynamics 365 Human Resources oma andmebaasi toomise (BYOD) funktsiooni.
author: andreabichsel
manager: tfehr
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: 4b9cf4b4181b64ef4daf397edd852fb2f881424e
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112150"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a>BYOD ajastatud pakett-tööde optimeerimine

Selles teemas selgitatakse, kuidas optimeerida jõudlust, kui kasutate oma andmebaasi toomise (BYOD) funktsiooni. Lisateavet BYOD kohta leiate teemast [Oma andmebaasi toomine (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database?toc=/dynamics365/human-resources/toc.json).

## <a name="performance-considerations-for-data-export"></a>Andmeekspordi jõudluse kaalutlused

Pärast seda, kui üksused on sihtkoha andmebaasi avaldatud, saate andmete teisaldamiseks kasutada tööruumi **Andmehaldus** ekspordifunktsiooni. Ekspordifunktsiooni abil saate määratleda andmete teisaldamise tööd, mis sisaldab mitut üksust. Lisateavet andmete eksportimise kohta vt [Andmete importimis- ja eksportimistööde ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job?toc=/dynamics365/human-resources/toc.json).

Andmete eksportimiseks muusse sihtvormingusse (nt komaga eraldatud väärtustega (CSV) fail) saate kasutada lehekülge **Eksportimine**. See lehekülg toetab ka SQL-i andmebaase teise sihtkohana.

Saate luua andmeprojekti, millel on mitu üksust, ja kasutada pakett-tööd andmeprojekti käitamise ajastamiseks. Kui valite suvandi **Eksportimine pakett-tööna**, saate ajastada andmeekspordi regulaarse käitamise.

BYOD ekspordi üldise usaldusväärsuse säilitamiseks peate olema ettevaatlik, kui lisate ekspordiprojektile mitu üksust. Kui määrate samale projektile lisatavate üksuste arvu, kaaluge järgmisi parameetreid.

- Üksuste keerukus
- Eeldatav andmemaht üksuse kohta
- Üldine aeg, mis on vajalik ekspordi lõpetamiseks töö tasemel

Parima jõudluse saavutamiseks vältige sadade üksuste lisamist ühte projekti. Soovitame luua mitu tööd, millest igaüks sisaldab vähem üksusi.

## <a name="scheduling-byod-batch-jobs"></a>BYOD pakett-tööde ajastamine

Et aidata vähendada teenuse Microsoft Dynamics 365 Human Resources mõju kasutajatele, käitage BYOD pakett-töid öösiti või väljaspool tööaega. Kontrollige kindlasti korduvate pakett-tööde ajavööndit. Osad pakett-tööd võivad kasutada Lääneranniku aega (PST).

Jõudlusprobleemide vältimiseks kaaluge järgmisi tegureid, kui konfigureerite BYOD pakett-tööde ajastamise sagedust.

- Iga pakett-töö lõpuleviimiseks vajalik aeg
- BYOD andmete ärivajadus

Määrake iga pakett-töö sagedus väärtusele, mis tagab, et töö saab lõpule viia enne järgmise ajastatud käitusaja algust. Vältige mitme töö paralleelset käitamist, kuna selline lähenemine võib negatiivselt mõjutada rakenduse Human Resources jõudlust.

Parima jõudluse tagamiseks kasutage BYOD pakett-tööde ajastamiseks suvandit **Ekspordi pakett-tööna** lehel **Eksportimine**. Vältige korduvate eksportide ajastamist lehel **Halda \> Halda korduvaid andmetöid**.

## <a name="incremental-export"></a>Astmeline eksport

Kui lisate üksuse andmete eksportimisele, saate teha kas astmelise jaotuse (eksport) või täieliku jaotuse. Täielik jaotus kustutab BYOD andmebaasi üksusest kõik olemasolevad kirjed. Seejärel sisestatakse praeguste kirjete kogum rakenduse Human Resources üksusest.

Astmelise jaotuse tegemiseks peate sisse lülitama lehe **Üksused** iga üksuse muudatuste jälgimise. Lisateabe saamiseks vt [Üksuste muudatuste jälgimise lubamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json).

Kui valite astmelise jaotuse, on esimene jaotus alati täielik jaotus. SQL jälgib muudatusi sellest esimesest jaotusest. Uue kirje sisestamisel või kirje värskendamisel või kustutamisel kajastub muudatus sihtkoha üksuses.

## <a name="time-outs"></a>Ajalõpud

Siin on BYOD ekspordi vaikimisi ajalõpud.

- 10 minutit kärpimiseks
- Üks tund hulgilisamiseks

Kui mahud on suured, ei pruugi need ajalõpusätted piisavad olla. Nende värskendamiseks avage **Dokumendihaldus \> Raamistiku parameetrid \> Oma andmebaasi toomine**. Need ajalõpud on ettevõtte-kohased ja tuleb iga ettevõte jaoks eraldi määrata.

## <a name="known-limitations"></a>Teadaolevad piirangud

Funktsioonil BYOD on järgmised piirangud.

- Sünkroonimisel ei tohi andmebaasis olla aktiivseid lukke. Aktiivsed lukud võivad põhjustada aeglast kirjutamist või isegi andmete Azure'i SQL-i andmebaasi eksportimise nurjumist.
- Te ei saa eksportida liitüksusi oma andmebaasi. Praegu ei toetata liitüksusi. Peate eksportima üksikuid üksusi, mis moodustavad liitüksuse. Siiski saate mõlemaid üksusi samasse projekti eksportida.
- Üksusi, millel pole kordumatuid võtmeid, ei saa astmelise jaotuse abil eksportida. Võite sellele piiranguga kokku puutuda eriti siis, kui proovite kirjeid valmisüksustest astmeliselt eksportida. Kuna need üksused on loodud lubama andmeimporti, pole neil kordumatut võtit.

## <a name="troubleshooting"></a>Tõrkeotsing

### <a name="incremental-push-doesnt-work-correctly"></a>Astmeline jaotus ei tööta õigesti

**Probleem:** kui üksuse jaoks tehakse täielik jaotus, kuvatakse BYOD-s suur kirjete kogum, kui kasutate lauset **vali**. Kui te aga teete astmelise jaotuse, kuvatakse BYOD-s ainult mõned kirjed. Näib, et astmeline jaotus kustutas kõik kirjed ja lisas ainult muudetud kirjed BYOD-s.

**Lahendus:** SQL-i muudatuste jälgimise tabelid ei pruugi olla eeldatud olekus. Seda tüüpi juhtumite korral soovitame teil üksuse muudatuste jälgimise välja lülitada ja seejärel see uuesti sisse lülitada. Lisateabe saamiseks vt [Üksuste muudatuste jälgimise lubamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json).

## <a name="see-also"></a>Vt ka

[Andmehalduse ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages?toc=/dynamics365/human-resources/toc.json)<br>
[Oma andmebaasi toomine (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database?toc=/dynamics365/human-resources/toc.json)<br>
[Andmete importimis- ja eksportimistööde ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-import-export-job?toc=/dynamics365/human-resources/toc.json)<br>
[Üksuste muudatuste jälgimise lubamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track?toc=/dynamics365/human-resources/toc.json)
