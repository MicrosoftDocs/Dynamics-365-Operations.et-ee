---
title: Vöötkoodide skannimine kaamera abil mobiilirakenduses Warehouse Management
description: Selles teemas selgitatakse, kuidas seadistada mobiilirakendust Warehouse Management nii, et see võimaldaks mobiilse seadme kaameraga vöötkoode skannida.
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
ms.openlocfilehash: cc58d88865fea17e0e27463b25e2ba815ee1a5b1
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901968"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Vöötkoodide skannimine kaamera abil mobiilirakenduses Warehouse Management

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada mobiilirakendust Warehouse Management nii, et see võimaldaks mobiilse seadme kaameraga vöötkoode skannida.

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