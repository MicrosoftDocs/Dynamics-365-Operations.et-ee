---
title: Kauba ja toormaterjali jälgimine varude, tootmise ja müügi puhul
description: Selles teemas kirjeldatakse, kuidas saate kasutada kauba jälgimist tuvastamaks, kus kaupu või toormaterjale tootmis- ja müügiprotsessides kasutatud on, kasutatakse või hakatakse kasutama.
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30191
ms.assetid: fdd0939a-855c-430f-a684-94f3baea1df4
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa1be4970f1106bf4b87eeaa428bac07c645b4f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426512"
---
# <a name="item-and-raw-material-tracing-in-inventory-production-and-sales"></a>Kauba ja toormaterjali jälgimine varude, tootmise ja müügi puhul

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas saate kasutada kauba jälgimist tuvastamaks, kus kaupu või toormaterjale tootmis- ja müügiprotsessides kasutatud on, kasutatakse või hakatakse kasutama.

Kauba jälgimise funktsioon on saadaval lehel **Kauba jälgimine**. Järgmised jaotised kirjeldavad, kuidas kauba jälgimist saab kasutada ja millised on valikud ning piirangud.

## <a name="what-is-item-tracing"></a>Mis on kauba jälgimine?
Kauba jälgimine on ärianalüüsi (BI) tööriist, mis annab ülevaate kaupade ja toormaterjalide lähte- ja sihtkohast tarneahelas. Tootjad saavad kaupu, toormaterjale või koostisosi jälgida tagasiulatuvalt hankijani ja edasiulatuvalt valmis toote tootmise ja müügini. Kauba jälgimine aitab tootjatel täita regulatiivseid nõudeid ning kvaliteedi- ja tootmisjuhtidel analüüsida hälbeid toodete ning materjalide kvaliteedis ja neile vastavalt toimida. Siin on mõned näited võimaluste kohta, kuidas tootjad saavad kauba jälgimist kasutada.

-   Tuvastage praegu varudes oleva kauba või toormaterjali summa ja kus seda talletatakse.
-   Määrake, kui palju kaubast või toormaterjalist on tarnitud ja millistele klientidele see tarniti.
-   Tuvastage plaanitud saadetised, mis hõlmavad kaupa või toormaterjali.
-   Määrake kaupa või toormaterjali kasutavate ja plaanitud, töös või valmis tootmistellimuste asukoht.
-   Uurige, kust kaup või toormaterjal osteti.
-   Uurige, kus kaupa või toormaterjali muu kauba tootmisel tarbiti.

## <a name="what-can-i-trace-and-are-there-any-limitations"></a>Mida saan jälgida ja kas kehtib mõni piirang?
Saate jälgida kaupade ja toormaterjalide ajaloolisi laokandeid, mis põhinevad kaubakoodil ja jälgimisdimensioonil, nagu seerianumber, partiinumber või hankija partiinumber. Kaupa või toormaterjali saab jälgida ainult juhul, kui sellele on määratud jälgimisdimensioon. Kuna jälgimine põhineb laokandel, on kaupade jälgimisel mõned piirangud. Näiteks on olemas projektide kannete, põhivarade ja kaubandusega seotud piirangud. Lisaks kuvatakse jälgimise üksikasjades kaastooted, kuid kõrvalsaadusi ei kaasata. Jälgimine hõlmab kõiki laokandeid ühest asukohast teiseni. Seetõttu võivad kasutajad leida, et teavet on liiga palju. Korraga kuvatakse ühe juriidilise isiku jälgimisandmed. Kontsernisiseses kontekstis puuduvad ettevõteteülesed võimalused. Kui kaup vastu võetakse või väljastatakse, tuleb alustada iga ettevõtte puhul uut jälgimist.

