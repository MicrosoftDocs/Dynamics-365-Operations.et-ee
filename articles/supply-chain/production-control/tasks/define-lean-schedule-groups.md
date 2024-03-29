---
title: Säästliku graafiku gruppide määratlemine
description: Säästliku graafiku grupid määratletakse toodete grupeerimiseks ja eristamiseks kanban-plaanimisel.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9d16c0d3192773c32c8dcc57a430607c6b60f97
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574445"
---
# <a name="define-lean-schedule-groups"></a>Säästliku graafiku gruppide määratlemine

[!include [banner](../../includes/banner.md)]

Säästliku graafiku grupid määratletakse toodete grupeerimiseks ja eristamiseks kanban-plaanimisel. Grupeerimine võib toimuda üldise seosena ettevõtte kohta või tööraku põhiselt. Igale grupile määratakse kanban-plaanimise loendilehel visuaalseks tähistamiseks värvikood. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="define-lean-scheduling-group"></a>Säästliku plaanimise grupi määratlemine
1. Avage Tooteteabe haldus > Lean manufacturing > Säästliku graafiku grupid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Graafikugrupp.
    * Graafikugruppi saab määratleda üldise grupina või töörakupõhise grupina. Selles lihtsas näites määratleme üldise grupi ja töörakk jääb tühjaks. Selle grupi sätted kehtivad kõigi töörakkude puhul, millel pole konkreetseid graafikugruppe.  
4. Valige värvivalikust värv.
    * Värve kasutatakse tööde esiletõstmiseks kanban-graafiku loendilehel või kanban-protsessi tahvlil.  
5. Märkige loendis valitud rida.
6. Klõpsake loendis valitud real olevat linki.

## <a name="associate-product"></a>Toote seostamine
1. Konkreetse toote seostamine
    * Toodete seostamiseks säästliku graafiku gruppidega on kaks võimalust: kas konkreetse tootena (kauba seose tüüp = kaup) või kauba eraldamisvõtme osana (kauba seose tüüp = grupp).    
2. Valige Kaup väljalt Kauba seose tüüp.
3. Sisestage väärtus väljale Kaubakood.
4. Sisestage number väljale Läbilaskemäär.
    * Läbilaskemäär on vaikimisi 1, mis tähendab, et seotud tooted tarbivad täpselt nii palju võimsust, kui on määratud tootmisvoogude protsessitoimingutes. Läbilaskemäär >1 määratleb suurema ressursitarbimise, Läbilaskemäär <1 määratleb väiksema ressursitarbimise. Suhtarvu kasutatakse kuluarvestuses ja kanban-töö tarbimise arvestuses.  

## <a name="associate-item-allocation-key"></a>Kauba eraldamisvõtme seostamine
1. Kauba eraldamisvõtme seostamine
    * Lisage kauba eraldamisvõtmele seos, kasutades kauba seose tüübi gruppi.   Pange tähele, et selle protsessi puhul on vaja teie andmetes määratletud eelarvekauba eraldamisvõtit.  
2. Valige Grupp väljalt Kauba seose tüüp.
3. Klõpsake väljal Kauba eraldamisvõti otsingu avamiseks ripploendi nuppu.
4. Klõpsake loendis valitud real olevat linki.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]