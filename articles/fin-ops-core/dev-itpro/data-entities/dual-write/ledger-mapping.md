---
title: Integreeritud pearaamat
description: Selles teemas kirjeldatakse pearaamatu andmete integreerimist rakenduse Finance and Operations ja teiste Dynamics 365 rakenduste vahel teenust Dataverse kasutades.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.openlocfilehash: 18a95725af8014845d6fb39806917de7632ad56b92b75387cd916de927127b38
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723077"
---
# <a name="integrated-ledger"></a>Integreeritud pearaamat

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Ärirakenduses määratlevad pearaamatu andmed põhiseadistuse, kuidas ettevõtte äri ajab. Näiteks kirjeldavad pearaamatu andmed finantsaastat, mida ettevõte järgib, valuutasid, milles see arveldab, ja kontosid, mida see kasutab. Selles teemas kirjeldatakse nende põhiliste finantsandmete integreerimist.

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
