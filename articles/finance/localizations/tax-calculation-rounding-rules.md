---
title: Maksuarvutuse ümardamisreeglid
description: Teemas antakse teavet maksu arvutamise teenuse maksuarvutuse parameetrite ümardamisreeglite kohta.
author: kailiang
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 38760879d84d8262cc1e8395c59bcbc0429bc753
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7347681"
---
# <a name="tax-calculation-rounding-rules"></a>Maksuarvutuse ümardamisreeglid

[!include [banner](../includes/banner.md)]

Teemas antakse teavet, kuidas maksu arvutamise teenuse maksuarvutuse parameetrites ümardamisreeglid toimivad.

> [!NOTE] 
> Kui maksu arvutamise teenus on lubatud, ei ole lehtedel **Käibemaksukood** ja **Käibemaksugrupp** olevad ümardamisreeglid kehtivad.

Maksu arvutamise teenuse ümardamisreeglite konfiguratsiooni saate vaadata jaotise **Käibemaksu ümardamisreeglid** lehe **Maksuarvutuse parameetrid** vahekaardi **Üldist** kiirkaardilt **Arvutamine** (**Maks** \> **Seadistamine** \> **Maksukonfiguratsioon** \> **Maksuarvutuse parameetrid**).

[![Ümardamisreegli konfiguratsioon maksuarvutuse parameetrite lehel](./media/tax-calculation-parameters-calculation-1.png)](./media/tax-calculation-parameters-calculation-1.png)

Väljad **Ümardamistäpsus** ja **Ümardamismeetod** määratlevad, kuidas maksu arvutamise teenuse koormuses arvutatud summasid ümardatakse.

## <a name="rounding-precision"></a>Ümardamistäpsus

Väli **Ümardamistäpsus** toetab väärtust, millel on kuni kuus kümnendkohta. Kui määrate näiteks välja **Ümardamistäpsus** väärtuseks **0,000000**, ümardatakse arvutatud summad kuue kümnendkohani ja saadetakse siis rakendusse Microsoft Dynamics 365 Finance. Näiteks kui kasutatakse ümardamismeetodit **Tavaline**, ümardatakse summa **987,1234567** summaks **987,123457**.

> [!NOTE]
> Finance ümardab summad vastavalt valuuta ümardamisreeglitele. Seetõttu mõjutavad kannetes kuvatud ja talletatud maksusummasid nii maksuarvutuse ümardamisreeglid kui ka valuuta ümardamisreeglid.

## <a name="rounding-method"></a>Ümardamismeetod

Maksuarvutuse ümardamismeetodit saab konfigureerida iga juriidilise isiku jaoks. Väljal **Ümardamismeetod** saate valida kolme suvandi vahel: **Tavaline**, **Allapoole** ja **Ümardamine**.

### <a name="rounding-example"></a>Ümardamise näide

Järgmises tabelis on näide, mis näitab, kuidas summat **987,345** ümardatakse ümardamistäpsuse ja ümardamismeetodite erinevate kombinatsioonide puhul.

<table>
<thead>
<tr>
<th rowspan="2">Ümardamismeetod</th>
<th colspan="8">Ümardamistäpsus</th>
</tr>
<tr>
<th>0,00</th>
<th>0.01</th>
<th>0.10</th>
<th>1.00</th>
<th>10.00</th>
<th>0.02</th>
<th>0.05</th>
<th>0.25</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tavaline</td>
<td>987.35</td>
<td>987.35</td>
<td>987.30</td>
<td>987.00</td>
<td>990.00</td>
<td>987.34</td>
<td>987.35</td>
<td>987.25</td>
</tr>
<tr>
<td>Allapoole</td>
<td>987.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.00</td>
<td>980.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.25</td>
</tr>
<tr>
<td>Ümardamine</td>
<td>988.00</td>
<td>987.35</td>
<td>987.40</td>
<td>988.00</td>
<td>990.00</td>
<td>987.36</td>
<td>987.35</td>
<td>987.50</td>
</tr>
</tbody>
</table>

Maksusummade arvutamise ja ümardamise loogikat saab konfigureerida vastavalt maksureeglitele.

## <a name="rounding-by"></a>Ümardusalus 

Valige väljal **Ümardusalus** ümardamispõhimõte, mida maksudele rakendatakse. Valikud on järgmised:

- **Maksukoodid** – maksusumma ümardatakse iga maksukoodi sees.
- **Maksukoodide kombinatsioonid** – maksusumma ümardatakse real oleva maksukoodi kombinatsiooni sees.

