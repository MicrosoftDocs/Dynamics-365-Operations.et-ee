--- 
title: Kaastoodete jaoks materjaliplaani loomine
description: "Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a>Kaastoodete jaoks materjaliplaani loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul. Selle protseduuri loomiseks kasutati demoettevõtte USP2 andmeid.


## <a name="create-requirement-for-a-co-product"></a>Kaastoote nõude loomine
1. Avage Vaikearmatuurlaud.
2. Klõpsake valikut Müügitellimuse töötlemine ja päring.
3. Klõpsake Uus.
4. Klõpsake valikut Müügitellimus.
5. Sisestage väärtus väljale Kliendi konto.
    * Näide: US-001.  
6. Klõpsake nuppu OK.
7. Sisestage väärtus väljale Kaubakood.
    * Näide: P6003.  
8. Sisestage arv väljale Kogus.
    * Näide: 50000  
9. Klõpsake nuppu Salvesta.

## <a name="create-a-material-plan-for-co-products"></a>Kaastoodete jaoks materjaliplaani loomine
1. Klõpsake valikul Koondplaneerimine.
2. Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.
3. Klõpsake loendis valitud real olevat linki.
    * Näide: MasterPlan  
4. Klõpsake nuppu Käivita.
5. Laiendage või ahendage jaotist Kaasatavad kirjed.
6. Klõpsake käsku Filtreeri.
7. Valige loendist rida, mille väli = kaubakood.
8. Sisestage väärtus väljale Kriteeriumid.
    * Näide: P6003.  
9. Klõpsake nuppu OK.
10. Klõpsake nuppu OK.
11. Klõpsake valikut Planeeritud tellimused.
12. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja Kaubakood väärtuse P6000 järgi.
    * Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.  
13. Märkige loendis valitud rida.
    * Valige mis tahes filtri tagastatud read.  
14. Klõpsake loendis valitud real olevat linki.
15. Laiendage või ahendage jaotist Sidumine.
16. Klõpsake loendis valitud real olevat linki.
    * Plaanitud tellimus on seotud kaastoote müügitellimusega.  
17. Sulgege leht.


