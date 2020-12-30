---
title: Kontsernisiseste tellimuste filtreerimine üksuste Orders ja OrderLines sünkroonimise vältimiseks
description: See teema kirjeldab, kuidas filtreerida kontsernisiseseid tellimusi üksuste Orders (Tellimused) ja OrderLines (Tellimuse read) sünkroonimise vältimiseks.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701029"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>Kontsernisiseste tellimuste filtreerimine üksuste Orders ja OrderLines sünkroonimise vältimiseks

[!include [banner](../../includes/banner.md)]

Saate filtreerida kontsernisiseseid tellimusi, et vältida üksuste **Orders** ja **OrderLines** sünkroonimist. Mõningatel juhtudel ei ole kontsernisiseste tellimuste üksikasjad klientide kaasamise rakenduses vajalikud.

Kõiki standardsed teenuse Common Data Service üksused on laiendatud viidetega väljale **IntercompanyOrder** ja topeltkirjutamise kaardid on muudetud, et need viitaksid filtrites täiendavatele väljadele. Selle tulemuseks on, et kontsernisiseseid tellimusi enam ei sünkroonita. See protsess väldib tarbetuid andmeid klientide kaasamise rakenduses.

1. Lisage üksuse **IntercompanyOrder** viide suvandile **CDS-i müügitellimuse päised**. See on täidetud ainult kontsernisiseste tellimuste puhul. Väli **IntercompanyOrder** on saadaval üksuses **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Sihtmärgini ajastamise kaardistamine, SalesOrderHeader":::
    
2. Pärast suvandi **CDS-i müügitellimuse päised** laiendamist on väli **IntercompanyOrder** vastendamiseks saadaval. Rakendage filter atribuudiga `INTERCOMPANYORDER == ""` päringu stringina.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Müügitellimuste päised, päringu redigeerimine":::

3. Lisage viide üksusest **IntercompanyInventTransId** suvandisse **CDS-i müügitellimuste read**.  See on täidetud ainult kontsernisiseste tellimuste puhul. Väli **InterCompanyInventTransID** on saadaval üksuses **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Sihtmärgini ajastamise kaardistamine, SalesOrderLine":::

4. Pärast suvandi **CDS-i müügitellimuse read** laiendamist on väli **IntercompanyInventTransId** vastendamiseks saadaval. Rakendage filter atribuudiga `INTERCOMPANYINVENTTRANSID == ""` päringu stringina.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Müügitellimuse read, päringu redigeerimine":::

5. Laiendage suvandid **müügitellimuse päis V2** ja **müügiarve read V2** samal viisil, nagu laiendasite teenuse Common Data Service olemid etappides 1 ja 2. Seejärel lisage filtri päringud. Filtri string suvandi **müügiarve päis V2** jaoks on `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`. Filtri string suvandi **müügiarve read V2** jaoks on `INTERCOMPANYINVENTTRANSID == ""`.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Sihtmärgini ajastamise kaardistamine, müügiarve päised":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Müügiarve päised, päringu redigeerimine":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Müügiarve read, päringu redigeerimine":::

6. Olemil **Pakkumised** puudub kontsernisisene suhe. Kui keegi loob ühe teie kontsernisisese kliendi jaoks pakkumise, saate panna kõik need kliendid ühte kliendigrupi, kasutades välja **CustGroup**.  Päist ja ridu saab laiendada, et lisada väli **CustGroup** ja seejärel filtreerida, et see grupp ei oleks kaasatud.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Sihtmärgini ajastamise kaardistamine, müügipakkumise päis":::

7. Pärast olemi **Pakkumised** laiendamist rakendage filter koos atribuudiga `CUSTGROUP !=  "<company>"` päringu stringina.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Müügipakkumise päis, päringu redigeerimine":::
