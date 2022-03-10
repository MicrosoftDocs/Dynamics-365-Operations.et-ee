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
ms.openlocfilehash: c76eadc5839785ba1624ee3894ef1d0872369aa9
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403837"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Imporditööde kuupäeva ja kellaaja sünkroonimine

[!include [banner](../includes/banner.md)]

Oluline on määrata imporditöö ajavööndiks koordineeritud maailmaaeg (UTC). Erineva sätte kasutamisel võite näha imporditud andmetes ootamatuid kuupäevi ja kellaaegu. Ilma õige sätteta teisendab impordiprotsess UTC kuupäeva kohalikku vormingusse ja seejärel teisendavad süsteemisätted selle uuesti.

See topeltteisendus põhjustab rakenduste vahelise muutuse. Näiteks võib topeltteisenduse tõttu töötaja kuupäev olla erinevate kohalike ajavööndite tõttu rakendustes Dynamics 365 Human Resources ja Dynamics 365 Finance erinev. Imporditöö seadmine UTC peale lahendab selle probleemi.

1. Valige rakenduses Dynamics 365 Finance and Operations suvand **Andmehaldus**.

2. Valige suvand **Impordi projektid** ja valige seejärel projekt.

3. Suvandis **Allika kuupäevavorming** valige **CSV-Unicode**.

   [![Allika kuupäevavormingu muutmine UTC-le.](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Muutke suvandi **Ajavöönd** väärtuseks **Koordineeritud maailmaaja vöönd** ja muutke suvandi **Keel** väärtuseks **En-US**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
