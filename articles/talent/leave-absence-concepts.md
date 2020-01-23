---
title: Puhkuste ja puudumiste põhimõtted
description: Selles teemas kirjeldatakse puhkuste ja puudumiste mõisteid ja kuidas vaba aja saldosid määratletakse.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 03e2557e29194f17a9a586470ced5b352408b07c
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898638"
---
# <a name="leave-and-absence-concepts"></a>Puhkuste ja puudumiste põhimõtted

Mõistete ja tingimuste abil, mida selles teemas kirjeldatakse, saate määrata, kuidas antakse töötajale töölt vaba aega ja kuidas selle töötaja ajasaldosid arvutada. Puhkuste ja puudumiste halduse kohta lisateabe saamiseks vt [Puhkuste ja puudumiste haldus](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).

## <a name="leave-plan-details"></a>Puhkuseplaani üksikasjad

### <a name="start-date"></a>Alguskuupäev

Alguskuupäev on see kuupäev, mil viitvõlgade töötlus algab. Alguskuupäev on samas ka edasikantavate summade arvutamiseks kasutatav tähtpäeva kuupäev.

## <a name="accruals"></a>Viitvõlad

Viitvõlad määravad, millal ja kui sageli määratakse töötajale vaba aega. Poliitika selle kohta, millal viitvõlgu määrata, ja poliitika proportsionaalse arvestuse kohta on määratletud jaotises **Viitvõlad** puhkuste ja puudumiste plaani loomisel.

### <a name="accrual-frequency"></a>Puhkuse andmise sagedus

Puhkuse andmise sagedus määratleb, kui tihti on puhkus kogunenud või määratud. Valikud on järgmised:

- Kord päevas
- Iganädalane
- Kaks korda nädalas
- Kaks korda kuus
- Kord kuus
- Kord kvartalis
- Poolaasta kohta
- Kord aastas
- Pole

### <a name="accrual-period-basis"></a>Puhkuseperioodi alus

Puhkuseperioodi baas määratleb kuupäeva, mida kasutatakse puhkuseperioodi arvutamiseks. Valikud on järgmised:

- **Plaanitav alguskuupäev**
- **Töötajale kindlal kuupäeval** - selle suvandi valimisel määratleb selle väärtus puhkuseperioodide alguskuupäeva allikat. Valikud on järgmised:

    - Kohandatud
    - Tähtpäeva kuupäev
    - Värbamise algne kuupäev
    - Staaž kuupäeval
    - Töötaja töösuhte korrigeeritud alguskuupäev
    - Töötaja töösuhte alguskuupäev

### <a name="accrual-award-date"></a>Puhkuse andmise kuupäev

Puhkuse andmise kuupäev määrab, millal antakse töötajale vaba aega. Valikud on järgmised:

- **Viitvõlgade lõppkuupäev** – töötajale määratakse puhkus puhkuseperioodi viimasel päeval.

    Õige koguse lisandumisel peab viitvõlgade protsess sisaldama kogu perioodi. Näiteks puhkuseperiood on 1. jaanuarist 2018 kuni 31. jaanuarini 2018. Sel juhul, et kaasata jaanuari, käivitatakse viitvõlg 1. veebruaril 2018.

- **Viitvõlgade alguskuupäev** – töötajale määratakse puhkus puhkuseperioodi esimesel päeval.

### <a name="accrual-policy-on-enrollment"></a>Viitvõlgade poliitika registreerimine

Viitvõlgade poliitika registreerimise määratleb viitvõlgade arvutamise, kui töötaja on liitunud keset puhkuseperioodi. Valikud on järgmised:

- **Proportsionaalne arvestus** – kuupäevade vahemik, mida kasutatakse päevade erinevuse määramiseks registreerimise kuupäevast kuni alguskuupäevani. Viitvõlgade töötlemisel rakendatakse seda erinevust.
- **Täielik arvestus** – täielik arvestuslik kogus, mis põhineb järgul, antakse esimesel arvestuslikul töötlemisel.
- **Arvestus puudub** – pole viitvõlgade andmist enne järgmist puhkuseperioodi.

### <a name="accrual-policy-on-unenrollment"></a>Viitvõlgade poliitika registreerimise tühistamise kohta

Viitvõlgade poliitika registreerimise tühistamise kohta määratleb viitvõlgade arvutamise, kui töötaja on lahkunud keset puhkuseperioodi. Valikud on järgmised:

