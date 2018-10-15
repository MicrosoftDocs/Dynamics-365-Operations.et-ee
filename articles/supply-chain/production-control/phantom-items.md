---
title: Fiktiivsed kaubad
description: "Selles teemas kirjeldatakse üksikasjalikult, kuidas saab fiktiivset reatüüpi kasutada koosluse- (BOM) ja valemiridade puhul rakenduses Microsoft Dynamics 365 for Finance and Operations."
author: ShylaThompson
manager: AnnBe
ms.date: 06/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: shylaw
ms.search.validfrom: 
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: a92dd82f309867586f047e0dfc36e452a44a0f9c
ms.contentlocale: et-ee
ms.lasthandoff: 10/01/2018

---

# <a name="phantom-items"></a>Fiktiivsed kaubad

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse üksikasjalikult, kuidas saab fiktiivset reatüüpi kasutada koosluse- (BOM) ja valemiridade puhul. Järgmisel joonisel tähistab (a) toote H ning osade F ja G kooslust ning (b) toodete H ja osa F protsessilehte.

![Toode H ja osa F](media/product-H-part-F.png)


Sellel joonisel on toodud näide koosluse struktuurist kahel tasemel. Lõpetatud toode H tähistab masinakoostu toodet. Masinakoost koosneb kahest osast: elektriseadmest (F), millel on kaks materjali (A ja B), ning pakkematerjalide rühmast, millel on samuti kaks materjali (C ja D). Veel üht materjali (E) kasutatakse masina üldise kokkupaneku ajal.

![Toode H ja osa F](media/product-H-part-B.png)

Eeltoodud joonis kujutab toote H tehnilist joonist. See struktuur annab hea ülevaate masina üldkoostu osadest ja komponentidest. Ehkki tootekujundajad eelistaksid koosluse kujutamist sellisel viisil, ei pruugi see struktuur õigesti esitada viisi, kuidas masinat töökohas koostatakse. 

Näiteks tehniline kooslus eeltoodud joonisel näitab, et elektriseade F pannakse kokku eraldi osana eraldi töökäsul. Siiski võidakse töökojas hinnata optimaalsemaks panna elektriseade kokku masina üldkoostu osana, mitte eraldi töökäsuna.

See tehniline kooslus näitab ka, et osa G on eraldi osa. Selles struktuuris ei tähista aga G füüsilist osa, vaid pakkematerjalide kogumit. 

Seetõttu, kuigi tehniline kooslus annab toote kujundusele ja selle haldusele olulise väärtuse, ei pruugi see olla kõige loogilisem viis toote tootmise käivitamisprotsessi toetamiseks. Seevastu kujutab tootmise kooslus parimat viisi toote koostamiseks.

Järgmisel joonisel on näidatud, kuidas eelnev tehniline kooslus viiakse üle tootmise koosluseks. Sellel joonisel tähistab (a) toote H kooslust ja (b) toote H protsessilehte.

Sellises struktuuris näete, et osasid F ja G ei ole näidatud ning materjalid, millest need osad koosnevad, on tõstetud järgmisele kooslusetasandile. 

Vastupidiselt tehnilisele kooslusele, millel oli kaks toimingulehte, on tootmise kooslusel ainult üks toiminguleht. Osaga G seotud pakkimistoiming on samuti tõstetud ja on nüüd osa toote H toimingulehest. Elektriseadme kokkupanek on esimene toiming. See järjekord on mõistlik, kuna seda seadet kasutatakse järgmises toimingus, milleks on masina kokkupanek. Viimane toiming on pakkimistoiming, mis tarbib kaht pakkematerjali (C ja D).

Rakenduses Microsoft Dynamics 365 for Finance and Operations on üleminek tehnilise koosluse ja tootmise koosluse vahel lubatud fiktiivse koosluse reatüübi kaudu. Mõiste „fiktiivne” näitab, et F ja G on kahe koosluse tüübi vahelisel üleminekul kadunud. Selles näites on fiktiivne reatüüp rakendatud tehnilises koosluses osade F ja G koosluseridadele. Tootmis- või partiitellimuse loomisel kopeeritakse tehniline kooslus tootmis- või partiitellimusele. Kui tellimus on hinnatud, toimub üleminek tehniliselt koosluselt tootmise kooslusele, nagu on näidatud eeltoodud joonistel. Teisel joonisel näidatud toimingulehelt sisestatakse toimingu jaoks pakkematerjalid C ja D. 

## <a name="multilevel-phantom-bom-structures"></a>Mitmetasandilised fiktiivse koosluse struktuurid
Fiktiivset reatüüpi saab kasutada mitmetasandilistes kooslusestruktuurides, nagu on näidatud järgmisel joonisel. Sellel joonisel tähistab (a) toote G kooslust ning (b) osade E ja F ning toote G protsessilehte. 

![Toode G ja osa F koos protsessilehtedega](media/product-G-route-sheet-G.png)


Järgmisel joonisel on näidatud tulemuseks saadud tootmise kooslus ja protsessileht, kui osade E ning F koosluseread on konfigureeritud nii, et reatüüp on Fiktiivne. Sellel joonisel tähistab (a) toote G kooslust ja (b) toote G protsessilehte.

![Toode G](media/product-G.png)


## <a name="phantom-and-route-network"></a>Fiktiivne ja protsessivõrk
Fiktiivseid kooslusi saab kasutada ka protsessivõrguga koosluse puhul. Protsessivõrgus tehakse paralleelselt üht või mitut toimingut. Järgmisel joonisel on näidatud mitmetasandilises koosluses kasutatava protsessivõrgu näide. Sellel joonisel tähistab (a) toote G ja osa F kooslust ning (b) toote G ja osa F protsessilehte, millel on protsessivõrk.

![Toode G ja osa F](media/product-G-part-F.png)


Järgmisel joonisel tähistab (a) toote G ning osa F kooslust ning (b) toote G ja osa F protsessilehte.

![Toode G ja osa F koos protsessilehtedega](media/product-G-part-F-with-route-sheet.png)

