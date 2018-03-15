--- 
title: " Järjepidevusprogrammi kasutamine"
description: "See protseduur selgitab järjepidevusprogrammi müüki ja seotud müügitellimuste töötlemist."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2017
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
ms.openlocfilehash: d2642d922fc1fa03644be8195a8c9dd3edfc3483
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---
# <a name="use-a-continuity-program"></a> Järjepidevusprogrammi kasutamine

[!include[task guide banner](../includes/task-guide-banner.md)]

See protseduur selgitab järjepidevusprogrammi müüki ja seotud müügitellimuste töötlemist. Protseduuri tegemiseks tuleb kasutaja seadistada kõnekeskuse kasutajaks. Protseduur kasutab demoettevõtte USRT andmeid.

1. Avage Jaemüük ja kaubandus > Kliendid > Klienditeenindus.
2. Tippige väljale SearchText väärtus Karen ja vajutage siis tabeldusklahvi.
    * Avanema peaks täpsema otsingu dialoog. Kui see ei avane, klõpsake nuppu Otsing sellest väljast paremal.  
3. Märkige loendis valitud rida.
    * Seal peaks olema ainult üks rida, milles on näha Karen Berg. Valige see rida, klõpsates linnukese veergu ruudustiku vasakus servas.  
4. Klõpsake Vali.
5. Klõpsake valikul New sales order (Uus müügitellimus).
    * Müügitellimuse number tuleks üles märkida. Seda on protseduuris hiljem vaja.  
6. Tippige väljale Kaubakood väärtus 88000 ja vajutage siis tabeldusklahvi.
    * See on demoettevõtte USRT puhul järjepidev kaup.  
7. Klõpsake valikut Valmis.
8. Sisestage väljale Makseviis väärtus Visa.
9. Klõpsake nuppu Lisa krediitkaart.
    * Sisestage sellele lehele vajalik krediitkaarditeave.  
10. Klõpsake nuppu OK.
11. Laiendage jaotist Makse.
    * Kõnekeskuse tellimuse esitamiseks tuleb tellimusele sisestada maksed.  
12. Klõpsake nuppu OK.
13. Klõpsake Edasta.
    * Uus järjepidev tellimus on valmis. Järgmiseks tuleb käivitada kaks partiitöötlust, mida kasutatakse järjepidevate tellimuste töötlemiseks.  
14. Sulgege leht.
15. Avage Jaemüük ja kaubandus > Järjepidevus > Järjepidevuse maksete töötlemine.
16. Tippige väljale Järjepidev kaup väärtus 88000 ja vajutage siis tabeldusklahvi.
17. Klõpsake nuppu OK.
18. Avage Jaemüük ja kaubandus > Järjepidevus > Järjepidevuse tütartellimuste loomine.
    * See protsess loob uued müügitellimused, mis põhinevad teie järjepidevusprogrammide sätetel.  
19. Tippige väljale Järjepidev kaup väärtus 88000 ja vajutage siis tabeldusklahvi.
    * Kaup 88000 on demoettevõtte USRT puhul järjepidev kaup.  
20. Valige või sisestage väärtus väljal Müügitellimus.
    * Sisestage müügitellimuse number, mille protseduuris enne üles märkisite. See tagab sellele protseduurile minimaalse töötlemisaja. Müügitellimuse väli on valikuline – töödelda saab mis tahes programmi kõiki tellimusi.  
21. Klõpsake nuppu OK.


