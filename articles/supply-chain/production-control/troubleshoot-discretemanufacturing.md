---
title: Diskreetse tootmise tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada diskreetse tootmisega töötamisel tekkivaid probleeme.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b0073cb2c3e3d6b9218caf20c394c8c0ca67b796
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966201"
---
# <a name="troubleshoot-discrete-manufacturing"></a>Diskreetse tootmise tõrkeotsing

Selles teemas kirjeldatakse, kuidas lahendada diskreetse tootmisega töötamisel tekkivaid probleeme.

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a>Kuvatakse järgmine tõrketeade: "Laohalduse protsesse kasutatakse praegu. Kui tööread ei ole veel registreeritud, saate loodud töö ja koorma või saadetise read tühistada ning jätkata komplekteerimise või saatmise protsessiga.

### <a name="issue-description"></a>Probleemi kirjeldus

See probleem ilmneb juhul, kui proovite reserveerida või vabastada tööd rea jaoks, kuid laokande olek on *Komplekteeritud*, mis näitab, et materjal on komplekteeritud.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selle probleemi lahendamiseks järgige üht järgmistest sammudest.

- Muutke tootmistellimuse olek tagasi väärtusele *Hinnanguline* või *Väljastatud*.
- Avage leht vastava tootmistellimuse üksikasjade kohta. Valige tegumiribal vahekaardil **Ladu** grupis **Peatamine** valik **Peata ja Tühista**, et tühistada kõik komplekteeritud kanded. Seejärel valige tootmistellimuse töötlemiseks **Eemalda peatus**.

Siin on *Komplekteerimise tühistamise* ja *Peatamise* funktsioonide kirjeldus:

- **Komplekteerimise tühistamine** – See funktsioon tühistab laokannete oleku koosluse ridade ja valemi ridade jaoks, mille olek on *Komplekteeritud* *tellimuse alusel*. Kui tooraine komplekteerimise töö on lõpetatud, seatakse ridade olekuks *Komplekteeritud*. See olek takistab tootmistellimuse lähtestamist *Loodud* olekusse. Sel juhul saate kasutada funktsiooni *Tühista komplekteerimine*, et ennistada kanded *Komplekteeritud* olekust ja seejärel lähtestada tootmistellimus olekusse *Loodud*.
- **Peata** – See funktsioon määrab tootmistellimusele **Peatatud** lipu, et vältida tellimuse oleku uuendamist. **Peatatud** lipu leiate **Lao** FastTab-is tootmistellimuse üksikasjade lehelt.

> [!NOTE]
>
> - Nupud on nähtavad ainult siis, kui tootmistellimused on loodud kaubale, mis on lao protsesside jaoks lubatud.
> - **Peata** grupp on nähtav ainult tootmistellimuse üksikasjade lehe tegumiriba **Lao** vahekaardil. See ei ole kuvatud **Lao** FastTab-is **Tootmistellimuste** loendi lehel.

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a>Vastava ressursi nime ei värskendata pärast töötaja nime muutmist globaalses aadressiraamatus.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui muudate töötaja nime globaalses aadressiraamatus, ei uuendata vastava ressursi nime ressursigrupi koondandmetes.

### <a name="issue-resolution"></a>Probleemi lahendamine

Seda stsenaariumit praegu ei toetata. Probleemi lahendamiseks peate ressursi nime käsitsi värskendama.

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a>Uue tootmistellimuse loomisel ei saa ma järgmist teadet: "Sisestage koosluse ja protsessi aktiivne versioon?"

### <a name="issue-description"></a>Probleemi kirjeldus

Kui loote uue tootmistellimuse, seadistatakse pärast kaubakoodi sisestamist **Saidi** ja **Lao** väljad automaatselt vaikimisi saidi ja lao jaoks, mis on määratud lõpetatud tooteüksusele **Vaikimisi tellimuse sätete** lehel. Lisaks sisestatakse aktiivse koosluse number ja protsessi number automaatselt. Te ei saa järgmist teadet, mis küsib teilt neid väärtusi:

> Kas sisestada koosluse ja protsessi jaoks aktiivne versioon?

### <a name="issue-resolution"></a>Probleemi lahendamine

Teil ei paluta sisestada koosluse ja protsessi numbreid, kui valite toote, mille sait ja ladu on **Vaikimisi tellimuse sätete** lehel määratud. Teilt küsitakse ainult juhul, kui need väärtused pole valitud toote puhul määratletud.

## <a name="production-orders-arent-shown-on-the-marking-page"></a>Tootmistellimusi ei kuvata märgistuse lehel.

### <a name="issue-description"></a>Probleemi kirjeldus

Mõningaid tootmistellimusi ei kuvata **Märgistamine** lehel.

### <a name="issue-resolution"></a>Probleemi lahendamine

Tooted, millel on järgmine konfiguratsioon, pole märkimiseks saadaval. Seetõttu ei kuvata neid **Märgistamine** lehel:

- Tooted on määratletud kui *tegeliku kaalu* tüübi tooted.
- Need on lubatud täpsemate lao protsesside jaoks.
- Need on konfigureeritud, et neid kontrollitaks *Standardkulu* põhimõttega.

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a>Kui üritan tootmistellimuse lõpetada, kuvatakse järgmine tõrketeade: "Koosluse consumptionCost arvutamine peab laost väljamineku puhul olema negatiivne."

