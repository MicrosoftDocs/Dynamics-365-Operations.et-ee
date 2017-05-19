---
title: "Tükeldatud perioodid perioodilistes töölehtedes"
description: "Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse. Töölehe loomisel saate määrata perioodi kordumise intervalli, näiteks päeva või kuu. Saate määrata ka perioodide arvu, millal tööleht postitatakse."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261354
ms.assetid: 76c0d7bf-f795-4d42-9a86-a9f36989962c
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 8a0c6ee25b7130dcee2cc8eada9e83823db21faf
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="split-periods-in-periodic-journals"></a>Tükeldatud perioodid perioodilistes töölehtedes

[!include[banner](../includes/banner.md)]


Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse. Töölehe loomisel saate määrata perioodi kordumise intervalli, näiteks päeva või kuu. Saate määrata ka perioodide arvu, millal tööleht postitatakse.

Kanderidade korduvaks toomiseks ja sisestamiseks saate kasutada lehte **Perioodilised töölehed**. Juriidiliste isikute puhul Tšehhi Vabariigis, Eestis, Ungaris, Lätis, Leedus, Poolas ja Venemaal on lehte **Perioodilised töölehed** laiendatud perioodide tükeldamise funktsiooniga. <!---For more information, see [Create and process a periodic journal](http://ax.help.dynamics.com/en/wiki/create-and-process-a-periodic-journal/).-->

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




