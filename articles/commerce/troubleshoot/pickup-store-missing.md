---
title: Kaupluset ei kuvata kaupluste loendis, kuhu saab järele minna
description: See artikkel annab tõrkeotsingu juhised, mis aitavad, kui jaemüügikauplust ei kuvata kaupluste loendis, kus kaupu saab peale võtta.
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
ms.openlocfilehash: b6cec3d9d598be221516506388e4797ad579a610
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286748"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>Kaupluset ei kuvata kaupluste loendis, kuhu saab järele minna

[!include [banner](../../includes/banner.md)]

See artikkel annab tõrkeotsingu juhised, mis aitavad, kui jaemüügikauplust ei kuvata kaupluste loendis, kus kaupu saab peale võtta.

## <a name="description"></a>Kirjeldus

Jaekauplust ei kuvata kaupluste loendis, kust kaubad saab peale võtta.

## <a name="resolution"></a>Eraldusvõime

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a>Konfigureerige poe aadressi pikkus- ja laiuskraad Commerce Headquarters`is

Konfigureerige poe aadressi pikkus- ja laiuskraadid Commerce Headquarters`is, järgides järgmisi samme.

1. Minge jaotisse **Jaemüük ja kaubandus \> Kanalid \> Kauplused \> Kõik kauplused**.
1. Otsige kauplust, mida soovite kuvada e-ärisaidil järele minemise kohana. Tehke märkus selle **tootmisüksuse numbri** väärtuse kohta.
1. Avage **Organisatsiooni haldamine \> Organisatsioonid \> Tootmisüksused**.
1. Otsige varem märgitud tootmisüksuse numbrit ja seejärel valige otsingutulemustest tootmisüksus.
1. Valige **Aadressid** kiirkaardil suvand **Veel võimalusi** ja siis valige **Täpsem**.
1. Veenduge, et **Üldine** kiirkaardil oleks **Pikkuskraad** ja **Laiuskraad** õigesti seadistatud. Selle sammu osana veenduge, et väärtused on õigesti määratud positiivsete või negatiivsete numbritena.

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a>Täitmisgruppide konfigureerimine Commerce Headquarters`is

Commerce headquarters`is kannete redigeerimiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus \> Kanalid \> Veebipoed**.
1. Valige konfigureerimiseks võrgupood.
1. Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Täitmisgrupi määramine**.
1. Lehel **Täitmisgrupi määramine** valige veebipoe jaoks täitmisgrupp.
1. Veenduge et jaotises **Seadista** oleks jaekauplus õigesti konfigureeritud.

## <a name="additional-resources"></a>Lisaressursid 

[Tootmisüksuse loomine](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[Võrgukanali häälestamine](../channel-setup-online.md)
