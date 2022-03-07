---
title: Tehniliste muudatuste halduse ülevaade
description: See teema annab ülevaate tehniliste muudatuste haldusest, mis aitab teil planeerida ja hallata toote versioonimist ning hallata toote töötsüklit ja tehnilisi muudatusi.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 964db71efc9dc81d60199e37de8668de9d667496
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842077"
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

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a>Lülitage oma süsteemi jaoks sisse tehnilise muudatuse halduse ja versiooni dimensiooni funktsioonid

Enne, kui saate kasutada tehnilise muudatuse haldust, peate lubama nii funktsiooni *Tehnilise muudatuse haldus* kui selle konfiguratsioonivõtme. Kui soovite ka jälgida kannetes toodete versiooni dimensiooni (valikuline), peate lisaks lubama funktsiooni *Tooteversiooni dimensioon* ja selle konfiguratsioonivõtme.

Esmalt lülitage sisse funktsioonid, järgides järgmisi etappe.

1. Avage [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
1. Otsige värskendusi.
1. Lülitage sisse funktsioon nimega **Tehniliste muudatuste haldus**.
1. Kui soovite seda kasutada, lülitage sisse ka funktsioon nimega **Tootedimensiooni versioon**.

Seejärel lülitage sisse konfiguratsioonivõtmed, järgides järgmisi etappe.

1. Pange oma süsteem hooldusrežiimi, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Valige suvandid **Süsteemihaldus \> Häälestus \> Litsentsi konfiguratsioon**.
1. Laiendage sõlme **Valdkond**
1. Märkige ruut **Tehniliste muudatuste haldus**.
1. Kui soovite seda kasutada, märkige ka ruut **Tootedimensioon – versioon**.
1. Lülitage hooldusrežiim välja, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
