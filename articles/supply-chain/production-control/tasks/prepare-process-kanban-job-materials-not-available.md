---
title: Protsessi kanban-töö ettevalmistamine, kui materjalid pole tööraku jaoks saadaval
description: See protseduur keskendub protsessi kanban-töö ettevalmistamisele, kui mõned materjalid pole tööraku puhul saadaval, mistõttu tuleb materjalid laost komplekteerida.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df0396a1d00e61ad82e52fc07779e239cd811ab8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994087"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>Protsessi kanban-töö ettevalmistamine, kui materjalid pole tööraku jaoks saadaval

[!include [banner](../../includes/banner.md)]

See protseduur keskendub protsessi kanban-töö ettevalmistamisele, kui mõned materjalid pole tööraku puhul saadaval, mistõttu tuleb materjalid laost komplekteerida. Protseduur Protsessi kanban-töö ettevalmistamine materjalide mittesaadavusel on selle protseduuri loomise eeltingimus. See protseduur on mõeldud masinaoperaatorile. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.

1. Avage Tootmise juhtimine > Kanban > Protsessitööde kanban-tahvel.
2. Klõpsake väljal Töörakk otsingu avamiseks ripploendi nuppu.
3. Klõpsake loendis valitud real olevat linki.
    * Valige töörakk 1250.  
4. Otsige loendist ja valige soovitud kirje.
    * Valige Kanban 000356.  
5. Otsige loendist ja valige soovitud kirje.
    * Tühistage loendis rea 4 valik. või valige rida 4, kui te pole lõpetanud ülesannet „Protsessi kanban-töö ettevalmistamine materjalide saadavusel“.  
6. Laiendage jaotist Komplekteerimisleht.
    * Kirje puudumise ikoon tarne olekus näitab, et kauba P0002 rida 48 puudub tööraku puhul.  

## <a name="transfer-materials-to-work-cell"></a>Materjalide ülekanne töörakku
1. Laiendage jaotist Ülekandetööd.
2. Kasutage kiirfiltrit, et filtreerida väli Kaubakood väärtuse P0002 alusel.
3. Otsige loendist ja valige soovitud kirje.
4. Klõpsake nuppu Käivita.
    * Edastamine on pooleli.  
5. Klõpsake valikut Valmis.
    * Kaup P0002 on nüüd kanban-töö puhul komplekteerimislehel saadaval. See tähendab, et saame kanbani koos kõigi vajalike materjalidega ette valmistada.  
6. Klõpsake suvandit Valmista ette.
    * Pange tähele, et töö oleku ikoon näitab, et töö on nüüd valmis.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]