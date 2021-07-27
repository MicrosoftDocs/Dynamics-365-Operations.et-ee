---
title: Hooldusolek
description: Selles teemas tutvustatakse, kuidas arvutada hoolduse olekut varahalduses.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1b0c8b6a81fd863d66ca01689262f0ec08a94d76
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354972"
---
# <a name="maintenance-status"></a>Hooldusolek

[!include [banner](../../includes/banner.md)]

 

Varahalduses saate teha ülevaatlikke arvutusi teatud perioodi kohta, et näha uusi, aktiivseid ja lõpetatud hooldusnõudeid, töökäske ja hoolduskatkestuste tegevusi. Saate näha ka sama perioodi lõpetatud tingimuse hindamiste arvu. Kasutage seda arvutust, et saada ülevaade sissetulevate ja lõpetatud hooldusnõuete ja töökäskude töökoormusest.

## <a name="make-a-maintenance-status-calculation"></a>Hoolduse oleku arvutuse tegemine

1. Klõpsake **Varahaldus** > **Päringud** > **Hoolduse olek**.

2. Valige dialoogist **Oleku arvutamine** see ajavahemik, millele soovite väljadel **Alguskuupäev** ja **Lõppkuupäev** arvutusi teha.

3. Saate kasutada välja **Tase**, et näidata kui üksikasjalikke töö asukohtade hoolduse ridu te soovite. 

  Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik töö asukoha hoolduse read ning seetõttu võivad rea olekud olla alumisel tasemel asuvate töö asukohtade summad. 
  
  Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki hoolduse ridu kõigi töö asukoha tasemete kohta, millega nad on seotud.

4. Arvutuse alustamiseks klõpsake **OK**.

5. Valige nupud **Rühmitusalus**, et vaadata arvutuse soovitud üksikasja taset. Valitud nupud **Rühmitusalus** on esile tõstetud. Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.

6. Pidage meeles klõpsata nuppu **Värskenda**, et värskendada arvutust iga kord, kui teete muudatusi, aktiveerides või inaktiveerides nuppe **Rühmitusalus** või tehes arvutusi uue perioodi jaoks.

7. Klõpsake valikul **Olek**, kui soovite luua uue hoolduse oleku arvutuse.

>[!NOTE]
>Jaotises **Hoolduse olek** kuvatavad tulemused sisaldavad ainult hooldusnõudeid ja töökäske, millel on tegeliku alguskuupäev ja -kellaaeg. Lõppkuupäev ja -kellaaeg võivad olla tühjad.

## <a name="example-1"></a>Näide 1

Alloleval kuvatõmmisel on nupud **Aasta** ja **Kuu** aktiveeritud. Kui valikud **Rühmitusalus** on valitud, saate igakuiselt üldise ülevaate hooldusnõuetega ja töökäskudega seotud töökoormusest ja läbilaskevõimest. 

![Igakuise töökoormuse näide.](media/13-controlling-and-reporting.png)

## <a name="example-2"></a>Näide 2

Alloleval kuvatõmmisel on lisatud info töö asukohtade kohta. Nüüd on võimalik võrrelda töökoormust ja läbilaskevõimet töö asukohtade vahel, mis võib esindada geograafilisi asukohti, tehaseid või tööalasid. 

![Igakuise töökoormuse näide töö asukohtadega.](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]