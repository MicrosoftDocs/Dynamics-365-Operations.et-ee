---
title: Poolaasta kulumiarvestuse konventsiooni metoodika
description: Selles teemas kirjeldatakse meetodit, mida põhivarad kasutavad kulumi arvestamiseks, kasutades poolaasta reeglit, mis arvutab kuue kuu kulumi vara esimesel ja viimasel kasutusaastal.
author: moaamer
manager: Ann Beebe
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 55fb03cf08d8ec042aa8fb37fd1fb858d98279b1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442227"
---
# <a name="half-year-depreciation-convention-methodology"></a>Poolaasta kulumiarvestuse konventsiooni metoodika

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles teemas kirjeldatakse meetodit, mida kasutatakse põhivarade korral kulumi arvestamiseks poolaasta konventsiooni kasutades. Poolaasta konventsioon arvestab kuue kuu kulumi vara esimese ja viimase kasutusaasta jooksul. Lisateavet kulumiarvestuse konventsioonide kohta leiate jaotisest [Kulumimeetodid ja kulumiarvestusreeglid](Fixed-asset-depreciation-conventions.md). 

Kui kasutate kuue kuu kulumiarvestuse konventsiooni, kasutab süsteem soetusaastat või aastat, mil vara võeti kasutusse, seejärel arvestab viie aasta kulumi alates sellest aastast ja lisab seejärel kuus kuud. Selle protsessi näitlikustamiseks kasutage vara, mis soetati hinnaga 50 000 ja võeti kasutusele 2020. aasta aprillis. Samuti eeldage, et varal on viieaastane tööiga.

Esimene kasutusaasta lõppes 2020. aasta detsembris, mis tähendab, et vara viieaastane tööiga lõppeb 2024. aasta detsembris. Poolaasta kulumiarvestuse konventsioon lisab vara tööeale kuus kuud, mis tähendab, et selle tööiga lõpeb juunis 2025. 

> Aastane kulum: 50 000:5 = 10 000; igakuine kulum: 10000:12 = 833,33 <br>
> Esimese aasta kulum: 10 000:2 = 5 000; ja järgnev igakuine kulum: 5000:9 = 555,56

   [![Poolaasta kulumiarvestuse konventsiooni kulumiarvestuse ajakava](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)

Pikendatud kulumiperioodid, mis on lisatud pooleaastase konventsiooniga, võimaldavad kulumi täpsemat jaotamist. Kuuekuuline konventsioon kajastab kulumiarvestuse kulusid võrdsemalt, mis on kasulik kasumiaruande koostamiseks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]