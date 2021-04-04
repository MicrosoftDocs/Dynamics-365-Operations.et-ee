---
title: Kaupluset ei kuvata kaupluste loendis, kuhu saab järele minna
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui kaupluset ei kuvata kaupluste loendis, kust kaubad saab peale võtta.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: 652f5f1a779a412c21c18814071ba0fb7dd2e155
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585292"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>Kaupluset ei kuvata kaupluste loendis, kuhu saab järele minna

[!include [banner](../../includes/banner.md)]

See teema annab tõrkeotsingu juhised, mis aitavad, kui kaupluset ei kuvata kaupluste loendis, kust kaubad saab peale võtta.

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

[Tootmisüksuse loomine](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[Võrgukanali häälestamine](../channel-setup-online.md)
