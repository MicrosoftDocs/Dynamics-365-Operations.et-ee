---
title: "Tükeldatud perioodid perioodilistes töölehtedes"
description: "Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse. Töölehe loomisel saate määrata perioodi kordumise intervalli, näiteks päeva või kuu. Saate määrata ka perioodide arvu, millal tööleht postitatakse."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261354
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 9b07d2c274d3e4818ffd917a730aeba3e5dff76c
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---

# <a name="split-periods-in-periodic-journals"></a>Tükeldatud perioodid perioodilistes töölehtedes

[!include[banner](../includes/banner.md)]


Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse. Töölehe loomisel saate määrata perioodi kordumise intervalli, näiteks päeva või kuu. Saate määrata ka perioodide arvu, millal tööleht postitatakse.

Kanderidade korduvaks toomiseks ja sisestamiseks saate kasutada lehte **Perioodilised töölehed**. Juriidiliste isikute puhul Tšehhi Vabariigis, Eestis, Ungaris, Lätis, Leedus, Poolas ja Venemaal on lehte **Perioodilised töölehed** laiendatud perioodide tükeldamise funktsiooniga. Lisateavet vaadake jaotisest [Perioodilise töölehe sisestamine](/dynamics365/unified-operations/financials/general-ledger/tasks/post-periodic-journals)

### <a name="example-split-for-periods-in-periodic-journals"></a>Näide: perioodide tükeldamine perioodilistes töölehtedes

Kindlustusfirma pakub teie organisatsioonile allahindlust terve aasta kindlustuspoliisi ettemaksule. Makse postitatakse põhivara kontole, näiteks ettemakstud kindlustuse kontole. Seejärel amortiseerite kindlustuse aastase kuumaksu, luues perioodilise töölehe, mis sisaldab ettemakstud kindlustuse konto krediiti ja kindlustuse kulukonto deebetit. Sellisel juhul saate kasutada perioodideks tükeldamise funktsiooni. Klõpsake toimingupaani lehel **Perioodilise töölehe** **read** nuppu **Tükelda perioodideks** ja täitke järgmised väljad.

|                       |                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Väli**             | **Kirjeldus**                                                                                                                                                                                             |
| **Alguskuupäev**        | Valige esimese perioodilise töölehe rea kuupäev.                                                                                                                                                        |
| **Perioodide arv** | Sisestage perioodide arv, millega töölehe ridade arv jagada. See väärtus määratleb, mitu uut kannet luuakse. Kande summa jagatakse ühtlaselt uute kannetega. |
| **Ühik**              | Valige perioodile mõõtühik.                                                                                                                                                                  |
| **Perioodi intervall**   | Määrake sisestusperioodide vaheline intervall.                                                                                                                                                              |

Näiteks kvartalipõhiste sisestuste loomiseks sisestage väljale **Perioodide arv** väärtus **4**, valige väljal **Ühik** säte **Kuud** ja sisestage väljale **Perioodi intervall** väärtus **3**. Süsteem loob neli töölehe rida, iga rida on üks neljandik sisestatud töölehe rea summast iga 3 kuu järel. Sarnane funktsioon on saadaval ka päevaraamatu kohta. Päevaraamatu ridade vaatamisel valige **Perioodi tööraamat** &gt; **Salvesta tööraamat**.




