---
title: Pärast keskkonna kopeerimist puuduvad tooted ja kategooriad
description: See artikkel annab tõrkeotsingu juhised, mis aitavad, kui tooted ja kategooriad puuduvad pärast saidi kopeerimist keskkondade vahel või samas keskkonnas.
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
ms.openlocfilehash: 0c094f6da7756d2a6a3b80ebdb211d7b78148813
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851101"
---
# <a name="products-and-categories-missing-after-environment-copy"></a>Tooted ja kategooriad pärast keskkonna kopeerimist puuduvad

[!include [banner](../../includes/banner.md)]

See artikkel annab tõrkeotsingu juhised, mis aitavad, kui tooted ja kategooriad puuduvad pärast saidi kopeerimist keskkondade vahel või samas keskkonnas.

## <a name="description"></a>Kirjeldus

Kui sait on kopeeritud ühest keskkonnast või samas keskkonnas, puuduvad tooted ja kategooriad saidilt. Tooted ja kategooriad puuduvad e-kaubanduse laost ja e-commerce'i saidilooja **tooted** vahekaardilt.

## <a name="resolution"></a>Eraldusvõime

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a>Kanali tootmisüksuse numbri vastendamine äsja kopeeritud saidiga Commerce'i saidi koostajas

Kanali tootmisüksuse numbri vastendamine äsja kopeeritud saidiga Commerce'i saidi koostajas, jälgige järgmisi samme.

1. Valige äsja kopeeritud sait.
1. Jaotises **Saidi sätted** valige **Kanalid**.
1. Kanali nime kõrval valige kolmikpunkt (**...**) ja seejärel valige suvand **Muuda võrgupoe kanalit**.
1. Dialoogiboksis **Võrgupoe kanali muutmine** valige kanal, mida vast kopeeritud saidiga vvastendada ja seejärel valige **OK**.
1. Valige käsk **Salvesta ja avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Dynamics 365 Commerce'i saidi seostamine võrgukanaliga](../associate-site-online-store.md)
