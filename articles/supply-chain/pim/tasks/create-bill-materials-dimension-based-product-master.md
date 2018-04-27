--- 
title: "Dimensioonipõhise tooteetaloni jaoks koosluse loomine"
description: "Selle protseduuri puhul peab teil olema lõpule viidud eelmised 4 juhist selles kaheksa salvestuse järjekorras."
author: YuyuScheller
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8b5432addd1dd79a64dcbb751a59cf3084a63ab1
ms.openlocfilehash: 05837c2b21957133729074f614a6d3d7b7c08dad
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Dimensioonipõhise tooteetaloni jaoks koosluse loomine

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Selle protseduuri puhul peab teil olema lõpule viidud eelmised 4 juhist selles kaheksa salvestuse järjekorras. Esimesed 4 salvestust seadistavad andmed, mida on selle protseduuri lõpuleviimiseks vaja. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. Seda ülesannet täidab tavaliselt toote koostaja.


## <a name="select-the-product"></a>Toote valimine
1. Klõpsake valikut Väljastatud toodete hooldus.
2. Klõpsake valikut Väljastatud tooted.
3. Märkige loendis valitud rida.
    * Otsige üles väljastatud tooteetalon koos dimensioonipõhise konfiguratsiooni tehnoloogiaga, mille lõite esimese ülesande juhendis selles järjekorras.  
4. Klõpsake toimingupaanil suvandit Projekteeri.
5. Klõpsake koosluse versioone.

## <a name="create-new-bom-and-bom-version"></a>Uue koosluse ja koosluse versiooni loomine
1. Klõpsake valikut Uus.
2. Klõpsake kooslust ja koosluse versiooni.
3. Sisestage väärtus väljale Nimi.
    * Tegevuskoha seadistamine  
    * Selles protseduuris ei määrata kooslusele konkreetset tegevuskohta.  
4. Klõpsake nuppu OK.
5. Klõpsake valikut Uus.
    * Selles protseduuris lisame kooslusele neli rida. Kaks rida tähistavad kaabli suvandeid ja kaks rida tähistavad kartoteegi suvandeid.  
6. Märkige loendis valitud rida.
7. Sisestage või valige väärtus väljal Kaubakood.
    * Valige kauba number A0001, HDMI 6' kaablid.  
8. Sisestage või valige väärtus väljal Konfiguratsioonigrupp.
    * Valige kaabli konfiguratsioonigrupp, mis loodi juhendis 4 selles järjekorras.  
9. Klõpsake valikut Uus.
    * Valige kauba number A0002, HDMI 12' kaablid.  
10. Märkige loendis valitud rida.
11. Sisestage või valige väärtus väljal Kaubakood.
12. Sisestage või valige väärtus väljal Konfiguratsioonigrupp.
    * Valige uuesti kaabli konfiguratsioonigrupp.  
13. Klõpsake valikut Uus.
14. Märkige loendis valitud rida.
15. Sisestage või valige väärtus väljal Kaubakood.
    * Valige kauba number D0002 kartoteek.  
16. Sisestage või valige väärtus väljal Konfiguratsioonigrupp.
    * Valige kartoteegi konfiguratsioonigrupp sellele koosluse reale.  
17. Klõpsake valikut Uus.
18. Märkige loendis valitud rida.
19. Sisestage või valige väärtus väljal Kaubakood.
    * Valige kauba number M0007 StandardCabinet viimase koosluse reana.  
20. Sisestage või valige väärtus väljal Konfiguratsioonigrupp.
    * Valige kartoteegi konfiguratsioonigrupp viimasele koosluse reale.  

## <a name="approve-and-activate"></a>Kinnita ja aktiveeri
1. Sulgege leht.
2. Klõpsake nuppu Kinnita.
3. Valige või sisestage väärtus väljal Kinnitaja.
4. Valige Jah väljal Kas soovite ka koosluse kinnitada?
5. Klõpsake nuppu OK.
6. Klõpsake käsku Aktiveeri.


