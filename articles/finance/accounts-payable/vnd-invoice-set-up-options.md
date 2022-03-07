---
title: Hankija arve automatiseerimise seadistussuvandid (eelversioon)
description: Selles teemas kirjeldatakse suvandeid, mis on saadaval hankija arve automatiseerimise seadistamiseks ja konfigureerimiseks.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 32da8dc569f4eabfe3d7ddbfac55e827f469d871
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837197"
---
# <a name="setup-options-for-vendor-invoice-automation"></a>Hankija arve automatiseerimise seadistussuvandid

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse suvandeid, mis on saadaval hankija arve automatiseerimise seadistamiseks ja konfigureerimiseks. Arvete automatiseerimise funktsioonid kasutavad järgmist tüüpi seadistusparameetreid.

- Parameetrid imporditud hankija arvete edastamiseks töövoosüsteemile ja sisestatud toote sissetuleku ridade vastavusse viimiseks ootel hankija arve ridadega.
- Parameetrid automatiseerimise taustaülesannete töötlemiseks. Protsessi automatiseerimise raamistikku kasutatakse imporditud hankija arvete edastamiseks töövoosüsteemile. Seda kasutatakse ka automaatselt sisestatud toote sissetulekuridade vastendamiseks ootel hankija arve ridadega ja arve vastendamise valideerimiseks käsitsi arvete korral, mis on automaatselt toote sissetulekuridadega vastendatud. Erinevad äriprotsessid kasutavad seda raamistikku määramiseks, kui tihti valitud protsessi käitatakse. Saadaolevad sagedused taustaprotsesside **Toote sissetuleku vastavusseviimine arve ridadega** ja **Hankija arvete edastamine töövoole** puhul on **Iga tund** ja **Iga päev**.

Taustaülesande seadistamiseks või selle kohta teabe vaatamiseks avage **Süsteemihaldus \> Seadistus \> Protsessi automatiseerimine** ja valige vahekaart **Taustaülesanne**.

Et töö oleks täiesti automaatne alates impordiprotsessist kuni hankija arve sisestamiseni, peate seadistama hankija arve töövoo. Töövoo seadistamiseks avage **Ostureskontro > Seadistus > Ostureskontro töövood**. Tagamaks, et arvet saaks töödelda algusest lõpuni automaatselt, peate oma töövookonfiguratsiooni kaasama automatiseeritud sisestamisülesande.

## <a name="parameters-for-submitting-imported-vendor-invoices-to-the-workflow-system"></a>Parameetrid imporditud hankija arvete edastamiseks töövoosüsteemile

Imporditud hankija arvete edastamiseks töövoosüsteemile kasutatakse kindlaid parameetreid. Lisaks kasutatakse mõnd parameetrit ka sisestatud toote sissetuleku ridade vastavusseviimiseks ootel hankija arve ridadega. Lehe **Ostureskontro parameetrid** vahekaardil **Hankija arve automatiseerimine** on parameetrid, mis tuleb seadistada, jagatud järgmiste jaotiste vahel.

- Hankija arvete töövoog
- Toote sissetulekute automaatne vastendamine

Saadaval on järgmised parameetrid.

- **Imporditud arvete automaatne edastamine töövoogu** – kui seate selle suvandi väärtuseks **Jah**, edastatakse imporditud arved automaatselt töövoosüsteemi. Kui selle suvandi väärtuseks on seatud **Ei**, tuleb arved käsitsi edastada. Kui määrate selle suvandi väärtuseks **Jah**, lubate täisautomaatse protsessi importimise tulemustest kuni sisestamiseni.

    Selle suvandi väärtuseks saate seada **Jah** ainult juhul, kui teie juriidilise isiku jaoks on seadistatud aktiivne hankija arve töövoog. Töövoo seadistamiseks avage **Ostureskontro \> Seadistus \> Ostureskontro töövoog**.

- **Toote sissetulekute vastavusseviimine arve ridadega enne automaatset edastamist** – kui seate selle suvandi väärtuseks **Jah**, ei saa imporditud arvet automaatselt töövoosüsteemile edastada enne, kui vastavusse viidud toote sissetuleku kogus võrdub arve kogusega. Kui määrate selle suvandi väärtuseks **Jah**, lubate sisestatud toote sissetulekute automaatse vastavusseviimise arve ridadega, mille jaoks on määratletud kolmesuunaline vastavusse viimise poliitika. See protsess töötab seni, kuni vastavusse viidud toote sissetuleku kogus võrdub arve kogusega. Seejärel edastatakse arve automaatselt töövoosüsteemile.

    Suvand „Toote sissetulekute vastavusseviimine arve ridadega enne automaatset edastamist” on saadaval ainult siis, kui valitud on suvand **Luba arvete vastavusseviimise kontrollimine**. Kui see suvand on valitud, valitakse automaatselt suvand **Vii toote sissetulekud automaatselt arve ridadega vastavusse**.

- **Nõua, et arvutatud kogusummad võrduksid automaatse töövoole edastamise puhul imporditud kogusummadega** – kui seate selle suvandi väärtuseks **Jah**, ei saa arvet automaatselt töövoosüsteemile edastada enne, kui arve jaoks arvutatud kogusummad võrduvad imporditud kogusummadega. Kui selle suvandi väärtuseks on seatud **Ei**, saab arvet automaatselt edastada töövoosüsteemi, kuid seda ei saa sisestada enne, kui arvutatud kogusummasid parandatakse nii, et need ühtiksid imporditud kogusummadega. Kui te ei impordi arve summat või käibemaksu summat, peaks selle suvandi väärtuseks olema seatud **Ei**.
- **Vii toote sissetulekud automaatselt arve ridadega vastavusse** – kui seate selle suvandi väärtuseks **Jah**, saab taustatöötlust kasutada sisestatud toote sissetulekute automaatseks vastavusse viimiseks arve ridadega, mille jaoks on määratletud kolmesuunaline vastavusse viimise poliitika. See protsess töötab seni, kuni vastavusse viidava toote sissetuleku kogus võrdub arve kogusega või kuni saavutatakse välja **Automaatse vastavusseviimise katsete arv** väärtus. Protsessi saab käivitada seni, kuni arve on edastatud töövoosüsteemile.

    See suvand on saadaval ainult juhul, kui on tehtud valik **Luba arvete vastavusseviimise kontrollimine**.

    Kui seate suvandi **Toote sissetulekute vastavusseviimine arve ridadega enne automaatset edastamist** väärtuseks **Jah**, ei saa selle suvandi väärtus olla **Ei**. Et seada selle suvandi väärtuseks **Ei**, peate esmalt seadma suvandi **Toote sissetulekute vastavusseviimine arve ridadega enne automaatset edastamist** väärtuseks **Ei**.

- **Automaatse vastavusseviimise katsete arv** – valige mitu korda peaks süsteem maksimaalset üritama viia toote sissetulekuid vastavusse arve ridadega, enne kui see jõuab järeldusele, et protsess nurjus. Kui määratud katsete arv on saavutatud, eemaldatakse arve automatiseeritud töötlemisest.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]