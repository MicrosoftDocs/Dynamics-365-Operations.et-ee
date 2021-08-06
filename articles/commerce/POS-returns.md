---
title: Tagastuste loomine müügikohas
description: See teema kirjeldab, kuidas käivitada kassarakenduses sularaha- ja käsirahakannete tagastamine Microsoft Dynamics 365 Commerce Point of Sale (POS) rakendustes.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.20
ms.openlocfilehash: 53cad70e2c4866a18427157bc8b7fa1c3fda4daa
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638141"
---
# <a name="create-returns-in-pos"></a>Tagastuste loomine müügikohas

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas käivitada kassarakenduses sularaha- ja käsirahakannete tagastamine Microsoft Dynamics 365 Commerce müügikoha (POS) rakendustes.

> [!NOTE]
> Commerce version 10.0.20 väljalaskes ja hilisemas versioonis on saadaval uus funktsioon nimega **Ühtne tagastuse töötlemise kogemus kassas**. See funktsioon pakub järjepidevama ja ühtsema tagastusprotsessi kassas, sõltumata kande tüübist (sularaha- ja kande- või klienditellimus) või algsest kanalist, kus tellimus loodi. Soovitame, et kõik organisatsioonid lülitaks selle uue funktsiooni sisse, et parandada kassa kaudu tagastamise töötlemise üldist usaldusväärsust.
>
> Kui funktsioon on sisse lülitatud, ei saa seda välja lülitada.

## <a name="process-returns-by-using-the-return-transaction-operation"></a>Tagastuste protsess tagastuskande toimingut kasutades

Soovitame teil tagastuskande toimingu lisada [kassa ekraani](pos-screen-layouts.md). Väljalasetel enne Commerce'i versiooni 10.0.20 väljalaset toetab tagastuskande toiming õigesti tagastamist ainult sularaha- ja ülekandekannete puhul. Kui olete äriversiooni **kassa funktsiooni ühtne tagastustöötlus** 10.0.20 väljalaskes või hiljem sisse lülitanud, toetab tagastamiskande toiming ka klienditellimustest tulenevaid tagastuste töötlemisi, nt juba arveldatud "järele tulemist" või "kodudesse lähetamise" tellimusi.

Tagastuskande toimingust saavad kasutajad otsida sularaha- ja ülekandekannet või kliendi tellimust, mille suhtes tagasi pöörduda, sisestades mis tahes järgmisest neljast otsingukriteeriumist. Kasutajad saavad sisestada need kriteeriumid seadme klaviatuuri, ekraani võtmeklahvistiku või vöötkoodiskanneri abil.

- Kviitungi ID
- Tellimuse kood
- Kanaliviite ID (tuntud ka kui tellimuse kinnituse ID)
- Arve ID

Kui leitakse otsingukriteeriumega kattuv kanne või tellimus, kuvatakse lehekülg **Tagastatavad tooted**. Kasutajad saavad määrata tagastatavad kaubad. Samuti saavad nad sisestada tagastuskoguseid ja põhjusekoode.

Iga tagastatavate toodete loendis oleva tellimuse rea puhul näitab müügikoht teavet algse ostukoguse ja eelnevalt töödeldud tagastuste koguste kohta. Tagastuskogus, mille kasutaja tellimusereale sisestab, peab olema väiksem või võrdne kui väli **Tagastuseks saadav**.

![Tagastatavate toodete leht.](media/returnslist.png)

Kui kasutajal on tagastuse töötlemisel füüsiline toode ja tootel on vöötkood, saab kasutaja tagastuse registreerimiseks vöötkoodi skannida. Iga vöötkoodi skannimine suurendab tagastatud kogust ühe kauba kaupa. Kui vöötkoodi sildil on manustatud kogus, sisestatakse kogus väljale **Tagastamine nüüd**.

Kasutajad saavad ka käsitsi valida kaupu, mida **tagastatavate toodete** lehel tagastada ja seejärel värskendada välja **Tagastamine kohe** kasutades parempoolset üksikasjade paani.

Kui kandele on määratud maksimaalne **Tagasta nüüd** kogus, saab kasutaja valida kassa rakenduse ribal suvandi **Vali kõik**, et määrata maksimaalne tagastatav kogus ridadel.

Iga rea puhul, millel on **Tagasta praegul** kogus, peab kasutaja valima üksikasjapaneeli abil tagastuspõhjuse koodi. Sularaha- ja kandetagastuste puhul konfigureeritakse tagastuspõhjuste koodid kaupluse funktsiooniprofiilis teabekoodidega. Klienditellimuste tagastuste puhul konfigureeritakse **Tagastuspõhjuste koodid** Dynamics 365 Commerce peakontori lehel.

