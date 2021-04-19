---
title: Säästliku graafiku gruppide määratlemine
description: Säästliku graafiku grupid määratletakse toodete grupeerimiseks ja eristamiseks kanban-plaanimisel.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 647e721a0616ceae387322517f2955d75c06bfd2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828750"
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