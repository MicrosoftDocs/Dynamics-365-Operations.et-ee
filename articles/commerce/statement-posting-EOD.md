---
title: Väljavõtte sisestamise funktsiooni täiustused
description: Selles teemas kirjeldatakse väljavõtte sisestamise täiustusi.
author: josaw1
manager: AnnBe
ms.date: 05/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: anpurush
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e76a5ad741dca5831b609a5b991aa70e3753c621
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009639"
---
# <a name="improvements-to-statement-posting-functionality"></a>Väljavõtte sisestamise funktsiooni täiustused

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse väljavõtte sisestamise esimest täiustuste kogumit. Need täiustused on saadaval rakenduses Microsoft Dynamics 365 for Finance and Operations7.3.2.

## <a name="activation"></a>Aktiveerimine

Vaikimisi on juurutamisel rakendus Finance and Operations 7.3.2 seadistatud kasutama väljavõtte sisestamise pärandfunktsiooni. Täiustatud väljavõtte sisestamise funktsiooni lubamiseks peate sisse lülitama selle konfiguratsioonivõtme.

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

Lisaks on kiirkaardil **Pakktöötlus** vahekaardil **Sisestamine** lehel **Parameetrid** kasutusele võetud järgmised parameetrid. 

- **Paralleelselt sisestatavate väljavõtete maksimumarv** – see väli määratleb mitme väljavõtte sisestamiseks kasutatavate pakett-ülesannete arvu. 
- **Lõimede maksimumarv tellimuse töötlemisel väljavõtte kohta** – see väli näitab maksimaalset lõimede arvu, mida kasutatakse väljavõtte sisestamisel pakett-töös, et luua ja arveldada müügitellimusi ühe väljavõtte jaoks. Väljavõtete sisestamise protsessi kasutatav lõimede koguarv arvutatakse selle parameetri väärtuse alusel, mis korrutatakse parameetri **Paralleelselt sisestatavate väljavõtete maksimumarv** väärtusega. Selle parameetri väärtuse liiga kõrgeks määramine võib negatiivselt mõjutada väljavõtte sisestamise protsessi jõudlust.
- **Kogumisse kaasatud kanderidade maksimumarv** – see väli määrab kanderidade arvu, mis kaasatakse ühte kandekogumisse enne uue loomist. Koondatud kanded luuakse erinevate koondamiskriteeriumide alusel, nagu näiteks klient, ärikuupäev või finantsdimensioonid. Oluline on märkida, et ühest kandest pärinevaid ridu ei tükeldata erinevate koondatud kannete vahel. See tähendab võimalust, et koondatud kandes on ridade arv veidi suurem või väiksem, põhinedes sellistel teguritel nagu eristavate toodete arv.
- **Maksimaalne lõimede arv poe kannete kinnitamiseks** – see väli määratleb nende lõimede arvu, mida kasutatakse kannete kontrollimiseks. Kannete kinnitamine on nõutud etapp, mis peab toimuma enne kannete sisestamist väljavõtetesse. Peate ka määratlema suvandi **Kingekaardi toode** kiirkaardil **Kinkekaart** vahekaardil **Sisestamine** lehel **Commerce’i, parameetrid**. See tuleb määrata isegi siis, kui organisatsioon ei kasuta kinkekaarte.

> [!NOTE]
> Kõik väljavõtte sisestamisega seotud ja poodide lehel ning lehel **Commerce’i parameetrid** määratud sätted ja parameetrid kehtivad väljavõtte sisestamise täiustatud funktsioonile.

## <a name="processing"></a>Teostamine

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

Sisestamise protsessi ajal koondatakse müügikanded konfiguratsiooni järgi. Koondatud kanded salvestatakse süsteemi ja neid kasutatakse müügitellimuste loomiseks. Iga koondatud kanne loob süsteemis ühe vastava müügitellimuse. Koondatud kandeid saate vaadata, kasutades nuppu **Koondatud kanded** väljavõtte grupis **Käivitamise üksikasjad**.

Koondatud kande vahekaardil **Müügitellimuse üksikasjad** kuvatakse järgmine teave.

- **Kirje ID** – koondatud kande ID.
- **Väljavõtte number** – väljavõte, mille juurde koondatud kanne kuulub.
- **Kuupäev** – kuupäev, millal koondatud kanne loodi.
- **Müügi ID** – kui müügitellimus luuakse koondatud kandest, on see müügitellimuse ID. Kui see väli on tühi, ei ole vastavat müügitellimust veel loodud.
- **Koondatud ridade arv** – koondatud kande ja müügitellimuse ridade koguarv.
- **Olek** – koondatud kande viimane olek.
- **Arve ID** – kui koondatud kande müügitellimuse kohta koostatakse arve, on see müügiarve ID. Kui see väli on tühi, ei ole müügitellimuse kohta arvet veel sisestatud.

Koondatud kande vahekaardil **Kande üksikasjad** kuvatakse kõik kanded, mis on koondatud kandesse tõmmatud. Koondatud kande koondread kuvavad kannete koondatud kirjed. Koondread kuvavad ka üksikasjad, näiteks kauba, variandi, koguse, hinna, netosumma, ühiku ja lao. Põhimõtteliselt vastab iga koondrida ühele müügitellimuse reale.

Lehelt **Koondatud kanded** saate alla laadida konkreetse koondatud kande XML-i, kasutades nuppu **Müügitellimuste eksportimise XML**. XML-i saate kasutada müügitellimuse loomise ja sisestamisega seotud probleemide silumiseks. Laadige lihtsalt XML all, laadige see katsekeskkonda ja siluge probleemi katsekeskkonnas. Koondatud kannete XML-i allalaadimise funktsioon ei ole saadaval sisestatud väljavõtete jaoks.

Koondatud kande vaatel on järgmised eelised.

- Kasutajal on ülevaade koondatud kannetest, mis nurjusid müügitellimuse loomise ajal, ja müügitellimustest, mis nurjusid arve koostamise ajal.
- Kasutaja näeb, kuidas kandeid koondatakse.
- Kasutajal on täielik kontrolljälg kannetest müügitellimuste ja müügiarveteni. See kontrolljälg ei olnud saadaval väljavõtte sisestamise pärandfunktsioonis.
- Koondatud XML-fail muudab lihtsamaks probleemide tuvastamise müügitellimuse loomise ja arve koostamise ajal.

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