Kui tagastuskogus ja põhjuse kood on igale tagastatavale kaubale määratud, saab kasutaja töötlemise jätkamiseks valida kassa rakenduse ribalt toimingu **Tagasta**. Ilmub müügikoha kandeleht, kuhu eelmisel lehel valitud tagastatavad kaubad on ostukorvi lisatud. **Tagasta kohe** kaupade kogused kuvatakse kandel negatiivse koguse ridadena ja arvutatakse kogu tagasimakse.

Kasutajad saavad tagastuskandele ridu lisada, kui nad loovad vahetustellimuse. Kasutajad saavad tagastamiskandele lisada ka sihtotstarbelilisi tagastusüksusi, kasutades toimingut **Tagasta toode** positiivses koguses müügirea puhul, mis on lisatud.

> [!NOTE]
> **Tagastatud toote** toiming müügikohas ei kinnita ühtegi algset kannet ja võimaldab mis tahes toote tagastamist. Seetõttu on soovitatav, et seda operatsiooni tohivad teha ainult volitatud kasutajad, või et operatsiooni kasutamisel on nõutav juhataja kontroll.

Kui tagasimakse tähtaeg on maksmisel, saavad organisatsioonid konfigureerida [tagasimakse maksepoliitikaid](refund_policy_returns.md) mida saab kasutada klientidele tagastamiseks. Kui originaalkande eest tasuti krediitkaardiga, sõltuvalt makseprotsessorist ja süsteemi konfiguratsioonist, võib kasutajatel olla võimalus [kanda tagasi originaalkaardile](dev-itpro/linked-refunds.md). Sel juhul saab tagasimakset töödelda ilma, et klient peaks uuesti krediitkaarti kasutama. Algset makseluba kasutatakse tagasimakse väljastamiseks.

## <a name="other-return-options-in-pos"></a>Muud tagastusvalikud müügikohas

Kui **ühtse tagastuse töötlemise kogemus kassas** funktsioon on sisse lülitatud, saavad kasutajad kasutada ka kassa töölehe **toimingu näitamist**, et algatada tagastamine sularaha- ja ülekandekannete või klienditellimuste puhul. Seejärel saavad nad valida töölehel kande ja valida **Tagasta** kassa rakenduseribalt toimingu . Toiming on saadaval ainult juhul, kui tellimusel on tagastatavaid ridu. See käivitab sama kasutajakogemuse kui **tagastamiskande** toiming.

Kasutajad saavad kassas kasutada ka **tellimuse tagasikutsumise** toimingut klienditellimuste otsimiseks ja tagasikutsumiseks. (Seda toimingut ei saa kasutada sularaha- ja kandekannete puhul). Sellisel juhul saab pärast kliendi tellimuse valimist kasutada kassa rakenduseribal tagastustoimingut, et algatada kliendi tellimuse **Tagastus**. Toiming on saadaval ainult juhul, kui tellimusel on tagastatavaid ridu. See käivitab sama kasutajakogemuse kui **tagastamiskande** või **Näita arveraamatut** toiming.

## <a name="return-orders-are-posted-to-commerce-headquarters-as-sales-orders"></a>Tagastustellimused sisestatakse müügitellimustena teenusesse Commerce Headquarters 

Kui **ühtne tagastuse töötlemise kogemus kassas** funktsioon on sisse lülitatud, kirjutatakse kõik kassas loodud tagastused Commerce Headquartersi kui negatiivsete ridadega müügitellimused. Väljaanded enne Commerce version 10.0.20 väljalaset saavad kasutajad valida, kas tagastustellimused tuleks sisestada müügitellimustena, mille negatiivsed read on negatiivsed, või kas need peaksid olema tagastustellimused, mis luuakse tagastatud kauba autoriseerimise (RMA) protsessi kaudu. 

Kassa funktsioonis **ühtne tagastustöötluse kogemus** on aegunud võimalus kasutada RMA protsessi tagastuste loomiseks. Kui see funktsioon on sisse lülitatud, luuakse kõik tagastused negatiivsete ridadega müügitellimustena.

## <a name="offline-return-processing-improvements"></a>Võrguühenduseta tagastustöötluse parendused

Enamasti püüab süsteem kassas tagastuse töötlemisel teha reaalajas teenuse (RTS) kutse Commerce Headquartersisse, et kontrollida praegusi tagastamiseks saadaolevaid koguseid. Selline kinnitamine aitab ennetada petturlikku stsenaariumi, kus klient proovib tagastada sama kaupa mitmes asukohas.

