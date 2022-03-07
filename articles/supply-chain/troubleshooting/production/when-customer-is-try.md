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
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026424"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>Partiinumber eemaldatakse uue partii ID valimisel

KB number: 4613107

## <a name="symptoms"></a>Sümptomid

Kui valite komplekteerimislehe töölehe rea läbivaatamisel, tühjendatakse **partiinumbri välja** väärtus, kui valite väljal **Saatepartii ID** uue väärtuse.

## <a name="resolution"></a>Eraldusvõime

Süsteem käitub kavandatud viisil. Partii ID muutmisel muudate kauba konteksti. Seetõttu lähtestatakse partiinumber.

Partiinumbri seostamiseks saatepartii ID-ga peate esmalt seadistama saatepartii ID.
