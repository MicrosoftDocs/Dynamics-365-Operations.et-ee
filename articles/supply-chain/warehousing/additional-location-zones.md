---
title: Täiendavad asukohatsoonid
description: See artikkel annab ülevaate uutest Microsofti lisatud asukohatsoonidest Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: c20225cfb3c44fff955d0ad4e96c7fecf0ddf715
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900647"
---
# <a name="additional-location-zones"></a>Täiendavad asukohatsoonid

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Managementis on saadaval kolm uut tsoonivälja. Laohaldurid saavad määratleda nende abil täiendavaid ladude organisatsioone või paigutusi. Uusi tsoonivälju saab seadistada käsitsi või viisardi **Asukoha häälestus** abil. Neid saab kasutada mis tahes päringus või filtreerimises, mis kasutab tabelit Asukohad.

Tsooniväljade kasutamiseks pole vaja täiendavat häälestust.

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>Täiendava asukohatsooni funktsiooni sisse- või väljalülitamine

Tarneahela halduse versiooni 10.0.25 puhul lülitatakse see funktsioon vaikimisi sisse. Administraatorid saavad selle funktsiooni sisse või välja lülitada, otsides Funktsioonihalduse *tööruumist* täiendavat asukohatsooni [funktsiooni](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]