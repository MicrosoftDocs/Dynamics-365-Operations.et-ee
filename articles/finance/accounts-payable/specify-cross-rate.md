---
title: Ristkursi määramine
description: See teema annab üldteavet ristkursside kohta rakenduses Microsoft Dynamics 365 Finance.
author: abruer
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eafaf660470cec5fd82454660f2f59b86d488d0c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810290"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]