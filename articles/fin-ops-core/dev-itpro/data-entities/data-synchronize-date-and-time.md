---
title: Imporditööde kuupäeva ja kellaaja sünkroonimine
description: Kasutage imporditöödes ajavööndite teisendamise probleemide vältimiseks UTC ajavööndeid.
author: Sunil-Garg
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f677767e12de3a1706bc4b956a70afe0d941caa0c70366fc47c6c136e617cd46
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770805"
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