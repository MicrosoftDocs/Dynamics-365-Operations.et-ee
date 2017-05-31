---
title: Finantsdimensioonid
description: "See artikkel selgitab erinevaid finantsdimensioonide tüüpe ja nende seadistamist."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 01f189b8de3f0cc707dcc54f4cde75aed95b8e3f
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="financial-dimensions"></a>Finantsdimensioonid

[!include[banner](../includes/banner.md)]


See artikkel selgitab erinevaid finantsdimensioonide tüüpe ja nende seadistamist.

Kasutage lehte Finantsdimensioonid, et luua finantsdimensioonid, mida saab kasutada kontosegmentidena kontoplaanide puhul. Finantsdimensioone on kaht tüüpi: kohandatud dimensioonid ja üksuse tagatud dimensioonid. Kohandatud dimensioone kasutavad juriidilised isikud ühiselt ning väärtusi sisestab ja haldab kasutaja. Üksuse tagatud dimensioonid on dimensioonid, mille väärtused määratletakse mujal süsteemis, nt moodulis Kliendid või Kauplused. Mõnd üksuse tagatud dimensiooni kasutavad juriidilised isikud ühiselt ja mõni on ettevõttekohane. 

Kui olete finantsdimensioonid loonud, kasutage igale finantsdimensioonile täiendavate atribuutide lisamiseks lehte Finantsdimensiooni väärtused. 

Ehkki saate kasutada finantsdimensioone juriidiliste isikute kajastamiseks rakenduses Microsoft Dynamics 365 for Operations juriidilisi isikuid loomata, pole finantsdimensioonid mõeldud juriidiliste isikute tegevus- või ärivajaduste rahuldamiseks. Üksustevaheline raamatupidamisfunktsioon rakenduses Microsoft Dynamics 365 for Operations on mõeldud ainult iga kande loodavate raamatupidamiskirjete käsitlemiseks. 

 Finantsdimensioonide juriidilised isikud häälestamiseks hinnata äriprotsessist järgmistes määratlemiseks, kui teie organisatsioon töö see seadistus:

-   Varud
-   Müügi ja ostu finantsdimensioonide ja juriidilised isikud
-   Käibemaksuaruandluse koodi genereerimine
-   Tegevuse aruandlus

Piiranguid näited on järgmised:

-   Ainult juriidiliste isikutega, finantsdimensioonide, saate käibemaksu funktsiooni.
-   Mõnes aruandes ei sisalda finantsdimensioonide, nii et te ei saa alati aruanne finantsdimensiooni kui aruanded on muudetud.

**Kohandatud dimensioonid** 

Kasutaja määratletud finantsdimensiooni loomiseks valige väljal Kasuta väärtusi allikast suvand &lt; Kohandatud dimensioon &gt;. Samuti saate määrata kontomaski, et piirata dimensiooniväärtuste puhul sisestatava teabe hulka ja tüüpi. Saate sisestada märke, mis jäävad samaks igale dimensiooniväärtusele, näiteks tähti või sidekriipsu. Saate sisestada ka trelle (\#) ning ja-märke (&) kohatäidetena tähtede ja numbrite jaoks, mis muutuvad iga kord, kui luuakse dimensiooniväärtus. Kasutage numbrimärki (\#) kohatäitena numbrile ning ja-märki (&) kohatäitena tähele. 

**Näide** 

Dimensiooniväärtuse piiramiseks tähtedele CC ja kolmele arvule, saate vormingumaskina sisestada CC-\#\#\#. See väli on saadaval ainult siis, kui valite väljal Kasuta välja väärtusi suvandi &lt; Kohandatud dimensioon &gt;. 

**Üksuse tagatud dimensioonid** 

Üksuse tagatud finantsdimensiooni loomiseks valige väljalt Kasuta väärtusi allikast süsteemi määratletud üksus, millele finantsdimensioon tugineb. Finantsdimensiooni väärtused luuakse sellest valikust. Näiteks projektide dimensiooniväärtuste loomiseks valige Projektid. Dimensiooniväärtus luuakse igale projektinimele. Dimensiooniväärtuste lehel kuvatakse üksuse väärtused ja kui need on ettevõttekohased, siis ka väärtusega seotud ettevõtet. 

**Dimensioonide aktiveerimine** 

Finantsdimensiooni aktiveerimine värskendab tabelit finantsdimensiooni nimega ja eemaldab kustutatud dimensioonid. Dimensiooniväärtusi saate sisestada enne finantsdimensiooni aktiveerimist, kuid finantsdimensiooni ei saa kuskil kasutada enne, kui see on aktiveeritud. Näiteks ei saa te lisada finantsdimensiooni kontostruktuurile, enne kui finantsdimensioon on aktiveeritud. Aktiveerimisnupu klõpsamisel värskendatakse kõik dimensioonid koos olekumuutustega. 

**Tõlked** 

Lehel Teksti tõlkimine saate sisestada teksti, mis kuvatakse valitud finantsdimensiooni puhul erinevates keeltes. Lehel Põhikonto tõlkimine saate sisestada teksti, mis kuvatakse põhikonto puhul erinevates keeltes. 

**Juriidilise isiku tühistamised** 

Kõik dimensioonid ei kehti kõigi juriidiliste isikute puhul ja mõni võib olla asjakohane ainult konkreetsel ajaperioodil. Sel juhul saab jaotist Juriidilise isiku tühistamised kasutada tuvastamaks, milliste ettevõtete dimensioon tuleks peatada, kes on omanik ja mis ajaperioodil on dimensioon aktiivne.






