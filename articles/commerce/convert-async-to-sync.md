---
title: Asünkroonsete klientide teisendamine sünkroonseteks klientideks
description: See teema kirjeldab, kuidas teisendada asünkroonsed kliendid sünkroonsetele klientidele Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: fc1690ff6068317c748bda0d767a10f306f3debe
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691440"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Asünkroonsete klientide teisendamine sünkroonseteks klientideks

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas teisendada asünkroonsed kliendid sünkroonsetele klientidele Microsoft Dynamics 365 Commerce.

Asünkroonsed kliendid sünkroonseks klientideks teisendamiseks järgige neid samme.

1. Käitage Commerce Headquartersis **P-töö asünkroonsete** klientide saatmiseks Commerce Headquartersi.
1. Kliendikonto **ID-de loomiseks käivitage Async Mode** tööst klientide ja äripartnerite sünkroonimine. (Selle töö nimi oli varasem **Sünkroonige kliendid ja äripartnerid Async Mode'i abil**.)
1. Käivitage **1010** töö, et sünkroonida uued kliendi konto ID-d kanalitega.

Kui tellimus viitab asünkroonsele kliendile või aadressile, mida pole veel Commerce Headquartersiga sünkroonitud, **sünkroonitakse klient või aadress osana tellimuste sünkroonimise pakett-tööst**. Kui sularaha- ja ülekandekanne viitab asünkroonsele kliendile või aadressile, sünkroonitakse klient või aadress enne päeva lõpetamise (EOD) sisestamist.

## <a name="additional-resources"></a>Lisaressursid

[Kaupluste kliendihaldus](customer-mgmt-stores.md)

[Asünkroonne kliendi loomise režiim](async-customer-mode.md)

[Kliendi atribuudid](dev-itpro/customer-attributes.md)

[Võrguühenduseta andmete välistamine](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
