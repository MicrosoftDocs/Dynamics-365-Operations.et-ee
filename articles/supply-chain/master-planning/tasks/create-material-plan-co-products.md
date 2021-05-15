---
title: Kaastoodete jaoks materjaliplaani loomine
description: Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920725"
---
# <a name="create-a-material-plan-for-co-products"></a>Kaastoodete jaoks materjaliplaani loomine

[!include [banner](../../includes/banner.md)]

Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul. Selle protseduuri loomiseks kasutati demoettevõtte USP2 andmeid.

## <a name="create-requirement-for-a-co-product"></a>Kaastoote nõude loomine

1. Minge **müügi ja turunduse \> tööruumides \> müügitellimuse töötlemisele ja päringule**.
1. Valige suvand **Uus**.
1. Valige **Müügitellimus**.
1. Sisestage väärtus väljale **Kliendi konto**.
    * Näide: US-001.  
1. Valige nupp **OK**.
1. Sisestage väärtus väljale **Kaubakood**.
    * Näide: P6003.  
1. Sisestage arv väljale **Kogus**.
    * Näide: 50000  
1. Valige käsk **Salvesta**.

## <a name="create-a-material-plan-for-co-products"></a>Kaastoodete jaoks materjaliplaani loomine

1. Sulgege leht.
1. Sulgege leht.
1. Valige **Koondplaneerimine**.
1. Väljal **Plaan** valige ripploendi nuppu, et avada otsing.
1. Valige loendis link valitud reas.
    * Näide: MasterPlan  
1. Valige käsk **Käitus**.
1. Laiendage või ahendage jaotist **Kaasatavad kirjed**.
1. Valige **Filter**.
1. Valige loendist rida **Välja** = *üksuse numbri* kohta.
1. Sisestage väärtus väljale **Kriteerium**.
    * Näide: P6003.  
1. Valige nupp **OK**.
1. Valige nupp **OK**.
1. Valige **Plaanitud tellimused**.
1. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja **Kaubakood** väärtuse P6000 järgi.
    * Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.  
1. Märkige loendis valitud rida.
    * Valige mis tahes filtri tagastatud read.  
1. Valige loendis link valitud reas.
1. Laiendage jaotist **Sidumine**.
1. Valige loendis link valitud reas.
    * Plaanitud tellimus on seotud kaastoote müügitellimusega.  
1. Sulgege leht.

## <a name="create-a-second-requirement-for-a-co-product"></a>Teise kaastoote nõude loomine

1. Minge **müügi ja turunduse \> tööruumides \> müügitellimuse töötlemisele ja päringule**.
1. Valige suvand **Uus**.
1. Valige **Müügitellimus**.
1. Sisestage väärtus väljale **Kliendi konto**.
    * Näide: US-001.  
1. Valige nupp **OK**.
1. Sisestage väärtus väljale **Kaubakood**.
    * Näide: P6003.  
1. Sisestage arv väljale **Kogus**.
    * Näide: 50000  
1. Valige käsk **Salvesta**.

## <a name="create-a-second-material-plan-for-co-products"></a>Kaastoodete jaoks teise materjaliplaani loomine

1. Väljal **Plaan** valige ripploendi nuppu, et avada otsing.
2. Valige loendis link valitud reas.
    * Näide: MasterPlan  
3. Valige käsk **Käitus**.
4. Laiendage või ahendage jaotist **Kaasatavad kirjed**.
5. Valige **Filter**.
6. Valige loendist rida **Välja** = *üksuse numbri* kohta.
7. Sisestage väärtus väljale *Kriteerium*.
    * Näide: P6003.  
8. Valige nupp **OK**.
9. Valige nupp **OK**.
10. Valige **Plaanitud tellimused**.
11. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja **Kaubakood** väärtuse P6000 järgi.
    * Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.  
12. Märkige loendis valitud rida.
    * Valige mis tahes filtri tagastatud read.  
13. Valige loendis link valitud reas.
14. Laiendage või ahendage jaotist **Sidumine**.
15. Valige loendis link valitud reas.
    * Plaanitud tellimus on seotud kaastoote müügitellimusega.  
16. Sulgege leht.
17. Valige **Koondplaneerimine**.
18. Avage **Koondplaneerimine \> Seadistus \> Koondplaneerimise parameetrid**.
19. Valige väljal *Keela kõik planeerimisprotsessid* suvand **Ei**.
20. Sulgege leht.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]