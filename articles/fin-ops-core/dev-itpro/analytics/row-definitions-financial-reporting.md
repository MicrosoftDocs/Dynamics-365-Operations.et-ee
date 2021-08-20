---
title: Readefinitsioonid finantsaruande koosturis
description: Readefinitsioon on aruande komponent (koosteüksus), mis määrab finantsaruandel iga rea sisu.
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e175d1e3de1f5db31de9c4600c8a5935f0cb11a9d39bc0f4e142edf5fc00ce86
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745908"
---
# <a name="row-definitions-in-financial-report-designer"></a>Readefinitsioonid finantsaruande koosturis

[!include [banner](../includes/banner.md)]

Readefinitsioon on aruande komponent (koosteüksus), mis määrab finantsaruandel iga rea sisu. Readefinitsiooni saab kombineerida veerudefinitsioonide, aruandluspuu definitsioonide ja aruande definitsioonidega koosteüksuste grupi loomiseks, mida saavad kasutada mitu ettevõtet.

## <a name="create-a-row-definition"></a>Readefinitsiooni loomine

1. Klõpsake aruandekoosturis navigeerimispaanil suvandit **Readefinitsioonid**.
2. Klõpsake menüüs **Fail** valikut **Uus** ja seejärel valikut **Readefinitsioon**. Lisateabe saamiseks iga lahtri sisu kohta vt osa [Readefinitsiooni lahtrite muutmine](modify-row-definition-cells-financial-reporting.md).

## <a name="open-a-row-definition"></a>Readefinitsiooni avamine
1. Klõpsake aruandekoosturis navigeerimispaanil suvandit **Readefinitsioonid**.
2. Avamiseks topeltklõpsake readefinitsiooni nime.
3. Mis tahes readefinitsiooniga seostatud koosteüksuse vaatamiseks paremklõpsake readefinitsiooni ja seejärel valige **Seosed**.

## <a name="contents-of-a-row-definition"></a> Readefinitsiooni sisu
Readefinitsioon võib sisaldada kuni 20 000 finantsdimensiooni rida ja võib sisaldada järgmist teavet.

- Kirjeldav tekst, mis lisab aruandele tähenduse, luues jaotise päiseid, ridu ja tühikuid, nt **Sularaha** või **Kogutulu**
- Lingid finantsandmete juurde, mille hulka võivad kuuluda Microsoft Dynamics 365 Financei dimensiooniväärtused

    > [!NOTE]
    > Saate readefinitsiooni nii seadistada, et see võtab iga kord, kui aruanne luuakse, finantsdimensiooni süsteemist andmeid.

- Ridade kogusummad ja valemid, mis põhinevad lingitud finantsandmetel

Üldjuhul sisaldab iga readefinitsioon üht järgmist tüüpi teavet.

- Viited finantsdimensioonide süsteemile
- Andmetel põhinevad kogusummad või arvutused
- Vormindus

Readefinitsiooni teabe sisestamiseks on kaks viisi.

- Rea teabe käsitsi sisestamine uude readefinitsiooni. Lisateabe saamiseks vt osa [Readefinitsiooni lahtrite muutmine](modify-row-definition-cells-financial-reporting.md).
- Kasutage aruandekoosturit rea teabe toomiseks otse finantsdimensioonidest. Lisateavet leiate jaotisest Seotud valemid/read/üksused osas [Readefinitsiooni lahtrite muutmine](modify-row-definition-cells-financial-reporting.md).

## <a name="add-dimensions-in-a-row-definition"></a> Dimensioonide lisamine readefinitsioonis
Dimensioon on andmete ja väärtuste ühisosa. Aruandekoosturis saab andmeid ja väärtusi rühmitada. Seejärel saab kandeid üksikasjalikumalt liigitada ja analüüsida. Saate kasutada dialoogiboksi **Ridade sisestamine dimensioonidest**, et lisada readefinitsiooni korraga mitu rida. Dialoogiboksis kuvatakse iga dimensiooni puhul üks veerg. Järgmine tabel kirjeldab teavet, mida saab iga dimensiooni kohta määrata.

