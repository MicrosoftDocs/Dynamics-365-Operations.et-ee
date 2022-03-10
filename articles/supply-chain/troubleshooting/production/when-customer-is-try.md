---
title: Partiinumber eemaldatakse uue partii ID valimisel
description: Kui valite komplekteerimislehe töölehe rea läbivaatamisel, tühjendatakse partiinumbri välja väärtus, kui valite väljal Saatepartii ID uue väärtuse.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6d71720b1d3a34a31639db0f829dee300d6f96d53fd61c0a8740be9f2306d6dd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738815"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>Partiinumber eemaldatakse uue partii ID valimisel

KB number: 4613107

## <a name="symptoms"></a>Sümptomid

Kui valite komplekteerimislehe töölehe rea läbivaatamisel, tühjendatakse **partiinumbri välja** väärtus, kui valite väljal **Saatepartii ID** uue väärtuse.

## <a name="resolution"></a>Eraldusvõime

Süsteem käitub kavandatud viisil. Partii ID muutmisel muudate kauba konteksti. Seetõttu lähtestatakse partiinumber.

Partiinumbri seostamiseks saatepartii ID-ga peate esmalt seadistama saatepartii ID.
