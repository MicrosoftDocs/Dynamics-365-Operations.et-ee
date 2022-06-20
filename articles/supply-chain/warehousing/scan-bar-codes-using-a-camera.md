---
title: Vöötkoodide skannimine kaamera abil mobiilirakenduses Warehouse Management
description: See artikkel selgitab, kuidas laohalduse mobiilirakendust häälestada vöötkoodide skannimiseks mobiilses seadmes kaameraga.
author: Mirzaab
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8459ea6912328fa589b92f1731551f56df89c11b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862333"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Vöötkoodide skannimine kaamera abil mobiilirakenduses Warehouse Management

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas laohalduse mobiilirakendust häälestada vöötkoodide skannimiseks mobiilses seadmes kaameraga.

## <a name="setup"></a>Seadistus

Mobiilirakenduse Warehouse Management kuvasätetes saate valida, kas kaamerat vöötkoodide skannimiseks kasutada. Kui lubate valiku **Kaamera kasutamine skannerina**, saate kaamerat kasutada igas sisendväljas, mille eelistatud sisestusrežiim on seatud väärtusele **Skannimine**.

Selleks et määrata, kas sisendväli peaks olema skannitav, määrake lehel **rakenduse Ladustamine väljade nimed** **Eelistatud sisestusrežiim** olekusse **Skannimine**. Selle suvandi valimisel saab mobiilirakenduses Warehouse Management kasutada kaamerat skannimiseks. Lisateavet vt [Mobiilirakenduse Warehouse Management väljade konfigureerimine](configure-app-field-names-priorities-warehouse.md).

## <a name="supported-bar-code-formats"></a>Toetatud vöötkoodivormingud

Toetatud on levinuimad vöötkoodivormingud, sh kood 128, kood 39, kood 93, EAN-8, EAN-13, UPC-E, UPC-A ja QR-koodid.

## <a name="navigation"></a>Navigeerimine

Kaameraleht käivitub igal lehel, kus **sisestusvälja eelistatud sisestusrežiim** on seatud väärtusele *Skannimine*. Kaameralehel olles kasutage navigeerimiseks järgmiseid valikuid.

- **Ülesande ja üksikasjade** lehele naasmiseks valige tagasi nuppu.
- Valige **ülesande ja üksikasjade** lehel pliiatsi ikooni, et minna lehele, kus saate sisendit käsitsi tippida.
- Valige **ülesande ja üksikasjade** lehel kaamera ikooni, et minna tagasi kaameralehele.

Kui valite kaameralehel kaamera nuppu, kuvatakse see vöötkoodi tuvastamise ajal tuhmina. Kui vöötkoodi 5 sekundi jooksul ei tuvastata, aegub protsess ja kaameranupp muutub uuesti kättesaadavaks. Seejärel saate proovida vöötkoodi uuesti skannida.

Kaamerat vöötkoodile suunates hoidke parima tulemuse saavutamiseks vöötkood sulgudega joondatuna. Kui vöötkoodi skannimine õnnestub, läheb tulemus töötlemisele ja teid suunatakse järgmise etapi juurde. Kui järgmine etapp sisaldab järjekordset sisendvälja, mille eelistatud sisestusrežiim on seatud väärtusele Skannimine, käivitub kaameraleht uuesti. Kui järgmine etapp ei sisalda skannimisvälja, siis kaameraleht ei käivitu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]