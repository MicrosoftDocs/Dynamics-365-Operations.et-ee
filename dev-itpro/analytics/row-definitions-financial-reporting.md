---
title: Readefinitsioonid finantsaruande koosturis
description: "Readefinitsioon on aruande komponent (koosteüksus), mis määrab finantsaruandel iga rea sisu. Readefinitsiooni saab kombineerida veerudefinitsioonide, aruandluspuu definitsioonide ja aruande definitsioonidega koosteüksuste grupi loomiseks, mida saavad kasutada mitu ettevõtet."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-18 15 - 42 - 39
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Management Reporter, Core
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: a2f92effd1cfdc1d5da2c5ec895c0487a6fc82a4
ms.lasthandoff: 03/29/2017


---

# <a name="row-definitions-in-financial-report-designer"></a>Readefinitsioonid finantsaruande koosturis

Readefinitsioon on aruande komponent (koosteüksus), mis määrab finantsaruandel iga rea sisu. Readefinitsiooni saab kombineerida veerudefinitsioonide, aruandluspuu definitsioonide ja aruande definitsioonidega koosteüksuste grupi loomiseks, mida saavad kasutada mitu ettevõtet.

<a name="create-a-row-definition"></a>Readefinitsiooni loomine
-----------------------

1.  Klõpsake aruandekoosturis navigeerimispaanil suvandit **Readefinitsioonid**.
2.  Klõpsake menüüs **Fail** valikut **Uus** ja seejärel valikut **Readefinitsioon**. Lisateabe saamiseks iga lahtri sisu kohta vt osa [Readefinitsiooni lahtrite muutmine](modify-row-definition-cells-financial-reporting.md).

## <a name="open-a-row-definition"></a>Readefinitsiooni avamine
1.  Klõpsake aruandekoosturis navigeerimispaanil suvandit **Readefinitsioonid**.
2.  Avamiseks topeltklõpsake readefinitsiooni nime.
3.  Mis tahes readefinitsiooniga seostatud koosteüksuse vaatamiseks paremklõpsake readefinitsiooni ja seejärel valige **Seosed**.

## <a name="contents-of-a-row-definition"></a> Readefinitsiooni sisu
Readefinitsioon võib sisaldada kuni 20 000 finantsdimensiooni rida ja võib sisaldada järgmist teavet.

-   Kirjeldav tekst, mis lisab aruandele tähenduse, luues jaotise päiseid, ridu ja tühikuid, nt **Sularaha** või **Kogutulu**
-   Lingid finantsandmetele, mis võivad hõlmata dimensiooniväärtusi Microsoft Dynamics 365 for Operationsis. **Märkus.** Saate seadistada readefinitsiooni andmete tõmbamiseks finantsdimensioonide süsteemist iga kord, kui aruanne luuakse.
-   Ridade kogusummad ja valemid, mis põhinevad lingitud finantsandmetel

Üldjuhul sisaldab iga readefinitsioon üht järgmist tüüpi teavet.

-   Viited finantsdimensioonide süsteemile
-   Andmetel põhinevad kogusummad või arvutused
-   Vormindus

Readefinitsiooni teabe sisestamiseks on kaks viisi.

-   Rea teabe käsitsi sisestamine uude readefinitsiooni. Lisateabe saamiseks vt osa [Readefinitsiooni lahtrite muutmine](modify-row-definition-cells-financial-reporting.md).
-   Kasutage aruandekoosturit rea teabe toomiseks otse finantsdimensioonidest. Lisateavet leiate jaotisest Seotud valemid/read/üksused osas [Readefinitsiooni lahtrite muutmine](modify-row-definition-cells-financial-reporting.md).

## <a name="add-dimensions-in-a-row-definition"></a> Dimensioonide lisamine readefinitsioonis
Dimensioon on andmete ja väärtuste ühisosa. Aruandekoosturis saab andmeid ja väärtusi rühmitada. Seejärel saab kandeid üksikasjalikumalt liigitada ja analüüsida. Saate kasutada dialoogiboksi **Ridade sisestamine dimensioonidest**, et lisada readefinitsiooni korraga mitu rida. Dialoogiboksis kuvatakse iga dimensiooni puhul üks veerg. Järgmine tabel kirjeldab teavet, mida saab iga dimensiooni kohta määrata.

