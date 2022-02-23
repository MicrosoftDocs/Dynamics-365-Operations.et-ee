---
title: Etapi põhjuse koodide kasutamine
description: Teenindustaseme lepingu (SLA) tühistamise või SLA-s kehtestatud ajalimiidi ületamise põhjuse näitamiseks kasutate te põhjusekoodi.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4acba8f723ceb3d629671833db59c97a900c9f01
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965701"
---
# <a name="use-stage-reason-codes"></a>Etapi põhjuse koodide kasutamine 

[!include [banner](../includes/banner.md)]


Teenindustaseme lepingu (SLA) tühistamise või SLA-s kehtestatud ajalimiidi ületamise põhjuse näitamiseks kasutate te põhjusekoodi.

Samuti saate määrata, et põhjusekood on nõutav SLA tühistamisel või kui tähtaeg ületab hooldustellimuse SLA jaoks määratu.

Kui määrasite, et põhjuse tähis on nõutav, tuleb põhjusekood sisestada järgmistes olukordades:

  - Kui teenustellimus viiakse üle etappi, kus SLA-põhise teenustellimuse aja kirjendamise seiskub.

  - Kui teenustellimusest on välja logitud.

  - Kui aja kirjendamine peatatakse käsitsi.

## <a name="set-up-reason-codes"></a>Põhjusekoodide häälestamine

1.  Klõpsake valikuid **Teeninduse haldus** \> **Häälestus** \> **Hooldustellimused** \> **Etapi põhjuse koodid**.

2.  Klõpsake vormis **Etapi põhjusekoodid** uue põhjusekoodi loomiseks valikut **Uus**.

3.  Sisestage välja **Etapi põhjusekood** unikaalne etapi põhjusekood.

4.  Sisestage välja **Kirjeldus** etapi põhjusekoodi kirjeldus.

5.  Muudatuste salvestamiseks sulgege vorm.

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a>Põhjusekoodide nõudmine teenindustaseme lepingu tühistamisel

1.  Klõpsake valikul **Hooldushaldus** \> **Häälestus** \> **Teenuste halduse parameetrid**.

2.  Klõpsake vormis **Teenuste halduse parameetrid** linki **Üldine** ja valige märkeruut **Tühistamise põhjusekood**.

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a>Põhjusekoodide nõudmine teenindustaseme lepingus kehtestatud teenusetellimuse ajalimiidi ületamisel

1.  Klõpsake valikul **Hooldushaldus** \> **Häälestus** \> **Teenuste halduse parameetrid**.

2.  Klõpsake vormis **Teenuste halduse parameetrid** linki **Üldine** ja valige märkeruut **Aja ületamise põhjusekood**.

## <a name="see-also"></a>Vt ka

[teenustellimuses aja salvestuse käivitamine ja salvestamine](start-and-stop-time-recording-on-a-service-order.md)

  


