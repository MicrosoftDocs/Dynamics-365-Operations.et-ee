---
title: Planeerimise optimiseerimise kasutamise alustamine
description: Selles teemas selgitatakse, kuidas hakata kasutama planeerimise optimeerimise funktsiooni.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773939"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a>Planeerimise optimiseerimise kasutamise alustamine

Planeerimise optimeerimise funktsioon ei toeta hetkel kõiki funktsioone, mis on Microsoft Dynamics 365 Supply Chain Managementi ehitatud planeerimismootoris saadaval. Seega on oluline, et hindaksite, kas hetkel planeerimise optimeerimises saadaolev funktsioonide komplekt vastab teie nõuetele. Vaikimisi ei ole planeerimise optimeerimise funktsioon portaalis Dynamics Lifecycle Services (LCS) sisse lülitatud. Seetõttu on teil võimalus teha oma hindamine enne selle sisselülitamist.

Lõpuks asendab planeerimise optimeerimine olemasoleva sisseehitatud tarneahela halduse planeerimismootori.

Enne planeerimise optimeerimise sisselülitamist soovitame teil hinnata planeerimise optimeerimise sobivuse analüüsi tulemusi. Lisateavet vt [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md).

### <a name="licensing"></a>Litsentsimine

Kui saate käivitada koondplaneerimise oma praegust litsentsi kasutades, ei pea te täiendavat litsentsi ostma, et hakata planeerimise optimeerimist kasutama.

### <a name="install-the-add-in"></a>Lisandmooduli installimine

Planeerimise optimeerimise kasutamiseks installige Dynamics 365 Supply Chain Managementi planeerimise optimeerimise lisandmoodul. Saate kasutada lisandmoodulit oma LCS projektist ja lülitada planeerimise optimeerimise funktsiooni sisse tarneahela halduse kasutajaliidesest.

1. Logige LCS-i sisse ja avage soovitud keskkond.
1. Avage **Kõik üksikasjad**.
1. Valige **Hooldamine** või kerige alla kiirkaardile **Keskkonna lisandmoodulid**.
1. Valige **Installi uus lisandmoodul**.
1. Valige **Planeerimise optimeerimine**.
1. Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.
1. Valige **Installi**.

### <a name="planning-optimization-integration"></a>Planeerimise optimeerimise integreerimine

Konfigureerimaks, kas planeerimise optimeerimise lisandmoodulit peaks koondplaneerimise jaoks kasutama, avage **Koondplaneerimine** \> **Seadistamine** \> **Planeerimise optimeerimise integreerimine** \> **Integreerimise parameetrid**.

#### <a name="connection-status"></a>Ühenduse olek

Ühenduse olek näitab tarneahela halduse ja planeerimise optimeerimise teenuse vahelise ühenduse hetkeolekut. Järgmine tabel näitab võimalikke väärtuseid.

| Ühenduse olek | Kirjeldus | Kas planeerimise optimeerimist saab kasutada? |
|---|---|---|
| Ühendus on loodud | Planeerimise optimeerimise teenuse ja tarneahela halduse vahel on loodud ühendus. | Jah |
| Ühenduse loomine | Planeerimise optimeerimise teenuse ühendamise sisselülitamise taotlus on praegu tööd. | Ei |
| Ühendus on katkestatud | Planeerimise optimeerimise teenusega puudub ühendus. Ühenduse saab lülitada sisse LCS-ist, nagu selles teemas varasemalt on kirjeldatud. | Ei |
| Ühenduse katkestamine | Planeerimise optimeerimise teenuse ühendamise väljalülitamise taotlus on praegu tööd. | Ei |
| Oleku hankimine | Süsteem ootab planeerimise optimeerimise teenuselt oleku teavet. | Ei |

#### <a name="the-use-planning-optimization-option"></a>Planeerimise optimeerimise kasutamise suvand

Suvandi **Planeerimise optimeerimise kasutamine** säte määrab, millist planeerimismootorit koondplaneerimiseks kasutatakse.

- **Jah** – planeerimise optimeerimist kasutatakse koondplaneerimiseks.
- **Ei** – koondplaneerimise jaoks kasutatakse sisseehitatud tarneahela halduse planeerimise mootorit.

> [!NOTE]
> Kui olemasoleva planeerimise paketi tööd, mis sisseehitatud tarneahela halduse planeerimismootori jaoks loodi, käivitatakse sel ajal, kui suvandi **Planeerimise optimeerimise kasutamine** väärtuseks on seatud **Jah**, siis need tööd nurjuvad.

### <a name="integration-with-the-setup"></a>Integreerimine seadistamisega

Kui planeerimise optimeerimise eelvaade on sisse lülitatud, tehakse koondplaneerimine planeerimise optimeerimise lisandmoodulit kasutades. Sel juhul on koondplaneerimise tulemused ja funktsioonid mõjutatud.

## <a name="related-resources"></a>Seotud ressursid

[Eelvaate tingimused ja nõuded](https://go.microsoft.com/fwlink/?linkid=2015274)

[Planeerimise optimeerimise ülevaade](planning-optimization-overview.md)

[Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)

[Plaani ajaloo ja plaanimise logide vaatamine](plan-history-logs.md)

[Plaanile filtrite rakendamine](plan-filters.md)

[Planeerimistöö tühistamine](cancel-planning-job.md)
