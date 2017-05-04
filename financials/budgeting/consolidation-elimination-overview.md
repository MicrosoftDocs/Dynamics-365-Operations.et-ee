---
title: "Konsolideerimise ja eemaldamise ülevaade"
description: "Selles artiklis anatkse üldist teavet konsolideerimis- ja eemaldamisprotsessi kohta. See sisaldab vastuseid korduma kippuvatele küsimustele."
author: RobinARH
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13151
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 3868605826e3c6f0714736ffa8630d1569e17d6f
ms.lasthandoff: 03/31/2017


---

# <a name="consolidation-and-elimination-overview"></a>Konsolideerimise ja eemaldamise ülevaade

Selles artiklis anatkse üldist teavet konsolideerimis- ja eemaldamisprotsessi kohta. See sisaldab vastuseid korduma kippuvatele küsimustele.

Andmete konsolideerimisel kombineeritakse mitme tütarettevõtte finantstulemused ühe konsolideeritud ettevõtte tulemusteks. Tütarettevõtted võivad olla eri versioonides või süsteemides, need ei pruugi olla ainuomanduses ja need võivad kasutada eri valuutasid. Andmete konsolideerimiseks on mitu võimalust.

-   **Konsolideeri võrgus** – see suvand konsolideerib päevasaldod valitud kontode ja dimensioonidega ja salvestab need konsolideeritud ettevõttesse.
-   **Finantsaruandlus** – see suvand võimaldab kannete ja saldode konsolideerimise ja selle saab luua igal ajal. Luua saab mitu taset hierarhiaid ja vaadata mitut aruandluse valuutat.
-   **Konsolideeri impordiga** – see suvand impordib saldod konsolideeritud ettevõttesse.
-   **Ekspordi ettevõtte saldod** – see suvand annab ettevõtte saldode ekspordifaili. Seejärel saate faili importida teistesse eksemplaridesse või süsteemidesse. Finantsaruandlust saab kasutada ka saldode eksportimiseks Microsoft Exceli faili.

Eemaldamisi saab esitada mitmel moel.

-   Eemaldamisreeglid saate seadistada süsteemis ja seejärel töödelda konsolideerimisprotsessi käigus või eemaldamissoovituse kaudu. Reegleid saab sisestada mis tahes ettevõttele, mille puhul on juriidilise isiku seadistuses valitud suvand **Kasuta finantsiliseks eemaldamisprotsessiks**.
-   Eraldi ettevõtte saab luua ja seda kasutada eemaldamiskannete käsitsi määramiseks ja sisestamiseks. Seda ettevõtet saab kasutada konsolideerimisprotsessis või finantsaruandluses.
-   Kontsernisisese tegevuse määratlemiseks kasutatavaid kontosid ja finantsdimensioone saab filtrida finantsaruandluses readefinitsiooni või veeru definitsiooni põhjal ja kasutada saab kõiki süvitsimineku võimalusi. Arvutatud veergu või rida saab seejärel kasutada kontode ja finantsdimensioonide eemaldamiseks konsolideeritud kogusummast.

Konsolideerimisstsenaariume on mitu ja iga meetod saab käsitleda stsenaariume erinevalt.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused
1.  Eelistan eemaldamiste sisestamist andmebaasi. Millised võimalused mul selleks on?

Teil on mitu võimalust. Saate kasutada suvandit **Konsolideeri võrgus** ja kaasata eemaldamised protsessi käigus või soovitusena. Kanded sisestatakse konsolideeritud ettevõttes. Teise võimalusena võib teil olla eraldi ettevõte, millesse loote eemaldamisi käsitsi ja kasutate seejärel seda ettevõtet finantsaruandluses või konsolideerimisprotsessis.

2.  Vajame konsolideeritud tulemusi mitmes aruandluse valuutas.

Suvandil **Finantsaruandlus** on piiramatult aruandlusvaluutasid. Andmed teisendatakse aruande loomisel põhikontol seadistatud vahetuskursi tüübi ja valuuta teisendusmeetodi põhjal. Kuna suvandil **Konsolideeri võrgus** on ainult üks aruandlusvaluuta, on selle suvandi kasutamisel konsolideeritud ettevõte vajalik iga aruandlusvaluuta puhul. Soovitatavaks meetodiks on suvand **Finantsaruandlus**.

