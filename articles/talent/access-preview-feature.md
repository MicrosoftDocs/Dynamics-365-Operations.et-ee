---
title: Funktsioonide haldamine
description: Selles teemas kirjeldatakse, kuidas administraator saab lubada eelvaatefunktsioone rakenduses Microsoft Dynamics 365 Talent, ja loetletakse funktsioone, mis on praegu eelvaate jaoks lubatud.
author: tracykeya
manager: AnnBe
ms.date: 05/30/2019
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
ms.openlocfilehash: 9f1fb4b929660bbe9018fb98169b3cfddcaec547
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833296"
---
# <a name="manage-features"></a>Funktsioonide haldamine

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent pidevate inimkapitali juhtimisvõimaluste (HCM) levitamise osana tahame, et kliendid saaksid proovida uusi funktsioone niipea kui võimalik. Administraatorid saavad näha ja kasutada eelvaatefunktsioone oma keskkondades. Need funktsioonid on peaaegu valmis üldiseks kasutamiseks ja on läbinud põhjalikud kontrollid. Eelvaatefunktsioonide puhul soovime saada täiendavat kasutajate tagasidet ja kinnitust, enne kui funktsioonid üldiselt kättesaadavaks teeme.

Selles teemas kirjeldatakse, kuidas saate lubada eelvaatefunktsioone, ja loetletakse funktsioone, mis on praegu eelvaatena saadaval. Loendit värskendatakse, kui funktsioonid tehakse üldiselt kättesaadavaks ja/või lisatakse uusi eelvaatefunktsioone. Uute eelvaatefunktsioonide kohta ei saadeta teatisi. Kasutajad märkavad lihtsalt uusi funktsioone. Lisateavet Talenti uute funktsioonide kohta vt teemast [Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent](./whats-new.md) ja [Dynamics 365 ja Power Platformi väljalaskemärkmed](https://docs.microsoft.com/business-applications-release-notes).

## <a name="enable-or-disable-preview-features"></a>Eelvaatefunktsioonide lubamine või keelamine

Eelvaatefunktsioonidele ligipääsemiseks peate kõigepealt need oma keskkonnas lubama. Eelvaatefunktsioonide lubamine või keelamine sõltub keskkonnast.

> [!IMPORTANT]
> Kui lülitate sisse sätte **Eelvaatefunktsioonid**, siis lubate eelvaatefunktsioonid kõikidele teie organisatsiooni kasutajatele, kes on selles keskkonnas. Kui lülitate sätte välja, siis keelate eelvaatefunktsioonid ja teie kasutajatel pole nendele juurdepääsu. Rakenduses Talent on eelvaatefunktsioonidel piiratud tugi. Need võivad kasutada vähem privaatsus- ja turbemeetmeid ning pole hõlmatud rakenduse Talent teenindustaseme lepingus (SLA). Eelvaatefunktsioone ei tohi kasutada isikuandmete (st igasugused andmed, mis võimaldavad isikut tuvastada) ega muude andmete töötlemiseks, millele kehtivad seaduste või regulatsioonide järgmise nõuded.

### <a name="attract"></a>Attract

1. Rakenduse Microsoft Dynamics 365 Talent: Attract sisselogimine.
2. Valige ülemises parempoolses nurgas olevast menüüst **Seadistus** (hammasratta sümbol) suvand **Halduskeskus**.
3. Valige vahekaardi **Funktsioonide haldus** suvandi **Eelvaatefunktsioonid** kõrval olev suvand nii, et see muutuks siniseks ja sellel oleks tähis **Sees**.

    ![Eelvaatefunktsioonide lubamine rakenduses Attract](./media/attract-enable-preview-features.png)

4. Valige üksikud eelvaatefunktsioonid või tühistage valik. Kui te ei tee midagi, on kõik saadaolevad eelvaatefunktsioonid lubatud.
5. Uute funktsioonide nägemiseks värskendage oma brauserit. Sisselogitud kasutajad näevad uusi funktsioone, kui nad logivad uuesti sisse, või nad võivad uute funktsioonide kohe nägemiseks oma brauserit värskendada.

> [!NOTE]
> Mõne funktsiooni jaoks võib vaja minna lisakonfiguratsiooni. Seadistamise lõpetamiseks järgige linke eelvaatefunktsiooni kõrval.

### <a name="core-hr"></a>Core HR

1. Logige sisse rakendusse Talent.
2. Valige suvand **Süsteemihaldus** ja seejärel valige vahekaart **Lingid**.
3. Lehel **Süsteemihaldus** jaotisest **Seadistamine** valige suvand **Süsteemi parameetrid**.
4. Lehel **Süsteemi parameetrid** valige vahekaart **Eelvaatefunktsioonid**.
5. Seadistage suvand **Luba eelvaaterežiim kõigi kasutajate jaoks** valikule **Jah**, et eelvaatefunktsioonid oleks saadaval.

    ![Eelvaatefunktsioonide lubamine rakenduses Core HR](./media/corehr-enable-preview-features.png)

> [!NOTE]
> Eelvaatefunktsioonide keelamiseks kasutage samu etappe, aga seadistage suvand **Luba eelvaaterežiim kõiki kasutajate jaoks** valikule **Ei**. Eelvaatefunktsioonide keelamisega võivad funktsioonid kasutajatele juurdepääsmatuks muutuda ja põhjustada tõrkeid nende funktsioonidega seostatud protsessides.

### <a name="onboard"></a>Sisseelamine

Rakenduse Microsoft Dynamics 365 Talent: Onboard jaoks pole praegu saadaval ühtegi eelvaatefunktsiooni.

## <a name="features-that-are-currently-in-preview"></a>Praegused eelvaatefunktsioonid

### <a name="attract"></a>Attract

- [Kandidaadisoovitus](./intelligent-recommendations.md#candidate-recommendations) – kui rohkem kui kümnel kandidaadil on elulookirjeldused või täidetud profiilid, ilmuvad kandidaadid, kes vastavad kõige paremini töö nõutele, jaotisesse **Kandidaadid, keda kaaluda** selle töö lehel.
- [Töösoovitus](./intelligent-recommendations.md#job-recommendations) – kui teie karjäärisaidile sisestatakse rohkem kui kümme tööd, pakub Attract töövõtjatele töösoovitusi.
- [Broadbeani integreerimine](./posting-jobs-external.md#post-jobs-to-broadbean) – saate sisestada töid Attractist Broadbeani, välisele töösisestuse saidile. Kui selle eelvaatefunktsiooni lubate, peate tegema seadistuse, sisestades Broadbeani kasutajanime, kliendi ID ja krüptimise loa.
- [Analüütika](./analytic-reports.md) – analüüsikeskuses näevad värbamistöörühmad ühe töö põhimõõdikuid ja koondmõõdikuid kõigi tööde kohta.
- [EEO](./activities-attract.md) – uute tegevustüüpidega saate kasutada valmis vormi võrdsete tööhõivevõimaluste (Equal Employment Opportunity (EEO)) ja USA föderaalse lepingute vastavusprogrammi (Office of Federal Contract Compliance Program (OFCCP)) andmete kogumiseks kandidaadilt. Valmis vormi ei saa redigeerida.
- [Potentsiaalselt sobiva kandidaadi soovitamine](./intelligent-recommendations.md#prospect-recommendations) – Attract vaatab üle varasemad ja praegused kandidaadid, et esitada tööle potentsiaalselt sobivate kandidaatide loend.
- [Asjakohasuse otsing](./attract-talent-pools.md#search-and-view-candidate-profiles) – saate otsida kogu kandidaatide andmebaasist teatud oskusi, nimesid või hariduskäiku. Attract otsib kogu profiilist ja tõstab esile leitud vasted. Attract otsib ka kõigist kandidaadile saadaolevatest dokumentidest ja järjestab intelligentselt otsingutulemused.
- [Tegevuse publik](./whats-new-talent-march-20.md#setting-the-audience-on-activities) – saate määrata tegevuste (nt vestluse, graafiku või tagasiside) publiku valikule **Kõik kandidaadid**, **Sisekandidaadid** või **Välised kandidaadid**. Klienditegevusi, näiteks YouTube’i videoid, veebisisu ja Microsoft Formsi, saab edastada kõikidele kandidaatidele, ainult sisekandidaatidele, ainult välistele kandidaatidele või värbamistöörühmale.
- [Kandideeri LinkedIni kaudu](./career-site.md#enable-applying-for-jobs-with-linkedin-profiles) – saate Attracti karjäärisaidil seadistada suvandi, et töökoha kandidaadid saaksid kandideerida LinkedIni kaudu. See funktsioon muudab kandideerimisprotsessi kandidaatide jaoks sujuvamaks, lubades neil kasutada LinkedIni profiili avalduste automaatseks täitmiseks teie karjäärisaidil.
- [Allika jälgimine](./source-tracking.md) – Attract jälgib kandidaadi avalduste allikaid, et pakkuda teile väärtuslikku abiteavet värbamisprotsessi jaoks. Võite kandidaadi tööle või talendikausta lisamisel valida ka avalduse allika.
- [Hõbemedalist](./whats-new-talent-march-20.md#designate-silver-medalists-to-assign-high-value-applicants-for-future-positions) – kui mõni kandidaat sobib teie organisatsioonile eriti hästi, aga te ei teinud talle pakkumist praegusele ametikohale, saate ta määrata hõbemedalistiks. See funktsioon aitab säästa värbamisele kuluvat aega järgmine kord, kui sarnane ametikoht avaneb.

### <a name="core-hr"></a>Core HR

- [Ametikoha hierarhia andmete kinnitamine](./whats-new-talent-may-13-2019.md#new-page-to-validate-position-hierarchy-data) – saate kinnitada juhtimishierahiat mis tahes ringviidetega, mis võivad olla kogemata imporditud.
- [Määrake puhkuse tüüpide põhjusekoodid](./whats-new-talent-may-13-2019.md#specify-reason-codes-on-leave-types) – saate määrata põhjusekoodid puhkuse tüüpidele.
- [Puhkuseavaldustele põhjusekoodide nõudmine](./whats-new-talent-may-13-2019.md#require-reason-codes-for-specific-leave-types-on-time-off-requests) – peale puhkuse tüüpide kindlate põhjusekoodide saate nõuda põhjusekoode puhkusetaotlustele.
- [Personaliosakonnale puhkuse ja puudumise kannete nimekirja esitamine](./whats-new-talent-may-13-2019.md#provide-a-leave-and-absence-transaction-list-for-hr) – saate vaadata puhkuse ja puudumise kannete loendit, et saada ülevaadet vabade päevade saldodest.

### <a name="onboard"></a>Sisseelamine

Rakenduse Onboard jaoks pole praegu saadaval ühtegi eelvaatefunktsiooni.

## <a name="feedback"></a>Tagasiside

Ootame teie tagasisidet teie kogemuse kohta nende eelvaatefunktsioonidega. Soovitame teil postitada tagasisidet nende või muude funktsioonide kasutamise kohta järgmistel saitidel.

- [Kogukonna foorum](https://community.dynamics.com/enterprise/f/759?pi53869=0&category=Talent) – sellel saidil on mitmeid ressursse ning kasutajad saavad arutada kasutusjuhtumeid, küsida küsimusi ja otsida kogukonnalt abi.
- Andke meile teada funktsioonidest, mida soovite tootes näha, või andke teada muudatustest, mida teie arvates oleks olemasolevates funktsioonides vaja. Tooteideid pakkuge järgmistel saitidel.

    - [Attracti ideed](https://powerusers.microsoft.com/t5/Ideas-for-Attract/idb-p/Attract)
    - [Core HR-i ideed](https://powerusers.microsoft.com/t5/Ideas-for-Human-Resources/idb-p/HumanResources)
    - [Onboardi ideed](https://powerusers.microsoft.com/t5/Ideas-for-Onboard/idb-p/Onboard)

Ärge kindlasti kasutage tagasisides ega tootearvustustes isikuandmeid (igasugused andmed, mis võimaldavad isikut tuvastada). Kogutud teavet võidakse põhjalikumalt analüüsida ja seda ei kasutata kohalduvate isikuandmete kaitse seaduste järgi taotluste täitmiseks. Isikuandmetele, mida kogutakse eraldi nende programmidega, kehtib [Microsofti privaatsusavaldus](https://privacy.microsoft.com/privacystatement).

> [!TIP]
> Lisage see teema järjehoidjatesse ja kontrollige seda tihti, et olla kursis uusimate eelvaatefunktsioonidega, kui neid väljastame.

## <a name="see-also"></a>Vt ka

- [Talenti rakenduste proovimine või ostmine](https://dynamics.microsoft.com/talent/overview/)
- [Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent?](./whats-new.md)
- [Väljalaskeplaanid](https://docs.microsoft.com/business-applications-release-notes/index)
- [Toe hankimine rakendusele Microsoft Dynamics 365 Talent](./talent-support.md)
