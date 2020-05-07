---
title: Täiustatud RCS-i filtreerimine RCS-i/globaalses hoidlas
description: Selles teemas kirjeldatakse täiustatud filtreerimise võimalusi RCS-i globaalses hoidlas, mida on täiustatud täiendavate filtrite lisamisega.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1913b661c46af5e34da1a2939cb2a5d5b4e46411
ms.sourcegitcommit: 7df49a85de484d013518217ba8ada6c61da4b6e4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/24/2020
ms.locfileid: "3287935"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>Täiustatud RCS-i filtreerimise võimalused konfiguratsioonide leidmiseks RCS-i/globaalses hoidlas

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse täiustatud filtreerimise võimalusi teenuste Regulatory Configuration Services (RCS) globaalses hoidlas, mida on täiustatud järgmiste täiendavate filtreerimisvõimaluste lisamisega. 
- **Riik/piirkond** – ISO riigikoodide põhjal  
- **Siltide** tüübid järgmiste jaoks.
  - Funktsionaalne ala
  - Funktsiooniala
  - Majandusharu 
  - Äridokument 

Saate määrata filtreid nii eraldi kui ka grupina, et teha kindlate või seostatud konfiguratsioonide leidmine lihtsamaks. Näiteks võiksite rakendada filtrit **Äridokumendi tüüp**, et leida hankija arvetega seostatud konfigureeritavate äridokumentide üks tüüp ja otsida seda tüüpi dokumente. 

[![Globaalse hoidla jaotise filtreerimine](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Otsingut saate täpsemalt piiritleda, valides dokumendi tüübi, näiteks „hankija arve”, ja klõpsates käsku **Rakenda filter**. Järgmine näide kuvab tulemusi filtri **Äridokumendi tüüp** rakendamise korral koos lisatud dokumendi tüübiga. 

[![Äridokumendi tüübi rakendatud filter ja importimine](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Filtreeritud tulemusi saab importida kasutajate RCS-i hoidlasse või Dynamics 365 Finance'i keskkonda nii eraldi kui ka komplektina. Selleks valige konfiguratsioonide grupp ja klõpsake käsku **Impordi**.
