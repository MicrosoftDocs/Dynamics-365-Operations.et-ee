---
title: Avaldisepiirangud ja tabelipiirangud toote konfiguratsioonimudelites
description: "Selles teemas kirjeldatakse avaldise piirangute ja tabeli piirangute kasutamist. Piirangute abil kontrollitakse atribuutide väärtusi, mida saab valida toodete konfigureerimisel müügitellimuse, müügipakkumise, ostutellimuse või tootmistellimuse jaoks. Saate avaldise piiranguid või tabeli piiranguid kasutada sõltuvalt sellest, kuidas soovite piiranguid luua."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15 - 08 - 06
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 1fe8a0d90a3f707fa7b0fea0310c819ce5040a42
ms.lasthandoff: 03/30/2017


---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a>Avaldisepiirangud ja tabelipiirangud toote konfiguratsioonimudelites

Selles teemas kirjeldatakse avaldise piirangute ja tabeli piirangute kasutamist. Piirangute abil kontrollitakse atribuutide väärtusi, mida saab valida toodete konfigureerimisel müügitellimuse, müügipakkumise, ostutellimuse või tootmistellimuse jaoks. Saate avaldise piiranguid või tabeli piiranguid kasutada sõltuvalt sellest, kuidas soovite piiranguid luua. 

Piirangute abil juhitakse atribuutide väärtusi, mida saab valida toodete konfigureerimisel müügitellimuse, müügipakkumise, ostutellimuse või tootmistellimuse jaoks. Saate avaldise piiranguid või tabeli piiranguid kasutada sõltuvalt sellest, kuidas soovite piiranguid luua.

## <a name="what-are-expression-constraints"></a>Mis on avaldise piirangud?
Avaldise piiranguid iseloomustab avaldis, milles kasutatakse aritmeetilisi ja kahendmuutujaid ning funktsioone. Avaldise piirang kirjutatakse konkreetsele toote konfiguratsioonimudeli komponendile. Seda ei saa uuesti kasutada või teise komponendiga jagada. Kuid komponendi avaldise piirangud võivad viidata komponendi alamkomponentide atribuutidele.

## <a name="what-are-table-constraints"></a>Mis on tabeli piirangud?
Tabeli piirangud loetlevad väärtuste kombinatsioonid, mis toote konfigureerimisel atribuutide puhul lubatud on. Tabeli piirangu definitsioone saab üldiselt kasutada. Komponendile toote konfiguratsioonimudelis tabeli piirangu loomisel tuleb valida tabeli piirangu definitsioon. Lubatud kombinatsioonide loomiseks tuleb lisada komponentidele teatud tüüpi atribuudid. Igal atribuudi tüübil on kindel väärtus.

### <a name="example-of-a-table-constraint"></a>Tabeli piirangu näide

Selles näites selgitatakse, kuidas saate piirata kõlari konfiguratsiooni kindla korpuseviimistluse ja esiküljega. Esimeses tabelis on üldkonfiguratsiooniks saadaolevad korpuseviimistlused ja esiküljed. Väärtused on määratletud selle ** kapis valmis ** ja **ees grill** atribuut tüübid.

| Atribuudi tüüp | Väärtused                      |
|----------------|-----------------------------|
| Kabinetiviimistlus | Must, tamm, roosipuu, valge |
| Esivõre    | Must, metall, valge         |

Järgmises tabelis on toodud kombinatsioonid, mis on määratletud tabelipiiranguga **Värv ja viimistlus**. Selle tabelipiirangu abil saate konfigureerida tammeviimistluse ja musta võrega kõlari, roosipuust viimistluse ja valge võrega kõlari jne.

| Valmis         | Võre                       |
|----------------|-----------------------------|
| Tamm            | Must                       |
| Roosipuu       | Valge                       |
| Valge          | Must                       |
| Valge          | Valge                       |
| Must          | Must                       |
| Must          | Metall                       | 

Saate luua süsteemi ja kasutaja määratletud tabeli piiranguid. Lisateabe saamiseks vt jaotist [Süsteemi määratletud ja kasutaja määratletud tabelipiirangud](system-defined-user-defined-table-constraints.md).

## <a name="what-syntax-should-be-used-to-write-constraints"></a>Millist süntaksit kasutada kirjutada piiranguid?
Piirangute kirjutamisel tuleb kasutada optimeerimise modelleerimiskeele (OML) süntaksit. Süsteem kasutab Microsoft Solver sihtasutuse piirangu solver lahendada piiranguid.

