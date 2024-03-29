---
title: Väljavõtte sisestamise funktsiooni täiustused
description: See artikkel kirjeldab väljavõtte sisestamise funktsiooni tehtud parendusi.
author: analpert
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: 33b4f17cd46338b62bed96f0a285e7b9634cc87a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067815"
---
# <a name="improvements-to-statement-posting-functionality"></a>Väljavõtte sisestamise funktsiooni täiustused

[!include [banner](includes/banner.md)]

See artikkel kirjeldab väljavõtte sisestusfunktsioonis tehtud esimest parenduste komplekti. Need parendused on saadaval Microsoft Dynamics 365 Finance 7.3.2.

## <a name="activation"></a>Aktiveerimine

Vaikimisi on programm finantside ja toimingute 7.3.2 juurutamisel seadistatud kasutama väljavõtte sisestustes pärandfunktsiooni. Täiustatud väljavõtte sisestamise funktsiooni lubamiseks peate sisse lülitama selle konfiguratsioonivõtme.

- Avage **Süsteemihaldus** \> **Seadistamine** \> **Litsentsi konfiguratsioon** ja seejärel tühjendage sõlmes **Jaemüük ja kaubandus** märkeruut **Väljavõtted (pärand)** ja valige märkeruut **Väljavõtted**.

Kui sisse on lülitatud uus konfiguratsioonivõti **Väljavõtted**, on saadaval uus menüükäsk nimega **Väljavõtted**. Selle menüükäsuga saab väljavõtteid käsitsi luua, arvutada ja sisestada. Selle menüükäsu kaudu on saadaval ka kõik väljavõtted, mis põhjustavad pakettsisestuse protsessi kasutamisel tõrke. (Kui sisse on lülitatud konfiguratsioonivõti **Väljavõtted (pärand)**, on saadaval menüükäsk nimega **Avatud väljavõtted**.)

Rakenduses Commerce on järgmised nende konfiguratsioonivõtmetega seotud kontrolltoimingud.

- Mõlemat konfiguratsioonivõtit ei saa korraga sisse lülitada.
- Konkreetse väljavõtte elutsükli jooksul (loomine, arvutamine, sisestamine jne) tehtavate kõikide toimingute jaoks tuleb kasutada sama konfiguratsioonivõtit. Näiteks ei saa luua ja arvutada väljavõtet, kui konfiguratsioonivõti **Väljavõte (pärand)** on sisse lülitatud, ja üritada sama väljavõtet sisestada konfiguratsioonivõtmega **Väljavõte**.

> [!NOTE]
> Soovitame kasutada konfiguratsioonivõtit **Väljavõtted** väljavõtte sisestamise täiustatud funktsiooni jaoks, kui teil pole just mõjuvat põhjust kasutada konfiguratsioonivõtit **Väljavõtted (pärand)**. Microsoft investeerib ka edaspidi uude ja täiustatud väljavõtte sisestamise funktsiooni ning on oluline, et te esimesel võimalusel sellele üle läheksite, et sellest kasu saada. Väljavõtte sisestamise pärandfunktsioon on aegunud alates väljaandest 8.0.

## <a name="setup"></a>Seadistamine

Väljavõtte sisestamise funktsiooni täiustuste osana on lehe **Commerce’i parameetrid** vahekaardi **Sisestamine** kiirkaardile **Väljavõte** lisatud kolm uut parameetrit.

