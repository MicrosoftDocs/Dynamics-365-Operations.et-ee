---
title: Pearaamatu välisvaluuta ümberarvutamine
description: 'Selles teemas antakse ülevaade pearaamatu välisvaluuta ümberarvutamise protsessi järgmistest toimingutest: seadistamine, protsessi käitamine, protsessi jaoks arvutamine ja vajaduse korral ümberarvutuskannete tühistamine.'
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.reviewer: roschlom
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2f24c60b3fb82532f50e58dde9a19f5fefb25d5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832918"
---
# <a name="foreign-currency-revaluation-for-general-ledger"></a>Pearaamatu välisvaluuta ümberarvutamine

[!include [banner](../includes/banner.md)]

Selles teemas antakse ülevaade pearaamatu välisvaluuta ümberarvutamise protsessi järgmistest toimingutest: seadistamine, protsessi käitamine, protsessi jaoks arvutamine ja vajaduse korral ümberarvutuskannete tühistamine. 

Perioodi lõpu osana nõuavad raamatupidamistavad välisvaluutas pearaamatukonto saldode ümberarvutamist, kasutades erinevaid vahetuskursitüüpe (praegune, ajalooline, keskmine jne). Näiteks nõuab üks raamatupidamistava varade ja kohustuste ümberarvutamist praeguse vahetuskursi, põhivarade ümberarvutamist ajaloolise vahetuskursi ning tulu- ja kulukontode ümberarvutamist igakuise keskmise vahetuskursi alusel. Pearaamatu välisvaluuta ümberarvutamist saab kasutada bilansi ning tulu- ja kulukontode ümberarvutamiseks. 

> [!NOTE]
> Välisvaluuta ümberarvutamine on saadaval ka müügireskontros ja ostureskontros. Kui kasutate neid mooduleid, tuleb tasumata kanne ümber arvutada neis moodulites välisvaluuta ümberarvutamist kasutades. Müügireskontro ja ostureskontro välisvaluuta ümberarvutamine loob pearaamatus raamatupidamiskirje, et kajastada realiseerimata kasumit või kahjumit, tagades, et alammoodulid ja pearaamatu saab vastavusse viia. Kuna müügireskontro ja ostureskontro välisvaluuta ümberarvutamine loob pearaamatusse raamatupidamiskirjed, tuleb müügireskontro ja ostureskontro põhikontod välistada pearaamatu välisvaluuta ümberarvutusest. 

Ümberarvutusprotsessi käivitamisel arvutatakse ümber igas põhikontos olev välisvaluutas sisestatud saldo. Ümberarvutamise protsessi käigus loodud realiseerimata kasumi või kahjumi kanded on süsteemi loodud. Luua võib kaks kannet: ühe arvestusvaluuta ja teise aruandlusvaluuta jaoks, kui see on asjakohane. Iga raamatupidamiskirje sisestatakse realiseerimata kasumisse või kahjumisse ja põhikonto arvutatakse ümber.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Välisvaluuta ümberarvutamise käivitamiseks valmistumine
Enne kui saate ümberarvutamise protsessi käivitada, on nõutav järgmine seadistus.

-   **Põhikonto** lehel
-   Kui põhikonto tuleb ümber arvutada pearaamatus, valige suvand **Välisvaluuta ümberarvutamine**. Kui põhikontot ei tohiks ümber arvutada (näiteks alammoodulis ümberarvutatud müügireskontro ja ostureskontro puhul), tühistage valik.
-   Kui põhikonto on ümberarvutamiseks märgitud, sisestage **Vahetuskursi tüüp**. Vahetuskursi tüüpi kasutatakse põhikonto ümberarvutamiseks. Finantsaruandluse jaoks on saadaval eraldi väli **Finantsaruandluse vahetuskursi tüüp**. Need kaks välja pole sünkroonis, mis võimaldab kasutada ümberarvutamisel ja aruandlusel erinevaid vahetuskursi tüüpe.

-   Lehel **Pearaamat**
-   Määrake **Vahetuskursi tüüp**. Kui vahetuskursi tüüp on põhikontol määratlemata, kasutatakse seda vahetuskursi tüüpi välisvaluuta ümberarvutamisel.
-   Määrake valuuta ümberarvutamiseks realiseeritud kasumi, realiseeritud kahjumi, realiseerimata kasumi ja realiseerimata kahjumi kontod. Realiseeritud kasumi ja realiseeritud kahjumi kontosid kasutatakse müügireskontro ja ostureskontro kannete tasakaalustamisel ning realiseerimata kasumi ja realiseerimata kahjumi kontosid avatud kannete ja pearaamatu põhikontode ümberarvutamiseks.

