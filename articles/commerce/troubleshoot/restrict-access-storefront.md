---
title: Piirake katsetamise või arenduse ajal ligipääsu kauplusele
description: See teema kirjeldab, kuidas piirata juurdepääsu Microsoft Dynamics 365 Commerce sisemistele testimistele ja arendustele.
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
ms.openlocfilehash: cdc9b6af55bcba98f5ea7607bb1847f61a707778
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018334"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>Piirake katsetamise või arenduse ajal ligipääsu kauplusele

[!include [banner](../../includes/banner.md)]

See teema kirjeldab, kuidas piirata juurdepääsu Microsoft Dynamics 365 Commerce sisemistele testimistele ja arendustele.

## <a name="description"></a>Kirjeldus

Sisetestimisel või aktiivsel arenduse ajal soovite võibolla piirata juurdepääsu oma saidile, et takistada väliskasutajatel pääseda juurde avaldatud siselao lehtedele.

## <a name="resolution"></a>Eraldusvõime

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>Azure AD B2C seadistamine standardsete kasutajavoogude abil

Teavet Azure Active Directory (Azure AD B2C) konfigureerimise kohta e-kaubanduse saidi jaoks vaata [B2C rentniku seadistamine Commerce`s](../set-up-b2c-tenant.md).

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>Piira kasutaja juurdepääsu kaupluse lehtedele ja blokeeri uute kasutajate loomine

Rakenduse Commerce saidi koostajas kasutaja juurdepääsu piiramiseksfronte lehekülgedele, järgige neid samme.

1. Avage rakenduses oma sait.
1. Valige **leheküljed** ja seejärel valige leht, mille kasutaja juurdepääsu piirata.
1. Valige moodul või killupesa ja seejärel valige käsk **Redigeeri**.
1. Valige atribuutide paanil suvand **Nõuab sisselogimist?** ja valige suvand **Lõpeta redigeerimine**.
1. Valige **Avalda**.

Uute kasutajate loomise blokeerimiseks Azure AD järgige neid samme.

1. Avage [Azure’i portaalis](https://portal.azure.com/).
1. Valige Azure AD B2C-rakendus, mille lõite oma saidi juurdepääsuks.
1. Valige vasakpoolsel navigeerimispaanil suvand **Kasutaja voog**.
1. Ülal **Kasutaja voog** lehel valige **Uus kasutajavoog**.
1. Lehel **Valige kasutaja voo tüüp** valige suvand **Eelvaade**.
1. Lehe keskel valige **Logi sisse v2**. Seejärel järgige [Commerce'i B2C rentniku häälestamise samme](../set-up-b2c-tenant.md) voo konfigureerimiseks oma saidi standardse kasutajavoona Azure AD B2C jaoks testimise või arendamise ajal.

## <a name="additional-resources"></a>Lisaressursid

[B2C-rentniku häälestus Commerce'is](../set-up-b2c-tenant.md)

[Kohandatud lehtede häälestus kasutajate sisselogimise jaoks](../custom-pages-user-logins.md)
