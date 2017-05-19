---
title: "Organisatsioonid ja organisatsiooni hierarhiad (Commerce’i põhitõed)"
description: "Commerce’i põhitõdedes on kolme tüüpi siseorganisatsioonid, mida saate määratleda, et aidata organisatsioonil äriprotsessi läbi viia või eesmärki saavutada."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21251
ms.assetid: 2bfc6bfe-784b-42e8-8bf0-116e9f0a558e
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 50d29b6552cf7af5f2d9296b1d70b838a8edd637
ms.contentlocale: et-ee
ms.lasthandoff: 04/26/2017


---

# <a name="organizations-and-organizational-hierarchies-commerce-essentials"></a>Organisatsioonid ja organisatsiooni hierarhiad (Commerce’i põhitõed)

[!include[banner](includes/banner.md)]


Commerce’i põhitõdedes on kolme tüüpi siseorganisatsioonid, mida saate määratleda, et aidata organisatsioonil äriprotsessi läbi viia või eesmärki saavutada. 

Organisatsioon on inimeste grupp, kes töötavad koos äriprotsessi teostamiseks või eesmärgi saavutamiseks. Organisatsiooni hierarhia kajastab teie ettevõttesse kuuluvate äriüksuste vahelisi seoseid.

## <a name="organizations"></a>Organisatsioonid
Jaotises Commerce’i põhitõed saate määratleda kolme tüüpi siseorganisatsioonid: juriidilised isikud, tootmisüksused ja töörühmad. Microsoft Dynamics AX-is on kõik siseorganisatsioonid osapoole üksuse tüübid. Seetõttu kasutavad need organisatsioonid aadresside ja muu kontaktteabe talletamiseks aadressiraamatut. Osapool saab olla kas isik või organisatsioon ning see saab kuuluda ühte või mitmesse aadressiraamatusse.
### <a name="legal-entities"></a>Juriidilised isikud

Juriidiline isik on registreeritud või õigusliku struktuuriga organisatsioon. Juriidilised isikud võivad sõlmida juriidilisi lepinguid ja on kohustatud koostama oma tegevuse kohta aruandeid. Ettevõte on Microsoft Dynamics AX-is juriidilise isiku tüüp ja iga juriidiline isik on seostatud ettevõtte ID-ga. Selline seos on loodud seetõttu, et ettevõtte ID-d või DataAreaId-d kasutatakse mõnes andmemudelis, kus ettevõtteid kasutatakse andmeturbe piirina. Kasutajad pääsevad juurde ainult selle ettevõtte andmetele, millesse nad parasjagu sisse on loginud.

### <a name="operating-units"></a>Tootmisüksused

Tootmisüksus on organisatsioon, mida kasutatakse äri majandusressursside ja tööprotsesside juhtimise jagamiseks. Inimestel tootmisüksuses on kohustus maksimeerida nappide ressursside kasutamist, täiustada protsesse ja vastutada nende toimivuse eest. Commerce’i põhitõdedes hõlmavad tootmisüksuste tüübid kulukeskusi, äriüksusi, väärtusevoogusid, osakondi ja jaemüügikanaleid. Järgmine tabel annab lisateavet iga tüüpi tootmisüksuse kohta.
|                         |                                                                                         |                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Tootmisüksuse tüüp** | **Kirjeldus**                                                                         | **Eesmärk**                                                                                                                                 |
| Äriüksus           | Poolautonoomne tootmisüksus, mis on loodud strateegilise ärieesmärkide saavutamiseks. | Kasutage äriüksuseid finantsaruandluseks, mis põhineb tööstusvaldkondadel või tootmissuundadel, mida organisatsioon juriidiliste isikute lõikes pakub. |
| Jaemüügikanal          | Traditsioonilist kauplust tähistav tootmisüksus.                             | Kasutage ühe või mitme poe haldamiseks ja kontrollimiseks juriidiliste isikute piires või vahel.                                                               |

