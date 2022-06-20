---
title: Partii ja litsentsiplaadi kinnitus
description: See artikkel kirjeldab, kuidas seadistada ja rakendada mobiilsest seadmest partii- ja litsentsiplaadi kinnitusi.
author: Mirzaab
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef0d528d23c1ee9424e35e29d39121d42ba548e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903720"
---
# <a name="batch-and-license-plate-confirmation"></a>Partii ja litsentsiplaadi kinnitus

[!include [banner](../includes/banner.md)]

Partii kinnitamine võimaldab kontrollida, kas mobiilselt seadmelt võetakse õige partii. Algsel töö komplekteerimisel ainult *eespool oleva partii\[asukoht\]* kaupadest, kus eespool olev partii näitab, et see on kõrgemal kui asukoht otsinguhierarhias, peate kontrollima, et komplekteeritav partii vastaks töö real olevale partiile.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
