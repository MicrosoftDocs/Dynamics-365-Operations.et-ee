---
title: Dimensioonipõhise tooteetaloni jaoks koosluse loomine
description: Selle protseduuri puhul peab teil olema lõpule viidud eelmised 4 juhist selles kaheksa salvestuse järjekorras.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 799479c4b4cdf5b61b1f55a61454823558b9013b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237420"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Dimensioonipõhise tooteetaloni jaoks koosluse loomine

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]