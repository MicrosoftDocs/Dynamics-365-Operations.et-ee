---
title: Koosluse arvutusgrupid
description: Selles artiklis antakse teavet koosluste arvutusgruppide ja nende seadistamise kohta. Koosluse arvutuse käivitamiseks tuleb seadistada arvutusgrupid ja määrata need eraldi üksustele või määrata vaike-arvutusgrupp. Arvutusgrupi arvutussätteid kasutatakse siis koosluse arvutamise ajal lehel Koosluse arvutamine vaikeväärtustena.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcGroup, BOMCalcTable, BOMCalcTrans, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94063
ms.assetid: 63e1b7dc-c2c5-41b0-81ed-e3e02d1b39e0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce954b61b4d6a12f2bc62a71ef2e1bc69732a4c0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813287"
---
# <a name="bom-calculations-groups"></a>Koosluse arvutusgrupid

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet koosluste arvutusgruppide ja nende seadistamise kohta. Koosluse arvutuse käivitamiseks tuleb seadistada arvutusgrupid ja määrata need eraldi üksustele või määrata vaike-arvutusgrupp. Arvutusgrupi arvutussätteid kasutatakse siis koosluse arvutamise ajal lehel Koosluse arvutamine vaikeväärtustena. 

Lehel **Varude ja laohalduse parameetrid** on vajalik vaike-arvutusgrupp või lehel **Väljastatud toote üksikasjad** on vajalik tootepõhine arvutusgrupp. Süsteem otsib kõigepealt lehel **Väljastatud toote üksikasjad** seadistatud arvutusgruppi. Kui ta sealt arvutusgruppi ei leia, otsib ta seda lehelt **Varude ja laohalduse parameetrid**. Kui süsteem arvutusgruppi ei leia, saab kasutaja arvutamise käigus tõrketeate. Arvutusgrupp sisaldab omahinna mudeli ja müügihinna mudeli poliitikaid ning hoiatuste kontroll-loendit. Arvutusgrupi arvutussätteid kasutatakse koosluse arvutamise ajal lehel **Koosluse arvutamine** vaikeväärtustena.

## <a name="purposes-of-bom-calculation-groups"></a>Koosluse arvutusgruppide eesmärgid
Koosluse arvutusgrupp võidakse kaupadele määrata mitmel põhjusel.

-   Välja **Omahinna mudel** seadistamisega näitate toodetud kauba plaanitud kulu arvutamise käigus ostetud komponendi kulu panuse andmeallikat. Mõned tootjad arvutavad plaanitud kulusid, kasutades ostetud komponentide ostuhinna kaubandusleppeid või muud alust, näiteks ostuhinna kirjeid kuluversioonis.
-   Välja **Müügihinna mudel** seadistamisega näitate, kuidas kauba andmeid soovitatava müügihinna arvutamiseks kasutatakse. Saate määrata kauba müügihinna või kulugrupi. Mõned tootjad soovivad arvutada soovitatava müügihinna toodetud kaupadele. Arvutatud müügihind võib kajastada alamhinna lähenemist komponendi müügihinna kirje põhjal. Teise võimalusena võib arvutatud müügihind kajastada kulupõhise hinnalisandi lähenemist, mis põhineb komponendi kulul ja rakendataval kasumiprotsendil, mis on seostatud kauba kulugrupiga.
-   Välja **Peata koosnevusarvutus** abil näitate, et toodetud kaupa tuleb koosluse arvutamisel käsitleda kulu hinnalisandi tähenduses ostetud kaubana. Tüüpilised stsenaariumid hõlmavad ostetud kaupa, mida on aeg-ajalt toodetud või toodetud kaupa, mida parajasti ostetakse. Esmalt määratakse kaup koosluse- ja protsessiteabe määramiseks ning kauba tootmistellimuste toetamiseks toodetavaks kaubaks. Kuid lipp **Peata koosnevusarvutus** takistab kuluarvutustel kauba koosluse ja protsessi kasutamist. Selle asemel kasutab koosluse arvutus kauba määratud kulusid.

## <a name="calculation-groups"></a>Kalkulatsioonigrupid
Arvutusgrupid saab määratleda kuluhalduse mooduli jaotises **Eelmääratud kulupoliitikate seadistus**. Kaupadele määratud arvutusgrupid võimaldavad määrata, kuidas komponentide kulu või müügihind (nagu arvutusgrupis näidatud) arvutuse jaoks hangitakse. Lehel **Arvutusgrupid** saate määratleda omahinna mudeli, alternatiivse omahinna mudeli, müügihinna mudeli ja hoiatused.

