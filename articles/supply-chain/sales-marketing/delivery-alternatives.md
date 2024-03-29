---
title: Tarne alternatiivid
description: Müügitellimuse vastuvõtjad saavad alternatiivsete tellimuse täitmise valikute uurimiseks kasutada lehte Tarnealternatiivid.
author: Henrikan
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: henrikan
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f58f7923d82f3aa371ba916352211195870f9a75
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572621"
---
# <a name="delivery-alternatives"></a>Tarne alternatiivid

[!include [banner](../includes/banner.md)]

Müügitellimuse vastuvõtjad saavad alternatiivsete tellimuse täitmise valikute uurimiseks kasutada lehte **Tarne alternatiivid**.

Lehepaigutus **Tarne alternatiivid** annab ülevaate alternatiivsetest valikutest. See võimaldab tellimuse vastuvõtjatel vaadata täitmise võimalusi ka praegusest ettevõttest väljaspool. Nüüd saavad nad vaadata nii kontsernisiseseid kui ka väliste hankijate pakutavaid võimalusi. Valikute sortimiseks tarnekuupäeva järgi saavad müügitellimuste vastuvõtjad vaadata tarnealternatiivide arukat loendit. Peale selle aitavad parameetrid neil soovitatud tarneid paremini hallata. Kuna transpordiaeg võib mõjutada tarnekuupäevi, saavad müügitellimuse vastuvõtjad uurida vedajate pakutavaid erinevaid transpordivalikuid. Kuna iga soovituse kohta kuvatakse üksikasjalikku teavet, saavad tellimuste vastuvõtjad teha teadlikke otsuseid otse lehel **Tarnealternatiivid**.

## <a name="open-the-delivery-alternatives-page"></a>Lehe Tarnealternatiivid avamine

Lehe **Tarne alternatiivid** saate avada müügitellimuse realt.

1. Valige **Tooted ja tarne \> Tarnealternatiivid**.
1. Valige **Rea üksikasjad \> Tarne \> Tarne alternatiivid.**

Saate lehe **Tarnealternatiivid** avada ka tööruumist **Müügitellimuse töötlemine ja päring**, valides suvandi **Tellimused ja lemmikud \> Hilinenud tellimuse read \> Tarnealternatiivid**. **Märkus.** Saate avada lehe **Tarnealternatiivid** ainult siis, kui mõlemad järgmised tingimused on täidetud.

- Kogu kohustuslik müügireateave on sisestatud.
- Välja **Tarnekuupäeva kontroll** väärtuseks on valitud muu väärtus kui **Pole**.

## <a name="delivery-date-control-methods"></a>Tarnekuupäeva kontrollimeetodid

Tarnekuupäeva kontrollimeetod määrab, kuidas süsteem loob tarnekuupäevi, kuidas tarnekuupäevi arvutatakse ja millist teavet kuvatakse. Pange tähele, et tarne kuupäeva kontroll võtab arvesse kalendreid. Seetõttu võivad soovitatud vastuvõtukuupäeva mõjutada järgmised kalendrid: laokalender, transpordikalender, hankija kalender ja kliendi kalender. Järgmises tabelis kirjeldatakse iga tarnekuupäeva kontrollimeetodit.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Meetod</strong></td>
<td><strong>Kirjeldus</strong></td>
</tr>
<tr class="even">
<td><strong>None</strong></td>
<td><ul>
<li>Tarnealternatiive müügiridade puhul ei toetata. See suvand lülitab tarne kuupäeva kontrolli välja.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Müügi täitmisaeg</strong></td>
<td><ul>
<li>Tarnealternatiivid arvutatakse eelmääratletud müügi täitmisaja põhjal. Transpordipäevad arvutatakse tarneviisi põhjal.</li>
<li>Tarnealternatiivid hõlmavad ladusid, millel on vaba kaubavaru, ja tarne-/nõudlustellimusi.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>ATP</strong></td>
<td><ul>
<li>Tarnealternatiivid arvutatakse loogika „saadaval lubamiseks” (ATP) põhjal. Arvesse võetakse praegust saadavust ja eeldatavat tulevast saadavust. Transpordipäevad arvutatakse tarneviisi põhjal.</li>
<li>Tarnealternatiivid hõlmavad ladusid, millel on vaba kaubavaru, ja tarne-/nõudlustellimusi.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>ATP + väljamineku ohutusvaru</strong></td>
<td><ul>
<li>Tarnealternatiivid arvutatakse nagu ATP-meetodi puhul, kuid arvutusse kaasatakse väljamineku ohutusvaru.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>CTP</strong></td>
<td><ul>
<li>Tarnealternatiivid arvutatakse loogika „võimeline lubama” (CTP) põhjal. Saadavuse määramiseks kasutatakse MRP koosnevusarvutust. Pange tähele, et CTP nihutab tarnekuupäevad minimaalselt müügi täitmisajale. Transpordipäevad arvutatakse tarneviisi põhjal.</li>
<li>Tarnealternatiivid hõlmavad soovitusi järgmiste ladude kohta:
<ul>
<li>Praegune ladu</li>
<li>Vaikeladu</li>
<li>Kõik laod, millel on olemas vaba kaubavaru</li>
<li>Kõik laod, millel on hanketellimusi</li>
<li>Kõik laod, millel on aktiivseid koosluse versioone</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a>Tarnealternatiivide teabe kuvamine

Selles jaotises kirjeldatakse teavet saadaolevate tarnealternatiivide kohta igal lehe **Tarnealternatiivid** kiirkaardil.

