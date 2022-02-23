---
title: Kliendi jaoks otsekorralduse loa loomine
description: See ülesande juhend näitab, kuidas luua otsekorralduse luba ja seda arvel kasutada.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86d29782f616219b5d84e3567910cb28c60b65ae
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442259"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Kliendi jaoks otsekorralduse loa loomine

[!include [banner](../../includes/banner.md)]

See ülesande juhend näitab, kuidas luua otsekorralduse luba ja seda arvel kasutada.


## <a name="create-a-bank-account"></a>Pangakonto loomine
1. **Navigeerimispaan** il avage **Moodulid > Müügireskontro > Kliendid > Kõik kliendid**.
2. Valige loendis kirje. Näiteks valige US-001
3. Toimingupaanil klõpsake **Klient**.
4. Klõpsake **Pangakontod**.
5. Klõpsake valikut **Uus**.
6. Sisestage väärtus väljale **Pangakonto**.
7. Sisestage väärtus väljale **Nimi**.
8. Sisestage väärtus väljale **IBAN**.
9. Sisestage väärtus väljale **Valuuta**.
10. Klõpsake valikut **Salvesta**.
11. Sulgege leht.
12. Paanil **Navigeerimispaan** avage **Moodulid > Sularaha- ja pangahaldus > Pangakontod > Pangakontod**.
13. Otsige loendist ja valige soovitud kirje.
14. Klõpsake loendis valitud real olevat linki.
15. Klõpsake valikut **Redigeeri**.
16. Laiendage kiirkaart **Täiendav identifitseerimine**.
17. Väljale **Otsedeebeti ID** sisestage väärtus.
18. Sisestage väärtus väljale **IBAN**.
19. Sulgege leht.
20. Sulgege leht.

## <a name="define-the-electronic-payment-method"></a>Elektroonilise makseviisi määratlemine
1. Paanil **Navigeerimispaan** avage **Moodulid > Müügireskontro > Maksete seadistamine > Makseviisid**.
2. Klõpsake valikut **Uus**.
3. Väljale **Makseviis** sisestage väärtus.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Väljale **Maksetüüp** sisestage "Elektrooniline makse". Makse tüübiks peab otsekorralduse loa makseviisi puhul olema elektrooniline makse.
6. Valige väärtus "Jah" väljal **Nõua luba**.
7. Sulgege leht.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Kliendile otsekorralduse loa lisamine.
1. **Navigeerimispaan** il avage **Moodulid > Müügireskontro > Kliendid > Kõik kliendid**.
2. Valige loendis kirje. Näiteks valige US-001
3. Klõpsake valikut **Redigeeri**.
4. Laiendage kiirkaart **Makse vaikeandmed**.
5. Valige või sisestage väärtus väljal **Makseviis**.
6. Laiendage kiirkaart **Makse vaikeandmed**.
7. Laiendage kiirkaart **Otsedeebeti load**.
8. Klõpsake käsku **Lisa**.
9. Sisestage või valige väärtus väljal **Pangakonto**.
10. Väljale **Kreeditori pangakonto** sisestage või valige väärtus.
11. Väljale **Makse sagedus** sisestage maksete arv, mida selle loa täitmiseks eeldate.
12. Klõpsake valikut **OK**.
13. Klõpsake **Prindi**.
14. Klõpsake **Loa aruanne**.
15. Sulgege leht.
16. Klõpsake valikut **Redigeeri**.
17. Väljale **Allkirjastamise kuupäev** sisestage kuupäev.
18. Klõpsake nuppu **Jah**.
19. Sisestage asukoht, kus luba allkirjastati.
20. Klõpsake valikut **OK**.
21. Sulgege leht.

## <a name="create-a-free-text-invoice-with-mandate"></a>Vabas vormis arve loomine loaga
1. Paanil **Navigeerimispaan** avage **Moodulid > Müügireskontro > Arved > Kõik vaba tekstiga arved**.
2. Klõpsake valikut **Uus**.
3. Valige klient, kellele loa lisasite.
4. Väljale **Otsedeebeti loa ID** sisestage või valige väärtus.