## <a name="what-criteria-can-i-specify-for-an-item-trace"></a>Millised kriteeriumid saab kauba jälgimisele määrata?
Kauba jälgimisel on nõutavad kriteeriumid kaubakood, jälgimisdimensioon (nt partiinumber või seerianumber) ja suund. Järgmises tabelis kirjeldatakse kriteeriume, mida saate kauba jälgimisel kasutada.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Väljagrupp</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kaubakood</td>
<td>Sisestage jälgitavale kaubale või toormaterjalile identifikaator.</td>
</tr>
<tr class="even">
<td>Tootedimensioonid</td>
<td>Valikuline: jälgige tootemääratluse konkreetseid aspekte, nagu konfiguratsioon, suurus, värv või laad.</td>
</tr>
<tr class="odd">
<td>Jälgimisdimensioonid</td>
<td>Sisestage partiinumbri, hankija partiinumbri või seerianumbri jälgimisdimensioon. Kui kasutate kriteeriumina partiinumbrit, kuvatakse hankija partiinumber, kui olete selle teabe salvestanud.</td>
</tr>
<tr class="even">
<td>Laoala dimensioonid</td>
<td>Valikuline: jälgige kaupu, mis on ladustatud kindlas asukohas.</td>
</tr>
<tr class="odd">
<td>Periood</td>
<td>Valikuline: sisestage kuupäevad, et piirata jälgimist kindla perioodiga. Jälgimise üksikasjades kuvatakse ainult dokumendid ja kanded, mis loodi selles kuupäevavahemikus.</td>
</tr>
<tr class="even">
<td>Edasi või tagasi</td>
<td>Valige jälgimise suund. Saate jälgida edasi- või tagasiulatuvalt.
<ul>
<li><strong>Tagasiulatuvalt</strong> – saate jälgida tagasisuunas, et tuvastada allikat, lattu jäävat kogust ning kõiki tootmistellimusi, mis on vähemalt osaliselt lõpetatuna kinnitatud.</li>
<li><strong>Edasiulatuvalt</strong> – saate jälgida edasisuunas, et tuvastada sihtkohta. Leiate müügitellimused ja kliendid, kellele jälgitav kaup või toormaterjal on vähemalt osaliselt tarnitud.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="what-information-is-included-in-the-trace-details"></a>Millist teavet jälgimise üksikasjad sisaldavad?
Jälgimise tulemused kuvatakse lehe **Kauba jälgimine** kiirkaardi **Üksikasjad** puul kronoloogilises järjekorras. Järjekord erineb olenevalt jälgimise suunast. Üksikasjad sisaldavad kõiki kandeid, alustades hankijalt ostetud kaubast ja lõpetades selle müügiga kliendile. Jälgimise tulemused sisaldavad ka vahetooteid, mis on seotud kauba või jälgimisdimensiooniga, mis määrati jälgimise kriteeriumis. Ülemine sõlm näitab kauba kogust laoühikutes, mis jääb järele vastavalt jälgimise kriteeriumis määratud laoala dimensioonidele. **Märkus:** jälgimise üksikasjad kuvavad hetktõmmise jälgimise ajal saadaval olnud teabest. Jälgimise üksikasju ei värskendata, kui teavet on pärast jälgimise läbiviimist muudetud.

## <a name="why-dont-some-nodes-contain-any-details"></a>Miks mõned sõlmed ei sisalda üksikasju?
Jälgimise üksikasjades teabe koguse vähendamiseks sisaldab üksikasju ainult kauba või toormaterjali esimese eksemplari sõlm. Kui valitud sõlm üksikasju ei sisalda, saate vaadata üksikasju sisaldavat sõlme, klõpsates suvandit **Mine jälgitavale reale**. Sõlme juurde saate seejärel naasta, klõpsates suvandit **Mine tagasi**.

## <a name="can-i-view-only-a-particular-type-of-document-for-example-can-i-view-only-production-orders-customers-or-vendors"></a>Kas saan vaadata ainult kindlat tüüpi dokumenti? Näiteks kas saan vaadata ainult tootmistellimusi, kliente või hankijaid?
Jah, jälgimise üksikasjadest saate avada loendilehed, mis sisaldavad ainult teatud tüüpi dokumenti või kannet. Pääsete nende lehtede juurde tegumiriba menüü-üksusest **Jälgimine** gruppides **Kaup**, **Müük**, **Ost**, **Tootmine** ja **Kvaliteet**. Näiteks jälgimise üksikasjades hankijate loendi vaatamiseks klõpsake valikuid **Jälgimine** &gt; **Ost** &gt; **Hankijad**. Loendilehed võtavad kokku jälgimise üksikasjade dokumendid või kanded. Loendilehtedel **Ootel kanded**, **Ootel tellimused** ja **Saatmata müügitellimused** kuvatakse ka muu jälgimise üksikasjadesse kaasamata teave. Lisaks kuvavad need alati käesoleva kuupäeva tulemused, isegi kui kuupäevavahemik on määratud. Järgmises tabelis kirjeldatakse täiendavaid üksikasju, mida need lehed sisaldada võivad.

