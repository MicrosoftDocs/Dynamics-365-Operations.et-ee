---
title: Kinnipeetav maks müügitehingutes
description: Selles artiklis loetletakse valitud klientide kinnipeetava maksu arvutamise vältimise etapid. Klientidele, kes määravad teile maksetes kinnipeetava maksu, saate määrata kinnipeetava maksu vaikegrupi.
author: kailiang
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 75a7fc62c1d493007f3aa88a723465828c557df7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910080"
---
# <a name="withholding-tax-in-sales-transactions"></a>Kinnipeetav maks müügitehingutes

Selles artiklis loetletakse valitud klientide kinnipeetava maksu arvutamise vältimise etapid. Klientidele, kes määravad teile maksetes kinnipeetava maksu, saate määrata vaikimisi **Kinnipeetava maksu grupi** lehel **Kliendid**. 

1. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Kliendid > Kõik kliendid**.

2. Klõpsake vastavat kliendikontot ja seejärel käsku **Redigeeri**.

3. Seadke vahekaardil **Arve ja tarne** väli **Kinnipeetava maksu arvutamine** väärtusele **Jah**.

   > [!NOTE] 
   > Kinnipeetavat maksu ei arvutata, kui **Kinnipeetava maksu arvutamine** ei ole selle kliendi jaoks koondandmetes sisse lülitatud.

4. Valige kinnipeetava maksu grupp loendist **Kinnipeetava maksu grupp**.

5. Klõpsake valikut **Salvesta**.

Kaupadele/teenustele, millelt kinnipeetav maks on kohustuslik, saate määrata vaikimisi **Kauba kinnipeetava maksu grupi** jaotises **Väljastatud tooted**.

1. Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.

2. Klõpsake vastavat üksuse numbrit ja seejärel käsku **Redigeeri**.

3. Klõpsake vahekaardil **Müük** käsku **Arvuta kinnipeetav maks**.

   > [!NOTE] 
   > Kinnipeetavat maksu ei arvutata, kui suvand **Arvuta kinnipeetav maks** ei ole määratud selle kauba jaoks olekusse **Jah** vahekaardil **Müük**, mis asub lehel **Väljastatud toode**.

4. Valige kauba kinnipeetava maksu grupp loendist **Kauba kinnipeetava maksu grupp**.

5. Klõpsake valikut **Salvesta**.

Kinnipeetava maksu gruppe ja kauba kinnipeetava maksu gruppe saab määrata lehel **Müügitellimus**. 

Vaikimisi kinnipeetava maksu gruppi ja kauba kinnipeetava maksu gruppi kasutatakse vaikekirjetena müügitellimuse ridadel uut müügitellimust luues.

Kinnipeetav maks arvutatakse ja sisestatakse koos **Kliendi makse töölehega**. Saate kohaldatavat kinnipeetava maksu koodi ja ka tegelikku kinnipeetava maksu summat käsitsi reguleerida vahekaardil **Kinnipeetav maks** lehel **Kannete tasakaalustamine**.

Arvutatud kinnipeetava maksu summa arvatakse kliendimaksest maha ja sisestatakse seotud kande **Kinnipeetava maksu** vastaskontole.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
