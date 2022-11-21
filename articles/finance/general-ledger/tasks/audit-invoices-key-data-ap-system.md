---
title: Arvete ja võtmeandmete audit ostureskontros
description: See artikkel näitab arvete ja ostureskontro põhiandmete auditit.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4525534f906322c7fe4c232f0f6da5b308829087
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775211"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Arvete ja võtmeandmete audit ostureskontros

[!include [banner](../../includes/banner.md)]

Kui saate hankijalt ostutellimuse alusel arve kaupade või teenuste kohta, võivad äriprotsessid nõuda, et kaubad või teenused peavad enne arve makseks kinnitamist olema kätte saadud. Enne alustamist veenduge, et valitud on konfiguratsioonivõti Arvete vastendamine. 

Veenduge, **et** ostureskontro parameetrite lehel on valitud suvand Luba arvete vastendamise kontrollimine, **·** **·** **·** **väli Sisesta lahknevustega arve on seatud valikule Nõua kinnitamist ja rea vastavusse viimise poliitika väli on seatud kolmepoolelisteks vastavusse viimiseks.** **·**

See protsess kasutab demoettevõtte USMF-i andmeid. Järgmiste sammude tegemiseks on vaja ostureskontro juhi või pearaamatupidaja rolli.


## <a name="create-a-purchase-order"></a>Ostutellimuse loomine
1. Avage valik **Kõik ostutellimused**.
2. Klõpsake **Uus**.
3. Sisestage väärtus väljale **Hankija konto**.
4. Klõpsake nupul **OK**.
5. Klõpsake käsku **Lisa rida**.
6. Sisestage väärtus väljale **Kaubakood**.
7. Klõpsake toimingupaanil valikut **Ost**.
8. Klõpsake käsku **Kinnita**.

## <a name="post-a-product-receipt"></a>Toote sissetuleku sisestamine
1. Klõpsake toimingupaanil valikut **Vastuvõtt**.
2. Klõpsake valikut **Toote sissetulek**.
3. Sisestage väärtus väljale **Toote sissetulek**.
4. Klõpsake nupul **OK**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Hankija arve salvestamine ja vastendamine toote sissetulekuga
1. Klõpsake toimingupaanil valikut **Arve > Arve**.
2. Sisestage väärtus väljale **Arv**.
3. Rippdialoogi avamiseks klõpsake valikut **Vaikimisi asukohast: tellitud kogus**.
4. Valige suvand väljal **Ridade vaikekogus**.
5. Klõpsake nupul **OK**.
6. Klõpsake nuppu **Jah**.
7. Klõpsake valikut **Toote sissetulekute vastendamine**.
8. Klõpsake nupul **OK**.
9. Klõpsake toimingupaanil valikut **Vaata üle**.
10. Klõpsake valikut **Vastanduvad üksikasjad**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
