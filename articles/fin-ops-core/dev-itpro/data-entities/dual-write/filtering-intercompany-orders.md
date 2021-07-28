---
title: Kontsernisiseste tellimuste filtreerimine tellimuse ja tellimuseridade sünkroonimise vältimiseks
description: See teema kirjeldab, kuidas filtreerida kontsernisiseseid tellimusi nii, et tellimuste ja tellimuseridade üksused ei oleks sünkroonitud.
author: negudava
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 5e7b0188d5c2dc4ee7691266aa4c857fc189d0f0
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347244"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>Kontsernisiseste tellimuste filtreerimine tellimuse ja tellimuseridade sünkroonimise vältimiseks

[!include [banner](../../includes/banner.md)]

Saate filtreerida kontsernisiseseid tellimusi nii, et tabeleid **Tellimused** ja **Tellimuseread** ei sünkroonita. Mõningatel juhtudel ei ole kontsernisiseste tellimuste üksikasjad klientide kaasamise rakenduses nõutavad.

Kõik standardsed teenuse Dataverse tabelid on laiendatud viidetega veerule **IntercompanyOrder** ja topeltkirjutamise kaardid on muudetud, et need viitaksid filtrites täiendavatele veergudele. Seega kontsernisiseseid tellimusi enam ei sünkroonita. See protsess aitab ennetada tarbetuid andmeid klientide kaasamise rakenduses.

1. Laiendage tabelit **CDS-i müügitellimuse päised**, lisades viite veerule **IntercompanyOrder**. See veerg täidetakse ainult kontsernisiseste tellimuste puhul. Veerg **IntercompanyOrder** on saadaval tabelis **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="CDS-i müügitellimuse päiste vastendamine kaardil sihtkohaks.":::

2. Pärast suvandi **CDS-i müügitellimuse päised** laiendamist on veerg **IntercompanyOrder** vastendamiseks saadaval. Rakendage filter, millel on `INTERCOMPANYORDER == ""`, päringu stringina.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="CDS-i müügitellimuse päisete päringu dialoogiboksi redigeerimine.":::

3. Laiendage tabelit **CDS-i müügitellimuse read**, lisades viite veerule **IntercompanyInventTransId**. See veerg täidetakse ainult kontsernisiseste tellimuste puhul. Veerg **InterCompanyInventTransId** on saadaval tabelis **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="CDS-i müügitellimuse ridade vastendamine kaardil sihtkohaks.":::

4. Pärast suvandi **CDS-i müügitellimuse read** laiendamist on veerg **IntercompanyInventTransId** vastendamiseks saadaval. Rakendage filter, millel on `INTERCOMPANYINVENTTRANSID == ""`, päringu stringina.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="CDS-i müügitellimuse ridade päringu dialoogiboksi redigeerimine.":::

5. Korrake samme 1 ja 2, et laiendada tabelit **Müügiarve päis V2**, ja lisage filtripäring. Sellisel juhul kasutage filtri päringustringina atribuuti `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Müügiarve päise V2 vastendamine kaardil sihtkoha lehele.":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Müügiarve päise V2 päringu dialoogiboksi redigeerimine.":::

6. Korrake samme 3 ja 4, et laiendada tabelit **Müügiarve read V2**, ja lisage filtripäring. Sellisel juhul kasutage filtri päringustringina atribuuti `INTERCOMPANYINVENTTRANSID == ""`.

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Müügiarve V2 päringu ridadde dialoogiboksi redigeerimine.":::

7. Tabelil **Pakkumised** puudub kontsernisisene suhe. Kui keegi loob ühe teie kontsernisisese kliendi jaoks pakkumise, saate kasutada veergu **CustGroup**, et panna kõik need kliendid ühte kliendigruppi. Saate laiendada päist ja ridu, lisades veeru **CustGroup** ja seejärel filtreerida nii, et gruppi ei kaasata.

    :::image type="content" source="media/filter-cust-group.png" alt-text="CDS-i müügipakkumise päise vastendamine kaardil sihtkoha lehele.":::

8. Pärast olemi **Pakkumised** laiendamist rakendage filter, millel on atribuut `CUSTGROUP != "<company>"`, päringu stringina.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="CDS-i müügipakkumise päise päringu dialoogiboksi redigeerimine.":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]