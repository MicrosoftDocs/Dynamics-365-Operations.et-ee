---
title: Kinnipeetav maks ostutehingutes
description: Hankijatele, kellele on kohustuslik kinnipeetav maks, saab määrata vaikimisi **Kinnipeetava maksu grupi** lehel **Kõik hankijad**.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 06c18e6b0779539a6da7ae7afbe000c4cfc78d9e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256663"
---
# <a name="withholding-tax-in-purchase-transactions"></a>Kinnipeetav maks ostutehingutes

Hankijatele, kellele on kohustuslik kinnipeetav maks, saab määrata vaikimisi **Kinnipeetava maksu grupi** lehel **Kõik hankijad**.

1. Avage **Navigeerimispaan > Moodulid > Ostureskontro > Hankijad > Kõik hankijad**.

2. Klõpsake vastavat hankija kontot ja seejärel käsku **Redigeeri**.

3. Seadke vahekaardil **Arve ja tarne** väli **Kinnipeetava maksu arvutamine** väärtusele **Jah**.

   > [!NOTE] 
   > Kinnipeetavat maksu ei arvutata, kui **Kinnipeetava maksu arvutamine** ei ole selle hankija jaoks sisse lülitatud.

4. Valige kinnipeetava maksu grupp loendist **Kinnipeetava maksu grupp**.

5. Klõpsake valikut **Salvesta**.

Kaupadele/teenustele, millelt kinnipeetav maks on kohustuslik, saate määrata vaikimisi **Kauba kinnipeetava maksu grupi** jaotises **Väljastatud tooted**.

1. Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.

2. Klõpsake vastavat üksuse numbrit ja seejärel käsku **Redigeeri**.

3. Klõpsake vahekaardil **Ost** käsku **Arvuta kinnipeetav maks**.

   > [!NOTE] 
   > Kinnipeetavat maksu ei arvutata, kui suvand **Arvuta kinnipeetav maks** ei ole määratud selle kauba jaoks olekusse **Jah** vahekaardil **Ost**, mis asub lehel **Väljastatud toode**.

4. Valige kauba kinnipeetava maksu grupp loendist **Kauba kinnipeetava maksu grupp**.

5. Klõpsake valikut **Salvesta**.

Kinnipeetava maksu gruppe ja kauba kinnipeetava maksu gruppe saab määrata järgmistel lehtedel. 

- **Ostutellimus**
- **Hankija arve**
- **Arve tööleht**

Kinnipeetava maksu grupi ja kauba kinnipeetava maksu grupi vaikeväärtused viiakse **Ostutellimuste** ja/või **Ootel hankija arvete** loomisel ridadele. **Hankija arve töölehe** korral võite lülitada suvandi **Kinnipeetava maksu arvutamine** sisse ja seejärel valida **Kauba kinnipeetava maksu grupi** töölehe vahekaardil **Üldine**.

Kinnipeetava maksu ajutine summa on saadaval lehe **Ostutellimus** vahekaardi **Kogusummad** väljal **Korrigeeritud kinnipeetav maks**.

![Kinnipeetav maks sisaldub ostutellimuses](media/withholding-tax-adjusted.png)

Kinnipeetav maks arvutatakse **Hankija makse töölehel**. Saate kohaldatavat kinnipeetava maksu koode ja ka tegelikku kinnipeetava maksu summasid käsitsi reguleerida vahekaardil **Kinnipeetav maks** lehel **Kannete tasakaalustamine**.

![Kinnipeetavat maksu saab käsitsi korrigeerida lehel Kannete tasakaalustamine](media/withholding-tax-vendor-payment-tab.png)

Saadud kinnipeetava maksu summa arvatakse hankija maksest maha ja sisestatakse seotud kande **Kinnipeetava maksu kontole**.

![Kinnipeetava maksu konto, kus kuvatakse seostuv kanne](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]