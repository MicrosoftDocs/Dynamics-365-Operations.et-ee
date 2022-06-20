---
title: Poolaasta kulumiarvestuse konventsiooni metoodika
description: See artikkel kirjeldab meetodit, mida põhivara kasutab kulumi arvutamiseks poolaastareeglite alusel, mille puhul arvutatakse vara esimesel ja eelmisel teenuseaastal kuus kuud kulumit.
author: moaamer
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: fac20f7a31eca7922ed079f9554437f28448620d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879591"
---
# <a name="half-year-depreciation-convention-methodology"></a>Poolaasta kulumiarvestuse konventsiooni metoodika

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles artiklis kirjeldatakse põhivarades kulumi arvutamiseks poolaastareeglite abil kasutatavat meetodit. Poolaasta konventsioon arvestab kuue kuu kulumi vara esimese ja viimase kasutusaasta jooksul. Lisateavet kulumiarvestuse konventsioonide kohta leiate jaotisest [Kulumimeetodid ja kulumiarvestusreeglid](Fixed-asset-depreciation-conventions.md). 

Kui kasutate kuue kuu kulumiarvestuse konventsiooni, kasutab süsteem soetusaastat või aastat, mil vara võeti kasutusse, seejärel arvestab viie aasta kulumi alates sellest aastast ja lisab seejärel kuus kuud. Selle protsessi näitlikustamiseks kasutage vara, mis soetati hinnaga 50 000 ja võeti kasutusele 2020. aasta aprillis. Samuti eeldage, et varal on viieaastane tööiga.

Esimene kasutusaasta lõppes 2020. aasta detsembris, mis tähendab, et vara viieaastane tööiga lõppeb 2024. aasta detsembris. Poolaasta kulumiarvestuse konventsioon lisab vara tööeale kuus kuud, mis tähendab, et selle tööiga lõpeb juunis 2025. 

> Aastane kulum: 50 000:5 = 10 000; igakuine kulum: 10000:12 = 833,33 <br>
> Esimese aasta kulum: 10 000:2 = 5 000; ja järgnev igakuine kulum: 5000:9 = 555,56

   [![Poolaasta kulumiarvestuse konventsiooni kulumiarvestuse ajakava.](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)

Pikendatud kulumiperioodid, mis on lisatud pooleaastase konventsiooniga, võimaldavad kulumi täpsemat jaotamist. Kuuekuuline konventsioon kajastab kulumiarvestuse kulusid võrdsemalt, mis on kasulik kasumiaruande koostamiseks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
