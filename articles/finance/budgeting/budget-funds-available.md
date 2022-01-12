---
title: Saadaolevad eelarvefondid
description: Selles teemas tutvustatakse saadaolevaid eelarvefondide funktsiooni ja antakse teavet, mis aitab teil konfigureerida eelarve juhtimist, et optimeerida teie organisatsiooni finantsressursside haldamist.
author: rcarlson
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "60493"
- intro-internal
ms.assetid: be964167-43bc-431d-9adb-48bff32d68d5
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-11-28
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: a8279ae9b08c7537548c1c8b71e6e978fee2b8a1
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891354"
---
# <a name="budget-funds-available"></a>Saadaolevad eelarvefondid

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles teemas tutvustatakse saadaolevaid eelarvefondide funktsiooni ja antakse teavet, mis aitab teil konfigureerida eelarve juhtimist, et optimeerida teie organisatsiooni finantsressursside haldamist.

## <a name="enhanced-calculation-feature-for-budget-funds-available"></a>Saadaoleva eelarvefondide täiustatud arvutamisfunktsioon

Ainult jälgida summasid saadaolevas eelarvefondi arvutamisfunktsioonis võimaldab teil jälgida aluseks olevaid eelarve juhtimise tabeleid dokumenditüüpide ja -riikide jaoks, mis põhinevad eelarve juhtimise parameetrite määratlemise **lehel** **olevatel** sätetel.

Mõnel eelarve juhtimise konfiguratsioonivalikul peavad funktsioonil olema kindlad sätted õigeks tööks. Need valikud valitakse või tühjendatakse vahekaardil **Saadaolevad** eelarvefondid lehel **Eelarve juhtimise parameetrite** määramine. Järgmine tabel näitab sätteid, mis on vajalikud saadaoleva eelarvefondi funktsiooni jaoks.

| Kui see suvand on valitud | See valik peab olema ka valitud |
| ------------------------- | -------------------------------- |
| Eelarve reserveerimised eelpandiõiguse jaoks | Pandiõiguste ja tegelike kulude *eelarve* reserveerimised |
| Pandiõiguste eelarve reserveerimised | Tegelikud kulud |
| Ostutaotluse tüübi dokumentidega pandiõiguste eelarve reserveerimised | Eelarve reserveerimised eelpandiõiguse jaoks |

See funktsioon mõjutab ainult uusi dokumente. Olemasolevate dokumentide summasid jälgitakse ja näidatakse eelarve juhtimise statistika päringus seni, kuni saadaolevad eelarvefondid on muudetud ja eelarve juhtimise uus konfiguratsioon aktiveeritud. Sel hetkel eemaldatakse eelarve jälgimise andmed dokumentide eest, mis eemaldati saadaolevast kalkulatsiooni eelarvefondidest.

Soovitame jätta suvandi **Sisestamata tegelikud kulud** tühjaks. Kui see on valitud, tehakse sisestamata dokumentidel, nt ootel hankijaarvetel, aeganõudev eelarve juhtimise arvutus.