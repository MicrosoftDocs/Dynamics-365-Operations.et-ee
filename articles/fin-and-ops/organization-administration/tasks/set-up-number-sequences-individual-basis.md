---
title: Individuaalsete numbriseeriate häälestamine
description: Selles teemas selgitatakse, kuidas seadistada individuaalseid numbriseeriaid.
author: sericks007
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58e69b680c006c814e9408135b6947161ad7c4f3
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/10/2019
ms.locfileid: "1738877"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a>Individuaalsete numbriseeriate häälestamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles teemas selgitatakse, kuidas seadistada individuaalseid numbriseeriaid. Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmetele ja kandekirjetele, mis neid nõuavad. Koondandmeid või kandekirjet, mis nõuavad identifikaatorit, nimetatakse viiteks. Enne kui saate viite jaoks uusi kirjeid luua, peate seadistama numbriseeria ja selle viitega siduma. Võite seadistada kõik vajalikud numbriseeriad samaaegselt, kasutades viisardit **Numbriseeriate seadistamine**, või võite luua või muuta üksikuid numbriseeriaid, kasutades lehte **Numbriseeriad**.

1. Avage **Navigeerimispaan > Moodulid > Organisatsiooni haldus > Numbriseeriad > Numbriseeriad**.
2. Valige **Numbriseeria**.
3. Sisestage väärtus väljale **Numbriseeria kood**.
4. Sisestage väärtus väljale **Nimi**.
5. Valige kiirkaardil **Ulatuse parameetrid** nubriseeriale ulatus ja valige ulatuse väärtused ripploendist. Ulatus määratleb, millised organisatsioonid kasutavad numbriseeriat. Lisaks saavad numbriseeriad, mille ulatus ei ole **Ühiskasutatav**, omada nende ulatusele vastavaid segmente. Näiteks võib numbriseerial ulatusega **Juriidiline isik** olla juriidilise isiku segment. Ulatuste kohta lisainfo saamiseks vaadake jaotist [numbriseeria ülevaade](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/fin-and-ops/organization-administration/number-sequence-overview.md).  
6. Laiendage jaotist **Segmendid**.
    - Määratlege numbriseeriate vorming, lisades, eemaldades või teisaldades segmente.  
    - Iga ulatusega numbriseeriad võivad sisaldada *Konstantseid segmente* ja *Tähtnumbrilisi segmente*. Konstantsed segmendid sisaldavad muutumatut tähe- või numbrimärkide kogumit. Selle segmendi tüübi abil saate lisada sidekriipsu või muu eraldaja numbriseeria segmentide vahele. Tähtedest ja numbritest koosnevad segmendid sisaldavad numbrimärkide kombinatsiooni (#) ning ja-märke (&). Need märgid tähistavad tähti ja numbreid, mis kasvavad iga kord, kui numbriseeria numbrit kasutatakse. Kasutage trelle (#), et tähistada kasvavaid numbreid ning ja-märki (&), et tähistada kasvavaid tähti. Näiteks loob vorming `#####_2014` seeria `00001_2014`, `00002_2014`ja nii edasi. Vähemalt üks tähtedest ja numbritest koosnev segment peab olemas olema. Ulatuse segmendid, nagu ettevõte või juriidiline isik, ei ole nõutavad. Kuid kui te ei kaasa ulatuse segmente vormingusse, luuakse iga ulatuse kohta ikkagi valitud viitele numbrid.  
7. Laiendage jaotist **Viited**. Valige dokumendi tüüp või kirje, millele see numbriseeria määrata. See etapp on valikuline järjestustele, mis on määratletud spetsiaalse rakendamise kasutusmustritele. Nende stsenaariumide puhul luuakse uus number, kasutades numbriseeriakoodi või ID väärtust, ilma viidet kasutamata. Näiteks spetsiaalse rakenduse kasutusmuster on kandeseeria, mida kasutatakse konkreetsete töölehenimede jaoks. Aga me ei soovita teil selliseid mustreid kasutada.  
8. Laiendage jaotist **Üldine**. Määrake kiirkaardil Üldine, kas numbriseeria on manuaalne ja pidev või katkev. Lisaks sisestage madalaimad ja kõrgeimad numbrid, mida numbriseerias saab kasutada. Me ei soovita katkevat numbriseeriat muuta pidevaks numbriseeriaks. Numbriseeria ei saa olla täiesti pidev. See muutus võib põhjustada ka dublikaatvõtme rikkumisi andmebaasis. Lisaks on pidevatel numbriseeriatel on suurem mõju tulemuslikkusele.   
9. Klõpsake valikut **Salvesta**.

