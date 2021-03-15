---
title: Kaastoodete jaoks materjaliplaani loomine
description: Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8e9067cdd8851da31c07a92217001e447f400d4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983387"
---
# <a name="create-a-material-plan-for-co-products"></a>Kaastoodete jaoks materjaliplaani loomine

[!include [banner](../../includes/banner.md)]

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
1. Sulgege leht.
2. Sulgege leht.
3. Klõpsake valikul Koondplaneerimine.
4. Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.
5. Klõpsake loendis valitud real olevat linki.
    * Näide: MasterPlan  
6. Klõpsake nuppu Käivita.
7. Laiendage või ahendage jaotist Kaasatavad kirjed.
8. Klõpsake käsku Filtreeri.
9. Valige loendist rida, mille väli = kaubakood.
10. Sisestage väärtus väljale Kriteeriumid.
    * Näide: P6003.  
11. Klõpsake nuppu OK.
12. Klõpsake nuppu OK.
13. Klõpsake valikut Planeeritud tellimused.
14. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja Kaubakood väärtuse P6000 järgi.
    * Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.  
15. Märkige loendis valitud rida.
    * Valige mis tahes filtri tagastatud read.  
16. Klõpsake loendis valitud real olevat linki.
17. Laiendage või ahendage jaotist Sidumine.
18. Klõpsake loendis valitud real olevat linki.
    * Plaanitud tellimus on seotud kaastoote müügitellimusega.  
19. Sulgege leht.

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
1. Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.
2. Klõpsake loendis valitud real olevat linki.
    * Näide: MasterPlan  
3. Klõpsake nuppu Käivita.
4. Laiendage või ahendage jaotist Kaasatavad kirjed.
5. Klõpsake käsku Filtreeri.
6. Valige loendist rida, mille väli = kaubakood.
7. Sisestage väärtus väljale Kriteeriumid.
    * Näide: P6003.  
8. Klõpsake nuppu OK.
9. Klõpsake nuppu OK.
10. Klõpsake valikut Planeeritud tellimused.
11. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja Kaubakood väärtuse P6000 järgi.
    * Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.  
12. Märkige loendis valitud rida.
    * Valige mis tahes filtri tagastatud read.  
13. Klõpsake loendis valitud real olevat linki.
14. Laiendage või ahendage jaotist Sidumine.
15. Klõpsake loendis valitud real olevat linki.
    * Plaanitud tellimus on seotud kaastoote müügitellimusega.  
16. Sulgege leht.
17. Klõpsake valikul Koondplaneerimine.
18. Avage Koondplaneerimine > Seadistus > Koondplaneerimise parameetrid.
19. Valige väljal Keela kõik planeerimisprotsessid suvand Ei.
20. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]