## <a name="should-i-use-table-constraints-or-expression-constraints"></a>Kas peaksin kasutama tabeli või avaldise piiranguid?
Saate kasutada avaldisepiiranguid või tabelipiiranguid olenevalt sellest, kuidas soovite piirangud koostada. Tabelipiirangu saate luua maatriksina, samas kui avaldisepiirang on eraldi lause. Toote konfigureerimisel pole oluline, millist piirangut kasutatakse. Järgmine näide selgitab kahe meetodi erinevust.  

Toote konfigureerimisel järgmiste piiranguseadistuste abil on need kombinatsioonid lubatud.

-   Toode, mille värv on must ja suurus 30 või 50.
-   Toode, mille värv on punane ja suurus 20.

### <a name="table-constraint-setup"></a>Tabeli piirangu seadistus

| Värv | Suurus |
|-------|------|
| Must | 30   |
| Must | 50   |
| Punane   | 20   |

### <a name="expression-constraint-setup"></a>Avaldisepiirangu seadistus

(Värv == "Must" & (suurus == "30" | suurus == "50")) | (värv == "Punane" & suurus = "20")

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a>Kas avaldise piirangute kirjutamisel tuleks kasutada tehtemärke või infix-märke?
Saate kirjutada avaldisepiirangu kas saadaolevaid tehtemärke või infix-märke kasutades. Tehtemärkide **Min**, **Max** ja **Abs **puhul ei saa infix-märke kasutada. Need tehtemärgid sisalduvad standardina enamikus programmeerimiskeeltes.

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a>Milliseid tehtemärke ja infix-märke saan avaldisepiirangute kirjutamisel kasutada?
Järgmistes tabelites on tehtemärkide ja infix-märkide loend, mida saate toote konfiguratsioonimudeli komponendile avaldisepiirangu kirjutamisel kasutada. Esimeses tabelis toodud näited selgitavad, kuidas infix-märkide või tehtemärkide abil avaldist kirjutada.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Tehtemärk</th>
<th>Kirjeldus</th>
<th>Süntaks</th>
<th>Näited</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tähendab</td>
<td>See on tõene, kui esimene tingimus on väär, teine tingimus on tõene või mõlemad.</td>
<td>Tähendab[a, b], infix: a -: b</td>
<td><ul>
<li><strong>Operaator:</strong> tähendab [x! = 0, y &gt;= 0]</li>
<li><strong>Infix märke:</strong> x! = 0-: y &gt;= 0</li>
</ul></td>
</tr>
<tr class="even">
<td>Ja</td>
<td>See on tõene ainult juhul, kui kõik tingimused on tõesed. Kui tingimuste arv on 0 (null), on vastus <strong>Tõene</strong>.</td>
<td>Ja [args] infix: a &amp;b &amp; ... &amp;z</td>
<td><ul>
<li><strong>Operaator:</strong> ja [x == 2, y &lt;= 2]</li>
<li><strong>Infix märke:</strong> x == 2 &amp;y &lt;= 2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Või</td>
<td>See on tõene, kui mis tahes tingimus on tõene. Kui tingimuste arv on 0 (null), on vastus <strong>Väär</strong>.</td>
<td>Või [args] infix: on | b | ... | z</td>
<td><ul>
<li><strong>Operaator:</strong> või [x == 2, y &lt;= 2]</li>
<li><strong>Infix märke:</strong> x == 2 | y &lt;= 2</li>
</ul></td>
</tr>
<tr class="even">
<td>Pluss</td>
<td>See summeerib tingimused. Kui tingimuste arv on 0 (null), on vastus <strong>0</strong>.</td>
<td>Pluss [args] infix: a + b +... + z</td>
<td><ul>
<li><strong>Tehtemärk:</strong> Plus[x, y, 2] == z</li>
<li><strong>Infix-märk:</strong> x + y + 2 == z</li>
</ul></td>
</tr>
<tr class="odd">
<td>Miinus</td>
<td>See muudab argumendi negatiivseks. Sel peab olema täpselt üks tingimus.</td>
<td>Miinus[avaldis], infix: –avaldis</td>
<td><ul>
<li><strong>Tehtemärk:</strong> Minus[x] == y</li>
<li><strong>Infix-märk:</strong> -x == y</li>
</ul></td>
</tr>
<tr class="even">
<td>Abs</td>
<td>See arvestab tingimuse absoluutväärtuse. Sel peab olema täpselt üks tingimus.</td>
<td>Abs[avaldis]</td>
<td><strong>Tehtemärk:</strong> Abs[x]</td>
</tr>
<tr class="odd">
<td>Ajad</td>
<td>See arvestab tingimuste korrutise. Kui tingimuste arv on 0 (null), on vastus <strong>1</strong>.</td>
<td>Infix korda [args]: a * b *... * z</td>
<td><ul>
<li><strong>Tehtemärk:</strong> Times[x, y, 2] == z</li>
<li><strong>Infix-märk:</strong> x * y * 2 == z</li>
</ul></td>
</tr>
<tr class="even">
<td>Võimsus</td>
<td>See võtab astme. See rakendab paremalt vasakule astendamise. (Tähendab, see on õigus-assotsiatiivne.) Seega <strong>võimu [a, b, c]</strong> on <strong>võimsus [a, võimsus [b, c]]</strong>. <strong>Astet</strong> saab kasutada ainult siis, kui aste on positiivne konstant.</td>
<td>Võimu [args], infix: a ^ b ^... ^ z</td>
<td><ul>
<li><strong>Tehtemärk:</strong> Power[x, 2] == y</li>
<li><strong>Infix-märk:</strong> x ^ 2 == y</li>
</ul></td>
</tr>
<tr class="odd">
<td>Suurim</td>
<td>See annab vastuseks suurima tingimuse. Kui tingimuste arv on 0 (null), on vastus <strong>Lõpmatus</strong>.</td>
<td>Max[argumendid]</td>
<td><strong>Tehtemärk:</strong> Max[x, y, 2] == z</td>
</tr>
<tr class="even">
<td>Väikseim</td>
<td>See annab vastuseks vähima tingimuse. Kui tingimuste arv on 0 (null), on vastus <strong>Lõpmatus</strong>.</td>
<td>Min[argumendid]</td>
<td><strong>Tehtemärk:</strong> Min[x, y, 2] == z</td>
</tr>
<tr class="odd">
<td>Ei ole</td>
<td>See annab vastuseks tingimuse loogilise pöördväärtuse. Sel peab olema täpselt üks tingimus.</td>
<td>Pole[avaldis], infix: !avaldis</td>
<td><ul>
<li><strong>Operaator:</strong> ei [x] &amp;ei [y == 3]</li>
<li><strong>Infix-märk:</strong> !x!(y == 3)</li>
</ul></td>
</tr>
</tbody>
</table>