-   Lehel **Valuuta ümberhindamise kontod**
-   Saate valida iga valuuta ja ettevõtte jaoks erinevad valuuta ümberarvutamise kontod. Kui ühtegi kontot pole määratletud, kasutatakse suvandi **Pearaamat** kontosid.

## <a name="process-foreign-currency-revaluation"></a>Välisvaluuta ümberarvutamise töötlemine
Pärast seadistamise lõpetamist kasutage põhikontode saldode ümberarvutamiseks lehte **Välisvaluuta ümberarvutamine**. Saate käivitada protsessi reaalajas või ajastada selle käivitamise, kasutades pakki. 

Lehel **Välisvaluuta ümberarvutamine** kuvatakse iga ümberhindamisprotsessi ajalugu, sh protsessi käitamise aeg, määratletud kriteeriumid, link ümberarvutuseks loodud kandele ja kirje, kui eelmine ümberarvutus tühistati. Ümberarvutamise protsessi käivitamiseks valige nupp **Välisvaluuta ümberarvutamine**. 

Väljade **Alguskuupäev** ja **Lõppkuupäev** väärtused määratlevad kuupäevaintervalli ümberarvutatava välisvaluuta saldo arvutamiseks. Kasumi ja kahjumi kontode ümberarvutamisel arvutatakse ümber kõik kuupäevavahemikku jäävate kannete summa. Bilansikontode ümberarvutamisel eiratakse alguskuupäeva. Selle asemel määratakse ümberarvutatav saldo finantsaasta algusest kuni lõppkuupäevani. 

Välja **Kursi kuupäev** abil saab määratleda kuupäeva, mille puhul vahetuskurss peaks olema vaikeväärtus. Näiteks saate ümber arvutada saldosid kuupäevavahemikus 1. jaanuarist 31. jaanuarini, kuid kasutada 1. veebruari jaoks määratletud vahetuskurssi. 

Valige, millised põhikontod tuleb ümber arvutada: Kõik, Bilanss või Kasum ja kahjum. Ümber arvutatakse ainult ümberarvutamiseks märgitud põhikontod (lehel Põhikontod). Kui soovite põhikontode valikut täiendavalt piirata, kasutage vahekaarti **Kaasatavad kirjed**, et määratleda põhikontode vahemik või üksikud põhikontod. 

Ümberarvutusprotsessi saab käitada ühe või mitme juriidilise isiku puhul. Otsingus kuvatakse ainult need juriidilised isikud, kellele teil on juurdepääs. Valige juriidilised isikud, mille puhul soovite ümberarvutamisprotsessi käitada. 

Ümberarvutamise saab käitada ühe või mitme välisvaluuta puhul. Otsingusse kaasatakse kõik valuutad, mis sisestati põhikonto tüübile (Bilanss või Kasum ja kahjum) vastavas kuupäevavahemikus ümberarvutamiseks valitud juriidiliste isikute puhul. Arvestusvaluuta lisatakse loendisse, kuid arvestusvaluuta valimisel ei arvutata midagi ümber. 

Valige suvandi **Eelvaade enne sisestamist** sätteks **Jah**, kui soovite kuvada pearaamatu ümberarvutamise tulemuse eelvaate. Eelvaade pearaamatus erineb müügireskontro ja ostureskontro välisvaluuta ümberarvutamise simulatsioonist. Ostureskontros ja müügireskontros on simulatsioon aruanne, kuid pearaamatul on eelvaade, mida saab sisestada, ilma et ümberarvutusprotsessi tuleks uuesti käitada. Eelvaate tulemused saab eksportida Microsoft Excelisse, et säilitada ajalugu summade arvutamise viisist. Pakktöötlust ei saa kasutada, kui soovite ümberarvutamise tulemusi eelvaadata. Eelvaates on kasutajal võimalus sisestada kõigi juriidiliste isikute tulemused nupuga **Sisesta**. Kui juriidilise isiku puhul on tulemustega probleeme, on kasutajal võimalus ka sisestada juriidiliste isikute alamkogum, kasutades nuppu **Valige sisestamiseks juriidilised isikud**. 