| Loendid                    | Kirjeldus                                                                                                                                                                                                                                                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Saatmata müügitellimused | Vaadake müügitellimuse ridu, mida ei ole valitud ja mida seega jälgimise üksikasjades ei kuvata.                                                                                                                                                                                                                        |
| Ootel tellimused           | Vaadake kõiki jälgitava kauba ootel tootmistellimusi, olenemata jälgimise kriteeriumis kasutatud jälgimisdimensioonidest. Samuti saate vaadata ootel tootmistellimusi, milles jälgitav kaup on koostisosa ning kus ühtegi registreerimist ei ole tehtud ja ühtegi tellimuse kannet ei ole lõpetatud. |
| Ootel kanded     | Vaadake jälgitava kauba ootel laokandeid, mis sisaldavad määratud jälgimisdimensioone või tühja jälgimisdimensiooni. Saate jälgimise üksikasjades vaadata ka kaupade ja jälgimisdimensioonide kombinatsioonide ootel laokandeid või tühja väärtust.                                                |

## <a name="how-many-levels-can-i-trace-up-or-down-in-a-bom-or-formula"></a>Mitme tasandi võrra saan koosluses või valemis tagasi- või edasiulatuvalt teavet jälgida?
Koosluse või valemi puhul saate jälgida ühe taseme võrra tagasi- või edasiulatuvalt. Näiteks kui käivitate toormaterjalide jälgimise, näete valmistoodet ja mis tahes kaastooteid. Kui aga jälgite kaastoodet, siis ei sisalda jälgimise üksikasjad valmistoodet.

## <a name="how-can-i-view-more-details-about-a-document-or-transaction-in-the-trace-details"></a>Kuidas saan näha jälgimise üksikasjades rohkem üksikasju dokumendi või kande kohta?
Kiirkaardil **Üksikasjad** saate jälgimise üksikasjades vaadata lisateavet valitud dokumendi või kande kohta järgmistel viisidel.

-   Kui valite kiirkaardil **Üksikasjad** jälgimise üksikasjades mõne sõlme, kuvatakse lehe teistel kiirkaartidel teave sõlmes oleva dokumendi või kande kohta.
-   Avage valitud sõlmes oleva dokumendi üksikasjade leht, klõpsates käsku **Kuva üksikasjad**. Näiteks kui valite sõlme, mis kirjeldab tootmistellimust, ja klõpsate käsku **Kuva üksikasjad**, kuvatakse vorm **Tootmistellimuste üksikasjad**.

Mõned kiirkaardid võimaldavad juurdepääsu valitud sõlme täiendavale teabele. Näiteks kiirkaardil **Mittevastavused** saate uurida, kas on olemas mittevastavuse ajalugu, klõpsates valikut **Päringud**. Kiirkaardil **Partii** saate klõpsata suvandit **Laoseisu loend**, et vaadata praegu olemasolevat füüsiliste varude kogust ja kõiki partiiga seotud laokandeid.

## <a name="can-i-run-more-than-one-trace-and-then-compare-the-details"></a>Kas saan käivitada mitu jälgimist ja seejärel üksikasju võrrelda?
Kui olete jälgimise käivitanud, saate kasutada nupu **Jälgi sõlmest** valikuid, et käivitada uus jälgimine valitud sõlme kandes.

-   **Tagasiulatuvalt** või **Edasiulatuvalt** – saate käivitada valitud sõlmes uue jälgimise ja kirjutada üle praeguse jälgimise üksikasjad.
-   **Uus tagasiulatuvalt** või **Uus edasiulatuvalt** – saate käivitada uue jälgimise uues aknas ja säilitada praeguse jälgimise üksikasjad.

Kui soovite kasutada valikut **Uus tagasiulatuvalt** või **Uus edasiulatuvalt**, tuleb kasutada funktsiooni **Ava uues aknas**, et uus jälgimine kuvataks uues aknas.