Järgmise tabeli näited selgitavad, kuidas kirjutada infix-märke.

| Infix-märk    | Kirjeldus                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| x + y + z         | Lisa                                                                                      |
| X \*y \*z       | Korrutamine                                                                                |
| x - y             | Binaarne lahutamine teisendatakse samamoodi nagu negatiivse teise liikmega binaarne liitmine. |
| x ^ y ^ z         | Parempoolse seosega astendamine                                                   |
| !x                | Kahendmuutuja pole                                                                                   |
| x -: y            | Kahendmuutuja mõju                                                                           |
| x | y | z         | Kahendmuutuja või                                                                                    |
| x & y & z         | Kahendmuutuja ja                                                                                   |
| x == y == z       | Võrdne                                                                                      |
| x != y != z       | Distinktne                                                                                      |
| X &lt;y &lt;z   | Väiksem kui                                                                                     |
| X &gt;y &gt;z   | Suurem kui                                                                                  |
| X &lt;= y &lt;= z | Väiksem kui või võrdne                                                                         |
| X &gt;= y &gt;= z | Suurem kui või võrdne                                                                      |
| (x)               | Sulud alistavad vaikejärjestuse.                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a>Miks minu avaldisepiiranguid õigesti ei kinnitata?
Toote konfiguratsioonimudelis ei saa kasutada atribuutide, komponentide või alamkomponentide nimena lahendaja nimena reserveeritud märksõnu. Siin on nimekiri ei saa kasutada reserveeritud märksõnad:

-   Ülempiir
-   Element
-   Võrdne
-   Põrand
-   Kui
-   Väiksem kui
-   Suurem
-   Tähendab
-   Logi
-   Suurim
-   Väikseim
-   Miinus
-   Pluss
-   Võimsus
-   Ajad
-   Pesa
-   Mudel
-   Otsus
-   Eesmärk


<a name="see-also"></a>Vt ka
--------

[Väljend piirangu (ülesande juhend) loomine](http://ax.help.dynamics.com/en/wiki/create-an-expression-constraint/)

[Lisada tootemudelile konfiguratsiooni (ülesande juhend) arvutus](http://ax.help.dynamics.com/en/wiki/add-a-calculation-to-a-product-configuration-model/)


