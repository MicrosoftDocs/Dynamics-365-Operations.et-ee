---
title: Panga välisvaluuta ümberarvutamine
description: Selles teemas antakse ülevaade panga välisvaluuta ümberarvutamise protsessi kohta. Siin on teave seadistamise, protsessi käitamise, protsessi jaoks arvutuste tegemise ja ümberarvutuskannete tühistamise kohta.
author: mikefalkner
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankCurrencyRevalHistory
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: 10
ms.openlocfilehash: d7e7006679757d7e779b86c58649cd3869e1c7d0
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842637"
---
# <a name="bank-foreign-currency-revaluation"></a>Panga välisvaluuta ümberarvutamine

[!include [banner](../includes/banner.md)]


Selles teemas antakse ülevaade panga välisvaluuta ümberarvutamise protsessi kohta. Siin selgitatakse, kuidas protsessi seadistada ja käitada, ning antakse teavet protsessi jaoks tehtavate arvutuste kohta. Samuti selgitatakse, kuidas ümberarvutuskandeid vajaduse korral tühistada.

Perioodi lõpu üks osa on raamatupidamistavade järgi pangakontode välisvaluutas saldode ümberarvutamist eri tüüpi vahetuskurssidega (praegune, ajalooline, keskmine jne). Panga välisvaluuta ümberarvutamise funktsiooni saab kasutada ühe võit mitme pangakonto ümberhindamiseks. See funktsioon ka globaalne funktsioon. Seetõttu saate ühelt lehelt ümber hinnata kõikide juriidiliste isikute pangakontosid, millele teil on juurdepääs.

> [!NOTE]
> Ümberarvutusprotsessi käitamisel arvutatakse ümber igal pangakontol olev välisvaluutas sisestatud saldo. Ümberarvutamise protsessi käigus loodud realiseerimata kasumi või kahjumi kanded on süsteemi loodud. Luua saab kaks kannet: ühe arvestusvaluutas ja vajaduse korral teise aruandlusvaluutas. Iga raamatupidamiskirje sisestatakse realiseerimata kasumisse või kahjumisse ja ümberarvutatavale põhikontole.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Välisvaluuta ümberarvutamise käivitamiseks valmistumine

Enne kui saate ümberarvutamise protsessi käivitada, on nõutav järgmine seadistus.

- Määrake vahetuskursi tüüp lehel **Pearaamat**. Kui vahetuskursi tüüp on põhikontol määratlemata, kasutatakse välisvaluuta ümberarvutamisel seda tüüpi vahetuskurssi.
- Määrake lehel **Pearaamat** valuuta ümberarvutamise puhul realiseeritud kasumi, realiseeritud kahjumi, realiseerimata kasumi ja realiseerimata kahjumi kontod. Realiseeritud kasumi ja realiseeritud kahjumi kontosid kasutatakse siis, kui müügireskontro ning ostureskontro kanded tasakaalustatakse. Realiseerimata kasumi ja realiseerimata kahjumi kontosid kasutatakse avatud kannete ning pearaamatu põhikontode ümberarvutamiseks.
- Valige lehel **Valuuta ümberarvutamise kontod** iga valuuta ja ettevõtte jaoks erisugused valuuta ümberarvutamise kontod. Kui ühtegi kontot pole määratletud, kasutatakse suvandi **Pearaamat** kontosid.

## <a name="enable-foreign-currency-revaluation"></a>Välisvaluuta ümberarvutamise lubamine

Välisvaluuta ümberarvutuste töötlemiseks peate sisse lülitama panga välisvaluuta ümberarvutamise funktsiooni.

1. Valige **Sularaha- ja pangahaldus \> Seadistus \> Sularaha- ja pangahalduse parameetrid**.
2. Funktsiooni sisselülitamiseks parajasti valitud juriidilise isiku jaoks määrake lehe **Välisvaluuta ümberarvutamine** vahekaardil **Üldine** suvandi **Luba panga ümberarvutamine** olekuks **Jah**. 
3. Vahekaardil **Numbriseeriad** lisage välisvaluuta ümberarvutamise jaoks numbriseeria.
4. Värskendage brauserit, et **Välisvaluuta ümberarvutamine** ilmuks ala lehe jaotisse **Perioodilised ülesanded**.

Peate funktsiooni sisse lülitama iga välisvaluuta ümberarvutamist kasutava juriidilise isiku korral. Kui teile on määratud süsteemiadministraatori või funktsioonihalduri roll, saate selle etapi eemaldada, lubades funktsiooni nimega **Panga ümberhindamine ilma parameetrita** tööruumis **Funktsioonihaldus**.

> [!NOTE]
> Kui teie juriidiline isik kasutab Vene, Poola või Ungari riigi/regiooni koodi, saate juba teha panga välisvaluuta ümberarvutamist. Te ei saa kasutada välisvaluuta ümberarvutamist, mida kasutatavad teised riigid või regioonid.

## <a name="process-foreign-currency-revaluation"></a>Välisvaluuta ümberarvutamise töötlemine

