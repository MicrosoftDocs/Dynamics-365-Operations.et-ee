---
title: KM/GST-süsteemi pöördmaksustamise mehhanism
description: See teema selgitab, kuidas seadistada Euroopa riikide ja Saudi Araabia pöördkäibemaksu (KM).
author: epodkolz
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom, Singapore, Bahrain, Kuwait, Oman, Qatar
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b9996b4d6ab84070cc3e9863a454c4fd8ed14091490273cde0eec1ea2bc508fc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756222"
---
# <a name="reverse-charge-mechanism-for-vatgst-scheme"></a>KM/GST-süsteemi pöördmaksustamise mehhanism

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse üldist lähenemist pöördmaksustamise funktsiooni seadistamiseks riikidele/regioonidele, kes võtavad kasutusele käibemaksu või GST-skeemid.
                                                                                 
Funktsiooni riigi/regiooni kättesaadavust haldavad tööruumis **Funktsioonihaldus** järgmised funktsioonid.

| Funktsioon                                              | Riik/regioon                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spetsiifilised funktsioonid puuduvad                                | Austria </br>Belgia </br>Bulgaaria </br>Horvaatia </br>Küpros </br>Tšehhi Vabariik </br>Taani  </br>Eesti  </br>Soome  </br>Prantsusmaa  </br>Saksamaa  </br>Ungari  </br>Island  </br>Iirimaa  </br>Itaalia  </br>Läti  </br>Liechtenstein  </br>Leedu  </br>Luksemburg  </br>Holland  </br>Norra Poola </br>Portugal </br>Rumeenia  </br>Saudi Araabia </br>Singapur  </br>Slovakkia  </br>Sloveenia  </br>Hispaania  </br>Rootsi  </br>Šveits  </br>Ühendkuningriik  </br>Araabia Ühendemiraadid |
| Täiendavate riikide pöördmaksustamine            | Bahrein  </br>Kuveit  </br>Omaan  </br>Katar                                                                                                                                                                                                                                                                                                                                                                                                                         |
| KM-/GST-skeemi jaoks pöördkäibemaksu mehhanismi lubamine | Kõik muud riigid/regioonid, välja arvatud järgnevad.  </br>Brasiilia  </br>India  </br>Venemaa                                                                                                                                                                                                                                                                                                                                                                                         |
 
 Lisateabe saamiseks vt selles teemas hiljem tuevat jaotist [KM-/GST-skeemi jaoks pöördkäibemaksu mehhanismi lubamine](#enable-reverse-charge).

Pöördmaks on maksuskeem, mis viib käibemaksu arvestamise ja registreerimise kohustuse kaupade ja/või teenuste müüjalt ostjale. Seetõttu registreerivad kaupade ja/või teenuste saajad nii arvestatud käibemaksu (müüja rollis) kui ka sisendkäibemaksu (ostja rollis) oma käibemaksuaruandes.

Mõnes riigis või regioonis rakendatakse pöördmaksu skeemi ainult mõne kauba ja/või teenuse puhul ja müügisummadele on kehtestatud lisatingimused või piirväärtused. Teistes riikides või regioonides sõltub vastutus käibemaksu tasumise eest tarnija ja ostja olekust. Kui ostja on käibemaksukohustuslane, peab see asjaolu olema tarnija väljastatud arvel märgitud. Näiteks peavad arvel olema sõnad „pöördmaks” ja peab olema näidatud, millised kaubakoodid kuuluvad pöördmaksu skeemi alla. 

Pöördmaksu rakendamiseks tuleb teha järgmine seadistus.

## <a name="set-up-sales-tax-codes"></a>Saate häälestada käibemaksukoode.
Soovitame kasutada müügi- ja ostutoimingute jaoks eraldi käibemaksukoode.

<table>
<body>
<tr>
<td><strong>Müügi käibemaksukood</strong></td>
<td>Looge käibemaksukood müügi pöördmaksu toimingutele (<strong>Maks</strong> &gt; <strong>Kaudsed maksud</strong> &gt; <strong>Käibemaks</strong> &gt; <strong>Käibemaksukoodid</strong>).
</td>
</tr>
<tr>
<td><strong>Ostude käibemaksukood</strong></td>
<td><p>Looge positiivsed ja negatiivsed käibemaksukoodid ostude pöördkäibemaksule (<strong>Maks</strong> &gt; <strong>Kaudsed maksud</strong> &gt; <strong>Käibemaks</strong> &gt; <strong>Käibemaksukoodid</strong>).</p>
<ol>
<li>Looge positiivse väärtusega käibemaksukood.</li>
<li>Looge negatiivse väärtusega käibemaksukood. Määrake valiku <strong>Luba negatiivset käibemaksuprotsenti</strong> väärtuseks <strong>Jah</strong>.
See negatiivne käibemaksukood tuleb määrata kauba käibemaksugrupile ja seejärel selle kauba käibemaksugrupi kaupadele, mis kuuluvad pöördmaksuga käibemaksustamisele.</li>
</ol>
<p>Lisateavet leiate järgmisest jaotisest &quot;Käibemaksugruppide ja kauba käibemaksugruppide häälestamine&quot;.</p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><a name="sales-tax-item-sales-tax-groups"></a>Käibemaksugruppide ja kauba käibemaksugruppide seadistamine
Soovitame kasutada müügi- ja ostutoimingute jaoks eraldi käibemaksugruppe.

<table>
<tr>
<td><strong>Müügi käibemaksugrupid</strong></td>
<td>Looge käibemaksugrupp pöördmaksuga müügitoimingutele (<strong>Maks</strong> &gt; <strong>Kaudsed maksud</strong> &gt; <strong>Käibemaks</strong> &gt; <strong>Käibemaksugrupid</strong>). Vahekaardil <strong>Seadistus</strong> lisage sellesse gruppi pöördmaksu käibemaksukood. Märkige käibemaksukoodi väljad <strong>Vabastus</strong> ja <strong>Pöördmaks</strong>.</td>
</tr>
<tr>
<td><strong>Ostude käibemaksugrupid</strong></td>
<td>Looge käibemaksugrupp pöördmaksuga ostutoimingutele (<strong>Maks</strong> &gt; <strong>Kaudsed maksud</strong> &gt; <strong>Käibemaks</strong> &gt; <strong>Käibemaksugrupid</strong>). Lisage vahekaardile <strong>Seadistus</strong> nii positiivsed kui ka negatiivsed käibemaksukoodid selles grupis. Märkige ruut <strong>Pöördmaks</strong> käibemaksukoodile, millel on negatiivne väärtus.</td>
</tr>
<tr>
<td><strong>Kauba käibemaksugrupid</strong></td>
<td>Looge või värskendage kauba käibemaksugrupp käibemaksukoodiga, millel on negatiivne väärtus (<strong>Maks</strong> &gt; <strong>Kaudsed maksud</strong> &gt; <strong>Käibemaks</strong> &gt; <strong>Kauba käibemaksugrupid</strong>). Kauba käibemaksu vaikegrupp tuleb määrata toodetele ja kategooriatele, millele kohaldatakse pöördmaksu.</td>
</tr>
</table>

## <a name="set-up-reverse-charge-item-groups"></a><a name="reverse-charge-item-group"></a>Pöördmaksu üksuse gruppide seadistamine
Lehel **Pöördmaksu kaubagrupid** (**Maks** &gt; **Seadistus** &gt; **Käibemaks** &gt; **Pöördmaksu kaubagrupid**) saate määratleda toodete või teenuste gruppe või eraldi tooteid või teenuseid, millele pöördmaksu saab rakendada. Määratlege iga pöördmaksu kaubagrupi puhul kaupade loend, kaubagrupid ja kategooriad müügi ja/või ostude jaoks.

## <a name="set-up-reverse-charge-rules"></a><a name="reverse-charge-rules"></a>Pöördmaksu reeglite häälestamine
Lehel **Pöördmaksu reeglid** (**Maks** &gt; **Seadistus** &gt; **Käibemaks** &gt; **Pöördmaksu reeglid**) saate määratleda rakendatavuse reeglid ostu ja müügi eesmärkidele. Saate konfigureerida pöördmaksu rakendatavuse reeglikogumi. Määrake igale reeglile järgmised väljad.

- **Dokumendi tüüp** – valige **Ostutellimus**, **Hankija arve tööleht**, **Müügitellimus**, **Vabas vormis arve**, **Kliendi arve tööleht** ja/või **Hankija arve**.
- **Partneri riigi/piirkonna tüüp** – valige **Kodumaine**, **EL**, **GCC** või **Välismaine**. Kui reeglit ei saa rakendada kõigile äripartneritele, olenemata nende aadressi riigist või piirkonnast, siis on teine võimalus valida **Kõik**.
- **Riigisisene tarneaadress** – märkige see ruut reegli rakendamiseks tarnetele samas riigis või piirkonnas. Seda ruutu ei saa dokumenditüüpide **Hankija arve tööleht** ja **Kliendi arve tööleht** puhul valida.
- **Pöördmaksu kaubagrupp** – valige grupp, millele reeglit saab rakendada.
- **Lävisumma** – pöördmaksu skeem rakendatakse arvele ainult juhul, kui pöördmaksu kaubagrupis sisalduvate kaupade ja/või teenuste väärtus ületab siin määratud piirväärtuse.

Võite kasutada ka välju **Jõustumiskuupäev** ja **Aegumiskuupäev** reegli kehtivusperioodi määramiseks.

Lisaks saate määrata, kas kuvatakse teade ja dokumendireale lisatakse pöördkäibemaksu vaikegrupp, kui selle dokumendirea tingimus on täidetud. Valikud on järgmised:

- **Puudub** – dokumendirida ei uuendata.
- **Küsi** – kuvatakse teade, milles küsitakse kinnitust, kas pöördmaksu saab rakendada.
- **Määra** – dokumendi rida uuendatakse täiendava teatiseta.

## <a name="set-up-countryregion-properties"></a><a name="Set-up-Country/region-properties"></a>Riigi/regiooni atribuutide häälestamine
Seadke lehe **Väliskaubanduse parameetrid** (**Maks** &gt; **Häälestus** &gt; **Käibemaks** &gt; **Väliskaubandus** &gt; **Väliskaubanduse parameetrid**) vahekaardil **Riigi/regiooni atribuudid** praeguse juriidilise isiku riigi/regiooni väärtuseks *Kodumaine*. Määrake praeguse juriidilise isikuga ELi kaubanduses osalevate ELi **riikide/regioonide** riigi/regiooni tüübiks *EL*. Määrake praeguse juriidilise isikuga GCC kaubanduses osalevate GCC **riikide/regioonide** riigi/regiooni tüübiks *GCC*.

## <a name="set-up-default-parameters"></a>Vaikeparameetrite seadistamine
Pöördkäibemaksu funktsiooni lubamiseks määrake lehel **Pearaamatu parameetrid** vahekaardil **Pöördmaks** suvandi **Luba pöördmaks** väärtuseks **Jah**. Valige väljadel **Ostutellimuse käibemaksugrupp** ja **Müügitellimuse maksugrupp** käibemaksu vaikegrupid. Kui pöördmaksu rakendatavuse tingimus on täidetud, lisatakse müügi- või ostutellimuse reale need käibemaksugrupid.

## <a name="reverse-charge-on-a-sales-invoice"></a><a name="reverse-charge-sale"></a>Pöördmaks müügiarvel
Müügi korral pöördmaksu skeemi alusel ei küsi müüja käibemaksu. Selle asemel on arvel näidatud nii kaubad, millelt nõutakse pöördkäibemaksu, kui ka pöördkäibemaksu koondsumma.

Kui sisestatakse pöördkäibemaksuga müügiarve, on müügikannetel maksusuund **Tasumisele kuuluv käibemaks** ja nullkäibemaks ning ruut **Pöördkäibemaks** ja **Vabastus** on märgitud.

## <a name="reverse-charge-on-a-purchase-invoice"></a><a name="reverse-charge-purchase"></a>Pöördmaks ostuarvel
Ostude korral pöördmaksu skeemi alusel tegutseb ostja, kes saab pöördmaksuga arve, käibemaksuarvestuse seisukohast ostja ja müüjana.

Pöördmaksuga ostuarve sisestamisel luuakse kaks käibemaksukannet. Ühel kandel on maksusuund **Saadaolev käibemaks**. Teisel kandel on maksusuund **Tasumisele kuuluv käibemaks** ja märgitud on ruut **Pöördmaks**.

Järgneval kuvatõmmisel on ühe kande suund **Saadaolev käibemaks** ja teise kande suund **Tasumisele kuuluv käibemaks**. 

![Sisestatud käibemaks.](media/apac-sau-posted-sales-tax.png)

## <a name="enable-reverse-charge-mechanism-for-vatgst-scheme-feature"></a><a name="enable-reverse-charge"></a>KM-/GST-skeemi jaoks pöördkäibemaksu mehhanismi funktsiooni lubamine
Leidke tööruumis **Funktsioonihaldus** funktsioon ja valige suvand **Luba**.

Pärast funktsiooni lubamist on vahekaart **Pöördmaksustamine** kõikidel juriidilistel isikutel saadaval. Juriidilise isiku jaoks pöördmaksustamise funktsiooni lubamine, määrates suvandi **Luba pöördmaksustamine** väärtuseks **Jah**.

Saadaval on järgmised funktsiooni häälestusega seotud lehed ja menüükäsud.
 - **Pöördmaksustamise üksuse grupid** (**Maks** > **Seadistus** > **Müügimaks** > **Üksuste gruppide pöördmaksustamine**). Lisateavet vt jaotisest [Pöördmaksu üksuse gruppide seadistamine](#reverse-charge-item-group).
 - **Pöördmaksu reeglid** (**Maks** > **Seadistamine** > **Müügimaks** > **Pöördmaksustamise reeglid**). Vt teemat [Pöördmaksu reeglite häälestamine](#reverse-charge-rules).
 - **Väliskaubanduse parameetrid** (**Maks** > **Seadistus** > **Müügimaks** > **Väliskaubandus** > **Väliskaubanduse parameetrid**). Vt teemat [Riigi/regiooni atribuutide häälestamine](#Set-up-Country/region-properties).

Saadabal on märkeruut **Pöördmaksustamine** lehtedel **Käibemaksu grupp** ja **Sisestatud käibemaks**. Lisateavet vt jaotistest [Käibemaksugruppide ja kauba käibemaksugruppide häälestus](#sales-tax-item-sales-tax-groups), [Pöördmaks müügiarvel](#reverse-charge-sale) ja [Pöördmaks ostuarvel](#reverse-charge-purchase).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]