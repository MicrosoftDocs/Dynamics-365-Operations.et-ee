---
title: Juurdepääs eelvaatefunktsioonidele rakenduses Talent
description: Selles teemas kirjeldatakse, kuidas administraator saab lubada eelvaatefunktsioone, ja loetletakse funktsioone, mis on praegu eelvaate jaoks lubatud.
author: tracykeya
manager: AnnBe
ms.date: 04/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: trkeya
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.1.0, Talent April 2019 update
ms.openlocfilehash: 72e2a3c62c7aab0f5cf8900c540a22d91be00609
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517842"
---
# <a name="access-preview-features-in-talent"></a>Juurdepääs eelvaatefunktsioonidele rakenduses Talent

[!include[banner](../includes/banner.md)]

Pidevate tootevõimaluste levitamise osana tahame, et kliendid saaksid proovida uusi funktsioone niipea kui võimalik. Administraatorid saavad näha ja kasutada eelvaatefunktsioone oma keskkondades. Need funktsioonid on peaaegu valmis üldiseks kasutamiseks ja on läbinud põhjalikud kontrollid. Eelvaatefunktsioonide puhul soovime saada täiendavat kasutajate tagasidet ja kinnitust, enne kui funktsioonid kättesaadavaks teeme.

Selles teemas kirjeldatakse, kuidas administraator saab lubada eelvaatefunktsioone, ja loetletakse funktsioone, mis on praegu eelvaatena saadaval. Loendit värskendatakse, kui funktsioonid tehakse üldiselt kättesaadavaks ja/või lisatakse uusi eelvaatefunktsioone. Uute eelvaatefunktsioonide kohta ei saadeta teatisi. Kasutajad märkavad lihtsalt uusi funktsioone.

## <a name="enable-or-disable-preview-features"></a>Eelvaatefunktsioonide lubamine või keelamine

Eelvaatefunktsioonide lubamiseks või keelamiseks saate rakenduse Microsoft Dynamics 365 for Talent halduskeskuses kasutada sätet **Eelvaatefunktsioonid**. Vaikimisi on see säte välja lülitatud. Eelvaatefunktsioonide lubamine või keelamine sõltub keskkonnast.

> [!IMPORTANT]
> Kui lülitate sisse sätte **Eelvaatefunktsioonid**, siis lubate eelvaatefunktsioonid kõikidele teie organisatsiooni kasutajatele, kes on selles keskkonnas. Kui lülitate sätte välja, siis keelate eelvaatefunktsioonid ja teie kasutajatel pole nendele juurdepääsu. Rakenduses Talent on eelvaatefunktsioonidel piiratud tugi. Need võivad kasutada vähem privaatsus- ja turbemeetmeid ning pole hõlmatud rakenduse Talent teenindustaseme lepingus. Eelvaatefunktsioone ei tohi kasutada isikuandmete (st igasugused andmed, mis võimaldavad isikut tuvastada) ega muude andmete töötlemiseks, millele kehtivad seaduste või regulatsioonide järgmise nõuded.

### <a name="enable-or-disable-preview-features-for-your-organization"></a>Eelvaatefunktsioonide lubamine või keelamine teie organisatsiooni jaoks

#### <a name="attract"></a>Tähelepanu köitmine

1. Rakenduse Microsoft Dynamics 365 for Talent: Attract sisselogimine.
2. Valige ülemises parempoolses nurgas olevast menüüst **Seadistus** (hammasratta sümbol) suvand **Administraatori sätted**.
3. Valige vahekaardi **Funktsioonide haldus** suvandi **Eelvaatefunktsioonid** kõrval olev suvand nii, et see muutuks siniseks.
4. Soovi korral saate sellel lehel olevaid spetsiifilisi funktsioone lubades/keelates juhtida üksikuid funktsioone.
5. Uute funktsioonide nägemiseks värskendage oma brauserit. (Sisselogitud kasutajad näevad uusi funktsioone, kui nad logivad uuesti sisse, või nad võivad uute funktsioonide kohe nägemiseks oma brauserit värskendada.)

#### <a name="core-hr"></a>Core HR

1. Logige sisse rakendusse Talent. Avaneb Inimressursside põhitööruum, milles saate teha järgmisi samme. 
2. Valige **Süsteemihaldus \> Lingid > Süsteemi parameetrid**.
3. Eelvaatefunktsioonide lubamiseks määrake lehe **Süsteemi parameetrid** vahekaardil **Eelvaatefunktsioonid** suvandi **Luba eelvaaterežiim kõigi kasutajate jaoks** väärtuseks **Jah**.

