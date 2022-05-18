---
title: Finantsdimensioonide määratlemine
description: Selles ülesandejuhendis selgitatakse üksuse tagatud finantsdimensiooni ja kohandatud finantsdimensiooni lisamist.
author: aprilolson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10a991938f68c0ade19999e48a02f032c92a6779
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716939"
---
# <a name="define-financial-dimensions"></a>Finantsdimensioonide määratlemine

[!include [banner](../../includes/banner.md)]

Selles ülesandejuhendis selgitatakse üksuse tagatud finantsdimensiooni ja kohandatud finantsdimensiooni lisamist. Juhendis kasutatakse demoettevõtte USMF andmeid.

## <a name="create-an-entity-backed-financial-dimension"></a>Üksuse tagatud finantsdimensiooni loomine
1. Avage **Navigatsioonipaan > Moodulid > Pearaamat > Kontoplaan > Dimensioonid > Finantsdimensioonid**.
2. Klõpsake valikut **Uus**.
3. Valige väljal **Kasutaja väärtuste vorm** süsteemi määratletud üksus, millele finantsdimensioon rajada. 
4. Sisestage väljale **Dimensiooni nimi** finantsdimensiooni kirjeldav väärtus. Nimi võib erineda süsteemi määratletud üksusest, kuid ei tohi sisaldada tühikuid ega erimärke.
5. Klõpsake käsku **Aktiveeri**. Finantsdimensiooni aktiveerimine värskendab tabelit finantsdimensiooni nimega ja eemaldab kustutatud dimensioonid. Dimensiooniväärtusi saate sisestada enne finantsdimensiooni aktiveerimist, kuid finantsdimensiooni ei saa kasutada enne, kui see on aktiveeritud.  
6. Klõpsake aktiveerimisteates suvandit **Sule**.
7. Klõpsake käsku **Aktiveeri**. Dimensiooni aktiveerimise saab planeerida partiiga käitamiseks kindlal kuupäeval ja kellaajal.  
8. Klõpsake **Toimingupaanil** valikut **Dimensiooniväärtused**. Mõned dimensiooniväärtused on ettevõttekohased. Saate nende ettevõttekohasust kontrollida, kui ettevõtte nimi kuvatakse dimensiooniväärtuste loendis.  

## <a name="create-a-custom-financial-dimension"></a>Kohanadtud finantsdimensiooni loomine
1. Klõpsake valikut **Uus**.
2. Valige väljal **Kasuta väärtusi allikast** suvand **Kohandatud dimensioon**.
3. Sisestage väljale **Dimensiooni nimi** finantsdimensiooni kirjeldav väärtus.
    - Nimi ei tohi sisaldada tühikuid ega erimärke.  
    - Samuti saate määrata kontomaski, et piirata dimensiooniväärtuste puhul sisestatava teabe hulka ja tüüpi.   
    - Saate sisestada märke, mis jäävad samaks igale dimensiooniväärtusele, näiteks tähti või sidekriipsu. Saate sisestada ka trelle (#) ning ja-märke (&) kohatäidetena tähtede ja numbrite jaoks, mis muutuvad iga kord, kui luuakse dimensiooniväärtus. Kasutage numbrimärki (#) kohatäitena numbrile ning ja-märki (&) kohatäitena tähele.  Näide. Dimensiooniväärtuse piiramiseks tähtedele CC ja kolmele arvule sisestage vormingumaskina CC-###.  
4. Klõpsake käsku **Aktiveeri**. Finantsdimensiooni aktiveerimine värskendab tabelit finantsdimensiooni nimega ja eemaldab kustutatud dimensioonid. Dimensiooniväärtusi saate sisestada enne finantsdimensiooni aktiveerimist, kuid finantsdimensiooni ei saa kasutada enne, kui see on aktiveeritud.     
5. Klõpsake käsku **Aktiveeri**. Dimensiooni aktiveerimise saab planeerida partiiga käitamiseks kindlal kuupäeval ja kellaajal.      
6. Klõpsake **Toimingupaanil** valikut **Dimensiooniväärtused**.
7. Klõpsake valikut **Uus**.
8. Sisestage väljale **Dimensiooni väärtus** oma finantsdimensiooni väärtust kirjeldav nimi.
9. Sisestage väljale **Kirjeldus** oma finantsdimensiooni väärtuse kirjeldus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
