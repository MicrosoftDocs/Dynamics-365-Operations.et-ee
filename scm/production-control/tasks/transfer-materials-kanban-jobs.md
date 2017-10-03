--- 
title: "Kanban-töödega materjalide ülekandmine (ainult veebruar 2016)"
description: "See protseduur keskendub tagastamise kanban-tööle materjalide ülekandeks."
author: ChristianRytt
manager: AnnBe
ms.date: 02/07/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 72403aa502cadf2a727bdd67ad8cd612dafd502b
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="transfer-materials-with-kanban-jobs-february-2016-only"></a>Kanban-töödega materjalide ülekandmine (ainult veebruar 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur keskendub tagastamise kanban-tööle materjalide ülekandeks. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See protseduur on mõeldud laotöötajale.


## <a name="display-transfer-jobs"></a>Ülekandetööde kuvamine
1. Avage Tootmise juhtimine > Kanban > Ülekandetööde kanban-tahvel.
2. Laiendage või ahendage jaotist Filtrid.
    * Jaotises Filtrid saate määrata, milliseid töid soovite kuvada, filtrides suvandid Tootmisvoog, Tegevuse nimi, Lähteladu ja -asukoht ning Sihtladu ja -asukoht.  
3. Sisestage väljale Laost väärtus 11.
4. Sisestage väljale Asukohta väärtus 12.

## <a name="start-a-transfer-job"></a>Käivita ülekandmistöö
1. Tühistage loendis olemasolul valitud rea valik.
2. Valige loendist rida 4.
    * Valige esimene töö, mille olek on Plaanimata. Veenduge, et valitud on ainult see töö.  
3. Klõpsake nuppu Käivita.
    * Pange tähele, et ikoon näitab, et tööd on alustatud.  

## <a name="select-a-second-transfer-job-and-change-quantity"></a>Teise ülekandetöö valimine ja koguse muutmine
1. Otsige loendist ja valige soovitud kirje.
    * Teil võib olla valitud mitu tööd, kuid praegu valige 5. rida.  
2. Otsige loendist ja valige soovitud kirje.
    * Veenduge, et valitud oleks ainult eelmises etapis olev töö. Tühistage kõikide muude tööde valik.  
3. Märkige väljal Töö kogus olev väärtus edasiseks viiteks üles
4. Määrake töö koguseks 30.
    * Pange tähele hoiatust! Teil pole lubatud üle kanda rohkem kui 30. Kanban-reegli seadistuse järgi saate üle kanda ainult algse koguse.  
5. Kasutage varem väljal Töö kogus märgitud väärtust
    * Seadistage Töö kogus eelmisele väärtusele.  

## <a name="start-the-second-transfer-job"></a>Teise ülekandetöö alustamine
1. Klõpsake nuppu Käivita.
    * See käivitab 5. reas oleva töö ülekande.  

## <a name="complete-both-transfer-jobs"></a>Mõlema ülekandetöö lõpetamine
1. Valige loendist rida 4.
    * Nüüd on 4. ja 5. real valitud kaks ülekandetööd.  
2. Klõpsake valikut Valmis.
    * See lõpetab mõlema töö ülekande.  


