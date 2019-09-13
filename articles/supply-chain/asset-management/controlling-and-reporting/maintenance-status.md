---
title: Hooldusolek
description: Selles teemas tutvustatakse, kuidas arvutada hoolduse olekut varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918345"
---
# <a name="maintenance-status"></a>Hooldusolek

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Varahalduses saate teha arvutusi, et näha uute, aktiivsete ja lõpetatud hooldusnõuete, töökäskude ja hoolduskatkestuste tegevuste ülevaadet teatud ajaperioodi kohta. Saate näha ka sama perioodi lõpetatud tingimuse hindamiste arvu. Kasutage seda arvutust, et saada ülevaade sissetulevate ja lõpetatud hooldusnõuete ja töökäskude töökoormusest.

## <a name="make-a-maintenance-status-calculation"></a>Hoolduse oleku arvutuse tegemine

1. Klõpsake **Varahaldus** > **Päringud** > **Hoolduse olek**.

2. Valige dialoogist **Oleku arvutamine** see periood, millele soovite väljadel **Alguskuupäev** ja **Lõppkuupäev** arvutusi teha.

3. Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohtade hoolduse ridu te soovite. Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha hoolduse read ning seetõttu võivad rea olekud olla alumisel tasemel asuvate töö asukohtade summad. Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki hoolduse ridu kõigi töö asukoha tasemete kohta, millega nad on seotud.

4. Arvutuse alustamiseks klõpsake **OK**.

5. Toimingupaani rühmades **Rühmitusalus** klõpsake asjakohastele nuppudele, et näidata arvutuse soovitud üksikasja taset. Valitud toimingupaani nupud on esile tõstetud. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

6. Pidage meeles klõpsata nupul **Värskenda**, et värskendada arvutust iga kord, kui teete muudatusi, aktiveerides või inaktiveerides nuppe **Rühmitusalus...** või tehes arvutusi uue perioodi jaoks.

7. Klõpsake valikul **Olek**, kui soovite luua uue hoolduse oleku arvutuse.

>[!NOTE]
>Jaotises **Hoolduse olek** kuvatavad tulemused sisaldavad ainult hooldusnõudeid ja töökäske, millel on tegeliku alguskuupäev ja -kellaaeg. Lõppkuupäev ja -kellaaeg võivad olla tühjad.

*Näide 1.*

Alloleval joonisel on nupud **Aasta** ja **Kuu** aktiveeritud. Siin saate igakuiselt üldise ülevaate hooldusnõuetega ja töökäskudega seotud töökoormusest ja läbilaskevõimest. 

![Joonis 1](media/13-controlling-and-reporting.png)

*Näide 2.*

Alloleval joonisel on lisatud info töö asukohtade kohta. Nüüd on võimalik võrrelda töökoormust ja läbilaskevõimet töö asukohtade vahel, mis võib esindada geograafilisi asukohti, tehaseid või tööalasid. 

![Joonis 2](media/14-controlling-and-reporting.png)

