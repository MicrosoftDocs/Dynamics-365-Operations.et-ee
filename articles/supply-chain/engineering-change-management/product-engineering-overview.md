---
title: Tehniliste muudatuste halduse ülevaade
description: See teema annab ülevaate tehniliste muudatuste haldusest, mis aitab teil planeerida ja hallata toote versioonimist ning hallata toote töötsüklit ja tehnilisi muudatusi.
author: t-benebo
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: f1aa04b472eaef7ed398f08a05d46bac2d589561
ms.sourcegitcommit: 9f32389715b226c11e74c53547527e0a8b51e300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514346"
---
# <a name="engineering-change-management-overview"></a>Tehniliste muudatuste halduse ülevaade

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Funktsiooni kokkuvõte

Tootjad nõuavad ranget tooteandmete haldamist, sest versioonihaldus ja tehniliste muudatuste haldus on, et saavutada edu tänapäeval, kus toote töötsüklid pidevalt lühenevad, kvaliteedi- ja töökindlusnõudeid karmistatakse ning tooteohutusele keskendutakse üha enam.

Tehniliste muudatuste haldus loob tooteandmete haldamise ümber struktuuri ja korra ning võimaldab toodete määratlemist, välja andmist ja läbivaatamist kontrollitud viisil, mida töövood toetavad. Toote versioonide ja tehniliste muudatuste haldamise kaudu saate dokumenteerida, hinnata ja rakendada tehnilisi muudatusi toote kogu töötsükli jooksul.

Tehniliste muudatuste haldus aitab teil planeerida ja hallata toote versioonimist ning hallata toote töötsüklit ja tehnilisi muudatusi. Siin on selle pakutavad põhifunktsioonid.

- Toodete versioonimine
- Täiustatud toote väljalaskefunktsioon, mis võimaldab teil säilitada toote koondandmed ühe juriidilise isiku juures (tehnikaettevõttes) ja avaldada teistele juriidilistele isikutele täielikult konfigureeritud välja antud toote
- Selle nõutava teabe kinnitamise reeglid sisestatakse enne toote versiooni aktiveerimist (valmisolekukontrollid)
- Põhjalik kontroll selle üle, millal välja antud toodet saab konkreetses äriprotsessis kasutada, täiustab toote töötsükli haldamist
- Tehniliste muudatuste taotlusi toetavad töövood
- Tehniliste muudatuste tellimusi toetavad töövood

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

See video ([Muudatuste halduse funktsioonid Dynamics 365 Supply Chain Managementis](https://youtu.be/N313FqvRuBc)) on [ esitusloendis Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), mis on saadaval YouTube'is.

## <a name="turn-on-engineering-change-management-for-your-system"></a>Süsteemis tehniliste muudatuste halduse sisselülitamine

Kõigepealt lülitage tehniliste muudatuste haldus sisse järgmiseid juhiseid järgides.

1. Avage [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Otsige värskendusi.
1. Lülitage sisse funktsioon nimega **Tehniliste muudatuste haldus**.

Järgmiseks lülitage sisse **tehniliste muudatuste halduse** konfiguratsioonivõti, järgides neid juhiseid.

1. Pange oma süsteem hooldusrežiimi, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Valige suvandid **Süsteemihaldus \> Häälestus \> Litsentsi konfiguratsioon**.
1. Laiendage sõlme **Kaubandus** ja märkige ruut **Tehniliste muudatuste haldus**.
1. Lülitage hooldusrežiim välja, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
