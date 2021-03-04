---
title: Kanban-töödega materjalide ülekandmine
description: See protseduur keskendub tagastamise kanban-tööle materjalide ülekandeks.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 96cb77b7b37fe6519a812735d9a41749da078cf2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426359"
---
# <a name="transfer-materials-with-kanban-jobs"></a>Kanban-töödega materjalide ülekandmine

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]