- **Proportsionaalne arvestus** – kuupäevade vahemik, mida kasutatakse päevade erinevuse määramiseks registreerimise kuupäevast kuni alguskuupäevani. Viitvõlgade töötlemisel rakendatakse seda erinevust.
- **Täielik arvestus** – täielik arvestuslik kogus, mis põhineb järgul, antakse esimesel arvestuslikul töötlemisel.
- **Arvestus puudub** – pole viitvõlgade andmist enne järgmist puhkuseperioodi.

## <a name="accrual-schedule"></a>Viitvõlgade skeemid

Viitvõlgade graafik määrab, kuidas töötaja puhkuse aeg koguneb ja millised summad antud töötajal kogunevad ja edasi kanduvad. Järkusid saab luua nii, et vaba aega premeeritakse erinevate tasemete alusel.

### <a name="months-of-service"></a>Töötatud kuud

Jaotise **Töötatud kuud** väärtus määratleb kuude miinimumarvu, kui palju töötaja peab töötama, et tal oleks õigus viitvõlgadele. Kui miinimuumarv töötajate kohta puudub, määrake väärtuseks **0**.

### <a name="hours-worked"></a>Töötunnid

Jaotise **Töötunnid** väärtus määratleb tundide miinimumarvu, kui palju töötaja peab puhkuseperioodi kohta töötama, et tal oleks õigus viitvõlgadele. Kui miinimuumarv töötajate kohta puudub, määrake väärtuseks **0**.

### <a name="accrual-amount"></a>Juurdekasvu summa

Viitvõla summat arvestatakse tundides või päevades, mis kogunevad töötajale perioodi kohta. Periood põhineb puhkuse andmise sageduse põhjal.

### <a name="minimum-balance"></a>Minimaalne saldo

Kui töötajad võtavad rohkem puhkust välja, kui neile on ette nähtud, võib miinimumsaldole anda negatiivse väärtuse.

### <a name="maximum-carry-forward"></a>Maksimaalne edasikandmine

Viitvõlgade protsess kohandab puhkusesaldod, mis ületab alguskuupäeva aastapäeva ülekandmise maksimumsaldot.

### <a name="grant-amount"></a>Hüvitise summa

Hüvitise summa on tundide või päevade esmane arv, mis töötajale antakse, kui nad esmakordselt registreeruvad puhkuseplaani. See summa ei kogune iga viitvõlaperioodiga.

## <a name="enrollments-and-balances"></a>Registreerimised ja saldod

### <a name="enrollment-date"></a>Registreerimise kuupäev

Registreerimise kuupäev määratleb, millal töötaja saaks alustada vaba aja kogumist. Näiteks kui töötaja on liitunud 15. juunil 2018 puhkusekavasse, ei saa tal vaba aega koguneda enne 15. juunit 2018.

### <a name="current-balance"></a>Praegune saldo

Praegune saldo on puhkuse aja taotluste jaoks saadaolev summa. See summa sisaldab viitvõlgu, kinnitatud taotlusi ja korrigeerimisi kuni praeguse kuupäevani.

### <a name="current-balance-examples"></a>Praeguse saldo näited

#### <a name="annual-plan"></a>Aastaplaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Registreerimise kuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus | Puhkuse andmise kuupäev    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Aastane            | Plaanitav alguskuupäev      | Puhkuseperioodi lõpp |

Viitvõlad töödeldakse 01. jaanuaril 2019 (01/01/2019), nii et kogu perioodi ei kaasata.

**Tulemused**

| Juurdekasvu summa | Minimaalne saldo | Maksimaalne edasikandmine | Taotletud summa | Praegune saldo (01. jaanuari 2019 seisuga) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Praegune saldo (160) = viitvõla summa (200) – taotluse summa (40)

#### <a name="semimonthly-plan"></a>Poole kuu plaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Registreerimise kuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus | Puhkuse andmise kuupäev    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaks korda kuus       | Plaanitav alguskuupäev      | Puhkuseperioodi lõpp |

Viitvõlad töödeldakse 01. mail 2018 (01/05/2018), nii et kogu perioodi ei kaasata.

**Tulemused**

| Juurdekasvu summa | Minimaalne saldo | Maksimaalne edasikandmine | Taotletud summa | Praegune saldo (01. jaanuari 2019 seisuga) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Praegune saldo (22) = viitvõla summa (5 × 6) – taotluse summa (8)