## <a name="calculation-method"></a>Arvutamismeetod

Valige väljal **Arvutamismeetod**, kas arvete maks arvutatakse iga rea kohta eraldi või kõigi ridade kohta kokku. Valikud on järgmised:

- **Rida** – maksusumma arvutamine ridahaaval. Igal real olevat maksusummat teiste ridade maksusummad ei mõjuta.
- **Kokku** – saate arvutada maksusumma ühe dokumendi kõigil ridadel.

### <a name="rounding-calculation-example"></a>Ümardamise arvutamise näide

Näide toob ära erinevad arvutused, mida ühe arve jaoks teha saab, kasutades väärtuste **Ümardusalus** ja **Arvutusmeetod** erinevaid kombinatsioone. Selle näite puhul kasutatakse järgmist seadistust.

- Arvel on neli rida.
- Esineb kaks maksukoodi: **KM1** (10 protsenti) ja **KM2** (10 protsenti).
- Ümardamistäpsuseks on **0,01**.
- Ümardamismeetodiks on **Ümardamine**.

#### <a name="rounding-by--tax-codes-and-calculation-method--line"></a>Ümardusalus = maksukoodid ja arvutusmeetod = rida

| Rea number | Rea netosumma | Määratud maksukoodid | Maksusumma enne ümardamist | Ümardatud maksusumma |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | KM1                 | 1.111                      | 1.12               |
| 2           | 22.22           | KM1; KM2           | 2,222; 2,222               | 2,23; 2,23         |
| 3           | 33.33           | KM1                 | 3.333                      | 3.34               |
| 4           | 44.44           | KM1; KM2           | 4,444; 4,444               | 4,45; 4,45         |

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--line"></a>Ümardusalus = maksukoodide kombinatsioonid ja arvutusmeetod = rida

| Rea number | Rea netosumma | Määratud maksukoodid | Maksusumma enne ümardamist | Ümardatud maksusumma |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | KM1                 | 1.111                      | 1.12               |
| 2\*         | 22.22           | KM1; KM2           | 2,222; 2,222               | 2,23; 2,22         |
| 3           | 33.33           | KM1                 | 3.333                      | 3.34               |
| 4\*\*       | 44.44           | KM1; KM2           | 4,444; 4,444               | 4,45; 4,44         |

\* 2. rida = ümardamine\[22,22 × (10 protsenti + 10 protsenti)\] = 2,23 + 2,22

\*\* 4. rida = ümardamine\[44,44 × (10 protsenti + 10 protsenti)\] = 4,45 + 4,44

#### <a name="rounding-by--tax-codes-and-calculation-method--total"></a>Ümardusalus = maksukoodid ja arvutusmeetod = kokku

| Rea number | Rea netosumma | Määratud maksukoodid | Maksusumma enne ümardamist | Ümardatud maksusumma |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | KM1\*               | 1.111                      | 1.12               |
| 2           | 22.22           | KM1\*; KM2\*\*     | 2,222; 2,222               | 2,22; 2,23         |
| 3           | 33.33           | KM1\*               | 3.333                      | 3.33               |
| 4           | 44.44           | KM1\*; KM2\*\*     | 4,444; 4,444               | 4,44; 4,44         |

\* KM1(1. rida, 2. rida, 3. rida 4. rida) = ümardamine\[(11,11 + 22,22 + 33,33 + 44,44) × 10 protsenti\] = 1,12 + 2,22 + 3,33 + 4,44

\*\* KM2(2. rida, 4. rida) = ümardamine\[(22,22 + 44,44) × 10 protsenti\] = 2,23 + 4,44

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--total"></a>Ümardusalus = maksukoodide kombinatsioonid ja arvutusmeetod = kokku

| Rea number | Rea netosumma | Määratud maksukoodid | Maksusumma enne ümardamist | Ümardatud maksusumma |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1\*         | 11.11           | KM1                 | 1.111                      | 1.12               |
| 2\*\*       | 22.22           | KM1; KM2           | 2,222; 2,222               | 2,23; 2,22         |
| 3\*         | 33.33           | KM1                 | 3.333                      | 3.33               |
| 4\*\*       | 44.44           | KM1; KM2           | 4,444; 4,444               | 4,44; 4,45         |

\* 1. rida, 3. rida = ümardamine\[(11,11 + 33,33) × 10 protsenti\] = 1,12 + 3,33

\*\* 2. rida, 4. rida = ümardamine\[(22,22 + 44,44) × (10 protsenti + 10 protsenti)\] = 2,23 + 2,22 + 4,44 + 4,45

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