- **Väljavõtte tühjendamise keelamine** – see suvand kehtib ainult väljavõtte sisestamise pärandfunktsioonile. Soovitame selle suvandi seada valikule **Ei**, et kasutajad ei saaks tühjendada väljavõtteid, mille sisestamine on pooleli. Kui tühjendatakse väljavõtteid, mille sisestamine on pooleli, muutuvad andmed vigaseks Seadke see suvand valikule **Jah** ainult erandolukorras.
- **Varude reserveerimine arvutamisel** – soovitame kasutada pakett-tööd **Varude sisestamine** varude reserveerimiseks ja seada selle suvandi valikule **Ei**. Kui see suvand on seatud valikule **Ei**, ei ürita väljavõtte sisestamise täiustatud funktsioon luua varude reserveerimise kirjeid arvutamise ajal (kui kirjeid pole juba loodud pakett-töö **Varude sisestamine** ajal). Selle asemel loob funktsioon varude reserveerimise kirjed ainult sisestamise ajal. See rakendus on kujundusealane valik ja selle tegemisel lähtuti sellest, et ajavahe arvutamise ja sisestamise protsessi vahel on enamasti väike. Kui aga soovite reserveerida varusid arvutamise ajal, võite suvandi seada valikule **Jah**.

    Väljavõtte sisestamise pärandfunktsioon reserveerib varud väljavõtte arvutamise protsessi ajal (kui reserveerimist pole juba tehtud pakett-töö **Varude sisestamine** kaudu), olenemata selle suvandi sättest.

- **Inventuuri keelamine on nõutav** – kui see suvand on seatud valikule **Jah**, jätkub väljavõtte sisestamise protsess, isegi kui väljavõttel oleva loendatud summa ja kandesumma vaheline erinevus jääb väljapoole läve, mis on määratud poe kiirkaardil **Väljavõte**.

> [!NOTE]
> Rakenduse Commerce version 10.0.14 **vabastamisel, kui jaemüügiväljavõtted –** kaupluste kanali funktsioon on lubatud, **ei** ole varude sisestamise pakett-töö enam rakendatav ja seda ei saa käitada.

## <a name="processing"></a>Töötlemisel

Väljavõtteid saab arvutada ja sisestada partiina, kasutades menüükäske **Väljavõtete arvutamine partiina** ja **Väljavõtete sisestamine partiina**. Väljavõtteid on võimalik ka arvutada ja sisestada, kasutades menüükäsku **Väljavõtted**, mida väljavõtte sisestamise täiustatud funktsioon pakub.

Väljavõtte partiina arvutamise ja sisestamise protsess ja etapid on samad kui väljavõtte sisestamise pärandfunktsioonis. Kuid olulisi täiustusi on tehtud väljavõtete tuuma tagavaratöötlemises. Need täiustused muudavad protsessi paindlikumaks ning annavad parema ülevaate olekute ja tõrgete teabest. Seetõttu võivad kasutajad tegeleda tõrgete juurpõhjusega ja seejärel jätkata sisestamise protsessi, ilma et andmeid rikutaks ja vaja oleks andmete parandamist.

Järgmistes jaotistes kirjeldatakse väljavõtte sisestamise funktsiooni olulisemaid täiustusi väljavõtete ja sisestatud väljavõtete kasutajaliideses.

### <a name="status-details"></a>Oleku üksikasjad

Väljavõtte sisestusprotsessi arvutamise ja sisestamise protsessis on lisatud uus olekumudel.

Järgmises tabelis kirjeldatakse arvutamise protsessi eri olekuid ja nende järjekorda.

| Olekute järjekord | Maakond      | Kirjeldus |
|-------------|------------|-------------|
| 1           | Alustatud    | Väljavõte on valmis ja arvutamiseks valmis. |
| 2           | Märgitud     | Väljavõtte ulatuses olevad kanded tuvastatakse väljavõtte parameetrite põhjal ja tähistatakse väljavõtte ID-ga. |
| 3           | Arvutatud | Arvutatakse ja kuvatakse väljavõtte read. |

Järgmises tabelis kirjeldatakse sisestamise protsessi eri etappe ja nende järjekorda.

