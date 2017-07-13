---
title: Finantsdimensioonid
description: "Selles teemas kirjeldatakse mitmesuguseid finantsdimensioonide tüüpe ja nende seadistamist."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: a0edbad63c51d111d7c8985aa7fdf7312da6149d
ms.openlocfilehash: e82d53b3f6b4c8d3e2363f26576331e1d03434d9
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017


---

# <a name="financial-dimensions"></a>Finantsdimensioonid

[!include[banner](../includes/banner.md)]

Selles teemas selgitatakse mitmesuguseid finantsdimensioonide tüüpe ja nende seadistamist.

Kasutage lehte **Finantsdimensioonid**, et luua finantsdimensioonid, mida saab kasutada kontosegmentidena kontoplaanide puhul. Finantsdimensioone on kaht tüüpi: kohandatud dimensioonid ja üksuse tagatud dimensioonid. Kohandatud dimensioone kasutavad juriidilised isikud ühiselt ning väärtusi sisestavad ja haldavad kasutajad. Üksuse tagatud dimensioonide puhul määratletakse väärtused mujal süsteemis, nt üksustes Kliendid või Kauplused. Mõnda üksuse tagatud dimensiooni kasutavad juriidilised isikud ühiselt, samas kui mõni on ettevõttekohane. 

Kui olete finantsdimensioonid loonud, kasutage igale finantsdimensioonile täiendavate atribuutide lisamiseks lehte **Finantsdimensiooni väärtused**. 

Finantsdimensioone saab kasutada juriidiliste isikute kajastamiseks. Rakenduses Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, ei pea juriidilisi isikuid looma. Kuid finantsdimensioonid pole mõeldud juriidiliste isikute tegevus- või ärivajaduste rahuldamiseks. Üksustevaheline raamatupidamisfunktsioon rakenduses Finance and Operations on mõeldud ainult iga kande loodavate raamatupidamiskirjete käsitlemiseks. 

 Finantsdimensioonide juriidilised isikud häälestamiseks hinnata äriprotsessist järgmistes määratlemiseks, kui teie organisatsioon töö see seadistus:

- Varud
- Müügi ja ostu finantsdimensioonide ja juriidilised isikud
- Käibemaksuaruandluse koodi genereerimine
- Tegevuse aruandlus

Siin on mõned neist piirangutest.

- Ainult juriidiliste isikutega, finantsdimensioonide, saate käibemaksu funktsiooni.
- Mõned aruanded ei sisalda finantsdimensioone. Seega võib finantsdimensioonide alusel aruande koostamiseks olla vaja aruandeid muuta.

## <a name="custom-dimensions"></a>Kohandatud dimensioonid

Kasutaja määratletud finantsdimensiooni loomiseks tehke väljal **Kasuta väärtusi allikast** valik **&lt; Kohandatud dimensioon &gt;**. Samuti saate määrata kontomaski, et piirata dimensiooniväärtuste puhul sisestatava teabe hulka ja tüüpi. Saate sisestada märke, mis jäävad samaks igale dimensiooniväärtusele, näiteks tähti või sidekriipsu (-). Saate sisestada ka trelle (\#) ning ja-märke (&) kohatäidetena tähtede ja numbrite jaoks, mis muutuvad iga kord, kui luuakse dimensiooniväärtus. Kasutage numbrimärki (\#) kohatäitena numbrile ning ja-märki (&) kohatäitena tähele. Vormingumaski väli on saadaval ainult siis, kui valite väljal **Kasuta välja väärtusi** suvandi **&lt; Kohandatud dimensioon &gt;**.

**Näide**

Dimensiooniväärtuse piiramiseks tähtede CC ja kolme arvuga saate vormingumaskina sisestada **CC-\#\#\#**.

## <a name="entity-backed-dimensions"></a>Üksuse tagatud dimensioonid

Üksuse tagatud finantsdimensiooni loomiseks valige väljalt **Kasuta väärtusi** allikast süsteemi määratletud üksus, millele finantsdimensioon tugineb. Finantsdimensiooni väärtused luuakse siis sellest üksusest. Näiteks projektide dimensiooniväärtuste loomiseks valige **Projektid**. Siis luuakse igale projektinimele dimensiooniväärtus. Lehel **Finantsdimensiooni väärtused** on näha üksuse väärtused. Kui need väärtused on ettevõttepõhised, kuvatakse lehel ka ettevõte.

## <a name="activating-dimensions"></a>Dimensioonide aktiveerimine

Finantsdimensiooni aktiveerimisel uuendatakse tabelit, nii et see sisaldab finantsdimensiooni nime. Kustutatud dimensioonid eemaldatakse. Võite sisestada dimensiooniväärtused enne finantsdimensiooni aktiveerimist. Kuid finantsdimensiooni ei saa enne aktiveerimist tarbida. Näiteks ei saa te lisada finantsdimensiooni kontostruktuurile, enne kui finantsdimensioon on aktiveeritud. Kui klõpsate nuppu **Aktiveeri**, siis uuendatakse kõiki dimensioone ja kuvatakse nende oleku muutused. 

## <a name="translations"></a>Tõlked

Lehele **Teksti tõlge** võite sisestada valitud finantsdimensiooni teksti mitmesugustes keeltes. Lehele **Põhikonto** võite sisestada põhikonto teksti mitmesugustes keeltes. 

## <a name="legal-entity-overrides"></a>Juriidilise isiku alistamised

Kõik dimensioonid ei sobi kõigile juriidilistele isikutele. Lisaks võivad mõningad dimensioonid olla asjakohased ainult konkreetse perioodi jooksul. Sel juhul saab kasutada jaotist **Juriidilise isiku tühistamised** tuvastamiseks, milliste ettevõtete dimensioon tuleks peatada, kes on omanik ja mis ajaperioodil on dimensioon aktiivne.

## <a name="deleting-financial-dimensions"></a>Finantsdimensioonide kustutamine

Andmete viiteterviklikkuse säilitamiseks saab finantsdimensioone harva kustutada. Kui püüate finantsdimensiooni kustutada, hinnatakse järgmisi kriteeriume.

- Kas finantsdimensiooni on mõnes sisestatud või sisestamata kandes või mõnes dimensiooniväärtuste kombinatsiooni tüübis kasutatud?
- Kas finantsdimensiooni on kasutatud mõnes aktiivses kontostruktuuris, täpsema reegli struktuuris või finantsdimensioonide kogumis?
- Kas finantsdimensioon kuulub mõnesse finantsdimensiooni integreerimise vaikevormingusse?
- Kas finantsdimensioon on seadistatud vaikedimensiooniks?

Kui mõni neist kriteeriumidest on täidetud, ei saa finantsdimensiooni kustutada.

