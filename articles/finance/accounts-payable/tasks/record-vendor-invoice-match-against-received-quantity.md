---
title: Hankija arve kirjendamine ja sissetulnud kogusega vastendamine
description: Kui saate hankijalt ostutellimuse alusel arve kaupade või teenuste kohta, võivad äriprotsessid nõuda, et kaubad või teenused peavad enne arve makseks kinnitamist olema kätte saadud.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: debf8ca47666252633e67e2592acd5a4e4122403
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778545"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>Hankija arve kirjendamine ja sissetulnud kogusega vastendamine

[!include [banner](../../includes/banner.md)]

Kui saate hankijalt ostutellimuse alusel arve kaupade või teenuste kohta, võivad äriprotsessid nõuda, et kaubad või teenused peavad enne arve makseks kinnitamist olema kätte saadud. Enne alustamist veenduge, et valitud on konfiguratsioonivõti Arvete vastendamine. 

Veenduge, **et** ostureskontro parameetrite lehel on valitud suvand Luba arvete vastendamise kontrollimine, **·** **·** **·** **väli Sisesta lahknevustega arve on seatud valikule Nõua kinnitamist ja rea vastavusse viimise poliitika väli on seatud kolmepoolelisteks vastavusse viimiseks.** **·**

See protsess kasutab demoettevõtte USMF-i andmeid. Järgmiste sammude tegemiseks on vaja ostureskontro juhi või pearaamatupidaja rolli.


## <a name="create-a-purchase-order"></a>Ostutellimuse loomine
1. Avage valik **Kõik ostutellimused**.
2. Klõpsake valikut **Uus**.
3. Klõpsake väljal **Hankija konto** otsingu avamiseks ripploendi nuppu.
4. Sisestage väärtus väljale **Hankija konto**.
5. Klõpsake valikut **OK**.
6. Klõpsake käsku **Lisa rida**.
7. Sisestage väärtus väljale **Kaubakood**.
8. Klõpsake toimingupaanil valikut **Ost**.
9. Klõpsake käsku **Kinnita**.

## <a name="post-a-product-receipt"></a>Toote sissetuleku sisestamine
1. Klõpsake toimingupaanil valikut **Vastuvõtt**.
2. Klõpsake valikut **Toote sissetulek**.
3. Märkige loendis valitud rida.
4. Sisestage väärtus väljale **Toote sissetulek**.
5. Klõpsake valikut **OK**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Hankija arve salvestamine ja vastendamine toote sissetulekuga
1. Klõpsake toimingupaanil valikut **Arve**.
2. Klõpsake **Arve**.
3. Sisestage väärtus väljale **Arv**.
4. Rippdialoogi avamiseks klõpsake valikut **Vaikimisi asukohast: tellitud kogus**.
5. Valige suvand väljal **Ridade vaikekogus**.
6. Klõpsake nupul **OK**.
7. Klõpsake nuppu **Jah**.
8. Klõpsake valikut **Toote sissetulekute vastendamine**.
9. Klõpsake nupul **OK**.
10. Klõpsake toimingupaanil valikut **Vaata üle**.
11. Klõpsake valikut **Vastanduvad üksikasjad**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
