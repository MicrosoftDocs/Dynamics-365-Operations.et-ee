---
title: Fiktiivsed kaubad
description: See artikkel kirjeldab, kuidas fiktiivst reatüüpi saab kasutada koosluse ridade ja valemi puhul moodulis Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 05/05/2022
ms.topic: article
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-05-05
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 64139873216decd8ecb2fcaf1f284e726c53c332
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893319"
---
# <a name="phantom-items"></a>Fiktiivsed kaubad

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab üksikasjalikult, kuidas fiktiivse rea tüüpi saab kasutada koosluse ja valemi ridadel.

Joonisel 1 on (a) toote H ning osade F ja G kooslus ning (b) on toodete H ja F protsessileht.

![Joonis 1: Tehnika kooslus.](media/product-H-part-F.png)
*Joonis 1: Tehnika kooslus*

Joonis 1 näitab näidet koosluse struktuuri kohta kahel tasemel. Lõpetatud toode H tähistab masinakoostu toodet. Masinakoost koosneb kahest osast: elektriseadmest (F), millel on kaks materjali (A ja B), ning pakkematerjalide rühmast, millel on samuti kaks materjali (C ja D). Veel üht materjali (E) kasutatakse masina üldise kokkupaneku ajal.

Joonis 1 tähistab toote H tehnika kooslust. See struktuur annab hea ülevaate üldise masinaassembleri osadest ja komponentidest. Ehkki tootekujundajad eelistaksid koosluse kujutamist sellisel viisil, ei pruugi see struktuur õigesti esitada viisi, kuidas masinat töökohas koostatakse.

Näiteks joonisel 1 näitab tehnika kooslus, et elektriühik F on monteeritud eraldi töötellimusel eraldi osana. Siiski võidakse töökojas hinnata optimaalsemaks panna elektriseade kokku masina üldkoostu osana, mitte eraldi töökäsuna.

See tehniline kooslus näitab ka, et osa G on eraldi osa. Selles struktuuris ei tähista aga G füüsilist osa, vaid pakkematerjalide kogumit.

Seetõttu, kuigi tehniline kooslus annab toote kujundusele ja selle haldusele olulise väärtuse, ei pruugi see olla kõige loogilisem viis toote tootmise käivitamisprotsessi toetamiseks. Seevastu kujutab tootmise kooslus parimat viisi toote koostamiseks.

Joonis 2 näitab, kuidas eelnev tehnika kooslus on üleminekul tootmiskooslusesse. Joonisel 2 on (a) toote H kooslus ja b on toote H protsessileht.

![Joonis 2: tootmiskooslus.](media/product-H-part-B.png)
*Joonis 2: tootmiskooslus*

Sellises struktuuris näete, et osasid F ja G ei ole näidatud ning materjalid, millest need osad koosnevad, on tõstetud järgmisele kooslusetasandile.

Vastupidiselt tehnilisele kooslusele, millel oli kaks toimingulehte, on tootmise kooslusel ainult üks toiminguleht. Osaga G seotud pakkimistoiming on samuti tõstetud ja on nüüd osa toote H toimingulehest. Elektriseadme kokkupanek on esimene toiming. See järjekord on mõistlik, kuna seda seadet kasutatakse järgmises toimingus, milleks on masina kokkupanek. Viimane toiming on pakkimistoiming, mis tarbib kaht pakkematerjali (C ja D).

Üleminek tehnilise koosluse ja tootmise koosluse vahel on lubatud fiktiivse koosluse reatüübi kaudu. Mõiste „fiktiivne” näitab, et F ja G on kahe koosluse tüübi vahelisel üleminekul kadunud. Selles näites on fiktiivne reatüüp rakendatud tehnilises koosluses osade F ja G koosluseridadele. Tootmis- või partiitellimuse loomisel kopeeritakse tehniline kooslus tootmis- või partiitellimusele. Seejärel, kui tellimust hinnatakse, toimub siirde tehnika kooslusest tootmiskooslusesse, nagu näha joonisel 2. Toimingusse sisestatakse pakkematerjalid C ja D toimingulehelt joonisel 2.

## <a name="multilevel-phantom-bom-structures"></a>Mitmetasandilised fiktiivse koosluse struktuurid

Fiktiivse rea tüüpi saab kasutada mitmetasemelistes kooslusestruktuurides, nagu näha joonisel 3. Joonisel 3 on (a) toote G kooslus ja (b) on protsessileht osadele E ja F ja tootele G.

![Joonis 3: Tehnika koosluse osa G.](media/product-G.png)
*Joonis 3: Tehnika koosluse osa G*

Joonis 4 näitab tulemuseks saadav tootmise kooslus ja protsessileht, kui osade E ja F koosluse read on konfigureeritud nii, et rea tüüp on fiktiivne. Joonisel 4 on (a) toote G kooslus ja (b) on toote G protsessileht.

![Joonis 4: Tootmise koosluse osa G.](media/product-G-route-sheet-G.png)
*Joonis 4: Tootmise koosluse osa G*

## <a name="phantom-and-route-network"></a>Fiktiivne ja protsessivõrk

Fiktiivseid kooslusi saab kasutada ka protsessivõrguga koosluse puhul. Protsessivõrgus tehakse paralleelselt üht või mitut toimingut. Joonis 5 näitab näidet protsessivõrgu kohta, mida kasutatakse mitmetasemelises koosluses. Joonisel 5 on (a) toote G ja F kooslus ning (b) on protsessileht tootele G ja osale F, millel on protsessivõrk.

![Joonis 5: Tehnika koosluse osa G, protsessi võrk.](media/product-G-part-F.png)
*Joonis 5: Tehnika koosluse osa G, protsessi võrk*

Joonisel 6 on (a) toote G ja osa F kooslus ning (b) on toote G ja F osa protsessileht.

![Joonis 6: Tootmiskoosluse osa G, protsessivõrk.](media/product-G-part-F-with-route-sheet.png)
*Joonis 6: Tootmiskoosluse osa G, protsessivõrk*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]