---
title: "Nõudluse prognooside kohta varasemate andmete importimine"
description: "Täpsete nõudluse prognooside saamiseks on vaja varasemaid nõudluse andmeid kauba või kauba eraldamisvõtme kohta. Selles teemas selgitatakse, kuidas kasutada andmeüksusi varasemate nõudluse andmete importimiseks mis tahes süsteemist, et nõudluse prognoosi andmed oleksid olemas pikema perioodi kohta."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c46b659a0ecffd6180fd0a76ff1b8d228f121571
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="import-historical-data-for-demand-forecasts"></a>Nõudluse prognooside kohta varasemate andmete importimine

[!include[banner](../includes/banner.md)]

Nõudluse prognooside täpsuse tagamiseks peab varasemaid nõudluse andmeid olema kauba või kauba eraldamisvõtme kohta võimalikult palju. Kui varasemaid nõudluse andmeid pole veel imporditud, siis kasutage nende importimiseks andmeüksust **Varasem väline nõudlus** (ReqDemPlanHistoricalExternalDemandEntity) rakenduses Microsoft Dynamics 365 for Finance and Operations.

Tööruumis **Andmehaldus** näete ülevaadet kõigist üksuse väljadest.

1. Avage tööruum **Andmehaldus**.
2. Klõpsake paani **Andmeüksused**.
3. Otsige valiku **Varasem väline nõudlus** üksuste loendit.
4. Klõpsake valikut **Sihtväljad**. Järgmised üksuste väljad on kohustuslikud: laoala (**DeliveringSiteId**), kuupäev (**DemandDate**), kogus (**DemandQuantity**) ja kas kaubakood (**ItemNumber**) või kauba eraldamisvõti (**ProductAllocationKeyId**).

Andmeüksuse kasutamiseks peab teil olema Microsoft Exceli fail või komaeraldusega (CSV) fail, mis sisaldab varasema nõudluse andmeid. Järgmine näide selgitab andmete importimist CSV-failist.

## <a name="example"></a>Näide

Näitena saab kasutada järgmist faili. Laadige alla [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast). See fail sisaldab kauba D0001 varasema nõudluse andmeid. See sisaldab järgmisi kohustuslikke välju: laoala, kogus ja nõudluse kuupäev.

1. Valige ettevõtte, mille alla varasema nõudluse andmed importida.
2. Avage tööruum **Andmehaldus**.
3. Klõpsake paani **Impordi**.
4. Sisestage impordiprojekti nimi, nt **Kauba D0001 varasema nõudluse importimine**.
5. Valige väljalt **Lähteandmete vorming** imporditava faili vorming. Selles näites valige faili HistoricalDemandData importimiseks **CSV**.
6. Tehke väljal **Üksuse nimi** valik **Varasem väline nõudlus**.
7. Salvestage fail arvutisse ja laadige see siis üles.
8. Klõpsake nuppu **Impordi**.
9. Leht **Täitmise kokkuvõte** avaneb automaatselt. Kontrollige lehelt imporditud andmeid.

Pärast ajalooliste andmete importimist saate nõudluse prognoosi koostada.

## <a name="see-also"></a>Vt ka

[Statistilise alusprognoosi loomine](generate-statistical-baseline-forecast.md)

