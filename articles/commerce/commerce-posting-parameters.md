---
title: Commerce'i sisestusparameetrid
description: See artikkel kirjeldab parameetreid, mis on spetsiifilised finants- ja füüsiliste kannete sisestamisele moodulisse Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 56a2d1d2bcafdcdd9d88c132986e8ef485bf6b24
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027224"
---
# <a name="commerce-posting-parameters"></a>Commerce'i sisestusparameetrid

[!include [banner](includes/banner.md)]

See artikkel kirjeldab parameetreid, mis on spetsiifilised finants- ja füüsiliste kannete sisestamisele moodulisse Microsoft Dynamics 365 Commerce. Äri sisestamisparameetrid asuvad rakenduse Retail ja Commerce Headquarters **häälestamise parameetrite Commerce \> Headquartersis \>\> (sisestamine \>)**.

## <a name="periodic-discount-parameters"></a>Perioodilise allahindluse parameetrid

Järgmises tabelis loetletakse perioodiliste allahindlusparameetrite parameetrid, mis on omased finants- ja füüsiliste kannete sisestamisele.

| Parameeter | Kirjeldus |
|-----------|-------------|
| Sisestage perioodiline allahindlus | See valik kontrollib, kas perioodilisi pakkumisi pearaamatukontodele sisestatakse. Perioodilised allahindlused sisaldavad segamise ja sobitamise allahindlust, koguse allahindlust ning allahindluse pakkumisi. Kui see parameeter on lubatud, saab jaotises Perioodilised allahindlused **seada lisaväljad**. |
| Pearaamatukonto tüüp | <p>Valige konto tüüp, mida kasutatakse perioodiliste allahindluste sisestamiseks:</p><ul><li>**Standard** – süsteem ei kasuta selle lehe allahindlusega seotud välju. Selle asemel kasutab see kontosid, mis on määratud sisestuse **lehel** Commerce headquarters (**Laohalduse seadistuse \> sisestamise \> sisestamise \> vormid**).</li><li>**Perioodiline** : süsteem kasutab commerce'i allahindluse kontosid, mis on määratud allahindlusega seotud väljadel sellel lehel. Kui valite selle suvandi, peate määrama pearaamatukonto igat tüüpi pakkumisele (allahindlus, segamine ja sobitamine, kogus ja lävi). Iga allahindluse häälestamisel saate määratleda konto. Kui allahindluse konto sisestusfunktsiooni kasutatakse allahindluse häälestuse lehel, tehakse täiendav deebetkanne ja kreeditkanne, et klassifitseerida allahindluse sisestamine äriallahindluse pearaamatukontolt ümber pearaamatu allahindluse kontole. Lisateavet vt jaemüügi [allahindlustest](retail-discounts-overview.md).</li></ul> |
| Sisestage teabekoodi allahindlus | Seda valikut ei kasutata enam standardses Commerce'i lahenduses ja see on taunimatu. |
| Perioodiline allahindlus tellimustele | See valik kontrollib, kas kliendi tellimuse ja kõnekeskuse tellimuste puhul sisestatakse jaemüügi perioodilised allahindlused pearaamatusse. |

## <a name="inventory-update-parameters"></a>Lao uuendamise parameetrid

Järgmises tabelis loetletakse varude uuendamise parameetrid, mis on omased finants- ja füüsiliste kannete sisestamisele.

| Parameeter | Kirjeldus |
|-----------|-------------|
| Kasuta partii vaike-ID-d, kui partiinumbreid ei leita | See valik määrab, kas partii vaikimisi ID-d kasutatakse partii puhul lubatud kaupade puhul, kui partiinumbreid ei leita ja negatiivne laovaru on lubatud. |
| Partii vaike-ID | Partiinumber, mida kasutada, kui kaupade **partiinumbreid ei leita ja kui partiinumbrite ei leita, on parameeter Kasuta vaikimisi partii ID-d** lubatud. |

## <a name="aggregation-parameters"></a>Liitmise parameetrid

Järgmises tabelis loetletakse liitmise parameetrid, mis on omased finants- ja füüsiliste kannete sisestamisele.

| Parameeter | Kirjeldus |
|-----------|-------------|
| Seifi viidav raha | Lubage sellel parameetril liita väljavõtte sisestamisel kõik kanded ja looge sisestamiseks töölehel üks rida eraldi rea asemel iga raha lohistamise jaoks. |
| Raha hoiustamine panka | Lubage sellel parameetril liita väljavõtte sisestamisel kõik kanded ja looge sisestamiseks töölehel üks rida eraldi rea asemel iga raha lohistamise jaoks. |
| Müügikanded | Lubage see parameeter, et konsolideerida kanded kandeväljavõtte sisestusprotsessi osana. Soovitame selle parameetri lubada. Selle nimi oli varem Kande **kanded**. |
| Ära koonda tagastusi | Kui see suvand on valitud, sisestatakse iga tagastuskanne eraldi müügitellimusena jaemüügi väljavõtte sisestamisel. |

