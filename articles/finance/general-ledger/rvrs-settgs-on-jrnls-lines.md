---
title: Storno sätted töölehtedel ja ridadel
description: Selles artiklis käsitletakse, miks üldisele töölehele sisestatud stornokannet ei kaasata tingimata sisestatud kandesse.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e36a3ea1736e4d7f60a5a6ce588ad3e66c950c14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899838"
---
# <a name="reverse-settings-on-journals-and-lines"></a>Storno sätted töölehtedel ja ridadel

[!include [banner](../includes/banner.md)]

Selles artiklis käsitletakse, miks üldisele töölehele sisestatud stornokannet ei kaasata tingimata sisestatud kandesse.  

## <a name="symptom"></a>Sümptom

Päevane tööleht sisaldab stornokannet ja tühistuskuupäeva töölehel. Töölehe sisestamisel ei tühistata ühtki kannet. Miks see juhtub?

## <a name="resolution"></a>Lahendus

Töölehe sisestamisel vaatab tühistamisprotsess ainult kande jaotise **Read** seadeid **Stornokanne** ja **Tühistamiskuupäev**. See lähenemine võimaldab töölehele lisada mõned kanded, mis on märgitud tühistamiseks, ja teised, mis pole.

Töölehe väärtusi kasutatakse vaikeväärtustena ainult *uute* ridade lisamisel. Väärtuste muutmine töölehel ei mõjuta olemasolevaid ridu. Selles näites sisestati esmalt kanderead. Kui sisestate rea üksikasjad enne töölehe tühistatavaks määramist, ei kohaldata stornokandeks ja tühistamiskuupäevaks määramist ühelegi olemasolevale reale.

Stornokande või tühistamiskuupäeva muutmisel olemasoleval real rakendatakse see muudatus ka sama kande muudele ridadele. Jõudluse optimeerimiseks ei värskendata ruudustikku pärast muudatuste rakendamist muudele ridadele. Uuendatud väärtusi saab kuvada ruudustiku värskendamisega.


