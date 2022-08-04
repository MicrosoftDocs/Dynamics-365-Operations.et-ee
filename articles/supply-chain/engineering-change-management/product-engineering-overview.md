---
title: Tehnika muudatusehalduse ülevaade (sisaldab videot)
description: See artikkel annab ülevaate tehnika muudatusehaldusest, mis aitab teil planeerida ja hallata toote versioonimist ning hallata toote töötsükliid ja tehnika muudatusi.
author: t-benebo
ms.date: 01/11/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3a27548fff9728c74814fb92438da1d0c17b5e2b
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067388"
---
# <a name="engineering-change-management-overview"></a>Tehniliste muudatuste halduse ülevaade

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a>Funktsiooni kokkuvõte

Tänased tootjad nõuavad tugevat tooteandmete haldust, versioonijuhtimist ja tehnika muudatusehaldust, et edukas olla toote töötsüklite kahandamises, kvaliteedi ja usaldusväärsuse nõuetele ning keskenduda tooteohutusele.

Tehnika muudatusehaldus viib struktuuri ja distsipliini tooteandmete haldusprotsessi ning võimaldab toodete määratlemist, vabastamist ja üle vaatamist kontrollitud viisil, mida töövood toetavad. Tooteversioonide ja tehnika muudatusehalduse kaudu saate dokumenteerida, hinnata toote tehnikamuudatuste mõju ja rakendada neid läbi kogu toote töötsükli.

Tehniliste muudatuste haldus aitab teil planeerida ja hallata toote versioonimist ning hallata toote töötsüklit ja tehnilisi muudatusi. Siin on selle pakutavad põhifunktsioonid.

- Toodete versioonimine
- Täiustatud toote väljalaskefunktsioon, mis võimaldab teil säilitada toote koondandmed ühe juriidilise isiku juures (tehnikaettevõttes) ja avaldada teistele juriidilistele isikutele täielikult konfigureeritud välja antud toote
- Selle nõutava teabe kinnitamise reeglid sisestatakse enne toote versiooni aktiveerimist (valmisolekukontrollid)
- Põhjalik kontroll selle üle, millal välja antud toodet saab konkreetses äriprotsessis kasutada, täiustab toote töötsükli haldamist
- Tehniliste muudatuste taotlusi toetavad töövood
- Tehniliste muudatuste tellimusi toetavad töövood

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4HE6B]

