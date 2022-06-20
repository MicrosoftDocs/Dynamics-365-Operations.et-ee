---
title: BYOD ajastatud pakett-tööde optimeerimine
description: See artikkel selgitab, kuidas optimeerida jõudlust, kui kasutate Microsoftile oma andmebaasi (BYOD) funktsiooni Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: 4df60a82e016ec8f3ba6ba0d70c261824961d221
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848309"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a>BYOD ajastatud pakett-tööde optimeerimine


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel selgitab, kuidas optimeerida jõudlust, kui kasutate oma andmebaasi (BYOD) funktsiooni. Lisateavet BYOD kohta leiate teemast [Oma andmebaasi toomine (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

## <a name="performance-considerations-for-data-export"></a>Andmeekspordi jõudluse kaalutlused

Pärast seda, kui üksused on sihtkoha andmebaasi avaldatud, saate andmete teisaldamiseks kasutada tööruumi **Andmehaldus** ekspordifunktsiooni. Ekspordifunktsiooni abil saate määratleda andmete teisaldamise tööd, mis sisaldab mitut üksust. Lisateavet andmete eksportimise kohta vt [Andmete importimis- ja eksportimistööde ülevaade](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

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

Astmelise jaotuse tegemiseks peate sisse lülitama lehe **Üksused** iga üksuse muudatuste jälgimise. Lisateabe saamiseks vt [Üksuste muudatuste jälgimise lubamine](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

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

**Lahendus:** SQL-i muudatuste jälgimise tabelid ei pruugi olla eeldatud olekus. Seda tüüpi juhtumite korral soovitame teil üksuse muudatuste jälgimise välja lülitada ja seejärel see uuesti sisse lülitada. Lisateabe saamiseks vt [Üksuste muudatuste jälgimise lubamine](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="staging-tables-arent-clearing"></a>Koondamistabelid ei tühjendata

**Probleem:** projekti ajalist jaotust kasutades ei tühjendata koondamistabeleid õigesti. Tabelis olevate andmete hulk kasvab, mis põhjustab jõudlusprobleeme.

**Lahendus:** koondamistabelites säilitatakse 7 päeva ajalugu. Seitsmest päevast vanemad ajaloolised andmed tühjendatakse automaatselt koondamistabelite **impordi-ekspordi ajastuspuhastuse** pakett-tööga. Kui see töö hangub, ei tühjenda tabelid õigesti. Selle pakett-töö taaskäivitamine jätkab protsessi, et tühjendada automaatselt koondamistabelid.

## <a name="see-also"></a>Vt ka

[Andmehalduse ülevaade](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Oma andmebaasi toomine (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Andmete importimis- ja eksportimistööde ülevaade](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[Üksuste muudatuste jälgimise lubamine](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
