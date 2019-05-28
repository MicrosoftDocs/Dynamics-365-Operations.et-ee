---
title: " Jaekaupluse jaoks väljavõtte loomine, arvutamine ja sisestamine"
description: See protseduur kirjeldab kaupluse kohta väljavõtte loomise, arvutamise ja sisestamise etappe.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9ea30e7e008bfcce77a7ee2f4d7d01a6cf1ababc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548320"
---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a> Jaekaupluse jaoks väljavõtte loomine, arvutamine ja sisestamine

[!include[task guide banner](../includes/task-guide-banner.md)]

See protseduur kirjeldab kaupluse kohta väljavõtte loomise, arvutamise ja sisestamise etappe. Samade ülesannete jaoks saab konfigureerida ka pakett-töid. Pakett-tööde konfigureerimise ja käitamise etapid leiate teistest teemadest. Selle protseduuri tegemiseks peavad teil olema kassas lõpule viidud ja seejärel Dynamics AX-i tõmmatud kanded. See salvestis kasutab demoettevõtte USRT andmeid. See toiming võib viidata Microsoft Dynamics AX-ile. Pange tähele, et Dynamics AX-i nimi on nüüd Microsoft Dynamics 365 for Operations.

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

