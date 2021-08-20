---
title: Kasutajate importimine rakendusest Azure Active Directory
description: Süsteemiadministraatorid saavad seda toimingut kasutada valitud kasutajate käsitsi importimiseks või suure hulga kasutajate importimiseks Azure Active Directoryst.
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce8c98add0c6d5fb07b3ba5338037d9a12b1d8e50a2d2039b0231d3d305c9ebe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748284"
---
# <a name="import-users-from-azure-active-directory"></a>Kasutajate importimine rakendusest Azure Active Directory

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>Valitud kasutajate importimine

Süsteemiadministraatorid saavad seda toimingut kasutada valitud kasutajate importimiseks Azure Active Directoryst (Azure AD).

1. Kasutaja imporditakse praeguse seansi ettevõttega kui nende vaikimisi ettevõte. Kui see on kohaldatav, muutke praegust ettevõtet enne kasutajate importimist.
2. Minge jaotisse **Süsteemihaldus > Kasutajad > Kasutajad**.
3. Klõpsake **Impordi kasutajad**.
4. Valige importimiseks kasutajad ja valige **Impordi kasutajad**.

Pärast importimise lõpetamist on vaja kasutajatele määrata rollid.

## <a name="import-users-in-bulk"></a>Kasutajate hulgiimport

Süsteemiadministraatorid saavad seda toimingut kasutada suure hulga kasutajate importimiseks Azure Active Directoryst.
Pange tähele, et partii importimise suvandit kasutades ei ole võimalik kasutajaid valida.

## <a name="run-the-import-as-a-batch-job"></a>Partii tööna importimise käivitamine
1. Kasutaja imporditakse praeguse seansi ettevõttega kui nende vaikimisi ettevõte. Kui see on kohaldatav, muutke praegust ettevõtet enne kasutajate importimist.
2. Minge jaotisse **Süsteemihaldus > Kasutajad > Kasutajad**.
3. Klõpsake suvandit **Partii import**.
4. Laiendage jaotist **Käivita taustal**.
4. Valige väärtus **Jah** väljal **Pakett-töötlus**.
6. Sisestage või valige väärtus väljal **Partiigrupp**. See on valikuline etapp.  
7. Valige väljal **Privaatne** väärtus **Jah**. See on valikuline etapp.  
8. Valige väljal **Kriitiline töö** väärtus **Jah**. See on valikuline etapp.  
9. Valige väljal **Jälgimiskategooria** soovitud suvand.
10. Klõpsake valikut **OK**.

Pärast importimise lõpetamist on vaja kasutajatele määrata rollid.

## <a name="run-in-a-sandbox-environment"></a>Liivakastikeskkonna käitamine
1. Valige **Partii import**.
2. Valige nupp **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]