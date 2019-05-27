---
title: Kliendi jaoks otsekorralduse loa loomine
description: See ülesande juhend näitab, kuidas luua otsekorralduse luba ja seda arvel kasutada.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc3052fdfc6e3dcf2826b3069f6d644201a70c3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572531"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Kliendi jaoks otsekorralduse loa loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See ülesande juhend näitab, kuidas luua otsekorralduse luba ja seda arvel kasutada.


## <a name="create-a-bank-account"></a>Pangakonto loomine
1. Avage Müügireskontro > Kliendid > Kõik kliendid.
2. Näiteks valige US-001
3. Klõpsake toimingupaanil suvandit Klient.
4. Klõpsake valikut Pangakontod.
5. Klõpsake valikut Uus.
6. Sisestage väärtus väljale Pangakonto.
7. Sisestage väärtus väljale Nimi.
8. Sisestage väärtus väljale IBAN.
9. Sisestage väärtus väljale Valuuta.
10. Klõpsake nuppu Salvesta.
11. Sulgege leht.
12. Avage Sularaha- ja pangahaldus > Pangakontod > Pangakontod.
13. Otsige loendist ja valige soovitud kirje.
14. Klõpsake loendis valitud real olevat linki.
15. Klõpsake nuppu Redigeeri.
16. Laiendage jaotist Täiendav identifitseerimine.
17. Tippige väärtus väljale Otsekorralduse ID.
18. Sisestage väärtus väljale IBAN.
19. Sulgege leht.
20. Sulgege leht.

## <a name="define-the-electronic-payment-method"></a>Elektroonilise makseviisi määratlemine
1. Avage Müügireskontro > Maksete seadistus > Makseviisid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Makseviis.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Makse tüübiks peab otsekorralduse loa makseviisi puhul olema elektrooniline makse.
6. Valige väljal Nõua luba suvand Jah.
7. Sulgege leht.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Kliendile otsekorralduse loa lisamine.
1. Avage Müügireskontro > Kliendid > Kõik kliendid.
2. Näiteks valige US-001
3. Klõpsake nuppu Redigeeri.
4. Laiendage jaotist Makse vaikeandmed.
5. Valige või sisestage väärtus väljal Makseviis.
6. Laiendage jaotist Makse vaikeandmed.
7. Laiendage jaotist Otsekorralduse load.
8. Klõpsake vahekaarti Lisa.
9. Sisestage väärtus väljale Pangakonto või valige see.
10. Sisestage väärtus väljale Kreeditori pangakonto või valige see.
11. Sisestage maksete arv, mille loodate selle loa puhul töödelda.
12. Klõpsake nuppu OK.
13. Klõpsake Prindi.
14. Klõpsake suvandit Loa aruanne.
15. Sulgege leht.
16. Klõpsake nuppu Redigeeri.
17. Sisestage kuupäev väljale Allkirjastamise kuupäev.
18. Klõpsake nuppu Jah.
19. Sisestage asukoht, kus luba allkirjastati.
20. Klõpsake nuppu OK.
21. Sulgege leht.

## <a name="create-a-free-text-invoice-with-mandate"></a>Vabas vormis arve loomine loaga
1. Avage Müügireskontro > Arved > Kõik vabas vormis arved.
2. Klõpsake valikut Uus.
3. Valige klient, kellele loa lisasite.
4. Sisestage või valige väärtus väljal Otsekorralduse luba.

