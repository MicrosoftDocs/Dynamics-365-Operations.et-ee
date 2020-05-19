---
title: Koondplaneerimise käitamise jälgimine
description: Selles teemas selgitatakse, kuidas tootmise plaanija saab näha, kas koondplaneerimise käitamine on pooleli.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91ed725e684eda02d94a87ee2a61e5a82034a84e
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323481"
---
# <a name="monitor-a-master-planning-run"></a>Koondplaneerimise käitamise jälgimine

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a>Gantti diagrammi kasutamine koondplaneerimise edenemise visualiseerimiseks

Lehel **Koondplaneerimise edenemise kuva** saate vaadata ajalooliste koondplaneerimiste käitamiste üksikasju Gantti diagrammina. See funktsioon aitab teil mõista koondplaneerimise erinevatele etappidele kulutatavat aega. Praeguse aktiivse planeerimistöö jaoks saab lehte **Koondplaneerimise edenemise kuva** kasutada edenemise jälgimiseks ja hinnangulise allesjäänud aja vaatamiseks.

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a>Koondplaneerimise edenemise visualiseerimise funktsiooni sisselülitamine ja kasutamine

Sulle funktsiooni kasutamiseks tehke järgmist.

1. Valige tööruumis **Funktsiooni haldus** vahekaardil**Uus** loendist suvand **Koondplaneerimise edenemise visualiseerimine**. Kui funktsioon vahekaardile **Uus** ei ilmu, vaadake vahekaartidelt **Pole lubatud** ja **Kõik**.
1. Valige **Luba kohe**. Teise võimalusena valige **Graafik**ja seejärel valige kellaaeg, millal soovite funktsiooni sisse lülitada.

Leht **Koondplaneerimise edenemise kuva** võib kuvada nii ajaloolised planeerimistööd kui ka aktiivsed planeerimistööd. 

Ajalooliste planeerimistööde vaatamiseks on kaks valikut. 

1. Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid** ja seejärel valige tegumiribal suvand **Ajalugu**. Kui soovitud töö on valitud, valige **Päringud** ja valige seejärel **Kuva edenemine**
1. Avage **Koondplaneerimine \> Tööruumid \> Koondplaneerimine** ja paanil Koondplaneerimine klõpsake suvandit **Ajalugu**. Kui soovitud töö on valitud, valige **Päringud** ja valige seejärel **Kuva edenemine**

Aktiivsete planeerimistööde vaatamiseks on kaks valikut. 
1. Avage **Koondplaneerimine \> Tööruumid \> Koondplaneerimine** ja paanil Tegevus valige suvand **Lõpetamata planeerimisprotsess**. Kui soovitud töö on valitud, valige **Päringud** ja valige seejärel **Kuva edenemine**.
1. Avage **Koondplaneerimine \> Tööruumid \> Koondplaneerimine** ja paanil Koondplaneerimine klõpsake suvandit **Kuva edenemine**. Kui soovitud töö on valitud, valige **Päringud** ja valige seejärel **Kuva edenemine**

Pange tähele, et saate aktiivseid töösid vaadata ainult siis kui planeerimistöö on töötlemisel.

### <a name="analyze-a-master-planning-job"></a>Koondplaneerimise töö analüüsimine

Gantti diagrammis saate iga järgmist planeerimisprotsessi laiendada, et vaadata kulutatud aja kohta lisateavet.

- Käivitamine
- Andmete kustutamine ja lisamine
- Laovarude plaanimine
- Hilinemised
- Tegevusteated
- Lõpuleviimine
- Automaatkinnitamine

Gantti diagramm on kasulik tööriist, kui soovite vaadata tegevuseteadete kasutamise mõju.

#### <a name="navigation-in-the-gantt-chart"></a>Gantti diagrammis navigeerimine

