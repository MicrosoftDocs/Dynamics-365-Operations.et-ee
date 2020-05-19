---
title: Plaanile filtrite rakendamine
description: Selles teemas selgitatakse, kuidas kasutada filtreid plaaniga, kui kasutatakse planeerimise optimeerimise funktsiooni.
author: ChristianRytt
manager: tfehr
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9ddf9934965bd06ec805731a1cc1a667846fa180
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323412"
---
# <a name="apply-filters-to-a-plan"></a>Plaanile filtrite rakendamine

[!include [banner](../../includes/banner.md)]

Planeerimise optimeerimise funktsiooni kasutamisel saate rakendada plaanile filtri. Suvand **Plaani filter** rakendatakse alati koondplaneerimise käivitamisel. Suvand **Plaani filter** on kasulik, kui soovite piiritleda plaani kindlale tootegrupile ja veenduda, et ükski teine kaup ei oleks tulemiks saadud koondplaneerimisse kaasatud.

Kui suvandit **Plaani filter** rakendatakse ja koondplaneerimise käivitamisel rakendatakse ka käitusaja filtrit, kaasatakse planeerimise käivitamisel ainult kahe filtri lõikuv osa.

Suvandile **Plaani filter** pääseb optimeerimise planeerimisel kasutamise ajal juurde suvandist **Koondplaanid**.

## <a name="example-scenario"></a>Näidisstsenaarium

Plaani filter on seadistatud hõlmama kaupu A, B ja C. Koondplaneerimise käitamine käivitatakse seejärel sama plaani jaoks, kuid rakendatakse erinevaid käitusaja filtreid.

- **Käitusaja filter, mis sisaldab kaupa D**: ühtegi kaupa ei ole planeeritud, kuna plaani filtri ja käitusaja filtri vahel pole lõikuvat osa.
- **Käitusaja filter, mis sisaldab kaupa A ja D**: planeerimise käivitamisel kaasatakse ainult kaup A, kuna kaup D pole plaani filtri osa.
- **Käitusaja filter, mis sisaldab kaupa B**: planeerimise käivitamisel kaasatakse ainult kaup B ja eelmise kauba A planeerimise väljund hoitakse alles.
- **Käitusaja filter, mis sisaldab kõiki kaupu (tühi filter)** : kaubad A, B ja C kaasatakse planeerimise käivitamisse ning kaupade A ja B eelmine planeerimise väljund kirjutatakse üle.

> [!NOTE]
> Peaksite vältima plaani filtri seadmist plaanile, mis on valitud kui **Praegune dünaamiline koondplaan** lehel **Koondplaneerimise parameetrid**. Vastasel juhul on dünaamilise koondplaani funktsioon piiratud filtreeritud kaupadega. Näiteks kui uuendatakse kauba netonõudeid, mis ei ole plaani filtri osaks, tulemusi ei looda.

## <a name="related-resources"></a>Seotud ressursid

[Planeerimise optimeerimise ülevaade](planning-optimization-overview.md)

[Planeerimise optimiseerimise kasutamise alustamine](get-started.md)

[Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)

[Plaani ajaloo ja plaanimise logide vaatamine](plan-history-logs.md)

[Planeerimistöö tühistamine](cancel-planning-job.md)
