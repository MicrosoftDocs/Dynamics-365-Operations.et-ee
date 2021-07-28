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
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 70567489e5a1b84677ee63c296d15f5bdeb728ca
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6338603"
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

1. Avage [Funktsioonihaldus rakenduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruum.
1. Otsige värskendusi.
1. Lülitage sisse funktsioon nimega *Tehniliste muudatuste haldus*.
1. Kui soovite seda kasutada, lülitage sisse ka funktsioon nimega *Tootedimensiooni versioon*.

Seejärel lülitage sisse konfiguratsioonivõtmed, järgides järgmisi etappe.

1. Pange oma süsteem hooldusrežiimi, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Valige suvandid **Süsteemihaldus \> Häälestus \> Litsentsi konfiguratsioon**.
1. Laiendage **Äritegevuse** sõlmpunkti.
1. Lubage põhifunktsiooni konfiguratsioonivõti, valides märkeruudu **Tehniliste muudatuste haldus**.
1. Laiendage **tehnika muutmise halduse** sõlme ja märkige või tühjendage järgmised märkeruudud vastavalt vajadusele (sõltuvalt funktsioonidest, mida soovite kasutada):

    - **Atribuudi otsing** – märkige see ruut, et lubada [atribuud otsingufunktsioon](engineering-attributes-and-search.md). Soovitame selle funktsiooni lubada, kuid kui te seda ei kasuta, võite märkeruudu tühjendada.
    - **Protsessi tootmise muudatuste haldamine** – märkige see ruut, kui soovite kasutada tehnika muudatusehalduse funktsioone protsessi tootmise valemite muudatuste haldamiseks. Kui te ei pea valemeid haldama, saate märkeruudu tühjendada. Lisateavet vt jaotisest [Valemite ja nende koostisainete muudatuste haldamine](manage-formula-changes.md).

1. Kui soovite kasutada ka versiooni dimensiooni, märkige ruut **Tootedimensioon – versioon**. (See märkeruut asub loendis allpool, mitte pesastatud **Tehniliste muudatuste halduse** sõlmpunkti alla.)
1. Lülitage hooldusrežiim välja, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

> [!IMPORTANT]
> Alates 2022. aasta aprillist lubatakse kõigi uute installide puhul vaikimisi nii **Tehniliste muudatuste haldus** kui ka **Toote dimensioon – versioon** litsentsivõtmed, kuid vajadusel saate need siiski keelata.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