- Valitud grupi laiendamiseks ja üksikasjade kuvamiseks valige puuvaates plussmärk (**+**).
- Valitud grupi ahendamiseks valige puuvaates miinusmärk (**–**).
- Saate kasutada navigeerimiseks oma klaviatuuri. Kasutage ridade vahel liikumiseks klahve **Ülesnool** ja **Allanool**. Gruppide laiendamiseks ja ahendamiseks kasutage klahve **Paremnool** ja **Vasaknool**.
- Gantti diagrammis kõikide tasemete avamiseks või sulgemiseks valige suvand **Laienda kõik** või **Ahenda kõik**.
- Seotud töötlemisaja vaatamiseks liikuge kursoriga üle ülesande. (Ülesanded on Gantti diagrammi madalaim tase.)

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a>Tööde võrdlemiseks täiendava koondplaneerimise käivitamise kuvamine

Kui valite väljal **Täiendava koondplaneerimise käivitamise kuvamine** koondplaneerimise töö, saate vaadata Gantti diagrammis täiendavat koondplaneerimise käitamist ja võrrelda kahte tööd.

#### <a name="bom-level-display"></a>Koosluse taseme kuva

Koosluse tasemed kuvatakse laovarude planeerimise, viivituste, tegevuste ja kinnitamiste jaoks erinevalt.

- **Laovarude planeerimine** – koosluse tasemed on näidatud nagu oodatud. Need arvutatakse ülevalt alla.

    **Näide:** koosluse tase 0, 1, 2

- **Viivitused** – koosluse tasemed kuvatakse laovarude planeerimise koosluse tasemetena korrutatud –1-ga. (Teisisõnu on neil negatiivne märk.)

    **Näide:** koosluse tase –2, –1, 0

- **Tegevussoovitus** – koosluse tasemed on näidatud nagu oodatud. Need arvutatakse ülevalt alla.

    **Näide:** koosluse tase 0, 1, 2

- **Automaatkinnitamine** – koosluse tasemed kuvatakse 999 miinus laovarude planeerimise koosluse tase.

    **Näide:** koosluse tase 999, 998, 997

Järgmine tabel võtab käitumise kokku.

| Kuvatav koosluse tase | Lõppkaup | Alamkomponent | Toormaterjal |
|---|---|---|---|
| Laovarude plaanimine | 0 | 1 | 2 |
| Hilinemised | 0 | –1 | –2 |
| Tegevussoovitus | 0 | 1 | 2 |
| Automaatkinnitamine | 999 | 998 | 997 |

#### <a name="visualize-progress"></a>Edenemise visualiseerimine

Kui vaatate praegu käitatavat koondplaneerimise tööd, kuvatakse edenemine Gantti diagrammi värvide kaudu. Järgmised värvid kehtivad sinisele teemale. Teistes värvikujundustes on värvid erinevad.

- **Tumesinine** – lõpuleviidud planeerimisülesanded.
- **Oranž** – hetkel pooleli olev ülesanne.
- **Helesinine** – järelejäänud ülesannete hinnang.

Värv kuvatakse ainult Gantti diagrammi madalaimal tasemel. Koondplaneerimise tööd kõikide ülesannete vaatamiseks valige **Laienda kõik**. Järelejäänud ülesannete hinnang põhineb ajaloolistel koondplaneerimise töödel.

## <a name="run-master-planning-and-track-processing-time"></a>Koondplaneerimise käitamine ja töötlemisaja jälgimine

1. Valige vaikimisi armatuurlaual **Koondplaneerimine**.
1. Sisestage või valige väärtus väljal **Plaan**.
1. Valige käsk **Käitus**.
1. Määrake suvandi **Töötlemisaja jälgimine** väärtuseks **Jah**.
1. Väljale **Lõimede arv** sisestage arv.
1. Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**.
1. Valige ruudustikus rida, kus väli **Väli** on määratud üksusele **Kaubakood**.
1. Sisestage väljal **Kriteeriumid** väärtus.
1. Valige nupp **OK**.
