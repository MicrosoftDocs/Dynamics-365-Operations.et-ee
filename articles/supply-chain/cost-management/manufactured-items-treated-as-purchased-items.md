---
title: Toodetavate või hangitavate toodete seadistamine
description: 'Tooteid saab hankida mitmel viisil: neid saab toota (valmistada) või hankida (osta). See artikkel kirjeldab mõnda tüüpilist punkti, mida arvestada, kui konfigureerite tooteid mitme allhanke toetamiseks.'
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4910faa2e66cb61f6064e686c49369d14526cc1f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674501"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a>Toodetavate või hangitavate toodete seadistamine

[!include [banner](../includes/banner.md)]

Tooteid saab hankida mitmel viisil: neid saab toota (valmistada) või hankida (osta). See artikkel kirjeldab mõnda tüüpilist punkti, mida arvestada, kui konfigureerite tooteid mitme allhanke toetamiseks. 

Mitme tarnijaga hanget kasutatakse tavaliselt harva toodetava kauba ostmiseks või juhul, kui peamiselt toodetud kaupa muudetakse, nii et nüüd on see peamiselt ostetav kaup. Esmalt määratakse kaup toodetavaks kaubaks, et määratleda saaks koosluse- ja protsessiteabe ning toetada kauba tootmistellimusi. Tootmise tüübiks peab olema määratud **Kooslus** (tootmise töötlemiseks **Valem** või **Kaastoode**).

Standardkulu kasutamisel saab toodetud kauba jaoks arvutada kauba kulukirje. Kauba kulukirje ei pruugi siiski ühtida standardkuluga, mida ostu puhul soovite. Sellisel juhul tuleb soovitud standardkulu kauba kulukirje jaoks käsitsi sisestada ja aktiveerida. Kuluarvutuseks kaaluge erikoosluse ja -protsessi kasutamist, mis esindaks toote tarnekombinatsiooni rahandusperioodi jooksul, et minimeerida aja jooksul hälbeid. Peale selle saab ühes tegevuskohas toodetud kauba üle kanda teise tegevuskohta. Seetõttu tuleb kauba kulu käsitsi sisestada ja aktiveerida selle tegevuskoha puhul, kuhu kaup üle kantakse. Kui kasutate toodetud kaupa kõrgema taseme toodete komponendina, tuleb komponendi kulusid käsitleda ostetud kaubana. See juhis kehtib olenemata sellest, kas komponendi kulud on arvutatud või käsitsi sisestatud. Teisisõnu tuleb koosluse arvutus käsitlema kauba kulusid ostetud komponendina, mitte kasutama kulude arvutamiseks kauba koosluse- ja protsessiteavet. 

Arvutamise vältimiseks valige lipp **Peata koosnevusarvutus**, mis on manustatud kaubale määratud koosluse arvutamise grupile. Selleks et vältida kauba kaudu koondplaneerimise arvutusi koosnevusnõuetest, määrake kauba laovarudes või laovarude grupis koosnevuspiiriks 0 (null) päeva. Koondplaneerimise arvutus käsitleb siis kaupa ostetud kaubana ega tee kauba koosluse- ja protsessiteabe jaoks rohkem arvutusi.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]