### <a name="cost-price-model"></a>Omahinna mudel

Väljal **Omahinna mudel** on neli võimalust.

-   **Kauba omahind** – omahinnana kasutatakse omahinda tabelist **Väljastatud toode** või kauba dimensioonide kombinatsiooni.
-   **Kauba ostuhind** – kasutage ostuhinda väljalt **Omahind** vahekaardil **Ost** lehel **Väljastatud toodete loend**.
-   **Kaubanduslepped** – saate konfigureerida kaubandusleppeid teatud kaupade kombinatsioonide ja hankijate või konkreetsete laoalade kohta. Siis, kui teete siin valiku **kaubanduslepped**, kasutatakse kaubanduslepet, mille ostuhinnale lõite, koos kauba ja laoalaga.
-   **Laohind** – koosluse arvutuse ühikuhinna arvutamiseks kasutatakse kauba kehtivat laoväärtust. Ühiku omahind arvutatakse sinult juhul, kui sisestatud kogus ja füüsiline kogus on rohkem kui 0 (null).

### <a name="alternative-cost-price"></a>Alternatiivne omahind

Väljal **Alternatiivne omahind** on samad valikud, mis väljal **Omahinna mudel**. Kuid seda välja kasutatakse ainult siis, kui peamisest omahinna mudelist ei õnnestu hinda leida.

### <a name="sales-price-model"></a>Müügihinna mudel

Välja **Müügihinnad** arvutamiseks on kaks võimalust.

-   **Kulugrupp** – kui on tehtud see valik, arvutatakse müügihind omahinna ja kasumisätte protsendi põhjal kulugrupist.
-   **Kauba müügihind** – kui on tehtud see valik, kasutatakse müügihinda tabeli Väljastatud toode kiirkaardilt **Müük**.

### <a name="stop-explosion"></a>Peata koosnevusarvutus

Märkeruutu **Peata koosnevusarvutus** kasutatakse näitamiseks, millal toodetud kaupa tuleks kohelda ostetud kaubana. Tavaliselt jäetakse märkeruut **Peata koosnevusarvutus** tühjaks. Selle ruudu märkimisel näitate, et toodetud kaupa tuleb käsitleda koosluse arvutamiseks toodetud komponendi asemel ostukomponendina. Olenevalt laoalast saab kauba kulu siiski koosluse arvutuste abil arvutada. Plaanitud ostutellimuste ja tootmistellimuste koosnevusarvutus peatatakse koosluse juures, mille komponendid on seotud kalkulatsioonigrupiga, millel märkeruut **Peata koosnevusarvutus** on valitud. Koondplaneerimine loob plaanitud tellimused kooslusel endal, mitte koosluses sisaldavatel kaupadel. Põhimõtteliselt määrate selle ruudu märkimisel, et kulu ei lisata koosluse arvutusse nende kaupade puhul, millel on see arvutusgrupp.

### <a name="warnings"></a>Hoiatused

Kiirkaardil **Hoiatused** saate teha valikud igasuguste hoiatusteadete kohta, mille kasutajad peaksid saama, kui nad koosluse arvutusi teevad. 

Näiteks kui märgite ruudu **Kooslust pole**, saab kasutaja hoiatuse, kui mõne komponendi või põhiüksuse puhul, mille koosluse arvutust käitatakse, ei leita ühtegi aktiivset koosluse versiooni. Kui märgite ruudu **Marsruut puudub**, saab kasutaja hoiatuse, kui ühtegi aktiivset marsruudi versiooni ei leita. Kui kasutate marsruutidel ja toimingutes ressursse, võite juhendada süsteemi neid ressursse otsima. Siis, kui aktiivse marsruudi igal real ressurssi ei leita, saab kasutaja hoiatuse. 

Samuti saate kinnitada ja kontrollida tarbimist. Tarbimine on konkreetse marsruudi kogus. Tavaliselt kajastab see aja hulka, mis on vajalik tootmisprotsessi konkreetse toimingu tegemiseks. Saate kontrollida, kas kaubal puudub omahind. Kui kaubal pole aktiivset omahinda, ei lisata koosluse arvutusse kulu. 

