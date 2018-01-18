--- 
title: " Kõnekeskuse tellimuste loomine"
description: "See protseduur juhendab kliendi otsimisel, uue tellimuse loomisel, toote otsimisel ja kliendilt makse vastuvõtmisel."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f702690f72b3e299f6c2744da326a23d5753eb5d
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-call-center-orders"></a> Kõnekeskuse tellimuste loomine

[!include[task guide banner](../includes/task-guide-banner.md)]

See protseduur juhendab kliendi otsimisel, uue tellimuse loomisel, toote otsimisel ja kliendilt makse vastuvõtmisel. See protseduur kasutab ettevõtte USRT demoandmeid ja on mõeldud müügitellimuste ametnikule. Eeltingimused: kasutaja, kes viib protseduuri lõpule, häälestatakse kõnekeskuse kasutajana ja Fabrikami poolaastakataloogis avaldatakse vähemalt üks lähtekood.

1. Avage Jaemüük ja kaubandus > Kliendid > Klienditeenindus.
2. Sisestage väljale SearchText otsingukriteeriumid kliendi leidmiseks.
    * Selleks näidisprotseduuriks trükkige "karen" ja vajutage klahvi Tab.  
3. Klõpsake nuppu Otsing.
    * Kuna demoandmetes on ainult ühe kliendi nimi Karen, valitakse need automaatselt.  
4. Klõpsake valikul New sales order (Uus müügitellimus).
5. Laiendage või ahendage jaotise Sales order (Müügitellimus) päiseosa.
6. Valige kataloogi jaoks lähtekood.
    * Kui ühtegi aktiivset lähtekoodi ei ole, saab välja Source (Allikas) sulgeda ning selle etapi vahele jätta.  
7. Klõpsake käsku Lisa rida.
8. Sisestage väljale Item number (Kauba number) kauba otsingusõna.
    * Selleks näidisprotseduuriks sisestage osaline kaubanumber 8111 ja vajutage klahvi Tab. See avab kauba otsingu hüpikakna.  
9. Valige toode müügitellimusele lisamiseks
10. Sisestage müügikogus.
11. Klõpsake käsku Loo.
12. Klõpsake kliendi makse vastuvõtmiseks nuppu Complete (Valmis).
13. Klõpsake vahekaarti Lisa.
    * Lisamise link on vahekaardil Payments (Maksed). Laiendage maksete vahekaarti, kui see on kokku pandud.  
14. Valige makseviis.
    * Valige selle protseduuri jaoks sularaha maksemeetod.  
15. Sulgege leht.
16. Sisestage summa.
    * Sisestage selle protseduuri jaoks summa, mis on võrdne tellimuse saldoga, mis on nähtav müügitellimuse kokkuvõtte lehel summa väljast vasakul pool. See võimaldab teil tellimuse täielikult tasutuna lõpetada.  
17. Klõpsake nuppu OK.
18. Klõpsake Edasta.