3.  Soovin näha kande taseme üksikasju iga ettevõtte puhul.

Lahenduseks on suvand **Finantsaruandlus**, kuna kande taseme üksikasju saab vaadata nii mitme ettevõtte puhul kui neid on aruandluspuu definitsiooni kaasatud.

4.  Kasutame eelarve plaanimist või eelarve juhtimist ja see tuleb konsolideerida.
Mis tahes eelarve plaanimise või eelarve juhtimise andmete konsolideerimise lahenduseks on suvand **Finantsaruandlus**.

5.  Meie tütarettevõtted asuvad kogu maailmas ja neil on mitu kontoplaani. Mis on parim viis meie andmete konsolideerimiseks?

Mitme kontoplaani käsitsemiseks on teil mitu võimalust. Saate kasutada suvandit **Konsolideeri võrgus** ja valida seejärel põhikontol määratletud konsolideerimiskonto või konsolideerimiskontode grupi kasutamise. Saate kasutada ka suvandit **Finantsaruandlus**, lisada readefinitsioonis mitu linki finantsdimensioonidele ja kontod vastendada.

6.  Nõuame konsolideerimist mitmel tasemel. Teisisõnu konsolideerime esmalt meie Euroopa tütarettevõtted Briti naeltesse (GBP). Seejärel võtame need andmed ja teisendame konsolideeritud summa USA dollaritesse. Kuidas me seda teha saame?

Konsolideerimise mitme taseme nõudmisel ja igal tasemel eri valuutade kasutamisel peate kasutama suvandit **Konsolideeri võrgus**. Luua tuleb mitu konsolideerimisettevõtet, mis erinevad arvestus- ja aruandlusvaluutade poolest. Konsolideerimist tuleb seejärel käivitada mitu korda. Suvand **Finantsaruandlus** teisendab alati iga lähteettevõtte arvestusvaluutast valitud valuutasse.

7.  Meil on tütarettevõtteid eri süsteemis. Kuidas saame neid konsolideerida?

Kasutage suvandit **Konsolideeri impordiga** saldode viimiseks konsolideeritud ettevõttesse.

8.  Mõned meie tütarettevõtted pole ainuomanduses. Mis on parim viis nende konsolideerimiseks?

Teil on osaomanduses tütarettevõtete puhul mitu võimalust. Kasutades suvandit **Finantsaruandlus** saate määratleda aruandluspuu definitsiooni ja omandiõiguse. Samuti saate kasutada osaomanduses summa tähistamiseks arvutatud rida või veergu. Saate kuvada ka vähemusosaluse aruande eraldi reana. Samuti saate kasutada suvandit **Konsolideeri võrgus**. Vahekaardil **Juriidilised isikud** on veerg **Omandiõigus**, milles saate määrata emaettevõtte osalusprotsendi.

9.  Meie organisatsioon peab näitama konsolideerimisi äriüksuse järgi või soovib kasutada organisatsiooni hierarhiaid.

Lahenduseks on suvand **Finantsaruandlus**. Organisatsiooni hierarhiad, milles on juriidilisi isikuid või finantsdimensioone, saab esitada finantsaruandluses. Saate luua ka oma mitmetasandilised hierarhiad, kasutades aruandluspuu definitsiooni, milles on juriidiliste isikute ja dimensiooniväärtuste kombinatsioon.

10. Meil on rohkem kui üks süsteemi eksemplar.

Kasutades ühest eksemplarist eksportimiseks suvandit **Ekspordi ettevõtte saldod** ja kasutades seejärel teisel eksemplaril suvandit **Konsolideeri impordiga**, saate andmed konsolideerida.


Lisateavet vt teemast [Valuuta ümberarvutamine konsolideeritavas ettevõttes](\finanicials\general-ledger\currency-revaluation-consolidation-company).

