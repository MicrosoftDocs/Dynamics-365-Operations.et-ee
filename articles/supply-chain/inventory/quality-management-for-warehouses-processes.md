---
title: Kvaliteedijuhtimine laoprotsesside jaoks
description: Teema annab teavet funktsiooni „Kvaliteedijuhtimine laoprotsesside jaoks” kohta. See funktsioon laiendab kvaliteedijuhtimise võimalusi ja võimaldab kasutajatel täpsema laohalduse abil kauba valimi juhtelemendid lao vastuvõtmisprotsessi integreerida.
author: Henrikan
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-02
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 79eb7d750869ef365ad117ecc024afc8db2edbf7
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348825"
---
# <a name="quality-management-for-warehouse-processes"></a>Kvaliteedijuhtimine laoprotsesside jaoks

Funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ võimaldab teil täpsema laohalduse abil kauba valimi juhtelemendid lao vastuvõtmisprotsessi integreerida. Laotöid saab automaatselt luua, et teisaldada varusid kvaliteedikontrolli asukohta protsendi või fikseeritud koguse põhjal või iga *n*-inda litsentsiplaadi põhjal. Pärast kvaliteettellimuse lõpule viimist saab luua automaatselt töid varude järgmisesse asukohta teisaldamiseks protsessis, sõltuvalt kvaliteedikontrolli tulemustest.

Funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ laiendab põhilise kvaliteedijuhtimise funktsiooni võimalusi. See annab võimaluse luua kvaliteedikontrolli asukohta saadetavate varude jaoks kvaliteettellimusi, kuigi need pole alati kohustuslikud. Seetõttu on tulemuseks lihtne kvaliteedikontrolli protsess, mis põhineb laotööl.

## <a name="turn-on-the-quality-management-for-warehouse-processes-feature"></a>Funktsiooni „Kvaliteedijuhtimine laoprotsesside jaoks” sisselülitamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Kvaliteedijuhtimine laoprotsesside jaoks*

## <a name="key-benefits"></a>Peamised eelised

Funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ loob automaatselt töö vastuvõtmisprotsessi osana, et teisaldada kvaliteedikontrolli jaoks vajalik kogus varusid kvaliteedikontrolli asukohta. Kui saadud kogus ületab kvaliteedikontrolli jaoks vajaliku koguse (vastavalt kauba valimi seadistusele), teisaldatakse liigne kogus saabumisasukohta, mis on määratletud asukohakorralduse seadistuses. Pärast kvaliteettellimuse kinnitamist luuakse automaatselt töö, et liigutada kvaliteettellimuse kogus kinnitamise tulemuse ja asukohakorralduse seadistuse põhjal uude sissetuleku või tagastusasukohta. Sellise töö automaatne loomine, mis hõlmab ainult kogust, mis tuleb teisaldada kvaliteedikontrolli asukohta või sealt välja, loob integreeritud protsessi kogemuse.

> [!NOTE]
> Kui funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ on sisse lülitatud, saate siiski manuaalset protsessi kasutada. Manuaalses protsessis kasutatakse varude liikumist ja liikumist malli alusel, et laotöötaja saaks käivitada laotöö loomise varude teisaldamiseks kvaliteedikontrolli asukohast uude asukohta. Te saate jätkuvalt seadistada sissetuleku asukoha korralduse, mis teisaldab kõik varud vastuvõtvast asukohast üle kvaliteedikontrolli asukohta, võtmata arvesse kauba valimi seadistust.

## <a name="quality-management-and-the-quality-management-for-warehouse-processes-feature"></a>Kvaliteedijuhtimine ja funktsioon „Kvaliteedijuhtimine laoprotsesside jaoks”

Kui funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ on sisse lülitatud, muudab see peamiste laohaldus- ja kvaliteedijuhtimise üksuste seadistust. Järgmisel joonisel on näha ülevaade üksustest, mis võimaldavad laoprotsesside jaoks kvaliteettellimusi luua. Sulgudes olev tekst näitab soovitatavaid tegevusi, kui kvaliteedijuhtimist rakendati enne funktsiooni _Kvaliteedijuhtimine laohaldusprotsesside jaoks_ sisselülitamist.

![Kvaliteedijuhtimise üksused.](media/quality-management-entity-diagram.png "Kvaliteedijuhtimise üksused")

## <a name="enablers-the-quality-item-sampling-and-quality-order-work-order-types"></a>Aktiveerijad: kauba kvaliteedivalimi ja kvaliteettellimuse töökäsu tüübid

Funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ toob juurde kaks töökäsu tüüpi, mille abil saab töid luua.

- **Kauba kvaliteedivalim** – seda töökäsu tüüpi kasutatakse töö loomiseks, et teisaldada registreeritud varud kvaliteedikontrolli.
- **Kvaliteettellimus** – seda töökäsu tüüpi kasutatakse sellise töö loomiseks, mis teisaldab varud asukohakorralduse seadistuse põhjal kvaliteedikontrollist uude asukohta.

### <a name="work-classes-location-directives-and-work-templates"></a>Töö klassid, asukohakorraldused ja töömallid

Töökäsu tüüpe _Kauba kvaliteedivalim_ ja _Kvaliteettellimus_ kasutavad asukohakorraldused, töö klassid ja töömallid.

Enne laotöö automaatset loomist varude teisaldamiseks kvaliteedikontrolli, peate oma süsteemi seadistamiseks järgima järgmisi samme.

1. Looge eraldi töö klassid töökäsu tüüpide _Kauba kvaliteedivalim_ ja _Kvaliteettellimus_ jaoks. Sel viisil tagate, et kahe töökäsu tüübi põhjal saab automaatselt luua sobiva töö ja seda tööd saab seejärel käitada mobiilirakenduse Warehouse Management abil.
1. Seadistage iga töökäsu tüübi jaoks töömall.

    - Seadistage töömall, mis kasutab töökäsu tüüpi _Kauba kvaliteedivalim_, et teisaldada registreeritud varud automaatselt kvaliteedikontrolli asukohta.
    - Seadistage töömall, mis kasutab töökäsu tüüpi _Kvaliteettellimus_, et teisaldada varusid kvaliteedikontrolli asukohast pärast kvaliteedikontrolli lõpule viimist.

1. Seadistage igale töökäsu tüübile asukohakorraldused, mis rakendavad õigeid kvaliteedikontrolli asukohti, kuhu varud tuleks teisaldada. Pärast kvaliteedikontrolli lõpule viimist tagab töökäsu tüübi _Kvaliteettellimus_ asukohakorraldus uue sihtkoha valimise, et varud viidaks kvaliteedikontrolli asukohast välja.
1. Seadistage asjakohased mobiilse seadme menüüelemendid, et toetada vastuvõetud varude liikumist kvaliteedikontrolli asukohta ning varude, mis läbivad või ei läbi kvaliteedikontrolli, liikumist kvaliteedikontrolli asukohast üle uude asukohta.

