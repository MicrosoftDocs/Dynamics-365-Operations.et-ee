---
title: Toote konfiguratsioonimudeli arvutamise
description: See teema kirjeldab, kuidas luua rakenduse toote konfiguratsioonimudelile atribuutide kalkulatsioone
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829614"
---
# <a name="product-configuration-model-calculations"></a>Toote konfiguratsioonimudeli arvutamise

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas luua rakenduse toote konfiguratsioonimudelile atribuutide kalkulatsioone.

## <a name="prerequisites"></a>Eeltingimused

Arvutusi kasutatakse toote konfiguratsioonimudelis toote konfiguratsiooniväärtuste arvutamiseks. Enne arvutuste määratlemist peab olemas olema seotud toote konfiguratsioonimudel. Konfiguratsioonimudelite ja seotud ülesannete seadistusprotsessist ülevaate saamiseks vt [Toote konfiguratsioonimudeli seadistamine](set-up-maintain-product-configuration-model.md).

## <a name="create-a-calculation"></a>Kalkulatsiooni loomine

Arvutus koosneb avaldisest ja sihtatribuudist. Lisateavet vt teemast [Toote konfiguratsioonimudeli kalkulatsioonide KKK](calculate-product-configuration-models.md).

Olemasoleva tootemudeli arvutuse loomiseks järgige järgmisi samme.

1. Minge asukohta **Tooteteabe haldus \> Üldine \> Toote konfiguratsioonimudelid**.
1. Avage toote konfiguratsioonimudel ja seejärel valige suvand **Redigeeri**.
1. Valige kiirkaardil **Kalkulatsioonid** suvand **Lisa**, et lisada kalkulatsioon, ja seejärel määrake järgmised väljad:

    - **Nimi** – sisestage kalkulatsiooni nimi.
    - **Kirjeldus** – sisestage kalkulatsiooni kirjeldus.
    - **Sihtatribuut** – valige atribuut, millele kalkulatsiooni teete.

1. Valige **Redigeeri avaldis**.
1. Lisage dialoogiboksi **Sisesta kalkulatsioon** nõutavad atribuudid, tehtemärgid ja väärtused. Lisateavet elementidega töötamise kohta vaadake jaotisest [Avaldiste piirangud ja tabelipiirangud tootekonfiguratsioonimudelites](expression-constraints-table-constraints-product-configuration-models.md).
1. Kui avaldis on valmis, valige **OK**.

## <a name="calculation-examples"></a>Arvutusnäited

Selles jaotises kuvatakse mõned näited kalkulatsioonide töötamise kohta.

### <a name="example-1"></a>Näide 1

Sihtatribuut on kahendmuutuja tüüpi ja arvutus kasutab järgmist tingimuslikku-avaldist:

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

Avaldis tagastab sihtatribuudile väärtuse *Tõene*, kui `decimalAttribute2` on suurem kui `decimalAttribute1` või sellega võrdne. Muidu tagastab see kahendväärtuse *Väär*.

### <a name="example-2"></a>Näide 2

Selles näites kasutatakse `textFixedList` sihtatribuudina tekstiatribuudi. See atribuut sisaldab järgmist fikseeritud loendit.

| Väärtus | Lahendaja väärtus |
|---|---|
| A | 1a |
| B | 2b |
| C | 2c |

Järgmine kuvatõmmis näitab, kuidas selle atribuudi sätted teie süsteemis võidakse kuvada.

![Atribuudi tüübi sätted, näiteks 2](media/model-calculations-example2.png "Atribuudi tüübi sätted, näiteks 2")

Atribuuti kasutatakse järgmises tingimuslikus lauses:

`If[integerAttribute < 150, 0, 2]`

Kui `integerAttribute` väärtus on väiksem kui 150, tagastab see lause fikseeritud loendi *A* esimese kirje tekstiväärtuse. Vastasel juhul tagastab see fikseeritud loendis *C* kolmanda kirje tekstiväärtuse.

> [!NOTE]
> Fikseeritud loend on samaväärne null-põhise loeteluga (enum) ja selle väärtustele pääseb juurde sobiva täisarvu väärtusega. Seetõttu vastendatakse esimene fikseeritud loendi väärtus (*A*) väärtuseks *0*, teine väärtus (*B*) *1*-ga ja kolmas väärtus (*C*) vastendatakse *2*-ga.

### <a name="example-3"></a>Näide 3

Selles näites kasutatakse `textFixedList` sihtatribuuti eelmisest näitest. See kasutab ka teist tekstiatribuudi `textAttribute`, mis sisaldab järgmist fikseeritud loendit.

| Väärtus | Lahendaja väärtus |
|---|---|
| AA | 1aa |
| BB | 2bb |

Järgmine kuvatõmmis näitab, kuidas selle atribuudi sätted teie süsteemis võidakse kuvada.

![Atribuudi tüübi sätted, näiteks 3](media/model-calculations-example3.png "Atribuudi tüübi sätted, näiteks 3")

Atribuudi `textFixedList` väärtus arvutatakse järgmise tingimusliku lause abil:

`If[textAttribute == "1aa", 0, 2]`

Kui `textAttribute` väärtusel on lahendusväärtus, mis võrdub *1aa*, tagastab see avaldis fikseeritud loendi `textFixedList` *A* esimese kirje tekstiväärtuse. Vastasel juhul tagastab see fikseeritud loendis `textFixedList` *C* kolmanda kirje tekstiväärtuse.

> [!NOTE]
> - Tingimuslik lause peab kasutama atribuudi lahendaja väärtust.
> - Arvutustes saab kasutada ainult fikseeritud loendiga tekstiatribuute.

## <a name="see-also"></a>Vt ka

- [Toote konfiguratsioonimudelite arvutuste KKK](calculate-product-configuration-models.md)
- [Avaldise piirangu lisamine toote konfiguratsioonimudelile](tasks/add-expression-constraint-product-configuration-model.md)
- [Toote konfiguratsioonimudelite ülevaade](product-configuration-models.md)
