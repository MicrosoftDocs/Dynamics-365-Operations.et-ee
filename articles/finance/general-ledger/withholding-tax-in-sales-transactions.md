---
title: Kinnipeetav maks müügitehingutes
description: Selles teemas loetletakse valitud klientidele kinnipeetava maksu arvutamise vältimise etapid. Klientidele, kes määravad teile maksetes kinnipeetava maksu, saate määrata kinnipeetava maksu vaikegrupi.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8e11ce10faa9b450b6f36a856b34b06b4ee1838d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842340"
---
# <a name="withholding-tax-in-sales-transactions"></a>Kinnipeetav maks müügitehingutes

Selles teemas loetletakse valitud klientidele kinnipeetava maksu arvutamise vältimise etapid. Klientidele, kes määravad teile maksetes kinnipeetava maksu, saate määrata vaikimisi **Kinnipeetava maksu grupi** lehel **Kliendid**. 

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