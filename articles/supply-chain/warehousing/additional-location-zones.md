---
title: Täiendavad asukohatsoonid
description: Selles teemas antakse ülevaate uutest Microsoft Dynamics 365 Supply Chain Managementi lisatud asukohatsoonidest.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 32114db4cf202870bae5ce307517170d3e618762
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597138"
---
# <a name="additional-location-zones"></a>Täiendavad asukohatsoonid

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Managementis on saadaval kolm uut tsoonivälja. Laohaldurid saavad määratleda nende abil täiendavaid ladude organisatsioone või paigutusi. Uusi tsoonivälju saab seadistada käsitsi või viisardi **Asukoha häälestus** abil. Neid saab kasutada mis tahes päringus või filtreerimises, mis kasutab tabelit Asukohad.

Tsooniväljade kasutamiseks pole vaja täiendavat häälestust.

## <a name="turn-on-the-additional-location-zone-feature"></a>Funktsiooni Täiendav asukohatsoon sisselülitamine

Enne funktsiooni *Täiendav asukohatsoon* kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Täiendav asukohatsoon*

## <a name="use-location-zones"></a>Asukohatsoonide kasutamine

1. Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukoha häälestuse viisard**.
2. Määrake järgmised väärtused.

    - Valige väljal **Ladu** väärtus _62_.
    - Valige väljal **Tsooni ID** väärtus _FLOOR_.
    - Valige väljal **Täiendav tsoon 1** väärtus _PICKZONE1_.
    - Valige väljal **Täiendav tsoon 2** väärtus _WEBSHOP1_.
    - Valige väljal **Asukoha profiili ID** väärtus _FLOOR_.

3. Valige rida **Korrus**.
4. Sisestage väljale **Alates numbrist** väärtus _1_. Sisestage väljale **Kuni numbrini** väärtus _3_.
5. Valige rida **Riiulirida**.
6. Sisestage väljale **Alates numbrist** väärtus _1_. Sisestage väljale **Kuni numbrini** väärtus _5_.
7. Valige **Loo**.
8. Teile kuvatakse teateid selle kohta, et uued asukohad on lisatud. Teadete nägemiseks valige nupp **Kuva sõnumid**.
9. Avage **Laohaldus \> Seadistus \> Ladu \> Asukohad**. Uued asukohad kuvatakse loendis ja kõik tsooniväljad on saadaval (st olemasolev tsooniväli ja uued täiendavad tsooniväljad).