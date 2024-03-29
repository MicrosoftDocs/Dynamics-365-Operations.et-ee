---
title: Järjepidevusprogrammi kasutamine
description: See protseduur selgitab järjepidevusprogrammi müüki ja seotud müügitellimuste töötlemist.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
ms.openlocfilehash: 3736984a336b35b23b7060b2d98770912cc9ec6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267400"
---
# <a name="using-continuity-program"></a>Järjepidevusprogrammi kasutamine

[!include [banner](../includes/banner.md)]

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
