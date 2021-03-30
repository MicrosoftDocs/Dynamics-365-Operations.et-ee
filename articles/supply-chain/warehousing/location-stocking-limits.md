---
title: Asukoha ladustamispiirangud
description: See teema kirjeldab asukoha ladustamispiirangute funktsioone.
author: perlynne
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: e336b54b894669f8a49091473314e1d7d2639e5f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216977"
---
# <a name="location-stocking-limits"></a>Asukoha ladustamispiirangud

[!include [banner](../includes/banner.md)]

Saate kasutada lehte **Asukoha ladustamispiirangud** (**Laohaldus \> Häälestus \> Ladu \> Asukoha ladustamispiirangud**), et kontrollida koorma mahtu ladudes ilma füüsiliste toodete mahu arvutamiseks täpsemaid protsesse kasutamata.

Asukoha ladustamispiirangute eesmärk on hinnata maksimaalset kogust, mis asukohas saab olla. Saate häälestada funktsiooni kolmel tasemel, millest igaühel on oma vahekaart lehel **Asukoha ladustamispiirangud**.

- Tooted
- Tootevariandid
- Konteineritüübid

Iga taseme jaoks saate määratleda erinevad väljaväärtused. Seejärel hindab süsteem kindla asukoha võimekust, võttes aluseks väärtuse **Kogus** ja **Ühik**, mis on igal real. See valib esmalt kõige üksikasjalikuma vastega kirje. Näiteks rida, millel on väärtus **Asukohaprofiili ID** hinnatakse enne rida, millel on väärtus ainult väljal **Ladu**. Ülejäänud võimekust hinnatakse ka, võttes aluseks kasutatava asukoha ladustamispiirangu kirje väärtuse **Kogus**.

Lehe jaotises **Tooted** saate asukoha ladustamispiirangute otsimiseks määratleda järgmised väljaväärtused.

- Ladu
- Asukoha profiili ID
- Koht
- Pakendi suuruse kategooria ID
- Kaubakood
- Ühik

> [!NOTE]
> Te ei pea iga asukoha ladustamispiirangu kirje jaoks määrama väärtust **Ühik**. Asukoha võimekuse arvutused põhinevad laoühikute kogusel. Kui kasutatava väärtuse jaoks ei ole ühiku teisendust määratletud, jäetakse asukoha ladustamispiirangu kirje vahele, nagu oleks selle jaoks määratud mõni muu väärtus **Kaubakood**.

## <a name="example--purchase-order-receiving"></a>Näide – ostutellimuse vastuvõtmine

See näide põhineb puhastel *USMF*-i demoandmetel, kus on häälestatud järgmised väärtused lehe **Asukoha ladustamispiirangud** vahekaardil **Tootevariandid**.

| Ladu | Asukoha profiili ID | Kaubakood | Maht | Kogus | Ühik |
|-----------|---------------------|-------------|------|----------|------|
| 24        | PÕRAND               | D0013       | E    | 300      | Ea   |
| 24        | PÕRAND               | D0013       | L    | 240      | Ea   |
| 24        | PÕRAND               | D0013       | L    | 360      | Ea   |

Toodete jaoks on häälestatud erinevate mõõtühikutega tootevariandid. Need variandid on sobitatud kolme kaubaaluse (PL-i ) asukoha ladustamispiirangutega.

- **Suurus M:** 1 PL = 100 tk (Ea)
- **Suurus L:** 1 PL = 80 Ea
- **Suurus S:** 1 PL = 120 Ea

Seetõttu mahutab iga asukoht, kus **Asukohaprofiili ID** väärtuseks on määratud *PÕRAND*, *3* *PL*-i kaubanumbriga *D0013*.

### <a name="prepare-for-the-example"></a>Ettevalmistav näide

Selles näites esitate ostutellimuse, kus on kaks vastuvõtuvooga rida. Kuid peate esmalt uuendama demoandmeid järgmisel viisil, et tagada asukohtades segatud kaupade veo lubamine, ainult tühjade asukohtade kasutamine vahemikus *FL-002* kuni *FL-004* ja see, et avatud sissetulevat tööd pole.

1. Asukohal *FL-001* muutke välja **Asukohaprofiil** väärtus *KORRUS* väärtuseks *KORRUS-05*.
1. Asukohaprofiili *FLOOR* korral määrake suvandi **Luba segakaubad** väärtuseks *Jah*.
1. Looge järgmise kahe reaga ostutellimus.

    | Ladu | Kaubakood | Maht | Kogus | Ühik |
    |-----------|-------------|------|----------|------|
    | 24        | D0013       | L    | 4        | PL   |
    | 24        | D0013       | L    | 4        | PL   |

### <a name="process-the-example"></a>Näite töötlemine

Kõigepealt saate üksuse *PL* suurusega *S* koguses *4* ja saate kontrollida loodava töö asetusridade asukohti. Seejärel saate üksuse *PL* suurusega *L* koguses *4* ja saate kontrollida loodava töö asetusridade asukohti.

1. Logige sisse laorakendusse, kasutades kasutaja ID-na nr *24* ja paroolina nr *1*.
1. Valige **Sissetulev** \> **Vastuvõetud ost**.
1. Saate *4* *PL*-i kaubakoodiga *D0013* ja suurusega *S*.
1. Vaadake üle loodud ladustamistöö. Teile peaks olema kuvatud järgmine tulemus.

    - 3 PL -\> FL-002
    - 1 PL -\> FL-003

1. Saate *4* *PL*-i kaubakoodiga *D0013* ja suurusega *L*.
1. Vaadake üle loodud ladustamistöö. Teile peaks olema kuvatud järgmine tulemus.

    - 1 PL -\> FL-003
    - 3 PL -\> FL-004

Tulemuste põhjal saate järeldada, et süsteem ei suutnud eraldada õigeid ladustamistöö asukohti. Miks süsteem muidu viimases erapis lisas ainult *1* *PL*-i suuruses *L* asukohale *FL-003* ja mitte *2* *PL*-i? Ehk miks pole sellel asukohal kokku *3* *PL*-i ladustamistööd?

Selle ilmse nurjumise selgitamiseks peate mõistma asukoha ladustamispiirangute valikukriteeriume. Süsteem valib esmalt kõige üksikasjalikuma vastega kirje. Selles näites on kõige üksikasjalikuma vastega kirje rida, kus väärtus **Suurus** on *L*, väärtus **Kogus** on *240* ja väärtus **Üksus** on *Ea*. Kuna teil on juba avatud eelmine sissetulev töö, kus kogus on *120* *Ea* suurusega *S*, siis arvutatakse ülejäänud võimekus nii: *240* – *120* = *120* *Ea*. Seetõttu saab veel mahutada ainult *1* *PL*-i (*80* *Ea*).

> [!NOTE]
> Te ei saa kasutada asukoha ladustamispiiranguid, et juhtida näiteks nende kaubavarude täiendamist, mida on samas asukohas erinevas koguses. Sel juhul kasutage *täiendamise malli*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]