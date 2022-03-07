---
title: Kulumiarvutuste ümardatav summa
description: See artikkel käsitleb kulumi ümardamise välja raamatu seadistamise lehtedel.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetDepBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 13931
ms.assetid: faf7db87-046f-41d1-9baf-0df66e373e97
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01c8662f0731abd089c9039c16bb77e39c1d3e51
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976011"
---
# <a name="round-off-amount-for-depreciation-calculations"></a>Kulumiarvutuste ümardatav summa

[!include [banner](../includes/banner.md)]

See artikkel käsitleb kulumi ümardamise välja raamatu seadistamise lehtedel.

Kulumi ümardamise summad seadistatakse igale raamatule. Kulumi ümardamise summasid kasutatakse põhivara kulumireeglites, kus näidatakse edaspidist kulumit ja põhivara väärtust, samuti kulumisoovitustes. Sisestage väikseim raamatu puhul lubatud kulumisumma. 

Olenemata ümardamise seadistusest ei ümardata viimase kulumiperioodi kulumisummat. Viimase kulumiperioodi lõpus peab põhivara väärtus olema 0 (null) või mahakandmismaksumus, kui mahakandmismaksumust kasutatakse.

### <a name="example"></a>Näide

Kulum ilma ümardamiseta arvutatakse kui 2444,44. Nagu tabelist näha, varieeruvad pakutavad summad olenevalt ümardamise seadistustest.

| Ümardamismeetod | Kulumisumma |
|-----------------|---------------------|
| Ümardamine 0,1    | 2444,40            |
| Ümardamine 1,00   | 2444,00            |
| Ümardamine 10,00  | 2440,00            |
| Ümardamine 100,00 | 2400,00            |





