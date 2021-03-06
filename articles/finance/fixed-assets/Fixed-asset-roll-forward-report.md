---
title: Põhivarade edasiarvestuse aruanne
description: Selles teemas kirjeldatakse, kuidas kasutada põhivarade edasiarvestuse aruannet.
author: saraschi2
ms.date: 01/08/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: b1693df7d535a340306d2b817ce008c292bad521
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897668"
---
# <a name="fixed-assets-roll-forward-report"></a>Põhivarade edasiarvestuse aruanne

[!include [banner](../includes/banner.md)]

**Põhivarade edasiarvestuse** aruandes esitatakse hõlpsasti loetavas Microsoft Exceli vormingus põhivara üksikasjalikud andmed, mida vajate perioodi sulgemise, finantsaruannete ja maksuaruandluse tegemiseks. Aruanne sisaldab põhivarade alg- ja lõppsaldosid koos sel perioodil tehtud hinna määramistega ning iga sel perioodil tehtud põhivara soetamise ja likvideerimisega. Andmed esitatakse põhivarade kohta eraldi ning väärtusi summeeritakse ka põhivaragruppide ja juriidilise isiku jaoks.

**Põhivarade edasiarvestuse** aruanne kasutab elektroonilise aruandluse (ER) raamistikku. Enne aruande käivitamist tuleb teenusest Microsoft Dynamics Lifecycle Services (LCS) importida põhivarade mudel ja põhivara edasiarvestuse konfiguratsioonid. Juhiste saamiseks vaadake teemat [Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

See aruanne on saadaval rakenduses Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 või kiirparandusena rakendusele Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juuli 2017). Juuli 2017 väljalaske keskkondadele tuleb rakendada kolm järgmist kiirparandust.

- **KB 4041754:** elektroonilise aruandluse (ER) konfiguratsiooni ei saa LCS-ist alla laadida, kuna see ei ole pärast platvormivärskenduste paketi rakendamist praegusele versioonile rakendatav
- **KB 4056107:** elektroonilise aruandluse (GER) kumulatiivne värskendus 5
- **KB 4056353:** põhivara väljavõtte ja märkuste aruanded ei vasta GAAP-i ja IFRS-i nõuetele

Järgmises tabelis on kirjeldatud aruandes olevaid välju.


|                    Väli                    |                                                                                                                                Kirjeldus                                                                                                                                |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              Saldod: algsaldo              |                                                                                           Põhivara raamatupidamislik jääkväärtus aruandel määratletud alguskuupäeva seisuga.                                                                                           |
|              Saldod: lõppsaldo              |                                                                                            Põhivara raamatupidamislik jääkväärtus aruandel määratletud lõppkuupäeva seisuga.                                                                                            |
|         Soetamised: algväärtus         |                                                 Tehingutüüpide <strong>Soetus</strong> ja <strong>Soetuse korrigeerimine</strong> summa kuni aruandel määratletud alguskuupäevani.                                                  |
|      Soetamised: perioodi soetamised      |                                                 Aruande kuupäevavahemiku jooksul sisestatud tehingutüüpide <strong>Soetus</strong> ja <strong>Soetuse korrigeerimine</strong> summa.                                                  |
|       Soetamised: perioodi likvideerimised        |                                                                        Aruande kuupäevavahemiku jooksul sisestatud likvideerimiskandega kõigi soetamiste likvideerimiste summa.                                                                        |
|         Soetamised: lõppväärtus         |                                                  Tehingutüüpide <strong>Soetus</strong> ja <strong>Soetuse korrigeerimine</strong> summa kuni aruandel määratletud lõppkuupäevani.                                                   |
|        Kulum: algväärtus         | Tehingutüüpide <strong>Kulum</strong>, <strong>Kulumi korrigeerimine</strong>, <strong>Kulumi erihüvitis</strong> ja <strong>Plaaniväline kulum</strong> summa kuni aruandel määratletud alguskuupäevani. |
|     Kulum: perioodi kulum     |                         Aruande kuupäevavahemiku jooksul sisestatud tehingutüüpide <strong>Kulum</strong>, <strong>Kulumi korrigeerimine</strong> ja <strong>Plaaniväline kulum</strong> summa.                          |
| Kulum: perioodi erikulum |                                                              Aruande kuupäevavahemiku jooksul sisestatud tehingutüübi <strong>Kulumi erihüvitis</strong> korrigeerimine summa.                                                               |
|       Kulum: perioodi likvideerimised       |                                                                       Aruande kuupäevavahemiku jooksul sisestatud likvideerimiskandega kõigi kulumite tühistamiste summa.                                                                        |
|        Kulum: lõppväärtus         |  Tehingutüüpide <strong>Kulum</strong>, <strong>Kulumi korrigeerimine</strong>, <strong>Kulumi erihüvitis</strong> ja <strong>Plaaniväline kulum</strong> summa kuni aruandel määratletud lõppkuupäevani.  |
|    Üleshindlused/allahindamised: algväärtus     |                              Tehingutüüpide <strong>Üleshindlus</strong>, <strong>Allahindlus</strong> ja <strong>Ümberhindlus</strong> summa kuni aruandel määratletud alguskuupäevani.                               |
|   Üleshindlused/allahindamised: perioodi üleshindlused   |                                                                    Aruande kuupäevavahemiku jooksul sisestatud tehingutüübi <strong>Üleshindlus</strong> korrigeerimine summa.                                                                    |
|  Üleshindlused/allahindamised: perioodi allahindlused  |                                                                   Aruande kuupäevavahemiku jooksul sisestatud tehingutüübi <strong>Allahindlus</strong> korrigeerimine summa.                                                                   |
| Üleshindlused/allahindamised: perioodi ümberhindlused  |                                                                        Aruande kuupäevavahemiku jooksul sisestatud tehingutüübi <strong>Ümberhindlus</strong> korrigeerimine summa.                                                                        |
|   Üleshindlused/allahindamised: perioodi likvideerimised   |                                                           Aruande kuupäevavahemiku jooksul sisestatud likvideerimiskandega kõigi üleshindluste, allahindluste ja ümberhindluste tühistamiste summa.                                                           |
|    Üleshindlused/allahindamised: lõppväärtus     |                               Tehingutüüpide <strong>Üleshindlus</strong>, <strong>Allahindlus</strong> ja <strong>Ümberhindlus</strong> summa kuni aruandel määratletud lõppkuupäevani.                                |
|          Likvideerimised: likvideerimise kuupäev           |                                                                                                                Põhivararaamatu likvideerimise kuupäev.                                                                                                                |
|    Likvideerimised: raamatupidamislik jääkväärtus likvideerimisel    |                                                                                                    Põhivararaamatu raamatupidamislik jääkväärtus likvideerimise ajal.                                                                                                    |
|            Likvideerimised: müügiväärtus            |                                                                                               Põhivararaamatu müügiväärtus likvideerimise müügitehingu korral.                                                                                                |
|           Likvideerimised: mahakandmise väärtus            |                                                                                               Põhivararaamatu mahakandmise väärtus likvideerimise mahakandmistehingu korral.                                                                                               |
|           Likvideerimised: kasum/kahjum            |                                                                                 Kasumi või kahjumi väärtus, mis arvutatakse põhivararaamatu likvideerimiskande osana.                                                                                 |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]