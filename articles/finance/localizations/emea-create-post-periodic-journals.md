---
title: Perioodide tükeldamine perioodilistes töölehtedes
description: See artikkel annab teavet perioodiliste töölehtede tükeldamisperioodide või korduvate töölehtede kohta juriidilistele isikutele Tšehhi Vabariigis, Eestis, Ungaris, Leedus, Poolas ja Venemaal.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 261354
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 113b936aab15e9c8f28fc63f745780a76f6f3ab7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848482"
---
# <a name="split-periods-in-periodic-journals"></a>Perioodide tükeldamine perioodilistes töölehtedes

[!include [banner](../includes/banner.md)]

Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse. Töölehe loomisel saate määrata perioodi kordumise intervalli, näiteks päeva või kuu. Saate määrata ka perioodide arvu, millal tööleht postitatakse.

Kanderidade korduvaks toomiseks ja sisestamiseks saate kasutada lehte **Perioodilised töölehed**. Juriidiliste isikute puhul Tšehhi Vabariigis, Eestis, Ungaris, Lätis, Leedus, Poolas ja Venemaal on lehte **Perioodilised töölehed** laiendatud perioodide tükeldamise funktsiooniga. Lisateabe saamiseks vt [perioodijärgseid aruandeid](../general-ledger/tasks/post-periodic-journals.md)

### <a name="example-split-for-periods-in-periodic-journals"></a>Näide: perioodide tükeldamine perioodilistes töölehtedes

Kindlustusfirma pakub teie organisatsioonile allahindlust terve aasta kindlustuspoliisi ettemaksule. Makse postitatakse põhivara kontole, näiteks ettemakstud kindlustuse kontole. Seejärel amortiseerite kindlustuse aastase kuumaksu, luues perioodilise töölehe, mis sisaldab ettemakstud kindlustuse konto krediiti ja kindlustuse kulukonto deebetit. Sellisel juhul saate kasutada perioodideks tükeldamise funktsiooni. Klõpsake toimingupaani lehel **Perioodilise töölehe** **read** nuppu **Tükelda perioodideks** ja täitke järgmised väljad.


| Väli            | Kirjeldus                                                                                                                                                                                             |
|-----------------------|---------------------------------------------------------------|
| **Alguskuupäev**        | Valige esimese perioodilise töölehe rea kuupäev.                                                                                                                                                        |
| **Perioodide arv** | Sisestage perioodide arv, millega töölehe ridade arv jagada. See väärtus määratleb, mitu uut kannet luuakse. Kande summa jagatakse ühtlaselt uute kannetega. |
| **Ühik**              | Valige perioodile mõõtühik.                                                                                                                                                                  |
| **Perioodi intervall**   | Määrake sisestusperioodide vaheline intervall.                                                                                                                                                              |

Näiteks kvartalipõhiste sisestuste loomiseks sisestage väljale **Perioodide arv** väärtus **4**, valige väljal **Ühik** säte **Kuud** ja sisestage väljale **Perioodi intervall** väärtus **3**. Süsteem loob neli töölehe rida, iga rida on üks neljandik sisestatud töölehe rea summast iga 3 kuu järel. Sarnane funktsioon on saadaval ka päevaraamatu kohta. Päevaraamatu ridade vaatamisel valige **Perioodi tööraamat** &gt; **Salvesta tööraamat**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]