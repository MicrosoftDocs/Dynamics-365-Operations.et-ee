---
title: Makse tagasimaksete töötlemine
description: See protseduur näitab, kuidas teisendada kliendi kinnitatud ja töödeldud tagasimakseid kreeditarveteks.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2d97a59ae782af0a3d5ab71903961ef244a8e62
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570712"
---
# <a name="process-rebates-for-payment"></a>Makse tagasimaksete töötlemine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas teisendada kliendi kinnitatud ja töödeldud tagasimakseid kreeditarveteks. Saate seda juhendit kasutada demoettevõtte USMF andmetega. Selle juhendi eeltingimus on üks või mitu olemasolevat tagasimaksenõuet, mille olek on Märgi. USMF-i kasutamisel peate enne selle juhendi käivitamist käitama juhendit „Kliendi tagasimaksete loomine ja töötlemine”.


## <a name="convert-rebate-claims-to-credit-note"></a>Tagasimaksenõuete teisendamine kreeditarveks
1. Minge jaotisse Kõik kliendid.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake toimingupaanil suvandit Sissenõudmine.
5. Klõpsake suvandit Kannete tasakaalustamine.
6. Klõpsake suvandit Funktsioonid.
7. Klõpsake suvandit Tagasimakseprogramm.
    * Lehel Tagasimakse loetletakse tagasimaksenõuded, mida olete kliendi tagasimaksete töölaual töödelnud ja mille olek on Märgi.    
8. Klõpsake nuppu Redigeeri.
    * Märkige väli Märgi nende nõuete puhul, mille soovite kreeditarvesse kaasata.   
9. Klõpsake suvandit Funktsioonid.
10. Klõpsake suvandit Loo kreeditarve.
    * Kuvatakse teade, et tööleht on sisestatud (see on tööleht Müügireskontro tarbimine, nagu on määratud lehel Müügireskontro parameetrid). Selle tagajärjel teisaldatakse reaalkohustuse (krediidi) summa kliendi saldole. See tähendab, et kliendi konto on krediteeritud ja tagasimakse juurdekasvukonto on debiteeritud.  
11. Sulgege leht.
12. Klõpsake valikut Tühista.
    * See värskendab lehte, nii et näete värskendusi.  
13. Klõpsake toimingupaanil suvandit Sissenõudmine.
14. Klõpsake suvandit Kannete tasakaalustamine.
    * Pange tähele, et kliendi saldole on lisatud negatiivse summa kanne, mis tähistab tagasimakse kogusummat ilma arve viiteta.   
15. Klõpsake valikut Tühista.

