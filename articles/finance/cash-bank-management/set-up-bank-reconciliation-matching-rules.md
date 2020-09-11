---
title: Pangakonto vastavusseviimise reeglite seadistamine
description: Selles teemas selgitatakse, kuidas seadistada vastavusseviimise vastendusreeglid ja vastavusseviimise vastendusreeglite komplektid, et aidata kaasa panga vastavusseviimise protsessile. Vastavusseviimise vastendusreeglid on komplekt kriteeriume, mida kasutatakse pangaväljavõtte ja pangadokumendi ridade filtreerimiseks vastavusseviimise protsessi ajal.
author: panolte
manager: AnnBe
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2dcff7abfaf71c9e5e73ec2ffbdc1b377babdb2
ms.sourcegitcommit: 1daa297b0c09090a9c30c5f84bd7000e5b948a26
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/25/2020
ms.locfileid: "3720689"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Pangakonto vastavusseviimise reeglite seadistamine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas seadistada vastavusseviimise vastendusreeglid ja vastavusseviimise vastendusreeglite komplektid, et aidata kaasa panga vastavusseviimise protsessile. Vastavusseviimise vastendusreeglid on komplekt kriteeriume, mida kasutatakse pangaväljavõtte ja pangadokumendi ridade filtreerimiseks vastavusseviimise protsessi ajal.

Saate seadistada vastavusseviimise vastendusreeglid ja vastavusseviimise vastendusreeglite komplektid, et aidata kaasa panga vastavusseviimise protsessile. Vastavusseviimise vastendusreegel on komplekt kriteeriume, mida kasutatakse pangaväljavõtte ja Dynamics 365 Financei pangakande ridade filtreerimiseks vastavusseviimise protsessi ajal. Kasutage vastavusseviimise vastendusreeglite seadistamiseks lehte **Vastavusseviimise vastendusreeglid**. Saate seadistada rohkem kui ühe vastendusreegli ja luua seejärel vastavusseviimise vastendusreeglite komplekti lehel **Vastavusseviimise vastavusreeglite komplektid**. 

> [!NOTE] 
> Panga vastavusseviimise vastendusreegleid kasutatakse elektroonilise pangaväljavõtte vastavusseviimiseks, kasutades ettemakse panga vastavusseviimist. 

Lehel **Vastavusseviimise vastendusreeglid** saate valida, milliseid toiminguid ja valikukriteeriume vastendusreegli käivitamisel kasutatakse. Väljagrupis **Tegevused** valige tegevus, mis tehakse siis, kui vastavusseviimise protsessi käigus käivitatakse vastendusreegel.  

Vaikimisi ühtivad vastavusse viimise reeglid esimese pangadokumendiga, mis vastab vastavusse viimise reegli kriteeriumitele. Kui reegli kriteeriumitele vastab mitu panga dokumenti, saab käsitsi sobitamise parameetri taotlemise sisse lülitada, kui avate **Sularaha ja pangahaldus > Häälestus > Sularaha ja pangahalduse parameetrid > Panga vastavusseviimine > Nõua käsitsi sobitamist, kui täpsemad panga vastavusseviimise reeglid leiavad mitu dokumenti, mis vastavad summale**.

> [!NOTE] 
> Valitud suvand määrab kuvatavad väljad.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tegevus**                         |                                                                                                                                                                                                                                                                                                               | **Tegevuse valimisel saadaolevad valikukriteeriumid**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Vastendamine pangadokumendiga**       | Looge kriteeriumid määramaks, kuidas pangadokumente ja pangaväljavõtte ridu vastendatakse, kui vastendusreegel käivitatakse lehelt **Panga vastavusseviimise tööleht** . Kanderead valitakse kiirkaartides seadistatud täiendavate kriteeriumide alusel.                                | **1.etapp: vastendusreegli määratlemine**– valige kriteeriumid määramaks, milliseid pangaväljavõtteid tuleks Finance’i pangakannetega vastendada. **2. etapp (valikuline): valige väljavõtte read, millega vastendusreegleid käivitada:** rakendage filter, millisel väljavõttereal reegleid käivitada.                                                                                                                                                                                                                                                                                                               |
| **Tagasimaksmise väljavõtteridade tühjendamine** | Looge kriteeriumid määramaks, kuidas tagasimaksmise väljavõtteread tuleks vastendusreegli käivitamisel lehelt **Panga vastavusseviimise tööleht** eemaldada. Seda suvandit kasutatakse, kui pangatõrge põhjustab kahe pangaväljavõtte rea loetlemise imporditud pangaväljavõttes ja read tuleb vastavusse viia. | **1. etapp**:**tagasimaksmise väljavõtteridade leidmine**– lisage tagasimaksmise pangaväljavõtte ridade valimiseks valikukriteeriumid. Näiteks ainult tšekkide valimiseks valige väljalt Väli suvand **Pangakande kood**, valige plussmärk (+) väljalt **Tehtemärk** ja seejärel sisestage väljale Väärtus **Tšekid**. **2. etapp: algsete väljavõtteridade leidmine** – saate lisada valikukriteeriumid pangadokumendi ridade vastavusse viimiseks pangaväljavõtte ridadega. **3. etapp: Finance’i pangakannete leidmine**– saate lisada valikukriteeriumid Finance’i pangakannete vastavusse viimiseks pangaväljavõtte ridadega. |
| **Uute kannete märkimine**          | Looge kriteeriumid määramaks, kuidas tuleks uusi kandeid vastendusreegli käivitamisel lehel **Panga vastavusseviimise tööleht** märkida.                                                                                                                                                                 | **1.etapp: väljavõtteridade leidmine**– lisage valikuvälju määramaks, millised pangaväljavõtte read tuleks lehelt **Panga vastavusseviimise tööleht** valida. **2. etapp: Finance and Operations**i leidmine – saate lisada valikukriteeriumid pangadokumendi ridade otsimiseks. Kui ühtegi pangadokumenti ei leita, märgitakse väljavõtterida uue kandena.                                                                                                                                                                                                                                             |
