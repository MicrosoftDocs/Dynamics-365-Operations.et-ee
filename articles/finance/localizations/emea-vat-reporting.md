---
title: Euroopa käibemaksuaruandlus
description: See artikkel annab üldist teavet mõne Euroopa riigi käibemaksuaruande seadistamise ja loomise kohta.
author: mrolecki
ms.date: 03/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: mrolecki
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 266844
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
ms.openlocfilehash: 54be8844fadf744cc5527001737ab470fcec46d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283412"
---
# <a name="vat-reporting-for-europe"></a>Euroopa käibemaksuaruandlus

[!include [banner](../includes/banner.md)]

See artikkel annab üldist teavet mõne Euroopa riigi käibemaksuaruande seadistamise ja loomise kohta.

See artikkel pakub üldist lähenemist KM-aruande seadistamisele ja loomisele. See lähenemine on tavapärane kasutajate puhul järgmiste riikide/regioonide juriidiliste isikute puhul:

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

> [!IMPORTANT]
> Selles artiklis kirjeldatud funktsioonid Austria, Tšehhi Vabariigi, Saksamaa, Hollandi ja Rootsi puhul on taunitav. Lisateavet vt jaotisest Eemaldatud [ja aegunud funktsioonid](../get-started/removed-deprecated-features-finance.md).
> Kasutage järgmise tabeli linke, et saada lisateavet km-i deklaratsiooni uue kujunduse kohta vastavates riikides.
> 
>
> | Riik        | Lisateave                                                          |
> |----------------|---------------------------------------------------------------------------------|
> | Austria        | [KM-i deklaratsioon (Austria)](emea-aut-vat-declaration-austria.md)       |                                                                           
> | Tšehhi Vabariik | [KM-deklaratsioon (Tšehhi Vabariik](emea-cze-vat-declaration-tax-declaration-model.md) |
> | Taani        | [KM-deklaratsioon (Taani)](emea-dnk-vat-declaration-denmark.md)         |
> | Prantsusmaa         | [KM-i deklaratsioon (Prantsusmaa)](emea-fra-vat-declaration-preview-france.md)       |
> | Saksamaa        | [KM-i deklaratsioon (Saksamaa)](emea-deu-vat-declaration-germany.md)           |
> | Holland    | [KM-deklaratsioon (Holland)](emea-nl-vat-declaration-netherlands.md)    |
> | Norra         | [Käibemaksutagastus otseedastusega Altinnile](emea-nor-vat-return.md) |
> | Hispaania          | [KM-i deklaratsioon (Hispaania)](emea-esp-vat-declaration-spain.md)              |
> | Rootsi         | [KM-i deklaratsioon (Rootsi)](emea-swe-vat-declaration-sweden.md)          |
> | Šveits    | [KM-deklaratsioon (Šveits)](emea-che-vat-declaration-switzerland.md) |
> | Uk             | [Ettevalmistamine INTEGREERIMISEks MRD-ga KM jaoks](emea-gbr-mtd-vat-integration.md) |

## <a name="vat-statement-overview"></a>KM-aruande ülevaade
KM-aruanne põhineb maksukannete summadel. KM-aruande koostamise protsess kuulub käibemaksu tasumise protsessi juurde, mida rakendatakse funktsiooni Käibemaksu tasakaalustamine ja sisestamine kaudu. See funktsioon arvutab käibemaksu, mille tähtaeg jääb antud perioodi sisse. Tasakaalustuse arvutamine sisaldab maksukannete valitud tasakaalustusperioodil sisestatud käibemaksu. KM-aruande andmete arvutusprotsess põhineb käibemaksukoodide ja käibemaksuaruandluse koodide vahelisel seosel, mille alusel käibemaksuaruandluse koodid vastavad käibemaksuaruannete väljadele (või XML-i siltidele). Iga käibemaksukoodi puhul tuleb seadistada igale kandetüübile (nt maksustatav müügikäive, maksustatavad ostud, maksustatav import) käibemaksuaruandluse koodid. Seda tüüpi kandeid kirjeldatakse selles artiklis allpool olevates käibemaksuaruandluse jaotistes Käibemaksukoodid.

Iga käibemaksuaruandluse koodi puhul tuleb määrata konkreetne aruande paigutus. Samal ajal on käibemaksukoodid seotud käibemaksu tasakaalustamise perioodide kaudu konkreetse käibemaksuasutusega. Iga käibemaksuasutuse puhul tuleb määrata aruande paigutus. Seega saab käibemaksukoodi aruande seadistuses valida ainult sama aruande paigutusega KM-aruandluse koode, mis on seadistatud käibemaksuasutuse jaoks käibemaksukoodi käibemaksu tasakaalustusperioodil. Tellimuse või töölehe sisestamisel loodud käibemaksukanne sisaldab käibemaksukoodi, käibemaksu allikat, käibemaksu suunda ja kandesummasid (maksu põhisumma ja maksusumma arvestusvaluutas, käibemaksu valuuta ja kande valuuta). Maksukannete atribuutide kombinatsiooni põhjal koostavad kandesummad käibemaksukoodidele määratud käibemaksuaruandluse koodide koondsummad. Järgmine illustratsioon näitab andmete seost.

![diagramm.](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a>KM-aruande seadistus
KM-aruande koostamiseks tuleb seadistada järgmine.

### <a name="sales-tax-authorities-for-vat-reporting"></a>KM-asutused KM-aruandluse jaoks

Enne käibemaksuaruandluse koodide seadistamist tuleb valida käibemaksuasutuse jaoks õige aruande paigutus. Tehke lehel **Käibemaksuasutused** jaotises **Üldine** valik **Aruande paigutus**. Seda paigutust kasutatakse käibemaksuaruandluse koodide seadistamisel.

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a>Käibemaksuaruandluse koodid

Käibemaksuaruandluse koodid on väljade koodid KM-aruandes või siltide nimed XML-vormingus. Neid koode kasutatakse aruande summade liitmiseks ja ettevalmistamiseks. KM-aruande elektroonilise aruandluse vormingu konfigureerimisel kasutatakse saadud summade nimesid. Käibemaksuaruandluse koode saab luua ja hallata lehel **Käibemaksuaruandluse koodid**. Igale koodile tuleb määrata aruande paigutus. Pärast käibemaksuaruandluse koodide loomist saate valida koodid jaotisest **Aruande seadistus** lehel **Käibemaksukoodid**. <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a>Käibemaksukoodid KM-aruandluse jaoks

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).-->  Alussummad ja käibemaksukannete maksusummad saab KM-aruandes aruandluskoodide all summeerida (XML-sildid või deklaratsiooni väljad). Selle saab seadistada, seostades käibemaksukoodide erinevate kandetüüpide käibemaksuaruandluse koodid lehel <strong>Käibemaksukoodid</strong>. Järgmises tabelis kirjeldatakse kandetüüpe käibemaksukoodide aruande seadistuses. Arvutus sisaldab kandeid kõigi allikatüüpide kohta, v.a käibemaks.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Kande tüüp</strong></td>
<td><strong>Kande tüübi all arvestatud kannete ja summade kirjeldus</strong></td>
</tr>
<tr class="even">
<td><strong>Maksustatav müük</strong></td>
<td>Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil /</li>
<li>Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Maksuvaba müük</strong></td>
<td>Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li>Müük on eksport (<strong>Maksu suund</strong> on <strong>Maksuvaba müük</strong>).</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Tasumisele kuuluv käibemaks</strong></td>
<td>Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li>Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Maksustatava müügi kreeditarve</strong></td>
<td>Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li>Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Maksuvaba müügi kreeditarve</strong></td>
<td>Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li>Müük on eksport (<strong>Maksu suund</strong> on <strong>Maksuvaba müük</strong>).</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Käibemaks müügi kreeditarvel</strong></td>
<td>Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li>Müük on siseriiklik (<strong>Maksu suund</strong> on <strong>Tasumisele kuuluv käibemaks</strong>).</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Maksustatavad ostud</strong></td>
<td>Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li>Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Maksuvaba ost</strong></td>
<td>Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li>Ost on import (<strong>Maksu suund</strong> on <strong>Maksuvaba ost</strong>).</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Saadaolev käibemaks</strong></td>
<td>Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li>Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Maksustatav ostu kreeditarve</strong></td>
<td>Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li>Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Maksuvaba ostu kreeditarve</strong></td>
<td>Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li>Ost on import (<strong>Maksu suund</strong> on <strong>Maksuvaba ost</strong>).</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Käibemaks ostu kreeditarvel</strong></td>
<td>Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li>Ost on siseriiklik (<strong>Maksu suund</strong> on <strong>Saadaolev käibemaks</strong>).</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Maksustatav import</strong></td>
<td>Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong></li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Tasakaalusta maksustatav import</strong></td>
<td>Väärtuste <strong>Maksu baassummad</strong> pöördsumma kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Maksustatava impordi kreeditarve</strong></td>
<td>Väärtuste <strong>Maksu baassummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
e<li><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Tasakaalusta maksustatav impordi kreeditarve</strong></td>
<td>Väärtuste <strong>Maksu baassummad</strong> pöördsumma kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li>Maksusuund on <strong>Kasutusmaks</strong>.</li>
d<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &lt; 0.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Kasutusmaks</strong></td>
<td>Väärtuste <strong>Maksusummad</strong> summa kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Kasutusmaksu vastasmaks</strong></td>
<td>Väärtuste <strong>Maksusummad</strong> pöördsumma kannete puhul, mis vastavad järgmistele tingimustele.
<ul>
<li>Kande kuupäev on valitud perioodil.</li>
<li><strong>Maksusuund</strong> on <strong>Kasutusmaks</strong>.</li>
<li>Kande <strong>Maksu baassumma</strong> või <strong>Maksu summa</strong> &gt; 0.</li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Ülal antud tabeli puhul eeldatakse, et täidetud on järgmised tingimused. 
> -   Maksu baassumma on kande summa väljalt **Päritolu arvestusvaluutas**.
> -   Maksu baassumma on üleviidav summa väljalt **Tegelik käibemaksusumma arvestusvaluutas**.

### <a name="configure-the-er-model-and-format-for-the-report"></a>ER-mudeli ja aruande vormingu konfigureerimine

Elektroonilist aruandlust (ER) saab kasutada väljavõtete ja aruande konfigureerimiseks ning andmete eksportimiseks erinevates elektroonilistes vormingutes, X++ koodi muutmata. Lisateave:

-   [Elektroonilise aruandluse ülevaade](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)
-   [Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [Lokaliseerimisnõuded – GER-i konfiguratsiooni loomine](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a>Riigipõhised ressursid KM-aruannete puhul
Iga riigi KM-aruanne peab vastama selle riigi seaduste nõuetele. Järgmises tabelis loetletud riikide puhul on olemas KM-aruannete eelmääratud üldised mudelid ja vormingud.


| Riik        | Lisateave                                                          |
|----------------|---------------------------------------------------------------------------------|
| Austria        | [KM-aruande üksikasjad Austria puhul](emea-aut-vat-statement-details.md)         |
| Belgia        |                                                                                 |
| Tšehhi Vabariik | [KM-aruanne Tšehhi Vabariigis](emea-cze-vat-statement-details.md)   |
| Eesti        | [KM-aruande üksikasjad Eesti puhul](emea-est-vat-statement-details.md) |
| Soome        | [Soome käibemaksu aruanne](emea-fin-sales-tax-payment-report-finland.md)          |
| Saksamaa        | [Saksamaa KM-i deklaratsioon](emea-de-vat-declaration.md)                       |
| Itaalia          | [KM-aruannete üksikasjad Itaalias](emea-ita-vat-statements-details.md)            |
| Läti         | [KM-aruande üksikasjad Läti puhul](emea-lva-vat-statement-details.md)           |
| Leedu      | [KM-aruande üksikasjad Leedu puhul](emea-ltu-vat-statement-details.md)         |
| Holland    | [KM-i deklaratsiooni vorming Hollandi puhul](emea-nl-vat-declaration.md)           |
| Rootsi         | [Rootsi käibemaksu aruanne](emea-swe-sales-tax-payment-report-sweden.md)          |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
