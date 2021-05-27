---
title: Otse tuletatud ja kindlad tellimused töödeldakse ülevaatuse töövooga
description: Otse tuletatud ja kindlad tellimused töödeldakse ülevaatuse töövooga.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026447"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Otse tuletatud ja kindlad tellimused töödeldakse ülevaatuse töövooga

KB number: 4612450

## <a name="symptoms"></a>Sümptomid

Otse tuletatud ja kindlad tellimused töödeldakse *ülevaatuse* töövooga.

## <a name="resolution"></a>Eraldusvõime

Kui juhtumi muudatuste jälgimine on lubatud, kuvatakse kindlad tuletatud tellimused (allhanke ostutellimused) olekuks *Ülevaatus*. Seega, kui ostutellimus on tuletatud (allhanke ostutellimus), on see esitatud ainult töövoole. Kui ostutellimus on kinnitatud kui plaanitud ostutellimus, kinnitatakse see automaatselt, kindlustamaks, et plaanimismootor ei looks uusi plaanitud tellimusi, kui ostutellimus on veel olekus *Mustand*.
