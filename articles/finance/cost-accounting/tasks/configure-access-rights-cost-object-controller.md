---
title: Kuluobjekti kontrolleri pääsuõiguste konfigureerimine
description: Selle protseduuri abil saate konfigureerida kuluobjekti kontrollija pääsuõigusi.
author: kfend
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17615ff70c15789ac30223464b20ccd61a1bad55
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710626"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>Kuluobjekti kontrolleri pääsuõiguste konfigureerimine

[!include [banner](../../includes/banner.md)]

Selle protseduuri abil saate konfigureerida kuluobjekti kontrollija pääsuõigusi. See salvestis kasutab USP2 demoandmete ettevõtet.


## <a name="assign-the-cost-object-controller-role"></a>Kuluobjekti kontrollija rolli määramine
1. Minge jaotisse Süsteemihaldus > Kasutajad > Kasutajad.
2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtreerida välja Kasutajanimi väärtuse "alicia" järgi.
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake suvandit Määra rollid.
5. Otsige loendist ja valige soovitud kirje.
6. Klõpsake nuppu OK.

## <a name="enable-access-list-security"></a>Juurdepääsuloendi turbe lubamine
1. Valige menüü Kuluarvestus jaotis Dimensioonid ja seejärel jaotis Dimensioonihierarhiad.
2. Otsige loendist ja valige soovitud kirje.
    * Valige suvand Organisatsioon.  
3. Klõpsake nuppu Redigeeri.
4. Valige väljal Juurdepääsuloendi hierarhia väärtus Jah.
5. Klõpsake käsku Kuva hierarhia.

## <a name="assign-access-rights-to-user"></a>Kasutajale pääsuõiguste määramine
1. Klõpsake valikut Uus.
2. Märkige loendis valitud rida.
3. Sisestage või valige väärtus väljal Kasutaja ID.
    * Valige suvand Administraator.  
4. Valige puus väärtus "Organization\CEO\CFO\FIM".
5. Klõpsake valikut Uus.
6. Märkige loendis valitud rida.
7. Sisestage või valige väärtus väljal Kasutaja ID.
    * Valige Alicia.  
8. Klõpsake nuppu Salvesta.

## <a name="enable-access-rights-in-cost-accounting"></a>Pääsuõiguste lubamine kuluarvestuses
1. Valige menüü Kuluarvestus > Seadistus > Parameetrid.
2. Klõpsake vahekaarti Üldine.
3. Valige väljal Luba kuvamise juurdepääs kuluobjekti dimensiooniliikmete jaoks väärtus Jah.
4. Klõpsake nuppu Salvesta.
5. Sulgege leht.
6. Valige menüü Kuluarvestus > Seadistus > Kulujuhtimise tööruumi konfiguratsioon.
7. Klõpsake nuppu Redigeeri.
8. Valige väljal Avaldatud väärtus Jah.
    * Kui klõpsate nuppu Jah, saab kasutaja, kellele on määratud üks järgmisest neljast rollist, vaadata aruandeid kulude juhtimise tööruumis: kuluarvestuse haldur, kuluarvestaja, kuluarvestuse spetsialist ja kuluobjekti kontrollija. Kui klõpsate nuppu Ei, saab ainult kasutaja, kellele on määratud üks järgmistest rollidest, vaadata aruandeid: kuluarvestuse haldur, kuluarvestaja ja kuluarvestuse spetsialist.    
9. Klõpsake nuppu Salvesta.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