Pärast seadistamist kasutage kõikide juriidiliste isikute pangakontode saldode ümberarvutamiseks sularaha- ja pangahalduse mooduli lehte **Välisvaluuta ümberarvutamine**. Seda protsessi saate käitada reaalajas või ajastada selle käitamine partiid kasutades.

Lehel **Välisvaluuta ümberarvutamine** kuvatakse iga ümberarvutamise ajalugu. Seal kuvatakse protsessi käitamise aeg ja määratud kriteeriumid ning ümberarvutamise kohta loodud kande link. Samuti näete, kas eelmine ümberarvutus tühistati. Ümberarvutusprotsessi käitamiseks valige toimingupaanilt **Välisvaluuta ümberarvutamine** ja avaneb dialoogiboks **Pank – välisvaluuta ümberarvutamine**.

Väljaga **Ümberarvutamise kuupäev** määratakse ümberarvutatava välisvaluuta saldo arvutamiseks kindlaks äralõikekuupäev. Kõigi selle kuupäevani toimunud pangatehingute summa arvutatakse ümber.

Väljaga **Vahetuskursi kuupäev** määratakse kindlaks valuutasaldode ümberarvutamiseks kasutatava vahetuskursi kuupäev. Näiteks saate saldosid ümber arvutada 31. jaanuari seisuga, kuid kasutada 1. veebruariks määratud vahetuskurssi.

Ümberarvutusprotsessi saab käitada ühe või mitme juriidilise isiku puhul. Otsing kuvab ainult need juriidilised isikud, kellele teil on juurdepääs. Valige juriidilised isikud, kellele soovite valida pangakontod, mis sobivad välisvaluuta ümberarvutamiseks. Kõik nende juriidiliste isikute pangakontod kuvatakse ruudustikus.

Kui soovite ümberarvutamise tulemusi enne sisestamist üle vaadata, määrake suvandi **Eelvaade enne sisestamist** olekuks **Jah**. Välisvaluuta ümberarvutamisel on eelvaade, mida saab sisestada. Te ei pea ümberarvutamisprotsessi uuesti käivitama. Te saate eksportida eelvaates olevad tulemused Microsoft Excelisse, et säiliks summade arvutamise ajalugu. Kui soovite ümberarvutamise tulemuste eelvaadet näha, ei saa te kasutada pakktöötlust.

Välisvaluuta ümberarvutamise töötlemiseks valige **OK**. Iga tsükli ajaloo jälgimiseks luuakse kirje. Iga juriidilise isiku ja sisestamiskihi kohta luuakse eraldi kirje.

## <a name="calculate-unrealized-gainloss"></a>Realiseerimata kasumi/kahjumi arvutamine

Sularaha- ja pangahalduse moodulis peetakse pangavaluutat baasvaluutaks ja seda ei arvutata ümber. Pangakonto saldo, mis on arvestusvaluutas, arvutatakse ümber pangavaluuta ja arvestusvaluuta vaheliste vahetuskurssidega, mis kehtivad sättega **Vahetuskursi kuupäev** määratud kuupäeval. Pangakonto saldo, mis on aruandlusvaluutas, arvutatakse samuti ümber pangavaluuta ja aruandlusvaluuta vaheliste vahetuskurssidega, mis kehtivad sättega **Vahetuskursi kuupäev** määratud kuupäeval.

Pangakonto saldo ja arvestusvaluuta jaoks arvutatud uue saldo vahelise erinevuse kohta luuakse kanne. Pangakonto saldo ja aruandlusvaluuta jaoks arvutatud uue saldo vahelise erinevuse kohta luuakse teine kanne. Nende kannete kirjed märgitakse vastavusse viiduks. 

Arvestusvaluuta kohta ei tehta kirjet, kui pangavaluuta ühtib arvestusvaluutaga. Samuti ei tehta kirjet aruandlusvaluuta kohta, kui pangavaluuta ühtib aruandlusvaluutaga.

Samuti jagatakse välisvaluuta ümberarvutamise kanne pangakannete kohta leitud dimensioonide vahel. Jagamise alus on iga dimensiooni saldo. Näiteks kogu pangasaldo on 10 000, kuid äriüksuse 001 saldo on 4000 ja äriüksuse 002 saldo on 6000. Sellisel juhul sisestatakse 40 protsenti ümberarvutuse summast ümberarvutuskontole, millel on äriüksus 001, ja 60 protsenti sisestatakse ümberarvutuskontole, millel on äriüksus 002. Kui konto struktuuris ei ole äriüksust, sisestatakse kogu summa ümberarvutuskontole.

## <a name="reverse-foreign-currency-revaluation"></a>Välisvaluuta ümberarvutamise ümber pööramine

Kui peate ümberarvutuskande tühistama, valige lehe **Välisvaluuta ümberarvutamine** toimingupaanilt nupp **Tühista kanne**. Luuakse uue välisvaluuta ümberarvutamise ajalooline kirje, et säilitada ajalooline kontrolljälg ümberarvutamise toimumise või tühistamise ajast.

Mitme ümberarvutuse tühistamiseks peate tühistama kõige värskema ümberarvutuse. Seejärel jätkake vanemate ümberarvutuste tühistamist kuupäevalises järjestuses. Seejärel saate töödelda uusi ümberarvutusi tühistatud perioodide kohta.
