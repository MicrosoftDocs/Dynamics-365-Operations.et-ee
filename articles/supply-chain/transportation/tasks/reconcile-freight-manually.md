--- 
title: "Veose käsitsi vastavusseviimine"
description: "See protseduur näitab, kuidas veost käsitsi tasakaalustada."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench, TMSFreightBillDetail, TMSInvoiceTable, TMSFreightBillInvoiceReconcile, TMSInvoiceJournal, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 15148725664d839694ede8419213d881c7be83dd
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="reconcile-freight-manually"></a>Veose käsitsi vastavusseviimine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas veost käsitsi tasakaalustada. Seda teeb üldjuhul transpordikoordinaator. Saate seda protseduuri kasutada demoandmete ettevõttes USMF.


## <a name="select-a-load-to-reconcile"></a>Valige vastavusseviimiseks koorem
1. Avage Transpordihaldus > Plaanimine > Koorma plaanimise töölaud.
2. Tühjendage märkeruut Peida saadetud ja vastuvõetud. 
3. Valige loendist koorem, mille koorma ID on 00006.

## <a name="create-a-carrier-invoice"></a>Vedaja arve loomine
    * Kui viite veose käsitsi vastavusse ega saa automaatselt vedaja arveid, võite luua arve veoarve põhjal.  
1. Klõpsake valikut Seostuv teave.
2. Klõpsake valikut Veoarve üksikasjad.
3. Klõpsake valikut Veoarve loomine.
4. Sisestage väärtus väljale Arve.
5. Klõpsake nuppu OK.

## <a name="reconcile-the-invoice"></a>Arve vastavusseviimine
    * Vedaja arve ja veoarve tasakaalustamisel tehakse seda reakaupa.  
1. Klõpsake valikut Vastenda veoarved ja arved.
2. Laiendage jaotist Arve üksikasjad.
3. Laiendage jaotist Vastendamata veoarve üksikasjad.
4. Märkige loendis valitud rida.
5. Klõpsake nuppu Vastenda.
6. Laiendage jaotist Vastendatud veoarve üksikasjad.

## <a name="submit-the-invoice-for-approval"></a>Esita arve kinnitamiseks
1. Klõpsake valikut Edasta kinnitamiseks.
2. Sulgege leht.
3. Tühjendage märkeruut Peida kinnitatud üksused. 
4. Klõpsake nuppu Hankijaarvete töölehed.
5. Klõpsake linki väljal Viitetöölehe number.
6. Klõpsake valikut Read.


