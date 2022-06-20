---
title: Hankijamaksete loomine ja eksportimine ISO20022 maksevormingu abil
description: See protseduur näitab, kuidas luua makseridu hankija makse töölehel ja kuidas luua hankija maksefaili, kasutades ISO2022 kreeditülekande näidet.
author: mrolecki
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ac84055586eff678ea489b35198b1c2dfab13658
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856463"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Hankijamaksete loomine ja eksportimine ISO20022 maksevormingu abil

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas luua makseridu hankija makse töölehel ja luua hankija maksefail ISO2022 krediidiülekande näite abil.

See on viies viiest protseduurist, mis illustreerib hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone. Kasutage selle näite lõpuleviimiseks DEMF-i demoandmeid.

## <a name="example"></a>Näide

1.    Minge jaotisse **Ostureskontro > Maksed > Makse tööleht**.
2.    Klõpsake **Uus**.
3.    Sisestage või valige väärtus väljal **Nimi**.
4.    Klõpsake valikuid **Read > Maksesoovitus > Loo maksesoovitus**.
5.    Jaotise kaasamiseks laiendage valikut **Kirjed**.
6.    Klõpsake käsku **Filtreeri**.
7.    Valige loendist rida **tabelile Hankijad** ja **väljale Hankija konto**.
8.    Sisestage või valige väärtus väljal **Kriteeriumid**. Saate rakendada mis tahes kriteeriume makstavate hankija kannete valimiseks, selles näites kasutage hankija kontot DE-001.
12.    Klõpsake nupul **OK**.
13.    Klõpsake nupul **OK**.
14.    Klõpsake suvandit **Maksete loomine**.
15. Looge ISO20022 maksefail.
    1.    Klõpsake suvandit **Loo maksed**.
    2.    Valige või sisestage väärtus väljal **Makseviis**.
    3.    Sisestage väärtus väljale **Faili nimi**. Selles näites on loodud fail euromakse tõttu SEPA-ga ühilduv. Maksete loomiseks muudes valuutades saab kasutada ni ISO20022 krediidiedastust kui ka muid hankija maksevorminguid.
    4.    Sisestage või valige väärtus väljal **Pangakonto**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]