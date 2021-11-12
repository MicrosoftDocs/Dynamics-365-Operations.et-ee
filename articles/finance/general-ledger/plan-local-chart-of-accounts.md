---
title: Kohalike kontoplaanide planeerimine
description: See teema annab teavet, mis aitab teil kontoplaani planeerida, kui teil on nõuded oma organisatsiooni seaduslike/kohalike nõuetega.
author: veneva
ms.date: 10/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts, LedgerConsolidateAccountGroup, MainAccountConsolidateAccount, DimensionDetails, MainAccountDetails
ROBOTS: ''
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.tgt_pltfrm: ''
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.search.industry: ''
ms.author: veneva
ms.search.validFrom: 10/07/2021
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a99e4ef3355188f574930c1d885e53fcb3134ad1
ms.sourcegitcommit: c4500b626667185643b3a2e7fc3a004d42198d07
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/29/2021
ms.locfileid: "7725171"
---
# <a name="plan-your-local-chart-of-accounts"></a>Kohalike kontoplaanide planeerimine

[!include [banner](../includes/banner.md)]

See teema annab teavet, mis aitab teil kontoplaani planeerida, kui teie organisatsioonis on juriidilised isikud, kes peavad vastama konkreetsetele lokaadidele, kus neil ärisuhted on. Selles teemas kasutatakse kontoplaanide kirjeldamiseks järgmisi tingimusi:

- **Globaalne** – kontoplaan, mida organisatsioon globaalselt kasutab. Enamasti konsolideerite te sellele kontoplaanile.
- **Kohalik** – kontoplaan, mida konkreetses riigis või regioonis kasutavad juriidilised isikud.
- **ühiskasutuses** – kontoplaan, mida saab kasutada rohkem kui üks juriidiline isik. Nii globaalset kontoplaani kui ka kohalikke kontoplaane saab jagada.

Saate luua ja jagada mitut kontoplaani. Ühiskasutusega kontoplaani saab kasutada rohkem kui üks juriidiline isik, kuid igale juriidilisele isikule saab määrata ainult ühe kontoplaani. Kontoplaan, mida juriidiline isik kasutab, on määratletud lehel **Pearaamat**.

Kontoplaani kujundades on paljude organisatsioonide eesmärk luua globaalne kontoplaan. Ühiskasutuses kontoplaan võimaldab luua globaalse kontoplaani. Üksiku kontoplaani loomisel ja kasutamisel on omad eelised. Näiteks on haldus ja juhtimine, hooldus ja aruandlus lihtsamad.

Enamik organisatsioone eelistab globaalset kontoplaani ja see on lihtsaim juurutamise tüüp. Sellest hoolimata nõuavad mõned juriidilised isikud järgmistel põhjustel kohalikku kontoplaani:

- Kohalikud seadusejärgsed nõuded
- Kohaliku raamatupidamisstandardi nõuded
- Tööstuse nõuded
- Ettevõttepõhise aruandluse ja analüüsi nõuded

Kui teie organisatsioon nõuab, et juriidiline isik kasutaks kohalikku kontoplaani, on selle rakendamiseks kaks võimalust:

- Määrake globaalne kontoplaan ja määratlege muud kohalikele nõuetele vastamise vahendid.
- Määrake juriidilisele isikule kohalik kontoplaan ja määratlege seosed globaalse kontoplaaniga.

Organisatsiooni struktuur ja aruandlusstruktuur määravad kasutatava suvandi.

[![Diagramm, mis näitab, kuidas organisatsiooni struktuur määratleb, kas kasutada globaalset või kohalikku kontoplaani](./media/local-chart-of-accounts-diagram.png)](./media/local-chart-of-accounts-diagram.png)

Kui globaalne kontoplaan on määratud juriidilisele isikule, on kohalike aruandlusnõuete täitmiseks saadaval järgmised valikud:

- Tehke lokaalne konsolideerimine.
- Kasutage finantsdimensiooni kohaliku kontoplaani jälgimiseks.
- Looge globaalses kontoplaanis kohalikud põhikontod.
- Tehke välist vastendamist kohaliku kontoplaaniga.

Kui kohalik kontoplaan on määratud juriidilisele isikule, on kohalike aruandlusnõuete täitmiseks praegu saadaval ainus võimalus ülemaailmne konsolideerimine.

## <a name="global-chart-of-accounts-assigned-to-a-legal-entity"></a>Juriidilisele isikule määratud globaalne kontoplaan

