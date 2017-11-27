---
title: Koosluse versiooni koosnevusarvutus
description: "Selles artiklis selgitatakse koondplaanimise stsenaariumi, mis hõlmab koosluse versiooni koosnevusarvutust."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0f852c8d100c91d055e58c4594106aedf6fe5afb
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="explosion-of-a-bom-version"></a>Koosluse versiooni koosnevusarvutus

[!include[banner](../includes/banner.md)]


Selles artiklis selgitatakse koondplaanimise stsenaariumi, mis hõlmab koosluse versiooni koosnevusarvutust.

Koosluse versiooni nõudluskoosnevusarvutus loob iga koosluserea kauba nõudluse konkreetses tegevuskohas ning võimalik, et ka konkreetses laos. Tegevuskohapõhises koosluses saab igale koosluse reale määrata konkreetse lao. Iga koosluserea puhul määratlevad kauba dimensioonisätted ka lao vajaduse. Iga koosluserea kaubast tulenevast nõudlusest saab seejärel täiendava nõudluskoosnevusarvutuse alguspunkt. See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.

-   Laoala dimensioon on kohustuslik ja see tuleb sisestada nõudluskandel.
-   Laoala dimensioon on kooskõlaline. Seepärast on madalatasemeline nõudlus sama, mis laoala algsel nõudluskandel.

Järgmisel joonisel on toodud koondplaneerimise nõudluskoosnevusarvutuse protsess. ![Nõude koostamine, kasutades koosluse versiooni](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a>Vt ka
--------

[Koondplaanimine – koosluse versiooni määratlemine](master-plan-bom-version-determined.md)

[Koondplaanimine ja mitme laoala funktsioon](master-plan-multisite-functionality.md)




