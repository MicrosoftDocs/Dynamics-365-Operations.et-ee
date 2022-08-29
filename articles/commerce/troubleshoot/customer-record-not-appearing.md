---
title: Kliendikirjeid ei kuvata Commerce headquarters`is
description: See artikkel annab tõrkeotsingu juhised, mis aitavad aidata, kui kliendikirjeid ei kuvata kohe Commerce Headquartersis.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: f1ad1f45abbc95cbf6d41b3c8681db781c6c9d23
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268834"
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
