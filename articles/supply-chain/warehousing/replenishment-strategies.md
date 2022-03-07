---
title: Täiendusstrateegiad
description: Selles teemas antakse teavet täiendusstrateegiate kohta ja selgitatakse, kuidas täiendamise strateegiat saab kasutada voo nõudluse täiendamismalli ridadel, et valida, kuidas täiendamist teostatakse.
author: mirzaab
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: bd2ddbfeef454f2759ca09d8d763bada36a1fc83
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574157"
---
# <a name="replenishment-strategies"></a>Täiendusstrateegiad

[!include [banner](../includes/banner.md)]

**Täiendamismallid** lehel defineeritud mallid sisaldavad voo nõudluse täiendamismalli ridu, kus saate valida, kuidas täiendamist teostatakse. Iga rida sisaldab nüüd **Täiendamisstrateegia** välja.

*Voo nõudluse koguse* strateegia on vaikimisi strateegia. See on täiendamisstrateegia, mida kasutati enne **Täiendamisstrateegia** välja kasutuselevõttu. See kasutab täiendamise asukoha direktiive, et leida asukohti, mida saab täiendada. Seejärel täiendatakse neid asukohti seni, kuni nõudlus on kaetud.

*Maksimaalne asukoha võimsuse* strateegia tutvustab uusi funktsioone. Nagu *Voo nõudluse koguse* strateegia, kasutab see strateegia täiendamise asukoha direktiive, et leida asukohti, mida saab täiendada ja seejärel täiendatakse neid asukohti seni, kuni nõudlus on kaetud. See erineb *Voo nõudluse koguse* strateegiast selle poolest, et kõik täiendatud asukohad täiendatakse nende maksimaalse võimsusega, nagu on määratletud asukoha varude piirangutes. *Maksimaalne asukoha võimsuse* strateegia püüab luua tööd, mis toob nõutud koguse, pluss mõned lisakogused, et täita need asukohad, mida täiendatakse. Kuid mõnel juhul võib see katse ebaõnnestuda. Näiteks ei pruugi suurema varuga asukohtadel olla piisavalt varusid lisakoguse katmiseks. Sellisel juhul tuvastab süsteem tõrke ja proovib taastuda.

Kõrghooaeg on üks näide olukorrast, kus *Maksimaalne asukoha võimsuse* strateegia on eelistatav *Voo nõudluse koguse* strateegiale. Kõrghooajal võivad mõned kaubad olla suure müügimahuga. Seetõttu võite soovida vastavaid komplekteerimisasukohti ennetavalt täiendada nii palju kui võimalik, et vähendada täiendamiseks loodud töö-ID-de arvu.

