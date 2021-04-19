---
title: Kliendikirjeid ei kuvata Commerce headquarters`is
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui kliendikirjeid ei kuvata kohe Commerce Headquarters`is.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 5499e3c059c9e735df87ef8b462d446e0710d90c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801791"
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
