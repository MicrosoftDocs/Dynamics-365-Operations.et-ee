---
title: Liikuv keskmine varukulu järjestus
description: Sellest teemast saate teavet liikuva keskmise varukulu järjestuse arvutamise kohta Microsoft Dynamics 365 Supply Chain Managementis.
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 541b7ecca5c1c36999f573d6d0f2dc0c9e901631
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967579"
---
# <a name="moving-average-fallback-cost-sequence"></a>Liikuv keskmine varukulu järjestus

Üks võimalus varude kulu arvutamiseks on selle tegemine _jooksva keskmise_ abil. Iga laokaubaga saab seostada kuni kolm kuluväärtust.

- **Viimane väljastus** – viimase väljastuse kulu, mis määrati enne varude negatiivseks muutumist
- **Aktiivne kulu** – hiljutisim kulu, mis aktiveeriti kuluarvutuse versioonis
- **Kauba hind** – väljastatud toote jaoks määratud kulu

Selleks, et määrata, millist kuluväärtust kasutada jooksva keskmise arvutamise puhul, kasutab süsteem _varukulu järjestust_ väärtuste eelistuse järjekorra määramiseks. Kui eelistatud kuluväärtus ei ole saadaval, kasutab süsteem järgmist eelistatud väärtust jne.

Microsoft Dynamics 365 Supply Chain Managementi varasemates versioonides kasutas süsteem fikseeritud varukulu järjestust (_Viimane väljastus – aktiivne kulu – kauba hind_). Versioonis 10.0.11 on see järjestus endiselt vaikejärjestus. Kuid saate ka sisse lülitada funktsiooni, mis võimaldab teil valida kolme saadaoleva varukulu järjestuse hulgast. See funktsioon võib olla eriti kasulik organisatsioonidele, mis kasutavad regulaarselt negatiivseid varude väärtusi.

Kui soovite, et varukulu järjestus oleks saadaval, peate (või administraator) aktiveerima [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) abil funktsiooni nimega _Liikuv keskmine varukulu järjestus_.

Liikuva keskmise varukulu järjestuse valimiseks toimige järgmiselt.

1. Avage leht **Parameetrid**.
2. Määrake vahekaardi **Laoarvestus** jaotises **Liikuv keskmine** väljale **Varukulu järjestus** üks järgmistest väärtustest.

    - **Viimane väljastus – Aktiivne kulu – Kauba hind** – see järjestus on vaikejärjestus. Seda järjestust kasutatakse siis, kui funktsioon _Liikuv keskmine varukulu järjestus_ ei ole sisse lülitatud.
    - **Aktiivne kulu – Viimane väljastus**
    - **Aktiivne kulu – kauba hind** – organisatsioonidel võib esineda jõudluse probleeme, kui kasutatakse äriprotsesse, kus laovarud muutuvad regulaarselt negatiivseks ja samal ajal on kannete maht kõrge. See säte aitab vähendada neid jõudluse probleeme.

![Laoarvestuse parameetrid](media/inventory-accounting-parameters.png "Laoarvestuse parameetrid")
