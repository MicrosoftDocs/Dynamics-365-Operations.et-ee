--- 
title: "Ülekandmistegevuste loomine: lean manufacturing"
description: "Ülekandetegevuse loomine lean manufacturingi jaoks."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: e19822fcd56a81cc0ef77d33e1c1e3e6e93d86e3
ms.contentlocale: et-ee
ms.lasthandoff: 07/28/2017

---
# <a name="create-transfer-activities-for-lean-manufacturing"></a>Ülekandmistegevuste loomine: lean manufacturing

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ülekandetegevuse loomine lean manufacturingi jaoks. 

Eeltingimused: 

1. Tuleb luua tootmisvoog ja mitteaktiivne versioon.

2. Tuleb luua saate- ja vastuvõtulaod ja asukohad. Soovi korral saate luua täiendava või täiendatud tööraku.


## <a name="find-the-production-flow-version"></a>Tootmisvoo versiooni leidmine
1. Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.
2. Otsige loendist ja valige soovitud kirje.
    * Pange tähele, et tootmisvool peab olema mustandolekus versioon.  
3. Klõpsake loendis valitud real olevat linki.

## <a name="create-a-new-activity"></a>Uue tegevuse loomine
1. Klõpsake suvandit Tegevused.
    * Veenduge, et valitud tootmisvool oleks mustandversioon, ja valige see versioon.  
2. Klõpsake suvandit Uue plaanitegevuse loomine.
3. Klõpsake käsku Edasi.
4. Sisestage väärtus väljale Nimi.
5. Valige väljal Tegevuse tüüp suvand Ülekanne.
6. Sisestage number väljale Protsessikogus.
7. Klõpsake käsku Edasi.

## <a name="select-the-work-cells"></a>Töörakkude valimine
1. Klõpsake väljal Täiendamine otsingu avamiseks ripploendi nuppu.
    * Tööraku väljundasukoha kasutamiseks ülekandetegevuse lähteasukohana valige töörakk. Sama saab teha täiendatud töörakuga, mis määrab ülekandetegevuse sihtasukoha.  
2. Klõpsake loendis valitud real olevat linki.

## <a name="define-the-inventory-updates"></a>Laovarude värskenduste määratlemine
1. Valige suvand väljal Toote tüüp.
    * Pange tähele, et ülekanne ei muuda toote tüüpi. Saate valmistooted või pooltooted üle kanda (ülekanne tootmisvoo ja võib-olla ka kanban-voo kahe tegevuse vahel).     Valmistoodete ülekandmisel saate valida varude ülekandes komplekteerimise või vastuvõtmise tulemused.  

## <a name="define-the-transfer-locations"></a>Ülekande asukohtade määratlemine
1. Klõpsake käsku Edasi.
2. Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.
3. Otsige loendist ja valige soovitud kirje.
4. Klõpsake loendis valitud real olevat linki.
5. Klõpsake väljal Asukoht otsingu avamiseks ripploendi nuppu.
6. Klõpsake loendis valitud real olevat linki.
7. Valige väljal Lastija suvand Saatja.
    * Suvandid hõlmavad järgmist: saatja – tarneladu juhtiv organisatsioon, saaja – vastuvõtvat ladu juhtiv organisatsioon, vedaja – muu osapoole hankija. Kui juhtiv organisatsioon on hankija, nõuab ülekandetegevus allhankelepingut.  
8. Klõpsake käsku Edasi.

## <a name="define-the-activity-times"></a>Tegevusaegade määratlemine
1. Otsige loendist ja valige soovitud kirje.
    * Vajalik on Käitusaja määratlus. Käitusaega kasutatakse kanban-tööde maksumuse ja läbilaskeaegade arvutamiseks. Käitusaegu ei kasutata täiskoormuse ja tarbimise arvutamiseks; neid arvutatakse tsükliaja järgi, mis saadakse tootmisvoo versiooni ülesandest.  
2. Sisestage number väljale Kellaaeg.
3. Sisestage väärtus väljale Ühik.
4. Valige ajaühik.
5. Sisestage number väljale Koguse kohta.
6. Otsige loendist ja valige soovitud kirje.
    * Ooteajad on valikulised.  
7. Sisestage number väljale Kellaaeg.
8. Sisestage väärtus väljale Ühik.
9. Valige ajaühik.
10. Sisestage number väljale Koguse kohta.
11. Klõpsake käsku Edasi.
12. Klõpsake Lõpeta.
13. Sulgege leht.

