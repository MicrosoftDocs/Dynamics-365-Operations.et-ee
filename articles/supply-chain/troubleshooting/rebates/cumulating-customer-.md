---
title: Kliendi tagasimaksete kumuleerimine kauba tagasimaksegruppide abil nurjub
description: Kui kasutate kliendi tagasimakseleppeid kombinatsioonis kauba tagasimaksegruppidega, arvutatakse tagasimaksed, kuid kumuleerimine nurjub.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026429"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Kliendi tagasimaksete kumuleerimine kauba tagasimaksegruppide abil nurjub

KB number: 4611372

## <a name="symptoms"></a>Sümptomid

Kui kasutate kliendi tagasimakseleppeid (*summa* tüüp) kombinatsioonis kauba tagasimaksegruppidega, arvutatakse tagasimaksed, kuid kumuleerimine nurjub.

## <a name="resolution"></a>Eraldusvõime

Süsteem käitub kavandatud viisil. Kaubagrupid grupeerivad ainult sama lävitingimusega kaubad. Tagasimakse tingimus (lävi) seatakse iga kauba summa suhtes, mitte iga kaubagrupi kauba kumuleeritud summa suhtes.