| Etappide järjekord | Maakond                   | Kirjeldus |
|-------------|-------------------------|-------------|
| 1           | Kontrollitud                 | Tehtud on mitu parameetrite (nt likvideerimistasu) ning väljavõtte ja väljavõtte ridadega (nt erinevus loendatud summa ja kandesumma vahel) seotud kontrolltoimingut. |
| 2           | Koondatud              | Nimeliste ja nimetute klientide müügikanded koondatakse konfiguratsiooni järgi. Iga koondatud kanne teisendatakse lõpuks müügitellimuseks. |
| 3           | Klienditellimus on loodud  | Koondatud kande põhjal luuakse süsteemis müügitellimused. |
| 4           | Klienditellimuse kohta on arve koostatud | Müügitellimuste kohta on arve koostatud. |
| 5           | Sisestatud allahindlused        | Perioodiliste allahindluste töölehed sisestatakse konfiguratsiooni järgi. |
| 6           | Sisestatud tulu/kulu   | Tulu/kulu kanded on sisestatud vautšeritena. |
| 7           | Seotud kanded         | Luuakse maksete töölehed ja need seostatakse vastava arvega. |
| 8           | Sisestatud maksed         | Sisestatakse maksete töölehed. |
| 9           | Sisestatud kinkekaardid       | Kinkekaardi kanded on sisestatud vautšeritena. |
| 10          | Sisestatud                  | Väljavõte märgitakse sisestatuks. |

Iga eelolevas tabelis olev etapp on oma olemuselt sõltumatu ja etappide vahele on ehitatud hierarhiline sõltuvus. See sõltuvus liigub ülevalt alla. Kui süsteemis tekib etapi töötlemisel mõni tõrge, viiakse väljavõtte etapp tagasi eelmisse etappi. Protsessi uus test jätkub nurjunud etapist ja protsess liigub edasi. Sellel lähenemisel on järgmised eelised.

- Kasutajal on selge ülevaade etapist, kus tõrge tekkis.
- Välditakse andmete rikkumist. Näiteks väljavõtte sisestamise pärandfunktsioonis olid eksemplarid, kus mõne müügitellimuse kohta arve koostati, kuid teised jäid avatuks. Olid ka eksemplarid, kus mõnel maksete töölehel puudus tasakaalustamiseks vastav arve, kuna arve sisestamisel tekkis tõrge.
- Kasutajad näevad väljavõtte praegust etappi, kasutades nuppu **Etapi üksikasjad** väljavõtte grupis **Käivitamise üksikasjad**. Etapi üksikasjade lehel on kolm jaotist.

    - Esimeses jaotises kuvatakse väljavõtte praegune etapp koos tõrkekoodi ja üksikasjaliku tõrketeatega, kui tekkis tõrge.
    - Teises jaotises kuvatakse arvutamise protsessi eri etapid. Visuaalsed vihjed näitavad etappe, mille käivitamine on õnnestunud, etappe, mida ei saanud tõrgete tõttu käivitada, ja etappe, mida pole veel käivitatud.
    - Kolmandas jaotises kuvatakse sisestamise protsessi eri etapid. Visuaalsed vihjed näitavad etappe, mille käivitamine on õnnestunud, etappe, mida ei saanud tõrgete tõttu käivitada, ja etappe, mida pole veel käivitatud.

Peale selle kuvab teise ja kolmanda jaotise päis asjakohaste protsesside üldist olekut.

### <a name="event-logs"></a>Sündmustelogid

Väljavõte läbib mitu toimingut (nt loomine, arvutamine, tühjendamine ja sisestamine) ning väljavõtte elutsükli jooksul võidakse sama toimingut käivitada mitu korda. Näiteks pärast väljavõtte loomist ja arvutamist saab kasutaja väljavõtte tühjendada ja selle uuesti arvutada. Nupp **Sündmustelogid** väljavõtte grupis **Käivitamise üksikasjad** annab täieliku kontrolljälje väljavõttega tehtud eri toimingutest koos teabega selle kohta, millal need toimingud käivitati.

### <a name="aggregated-transactions"></a>Koondatud kanded

