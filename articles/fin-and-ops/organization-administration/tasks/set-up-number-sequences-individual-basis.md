--- 
title: Eraldi numbriseeriate seadistamine
description: "Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmetele ja kandekirjetele, mis neid nõuavad."
author: sericks007
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5c63022586f24cc1a50f7734910f15b237d35216
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Eraldi numbriseeriate seadistamine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmetele ja kandekirjetele, mis neid nõuavad. Koondandmeid või kandekirjet, mis nõuavad identifikaatorit, nimetatakse viiteks. Enne kui saate viite jaoks uusi kirjeid luua, peate seadistama numbriseeria ja selle viitega siduma. Saate seadistada kõik vajalikud numbriseeriad korraga, kasutades viisardit Seadista numbriseeriad, või saate luua või muuta üksikuid numbriseeriad lehe Numbriseeriad abil.

1. Avage Organisatsiooni haldus > Numbriseeriad > Numbriseeriad.
2. Klõpsake suvandit Nnumbriseeria.
3. Tippige väärtus väljale Numbriseeria kood.
4. Sisestage väärtus väljale Nimi.
5. Laiendage jaotist Ulatuse parameetrid.
    * Kiirkaardil Ulatuse parameetrid valige numbriseeria ulatus ja valige ulatuse väärtused.     Ulatus määratleb, millised organisatsioonid kasutavad numbriseeriat. Numbriseeriatel, mille ulatus on muu kui Ühiskasutuses, võivad olla segmendid, mis vastavad nende ulatusele. Näiteks numbriseeria, mille ulatus on Juriidiline isik, võib sisaldada juriidilise isiku segmenti. Lisateavet ulatuste kohta leiate teemast "Numbriseeriate ülevaade".  
6. Laiendage jaotist Segmendid.
    * Kiirkaardil Segmendid määratlege numbriseeria vorming, lisades, eemaldades ja ümberkorraldades segmente.  
    * Kõikide ulatuste numbriseeriad võivad sisaldada konstantseid segmente ning tähtedest ja numbritest koosnevaid segmente. Konstantsed segmendid sisaldavad muutumatut tähe- või numbrimärkide kogumit. Selle segmendi tüübi abil saate lisada sidekriipsu või muu eraldaja numbriseeria segmentide vahele. Tähtedest ja numbritest koosnevad segmendid sisaldavad numbrimärkide kombinatsiooni (#) ning ja-märke (&). Need märgid tähistavad tähti ja numbreid, mis kasvavad iga kord, kui numbriseeria numbrit kasutatakse. Kasutage trelle (#), et tähistada kasvavaid numbreid ning ja-märki (&), et tähistada kasvavaid tähti. Näiteks vorming #####_2014 loob seeria 00001_2014, 00002_2014 jne.     Vähemalt üks tähtedest ja numbritest koosnev segment peab olemas olema. Ulatuse segmendid, nagu ettevõte või juriidiline isik, ei ole nõutavad. Kuid kui te ei kaasa ulatuse segmente vormingusse, luuakse iga ulatuse kohta ikkagi valitud viitele numbrid.  
7. Laiendage jaotist Viited.
    * Kiirkaardil Viited valige dokumendi tüüp või kirje, mida määrata sellele numbrijadale.     See etapp on valikuline järjestustele, mis on määratletud spetsiaalse rakendamise kasutusmustritele. Nende stsenaariumide puhul luuakse uus number, kasutades numbriseeriakoodi või ID väärtust, ilma viidet kasutamata. Näiteks spetsiaalse rakenduse kasutusmuster on kandeseeria, mida kasutatakse konkreetsete töölehenimede jaoks. Aga me ei soovita teil selliseid mustreid kasutada.  
8. Laiendage jaotis Üldine.
    * Määrake kiirkaardil Üldine, kas numbriseeria on manuaalne ja pidev või katkev. Lisaks sisestage madalaimad ja kõrgeimad numbrid, mida numbriseerias saab kasutada.     Me ei soovita katkevat numbriseeriat muuta pidevaks numbriseeriaks. Numbriseeria ei saa olla täiesti pidev. See muutus võib põhjustada ka dublikaatvõtme rikkumisi andmebaasis. Lisaks on pidevatel numbriseeriatel on suurem mõju tulemuslikkusele.   
9. Klõpsake nuppu Salvesta.


