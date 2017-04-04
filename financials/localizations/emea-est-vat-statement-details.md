---
title: "Käibemaksu väljavõtte üksikasjad Eesti"
description: See teema selgitab kuidas km aruande juriidiliste isikutele Eestis.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxPeriod, TaxReportCollection, TaxReportVoucher
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 266904
ms.assetid: 7a804f8e-3595-463c-8371-21425c992c91
ms.search.region: Estonia
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: f7fd20ef0c78bc781f0ef9f17fc612723906ac78
ms.openlocfilehash: 8035617516e2e3513b40a3c937cfc65fb7e09992
ms.lasthandoff: 03/31/2017


---

# <a name="vat-statement-details-for-estonia"></a>Käibemaksu väljavõtte üksikasjad Eesti

See teema selgitab kuidas km aruande juriidiliste isikutele Eestis.

See teema sisaldab riigi-/ regioonikohaste teavet seadistuse juures käibemaks (VAT) juriidiliste isikutele Eestis ainult. KM aruannete seadistuse kohta lisateabe saamiseks vaadake [km aruandlus](emea-vat-reporting.md).

## <a name="set-up-sales-tax-authorities"></a>Maksuhaldurite seadistamine
Ja õige vormingu korral maksuhaldur käibemaksu deklaratsiooni loomiseks peate seadistama aruande paigutuse käibemaksuhalduritele. Kohta ning **maksuhaldur** lehekülg, mis on **aruande paigutus** valige **Eesti aruande paigutus**. Valige sama maksuhalduri kasutatakse käibemaksukoode käibemaksu tasakaalustusperioodi.

## <a name="set-up-sales-tax-reporting-codes"></a>Saate häälestada käibemaksuaruandluse koode.
Siin on näide, mis näitab Käibemaksuaruandluse koodide genereerimiseks käibemaksudeklaratsioonide kasutamist.

| Käibemaksu aruandluskood | Kirjeldus                                                                                                                                                                                                                                   | Rida on km tagasi (KMD) |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| 1                        | Toimingud ja tehingud, mida maksustatakse 20% määraga                                                                                                                                                                         | 1                            |
| 11                       | Omatarve kaupu või teenuseid, mis maksustatakse 20%                                                                                                                                                                               | 1,1                          |
| 2                        | Toiminguid ja tehinguid, mis maksustatakse 9% määraga                                                                                                                                                                          | 2                            |
| 21                       | Omatarve kaupu või teenuseid, mis maksustatakse 9%                                                                                                                                                                                | 2,1                          |
| 3                        | Toiminguid ja tehinguid, mis maksustatakse määraga 0%, mis on hinna sees                                                                                                                                                               | 3                            |
| 31                       | Kaubad ja teenused, mis osutatakse teise liikmesriigi riigi/maksukohustuslane on piiratud vastutusega, kaasa arvatud maksukohustuslase kokku ühendusesisese käibe                                                                         | 3.1                          |
| 311                      | Kauba ühendusesisese käibe                                                                                                                                                                                                               | 3.1.1                        |
| 32                       | Kaupade, kaasa arvatud                                                                                                                                                                                                                    | 3.2                          |
| 321                      | Müük reisijatele, mis hõlmab käibemaksu tagastamine                                                                                                                                                                                            | 3.2.1                        |
| 5                        | Kokku summa, millest lahutatakse vastavalt seadusele, hinna sees on                                                                                                                                                            | 5                            |
| 51                       | Käibemaksu, mis on tasutud või ka tasumisele import                                                                                                                                                                                                         | 5.1                          |
| 52                       | Käibemaksu, mis on tasutud või ka tasumisele põhivarade soetamine                                                                                                                                                                                | 5.2                          |
| 6                        | Kogu territooriumil, mis on saadud teises liikmesriigis, kaasa arvatud maksukohustuslase                                                                                                           | 6                            |
| 61                       | Kaupade ühendusesisene soetamine                                                                                                                                                                                                         | 6.1                          |
| 7                        | Muud kaubad ja teenused, mida maksustatakse käibemaksuga, kaasa arvatud soetamine                                                                                                                                                                    | 7                            |
| 71                       | Kinnisasja ja metallijäätmete mis maksustatakse erikorra käibemaksu kehtestamist kinnisasja, metallijäätmete ja Väärismetallid (Vata §41) poolt                                                                    | 7.1                          |
| 8                        | Pakkumine, mida ei maksustata                                                                                                                                                                                                                | 8                            |
| 9                        | Esitama kauba, mis on maksustada kinnisasja käibemaksu kehtestada erikord, metallist jäätmete ja Väärismetallid (käibemaksu seaduse §1 41) ja näidatakse paigaldatava või kokkupandava koguda kaupade maksustatav väärtus | 9                            |
| 1010                     | Korrigeerimine (+)                                                                                                                                                                                                                               | 10                           |
| 1011                     | Täpsustused (-)                                                                                                                                                                                                                               | 11                           |

