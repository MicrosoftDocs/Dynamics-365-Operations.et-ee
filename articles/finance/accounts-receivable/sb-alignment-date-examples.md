---
title: Joonduse kuupäeva stsenaariumid
description: See teema pakub näiteid, mis näitavad, kuidas joonduse kuupäevad kordustellimuse arvelduses töötavad.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: e80797e8dd532bb4b2ef78422b459487430d83d6
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629703"
---
# <a name="alignment-date-scenarios"></a>Joonduse kuupäeva stsenaariumid

See teema pakub näiteid, mis näitavad, kuidas joonduse kuupäevad kordustellimuse arvelduses töötavad.

Nende näidete puhul on arveldusgraafiku arvelduse üksikasja joondamise kuupäev 31. oktoober 2019. Esimene rea arvelduse üksikasi lõpeb 31. oktoober 2019 ja jagatakse sellele vastavalt. Rida uuendatakse automaatselt, kasutades 11. novembri alguskuupäeva.

> [!NOTE]
> Aasta on oluline, kuna see võib põhjustada joonduskuupäeva rohkem või vähem kui aasta. Nende näidete puhul on katsetusmeetodiks kord kuus **lehel** Korduva **lepingu arveldusparameetrid**. Kui selle väärtuseks on määratud **Igapäevane**, erinevad mõned osalised summad.

## <a name="scenario-1-no-alignment"></a>Stsenaarium 1: joondus puudub

Arveldusgraafik seadistatakse järgmiste andmetega:

- **Alguskuupäev:** 1. mai 2019
- **Lõppkuupäev:** 31. detsember 2024
- **Summa:** $1,000

| Arvelduse alguskuupäev | Arvelduse lõppkuupäev | Eelmine lugemine | Praegune näit | Kogus sisestatud | Vaba kogus | Arveldatav kogus | Ühiku hind |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 30.4.2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2020 | 4/30/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2021 | 4/30/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2022 | 4/30/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2023 | 4/30/2024 | | | 1.00 | | 1.00 | 1,000.00 |
| 5/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-2-shortened-alignment"></a>2. stsenaarium: lühijoondus

Arveldusgraafik seadistatakse järgmiste andmetega:

- **Alguskuupäev:** 1. mai 2019
- **Lõppkuupäev:** 31. detsember 2024
- **Summa:** $1,000
- **Joonduskuupäev:** 31. detsember 2019

Esimene uuendatav summa on vähem kui aasta.

| Arvelduse alguskuupäev | Arvelduse lõppkuupäev | Eelmine lugemine | Praegune näit | Kogus sisestatud | Vaba kogus | Arveldatav kogus | Ühiku hind |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |
| 1.1.2020 | 31.12.2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2022 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-3-extended-alignment"></a>3. stsenaarium: laiendatud joondus

Arveldusgraafik seadistatakse järgmiste andmetega:

- **Alguskuupäev:** 1. mai 2019
- **Lõppkuupäev:** 31. detsember 2024
- **Summa:** $1,000
- **Joonduskuupäev:** 31. detsember 2020

Esimene uuendatav summa on rohkem kui ühe aasta jaoks.

| Arvelduse alguskuupäev | Arvelduse lõppkuupäev | Eelmine lugemine | Praegune näit | Kogus sisestatud | Vaba kogus | Arveldatav kogus | Ühiku hind |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 31.12.2020 | | | 1.00 | | 1.00 | 1,666.67 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2022 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 1,000.00 |

## <a name="scenario-4-alignment-with-a-different-end-month"></a>4. stsenaarium: joondamine teise lõppkuuga

Arveldusgraafik seadistatakse järgmiste andmetega:

- **Alguskuupäev:** 1. mai 2019
- **Lõppkuupäev:** 31. oktoober 2024
- **Summa:** $1,000
- **Joonduskuupäev:** 31. detsember 2019

> [!NOTE]
> See stsenaarium ei ole üldine.

| Arvelduse alguskuupäev | Arvelduse lõppkuupäev | Eelmine lugemine | Praegune näit | Kogus sisestatud | Vaba kogus | Arveldatav kogus | Ühiku hind |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |
| 1.1.2020 | 31.12.2020 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2021 | 12/31/2021 | | | 1.00 | | 1.00 | 1,000.00 |
| 1.1.2022 | 12/31/2022 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 1,000.00 |
| 1/1/2024 | 10/31/2024 | | | 1.00 | | 1.00 | 833.33 |

## <a name="scenario-5-single-partial-year"></a>5. stsenaarium: üks osaline aasta

Arveldusgraafik seadistatakse järgmiste andmetega:

- **Alguskuupäev:** 1. mai 2019
- **Lõppkuupäev:** 31. detsember 2019
- **Summa:** $1,000
- **Joonduskuupäev**: 31. detsember 2019

Selles stsenaariumis pole joonduse kuupäev vajalik. See stsenaarium on automaatsel uuendamisel tavaline.

