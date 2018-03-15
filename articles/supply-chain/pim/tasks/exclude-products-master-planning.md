--- 
title: "Toote elutsükli oleku loomine toodete välistamiseks koondplaneerimisest"
description: "See protseduur kirjeldab, kuidas luua uut toote elutsükli olekut, mis välistab tooted koondplaneerimisest ja koosluse taseme arvutusest."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: 1685e8eb706e29ef5b195e9163bf19345fee78b6
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Toote elutsükli oleku loomine toodete välistamiseks koondplaneerimisest

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur kirjeldab, kuidas luua uut toote elutsükli olekut, mis välistab tooted koondplaneerimisest ja koosluse taseme arvutusest.


## <a name="create-an-obsolete-state"></a>Aegunud oleku loomine
1. Avage Tooteteabe haldus > Häälestus > Toote elutsükli olek.
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Olek.
4. Valige Ei väljal On planeerimiseks aktiivne.
5. Sisestage väljale Kirjeldus soovitud väärtus.

## <a name="associate-the-obsolete-state-to-a-released-product"></a>Aegunud oleku seostamine väljastatud tootega
1. Sulgege leht.
2. Avage Tooteteabe haldus > Tooted > Väljastatud tooted.
3. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks filtreerige välja Otsingunimi väärtusega „M00”.
4. Klõpsake nuppu Redigeeri.
5. Märkige loendis valitud rida.
6. Väljal Toote elutsükli olek sisestage või valige väärtus.