## <a name="set-up-vat-declaration-tax-codes"></a>Käibemaksu deklaratsiooni käibemaksukoodide seadistamine
Käibemaksu deklaratsiooni maksu koode kasutatakse käibemaksukoodide vastendamiseks väärtused, mis on vajalikud avalduses (20, 9, 20erikord, või 9erikord). Peale iga maksukoodi saate määrata valikuline müük ja kommentaar ostutähiseid (01, 02 või 03 vastas ja 11 või 12 ostmiseks). Luua käibemaksu deklaratsiooni maksu koodi kohta ning **käibemaksu deklaratsiooni maksu koodi** lehekülg, määrata järgmised väljad.

| Väli                    | Kirjeldus                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------|
| Käibemaksukood           | Saate valida käibemaksukoodi, mida kasutatakse müügi- ja ostuarvetelt.                        |
| Käibemaksudeklaratsiooni maksukood | Sisestage kood, mis ilmub deklaratsiooni.                                           |
| Erikood             | Kommentaar sisestage, mis ilmuvad müüki ja osta deklaratsiooni lisad. |

## <a name="configure-the-electronic-reporting-model-and-format-for-the-report"></a>Konfigureerida e mudel ja aruande vormi kohta
Läbivaatamiseks või muutmiseks käibemaksu aruanne konfigureerimise kohta nende **aruandluse koosseisud** avamiseks valige **käibemaksu deklaratsiooni mudel**. Seda mudelit kasutatakse Austria, Tšehhi Vabariigi, Eesti, Soome, Läti ja Leedu ning kokku maksuandmete, mis on vajalik käibemaksu deklaratsiooni. Klõpsake **disainer** üle vaadata või muuta mudeli. Läbivaatamiseks või muutmiseks käibemaksu aruande vormi kohta on **aruandluse koosseisude** avamiseks valige **käibemaksu deklaratsiooni mudel**, ja seejärel klõpsake **disainer**.

## <a name="generate-a-vat-statement"></a>KM aruande loomine
Käibemaksuaruande perioodi, Settle ja post käibemaksu lõpus arvutab protsessi avaldus summade määratlemisel Käibemaksuaruandluse koodid, mille lõite.

-   Kui ettevõte kasutama km-registri kuupäeva asemel selle kuupäeva, on **kuupäev käibemaksukohustuslaste registrisse** sisse-välja ning **pearaamatu parameetrite** lehel tuleb valida.
-   **Eesti aruande paigutus** tuleb valida vastavalt konfigureeritud tasakaalustusperioodi maksuhalduri aruande paigutust.
-   Kui on **tingimuslik käibemaks** ruudu kohta on **pearaamatu parameetrite** lehekülg, Eesti käibemaksu deklaratsiooni toetada kassapõhist raamatupidamisarvestust ja müügi ja ostu lisades tuleb täita.

Luua käibemaksu XML-faili, et **käibemaksu maksete** lehekülg, valige üks või mitu kanded ja seejärel klõpsake **käibemaksu eksportida XML-faili**. **Märkused.**

-   Valige mitu käibemaksu tasumise rida nõutud tähtajaks.
-   Kui valitud ridade esines rohkem kui ühe perioodi, kuvatakse tõrketeade.

Seadke järgmised väljad.

| Väli                                          | Kirjeldus                                                                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Vormingu vastendamine                                 | Määrake nimi ja eksporditud XML faili.                                                                                 |
| Nimi                                           | Saate määrata töötaja, kes loob deklaratsiooni.                                                                                   |
| Deklaratsiooni perioodi tüüp                        | Valige järgmise deklaratsiooni tüüp: **normaalne** või **pankroti**.                                                        |
| Arve lävi                              | Määrake minimaalne kogu netosumma arvete kliendi või hankija puhul on aruandlusperioodi jooksul mis sisaldama lisades. |
| Deklaratsiooni (ja selle **eksportida** väli)    | Seadke selle suvandi väärtuseks **Jah** eksportimise deklaratsiooni keha.                                                                          |
| Müügi lisa (ja selle **eksportida** väli)    | Seadke selle suvandi väärtuseks **Jah** eksportida ja lisas müük.                                                  |
| Ostu lisa (ja selle **eksportida** väli) | Seadke selle suvandi väärtuseks **Jah** eksportida ja lisas ostu.                                               |

**Märkus:** väärtusi ning **perioodi** väli luuakse automaatselt, vastavalt võimaluste kohta ning **Käibemaksu tasakaalustusperioodid** lehel. Seadistatud käibemaksu tasakaalustusperioode, minge selle **Käibemaksu tasakaalustusperioodid** lehel.


