---
title: Planeerimise koefitsiendid
description: "See artikkel sisaldab näiteid planeerimise koefitsiendi seadistamise kohta. Selles on teave mitmesuguste planeerimise koefitsiendi sätete ja nende tulemuste kohta. Planeerimise koefitsiendi abil saate määratleda, kuidas eelarvevajadusi vähendada."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: ff7525f4360e755e68ac3d7ecae281770481ef89
ms.lasthandoff: 03/31/2017


---

# <a name="reduction-keys"></a>Planeerimise koefitsiendid

See artikkel sisaldab näiteid planeerimise koefitsiendi seadistamise kohta. Selles on teave mitmesuguste planeerimise koefitsiendi sätete ja nende tulemuste kohta. Planeerimise koefitsiendi abil saate määratleda, kuidas eelarvevajadusi vähendada.

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a>1. näide. Prognoosi vähendamise põhimõte Protsent – planeerimise koefitsient
---------------------------------------------------------------

See näide selgitab, kuidas vähendab planeerimise koefitsient nõudluse prognoosi nõudeid planeerimise koefitsiendiga määratletud protsentide ja perioodide alusel.

1.  Seadistage lehel **Planeerimise koefitsiendid** järgmised read.
    | Muuda | Ühik  | Protsent |
    |--------|-------|---------|
    | 1      | Kuu | 100     |
    | 2      | Kuu | 75      |
    | 3      | Kuu | 50      |
    | 4      | Kuu | 25      |

2.  Linkige planeerimise koefitsient kauba laovarude grupiga.
3.  Valige lehel **Koondplaanid** väljal **Vähenduspõhimõte** suvand **Protsent – planeerimise koefitsient**.
4.  Looge nõudluse prognoos 1000 tk kuus.

Kui käivitate eelplaneerimise 1. jaanuaril, tabitakse nõudluse prognoosi nõudeid lehel **Planeerimise koefitsiendid** seadistatud protsentide järgi. Koondplaani kantakse üle järgmised vajaduse kogused.

| Kuu                | Vajalik tükkide arv |
|----------------------|---------------------------|
| Jaanuar              | 0                         |
| Veebruar             | 250                       |
| Märts                | 500                       |
| aprill                | 750                       |
| Mai kuni detsember | 1000                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a>Näide 2: Tehingute koefitsendi Ilmaennustus vähendamise põhimõte
See näide selgitab, kuidas vähendavad planeerimise koefitsiendiga määratletud perioodide ajal tehtavad tegelikud tellimused nõudluse prognoosi nõudeid.

-   Valige lehel **Koondplaanid** väljal **Vähenduspõhimõte** suvand **Kanded – planeerimise koefitsient**.

1. jaanuaril on olemas järgmised müügitellimused.

| Kuu    | Tellitud tükkide arv |
|----------|--------------------------|
| Jaanuar  | 956                      |
| Veebruar | 1,176                    |
| Märts    | 451                      |
| Aprill    | 119                      |

Kui kasutate sama nõudluse prognoosi (1000 tk kuus), kantakse koondplaani üle järgmised vajaduse kogused.

| Kuu                | Vajalik tükkide arv |
|----------------------|---------------------------|
| Jaanuar              | 44                        |
| Veebruar             | 0                         |
| Märts                | 549                       |
| aprill                | 881                       |
| Mai kuni detsember | 1000                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a>Näide 3: Tehingute dünaamiline perioodi eelarve vähendamise põhimõte
Enamasti on süsteemid seadistatud nii, et kanded vähendavad nõudluse prognoosi teatud prognoosiperioodide (nädalad, kuud jne) jooksul. Need perioodid on määratletud planeerimise koefitsiendis. Siiski võib ka kahe nõudluse perioodi rea vaheline aeg *tähendada* perioodi.

1.  Looge nõudluse prognoos järgmiste kuupäevade ja koguste kohta.
    | Kuupäev       | Nõudluse prognoos |
    |------------|-----------------|
    | 1. jaanuar  | 1000           |
    | 5. jaanuar  | 500             |
    | 12. jaanuar | 1000           |

    Selles prognoosis ei ole prognoosi kuupäevade vahel selget perioodi: esimese ja teise kuupäeva vahel on neljapäevane vahe ning teise ja kolmanda kuupäeva vahel on seitsmepäevane vahe. Need erinevad vahed on dünaamilised perioodid.
2.  Looge müügitellimuse read järgmiselt.
    | Kuupäev                             | Müügitellimuse kogus |
    |----------------------------------|----------------------|
    | Eelmise aasta 15. detsember | 500                  |
    | 3. jaanuar                        | 100                  |
    | 10. jaanuar                       | 200                  |

Prognoosi vähendatakse järgmiselt.

-   Esimene müügitellimus ei jää ühegi perioodi piiresse ega vähenda seega ühtki prognoosi.
-   Teine müügitellimus jääb 1. jaanuari ja 5. jaanuari vahele ning vähendab seega prognoosi 1. jaanuariks 100 võrra.
-   Kolmas müügitellimus jääb 5. jaanuari ja 12. jaanuari vahele ning vähendab seega prognoosi 5. jaanuariks 200 võrra.

Järgmine plaanitud tellimus luuakse prognoosi täitmiseks.

| Nõudluse prognoosi kuupäev | Vähendatud kogus |
|----------------------|------------------|
| 1. jaanuar            | 900              |
| 5. jaanuar            | 300              |
| 12. jaanuar           | 1000            |

Siin on toodud vähenduse **Kanded – dünaamiline periood** kokkuvõte.

-   Eelarvevajadusi vähendatakse tegelike tellimusekannete võrra, mis tehakse dünaamilise perioodi jooksul. Dünaamiline periood katab praeguse eelarve kuupäevad ja lõpeb järgmise prognoosi algusega.
-   See meetod ei kasuta ega nõua planeerimise koefitsienti.
-   Selle suvandi kasutamisel ilmneb järgmine käitumine.
    -   Prognoosi täielikul vähendamisel muutub praeguse prognoosi eelarvevajaduseks 0 (null).
    -   Kui tulevasi prognoose pole, vähendatakse eelarvevajadusi viimati sisestatud prognoosist.
    -   Prognoosi vähenduse arvutamisse kaasatakse ajapiirid.
    -   Prognoosi vähenduse arvutamisse kaasatakse positiivne päevade arv.
    -   Kui tellimuse tegelikud kanded ületavad eelarvevajadusi, ei edastata järelejäänud kandeid järgmisse prognoosiperioodi.


<a name="see-also"></a>Vt ka
--------

[Master plans](master-plans.md)


