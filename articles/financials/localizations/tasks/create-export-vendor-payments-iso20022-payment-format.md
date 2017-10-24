--- 
title: Hankijamaksete loomine ja eksportimine ISO20022 maksevormingu abil
description: "See protseduur näitab, kuidas luua makseridu hankija makse töölehel ja kuidas luua hankija maksefaili, kasutades ISO2022 kreeditülekande näidet."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc90bc86cd489b124a806c480632dd53ba47f3f
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Hankijamaksete loomine ja eksportimine ISO20022 maksevormingu abil

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas luua makseridu hankija makse töölehel ja kuidas luua hankija maksefaili, kasutades ISO2022 kreeditülekande näidet. 

Selle protseduuri loomiseks kasutatav demoandmete ettevõte on DEMF.

See on viies viiest protseduurist, mis illustreerib hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="create-payment-lines"></a>Makseridade loomine
1. Avage Ostureskontro > Maksed > Makse tööleht.
2. Klõpsake valikut Uus.
3. Märkige loendis valitud rida.
4. Sisestage või valige väärtus väljal Nimi.
5. Klõpsake valikut Read.
6. Klõpsake suvandit Maksesoovitus.
7. Klõpsake suvandit Loo maksesoovitus.
8. Jaotise kaasamiseks laiendage kirjeid.
9. Klõpsake käsku Filtreeri.
10. Valige loendist rida tabelile Hankijad ja väljale Hankija konto.
11. Sisestage või valige väärtus väljal Kriteeriumid.
    * Saate rakendada mis tahes kriteeriume makstavate hankija kannete valimiseks, selles näites kasutage hankija kontot DE-001.  
12. Klõpsake nuppu OK.
13. Klõpsake nuppu OK.
14. Klõpsake suvandit Maksete loomine.

## <a name="generate-an-iso20022-payment-file"></a>ISO20022 maksefaili loomine


