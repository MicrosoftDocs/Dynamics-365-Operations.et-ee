--- 
title: Kohustuste jagamise seadistamine
description: "Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad."
author: maertenm
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 754f28cd2831d8a9a57c408518d240de460b732b
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-segregation-of-duties"></a>Kohustuste jagamise seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad. Seda põhimõtet nimetatakse kohustuste jagamiseks. Näiteks ei soovi te võib-olla, et sama isik kinnitab kaupade kättesaamise ja töötleb hankijale tehtavat makset. Kohustuste jagamine aitab vähendada pettuseriski ja tuvastada vigu või ebaregulaarsusi. Samuti saate kohustuste jagamise abil jõustada sisekontrollipoliitikaid. Reegli loomiseks järgige järgmist protseduuri. Protseduuri lõpuleviimiseks peate olema süsteemiadministraator. Selle protseduuri loomiseks kasutati demoettevõtte DAT andmeid. 

1. Avage Süsteemihaldus > Turve > Kohustuste jagamine > Kohustuste jagamise reeglid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
    * Sisestage reegli nimi.  
4. Klõpsake väljal Esimene kohustus otsingu avamiseks ripploendi nuppu.
5. Otsige loendist ja valige soovitud kirje.
    * Valige esimene kohustus, mida juhitakse reegliga.  
6. Klõpsake loendis valitud real olevat linki.
7. Klõpsake väljal Teine kohustus otsingu avamiseks ripploendi nuppu.
8. Otsige loendist ja valige soovitud kirje.
    * Valige teine kohustus, mida juhitakse reegliga.  
9. Klõpsake loendis valitud real olevat linki.
10. Valige suvand väljal Olulisusaste.
    * Valige riski, mis tekib, kui sama kasutaja või roll täidab mõlemat kohustust, olulisusaste.  
11. Sisestage väärtus väljale Turberisk.
    * Sisestage turberiski kirjeldus.  
12. Sisestage väärtus väljale Turbe vähendamine.
    * Sisestage turberiski vähendamiseks kasutatavate tegevuste kirjeldus. Näiteks saate riski vähendamiseks teha protsessi kohta üksikasjalikumaid ülevaateid, teha igakuise juhtiva ülevaatuse või jagada ressursse teiste osakondadega.  
13. Klõpsake nuppu Salvesta.


