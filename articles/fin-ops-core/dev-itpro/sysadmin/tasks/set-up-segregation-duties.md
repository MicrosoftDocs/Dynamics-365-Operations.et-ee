---
title: Kohustuste jagamise seadistamine
description: Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c06ce9325d7b0894ba53d6b9782f495a48280d45e538b048d883ab86f05dabf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755744"
---
# <a name="set-up-segregation-of-duties"></a>Kohustuste jagamise seadistamine

[!include [banner](../../includes/banner.md)]

Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad. Seda põhimõtet nimetatakse kohustuste jagamiseks. Näiteks ei soovi te võib-olla, et sama isik kinnitaks kaupade kättesaamise ja töötleks hankijale tehtavat makset. Kohustuste jagamine aitab vähendada pettuseriski ja tuvastada vigu või ebaregulaarsusi. Samuti saate kohustuste jagamise abil jõustada sisekontrollipoliitikaid. Reegli loomiseks järgige järgmist protseduuri. Protseduuri lõpuleviimiseks peate olema süsteemiadministraator.

1. Avage **Süsteemihaldus** > **Turve** > **Kohustuste jagamine** > **Kohustuste jagamise reeglid**.
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

> [!IMPORTANT] 
> Kohustuste jagamise reeglite järgimist ei kontrollita, kui loote reegli. Saate luua reegli, mis loob olemasolevatele rollidele vastuolu. Olemasolevad kasutajarolli määramised võivad olla vastuolus ka uue reegliga. Vastavust peate kontrollima pärast reegli loomist või muutmist. Lisateavet vt [Kohustuste jagamise konfliktide tuvastamine ja lahendamine](identify-resolve-conflicts-segregation-duties.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]