### <a name="the-product-fasttab"></a>Toote kiirkaart

Sellel kiirkaardil kuvatakse toote kokkuvõte ja praeguse müügirea üksikasjad.

### <a name="the-delivery-alternatives-fasttab"></a>Kiirkaart Tarnealternatiivid

Sellel kiirkaardil kuvatakse tarnealternatiivide loend, mis on sorditud vastuvõtu kuupäeva järgi. Loendi kohal saate valida, millistel valikutel peaksid soovitused põhinema. Saate valida ka tarneviisi, mis määrab ära transpordipäevad. Valikud on järgmised:

- **Kaasa muud tootevariandid** – see valik on saadaval tootevariantidega toodete puhul. See hõlmab toote muude variantide tarnealternatiive. See valik pole CTP puhul saadaval.
- **Kaasa osaline kogus** – vaikimisi kaasatakse ainult soovitused, mis täidavad müügirea täieliku koguse. Valige see suvand soovituste kaasamiseks, mis täidavad tellimuserea ainult osaliselt. See valik on kasulik, kui klient nõuab varasemat tarnekuupäeva ja nõustub osalise tarnega.
- **Kaasa hilisemad kuupäevad** – vaikimisi kuvatakse ainult soovitused, mis on paremad (varasemad) kui praegused kuupäevad müügireal. Valige see suvand hilisemate kuupäevade kaasamiseks. See suvand võib olla kasulik olukordades, kus prioriteet on muudel parameetritel kui kuupäev. Näiteks võib eelistatud olla kindel hankija või ladu.
- **Tarneviis** – saate valida transpordiaja ja -kulu optimeerimiseks eelistatud tarneviisi. Näete mõju soovitatud tarnealternatiividele kohe. Seega on alternatiive lihtne võrrelda.
- **Kaasa hange** – hanke valimisel hõlmavad soovitatud tarnealternatiivid valikuid hankimiseks nii välistelt hankijatelt kui ka teistelt kontserni ettevõtetelt (kontsernisiseselt). Valikut **Kaasa hange** toetatakse ATP ja ATP + väljamineku ohutusvaru tarnekuupäeva kontrolli puhul. Kaasatakse kõik hankevalikud toote vaike-ostuhankijalt ja kõigilt toote kinnitatud hankijatelt.
- Väliste hankijate puhul põhineb arvutus ostu täitmisajal.
- Kontsernisisese valiku puhul võtab arvutus arvesse, mis on hankeettevõttelt saadaval, arvestades hankeettevõtte tarnekuupäeva kontrolli.
- **Tarnetüüp** (hankimisel)
  - **Varud** – tooted saadetakse hankelaost müügireal toodud tegevuskohta/lattu. Seejärel saadetakse need laost kliendile.
  - **Otsetarne** – -tooted saadetakse hankelaost otse kliendile.

### <a name="the-availability-information-fasttab"></a>Kiirkaart Kättesaadavuse teave

Selle kiirkaardi teave on seotud valitud tarnealternatiivi reaga. Olenevalt müügitellimuse tarnekuupäeva kontrollist kuvatakse järgmine teave.

- **Müügi täitmisaeg**
  - **Saadaval täna** – kuvatakse praegune füüsiliselt vaba kaubavaru, füüsiliselt reserveeritud ja füüsiliselt saadaolevad varud.
  - **Parameetrid** – kuvatakse varude ühik ja müügi täitmisaeg.

- **ATP ja ATP + väljamineku ohutusvaru**
  - **Saadaval täna** – kuvatakse praegune füüsiliselt vaba kaubavaru, füüsiliselt reserveeritud ja füüsiliselt saadaolevad varud.
  - **Parameetrid** – kuvatakse varude ühik ja müügi täitmisaeg.
  - **Kättesaadavus tulevikus** – kuvatakse graafilisel kujul praegune ja tulevane kättesaadavus jaotises **Tarnealternatiivid** valitud tegevukoha ning lao kohta. Toote tulevikus saadavuse kohta üksikasjalikuma teabe nägemiseks valige diagrammi veerud. Liugur näitab asjakohaste nõudlus- ja tarnetellimuste loendit ATP ajavahemikus.

- **CTP**
  - **Saadaval täna** – kuvatakse praegune füüsiliselt vaba kaubavaru, füüsiliselt reserveeritud ja füüsiliselt saadaolevad varud.
  - **Parameetrid** – kuvatakse varude ühik ja müügi täitmisaeg.
  - **Koosnevusarvutus** – kuvatakse koosnevusarvutus valitud tarnealternatiivi kohta. Koosnevusarvutuses kuvatavate väljade ja varude dimensioonide muutmiseks saate kasutada jaotist **Seadistus**.

### <a name="the-impact-of-selected-alternative-fasttab"></a>Kiirkaart Valitud alternatiivi mõju

Sellel kiirkaardil on toodud esile valitud tarnealternatiivi mõju. Kui valite **OK**, värskendatakse müügirida VALITUD veergudel esiletõstetud väärtustega. Pange tähele, et kui valitud tarnealternatiivi kogus on väiksem kui müügirea kogus, luuakse tarnegraafik ja tellimuserida tükeldatakse kaheks reaks: üks rida valitud koguse jaoks ja teine rida ülejäänud koguse jaoks. Saate värskendada ka äriandmete rida, et see vastaks graafiku ridadele ja mõjutaks hinda.

## <a name="additional-resources"></a>Lisaressursid

[Tellimuse lubamine](delivery-dates-available-promise-calculations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]