## <a name="batch-processing-parameters"></a>Pakktöötluse parameetrid

Järgmises tabelis loetletakse pakktöötluse parameetrid, mis on omased finants- ja füüsiliste kannete sisestamisele.

| Parameeter | Kirjeldus |
|-----------|-------------|
| Paralleelväljavõttete maksimaalne arv | See väli määratleb partiiülesannete arvu, mida kasutatakse mitme väljavõtte sisestamiseks. |
| Tellimuse töötlemise lõimede maksimum väljavõtte kohta | See väli näitab lõimede maksimaalset arvu, mida väljavõtte sisestamise pakett-töö kasutab müügitellimuste loomiseks ja arveldamiseks ühele väljavõttele. Väljavõtte sisestusprotsessis kasutatud **lõimede koguarv arvutatakse, korrutades selle parameetri väärtuse paralleelväljavõtte sisestamisparameetri maksimaalse arvu väärtusega**. Kui selle parameetri väärtus on liiga kõrge, võib see negatiivselt mõjutada väljavõtte sisestusprotsessi jõudlust. |
| Kogumisse kaasatavate kanderidade maksimumarv | See väli määratleb kanderidade arvu, mis kaasatakse ühte koondkandesse enne uue kande loomist. Liidetud kanded luuakse erinevate liitmiskriteeriumide alusel, nagu klient, ärikuupäev või finantsdimensioonid. Pange tähele, et üksiku kande ridu ei jagata erinevate koondkannete vahel. Seega võib koondkande ridade arv olla veidi suurem või väiksem, võttes aluseks sellised tegurid nagu eristatavate toodete arv. |
| Maksimaalne lõimede arv kaupluse kannete kinnitamiseks | See väli määratleb kannete kinnitamiseks kasutatavate lõimede maksimaalse arvu. Kannete kinnitamine on nõutav samm, mis peab olema enne kannete väljavõtete sissetõstmist. Samuti peate **kinkekaardi** **·** **toote määratlema kinkekaardi kiirkaardi vahekaardil Commerce parameters**, isegi kui organisatsioon ei kasuta kinkekaarte. |

Järgmises tabelis loetletakse eelmises tabelis loetletud parameetrite soovituslikud väärtused. Neid väärtusi tuleb testida ja kohandada juurutuse konfiguratsioonile ja saadaolevale infrastruktuurile. Väärtused, mis ületavad soovitatud väärtused, võivad ebasoodsalt mõjutada teist pakktöötlust ja tuleks kinnitada.

| Parameeter | Soovitatav väärtus | Üksikasjad |
|-----------|-------------------|---------|
| Paralleelselt sisestatavate väljavõtete maksimumarv | <p>Seadistage see parameeter pakett-tööde arvule, mis on saadaval pakett-tööde grupile, mis käitab **väljavõtte** tööd.</p><p>**Üldine reegel:** korrutage rakendusobjekti serveri (AOS) virtuaalserverite arv partiiülesannete arvuga, mis on saadaval AOS-i virtuaalserveri kohta.</p> | See parameeter ei ole rakendatav, kui jaemüügi väljavõtete **– kaupluste söötmise funktsioon** on lubatud. |
| Tellimuse töötlemise lõimede maksimum väljavõtte kohta | Alustage katseväärtustele **4**. Tavaliselt ei tohi väärtus ületada **8**. | See parameeter määratleb müügitellimuste loomiseks ja sisestamiseks kasutatavate lõimede arvu. See näitab väljavõtte kohta sisestamiseks saadaolevaid lõimede arvu. |
| Kogumisse kaasatavate kanderidade maksimumarv | Alustage katseväärtustele **1000** juures. Sõltuvalt Commerce Headquartersi konfiguratsioonist võivad väiksemad tellimused olla jõudluses rohkem seotud. | See parameeter määratleb ridade arvu, mis kaasatakse väljavõtte sisestamisel igasse müügitellimusse. Kui see number on saavutatud, tükeldatakse read uude tellimusse. Müügiridade arv ei võrdu teie määratud arvuga, kuna tükeldamine toimub müügitellimuse tasemel. Sellest hoolimata on number seadistatud arvule lähedal. Seda parameetrit kasutatakse nende jaemüügikannete müügitellimuste loomiseks, kus pole nimetatud klienti. |
| Maksimaalne lõimede arv kaupluse kannete kinnitamiseks | Soovitame teil seada selle parameetri väärtuseks **4** ja seda suurendada ainult siis, kui te ei saavuta vastuvõetavat jõudlust. Lõimede arv, mida see protsess kasutab, ei saa ületada pakktöötluse serverile saadaval protsessorite arvu. Kui lõimede arv on liiga suur, võib see mõjutada muud pakktöötlust. | See parameeter reguleerib kannete arvu, mida saab antud kaupluses samal ajal kinnitada. |

