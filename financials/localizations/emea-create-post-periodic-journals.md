---
title: "Tükeldatud perioodid perioodilistele töölehtedele"
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
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 58ab77aea9e66834c516806e5f0cfe3069c94ff3
ms.lasthandoff: 03/31/2017


---

# <a name="split-periods-in-periodic-journals"></a>Tükeldatud perioodid perioodilistele töölehtedele

Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse. Töölehe loomisel saate määrata perioodi kordumise intervalli, näiteks päeva või kuu. Saate määrata ka perioodide arvu, millal tööleht postitatakse.

Korduvalt toodavate ja sisestavate ridade, kasutage selle **perioodilistele töölehtedele** lehel. Tšehhi Vabariik, Eesti, Ungari, Läti, Leedu, Poola ja Venemaa, juriidiliste isikute puhul on **perioodilistele töölehtedele** lehel on pikendatud split perioodide funktsionaalsuse. <!---For more information, see [Create and process a periodic journal](http://ax.help.dynamics.com/en/wiki/create-and-process-a-periodic-journal/).-->

### <a name="example-split-for-periods-in-periodic-journals"></a>Näide: Tükelda perioodideks perioodilistele töölehtedele

Kindlustusselts pakub organisatsiooni allahindlust prepaying kindlustuspoliisi aastaringselt. Makse postitatakse põhivara kontole, näiteks ettemakstud kindlustuse kontole. Seejärel amortiseerite kindlustuse aastase kuumaksu, luues perioodilise töölehe, mis sisaldab ettemakstud kindlustuse konto krediiti ja kindlustuse kulukonto deebetit. Sel juhul saate split perioodide funktsionaalsuse. Klõpsake selle **Tükelda perioodideks** Updatehagi paani nuppu ning **perioodilise töölehe****read** lehekülg ning määrake järgmised väljad.

|                       |                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**             | **Description**                                                                                                                                                                                             |
| **Start date**        | Saate valida perioodilise töölehe esimese rea.                                                                                                                                                        |
| **Number of periods** | Sisestage üle, et jaotada töölehe rea perioodide arv. See väärtus määratleb, mitu uut kannet luuakse. Kande summa jagatakse ühtlaselt uute kannetega. |
| **Unit**              | Valige mõõtühik perioodi.                                                                                                                                                                  |
| **Perioodi intervall**   | Kindlaks sisestamise vaheline aeg.                                                                                                                                                              |

Näiteks luua sisestusi kord kvartalis, sisestage **4** ja on **perioodide arv** valige **kuu** on on **üksus** ja sisestage **3** ja on **perioodiintervalli** välja. Süsteem genereerib neli tööleheread, iga neljandiku töölehe rea summa, mille te sisestasite, 3 kuu tagant. Sarnane funktsioon on ka rakenduse peažurnaali. Pearaamatu ridadele vaatamisel valige **perioodi töölehe**&gt;**Salvesta tööleht**.


