---
title: Tarnegraafiku loomine
description: Selles protseduuris näitlikustatakse, kuidas müügitellimuse jaoks tarnegraafikut luua.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d99dfae5e045262d34daf3529a6a3f4716b4afe3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "327960"
---
# <a name="create-delivery-schedule"></a>Tarnegraafiku loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris näitlikustatakse, kuidas müügitellimuse jaoks tarnegraafikut luua. Tarnegraafikut kasutatakse, kui tellimuse või pakkumise koguse puhul on nõutav mitme saadetisega tarne. Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.


## <a name="create-delivery-schedule"></a>Tarnegraafiku loomine
1. Avage Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Valige või sisestage väärtus väljal Kliendi konto.
4. Klõpsake nuppu OK.
5. Sisestage või valige väärtus väljal Kaubakood.
6. Sisestage väljale Kogus arv, mis on suurem kui 1.
7. Klõpsake valikut Müügitellimuse rida.
8. Klõpsake valikut Tarnegraafik.
    * Lehel Tarnegraafik saate määrata, mitme saadetisega tellimuse rea lõplik kogus kliendile tarnitakse.    
    * Vaikimisi kopeerib süsteem esimesele tarnegraafiku reale lõpliku koguse ja muud tarne üksikasjad algselt müügitellimuse realt. Selles näites loome kahe saadetisega graafiku, kus teise saadetise kuupäev on nädala võrra hilisem esimese omast.  
9. Sisestage väljale Kogus arv, mis moodustab osa lõplikust kogusest.
10. Klõpsake Uus.
11. Sisestage järelejäänud kogus väljale Kogus.
12. Sisestage väljale Nõutav lähetuskuupäev kuupäev, mis on nädala võrra hilisem esimesel tarnereal olevast kuupäevast.
    * Kui algsele tellimuse reale on määratud tarnegraafiku read, saate kiirkaardi Tasude teisendamine kahe suvandi abil kontrollida tarnegraafiku ridade kulude jaotust. Kui valite Kopeeri brutosummad, kopeeritakse igale reale sama tasu summa. Suvand Eralda tarneridadele jagab kulud tarneridade vahel võrdselt.  
    * Jagada saab ainult püsikulusid, kuid muutuvkulud kopeeritakse ridadele.  
13. Lehe värskendamiseks võtke kursor teiselt tarnereal ära.
    * Väljade Kokku ja Järelejäänud abil saate jälgida lõplikku kogust, mis tarnegraafiku ridadele eraldati. Kui järelejäänud kogus on null, eraldati graafikusse algse rea täielik kogus.   
14. Klõpsake nuppu OK.
    * Tarnegraafik on nüüd tellimuse ridadele kopeeritud.   
    * Algne tellimuse rida, millele on viidatud ka nimega Äriandmete rida, teisendati tellimusreaks Tellimusrida mitme tarnega. See tähistatud eristatava ikooniga ja toimib nagu tarneridade päis.  
    * Kaks uut rida, millele viidatakse ka kui tarneridadele, moodustavad ühe tarnegraafiku. Tellimust töödeldakse nende ridade, mitte algse rea alusel. Dokumentide, nagu kinnituslehed, komplekteerimislehed, saatelehed või arved, printimisel kuvatakse ainult tarneread.   
    * Tarneridadel võivad olla erinevad tarnekuupäevad, kogused, tarneviisid ja ladustamisdimensioonid, nagu koht ja ladu. Tootedimensioonid peavad siiski alati vastama äriandmete real olevatele ja neid ei saa muuta.  
15. Sisestage väljale Kogus arv, mis on suurem kui praegune.
16. Koguse ümberarvutuse mõju nägemiseks valige äriandmete rida.
17. Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.
18. Klõpsake valikut Saatelehe sisestamine.
19. Laiendage jaotis Parameetrid.
20. Valige väljal Kogus väärtus Kõik.
    * Pange tähele, et saateleht luuakse kahe tarnegraafiku rea, mitte algse tellimuse rea jaoks.  
21. Valige väljal Saatelehe printimine suvand Jah.
22. Klõpsake nuppu OK.
23. Klõpsake nuppu Jah.
24. Sulgege leht.

