--- 
title: " Jaekaupluse jaoks väljavõtte loomine, arvutamine ja sisestamine"
description: "See protseduur kirjeldab kaupluse kohta väljavõtte loomise, arvutamise ja sisestamise etappe."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 42ab631e29a7fae1140acd41ad80c13e55ca1404
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a> Jaekaupluse jaoks väljavõtte loomine, arvutamine ja sisestamine

[!include[task guide banner](../includes/task-guide-banner.md)]

See protseduur kirjeldab kaupluse kohta väljavõtte loomise, arvutamise ja sisestamise etappe. Samade ülesannete jaoks saab konfigureerida ka pakett-töid. Pakett-tööde konfigureerimise ja käitamise etapid leiate teistest teemadest. Selle protseduuri tegemiseks peavad teil olema kassas lõpule viidud ja seejärel Dynamics AX-i tõmmatud kanded. See salvestis kasutab demoettevõtte USRT andmeid. See protseduur võib viidata Microsoft Dynamics AX-ile. Arvestage, et Dynamics AX-i nimi on nüüd Microsoft Dynamics 365 for Operations.

1. Avage Kõik tööruumid >... > Jaekaupluse rahandus.
2. Klõpsake suvandit Uus väljavõte.
3. Klõpsake väljal Kaupluse number otsingu avamiseks ripploendi nuppu.
4. Klõpsake loendis valitud real olevat linki.
5. Klõpsake nuppu OK.
    * Seadistusgrupp sisaldab sätteid, mis määravad, millised kanded kaasatakse väljavõttesse ja kuidas need väljavõtteridadele grupeeritakse. Saate seadistusgrupi avada ja neid sätteid muuta, kuid võite kasutada ka vaikesätteid.  
    * Väli Väljavõtteviis määratleb väljavõtteridade grupeerimise viisi.  
    * Valige töötaja või register, kui soovite arvutada väljavõtte ainult kindla töötaja või registri kohta.  
6. Valige suvand väljal Sulgemismeetod.
7. Klõpsake suvandit Väljavõtte arvutamine.
8. Klõpsake nuppu Jah.
    * Pärast väljavõtte arvutamist peaksid olema loodud read koos kogusummadega iga kasutatud makseviisi ja väljavõtteviisi kohta.  
    * Sisestage igale reale inventeeritud summa, kui see tuleb sisestada või seda värskendada. Inventeeritud summa väli täidetakse summadega kassas tehtud päevakassadest.  
9. Klõpsake suvandit Väljavõtte sisestamine.
10. Klõpsake valikut Sule.
11. Minge jaotisse Jaemüük ja kaubandus > Kanalid > Jaekaupluse rahandus.
12. Klõpsake vahekaarti Sisestatud väljavõtted.


