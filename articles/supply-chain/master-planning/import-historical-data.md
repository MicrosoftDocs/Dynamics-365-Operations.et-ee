---
title: Nõudluse prognooside kohta varasemate andmete importimine
description: Täpsete nõudluse prognooside saamiseks on vaja varasemaid nõudluse andmeid kauba või kauba eraldamisvõtme kohta. Selles teemas selgitatakse, kuidas kasutada andmeüksusi varasemate nõudluse andmete importimiseks mis tahes süsteemist, et nõudluse prognoosi andmed oleksid olemas pikema perioodi kohta.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301646"
---
# <a name="import-historical-data-for-demand-forecasts"></a>Nõudluse prognooside kohta varasemate andmete importimine

[!include [banner](../includes/banner.md)]

Nõudluse prognooside täpsuse tagamiseks peab varasemaid nõudluse andmeid olema kauba või kauba eraldamisvõtme kohta võimalikult palju. Kui varasemaid nõudluse andmeid pole veel imporditud, siis kasutage nende importimiseks andmeüksust **Varasem väline nõudlus** (ReqDemPlanHistoricalExternalDemandEntity) rakenduses Dynamics 365 Supply Chain Management.

Tööruumis **Andmehaldus** näete ülevaadet kõigist üksuse väljadest.

1. Avage tööruum **Andmehaldus**.
2. Valige paan **Andmeüksused**.
3. Otsige valiku **Varasem väline nõudlus** üksuste loendit.
4. Valige **Sihtväljad**. Järgmised üksuste väljad on kohustuslikud: laoala (**DeliveringSiteId**), kuupäev (**DemandDate**), kogus (**DemandQuantity**) ja kas kaubakood (**ItemNumber**) või kauba eraldamisvõti (**ProductAllocationKeyId**).

Andmeüksuse kasutamiseks peab teil olema Microsoft Exceli fail või komaeraldusega (CSV) fail, mis sisaldab varasema nõudluse andmeid. Järgmine näide selgitab andmete importimist CSV-failist.

Lisateavet andmete importimise kohta, sh kuidas andmed pärast importimist korrastada, vt jaotisest [Andmete importimis- ja eksportimistööde ülevaade](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) ja sellega seotud teemadest.

Vt ka [Statistilise alusprognoosi loomine](generate-statistical-baseline-forecast.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]