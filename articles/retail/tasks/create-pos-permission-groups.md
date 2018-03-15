--- 
title: " Kassa loagruppide loomine"
description: "See protseduur näitab, kuidas kassalubade gruppi luua."
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: bcda7c3a5c2cc97fbc6e4945e4d5f0ec42a7a478
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---
# <a name="create-pos-permission-groups"></a> Kassa loagruppide loomine

[!include[task guide banner](../includes/task-guide-banner.md)]

See protseduur näitab, kuidas kassalubade gruppi luua. Selle tegevuse loomisel kasutati demoettevõtte USRT-i andmeid. See ülesanne on mõeldud Jaemüügitoimingute halduri rolli jaoks.

1. Tehke valik Permission groups (Lubade grupid).
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale POS permission group ID (Kassalubade grupi ID).
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Valige Yes (Jah) väljal View time clock entries (Vaata ajaarvesti kirjeid).
    * Saate nüüd oma kassalubade grupile erinevaid lube anda või neid eemaldada. Mõne loa jaoks saate määrata väärtuse, mida kasutatakse hindamiseks, kas kassa kasutaja saab seda toimingut teha.  See tegevusjuhend annab mõned load, mida kassapidajale võidakse määrata.  
6. Valige Yes (Jah) väljal Allow create order (Luba tellimuse loomine).
7. Valige Yes (Jah) väljal Allow edit order field (Luba tellimuse redigeerimine).
8. Valige Yes (Jah) väljal Allow retrieve order (Luba tellimuse väljaotsimine).
9. Valige Yes (Jah) väljal Allow password change (Luba parooli muutmine).
10. Valige Yes (Jah) väljal Allow blind close (Luba pimesi sulgemine).
11. Klõpsake nuppu Salvesta.
    * Pärast muudatuste salvestamist peate käivitama personali jaotusgraafiku, et muutused jaemüügikanalitesse edastada.  
12. Sulgege leht.
13. Minge valikusse Jobs (Tööd).
    * Järgmisena määrame kassalubade grupi töö järgi.  
14. Otsige loendist ja valige soovitud kirje.
15. Klõpsake loendis valitud real olevat linki.
16. Klõpsake nuppu Redigeeri.
17. Laiendage jaotist Job classification (Tööde klassifikatsioon).
18. Sisestage või valige väärtus väljal POS permission group (Kassalubade grupp).
    * Kõik töötajad, kelle ametikohad sellele tööle vastavad, kasutavad selle kassalubade grupi sätteid, kui töötajate kassalube ei ole nende ametikoha tasemel tühistatud.  
19. Klõpsake nuppu Salvesta.
    * Pärast muudatuste salvestamist peate käivitama personali jaotusgraafiku, et muutused jaemüügikanalitesse edastada.  


