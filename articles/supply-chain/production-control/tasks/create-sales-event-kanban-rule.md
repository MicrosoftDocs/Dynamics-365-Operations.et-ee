---
title: Müügisündmuse kanban-reegli loomine
description: See protseduur keskendub müügitellimuse loomise ajal käivitatava kanban-reegli loomiseks vajalikule seadistusele.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3cd2b579e542b9f905fc51b63f2120e5a5c883ae
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566643"
---
# <a name="create-a-sales-event-kanban-rule"></a>Müügisündmuse kanban-reegli loomine

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]