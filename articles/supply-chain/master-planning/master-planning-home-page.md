---
title: Koondplaneerimise kodulehekülg
description: Koondplaneerimise võimaldab ettevõtetel kindlaks määrata ja tasakaalustada edaspidise vajaduse toormaterjalide järele ning vajalikud võimsused ettevõtte eesmärkide täitmiseks.
author: t-benebo
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f7289e7ecee49353ca8ee4554914a08074401df
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740491"
---
# <a name="master-planning-home-page"></a>Koondplaneerimise kodulehekülg

[!include [banner](../includes/banner.md)]

Koondplaneerimise võimaldab peamiselt ettevõtetel kindlaks määrata ja tasakaalustada edaspidise vajaduse toormaterjalide järele ning vajalikud võimsused ettevõtte eesmärkide täitmiseks. Koondplaneerimise hindab järgmist:

- Millised toormaterjalid ja võimsused on praegu saadaval?
- Milliseid toormaterjale ja võimsuseid on vaja tootmise lõpule viimiseks? Näiteks, mida tuleb toota, osta, üle kanda või puhvervaruna kõrvale panna, enne kui tootmise saab lõpule viia.

Koondplaneerimine kasutab saadud teavet, et arvutada vajadused ja luua plaanitud tellimused.

Kolme peamist plaanimisprotsessi on järgmised.

- **Koondplaneerimine** – koondplaan arvutab netovajadused. See põhineb praegustel tegelikel tellimustel ja võimaldab ettevõtetel juhtida varude täiendamist lühiajaliselt, igapäevaselt. Teine mõiste selle kirjeldamiseks on *netovajaduste plaan*. Lisateavet vt teemast [Koondplaanide ülevaade](master-plans.md).

- **Eelarveplaanimine** – eelarve graafik arvutab brutonõuded. See põhineb tulevikku suunatud hinnangutel (või prognoosidel) ning võimaldab ettevõtetel teostada materjalide ja võimsuse pikaajalist planeerimist. Lisateavet vt teemast [Nõudluse prognoosi ülevaade](introduction-demand-forecasting.md).

- **Kontsernisisene koondplaneerimine** – kontsernisisene koondplaan arvutab juriidiliste isikute netonõuded. See ühendab nii ettevõtetevahelise lühiajalise, kindla nõudluse ja pakkumise, kui ka pikaajalise, plaanitud (veel kinnitamata) nõudluse ja pakkumise. Lisateavet vt teemast [Ettevõtesisene plaanimine](planning-optimization/Intercompany-planning.md).

Ettevõtted saavad plaani väljundit muuta. Nad saavad käivitada regeneratiivse või netomuutuse plaani või mõlemad. Regeneratiivsed plaanid uuendavad kõiki nõudeid, kuid netomuutuse plaanid uuendavad plaani ainult uute nõuetega kaupade korral, mis on saabunud pärast viimast käitamist.

Koondplaneerimise plaanid on tavaliselt lühiajalised ja võivad kehtida nii ühe nädala kui ka kuni kuue kuu kohta. Koondplaneerimise moodul määrab tarne (materjalid) ja võimsuse (ressursid) vajadused, mis vastavad praegusele nõudmisele (netonõuded). Enamikus ettevõtetes on seda laiendatud nii, et see hõlmaks vastuvõetavate toodete hulgas ka kõige pikemat kumulatiivset täitmisaega.

## <a name="learning-map"></a>Õppekaart

Järgmisel õppekaardil on näidatud peamised põhimõtted ja ülesanded, millest koondplaneerimise mooduli raamistik koosneb. Klõpsake linke jaotises [Kiirlingid](#quick-links), et õppida moodulit kasutama.

[![Koondplaneerimise õppekaart.](./media/master-planning-learning-map.png)](./media/master-planning-learning-map.png)

## <a name="quick-links"></a>Kiirlingid

- [Koondplaanide ülevaade](master-plans.md)  
- [Piirangutega plaani koostamine](./tasks/constrained-plan.md)
- [Kaastoodete jaoks materjaliplaani loomine](./tasks/create-material-plan-co-products.md)
- [Koondplaneerimine ja mitme tegevuskoha funktsiooni ülevaade](master-plan-multisite-functionality.md)
- [Kontsernisisese plaani loomine](./tasks/create-intercompany-plan.md)
- [Nõudluse prognoosimise ülevaade](introduction-demand-forecasting.md)
- [Eelarve planeerimise koefitsiendid](reduction-keys.md)

## <a name="additional-resources"></a>Lisaressursid

### <a name="roadmaps"></a>Sisukaardid

Avage [Microsoft Dynamics 365 sisukaart](https://roadmap.dynamics.com/), et näha, millised uued funktsioonid on välja antud ja millised uued funktsioonid on arendamisel.

### <a name="blogs"></a>Ajaveebid

[Dynamics AX-i tootmise uurimis- ja arendustöörühma ajaveebist](/archive/blogs/axmfg/) ning [Dynamics AX-i Supply Chain Managementi uurimis- ja arendustöörühma ajaveebist](https://blogs.msdn.microsoft.com/dynamicsaxscm) leiate arvamusi, uudiseid ning muud teavet koondplaneerimise ja muude lahenduste kohta.

### <a name="task-guides"></a>Tegevusjuhised

Täiendav spikker on saadaval ülesandejuhistena. Tegevuse juhistele juurdepääsemiseks klõpsake ükskõik millisel lehel nuppu **Spikker**.

### <a name="webinars"></a>Veebipõhised seminarid

[Azure’i masinõppe kasutamine nõudluse prognoosimiseks](https://www.youtube.com/watch?v=4nQsccdFFDA&feature=youtu.be)

### <a name="tech-conference-recordings"></a>Tehnoloogiakonverentsi salvestised

- [Nõudluse prognoosi funktsiooni pikendamine](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
- [MRP jõudluse häälestamine](https://youtu.be/RLXybx20B5o)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]