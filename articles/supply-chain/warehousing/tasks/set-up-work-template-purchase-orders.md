--- 
title: "Ostutellimuste jaoks töömalli seadistamine"
description: "See protseduur keskendub lihtsa töömalli seadistamisele, mida saab kasutada saadud kaupade paigutamiseks."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fbbe019bdca2d5182466a20370418a14032fe63d
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Ostutellimuste jaoks töömalli seadistamine

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

See protseduur keskendub lihtsa töömalli seadistamisele, mida saab kasutada saadud kaupade paigutamiseks. Töömallid määravad juhiste kogumi, mis esitatakse laotöötajale mobiilsel seadmel, kui kaupu vastuvõtualalt ära viiakse. Saate kasutada seda protseduuri demoettevõttes USMF nimetatud andmetega. Enne selle juhendi käivitamist looge töökausta ID. Selles näites kasutatakse töökausta ID-d nimega Sissetulev. See protseduur on mõeldud laohaldurile.

1. Avage Laohaldus > Seadistus > Töö > Töömallid.
2. Valige väljal Töötellimuse tüüp suvand Ostutellimus.

## <a name="create-a-work-template-header"></a>Töömalli päise loomine
1. Klõpsake valikut Uus.
2. Sisestage number väljale Seerianumber.
    * See on järjestus, milles töömalle hinnatakse. Vajaduse korral saate järjestust muuta.  
3. Sisestage väärtus väljale Töömall.
    * See on selle malli ainuidentifikaator.  
4. Tippige väärtus väljale Töömalli kirjeldus.
    * Suvandit Kehtiv ei märgita enne, kui olete lisanud kõik malli puhul vajaliku teabe ja klõpsanud seejärel käsku Salvesta.  
    * Töötellimuse tüüpi Ostutellimus ei saa automaatselt töödelda, seega jätke valiku Töötle automaatselt suvandiks Ei.  
5. Tippige väärtus väljale Töökausta ID.
    * Töökaustade ID-de abil saate töö gruppidesse korraldada. Siin määratud väärtus on vaikeväärtus selle malli abil loodud tööde puhul.  
6. Sisestage väljale Töö prioriteet väärtus 1.
    * See näitab töö olulisust ja siin määratud väärtus on selle malli abil loodud töö puhul vaikeväärtus.  
7. Klõpsake nuppu Salvesta.
    * Enne, kui saab kasutada nuppu Päringu redigeerimine, tuleb töömalli päis salvestada.  

## <a name="set-up-the-query-for-the-work-template"></a>Töömalli jaoks kasutatava päringu häälestamine
1. Klõpsake suvandit Redigeeri päringut.
    * Määrame piirangu, et malli saab kasutada ainult konkreetses laos.  
2. Klõpsake vahekaarti Lisa.
3. Märkige loendis valitud rida.
4. Sisestage väljale Väli sõna „ladu”.
5. Sisestage väärtus väljale Kriteeriumid.
6. Klõpsake nuppu OK.
7. Klõpsake nuppu Jah.

## <a name="set-work-template-details"></a>Töömalli üksikasjade häälestamine
1. Klõpsake valikut Uus.
2. Tehke väljal Töö tüüp valik Komplekteeri.
3. Sisestage väljale Tööklassi ID sõna „ost”.
    * Siin määratud tööklassist saab vaikeväärtus kõigile tööridadele tüübiga Komplekteerimine, mis selle malli abil luuakse. Töötellimuse ridadelt ei saa tööklassi alistada. Tööklassidega suunatakse ja/või piiratakse töötellimuse ridade tüüp, mida laotöötaja saab mobiilses seadmes töödelda.  
4. Klõpsake valikut Uus.
5. Valige väljal Töö tüüp suvand Pane.
6. Sisestage väärtus väljale Tööklassi ID.
    * Komplekteerimise ja asetamise juhised on üks kogum. Igal komplekteerimise ja asetamise kogumil peab olema sama töö klass. Kasutage sama töö klassi, mille komplekteerimisjuhise jaoks andsite.  
7. Klõpsake nuppu Salvesta.
    * Pange tähele, et märkeruut Kehtiv on nüüd märgitud.  


