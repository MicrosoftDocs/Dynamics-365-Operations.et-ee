---
title: Riskikursi määramine
description: See artikkel annab teavet 365 finantside Microsoft Dynamics ristkursside kohta.
author: abruer
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efb01948af2bcba9ca740e8bd0e12584cf021fce
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889957"
---
# <a name="specify-the-cross-rate"></a>Riskikursi määramine

[!include [banner](../includes/banner.md)]

See artikkel selgitab ristkursi eesmärki ja seda, kuidas määratleda ristkurssi, kui tasakaalustate makse arvega. Kasutage ristkurssi, kui kehtivad järgmised kriteeriumid: 
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
