---
title: Pangakonto vastavusseviimise reeglite häälestus
description: Selles artiklis selgitatakse, kuidas seadistada vastavusseviimise vastendusreeglid ja vastavusseviimise vastendusreeglite komplektid, et aidata kaasa panga vastavusseviimise protsessile. Vastavusseviimise vastendusreeglid on komplekt kriteeriume, mida kasutatakse pangaväljavõtte ja pangadokumendi ridade filtreerimiseks vastavusseviimise protsessi ajal.
author: angelad116
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac5ab5e2bcb9a63bb52d5a74bd5e4b5db51ba603
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803933"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Pangakonto vastavusseviimise reeglite häälestus

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse, kuidas seadistada vastavusseviimise vastendusreeglid ja vastavusseviimise vastendusreeglite komplektid, et aidata kaasa panga vastavusseviimise protsessile. Vastavusseviimise vastendusreeglid on komplekt kriteeriume, mida kasutatakse pangaväljavõtte ja pangadokumendi ridade filtreerimiseks vastavusseviimise protsessi ajal.

Saate seadistada vastavusseviimise vastendusreeglid ja vastavusseviimise vastendusreeglite komplektid, et aidata kaasa panga vastavusseviimise protsessile. Vastavusseviimise vastavusse viimise reegel on kriteeriumite kogum, mida kasutatakse pangaväljavõtte ridade ja Dynamics 365 Finantsi pangakande ridade filtreerimiseks vastavusseviimise protsessi ajal. Kasutage vastavusseviimise vastendusreeglite seadistamiseks lehte **Vastavusseviimise vastendusreeglid**. Saate seadistada rohkem kui ühe vastendusreegli ja luua seejärel vastavusseviimise vastendusreeglite komplekti lehel **Vastavusseviimise vastavusreeglite komplektid**. 

> [!NOTE] 
> Panga vastavusseviimise vastendusreegleid kasutatakse elektroonilise pangaväljavõtte vastavusseviimiseks, kasutades ettemakse panga vastavusseviimist. 

Lehel **Vastavusseviimise vastendusreeglid** saate valida, milliseid toiminguid ja valikukriteeriume vastendusreegli käivitamisel kasutatakse. Väljagrupis **Tegevused** valige tegevus, mis tehakse siis, kui vastavusseviimise protsessi käigus käivitatakse vastendusreegel.  

Vaikimisi ühtivad vastavusse viimise reeglid esimese pangadokumendiga, mis vastab vastavusse viimise reegli kriteeriumitele. Kui reegli kriteeriumitele vastab mitu panga dokumenti, saab käsitsi sobitamise parameetri taotlemise sisse lülitada, kui avate **Sularaha ja pangahaldus > Häälestus > Sularaha ja pangahalduse parameetrid > Panga vastavusseviimine > Nõua käsitsi sobitamist, kui täpsemad panga vastavusseviimise reeglid leiavad mitu dokumenti, mis vastavad summale**.

> [!NOTE] 
> Valitud suvand määrab kuvatavad väljad.

| Tegevus | Kirjeldus   | Tegevuse valimisel saadaolevad valikukriteeriumid     |
|--------|---------------|----------------------------------------------------------|
| **Vastendamine pangadokumendiga**       | Looge kriteeriumid määramaks, kuidas pangadokumente ja pangaväljavõtte ridu vastendatakse, kui vastendusreegel käivitatakse lehelt **Panga vastavusseviimise tööleht** . Kanderead valitakse kiirkaartides seadistatud täiendavate kriteeriumide alusel. | <ul><li>**1.etapp: vastendusreegli määratlemine**– valige kriteeriumid määramaks, milliseid pangaväljavõtteid tuleks Finance’i pangakannetega vastendada.</li><li> **2. etapp (valikuline): valige väljavõtte read, millega vastendusreegleid käivitada:** rakendage filter, millisel väljavõttereal reegleid käivitada.</li></ul>                                       |
| **Tagasimaksmise väljavõtteridade tühjendamine** | Looge kriteeriumid määramaks, kuidas tagasimaksmise väljavõtteread tuleks vastendusreegli käivitamisel lehelt **Panga vastavusseviimise tööleht** eemaldada. Seda suvandit kasutatakse, kui pangatõrge põhjustab kahe pangaväljavõtte rea loetlemise imporditud pangaväljavõttes ja read tuleb vastavusse viia. |<ul><li> **1. etapp**:**tagasimaksmise väljavõtteridade leidmine**– lisage tagasimaksmise pangaväljavõtte ridade valimiseks valikukriteeriumid. Näiteks ainult **tšekkide**  **valimiseks** valige pangakande kood väljal Väli, valige plussmärk (+) **väljal Operaator**  **ja seejärel sisestage Tšekid**  **väljale** Väärtus. </li><li>**2. etapp: algsete väljavõtteridade leidmine** – saate lisada valikukriteeriumid pangadokumendi ridade vastavusse viimiseks pangaväljavõtte ridadega. </li><li>**3. etapp: Finance’i pangakannete leidmine**– saate lisada valikukriteeriumid Finance’i pangakannete vastavusse viimiseks pangaväljavõtte ridadega.</li></ul>  |
| **Uute kannete märkimine**          | Looge kriteeriumid määramaks, kuidas tuleks uusi kandeid vastendusreegli käivitamisel lehel **Panga vastavusseviimise tööleht** märkida.                                                                                                                                                                 | <ul><li>**1.etapp: väljavõtteridade leidmine**– lisage valikuvälju määramaks, millised pangaväljavõtte read tuleks lehelt **Panga vastavusseviimise tööleht** valida.</li><li> **2. etapp: otsige finantse ja**  toiminguid – saate pangadokumendi ridade otsimiseks lisada valikukriteeriume. Kui ühtegi pangadokumenti ei leita, märgitakse väljavõtterida uue kandena. </li></ul>         |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

