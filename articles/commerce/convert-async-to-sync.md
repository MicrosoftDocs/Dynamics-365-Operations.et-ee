---
title: Asünkroonsete klientide teisendamine sünkroonseteks klientideks
description: See artikkel selgitab, kuidas teisendada asünkroonsed kliendid sünkroonsetele klientidele Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 0ce4906816deab8824b1079a34489e55651c0e03
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884387"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Asünkroonsete klientide teisendamine sünkroonseteks klientideks

[!include [banner](includes/banner.md)]

See artikkel selgitab, kuidas teisendada asünkroonsed kliendid sünkroonsetele klientidele Microsoft Dynamics 365 Commerce.

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
