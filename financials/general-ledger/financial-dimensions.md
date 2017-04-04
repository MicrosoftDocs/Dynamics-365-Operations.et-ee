---
title: Finantsdimensioonid
description: "See artikkel selgitab erinevaid finantsdimensioonide tüüpe ja nende seadistamist."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25871
ms.assetid: af54621c-c8be-4b72-b6df-dcf886c40ce4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f849b98cac88d182875aca88aaf04cd3575ed99f
ms.lasthandoff: 03/31/2017


---

# <a name="financial-dimensions"></a>Finantsdimensioonid

See artikkel selgitab erinevaid finantsdimensioonide tüüpe ja nende seadistamist.

Kasutage lehte Finantsdimensioonid, et luua finantsdimensioonid, mida saab kasutada kontosegmentidena kontoplaanide puhul. Finantsdimensioone on kaht tüüpi: kohandatud dimensioonid ja üksuse tagatud dimensioonid. Kohandatud dimensioone kasutavad juriidilised isikud ühiselt ning väärtusi sisestab ja haldab kasutaja. Üksuse tagatud dimensioonid on dimensioonid, mille väärtused määratletakse mujal süsteemis, nt moodulis Kliendid või Kauplused. Mõnd üksuse tagatud dimensiooni kasutavad juriidilised isikud ühiselt ja mõni on ettevõttekohane. 

Kui olete finantsdimensioonid loonud, kasutage igale finantsdimensioonile täiendavate atribuutide lisamiseks lehte Finantsdimensiooni väärtused. 

Kuigi saate finantsdimensioonide, kes esindavad juriidilised isikud loomata juriidiliste isikute Microsoft Dynamics 365 toiminguteks, finantsdimensioonide ei ole mõeldud rahuldama rakenduskava või ettevõte vajab juriidiliste isikute. Interunit arvestuse funktsioonile Microsoft Dynamics 365 operatsioonide eesmärk on käsitleda ainult raamatupidamise kanded, mis on loodud iga tehingu. 

 Finantsdimensioonide juriidilised isikud häälestamiseks hinnata äriprotsessist järgmistes määratlemiseks, kui teie organisatsioon töö see seadistus:

-   Varud
-   Müügi ja ostu finantsdimensioonide ja juriidilised isikud
-   Käibemaksuaruandluse koodi genereerimine
-   Tegevuse aruandlus

Piiranguid näited on järgmised:

-   Ainult juriidiliste isikutega, finantsdimensioonide, saate käibemaksu funktsiooni.
-   Mõnes aruandes ei sisalda finantsdimensioonide, nii et te ei saa alati aruanne finantsdimensiooni kui aruanded on muudetud.

**Custom dimensions** 

Kasutaja määratletud rahalise küljega, kasutamise väärtused väljal valige &lt;kohandatud dimensiooni&gt;. Samuti saate määrata kontomaski, et piirata dimensiooniväärtuste puhul sisestatava teabe hulka ja tüüpi. Saate sisestada märke, mis jäävad samaks igale dimensiooniväärtusele, näiteks tähti või sidekriipsu. Saate sisestada ka arvu märke (\#) ja ja-märki (&) kohatäidetena tähti ja numbreid, mis muutub iga kord, kui luuakse dimensiooniväärtus. Kasutage arvu märk (\#) kohatäitena mitmeid ja ampersandiga (&) kohatäitena kirja. 

**Näide** 

Dimensiooniväärtuse kirjad CC ja kolm arvu piiramiseks sisestage CC -\#\#\# formaadis mask. See väli on saadaval ainult siis, kui valite &lt;kohandatud dimensiooni &gt;väljalt väärtuste kasutamist. 

**Kindlustatud isiku Mõõdud** 

Kindlustatud isiku rahalise küljega väljalt väärtuste kasutamiseks valige süsteemi määratletud üksus rajada rahalise küljega. Finantsdimensiooni väärtused luuakse sellest valikust. Näiteks projektide dimensiooniväärtuste loomiseks valige Projektid. Dimensiooniväärtus luuakse igale projektinimele. Dimensiooniväärtuste lehel kuvatakse üksuse väärtused ja kui need on ettevõttekohased, siis ka väärtusega seotud ettevõtet. 

**Aktiveerides mõõtmed** 

Finantsdimensiooni aktiveerimine värskendab tabelit finantsdimensiooni nimega ja eemaldab kustutatud dimensioonid. Dimensiooniväärtusi saate sisestada enne finantsdimensiooni aktiveerimist, kuid finantsdimensiooni ei saa kuskil kasutada enne, kui see on aktiveeritud. Näiteks ei saa te lisada finantsdimensiooni kontostruktuurile, enne kui finantsdimensioon on aktiveeritud. Aktiveerimisnupu klõpsamisel värskendatakse kõik dimensioonid koos olekumuutustega. 

**Translations** 

Teksti tõlge lehel saate sisestada teksti, mis kuvatakse valitud finantsmõõtme erinevates keeltes. Lehel Põhikonto tõlkimine saate sisestada teksti, mis kuvatakse põhikonto puhul erinevates keeltes. 

**Legal entity overrides** 

Kõik mõõtmed kehtivad juriidilised isikud ja mõned võib olla asjakohane ainult teatud aja jooksul. Sel juhul saab jaotist Juriidilise isiku tühistamised kasutada tuvastamaks, milliste ettevõtete dimensioon tuleks peatada, kes on omanik ja mis ajaperioodil on dimensioon aktiivne.




