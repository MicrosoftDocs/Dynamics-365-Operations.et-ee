---
title: Litsentsiplaati ei saa teisaldada, kui on lubatud tühi väljaminek ja sissetulek on tühi
description: Litsentsiplaati ei saa teisaldada, kui seerianumber on tühi ja lubatud on tühi kviitung. See määratakse kindlaks, muutes seerianumbri välja valikuliseks.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476112"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>Litsentsiplaati ei saa teisaldada, kui seerianumber on tühi ja lubatud on tühi väljaminek

## <a name="symptoms"></a>Sümptomid

Te ei saa teisaldada litsentsiplaati kasutades **Teisaldamine** menüükäsku, kui seerianumbril on jälgimise dimensiooni grupis *Tühjad väljaminekud lubatud* ja *Tühjad vastuvõtmised lubatud* ning kui mitu litsentsiplaati on samas asukohas, millest mõnel on seerianumbrid ja mõnel ei ole.

## <a name="resolution"></a>Lahendus

See probleem parandatakse muudatustega, mida kasutatakse [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Need muudatused muudavad **Seerianumbri** välja valikuliseks, kui tühi sissetulek ja tühi väljaminek on lubatud.
