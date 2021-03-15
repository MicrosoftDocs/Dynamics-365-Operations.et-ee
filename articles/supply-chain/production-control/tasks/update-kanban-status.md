---
title: Kanbani oleku uuendamine
description: Kui kanban on tühjendatud kogemata või vkui saadud kanban tuleb tühjendada, tuleb värskendada kanbani olekut.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1161e642f8b3b1cd0a2568e0745caa6db5fe5afb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980989"
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