Kui välisvaluuta ümberarvutamise protsess on lõppenud, luuakse kirje iga tsükli ajaloo jälgimiseks.  Iga juriidilise isiku ja sisestamiskihi kohta luuakse eraldi kirje.

## <a name="calculate-unrealized-gainloss"></a>Realiseerimata kasumi/kahjumi arvutamine
Realiseerimata kasumi/kahjumi kanded luuakse pearaamatu ümberarvutamise ning müügireskontro ja ostureskontro ümberarvutamise protsessi puhul erinevalt. Müügireskontros ja ostureskontros tühistatakse eelmine ümberarvutus täielikult (eeldusel, et kanne pole veel tasakaalustatud) ning realiseerimata kasumi/kahjumi jaoks luuakse uue vahetuskursi alusel uus kanne. Selle põhjuseks on müügireskontros ja ostureskontros iga üksiku kande ümberarvutamine. Pearaamatus ei tühistata eelmist ümberarvutust. Selle asemel luuakse kanne põhikonto saldo vahelise delta jaoks (sh kõik varasemad ümberarvutussummad) ning uus väärtus arvutatakse kursi kuupäeva vahetuskursi põhjal. 

**Näide** Põhikonto 110110 puhul on olemas järgmised saldod.

| Kuupäev   | Pearaamatukonto| Kandesumma | Raamatupidamissumma |
|------------|--------------------|------------------------|-----------------------|
| 20. jaanuar | 110110 (sularaha)      | 500 eurot (deebet)        | 1000 USA dollarit (deebet)      |

Põhikonto arvutatakse ümber 31. jaanuaril.  Realiseerimata kasum/kahjum arvutatakse järgmiselt.

| Praegune saldo kandevaluutas | Praegune saldo arvestusvaluutas | Vahetuskurss ümberarvutamisel | Uue arvestusvaluuta summa | Realiseerimata kasum/kahjum    |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| 500 eurot                                     | 1000 USA dollarit                                   | 166.6667                         | 833.33 USA dollarit (500 × 1,666667)        | Kahjum 166,67 (833,33 – 1000) |

Luuakse järgmine raamatupidamiskirje.

| Kuupäev   | Pearaamatukonto       | Debiteeri | Krediit |
|------------|--------------------------|-----------|------------|
| 31. jaanuar | 110110 (sularaha)            |           | 166.67     |
| 31. jaanuar | 801 400 (realiseerimata kahjum) | 166.67    |            |

Veebruari kohta uusi kandeid ei sisestata.  Põhikonto arvutatakse ümber 28. veebruaril.

| Praegune saldo kandevaluutas | Praegune saldo arvestusvaluutas | Vahetuskurss ümberarvutamisel | Uue arvestusvaluuta summa | Realiseerimata kasum/kahjum    |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| 500 eurot                                     | 833,33 USA dollarit (1000 – 166,67)                 | 250.0000                         | 1250 USA dollarit (500 × 2,5)               | Kasum 416,67 (1250 – 833,33) |

Luuakse järgmine raamatupidamiskirje.

| Kuupäev    | Pearaamatukonto       | Debiteeri | Krediit |
|-------------|--------------------------|-----------|------------|
| 28. veebruar | 110110 (sularaha)            | 416.67    |            |
| 28. veebruar | 801 600 (realiseerimata kasum) |           | 416.67     |

## <a name="reverse-foreign-currency-revaluation"></a>Välisvaluuta ümberarvutamise tühistamine
Kui soovite ümberarvutuskande tühistada, valige lehel **Välisvaluuta ümberarvutamine** nupp **Tühista kanne**. Luuakse uue välisvaluuta ümberarvutamise ajalooline kirje, et säilitada ajalooline kontrolljälg ümberarvutamise toimumise või tühistamise ajast. 

Saate tühistada ümberarvutuste tulemused aegumisjärjestuses, kuid samuti on teil võimalik tühistada ajakohasemat ümberarvutust, et tagada iga ümberarvutatud põhikonto puhul õiged saldod. Tühistamised võivad toimuda aegumisjärjestuses, kuna pole mingit viisi määrata, millised põhikontod ümber hinnatakse ja kui sageli seda tehakse. Näiteks võib organisatsioon soovida oma sularaha põhikontod ümber hinnata kord kvartalis, kuid kõik muud põhikontod kord kuus.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
