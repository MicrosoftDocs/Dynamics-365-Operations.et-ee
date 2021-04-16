---
title: Krediidilimiidi korrektsioonid
description: Selles teemas kirjeldatakse krediidilimiidi korrigeerimiste seadistamist ja lisamist.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: b1669029f28cef924170b47340567af49525e1b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835360"
---
# <a name="credit-limit-adjustments"></a>Krediidilimiidi korrektsioonid 

[!include [banner](../includes/banner.md)]

Krediidilimiidi korrigeerimised lasevad krediidihalduritel värskendada ühe kliendi, kliendigrupi või kõigi klientide krediidilimiite ja aegumiskuupäevi. Saate lisada krediidilimiiti korrigeerimise kandeid klientide ja kliendi krediidigruppide värskendamiseks või kasutada neid automaatsete krediidilimiitide arvutamiseks. Seejärel saab kanded üle vaadata, saata läbi töövoo kinnitamiseks ja sisestada kliendi kontodele.

## <a name="set-up-credit-limit-adjustments"></a>Krediidilimiidi korrigeerimiste seadistamine

Saate luua krediidilimiidi korrigeerimise töölehele kandeid lehel **Krediidilimiidi korrigeerimine** (**Krediidihaldus \> Krediidilimiidi korrigeerimine \> Krediidilimiidi korrigeerimine**).

1. Valige suvand **Uus**. Luuakse uus kirjete grupp, millel on krediidilimiidi korrigeerimise number.
2. Krediidilimiidi korrigeerimise tüübi valik.

    - Kliendi krediidilimiidi muutmiseks valige **Krediidilimiit**.
    - ajutise krediidilimiidi loomiseks kliendi praeguse krediidilimiidi muutmise asemel valige **Ajutine krediidilimiit**. Ajutised krediidilimiidid alistavad kliendi krediidilimiidi määratud perioodil. Pärast selle perioodi lõppu kasutatakse kliendi krediidilimiiti uuesti.
3. Sisestage kirjeldus. 

Kui märkeruut **Sisestatud** on valitud on krediidilimiidid rakendatud. Väli **Kinnitamise olek** näitab töölehe töövoo olekut. Töövoog on valikuline.

### <a name="add-credit-limit-adjustments"></a>Krediidilimiidi korrigeerimiste lisamine

Krediidilimiidi korrigeerimiste käsitsi lisamiseks valige **Read** ja seejärel järgige neid samme.

1. Kliendi jaoks krediidilimiidi korrigeerimise lisamiseks kasutage menüüd **Kliendi korrigeerimised**. Kliendi krediidigrupi krediidilimiidi lisamiseks valige **Kliendi krediidigrupi korrigeerimised**.
2. Sisestage kliendi konto arve kliendikonto jaoks, mida tuleks uue krediidilimiidiga värskendada. Kui valisite 1. etapis **Kliendi krediidigrupi korrigeerimine**, sisestage kliendi krediidigrupp. Samale töölehe reale ei saa sisestada nii kliendi kontot kui ka kliendi krediidigrupi ID-d.

    Kuvatakse praegune krediidilimiit ja nimi kuvatakse automaatselt.

3. Sisestage uus krediidilimiit, mis peaks asendama praeguse krediidilimiidi, kui krediidilimiidi kirje sisestatakse.
4. Sisestage kuupäev kliendi krediidilimiidi uue aegumiskuupäeva määratlemiseks. Krediidilimiidi korrigeerimise loomisel peate sisestama krediidilimiidi aegumiskuupäeva.

Väli **Kinnitamise olek** näitab töölehe rea töövoo olekut.

Kui soovite, et krediidilimiidi korrektsioonid luuakse automaatselt, saate kasutada tegevuspaani menüüd **Loo**.
 
### <a name="add-temporary-credit-limit-adjustments"></a>Ajutiste krediidilimiidi korrigeerimiste lisamine

Ajutiste krediidilimiidi korrigeerimiste käsitsi lisamiseks järgige neid töölehe ridade etappe.

1. Kliendi jaoks krediidilimiidi korrigeerimise lisamiseks kasutage menüüd **Kliendi korrigeerimised**. Kliendi krediidigrupi krediidilimiidi lisamiseks valige **Kliendi krediidigrupi korrigeerimised**.
2. Sisestage kliendi konto arve kliendikonto jaoks, mida tuleks uue krediidilimiidiga värskendada. Kui valisite 1. etapis **Kliendi krediidigrupi korrigeerimine**, sisestage kliendi krediidigrupp. Samale töölehe reale ei saa sisestada nii kliendi kontot kui ka kliendi krediidigrupi ID-d.

    Kui aktiivne või tulevane ajutine krediidilimiit on juba olemas, kuvatakse iga ajutise krediidilimiidi puhul praegune ajutine krediidilimiit ja kuupäevavahemik. Nimi kuvatakse automaatselt.

3. Sisestage uus krediidilimiit, mis peaks praeguse krediidilimiidi asendama.
4. Määratlege väljadel **Uus alguskuupäev** ja **Uus lõpukuupäev** periood, millal täpsem krediidilimiit kehtib. Krediidilimiidi korrigeerimise töölehe loomisel peate sisestama krediidilimiidi aegumiskuupäevad.

Väli **Kinnitamise olek** näitab töölehe rea töövoo olekut.

## <a name="generate-credit-limit-adjustments"></a>Krediidilimiidi korrigeerimiste loomine

