---
title: Kuluarvutuse tase
description: Selles teemas kirjeldatakse koosluse (BOM) taset, mille nimi on kuluarvutuse tase. See koosluse tase ei arvesta arvutamisel ei tootmis- ega partiitellimusi.
author: JennySong-SH
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 563d866c93e9205914f633f3435ef4b46f85b814
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679551"
---
# <a name="cost-calculation-level"></a>Kuluarvutuse tase

[!include [banner](../includes/banner.md)]

Koosluse (BOM) taseme puhul, mille nimi on **Kulu arvutamise tase**, ei arvestata arvutamisel ei tootmis- ega partiitellimusi. Süsteem kasutab seda taset kuluarvutuse versioonides kulu arvutamisel. Protsessides, nagu ümberarvutamine ja lao sulgemine, kasutab süsteem hoopis koosluse taset **Kuluarvutuse tase**.

Järgmises lihtsas stsenaariumis on näha, mille poolest erinevad koosluse tase **Kulu arvutamise tase** ja koosluse tase **Kuluarvutuse tase**.

Teil on kolm toodet: A, B ja C. Toode C on toote B komponent ning toode B on toote A komponent.

- **Kuluarvutuse tase** määrab järgmised koosluse tasemed.

    - **Toode A:** 0
    - **Toode B:** 1
    - **Toode C:** 2

- **Kulu arvutamise tase** määrab järgmised koosluse tasemed.

    - **Toode A:** 0
    - **Toode B:** 1
    - **Toode C:** 2

Seejärel luuakse tootmistellimus toote C jaoks ning toode A lisatakse tootmistellimuse kooslusesse. Pärast tellimuse hindamist uuendatakse koosluse tasemed järgmisel viisil.

- **Kuluarvutuse tase** määrab järgmised koosluse tasemed.

    - **Toode B:** 1
    - **Toode C:** 2
    - **Toode A:** 3

- **Kulu arvutamise tase** määrab järgmised koosluse tasemed.

    - **Toode A:** 0
    - **Toode B:** 1
    - **Toode C:** 2

Selline käitumine tagab, et tootmistellimuse kooslustes tehtud muudatused ei mõjuta hilisemat kulu arvutamist.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]