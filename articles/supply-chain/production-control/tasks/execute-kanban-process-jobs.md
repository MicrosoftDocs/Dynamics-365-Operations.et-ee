---
title: Kanbani protsessitööde käivitamine
description: See protseduur keskendub kanbani protsessitööde käivitamisele.
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
ms.openlocfilehash: 7ac6f0f6139fe17532f6fbd996b314e0b14f3d90
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566575"
---
# <a name="execute-kanban-process-jobs"></a>Kanbani protsessitööde käivitamine

[!include [banner](../../includes/banner.md)]

See protseduur keskendub kanbani protsessitööde käivitamisele. Esimene töö on lõpule viidud eeldatava kogusega ja tõrkeid ei ole. Teine töö on lõpule viidud tõrgetega. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See protseduur on mõeldud masinaoperaatorile.


## <a name="select-a-kanban-job"></a>Kanban-töö valimine
1. Avage Tootmise juhtimine > Kanban > Protsessitööde kanban-tahvel.
2. Klõpsake väljal Töörakk otsingu avamiseks ripploendi nuppu.
3. Klõpsake rida ressursigrupiga 1250. See filtreerib tööde loendit, nii et see kuvab ainult tööraku 1250 tööd.
    * Märkige rida, millel on olek Plaanitud töö.  

## <a name="complete-a-job-with-expected-quantity"></a>Töö lõpuleviimine eeldatud kogusega
1. Laiendage või ahendage jaotist Üksikasjad.
    * Selles jaotises kuvatakse tähtsat teavet kaardi numbri, kaubakoodi, tellitud koguse ja tegevuse nime kohta.  
2. Laiendage või ahendage jaotist Tootmisjuhendid.
    * Selles jaotises kuvatakse tegevuse tootmise juhised. Juhised võivad olla tekst, pildid, joonistused ja muud dokumendid.  
3. Klõpsake nuppu Käivita.
    * Valige töö, mis ei ole lõpule viidud. Töö oleku vaatamiseks kasutage väljal Töö olek olevaid olekuikoone.      
4. Klõpsake valikut Valmis.
    * Töö on lõpule viidud eeldatud kvaliteediga.  

## <a name="complete-a-job-with-errors"></a>Töö lõpuleviimine tõrgetega
1. Klõpsake nuppu Käivita.
    * Kui töö on lõpule viidud, valitakse automaatselt järgmine töö loendist. Sellepärast ei pea te valima tööd enne nupu Start klõpsamist.  
2. Klõpsake toimingupaanil suvandit Tootmine.
3. Klõpsake käsku Lõpeta (üksikasjad).
4. Märkige loendis valitud rida.
5. Sisestage väljale Tõrgete kogus number.
6. Sisestage number väljale Hea kogus.
7. Klõpsake nuppu OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]