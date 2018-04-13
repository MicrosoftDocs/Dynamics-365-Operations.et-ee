--- 
title: "EL-i käibearuandluse seadistamine"
description: "See ülesandejuhend selgitab EL-i käibearuande jaoks nõutavate eeltingimuste ülevaadet."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5c415b06debc882c9ecdacc1c89e64325df4d4c7
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-eu-sales-list-reporting"></a>EL-i käibearuandluse seadistamine

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

See ülesandejuhend selgitab EL-i käibearuande jaoks nõutavate eeltingimuste ülevaadet. Lisateavet EL-i müügiloendi aruandluse, sh nõutavate eeltingimuste kohta leiate rakenduse Dynamics 365 for Finance and Operations spikrist.

See ülesanne kohaldub kõigile Euroopa riikidele/piirkondadele. Juhendi loomisel kasutatakse demoettevõtte DEMF andmeid, seega on kodumaise riigi/piirkonna näiteks Saksamaa. Juhend kasutab EL-i riigi/piirkonna näitena ka Portugali.

Need ülesanded on mõeldud süsteemi administraatoritele.


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a>Elektroonilise aruandluse konfiguratsioonide importimine EL-i käibearuandluse jaoks
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Klõpsake valikut Määra aktiivseks.
3. Klõpsake valikut Hoidlad.
4. Klõpsake valikut Ava.
5. Klõpsake toimingupaanil valikut Suvandid.
6. Klõpsake suvandit Täpsem filter/sortimine.
7. Klõpsake vahekaarti Lisa.
8. Valige väljal Väli suvand Konfiguratsiooni nimi.
9. Sisestage väljale Kriteeriumid tekst „EL-i käibearuanne (DE)”.
10. Klõpsake nuppu OK.
11. Klõpsake Import.
12. Klõpsake nuppu Jah.
13. Klõpsake toimingupaanil valikut Suvandid.
14. Klõpsake suvandit Täpsem filter/sortimine.
15. Klõpsake nuppu Lähtesta.
16. Klõpsake vahekaarti Lisa.
17. Valige väljal Väli suvand Konfiguratsiooni nimi.
18. Sisestage väljale Kriteeriumid tekst „EL-i käibearuanne ridade kaupa”.
19. Klõpsake nuppu OK.
20. Klõpsake Import.
21. Klõpsake nuppu Jah.

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a>Käibemaksukoodide seadistamine EL-i käibearuandluse jaoks
1. Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksukoodid.
2. Kasutage kiirfiltrit, et filtreerida välja Käibemaksukood väärtuse „KM19” järgi.
3. Laiendage jaotist Aruande seadistus.
    * Kontrollige, kas suvandi Välistatud valik sätteks on valitud Ei.  
    * Võib-olla peate selle sätte muutmiseks avama ülesandejuhendi.  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a>Käibemaksugruppide seadistamine EL-i käibearuandluse jaoks
1. Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksu grupid.
2. Kasutage kiirfiltrit, et filtreerida välja Käibemaksugrupp väärtuse „AR-DOM” järgi.
3. Klõpsake nuppu Redigeeri.
4. Laiendage jaotist Seadistus.
5. Valige loendist esimene rida.
6. Märkige ruut Vabastus.
7. Valige loendist teine rida.
8. Märkige ruut Vabastus.
9. Valige loendist kolmas rida.
10. Märkige ruut Vabastus.

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a>Kauba käibemaksugruppide seadistamine EL-i käibearuandluse jaoks
1. Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksukoodid.
2. Kasutage kiirfiltrit, et filtreerida välja Kauba käibemaksugrupp väärtuse „TÄIELIK” järgi.
    * Kontrollige, kas suvandi Aruandlustüübi valik sätteks on valitud Kaup.  
    * Võib-olla peate selle välja väärtuse muutmiseks avama ülesandejuhendi.  
3. Kasutage kiirfiltrit, et filtreerida välja Kauba käibemaksugrupp väärtuse „PUNANE” järgi.
    * Kontrollige, kas suvandi Aruandlustüübi valik sätteks on valitud Teenus.  
    * Võib-olla peate selle välja väärtuse muutmiseks avama ülesandejuhendi.  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a>Riigi/piirkonna parameetrite seadistamine EL-i käibearuandluse jaoks
1. Minge jaotisse Maks > Seadistus > Käibemaks > Riigi/piirkonna parameetrid.
2. Klõpsake valikut Uus.
3. Valige väljal Riik/piirkond tüüp PRT.
4. Sisestage väljale Käibemaks tekst „PT”.

## <a name="create-tax-exempt-numbers"></a>Maksuvabastuse numbrite loomine
1. Minge jaotisse Maks > Seadistus > Käibemaks > Maksuvabastuskoodid.
2. Klõpsake valikut Uus.
3. Valige väljal Riik/piirkond tüüp PRT.
4. Sisestage väljale Maksuvabastuse number tekst „PT12345”.

## <a name="set-up-eu-sales-list-reporting-parameters"></a>EL-i käibearuandluse parameetrite seadistamine
1. Minge jaotisse Maks > Seadistus > Väliskaubandus > Väliskaubanduse parameetrid.
2. Klõpsake vahekaarti EL-i käibearuanne.
3. Valige väljal Ostude ülekandmine suvand Jah.
4. Laiendage jaotist Ümardamisreeglid.
5. Määrake ümardamisreegli väärtuseks „0,1”.
6. Valige väljal Kasuta miinimumväärtust suvand Jah.
7. Sisestage väljale Kümnendkohtade arv väärtus „2”..
8. Laiendage jaotist Elektrooniline aruandlus.
9. Valige väljal Failivormingu vastendus suvand EL-i käibearuanne (DE).
10. Valige väljal Aruandevormingu vastendus suvand EL-i käibearuanne ridade kaupa.
11. Klõpsake vahekaarti Riigi/regiooni atribuudid.
    * Kontrollige, kas välja Riigi/piirkonna tüüp sätteks on valitud Kodumaine või Riigi/piirkonna DEU.  
    * Võib-olla peate selle välja väärtuse muutmiseks avama ülesandejuhendi.  
12. Klõpsake valikut Uus.
13. Valige väljal Riik/piirkond tüüp PRT.
14. Sisestage väljale Intrastati kood tekst „PT”.
15. Valige väljal Riigi/piirkonna tüüp suvand EL.
16. Klõpsake vahekaarti Numbriseeriad.
    * Kontrollige, kas viitele EL-i käibearuanne on määratud numbriseeria kood.  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a>Kliendi loomine EL-i käibearuandluse demoeesmärgil
1. Avage Müügireskontro > Kliendid > Kõik kliendid.
2. Klõpsake valikut Uus.
3. Sisestage väljale Kliendi konto tekst „PRT-001”.
4. Sisestage väljale Nimi tekst „Klient Portugalist”.
5. Valige väljal Kliendigrupp suvand 10.
6. Valige väljal Käibemaksugrupp suvand AR-DOM.
7. Valige väljal Maksuvabastuse number suvand PT12345.
8. Valige väljal Riik/piirkond tüüp PRT.
9. Klõpsake nuppu Salvesta.