#### <a name="monthly-plan"></a>Kuuplaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Registreerimise kuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus | Puhkuse andmise kuupäev    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaks korda kuus       | Plaanitav alguskuupäev      | Puhkuseperioodi lõpp |

Viitvõlad töödeldakse 01. mail 2018 (01/05/2018), nii et kogu perioodi ei kaasata.

**Tulemused**

| Juurdekasvu summa | Minimaalne saldo | Maksimaalne edasikandmine | Taotletud summa | Praegune saldo (01. jaanuari 2019 seisuga) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Praegune saldo (7) = viitvõla summa (5 × 3) – taotluse summa (8)

### <a name="forecasted-balance"></a>Prognoositud saldo

See *eelarvesaldo* on tulevasel kuupäeval saadaolev puhkuse kogus. Viitvõlgade ja ülekandmise korrigeerimised on prognoositud selleks kuupäevaks.

Arvutamisel kasutatakse järgmist valemit:

Esmaspäeva prognoositud saldo = praegune saldo – taotlused + viitvõlad – ülekandmise korrigeerimine

### <a name="forecasted-balance-examples"></a>Prognoositud saldo näited

#### <a name="annual-plan"></a>Aastaplaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Registreerimise kuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus | Puhkuse andmise kuupäev    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Aastane            | Plaanitav alguskuupäev      | Puhkuseperioodi lõpp |

Viitvõlad töödeldakse 15. veebruaril 2019 (15/02/2019), nii et kogu perioodi ei kaasata.

**Tulemused**

| Juurdekasvu summa | Minimaalne saldo | Maksimaalne edasikandmine | Praegune saldo | Prognoositud saldo (15. veebruari 2019 seisuga) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Prognoositud saldo (40) = juurdekasvu summa (20) – praegune saldo (40) – ülekandmise korrigeerimine (20)

#### <a name="semimonthly-plan"></a>Poole kuu plaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Registreerimise kuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus | Puhkuse andmise kuupäev    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaks korda kuus       | Plaanitav alguskuupäev      | Puhkuseperioodi lõpp |

Viitvõlad töödeldakse 15. veebruaril 2019 (15/02/2019), nii et kogu perioodi ei kaasata.

**Tulemused**

| Juurdekasvu summa | Minimaalne saldo | Maksimaalne edasikandmine | Praegune saldo | Prognoositud saldo (15. veebruari 2019 seisuga) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Prognoositud saldo (35) = juurdekasvu summa (5 × 3) + praegune saldo (40) – ülekandmise korrigeerimine (20)

#### <a name="monthly-plan"></a>Kuuplaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Registreerimise kuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus | Puhkuse andmise kuupäev    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kaks korda kuus       | Plaanitav alguskuupäev      | Puhkuseperioodi lõpp |

Viitvõlad töödeldakse 15. veebruaril 2019 (15/02/2019), nii et kogu perioodi ei kaasata.

**Tulemused**

| Juurdekasvu summa | Minimaalne saldo | Maksimaalne edasikandmine | Praegune saldo | Prognoositud saldo (15. veebruari 2019 seisuga) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Prognoositud saldo (30) = juurdekasvu summa (10 × 1) – praegune saldo (40) – ülekandmise korrigeerimine (20)

### <a name="proration-balance-examples"></a>Proportsionaalse arvestuse saldo näited

#### <a name="prorated-monthly-plan"></a>Proportsionaalse arvestuse kuuplaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Kord kuus           | Plaanitav alguskuupäev      |

**Tulemused**

| Töötaja            | Töötatud kuud | Registreerimise kuupäev | Alguskuupäev | Juurdekasvu summa | Viitvõlgade protsess | Saldo |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2,53    |

#### <a name="full-accrual-monthly-plan"></a>Täieliku arvestuse kuuplaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Kord kuus           | Plaanitav alguskuupäev      |

**Tulemused**

| Töötaja            | Töötatud kuud | Registreerimise kuupäev | Alguskuupäev | Juurdekasvu summa | Viitvõlgade protsess | Saldo |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>Arvestuse puudumise kuuplaan

**Plaani seadistus**

| Plaanitav alguskuupäev | Puhkuse andmise sagedus | Puhkuseperioodi alus |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Kord kuus           | Plaanitav alguskuupäev      |

**Tulemused**

| Töötaja            | Töötatud kuud | Registreerimise kuupäev | Alguskuupäev | Juurdekasvu summa | Viitvõlgade protsess | Saldo |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2.00    |
