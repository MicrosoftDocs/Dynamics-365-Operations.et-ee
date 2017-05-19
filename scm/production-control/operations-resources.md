---
title: Operationsi ressursid
description: "Operatsiooniressurssid sooritavad projekti või tootmisprotsessi tegevusi. Need võivad olla erinevat tüüpi ja erinevate võimalustega."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WrkCtrCapability
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 53700246fb072c4d9afb2e475ae27892700a078a
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="operations-resources"></a>Operationsi ressursid

[!include[banner](../includes/banner.md)]


Operatsiooniressurssid sooritavad projekti või tootmisprotsessi tegevusi. Need võivad olla erinevat tüüpi ja erinevate võimalustega. 

<a name="operations-resources"></a>Operationsi ressursid
--------------------

Operatsiooniressursid on masinad, tööriistad, töötajad, ruumid, füüsilised alad või hankijad, kes teostavad projekti või tootmisprotsessi tegevusi. Need võivad olla erinevat tüüpi ja erinevate võimalustega.

-   **Hankija** – väline ressurss, mis teostab projektitegevusi või tootmisoperatsioone. Selle näiteks on allhankija. Hankija ressursside linkimisel hankijakontoga saate luua allhankijatele oste koosluseridade või tootmisridade põhjal.
-   **Inimressurssid** – projekti- või tootmistöötaja, kes teostab tegevust kas ise või tööriista või masina operaatorina. Kui kasutate inimressursside funktsionaalsust, saate linkida inimressurssid hankijaga. Seejärel saab planeerimismootor ressursse eraldada, võttes aluseks vastava töötaja kohta määratletud pädevused.
-   **Masin** – masin või muu tootmises vajalik tootmisseade.
-   **Tööriist** – vahend või seade, mida tavaliselt kasutatakse koos teise ressursiga projektis või tootmises mingi tegevuse teostamiseks.
-   **Asukoht** – kindla suurusega füüsiline asukoht, mis on tegevuse teostamiseks nõutav. Selle näiteks on montaažiala.
-   **Ruum** – hoone või fikseeritud struktuur, mis on nõutav tegevuse teostamiseks.

## <a name="calendars"></a>Kalendrid
Kalendri saab määrata operatsiooniressursile ja see kirjeldab selle ressursi võimsust (tundides). Operatsiooniressursi tööajad määratakse kalendriga, mis on määratud ressursigrupile, millesse operatsiooniressurss kuulub. Saate seadistada määratud kalendri jõustumiskuupäeva ja aegumiskuupäeva. Seejärel saate määrata operatsiooniressursile rohkem kui ühe kalendri. Määratud kalendrite kuupäevad ei tohi siiski kattuda ja igale operatsiooniressursile saab määrata korraga ainult ühe kalendri. **Märkus.** Kui ressursigrupil ei ole kehtivaid kalendreid (näiteks kui viimane määratud kalender või ainuke määratud kalender on aegunud), ei ole teil enam juurdepääsu operatsiooniressurssidele, mis on määratud ressursigrupi tootmise planeerimiseks ja operatsioonide planeerimiseks. Saate määrata kalendri ressursigrupile ka selleks, et määrata tööaegu nii ressursigrupile kui ka kõigile ressursigrupile määratud operatsiooniressurssidele. Ressursigrupi võimsus arvutatakse iga sellele ressursigrupile määratud operatsiooniressursi võimsuste summana. Ressursigrupile määratud kalendrit saab aja jooksul muuta.

## <a name="resource-capabilities"></a>Ressursi võimalused
Võimsus on operatsiooniressursi võime konkreetset tegevust sooritada. Seejärel saate määrata operatsiooniressursile ühe või mitu võimsust. Siis eraldab planeerimismootor ressursid, sobitades iga tegevuse ressursinõuded saadaolevate operatsiooniressursside võimsustega. Võimsusi saab määrata igat tüüpi operatsiooniressurssidele (**tööriist**, **hankija**, **masin**, **inimressurss**, **asukoht** või **ruum**). Operatsiooniressurssidele piiratud ajaks võimsuste määramiseks määratlege võimsuse määramise algus- ja aegumiskuupäev. Lisateavet vt jaotisest [Ressursivõimsused](resource-capabilities.md).

