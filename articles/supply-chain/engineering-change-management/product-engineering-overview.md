---
title: Tehniliste muudatuste halduse ülevaade
description: See teema annab ülevaate tehniliste muudatuste haldusest, mis aitab teil planeerida ja hallata toote versioonimist ning hallata toote töötsüklit ja tehnilisi muudatusi.
author: t-benebo
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 89a3eb584275e52910726ca5a9ed53f744f10b8d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574685"
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

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Lülitage oma süsteemis sisse tehniliste muudatuste haldamise funktsioonid

Enne, kui saate kasutada tehnilise muudatuse haldust, peate lubama nii funktsiooni *Tehnilise muudatuse haldus* kui selle konfiguratsioonivõtme. Kui soovite ka jälgida kannetes toodete versiooni dimensiooni (valikuline), peate lisaks lubama funktsiooni *Tooteversiooni dimensioon* ja selle konfiguratsioonivõtme. Kui need eeltingimused on vastavalt vajadusele seadistatud, saate lülitada sisse täiendavad valikulised funktsioonid tehnika muudatusehalduse jaoks.

### <a name="turn-on-the-basic-engineering-change-management-features"></a>Lülitage oma süsteemis sisse tehniliste muudatuste haldamise funktsioonid

Esmalt lülitage sisse funktsioonid, järgides järgmisi etappe.

1. Avage [Funktsioonihaldus rakenduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruum.
1. Otsige värskendusi.
1. Lülitage sisse funktsioon nimega *Tehniliste muudatuste haldus*.
1. Kui soovite seda kasutada, lülitage sisse ka funktsioon nimega *Tootedimensiooni versioon*.

### <a name="turn-on-the-required-configuration-keys"></a>Lülitage vajalikud konfiguratsioonivõtmed sisse

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

### <a name="turn-on-additional-engineering-change-management-features"></a>Lülitage oma süsteemis sisse tehniliste muudatuste haldamise funktsioonid

Pärast seda, kui lülitate sisse peamised tehnika muudatuste haldamise funktsioonid ja lubate nende konfiguratsioonivõtmed, lisatakse funktsioonihaldusele mitu lisa- ja valikulist tehnika muudatusehalduse funktsiooni. Kõik need funktsioonid on loetletud **tehnika muudatusehalduse** moodulis. Järgmises tabelis kirjeldatakse iga valikulist funktsiooni ja antakse lisateabe jaoks linke.

| Funktsiooni nimi funktsioonihalduses | Kirjeldus |
|---|---|
| Luba olemasolevate toodete muudatuste haldamine | <p>See funktsioon võimaldab teil teisendada olemasolevaid tooteid tehnika toodeteks, nii et saate alustada nende haldamist tehnika muudatusehalduse abil.</p><p>Lisateavet vt [Olemasolevate toodete muudatuste haldamise lubamine](change-management-existing-products.md).</p> |
| Tootmise tehnilised teatised | <p>Kui toode on tehnikas muutunud, võib olla oluline teavitada tootmist nendest muudatustest. Sel viisil saavad tootmistöötajad teha vastavaid tegevusi, nt komponentide asendamine, koosluse asendamine või protsessi asendamine. See funktsioon võimaldab teil teavitada tootmist toodetavate toodete muudatustest.</p><p>Lisateavet vt teemast [Tehniliste toodete muudatuste haldamine](engineering-change-management.md).</p> |
| Paranenud tehnilise muudatuse halduse atribuudi pärimine | <p>See funktsioon lihtsustab lõpetatud kaupade või vahekaupade atribuutide haldust. Kui see funktsioon on sisse lülitatud, on lihtsam tuvastada kõiki üksusele kuuluvaid atribuute ja valida atribuudid, mida tuleks sellelt kaubalt emaüksusele levitada. See funktsioon on kasulik näiteks siis, kui üks valmistoote komponent on habras, mürgine või tuleohtlik, sest saate kergesti tuvastada hapra, mürgise või tuleohtliku atribuudi ja levitate seda valmistoodangule.</p><p>Lisateavet vt jaotisest [Tehnilised atribuudid ja tehnilise atribuudi otsing](engineering-attributes-and-search.md).</p> |
| Toote valmisoleku kontrollid | <p>See funktsioon võimaldab seadistada standardsete toodete (mitteinsenerilistele) toodete valmisolekukontrolli. Kasutage toote valmisoleku kontrolle, et tagada iga toote täielik määratlemine ja kõigi nõutud poliitikate konfigureerimine enne toote kättesaadavaks tegemist ja kannetes kasutamist. Kui keelate selle funktsiooni mõneks ajaks pärast seda, kustutatakse kõik olemasolevad standardtoodete valmisolekukontrollid.</p><p>Lisateavet vt jaotisest [Toote valmisolek](product-readiness.md).</p> |
| Valemite ja nende koostisosade muudatuste haldamine | <p>See funktsioon võimaldab teil jälgida valemi koostisainete, kaastoodete ja kõrvaltoodete muutusi.</p><p>Lisateavet vt jaotisest [Valemite ja nende koostisainete muudatuste haldamine](manage-formula-changes.md).</p> |
| Tehnikatoodetele variantide loomine | <p>See funktsioon võimaldab teil luua saadaolevatel dimensiooniväärtustel põhinevaid tehnikatoodete variante.</p><p>Lisateavet vt teemast [Tehnikatoodete variantide loomine](engineering-variants.md).</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
