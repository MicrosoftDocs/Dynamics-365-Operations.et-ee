---
title: Proovibilansi finantsaruanded
description: See artikkel kirjeldab proovibilansi vaikearuandeid. See kirjeldab ka nende aruannetega seotud alustalasid ja kuidas saate muuta aruandeid, et sobituda teie ärivajadustega.
author: jinniew
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: kfend
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b26d2ec261720499fc309a5fb850de2cb796bd8b
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802603"
---
# <a name="trial-balance-financial-reports"></a>Proovibilansi finantsaruanded

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab proovibilansi vaikearuandeid. See kirjeldab ka nende aruannetega seotud alustalasid ja kuidas saate muuta aruandeid, et sobituda teie ärivajadustega. 

## <a name="default-trial-balance-reports"></a>Proovibilansi vaikearuanded

Finantsaruandluses on saadaval kolm proovibilansi aruannet.

| Vaikearuanne                                 | Selle funktsioon                                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------|
| Üksikasjalik proovibilanss – vaikimisi               | Pakub saldoteavet kõigi kontode puhul, hõlmates deebet- ja kreeditsaldosid ja nende saldode netoväärtust koos kande kuupäeva, kande ja töölehe kirjeldusega.                  |
| Proovibilansi kokkuvõte – vaikimisi                | Pakub saldoteavet kõigi kontode puhul, hõlmates avamis- ja sulgemissaldosid ning deebet- ja kreeditsaldosid koos nende netoerinevusega.                                        |
| Proovibilansi kokkuvõte aasta-aastalt – vaikimisi | Pakub saldoteavet kõigi kontode puhul, hõlmates avamis- ja sulgemissaldosid ning deebet- ja kreeditsaldosid koos nende netoerinevusega praeguse aasta ja möödunud aasta kohta. |

## <a name="building-blocks"></a>Koosteüksused
Proovibilansi finantsaruanded kasutavad järgmisi koosteüksusi.

| Vaikearuanne                                 | Rea definitsioon          | Veeru määratlus                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| Üksikasjalik proovibilanss – vaikimisi               | Proovibilanss – vaikimisi | Üksikasjalik proovibilanss – vaikimisi               |
| Proovibilansi kokkuvõte – vaikimisi                | Proovibilanss – vaikimisi | Proovibilansi kokkuvõte – vaikimisi                |
| Proovibilansi kokkuvõte aasta-aastalt – vaikimisi | Proovibilanss – vaikimisi | Proovibilansi kokkuvõte aasta-aastalt – vaikimisi |

> [!NOTE] 
> **Proovibilansi** finantsaruandluses koostades märkige kindlasti **Kuva summadeta read** ja **Kuva aktiivsete ridadeta** read **Sätted** vahekaardil.

### <a name="row-definition"></a>Rea definitsioon

Rea määratlus Proovibilanss – vaikimisi sisaldab ühte rida, mis koondab kõiki põhikontosid. Seega saab igaüks luua aruande ilma muudatusi tegemata. Aruande vaatamisel saate iga konto üksikasjade kuvamiseks minna ühes reas süvitsi. Saate muuta readefinitsiooni nii, et see hõlmaks rohkem üksikasju. Suvandi Proovibilanss – vaikimisi readefinitsiooni muutmiseks nii, et see hõlmaks kõikide kontode ridu, toimige järgmiselt.

1.  Klõpsake **nuppu** Redigeeri ja seejärel käsku **Lisa dimensioonidest read**. Käsuga **Lisa dimensioonide** read saate valida readefinitsioonis soovitud dimensioonid. Selle readefinitsiooni puhul kasutatakse **põhikontot**.
2.  Veenduge, et **põhikonto sisaldab** kõiki ampersands (&) ja seejärel klõpsake **OK**.

Readefinitsioon sisaldab nüüd kõiki teie vaikimisi juriidilise isiku põhikontosid.

### <a name="column-definition"></a>Veeru määratlus

Iga proovibilansi aruanne kasutab erinevat veeru definitsiooni. Need veeru definitsioonid sisaldavad eri tüüpi veerge üksikasjade ja finantsandmete eri tasemete pakkumiseks.

-   **Üksikasjalik proovibilanss – vaikimisi veerutüübid:**
    -   **DESC** – kirjeldus readefinitsioonist
    -   **ACCT** – kontokoodid
    -   **ATTR (3)** – atribuudid:
        -   Kande kuupäev
        -   Kanne
        -   Töölehe kirjeldus
    -   **FD** – finantsandmed, mis sisaldavad ainult deebeteid
    -   **FD** – finantsandmed, mis sisaldavad ainult kreediteid
    -   **CALC** – netoerinevus
-   **Proovibilansi kokkuvõte – vaikimisi veerutüübid:**
    -   **ACCT** – kontokoodid
    -   **DESC** – kirjeldus readefinitsioonist
    -   **ATTR** – atribuut:
        -   Kanne
    -   **FD** – algsaldo finantsandmed
    -   **FD** – finantsandmed, mis sisaldavad ainult deebeteid
    -   **FD** – finantsandmed, mis sisaldavad ainult kreediteid
    -   **CALC** – netoerinevus
    -   **CALC** – sulgemissaldo
-   **Proovibilansi kokkuvõte aasta-aastalt – vaikimisi:**
    -   **ACCT** – kontokoodid
    -   **DESC** – kirjeldus readefinitsioonist
    -   **ATTR** – atribuut
        -   Kanne
    -   **FD** – algsaldo finantsandmed praeguse aasta puhul
    -   **FD** – finantsandmed, mis sisaldavad ainult jooksva aasta deebeteid
    -   **FD** – finantsandmed, mis sisaldavad ainult jooksva aasta kreediteid
    -   **CALC** – netoerinevus
    -   **CALC** – sulgemissaldo
    -   **FD** – finantsandmed, mis sisaldavad ainult möödunud aasta deebeteid
    -   **FD** – finantsandmed, mis sisaldavad ainult möödunud aasta kreediteid

## <a name="additional-resources"></a>Lisaressursid

[Finantsaruandluse ülevaade](financial-reporting-getting-started.md)

[Finantsaruannete vaatamine](view-financial-reports.md)

[Dynamicsi finantsaruandluse ajaveeb](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
