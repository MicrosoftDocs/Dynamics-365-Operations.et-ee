---
title: Imporditööde kuupäeva ja kellaaja sünkroonimine
description: Kasutage imporditöödes ajavööndite teisendamise probleemide vältimiseks UTC ajavööndeid.
author: peakerbl
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8faa7b73349c48d3a02b685546b47c4969c6027
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109428"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Imporditööde kuupäeva ja kellaaja sünkroonimine

[!include [banner](../includes/banner.md)]

Oluline on määrata imporditöö ajavööndiks koordineeritud maailmaaeg (UTC). Erineva sätte kasutamisel võite näha imporditud andmetes ootamatuid kuupäevi ja kellaaegu. Ilma õige sätteta teisendab impordiprotsess UTC kuupäeva kohalikku vormingusse ja seejärel teisendavad süsteemisätted selle uuesti.

See topeltteisendus põhjustab rakenduste vahelise muutuse. Näiteks võib topeltteisendus põhjustada töötaja Dynamics 365 Human Resources alguskuupäeva ja Dynamics 365 Financei vahelise erinevuse tõttu kohalikes ajavööndites. Imporditöö seadmine UTC peale lahendab selle probleemi.

1. Dynamics 365 finantside ja toimingute puhul valige **andmehaldus**.

2. Valige suvand **Impordi projektid** ja valige seejärel projekt.

3. Suvandis **Allika kuupäevavorming** valige **CSV-Unicode**.

   [![Allika kuupäevavormingu muutmine UTC-le.](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Muutke suvandi **Ajavöönd** väärtuseks **Koordineeritud maailmaaja vöönd** ja muutke suvandi **Keel** väärtuseks **En-US**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

