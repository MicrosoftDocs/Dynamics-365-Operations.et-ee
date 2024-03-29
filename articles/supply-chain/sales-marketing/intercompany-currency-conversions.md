---
title: Kontsernisisene valuuta teisendamine
description: See artikkel selgitab kontsernisiseste kannete valuutateisendusi.
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
ms.openlocfilehash: 41bfafc0dcb3bd356931b67dc63b717c0d098116
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851474"
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
