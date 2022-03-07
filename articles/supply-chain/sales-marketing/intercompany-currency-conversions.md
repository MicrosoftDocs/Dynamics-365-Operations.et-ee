---
title: Kontsernisisene valuuta teisendamine
description: See teema kirjeldab kontsernisiseste kannete valuuta teisendusi
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 540849003d532ef2f0905c18332d9cb82a04cf7c
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548226"
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
