---
title: Prognoosi täpsuse jälgimine
description: Selles teemas kirjeldatakse, millist tüüpi prognoosi täpsust Dynamics 365 Supply Chain Management arvutab, ning selgitatakse, kuidas täpsuse väärtusi vaadata.
author: roxanadiaconu
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e6806b6d13d8c8e88cde52c444e684e6b40bbd77d3e5c6181ff5a49b183b8f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771440"
---
# <a name="monitor-forecast-accuracy"></a>Prognoosi täpsuse jälgimine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, millist tüüpi prognoosi täpsust Microsoft Dynamics 365 Supply Chain Management arvutab, ning selgitatakse, kuidas täpsuse väärtusi vaadata.

Supply Chain Management arvutab järgmised prognoosi täpsuse tüübid.

-   Ajalooline prognoosi täpsus, kus võrreldakse koondplaneerimises kasutatavat prognoosi ajaloolise nõudlusega. Ajaloolise prognoosi täpsuse väärtuste (nii absoluutsete väärtuste kui ka väärtuste protsendi) vaatamiseks klõpsake lehel **Nõudluse prognoosi üksikasjad** nuppu **Kuva täpsus**.
-   Prognooside loomisel kasutatud prognoosimudeli eeldatav täpsus. Saate vaadata täpsusprotsenti lehe **Nõudluse prognoosi üksikasjad** jaotisest **Mudeli üksikasjad – MAPE**. 

> [!NOTE]
> Kui kasutate nõudluse prognoosimise Microsoft Azure’i masinõpet, põhineb sisemise mudeli täpsuse arvutus katseandmete kogumil. Testandmete kogumi suuruse määramiseks seadke lehel **Nõudluse prognoosimise parameetrid** parameeter **TEST\_SET\_SIZE\_PERCENT**. Näiteks kui seate väärtuseks **20**, kasutatakse sisemise mudeli täpsuse arvutamiseks viimast 20% ajaloolistest andmetest.


## <a name="additional-resources"></a>Lisaressursid

[Korrigeeritud prognoosi autoriseerimine](authorize-adjusted-forecast.md)

[Nõudluse prognoosi arvutamisel võõrväärtuste eemaldamine kandeandmete ajaloost](remove-historical-outliers-calculating-demand-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]