Krediidilimiiti saate korrigeerida ka automaatselt. Valige toimingupaanil **Loo** ja seejärel valige üks järgmistest valikutest.

- Olemasolevast kliendist
- Olemasoleva kliendi krediidigrupist
- Automaatselt määratud krediidilimiidid

### <a name="from-existing-customer"></a>Olemasolevast kliendist

Töölehe ridu saate luua olemasolevatest klientidest. Kui valite **Loo \> Olemasolevast kliendist**, kuvatakse dialoogiboks, kuhu saate sisestada kriteeriume klientide valimiseks ja uute limiitide arvutamiseks.

1. Sisestage korrigeerimise väärtus, et lisada või lahutada summa krediidilimiidist. Sisestage negatiivne väärtus, et vähendada praegust krediidilimiiti või positiivne väärtus selle suurendamiseks.
2. Valige väljal **Väärtuse tüüp**, kuidas tuleks 1. etapis sisestatud väärtust uue krediidilimiidi arvutamisel kasutada.

    - Valige **Fikseeritud väärtus**, et muuta krediidilimiiti summa võrra.
    - Valige **Protsent**, et muuta krediidilimiiti protsendi võrra.

3. Sisestage väärtus, mida kasutatakse arvutatud krediidilimiidi ümardamiseks. Näiteks sisestage **10.00**, et ümardada krediidilimiit lähima 10.00 valuutaühikuni.
4. Seadistage väli **Ümardamise vorm**, et määrata, kas jääk tuleb ümardada üles- või allapoole.
5. Valige kuupäevade kohandamiseks kasutatav meetod.

    - Kui valite **Absoluutne**, saate sisestada kuupäevad, mis määratlevad krediidilimiitide kuupäevavahemiku.
    - Kui valite **Suhteline**, saate sisestada vahemikule nihke kuupäevad. Krediidilimiidi praegust kuupäevavahemiku korrigeeritakse nihke võrra.

6. Kasutage kiirkaarti **Kaasatavad kirjed**, et filtreerida välja kaasatavate klientide loend. Kui te ei kaasa filtreid, luuakse krediidilimiiti kanded kõigi klientide jaoks.
7. Krediidilimiidi korrigeerimiskirjete loomiseks valige **OK**.

### <a name="from-existing-customer-credit-group"></a>Olemasoleva kliendi krediidigrupist

Töölehe ridu saate luua olemasolevatest kliendi krediidigruppidest. Kui valite **Loo \> Olemasolevast kliendi krediidigrupist**, kuvatakse dialoogiboks, kuhu saate sisestada kriteeriume kliendi krediidigruppide valimiseks ja uute limiitide arvutamiseks. Kriteeriumid on samad kriteeriumid, mida kasutatakse tööleheridade loomisel olemasolevatest klientidest. Vaadake eelmise jaotise etappe.

### <a name="automatic-credit-limits"></a>Automaatselt määratud krediidilimiidid

Kliendi kreediti limiitide määratlemiseks ja värskendamiseks saate luua automaatseid krediidilimiite. Automaatseid krediidilimiite luuakse riskigrupile ja need põhinevad kindlatel väärtustel, mida kasutatakse punktigruppides. Neid automaatseid krediidilimiite saate kasutada krediidilimiidi kannete loomiseks. Kui klient on määratud kindlasse riskigruppi ja kliendi krediidiandmed vastavad automaatse krediidilimiidi kriteeriumile, luuakse krediidilimiiti korrigeerimise kanne.

#### <a name="create-automatic-credit-limits"></a>Automaatsete krediidilimiitide loomine

Automaatseid krediidilimiite luuakse krediidilimiidi korrigeerimiste abil. Kui valite **Loo \> Automaatsed krediidilimiidid**, kuvatakse dialoogiboks, kus saate määrata aegumiskuupäeva uutele krediidilimiitidele, mis luuakse nende riskigruppide põhjal, kuhu kliendid määratud on. Kui olete lõpetanud, valige krediidilimiidi korrigeerimiste ridade loomiseks **OK**.

### <a name="post-adjustments"></a>Korrigeerimiste sisestamine

Pärast krediidilimiidi korrigeerimise ridade loomist saate kannete sisestamiseks ja kliendi krediidilimiitide värskendamiseks kasutada nuppu **Sisesta**. Kuid kui olete töövoo seadistanud, peate töölehe kinnitamisele esitamiseks valima toimingupaanil **Töövoog \> Esita**.

### <a name="credit-limit-adjustments-workflows"></a>Krediidilimiidi korrigeerimise töövood

**Krediidilimiidi korrigeerimiste** töövoogusid saab kasutada krediidilimiidi korrigeerimiste saatmiseks läbi töövoo kinnitamise protsessi. Lehel **Krediidihalduse töövoog** (**Krediidihaldus \> Seadistus \> Krediidihalduse töövoog** worfklow) saate luua kaks töövoogu.

- **Krediidilimiidi korrigeerimised** – seda töövoogu saab kasutada kannete kinnitamiseks päise tasemel.
- **Krediidilimiidi korrigeerimise rida** – seda töövoogu saab kasutada korrigeerimise kannete kinnitamiseks, nii et kirjed saavad töövoo kriteeriumide alusel kinnitada erinevad inimesed.

> [!NOTE]
> Kui loote töövoo **Krediidilimiidi korrigeerimised**, saate selle seadistada nii, et korrigeerimised sisestatakse pärast ridade kinnitamist automaatselt. Lihtsalt lisage töövoole ülesanne **Sisesta tööleht automaatselt**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]