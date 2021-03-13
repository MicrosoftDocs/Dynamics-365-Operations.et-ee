---
title: Nõudluse prognooside kohta varasemate andmete importimine
description: Täpsete nõudluse prognooside saamiseks on vaja varasemaid nõudluse andmeid kauba või kauba eraldamisvõtme kohta. Selles teemas selgitatakse, kuidas kasutada andmeüksusi varasemate nõudluse andmete importimiseks mis tahes süsteemist, et nõudluse prognoosi andmed oleksid olemas pikema perioodi kohta.
author: roxanadiaconu
manager: tfehr
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: d6ba2e1a3a884d29bff491f914aa2d5f9ece2b84
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154223"
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

## <a name="example"></a>Näide

Näitena saab kasutada järgmist faili. Laadige alla [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/). See fail sisaldab kauba D0001 varasema nõudluse andmeid. See sisaldab järgmisi kohustuslikke välju: laoala, kogus ja nõudluse kuupäev.

1. Valige ettevõtte, mille alla varasema nõudluse andmed importida.
2. Avage tööruum **Andmehaldus**.
3. Valige paan **Import**.
4. Sisestage impordiprojekti nimi, nt **Kauba D0001 varasema nõudluse importimine**.
5. Valige väljalt **Lähteandmete vorming** imporditava faili vorming. Selles näites valige faili HistoricalDemandData importimiseks **CSV**.
6. Tehke väljal **Üksuse nimi** valik **Varasem väline nõudlus**.
7. Salvestage fail arvutisse ja laadige see siis üles.
8. Valige **Impordi**.
9. Leht **Täitmise kokkuvõte** avaneb automaatselt. Kontrollige lehelt imporditud andmeid.

Pärast ajalooliste andmete importimist saate nõudluse prognoosi koostada.

## <a name="additional-resources"></a>Lisaressursid

[Statistilise alusprognoosi loomine](generate-statistical-baseline-forecast.md)  
[Andmete importimis- ja eksportimistööde ülevaade](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)