Kui peate globaalse kontoplaani määrama juriidilisele isikule, on süsteemi konfigureerimiseks saadaval neli eelnevalt kirjeldatud võimalust. Kõigi nelja valiku puhul konfigureeritakse üks kontoplaan ja lingitakse iga **pearaamatu** lehel oleva juriidilise isikuga. Iga valik kasutab siis lokaliseerimisnõuete täitmiseks erinevat lähenemist. Järgmistes jaotistes antakse välja kõrgema taseme etapid süsteemi konfigureerimiseks lokaliseerimisnõuete jaoks. Samuti kirjeldavad need iga suvandi eeliseid ja puudusi.

### <a name="do-local-consolidation"></a>Tehke lokaalne konsolideerimine

Kohalik konsolideerimine on soovitatav lähenemine kohaliku kontoplaani nõuete täitmiseks ja selleks otstarbeks loodud süsteemifunktsiooni kasutamine.

#### <a name="set-up-consolidation-for-a-local-chart-of-accounts"></a>Kohaliku kontoplaani konsolideerimise seadistamine

1. Looge üks globaalne kontoplaan, mis sisaldab kõiki vajalikke põhikontosid.
2. Määrake igale juriidilisele isikule **pearaamatu** lehel globaalne kontoplaan.
3. Looge iga vajaliku lokaliseerimise jaoks konsolideeriv juriidiline isik.
4. Järgige üht neist sammudest.

    - Kui on vaja ainult ühte lokaliseerimist, konfigureerige konsolideerimiskonto **põhikonto** lehel või kasutage **konsolideerimisgruppe** ja **täiendavaid konsolideerimiskonto** lehekülgi.
    - Kui on vaja rohkem kui ühte lokaliseerimist või kui nii konto number kui ka konto nimi vajavad tõlget, kasutage lokaliseerimisnõudeid kajastamiseks **konsolideerimisgruppe** ja **täiendavaid konsolideerimiskonto** lehekülgi.

5. Käivitage konsolideerimisprotsess, et muuta väärtus allika juriidiliselt isikult, mis kasutab globaalset kontoplaani konsolideeritud ettevõtteks, mis kasutab kohalikku kontoplaani.

#### <a name="advantages"></a>Eelised

- See lähenemine pakub järjepidevat viisi organisatsiooniga töötamiseks.
- Üks kohaliku ametikoha tõlge on tehtud.
- Selline lähenemine toetab nii põhikonto ID kui ka iga põhikonto nime tõlget.
- See toetab mitut lokaliseerimist.

#### <a name="disadvantages"></a>Puudused

- Luuakse täiendav konsolideeritud ettevõte.
- Täiendav konsolideeritud protsess on lõpetatud.
- Selline lähenemine saab lokaliseeritud diagrammi kohta aru saada alles pärast konsolideerimisprotsessi lõpetamist.

### <a name="use-a-financial-dimension-to-track-the-local-chart-of-accounts"></a>Kasutage finantsdimensiooni kohaliku kontoplaani jälgimiseks

See lähenemine kasutab finantsdimensiooni, kus finantsdimensiooni väärtused tähistavad kohalikke põhikontosid, mis on lokaliseerimiseks vajalikud. See toimib hästi, kui nõutav on ainult üks lokaliseerimine. Kuid see on vähem kasutatav, kuna lisate rohkem lokaliseerimise ja finantsdimensioone.

#### <a name="set-up-a-financial-dimension-for-a-local-chart-of-accounts"></a>Seadistage kohaliku kontoplaani finantsmõõde

1. Looge üks globaalne kontoplaan, mis sisaldab kõiki vajalikke põhikontosid.
2. Määrake igale juriidilisele isikule **pearaamatu** lehel globaalne kontoplaan.
3. Looge finantsdimensioon mis esindab kohalikku kontoplaani.
4. Looge finantsdimensiooni väärtused, mis esindavad põhikontosid kohalikus kontoplaanis.
5. Värskendage konto struktuuri nii, et see hõlmab "kohalikku kontoplaani" finantsdimensiooni.
6. Veenduge, et "kohaliku kontoplaani" finantsdimensioonil oleks alati väärtus ja et sel ei oleks lubatud tühi väärtus. Kaaluge tuletatud dimensioonide või fikseeritud dimensioonide kasutamist.
7. Looge finantsdimensiooni kogum, kus "kohalik kontoplaan" finantsdimensioon on esimene valitud finantsdimensioon. Rahalise dimensioonikogumit saab kasutada proovibilansi loomisel.

