--- 
title: Tegevuskoha jaoks plaani loomine
description: "Tootmise plaanija arvutab materjali ja võimsuse nõuded konkreetse kauba tootmiseks."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
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
ms.openlocfilehash: d89d34d4d429faf87c70943961f7141a6258d482
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-plan-for-a-site"></a>Tegevuskoha jaoks plaani loomine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tootmise plaanija arvutab materjali ja võimsuse nõuded konkreetse kauba tootmiseks. Pärast hankimissoovituste loomist otsib ta planeeritava tegevuskoha tellimused ja kinnitab tellimused, alustades pakilisematega. Kõige pakilisemad tellimused on need, mis tuleb kinnitada käesoleval kuupäeval. Kasutage nende ülesannete täitmiseks demoandmete ettevõtet USMF.


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>Kaubale materjalide ja võimsuse plaani loomine
1. Klõpsake valikul Koondplaneerimine.
    * Peate liikuma vaikearmatuurlauale.  
2. Klõpsake nuppu Käivita.
3. Jaotise kaasamiseks laiendage kirjeid.
4. Klõpsake käsku Filtreeri.
5. Märkige loendis valitud rida.
6. Sisestage väärtus väljale Kriteeriumid.
    * Näide: D0001.  
7. Klõpsake nuppu OK.
8. Klõpsake nuppu OK.
    * Selleks võib kuluda mõni minut.  
9. Värskendage lehte.

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>Pakiliste plaanitud kaubatellimuste tuvastamine
1. Avage veeru Kaubakood filter.
2. Rakendage väljal Kaubakood filtrit väärtusega „D0001”ning kasutage filtri tehtemärki algab järgmisega.
3. Avage veeru Tellimuse kuupäev filter.
4. Rakendage filtrit väljal Tellimuse kuupäev koos praeguse kuupäeva väärtusega, kasutades filtrit väärtusega „on täpselt”.

## <a name="firm-all-the-urgent-orders-for-the-item"></a>Kõikide pakiliste kaubatellimuste kinnitamine
1. Märkige või tühjendage loendis kõik read.
2. Klõpsake nuppu Kinnita.
3. Klõpsake nuppu OK.