| Arvelduse alguskuupäev | Arvelduse lõppkuupäev | Eelmine lugemine | Praegune näit | Kogus sisestatud | Vaba kogus | Arveldatav kogus | Ühiku hind |
|---|---|---|---|---|---|---|---|
| 5/1/2019 | 12/31/2019 | | | 1.00 | | 1.00 | 666.67 |

## <a name="scenario-6-calculated-dates"></a>6. stsenaarium: arvutatud kuupäevad

Tugi ja uuendamine on seadistatud järgmiste andmetega:

- **Alistamise alguskuupäev:** ei
- **Toe ja uuendamise alguskuupäevad:** järgmise kuu algus
- **Arve sisestamise kuupäev:** 22. juuni 2019
- **Joonduskuupäev:** 31. detsember 2020

| Arvelduse alguskuupäev | Arvelduse lõppkuupäev | Eelmine lugemine | Praegune näit | Kogus sisestatud | Vaba kogus | Arveldatav kogus | Ühiku hind |
|---|---|---|---|---|---|---|---|
| 7/1/2019 | 7/31/2019 | | | 1.00 | | 1.00 | 297.60 |
| 8/1/2019 | 31.12.2020 | | | 1.00 | | 1.00 | 6,936.00 |

## <a name="scenario-7-calculated-dates-and-future-posting"></a>7. stsenaarium: arvutatud kuupäevad ja tulevane sisestamine

Tugi ja uuendamine on seadistatud järgmiste andmetega:

- **Alistamise alguskuupäev:** ei
- **Toe ja uuendamise alguskuupäevad:** järgmise kuu algus
- **Arve sisestamise kuupäev:** 22. juuni 2019
- **Joonduskuupäev:** 31. detsember 2020

Selle stsenaariumi puhul muudetakse joonduskuupäevaks 31. detsember 2021.

| Arvelduse alguskuupäev | Arvelduse lõppkuupäev | Eelmine lugemine | Praegune näit | Kogus sisestatud | Vaba kogus | Arveldatav kogus | Ühiku hind |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 8/1/2019 | 31.12.2020 | | | 1.00 | | 1.00 | 4,250.00 |

## <a name="scenario-8-manual-dates-and-multiple-years"></a>Stsenaarium 8: käsitsi kuupäevad ja mitu aastat

Tugi ja uuendamine on seadistatud järgmiste andmetega:

- **Alistamise alguskuupäev:** Jah
- **Uuendamise alguskuupäev:** 1. juuli 2020
- **Uuendamise lõppkuupäev:** 31. detsember 2024
- **Joonduskuupäev:** 31. detsember 2021

| Arvelduse alguskuupäev | Arvelduse lõppkuupäev | Eelmine lugemine | Praegune näit | Kogus sisestatud | Vaba kogus | Arveldatav kogus | Ühiku hind |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 7/1/2020 | 12/31/2021 | | | 1.00 | | 1.00 | 375.00 |
| 1.1.2022 | 12/31/2022 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2024 | 12/31/2024 | | | 1.00 | | 1.00 | 250,00 |

## <a name="scenario-9-manual-dates-multiple-years-and-a-different-end-month"></a>Stsenaarium 9: käsitsi kuupäevad, mitu aastat ja teine lõppkuu

Tugi ja uuendamine on seadistatud järgmiste andmetega:

- **Alistamise alguskuupäev:** Jah
- **Uuendamise alguskuupäev:** 1. juuli 2020
- **Uuendamise lõppkuupäev:** 31. oktoober 2024
- **Joonduskuupäev:** 31. detsember 2021

| Arvelduse alguskuupäev | Arvelduse lõppkuupäev | Eelmine lugemine | Praegune näit | Kogus sisestatud | Vaba kogus | Arveldatav kogus | Ühiku hind |
|---|---|---|---|---|---|---|---|
| 6/22/2019 | 6/22/2019 | | | 1.00 | | 1.00 | 0,00 |
| 7/1/2020 | 12/31/2021 | | | 1.00 | | 1.00 | 375.00 |
| 1.1.2022 | 12/31/2022 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2023 | 12/31/2023 | | | 1.00 | | 1.00 | 250,00 |
| 1/1/2024 | 10/31/2024 | | | 1.00 | | 1.00 | 208.33 |

## <a name="scenario-10-alignment-without-proration"></a>Stsenaarium 10: joondamine ilma katseta

Tugi ja uuendamine on seadistatud järgmiste andmetega:

- **Alistamise alguskuupäev:** ei
- **Arve sisestamise kuupäev:** 22. juuni 2019
- **Joonduskuupäev:** 31. detsember 2019

Uuendamise alguskuupäev ja joonduse kuupäevad korrigeeritakse nii, et mõlemad alguskuupäevad on pärast sisestuskuupäeva.

- **Uuendamise alguskuupäev:** 1. jaanuar 2020
- **Uuendamise lõppkuupäev:** 31. detsember 2020