#### <a name="advantages"></a>Eelised

- Kandetasemel on nii globaalsete kui ka kohalike kontoplaanide põhikontod. Põhikonto on globaalne ja finantsdimensiooni väärtus on kohalik.
- See lähenemine pakub reaalajas aruandlust ja vaateid nii globaalsest finantspositsioonist kui ka kohalikust finantspositsioonist.

#### <a name="disadvantages"></a>Puudused

- Kui pearaamatu parameetrites on **Väärtused summakonto jaoks** välja väärtuseks seatud **Arvestuse jaotused**, on finantsdimesnsioonid, mis esindavad kulu/vara/tulu põhikontot, müügireskontro ja ostureskontro summakonto puhul valesti. Soovitame selle välja seada lähtedokumendiks, et tagada õigete finantsdimensiooni väärtuste kasutamine.
- Kui nõutavad on paljud kohalikud kontoplaanid ja kõigil nende puhul kasutatakse üht finantsdimensiooni, võib kasutatud finantsdimensiooni väärtuste loend muutuda pikaks ja raskeks.
- Kui nõutavad on paljud kohalikud kontoplaanid ja iga konto tähistamiseks kasutatakse eraldi finantsdimensiooni, võib finantsdimensioonide ja finantsdimensioonide kogumite lisamist mõjutada süsteemi kasutatavust ja jõudlust.
- Soovitame teil hoolikalt järele vaadata rahalisi dimensioone, mida vajate, väärtuste arvu igaühele ja finantsdimensiooni kogumite arvu, sest kõik need tegurid võivad mõjutada süsteemi jõudlust.

### <a name="create-local-main-accounts-in-the-global-chart-of-accounts"></a>Looge globaalses kontoplaanis kohalikud põhikontod

*Kopeerimise redaktor küsib järgmist:* selle lähenemise puhul sisaldavad globaalse kontoplaani kohalikud põhikontod globaalsesse kontoplaani põhikontosid kohalikus kontoplaanis.

*Algne versioon:* Kohalikud põhikontod globaalses CoA lähenemisviisis on, et CoA põhikontod kaasatakse ülemaailmsesse CoA-sse.

*Kui see on nii:* Sel juhul kohalikud põhikontod kohalikus kontoplaanis on lisatud globaalsesse kontoplaani.


#### <a name="set-up-local-main-accounts-in-the-global-chart-of-accounts"></a>Seadistage kohalikud põhikontod globaalses kontoplaanis

1. Looge üks kontoplaan, mis hõlmab nii globaalse kontoplaani kui ka kohaliku kontoplaani põhikontosid.
2. Määrake igale juriidilisele isikule **pearaamatu** lehel globaalne kontoplaan.
3. Looge kontoplaanis summakontod, et summeerida sama eesmärki tähistavad põhikontod.
4. Looge igale kohalikule kontole juriidiline isik, et vältida teistest juriidilistest isikutest pärit kandeid, mille jaoks kohalik konto ei olnud mõeldud.
5. Looge igale globaalsele kontole juriidiline isik, et vältida kannete lokaliseerimise juriidilistest isikutest pärit kandeid.

#### <a name="advantages"></a>Eelised

- Nii globaalse finantspositsiooni kui ka kohaliku finantspositsiooni reaalajas vaade on saadaval kindlates aruannetes ja süsteemi kindlates vaadetes (nt bilansi finantsaruanne). Sellele pääseb juurde ka summakonto **Periood** nupu abil.
- Teil ei ole pearaamatukontos täiendavat segmenti.

#### <a name="disadvantages"></a>Puudused

- Konto kogukasutus ja nähtavus on piiratud. Näiteks ei ole kogusummade kontod **proovibilansi** loendilehel nähtavad.
- Hooldus nõuab lisakoormust.
- Finantsaruannete loomine nõuab täiendavat käsitsi sisestamist.

### <a name="do-external-mapping-to-the-local-chart-of-accounts"></a>Tehke välist vastendamist kohaliku kontoplaaniga

Globaalse kontoplaani väljaminek eeldab, et haldate vastendamist ja lokaliseerimist väljaspool süsteemi. Selles lähenemises loote rakenduses Microsoft Dynamics 365 Finance lihtsalt ühe globaalse kontoplaani ja käsitlete nõudeid väljaspool süsteemi.

