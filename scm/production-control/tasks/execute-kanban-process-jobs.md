--- 
title: "Kanbani protsessitööde käivitamine"
description: "See protseduur keskendub kanbani protsessitööde käivitamisele."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 50b5048a5f9277c47444fa69d2c8cc8e36ba7dcd
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="execute-kanban-process-jobs"></a>Kanbani protsessitööde käivitamine

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


