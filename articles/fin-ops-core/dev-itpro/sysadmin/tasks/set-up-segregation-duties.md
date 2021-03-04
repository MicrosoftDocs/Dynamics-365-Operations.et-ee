---
title: Kohustuste jagamise seadistamine
description: Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad.
author: peakerbl
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57c7c436c91ab11404cac3ea056b028023a0617a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688169"
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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]