---
title: "Käibemaksuaruande Euroopa"
description: "Selles teemas kirjeldatakse seadistamine ja loomine mõnes Euroopa riigis käibemaks (VAT) lause."
author: ShylaThompson
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266844
ms.assetid: 06798e29-6140-489e-9b4e-66b45b26be2b
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 84a639b25c64821e00ca4397f42f69298953e599
ms.lasthandoff: 03/31/2017


---

# <a name="vat-reporting-for-europe"></a>Käibemaksuaruande Euroopa

Selles teemas kirjeldatakse seadistamine ja loomine mõnes Euroopa riigis käibemaks (VAT) lause.

See teema pakub üldist lähenemisviisi seadistamine ja km aruande loomine. Selline lähenemine on tavaline kasutajatele juriidiliste isikute järgmistes riikides/piirkondades:

-   Austria
-   Belgia
-   Tšehhi Vabariik
-   Eesti
-   Soome
-   Saksamaa
-   Läti
-   Leedu
-   Holland
-   Rootsi

## <a name="vat-statement-overview"></a>KM aruande ülevaade
KM aruande põhineb maksu kannete summad. KM aruande loomisel on käibemaksu maksmise käigus, mida rakendatakse läbi Settle ja post käibemaksu funktsiooni. See funktsioon arvutab käibemaksu, mis on tingitud teatava ajavahemiku jooksul. Tasakaalustuse arvutamisse sisestatud käibemaks maksukannete valitud tasakaalustusperioodil. KM aruande andmete arvutamise protsessi aluseks käibemaksukoodide ja Käibemaksuaruandluse koodide, kus käibemaksu koodid vasta käibemaksu ütlusi kastid (ja sildid XML) suhe. Iga käibemaksukoodi käibemaksu koodid tuleb seadistada igat liiki tehingu maksustatavat kaupa, nagu maksustatavaid oste, maksustatava impordi. Need tüüpi tehingud on kirjeldatud kui [käibemaksu koodid km aruandlus](#Sales tax codes for VAT reporting) lõik käesoleva teema.

Iga käibemaksukoodi, tuleks määrata kindla aruande paigutus. Samal ajal on käibemaksu koodiga seotud kindlatest asutuse kaudu Käibemaksu tasakaalustusperioodid. Iga käibemaksuhalduri määratakse aruande kavandi. Seega, ainult Käibemaksuaruandluse koodid seadistatakse jaoks maksuhaldur käibemaksu tasakaalustusperioodid käibemaksu sama aruande kavandi valimist käibemaksu aruande seadistamisel. Käibemaksu kande korral tellimuse või žurnaali, sisaldab käibemaksukood, käibemaksu allikas, suund ja tehingu summad (käibemaksu ja tulumaksu summa raamatupidamise valuuta, käibemaksu, valuuta ja tehingu valuuta). Vastavalt maksu tehingu atribuutide kombinatsioon, tehingu summad moodustavad Käibemaksuaruandluse koodid määratletud käibemaksukoodide kogusummad. Järgmine joonis näitab andmeid.

![diagramm](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>KM aruande seadistamine
KM aruande loomiseks peate seadistama järgmised.

### <a name="sales-tax-authorities-for-vat-reporting"></a>Maksuhaldur käibemaksu aruandluseks

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-authorities/). -->
Enne Käibemaksuaruandluse koodide valige maksuhaldur õige aruande paigutuse. Kohta ning **maksuhaldur** lehekülg, mis on **üldise** jaotises Valige on **aruande paigutus**. See kujundus kasutab Käibemaksuaruandluse koodide seadistamisel.

### <a name="sales-tax-reporting-codes"></a>Käibemaksuaruandluse koodid

Käibemaksu koodid on boksi koodid km silt või avaldus nimed XML-vormingus. Neid koode kasutatakse koondab ja koostab aruande summad. KM aruande aruande elektrooniliselt konfigureerimisel kasutatakse tulemuse summad nimed. Saate luua ja hallata Käibemaksuaruandluse koodide kohta ning **Käibemaksuaruandluse koodide** lehel. Peate määrama iga kood aruande kavandi. Käibemaksuaruandluse koodide loomise järel saate koodid on **seadistus** jaotises on **käibemaksukoodide** lehel. <!---For more information, see [Set up sales tax reporting codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-reporting-codes/) and [Sales tax reporting codes page (Field descriptions)](http://ax.help.dynamics.com/en/wiki/sales-tax-reporting-codes-page-field-descriptions/).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>Käibemaksu koodiga km aruandlus

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](http://ax.help.dynamics.com/en/wiki/set-up-sales-tax-codes/).-->Summade alus ja maksustamine saab liita tehingute käibemaksu summad aruandluskoodid km aruande (XML-silte või deklaratsiooni lahtrid). Seadistage see täiendavaid Käibemaksuaruandluse koodid erinevad tüübid käibemaksukoodi kohta ning **käibemaksu koodiga** lehel. Järgnev tabel kirjeldab kuvamiseks aruande seadistus käibemaksukoode. Arvutus hõlmab igat liiki allikatest, välja arvatud käibemaksu kandeid.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Transaction type</strong></td>
<td><strong>Tehingute ja summad arvestatakse tehingu liigi kirjeldus</strong></td>
</tr>
<tr class="even">
<td><strong>Maksustatav müük</strong></td>
<td>Summa <strong>maksu baasi summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud /</li>
<li>Müümine on siseriikliku (<strong>käibemaksu suund</strong> on <strong>tasumisele kuuluva</strong>).</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Tax-free müük</strong></td>
<td>Summa <strong>maksu baasi summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li>Müük on eksport (<strong>käibemaksu suund</strong> on <strong>maksuvaba müük</strong>).</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sales tax payable</strong></td>
<td>Summa <strong>maksude summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li>Müümine on siseriikliku (<strong>käibemaksu suund</strong> on <strong>tasumisele kuuluva</strong>).</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Taxable sales credit note</strong></td>
<td>Summa <strong>maksu baasi summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li>Müümine on siseriikliku (<strong>käibemaksu suund</strong> on <strong>tasumisele kuuluva</strong>).</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Faks maksuvaba müügi kreeditarve</strong></td>
<td>Summa <strong>maksu baasi summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li>Müük on eksport (<strong>käibemaksu suund</strong> on <strong>maksuvaba müük</strong>).</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sales tax on sales credit note</strong></td>
<td>Summa <strong>maksude summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li>Müümine on siseriikliku (<strong>käibemaksu suund</strong> on <strong>tasumisele kuuluva</strong>).</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable purchases</strong></td>
<td>Summa <strong>maksu baasi summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li>Ostmine on kodune (<strong>käibemaksu suund</strong> on <strong>saadaolev käibemaks</strong>).</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Tax-free purchase</strong></td>
<td>Summa <strong>maksu baasi summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li>Import on (<strong>käibemaksu suund</strong> on <strong>maksuvaba ost</strong>).</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sales tax receivable</strong></td>
<td>Summa <strong>maksude summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li>Ostmine on kodune (<strong>käibemaksu suund</strong> on <strong>saadaolev käibemaks</strong>).</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Taxable purchase credit note</strong></td>
<td>Summa <strong>maksu baasi summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li>Ostmine on kodune (<strong>käibemaksu suund</strong> on <strong>saadaolev käibemaks</strong>).</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Tax exempt purchase credit note</strong></td>
<td>Summa <strong>maksu baasi summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li>Import on (<strong>käibemaksu suund</strong> on <strong>maksuvaba ost</strong>).</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sales tax on purchase credit note</strong></td>
<td>Summa <strong>maksude summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li>Ostmine on kodune (<strong>käibemaksu suund</strong> on <strong>saadaolev käibemaks</strong>).</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable import</strong></td>
<td>Summa <strong>maksu baasi summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li><strong>Käibemaksu suund</strong> on <strong>kasutada maksu</strong></li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset taxable import</strong></td>
<td>Tühistatud summa <strong>maksu baasi summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li><strong>Käibemaksu suund</strong> on <strong>kasutada maksu</strong>.</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Taxable import credit note</strong></td>
<td>Summa <strong>maksu baasi summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
e<li><strong>Käibemaksu suund</strong> on <strong>kasutada maksu</strong>.</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset taxable import credit note</strong></td>
<td>Tühistatud summa <strong>maksu baasi summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li>Suund on <strong>kasutada maksu</strong>.</li>
d<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Use tax</strong></td>
<td>Summa <strong>maksude summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li><strong>Käibemaksu suund</strong> on <strong>kasutada maksu</strong>.</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Offset use tax</strong></td>
<td>Tühistatud summa <strong>maksude summad</strong> maksukannete, mis vastavad järgmistele tingimustele:
<ul>
<li>Kande kuupäev on valitud.</li>
<li><strong>Käibemaksu suund</strong> on <strong>kasutada maksu</strong>.</li>
<li>Tehingu <strong>käibemaksu</strong> või <strong>maksusumma</strong>&gt; 0.</li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Ülaltoodud tabelis eeldatakse järgmistel tingimustel: 
> -   Käibemaksu on tehingu summa: selle **päritolu raamatupidamise valuutas** välja.
> -   Maksusumma on üleminek: selle **tegelik Käibemaksusumma valuutas raamatupidamise** välja.

### <a name="configure-the-er-model-and-format-for-the-report"></a>ER mudeli ja aruande vormi kohta

Elektroonilise aruandluse (ER) saate seadistada avalduste ja aruande ja eksportida andmeid eri elektroonilistes formaatides X ++ koodi muutmata. Lisainfo:

-   [Elektroonilise aruandluse ülevaade](/dynamics365/operations/dev-itpro/dev-itpro/analytics/general-electronic-reporting)
-   [Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)
-   [Lokaliseerimine nõue – GER konfiguratsiooni loomine](/dynamics365/operations/dev-itpro/analytics/electronic-reporting-configuration)

## <a name="countryspecific-resources-for-vat-statements"></a>KM aruannete Countryspecific ressursid
KM aruande iga riigi vastama riigi õigusaktidega. On eelnevalt määratletud üldised mudelid ja formaadid Käibemaksudeklaratsioonide koostamisel järgmises tabelis loetletud riigid.


| Riik        | Lisateave                                                          |
|----------------|---------------------------------------------------------------------------------|
| Austria        |  [Austria käibemaksu väljavõtte üksikasjad](emea-aut-vat-statement-details.md)         |
| Belgia        |                                                                                 |
| Tšehhi Vabariik |  [Käibemaksu väljavõtte üksikasjad Tšehhi Vabariik](emea-cze-vat-statement-details.md)   |
| Eesti        |  [Käibemaksu väljavõtte üksikasjad Eesti](emea-est-vat-statement-details.md) |
| Soome        |                                                                                 |
| Saksamaa        |                                                                                 |
| Itaalia          | [Käibemaksu väljavõtte üksikasjad, Itaalia](emea-ita-vat-statements-details.md)            |
| Läti         | [Läti käibemaksu väljavõtte üksikasjad](emea-lva-vat-statement-details.md)           |
| Leedu      | [Käibemaksu väljavõtte üksikasjad Leedu](emea-ltu-vat-statement-details.md)         |
| Holland    |                                                                                 |
| Rootsi         |                                                                                 |