| Suvand                | Kirjeldus |
|-----------------------|-------------|
| Dimensioon             | Muster, mis tuvastab readefinitsiooni lisatava dimensiooni. See muster sisaldab ühte ampersandi (&) või numbrimärki (\#) iga koha puhul dimensioonides. Üldiselt kasutatakse kõiki ampersande põhikonto dimensiooni ja kõiki numbrimärke muude dimensioonide puhul. |
| Dimensioonivahemiku algus | Readefinitsiooni lisatava dimensiooni esimene väärtus. |
| Dimensioonivahemiku lõpp   | Viimane selle dimensiooni puhul readefinitsiooni lisatav väärtus. |

Readefinitsiooni dimensioonide lisamiseks tehke järgmist.

1. Klõpsake aruandekoosturis valikut **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.
2. Klõpsake menüüs **Redigeeri** suvandit **Sisesta read dimensioonidest**.
3. Valige dialoogiboksist **Ridade lisamine dimensioonidest** real **Dimensioonid** readefinitsiooni teisaldatava dimensiooni lahter ja seejärel klõpsake valikut **Kõik &&&**.
4. Readefinitsiooni piiramiseks dimensiooniväärtuste kindlasse vahemikku sisestage alguse dimensiooniväärtus lahtrisse **Dimensioonivahemiku algus** ja seejärel sisestage lõpu dimensiooniväärtus lahtrisse **Dimensioonivahemiku lõpp**. Kõikide valitud dimensiooni väärtuste kaasamiseks jätke need lahtrid tühjaks.

    > [!NOTE]
    > Kui dimensioonivahemikes on metamärke (\* ?), ei pruugi te olenevalt sellest, kuidas ERP andmebaas andmeid sordib, kõiki soovitud tulemusi saada.

5. Määrake väljal **Algrea kood** readefinitsiooni lisatava esimese dimensiooniväärtuse reakood.
6. Määrake väljal **Iga rea juurdekasv** järjestikuste reakoodide vahe. Näiteks kui esimene reakood on 100 ja juurdekasvu väärtus on 30, on esimeste uute ridade koodideks 100, 130, 160, 190 ja 220. Kasutage juurdekasvu väärtust, mis annab piisavalt ruumi uute vormingu ja valemi ridade lisamiseks.
7. Klõpsake nupul **OK**. Readefinitsiooni lisatakse iga valitud dimensiooniväärtuse kohta üks rida.

## <a name="adjust-rounding-in-a-row-definition"></a> Readefinitsiooni ümardamise korrigeerimine
Ümardatud summadega bilansi puhul ei pruugi kogusummad tasakaalus olla. See probleem võib ilmneda, kui kasutate bilansiaruandes ümardamist ja aruande definitsioon määrab samuti ümardamise. Võite kasutada valikut **Ümardamise korrigeerimine** readefinitsioonis bilansside summade tasakaalustamiseks. Ümardamise saab välja lülitada või muuta seda aruandedefinitsiooni vahekaardil **Sätted**. Järgmises tabelis näidatakse, kuidas summasid ümardatakse. Selles tabelis erinevad ridade 100 ja 200 kogusummad, kui ümardamine on sisse lülitatud.

| Rea kood | Summad ümardamata | Summa tuhandikeni ümardatuna |
|----------|--------------------------|-----------------------------------------|
| 100      | 3,600                    | 4                                       |
| 200      | 3,700                    | 4                                       |
| Kokku    | 7,300                    | 8                                       |

Bilansi ümardamise korrigeerimiseks tehke järgmist.

1. Klõpsake aruande kujundajas suvandit **Readefinitsioonid** ja seejärel avage muutmiseks readefinitsioon.
2. Klõpsake menüüs **Redigeeri** suvandit **Ümardusparandus**.
3. Sisestage dialoogiboksi **Ümardamise korrigeerimised** järgmised väärtused.

    - **Ümardamise korrigeerimise rida** – bilansi tasakaalustamiseks korrigeeritava rea reakood.
    - **Koguvarade rida** – bilansis koguvarasid sisaldava rea reakood.
    - **Kogu kohustuste ja omakapitali rida** – bilansis kogu kohustusi ja omakapitali sisaldava rea reakood.
    - **Korrigeerimissumma limiit** – positiivne täisarv, mis määrab automaatsete korrigeerimiste limiidi. Seda summat võrreldakse tegeliku ümardamise erinevuse absoluutväärtusega.

    > [!NOTE]
    > Need reakoodid tuleb teie finantsandmetega siduda. Teisisõnu peab real olema lahtris **Link finantsdimensioonidele** dimensiooniväärtus. **Ärge** viidake kirjelduse (**DESC**), arvutatud (**CALC**) või summeeritud (**TOT**) reale.

Teie bilansi summad tasakaalustatakse nüüd ümardamise sisselülitamisel võrdselt.

> [!NOTE]
> Korrigeerimise piirangut kohaldatakse aruande definitsiooni puhul määratud suvandi **Ümardamistäpsus** põhjal. Näiteks kui valite aruande ümardamise tuhandikeni ja sisestate arvu **2** väljale **Korrigeerimissumma limiit**, kuvatakse hoiatusteade, kui välja **Ümardamise korrigeerimise rida** väärtus suureneb või väheneb rohkem kui 2,000.

## <a name="format-row-and-column-text"></a>Ridade ja veergude teksti vormindamine
Saate kohandada aruannete ilmet fontide muutmise ja teksti vormindamise teel. Järgmistes jaotistes selgitatakse, kuidas aruannetes ridade ja veergude ilmet vormindada.

### <a name="manage-font-styles"></a>Kirjatüüpide haldamine

Saate aruande fondilaade luua ja muuta. Seejärel saab rakendada need laadid dokumendile või aruande konkreetsele reale või veerule.

<table>
<tbody>
<tr>
<td><strong>Kirjatüübi loomine</strong></td>
<td>
<ol>
<li>Klõpsake aruande kujundaja menüüs <strong>Vorming </strong>suvandit <strong>Laadid ja vorming</strong>.</li>
<li>Klõpsake dialoogiboksis <strong>Laadid ja vormindamine</strong> suvandit <strong>Uus</strong> ning seejärel sisestage uuele laadile kordumatu nimi.</li>
<li>Tehke fondivalikud ja seejärel klõpsake suvandit <strong>OK</strong>.</li>
</ol>
</td>
</tr>
<tr>
<td><strong>Fondi laadi muutmine</strong></td>
<td>
<ol>
<li>Klõpsake aruande kujundaja menüüs <strong>Vorming </strong>suvandit <strong>Laadid ja vorming</strong>.</li>
<li>Valige muudetav laad dialoogiboksist <strong>Laadid ja vormindamine</strong> ja klõpsake seejärel suvandit <strong>Muuda</strong>.</li>
<li>Tehke fondivalikud ja seejärel klõpsake suvandit <strong>OK</strong>.</li>
</ol>
</td>
</tr>
<tr>
<td><strong>Kirjatüübi rakendamine</strong></td>
<td>
<ol>
<li>Valige aruandekoosturi definitsioonis või veeru definitsioonis või päistes ja jalustes vähemalt üks lahter.</li>
<li>Valige tööriistaribal olevast loendist <strong>Laad</strong> fondi laad.</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a>Rea teksti vormindamine

Readefinitsioonis määratud vorming alistab veeru- ja aruande definitsioonis määratud vormingu. Saate tekstivormingut muuta, kasutades vormindamise tööriistariba nuppe. Tegemist on Microsoft Windowsi standardsete juhtelementidega.

1. Avage aruandekoosturis muudetav readefinitsioon.
2. Valige vormindatavad lahtrid. Mitme lahtri valimiseks hoidke lahtri valimisel all klahvi Ctrl.
3. Vormingu rakendamiseks klõpsake tööriistariba nuppu. Näiteks rea taandamiseks valige rida ja seejärel klõpsake tööriistariba ikooni **Suurenda taanet** ![Suurenda taanet.](media/indent.gif "Suurenda taanet") tööriistaribal.

### <a name="adjust-columns-while-you-design-reports"></a>Veergude korrigeerimine aruannete kujundamisel

Nende veergude vaatamise lihtsustamiseks, mille kallal readefinitsioonis töötate, saate korrigeerida veeru laiust ning samuti peita (minimeerida) või kuvada veerge vaatepaanil. Tehtavad muudatused mõjutavad ainult veergude ilmet ekraanil. Need ei mõjuta veeru vormindust aruannetes.

### <a name="change-the-width-of-a-column-in-the-view-pane"></a>Veeru laiuse muutmine vaatepaanil

1. Avage aruande kujundajas muudetav readefinitsioon.
2. Valige menüüs **Vorming** suvand **Veeru laius**.
3. Sisestage dialoogiboksi **Veeru laius** väärtus ja klõpsake siis nuppu **OK**. Teine võimalus on lohistada veeru laiuse muutmiseks veeru päise lahtri paremat äärt.

### <a name="hide-columns-in-the-view-pane"></a>Veergude peitmine vaatepaanil

1. Avage aruande kujundajas muudetav readefinitsioon.
2. Valige minimeeritav(ad) veerg (veerud).
3. Paremklõpsake ja seejärel klõpsake suvandit **Peida**.

### <a name="show-all-hidden-columns-in-the-view-pane"></a>Kõikide peidetud veergude kuvamine vaatepaanil

1. Avage aruande kujundajas muudetav readefinitsioon.
2. Paremklõpsake kuvatavat minimeeritud veergu ja klõpsake seejärel valikut **Kuva**.


## <a name="additional-resources"></a>Lisaressursid

[Finantsaruandlus](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]