Eelnev video (change [management capabilitiesies in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) on kaasatud finantsidesse [ja toimingutesse, mis](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) on saadaval YouTube.

## <a name="turn-on-the-engineering-change-management-features-for-your-system"></a>Lülitage oma süsteemis sisse tehniliste muudatuste haldamise funktsioonid

Enne, kui saate kasutada tehnilise muudatuse haldust, peate lubama nii funktsiooni *Tehnilise muudatuse haldus* kui selle konfiguratsioonivõtme. Kui soovite ka jälgida kannetes toodete versiooni dimensiooni (valikuline), peate lisaks lubama funktsiooni *Tooteversiooni dimensioon* ja selle konfiguratsioonivõtme. Kui need eeltingimused on vastavalt vajadusele seadistatud, saate lülitada sisse täiendavad valikulised funktsioonid tehnika muudatusehalduse jaoks.

### <a name="turn-the-basic-engineering-change-management-features-on-or-off"></a>Lülitage tehnika põhi muudatusehalduse funktsioonid sisse ja välja

Järgige neid samme, et lülitada peamised tehnika muutmise haldamise funktsioonid sisse ja välja. Tarneahela halduse versiooni 10.0.25 *puhul* on tehnika muutmise haldamise funktsioon vaikimisi sisse lülitatud.

1. Avage [Funktsioonihaldus rakenduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruum.
1. Otsige värskendusi.
1. Lülitage funktsioon nimega *Engineering Change Management vastavalt* vajadusele sisse ja välja.
1. Kui soovite jälgida kannetes toodete versioonidimensiooni (valikuline), lülitage sisse funktsioon nimega Tootedimensiooni *versioon*.

### <a name="turn-the-required-configuration-keys-on-or-off"></a>Lülitage nõutud konfiguratsioonivõtmed sisse ja välja

Seejärel lülitage sisse konfiguratsioonivõtmed, järgides järgmisi etappe. Vaikimisi ei ole need sisse lülitatud.

1. Pange oma süsteem hooldusrežiimi, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Valige suvandid **Süsteemihaldus \> Häälestus \> Litsentsi konfiguratsioon**.
1. Laiendage **Äritegevuse** sõlmpunkti.
1. Lubage või keelake põhifunktsiooni konfiguratsioonivõti, kasutades märkeruutu **Tehnika muudatusehaldus**.
1. Laiendage **tehnika muutmise halduse** sõlme ja märkige või tühjendage järgmised märkeruudud vastavalt vajadusele (sõltuvalt funktsioonidest, mida soovite kasutada):

    - **Atribuudi otsing** – märkige see ruut, et lubada [atribuud otsingufunktsioon](engineering-attributes-and-search.md). Soovitame selle funktsiooni lubada, kuid kui te seda ei kasuta, võite märkeruudu tühjendada.
    - **Protsessi tootmise muudatuste haldamine** – märkige see ruut, kui soovite kasutada tehnika muudatusehalduse funktsioone protsessi tootmise valemite muudatuste haldamiseks. Kui te ei pea valemeid haldama, saate märkeruudu tühjendada. Lisateavet vt jaotisest [Valemite ja nende koostisainete muudatuste haldamine](manage-formula-changes.md).

1. Kui soovite kasutada ka versiooni dimensiooni, märkige ruut **Tootedimensioon – versioon**. (See ruut on loendi all, mitte pesastatud loendi alla **Tehnika muutmise** halduse sõlm.) Selle ruudu saate tühjendada, kui te seda funktsiooni ei vaja.
1. Lülitage hooldusrežiim välja, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Muudatuste kajastamiseks peab andmebaas olema sünkroonitud, et tagada konfiguratsioonivõtmete õige uuendamine. Sõltuvalt kasutatava keskkonna tüübist tehke ühte järgmistest sammudest:
    - **Järgu 1 (arendus) keskkondades: avage Microsoftis** oma projekt ja valige suvand Visual Studio Dynamics 365 Sünkrooni **andmebaas \> Sünkrooni \>.**
    - **Järgu 2 (ja kõrgema taseme)** keskkondades: andmebaas sünkroonib automaatselt pärast seda, kui panete keskkonna hooldusrežiimile ja sealt välja, seega võite selle sammu vahele jätta.

### <a name="turn-on-additional-engineering-change-management-features"></a>Lülitage oma süsteemis sisse tehniliste muudatuste haldamise funktsioonid

Pärast seda, kui lülitate sisse peamised tehnika muudatuste haldamise funktsioonid ja lubate nende konfiguratsioonivõtmed, lisatakse funktsioonihaldusele mitu lisa- ja valikulist tehnika muudatusehalduse funktsiooni. Kõik need funktsioonid on loetletud **tehnika muudatusehalduse** moodulis. Järgmises tabelis kirjeldatakse iga valikulist funktsiooni ja antakse lisateabe jaoks linke. Vastavalt tarneahela halduse versioonile 10.0.25 on kõik need funktsioonid vaikimisi sisse lülitatud, kuid saate need siiski välja lülitada.

| Funktsiooni nimi funktsioonihalduses | Kirjeldus | Funktsiooni olek |
|---|---|---|
| Luba olemasolevate toodete muudatuste haldamine | <p>See funktsioon võimaldab teil teisendada olemasolevaid tooteid tehnika toodeteks, nii et saate alustada nende haldamist tehnika muudatusehalduse abil.</p><p>Lisateavet vt [Olemasolevate toodete muudatuste haldamise lubamine](change-management-existing-products.md).</p> |
| Tootmise tehnilised teatised | <p>Kui toode on tehnikas muutunud, võib olla oluline teavitada tootmist nendest muudatustest. Sel viisil saavad tootmistöötajad teha vastavaid tegevusi, nt komponentide asendamine, koosluse asendamine või protsessi asendamine. See funktsioon võimaldab teil teavitada tootmist toodetavate toodete muudatustest.</p><p>Lisateavet vt teemast [Tehniliste toodete muudatuste haldamine](engineering-change-management.md).</p> |
| Paranenud tehnilise muudatuse halduse atribuudi pärimine | <p>See funktsioon lihtsustab lõpetatud kaupade või vahekaupade atribuutide haldust. Kui see funktsioon on sisse lülitatud, on lihtsam tuvastada kõiki üksusele kuuluvaid atribuute ja valida atribuudid, mida tuleks sellelt kaubalt emaüksusele levitada. See funktsioon on kasulik näiteks siis, kui üks valmistoote komponent on habras, mürgine või tuleohtlik, sest saate kergesti tuvastada hapra, mürgise või tuleohtliku atribuudi ja levitate seda valmistoodangule.</p><p>Lisateavet vt jaotisest [Tehnilised atribuudid ja tehnilise atribuudi otsing](engineering-attributes-and-search.md).</p> |
| Toote valmisoleku kontrollid | <p>See funktsioon võimaldab seadistada standardsete toodete (mitteinsenerilistele) toodete valmisolekukontrolli. Kasutage toote valmisoleku kontrolle, et tagada iga toote täielik määratlemine ja kõigi nõutud poliitikate konfigureerimine enne toote kättesaadavaks tegemist ja kannetes kasutamist. Kui keelate selle funktsiooni mõneks ajaks pärast seda, kustutatakse kõik olemasolevad standardtoodete valmisolekukontrollid.</p><p>Lisateavet vt jaotisest [Toote valmisolek](product-readiness.md).</p> |
| Valemite ja nende koostisosade muudatuste haldamine | <p>See funktsioon võimaldab teil jälgida valemi koostisainete, kaastoodete ja kõrvaltoodete muutusi.</p><p>Lisateavet vt jaotisest [Valemite ja nende koostisainete muudatuste haldamine](manage-formula-changes.md).</p> |
| Tehnikatoodetele variantide loomine | <p>See funktsioon võimaldab teil luua saadaolevatel dimensiooniväärtustel põhinevaid tehnikatoodete variante.</p><p>Lisateavet vt teemast [Tehnikatoodete variantide loomine](engineering-variants.md).</p> |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

