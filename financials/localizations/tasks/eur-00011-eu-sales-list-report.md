--- 
title: "EL-i käibearuande koostamine"
description: "See protseduur juhatab teid läbi EL-i käibearuande koostamise protseduuri."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 10e7399b058695fb1c1b0db8c696c926619c995a
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="generate-an-eu-sales-list-report"></a>EL-i käibearuande koostamine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur juhatab teid läbi EL-i käibearuande koostamise protseduuri. See hõlmab ühendusesisese kaubanduse kannete edastamist ELi käibearuandesse ja aruande käivitamist. See protseduur hõlmab ka ühendusesisese kaubanduse kande loomist demonstreerimiseks. Lisateavet EL-i müügiloendi aruandluse, sh nõutavate eeltingimuste kohta leiate rakenduse Dynamics 365 for Finance and Operations spikrist.

See protseduur kohaldub kõigile Euroopa riikidele/piirkondadele. Protseduuri loomisel kasutatakse demoettevõtte DEMF andmeid, seega on kodumaise riigi/piirkonna näiteks Saksamaa. Protseduur kasutab EL-i riigi/piirkonna näitena ka Portugali. Enne selle protseduuri läbimist tuleb konfigureerida EL-i käibearuandlus.

See protseduur on mõeldud raamatupidajatele.


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a>Ühendusesisese müügikande loomine demonstreerimiseks
1. Avage Müügireskontro > Tellimused > Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Sisestage väljale Kliendi konto tekst „PRT-001”.
4. Klõpsake nuppu OK.
5. Sisestage väljale Kaubakood tüüp D0001.
6. Laiendage jaotis Rea üksikasjad.
7. Klõpsake vahekaarti Seadistus.
8. Sisestage FULL väljale Kauba käibemaksugrupp.
9. Klõpsake käsku Lisa rida.
10. Sisestage väljale Kaubakood tüüp D0003.
11. Sisestage RED väljale Kauba käibemaksugrupp.
12. Klõpsake nuppu Salvesta.
13. Klõpsake toimingupaanil valikut Arve.
14. Klõpsake valikut Arve.
15. Laiendage jaotis Parameetrid.
16. Valige väljal Kogus väärtus Kõik.
17. Laiendage jaotist Seadistus.
18. Määrake väljal Arve kuupäev kuupäevaks 01/11/2016.
19. Klõpsake nuppu OK.
20. Klõpsake nuppu OK.

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a>Ühendusesisese kaubanduse kannete edastamine ELi käibearuandesse
1. Avage Maks > Deklaratsioonid > Väliskaubandus > EL-i käibearuanne.
2. Klõpsake käsku Ülekanne.
3. Kauba kannete edastamiseks valige Jah väljal Kaup.
4. Teenuse kannete edastamiseks valige Jah väljal Teenus.
    * Saate määrata lisafiltreid ka edastatavatele ühendusesisese kaubanduse kannetele.  
5. Klõpsake käsku Ülekanne.
    * Kontrollige, et ühendusesisene müügitehing on edukalt EL-i käibearuandesse edastatud.  

## <a name="generate-the-eu-sales-list-report"></a>EL-i käibearuande loomine
1. Klõpsake vahekaarti Aruandlus.
2. Valige Igakuine väljal Aruandlusperiood.
3. Määrake väljal Alguskuupäev kuupäevaks 01/01/2016.
4. Valige Jah väljal Loo fail.
5. Valige Jah väljal Loo aruanne.
6. Tippige väljale Faili nimi väärtus EUSalesList.
7. Tippige väljale Aruandefaili nimi väärtus EUSalesList.
8. Tippige väljale EL-i käibearuande registreerimise ID väärtus 123.
    * See väli on saadaval ainult Saksamaa puhul.  
    * Saate määrata lisafiltreid ka aruandesse lisatavatele ühendusesisese kaubanduse kannetele.  
9. Klõpsake nuppu OK.
    * Kontrollige, et kuvatakse hüpikaknad, mis kinnitavad faili ja kontrollaruande allalaadimist.  

## <a name="mark-eu-sales-list-lines-as-reported"></a>ELi käibearuande ridade esitatuks märkimine
1. Klõpsake käsku Märgi.
2. Klõpsake käsku Märgi esitatuks.
3. Valige loendist välja Arve kuupäev rida.
4. Tippige väljale Kriteerium väärtus 01/01/2016..01/31/2016.
5. Valige loendist rida väljale Aruandluse olek.
6. Valige väljal Kriteeriumid väärtus Kaasatud.
    * Saate määrata lisafiltreid ka edastatuks märgitavatele ühendusesisese kaubanduse kannetele.  
7. Klõpsake nuppu OK.
8. Valige väljal Valik väärtus Esitatud.

## <a name="mark-eu-sales-list-lines-as-closed"></a>ELi käibearuande ridade suletuks märkimine
1. Klõpsake käsku Märgi.
2. Klõpsake käsku Märgi suletuks.
3. Märkige loendis välja Arve kuupäev rida.
4. Tippige väljale Kriteerium väärtus 01/01/2016..01/31/2016.
5. Märkige loendis välja Aruandluse olek rida.
6. Valige väljal Kriteeriumid väärtus Esitatud.
    * Saate määrata lisafiltreid ka suletuks märgitavatele ühendusesisese kaubanduse kannetele.  
7. Klõpsake nuppu OK.
8. Valige väljal Valik väärtus Suletud.

