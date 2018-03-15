---
title: "Põhivarade edasiarvestuse aruanne"
description: "Selles teemas kirjeldatakse, kuidas kasutada põhivarade edasiarvestuse aruannet."
author: saraschi2
manager: 
ms.date: 01/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7a81697a8e90fb6b0695a02db0868f5708fdbddf
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---
# <a name="fixed-assets-roll-forward-report"></a>Põhivarade edasiarvestuse aruanne

[!include[banner](../includes/banner.md)]

**Põhivarade edasiarvestuse** aruandes esitatakse hõlpsasti loetavas Microsoft Exceli vormingus põhivara üksikasjalikud andmed, mida vajate perioodi sulgemise, finantsaruannete ja maksuaruandluse tegemiseks. Aruanne sisaldab põhivarade alg- ja lõppsaldosid koos sel perioodil tehtud hinna määramistega ning iga sel perioodil tehtud põhivara soetamise ja likvideerimisega. Andmed esitatakse põhivarade kohta eraldi ning väärtusi summeeritakse ka põhivaragruppide ja juriidilise isiku jaoks.

**Põhivarade edasiarvestuse** aruanne kasutab elektroonilise aruandluse (ER) raamistikku. Enne aruande käivitamist tuleb Microsoft Dynamicsi teenusest Lifecycle Services (LCS) importida põhivarade mudel ja põhivara edasiarvestuse konfiguratsioonid. Juhiste saamiseks vaadake teemat [Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

Aruanne on saadaval rakenduses Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 või rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juuli 2017) kiirparanduses. Juuli 2017 väljalaske keskkondadele tuleb rakendada kolm järgmist kiirparandust.

- **KB 4041754:** elektroonilise aruandluse (ER) konfiguratsiooni ei saa LCS-ist alla laadida, kuna see ei ole pärast platvormivärskenduste paketi rakendamist praegusele rakenduse versioonile rakendatav
- **KB 4056107:** elektroonilise aruandluse (GER) kumulatiivne värskendus 5
- **KB 4056353:** põhivara väljavõtte ja märkuste aruanded ei vasta GAAP-i ja IFRS-i nõuetele

Järgmises tabelis on kirjeldatud aruandes olevaid välju.

| Väli                                       | Kirjeldus |
|---------------------------------------------|-------------|
| Saldod: algsaldo                           | Põhivara raamatupidamislik jääkväärtus aruandel määratletud alguskuupäeva seisuga. |
| Saldod: lõppsaldo                           | Põhivara raamatupidamislik jääkväärtus aruandel määratletud lõppkuupäeva seisuga. |
| Soetamised: algväärtus                 | Tehingutüüpide **Soetus** ja **Soetuse korrigeerimine** summa kuni aruandel määratletud alguskuupäevani. |
| Soetamised: perioodi soetamised           | Aruande kuupäevavahemiku jooksul sisestatud tehingutüüpide **Soetus** ja **Soetuse korrigeerimine** summa. |
| Soetamised: perioodi likvideerimised              | Aruande kuupäevavahemiku jooksul sisestatud likvideerimiskandega kõigi soetamiste likvideerimiste summa. |
| Soetamised: lõppväärtus                 | Tehingutüüpide **Soetus** ja **Soetuse korrigeerimine** summa kuni aruandel määratletud lõppkuupäevani. |
| Kulum: algväärtus                | Tehingutüüpide **Kulum**, **Kulumi korrigeerimine**, **Kulumi erihüvitis** ja **Plaaniväline kulum** summa kuni aruandel määratletud alguskuupäevani. |
| Kulum: perioodi kulum         | Aruande kuupäevavahemiku jooksul sisestatud tehingutüüpide **Kulum**, **Kulumi korrigeerimine** ja **Plaaniväline kulum** summa. |
| Kulum: perioodi erikulum | Aruande kuupäevavahemiku jooksul sisestatud tehingutüübi **Kulumi erihüvitis** korrigeerimine summa. |
| Kulum: perioodi likvideerimised             | Aruande kuupäevavahemiku jooksul sisestatud likvideerimiskandega kõigi kulumite tühistamiste summa. |
| Kulum: lõppväärtus                | Tehingutüüpide **Kulum**, **Kulumi korrigeerimine**, **Kulumi erihüvitis** ja **Plaaniväline kulum** summa kuni aruandel määratletud lõppkuupäevani. |
| Üleshindlused/allahindamised: algväärtus        | Tehingutüüpide **Üleshindlus**, **Allahindlus** ja **Ümberhindlus** summa kuni aruandel määratletud alguskuupäevani. |
| Üleshindlused/allahindamised: perioodi üleshindlused     | Aruande kuupäevavahemiku jooksul sisestatud tehingutüübi **Üleshindlus** korrigeerimine summa. |
| Üleshindlused/allahindamised: perioodi allahindlused   | Aruande kuupäevavahemiku jooksul sisestatud tehingutüübi **Allahindlus** korrigeerimine summa. |
| Üleshindlused/allahindamised: perioodi ümberhindlused  | Aruande kuupäevavahemiku jooksul sisestatud tehingutüübi **Ümberhindlus** korrigeerimine summa. |
| Üleshindlused/allahindamised: perioodi likvideerimised     | Aruande kuupäevavahemiku jooksul sisestatud likvideerimiskandega kõigi üleshindluste, allahindluste ja ümberhindluste tühistamiste summa. |
| Üleshindlused/allahindamised: lõppväärtus        | Tehingutüüpide **Üleshindlus**, **Allahindlus** ja **Ümberhindlus** summa kuni aruandel määratletud lõppkuupäevani. |
| Likvideerimised: likvideerimise kuupäev                    | Põhivararaamatu likvideerimise kuupäev. |
| Likvideerimised: raamatupidamislik jääkväärtus likvideerimisel       | Põhivararaamatu raamatupidamislik jääkväärtus likvideerimise ajal. |
| Likvideerimised: müügiväärtus                       | Põhivararaamatu müügiväärtus likvideerimise müügitehingu korral. |
| Likvideerimised: mahakandmise väärtus                      | Põhivararaamatu mahakandmise väärtus likvideerimise mahakandmistehingu korral. |
| Likvideerimised: kasum/kahjum                      | Kasumi või kahjumi väärtus, mis arvutatakse põhivararaamatu likvideerimiskande osana. |

