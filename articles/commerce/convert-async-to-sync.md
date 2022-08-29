---
title: Asünkroonsete klientide teisendamine sünkroonseteks klientideks
description: See artikkel selgitab, kuidas teisendada asünkroonsed kliendid sünkroonsetele klientidele Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: b442bfc0685706359771e4d9e2729565d3652a60
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278188"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Asünkroonsete klientide teisendamine sünkroonseteks klientideks

[!include [banner](includes/banner.md)]

See artikkel selgitab, kuidas teisendada asünkroonsed kliendid sünkroonsetele klientidele Microsoft Dynamics 365 Commerce.

Asünkroonsed kliendid sünkroonseks klientideks teisendamiseks järgige neid samme.

1. Käitage Commerce Headquartersis **P-töö asünkroonsete** klientide saatmiseks Commerce Headquartersi.
1. Kliendikonto **ID-de loomiseks käivitage Async Mode** tööst klientide ja äripartnerite sünkroonimine. (Selle töö nimi oli varasem **Sünkroonige kliendid ja äripartnerid Async Mode’i abil**.)
1. Käivitage **1010** töö, et sünkroonida uued kliendi konto ID-d kanalitega.

Kui tellimus viitab asünkroonsele kliendile või aadressile, mida pole veel Commerce Headquartersiga sünkroonitud, **sünkroonitakse klient või aadress osana tellimuste sünkroonimise pakett-tööst**. Kui sularaha- ja ülekandekanne viitab asünkroonsele kliendile või aadressile, sünkroonitakse klient või aadress enne päeva lõpetamise (EOD) sisestamist.

## <a name="additional-resources"></a>Lisaressursid

[Kaupluste kliendihaldus](customer-mgmt-stores.md)

[Asünkroonne kliendi loomise režiim](async-customer-mode.md)

[Kliendi atribuudid](dev-itpro/customer-attributes.md)

[Võrguühenduseta andmete välistamine](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
