---
title: Täiustatud RCS-i filtreerimine RCS-i/globaalses hoidlas
description: See artikkel kirjeldab RCS-i globaalse hoidla täiustatud filtreerimisvõimalusi, mida on täiustatud lisafiltrite kaasamiseks.
author: kfend
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: e0408d0561c0cfead8781b9f49fdb84d5caf179a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274508"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>Täiustatud RCS-i filtreerimise võimalused konfiguratsioonide leidmiseks RCS-i/globaalses hoidlas

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab täiustatud filtreerimisvõimalusi regulatiivsete konfiguratsiooniteenuste (RCS) globaalsele hoidlale, mida on täiustatud, et kaasata filtreerimisvõimalus järgmiste kriteeriumidega: 
- **Riik/piirkond** – ISO riigikoodide põhjal  
- **Siltide** tüübid järgmiste jaoks.
  - Funktsionaalne ala
  - Funktsiooniala
  - Majandusharu 
  - Äridokument 

Saate määrata filtreid nii eraldi kui ka grupina, et teha kindlate või seostatud konfiguratsioonide leidmine lihtsamaks. Näiteks võiksite rakendada filtrit **Äridokumendi tüüp**, et leida hankija arvetega seostatud konfigureeritavate äridokumentide üks tüüp ja otsida seda tüüpi dokumente. 

[![Globaalse hoidla jaotise filtreerimine.](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Otsingut saate täpsemalt piiritleda, valides dokumendi tüübi, näiteks „hankija arve”, ja klõpsates käsku **Rakenda filter**. Järgmine näide kuvab tulemusi filtri **Äridokumendi tüüp** rakendamise korral koos lisatud dokumendi tüübiga. 

[![Äridokumendi tüübi rakendatud filter ja importimine.](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Filtreeritud tulemusi saab importida kas eraldi või komplektina kasutajate RCS-hoidlasse või Dynamics 365 Finance keskkonda. Selleks valige konfiguratsioonide grupp ja klõpsake käsku **Impordi**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