## <a name="resource-groups"></a>Ressursigrupid
Ressursigrupp on operatsiooniressursside kogum, mis näitab operatsioonide planeerimismeetodi kasutamisel ressursside plaanimise granulaarsust. Seega vastavad ressursigrupid tootmistöödes kollaste joontega määratletud töörakkude füüsilisele korraldusele. Ressursigrupp määratleb grupile määratud operatsiooniressursside tegevuskoha, tootmisüksuse ja lao konteksti. Kui määrate operatsiooniressursi ressursigrupile, saab ressursi planeerida tegevuskohta, kus ressursigrupp asub. Te ei pea loodavaid operatsiooniressursse ressursigrupile määrama. Siiski tuleb operatsiooniressurss määrata ressursigrupile, enne kui seda saab planeerida tööd tegema. Operatsiooniressurssi saab määrata ressursigrupile piiratud aja jooksul. Samuti saate operatsiooniressursi määrata mitmele ressursigrupile, et saaksite ressurssi seejärel tegevuskohtades ühiselt kasutada. Jõustumis- ja aegumiskuupäevad ei tohi siiski kattuda. Teisisõnu ei saa operatsiooniressurssi määrata samal ajal kahele ressursigrupile. Ressursigrupi määramiste muutused kehtivad ainult uute ressursieralduste jaoks. Võimsuse reserveerimisi juba planeeritud töödele, operatsioonidele ja projekti tunnieelarvetele ei mõjutata. **Märkus.** Kui määrate ressursigrupile operatsiooniressursid, mille tüüp on **Hankija**, peab kõigi sellele ressursigrupile määratud operatsiooniressursside tüüp olema **Hankija** ja need peavad olema lingitud sama hankijakontoga.

## <a name="production-units"></a>Tootmisüksused
Tootmisüksus on haldusüksus, mis on ressursigruppide kogum. Tootmisüksus võib sisaldada mitut ressursigruppi, kuid ressursigrupi saab määrata ainult ühte tootmisüksusse. Tootmisüksus kajastab tootmisressursside füüsilist paigutust ega mõju kannetele ega nende töötlemisviisile. Peate tootmisüksuse seostama saidiga. Saate määrata tootmisüksusele ka komplekteerimislaoala ja ladustamislaoala. Saate kasutada tootmisüksust tootmisega seotud teabe konsolideerimiseks ja filtreerimiseks. Nt tööde juhtimise haldur saab üle vaadata silmapaistva töökoormuse ja kindla tootmisüksuse saadaoleva võimsuse. Saate ressursigrupile määratud tootmisüksust muuta. Samuti saate tootmisüksust kustutada. Need tootmisüksuse muudatused rakenduvad aga ainult uutele tellimustele, mis luuakse pärast koondplaneerimise käitamist. Kui tahate tootmisüksuse muudatusi rakendada olemasolevatele tellimustele, peate seda käsitsi tegema.

## <a name="resource-scheduling"></a>Ressursside plaanimine
Operatsiooniressurssid määratakse tegevustele projekti või tootmise planeerimisel. Saadaval on kaks planeerimismeetodit: operatsioonide planeerimine ja tööde planeerimine. Kui kasutate operatsioonide planeerimist, planeeritakse iga operatsioon või projektitegevus ressursigrupis, mis sisaldab operatsiooni jaoks määratud ressursinõuetele vastavaid operatsiooniressursse. Kui operatsiooniks on nõutav kindel operatsiooniressurss, reserveerib planeerimine võimsuse ainult konkreetsele operatsiooniressursile grupis. Tööde planeerimine on üksikasjalikum planeerimisvorm kui operatsioonide planeerimine. See jaotab iga operatsiooni üksikülesanneteks või töödeks. Need tööd määratakse siis operatsiooniressurssidele, kes need ära teevad. Planeerimine reserveerib võimsuse ressursigruppides tootmisprotsessis või tootmistegevustes määratletud operatsiooniaegade põhjal. Kui töötate piiratud võimsusega, sõltub graafik tegevuse lõpule viimiseks nõutavate operatsiooniressursside kättesaadavusest. Operatsioonide planeerimisel on ressursigrupp sellesse gruppi kuuluvate operatsiooniressursside saadaolevate võimsuste summa. Operatsiooniressurssides juba olemas olevaid võimsuse reserveerimisi käsitletakse mittesaadava võimsusena. Kui tootmise jaoks ei ole piisavalt võimsust, saab tootmistellimused edasi lükata või isegi peatada. Lehel **Ressurssid**saate määratleda mitu atribuuti, mis reguleerivad võimsuse reserveerimiste tegemist.

