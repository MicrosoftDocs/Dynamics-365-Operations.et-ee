---
title: Partii ja litsentsiplaadi kinnitus
description: Selles teemas kirjeldatakse, kuidas seadistada ja rakendada partii ning litsentsiplaadi kinnitust mobiilselt seadmelt.
author: Mirzaab
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a953b677b1188750241772d7ae966a1dba77b92e
ms.sourcegitcommit: 9f32389715b226c11e74c53547527e0a8b51e300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514298"
---
# <a name="batch-and-license-plate-confirmation"></a>Partii ja litsentsiplaadi kinnitus

[!include [banner](../includes/banner.md)]

Partii kinnitamine võimaldab kontrollida, kas mobiilselt seadmelt võetakse õige partii. Algsel töö komplekteerimisel ainult eespool oleva partii kaupadest, kus eespool olev partii näitab partiivahemikke, mis on kõrgemal kui asukoht otsinguhierarhias, peate kontrollima, et komplekteeritav partii vastaks töö real olevale partiile.

Litsentsiplaadi kinnitamine võimaldab kontrollida, kas mobiilselt seadmelt võetakse õige litsentsiplaat. Töö komplekteerimisel etapi asukohast peate kontrollima, et komplekteeritav litsentsiplaat vastaks tööga seostatud litsentsiplaadile. Kui tööd alustatakse litsentsiplaadi skannimisega, siis jäetakse see kinnitamise etapp vahele.

## <a name="where-it-applies"></a>Kus see kehtib

Kinnitus kehtib järgmistel juhtudel.

- Partii kinnitus kehtib töö algsel komplekteerimisel eespool oleva partii kaupade puhul.
- Litsentsiplaadi kinnitus kehtib komplekteerimiste korral etapi asukohtadest.

> [!IMPORTANT]
> Litsentsiplaadi kinnitamisel täiendamist ei toetata. Täiendamise töö läbiviimisel ei looda ühtegi litsentsiplaadi kinnituse etappi.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Partii ja litsentsiplaadi kinnituse seadistamine

Partii ja litsentsiplaadi kinnitust saab konfigureerida mobiilse seadme menüüelementidest.

1. Sisenege mobiilse seadme menüüelementidest töö kinnitamise seadistusse.  
1. Valige partii või litsentsiplaadi kinnitamine. Mõlemad valikud on saadaval töö tüübi komplekteerimiste puhul, millel pole automaatne kinnitamine lubatud.  
