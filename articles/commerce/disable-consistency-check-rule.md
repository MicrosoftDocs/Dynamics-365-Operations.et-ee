---
title: Kande kinnitamisprotsessis kasutatavate reeglite keelamine
description: Selles teemas kirjeldatakse kande kinnitamise reeglite keelamise funktsiooni teenuses Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 12/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: cdaea51b4c84e6a62f0eb9412315ae77b4c11503
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919521"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Kande kinnitamisprotsessis kasutatavate reeglite keelamine

[!include [banner](../includes/banner.md)]

Jaemüüjatel võib olla kordumatuid äristsenaariume ja protsesse. Seetõttu ei kehti kõigi jaemüüjate kohta kõik reeglid, mis on kaubanduse kande kinnitamisprotsessis kaasatud. Nende muudatustega arvestamiseks sisaldab Microsoft Dynamics 365 Commerce funktsiooni, mida saab kasutada mittekohaldatavate reeglite keelamiseks.

Teie keskkonnas kande kinnitamisprotsessis saadaolevate reeglite loendi kuvamiseks ja kõigi reeglite oleku kuvamiseks avage jaotis **Retail ja Commerce \> Peakontori seadistamine \> Parameetrid \> Commerce'i parameetrid** ja valige vahekaart **Kande kinnitamine**. Kõiki lubatud reegleid kasutatakse kannete kinnitamiseks protsessis **Kaupluse kannete kinnitamine** ja need peavad vastama kandeväljavõtte aruandesse kogutavatele ja sisestatavatele kannetele.

Vaikimisi on iga reegli olekuks seatud **Lubatud**. Nii kasutatakse kannete kontrollimiseks, enne kui need kaubanduse kandeväljavõtetesse lisatakse, kõiki reegleid. Reegli keelamiseks seadke selle olekuks **Keelatud**. Keelatud reegleid ei võeta arvesse, kui kandeid protsessi **Kaupluse kannete kinnitamine** ajal kontrollitakse.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