> [!IMPORTANT]
> *Asukoha maksimaalse võimsuse* strateegia täielikuks ärakasutamiseks peate vastavate asukohtade ladustamislimiidid uuesti määratlema. Vastasel juhul töötab see strateegia nagu *Voo nõudluse koguse* strateegia.

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a>Lülitage sisse maksimaalne täiendamine vastavalt laovarude piirangutele funktsioon

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [Funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida selle funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Maksimaalne täiendamine vastavalt laovarude piirangutele*

## <a name="set-up-replenishment-strategies"></a>Täiendusstrateegiate seadistamine

Mallide juurdepääsuks minge **Laohaldus \> Seadistus \> Täiendamine \> Täiendamise mallid**. Jaotises **Ülevaade** valige või looge voo nõudluse täiendamise mall, kus välja **Täiendamise tüüp** väärtuseks on seatud *Voo nõudlus*. Seejärel seadistage täiendamise malli read jaotises **Täiendamise malli üksikasjad**. **Täiendamisstarteegia** väljal valige iga real jaoks täiendamisstrateegia, mida soovite kasutada.

![Täiendamise mallide leht](media/ReplenTempWaveDmdMaxLocCap.png "Täiendamise mallide leht")

Kui **Täiendamisstrateegia** veergu ei kuvata **Täiendamise malli üksikasjade** ruudustikus, veenduge, et funktsioon on sisse lülitatud ja valitud täiendamise malli täiendamise tüübiks on seatud *Voo nõudlus*.

> [!NOTE]
> *Voo nõudluse koguse* strateegia on vaikimisi strateegia. Seetõttu tuleb teil lihtsalt uuendada varude täiendamise malli read, kus soovite selle asemel kasutada *Asukoha maksimaalse võimsuse* strateegiat.

## <a name="example-scenarios"></a>Näidisstsenaariumid

### <a name="example-1"></a>Näide 1

Selles näites on ainult üks täiendamise mall, millel on ainult üks täiendamise malli rida.

Loote müügitellimuse 130 tk kaubale A0001. Enne tellimuse lattu väljastamist seadistatakse ladu järgmisel viisil:

- On ainult üks suurema varuga asukoht ja sellel on 500 tk vaba kaubavaru.
- On kolm komplekteerimisasukohta, millest igaühes on varu piirang 100 tk. (Pidage meeles, et ladustamise piirangud on vajalikud *Asukoha maksimaalse võimsuse* strateegiaks.)
- Täiendamise asukohad on samad, mis komplekteerimise asukohad.
- Täiendamise ühik on kast (1 kast = 20 tk).

Tellimuse ajal on müügitellimuse komplekteerimise asukohtades vabad järgmised varud:

- **Komplekteerimine-001:** 20 tk (1 kast)
- **Komplekteerimine-002:** 0 tk
- **Komplekteerimine-003:** 0 tk

Esialgu seatakse täiendamise strateegiaks voo *Voo nõudluse kogus*.

Pärast seda, kui väljastate müügitellimuse lattu ja voo jaoks käivitub voo töötlemine, saate järgmise täiendamise töö:

- **Täiendamise töö 1:** Valige 4 kasti suurema varuga asukohast ja pange need asukohta komplekteerimine-001.
- **Täiendamise töö 2:** Valige 2 kasti suurema varuga asukohast ja pange need asukohta komplekteerimine-002.

Saate kaks täiendamise töö ID-d, kuna peate täiendama kahte asukohta ja mitut komplekteerimist ei toetata.

Kui seate täiendamise strateegiaks *Asukoha maksimaalne võimsus*, saate järgmise täiendamise töö:

- **Täiendamise töö 1:** Valige 4 kasti suurema varuga asukohast ja pange need asukohta komplekteerimine-001.
- **Täiendamise töö 2:** Valige 5 kasti suurema varuga asukohast ja pange need asukohta komplekteerimine-002.

[![Näide 1.](media/ReplenTemp_example_1.png "Näide 1")](media/ReplenTemp_example_1_large.png)

### <a name="example-2"></a>Näide 2

See näide näitab, mis juhtub, kui suurema varuga asukohtades ei ole lisakoguse katmiseks piisavalt varusid. See kasutab sama stsenaariumi nagu näide 1, kuid suurema varuga asukohtades on 160 tk (8 kasti).

*Voo nõudluse koguse* strateegia loob sama töö, mida tehti näites 1.

Kuna aga *Asukoha maksimaalse võimsuse* strateegia üritab luua töö ID-d, nagu see tegi näites 1, võib see nurjuda. Sel hetkel püüab süsteem taastuda.

Sõltuvalt asukoha direktiivides olevale täiendamise komplekteerimise sätte **Luba poolitamine** valikule on võimalikud kaks tulemust:

- Kui suvandi **Luba poolitamine** väärtuseks on seatud *Jah*, luuakse järgmine täiendamise töö:

    - **Täiendamise töö 1:** Valige 4 kasti suurema varuga asukohast ja pange need asukohta komplekteerimine-001.
    - **Täiendamise töö 2:** Valige 4 kasti suurema varuga asukohast ja pange need asukohta komplekteerimine-002.

- Kui suvandi **Luba poolitamine** väärtuseks on seatud *Ei*, luuakse järgmine täiendamise töö:

    - **Täiendamise töö 1:** Valige 4 kasti suurema varuga asukohast ja pange need asukohta komplekteerimine-001.
    - **Täiendamise töö 2:** Valige 2 kasti suurema varuga asukohast ja pange need asukohta komplekteerimine-002.

Tulemused erinevad sõltuvalt teabest, mis on saadaval, kui loote töö. Kui täiendamise komplekteerimiseks mõeldud asukoha direktiivide suvand **Luba poolitamine** väärtuseks on seatud *Jah*, siis teate, et teil õnnestus leida 160 tk. Seetõttu saate luua töö selle koguse jaoks. Kuid kui suvandi **Luba poolitamine** väärtuseks on seatud *Ei*, ei tea te 160 tk olemasolust. Kuna lisakogus, mida otsustasite täiendada, oli 3 kasti, unustate selle lisakoguse ja proovite uuesti algset kogust.

[![Näide 2.](media/ReplenTemp_example_2.png "Näide 2")](media/ReplenTemp_example_2_large.png)

Selleks, et saada maksimaalset kogust täiendatud asukohtadesse, peaksite täiendamise komplekteerimise asukoha direktiivides seadistama suvandi **Luba poolitamine** väärtusele *Jah*.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]