--- 
title: "Minimaalsete laovarude sündmuse abil kanban-reegli loomine"
description: "See protseduur keskendub seadistusele, mis on vajalik kanban-reegli loomiseks, kasutades minimaalset laosündmust tagamiseks, et konkreetne toode oleks alati konkreetses asukohas saadaval."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
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
ms.openlocfilehash: c655f9e2cb3967a44c357f16d18884ec0bc55357
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# Minimaalsete laovarude sündmuse abil kanban-reegli loomine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur keskendub seadistusele, mis on vajalik kanban-reegli loomiseks, kasutades minimaalset laosündmust tagamiseks, et konkreetne toode oleks alati konkreetses asukohas saadaval. Luuakse kanban-reegel materjali üleviimiseks asukohta, kui varude tase langeb alla 200 ühiku. Sidumissündmuse töötlemise käivitamisega luuakse vajalikud kanbanid. Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid. See toiming on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette uue või muudetud toote tootmist säästlikus keskkonnas.


## Looge uus kanban-reegel.
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

## Määrake kauba miinimumkogus
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

## Käivitage pakettsündmuse loomise töö
1. Avage Tootmise juhtimine > Perioodilised ülesanded > Kanban-töö pakktöötlus > Sidumissündmuse töötlemine.
2. Klõpsake nuppu OK.
3. Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.
4. Klõpsake loendis valitud real olevat linki.
    * Valige varem loodud kanban-reegel.  
5. Laiendage jaotist Kanbanid.
    * Pange tähele, et kanban loodi vajaliku materjali üleviimiseks lattu 12.  

