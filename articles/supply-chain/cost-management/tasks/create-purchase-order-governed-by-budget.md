---
title: Eelarvekohase ostutellimuse loomine
description: Kasutage seda protseduuri, et luua ostutellimus, mida kontrollitakse saadaoleva eelarve osas.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 100db102f74d477bcfde48a24828b817fd65e033
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239495"
---
# <a name="create-a-purchase-order-governed-by-budget"></a>Eelarvekohase ostutellimuse loomine

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]