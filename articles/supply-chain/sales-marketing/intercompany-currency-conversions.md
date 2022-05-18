---
title: Kontsernisisene valuuta teisendamine
description: See teema kirjeldab kontsernisiseste kannete valuuta teisendusi
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f0af05c324bb67744ba6650e3d7a4ba8b958040e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671894"
---
# <a name="intercompany-currency-conversions"></a>Kontsernisisene valuuta teisendamine

[!include [banner](../../includes/banner.md)]

Kui algse müügitellimuse ja kontsernisisese ostutellimuse valuutakood erinevad, siis sünkroonimise lubamise korral järgmiste väljade valuutad teisendatakse:

- **Ühiku hind**
- **Müügitasud** või **Ostutasud**
- **Allahindlus**
- **Multiallahindlus**

Seejärel sünkroonitakse need väljad kontsernisisese müügitellimuse reaga.

Kuna kontsernisisese ostutellimuse ja kontsernisisese müügitellimuse valuuta sünkroonitakse alati, siis sünkroonitakse järgmised väljad ilma valuuta teisendamiseta:

- **Ühiku hind**
- **Müügitasud** või **Ostutasud**
- **Allahindlus**
- **Allahindluse protsent**
- **Multiallahindlus**
- **Multiallahindluse protsent**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
