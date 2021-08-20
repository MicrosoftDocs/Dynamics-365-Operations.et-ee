---
title: Hankija arve kirjendamine ja sissetulnud kogusega vastendamine
description: Kui saate hankijalt ostutellimuse alusel arve kaupade või teenuste kohta, võivad äriprotsessid nõuda, et kaubad või teenused peavad enne arve makseks kinnitamist olema kätte saadud.
author: ShivamPandey-msft
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 352e188dcd25b486a1284be6958f44a5543f222c358153557366f9bdcc209f05
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722907"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Hankija arve kirjendamine ja sissetulnud kogusega vastendamine

[!include [banner](../../includes/banner.md)]

Kui saate hankijalt ostutellimuse alusel arve kaupade või teenuste kohta, võivad äriprotsessid nõuda, et kaubad või teenused peavad enne arve makseks kinnitamist olema kätte saadud. Enne alustamist veenduge, et valitud on konfiguratsioonivõti Arvete vastendamine. 

Veenduge lehel Ostureskontro parameetrid, et valitud on suvand Lubage arvete võrdlemise kontrollimine, suvand Nõua kinnitust väljal Lahknevustega arvete sisestamine ning suvand Kolmesuunaline vastavusse viimine väljal Rea vastavusse viimise poliitika.

See protsess kasutab demoettevõtte USMF-i andmeid. Järgmiste sammude tegemiseks on vaja ostureskontro juhi või pearaamatupidaja rolli.


## <a name="create-a-purchase-order"></a>Ostutellimuse loomine
1. Avage valik Kõik ostutellimused.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.
4. Sisestage väärtus väljale Hankija konto.
5. Klõpsake nuppu OK.
6. Klõpsake käsku Lisa rida.
7. Sisestage väärtus väljale Kaubakood.
8. Klõpsake toimingupaanil valikut Ost.
9. Klõpsake käsku Kinnita.

## <a name="post-a-product-receipt"></a>Toote sissetuleku sisestamine
1. Klõpsake toimingupaanil valikut Vastuvõtt.
2. Klõpsake valikut Toote sissetulek.
3. Märkige loendis valitud rida.
4. Sisestage väärtus väljale Toote sissetulek.
5. Klõpsake nuppu OK.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Hankija arve salvestamine ja vastendamine toote sissetulekuga
1. Klõpsake toimingupaanil valikut Arve.
2. Klõpsake valikut Arve.
3. Sisestage väärtus väljale Arv.
4. Rippdialoogi avamiseks klõpsake valikut Vaikimis asukohast: tellitud kogus.
5. Valige suvand väljal Ridade vaikekogus.
6. Klõpsake nuppu OK.
7. Klõpsake nuppu Jah.
8. Klõpsake valikut Toote sissetulekute vastendamine.
9. Klõpsake nuppu OK.
10. Klõpsake toimingupaanil valikut Vaata üle.
11. Klõpsake valikut Vastanduvad üksikasjad.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]