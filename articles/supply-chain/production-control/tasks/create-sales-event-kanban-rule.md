--- 
title: "Müügisündmuse kanban-reegli loomine"
description: "See protseduur keskendub müügitellimuse loomise ajal käivitatava kanban-reegli loomiseks vajalikule seadistusele."
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f1f66157b2e74ad1b490e10112cbc121ac9826fb
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-sales-event-kanban-rule"></a>Müügisündmuse kanban-reegli loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur keskendub müügitellimuse loomise ajal käivitatava kanban-reegli loomiseks vajalikule seadistusele. Sündmuse kanban-reegel täiendab müügitellimuse ridadelt pärinevaid nõudeid. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. See on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist.




## <a name="create-a-new-kanban-rule"></a>Looge uus kanban-reegel.
1. Minge jaotisse Kanban-reeglid.
2. Klõpsake valikut Uus.
3. Valige väljal Täiendusstrateegia suvand Sündmus.
    * Suvandi Sündmus valimine tähendab, et kanban-reegli käivitab sündmus, näiteks müügitellimuse rea loomine.   Seda rakendatakse aladele, kus iga kanban peaks hõlmama kindlat nõudlust.  
4. Sisestage või valige väärtus väljal Esimene plaanitegevus.
    * Valige suvand Lõplik assembler.  
5. Laiendage jaotist Üksikasjad.
6. Sisestage või valige väärtus väljal Toode.
    * Valige suvand L0050.  

## <a name="define-an-event"></a>Sündmuse määratlemine
1. Laiendage jaotist Sündmused.
2. Valige väljal Müügisündmus suvand Automaatne.
    * Kui valite müügisündmuse sätteks Automaatne, käivitatakse see kanban-reegel automaatselt, kui müügirida ühtib toote ja vastuvõtukohaga. Selle protseduuris on see toode L0050 laos 13.  
3. Valige välja Sündmuste miinimumkogus väärtuseks 50.
    * Kui sündmuse miinimumkogus on 50, käivitatakse kanban-reegel ainult sündmustega, mille kogus on vähemalt 50.  
4. Laiendage jaotist Tootmisvoog.
    * Pange tähele, et vastuvõtukoht on ladu 13. See tähendab, et see kanban-reegel käivitatakse selle asukoha puhul.  
    * Selles näites käivitab selle kanban-reegli müügirida tootele L0050, mille kogus on vähemalt 50, laos 13.  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>Müügirea loomine sündmuse kanban-reegli loomiseks
1. Avage Kõik müügitellimused.
    * Kanban-reegli salvestamisel kuvatakse hoiatus, mis tähendab, et kanbanid luuakse müügitellimuse loomisel reaalajas.  
2. Klõpsake valikut Uus.
3. Valige või sisestage väärtus väljal Kliendi konto.
    * Valige näiteks US-003.  
4. Klõpsake nuppu OK.
5. Sisestage väljale Kaubakood tüüp L0050.
6. Sisestage väljale Tegevuskoht väärtus 1.
    * Valige tegevuskoht 1, kuna ladu 13 asub tegevuskohas 1.  
7. Sisestage või valige väärtus väljal Ladu.
    * Valige välja Ladu väärtuseks 13.  
8. Määrake koguse väärtuseks 75.
    * Loodud kanban-reegli käivitamiseks sisestage koguseks vähemalt 50.  

## <a name="verify-that-kanban-is-created"></a>Kontrollimine, kas kanban on loodud
1. Klõpsake valikut Toode ja tarnimine.
2. Klõpsake suvandit Kuva sidumispuu.
    * Pange tähele, et luuakse kanban, mille kogus on sama mis müügireal. Samuti näete toote L0050 tootmiseks vajalikke materjaliväljastusi. See on selle protseduuri viimane etapp.  