> [!NOTE]
> Eelvaatefunktsioonide keelamiseks järgige samu samme. Eelvaatefunktsioonide keelamisega võivad funktsioonid kasutajatele juurdepääsmatuks muutuda ja põhjustada tõrkeid nende funktsioonidega seostatud protsessides.

## <a name="features-that-are-currently-in-preview"></a>Praegused eelvaatefunktsioonid

### <a name="attract"></a>Tähelepanu köitmine

- **Tööks sobivad kandidaadid** – värbajad ja personalijuhid näevad hõlpsalt, millised kandidaadid kõikidest kandidaatidest võivad olla tööks kõige sobivamad. Viie parima kandidaadi kuvamise aluseks on nende CV/profiili sobivus töö kirjeldusega.
- **Sobivad tööd** – kandidaadid näevad nüüd neile nende CV/profiili ja töö kirjelduse põhjal sobivate muude tööde loendit.  Praegu kuvatakse see kandidaatidele pärast seda, kui nad on esitanud taotluse olla soovitatud muudeks võimalusteks.
- **EEO/OFCCP tugi** – uued tegevustüübid võimaldavad kasutada võrdsete tööhõivevõimaluste (Equal Employment Opportunity – EEO) ja USA föderaalse lepingute vastavusprogrammi (Office of Federal Contract Compliance Program – OFCCP) andmete kogumiseks kandidaadilt valmis vormi.  See on valmis vorm ja seda ei saa muuta.

    > [!NOTE]
    > Sisestatud tööd on nähtavad ainult klientidele, kes on tellinud ühe või rohkem LinkedIni tööloendite toodet. Muul juhul näevad kliendid tööd vaid siis, kui nad seda konkreetselt otsivad. Tööde sisestamine LinkedIni toimub viivitusega. Pärast rakendusest Attract töö postitamist võib aega minna paar tundi, enne kui see nähtavaks muutub.

- **Kandidaatide taotlused** – nii sisemised kui välised kandidaatid saavad nüüd esitada taotlusi tööde lehelt ja karjäärisaidilt.
- **Pakkumiste haldus** – kasutajad saavad nüüd luua pakkumiskirju mallidest, mis hõlmavad kohatäiteid. Kui kandidaadid jõuavad etappi Pakkumine, saavad värbajad ja personalijuhid kasutada tööriista Pakkumine, et valmistada ette kandidaadi ametlikku pakkumist mallide abil, saata pakkumist sisemiseks kinnitamiseks ja lõpuks saate pakkumine kandidaadile allkirjastamiseks. Aja jooksul lisatakse tööriistale Pakkumine mitmeid uusi võimalusi ja eelvaatefunktsiooni värskendatakse nende võimalustega, kui oleme valmis neid eelvaateks väljastama.
- **[Analüütilised aruanded](analytic-reports.md)** – värbamistöörühmad näevad ühe töö põhimõõdikuid töö analüüsiga või koondmõõdikutega kõigi tööde kohta analüüsi keskuses.

### <a name="core-hr"></a>Core HR

- **Avatud registreerimine** – eeliste avatud registreerimine võimaldab töötajatel lihtsa iseteeninduse kaudu eelistusi valida. Inimressursside administraatorid saavad kohandada eeliste avatud registreerimise korda ja kogemust oma organisatsiooni ja töötajate jaoks, kui kasutavad hõlpsasti järgitavat juhist.

## <a name="feedback"></a>Tagasiside

Soovime saada teilt tagasisidet eelvaatefunktsioonide kasutamise kohta olenemata sellest, kas see on hea või halb. Soovitame teil postitada tagasisidet nende või muude funktsioonide kasutamise kohta järgmistel saitidel.

- [Kogukonna foorum](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – sellel saidil on mitmeid ressursse ning kasutajad saavad arutada kasutusjuhtumeid, küsida küsimusi ja otsida kogukonnalt abi.
- Tooteideede pakkumiseks kasutage järgmisi saite. Andke meile teada funktsioonidest, mida soovite tootes näha, ja ka muudatustest, mida teie arvates oleks olemasolevates funktsioonides vaja.

    - [Attract Ideas](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Core HR](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)

Ärge kasutage tagasisides ega tootearvustustes isikuandmeid (igasugused andmed, mis võimaldavad isikut tuvastada). Kogutud teavet võidakse põhjalikumalt analüüsida ja seda ei kasutata kohalduvate isikuandmete kaitse seaduste järgi taotluste täitmiseks. Isikuandmetele, mida kogutakse eraldi nende programmidega, kehtib [Microsofti privaatsusavaldus](https://privacy.microsoft.com/privacystatement).

> [!TIP]
> Lisage see teema järjehoidjatesse ja kontrollige seda tihti, et olla kursis uusimate eelvaatefunktsioonidega, kui neid väljastame.