-   **Võimsus** – saate määrata operatsiooniressursi võimsuse tunnis võimsuse mõõtühikutes.
-   **Partii võimsus** – saate määrata tükkide maksimaalse arvu, mida operatsiooniressurss suudab ühes käituses töödelda.
-   **Efektiivsusprotsent** – saate määrata operatsiooniressurssi oodatava efektiivsuse. Efektiivsusprotsent reguleerib operatsiooniressursside läbilaskevõimet ja mõjutab ressursile reserveeritud aega. Selle järgi reguleeritakse ka operatsiooniressurssi kasutavate operatsioonide täitmisaegu. Arvutamiseks kasutatakse järgmist valemit: planeerimisaeg = aeg × 100 ÷ efektiivsusprotsent. Selles valemis hõlmab *aeg* nii käitamisaega kui ka häälestusaega.
-   **Operatsioonide planeerimise protsent**– saate määrata operatsioonide planeerimisel kasutatava operatsiooniressursi suurima võimsuse protsendi. Tööde planeerimisel paindliku võimsuse lubamiseks peaks selle väärtus olema väiksem kui 100 protsenti.
-   **Piiratud võimsus** – seadke see suvandile **Jah**, kui operatsiooniressurss tuleks planeerida tegeliku saadavaloleva võimsuse alusel ja kui arvesse tuleks võtta olemasolevaid võimsuse reserveeringuid. Kui valitud on suvand **Ei**, siis eeldatakse, et operatsiooniressursil on piiramatu võimsus, mistõttu ressurss võib olla üle broneeritud.
-   **Piiratud omadus** – seadke see suvandile **Jah**, kui soovite operatsiooniressursi planeerida nõutava tööaja planeerimise omaduste suhtes saadaoleva tegeliku võimsuse alusel.
-   **Välistav** – seadke see suvandile **Jah**, kui te ei soovi, et operatsiooniressurss oleks kättesaadav teisele tööle või operatsioonile, kuni praegune tootmine on lõpule jõudnud. Sellisel juhul ei saa operatsiooniressurssi saa kasutada isegi siis, kui ressursi käitusajal esineb pause.
-   **Kitsaskohana toimiv ressurss** – saate määratleda operatsiooniressursi kitsaskohana toimiva ressursina. Kitsaskohana toimivat ressurssi planeeritakse piiratud võimsusega ressurssi kasutades, kui lehel **Koondplaanid** on valitud suvandid **Piiratud võimsus** ja **Kitsaskoha planeerimine**.

Selleks et planeerida mitme operatsiooniressurssi samaaegne toimimine (nt tootmisoperatsioon) peate määrama erinevate ressursside nõuded, kasutades esmaseid ja teiseseid operatsioone. Seejärel saate reserveerida mitu erinevate võimsusega operatsiooniressurssi. Esmase operatsiooni jaoks planeeritud operatsiooniressurss määravad tegevuse kestuse.

## <a name="lean-work-cells"></a>Säästlikud töörakud
Saate määrata ressursigrupi säästlikuks töörakuks. Seejärel saab ressursigrupp olla tootmisvoo osa. Ressursigrupi määramisega säästlikuks töörakuks saate ka takistada ressursigrupi ja määratud operatsiooniressursside eraldamist tootmistellimuse või projekti tunnieelarve operatsioonidele. Iga ressursigrupi puhul, mis toimib säästliku töörakuna, peate määrama järgmise teabe.

-   **Kalender** – tööraku, millel peab olema standardse tööpäeva omadus, töökalender.
-   **Sisendladu ja asukoht** – tegevuse jaoks materjali komplekteerimiseks kasutatav vaikeasukoht.
-   **Väljundladu ja asukoht** – vaikeasukoht, kuhu pannakse kogu tööraku väljund.
-   **Käitusaja kulukategooria** – see kategooria peab olema tööraku jaoks määratletud, kui kuluarvutuses jälgitakse otsest tööjõudu.

Ressursigrupi kasutamisel säästliku töörakuna määratakse tööraku võimsus otse ressursigrupis. Seetõttu ei pea te operatsiooniressursse ressursigrupile määrama. Töörakule tuleb määrata operatsiooniressurss tüübiga **Hankija** ainult siis, kui töörakku haldab allhankija. Kui määrate operatsiooniressursi ressursigrupile, mis on märgitud töörakuna, ei mõjuta see tööraku võimsust.

## <a name="costing-resources"></a>Kuluarvutuse ressursid
Kui määrtlete tegevuse, nagu protsessioperatsioon või projekti tunnieelarve, saate määrata konkreetse operatsiooniressursi või ressursigrupi nõude. Siiski saate määrata ka kindlat tüüpi operatsiooniressursi või teatud võimsuse või pädevusega operatsiooniressursi nõude. Sel põhjusel ei tehta tegelikku ressursimääramist enne, kui tegevus on planeeritud ja võimsus reserveeritud. Seetõttu saate protsessioperatsioonis määrata, et hinnang ja koosluse arvutus peavad põhinema konkreetsel operatsiooniressursil. Seda operatsiooniressurssi nimetatakse kuluarvutuse ressursiks. Saate kulukategooriaid ja operatsiooniaegu ka kuluarvutuse ressursist tegevusse üle kanda. Operatsiooni planeerimisel toimub hindamine ja koosluse arvutus juba planeeritud operatsiooniressurssi kasutades.