## <a name="organizational-hierarchies"></a>Organisatsiooni hierarhiad
Commerce’i põhitõdedes määratakse igale hierarhiale eesmärk. Hierarhia eesmärk määratleb organisatsioonide tüübid, mille saab hierarhiasse kaasata. Eesmärk määrab ka rakenduse stsenaariumid, milles hierarhiat saab kasutada. Näiteks saab jaemüügi hierarhiat kasutada jaekaupluses toodete ostmiseks ja müümiseks. Hierarhiasse kuuluvad organisatsioonid saavad jagada parameetrid, poliitikaid ja kanded. Organisatsioon võib pärida või alistada oma emaorganisatsiooni parameetrid. Kogu organisatsioonile kehtivad siiski ühised koondandmed, nagu tooted ja aadressiraamatud, ja neid ei saa üksikute organisatsioonide puhul tühistada.
### <a name="best-practices-for-setting-up-an-organization-in-a-hierarchy"></a>Organisatsiooni hierarhia seadistamise head tavad

Arvestage organisatsiooni hierarhia juurutamisel järgmisi parimaid praktikaid.
-   Juriidilise isiku ja äriüksuse vahelise ühisosa määramiseks looge osakond. Seejärel saate koondada osakonna andmed kohustusliku aruandluse jaoks juriidilise isiku alla ja kontsernisiseseks aruandluseks äriüksuse alla.
-   Ärge seadistage ühe juriidilise isiku puhul samal hierarhia eesmärgil mitut hierarhiat.
-   Ärge looge hierarhiat iga eesmärgi jaoks. Tavaliselt saab ühte hierarhiat kasutada mitmel eesmärgil. Näiteks saab ühe tootmisüksuste hierarhia määrata kõigile poliitikaga seotud eesmärkidele.
-   Tasakaalustatud hierarhiate loomine. Hierarhias määratletakse kõik juursõlmest ühel kaugusel olevad sõlmed tasemena. Tasakaalustatud hierarhias saab igal tasemel olla ainult ühte tüüpi tootmisüksus ja kaugus juursõlmest iga tasemeni on ühesugune. Kui osakonna ja juriidilise isiku või äriüksuse vahel on vahepealseid tasemeid, võivad tasakaalustatud hierarhia loomiseks olla vajalikud kohatäiteorganisatsioonid.
-   Ärge seadistage eraldi tootmisüksuste hierarhiat, kui juriidiliste isikute struktuur on ka teie tegevusstruktuur. Juriidiliste isikute ja tootmisüksuste segahierarhia võib täita mõlemat eesmärki.
-   Enne suuremate ümberstruktureerimise stsenaariumide seadistamist kasutage hierarhia kehtivuskuupäevi mõju analüüsi ja kontrolltesti sooritamiseks.
-   Kui hierarhias võib enne avaldamist muudatusi tulla, salvestage see mustandina.
-   Piirake inimeste arvu, kes tohivad organisatsioone tootmiskeskkonnas hierarhiasse lisada või neid sealt eemaldada. Väiksem arv vähendab kulukate eksimuste tekkimise ohtu ja vajadust paranduste järele.

## <a name="retail-store-management"></a>Jaekaupluse haldus
Järgmine tabel kirjeldab Commerce’i põhitõdede stsenaariume, kus saab kasutada organisatsiooni hierarhiaid.
| Ülesanne                                                                           | Kirjeldus                                                                                                                                                                                                                                                                                                | Hierarhia eesmärk    |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| Jaemüügisortimentide haldamine                                                      | Igas jaekaupluses saadaolevate toodete tuvastamine.                                                                                                                                                                                                                                             | Jaemüügi sortiment    |
| Jaemüügi täiendamise haldus                                                    | Saate rühmitada kauplused, täiendades varusid täiendamise reeglite alusel.                                                                                                                                                                                                                                          | Jaemüügi täiendamine |
| Kaupluste andmete aruandlus                                                         | Rühmitage kauplused aruandluse jaoks.                                                                                                                                                                                                                                                                                | Kaupluse aruanded     |
| Varude sisestamine, väljavõtete arvutamine või sisestamine kaupluste grupi kohta | Saate luua kaupluste grupi, mille saab pakett-tööle määrata. Kui määratlete pakett-töö varude sisestamiseks, väljavõtete arvutamiseks või sisestamiseks, saate määrata, millise hierarhia puhul see töö kehtib. Kaupluste lisamisel hierarhiasse või sealt eemaldamisel pole pakett-tööd vaja muuta. | Retail POS-i sisestamine   |