> [!NOTE]
> Kõik väljavõtte sisestamisega seotud ja poodide lehel ning lehel **Commerce’i parameetrid** määratud sätted ja parameetrid kehtivad väljavõtte sisestamise täiustatud funktsioonile.

## <a name="invoice-parameters"></a>Arve parameetrid

Järgmises tabelis loetletakse arve parameetrid, mis on omased finants- ja füüsiliste kannete sisestamisele.

| Parameeter | Kirjeldus |
|-----------|-------------|
| Töölehe nimi | Maksetöölehe nimi, mida kasutatakse kliendi maksetöölehtede loomisel müügitellimuse maksete jaoks. See säte kehtib kõigi kassa, kõnekeskuse ja e-äri kanalite tellimuste kohta sisestatud tellimuse maksete puhul. |
| Konto nimi | Maksekonto nimi. |
| Prioriseeri mõõtmed maksemeetodist | Kui see lipp on lubatud, prioriseerib maksetööleht kaupluse dimensioonide asemel dimensioonid makseviisist. |
| Käitumine maksu arvutamisel | See parameeter määrab käitumise, kui väljavõtte sisestamisel loodud müügitellimusi arveldatakse:<ul><li>**Arvuta uuesti – arvutage** maksud uuesti.</li><li> **Ära arvuta uuesti – kasutage kassas** arvutatud maksusummasid.</li></ul> |
| Töölehe nimi | Tagasimaksete kliendimakse töölehe loomisel kasutatav töölehe nimi. See säte kehtib kõigi kassa, kõnekeskuse ja e-äri kanali tellimuste kohta sisestatud tellimuse maksete kohta. |

## <a name="statement-parameters"></a>Väljavõtte parameetrid

Järgmises tabelis loetletakse finants- ja füüsiliste kannete sisestamisel konkreetsed väljavõtte parameetrid.

| Parameeter | Kirjeldus |
|-----------|-------------|
| Varude reserveerimine arvutamisel | Kui see parameeter on lubatud, reserveeritakse väljavõtte arvutamisel laovarud ajutiselt kuni väljavõtte sisestamiseni. See parameeter on väljavõtte arvutamise jõudluse parandamiseks vaikimisi keelatud. Uuendatud laoteabe saab arvutada pakett-tööga **Sisesta varud**. Pidage meeles, et **pakett-töö** Varude sisestamine ei ole enam kasutusel, kui [kaupluste](trickle-feed.md) kannete jaoks on lubatud kanalipõhise tellimuse loomine. |
| Inventuuri keelamine on nõutav | See lipp keelab inventuuri commerce headquartersis sisestamisel. |
| Arvuta tõrke korral finantsdimensioonid uuesti | Kui see parameeter on lubatud, saab finantsdimensioone järgnevatel väljavõtte sisestustel ümber hinnata, kui väljavõtte sisestamine nurjub. |
| Kaupluse finantsdimensioonide kasutamine | Kui see parameeter on lubatud, saab luua lingitud tagastusmüügitellimused, mis kasutavad algse kande finantsdimensioonide asemel kaupluse finantsdimensioone. |
| Tühista tagastuste seos | Kui see parameeter on lubatud, saab lause luua sisestamata müükide tagastused pimesi tagasi. See parameeter on vaikimisi keelatud ja soovitame selle keelata. |
| Keela ümarduserinevuse sisestamine | See parameeter keelab ümarduserinevuse sisestamise kande makse ja brutosumma vahel maksete töötlemisel. |
| Tasakaalusta klientide deposiidid automaatselt | Kui see parameeter on lubatud, tasakaalustatakse jaemüügi väljavõtte sisestamisel sisestatud kliendi deposiitid kliendi avatud kannetega. |
| Kassa kassa kassahalduse vastavusseviimise lubamine ja kasutamine | Kui see parameeter on lubatud, tehakse kassas sularahahalduse vastavusseviimine ja väärtused edastatakse väljavõtteridade loomiseks jaemüügi finantsaruande sisestustele. |
| Pearaamatu vautšeri üksikasjalikkuse tase | See parameeter määratleb kassast pärit valitud kannete pearaamatukandesse kaasatud üksikasjataseme. Kandetüübid hõlmavad tulusid, kulusid ja allahindlusi. Allahindluste puhul võetakse seda parameetrit arvesse ainult juhul, kui perioodilise allahindluse kontonumber ja regulaarse allahindluse kontonumber ei ole samad. Kui üksikasjad ei ole nõutavad **,** on kokkuvõte nende sisestuste soovitatav väärtus. Kui kokkuvõttetaseme sisestus on määratletud, ei **täideta TransactionDiscountTrans.RecID-d**. Commerce 10.0.27 versiooni väljaandes nimetati see lipp ümber ja teisaldati. Selle nimi oli varem **Detaili tase** ja oli jaotises Varude **uuendamine**. |