See probleem parandati versioonis 10.0.15.

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a>Kui tootmistellimuse olek muudetakse täielikult lõpetatuks, kuvatakse järgmine tõrketeade: "Värskenda konflikti. Standardne kulu ei ühti finantsilise laovaru väärtusega pärast uuendamist ja InventCostMovement.checkVariance funktsioonis on ilmunud kriitiline tõrge.

See probleem ilmneb, sest aluseks olevaid andmeid muudeti teise protsessiga. Protsess proovib värskendada andmeid kuni viis korda. Kui konflikt on pärast viit katset endiselt olemas, kuvatakse järgmine tõrketeade:

> Värskenduse konflikt. Standardkulu ei kattu pärast uuendamist finantsilise laovaru väärtusega.

> Funktsioonis InventCostMovement.checkVariance ilmnes kriitiline tõrge.

Selline käitumine on nii kavandatud. Probleemi leevendamiseks naaske partii juurde. See peaks lõpetama töötamise.

Kui partii töö järjepidevalt nurjub pärast selle jätkamist, veenduge, et pearaamatu vaikevaluuta ümardamise täpsus oleks vastavuses InventSum tabeli väärtustele rakendatud ümardamisega. Kui ümardamise täpsust on muudetud mittevastavaks väärtuseks, peate selle ilmselt muutma tagasi vastavale väärtusele. Otsige **ModifiedDateTime**. Sellisel juhul näitab väärtus tavaliselt, et ümardamise täpsust on viimati muudetud.

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a>Lattu väljastamisel kuvatakse järgmine tõrketeade: "Üksust RM ei saanud täielikult reserveerida. Veenduge, et täielik kogus on saadaval, või reserveerige kaubad käsitsi, kui koosluse rea välja reserveerimine on seatud väärtusele Käsitsi või Alustatud. Tellimust ei saanud lattu väljastada, kuna mõningaid materjale ei õnnestunud reserveerida." Olek on aga värskendatud väärtusele Väljastatud.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui kõik koosluse rea kaubad on tootmistellimuse vabastamisel füüsiliselt saadaval ja **Lattu väljastamise** poliitika on seatud tootmistellimusele *Nõua täielikku reserveerimist*, kuvatakse järgmine tõrketeade:

> Kauba RM-i ei saanud täielikult reserveerida. Veenduge, et täielik kogus on saadaval, või reserveerige kaubad käsitsi, kui koosluse rea välja reserveerimine on seatud väärtusele Käsitsi või Alustatud. Tellimust ei saanud lattu väljastada, kuna mõningaid materjale ei õnnestunud reserveerida.

### <a name="issue-resolution"></a>Probleemi lahendamine

Selline käitumine on disainitud ja töötab ootuspäraselt.

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a>Kui ma proovin tootmistellimuse lõpetada ja lõpetatuna kinnitada, kuvatakse järgmine tõrketeade: "Tootmise lõpetamiseks teatatud hea kogus kokku on %1. Tagasiside viimasele operatsioonile on kokku 0,00."

### <a name="issue-description"></a>Probleemi kirjeldus

Kui proovite sisestada tootmistellimuse lõpetatuna kinnitamise töölehte, kuvatakse järgmine tõrketeade:

> Õige lõpetatuna kinnitatud tootmise kogus tootmisele kokku on %1. Tagasiside viimasele operatsioonile on kokku 0,00.

### <a name="possible-cause"></a>Võimalik põhjus

See probleem ilmneb juhul, kui viimases toimingus sisestatud kogused olid valed. Näiteks kui tootmist alustatakse, kuid kogust, mis tuleb käivitada, ei eraldata, sisestatakse protsessikaardi tööleht ridadeta. Olukorra kinnitamiseks avage tootmistellimus ja seejärel valige toiminguribal **Kuvamine** vahekaardil suvand **Marsruudi kaart**.

### <a name="workaround"></a>Vastukaal

Selle probleemi saate lahendada, kui sisestate täiendavad töölehed operatsioonide jaoks, mille jaoks töölehed pole õigesti sisestatud. Käivitage tootmistellimus uuesti ja valige täiendavate töölehtede sisestamine. See tegevus ei käivita tootmistellimust, kuid see sisestab töölehed. Protsessi kaart peaks seejärel näitama sisestatud koguseid ja teil peaks olema võimalik tootmistellimused edukalt lõpetada.

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a>Kas ma saan esitada tootmistellimuse lõpetatuna, kui ma teatan tõrke kogusest, kuid mitte siis, kui ma teatan aja-või materjalikulu kogusest?

Te ei saa tootmistellimuse tõrke kogusest teatada, kui te just ei teata heast kogusest. Seda stsenaariumi **ei** toetata. Lõpetatuna kinnitamise aruanne nurjub, kui püüate tootmistellimuse lõpetada ja kuvatakse järgmine tõrketeade:

> Puuduv lõpetatuna kinnitatud kogus.

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a>Kas ma saan jälgida lõpetatud kaupade seerianumbrit tarbitud kaupade seerianumbrite suhtes?

Lõpetatud kaupade seerianumbrit ei saa jälgida materjali seerianumbrite suhtes, mida tootmistellimus tarbib nende lõpetatud kaupade valmistamiseks. Seda stsenaariumit praegu ei toetata. Vastukaaluks on tootmistellimuste loomine kogusele 1.