Sisestusprotsessi käigus koondatakse sularaha- ja kandekanded kliendi ja toote järgi. Seega vähendatakse müügitellimuste ja loodud ridade arvu. Koondkanded talletatakse süsteemis ja kasutatakse müügitellimuste loomiseks. Iga koondatud kanne loob süsteemis ühe vastava müügitellimuse. 

Kui väljavõtet ei sisestata täielikult, saate väljavõttes vaadata koondkandeid. Valige tegevuspaani vahekaardil **Väljavõte** grupi Käivitamise üksikasjad **suvand** Liidetud **kanded**.

![Koondkannete nupp väljavõtte jaoks, mis ei ole täielikult sisestatud.](media/aggregated-transactions.png)

Sisestatud väljavõtete puhul saate vaadata liidetud kandeid **lehel Sisestatud väljavõtted**. Tegevuspaanil valige **Päringud ja** seejärel valige Liidetud **kanded**.

![Sisestatud väljavõtete koondkannete käsk.](media/aggregated-transactions-posted-statements.png)

Liidetud **kande müügitellimuse** üksikasjade kiirkaart näitab järgmist teavet:

- **Kirje ID** – koondatud kande ID.
- **Väljavõtte number** – väljavõte, mille juurde koondatud kanne kuulub.
- **Kuupäev** – kuupäev, millal koondatud kanne loodi.
- **Müügi ID** – kui müügitellimus luuakse koondatud kandest, on see müügitellimuse ID. Kui see väli on tühi, ei ole vastavat müügitellimust veel loodud.
- **Koondatud ridade arv** – koondatud kande ja müügitellimuse ridade koguarv.
- **Olek** – koondatud kande viimane olek.
- **Arve ID** – kui koondatud kande müügitellimuse kohta koostatakse arve, on see müügiarve ID. Kui see väli on tühi, ei ole müügitellimuse kohta arvet veel sisestatud.
- **Tõrkekood** – see väli seatakse, kui liitmisel on vea olek.
- **Veateade** – see väli seatakse, kui liitmisel on vea olek. See näitab üksikasju protsessi nurjumise põhjuste kohta. Probleemi lahendamiseks saate kasutada tõrkekoodi teavet ja seejärel taaskäivitage protsess käsitsi. Olenevalt otsuse tüübist võib olla vaja koondmüük kustutada ja töödelda uuel väljavõttel.

![Koondkande müügitellimuse üksikasjade kiirkaardi väljad](media/aggregated-transactions-error-message-view.png)

Liidetud **kande** kande üksikasjade kiirkaart näitab kõiki kandeid, mis on koondkandesse võetud. Koondatud kande koondread kuvavad kannete koondatud kirjed. Koondread kuvavad ka üksikasjad, näiteks kauba, variandi, koguse, hinna, netosumma, ühiku ja lao. Põhimõtteliselt vastab iga koondrida ühele müügitellimuse reale.

![Liidetud kande kande üksikasjade kiirkaart](media/aggregated-transactions-sales-details.png)

Mõnel juhul võib konsolideeritud müügitellimuse sisestamine koondkannetega nurjuda. Sellises olukorras seostatakse tõrkekood väljavõtte olekuga. Ainult tõrgetega koondkannete vaatamiseks **saate ruudu märkimisega lubada kuvada ainult tõrgete kuvamise filtri koondkannete vaates**. Selle filtri lubamisega piirate tulemusi liidetud kannetega, mille tõrked vajavad lahendamist. Teavet nende tõrgete lahendamise kohta vt võrgutellimuse [redigeerimine ja auditeerimine ning asünkroonsed klienditellimuse kanded](edit-order-trans.md).

![Ainult tõrgete kuvamise filtri märkeruut koondkannete vaates.](media/aggregated-transactions-failure-view.png)

