--- 
title: "Arvete ja võtmeandmete audit ostureskontros"
description: "Kui saate hankijalt ostutellimuse alusel arve kaupade või teenuste kohta, võivad äriprotsessid nõuda, et kaubad või teenused peavad enne arve makseks kinnitamist olema kätte saadud."
author: saraschi2
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 38cc5587d970d05492638ed349484e6c002d5363
ms.contentlocale: et-ee
ms.lasthandoff: 07/28/2017

---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Arvete ja võtmeandmete audit ostureskontros

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


