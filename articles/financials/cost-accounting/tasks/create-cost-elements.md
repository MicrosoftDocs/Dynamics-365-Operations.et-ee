--- 
title: 'Kuluelementide loomine  '
description: "Kuluarvestuses on kuluelementide loomiseks mitu võimalust."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0b1045610881bc272798f1176fbca58731e5d43b
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="create-cost-elements"></a>Kuluelementide loomine   

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kuluarvestuses on kuluelementide loomiseks mitu võimalust. See protseduur näitab, kuidas luua kuluelemente, importides põhikontod andmekonnektori kaudu. Selle protseduuri loomiseks kasutati demoettevõtet USMF. See protseduur on kuluarvestuse funktsiooni jaoks, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="create-new-cost-elements"></a>Uute kuluelementide loomine
1. Avage Kuluarvestus > Dimensioonid > Kuluelemendi dimensioonid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
4. Sisestage või valige väärtus väljal Andmekonnektor dimensiooniliikmete jaoks.
5. Sisestage väljale Kirjeldus soovitud väärtus.
6. Klõpsake nuppu Salvesta.

## <a name="configure-the-data-connector"></a>Andmekonnektori konfigureerimine
1. Klõpsake valikut Dimensiooniliikme pakkuja konfigureerimine.
2. Sisestage väärtus väljale Kontoplaan või valige see.
    * Jagatud kontoplaani kasutamiseks valige Jagatud.  
3. Klõpsake valikut Uus.
4. Märkige loendis valitud rida.
    * Saate oma kriteeriumide täitmiseks rakendada kontodele filtreid.  
5. Sisestage väärtus väljale Põhikontolt või valige see.
6. Sisestage väärtus väljale Põhikontole või valige see.
7. Klõpsake nuppu OK.

## <a name="import-main-accounts"></a>Impordi põhikontod
1. Klõpsake valikut Dimensiooniliikmete importimine.
    * Põhikontod imporditakse kuluarvestusse ja neid kasutatakse kuluelementidena.  
2. Klõpsake nuppu OK.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Imporditud kontode vaatamine kuluelementidena
1. Klõpsake valikut Dimensiooniliikmete kuvamine.
    * Kuva imporditud pearaamatukontod kuluelementidena oma ettevõttes, kuhu kuluvoo saab suunata.  


