---
title: Koosluse versiooni koosnevusarvutus
description: Selles artiklis selgitatakse koondplaanimise stsenaariumi, mis hõlmab koosluse versiooni koosnevusarvutust.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 380f8069a726e53084164a5ac1fc0a0a99c83590
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213741"
---
# <a name="explosion-of-a-bom-version"></a>Koosluse versiooni koosnevusarvutus

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse koondplaanimise stsenaariumi, mis hõlmab koosluse versiooni koosnevusarvutust.

Koosluse versiooni nõudluskoosnevusarvutus loob iga koosluserea kauba nõudluse konkreetses tegevuskohas ning võimalik, et ka konkreetses laos. Tegevuskohapõhises koosluses saab igale koosluse reale määrata konkreetse lao. Iga koosluserea puhul määratlevad kauba dimensioonisätted ka lao vajaduse. Iga koosluserea kaubast tulenevast nõudlusest saab seejärel täiendava nõudluskoosnevusarvutuse alguspunkt. See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.

-   Laoala dimensioon on kohustuslik ja see tuleb sisestada nõudluskandel.
-   Laoala dimensioon on kooskõlaline. Seepärast on madalatasemeline nõudlus sama, mis laoala algsel nõudluskandel.

Järgmisel joonisel on toodud koondplaneerimise nõudluskoosnevusarvutuse protsess. ![Nõude koostamine, kasutades koosluse versiooni](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a>Lisaressursid
--------

[Koosluse versiooni määratlemine](master-plan-bom-version-determined.md)

[Koondplaneerimine ja mitme tegevuskoha funktsiooni ülevaade](master-plan-multisite-functionality.md)



