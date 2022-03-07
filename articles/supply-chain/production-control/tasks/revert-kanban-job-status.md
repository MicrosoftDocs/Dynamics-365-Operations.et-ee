---
title: Kanban-töö oleku taastamine
description: Protseduur keskendub vale kanban-töö oleku ennistamisele.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 771c3b95be05904c84483473a533c708964fbe62
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574397"
---
# <a name="revert-kanban-job-status"></a>Kanban-töö oleku taastamine

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]