Liidetud **kannete lehel** saate alla laadida konkreetse liidetud kande XML-i, valides ekspordi **liitmisandmed**. XML-i saate üle vaadata mis tahes XML-i vormindajaga, et vaadata tegelikke andme üksikasju, mis hõlmavad müügitellimuse loomist ja sisestamist. Koondatud kannete XML-i allalaadimise funktsioon ei ole saadaval sisestatud väljavõtete jaoks.

![Liitmisandmete nupu eksportimine lehel Liidetud kanded](media/aggregated-transactions-export.png)

Kui te ei saa tõrget parandada, parandades müügitellimuse andmeid või müügitellimust toetavaid andmeid, **on** saadaval nupp Kustuta kliendi tellimus. Tellimuse kustutamiseks valige nurjunud liidetud kanne ja seejärel valige suvand **Kustuta klienditellimus**. Nii liidetud kanne kui ka vastav müügitellimus kustutatakse. Nüüd saate kandeid üle vaadata, kasutades redigeerimise ja auditeerimise funktsioone. Teise võimalusena saab neid uue väljavõtte kaudu uuesti töödelda. Kui kõik tõrked on parandatud, saate väljavõtte sisestamist jätkata, käivitades vastava väljavõtte jaoks funktsiooni Väljavõtte sisestamine.

![Kliendi tellimuse nupu kustutamine koondkannete vaates](media/aggregated-transactions-delete-cust-order.png)

Koondatud kannete vaade pakub järgmisi soodustusi.

- Kasutajal on ülevaade koondatud kannetest, mis nurjusid müügitellimuse loomise ajal, ja müügitellimustest, mis nurjusid arve koostamise ajal.
- Kasutaja näeb, kuidas kandeid koondatakse.
- Kasutajal on täielik kontrolljälg kannetest müügitellimuste ja müügiarveteni. See kontrolljälg ei olnud saadaval väljavõtte sisestamise pärandfunktsioonis.
- Liidetud XML-fail lihtsustab probleemide tuvastamist müügitellimuse loomise ja arveldamise ajal.

> [!NOTE]
> Kannete liitmisel ei ole **kandesse** määratud töötaja enam ülemise personali müügiaruandes saadaval, mis tähendab, **et** personali tipparuanne ei näita kõiki kandeid. Soovitame teil mitte kasutada ülemise personali müügiaruannet **koos** koondkannetega.

### <a name="journal-vouchers"></a>Töölehe kanded

Nupp **Töölehe kanded** väljavõtte grupis **Käivitamise üksikasjad** kuvab kõik erinevad kanded, mis on loodud väljavõtte kohta ja mis on seotud allhindluste, tulu-/kulukontode, kinkekaartide jms.

Praegu kuvab programm neid andmeid ainult sisestatud väljavõtete kohta.

### <a name="payment-journals"></a>Maksete töölehed

Nupp **Maksete töölehed** väljavõtte grupis **Käivitamise üksikasjad** kuvab kõik väljavõtte kohta loodud erinevad maksete töölehed.

Praegu kuvab programm neid andmeid ainult sisestatud väljavõtete kohta.

## <a name="other-improvements"></a>Muud täiustused

Väljavõtte sisestamise funktsioonis on tehtud muid põhitäiustusi, mida kasutajad näevad. Järgmisena on toodud mõned näited.