Samuti saab omahinna vanust kontrollida ja kinnitada. Näiteks sisestage **60**, näitamaks, et ühiku omahind tuleb 60 päeva pärast ümber hinnata. Kui see piir on saavutatud, annab süsteem hoiatuse. Näiteks oletame, et kaubale sisestati omahind selle aasta jaanuaris. Kui praegu on august, mis on rohkem kui 60 päeva pärast omahinna sisestamist, saab kasutaja koosluse arvutuse käivitamisel hoiatuse. Võite sisestada protsendi väljale **Minimaalne brutokasum**. See väärtus näitab punkti, kus minimaalne brutokasum pole nõuetekohane. Kui konkreetse komponendi brutokasum pole nõuetekohane, saab kasutaja hoiatuse. Seega aitab see väli tagada, et kaupade puhul vajalikke kulusid ja täiendavaid veokulusid liigselt ei kärbitaks.

### <a name="default-setup-in-inventory-and-warehouse-management-parameters"></a>Vaikeseadistus varude ja laohaldusmooduli parameetrites

Kuna arvutusgrupid on arvutuste tegemiseks nõutavad, tuleb laohalduse parameetrite moodulis seadistada vaike-arvutusgrupp. See seadistus võimaldab ettevõtetel kasutada kõigi kaupade puhul standardset kulugrupi ja kasumi seadistust. Siis, kui konkreetsel kaubal on arvutamise erinõuded, saab kasutaja määrata sellele kaubale teise arvutusgrupi. Tavaliselt saate määrata arvutusgruppe kooslusekaupade asemel koosluse koostiskaupadele. Kuid kui kuvatakse hoiatusteated, saab arvutusgruppe rakendada. Kaupadele määratud arvutusgrupp alistab laohalduse parameetrites seadistatud vaikeväärtuse. 

Vaikeparameetri saate seadistada asukohas **Kuluhaldus** &gt; **Laoarvestuse poliitikate seadistus** &gt; **Parameetrid** &gt; **Laoarvestus** &gt; **Arvutusgrupp**. Vaikekonfiguratsioonigrupi seadistamisega saate konfigureerida ka hoiatamistingimusi, mis kasutajatele koosluse arvutusprotsessi ajal teateid kuvavad, kui valitud komponendid võiksid põhjustada arvutusvigu.

### <a name="view-warning-messages-on-the-complete-page"></a>Hoiatusteadete vaatamine lehel Lõpetatud

Koosluse arvutus loob hoiatusteated. Saate vaadata valitud kauba hoiatusi. Näiteks looge jaotises Müük ja turundus uus müügitellimus kaubale D0001. Seejärel klõpsake müügitellimuse rea menüüs **Uuenda rida** valikut **Arvuta koosluse/valemi põhjal** arvutuse üksikasjade ja hoiatuste vaatamiseks. Koosluse arvutustulemusi saab vaadata ka lehel **Lõpule viidud**. Hoiatusteadete puhul puudutab toodetud kaupu ainult kaks hoiatustingimust, samas kui kõigile kaupadele kehtib neli hoiatustingimust.
-   Tuvastage, kui toodetud kaubal puudub aktiivne kooslus.
-   Tuvastage, kui toodetud kaubal puudub aktiivne protsess.
-   Tuvastage, kui kaubal on koosluse real koguseks 0 (null).
-   Tuvastage, kui kaubal on koosluse real kuluks 0 (null) või kui sellel puudub kulukirje.
-   Tuvastage, kui kaubal on koosluse real aegunud kulu. Hoiatus kajastab võrdlust määratud kuupäevadele arvutamiskuupäeva kulu maksimaalse vanusega.
-   Tuvastage hoiatus, kui kaubal on koosluse real väiksem kasumiprotsent, kui soovite.

Saate määratleda mitu koosluse arvutusgruppi, olenevalt hoiatusteadete variatsioonide vajadustest. Näiteks üks koosluse kalkulatsioonigrupp, millel on hoiatustingimused aktiivse koosluse, komponendikoguse 0 (null) ja komponendi kulu 0 (null) kohta, võib olla piisav. Koosluse arvutuse alustamisel saate koosluse arvutusgrupiga seotud hoiatustingimusi alistada. Saate hoiatustingimusi ka lisada või eemaldada. Näiteks kui praegune olukord ei hõlma marsruudi andmeid, võite aktiivse marsruudi hoiatustingimuse eemaldada. **Märkus.** Moodulis Kellaaeg ja kohalolek on leht **Arvutusgrupid**, kuid sellel lehel pole koosluse arvutusgruppidega mingit seost. Moodulis Kellaaeg ja kohalolek saab töötajaid määrata arvutusgruppidesse, mis kajastavad sama ülevaataja või juhiga seotud töötajate grupeerimist. Töötajate registreerimiste arvutusi saab ülevaataja või juht teha kas automaatselt või käsitsi.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]