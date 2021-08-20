---
title: KM-aruande üksikasjad Eesti puhul
description: See teema selgitab, kuidas seadistada käibemaksuaruannet Eestis asuvate juriidiliste isikute puhul.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod, TaxReportCollection, TaxReportVoucher
audience: Application User
ms.reviewer: kfend
ms.custom: 266904
ms.search.region: Estonia
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 442309db43d6f154cccf48e49c3026ab57856f85e2c850613811c01364840e39
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779356"
---
# <a name="vat-statement-details-for-estonia"></a>KM-aruande üksikasjad Eesti puhul

[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas seadistada käibemaksuaruannet Eestis asuvate juriidiliste isikute puhul.

See teema sisaldab riigi-/piirkonnakohast teavet käibemaksu (KM) aruande seadistamise kohta ainult Eestis asuvate juriidiliste isikute puhul. Lisateavet käibemaksuaruannete seadistamise kohta vt teemast [Käibemaksuaruandlus Euroopas](emea-vat-reporting.md).

## <a name="set-up-sales-tax-authorities"></a>Käibemaksuhaldurite seadistamine
Käibemaksuaruande loomist asjakohase maksuasutuse jaoks sobivas vormingus peate seadistama käibemaksuasutuste jaoks aruande paigutuse. Tehke lehel **Käibemaksuasutused** väljal **Aruande paigutus** valik **Eesti aruande paigutus**. Valige käibemaksu tasakaalustamisperioodi kohta sama käibemaksuasutus, mida kasutatakse käibemaksukoodide puhul.

## <a name="set-up-sales-tax-reporting-codes"></a>Saate häälestada käibemaksuaruandluse koode.
Järgmises näites selgitatakse käibemaksuaruande koodide kasutamist käibemaksuaruannete loomiseks.

| Käibemaksu aruandluskood | Kirjeldus                                                                                                                                                                                                                                   | Käibemaksutagastuse rida (KMD) |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| 1                        | Lepped ja kanded, millele kehtib 20-protsendine maksumäär                                                                                                                                                                         | 1                            |
| 11                       | 20 protsendiga maksustavate kaupade või teenuste isevarustamine                                                                                                                                                                               | 1,1                          |
| 2                        | Lepped ja kanded, millele kehtib 9-protsendine maksumäär                                                                                                                                                                          | 2                            |
| 21                       | 9 protsendiga maksustavate kaupade või teenuste isevarustamine                                                                                                                                                                                | 2,1                          |
| 3                        | Lepped ja kanded, millele kehtib 0-protsendine maksumäär. k.a                                                                                                                                                               | 3                            |
| 31                       | Kaupade ja teenuste täielik sisetarne teise liikmesriigi maksukohuslasele / piiratud vastutusega maksukohustuslasele, k.a                                                                         | 3.1                          |
| 311                      | Kaupade sisetarne                                                                                                                                                                                                               | 3.1.1                        |
| 32                       | Kaupade eksport, k.a                                                                                                                                                                                                                    | 3.2                          |
| 321                      | Müük reisijatele, mis hõlmab käibemaksu tagastamist                                                                                                                                                                                            | 3.2.1                        |
| 5                        | Sisendkäibemaksu kogusumma, millele kohaldub mahaarvamine vastavalt seadusele, k.a                                                                                                                                                            | 5                            |
| 51                       | Importimisel tasutud või tasutav käibemaks                                                                                                                                                                                                         | 5.1                          |
| 52                       | Põhivara soetamisel tasutud või tasutav käibemaks                                                                                                                                                                                | 5.2                          |
| 6                        | Kaupade ja teenuste täielik sisesoetus teise liikmesriigi maksukohuslaselt, k.a                                                                                                           | 6                            |
| 61                       | Kaupade sisesoetus                                                                                                                                                                                                         | 6.1                          |
| 7                        | Muude kaupade ja teenuste soetus, millele kohaldub käibemaks, k.a                                                                                                                                                                    | 7                            |
| 71                       | Kinnisvara ja metallijäätmete soetus, mis on käibemaksuga maksustatavad kinnisvara, metallijäätmete ja väärismetallide erikorra alusel (Käibemaksuseaduse §41).                                                                    | 7.1                          |
| 8                        | Maksuvabastusega tarne                                                                                                                                                                                                                | 8                            |
| 9                        | Kaupade tarne, mis on käibemaksuga maksustatavad kinnisvara, metallijäätmete ja väärismetallide erikorralduste alusel (Käibemaksuseaduse §41 1). | 9                            |
| 1010                     | Korrigeerimised (+)                                                                                                                                                                                                                               | 10                           |
| 1011                     | Korrigeerimised (–)                                                                                                                                                                                                                               | 11                           |

## <a name="set-up-vat-declaration-tax-codes"></a>Käibemaksudeklaratsiooni maksukoodide seadistamine
Käibemaksudeklaratsiooni maksukoode kasutatakse käibemaksukoodide vastendamiseks deklaratsioonis nõutavate väärtustega (20, 9, 20erikord või 9erikord). Peale selle saate iga maksukoodi puhul määrata valikulised müügi- ja ostu seletuskoodid (01, 02 või 03 müügi puhul, 11 või 12 ostu puhul). Käibemaksudeklaratsiooni maksukoodide seadistamiseks määrake lehel **Käibemaksudeklaratsiooni maksukood** järgmised väljad.

| Väli                    | Kirjeldus                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------|
| Käibemaksukood           | Märkige käibemaksukood, mida kasutatakse müügi- või ostuarvete puhul.                        |
| Käibemaksudeklaratsiooni maksukood | Sisestage deklaratsioonil kuvatav kood.                                           |
| Erikood             | Sisestage seletuskood, mis kuvatakse deklaratsiooni müügi- ja ostulisades. |

## <a name="configure-the-electronic-reporting-model-and-format-for-the-report"></a>Elektroonilise aruandlusmudeli ja aruande vormingu konfigureerimine
Käibemaksuaruande konfiguratsiooni vaatamiseks või muutmiseks tehke lehel **Aruandluse konfiguratsioonid** valik **Käibemaksudeklaratsiooni mudel**. Sama mudelit kasutatakse Austria, Tšehhi Vabariigi, Eesti, Soome, Läti ja Leedu puhul ning koondmaksuandmete puhul, mis on käibemaksudeklaratsiooni jaoks nõutavad. Mudeli ülevaatamiseks või muutmiseks klõpsake valikut **Kujundaja**. Käibemaksuaruande vormingu vaatamiseks või muutmiseks tehke lehel **Aruandluse konfiguratsioonid** valik **Käibemaksudeklaratsiooni mudel** ja seejärel klõpsake valikut **Kujundaja**.

## <a name="generate-a-vat-statement"></a>Käibemaksuaruande loomine
Käibemaksu aruandlusperioodi lõpus arvutab käibemaksu tasakaalustamise ja sisestamise protsess aruande reasummad teie loodud käibemaksu aruandluskoodide määratlemiseks.

-   Kui ettevõte peab kasutama käibemaksukande kuupäeva asemel käibemaksuregistri kuupäeva, peab väli **Käibemaksuregistri kuupäev** lehel **Pearaamatu parameetrid** olema valitud.
-   Tasakaalustamisperioodi jaoks konfigureeritud käibemaksuasutuse aruande paigutusena peab olema valitud **Eesti aruandepaigutus**.
-   Kui lehel **Pearaamatu parameetrid** on valitud väli **Tingimuslik käibemaks**, toetab Eesti käibemaksudeklaratsioon sularahaarvestuse skeemi ning müügi- ja ostulisad peavad olema täidetud.

Käibemaksu XML-faili loomiseks valige lehel **Käibemaksu maksed** üks või mitu kannet ja klõpsake valikut **Ekspordi käibemaksu XML-fail**. **Märkused.**

-   Saate iga nõutud perioodi kohta valida rohkem kui ühe käibemaksu makserea.
-   Kui valitud read esinevad rohkem kui ühes tasakaalustamisperioodis, saate tõrketeate.

Seejärel määrake järgmised väljad.

| Väli                                          | Kirjeldus                                                                                                                         |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Vormingu vastendamine                                 | Määrake eksporditud XML-faili nimi ja tee.                                                                                 |
| Nimi                                           | Määrake töötaja, kes loob deklaratsiooni.                                                                                   |
| Deklaratsiooni perioodi tüüp                        | Valige üks järgmistest deklaratsioonitüüpidest: **Tavaline** või **Pankrot**.                                                        |
| Arve lävi                              | Määrake lisadesse kaasatav arvete minimaalne kogu netosumma kliendi või hankija kohta aruandlusperioodil. |
| Deklaratsioon (väljagrupis **Eksport**)    | Deklaratsiooni kehateksti eksportimiseks määrake selle valiku sätteks **Jah**.                                                                          |
| Müügilisa (väljagrupis **Eksport**)    | Arvete ja kreeditarvete eksportimiseks müügilisasse määrake selle valiku sätteks **Jah**.                                                  |
| Ostulisa (väljagrupis **Eksport**) | Arvete ja kreeditarvete eksportimiseks ostulisasse määrake selle valiku sätteks **Jah**.                                               |

**Märkus.** Väljade väärtused väljagrupis **Periood** sisestatakse automaatselt lehel **Käibemaksu tasakaalustusperioodid** tehtud valikute põhjal. Käibemaksu tasakaalustusperioodid saate seadistada lehel **Käibemaksu tasakaalustamisperioodid**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]