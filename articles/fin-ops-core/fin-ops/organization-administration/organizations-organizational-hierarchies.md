---
title: Organisatsioonide ja organisatsioonihierarhiate ülevaade
description: Organisatsiooni hierarhia kajastab teie ettevõttesse kuuluvate organisatsioonide vahelisi seoseid.
author: sericks007
ms.date: 01/03/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMOperatingUnit,
audience: Application User
ms.reviewer: sericks
ms.custom:
- "17291"
- intro-internal
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8e8f2c2004582f42c3f464fedf9f3d049b5278f
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7991735"
---
# <a name="organizations-and-organizational-hierarchies-overview"></a>Organisatsioonide ja organisatsiooniliste hierarhiate ülevaade

[!include [banner](../includes/banner.md)]

Organisatsiooni on grupp inimesi, kes töötavad koos äriprotsessi või eesmärgi saavutamiseks. Organisatsiooni hierarhia kajastab teie ettevõttesse kuuluvate organisatsioonide vahelisi seoseid.

## <a name="organizations"></a>Organisatsioonid

Saate määratleda järgmist tüüpi siseorganisatsioonid: juriidilised isikud, tootmisüksused ja töörühmad.

Kõik siseorganisatsioonid on **osapoole** üksuse tüübid. Seetõttu kasutavad need organisatsioonid aadressi- ja kontaktteave talletamiseks aadressiraamatut. Osapool, mis saab olla kas isik või organisatsioon, võib kuuluda ühte või mitmesse aadressiraamatusse.

### <a name="legal-entities"></a>Juriidilised isikud

Juriidiline isik on registreeritud või õigusliku struktuuriga organisatsioon. Juriidilised isikud võivad sõlmida juriidilisi lepinguid ja on kohustatud koostama oma tegevuse kohta aruandeid.

Ettevõte on juriidiline isik. Ettevõtted on praegu ainsad juriidilised isikud, mida saate luua, ja iga juriidiline isik on seostatud ettevõtte ID-ga. See seos on olemas, kuna mõni programmi funktsioonivaldkond kasutab oma andmemudelis ettevõtte ID-d või atribuuti DateAreaId. Neis funktsioonivaldkondades kasutatakse ettevõtteid andmeturbe piirina. Kasutajad pääsevad juurde ainult selle ettevõtte andmetele, millesse nad parasjagu sisse on loginud.

### <a name="operating-units"></a>Tootmisüksused

Tootmisüksus on organisatsioon, mida kasutatakse äri majandusressursside ja tööprotsesside juhtimise jagamiseks. Inimestel tootmisüksuses on kohustus maksimeerida nappide ressursside kasutamist, täiustada protsesse ja vastutada nende toimivuse eest.

Tootmisüksuste tüübid hõlmavad kulukeskuseid, äriüksuseid, väärtuse voogusid, osakondi ja kaubanduse kanaleid. Järgmine tabel annab lisateavet iga tüüpi tootmisüksuse kohta.

| Tootmisüksuse tüüp | Kirjeldus | Eesmärk |
|---------------------|-------------|---------|
| Kulukeskus         | Tootmisüksus, mille juhid vastutavad eelarveliste ja tegelike kulude eest. | Kasutatakse juriidilisi isikuid hõlmavate äriprotsesside haldamiseks ja tegevusjuhtimiseks. |
| Äriüksus       | Poolautonoomne tootmisüksus, mis on loodud strateegilise ärieesmärkide saavutamiseks. | Kasutatakse finantsaruandluseks, mis põhineb tööstusvaldkondadel või tootmissuundadel, mida organisatsioon juriidilistest isikutest sõltumatult pakub. |
| Väärtuse voog        | Tootmisüksus, mis kontrollib ühte või mitut tootmisvoogu. | Tavaliselt kasutatakse kulusäästlikus tootmises toote või teenuse tarbijani viimiseks vajalike tegevuste ja voogude juhtimiseks. |
| Osakond          | Tootmisüksus, mis kujutab kindlat ülesannet (nt müük või raamatupidamine) täitva organisatsiooni kategooriat või funktsionaalset osa. | Kasutatakse funktsioonivaldkondade aruandluseks. Osakond võib vastutada kasumi ja kahjumi eest ning koosneda kulukeskuste grupist. |
| Jaemüügikanal      | Tootmisüksus, mis esindab telefoni- ja matipoodi, e-poodi või kõnekeskust. | Kasutatakse ühe või mitme kaupluse haldamiseks ja tegevusjuhtimiseks juriidiliste isikute piires või vahel. |

### <a name="teams"></a>Meeskonnad

Töörühm on organisatsioon, mille liikmed jagavad ühist vastutust, huvi või eesmärki. Töörühmi ei saa kasutada organisatsiooni hierarhiates.

## <a name="organizational-hierarchies"></a>Organisatsiooni hierarhiad

Organisatsiooni hierarhiate seadistamine võimaldab teil oma äri vaadata ja selle aruandlust teha erinevatest aspektidest. Näiteks saate seadistada juriidiliste isikute hierarhia maksu-, õigus- või seadusliku aruandluse jaoks. Saate seadistada tootmisüksustel põhineva hierarhia finantsteabe aruandluseks, mis ei ole õiguslikult vajalik, kuid mida kasutatakse sisejuhtimiseks. Näiteks saate luua ostuhierarhia ostupoliitikate, -reeglite ja äriprotsesside juhtimiseks.

> [!NOTE]
> Pärast tootmisüksuse lisamist hierarhiasse ei saa tootmisüksust kustutada. 

Igale hierarhiale määratakse eesmärk. Hierarhia eesmärk määratleb organisatsioonide tüübid, mille saab hierarhiasse kaasata. Eesmärk määrab ka rakenduse stsenaariumid, milles hierarhiat saab kasutada.

Hierarhiasse kuuluvad organisatsioonid saavad jagada parameetrid, poliitikaid ja kanded. Organisatsioon võib pärida või alistada oma emaorganisatsiooni parameetrid. Kogu organisatsioonile kehtivad siiski ühised koondandmed, nagu tooted ja aadressiraamatud, ja neid ei saa üksikute organisatsioonide puhul alistada. Organisatsioonide ja hierarhiate loomine nõuab hoolikat planeerimist. Lisateavet kohta vt teemast [Oma organisatsiooni hierarhia planeerimine](plan-organizational-hierarchy.md).

## <a name="additional-resources"></a>Lisaressursid
- [Organisatsioonihierarhia kavandamine](plan-organizational-hierarchy.md)
- [Organisatsioonihierarhia loomine](tasks/create-organization-hierarchy.md)
- [Juriidilise isiku loomine](tasks/create-legal-entity.md)
- [Tootmisüksuse loomine](tasks/create-operating-unit.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
