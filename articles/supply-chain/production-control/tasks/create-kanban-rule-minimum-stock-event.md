---
title: Minimaalsete laovarude sündmuse abil kanban-reegli loomine
description: See protseduur keskendub seadistusele, mis on vajalik kanban-reegli loomiseks, kasutades minimaalset laosündmust tagamiseks, et konkreetne toode oleks alati konkreetses asukohas saadaval.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b295000e132b8551045520df1af55a37673f131d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425979"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a>Minimaalsete laovarude sündmuse abil kanban-reegli loomine

[!include [banner](../../includes/banner.md)]

See protseduur keskendub seadistusele, mis on vajalik kanban-reegli loomiseks, kasutades minimaalset laosündmust tagamiseks, et konkreetne toode oleks alati konkreetses asukohas saadaval. Luuakse kanban-reegel materjali üleviimiseks asukohta, kui varude tase langeb alla 200 ühiku. Sidumissündmuse töötlemise käivitamisega luuakse vajalikud kanbanid. Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid. See toiming on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist säästlikus keskkonnas.


## <a name="create-a-new-kanban-rule"></a>Looge uus kanban-reegel.
1. Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.
2. Klõpsake valikut Uus.
3. Tehke väljal Tüüp vali Tühistamine.
    * Seda tüüpi kasutatakse ülekande-kanbanide loomiseks.  
4. Valige väljal Täiendusstrateegia suvand Sündmus.
    * Sündmusel põhinevate kanbanide ülekandmise loomiseks kasutatakse sündmuse strateegiat. Edaspidi käivitate protseduuris üleviimise kanbanid, kasutades varude täiendamist.  
5. Sisestage või valige väärtus väljal Esimene plaanitegevus.
    * Sisestage või valige väärtus ReplenishSpeakerComponents. Sellel ülekandmistegevusel on sissetulev (väljund) ladu ja asukoht 12, mis tähendab, et materjalid teisaldatakse asukohta 12 laos 12.  
6. Laiendage jaotist Üksikasjad.
7. Sisestage või valige väärtus väljal Toode.
    * Valige suvand M0007.  
8. Laiendage jaotist Sündmused.
9. Valige väljalt Varude täiendamise sündmus väärtus Partii.
    * See loob kanbanid materjalivajaduste rahuldamiseks seotud asukohas sidumissündmuse töötlemise ajal.  

## <a name="set-the-minimum-quantity-for-the-item"></a>Määrake kauba miinimumkogus
1. Klõpsake, et järgida linki väljal Toode.
2. Klõpsake, et järgida linki väljal Kaubakood.
3. Laiendage toote pildi kiirinfot.
4. Klõpsake toimingupaanil valikut Plaan.
5. Klõpsake valikut Kauba laovarud.
6. Klõpsake valikut Uus.
7. Märkige loendis valitud rida.
8. Sisestage või valige väärtus väljal Ladu.
    * Valige välja Ladu väärtuseks 12.  
9. Määra valiku Miinimum väärtuseks 200.

## <a name="run-the-batch-event-creation-job"></a>Käivitage pakettsündmuse loomise töö
1. Avage Tootmise juhtimine > Perioodilised ülesanded > Kanban-töö pakktöötlus > Sidumissündmuse töötlemine.
2. Klõpsake nuppu OK.
3. Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.
4. Klõpsake loendis valitud real olevat linki.
    * Valige varem loodud kanban-reegel.  
5. Laiendage jaotist Kanbanid.
    * Pange tähele, et kanban loodi vajaliku materjali üleviimiseks lattu 12.  

