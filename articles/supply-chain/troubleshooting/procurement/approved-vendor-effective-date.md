---
title: Kinnitatud hankija kehtivuse kuupäeva ei saa muuta
description: Kinnitatud hankijate loend toote põhjal üksus ei lase muuta jõustumiskuupäeva
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: cb6dbd134d63daa163261cabdbd7eceb978877ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476076"
---
# <a name="cant-change-the-effective-date-for-an-approved-vendor"></a>Kinnitatud hankija kehtivuse kuupäeva ei saa muuta


## <a name="symptoms"></a>Sümptomid

Tootel on kinnitatud hankija, mille jõustumiskuupäev on näiteks 11. jaanuar 2018 (*01/11/2018*) ja aegumiskuupäev *Mitte kunagi*. Kui proovite muuta jõustumiskuupäevaks 10. jaanuari 2018 (*01/10/2018*) või 12. jaanuari 2018 (*01/12/2018*), kuvatakse järgmine tõrge.

> Kinnitatud tarnijate loendis (PdsApproveVendorList) ei saa kirjet luua. Väärtus „Aegumine” peab olema suurem kui väärtus „Jõustumine” või sellega võrdne.

## <a name="resolution"></a>Lahendus

Saate pikendada ainult perioodi, mille jooksul on hankija kinnitatud. Kehtivad järgnevad reeglid.

- Jõustumiskuupäeva muutmiseks nii, et see oleks varem kui ükskõik milline kauba hankija olemasolev kirje (periood), peab uue perioodi aegumiskuupäev olema enne kõiki olemasolevate kirjete aegumiskuupäevi.
- Aegumiskuupäeva muutmiseks nii, et see oleks hiljem kui mõni olemasolev periood, peab jõustumiskuupäev olema pärast mis tahes olemasoleva kirje hilisemat aegumiskuupäeva.
- Et vähendada tervet perioodi, mille jooksul on hankija kinnitatud, peate olemasolevad kirjed kustutama või neid muutma. Teise võimalusena saate kasutada importimise ajal **kärpimise** lülitit. See lüliti kustutab kõik tabelis „Kinnitatud hankijad kauba põhjal” olevad kirjed.

Probleemi kirjelduses kirjeldatud näidisstsenaariumi puhul, kus kirje jõustumiskuupäev on *01/11/2018* ja aegumiskuupäev *Mitte kunagi*, saate importida uue kirje, mille jõustumiskuupäev on *01/10/2018* ja aegumiskuupäev *Mitte kunagi*. Kuid te ei saa perioodi vähendada nii, et jõustumiskuupäev muudetaks andmehalduse kaudu kuupäevaks *01/12/2018*. Selle muudatuse peate tegema kasutajaliidese kaudu.
