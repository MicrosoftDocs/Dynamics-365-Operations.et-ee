---
title: Kohustuste jagamise seadistamine
description: Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47747cba7f83d0b43a284750cff232824e00053a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982402"
---
# <a name="set-up-segregation-of-duties"></a>Kohustuste jagamise seadistamine

[!include [banner](../../includes/banner.md)]

Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad. Seda põhimõtet nimetatakse kohustuste jagamiseks. Näiteks ei soovi te võib-olla, et sama isik kinnitab kaupade kättesaamise ja töötleb hankijale tehtavat makset. Kohustuste jagamine aitab vähendada pettuseriski ja tuvastada vigu või ebaregulaarsusi. Samuti saate kohustuste jagamise abil jõustada sisekontrollipoliitikaid. Reegli loomiseks järgige järgmist protseduuri. Protseduuri lõpuleviimiseks peate olema süsteemiadministraator. Selle protseduuri loomiseks kasutati demoettevõtte DAT andmeid. 

1. Avage **Navigeerimispaan > Moodulid > Süsteemiadministratsioon > Turvalisus > Kohustuste jagamine > Kohustuste reeglite jagamine**.
2. Klõpsake valikut **Uus**.
3. Tippige reegli väärtus väljale **Nimi**.
4. Väljal **Esimene kohustus**, klõpsake otsingu avamiseks ripploendi nuppu.
5. Otsige loendist ja valige soovitud kirje. Valige esimene kohustus, mida juhitakse reegliga.
6. Väljal **Teine kohustus**, klõpsake otsingu avamiseks ripploendi nuppu. 
7. Otsige loendist ja valige soovitud kirje. Valige teine kohustus, mida juhitakse reegliga.
10. Valige suvand väljal **Olulisusaste**. Valige riski, mis tekib, kui sama kasutaja või roll täidab mõlemat kohustust, olulisusaste.  
11. Sisestage väärtus väljale **Turberisk**. Sisestage turberiski kirjeldus.  
12. Sisestage väärtus väljale **Turberiski vähendamine**. Sisestage turberiski vähendamiseks kasutatavate tegevuste kirjeldus. Näiteks saate riski vähendamiseks teha protsessi kohta üksikasjalikumaid ülevaateid, teha igakuise juhtiva ülevaatuse või jagada ressursse teiste osakondadega.     
13. Klõpsake valikut **Salvesta**.

