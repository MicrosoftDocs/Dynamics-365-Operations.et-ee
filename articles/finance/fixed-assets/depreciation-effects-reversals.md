---
title: Tühistustega kulumiefektid
description: Selles artiklis käsitletakse põhivara kande ennitamise võimalikke mõjusid.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3c97690956b07a3a5708cfbf37c69f186073138
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995011"
---
# <a name="depreciation-effects-with-reversals"></a>Tühistustega kulumiefektid

[!include [banner](../includes/banner.md)]

Selles artiklis käsitletakse põhivara kande ennitamise võimalikke mõjusid. 

Põhivarakandeid, ja põhivaraga seotud kandeid saab tühistada. Samuti saab tühistada pöördkandeid. 

Saate tühistada kande, mis ei ole värskeim vara raamatusse sisestatud kanne. Peaksite kõigepealt välja selgitama, kas pärast tühistatavat kannet on sisestatud mõni kulumikanne. Seda seetõttu, et kulumit ei arvutata kande tühistamisel ümber. Seetõttu on kulum pärast tühistamist sageli suurendatud või vähendatud, nagu näidetest näha. 

Õige kulumi tagamiseks kande tühistamisel ärge jätkake tühistamisega, kui saate teate, mis ütleb, et kulumit ei arvutata ümber. Selle asemel tühistage esmalt kulumikanne, mis sisestati pärast kannet, mida üritasite tühistada, ja seejärel jätkake tühistamisega. Teid ei hoiatata kulumi ümberarvutamise eest ja saate tühistamisega jätkata. 

Järgmistes näidetes on arvutused, mis tehakse, kui jätkate pärast hoiatusteate saamist, kulumikandeid esmalt tühistamata.

## <a name="example-1-depreciation-is-overstated"></a> Näide 1. Kulumit on suurendatud
Vara seadistatakse 5-aastase kasuliku tööea ja lineaarse kulumiga (60 kulumiperioodi). Selles näites on kulumit suurendatud.
#### <a name="asset-transaction-history"></a>Vara kande ajalugu

| Kuupäev       | Kandetüüp                                                          | Summa                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| 1. jaanuar  | Soetamine                                                               | 59 000,00                                 |
| 1. jaanuar  | Soetuse korrigeerimine                                                    | 1 000,00                                  |
| 31. jaanuar | Kulum (arvutatud, kasutades ühe perioodi kulumisoovitust) | 1000.00 Arvutus: raamatupidamislik väärtus (59 000 + 1000 kulum) / järelejäänud kulumiperioodide arv (60) |

#### <a name="reversal-action"></a>Tühistustoiming

| Kuupäev      | Kande tüüp                | Summa    |
|-----------|---------------------------------|-----------|
| 1. jaanuar | Soetamise korrigeerimise tagasivõtmine | –1000,00 |

#### <a name="depreciation-effect"></a>Kulumi mõju

| Kuupäev        | Kande tüüp        | Summa                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| 28. veebruar | Kulum (soovitus) | 983.05 Arvutus: raamatupidamislik väärtus (59 000 – 1000 kulum) / järelejäänud kulumiperioodide arv (59) |

Kulumit on suurendatud 16,95 võrra (1000 - 983,05).

## <a name="example-2-depreciation-is-understated"></a> Näide 2. Kulumit on vähendatud
Vara seadistatakse 5-aastase kasuliku tööea ja lineaarse kulumiga (60 kulumiperioodi). Selles näites on kulumit vähendatud.
#### <a name="asset-transaction-history"></a>Vara kande ajalugu

| Kuupäev       | Kande tüüp                                                          | Summa                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| 1. jaanuar  | Soetus                                                               | 59 000,00                                   |
| 1. jaanuar  | Allahindlus                                                     | 1 000,00                                    |
| 31. jaanuar | Kulum (arvutatud, kasutades ühe perioodi kulumisoovitust) | 966.67 Arvutus: raamatupidamislik väärtus (59 000 – 1000 kulum) / järelejäänud kulumiperioodide arv (60) |

#### <a name="reversal-action"></a>Tühistustoiming

| Kuupäev      | Kande tüüp               | Summa    |
|-----------|--------------------------------|-----------|
| 1. jaanuar | Allahindluse tühistamine | –1000,00 |

#### <a name="depreciation-effect"></a>Kulumi mõju

| Kuupäev        | Kande tüüp        | Summa                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| 28. veebruar | Kulum (soovitus) | 983.62 Arvutus: raamatupidamislik väärtus (59 000 – 966.67 kulum) / järelejäänud kulumiperioodide arv (59) |

Kulumit on vähendatud 16,95 võrra (983,62 - 966,67).



<a name="additional-resources"></a>Lisaressursid
--------

[Põhivara kulum](fixed-asset-depreciation.md)



