---
title: Arvete ja võtmeandmete audit ostureskontros
description: See teema kirjeldab arvete ja võtmeandmete auditit ostureskontros.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: edb8799f8baf7b6ed775c73a1624abe794e692a3
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711516"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Arvete ja võtmeandmete audit ostureskontros

[!include [banner](../../includes/banner.md)]

Kui saate hankijalt ostutellimuse alusel arve kaupade või teenuste kohta, võivad äriprotsessid nõuda, et kaubad või teenused peavad enne arve makseks kinnitamist olema kätte saadud. Enne alustamist veenduge, et valitud on konfiguratsioonivõti Arvete vastendamine. 

Veenduge lehel **Ostureskontro parameetrid**, et valitud on suvand Lubage arvete võrdlemise kontrollimine, suvand **Nõua kinnitust** väljal **Lahknevustega arvete sisestamine** ning suvand **Kolmesuunaline vastavusse viimine** väljal **Rea vastavusse viimise poliitika**.

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
