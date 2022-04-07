---
title: Koosluse versiooni koosnevusarvutus
description: Selles artiklis selgitatakse koondplaanimise stsenaariumi, mis hõlmab koosluse versiooni koosnevusarvutust.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 119b77b695ff065c8e45693e1cf7cf15360d441e
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468632"
---
# <a name="explosion-of-a-bom-version"></a>Koosluse versiooni koosnevusarvutus

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse koondplaanimise stsenaariumi, mis hõlmab koosluse versiooni koosnevusarvutust.

Koosluse versiooni nõudluskoosnevusarvutus loob iga koosluserea kauba nõudluse konkreetses tegevuskohas ning võimalik, et ka konkreetses laos. Tegevuskohapõhises koosluses saab igale koosluse reale määrata konkreetse lao. Iga koosluserea puhul määratlevad kauba dimensioonisätted ka lao vajaduse. Iga koosluserea kaubast tulenevast nõudlusest saab seejärel täiendava nõudluskoosnevusarvutuse alguspunkt. See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.

-   Laoala dimensioon on kohustuslik ja see tuleb sisestada nõudluskandel.
-   Laoala dimensioon on kooskõlaline. Seepärast on madalatasemeline nõudlus sama, mis laoala algsel nõudluskandel.

Järgmisel joonisel on toodud koondplaneerimise nõudluskoosnevusarvutuse protsess. ![Nõude koostamine, kasutades koosluse versiooni.](./media/multisitedemandexplosionscenariousingbomversion.gif)

## <a name="additional-resources"></a>Lisaressursid

[Koosluse versiooni määratlemine](master-plan-bom-version-determined.md)

[Koondplaneerimine ja mitme tegevuskoha funktsiooni ülevaade](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]