---
title: Maksete loomine kliendile, kellel on otsekorralduse load
description: See protseduur näitab, kuidas luua ISO20022 otsekorralduse maksefaili kliendile, kellel on konfigureeritud otsekorraldus ja tasumisele kuuluv arve.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 129c5291a29994f91ef325aa9b9a3b54a0e958d6
ms.sourcegitcommit: 807dec193cd163c9f5d949e744cfde40f2eb24b4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2468951"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Maksete loomine kliendile, kellel on otsekorralduse load

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas luua ISO20022 otsekorralduse maksefaili kliendile, kellel on konfigureeritud otsekorraldus ja tasumisele kuuluv arve. Arve loomine ja sisestamine on valikuline. Tasumisele kuuluva arve asemel võite valida töölehel loa enne maksefaili loomist, toetades kliendi ettemakse stsenaariumi.



Selle protseduuri loomiseks kasutatav demoandmete ettevõte on DEMF.



See on viies viiest protseduurist, mis näitab kliendi makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone. Enne selle toimingu lõpetamist tuleb lõpetada varasemad toimingud. Kõigepealt tuleb importida kliendimakse elektroonilise aruandluse konfiguratsioonid, konfigureerida makseviisid ning seadistada teie ettevõtte ja kliendi andmed. 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a>Otsekorralduse andmetega vabas vormis arve sisestamine
1. Avage Müügireskontro > Arved > Kõik vabas vormis arved.
2. Klõpsake valikut Uus.
3. Valige või sisestage väärtus väljal Kliendi konto.
    * Valige näiteks DE-010.  
4. Valige või sisestage väärtus väljal Makseviis.
    * Näide. valige Elektrooniline.  
5. Sisestage või valige väärtus väljal Otsekorralduse luba.
6. Klõpsake käsku Lisa rida.
7. Sisestage väärtus väljale Kirjeldus.
8. Täpsustage soovitud väärtusi väljal Põhikonto.
9. Sisestage arv väljale Ühiku hind.
10. Klõpsake valikut Sisesta.
11. Klõpsake nuppu OK.

## <a name="create-a-payment"></a>Makse loomine
1. Avage Müügireskontro > Maksed > Makse tööleht.
2. Klõpsake valikut Uus.
3. Sisestage või valige väärtus väljal Nimi.
4. Klõpsake valikut Read.
5. Klõpsake suvandit Maksesoovitus.
6. Klõpsake suvandit Loo maksesoovitus.
7. Jaotise kaasamiseks laiendage kirjeid.
8. Klõpsake käsku Filtreeri.
9. Valige loendist tabeli Kliendi kanded rida ja väli Makseviis.
    * Maksmiseks kliendi kannete valimisel võite rakendada mis tahes kriteeriumi. Selle näite puhul kasutage kannete filtreerimiseks makseviisi Elektrooniline.  
10. Sisestage või valige väärtus väljal Kriteeriumid.
11. Klõpsake nuppu OK.
12. Klõpsake nuppu OK.
13. Klõpsake suvandit Maksete loomine.
