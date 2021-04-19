---
title: Kuluarvutuse tase
description: Selles teemas kirjeldatakse koosluse (BOM) taset, mille nimi on kuluarvutuse tase. See koosluse tase ei arvesta arvutamisel ei tootmis- ega partiitellimusi.
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f7cde239107528a6bc2aeb0e424d024d4f3fb2a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839483"
---
# <a name="cost-calculation-level"></a>Kuluarvutuse tase

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