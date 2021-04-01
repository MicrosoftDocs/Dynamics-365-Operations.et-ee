---
title: Vöötkoodide skannimine kaamera abil laorakenduses
description: Selles teemas selgitatakse, kuidas seadistada laorakendust nii, et see võimaldaks mobiilse seadme kaameraga vöötkoode skannida.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 28a49736f43bd2d3bfd4c6856f2f87079a005ba2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239298"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a>Vöötkoodide skannimine kaamera abil laorakenduses

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada laorakendust nii, et see võimaldaks mobiilse seadme kaameraga vöötkoode skannida. 

## <a name="prerequisites"></a>Eeltingimused
Selle funktsiooni kasutamiseks peab teil olema installitud laorakenduse versioon 1.2.0.0 ja teie seadmel peab olema kaamera. Pärast värskendamist rakenduse avamisel palutakse teilt lubada rakendusel kaamerat kasutada. Kui seadmel ei ole kaamerat, siis viibet ei kuvata ja te ei saa kaamerat skannerina kasutada. 

## <a name="setup"></a>Häälestus
Laorakenduse kuvasätetes saate valida, kas kaamerat vöötkoodide skannimiseks kasutada. Kui lubate valiku **Kaamera kasutamine skannerina**, saate kaamerat kasutada igas sisendväljas, mille eelistatud sisestusrežiim on seatud väärtusele **Skannimine**. 

Selleks et määrata, kas sisendväli peaks olema skannitav, määrake lehel **rakenduse Ladustamine väljade nimed** **Eelistatud sisestusrežiim** olekusse **Skannimine**. Selle suvandi valimisel saab laorakenduses kasutada kaamerat skannimiseks. Teavet, kuidas rakenduses Ladustamine väljanimesid konfigureerida, leiate teemast [Väljanimede konfigureerimine laorakenduses](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Toetatud vöötkoodivormingud
Toetatud on levinuimad vöötkoodivormingud, sh kood 128, kood 39, kood 93, EAN-8, EAN-13, UPC-E, UPC-A ja QR-koodid. 

## <a name="navigation"></a>Navigeerimine
Kaameraleht käivitub igal lehel, kus sisestusvälja eelistatud sisestusrežiim on seatud väärtusele Skannimine. Kaameralehel olles kasutage navigeerimiseks järgmiseid valikuid.
- Ülesande ja üksikasjade lehele naasmiseks klõpsake tagasi nuppu. 
- Klõpsake ülesande ja üksikasjade lehel pliiatsi ikooni, et minna lehele, kus saate sisendit käsitsi tippida.
- Klõpsake ülesande ja üksikasjade lehel kaamera ikooni, et minna tagasi kaameralehele. 

| Ülesande ja üksikasjade leht | Kaameraleht | 
| :---------------------: | :--------------------: |
| ![Kaameraga skannimise näidisülesande üksikasjade leht](./media/camera-scanning-example-task-detail-page50.png)          | ![Kaameraga skannimise näidise väiksem kaameraleht](./media/camera-scanning-example-camera-page50.png)          |

Kui klõpsate kaameralehel kaamera nuppu, kuvatakse see vöötkoodi tuvastamise ajal tuhmina. Kui vöötkoodi 5 sekundi jooksul ei tuvastata, aegub protsess ja kaameranupp muutub uuesti kättesaadavaks. Seejärel saate proovida vöötkoodi uuesti skannida.

Kaamerat vöötkoodile suunates hoidke parima tulemuse saavutamiseks vöötkood sulgudega joondatuna. Kui vöötkoodi skannimine õnnestub, läheb tulemus töötlemisele ja teid suunatakse järgmise etapi juurde. Kui järgmine etapp sisaldab järjekordset sisendvälja, mille eelistatud sisestusrežiim on seatud väärtusele Skannimine, käivitub kaameraleht uuesti. Kui järgmine etapp ei sisalda skannimisvälja, siis kaameraleht ei käivitu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]