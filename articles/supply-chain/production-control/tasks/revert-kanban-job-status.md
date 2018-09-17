--- 
title: "Kanban-töö oleku taastamine"
description: "Protseduur keskendub vale kanban-töö oleku ennistamisele."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 55d359232da5f3087b1e6baed182a20da09aeff7
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="revert-kanban-job-status"></a>Kanban-töö oleku taastamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Protseduur keskendub vale kanban-töö oleku ennistamisele. See on kasulik juhul, kui masinaoperaator uuendab vale tööd või määrab kogemata vale oleku. Selles protseduuris on kanban-töö kogemata registreeritud olekuga Ettevalmistatud, mistõttu olek ennistatakse. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. Protseduur on mõeldud tööde järelevaatajale või masinaoperaatorile, kes töötavad lean manufacturingil põhinevas ettevõttes.


## <a name="open-process-board-for-the-work-cell"></a>Avage tööraku protsessitahvel
1. Avage Protsessitööde kanban-tahvel.
2. Valige või sisestage väärtus väljal Töörakk.
    * Valige töörakk 1260.  

## <a name="prepare-kanban-job"></a>Kanban-töö ettevalmistamine
1. Klõpsake suvandit Valmista ette.
    * Kui te ei saa klõpsata suvandit Ettevalmistamine, kuna see on tuhm, kontrollige, kas valitud kanban-töö olek on plaanitud, mida näitab tühja kanbani ikoon. Kui ettevalmistamine nurjub, veenduge, et kõik komplekteerimislehel olevad materjalid oleksid saadaval.  
2. Valige loendis ettevalmistatud töö.
    * Valige esimene töö, mille äsja ette valmistasite.  
    * Pange tähele, et töö olek on Ettevalmistatud, mida tähistab kanbani ikoonil olev kolmnurk.  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a>Ettevalmistatud kanban-töö oleku ennistamine
1. Märkige loendis valitud rida.
    * Valige esimene töö, mille ette valmistasite.  
2. Klõpsake toimingupaanil suvandit Tootmine.
3. Klõpsake suvandit Oleku ennistamine.
    * Saate kasutada alternatiivset kanban-reeglit, kui on täidetud järgmised tingimused. - Täiendusstrateegia on mõlema reegli jaoks sama.  - Tootmisvoo versioon on mõlema reegli jaoks sama.  - Tarnitav toode on mõlema reegli jaoks sama.  - Kõik kanban-reeglite viimase tegevuse jaoks konfigureeritavad järgnevad tegevused peavad mõlema reegli jaoks olema samad.  - Mõlema reegli jaoks peavad olema konfigureeritud samad tarnitud varude dimensioonid.  - Materjali käsitlemisühiku olek peab olema Määramata.  - Sündmuse kanbanide konfiguratsioon peab olema sama.  
    * Kontrollige, kas uus olek on Plaanitud.  
4. Klõpsake nuppu OK.
5. Eemaldage loendis valitud realt märge.
    * Valige sama töö.  
    * Pange tähele, et ennistatakse kanban-töö olek Plaanitud, mida tähistab kanbani tühi ikoon.  


