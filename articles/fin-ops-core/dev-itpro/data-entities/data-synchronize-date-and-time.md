---
title: Imporditööde kuupäeva ja kellaaja sünkroonimine
description: Kasutage imporditöödes ajavööndite teisendamise probleemide vältimiseks UTC ajavööndeid.
author: Sunil-Garg
manager: tfehr
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
ms.openlocfilehash: 5ce3bf39e8342d3fe19a253f6d17684b2bd0aec0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570475"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Imporditööde kuupäeva ja kellaaja sünkroonimine

[!include [banner](../includes/banner.md)]

Oluline on määrata imporditöö ajavööndiks koordineeritud maailmaaeg (UTC). Erineva sätte kasutamisel võite näha imporditud andmetes ootamatuid kuupäevi ja kellaaegu. Ilma õige sätteta teisendab impordiprotsess UTC kuupäeva kohalikku vormingusse ja seejärel teisendavad süsteemisätted selle uuesti.

See topeltteisendus põhjustab rakenduste vahelise muutuse. Näiteks võib topeltteisenduse tõttu töötaja kuupäev olla erinevate kohalike ajavööndite tõttu rakendustes Dynamics 365 Human Resources ja Dynamics 365 Finance erinev. Imporditöö seadmine UTC peale lahendab selle probleemi.

1. Valige rakenduses Dynamics 365 Finance and Operations suvand **Andmehaldus**.

2. Valige suvand **Impordi projektid** ja valige seejärel projekt.

3. Suvandis **Allika kuupäevavorming** valige **CSV-Unicode**.

   [![Allika kuupäevavormingu muutmine UTC-le](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Muutke suvandi **Ajavöönd** väärtuseks **Koordineeritud maailmaaja vöönd** ja muutke suvandi **Keel** väärtuseks **En-US**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]