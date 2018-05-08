--- 
title: "Alltöövõtu tööraku loomine - lean manufacturing"
description: "Lean manufacturing tööde alltööde mudeli loomiseks peate looma tööraku, mis on seostatud tööd pakkuva hankijaga."
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fc8dc0bc29c6bdb662c46808491abf5395f0be5d
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a>Alltöövõtu tööraku loomine - lean manufacturing

[!include [task guide banner](../../includes/task-guide-banner.md)]

Lean manufacturing tööde alltööde mudeli loomiseks peate looma tööraku, mis on seostatud tööd pakkuva hankijaga. Alltöövõtu töörakk on lingitud hankijaga läbi ressursi seostamise hankija tüübiga. Kui esitate selle salvestise USMF-i demoettevõttes, saate valida hankija konto ID 1002 ja saidi 1.


## <a name="create-a-vendor-resource"></a>Looge hankija ressurss
1. Avage Ressursid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Ressurss.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Valige väljal Tüüp valik Hankija.
6. Klõpsake väljal Hankija otsingu avamiseks ripploendi nuppu.

## <a name="create-the-resource-group"></a>Looge ressursigrupp
1. Avage Ressursigrupid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Ressursigrupp.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.
    * Valige sait, mille jaoks tuleb eraldada töörakk. Teoreetiliselt võib said esindada ühte saiti, mida haldab hankija. Siiski enamasti eraldatakse alltöövõturessursid ainult alltöövõtulepinguga tööd tellivale saidile. Pange tähele, et alltöövõtu töörakkude sisend- ja väljundlaod peavad olema samal saidil.  
6. Sisestage väärtus väljale Koht.
7. @SysTaskRecorder:_RequestClose
8. Valige või tühjendage märkeruut Töörakk.
9. Klõpsake väljal Sisestusladu otsingu avamiseks ripploendi nuppu.
    * Valige ladu ja asukoht, mida kasutatakse hankija hallatud tööraku materjalide jaoks. Paljudel juhtudel esitatakse ladu ja asukoht nii, et iga hankija jaoks kasutatakse erinevat ladu ja iga tööraku jaoks kasutatakse ühte asukohta.  
10. Klõpsake väljal Sisestuskoht otsingu avamiseks ripploendi nuppu.
11. Klõpsake väljal Väljastusladu otsingu avamiseks ripploendi nuppu.
    * Määrake ladu ja asukoht, kuhu materjal sisestatakse, kui sisestatakse tööraku alltöövõtu tegevused. Ladu ja asukoht võivad olla hankija saidil, kui hankija raporteerib kanban-tööd. Alternatiivina võivad ladu ja asukoht olla vastuvõtvas asukohas, mis on seostatud tootmisvoo järgmise etapiga.  
12. Klõpsake väljal Väljastuskoht otsingu avamiseks ripploendi nuppu.
13. Laiendage või ahendage jaotist Kalendrid.
14. Klõpsake vahekaarti Lisa.
15. Klõpsake väljal Kalender otsingu avamiseks ripploendi nuppu.
    * Seostage tööraku tööaja kalender ressursigrupiga. Kriitiliste ressursside puhul soovitame teil määrata konkreetsed kalendrid, mis kujutavad tööraku või hankija saidi täpseid tööaegasid ja seotud võimekusi.  
16. Laiendage või ahendage jaotist Ressursid.
17. Klõpsake vahekaarti Lisa.
    * Alltöövõtu ressursigrupil peab olema vastava hankijatüübi seostatud ressurss, mis lingib ressursigrupi hankija kontoga.  
18. Klõpsake väljal Ressurss otsingu avamiseks ripploendi nuppu.
    * Valige või sisestage hankijaressurss, mille olete loonud eelmises alamülesandes.  
19. Laiendage või ahendage jaotist Tööraku võimsus.
20. Klõpsake vahekaarti Lisa.
    * Töörakul peab olema määratletud võimsus. Selles näites loome läbilaskevõime 100 ühikut standardse tööpäeva kohta.  
21. Klõpsake väljal Tootmisvoo mudel otsingu avamiseks ripploendi nuppu.
22. Valige suvand väljalt Võimsuse periood.
23. Sisestage number väljale Keskmine läbilaskekogus.
24. Klõpsake väljal Ühik otsingu avamiseks ripploendi nuppu.
25. Ühiku toiming ResolveChanges.


