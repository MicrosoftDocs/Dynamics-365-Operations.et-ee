---
title: Seadistage pangakonto vastavusseviimise reeglid
description: "Selles artiklis selgitatakse, kuidas seadistada vastavusseviimise vastendusreeglid ja vastavusseviimise vastendusreeglite komplektid, et aidata kaasa panga vastavusseviimise protsessile. Vastavusseviimise vastendusreeglid on komplekt kriteeriume, mida kasutatakse pangaväljavõtte ja pangadokumendi ridade filtreerimiseks vastavusseviimise protsessi ajal."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: fc3b12d05d6acb54a3868b67e1168188fcb12a6f
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Seadistage pangakonto vastavusseviimise reeglid

[!include[banner](../includes/banner.md)]


Selles artiklis selgitatakse, kuidas seadistada vastavusseviimise vastendusreeglid ja vastavusseviimise vastendusreeglite komplektid, et aidata kaasa panga vastavusseviimise protsessile. Vastavusseviimise vastendusreeglid on komplekt kriteeriume, mida kasutatakse pangaväljavõtte ja pangadokumendi ridade filtreerimiseks vastavusseviimise protsessi ajal.

Saate seadistada vastavusseviimise vastendusreeglid ja vastavusseviimise vastendusreeglite komplektid, et aidata kaasa panga vastavusseviimise protsessile. Vastavusseviimise vastendusreegel on komplekt kriteeriume, mida kasutatakse pangaväljavõtte ja Microsoft Dynamics 365 for Operationsi pangakande ridade filtrimiseks vastavusseviimise protsessi ajal. Kasutage vastavusseviimise vastendusreeglite seadistamiseks lehte **Vastavusseviimise vastendusreeglid**. Saate seadistada rohkem kui ühe vastendusreegli ja luua seejärel vastavusseviimise vastendusreeglite komplekti lehel **Vastavusseviimise vastavusreeglite komplektid**. 

> [!NOTE] 
> Panga vastavusseviimise vastendusreegleid kasutatakse elektroonilise pangaväljavõtte vastavusseviimiseks, kasutades ettemakse panga vastavusseviimist. 

Lehel **Vastavusseviimise vastendusreeglid** saate valida, milliseid toiminguid ja valikukriteeriume vastendusreegli käivitamisel kasutatakse. Väljagrupis **Tegevused** valige tegevus, mis tehakse siis, kui vastavusseviimise protsessi käigus käivitatakse vastendusreegel.  

> [!NOTE] 
> Valitud suvand määrab kuvatavad väljad.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tegevus**                         |                                                                                                                                                                                                                                                                                                               | **Tegevuse valimisel saadaolevad valikukriteeriumid**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Vastendamine pangadokumendiga**       | Looge kriteeriumid määramaks, kuidas pangadokumente ja pangaväljavõtte ridu vastendatakse, kui vastendusreegel käivitatakse lehelt **Panga vastavusseviimise tööleht** . Kanderead valitakse kiirkaartides seadistatud täiendavate kriteeriumide alusel.                                | **1. etapp: vastendamise reegli määratlemine** – valige kriteeriumid, et määrata, millised pangaväljavõtted tuleks rakenduse Dynamics 365 for Operations panga kannetega vastendada. **2. etapp (valikuline): valige väljavõtte read, millega vastendusreegleid käivitada:** rakendage filter, millisel väljavõttereal reegleid käivitada.                                                                                                                                                                                                                                                                                                               |
| **Tagasimaksmise väljavõtteridade tühjendamine** | Looge kriteeriumid määramaks, kuidas tagasimaksmise väljavõtteread tuleks vastendusreegli käivitamisel lehelt **Panga vastavusseviimise tööleht** eemaldada. Seda suvandit kasutatakse, kui pangatõrge põhjustab kahe pangaväljavõtte rea loetlemise imporditud pangaväljavõttes ja read tuleb vastavusse viia. | **1. etapp**:**tagasimaksmise väljavõtteridade leidmine**– lisage tagasimaksmise pangaväljavõtte ridade valimiseks valikukriteeriumid. Näiteks ainult tšekkide valimiseks valige väljalt Väli suvand **Pangakande kood**, valige plussmärk (+) väljalt **Tehtemärk** ja seejärel sisestage väljale Väärtus **Tšekid**. **2. etapp: algsete väljavõtteridade leidmine** – saate lisada valikukriteeriumid pangadokumendi ridade vastavusse viimiseks pangaväljavõtte ridadega. **3. etapp: rakenduse Dynamics 365 for Operations pangakannete leidmine ** – saate valida valikukriteeriumid, mille alusel vastendatakse rakenduse Dynamics 365 for Operations pangakanded pangaväljavõtte ridadega. |
| **Uute kannete märkimine**          | Looge kriteeriumid määramaks, kuidas tuleks uusi kandeid vastendusreegli käivitamisel lehel **Panga vastavusseviimise tööleht** märkida.                                                                                                                                                                 | **1.etapp: väljavõtteridade leidmine**– lisage valikuvälju määramaks, millised pangaväljavõtte read tuleks lehelt **Panga vastavusseviimise tööleht** valida. **2. etapp: Dynamics 365 for Operationsi pangakannete leidmine **– saate pangadokumendi ridadele valikukriteeriume lisada. Kui ühtegi pangadokumenti ei leita, märgitakse väljavõtterida uue kandena.                                                                                                                                                                                                                                             |

 







