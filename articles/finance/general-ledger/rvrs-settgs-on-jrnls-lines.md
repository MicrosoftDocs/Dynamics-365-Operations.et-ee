---
title: Storno seaded töölehtedel ja ridadel
description: Selles teemas käsitletakse, miks üldisele töölehele sisestatud stornokannet ei pruugi olla kaasatud sisestatud kandesse.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028558"
---
# <a name="reverse-settings-on-journals-and-lines"></a>Storno seaded töölehtedel ja ridadel

[!include [banner](../includes/banner.md)]

Selles teemas käsitletakse, miks üldisele töölehele sisestatud stornokannet ei pruugi olla kaasatud sisestatud kandesse.  

## <a name="symptom"></a>Sümptom

Päevane tööleht sisaldab stornokannet ja tühistuskuupäeva töölehel. Töölehe sisestamisel ei tühistata ühtki kannet. Miks see juhtub?

## <a name="resolution"></a>Lahendus

Töölehe sisestamisel vaatab tühistamisprotsess ainult kande jaotise **Read** seadeid **Stornokanne** ja **Tühistamiskuupäev**. See lähenemine võimaldab töölehele lisada mõned kanded, mis on märgitud tühistamiseks, ja teised, mis pole.

Töölehe väärtusi kasutatakse vaikeväärtustena ainult *uute* ridade lisamisel. Väärtuste muutmine töölehel ei mõjuta olemasolevaid ridu. Selles näites sisestati esmalt kanderead. Kui sisestate rea üksikasjad enne töölehe tühistatavaks määramist, ei kohaldata stornokandeks ja tühistamiskuupäevaks määramist ühelegi olemasolevale reale.

Stornokande või tühistamiskuupäeva muutmisel olemasoleval real rakendatakse see muudatus ka sama kande muudele ridadele. Jõudluse optimeerimiseks ei värskendata ruudustikku pärast muudatuste rakendamist muudele ridadele. Uuendatud väärtusi saab kuvada ruudustiku värskendamisega.


