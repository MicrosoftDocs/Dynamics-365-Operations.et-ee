---
title: Integreeritud pearaamat
description: See artikkel kirjeldab pearaamatu andmete integreerimist finantside ja toimingute ning teiste Dynamics 365 rakenduste vahel Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 728c131c260586e7f1f787f22ccf02ed81c94c01
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289144"
---
# <a name="integrated-ledger"></a>Integreeritud pearaamat

[!include [banner](../../includes/banner.md)]



Ärirakenduses määratlevad pearaamatu andmed põhiseadistuse, kuidas ettevõtte äri ajab. Näiteks kirjeldavad pearaamatu andmed finantsaastat, mida ettevõte järgib, valuutasid, milles see arveldab, ja kontosid, mida see kasutab. See artikkel kirjeldab selle finantse põhiandmete integreerimist.

## <a name="templates"></a>Mallid

Pearaamatu andmed sisaldavad põhiliste finantsiliste tabelikaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.

Finance and Operations rakendused | Klientide kaasamise rakendused     | Kirjeldus
---------------------------------|----------------------------------|------------
[CDS-i valuutakursid](mapping-reference.md#123) | msdyn_currencyexchangerates |
[Kontoplaan](mapping-reference.md#121) | msdyn_chartofaccountses |
[Valuutad](mapping-reference.md#218) | transactioncurrencies |
[Vahetuskursi valuutapaar](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[Vahetuskursi tüüp](mapping-reference.md#129) | msdyn_exchangeratetypes |
[Finantsdimensiooni vorming](mapping-reference.md#130) | msdyn_financialdimensionformats |
[Finantsdimensioonid](mapping-reference.md#128) | msdyn_dimensionattributes |
[Rahanduskalendri integratsiooniüksus](mapping-reference.md#132) | msdyn_fiscalcalendars |
[Rahanduskalendri periood](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[Rahanduskalendri aasta integratsiooniüksus](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[Ledger](mapping-reference.md#148) | msdyn_ledgers |
[Põhikonto](mapping-reference.md#152) | msdyn_mainaccounts |
[Põhikonto kategooriad](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

