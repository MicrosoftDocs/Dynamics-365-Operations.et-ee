---
title: Makse tagasimaksete töötlemine
description: See protseduur näitab, kuidas teisendada kliendi kinnitatud ja töödeldud tagasimakseid kreeditarveteks.
author: omulvad
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89848d9a5258fcb40f863261a6ba5d067296182989f0d10eb48b8e2a7dec008a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781778"
---
# <a name="process-rebates-for-payment"></a>Makse tagasimaksete töötlemine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas teisendada kliendi kinnitatud ja töödeldud tagasimakseid kreeditarveteks. Saate seda juhendit kasutada demoettevõtte USMF andmetega. Selle juhendi eeltingimus on üks või mitu olemasolevat tagasimaksenõuet, mille olek on Märgi. USMF-i kasutamisel peaksite enne selle juhendi käivitamist käitama juhendit „Kliendi tagasimaksete loomine ja töötlemine”.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]