| Suvand                | Kirjeldus                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dimensioon             | Muster, mis tuvastab readefinitsiooni lisatava dimensiooni. See muster sisaldab ühte ampersandi (&) või numbrimärki (\#) iga koha puhul dimensioonides. Üldiselt kasutatakse kõiki ampersande põhikonto dimensiooni ja kõiki numbrimärke muude dimensioonide puhul. |
| Dimensioonivahemiku algus | Esimene selle dimensiooni puhul readefinitsiooni lisatav väärtus.                                                                                                                                                                                                                 |
| Dimensioonivahemiku lõpp   | Viimane selle dimensiooni puhul readefinitsiooni lisatav väärtus.                                                                                                                                                                                                                  |

Readefinitsiooni dimensioonide lisamiseks tehke järgmist.

1.  Klõpsake aruandekoosturis valikut **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.
2.  Klõpsake menüüs **Redigeeri** suvandit **Sisesta read dimensioonidest**.
3.  Valige dialoogiboksist **Ridade lisamine dimensioonidest **real **Dimensioonid** readefinitsiooni teisaldatava dimensiooni lahter ja seejärel klõpsake valikut **Kõik &&&**.
4.  Readefinitsiooni piiramiseks dimensiooniväärtuste kindlasse vahemikku sisestage alguse dimensiooniväärtus lahtrisse** Dimensioonivahemiku algus **ja seejärel sisestage lõpu dimensiooniväärtus lahtrisse **Dimensioonivahemiku lõpp**. Kõikide valitud dimensiooni väärtuste kaasamiseks jätke need lahtrid tühjaks. **Märkus.** Metamärgid (\* või ?) dimensioonivahemikes ei pruugi tagastada kõiki soovitud tulemusi, olenevalt sellest, kuidas ERP andmebaas andmeid kogub.
5.  Määrake väljal **Algrea kood** readefinitsiooni lisatava esimese dimensiooniväärtuse reakood.
6.  Määrake väljal **Iga rea juurdekasv** järjestikuste reakoodide vahe. Näiteks kui esimene reakood on 100 ja juurdekasvu väärtus on 30, on esimeste uute ridade koodideks 100, 130, 160, 190 ja 220. Kasutage juurdekasvu väärtust, mis annab piisavalt ruumi uute vormingu ja valemi ridade lisamiseks.
7.  Klõpsake nupul **OK**. Readefinitsiooni lisatakse iga valitud dimensiooniväärtuse kohta üks rida.

## <a name="adjust-rounding-in-a-row-definition"></a> Readefinitsiooni ümardamise korrigeerimine
Ümardatud summadega bilansi puhul ei pruugi kogusummad tasakaalus olla. See probleem võib ilmneda, kui kasutate bilansiaruandes ümardamist ja aruande definitsioon määrab samuti ümardamise. Võite kasutada valikut **Ümardamise korrigeerimine** readefinitsioonis bilansside summade tasakaalustamiseks. Ümardamise saab välja lülitada või muuta seda aruandedefinitsiooni vahekaardil **Sätted**. Järgmises tabelis näidatakse, kuidas summasid ümardatakse. Selles tabelis erinevad ridade 100 ja 200 kogusummad, kui ümardamine on sisse lülitatud.

| Rea kood | Summad ümardamata | Summa tuhandikeni ümardatuna |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4                                       |
| 200      | 3,700                    | 4                                       |
| Kokku    | 7,300                    | 8                                       |

Bilansi ümardamise korrigeerimiseks tehke järgmist.

1.  Klõpsake aruande kujundajas suvandit **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.
2.  Klõpsake menüüs **Redigeerimine** suvandit **Ümardamise korrigeerimine**.
3.  Sisestage dialoogiboksi **Ümardamise korrigeerimised** järgmised väärtused.
    -   **Ümardamise korrigeerimise rida** – bilansi tasakaalustamiseks korrigeeritava rea reakood.
    -   **Koguvarade rida** – bilansis koguvarasid sisaldava rea reakood.
    -   **Kogu kohustuste ja omakapitali rida** – bilansis kogu kohustusi ja omakapitali sisaldava rea reakood.
    -   **Korrigeerimissumma limiit** – positiivne täisarv, mis määrab automaatsete korrigeerimiste limiidi. Seda summat võrreldakse tegeliku ümardamiserinevuse absoluutväärtusega.

    **Märkus. **Need reakoodid peavad olema teie finantsandmetega seotud. Teisisõnu peab real olema lahtris **Link finantsdimensioonidele** dimensiooniväärtus. **Ärge** viidake kirjelduse (**DESC**), arvutatud (**CALC**) või summeeritud (**TOT**) reale.

Teie bilansi summad tasakaalustatakse nüüd ümardamise sisselülitamisel võrdselt. **Märkus. **Korrigeerimise limiiti rakendatakse suvandi **Ümardamise täpsus** alusel, mis on määratud aruande definitsioonis. Näiteks kui valite aruande ümardamise tuhandikeni ja sisestate arvu **2** väljale **Korrigeerimissumma limiit**, kuvatakse hoiatusteade, kui välja **Ümardamise korrigeerimise rida** väärtus suureneb või väheneb rohkem kui 2,000.

## <a name="format-row-and-column-text"></a>Ridade ja veergude teksti vormindamine
Saate kohandada aruannete ilmet fontide muutmise ja teksti vormindamise teel. Järgmistes jaotistes selgitatakse, kuidas aruannetes ridade ja veergude ilmet vormindada.

### <a name="manage-font-styles"></a>Kirjatüüpide haldamine

Saate aruande fondilaade luua ja muuta. Seejärel saab rakendada need laadid dokumendile või aruande konkreetsele reale või veerule.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Kirjatüübi loomine</td>
<td><ol>
<li>Klõpsake aruande kujundaja menüüs <strong>Vorming </strong>suvandit <strong>Laadid ja vorming</strong>.</li>
<li>Klõpsake dialoogiboksis <strong>Laadid ja vorming</strong> valikut <strong>Uus</strong> ja seejärel sisestage uue laadi kordumatu nimi.</li>
<li>Tehke laadi valikud ja seejärel klõpsake nuppu <strong>OK</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Kirjatüübi muutmine</td>
<td><ol>
<li>Klõpsake aruande kujundaja menüüs <strong>Vorming </strong>suvandit <strong>Laadid ja vorming</strong>.</li>
<li>Valige dialoogiboksist <strong>Laadid ja vorming</strong> muudetav laad ja klõpsake seejärel valikut <strong>Muuda</strong>.</li>
<li>Tehke laadi valikud ja seejärel klõpsake nuppu <strong>OK</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kirjatüübi rakendamine</td>
<td><ol>
<li>Valige aruandekoosturi definitsioonis või veeru definitsioonis või päistes ja jalustes vähemalt üks lahter.</li>
<li>Valige kirjatüüp tööriistariba loendist <strong>Laad</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Rea teksti vormindamine

Readefinitsioonis määratud vorming alistab veeru- ja aruande definitsioonis määratud vormingu. Saate tekstivormingut muuta, kasutades vormindamise tööriistariba nuppe. Need juhtelemendid on standardsed Microsoft Windowsi juhtelemendid.

1.  Avage aruande kujundajas muudetav readefinitsioon.
2.  Valige vormindatavad lahtrid. Mitme lahtri valimiseks hoidke lahtri valimisel all klahvi Ctrl.
3.  Vormingu rakendamiseks klõpsake tööriistariba nuppu. Näiteks rea taandamiseks valige rida ja seejärel klõpsake tööriistariba ikooni **Suurenda taanet** ![Suurenda taanet](https://i-technet.sec.s-msft.com/dynimg/IC679497.gif "Suurenda taanet").

### <a name="adjust-columns-while-you-design-reports"></a>Veergude korrigeerimine aruannete kujundamisel

Nende veergude vaatamise lihtsustamiseks, mille kallal readefinitsioonis töötate, saate korrigeerida veeru laiust ning samuti peita (minimeerida) või kuvada veerge vaatepaanil. Tehtavad muudatused mõjutavad ainult veergude ilmet ekraanil. Need ei mõjuta veeru vormindust aruannetes.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>Veeru laiuse muutmine vaatepaanil

1.  Avage aruande kujundajas muudetav readefinitsioon.
2.  Valige menüüs **Vorming** suvand **Veeru laius**.
3.  Sisestage dialoogiboksi **Veeru laius** väärtus ja klõpsake siis nuppu **OK**. Teine võimalus on lohistada veeru laiuse muutmiseks veeru päise lahtri paremat äärt.

### <a name="hide-columns-in-the-view-pane"></a>Veergude peitmine vaatepaanil

1.  Avage aruande kujundajas muudetav readefinitsioon.
2.  Valige veerg või veerud, mida minimeerida.
3.  Paremklõpsake ja seejärel klõpsake suvandit **Peida**.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Kõikide peidetud veergude kuvamine vaatepaanil

1.  Avage aruande kujundajas muudetav readefinitsioon.
2.  Paremklõpsake kuvatavat minimeeritud veergu ja klõpsake seejärel valikut **Kuva**.


<a name="see-also"></a>Vt ka
--------

[Microsoft Dynamics 365 for Operationsi finantsaruandlus](financial-reporting-intro.md)