#### <a name="set-up-external-mapping-to-a-local-chart-of-accounts"></a>Seadistage väline vastendamine kohaliku kontoplaaniga

1. Looge üks globaalne kontoplaan, mis sisaldab kõiki vajalikke põhikontosid.
2. Määrake igale juriidilisele isikule **pearaamatu** lehel globaalne kontoplaan.
3. Tehke vastendamine kohaliku kontoplaaniga väljaspool Finance'i.

#### <a name="advantages"></a>Eelised

- See lähenemine pakub järjepidevat viisi organisatsiooniga töötamiseks.

#### <a name="disadvantages"></a>Puudused

- Ühtegi kohalikku aruandlust pole süsteemist saadaval.
- Selline lähenemine on tõenäoline veale finantsaruannete loomisel.

## <a name="local-chart-of-accounts-assigned-to-legal-entity"></a>Juriidilisele isikule määratud kohalik kontoplaan

Kui teie organisatsioon otsustab mitte kasutada globaalset kontoplaani juriidiliste isikute lõikes, luuakse igale kordumatule kohalikule kontoplaanile eraldi kontoplaan. Iga juriidiline isik on seejärel seotud vastava kontoplaaniga **Pearaamat** lehel.

### <a name="do-global-consolidation"></a>Tehke globaalne konsolideerimine

Selle lähenemise puhul kasutatakse konsolideeritud ettevõtet iga lähteettevõtte saldode kokku kogumiseks ja kombineerimiseks ühendatud globaalsesse kontoplaani konsolideerimisettevõttes. Selline lähenemine nõuab, et säilitate iga kohaliku kontoplaani vastendamise konsolideeritud ettevõttes globaalse kontoplaaniga.

#### <a name="set-up-global-consolidation"></a>Seadistage globaalne konsolideerimine

1. Looge eraldi kontoplaan igale juriidilisele isikule, kelle kontoplaanil on erinev kohalik kontoplaan. Kui mis tahes juriidilisel isikul on sama kohalik kontoplaan, on vaja ainult üht kohalikku kontoplaani ja seda saab jagada.
2. Määrake igale juriidilisele isikule **pearaamatu** lehel vastav kontoplaan.
3. Valikuline: looge kontoplaan globaalse kontoplaani jaoks iga konsolideeritud ettevõtte jaoks, kus on teine globaalne kontoplaan.
4. Looge konsolideeriv juriidiline isik iga nõutud konsolideerimistaseme jaoks ja määrake lehel **Pearaamat** sobiv kontoplaan.
5. Järgige üht neist sammudest.

    - Kui on vaja ainult ühte konsolideerimist, konfigureerige konsolideerimiskonto **põhikonto** lehel.
    - Kui on vaja rohkem kui ühte lokaliseerimist või kui nii konto number kui ka konto nimi vajavad tõlget, kasutage lokaliseerimisnõudeid kajastamiseks **konsolideerimisgruppe** ja **täiendavaid konsolideerimiskonto** lehekülgi.

6. Käivitage konsolideerimisprotsess saldode ülekandmiseks kohalikelt juriidilistelt isikutelt konsolideeritud juriidilisele isikule. See konsolideeritud juriidiline isik kasutab konsolideerimiskontosid, mille määratlesid sammus 5.

#### <a name="advantages"></a>Eelised

- Kohaliku raamatupidamise standardivormingut rakendatakse omalt.
- Selline lähenemine annab kohalikule finantsmeeskonnale lihtsama tööviisi.

#### <a name="disadvantages"></a>Puudused

- Globaalse positsiooni reaalajas vaade pole saadaval.
- Konsolideerimisprotsessi võidakse käivitada sagedamini.

## <a name="additional-resources"></a>Lisaressursid

- [Kontoplaanide plaanimine](plan-chart-of-accounts.md)
- [Pearaamatute konfigureerimine](configure-ledger.md)
- [Finantsdimensioonid ja sisestamine](Default-dimensions.md#balancing-dimension)
- [Finantsdimensioonikomplektid](financial-dimension-sets.md)
- [Konsolideerimise ja eemaldamise ülevaade](../budgeting/consolidation-elimination-overview.md)
- [Konsolideerimiskonto grupid ja täiendavad konsolideerimiskontod](../budgeting/consolidation-account-groups-consolidation-accounts.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
