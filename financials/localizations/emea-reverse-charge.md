---
title: "Pöördkäibemaks | Microsofti dokumendid"
description: "See teema selgitab, kuidas seadistada Euroopa riikide pöördkäibemaksu (KM)."
author: epodkolz
manager: AnnBe
ms.date: 05/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 6cb473962f40ed9ef2f5f807f089098764f47009
ms.openlocfilehash: b3c94fa73410d9bdcaaec11dee04a7a239e4d45a
ms.contentlocale: et-ee
ms.lasthandoff: 06/14/2017

---

# <a name="reverse-charge-vat"></a>Pöördkäibemaks
Selles teemas kirjeldatakse üldist lähenemist Euroopa riikide pöördkäibemaksu (KM) seadistamisele.

Pöördmaks on maksuskeem, mis viib käibemaksu arvestamise ja registreerimise kohustuse kaupade ja/või teenuste müüjalt ostjale. Seetõttu registreerivad kaupade ja/või teenuste saajad nii arvestatud käibemaksu (müüja rollis) kui ka sisendkäibemaksu (ostja rollis) oma käibemaksuaruandes.

Euroopa Liidu (EL) direktiiv laseb liikmesriikidel määrata, kuidas nad soovivad üldnõudeid kohalikele nõuetele kohandada. Seetõttu rakendatakse mõnes riigis pöördmaksu skeemi ainult mõne kauba ja/või teenuse puhul ja müügisummadele on kehtestatud lisatingimused või piirväärtused. Teistes riikides sõltub vastutus käibemaksu tasumise eest tarnija ja ostja olekust. Kui ostja on käibemaksukohustuslane, peab see asjaolu olema tarnija väljastatud arvel märgitud. Näiteks peavad arvel olema sõnad „pöördmaks” ja peab olema näidatud, millised kaubakoodid kuuluvad pöördmaksu skeemi alla. 

Pöördmaksu rakendamiseks tuleb teha järgmine seadistus.

## <a name="set-up-sales-tax-codes"></a>Saate häälestada käibemaksukoode.
Soovitame kasutada ostu- ja müügitoimingute jaoks eraldi käibemaksukoode.

<table>
<body>
<tr>
<td><strong>Müügi käibemaksukood</strong></td>
<td>Looge käibemaksukood müügi pöördmaksu toimingutele (<strong>Maks</strong> > <strong>Kaudsed maksud</strong> > <strong>Käibemaks</strong> > <strong>Käibemaksukoodid</strong>).
</td>
</tr>
<tr>
<td><strong>Ostude käibemaksukood</strong></td>
<td><p>Looge positiivsed ja negatiivsed käibemaksukoodid ostude pöördkäibemaksule (<strong>Maks</strong> > <strong>Kaudsed maksud</strong> > <strong>Käibemaks</strong> > <strong>Käibemaksukoodid</strong>).</p>
<ol>
<li>Looge positiivse väärtusega käibemaksukood.</li>
<li>Looge negatiivse väärtusega käibemaksukood. Määrake valiku <strong>Luba negatiivset käibemaksuprotsenti</strong> väärtuseks <strong>Jah</strong>.
See negatiivne käibemaksukood tuleb määrata kauba käibemaksugrupile ja seejärel selle kauba käibemaksugrupi kaupadele, mis kuuluvad pöördmaksuga käibemaksustamisele.</li>
</ol>
<p>Lisateavet leiate järgmisest jaotisest „Käibemaksugruppide ja kauba käibemaksugruppide häälestamine”.</p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a>Käibemaksugruppide ja kauba käibemaksugruppide häälestamine
Soovitame kasutada ostu- ja müügitoimingute jaoks eraldi käibemaksugruppe.

<table>
<tr>
<td><strong>Müügi käibemaksugrupid</strong></td>
<td>Looge käibemaksugrupp pöördmaksuga müügitoimingutele (<strong>Maks</strong> > <strong>Kaudsed maksud</strong> > <strong>Käibemaks</strong> > <strong>Käibemaksugrupid</strong>). Vahekaardil <strong>Seadistus</strong> lisage sellesse gruppi pöördmaksu käibemaksukood. Märkige käibemaksukoodi väljad <strong>Vabastus</strong> ja <strong>Pöördmaks</strong>.</td>
</tr>
<tr>
<td><strong>Ostude käibemaksugrupid</strong></td>
<td>Looge käibemaksugrupp pöördmaksuga ostutoimingutele (<strong>Maks</strong> > <strong>Kaudsed maksud</strong> > <strong>Käibemaks</strong> > <strong>Käibemaksugrupid</strong>). Lisage vahekaardile <strong>Seadistus</strong> nii positiivsed kui ka negatiivsed käibemaksukoodid selles grupis. Märkige ruut <strong>Pöördmaks</strong> käibemaksukoodile, millel on negatiivne väärtus.</td>
</tr>
<tr>
<td><strong>Kauba käibemaksugrupid</strong></td>
<td>Looge või uuendage kauba käibemaksugrupp käibemaksukoodiga, millel on negatiivne väärtus (<strong>Maks</strong> > <strong>Kaudsed maksud</strong> > <strong>Käibemaks</strong> > <strong>Kauba käibemaksugrupid</strong>). Kauba käibemaksu vaikegrupp tuleb määrata toodetele ja kategooriatele, millele kohaldatakse pöördmaksu.</td>
</tr>
</table>

