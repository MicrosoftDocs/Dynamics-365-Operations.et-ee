---
title: Kanban-rea sündmuse abil kanban-reegli loomine
description: See protseduur loob kanban-reegli, kasutades kanban-rea sündmuste seadistust protsessitegevusest tõmbamise käivitamiseks.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7aaf959db0f0a136fc615f9a57ec787ef6cf2ad
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579156"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a>Kanban-rea sündmuse abil kanban-reegli loomine

[!include [banner](../../includes/banner.md)]

See protseduur loob kanban-reegli, kasutades kanban-rea sündmuste seadistust protsessitegevusest tõmbamise käivitamiseks. Kanban-reegli käivitab kanban-protsessi tegevus, mille kogus on kummagi puhul vähemalt 25. Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid. See toiming on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist säästlikus keskkonnas.


## <a name="create-a-kanban-rule"></a>Kanban-reegli loomine
1. Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.
2. Klõpsake valikut Uus.
3. Valige väljal Täiendusstrateegia suvand Sündmus.
    * See loob kanbanid otse nõudlusest. Seda kasutatakse tellimuse järgi tegemise stsenaariumeid määratlevate reeglite seadistamiseks.  
4. Sisestage või valige väärtus väljal Esimene plaanitegevus.
    * Sisestage või valige SpeakerAssemblyAndPolish. Tootmise kanban-reegli esimene tegevus on protsessitegevus tootmisvoos. Tegevuse valimisel kopeeritakse selle kehtivuskuupäevade kanban-reegli kehtivuse kuupäevadele.  
5. Laiendage jaotist Üksikasjad.
6. Sisestage väljale Toode väärtus L0001.
7. Laiendage jaotist Sündmused.
8. Valige väljal Kanban-rea sündmus väärtus Automaatne.
    * See loob nõudmisel sündmuse kanbanid.  Selle välja abil saate konfigureerida kanban-reeglid, mis täiendavad järgmiste protsessitegevuste jaoks vajalikku materjali. Valiku Automaatne korral luuakse koos nõudlusega sündmuse kanbanid. See säte on soovitatav kui plaanite viia tootmise läbi samal päeval.  
9. Valige välja Sündmuste miinimumkogus väärtuseks 25.
    * Sündmuse kanbanid luuakse, kui nõudluse kogus on selle välja väärtusega võrdne või sellest suurem. Sellest on kasu, kui soovite toota ühel masinal sellest väljast väiksema tellimuse koguse ja teisel masinal sellest väljast suurema koguse.  
10. Klõpsake nuppu Salvesta.

## <a name="create-sales-order-and-trigger-kanban-chain"></a>Müügitellimuse loomine ja kanban-ahela käivitamine
1. Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Valige või sisestage väärtus väljal Kliendi konto.
    * Valige kliendikood US-003, metsa hulgimüük.  
4. Klõpsake nuppu OK.
5. Sisestage väljale Kaubakood tüüp L0001.
    * L0001 on kaup, millele kanban-reegli lõite.  
6. Määrake koguse väärtuseks 27.
    * Kuna 27 on suurem kui kanban-reegli miinimumkogus 25, käivitab see sündmuse kanbani.  
7. Sisestage väljale Tegevuskoht väärtus 1.
8. Sisestage või valige väärtus väljal Ladu.
    * Valige ladu 13.  
9. Klõpsake nuppu Salvesta.

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a>Kanban-reegliga loodud kanbani kuvamine
1. Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.
2. Otsige loendist ja valige soovitud kirje.
3. Laiendage jaotist Kanbanid.
    * Pange tähele, et 27 jaoks loodi kanban selleks, et töödelda loodud kanban-reeglil põhinevat tegevust.  
    * See on viimane etapp.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]