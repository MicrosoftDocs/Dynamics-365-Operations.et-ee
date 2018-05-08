--- 
title: "Finantsdimensioonide määratlemine"
description: "Selles ülesandejuhendis selgitatakse üksuse tagatud finantsdimensiooni ja kohandatud finantsdimensiooni lisamist."
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0b72acf763f0f6dbc64c3e00986bc9eb0e366bb5
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="define-financial-dimensions"></a>Finantsdimensioonide määratlemine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles ülesandejuhendis selgitatakse üksuse tagatud finantsdimensiooni ja kohandatud finantsdimensiooni lisamist.  Juhendis kasutatakse demoettevõtte USMF andmeid.


## <a name="create-an-entity-backed-financial-dimension"></a>Üksuse tagatud finantsdimensiooni loomine
1. Avage Pearaamat > Kontoplaan > Dimensioonid > Finantsdimensioonid.
2. Klõpsake valikut Uus.
3. Valige väljal Kasutaja väärtused süsteemi määratletud üksus, millele finantsdimensioon rajada. 
4. Sisestage väljale Dimensiooni nimi finantsdimensiooni kirjeldav väärtus.
    * Nimi võib erineda süsteemi määratletud üksusest, kuid ei tohi sisaldada tühikuid ega erimärke.  
5. Klõpsake käsku Aktiveeri.
    * Finantsdimensiooni aktiveerimine värskendab tabelit finantsdimensiooni nimega ja eemaldab kustutatud dimensioonid. Dimensiooniväärtusi saate sisestada enne finantsdimensiooni aktiveerimist, kuid finantsdimensiooni ei saa kasutada enne, kui see on aktiveeritud.  
6. Klõpsake aktiveerimisteates suvandit Sule.
7. Klõpsake käsku Aktiveeri.
    * Dimensiooni aktiveerimise saab planeerida partiiga käitamiseks kindlal kuupäeval ja kellaajal.  
8. Klõpsake suvandit Dimensiooniväärtused.
    * Mõned dimensiooniväärtused on ettevõttekohased. Saate nende ettevõttekohasust kontrollida, kui ettevõtte nimi kuvatakse dimensiooniväärtuste loendis.  

## <a name="create-a-custom-financial-dimension"></a>Kohanadtud finantsdimensiooni loomine
1. Sulgege leht.
2. Klõpsake valikut Uus.
3. Väljal Kasuta väärtusi valige suvand <Custom dimension> (kohandatud dimensioon).
4. Sisestage väljale Dimensiooni nimi finantsdimensiooni kirjeldav väärtus.
    * Nimi ei tohi sisaldada tühikuid ega erimärke.  
    * Samuti saate määrata kontomaski, et piirata dimensiooniväärtuste puhul sisestatava teabe hulka ja tüüpi.   
    * Saate sisestada märke, mis jäävad samaks igale dimensiooniväärtusele, näiteks tähti või sidekriipsu. Saate sisestada ka trelle (#) ning ja-märke (&) kohatäidetena tähtede ja numbrite jaoks, mis muutuvad iga kord, kui luuakse dimensiooniväärtus. Kasutage numbrimärki (#) kohatäitena numbrile ning ja-märki (&) kohatäitena tähele.  Näide. Dimensiooniväärtuse piiramiseks tähtedele CC ja kolmele arvule sisestage vormingumaskina CC-###.  
5. Klõpsake käsku Aktiveeri.
    * Finantsdimensiooni aktiveerimine värskendab tabelit finantsdimensiooni nimega ja eemaldab kustutatud dimensioonid. Dimensiooniväärtusi saate sisestada enne finantsdimensiooni aktiveerimist, kuid finantsdimensiooni ei saa kasutada enne, kui see on aktiveeritud.  
6. Klõpsake käsku Aktiveeri.
    * Dimensiooni aktiveerimise saab planeerida partiiga käitamiseks kindlal kuupäeval ja kellaajal.  
7. Klõpsake suvandit Dimensiooniväärtused.
8. Klõpsake valikut Uus.
9. Sisestage väljale Dimensiooni väärtus oma finantsdimensiooni väärtust kirjeldav nimi.
10. Sisestage väljale Kirjeldus oma finantsdimensiooni väärtuse kirjeldus.


