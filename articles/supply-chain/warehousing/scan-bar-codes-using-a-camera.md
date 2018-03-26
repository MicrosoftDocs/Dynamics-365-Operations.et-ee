---
title: "Vöötkoodide skannimine kaameraga Microsoft Dynamics 365 for Finance and Operationsi moodulis Ladustamine"
description: "Selles teemas selgitatakse, kuidas seadistada Microsoft Dynamics 365 for Finance and Operationsi moodulit Ladustamine nii, et see võimaldaks mobiilse seadme kaameraga vöötkoode skannida."
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: f7fe3ab07578b09822fbfeaa4b07331b79f13610
ms.contentlocale: et-ee
ms.lasthandoff: 03/09/2018

---

# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a>Vöötkoodide skannimine kaameraga Microsoft Dynamics 365 for Finance and Operationsi moodulis Ladustamine

[!include[banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada Microsoft Dynamics 365 for Finance and Operationsi moodulit Ladustamine nii, et see võimaldaks mobiilse seadme kaameraga vöötkoode skannida. 

## <a name="prerequisites"></a>Eeltingimused
Selle funktsiooni kasutamiseks peab teil olema installitud mooduli Ladustamine versioon 1.2.0.0 ja teie seadmel peab olema kaamera. Pärast värskendamist rakenduse avamisel palutakse teilt luba, et Microsoft Dynamics 365 for Finance and Operationsi moodul Ladustamine võib kaamerat kasutada. Kui seadmel ei ole kaamerat, siis viibet ei kuvata ja te ei saa kaamerat skannerina kasutada. 

## <a name="setup"></a>Seadistamine
Rakenduse Ladustamine kuvasätetes saate valida, kas kaamerat vöötkoodide skannimiseks kasutada. Kui lubate valiku **Kaamera kasutamine skannerina**, saate kaamerat kasutada igas sisendväljas, mille eelistatud sisestusrežiim on seatud väärtusele **Skannimine**. 

Selleks, et kontrollida, kas sisendväli peaks olema skannitav, seadke Dynamics 365 for Finance and Operationsi lehel **Väljanimed rakenduses Ladustamine** **Eelistatud sisestusrežiim** väärtusele **Skannimine**. Selle suvandi valimisel saab rakenduses Ladustamine kasutada kaamerat skannimiseks. Teavet, kuidas rakenduses Ladustamine väljanimesid konfigureerida, leiate teemast [Väljanimede konfigureerimine rakenduses Ladustamine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Toetatud vöötkoodivormingud
Toetatud on levinuimad vöötkoodivormingud, sh kood 128, kood 39, kood 93, EAN-8, EAN-13, UPC-E, UPC-A ja QR-koodid. 

## <a name="navigation"></a>Navigeerimine
Kaameraleht käivitub igal lehel, kus sisestusvälja eelistatud sisestusrežiim on seatud väärtusele Skannimine. Kaameralehel olles kasutage navigeerimiseks järgmiseid valikuid.
- Ülesande ja üksikasjade lehele naasmiseks klõpsake tagasi nuppu. 
- Klõpsake ülesande ja üksikasjade lehel pliiatsi ikooni, et minna lehele, kus saate sisendit käsitsi tippida.
- Klõpsake ülesande ja üksikasjade lehel kaamera ikooni, et minna tagasi kaameralehele. 

| Ülesande ja üksikasjade leht | Kaameraleht | 
| :---------------------: | :--------------------: |
| ![camera-scanning-example-task-detail-page](./media/camera-scanning-example-task-detail-page50.png)          | ![camera-scanning-example-camera-page-smaller](./media/camera-scanning-example-camera-page50.png)          |

Kui klõpsate kaameralehel kaamera nuppu, kuvatakse see vöötkoodi tuvastamise ajal tuhmina. Kui vöötkoodi 5 sekundi jooksul ei tuvastata, aegub protsess ja kaameranupp muutub uuesti kättesaadavaks. Seejärel saate proovida vöötkoodi uuesti skannida.

Kaamerat vöötkoodile suunates hoidke parima tulemuse saavutamiseks vöötkood sulgudega joondatuna. Kui vöötkoodi skannimine õnnestub, läheb tulemus töötlemisele ja teid suunatakse järgmise etapi juurde. Kui järgmine etapp sisaldab järjekordset sisendvälja, mille eelistatud sisestusrežiim on seatud väärtusele Skannimine, käivitub kaameraleht uuesti. Kui järgmine etapp ei sisalda skannimisvälja, siis kaameraleht ei käivitu.


