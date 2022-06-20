---
title: Kliendikirjeid ei kuvata Commerce headquarters`is
description: See artikkel annab tõrkeotsingu juhised, mis aitavad aidata, kui kliendikirjeid ei kuvata kohe Commerce Headquartersis.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5cdc96c9829be4d34e9346b2c99d300c2349bc41
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876541"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>Kliendikirjeid ei kuvata Commerce headquarters`is

[!include [banner](../../includes/banner.md)]

See artikkel annab tõrkeotsingu juhised, mis aitavad aidata, kui kliendikirjeid ei kuvata kohe Commerce Headquartersis.

## <a name="description"></a>Kirjeldus

Kui loote uue kliendi kirje kasutades registreerumisvoogu e-äris, ei kuvata vastavat kliendikirjet kohe Commerce Headquarters`is.

## <a name="resolution"></a>Eraldusvõime

### <a name="disable-customer-creation-in-async-mode"></a>Kliendi loomise keelamine asünkroonimisrežiimis

> [!IMPORTANT]
> Kui keelate asünkroonse kliendi loomise, võib see mõjutada süsteemi jõudlust, sest iga kirje loomine loob Commerce Headquarters`ile reaalajas taotluse. Kui Commerce headquarters ei püsi (nt voogude hooldamisel), luuakse iga uue kliendi loomise voogu tõrkeid.

Kliendi loomise keelamiseks asükroonses režiimis Commerce headquarters`is, järgige neid samme.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Funktsiooniprofiilid**.
1. Kui te ei kasuta juba oma võrgukanali jaoks funktsiooniprofiili, looge üks.
1. Veenduge, et suvand **Loo klient asünkroonses režiimis** oleks seatud väärtusele **Ei**.
1. Avage **Jaemüük ja kaubandus \> Kanalid \> Veebipoed**.
1. Valige võrgupood, mille asünkroonse kliendi loomise keelata.
1. Vahekaardil **Üldine** veenduge, et **Funktsiooniprofiil** väli on seadistatud funktsiooniprofiilile, mida kasutate oma võrgukanalil.

## <a name="additional-resources"></a>Lisaressursid

[B2C-rentniku häälestus Commerce'is](../set-up-b2c-tenant.md)