## <a name="can-i-save-the-trace-details"></a>Kas saan jälgimise üksikasjad salvestada?
Saate salvestada vahekaardil <strong>Üksikasjad</strong> oleva teabe XML-failina, klõpsates käsku <strong>Ekspordi</strong>tegumiriba toimingu *<strong><em>Jälgimine</em></strong>* all. Lisaks jälgimise üksikasjadele sisaldab XML-fail ka jälgimise kriteeriume, emasõlme ja laos olevat kogust. Jälgimise üksikasjade salvestamise võimalus on kasulik näiteks juhul, kui soovite manustada teavet kvaliteettellimusele või muule vastavusdokumentatsioonile. Saate määrata faili salvestamiskoha. Faili kohe vaatamiseks märkige ruut <strong>Kuva dokument</strong>. <strong>Märkus:</strong> fail salvestatakse alati, isegi siis, kui soovite seda ainult vaadata. Vaikimisi avaneb XML-fail brauseriaknas. Kuid võite faili paremklõpsata, valida <strong>Ava programmiga</strong> ja valida seejärel sisu kuvamiseks kasutatav programm.

## <a name="can-i-calculate-a-balance-for-a-particular-item-or-ingredient"></a>Kas saan arvutada konkreetse kauba või koostisosa saldo?
Saate eksportida teabe kokkuvõtte lehtedelt Microsoft Excelisse. Avage vastav leht, klõpsake ikooni **Ava Microsoft Office’is** ja valige siis **Ekspordi Microsoft Excelisse**. See funktsioon on eriti kasulik, kui soovite arvutada kauba või koostisosa hulgisaldo lehelt **Kannete kokkuvõte**. Lehel **Kannete kokkuvõte** saate soovi korral filtreerida kaupu või koostisosi ja partiid ning seejärel eksportida teabe Excelisse. Excelis saate näiteks laos oleva koguse müüdud kogusest ja tootmises kasutatud kogusest eraldada.

## <a name="can-i-investigate-whether-there-is-a-history-of-issues-with-items-or-raw-materials"></a>Kas saan uurida, kas on olemas kaupade või toormaterjalide probleemide ajalugu?
Jälgimise üksikasjad sisaldavad teavet kaupa või toormaterjali hõlmavate kvaliteettellimuste ja mittevastavuste kohta. Kvaliteettellimuste ja mittevastavuste kokkuvõtte vaatamiseks klõpsake tegumiribal valikut **Kvaliteettellimused** või **Mittevastavused**. **Märkus:** purustava katsega kvaliteettellimused võivad esineda jälgimise üksikasjades mitu korda. Kui dokumendi (nt ostutellimuse) jaoks luuakse purustava katsega kvaliteettellimus, kuvatakse see selle dokumendi iga kande puhul.

## <a name="are-there-any-reporting-capabilities-that-are-related-to-item-tracing"></a>Kas kauba jälgimisega on seotud mõni aruandlusvõimalus?
Saate luua aruande **Klientidele saadetud**, et tuvastada tarnitud kauba või toormaterjali kogus ja kliendid, kellele kaup tarniti. Vastavusega seotud päringu puhul saate koostada aruande kõikide klientide kohta. Klienditeenindusega seotud päringu puhul saate koostada aruande valitud kliendi kohta. Kui toode oli valmiskauba tootmisel kasutatud toormaterjal, lisatakse ka valmiskaup. **Märkus:** kui kasutate funktsioone müügitellimuste kustutamiseks või arhiveerimiseks, sisaldavad aruande tulemused ka kõiki kustutatud või arhiveeritud müügitellimusi.

## <a name="can-i-trace-coproducts-and-byproducts"></a>Kas ma saan jälgida kaastooteid ja kõrvalsaaduseid?
Saate jälgida kaastooteid, kuid te ei saa jälgida kõrvalsaadusi, sest tavaliselt ei ole kõrvalsaadustele määratud jälgimisdimensioone. Kaupa jälgides lisatakse jälgimise üksikasjadele kõik seotud kaastooted. Kaastoodet sisaldava sõlme üksikasjadesse on lisatud sõna „kaastoode”. Saate vaadata ka kaastoote üksikasju, valides jälgimise üksikasjades sõlme ja klõpsates siis kiirkaarti **Tootmine**.
