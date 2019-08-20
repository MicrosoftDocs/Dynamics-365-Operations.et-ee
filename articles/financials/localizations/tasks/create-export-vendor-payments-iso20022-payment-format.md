---
title: Hankijamaksete loomine ja eksportimine ISO20022 maksevormingu abil
description: See protseduur näitab, kuidas luua makseridu hankija makse töölehel ja kuidas luua hankija maksefaili, kasutades ISO2022 kreeditülekande näidet.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b70ad94014587ba8e55735192dbe0ab2e4adf4ee
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848987"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Hankijamaksete loomine ja eksportimine ISO20022 maksevormingu abil

[!include [task guide banner](../../includes/task-guide-banner.md)]

See teema selgitab, kuidas luua makseridu hankija makse töölehel ja kuidas luua hankija maksefaili, kasutades ISO2022 kreeditülekande näidet.

See on viies viiest protseduurist, mis illustreerib hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone. Kasutage selle näite lõpuleviimiseks DEMF-i demoandmeid.

## <a name="example"></a>Näide

1.  Minge jaotisse **Ostureskontro > Maksed > Makse tööleht**.
2.  Klõpsake **Uus**.
3.  Sisestage või valige väärtus väljal **Nimi**.
4.  Klõpsake valikuid **Read > Maksesoovitus > Loo maksesoovitus**.
5.  Jaotise kaasamiseks laiendage valikut **Kirjed**.
6.  Klõpsake käsku **Filtreeri**.
7.  Valige loendist rida **tabelile Hankijad** ja **väljale Hankija konto**.
8.  Sisestage või valige väärtus väljal **Kriteeriumid**. Saate rakendada mis tahes kriteeriume makstavate hankija kannete valimiseks, selles näites kasutage hankija kontot DE-001.
12. Klõpsake nupul **OK**.
13. Klõpsake nupul **OK**.
14. Klõpsake suvandit **Maksete loomine**.
15. Looge ISO20022 maksefail.
    1.  Klõpsake suvandit **Loo maksed**.
    2.  Valige või sisestage väärtus väljal **Makseviis**.
    3.  Sisestage väärtus väljale **Faili nimi**. Selles näites on loodud fail euromakse tõttu SEPA-ga ühilduv. Maksete loomiseks muudes valuutades saab kasutada ni ISO20022 krediidiedastust kui ka muid hankija maksevorminguid.
    4.  Sisestage või valige väärtus väljal **Pangakonto**.