Üksikasjaliku juhise, milles on näha, kuidas seadistust lõpule viia, leiate [näidisstsenaariumist](#example-scenario) selle teema lõpus.

## <a name="enable-a-warehouse-for-quality-management"></a>Lubage ladu kvaliteedijuhtimise jaoks

Enne kui funktsiooni _Kvaliteedijuhtimine laoprotsesside jaoks_ saab rakendada kindla lao puhul, peate järgima järgmisi samme, et teha funktsioon selle lao jaoks kättesaadavaks.

1. Avage **Laohaldus \> Seadistus \> Ladu \> Laod**.
1. Valige ladu, et lubada kvaliteedijuhtimine.
1. Seadke kiirkaardil **Ladu** valiku **Luba kvaliteettellimused laoprotsesside jaoks** väärtuseks _Jah_. (Pange tähele, et seda valikut saab seadistada väärtusele _Jah_ ainult ladude puhul, mis kasutavad laohaldusprotsesse.)

Kui suvand **Luba kvaliteettellimused laoprotsesside jaoks** on seatud väärtusele _Jah_, kontrollib kvaliteediseose seadistus, kas funktsiooni _Kvaliteedijuhtimine laoprotsesside jaoks_ rakendatakse tegelikult valitud lao puhul. Te saate suvandi igal ajal väärtusele _Ei_ muuta. Sel juhul ei rakendata funktsiooni enam lao puhul, sõltumata kvaliteediseose seadistusest.

## <a name="quality-control"></a>Kvaliteedikontroll

Funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ kontrollib mitut põhilist kvaliteediseoste ja kauba valimi sätet.

### <a name="quality-associations"></a>Kvaliteediseosed

Iga [kvaliteediseose kirje](enable-quality-management.md) määrab testide komplekti, vastuvõetava kvaliteeditaseme (AQL) ning valimi plaani, mida rakendada loodud kvaliteettellimustele. Kvaliteediseose kirje seadistamiseks tehke järgmist.

1. Avage **Varude haldus \> Seadistus \> Kvaliteedijuhtimine \> Kvaliteediseosed**.
1. Looge või valige kvaliteediseose kirje kauba või grupi jaoks, millega töötate, või kõigi kaupade jaoks.
1. Seadke kiirkaardil **Tingimused** väli **Kohaldatav lao tüüp** ühele järgmistest väärtustest.

    - **Kvaliteedijuhtimine ainult laoprotsesside jaoks** – funktsiooni _Kvaliteedijuhtimine laoprotsesside jaoks_ aktiveerimine. Selle väärtuse saate valida ainult juhul, kui viite tüüp on kas *Ost* või *Tootmine*.
    - **Kõik** – funktsiooni _Kvaliteedijuhtimine laoprotsesside jaoks_ inaktiveerimine. Valige see väärtus kõigi viite tüüpide jaoks, välja arvatud *Ost* ja *Tootmine*.

> [!NOTE]
> Funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ rakendub vaid siis, kui lähtedokumendi real olev kaup kasutab täpsemaid laohaldusprotsesse ja kui suvand **Luba kvaliteettellimused laoprotsesside jaoks** on lähtedokumendi real oleva lao puhul seatud väärtusele _Jah_.

Iga kauba registreerimise korral (või lõpetatuna kinnitamise järel) määrab süsteem, millised kvaliteediseosed sellele rakenduvad.

Kui funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ on sisse lülitatud, siis lisatakse kohaldatav lao tüüp loogiliselt kvaliteediseose otsinguhierarhia neljandasse otsingugruppi. Järgmine tabel näitab otsinguhierarhia loogilist esitust.

| Otsingugrupp | Kirjeldus |
|---|---|
| Grupp 1 | Võrrelge iga kvaliteediseose puhul suvandite **Viite tüüp**, **Sündmuse tüüp** ja **Täitmise vaste** väärtuseid kaubaga. Kui leiate lähtedokumendi realt vaste, liikuge edasi 2. gruppi. |
| Grupp 2 | Võrrelge iga kvaliteediseose puhul suvandi **Kauba kood** väärtust (_Tabel_, _Grupp_ või _Kõik_) kaubaga. _Tabel_ on täpsem kui _Grupp_ ja _Grupp_ on täpsem kui _Kõik_. Kui leiate suvandile _Tabel_ vaste (kindel kaup), liikuge 3. gruppi. Kui suvandil _Tabel_ pole vastet, otsige vastet suvandile _Grupp_. Kui suvandil _Grupp_ pole vastet, kehtib _Kõik_. Kui leiate vaste, liikuge 3. gruppi. |
| Grupp 3 | Võrrelge iga kvaliteediseose puhul suvandite **Konto kood** ja **Ressursi kood** väärtusi kaubaga. Rakendatav loogika meenutab loogikat, mida rakendatakse suvandi **Kauba kood** väärtuse puhul. |
| Grupp 4 | Võrrelge iga kvaliteediseose puhul suvandi **Kohaldatav lao tüüp** väärtust (_Kvaliteedijuhtimine ainult laoprotsesside jaoks_ või _Kõik_) kaubaga. Kui suvand **Luba kvaliteettellimused laoprotsesside jaoks** on lähtedokumendil oleva lao puhul seatud väärtusele _Jah_ ning lähtedokumendi real olev kaup on seatud väärtusele _Kasuta laohaldusprotsesse_, rakendatakse nende mõlema olemasolu korral samal ajal nii seoseid, millel on vaste suvandile _Kvaliteedijuhtimine laoprotsesside jaoks_, kui ka seoseid, millel on vaste suvandile _Kõik_. Kui valiku **Luba kvaliteettellimused laoprotsesside jaoks** väärtus on lähtedokumendis oleva lao puhul seatud väärtusele _Ei_ ning lähtedokumenti real olev kaup on seatud väärtusele _Kasuta laohaldusprotsesse_, rakendatakse ainult kvaliteedijuhtimist. |

Näiteks olete määratlenud lao, kus suvand **Luba kvaliteettellimused laoprotsesside jaoks** on seatud väärtusele _Jah_, ning teil on kaks kvaliteediseost, mis on määratletud viite tüübi *Ost* jaoks: üks kõigi kaupade ja üks sündmuse tüübi *Registreerimine* jaoks. Ainus erinevus kahe kvaliteediseose vahel on suvandi **Kohaldatav lao tüüp** väärtus, mis on ühe kvaliteediseose puhul seatud väärtusele _Kõik_ ja teise puhul väärtusele _Kvaliteedijuhtimine ainult laoprotsesside jaoks_. Sellisel juhul on mõlemad kvaliteediseosed võrdselt spetsiifilised ja rakendada saab mõlemaid.

Kvaliteediseoste välja **Katsegrupp** väärtus on samuti oluline. See väli määratleb katseprotsessi, mida tuleb rakendada. Kui suvandi **Katsegrupp** väärtus on mõlema seose puhul sama, luuakse ainult üks kvaliteettellimus kvaliteediseose jaoks, mille suvandi **Kohaldatav lao tüüp** väärtus on _Kvaliteedijuhtimine ainult laoprotsesside jaoks_. Kui suvandi **Katsegrupp** väärtus pole mõlema seose puhul sama, luuakse kaks kvaliteettellimust. Esimene kvaliteettellimus luuakse kvaliteediseose jaoks, mille suvandi **Kohaldatav lao tüüp** väärtus on _Kvaliteedijuhtimine ainult laoprotsesside jaoks_. Teine kvaliteettellimus luuakse kvaliteediseose jaoks, mille suvandi **Kohaldatav lao tüüp** väärtus on _Kõik_.

> [!NOTE]
> Suvandi _Kvaliteedijuhtimine ainult laoprotsesside jaoks_ väärtus on täpsem kui _Kõik_, kui gruppide 1 ja 2 kvaliteediseoste kriteeriumid on samad ja kui katsegrupp on sama. Kaks kvaliteettellimust luuakse ainult siis, kui katsegrupid on erinevad.

#### <a name="reference-types"></a>Viitetüübid

Kui suvandi **Viite tüüp** väärtus on _Ost_ ja suvandi **Kohaldatav lao tüüp** väärtus on _Kvaliteedijuhtimine ainult laoprotsesside jaoks_, peab väli **Sündmuse tüüp** kiirkaardil **Protsess** olema seatud väärtusele _Registreerimine_. _Registreerimine_ on ainus toetatud sündmuse tüüp viite tüübi _Ost_ jaoks, kui kasutate funktsiooni _Kvaliteedijuhtimine laoprotsesside jaoks_.

#### <a name="quality-processing-policy"></a>Kvaliteedi töötlemise poliitika

Funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ võimaldab luua töid ainult kauba valimi põhjal. Seetõttu teeb see protsessi lihtsamaks. Varud, mille jaoks töö luuakse, sõltuvad kauba valimist, mis on seostatud kvaliteediseosega. Kui kasutatakse lihtsustatud protsessi, saab kvaliteediosakond luua vajaduse korral automaatselt kvaliteettellimuse pärast seda, kui töötaja on koguse kvaliteedikontrolli asukohta viinud.

Väli **Kvaliteeditöötluse poliitika** kiirkaardil **Kvaliteettellimuse protsess** kontrollib, kas kvaliteettellimus luuakse ka siis, kui kauba teisaldamiseks kvaliteedikontrolli asukohta luuakse töö. Seda välja saab seadistada väärtusele _Loo kvaliteettellimus_ või _Loo ainult töö_. Vaikeväärtus on _Loo kvaliteettellimus_.

> [!NOTE]
> Sõltumata sellest, kas loote kvaliteettellimusi käsitsi või automaatselt, loob süsteem automaatselt töö, et teisaldada kaubad kvaliteedikontrolli asukohast välja, kui kvaliteettellimus on märgitud kinnitatuks.

Kvaliteettellimuse töö loomine ei ole seotud kvaliteediseoste seadistusega. Kui süsteemis on töömall, mille suvandi **Töökäsu tüüp** väärtus on *Kvaliteettellimus*, ning päringukriteeriumid on selle töömalli puhul täidetud, käivitab kvaliteettellimuse kinnitamine kvaliteettellimuse töö loomise.

#### <a name="referenced-item-sampling"></a>Viidatud kauba valim

Iga kvaliteediseos peab viitama kauba valimile. Kauba valim määratleb kvaliteedikontrolli saadetava koguse. Seda saab seadistada nii, et see rakenduks ainult kvaliteediseoste puhul, mille suvandi **Kohaldatav lao tüüp** väärtus on _Kvaliteedijuhtimine ainult laoprotsesside jaoks_. Kui kauba valimi suvandi **Valimi ulatus** väärtus on _Koorem_ või _Saadetis_ või suvandi **Koguse spetsifikatsioon** väärtus on _Kogu litsentsiplaat_, saab kauba valimile viidata ainult kvaliteediseostega, mille **Kohaldatav lao tüüp** on _Kvaliteedijuhtimine ainult laoprotsesside jaoks_.

Kui määratlete kauba valimi, mis kasutab ainult kohaldatavat lao tüüpi _Kvaliteedijuhtimine ainult laoprotsesside jaoks_, kuvatakse tõrge, kui püüate sellele viidata kvaliteediseosest, mis ei kasuta funktsiooni _Kvaliteedijuhtimine laoprotsesside jaoks_.

> [!NOTE]
> Täielikku blokeerimist kasutavat kauba valimit ei toetata kvaliteediseoste puhul, mille väli **Kohaldatav lao tüüp** on seatud väärtusele _Kvaliteedijuhtimine ainult laoprotsesside jaoks_.

### <a name="item-sampling"></a>Kauba valim

Kauba valim kontrollib, kui tihti kaupu kvaliteedikontrolli saadetakse. Funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ lisab _kauba valimi ulatuse_ suvandi. Süsteem kasutab kauba valimi ulatust hindamiseks, kas ja kuidas tuleks kvaliteettellimusi ja/või kauba kvaliteedivalimi töid ja kvaliteettellimuse töid luua.

Kauba valimi seadistamiseks avage **Laohaldus \> Seadistus \> Kvaliteedikontroll \> Kauba valim** ning seadke välja **Valimi ulatus** väärtuseks üks järgmistest väärtustest.

- **Tellimus** – selle hindamine, kas ja kuidas tuleks kvaliteettellimusi ja/või kauba kvaliteedivalimi töid ja kvaliteettellimuse töid luua, toimub lähtedokumendi rea põhjal. See väärtus on vaikeväärtus ja kui see on valitud, toimib süsteem samamoodi nagu see toimib siis, kui funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ pole sisse lülitatud.
- **Koorem** – selle hindamine, kas ja kuidas luuakse kvaliteettellimus ja/või töö, toimub koormate põhjal. See väärtus on saadaval ainult siis, kui funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ on sisse lülitatud.
- **Saadetis** – selle hindamine, kas ja kuidas luuakse kvaliteettellimus ja/või töö, toimub saadetiste põhjal. See väärtus on saadaval ainult siis, kui funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ on sisse lülitatud.

> [!NOTE]
> Kui välja **Valimi ulatus** väärtuseks on seatud *Koorem* või *Saadetis*, siis kasutatakse koorma ja saadetise üksusi, kui need on saadaval. Kui need pole saadaval, kasutatakse tellimuse üksust.

Funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ lisab ka väärtuse *Kogu litsentsiplaat* väljale **Koguse spetsifikatsioon**. See väärtus toetab kvaliteettellimuse töö ja kauba kvaliteedivalimi töö loomist litsentsiplaatide põhjal. Selle väärtuse valimisel ilmnevad järgmised muudatused.

- Valik **Lõpeta loendamine kauba põhjal** ja väli **Iga n-inda litsentsiplaadi järel** muutuvad kiirkaardil **Protsess** kättesaadavaks.
- Väli **Väärtus** pole enam kiirkaardil **Valimi kogus** kättesaadav.
- Valikud **Värskendatud koguse kohta**, **Asukoht** ja **Litsentsiplaat** seatakse kõik väärtusele *Jah* ning sätteid ei saa muuta.

Valik **Lõpeta loendamine kauba põhjal** määrab, kas litsentsiplaatide arvu hinnatakse kauba või kõigi valimi ulatuses olevate kaupade põhjal. Tootevariante käsitletakse sama kaubana. See suvand kontrollib ka seda, kas litsentsiplaatide arv lähtestatakse iga kauba puhul.

Välja **Iga n-inda litsentsiplaadi järel** väärtus määrab, kui tihti luuakse kvaliteettellimusi registreeritud kaupade arvu silmas pidades. Näiteks saadab väärtus *3* iga kolmanda kauba kvaliteedikontrolli, alustades esimesest kaubast. Väärtus peab olema suurem kui 0 (null).

Kui töötajad saavad kaupu mobiilirakenduse Warehouse Management abil, kontrollib süsteem, kas kvaliteediseos on iga sissetuleva kauba puhul seadistatud. Kui kvaliteediseos on seadistatud, kasutab süsteem selle kvaliteediseose jaoks konfigureeritud kauba valimi kirjet, et määrata, kuidas luuakse kvaliteettellimusi, kauba kvaliteedivalimi töid ja ostutellimuse töid.

> [!NOTE]
> Kui kauba sissetulek registreeritakse veebikliendis (väikese registreerimislehe või ostutellimuse ridade puhul saabuva kauba töölehe abil), siis ei looda seadistusest olenemata ei kauba kvaliteedivalimi tööd ega ostutellimuse tööd. Selle asemel kasutatakse kvaliteediseosega sobivate kaupade puhul viidatud kauba valimit, et kontrollida ainult kvaliteettellimuste loomist.

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Kvaliteettellimuste automaatse genereerimise näited

Järgmistes näidetes on näha, kuidas kvaliteediseoste ja seostatud kauba valimi seadistus mõjutab kvaliteettellimuste loomist, kui välja **Kohaldatav lao tüüp** on seadistatud väärtusele _Kvaliteedijuhtimine ainult laoprotsesside jaoks_.

Kui valiku **Koguse spetsifikatsioon** väärtus on _Kogu litsentsiplaat_, siis kontrollib väli **Iga n-inda litsentsiplaadi järel**, milliste litsentsiplaatide jaoks luuakse kauba kvaliteedivalimi töö. Esimene litsentsiplaat läheb alati kvaliteedikontrolli ja seejärel määrab selle välja väärtus, et pärast esimest läheb kvaliteedikontrolli ka iga *n*-is litsentsiplaat.

Valiku **Viite tüüp** väärtus on järgmiste näidete puhul _Ost_ ja valiku **Sündmuse tüüp** väärtus on *Registreerimine*.

| Valimi ulatus | Koguse spetsifikatsioon | Värskendatud koguse kohta | Laoala dimensiooni kohta | Jaota arv kauba järgi | Iga n. litsentsiplaat | Tulemus |
|---|---|---|---|---|---|---|
| Tellimus | Täielik litsentsiplaat | Jah _(lukustatud / pole redigeeritav)_ | <p>Asukoht: jah</p><p>Litsentsiplaat: jah _(lukustatud / pole redigeeritav)_</p> | Ei | 3 | <p>**Tellimuse rea kogus: 100 EA**</p><ol><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 20 EA, LP1 jaoks<p>Kauba kvaliteedivalimi töö 20 EA jaoks</p><p>Kvaliteettellimus 1 20 EA jaoks</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 20 EA, LP2 jaoks<p>Ostutellimuse töö 20 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 20 EA, LP3 jaoks<p>Ostutellimuse töö 20 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 20 EA, LP4 jaoks<p>Kauba kvaliteedivalimi töö 20 EA jaoks</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 20 EA, LP5 jaoks<p>Ostutellimuse töö 20 EA jaoks (ladustamine)</p></li></ol> |
| Tellimus | Fikseeritud kogus = 1 | Jah | <p>Asukoht: jah</p><p>Litsentsiplaat: jah</p> | Ei | Pole kohaldatav | <p>**Tellimuse rea kogus: 100**</p><ol><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 20 EA, LP1 jaoks<p>Kauba kvaliteedivalimi töö 1 EA jaoks</p><p>Kvaliteettellimus 1 1 EA jaoks</p><p>Ostutellimuse töö 19 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 20 EA, LP2 jaoks<p>Kauba kvaliteedivalimi töö 1 EA jaoks</p><p>Kvaliteettellimus 1 1 EA jaoks</p><p>Ostutellimuse töö 19 jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 20 EA, LP3 jaoks<p>Kauba kvaliteedivalimi töö 1 EA jaoks</p><p>Kvaliteettellimus 1 1 EA jaoks</p><p>Ostutellimuse töö 19 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 20 EA, LP4 jaoks<p>Kauba kvaliteedivalimi töö 1 EA jaoks</p><p>Kvaliteettellimus 1 1 EA jaoks</p><p>Ostutellimuse töö 19 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 20 EA, LP5 jaoks<p>Kauba kvaliteedivalimi töö 1 EA jaoks</p><p>Kvaliteettellimus 1 1 EA jaoks</p><p>Ostutellimuse töö 19 EA jaoks (ladustamine)</p></li></ol> |
| Tellimus | Protsent = 10 | Ei | <p>Asukoht: ei</p><p>Litsentsiplaat: ei</p> | Ei | Pole kohaldatav | <p>**Tellimuse rea kogus: 100 EA**</p><ol><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 50 EA, LP1 jaoks<p>Kauba kvaliteedivalimi töö 10 EA jaoks</p><p>Kvaliteettellimus 1 10 EA jaoks</p><p>Ostutellimuse töö 40 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 50 EA, LP2 jaoks<p>Ostutellimuse töö 50 EA jaoks (ladustamine)</p></li></ol> |
| Laadi | Protsent = 5 | Jah _(lukustatud / pole redigeeritav)_ | <p>Asukoht: ei</p><p>Litsentsiplaat: ei</p> | Ei | Pole kohaldatav | <p>**Tellimuse rea kogus: 500 EA**</p><p>**Kaks koormat: esimene koorem 200 EA, teine koorem 300 EA**</p><ol><li>Registreeri sissetulek mobiilirakenduses Warehouse Management esimese koorma puhul 100 EA jaoks<p>Kauba kvaliteedivalimi töö 5 EA jaoks</p><p>Kvaliteettellimus 1 5 EA jaoks</p><p>Ostutellimuse töö 95 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management esimese koorma puhul 100 EA jaoks<p>Kauba kvaliteedivalimi töö 5 EA jaoks</p><p>Kvaliteettellimus 1 5 EA jaoks</p><p>Ostutellimuse töö 95 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management teise koorma puhul 300 EA jaoks<p>Kauba kvaliteedivalimi töö 15 EA jaoks</p><p>Kvaliteettellimus 1 15 EA jaoks</p><p>Ostutellimuse töö 285 EA jaoks (ladustamine)</p></li></ol> |
| Järjesta | Protsent = 10 | Jah | <p>Asukoht: jah</p><p>Litsentsiplaat: jah</p> | Ei | Pole kohaldatav | <p>**Tellimuse rea kogus: 100**</p><ol><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 50 EA, LP1 jaoks<p>Kauba kvaliteedivalimi töö 5 EA jaoks</p><p>Kvaliteettellimus 1 5 EA jaoks</p><p>Ostutellimuse töö 45 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 50 EA, LP2 jaoks<p>Kauba kvaliteedivalimi töö 5 EA jaoks</p><p>Kvaliteettellimus 1 5 EA jaoks</p><p>Ostutellimuse töö 45 jaoks (ladustamine)</p></li></ol> |
| Laadi | Täielik litsentsiplaat | Jah _(lukustatud / pole redigeeritav)_ | <p>Asukoht: jah</p><p>Litsentsiplaat: jah _(lukustatud / pole redigeeritav)_</p> | Ei | 3 | <p>**Kaks kaupa:**</p><ul><li>**Tellimuse rea kogus kauba A puhul: 120 EA (4 kaubaalust)**</li><li>**Tellimuse rea kogus kauba B puhul: 90 EA (3 kaubaalust)**</li></ul><p>**Üks koorem, kaks koormarida iga tellimuserea kohta**</p><ol><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 30 EA, LP1 jaoks<p>Kauba kvaliteedivalimi töö 30 EA jaoks</p><p>Kvaliteettellimus 1 30 EA jaoks</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 30 EA, LP2 jaoks<p>Ostutellimuse töö 30 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 30 EA, LP3 jaoks<p>Ostutellimuse töö 30 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 30 EA, LP4 jaoks<p>Kauba kvaliteedivalimi töö 30 EA jaoks</p><p>Kvaliteettellimus 1 30 EA jaoks</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba B, 30 EA, LP5 jaoks<p>Ostutellimuse töö 30 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba B, 30 EA, LP6 jaoks<p>Ostutellimuse töö 30 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 30 EA, LP7 jaoks<p>Kauba kvaliteedivalimi töö 30 EA jaoks</p><p>Kvaliteettellimus 1 30 EA jaoks</p></li></ol> |
| Laadi | Täielik litsentsiplaat | Jah _(lukustatud / pole redigeeritav)_ | <p>Asukoht: jah</p><p>Litsentsiplaat: jah _(lukustatud / pole redigeeritav)_</p> | Jah | 3 | <p>**Kaks kaupa:**</p><ul><li>**Tellimuse rea kogus kauba A puhul: 120 EA (4 kaubaalust)**</li><li>**Tellimuse rea kogus kauba B puhul: 90 EA (3 kaubaalust)**</li></ul><p>**Üks koorem, kaks koormarida iga tellimuserea kohta**</p><ol><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 30 EA, LP1 jaoks<p>Kauba kvaliteedivalimi töö 30 EA jaoks</p><p>Kvaliteettellimus 1 30 EA jaoks</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 30 EA, LP2 jaoks<p>Ostutellimuse töö 30 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 30 EA, LP3 jaoks<p>Ostutellimuse töö 30 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 30 EA, LP4 jaoks<p>Kauba kvaliteedivalimi töö 30 EA jaoks</p><p>Kvaliteettellimus 1 30 EA jaoks</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba B, 30 EA, LP5 jaoks<p>Kauba kvaliteedivalimi töö 30 EA jaoks</p><p>Kvaliteettellimus 1 30 EA jaoks</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba B, 30 EA, LP6 jaoks<p>Ostutellimuse töö 30 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 30 EA, LP7 jaoks<p>Ostutellimuse töö 30 EA jaoks (ladustamine)</p></li></ol> |
| Laadi | Protsent = 10 | Jah _(lukustatud / pole redigeeritav)_ | <p>Asukoht: ei</p><p>Litsentsiplaat: ei</p> | Ei | Pole kohaldatav | <p>**Tellimuse rea kogus: 100 EA**</p><p>**Koormaid ei looda. Rakendatakse tellimuse ulatust.**</p><ol><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 50 EA, LP1 jaoks<p>Kauba kvaliteedivalimi töö 5 EA jaoks</p><p>Kvaliteettellimus 1 5 EA jaoks</p><p>Ostutellimuse töö 45 EA jaoks (ladustamine)</p></li><li>Registreeri sissetulek mobiilirakenduses Warehouse Management kauba A, 50 EA, LP2 jaoks<p>Kauba kvaliteedivalimi töö 5 EA jaoks</p><p>Kvaliteettellimus 1 5 EA jaoks</p><p>Ostutellimuse töö 45 EA jaoks (ladustamine)</p></li></ol> |

Kui töötaja kinnitab ühe eelmises tabelis toodud kvaliteettellimustest, loob süsteem automaatselt kvaliteettellimuse töö, et teisaldada varud kvaliteedikontrolli asukohast asukohta, mis on määratletud töökäsu tüübi _Kvaliteettellimus_ asukohakorralduses. Selleks otstarbeks saate seadistada mis tahes asukoha, nt tagastus- või ladustamisasukoha, sõltuvalt kvaliteettellimuse katsetulemusest. Selle seadistuse näite leiate selle teema lõpust jaotisest [näidisstsenaarium](#example-scenario).

Te saate juba kinnitatud kvaliteettellimuse uuesti avada, eeldusel, et varude kvaliteedikontrolli asukohast teisaldamisega seotud kvaliteettellimuse töö sätte **Töö olek** väärtus pole *Suletud* või *Pooleli*.

## <a name="process-insights-when-multiple-quality-associations-coexist"></a>Ülevaadete töötlemine mitme kvaliteediseose korral

Ühe lähtedokumendi rea puhul saab määratleda ja rakendada rohkem kui üht kvaliteediseost ning välja **Kohaldatav lao tüüp** saab seadistada mõne kvaliteediseose puhul väärtusele _Kvaliteedijuhtimine ainult laoprotsesside jaoks_ ja teiste puhul väärtusele _Kõik_.

Järgmises näites on suvandi **Viite tüüp** väärtus _Ost_.

1. Esimene kvaliteediseos on seadistatud järgmisel viisil.

    - **Kohaldatav lao tüüp:** *Kvaliteedijuhtimine ainult laoprotsesside jaoks*
    - **Kauba kood:** *A0001*
    - **Konto kood:** *Kõik*
    - **Katsegrupp:** *Raamistus*
    - **Kauba valim:** *5 tk*

1. Teine kvaliteediseos on seadistatud järgmisel viisil.

    - **Kohaldatav lao tüüp:** *Kõik*
    - **Kauba kood:** *Kõik*
    - **Konto kood:** *Kõik*
    - **Katsegrupp:** *Raamistus*
    - **Kauba valim:** *1 tk*

1. Kolmas kvaliteediseos on seadistatud järgmisel viisil.

    - **Kohaldatav lao tüüp:** *Kvaliteedijuhtimine ainult laoprotsesside jaoks*
    - **Kauba kood:** *Kõik*
    - **Konto kood:** *104*
    - **Kastegrupp:** *Takistus*
    - **Kauba valim:** *Iga teine litsentsiplaat* (see säte tähendab, et kvaliteettellimuse loovad esimene, kolmas, viies jne vastuvõetud litsentsiplaat.)

1. Neljas kvaliteediseos on seadistatud järgmisel viisil.

    - **Kohaldatav lao tüüp:** *Kõik*
    - **Kauba kood:** *Kõik*
    - **Konto kood:** *Kõik*
    - **Kastegrupp:** *Takistus*
    - **Kauba valim:** *5 tk*

1. Viies kvaliteediseos on seadistatud järgmisel viisil.

    - **Kohaldatav lao tüüp:** *Kõik*
    - **Kauba kood:** *Kõik*
    - **Konto kood:** *Kõik*
    - **Katsegrupp:** *Koonus*
    - **Kauba valim:** *10%*

Ostutellimus on nüüd loodud kauba A0001 koguse 10 kohta hankijale 104. Seejärel registreeritakse mobiilirakenduse Warehouse Management abil ostutellimuse rida, mille kogus on 10, ühe litsentsiplaadi all vastuvõetuks. Tulemus on järgmine.

- Katsegrupis *Raamistik* on esimese kvaliteediseosega seotud üks kvaliteettellimus. Kogus on 5. Teise kvaliteediseosega kvaliteettellimust seostatud pole, sest esimese kvaliteediseose kriteeriumid on katsegrupiga *Raamistik* võrreldes täpsemad.
- Katsegrupis *Takistus* on kolmanda kvaliteediseosega seotud üks kvaliteettellimus. Kogus on 10. Neljanda kvaliteediseosega kvaliteettellimust seostatud pole, sest esimese kvaliteediseose kriteeriumid on katsegrupiga *Takistus* võrreldes täpsemad.
- Katsegrupis *Koonus* on viienda kvaliteediseosega seotud üks kvaliteettellimus. Kogus on 1.

Ühe kvaliteettellimuse loomisel kõigi kolme kvaliteediseose jaoks luuakse ka kauba kvaliteedivalimi töö. Registreeritud kogus on ainult 10. Kuid kauba valimi seadistuse tõttu on kohaldatavale lao tüübile *Kvaliteedijuhtimine ainult laoprotsesside jaoks* loodud kvaliteettellimuse koguste summa 16, mis ületab füüsilise registreeritud koguse (10). Seetõttu ei looda tööd kõikide kvaliteettellimuse koguste jaoks (16), sest ainult 10 on füüsiliselt kvaliteedikontrolli asukohta teisaldamiseks saadaval. Kauba kvaliteedivalimi töö loomiseks kasutatav järjekord järgib kvaliteettellimuse loomise järjekorda.

- **Esimene kvaliteettellimus (kogus = 5):** kauba kvaliteedivalimi töö on loodud 5 jaoks. Järele jääb kogus 5 (10 – 5) järgmise kauba kvaliteedivalimi töö loomiseks.
- **Teine kvaliteettellimus (kogus = 10):** kauba kvaliteedivalimi töö on loodud 5 jaoks. Järele jääb kogus 0 (null) järgmise kauba kvaliteedivalimi töö loomiseks.
- **Kolmas kvaliteettellimus (kogus = 1):** kauba kvaliteedivalimi tööd ei looda.

Kvaliteettellimuste loomise protsessi osana luuakse varude blokeerimine kogusega 10. Varude blokeerimist võrreldakse kõigi kolme kvaliteettellimusega. Kvaliteettellimuse koguste summa on 16.

Kui kvaliteettellimused kinnitatakse, püüab süsteem luua iga kinnitatud kvaliteettellimuse jaoks kvaliteettellimuse töö. Kuna kvaliteettellimuse koguste summa ületab tegelikult blokeeritud ja seega ka töö loomisel saadaolevat kogust, ei saa kvaliteettellimuse tööd luua kogu kvaliteettellimuse koguste jaoks, nagu siin näidatud. (See näide jätkab eelmist näidet.)

1. **Kinnitage teine loodud kvaliteettellimus (kogus = 10). Kvaliteettellimuse töö luuakse kogusele 4.**

    Kvaliteettellimuse töö loomine käivitatakse varude blokeerimise koguse muutmisel. Kuna kvaliteettellimuste koguste summa oli 16, põhjustab koguse 10 kinnitamine järelejäänud kvaliteettellimuste koguste kinnitamise nii, nagu need oleksid võrdsed 6-ga. Varude blokeerimise kogust vähendatakse 10-lt 6-ni. Vähendatud kogus (4) eraldatakse kvaliteettellimuse töö loomisele.

2. **Kinnitage esimene loodud kvaliteettellimus (kogus = 5). Kvaliteettellimuse töö luuakse kogusele 5.**

    Kvaliteettellimuse töö loomine käivitatakse varude blokeerimise koguse muutmisel. Kuna kvaliteettellimuse koguste summa oli 6, põhjustab koguse 5 kinnitamine järelejäänud kvaliteettellimuse koguste kinnitamise nii, nagu need oleksid võrdsed 1-ga. Varude blokeerimise kogust vähendatakse 6-lt 1-ni. Vähendatud kogus (5) eraldatakse kvaliteettellimuse töö loomisele.

3. **Kinnitage kolmas loodud kvaliteettellimus (kogus = 1). Kvaliteettellimuse töö luuakse kogusele 1.**

    Kvaliteettellimuse töö loomine käivitatakse varude blokeerimise koguse muutmisel. Kuna kvaliteettellimuse koguste summa oli 1, põhjustab koguse 1 kinnitamine järelejäänud kvaliteettellimuse koguste kinnitamise nii, nagu need oleksid võrdsed 0-ga (null). Varude blokeerimine eemaldatakse (st varude blokeerimise kogust vähendatakse 1-st 0-ni). Vähendatud kogus (1) eraldatakse kvaliteettellimuse töö loomisele.

> [!NOTE]
> Kvaliteettellimuse töö loomine sõltub varude blokeerimise kogusest, mida kontrollitakse ühe või mitme kvaliteettellimuse abil. Kui kvaliteettellimuse koguste summa ületab kontrollitud varude blokeerimise kogust, määratleb kvaliteettellimuse töö loomise see tellimus, milles kvaliteettellimused kinnitatakse.

## <a name="canceling-quality-item-sampling-work"></a>Kauba kvaliteedivalimi töö tühistamine

Te saate tühistada töö, mis on loodud kauba kvaliteedivalimi jaoks. Et kontrollida, mis juhtub, kui see töö tühistatakse, toimige järgmiselt.

1. Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
1. Seadke vahekaardi **Üldine** kiirkaardil **Töö** suvand **Eemalda töö tühistamisel vastuvõtt registrist** ühele järgmistest väärtustest.

    - **Jah** – kui kauba kvaliteedivalimi töö tühistatakse, kustutatakse seotud kvaliteettellimus ja varud eemaldatakse registrist.
    - **Ei** – kui kauba kvaliteedivalimi töö tühistatakse, ei kustutata seotud kvaliteettellimust ja varusid ei eemaldata registrist.

## <a name="cross-docking"></a>Ristlaadimine

Teil võib olla kvaliteediseose seadistus, mis loob kauba valimi töid. Kuid kui ristlaadimine on aktiivne paralleelselt koos kauba kvaliteedivalimi töid loova kvaliteediseosega, luuakse siis, kui kogusest piisab vaid ristlaadimise täitmiseks, ainult kauba valimi töö. Juhul kui suvand **Luba kvaliteettellimused laoprotsesside jaoks** on vastuvõtva lao puhul seatud väärtusele _Jah_ ning väli **Kohaldatav lao tüüp** on kvaliteediseose puhul seatud väärtusele _Kvaliteedijuhtimine ainult laoprotsesside jaoks_, on kauba kvaliteedivalimi töö loomine tähtsam ristlaadimise töö loomisest. Kui kogus ületab ristlaadimiseks vajaliku kogust, loob süsteem ikkagi ainult kauba valimi töö.

## <a name="destructive-testing"></a>Purustav katse

Saate määrata katsegrupi, millega tehakse hävitavaid katseid. Hävitava katse puhul on eeldus see, et sõltumata testi tulemusest hävitatakse katsetatava kauba kogus katse osana. Viis, kuidas funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ toetab hävitavaid katseid, sarnaneb sellele, kuidas kvaliteedijuhtimine toetab neid siis, kui funktsioon ei ole sisse lülitatud. Enne kvaliteettellimuse kinnitamist peab kvaliteedi kontrollija määrama hävitatud kogusele komplekteerimise asukoha. Saate registreerida komplekteerimise kvaliteettellimuse lehel, valides toimingupaanil **Varud \> Komplekteeri**. Pärast seda, kui kvaliteettellimuse koguse komplekteerimine on registreeritud, saab kinnitamise lõpule viia.

## <a name="example-scenario"></a>Näidisstsenaarium

### <a name="prepare-the-scenario"></a>Stsenaariumi ettevalmistamine

Selle stsenaariumi läbitöötamiseks peate oma süsteemi ette valmistama järgmisel viisil.

- Veenduge, et demoandmed on süsteemi installitud ja valige juriidiline isik **USMF**.
- Lülitage funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ sisse [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Seadke ladu 51 kasutama funktsiooni _Kvaliteedijuhtimine laoprotsesside jaoks_ järgmiselt.

    1. Avage **Laohaldus \> Seadistus \> Ladu \> Laod**.
    1. Valige ladu 51.
    1. Seadke kiirkaardil **Ladu** valik **Luba kvaliteettellimused laoprotsesside jaoks** väärtusele *Jah*.

### <a name="quality-in-setup--move-to-the-quality-control-location"></a>Kvaliteedikontrolli mineva kauba seadistus – kvaliteedikontrolli asukohta teisaldamine

Nüüd peate valmistama ette põhiseadistuse, mis võimaldab teie süsteemil toetada lao 51 puhul funktsiooni _Kvaliteedijuhtimine laoprotsesside jaoks_. (Demoandmed määratlevad kvaliteedijuhtimise asukoha, mille nimi on *QMS*. Sellele asukohale viidatakse selles stsenaariumis mitu korda.) Valmistage ette järgmised elemendid, nagu on kirjeldatud selle jaotise alajaotistes.

- Töö klass
- Töömall
- Asukohakorraldus
- Üksuse valimivõtt
- Kvaliteediseos
- Mobiilse seadme menüü-üksused

#### <a name="work-class-for-quality-in"></a>Tööklass kvaliteedikontrolli mineva kauba jaoks

1. Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töö klassid**.
1. Looge töö klass ja seadke järgmised väärtused.

    - **Töö klassi ID:** _QualityIn_
    - **Kirjeldus:** _Kauba kvaliteedivalim_
    - **Töökäsu tüüp:** _Kauba kvaliteedivalim_

#### <a name="work-template"></a>Töömall

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Seadke välja **Töökäsu tüüp** väärtuseks _Kauba kvaliteedivalim_.
1. Looge töömall ja seadke järgmised väärtused.

    - **Töömall:** _51 kvaliteedikontrolli kaupa_
    - **Töömalli kirjeldus:** _51 kvaliteedikontrolli kaupa_

1. Lisage töömallile rida ja seadke järgmised väärtused.

    - **Töö tüüp:** _Komplekteerimine_
    - **Töö klassi ID:** _QualityIn_

1. Lisage töömallile tine rida ja seadke järgmised väärtused.

    - **Töö tüüp:** _Ladustamine_
    - **Töö klassi ID:** _QualityIn_

#### <a name="location-directive"></a>Asukohakorraldus

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Seadke välja **Töökäsu tüüp** väärtuseks _Kauba kvaliteedivalim_.
1. Looge asukohakorraldus ja seadke järgmised väärtused.

    - **Nimi:** _51 kvaliteedikontrolli_
    - **Töö tüüp:** _Ladustamine_
    - **Tegevuskoht:** 5
    - **Ladu:** _51_

1. Lisage asukorralduse jaoks rida ja seadke järgmised väärtused.

    - **Alates kogusest:** _1_
    - **Koguseni:** _1000000_

1. Looge asukohakorralduse tegevus ja seadke järgmine väärtus.

    - **Nimi:** _Kvaliteet_

1. Valige uue asukohakorralduse tegevuse jaoks valik **Redigeeri päringut** ja määrake **Vahemiku** kirje, millel on järgmised väärtused.

    - **Tabel:** *Asukohad*
    - **Väli:** _Asukohaprofiili ID_
    - **Kriteeriumid:** *QMS*

1. Valige **OK**, et päring ja uus asukohakorraldus salvestada.

Järgmisena peate lao 51 jaoks muutma olemasolevate ostutellimuse asukohakorralduste järjestust. Demoandmed sisaldavad kahte asukohakorraldust, mille suvandi **Töökäsu tüüp** väärtus on _Ost_: üks nimega _51 QMS_ ja teine nimega _51 otse-PO_. Tagamaks, et laos 51 rakendatakse funktsiooni *Kvaliteedijuhtimine laoprotsesside jaoks*, peate veenduma, et asukohakorraldust _51 QMS_ ei rakendata. Kuid selle asukohakorralduse kustutamise asemel (kuna võib juhtuda, et soovite seda tulevikus kasutada), saate järjestust lihtsalt muuta.

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Seadke väli **Töökäsu tüüp** väärtusele _Ostutellimus_.
1. Valige järjestuse loendis järjekorranumber 5 asukohakorralduse _51 otse-PO_ jaoks.
1. Teisaldage valitud järjestus järjekorranumbrini 4.
1. Kontrollige, et asukohakorralduse _51 QMS_ järjekorranumber oleks nüüd vähemalt 5.

#### <a name="item-sampling"></a>Üksuse valimivõtt

Funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ lisab mõned uued kauba valimi määramise võimalused. Suvandi **Valimi ulatus** väärtus võib nüüd olla _Tellimus_, _Saadetis_ või _Koorem_ ning suvandi **Valimi kogus** väärtus võib nüüd olla _Kogu litsentsiplaat_.

1. Avage **Varude haldus \> Seadistus \> Kvaliteedijuhtimine \> Kauba valim**.
1. Looge kauba valimi kirje ja seadke järgmised väärtused.

    - **Kauba valim:** _3. LP_
    - **Kirjeldus:** _Iga kolmas litsentsiplaat_
    - **Valimi ulatus:** _Tellimus_

1. Seadke kiirkaadil **Valimi kogus** välja **Koguse spetsifikatsioon** väärtuseks _Kogu litsentsiplaat_.
1. Seadke kiirkaardil **Protsess** välja **Iga n-inda litsentsiplaadi järel** väärtuseks _3_.
1. Lubage jaotises **Laoala dimensiooni järgi** nii **Ladu** kui ka **Varude olek**.

#### <a name="quality-associations"></a>Kvaliteediseosed

Looge kvaliteediseos, mis kasutab uut kauba valimit.

1. Avage **Varude haldus \> Seadistus \> Kvaliteedijuhtimine \> Kvaliteediseosed**.
1. Looge kvaliteediseose kirje ja seadke järgmised väärtused.

    - **Viite tüüp:** _Ost_
    - **Kauba kood:** _Tabel_
    - **Kaup:** _M9201_
    - **Tegevuskoht:** _5_

1. Seadke kiirkaardil **Protsess** välja **Sündmuse tüüp** väärtuseks *Registreerimine*.
1. Seadke kiirkaardil **Tingimused** välja **Kohaldatav lao tüüp** väärtuseks *Kvaliteedijuhtimine ainult laoprotsesside jaoks*.
1. Seadke kiirkaardil **Kvaliteettellimuse protsess** välja **Kvaliteeditöötluse poliitika** väärtuseks _Loo kvaliteettellimus_.
1. Paremklõpsake kiirkaardil **Spetsifikatsioonid** väljal **Katsegrupp** ja valige seejärel **Kuva üksikasjad**, et avada leht **Katsegrupid**.
1. Looge katsegrupp lehe **Katsegrupid** ülemise ruudustiku vahekaardil **Ülevaade** ja seadke järgmised väärtused.

    - **Katsegrupp:** _QMS_
    - **Kirjeldus:** _QMS-i katse_
    - **Sobiv kogus:** _100_
    - **Kauba valim:** _3. LP_ (valige)

1. Lisage alumise ruudustiku vahekaardil **Ülevaade** ühe katse jaoks kirje ja seadke järgmised väärtused.

    - **Järjestus:** *1*
    - **Katse:** *Raamistuse mõõtmine*

1. Määrake alumise ruudustiku vahekaardil **Katse** järgmised väärtused.

    - **Katse muutujad:** *Läbitud/nurjunud*
    - **Vaiketulemus:** *Läbitud*

1. Salvestage uus katsegrupp ja sulgege leht **Katsegrupid**.
1. Valige lehe **Kvaliteediseosed** väljal **Katsegrupp** suvand **QMS**.
1. Salvesta kirje.

#### <a name="mobile-device-menu-items-for-quality-in"></a>Mobiilse seadme menüüelement kvaliteedikontrolli mineva kauba jaoks

Kaupade kvaliteedikontrolli asukohta teisaldamise seadistuse lõpetamiseks peate muutma kauba valimi töö mobiilse seadme menüüelemendi kaudu kättesaadavaks.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Valige mobiilse seadme menüüelement **Ostu ladustamine**.
1. Lisage kiirkaardil **Töö klassid** töö klassi ID *QualityIn*.

#### <a name="summary-your-setup-to-move-goods-to-quality-control"></a>Kokkuvõte: teie seadistus kaupade teisaldamiseks kvaliteedikontrolli

Olete nüüd määratlenud kvaliteediseose, mis kasutab kvaliteettellimuse loomiseks funktsiooni *Kvaliteedijuhtimine laoprotsesside jaoks*. Olete seadistanud töö ja asukoha andmed lao 51 jaoks, et tagada kindla töö loomine, kui kauba M9201 ost registreeritakse. See seadistus tagab, et iga registreeritud kolmas litsentsiplaat viiakse üle kvaliteediasukohta (_QMS_) ja litsentsiplaadi koguse jaoks luuakse kvaliteettellimus. Kõik muu teisaldatakse kvaliteedikontrolli asukoha asemel ladustamiskohta.

### <a name="process-quality-management-work"></a>Kvaliteedijuhtimise töö töötlemine

1. Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.
1. Looge ostutellimus ja seadke järgmised väärtused.

    - **Määra hankija konto:** *104*
    - **Ladu:** *51*

1. Lisage ostutellimuse rida ja seadke järgmised väärtused.

    - **Kaup:** *M9201*
    - **Kogus:** *20*
    - **Mõõtühik:** *ea*
    - **Ladu:** *51*

1. Kirjutage ostutellimuse number üles, et saaksite seda hiljem kasutada.
1. Minge mobiilsesse seadmesse või emulaatorisse, milles töötab mobiilirakendus Warehouse Management, ja logige sisse lattu 51, kasutades kasutaja ID-d *51* ja parooli *1*.
1. Avage **Sissetulev \> Ostu ülevaade** ja sisestage järgmised väärtused.

    - **PONum:** äsja loodud ostutellimuse number
    - **Kogus:** *5*
    - **Ühik:** *ea*

1. Jätkake rea vastuvõtmist *5 ea* kaupa, kuni rida on täielikult vastu võetud. (Kokku luuakse neli litsentsiplaati.)
1. Laohalduse mobiilirakendusest välja logimine.
1. Avage veebikliendis **Hange \> Ostutellimused \> Kõik ostutellimused**.
1. Leidke ja avage oma ostutellimus.
1. Valige jaotises **Ostutellimuse read** kaubakoodi *M9201* rida ja seejärel valige **Ostutellimuse read \> Töö üksikasjad**.
1. Pange tähele, et loodud teise ja kolmanda töö päised on regulaarsed ladustamistööd, samas kui esimese ja neljanda töö päised on kauba kvaliteedivalimi tööd. See tulemus on kooskõlas kauba valimi seadistusega, mis on konfigureeritud kaasama iga kolmandat litsentsiplaati.

#### <a name="move-to-the-quality-control-location"></a>Kvaliteedikontrolli asukohta teisaldamine

Nüüd teisaldate te litsentsiplaadid nende määratud asukohtadesse. Esimene ja neljas litsentsiplaat lähevad kvaliteedikontrolli asukohta, samas kui teine ja kolmas litsentsiplaat lähevad otse lattu.

1. Minge mobiilsesse seadmesse või emulaatorisse, milles töötab mobiilirakendus Warehouse Management, ja logige sisse lattu 51, kasutades kasutaja ID-d *51* ja parooli *1*.
1. Avage **Sissetulev \> Ostu ladustamine** ja ladustage iga eelmise protseduuri litsentsiplaat, kuni olete kõik tööd sulgenud.

#### <a name="summary-process-quality-management-work"></a>Kokkuvõte: kvaliteedijuhtimise töö töötlemine

Nüüd olete käivitanud esimese ja neljanda litsentsiplaadi puhul kauba kvaliteedivalimi töö, teisaldades plaadid kvaliteedikontrolli asukohta. Olete ladustanud ka teise ja kolmanda litsentsiplaadi. Järgmine samm on teha kvaliteettellimuse katsed ja tellimusi kontrollida.

### <a name="quality-out-setup-move-from-the-quality-control-location-to-storage-or-return"></a>Kvaliteedikontrollist tuleva kauba seadistus: teisaldage kaup kvaliteedikontrolli asukohast lattu või tagasi

Kui töötajad teatavad kvaliteettellimuse tulemustest, loob süsteem automaatselt töö.

Nüüd jätkate te töö klassi, töömalli ja asukohakorralduse vajaliku põhiseadistusega, et lubada kvaliteedijuhtimine laoprotsesside jaoks selleks, et vajaliku töö loomine kvaliteettellimuse koguse teisaldamiseks kvaliteedikontrolli asukohast määratud lao asukohta oleks võimalik.

#### <a name="work-class-for-quality-out"></a>Tööklass kvaliteedikontrollist tuleva kauba jaoks

1. Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töö klassid**.
1. Looge töö klass ja seadke järgmised väärtused.

    - **Töö klassi ID:** *QualityOut*
    - **Kirjeldus:** *Kvaliteedikontrollist tulev*
    - **Töökäsu tüüp:** *Kvaliteettellimus*

#### <a name="work-templates"></a>Töömallid

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Muutke suvandi **Töökäsu tüüp** väärtuseks *Kvaliteettellimus*.
1. Looge töömall ja seadke järgmised väärtused.

    - **Töö mall:** *51 kvaliteedikontrollist tulevat*
    - **Töö malli kirjeldus:** *51 kvaliteedikontrollist tulevat*

1. Lisage rida ja määrake järgmised väärtused.

    - **Töö tüüp:** *Komplekteerimine*
    - **Töö klassi ID:** **QualityOut**

1. Lisage teine rida ja määrake järgmised väärtused.

    - **Töö tüüp:** *Ladustamine*
    - **Töö klassi ID:** *QualityOut*

#### <a name="location-directives"></a>Asukohakorraldus

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Muutke suvandi **Töökäsu tüüp** väärtuseks *Kvaliteettellimus*.
1. Looge asukohakorraldus ja seadke järgmised väärtused.

    - **Nimi:** *51 läbitud*
    - **Töö tüüp:** *Ladustamine*
    - **Tegevuskoht:** *5*
    - **Ladu:** *51*

1. Valige toiminguribal suvand **Redigeeri päringut**, et avada päringuredaktori dialoogiboks.
1. Määrake vahekaardil **Vahemik** järgmised väärtused.

    - **Tabel:** *Kvaliteettellimused*
    - **Väli:** *Olek*
    - **Kriteeriumid:** *Läbitud*

1. Päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.
1. Lisage kiirkaardil **Read** rida ja seadke järgmised väärtused.

    - **Alates kogusest:** *1*
    - **Koguseni:** *1000000*

1. Lisage rida kiirkaardil **Asukohakorralduse tegevused** ja seadke järgmine väärtus.

    - **Nimi:** *Läbitud*

1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Redigeeri päringut**, et avada päringuredaktori dialoogiboks.
1. Määrake vahekaardil **Vahemik** järgmised väärtused.

    - **Tabel:** *Asukohad*
    - **Väli:** *Tsooni ID*
    - **Kriteeriumid:** *Hulgiasukoht*

1. Päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.
1. Valige toimingupaanil **Salvesta**, et salvestada uus asukohakorraldus.
1. Looge teine asukohakorraldus ja seadke järgmised väärtused.

    - **Nimi:** *51 nurjumist*
    - **Töö tüüp:** *Ladustamine*
    - **Tegevuskoht:** *5*
    - **Ladu:** *51*

1. Valige toiminguribal suvand **Redigeeri päringut**, et avada päringuredaktori dialoogiboks.
1. Määrake vahekaardil **Vahemik** järgmised väärtused.

    - **Tabel:** *Kvaliteettellimused*
    - **Väli:** *Olek*
    - **Kriteeriumid:** *Nurjunud*

1. Päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.
1. Lisage kiirkaardil **Read** rida ja seadke järgmised väärtused.

    - **Alates kogusest:** *1*
    - **Koguseni:** *1000000*

1. Lisage rida kiirkaardil **Asukohakorralduse tegevused** ja seadke järgmine väärtus.

    - **Nimi:** *Nurjunud*

1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Redigeeri päringut**, et avada päringuredaktori dialoogiboks.
1. Määrake vahekaardil **Vahemik** järgmised väärtused.

    - **Tabel:** *Asukohad*
    - **Väli:** *Tsooni ID*
    - **Kriteeriumid:** *Tagastus*

1. Päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.
1. Valige toimingupaanil **Salvesta**, et salvestada uus asukohakorraldus.

#### <a name="mobile-device-menu-items-for-quality-out"></a>Mobiilse seadme menüüelement kvaliteedikontrollist tuleva kauba jaoks

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Valige mobiilse seadme menüüelement **QMS-i ladustamine**.
1. Lisage kiirkaardil **Töö klassid** töö klassi ID *QualityPut*.

Laotöötajad saavad nüüd valida kvaliteettellimuse töö, kasutades menüüelementi **QMS-i ladustamine**. Kaubad, mis ei läbinud kvaliteedikontrolli, saab panna tagastusasukohta ja kontrolli läbinud kaubad saab panna asukohta bulk-001.

#### <a name="summary-your-setup-to-move-goods-from-quality-control"></a>Kokkuvõte: teie seadistus kaupade teisaldamiseks kvaliteedikontrollist

Olete seadistanud töö ja asukoha andmed lao 51 jaoks, et tagada töö loomine automaatselt, kui kvaliteettellimused viiakse lõpule. See seadistus tagab, et iga kvaliteedikontrollist läbi käinud litsentsiplaat teisaldatakse kas hulgi- või tagastusasukohta.

### <a name="process-quality-management-work"></a>Kvaliteedijuhtimise töö töötlemine

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Kvaliteettellimused**.
1. Valige registreeritud koguste esimene kvaliteettellimus.
1. Valige **Kinnita**. Testi olekuks seatakse *Nurjunud*.
1. Avage **Laohaldus \> Kõik tööd**.
1. Avage äsja loodud töö ja pange tähele, et sätte **Töökäsu tüüp** väärtus on *Kvaliteettellimus*. Töö sisaldab rida, mille ladustamiskoht on *Tagastus* ja olek *Nurjunud*. (Kui kvaliteettellimuse olek oleks *Läbitud*, oleks ladustamiskoht selle asemel *Hulgiasukoht*.)
1. Avage uuesti **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Kvaliteettellimused**.
1. Valige registreeritud kaupade tine kvaliteettellimus.
1. Valige alumise ruudustiku kohalt **Tulemused**. Seadke sätte **Tulemuse koguse** väärtuseks *5* ja veenduge, et sätte **Katsetulemus** väärtuseks oleks märge.
1. Valige **Kinnita** ja sulgege leht.
1. Valige lehel **Kvaliteettellimused** suvand **Kinnita** ja viige läbi kinnitustoiming. Olek värskendatakse sättele *Läbitud*.

    > [!NOTE]
    > Kinnitamise sündmus käivitab kvaliteettellimuse töö loomise, et teisaldada kogus kvaliteedikontrolli asukohast uude asukohta.

1. Avage **Laohaldus \> Kõik tööd**.
1. Valige äsja loodud töö ja pange tähele, et loodud on teine kvaliteettellimuse töö päis, mille ladustamiskoht on *BULK-001*.
1. Minge mobiilsesse seadmesse või emulaatorisse, milles töötab mobiilirakendus Warehouse Management, ja logige sisse lattu 51, kasutades kasutaja ID-d *51* ja parooli *1*.
1. Avage **Kvaliteet \> QMS-ist ladustamine** ja töödelge mõlema tööga seostatud litsentsiplaati, et kõik tööd oleks suletud.

> [!NOTE]
> Kaaluge kvaliteedikontrollist tuleva kauba kirje lisamist mobiilse seadme menüüelemendile, mille tegevuse kood on *Kuva avatud tööloend*. Vaadake näiteks demo-andmetes mobiilse seadme menüüelementi, mille nimetus on **Tööloend**. Esmalt lisage kasutaja suunatud menüüelementi töö klass *Kvaliteettellimus*, kuna seda töö klassi on vaja tööde kuvamiseks tööloendis. Seejärel lisage töö klass *Kvaliteettellimus* menüüelemendile **Tööloend**. Tööloendile ligi pääsevad kasutajad saavad seejärel valida ja töödelda tööd, mis luuakse automaatselt kvaliteettellimuse kinnitamisel.

## <a name="additional-resources"></a>Lisaressursid

- [Kvaliteedi ja mittevastavuse haldamise ülevaade](quality-management-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]