---
title: Liikuv keskmine varukulu järjestus
description: Sellest teemast saate teavet liikuva keskmise varukulu järjestuse arvutamise kohta Microsoft Dynamics 365 Supply Chain Managementis.
author: AndersGirke
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: d91b3b4b8d49e59aa03d62f4dd101b5a1ec18c41
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568203"
---
# <a name="moving-average-fallback-cost-sequence"></a>Liikuv keskmine varukulu järjestus

[!include [banner](../includes/banner.md)]

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

![Laoarvestuse parameetrid.](media/inventory-accounting-parameters.png "Laoarvestuse parameetrid")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]