- Kogum ei võta arvesse personali, terminali ja vahetuse üksusi. Kuna koondparameetreid on vähe, tuleb töödelda vähem müügitellimusi.
- Tupikute tekkimist kande tabelites on vähendatud, lisades täiendavad laiendustabelid ja tehes kande tabelites värskendamise asemel sisestamise toiminguid.
- Käivitatud pakett-tööde arvu on parametriseeritud ja piiratud. Seega saab seda arvu peenhäälestada täpselt kliendi keskkonna järgi. Väljavõtte sisestamise pärandfunktsioonis loodi korraga piiramatu arv pakett-töid. Tulemuseks olid pakktöötlusserveri haldamatud koormused, ülekoormus ja ummikud.
- Väljavõtted on töötlemiseks tõhusalt järjekorda seatud, seades kõige tähtsamaks need väljavõtted, millel on maksimaalne arv kandeid.
- Pakktöötlus, näiteks **Väljavõtete arvutamine partiina** ja **Väljavõtete sisestamine partiina** käivitatakse ainult pakktöötlusrežiimis. Väljavõtte sisestamise pärandfunktsioonis said kasutajad valida pakktöötlusi interaktiivses režiimis, mis on ühe lõimega toiming, mis erineb mitme lõimega pakktöötlusest.
- Väljavõtte sisestamise pärandfunktsioonis tekitas pakktöötluse toimingu mis tahes rike tõrkeseisundi terves pakett-töös. Täiustatud funktsioonis ei tekita pakktöötluse toimingu rike pakett-töö tõrget, kui teiste pakktöötluse toimingute lõpetamine õnnestub. Peaksite hindama pakktöötluse täitmise sisestamise olekut, kasutades lehte **Väljavõtted**, kus näete väljavõtteid, mida tõrgete tõttu ei sisestatud.
- Väljavõtte sisestamise pärandfunktsioonis põhjustab väljavõtte rikke esmane tekkimine rikke terves partiis. Ülejäänud väljavõtteid ei töödelda. Täiustatud funktsioonis jätkab pakktöötlus kõikide väljavõtete töötlemist, isegi kui mõnes väljavõttes on tekkinud rike. Üks eeliseid on see, et kasutajad näevad täpset arvu, mitmes väljavõttes on tekkinud tõrge. Seega ei pea kasutajad jääma kinni tõrgete parandamise ja väljavõtete sisestamise protsessi lõpmatusse tsüklisse, kuni kõik väljavõtted on sisestatud.

## <a name="general-guidance-about-the-statement-posting-process"></a>Väljavõtte sisestamise protsessi üldised juhised

- Soovitame väljavõtte sisestamise protsessi käivitada partiina, kuna pakktöötlused kasutavad hargtöötluseks ära partii raamistiku võimsust. Hargtöötlust on vaja suure hulga kannete käsitsemiseks, mida enamasti nähakse väljavõtete sisestamisel.
- Soovitame kauba mudeligrupile sisse lülitada negatiivse füüsilise laovaru, et sisestamine oleks sujuv. Mõnel juhul ei pruugi negatiivsete väljavõtete sisestamine olla võimalik, kui negatiivne füüsiline laovaru puudub. Näiteks kui laovarus on vaid üks kauba ühik ning kaubale on tehtud müügikanne ja tagastuskanne, peaks kande sisestamine olema võimalik isegi siis, kui negatiivne laovaru pole sisse lülitatud. Kuid kuna väljavõtte sisestamise protsess tõmbab ühte klienditellimusse nii müügikande kui ka tagastuskande, siis puudub garantii, et müügirida sisestatakse esimesena ja seejärel tagastusrida. Seega võivad tekkida tõrked. Kui sellises stsenaariumis on negatiivne laovaru sisse lülitatud, ei ole kande sisestamisel negatiivset mõju ja süsteem kajastab laovaru õigesti.
- Soovitame väljavõtete arvutamisel ja sisestamisel kasutada kogumit. Seega on mõne koondparameetri jaoks soovitatavad järgmised sätted.

    - Avage **Jaemüük ja kaubandus** \> **Peakontori seadistamine** \> **Parameetrid** \> **Commerce’i parameetrid**. Seejärel valige vahekaardi **Sisestamine** kiirkaardi **Laovaru uuendamine** väljast **Üksikasjatase** suvand **Kokkuvõte**.
    - Avage **Jaemüük ja kaubandus** \> **Peakontori seadistamine** \> **Parameetrid** \> **Commerce’i parameetrid**. Seejärel määrake vahekaardi **Sisestamine** kiirkaardil **Kogum** suvandi **Pearaamatu kanded** väärtuseks **Jah**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

