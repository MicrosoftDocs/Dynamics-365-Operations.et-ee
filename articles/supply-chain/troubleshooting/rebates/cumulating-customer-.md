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
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760366"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Kliendi tagasimaksete kumuleerimine kauba tagasimaksegruppide abil nurjub

KB number: 4611372

## <a name="symptoms"></a>Sümptomid

Kui kasutate kliendi tagasimakseleppeid (*summa* tüüp) kombinatsioonis kauba tagasimaksegruppidega, arvutatakse tagasimaksed, kuid kumuleerimine nurjub.

## <a name="resolution"></a>Eraldusvõime

Süsteem käitub kavandatud viisil. Kaubagrupid grupeerivad ainult sama lävitingimusega kaubad. Tagasimakse tingimus (lävi) seatakse iga kauba summa suhtes, mitte iga kaubagrupi kauba kumuleeritud summa suhtes.
