---
title: Käitusaja probleemide ennetamiseks konfigureeritud ER-i komponendi kontrollimine
description: Selles teemas selgitatakse, kuidas kontrollida konfigureeritud elektroonilise aruandluse (ER) komponente, et vältida tekkida võivaid käitusaja probleeme.
author: NickSelin
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 309e613b707222920936d5af995ac57c4c423b40
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357662"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a>Käitusaja probleemide ennetamiseks konfigureeritud ER-i komponendi kontrollimine

[!include[banner](../includes/banner.md)]

Kõik konfigureeritud [elektroonilise aruandluse (ER)](general-electronic-reporting.md) [vormingu](general-electronic-reporting.md#FormatComponentOutbound) ja [mudeli vastendamise](general-electronic-reporting.md#data-model-and-model-mapping-components) komponendid saab kujundamise ajal [kontrollida](er-fillable-excel.md#validate-an-er-format). Selle kinnitamise ajal töötab järjepidevuse kontroll, et aidata ennetada esineda võivaid käitusaja probleeme, nt käivitustõrked ja jõudluse halvenemine. Iga leitud probleemi puhul esitab kontroll probleemse elemendi jaoks tee. Osade probleemide puhul on saadaval automaatne parandus.

Vaikimisi rakendatakse ER-i konfiguratsioonile automaatselt kontroll järgmistel juhtudel, mis sisaldab eelnevalt nimetatud ER-i komponente.

- Te [impordite](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) ER-i konfiguratsiooni uue [versiooni](general-electronic-reporting.md#component-versioning) oma Microsoft Dynamics 365 Finance’i olemisse.
- Muudate redigeeritava ER-i konfiguratsiooni [oleku](general-electronic-reporting.md#component-versioning) valikult **Mustand** valikule **Lõpetatud**.
- Muudate redigeeritava ER-i konfiguratsiooni [alust](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase), rakendades uue alusversiooni.

Selle kontrolli saate käivitada otse. Valige üks järgmisest kolmest valikust ja järgige esitatud samme.

- 1. valik.

    1. Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.
    2. Valige konfiguratsioonide puus vasakul paanil soovitud ER-i konfiguratsioon, mis sisaldab ER-i vormingut või ER-i mudeli vastendamise komponenti.
    3. Kiirkaardil **Versioonid** valige valitud ER-i konfiguratsiooni soovitud versioon.
    4. Valige toimingupaanil **Kinnita**.

- 2. valik, ER-i vormingu jaoks.

    1. Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.
    2. Valige konfiguratsioonide puus vasakul paanil soovitud ER-i konfiguratsioon, mis sisaldab ER-i vormingu komponenti.
    3. Kiirkaardil **Versioonid** valige valitud ER-i konfiguratsiooni soovitud versioon.
    4. Valige toimingupaanil valik **Koostaja**.
    5. Valige lehe **Vormingu koostaja** toimingupaanil suvand **Kinnita**.

- 3. valik, ER-i mudeli vastendamine.

    1. Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.
    2. Valige konfiguratsioonide puus vasakul paanil soovitud ER-i konfiguratsioon, mis sisaldab ER-i mudeli vastendamise komponenti.
    3. Kiirkaardil **Versioonid** valige valitud ER-i konfiguratsiooni soovitud versioon.
    4. Valige toimingupaanil valik **Koostaja**.
    5. Tehke lehe **Mudelist andmeallikasse vastendamine** tegevuse paanil valik **Kujundaja**.
    6. Tehke lehe **Mudelivastenduse kujundaja** tegevuse paanil valik **Kinnita**.

Kui konfiguratsioon on imporditud, järgige kinnitamise vahele jätmiseks järgmisi samme.

1. Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Määrake valik **Konfiguratsiooni kinnitamine pärast importimist** valikule **Ei**.

Versiooni oleku muutumisel või aluse muutmisel kinnitamise vahele jätmiseks toimige järgmiselt.

1. Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Määrake valik **Konfiguratsiooni oleku muutmise ja lahendamise vahele jätmine** väärtusele **Jah**.

ER kasutab järjepidevuse kontrollide rühmitamiseks järgmisi kategooriaid.

- **Täidetavus** – kontrollimised, mis tuvastavad käitamise ajal esineda võivad kriitilised probleemid. Need probleemid on enamasti tasemel **Tõrge**. 
- **Jõudlus** – kontrollimised, mis tuvastavad probleemid, mis võivad põhjustada konfigureeritud ER-i komponentide ebatõhusat käitamist. Need probleemid on enamasti tasemel **Hoiatus**.
- **Andmete terviklikkus** – kontrollimised, mis tuvastavad andmete kadu või käitusaja probleeme põhjustada võivad probleemid. Need probleemid on enamasti tasemel **Hoiatus**.

## <a name="list-of-inspections"></a>Kontrollimiste loend

Järgmises tabelis antakse ülevaade ER-i pakutavate kontrollide ülevaade. Nende kontrollimiste kohta lisateabe saamiseks kasutage esimeses veerus olevaid linke, et minna selle teema vastavatesse jaotistesse. Need jaotised selgitavad komponentide tüüpe, mille jaoks ER kontrolle pakub, ja kuidas saate probleemide ennetamise abistamiseks ER-i komponente uuesti konfigureerida.

<table>
<thead>
<tr>
<th>Nimi</th>
<th>Kategooria</th>
<th>Tase</th>
<th>Sõnum</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href='#i1'>Tüübiteisendus</a></td>
<td>Täidetavus</td>
<td>Viga</td>
<td>
<p>Ei saa teisendada avaldist tüüp &lt;tüüp&gt; väljaks tüüp &lt;tüüp&gt;.</p>
<p><b>Käitusaja tõrge:</b> tüübi erand</p>
</td>
</tr>
<tr>
<td><a href='#i2'>Tüübi ühilduvus</a></td>
<td>Täidetavus</td>
<td>Viga</td>
<td>
<p>Konfigureeritud avaldist ei saa kasutada praeguse vormingu elemendi sidumiseks andmeallikaga, kuna see avaldis tagastab andmetüübi &lt;tüüp&gt; väärtuse, mis on väljaspool andmetüüpide ulatust, mida tüübi &lt;tüüp&gt; praeguse vormindamise elemendiga toetatakse.</p>
<p><b>Käitusaja tõrge:</b> tüübi erand</p>
</td>
</tr>
<tr>
<td><a href='#i3'>Puuduv konfiguratsiooni element</a></td>
<td>Täidetavus</td>
<td>Viga</td>
<td>
<p>Teed ei leitud &lt;tee&gt;.</p>
<p><b>Käitusaja tõrge:</b> konfiguratsiooni teed &lt;tee&gt; ei leitud element</p>
</td>
</tr>
<tr>
<td><a href='#i4'>Funktsiooniga FILTER avaldise täidetavus</a></td>
<td>Täidetavus</td>
<td>Viga</td>
<td>
<p>Funktsiooni FILTER loendi avaldis ei ole päringuobjektiks sobilik.</p>
<p><b>Käitusaja tõrge:</b> filtreerimist ei toetata. Kontrollige konfiguratsiooni, et saada selle kohta lisateavet.</p>
</td>
</tr>
<tr>
<td rowspan='2'><a href='#i5'>Andmeallika GROUPBY täidetavus</a></td>
<td>Täidetavus</td>
<td>Viga</td>
<td>Tee &lt;tee&gt; ei toeta päringuid.</td>
</tr>
<tr>
<td>Täidetavus</td>
<td>Viga</td>
<td>
<p>Funktsiooni alusel rühmitamist ei saa päringuga käivitada.</p>
<p><b>Käitusaja tõrge:</b> funktsiooni alusel rühmitamist ei saa päringuga käivitada.</p>
</td>
</tr>
<tr>
<td><a href='#i6'>Andmeallika JOIN täidetavus</a></td>
<td>Täidetavus</td>
<td>Viga</td>
<td>
<p>Loendiga &lt;teega&gt;, mis ei ole päringufilter, ei saa liituda.</p>
<p><b>Käitusaja tõrge:</b> funktsioon Liidetud andmeallikas peab olema filtri avaldise arvutatud väli on valesti kutsutud.</p>
</td>
</tr>
<tr>
<td><a href='#i7'>Funktsiooni FILTER vs WHERE eelistatavus</a></td>
<td>Jõudlus</td>
<td>Hoiatus</td>
<td>Jõudluse vaatenurgast on avaldise jaoks funktsiooni FILTER kasutamine eelistatavam kui filtri WHERE kasutamine. Selle automaatselt asendamiseks valige suvand Paranda.</td>
</tr>
<tr>
<td><a href='#i8'>Funktsiooni ALLITEMSQUERY vs ALLITEMS eelistatavus</a></td>
<td>Jõudlus</td>
<td>Hoiatus</td>
<td>Jõudluse vaatenurgast on avaldise jaoks funktsiooni ALLITEMSQUERY kasutamine eelistatavam kui filtri ALLITEMS kasutamine. Selle automaatselt asendamiseks valige suvand Paranda.</td>
</tr>
<tr>
<td><a href='#i9'>Tühja loendiga juhtumite arvesse võtmine</a></td>
<td>Täidetavus</td>
<td>Hoiatus</td>
<td>
<p>Loendil &lt;teel&gt; ei ole ühtegi kontrolli tühja loendi juhtumi korral ja see võib põhjustada käitusaja tõrget. Loendi juhtumi tühjendamiseks lisage kontroll.</p>
<p><b>Käitusaja tõrge:</b> loend on asukohas &lt;tee&gt; tühi</p>
<p><b><a href='#i9a'>Võimalik probleem</a>:</b> rida asustatakse üks kord, samas kui andmeallikas on asustatud mitmes kirjas sisalduva põhjal</p>
</td>
</tr>
<tr>
<td><a href='#i10'>Funktsiooniga FILTER avaldise täidetavus (vahemällu salvestamine)</a></td>
<td>Täidetavus</td>
<td>Viga</td>
<td>
<p>Funktsiooni FILTER ei saa valitud andmeallika tüübile rakendada. Tabeli kirjete tüübi andmeallikas on rakendatav ainult siis, kui see ei ole vahemällu salvestatud, ja sellele ei ole käsitsi lisatud pesastatud andmeallikaid.</p>
<p><b>Käitusaja tõrge:</b> filtreerimist ei toetata. Kontrollige konfiguratsiooni, et saada selle kohta lisateavet.</p>
</td>
</tr>
<tr>
<td><a href='#i11'>Puuduv sidumine</a></td>
<td>Täidetavus</td>
<td>Hoiatus</td>
<td>
<p>Teel &lt;tee&gt; puudub mudeli vastendamist kasutades mis tahes andmeallikaga sidumine.</p>
<p><b>Käitusaja tõrge:</b> tee &lt;tee&gt; ei ole seotud</p>
</td>
</tr>
<tr>
<td><a href='#i12'>Linkimata mall</a></td>
<td>Andmete terviklikkus</td>
<td>Hoiatus</td>
<td>Fail &lt;nimi&gt; ei ole lingitud ühegi faili komponendiga ja eemaldatakse pärast konfiguratsiooni versiooni oleku muutmist.</td>
</tr>
<tr>
<td><a href='#i13'>Sünkroonimata vorming</a></td>
<td>Andmete terviklikkus</td>
<td>Hoiatus</td>
<td>Määratletud nime &lt;komponendi nimi&gt; ei ole Exceli lehel &lt;lehe nimi&gt; olemas</td>
</tr>
<tr>
<td><a href='#i14'>Sünkroonimata vorming</a></td>
<td>Andmete terviklikkus</td>
<td>Hoiatus</td>
<td>
<p>&lt;Wordi sildiga märgistatud&gt; sisu kontrollsilti pole Wordi mallifailis</p>
<p><b>Käivitustõrge:</b> &lt;Wordi sildiga märgistatud sisu kontroll&gt; silti pole Wordi mallifailis.</p>
</td>
</tr>
<tr>
<td><a href='#i15'>Vaikevastendus puudub</a></td>
<td>Andmete terviklikkus</td>
<td>Viga</td>
<td>
<p>Rohkem kui üks mudeli vastendamine &lt;esineb mudelinime (juurdeskriptori)&gt; andmemudeli konfiguratsioonides &lt;komaga eraldatuna&gt;. Määrake üks konfiguratsioonides vaikeväärtuseks</p>
<p><b>Käivitamistõrge:</b> Rohkem kui üks mudeli vastendamine esineb &lt;mudelinime (juureskriptori)&gt; andmemudeli konfiguratsioonides &lt;komaga eraldatuna&gt;. Määrake üks konfiguratsioonides vaikeväärtuseks.</p>
</td>
</tr>
<tr>
<td><a href='#i16'>Päise või jaluse komponentide ebaühtlane seadistus</a></td>
<td>Andmete terviklikkus</td>
<td>Viga</td>
<td>
<p>Päised/jalused (&lt;komponendi tüüp: päis või jalus&gt;) pole kooskõlas</p>
<p><b>Käitusaeg:</b> Viimast konfigureeritud komponenti kasutatakse käitusajal, kui konfigureeritud ER-vormingu mustandversioon on käivitatud.</p>
</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a>Tüübiteisendus

ER kontrollib, kas andmemudeli välja andmetüüp ühtib avalduse andmetüübiga, mis on konfigureeritud selle välja sidumiseks. Kui andmetüübid on ühildumatud, esineb ER-i mudeli vastendamise kujundajas valideerimise tõrge. Teie poolt vastu võetav teade annab teada, et ER ei saa teisendada tüübi A avaldist tüübi B väljaks.

Järgmised etapid näitavad, kuidas see probleem võib ilmneda.

1. Hakake konfigureerima ER-i andmemudeli ja ER-i mudeli kaardistamise komponente samaaegselt.
2. Lisage andmemudeli puus väli, mille nimi on **X**, ja valige andmetüübiks **Täisarv**.

    ![X-väli ja andmetüüp Integer lisati andmemudeli lehel andmerežiimi puule.](./media/er-components-inspections-01.png)

3. Mudeli vastendamise disainis **andmeallikate** paanil lisage tüübi **Arvutatud väli** andmeallikas.
4. Pange uue andmeallika nimeks **Y** ja konfigureerige see nii, et see sisaldaks avaldist `INTVALUE(100)`.
5. Siduge omavahel **X** ja **Y**.
6. Muutke andmemudeli kujundajas välja **X** andmetüüp väärtusest **Täisarv** valikule **Int64**.
7. Valige nupp **Kontrolli**, et kontrollida redigeeritava mudeli vastendamise komponenti lehel **Mudeli vastendamise kujundaja**.

    ![Redigeeritava mudeli vastendamise komponendi kinnitamine lehel mudeli vastendamise kujundaja.](./media/er-components-inspections-01.gif)

8. Valige suvand **Kinnita**, et kontrollida valitud ER-i konfiguratsiooni mudeli vastendamise komponent lehel **Konfigureerimised**.

    ![Kinnitage, et kontrollida mudeli vastendamise komponenti konfiguratsioonide lehel.](./media/er-components-inspections-01a.png)

9. Pange tähele, et kuvatakse valideerimise tõrge. Sõnumis on toodud, et tüübi **Täisarv** väärtus, mille avaldis `INTVALUE(100)` andmeallika **Y** puhul tagastas, ei saa talletada andmemudeli **X** väljal tüübiga **Int64**.

Järgmisel illustratsioonil on toodud käitusaja tõrge, mis ilmneb, kui te eirate hoiatust ja valite suvandi **Käivita**, et käitada vormingut, mis on konfigureeritud kasutama mudeli vastendamist.

![Käitusaja tõrked lehel Vormingu kujundaja.](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a>Automaatne lahendamine

Selle probleemi automaatseks lahendamiseks pole saadaval ühtegi valikut.

### <a name="manual-resolution"></a>Käsitsi lahendamine

#### <a name="option-1"></a>Suvand 1

Värskendage andmemudeli struktuuri, muutes selle andmetüübi välja andmetüüpi nii, et see ühtiks avaldise andmetüübiga, millega see on konfigureeritud, et ühendada see andmetüüp. Eelmise näite puhul tuleb välja **X** andmetüüp muuta tagasi väärtusele **Täisarv**.

#### <a name="option-2"></a>Suvand 2

Uuendage mudeli vastendust, muutes andmeallika avaldist, mis on seotud andmemudeli väljaga. Eelmise näite puhul tuleb andmeallikas **Y** muuta suvandile `INT64VALUE(100)`.

## <a name="type-compatibility"></a><a id="i2"></a>Tüübi ühilduvus

ER kontrollib, kas vormingu elemendi andmetüüp ühtib avalduse andmetüübiga, mis on konfigureeritud selle vormingu elemendi sidumiseks. Kui andmetüübid on ühildumatud, esineb ER-i toimingute kujundajas valideerimise tõrge. Teile kuvatavas sõnumis on kirjas, et konfigureeritud avaldist ei saa kasutada vormingu elemendi andmeallikaga sidumiseks, kuna see avaldis tagastab väärtuseks andmetüübi A, mis on väljaspool andmetüüpide ulatust, mida tüüp B praeguse vormindamise elemendina toetab.

Järgmised etapid näitavad, kuidas see probleem võib ilmneda.

1. Hakake konfigureerima ER-i andmemudeli ja ER-i vormingu komponente samaaegselt.
2. Lisage andmemudeli puus väli, mille nimi on **X**, ja valige andmetüübiks **Täisarv**.
3. Lisage vormingustruktuuri puus tüübi **Numbriline** vormingu element.
4. Pange uuele vormingu elemendile nimeks **Y**. Valige väljal **Numbriline tüüp** andmetüübiks **Täisarv**.
5. Siduge omavahel **X** ja **Y**.
6. Muutke vormingustruktuuri puus vormingu elemendi **Y** andmetüüp valikult **Täisarv** valikule **Int64**.
7. Valige nupp **Kontrolli**, et kontrollida redigeeritava vormindamise komponenti lehel **Vormingu kujundaja**.

    ![Vormingu kujundaja lehel tüübi ühilduvuse kontrollimine.](./media/er-components-inspections-02.gif)

8. Pange tähele, et kuvatakse valideerimise tõrge. Teade kinnitab, et konfigureeritud avaldis võib aktsepteerida ainult väärtusi **Int64**. Seega andmemudeli välja **X** väärtust tüübiga **Täisarv** ei saa sisestada vormingu elementi **Y**.

### <a name="automatic-resolution"></a>Automaatne lahendamine

Selle probleemi automaatseks lahendamiseks pole saadaval ühtegi valikut.

### <a name="manual-resolution"></a>Käsitsi lahendamine

#### <a name="option-1"></a>Suvand 1

Värskendage vormingu struktuuri, muutes vormingu elemendi **Numbriline** andmetüüpi nii, et see ühtiks avaldise andmetüübiga, millega see on konfigureeritud, et ühendada see element. Eelmise näite puhul tuleb vormingu elemendi **X** väärtus **Numbriline tüüp** muuta tagasi väärtusele **Täisarv**.

#### <a name="option-2"></a>Suvand 2

Värskendage vormingu elemendi **X** vormingu vastendamist, muutes avaldise valikult `model.X` valikule `INT64VALUE(model.X)`.

## <a name="missing-configuration-element"></a><a id="i3"></a>Puuduv konfiguratsiooni element

ER kontrollib, kas siduvad avaldised sisaldavad ainult andmeallikaid, mis on konfigureeritud redigeeritava ER-i komponendina. Iga sidumise korral, mis sisaldab redigeeritavast ER-i komponendist puuduvat andmeallikat, esineb valideerimise tõrge ER-i toimingute kujundajas või ER-i mudeli vastendamise kujundajas.

Järgmised etapid näitavad, kuidas see probleem võib ilmneda.

1. Hakake konfigureerima ER-i andmemudeli ja ER-i mudeli kaardistamise komponente samaaegselt.
2. Lisage andmemudeli puus väli, mille nimi on **X**, ja valige andmetüübiks **Täisarv**.

    ![Andmemudeli puu koos väljaga X ja täisarvulise andmetüübiga lehel Andmemudel.](./media/er-components-inspections-01.png)

3. Mudeli vastendamise disainis **andmeallikate** paanil lisage tüübi **Arvutatud väli** andmeallikas.
4. Pange uue andmeallika nimeks **Y** ja konfigureerige see nii, et see sisaldaks avaldist `INTVALUE(100)`.
5. Siduge omavahel **X** ja **Y**.
6. Kustutage mudeli vastendamise kujundajas **andmeallikate** paanil andmeallikas **Y**.
7. Valige nupp **Kontrolli**, et kontrollida redigeeritava mudeli vastendamise komponenti lehel **Mudeli vastendamise kujundaja**.

    ![Kontrollige redigeeritava ER-i mudeli vastendamise komponendi kinnitamist lehel mudeli vastendamise kujundaja.](./media/er-components-inspections-03.gif)

8. Pange tähele, et kuvatakse valideerimise tõrge. Teates on kirjas, et andmemudeli välja **X** sidumine sisaldab teed, mis viitab andmeallikale **Y**, kuid seda andmeallikat ei leitud.

### <a name="automatic-resolution"></a>Automaatne lahendamine

Valige suvand **Tühista sidumine**, et lahendada see probleem automaatselt, eemaldades puuduva andmeallika sidumise.

### <a name="manual-resolution"></a>Käsitsi lahendamine

#### <a name="option-1"></a>Suvand 1

Tühistage andmemudeli välja **X** sidumine, et lõpetada viitamine olematule andmeallikale **Y**.

#### <a name="option-2"></a>Suvand 2

ER-i mudeli vastendamise kujundaja **andmeallika** paanil lisage andmeallikas **Y** uuesti.

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a>Funktsiooniga FILTER avaldise täidetavus

Sisseehitatud ER-i funktsiooni [FILTER](er-functions-list-filter.md) kasutatakse rakenduse tabelitele, vaadetele või andmeüksustele juurdepääsuks, tehes ühe SQL-i kõne, et hankida nõutavad andmed kirjete loendina. Tüübi **Kirjete loend** andmeallikat kasutatakse selle funktsiooni avaldusena ja määratleb kõne jaoks rakenduse allika. ER kontrollib, kas võimalik on luua otsene SQL-päring andmeallikale, millele viidatakse funktsioonis `FILTER`. Kui otsest päringut ei saa luua, kuvatakse ER-i mudeli vastendamise kujundajas valideerimise tõrge. Teile kuvatavas teates on kirjas, et ER-i avaldist, mis sisaldav funktsiooni `FILTER` ei saa käitusajal käivitada.

Järgmised etapid näitavad, kuidas see probleem võib ilmneda.

1. Hakake konfigureerima ER-i mudeli vastendamise komponenti.
2. Lisage tüübi **Dynamics 365 for Operations \\ Tabeli kirjed** andmeallikas.
3. Pange uuele andmeallikale nimeks **Hankija**. Valige väljal **Tabel** suvand **VendTable**, et määratleda, et see andmeallikas taotleb tabelit VendTable.
4. Lisage tüübi **Arvutatud väli** andmeallikas.
5. Pange uue andmeallika nimeks **FilteredVendor** ja konfigureerige see nii, et see sisaldaks avaldist `FILTER(Vendor, Vendor.AccountNum="US-101")`.
6. Valige suvand **Kontrolli**, et kontrollida mudeli vastendamise kujundaja lehel **Mudeli vastendamise kujundaja** redigeeritud mudeli vastendamise komponenti ja kinnitada, et avaldisele `FILTER(Vendor, Vendor.AccountNum="US-101")` on võimalik andmeallikas **Hankija** saata päring.
7. Muutke andmeallikat **Hankija**, lisades tüübi **Arvutatud väli** pesastatud väli, et hankida kärbitud hankija konto number.
8. Pange uue pesastatud välja nimeks **$AccNumber** ja konfigureerige see nii, et see sisaldaks avaldist `TRIM(Vendor.AccountNum)`.
9. Valige suvand **Kontrolli**, et kontrollida mudeli vastendamise kujundaja lehel **Mudeli vastendamise kujundaja** redigeeritud mudeli vastendamise komponenti ja kinnitada, et avaldisele `FILTER(Vendor, Vendor.AccountNum="US-101")` on võimalik andmeallikas **Hankija** saata päring.

    ![Avaldise kontrollimise osas on võimalik saata päring mudeli vastendamise kujundaja lehel.](./media/er-components-inspections-04.gif)

10. Pange tähele, et ilmneb valideerimise tõrge, kuna andmeallikas **Hankija** sisaldab tüübi **Arvutatud väli** pesastatud välja, mis ei luba andmeallika **FilteredVendor** avaldist otse SQL-lauseks teisendada.

Järgmisel illustratsioonil on toodud käitusaja tõrge, mis ilmneb, kui te eirate hoiatust ja valite suvandi **Käivita**, et käitada vormingut, mis on konfigureeritud kasutama mudeli vastendamist.

![Käitusaja tõrked, mis ilmnevad, kui käivitate vormingu kujundaja lehel redigeeritava vormingu.](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a>Automaatne lahendamine

Selle probleemi automaatseks lahendamiseks pole saadaval ühtegi valikut.

### <a name="manual-resolution"></a>Käsitsi lahendamine

#### <a name="option-1"></a>Suvand 1

Tüübi **Arvutatud väli** pesastatud välja andmeallikale **Hankija** lisamise asemel lisage pesastatud väli **$AccNumber** andmeallikale **FilteredVendor** ja konfigureerige see nii, et sisaldaks avaldist `TRIM(FilteredVendor.AccountNum)`. Sel viisil saab avaldis `FILTER(Vendor, Vendor.AccountNum="US-101")` töötada SQL-tasemel ja arvutada pesastatud välja **$AccNumber** hiljem.

#### <a name="option-2"></a>Suvand 2

Muutke andmeallika **FilteredVendor** avaldis valikult `FILTER(Vendor, Vendor.AccountNum="US-101")` valikule `WHERE(Vendor, Vendor.AccountNum="US-101")`. Me ei soovita teil muuta tabeli avaldist, millel on suur hulk andmeid (ülekande tabel), sest tuuakse kõik kirjed ja nõutud kirjete valik toimub mälus. Seetõttu võib selline lähenemine põhjustada kehva jõudluse. Lisateavet vaadake teemast [Funktsioon WHERE ER](er-functions-list-where.md).

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a>Andmeallika GROUPBY täidetavus

Andmeallikas **GROUPBY** jaotab päringu tulemused kirjete gruppidesse, tavaliselt igas grupis ühe või mitme kogumi loomise eesmärgil. Iga andmeallika **GROUPBY** saab konfigureerida nii, et see käivitatakse kas andmebaasi tasemel või mälus. Kui andmeallikas **GROUPBY** on konfigureeritud nii, et see käivitatakse andmebaasi tasemel, kontrollib ER, kas on võimalik luua otsene SQL-päring andmeallikale, millele on selles andmeallikas viidatud. Kui otsest päringut ei saa luua, kuvatakse ER-i mudeli vastendamise kujundajas valideerimise tõrge. Teile saadetavas teated on toodud, et konfigureeritud andmeallikat **GROUPBY** ei saa käitusajal käivitada.

Järgmised etapid näitavad, kuidas see probleem võib ilmneda.

1. Hakake konfigureerima ER-i mudeli vastendamise komponenti.
2. Lisage tüübi **Dynamics 365 for Operations \\ Tabeli kirjed** andmeallikas.
3. Pange uuele andmeallikale nimi **Kanne**. Valige väljal **Tabel** suvand **VendTrans**, et täpsustada, et see andmeallikas esitab taotluse tabelile VendTrans.
4. Lisage tüübi **Rühmitamise alus** andmeallikas.
5. Pange uuele andmeallikale nimeks **GroupedTrans** ja konfigureerige see järgmisel viisil.

    - Valige rühmitamiseks kirjete allikaks andmeallikaks suvand **Kanne**.
    - Valige väljal **Täitmise asukoht** suvand **Päring**, et määrata, et soovite käitada seda andmeallikat andmebaasi tasemel.

    ![Andmeallika konfigureerimine lehel Rühmitamisaluse parameetrite redigeerimine.](./media/er-components-inspections-05a.gif)

6. Valige suvand **Kontrolli**, et kontrollida redigeeritava mudeli vastendamise komponenti lehel **Mudeli vastendamise kujundaja** ja kinnitada, et konfigureeritud andmeallika **GroupedTrans** saab päringusse kaasata.
7. Muutke andmeallikat **Kanne**, lisades tüübi **Arvutatud väli** pesastatud väli, et hankida kärbitud hankija konto number.
8. Pange uue andmeallika nimeks **$AccNumber** ja konfigureerige see nii, et see sisaldaks avaldist `TRIM(Trans.AccountNum)`.

    ![Andmeallikas konfigureerimine mudeli vastenduse koostaja lehel.](./media/er-components-inspections-05a.png)

9. Valige suvand **Kontrolli**, et kontrollida redigeeritava mudeli vastendamise komponenti lehel **Mudeli vastendamise kujundaja** ja kinnitada, et konfigureeritud andmeallika **GroupedTrans** saab päringusse kaasata.

    ![Kinnitage ER-i mudeli vastendamise komponent ja veenduge, et konfigureeritud andmeallika GroupedTrans saaks mudeli vastendamise kujundaja lehel päringusse kaasata.](./media/er-components-inspections-05b.png)

10. Pange tähele, et ilmneb valideerimise tõrge, kuna andmeallikas **Kanne** sisaldab tüübi **Arvutatud väli** pesastatud välja, mis ei luba andmeallika **GroupedTrans** kõnet otse SQL-lauseks teisendada.

Järgmisel illustratsioonil on toodud käitusaja tõrge, mis ilmneb, kui te eirate hoiatust ja valite suvandi **Käivita**, et käitada vormingut, mis on konfigureeritud kasutama mudeli vastendamist.

![Käitusaja tõrked, mis ilmnevad, kui te ignoreerite vormindamist kujundaja lehel.](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a>Automaatne lahendamine

Selle probleemi automaatseks lahendamiseks pole saadaval ühtegi valikut.

### <a name="manual-resolution"></a>Käsitsi lahendamine

#### <a name="option-1"></a>Suvand 1

Tüübi **Arvutatud väli** pesastatud välja andmeallikale **Kanne** lisamise asemel lisage pesastatud väli **$AccNumber** andmeallika **GroupedTrans** üksusele **GroupedTrans.lines** ja konfigureerige see nii, et sisaldaks avaldist `TRIM(GroupedTrans.lines.AccountNum)`. Sel viisil saab andmeallikas **GroupedTrans** töötada SQL-tasemel ja arvutada pesastatud välja **$AccNumber hiljem**.

#### <a name="option-2"></a>Suvand 2

Muutke välja **Täitmise asukoht** väärtust andmeallika **GroupedTrans** jaoks valikult **Päring** valikule **Mälus**. Me ei soovita teil muuta tabeli väärtust, millel on suur hulk andmeid (ülekande tabel), sest tuuakse kõik kirjed ning rühmitamine ja koondamine toimub mälus. Seetõttu võib selline lähenemine põhjustada kehva jõudluse.

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a>Andmeallika JOIN täidetavus

Andmeallikas [JOIN](er-join-data-sources.md) ühendab kahe või enama andmebaasi tabeli kirjed, mis põhinevad seotud väljadel. Iga andmeallika **JOIN** saab konfigureerida nii, et see käivitatakse kas andmebaasi tasemel või mälus. Kui andmeallikas **JOIN** on konfigureeritud nii, et see käivitatakse andmebaasi tasemel, kontrollib ER, kas on võimalik luua otsene SQL-päring andmeallikatele, millele on selles andmeallikas viidatud. Kui otsest SQL-päringut vähemalt ühe viite andmeallikaga ei saa luua, kuvatakse ER-i mudeli vastendamise kujundajas valideerimise tõrge. Teile saadetavas teated on toodud, et konfigureeritud andmeallikat **JOIN** ei saa käitusajal käivitada.

Järgmised etapid näitavad, kuidas see probleem võib ilmneda.

1. Hakake konfigureerima ER-i mudeli vastendamise komponenti.
2. Lisage tüübi **Dynamics 365 for Operations \\ Tabeli kirjed** andmeallikas.
3. Pange uuele andmeallikale nimeks **Hankija**. Valige väljal **Tabel** suvand **VendTable**, et määratleda, et see andmeallikas taotleb tabelit VendTable.
4. Lisage tüübi **Dynamics 365 for Operations \\ Tabeli kirjed** andmeallikas.
5. Pange uuele andmeallikale nimi **Kanne**. Valige väljal **Tabel** suvand **VendTrans**, et täpsustada, et see andmeallikas esitab taotluse tabelile VendTrans.
6. Lisage tüübi **Arvutatud väli** andmeallikas andmeallika **Hankija** pesastatud väljana.
7. Pange uue andmeallika nimeks **FilteredTrans** ja konfigureerige see nii, et see sisaldaks avaldist `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.
8. Lisage tüübi **Liitumine** andmeallikas.
9. Pange uuele andmeallikale nimeks **JoinedList** ja konfigureerige see järgmisel viisil.

    1. Lisage andmeallikas **Vendor** liitumiseks esimeste kirjete kogumina.
    2. Lisage andmeallikas **Vendor.FilteredTrans** liitumiseks teise kirjete kogumina. Valige tüübiks **INNER**.
    3. Valige väljal **Täitmine** suvand **Päring**, et määrata, et soovite käitada seda andmeallikat andmebaasi tasemel.

    ![Andmeallikas konfigureerimine Join koostaja lehel.](./media/er-components-inspections-06a.gif)

10. Valige suvand **Kontrolli**, et kontrollida redigeeritava mudeli vastendamise komponenti lehel **Mudeli vastendamise kujundaja** ja kinnitada, et konfigureeritud andmeallika **JoinedList** saab päringusse kaasata.
11. Muutke andmeallika **Vendor.FilteredTrans** avaldis valikult `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` valikule `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.
12. Valige suvand **Kontrolli**, et kontrollida redigeeritava mudeli vastendamise komponenti lehel **Mudeli vastendamise kujundaja** ja kinnitada, et konfigureeritud andmeallika **JoinedList** saab päringusse kaasata.

    ![Valige redigeeritava mudeli vastendamise komponent ja veenduge, et JoinedList andmeallika saab esitada päringu mudeli vastendamise kujundaja lehel.](./media/er-components-inspections-06b.png)

13. Pange tähele, et valideerimise tõrge ilmneb, kuna andmeallika **Vendor.FilteredTrans** väljendit ei saa otseseks SQL-i kõneks tõlkida. Lisaks ei luba otsene SQL-i kõne andmeallika **JoinedList** kõnet, mis teisendatakse otse SQL-i avaldiseks.

    ![Käitusaja tõrked JoinedList andmeallika nurjunud valideerimise tõttu mudeli vastendamise kujundaja lehel.](./media/er-components-inspections-06c.png)

Järgmisel illustratsioonil on toodud käitusaja tõrge, mis ilmneb, kui te eirate hoiatust ja valite suvandi **Käivita**, et käitada vormingut, mis on konfigureeritud kasutama mudeli vastendamist.

![Vormingu kujundaja lehel redigeeritava vormingu käitamine.](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a>Automaatne lahendamine

Selle probleemi automaatseks lahendamiseks pole saadaval ühtegi valikut.

### <a name="manual-resolution"></a>Käsitsi lahendamine

#### <a name="option-1"></a>Suvand 1

Muutke andmeallika **Vendor.FilteredTrans** avaldis suvandilt `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` tagasi väärtusele `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, nagu hoiatus soovitas.

![Andmeallika värskendatud avaldis mudeli vastenduse koostaja lehel.](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a>Suvand 2

Muutke välja **Täitmine** väärtust andmeallika **JoinedList** jaoks valikult **Päring** valikule **Mälus**. Me ei soovita teil muuta tabeli väärtust, millel on suur hulk andmeid (ülekande tabel), sest tuuakse kõik kirjed ning liitumine leiab aset mälus. Seetõttu võib selline lähenemine põhjustada kehva jõudluse. Kuvatakse kinnitamise hoiatus, mis teavitab teid sellest ohust.

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a>Funktsiooni FILTER vs WHERE eelistatavus

Sisseehitatud ER-i funktsiooni [FILTER](er-functions-list-filter.md) kasutatakse rakenduse tabelitele, vaadetele või andmeüksustele juurdepääsuks, tehes ühe SQL-i kõne, et hankida nõutavad andmed kirjete loendina. Funktsioon [WHERE](er-functions-list-where.md) toob kõik vastava allika kirjed ja valib kirjed mälus. Tüübi **Kirjete loend** andmeallikat kasutatakse mõlema funktsiooni avaldisena ja see määratleb kirjete hankimise allika. ER kontrollib, kas võimalik on luua otsene SQL-i kõne andmeallikale, millele viidatakse funktsioonis **WHERE**. Kui otsest kõnet ei saa luua, kuvatakse ER-i mudeli vastendamise kujundajas valideerimise hoiatus. Teile kuvatav teade soovitab teil kasutada tõhususe parandamiseks funktsiooni **WHERE** asemel funktsiooni **FILTER**.

Järgmised etapid näitavad, kuidas see probleem võib ilmneda.

1. Hakake konfigureerima ER-i mudeli vastendamise komponenti.
2. Lisage tüübi **Dynamics 365 for Operations \\ Tabeli kirjed** andmeallikas.
3. Pange uuele andmeallikale nimi **Kanne**. Valige väljal **Tabel** suvand **VendTrans**, et täpsustada, et see andmeallikas esitab taotluse tabelile VendTrans.
4. Lisage tüübi **Arvutatud väli** andmeallikas andmeallika **Hankija** pesastatud väljana.
5. Pange uue andmeallika nimeks **FilteredTrans** ja konfigureerige see nii, et see sisaldaks avaldist `WHERE(Trans, Trans.AccountNum="US-101")`.
6. Lisage tüübi **Dynamics 365 for Operations \\ Tabeli kirjed** andmeallikas.
7. Pange uuele andmeallikale nimeks **Hankija**. Valige väljal **Tabel** suvand **VendTable**, et määratleda, et see andmeallikas taotleb tabelit VendTable.
8. Lisage tüübi **Arvutatud väli** andmeallikas.
9. Pange uue andmeallika nimeks **FilteredVendor** ja konfigureerige see nii, et see sisaldaks avaldist `WHERE(Vendor, Vendor.AccountNum="US-101")`.
10. Valige nupp **Kontrolli**, et kontrollida redigeeritava mudeli vastendamise komponenti lehel **Mudeli vastendamise kujundaja**.

    ![Kontrollige redigeeritava ER-i mudeli vastendamise komponendi kinnitamist mudeli vastendamise kujundaja lehel.](./media/er-components-inspections-07a.png)

11. Pange tähele, et kinnitamise hoiatused soovitavad kasutada funktsiooni **WHERE** asemel funktsiooni **Filter** andmeallikates **FilteredVendor** ja **FilteredTrans**.

    ![Kinnitamise hoiatused, mis soovitavad kasutada mudeli vastendamise kujunduse lehel funktsiooni, kus asemel filtri funktsiooni.](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a>Automaatne lahendamine

Valige suvand **Parandus**, et automaatselt asendada funktsioon **WHERE** funktsiooniga **FILTER** kõikides andmeallikate avaldistes, mis seda tüüpi läbivaatuse vahekaardil **Hoiatused** ruudustikus kuvatakse.

Teise võimalusena saate valida ruudustikus üksiku rea hoiatuse ja valida seejärel suvandi **Paranda valitud**. Sel juhul muudetakse avaldis automaatselt ainult valitud hoiatuses mainitud andmeallikas.

![Valige Paranda, et asendada mudeli vastendamise Where funktsioon kujunduse lehel funktsiooniga Filter.](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a>Käsitsi lahendamine

Saate käsitsi korrigeerida kõigi andmeallikate avaldisi kinnitamise ruudustikus, asendades funktsiooni **WHERE** funktsiooniga **FILTER**.

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a>Funktsiooni ALLITEMSQUERY vs ALLITEMS eelistatavus

Sisseehitatud ER-i funktsioonid [ALLITEMS](er-functions-list-allitems.md) ja [ALLITEMSQUERY](er-functions-list-allitemsquery.md) tagastavad tasandatud väärtuse **Kirje loend** hankimiseks, mis koosneb kirjete loendist, mis esindavad kõiki määratud teega ühtivaid üksusi. ER kontrollib, kas võimalik on luua otsene SQL-i kõne andmeallikale, millele viidatakse funktsioonis **ALLITEMS**. Kui otsest kõnet ei saa luua, kuvatakse ER-i mudeli vastendamise kujundajas valideerimise hoiatus. Teile kuvatav teade soovitab teil kasutada tõhususe parandamiseks funktsiooni **ALLITEMS** asemel funktsiooni **ALLITEMSQUERY**.

Järgmised etapid näitavad, kuidas see probleem võib ilmneda.

1. Hakake konfigureerima ER-i mudeli vastendamise komponenti.
2. Lisage tüübi **Dynamics 365 for Operations \\ Tabeli kirjed** andmeallikas.
3. Pange uuele andmeallikale nimeks **Hankija**. Valige väljal **Tabel** suvand **VendTable**, et määratleda, et see andmeallikas taotleb tabelit VendTable.
4. Lisage tüübi **Arvutatud väli** andmeallikas, et hankida mitme hankija kirjed.
5. Pange uue andmeallika nimeks **FilteredVendor** ja konfigureerige see nii, et see sisaldaks avaldist `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.
6. Lisage tüübi **Arvutatud väli** andmeallikas, et hankida kõikide filtreeritud hankijate kanded.
7. Pange uue andmeallika nimeks **FilteredVendorTrans** ja konfigureerige see nii, et see sisaldaks avaldist `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.
8. Valige nupp **Kontrolli**, et kontrollida redigeeritava mudeli vastendamise komponenti lehel **Mudeli vastendamise kujundaja**.

    ![Kontrollige redigeeritava ER-i mudeli vastendamise komponendi kinnitamist lehel mudeli vastendamise kujundaja.](./media/er-components-inspections-08a.png)

9. Pange tähele, et kuvatakse valideerimise hoiatus. Sõnum soovitab kasutada funktsiooni **ALLITEMS** asemel funktsiooni **ALLITEMSQUERY** andmeallika **FilteredVendorTrans** jaoks.

    ![Soovitus kasutada mudeli kaardistamise kujundaja lehel funktsiooni ALLITEMSQUERY asemel funktsiooni ALLITEMSQUERY.](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a>Automaatne lahendamine

Valige suvand **Parandus**, et automaatselt asendada funktsioon **ALLITEMS** funktsiooniga **ALLITEMSQUERY** kõikides andmeallikate avaldistes, mis seda tüüpi läbivaatuse vahekaardil **Hoiatused** ruudustikus kuvatakse.

Teise võimalusena saate valida ruudustikus üksiku rea hoiatuse ja valida seejärel suvandi **Paranda valitud**. Sel juhul muudetakse avaldis automaatselt ainult valitud hoiatuses mainitud andmeallikas.

![Valides paranda mudeli vastendamise kujundaja lehel.](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a>Käsitsi lahendamine

Saate käsitsi korrigeerida kõigi andmeallikate avaldisi, mis on märgitud kinnitamise ruudustikus, asendades funktsiooni **ALLITEMS** funktsiooniga **ALLITEMSQUERY**.

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a>Tühja loendiga juhtumite arvesse võtmine

Saate konfigureerida oma ER-i vormingu või mudeli vastendades komponendi, et hankida tüübi **Kirje loend** andmeallika välja väärtus. ER kontrollib, kas teie disainilahendus leiab, et kutsutud andmeallikas ei sisalda kirjeid (st see on tühi), et vältida käitusaja tõrkeid, kui väärtus tuuakse olematu kirje väljalt.

Järgmised etapid näitavad, kuidas see probleem võib ilmneda.

1. Hakake konfigureerima ER-i andmemudeli, ER-i mudeli vastendamise ja ER-i vormingu komponente samaaegselt.
2. Lisage andmemudeli puus juurüksus nimega **Root3**.
3. Muutke üksust **Root3**, lisades tüübi **Kirje loend** pesastatud üksuse.
4. Pange uuele pesastatud üksusele nimeks **Hankija**.
5. Muutke üksust **Hankija** järgmisel viisil.

    - Lisage tüübi **String** pesastatud väli ja pange sellele nimeks **Name**.
    - Lisage tüübi **String** pesastatud väli ja pange sellele nimeks **AccountNumber**.

    ![Pesastatud väljade lisamine andmemudeli lehele.](./media/er-components-inspections-09a.png)

6. Mudeli vastendamise disainis paanil **Andmeallikas** lisage **Dynamics 365 for Operations andmeallikas \\ Tabeli andmed** tüüp.
7. Pange uuele andmeallikale nimeks **Hankija**. Valige väljal **Tabel** suvand **VendTable**, et määratleda, et see andmeallikas taotleb tabelit VendTable.
8. Lisage tüübi **Üldine \\ Kasutaja sisendi parameeter** andmeallikas, et otsida hankija kontot dialoogiboksis käitusaeg.
9. Pange uuele andmeallikale nimeks **RequestedAccountNum**. Sisestage väljal **Silt** suvand **Hankija kontonumber**. Jätke väljale **Toimingute andmetüübi nimi** vaikeväärtus **Kirjeldus**.
10. Lisage tüübi **Arvutatud väli** andmeallikas, et filtreerida välja hankija, kelle kohta päring esitati.
11. Pange uue andmeallika nimeks **FilteredVendor** ja konfigureerige see nii, et see sisaldaks avaldist `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Siduge andmemudeli üksused konfigureeritud andmeallikatega järgmisel viisil.

    - Siduge **FilteredVendor** atribuudiga **Vendor**.
    - Siduge **FilteredVendor.AccountNum** atribuudiga **Vendor.AccountNumber**.
    - Siduge **FilteredVendor.'name()'** atribuudiga **Vendor.Name**.

    ![Andmemudeli üksuste sidumine mudeli vastenduse koostaja lehel.](./media/er-components-inspections-09b.png)

13. Lisage vormingu struktuuri puul järgmised üksused, et luua väljuv dokument XML-vormingus, mis sisaldab hankija üksikasju.

    1. Lisage juure **Avaldis** XML-element.
    2. XML-elemendi **Avaldis** jaoks lisage pesastatud XML-element **Osapool**.
    3. Lisage XML-elemendile **Osapool** järgmised pesastatud XML-i atribuudid.

        - Nimi
        - AccountNum

14. Siduge vormingu elemendid, et esitada andmeallikad järgmisel viisil.

    - Siduge vormingu element **Avaldis\\Osapool\\Nimi** andmeallika väljaga **model.Vendor.Name**.
    - Siduge vormingu element **Avaldis\\Osapool\\AccountNum** andmeallika väljaga **model.Vendor.AccountNumber**.

15. Valige nupp **Kontrolli**, et kontrollida redigeeritava vormindamise komponenti lehel **Vormingu kujundaja**.

    ![Vormingu elementide kinnitamine, mis on vormingu kujundaja lehel seotud andmeallikatega.](./media/er-components-inspections-09c.png)

16. Pange tähele, et kuvatakse valideerimise tõrge. Sõnumis on kirjas, et konfigureeritud vormingu komponentidele **Avaldis\\Osapool\\Nimi** ja **Avaldis\\Osapool\\AccountNum** võidakse käitusajal kuvada tõrge, kui loend `model.Vendor` on tühi.

    ![Kinnitamise tõrge, mis teavitab konfigureeritud vormingu komponentide võimalikust tõrkest.](./media/er-components-inspections-09d.png)

Järgmisel illustratsioonil on toodud käitusaja tõrge, mis ilmneb, kui te eirate hoiatust, valite suvandi **Käivita**, et käitada vormingut, ja valite olematu hankija kontonumbri. Kuna taotletud hankijat pole, siis on loend `model.Vendor` tühi (st see ei sisalda kirjeid).

![Käitusaja tõrked, mis ilmnesid vormingu vastendamise ajal.](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a>Automaatne lahendamine

Saate vahekaardil **Hoiatused** ruudustiku valitud real valida suvandi **Tühista sidumine**. Seos, millele viidatakse veerus **Tee**, eemaldatakse vormingu elementidelt automaatselt.

### <a name="manual-resolution"></a>Käsitsi lahendamine

#### <a name="option-1"></a>Suvand 1

Saate siduda vormingu elemendi **Avaldis\\Osapool\\Nimi** andmeallika üksusega `model.Vendor`. Käitusaja korral nõuab see sidumine esmalt andmeallikat `model.Vendor`. Kui `model.Vendor` tagastab tühja kirje loendi, pesastatud vormingu elemendid ei tööta. Seega selle vormingu konfiguratsiooni puhul kinnituse hoiatusi ei esine.

![Siduge vormingu element vormingu kujundaja lehel üksuse andmeallikaga.](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a>Suvand 2

Muutke vormingu elemendi **Avaldis\\Osapool\\Nimi** sidumine valikult `model.Vendor.Name` valikule `FIRSTORNULL(model.Vendor).Name`. Uuendatud sidumine teisendab tingimuslikult andmeallika `model.Vendor` esimese kirje tüübis **Kirje loend** uuele tüübi **Kirje** andmeallikale. See uus andmeallikas sisaldab sama väljade kogumit.

- Kui andmeallikas `model.Vendor` on saadaval vähemalt üks kirje, on selle kirje väljad täidetud andmeallika `model.Vendor` mudeli esimese kirje väljade väärtustega. Sel juhul tagastab uuendatud sidumine hankija nime.
- Vastasel juhul täidetakse iga looda kirje väli selle välja andmetüübi vaikeväärtusega. Sellisel juhul tagastatakse andmetüübi **String** vaikeväärtusena tühi string.

Seetõttu ei esine kinnitamise hoiatusi vormingu elemendis **Avaldis\\Osapool\\Nimi**, kui see on seotud avaldisega `FIRSTORNULL(model.Vendor).Name`.

![Muudetud sidumine lahendab kinnitamise hoiatused lehel Vormingu kujundaja.](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a>Suvand 3

Kui soovite luua selgesõnaliselt andmed, mis sisestatakse loodud dokumenti, kui andmeallikas `model.Vendor` tüübis **Kirje loend** ei tagasta ühtegi kirjet (selles näites tekst **Pole saadaval**), muutke vormingu elemendi **Avaldis\\Osapool\\Nimi** sidumine valikult `model.Vendor.Name` valikule `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`. Samuti võite kasutada avaldist `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.

### <a name="additional-consideration"></a><a id="i9a"></a>Täiendav arvestamine

Kontroll hoiatab teid ka teise võimaliku probleemi eest. Kui te vaikimisi seote vormingu elemendid **Avaldis\\Osapool\\Nimi** ja **Avaldis\\Osapool\\AccountNum** vastavate väljadega andmeallikas `model.Vendor` tüübis **Kirje loend**, need seosed käitatakse ja need hangivad väärtused andmeallika `model.Vendor` esimese kirje vastavate väljade väärtustelt, kui see loend ei ole tühi.

Kuna te pole sidunud vormingu elementi **Avaldis\\Osapool** andmeallikaga `model.Vendor`, siis elementi **Avaldis\\Osapool** ei saa andmeallikat `model.Vendor` vormindamise teostamise ajal iga kirje jaoks itereerida. Selle asemel täidetakse loodud dokument teabega kirjete loendi esimese kirjega, kui see loend sisaldab mitut kirjet. Seetõttu võib tekkida probleem, kui vorming on mõeldud täitma loodud dokumendi koos teabega kõigi hankijate kohta andmeallikast `model.Vendor`. Probleemi lahendamiseks siduge element **Avaldis\\Osapool** andmeallikaga `model.Vendor`.

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a>Funktsiooniga FILTER avaldise täidetavus (vahemällu salvestamine)

Mitu sisseehitatud ER-i funktsiooni, sh [FILTER](er-functions-list-filter.md) ja [ALLITEMSQUERY](er-functions-list-allitemsquery.md) kasutatakse rakenduse tabelitele, vaadetele või andmeüksustele juurdepääsuks, tehes ühe SQL-i kõne, et hankida nõutavad andmed kirjete loendina. Tüübi **Kirjete loend** andmeallikat kasutatakse iga sellise funktsiooni avaldusena ja määratleb kõne jaoks rakenduse allika. ER kontrollib, kas võimalik on luua otsene SQL-i kõne andmeallikale, millele ühes nendest funktsioonidest viidatakse. Kui otsest kõnet ei saa luua, kuna andmeallikas märgiti kui [vahemällu salvestatud](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), ilmub ER-i mudeli vastendamise kujundajas valideerimise tõrge. Teile kuvatavas teates on kirjas, et ER-i avaldist, mis sisaldab ühte nendest funktsioonidest, ei saa käitusajal käivitada.

Järgmised etapid näitavad, kuidas see probleem võib ilmneda.

1. Hakake konfigureerima ER-i mudeli vastendamise komponenti.
2. Lisage tüübi **Dynamics 365 for Operations \\ Tabeli kirjed** andmeallikas.
3. Pange uuele andmeallikale nimeks **Hankija**. Valige väljal **Tabel** suvand **VendTable**, et määratleda, et see andmeallikas taotleb tabelit VendTable.
4. Lisage tüübi **Üldine \\ Kasutaja sisendi parameeter** andmeallikas, et otsida hankija kontot dialoogiboksis käitusaeg.
5. Pange uuele andmeallikale nimeks **RequestedAccountNum**. Sisestage väljal **Silt** suvand **Hankija kontonumber**. Jätke väljale **Toimingute andmetüübi nimi** vaikeväärtus **Kirjeldus**.
6. Lisage tüübi **Arvutatud väli** andmeallikas, et filtreerida välja hankija, kelle kohta päring esitati.
7. Pange uue andmeallika nimeks **FilteredVendor** ja konfigureerige see nii, et see sisaldaks avaldist `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
8. Märkige konfigureeritud andmeallikas **Hankija** vahemällu talletatuks.

    ![Mudeli vastendamise komponendi konfigureerimine Mudeli vastendamise kujundaja lehel.](./media/er-components-inspections-10a.gif)

9. Valige nupp **Kontrolli**, et kontrollida redigeeritava mudeli vastendamise komponenti lehel **Mudeli vastendamise kujundaja**.

    ![Mudeli vastendamise vahemällu salvestatud hankijale rakendatud filtri funktsiooni kinnitamine kujundaja lehel.](./media/er-components-inspections-10a.png)

10. Pange tähele, et kuvatakse valideerimise tõrge. Teade ütleb, et funktsiooni **FILTER** ei saa rakendada vahemällu salvestatud andmeallikale **Hankija** rakendada.

Järgmisel illustratsioonil on toodud käitusaja tõrge, mis ilmneb, kui te eirate hoiatust ja valite suvandi **Käivita**, et käitada vormingut.

![Käitusaja tõrge, mis ilmnes vormingu vastendamise käitamise ajal kujundaja lehel.](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution&quot;></a>Automaatne lahendamine

Selle probleemi automaatseks lahendamiseks pole saadaval ühtegi valikut.

### <a name=&quot;manual-resolution&quot;></a>Käsitsi lahendamine

#### <a name=&quot;option-1&quot;></a>Suvand 1

Eemaldage lipp **Vahemälu** andmeallikalt **Hankija**. Andmeallikas **FilteredVendor** muutub siis käivitatavaks, kuid andmeallikas **Hankija**, millele viidatakse tabelis VendTable, pääsetakse ligi iga kord, kui andmeallikas **FilteredVendor** kutsutakse.

#### <a name=&quot;option-2&quot;></a>Suvand 2

Muutke andmeallika **FilteredVendor** avaldis valikult `FILTER(Vendor, Vendor.AccountNum=&quot;US-101")` valikule `WHERE(Vendor, Vendor.AccountNum="US-101")`. Sellisel juhul andmeallikas **Hankija**, millele viidatakse tabelis VendTable, pääseb ligi ainult andmeallika **Hankija** esmakordse kutsumise ajal. Samas kirjete valimine tehakse mälus. Seetõttu võib selline lähenemine põhjustada kehva jõudluse.

## <a name="missing-binding"></a><a id="i11"></a>Puuduv sidumine

Kui konfigureerite ER-vormingu komponendi, pakutakse peamist ER-i andmemudelit ER-vormingus vaikimisi andmeallikana. Kui konfigureeritud ER-i vorming on käivitatud, kasutatakse andmemudeli rakenduse andmetega täitmiseks [vaikimisi mudeli vastendamist](er-country-dependent-model-mapping.md). ER-i vorming kujundaja kuvab hoiatuse, kui seote vormingu elemendi andmemudeli üksusega, mis ei ole seotud ühegi andmeallikaga mudeli vastendamisel, mis on praegu valitud vorminguga vaikimisi mudeli vastendamine. Seda tüüpi sidumist ei saa käitusaja ajal käitada, sest käivituv vorming ei saa täita seotud elementi rakenduse andmetega. Seetõttu ilmneb käitamise ajal tõrge.

Järgmised etapid näitavad, kuidas see probleem võib ilmneda.

1. Hakake konfigureerima ER-i andmemudeli, ER-i mudeli vastendamise ja ER-i vormingu komponente samaaegselt.
2. Lisage andmemudeli puus juurüksus nimega **Root3**.
3. Muutke üksust **Root3**, lisades tüübi **Kirje loend** uue pesastatud üksuse.
4. Pange uuele pesastatud üksusele nimeks **Hankija**.
5. Muutke üksust **Hankija** järgmisel viisil.

    - Lisage tüübi **String** pesastatud väli ja pange sellele nimeks **Name**.
    - Lisage tüübi **String** pesastatud väli ja pange sellele nimeks **AccountNumber**.

    ![Hankija üksusele andmemudeli lehel pesastatud väljade lisamine.](./media/er-components-inspections-11a.png)

6. Mudeli vastendamise disainis paanil **Andmeallikas** lisage **Dynamics 365 for Operations andmeallikas \\ Tabeli andmed** tüüp.
7. Pange uuele andmeallikale nimeks **Hankija**. Valige väljal **Tabel** suvand **VendTable**, et määratleda, et see andmeallikas taotleb tabelit VendTable.
8. Lisage tüübi **Üldine \\ Kasutaja sisendi parameeter** andmeallikas, et teha päring hankija konto dialoogiboksis käitusaja kohta.
9. Pange uuele andmeallikale nimeks **RequestedAccountNum**. Sisestage väljal **Silt** suvand **Hankija kontonumber**. Jätke väljale **Toimingute andmetüübi nimi** vaikeväärtus **Kirjeldus**.
10. Lisage tüübi **Arvutatud väli** andmeallikas, et filtreerida välja hankija, kelle kohta päring esitati.
11. Pange uue andmeallika nimeks **FilteredVendor** ja konfigureerige see nii, et see sisaldaks avaldist `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Siduge andmemudeli üksused konfigureeritud andmeallikatega järgmisel viisil.

    - Siduge **FilteredVendor** atribuudiga **Vendor**.
    - Siduge **FilteredVendor.AccountNum** atribuudiga **Vendor.AccountNumber**.

    > [!NOTE]
    > Andmemudeli väli **Vendor.Name** jääb sidumata.

    ![Andmemudeli üksused, mis on seotud konfigureeritud andmeallikatega ja andmerežiimi üksusega, mis on mudeli vastendamise kujundaja lehel sidumata.](./media/er-components-inspections-11b.png)

13. Lisage vormingu struktuuri puul järgmised üksused, et luua väljuv dokument XML-vormingus, mis sisaldab hankija üksikasju, kelle kohta päringu esitasite.

    1. Lisage juure **Avaldis** XML-element.
    2. XML-elemendi **Avaldis** jaoks lisage pesastatud XML-element **Osapool**.
    3. Lisage XML-elemendile **Osapool** järgmised pesastatud XML-i atribuudid.

        - Nimi
        - AccountNum

14. Siduge vormingu elemendid, et esitada andmeallikad järgmisel viisil.

    - Siduge vormingu elemendi **Avaldis\\Osapool** andmeallika üksusega `model.Vendor`.
    - Siduge vormingu element **Avaldis\\Osapool\\Nimi** andmeallika väljaga **model.Vendor.Name**.
    - Siduge vormingu element **Avaldis\\Osapool\\AccountNum** andmeallika väljaga **model.Vendor.AccountNumber**.

15. Valige nupp **Kontrolli**, et kontrollida redigeeritava vormindamise komponenti lehel **Vormingu kujundaja**.

    ![ER-i vormingu komponendi kinnitamine kujundaja vormingu lehel.](./media/er-components-inspections-11c.png)

16. Pange tähele, et kuvatakse valideerimise hoiatus. Sõnum ütleb, et andmeallika väli **model.Vendor.Name** ei ole mudeli vastendamisel seotud ühegi andmeallikaga, mis on konfigureeritud vormingu poolt kasutamiseks. Seega ei pruugi vormingu element **Avaldis\\Osapool\\Nimi** olla käitusajal täidetud ja esineda võib käitusaja erand.

    ![ER-i vormingu komponendi kinnitamine vormingu kujundaja lehel.](./media/er-components-inspections-11d.png)

Järgmisel illustratsioonil on toodud käitusaja tõrge, mis ilmneb, kui te eirate hoiatust ja valite suvandi **Käivita**, et käitada vormingut.

![Vormingu kujundaja lehel redigeeritava vormingu käitamine.](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a>Automaatne lahendamine

Selle probleemi automaatseks lahendamiseks pole saadaval ühtegi valikut.

### <a name="manual-resolution"></a>Käsitsi lahendamine

#### <a name="option-1"></a>Suvand 1

Muutke konfigureeritud mudeli vastendust, lisades andmeallika välja **model.Vendor.Name** jaoks sidumise.

#### <a name="option-2"></a>Suvand 2

Muutke konfigureeritud vormingut, eemaldades vormingu elemendi **Avaldis\\Osapool\\Nimi** sidumine.

## <a name="not-linked-template"></a><a id="i12"></a>Linkimata mall

Kui konfigureerite ER-i vormingu komponendi [käsitsi](er-fillable-excel.md#manual-entry), et kasutada väljuva dokumendi loomiseks malli, peate lisama elemendi **Excel\\Fail**, lisama nõutavad mallid redigeeritava komponendi manusena ja valima selle manuse lisatud elemendis **Excel\\Fail**. Sel viisil saate näidata, et lisatud element täidab valitud malli käitusajal. Kui konfigureerite vormingu komponendi versiooni **Mustandi** [olekus](general-electronic-reporting.md#component-versioning), võite lisada redigeeritavale komponendile mitu malli ja seejärel valida iga malli elemendis **Excel\\Fail**, element käitada ER-i vormingusse. Sel viisil saate vaadata, kuidas erinevad mallid on käitusajal täidetud. Kui teil on malle, mis ei ole üheski elemendis **Excel\\Fail** valitud, hoiatab ER-i vormingu kujundaja teid, et need mallid kustutatakse redigeeritavate ER-i vormingu komponentide versioonist, kui selle olek muudetakse valikult **Mustand** valikule **Lõpetatud**.

Järgmised etapid näitavad, kuidas see probleem võib ilmneda.

1. Hakake konfigureerima ER-i vormingu komponenti.
2. Lisage vormi struktuuri puus element **Excel\\Fail**.
3. Äsja lisatud elemendi **Excel\\Fail** jaoks lisage Exceli tööraamatu fail **A.xlsx** manusena. Kasutage dokumendi tüüpi, mis on konfigureeritud [ER-i parameetrites](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents), et määrata ER-i vormingu mallide talletamine.
4. Lisage elemendi **Excel\\Fail** jaoks täiendav Exceli tööraamatu fail **B.xlsx** manusena. Kasutage sama dokumendi tüüpi, mida kasutatakse töölehe failil A.
5. Valige elemendis **Excel\\Fail** töölehe fail A.
6. Valige nupp **Kontrolli**, et kontrollida redigeeritava vormindamise komponenti lehel **Vormingu kujundaja**.

    ![Töölehe faili redigeeritavas vormingus komponentide valideerimine vormingu kujundaja lehel.](./media/er-components-inspections-12a.gif)

7. Pange tähele, et kuvatakse valideerimise hoiatus. Sõnum ütleb, et töölehe fail B.xlsx ei ole ühegi komponendiga lingitud ja see eemaldatakse pärast konfiguratsiooni versiooni oleku muutmist.

### <a name="automatic-resolution"></a>Automaatne lahendamine

Selle probleemi automaatseks lahendamiseks pole saadaval ühtegi valikut.

### <a name="manual-resolution"></a>Käsitsi lahendamine

Konfigureeritud vormingu muutmine, eemaldades kõik mallid, mis ei ole ühegi elemendiga **Excel\\Fail** lingitud.

## <a name="not-synced-format"></a><a id="i13"></a>Sünkroonimata vorming

Kui [konfigureerite](er-fillable-excel.md) ER-i vormingu komponendi, et kasutada väljuva dokumendi loomiseks Exceli malli, saate lisada elemendi **Excel\\Fail**, lisada nõutavad mallid redigeeritava komponendi manusena ja valida selle manuse lisatud elemendis **Excel\\Fail**. Sel viisil saate näidata, et lisatud element täidab valitud malli käitusajal. Kuna lisatud Exceli mall on väliselt konstrueeritud, võib redigeeritav ER-i vorming sisaldada lisatud mallist puuduvaid Exceli nimesid. ER-i vormingu kujundaja hoiatab teid mis tahes vastuolude suhtes ER-i vormingu elementide atribuutide vahel, mis viitavad nimele, mis ei sisaldu lisatud Exceli mallis.

Järgmised etapid näitavad, kuidas see probleem võib ilmneda.

1. Hakake konfigureerima ER-i vormingu komponenti.
2. Lisage vormi struktuuri puus **Excel\\Fail** element **Aruanne**.
3. Äsja lisatud elemendi **Excel\\Fail** jaoks lisage Exceli tööraamatu fail **A.xlsx** manusena. Kasutage dokumendi tüüpi, mis on konfigureeritud [ER-i parameetrites](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents), et määrata ER-i vormingu mallide talletamine.

    > [!IMPORTANT]
    > Veenduge, et lisatud Exceli töövihik ei sisaldaks nime **ReportTitle**.

4. Lisage järgmine **Exceli\\lahtri** elemendi **pealkiri** elemendi **Aruanne** pesastatud elemendina. Sisestage väljal **Exceli vahemik** suvand **ReportTitle**.
5. Valige nupp **Kontrolli**, et kontrollida redigeeritava vormindamise komponenti lehel **Vormingu kujundaja**.

    ![Pesastatud elementide ja väljade kinitamine vormingu kujundaja lehel.](./media/er-components-inspections-13a.png)

6. Pange tähele, et kuvatakse valideerimise hoiatus. Sõnum ütleb, et nime **ReportTitle** ei ole teie asutataval Exceli mallil lehel **Leht1** olemas.

    ![Kinnitamise hoiatus, et nime ReportTitle ei ole Exceli malli vahekaardil Leht1 olemas.](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a>Automaatne lahendamine

Selle probleemi automaatseks lahendamiseks pole saadaval ühtegi valikut.

### <a name="manual-resolution"></a>Käsitsi lahendamine

#### <a name="option-1"></a>Suvand 1

Muutke konfigureeritud vormingut, eemaldades kõik elemendid, mis viitavad mallist puuduvatele Exceli nimedele.

#### <a name="option-2"></a>Suvand 2

[Värskendage](er-fillable-excel.md#template-import) redigeeritavat ER-i vormingut, importides Exceli malli. Redigeeritava ER-i vormingu struktuur [sünkroonitakse](modify-electronic-reporting-format-reapply-excel-template.md) imporditud Exceli malli struktuuriga.

### <a name="additional-consideration"></a>Täiendav arvestamine

Lisateavet selle kohta, kuidas vormingu struktuuri saab ER-i malliga [äridokumentide haldamise](er-business-document-management.md) malli redaktoris sünkroonida, vt teemast [Äridokumendimalli struktuuri värskendamine](er-bdm-update-structure.md).

## <a name="not-synced-with-a-word-template-format"></a><a id="i14"></a>Pole Wordi mallivorminguga sünkroonitud

Kui [konfigureerite](er-fillable-excel.md) ER-i vormingu komponendi, et kasutada väljuva dokumendi loomiseks Exceli malli, saate lisada elemendi **Excel\\Fail**, lisada nõutavad mallid redigeeritava komponendi manusena ja valida selle manuse lisatud elemendis **Excel\\Fail**.

> [!NOTE]
> Kui Wordi dokument on lisatud, esitab ER-vormingu kujundaja redigeeritava elemendi **Word\\failina**.

Sel viisil saate näidata, et lisatud element täidab valitud malli käitusajal. Kuna lisatud Exceli mall on väliselt konstrueeritud, võib redigeeritav ER-i vorming sisaldada lisatud mallist puuduvaid Exceli nimesid. ER-i vormingu kujundaja hoiatab teid mis tahes vastuolude suhtes ER-i vormingu elementide atribuutide vahel, mis viitavad nimele, mis ei sisaldu lisatud Exceli mallis.

Näiteid, mis näitavad, kuidas see probleem võib ilmneda, vaadake jaotisest [Konfigureeri redigeeritav vorming kokkuvõttejao vastu kindlustamiseks](er-design-configuration-word-suppress-controls.md#configure-to-suppress-control).

### <a name="automatic-resolution"></a>Automaatne lahendamine

Selle probleemi automaatseks lahendamiseks pole saadaval ühtegi valikut.

### <a name="manual-resolution"></a>Käsitsi lahendamine

#### <a name="option-1"></a>Suvand 1

Muutke konfigureeritud vormingut, kustutades **Eemaldatud** valemi kinnitushoiatuses mainitud vorminguelemendist.

#### <a name="option-2"></a>Suvand 2

Muutke Wordi malli [lisades](er-design-configuration-word-suppress-controls.md#tag-control) nõutava sildi vastavale Wordi sisu juhtelemendile.

## <a name="no-default-mapping"></a><a id="i15"></a>Vaikevastendus puudub

Kui tehakse [puuduva sidumise](#i11) kontroll, hinnatakse kontrollitud vormingu sidumisi vastava mudeli vastenduskomponendi sidumiste suhtes. Kuna saate importida [mitu](./tasks/er-manage-model-mapping-configurations-july-2017.md) ER-mudeli vastendamise konfiguratsiooni oma finantseksemplari ja iga konfiguratsioon võib sisaldada rakendatavat mudelivastenduse komponenti, peab vaikekonfiguratsiooniks olema valitud üks konfiguratsioon. Vastasel juhul, kui proovite kontrollitud ER-vormingut käitada, redigeerida või kontrollida, ilmneb erand ja saate järgmise teate: "Konfiguratsioonides on andmemudeli kohta olemas rohkem kui üks \<model name (root descriptor)\> mudelivastendus \<configuration names separated by comma\>. Määrake üks konfiguratsioonides vaikeväärtuseks."

Näiteid, mis näitavad, kuidas see probleem võib ilmneda ja kuidas seda saab parandada, vt [Mitme mudeli juure kohta teemast tuletatud vastenduse haldamine](er-multiple-model-mappings.md).

## <a name="inconsistent-setting-of-header-or-footer-components"></a><a id="i16"></a>Päise või jaluse komponentide ebaühtlane seadistus

Kui [konfigureerite](er-fillable-excel.md) ER-i vormingu komponenti kasutama Exceli malli väljamineva dokumendi loomiseks, saate lisada **Exceli\\päise** komponendi, et täita päised töölehe ülaosas Excelitöövihikus. Samuti saate lisada **Exceli\\jaluse** komponendi töölehe allserva jalusesse täitmiseks. Iga **Exceli\\Päise** või **Exceli\\jaluse** komponendi jaoks, mille lisate, peate seadistama **päise/jaluse** välimuse atribuudi, et määrata leheküljed, mille jaoks komponenti käitatakse. Kuna saate konfigureerida **Exceli\\päise** või **Exceli\\jaluse** komponenti ühe **Lehe** komponendi jaoks ja saate exceli töölehel luua erinevaid päiseid või jaluseid eri tüüpi lehtedele, peate konfigureerima **Exceli\\päise** või **Exceli\\jaluse** komponendi konkreetse **päise/jaluse välimuse** atribuudile. Kui **Exceli\\päise** või **Exceli\\jaluse** välimuse atribuudi konkreetse väärtuse jaoks on konfigureeritud rohkem kui üks **päise/jalus välimuse** atribuut, ilmneb kinnitamistõrge ja kuvatakse järgmine tõrketeade: "Päised/jalused (&lt;komponendi tüüp: päis või jalus&gt;) on vastuolus."

### <a name="automatic-resolution"></a>Automaatne lahendamine

Selle probleemi automaatseks lahendamiseks pole saadaval ühtegi valikut.

### <a name="manual-resolution"></a>Käsitsi lahendamine

#### <a name="option-1"></a>Suvand 1

Muutke konfigureeritud vormingut, kustutades ühe vastuolulise **Exceli\\päis** või **Exceli\\jalus** komponendi.

#### <a name="option-2"></a>Suvand 2

Muutke **päise/jaluse välimuse** atribuudi väärtust ühes vastuolulises **Exceli\\päise** või **Exceli\\jaluse** komponedis.

## <a name="additional-resources"></a>Lisaressursid

[ER-i funktsioon ALLITEMS](er-functions-list-allitems.md)

[ER-i funktsioon ALLITEMSQUERY](er-functions-list-allitemsquery.md)

[ER-i funktsioon INT64VALUE](er-functions-conversion-int64value.md)

[ER-i funktsioon INTVALUE](er-functions-conversion-intvalue.md)

[ER-i funktsioon FILTER](er-functions-list-filter.md)

[ER-i funktsioon WHERE](er-functions-list-where.md)

[Andmeallikate JOIN kasutamine elektroonilises aruandluse (ER) mudeli vastendustes andmete mitmest rakendusetabelist hankimiseks](er-join-data-sources.md)

[Elektroonilise aruandluse vormingute täitmise jälitamine jõudlusprobleemide tõrkeotsingu tegemiseks](trace-execution-er-troubleshoot-perf.md)

[Äridokumentide halduse ülevaade](er-business-document-management.md)

[Ära otsi loodud aruannetes Wordi sisu juhtelemente](er-design-configuration-word-suppress-controls.md)

[Ühe mudeli juure jaoks mitme tuletatud vastenduse haldamine](er-multiple-model-mappings.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
