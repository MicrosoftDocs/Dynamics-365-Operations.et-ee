---
title: "Ristkursi määramine"
description: See teema annab teavet ristkursside kohta rakenduses Microsoft Dynamics 365 for Finance and Operations.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf531c3a8f3bdb17314d1de436b98249169f82a3
ms.openlocfilehash: 112f77738b33aae94babe0cf8e9e61ff2ea3d004
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="specify-the-cross-rate"></a>Ristkursi määramine

[!include [banner](../includes/banner.md)]

See teema selgitab ristkursi eesmärki ja ristkursi määramist makse tasakaalustamisel arvega. Kasutage ristkurssi, kui kehtivad kõik järgmised kriteeriumid. 
-   Tasakaalustate makse arvega. 
-   Makse rida ja arve rida kasutavad erinevaid valuutasid. 
-   Kumbki valuuta pole arvestusvaluuta. 

Ristkurssi ei kasutata, et arvutada maksekande valuuta ümberarvestus makse arvestusvaluutaks. Selle asemel tuuakse vahetuskursside tabelitest vahetuskursid, et arvutada maksekande valuuta summa ja makse arvestusvaluuta summa väärtus. 

Näiteks arvestusvaluuta on USD, arve valuuta on CAD ja makse valuuta on EUR. Ristkurss võimaldab sisestada vahetuskursi otse CAD ja EURi vaheliseks teisendamiseks, nii et USD-d pole vaja kasutada. Kui valite arve ja esmase makse, saate arve rea jaoks sisestada ristkursi. Ristkurss on nende kannete valuutade vaheline vahetuskurss tasakaalustamise kuupäeva seisuga.

1.  Minge ühele järgmistest lehtedest:
- **Müügireskontro > Üldine > Kliendid > Kõik kliendid** 
- **Ostureskontrod > Üldine > Hankijad > Kõik hankijad** 
- **Hanked > Üldine > Hankijad > Kõik hankijad**
2.  Valige klient või tarnija, kelle avatud kandeid te tasakaalustate. 
3.  Kliendi korral tehke loendilehel **Kõik kliendid** valik **Kogumine > Avatud kannete tasakaalustamine**. Hankija korral tehke loendilehel **Kõik hankijad** valik **Arve > Avatud kannete tasakaalustamine**. 
4.  Valige kanne, mis on esmane makse ja klõpsake nuppu **Märgi makse**. Veerus **Märgi** valitakse märkeruut ja veerus **Esmane makse** kuvatakse ikoon teabega. 
5.  Väljale **Ristkurss** sisestage arve valuuta ja makse valuuta vaheline vahetuskurss tasakaalustamise kuupäeva seisuga. 

