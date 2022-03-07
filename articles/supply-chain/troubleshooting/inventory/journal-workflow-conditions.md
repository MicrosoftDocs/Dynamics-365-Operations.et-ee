---
title: Varude töölehe töövoo tingimused kehtivad ainult töölehe tasemel, mitte rea tasemel
description: Varude töölehe töövoo tingimused kehtivad ainult töölehe tasemel, mitte rea tasemel.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 46bdde7f09c639fbefd46162431762b056d521ae
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476119"
---
# <a name="inventory-journal-workflow-conditions-apply-at-the-journal-level-not-line-level"></a>Varude töölehe töövoo tingimused kehtivad ainult töölehe tasemel, mitte rea tasemel

## <a name="symptoms"></a>Sümptomid

Teil võib tekkida selline probleem, kui proovite näiteks seadistada varude töölehe töövoo tingimust kulusummale. Seadistate tingimuse nii, et 1. etappi käitatakse ainult siis, kui omahind on väiksem kui 100. Seejärel seadistate teise tingimuse nii, et 2. etappi käitatakse ainult siis, kui omahind on suurem või võrdne kui 100. Töövoo käivitamisel kuvatakse töövoo ajaloos ainult üks rida ja esimene tingimus hinnatakse alati *tõesena*, sõltumata edastatud väärtusest.

## <a name="workaround"></a>Vastukaal

Praeguses versioonis kehtivad varude töövoo tingimused ainult töölehe tasemel, mitte rea tasemel. Selline käitumine on nii kavandatud. Soovitame seada tingimuse kriteeriumiks ainult töölehe taseme atribuudid.
