---
title: "Pearaamatu välisvaluuta ümberarvutamine"
description: "Selles teemas antakse ülevaade järgmistest pearaamatu välisvaluuta ümberhindluse protsessi - setup, töötab protsessi, arvutamise protsessi ja kuidas reverse ümberhindamisgruppe, vajaduse korral."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5d6d13fe44eef7766b4dcaf274c3522bce3da816
ms.lasthandoff: 03/31/2017


---

# <a name="foreign-currency-revaluation-for-general-ledger"></a>Pearaamatu välisvaluuta ümberarvutamine

Selles teemas antakse ülevaade järgmistest pearaamatu välisvaluuta ümberhindluse protsessi - setup, töötab protsessi, arvutamise protsessi ja kuidas reverse ümberhindamisgruppe, vajaduse korral. 

Perioodi lõpu osana nõuavad raamatupidamistavad välisvaluutas pearaamatukonto saldode ümberarvutamist, kasutades erinevaid vahetuskursitüüpe (praegune, ajalooline, keskmine jne). Näiteks nõuab üks raamatupidamistava varade ja kohustuste ümberarvutamist praeguse vahetuskursi, põhivarade ümberarvutamist ajaloolise vahetuskursi ning tulu- ja kulukontode ümberarvutamist igakuise keskmise vahetuskursi alusel. Pearaamatu välisvaluuta ümberarvutamist saab kasutada bilansi ning tulu- ja kulukontode ümberarvutamiseks. 

> [!NOTE]
> Välisvaluuta ümberhindluse pakutakse ka (AR) Müügireskontro ja Ostureskontro (AP). Kui te kasutate neid mooduleid, pooleliolevatest tehingutest ümberhindamise korra välisvaluuta ümberhindluse nende moodulite abil. Müügireskontro ja ostureskontro välisvaluuta ümberarvutamine loob pearaamatus raamatupidamiskirje, et kajastada realiseerimata kasumit või kahjumit, tagades, et alammoodulid ja pearaamatu saab vastavusse viia. Kuna müügireskontro ja ostureskontro välisvaluuta ümberarvutamine loob pearaamatusse raamatupidamiskirjed, tuleb müügireskontro ja ostureskontro põhikontod välistada pearaamatu välisvaluuta ümberarvutusest. 

Ümberarvutusprotsessi käivitamisel arvutatakse ümber igas põhikontos olev välisvaluutas sisestatud saldo. Ümberarvutamise protsessi käigus loodud realiseerimata kasumi või kahjumi kanded on süsteemi loodud. Kaks tehingut võib luua, üks valuuta arvestus ja aruandevaluuta, teine vajadusel. Iga arvestuskande pärast realiseerimata kasum või kahjum ja peamine konto, mida hinnatakse ümber.

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

Selle **kursi kuupäev** saab määrata kuupäeva, mille vahetuskurss tuleks vaikimisi. Näiteks võib ümber hinnata saldode vahel kuupäeva vahemikus jaanuar 1-31. jaanuar, kuid veebruar 1 määratud vahetuskurssi. 

Valige, millised põhikontod tuleb ümber arvutada: Kõik, Bilanss või Kasum ja kahjum. Hinnatakse ümber ümberhindluse (Main konto lehel) märgitud ainult keskne raamatupidamine. Kui soovite piirata keskne raamatupidamine hulk, kasutage kirjete **lisada** vahekaarti Otsi keskne raamatupidamine või üksikute keskne raamatupidamine. 

Ümberhindamise protsessi saab käivitada ühe või mitme juriidilise isiku. Otsingu kuvab ainult juriidilised isikud, millele teil on juurdepääs. Juriidilised isikud, mille soovite ümberhindamise protsessi käivitamiseks valige. 

Ümberarvutamise saab käitada ühe või mitme välisvaluuta puhul. Otsingu sisaldab kõiki valuutasid, konteeritud kuupäevavahemikku jäävate põhikonto (bilanss või kasumiaruanne), juriidiliste isikute ümber hinnata valitud tüübist. Raamatupidamise valuuta on nimekirja kantud, kuid midagi hinnatakse ümber raamatupidamise valuuta valimisel. 

Seada **eelvaade enne postitamist** et **Jah** kui soovite vaadata pearaamatu ümberhindluse tulemusena. Eelvaate üldiselt pearaamatu erineb AR ja AP välisvaluuta ümberhindluse simulatsioon. Simulatsiooni AR ja AP on aruande, kuid pearaamatu on eelvaade, mida saab, ilma et ümberhindamise protsessi uuesti käivitada. Eelvaate tulemused saab eksportida Microsoft Excelisse, et säilitada ajalugu summade arvutamise viisist. Pakktöötlust ei saa kasutada, kui soovite ümberarvutamise tulemusi eelvaadata. Eelvaates on kasutajal võimalus sisestada kõigi juriidiliste isikute tulemused nupuga **Sisesta**. Kui juriidilise isiku puhul on tulemustega probleeme, on kasutajal võimalus ka sisestada juriidiliste isikute alamkogum, kasutades nuppu **Valige sisestamiseks juriidilised isikud**. 

