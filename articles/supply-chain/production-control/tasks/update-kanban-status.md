---
title: Kanbani oleku uuendamine
description: Kui kanban on tühjendatud kogemata või vkui saadud kanban tuleb tühjendada, tuleb värskendada kanbani olekut.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a0e03da4671ffec4ecf4835b20a00ef87971c94
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831813"
---
# <a name="update-kanban-status"></a>Kanbani oleku uuendamine

[!include [banner](../../includes/banner.md)]

Kui kanban on tühjendatud kogemata või vkui saadud kanban tuleb tühjendada, tuleb värskendada kanbani olekut. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See protseduur on mõeldud tööde järelevaatajale.


## <a name="find-the-kanban"></a>Otsige kanban üles.
1. Avage Tootmise juhtimine > Kanban > Kanbanid.
2. Avage oleku veeru filter Töötlusühik
3. Klõpsake käsku Tühjenda.
    * See lähtestab filtrid.  
4. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Filtreerige näiteks välja Kaardi number väärtusega 000149.

## <a name="change-emptied-status-to-received-status"></a>Tühjendatud oleku muutmine saadud olekuks
1. Klõpsake suvandit Tühja materjali käsitsemisühiku pööramine
2. Klõpsake nuppu OK.
    * Pange tähele, et suvandi Töötlusühik olek on Saadud.  

## <a name="change-received-status-to-emptied-status"></a>Saadud oleku muutmine tühjendatud olekuks
1. Klõpsake suvandit Tühi kanban.
2. Märkige loendis valitud rida.
    * Pange tähele, et suvandi Töötlusühik olek on Tühjendatud.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]