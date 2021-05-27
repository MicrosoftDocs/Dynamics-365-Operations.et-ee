---
title: Kliendikirjeid ei kuvata Commerce headquarters`is
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui kliendikirjeid ei kuvata kohe Commerce Headquarters`is.
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
ms.openlocfilehash: b8d065dd104df616ba8f10f7813e74c900fdcf77
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018478"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>Kliendikirjeid ei kuvata Commerce headquarters`is

[!include [banner](../../includes/banner.md)]

See teema annab tõrkeotsingu juhised, mis aitavad, kui kliendikirjeid ei kuvata kohe Commerce Headquarters`is.

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