Kui välisvaluuta ümberhindluse protsess on lõppenud, luuakse kirje iga katse ajalugu jälgida.  Iga juriidiline isik ja sisestamiskihi luuakse eraldi kirje.

## <a name="calculate-unrealized-gainloss"></a>Realiseerimata kasumi/kahjumi arvutamine
Realiseerimata kasumi/kahjumi kanded luuakse pearaamatu ümberarvutamise ning müügireskontro ja ostureskontro ümberarvutamise protsessi puhul erinevalt. Müügireskontros ja ostureskontros tühistatakse eelmine ümberarvutus täielikult (eeldusel, et kanne pole veel tasakaalustatud) ning realiseerimata kasumi/kahjumi jaoks luuakse uue vahetuskursi alusel uus kanne. Selle põhjuseks on müügireskontros ja ostureskontros iga üksiku kande ümberarvutamine. Pearaamatu, eelmise ümberhindluse ei tühistata. Selle asemel luuakse tehingu saldo, mille peamine, sealhulgas eelmise ümberhindluse summad ja uus väärtus vastavalt vahetuskursile Määra kuupäev delta. 

**Näide** saldosid olemas peamine konto 110110.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Kuupäev**   | **Pearaamatukonto** | **Kandesumma** | **Raamatupidamissumma** |
| 20. jaanuar | 110110 (sularaha)      | 500 eurot (deebet)        | 1000 USA dollarit (deebet)      |

31. jaanuaril hinnatakse ümber peamine konto.  Realiseerimata kasum/kahjum arvutatakse järgmiselt.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Praegune saldo kandevaluutas** | **Praegune saldo arvestusvaluutas** | **Vahetuskurss ümberarvutamisel** | **Uue arvestusvaluuta summa** | **Realiseerimata kasum/kahjum**    |
| 500 eurot                                     | 1000 USA dollarit                                   | 166.6667                         | 833,33 eurot (500 × 1,666667)        | Kahjum 166,67 (833,33 – 1000) |

Luuakse järgmine raamatupidamiskirje.

|            |                          |           |            |
|------------|--------------------------|-----------|------------|
| **Kuupäev**   | **Pearaamatukonto**       | **Debiteeri** | **Krediit** |
| 31. jaanuar | 110110 (sularaha)            |           | 166.67     |
| 31. jaanuar | 801 400 (realiseerimata kahjum) | 166.67    |            |

Uusi kandeid ei sisestata veebruarikuu.  Peamine konto on ümberhindamine toimub veebruar 28.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Praegune saldo kandevaluutas** | **Praegune saldo arvestusvaluutas** | **Vahetuskurss ümberarvutamisel** | **Uue arvestusvaluuta summa** | **Realiseerimata kasum/kahjum**    |
| 500 eurot                                     | 833,33 USA dollarit (1000 – 166,67)                 | 250.0000                         | 1250 USA dollarit (500 × 2,5)               | Kasum 416,67 (1250 – 833,33) |

Luuakse järgmine raamatupidamiskirje.

|             |                          |           |            |
|-------------|--------------------------|-----------|------------|
| **Kuupäev**    | **Pearaamatukonto**       | **Debiteeri** | **Krediit** |
| 28. veebruar | 110110 (sularaha)            | 416.67    |            |
| 28. veebruar | 801 600 (realiseerimata kasum) |           | 416.67     |

## <a name="reverse-foreign-currency-revaluation"></a>Välisvaluuta ümberarvutamise tühistamine
Kui soovite ümberarvutuskande tühistada, valige lehel **Välisvaluuta ümberarvutamine** nupp **Tühista kanne**. Luuakse uue välisvaluuta ümberarvutamise ajalooline kirje, et säilitada ajalooline kontrolljälg ümberarvutamise toimumise või tühistamise ajast. 

Te saate tulemid ümberhindluse kuupäeva järjekorras kokku, kuid võib osutuda ka vastupidine ajakohasemaid ümberhindluse iga ümberhinnatud peamine konto õige tasakaalu tagamiseks. Selle pöördumise saab aegunud tellimuse tekkida, sest kuidagi kontrollida, milline keskne raamatupidamine hinnatakse ümber ja millal nad hinnatakse ümber sagedus. Näiteks võite organisatsioon ümber hinnata iga kuu raha põhiaruanded kvartalis, kuid kõik muud keskne raamatupidamine.


