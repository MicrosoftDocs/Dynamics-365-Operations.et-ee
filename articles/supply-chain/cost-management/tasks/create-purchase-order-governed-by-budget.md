--- 
title: Eelarvekohase ostutellimuse loomine
description: Kasutage seda protseduuri, et luua ostutellimus, mida kontrollitakse saadaoleva eelarve osas.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc024caa54db6629a1e573df295fe8333996647
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-governed-by-budget"></a>Eelarvekohase ostutellimuse loomine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kasutage seda protseduuri, et luua ostutellimus, mida kontrollitakse saadaoleva eelarve osas. See salvestis kasutab USMF demoandmete ettevõtet.


## <a name="review-the-budget-control-configuration"></a>Vaadake üle eelarve juhtimise konfiguratsioon
1. Avage Eelarve koostamine > Häälestamine > Eelarve juhtimine > Eelarve juhtimise konfiguratsioon.
2. Klõpsake vahekaarti Saadaval eelarvefondid.
3. Klõpsake vahekaarti Dokumendid ja töölehed.
4. Klõpsake vahekaarti Eelarve juhtimise määratlemine.
5. Klõpsake vahekaarti Eelarvegruppide määratlemine.
6. Sulgege leht.

## <a name="create-the-purchase-order-header"></a>Ostutellimuse päise loomine
1. Avage Hanked > Ostutellimused > Kõik ostutellimused.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Hankija konto või valige see.
4. Laiendage jaotist Üldine.
5. Määrake aruandluskuupäeva väljal kuupäev „2016-01-01”.
6. Klõpsake nuppu OK.

## <a name="add-a-purchase-order-line"></a>Ostutellimuse rea lisamine
1. Sisestage või valige väärtus väljal Hanke kategooria.
2. Valige välja Kogus väärtuseks 2.
3. Sisestage või valige väärtus väljal Ühik.
4. Määrake ühiku hinna väärtuseks „10000”.
5. Klõpsake suvandit Finantsid.
6. Klõpsake suvandit Summade jaotamine.
7. Määrake pearaamatukonto väljal väärtus „601300-001-023--”.
8. Sulgege leht.

## <a name="perform-budget-checking"></a>Eelarve kontrollimine
1. Klõpsake suvandit Finantsid.
2. Klõpsake valikut Eelarve kontrollimine.
3. Klõpsake suvandit Finantsid.
4. Klõpsake valikut Eelarvekontrolli tõrked ja hoiatused.
5. Klõpsake valikut Sule.


