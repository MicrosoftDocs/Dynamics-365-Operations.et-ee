---
title: Kanban-tööde plaanimine
description: See protseduur keskendub protsessi kanban-tööde plaanimisele kindla tööraku puhul.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2cab3af0802ae6fa942460cfdd9c0819e1d31d4b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579084"
---
# <a name="schedule-kanban-jobs"></a>Kanban-tööde plaanimine

[!include [banner](../../includes/banner.md)]

See protseduur keskendub protsessi kanban-tööde plaanimisele kindla tööraku puhul. Protseduur Protsessi kanban-töö ettevalmistamine materjalide mittesaadavusel tööraku puhul on selle protseduuri loomise eeltingimus. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See ülesanne on mõeldud kanbanidega töötavale tööde järelevaatajale ja tootmise planeerijale.


## <a name="select-kanban-jobs-for-a-work-cell"></a>Kanban-tööde valimine tööraku puhul
1. Avage Tootmise juhtimine > Kanban > Kanban-tööde plaanimine.
2. Kiirinfo Perioodi võimsus laiendamine
    * Laiendage kiirinfot Kanban.  
3. Klõpsake väljal Töörakk otsingu avamiseks ripploendi nuppu.
4. Märkige loendis valitud rida.
    * Valige töörakk 1250. See filtrib vaate kuvama ainult tööraku 1250 töid.  
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake Vali.

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a>Kanban-töö plaanimine esimeses saadaolevas perioodis
1. Märkige loendis valitud rida.
    * Valige esimene rida loendist, mille olek on Plaanimata. Punktiirikoon väljal Töö olek näitab plaanimatust.  
2. Klõpsake suvandit Graafik.
    * See kavandab kanban-töö esimeses saadaolevas perioodis.  
    * Pange tähele, et kanban-töö teisaldatakse loendi lõppu, kuna see on lisatud perioodi alates tänasest.  
    * Kui periood alates tänasest on täis, teisaldatakse töö esimesse saadaolevasse perioodi.  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a>Kahe kanban-töö plaanimine kindlaks päevaks
1. Valige loendist rida 1.
    * Peaksite nägema, et esimesel real on väljal Töö olek suvandiks Plaanimata.  
2. Valige loendist rida 2.
    * Peaksite nägema, et teisel real on väljal Töö olek suvandiks Plaanimata. Nüüd on teil kaks esimest tööd valitud.  
3. Rippdialoogi avamiseks klõpsake suvandit Plaani alates kuupäevast.
4. Märkige või tühjendage ruut Alista mahu puudujäägi reaktsioon.
    * See suvand võimaldab teil vaikimisi mahu puudujäägi reaktsiooni alistada.  
5. Valige väljalt Võimsuse puudujäägi reaktsioon suvand Lisa taotletud perioodile.
    * See suvand tagab töö lisamise taotletud perioodi olenemata sellest, kas töörakk võib olla ülekoormatud.  
6. Klõpsake suvandit Graafik.
    * Pange tähele, et mõlemad tööd lisatakse soovitud perioodi.  
    * Jaotises Perioodi võimsus saate vaadata iga perioodi koormust. Väli Tarbimine kuvab plaanitud tarbimise sellel perioodil. Kui plaanitud tarbimine selles perioodis on saadaolevast võimsusest suurem, valitakse ülekoormatud tarbimine.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]