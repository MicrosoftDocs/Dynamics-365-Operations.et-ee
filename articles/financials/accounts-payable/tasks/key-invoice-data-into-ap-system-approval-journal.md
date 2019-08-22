---
title: Arve põhiandmed AP-süsteemi, kasutades kinnitamise töölehte
description: Selles tegevuse juhises näitlikustatakse, kuidas kasutada arveregistrit arvete loomiseks ja seejärel kasutada kinnitamise töölehte kulukontode värskendamiseks.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0faece510cc85fd86113d8b62d54b71f3014b1db
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837033"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a>Arve põhiandmed AP-süsteemi, kasutades kinnitamise töölehte

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles tegevuse juhises näitlikustatakse, kuidas kasutada arveregistrit arvete loomiseks ja seejärel kasutada kinnitamise töölehte kulukontode värskendamiseks.


## <a name="create-and-post-and-invoice"></a>Arve loomine ja sisestamine
1. Avage Ostureskontro > Arved > Arveregister.
2. Klõpsake valikut Uus.
3. Valige selle arveregistri nimi, mida soovite kasutada.
4. Klõpsake loendis valitud real olevat linki.
5. Registri avamiseks ja kuluridade sisestamiseks klõpsake nuppu Read.
6. Valige hankija. Näiteks sisestage või valige US‑104
7. Sisestage väärtus väljale Arve.
8. Sisestage väärtus väljale Kirjeldus.
9. Sisestage arv väljale Kreedit.
10. Klõpsake väljal Kinnitaja otsingu avamiseks ripploendi nuppu.
11. Tõstke kinnitaja esile ja klõpsake nuppu Vali, et see kinnitaja valida.
12. Klõpsake valikut Sisesta.
13. Sulgege leht.
14. Sulgege leht.

## <a name="approve-an-invoice"></a>Arve heakskiitmine
1. Avage Ostureskontro > Arved > Arve kinnitamine.
2. Klõpsake valikut Uus.
3. Valige soovitud arve kinnitamise töölehe nimi.
4. Klõpsake loendis valitud real olevat linki.
5. Klõpsake valikud Read, et kuvada lehekülg, kus saate valida kinnitatavad arved.
6. Valige Kannete otsimine, et kuvada kõiki arveid, mis on kinnitamiseks valmis.
7. Märkige loodud arve.
8. Klõpsake Vali.
    * Ülal valitud kanded viiakse sellesse loendisse pärast nende valimist.  
9. Klõpsake nuppu OK.
10. Arvele kulukonto lisamiseks klõpsake kontonumbri väljal.
11. Sisestage kontonumber ja klõpsake väljapool välja. Näiteks sisestage 600120.
12. Klõpsake valikut Sisesta.
13. Sisestatud kannete kuvamiseks klõpsake valikut Kanne.
    * Kinnituse ootel arvete konto tühistatakse ja asendatakse tegeliku kulukontoga.  