Et käsitleda olukordi, kus RTS-i kõnet ei saa võrgu- või ühenduvusprobleemide tõttu teha, on protsess esitatud commerce headquarters`is tagastatud koguse andmete perioodiliseks sünkroonimiseks kaupluse kanali andmebaasi. Kanalipoolse tagastuse jälitamine aitab tagada, et **Saadaval tagastuseks** kogused kassas kuvatakse mõistlikult täpselt, isegi kui kassa on võrguühenduseta. See tagab ka selle, et müügikoht saab jätkata kanalipoolse teabe valideerimist, et petturlike tagastusi ära hoida.

Ühenduseta tagastusprotsessi sobival viisil kasutamiseks peaksid organisatsioonid planeerima **tagastuskoguste uuendamist** Commerce Headquartersis sageli. Soovitame seda tööd käitada samal sagedusel kui P-tööd, mis tõmbab ärikanalites uued kanded Commerce Headquartersi.

**Tagastuskoguste värskendamise** töö arvutab koguse, mis on saadaval kõikide rakenduse Commerce Headquarters`is leitud müügitellimuste tagastamiseks. Andmed, mida töö arvutab, tuleb seejärel saata kanali andmebaasidesse, et kaupluse kanaleid saaks värskendada. **Tagastuskoguste** (1200) jaotustööd kasutatakse sel eesmärgil. Kuna tagastatava koguse andmed sünkroonitakse Commerce Headquartersist, kui tagastust töödeldakse müügikohas, kuid RTS-i ei saa teha, saab kassa kasutada kanalipoolset tagastusteavet, et kontrollida antud müügirea puhul **Tagastamiseks saadaolevaid** koguseid.

Kui RTS-i kõnesid ei saa teha ja kassa kasutab tagastuse registreerimisel kanalipoolseid andmeid, teavitab hoiatusteade kasutajaid, et loovad "võrguühenduseta" tagastuse. Seetõttu on nad kursis, et müügikohas kuvatav **Tagastatav kogus** võib olla lõppkuupäevast väljas ja ei pruugi enam täpne olla, sõltuvalt sellest, millal viimati **tagastuskoguste värskendamise** töö kanaliga töödeldi ja sünkrooniti.

Näiteks, klient töötles hiljuti tellimuserea tagastust teises kanalis, kuid need andmed pole veel kanali andmebaasidega sünkroonitud **tagastuskoguste värskendamise** töö kaudu. Klient läheb siis teise kauplusesse ja proovib sama kaupa uuesti tagastada. Sel juhul võimaldab kassa kauba uuesti tagastada, kui kauplus ei saa teha RTS-kõnet Commerce Headquarters`isse reaalajas tagastusandmete kogumiseks. Kasutajat hoiatatakse, et tagastuse kinnitamiseks kasutatav teave võib olla lõppkuupäevast väljas. Teade, mille kasutaja saab, on ainult hoiatusteade. See ei takista kasutajat tagastuse töötlemisega jätkamist.

Kui kanali poolne teave ei ole mõnel põhjusel uuendatud ja ühenduseta tagastus töödeldakse koguse kohta, mis ületab tegeliku **Tagastuseks saada oleva** koguse võib rakenduse Commerce headquarters kande loomiseks luua tõrke.

> [!NOTE]
> Kui **ühtne tagastuste töötlemise kogemus kassas** funktsioon on sisse lülitatud, muutuvad kättesaadavaks uued valikulised funktsioonid, mis toetavad seeriaks jaotatud toote tagastuste kinnitamist. Lisateavet vt [müügikohas (POS) jaotisest Seerianumbriga kontrollitud toodete tagastus](POS-serial-returns.md).

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Luba osalise kogusega tagastuste korral nõuetekohane maksuarvutus

Funktsioon tagab selle, et kui tellimus tagastatakse mitme arvega, võrduvad maksud lõpuks algselt tasutud maksusummaga.
1.  Avage tööruum **Funktsioonihaldus** ja otsige märksõna **Luba osalise kogusega tagastuste korral nõuetekohane maksuarvutus**.
2.  Valige **Luba osalise kogusega tagastuste korral nõuetekohane maksuarvutus** ja klõpsake seejärel nuppu **Luba**.


## <a name="additional-resources"></a>Lisaressursid

[Tagasta seerianumbriga kontrollitud tooted kassas](POS-serial-returns.md)

[Eelnevalt kinnitatud ja kinnitatud kannete lingitud tagasimaksed](dev-itpro/linked-refunds.md)

[Kanali tagastuste ja tagasimaksete poliitika loomine ja värskendamine](refund_policy_returns.md)

[Kassa kasutajaliidese visuaalsed konfiguratsioonid](pos-screen-layouts.md)
