--- 
title: " Kõnekeskuse tellimuste loomine"
description: "See protseduur juhendab kliendi otsimisel, uue tellimuse loomisel, toote otsimisel ja kliendilt makse vastuvõtmisel."
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: b2e986df1e089ef2a394d0e9d9236d39f2726c77
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

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