## <a name="set-up-reverse-charge-groups"></a>Pöördmaksu gruppide seadistamine
Lehel **Pöördmaksu kaubagrupid** (**Maks** > **Seadistus** > **Käibemaks** > **Pöördmaksu kaubagrupid**) saate määratleda toodete või teenuste gruppe või eraldi tooteid või teenuseid, millele pöördmaksu saab rakendada. Määratlege iga pöördmaksu kaubagrupi puhul kaupade loend, kaubagrupid ja kategooriad müügi ja/või ostude jaoks.

## <a name="set-up-reverse-charge-rules"></a>Pöördmaksu reeglite häälestamine
Lehel **Pöördmaksu reeglid** (**Maks** > **Seadistus** > **Käibemaks** > **Pöördmaksu reeglid**) saate määratleda rakendatavuse reeglid ostu ja müügi eesmärkidele. Saate konfigureerida pöördmaksu rakendatavuse reeglikogumi. Määrake igale reeglile järgmised väljad.

- **Dokumendi tüüp** – valige **Ostutellimus**, **Hankija arve tööleht**, **Müügitellimus**, **Vabas vormis arve**, **Kliendi arve tööleht** ja/või **Hankija arve**.
- **Partneri riigi/piirkonna tüüp** – valige **Kodumaine**, **EL** või **Välismaine**. Kui reeglit ei saa rakendada kõigile äripartneritele, olenemata nende aadressi riigist või piirkonnast, siis on teine võimalus valida **Kõik**.
- **Riigisisene tarneaadress** – märkige see ruut reegli rakendamiseks tarnetele samas riigis või piirkonnas. Seda ruutu ei saa dokumenditüüpide **Hankija arve tööleht** ja **Kliendi arve tööleht** puhul valida.
- **Pöördmaksu kaubagrupp** – valige grupp, millele reeglit saab rakendada.
- **Lävisumma** – pöördmaksu skeem rakendatakse arvele ainult juhul, kui pöördmaksu kaubagrupis sisalduvate kaupade ja/või teenuste väärtus ületab siin määratud piirväärtuse.

Võite kasutada välju **Jõustumiskuupäev** ja **Aegumiskuupäev** reegli kehtivusperioodi määramiseks.

Lisaks saate määrata, kas kuvatakse teade ja dokumendireale lisatakse pöördkäibemaksu vaikegrupp, kui selle dokumendirea tingimus on täidetud. Valikud on järgmised:

- **Puudub** – dokumendirida ei uuendata.
- **Küsi** – kuvatakse teade, milles küsitakse kinnitust, kas pöördmaksu saab rakendada.
- **Määra** – dokumendi rida uuendatakse täiendava teatiseta.

## <a name="set-up-default-parameters"></a>Vaikeparameetrite seadistamine
Selle funktsiooni lubamiseks määrake lehel **Pearaamatu parameetrid** vahekaardil **Pöördmaks** valiku **Luba pöördmaks** väärtuseks **Jah**. Valige väljadel **Ostutellimuse käibemaksugrupp** ja **Müügitellimuse maksugrupp** käibemaksu vaikegrupid. Kui pöördmaksu rakendatavuse tingimus on täidetud, lisatakse müügi- või ostutellimuse reale need käibemaksugrupid.

## <a name="reverse-charge-on-a-sales-invoice"></a>Pöördmaks müügiarvel
Müügi korral pöördmaksu skeemi alusel ei küsi müüja käibemaksu. Selle asemel on arvel näidatud nii kaubad, millelt nõutakse pöördkäibemaksu, kui ka pöördkäibemaksu koondsumma.

Kui sisestatakse pöördkäibemaksuga müügiarve, on müügikannetel maksusuund **Tasumisele kuuluv käibemaks** ja nullkäibemaks ning ruut **Pöördmaks** on märgitud.

## <a name="reverse-charge-on-a-purchase-invoice"></a>Pöördmaks ostuarvel
Ostude korral pöördmaksu skeemi alusel tegutseb ostja, kes saab pöördmaksuga arve, käibemaksuarvestuse seisukohast ostja ja müüjana.

Pöördmaksuga ostuarve sisestamisel luuakse kaks käibemaksukannet. Ühel kandel on maksusuund **Saadaolev käibemaks**. Teisel kandel on maksusuund **Tasumisele kuuluv käibemaks** ja märgitud on ruut **Pöördmaks**.
