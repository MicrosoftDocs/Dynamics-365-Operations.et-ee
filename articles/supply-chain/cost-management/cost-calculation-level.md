---
title: Kuluarvutuse tase
description: See artikkel kirjeldab koosluse taset nimega Kulukalkulatsiooni tase. See koosluse tase ei arvesta arvutamisel ei tootmis- ega partiitellimusi.
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: e63a868696e36c1d4f5d19ea87bdf4d682c39f8c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334951"
---
# <a name="cost-calculation-level"></a>Kuluarvutuse tase

[!include [banner](../includes/banner.md)]

Koosluse (BOM) taseme puhul, mille nimi on **Kulu arvutamise tase**, ei arvestata arvutamisel ei tootmis- ega partiitellimusi. Süsteem kasutab seda taset kuluarvutuse versioonides kulu arvutamisel. Protsessides, nagu ümberarvutamine ja lao sulgemine, kasutab süsteem hoopis koosluse taset **Kuluarvutuse tase**.

## <a name="turn-the-cost-calculation-level-feature-on-or-off"></a>Lülitab kuluarvutuse taseme funktsiooni sisse ja välja

Selle funktsiooni kasutamiseks peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.29 puhul lülitatakse funktsioon vaikimisi sisse. Administraatorid saavad selle funktsiooni sisse või välja lülitada, otsides Funktsioonihalduse *tööruumis* kuluarvutuse [taseme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) funktsiooni.

## <a name="example-scenario"></a>Näidisstsenaarium

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