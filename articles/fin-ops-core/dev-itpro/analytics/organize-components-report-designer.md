---
title: Aruande komponentide korraldamine aruandekoosturis
description: Selles teemas selgitatakse olemasolevate aruannete, koosteüksuste ja objektide korraldamist aruandekoosturis.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e1672ee1777150a7f78c03d07dc79df118a3632f
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347872"
---
# <a name="organize-report-components-in-report-designer"></a>Aruande komponentide korraldamine aruandekoosturis

[!include [banner](../includes/banner.md)]

Kui olete koosteüksused kujundanud ja aruanded koostanud, on abiks nende objektide korraldamine, et kasutajatel oleks neid hõlpsam leida. Selles artiklis kirjeldatakse olemasolevate aruannete,koosteüksuste ja objektide korraldamist aruandekoosturis.

Failide korraldamiseks saate aruandekoosturis kaustu, aruandeid, koosteüksusi ja muid objekte ümber nimetada. Ümbernimetatava objekti tüübist olenevalt võib teil olla vaja selle objekti seoseid värskendada.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Aruande kujundaja kausta või koosteüksuse ümbernimetamine
Saate aruandekoosturis kaustade, aruande-, rea-, veeru- ja aruandluspuu definitsioonide nime muuta.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Kausta või koosteüksuse ümbernimetamine aruandekoosturis

1. Kasutage aruandekoosturis ümbernimetatava kausta või objekti leidmiseks navigeerimispaani.
2. Paremklõpsake kausta või objekti ja seejärel klõpsake suvandit **Nimeta ümber**. Navigeerimispaani väli **Nimi** muutub aktiivseks.
3. Sisestage uus nimi ja seejärel vajutage suvandit Sisesta.
4. Kui koosteüksus on readefinitsioon, veeru definitsioon või aruandluspuu definitsioon, peate värskendama teisi sellega seotud koosteüksusi. Paremklõpsake 3. etapis ümbernimetatud koosteüksust, valige **Seosed** ja seejärel valige element loendist selle värskendamiseks.
5. Korrake 4. etappi, kuni kõik seotud elemendid on värskendatud.

## <a name="create-and-manage-report-groups"></a>Aruandegruppide loomine ja haldamine
Saate grupeerida aruande definitsioone korraga mitme aruande loomiseks. Aruandegruppide loomiseks, muutmiseks ja kustutamiseks peab teil olema kujundaja või administraatori roll. Looja rolliga kasutajad saavad aruandegruppe luua ja ka aruandegruppide kasutaja aruande definitsiooni seadistust muuta.

### <a name="create-a-report-group"></a>Aruandegrupi loomine

1. Klõpsake aruandekoosturi navigeerimispaanil valikut **Aruandegrupid**.
2. Klõpsake menüüs **Fail** valikuid **Uus** &gt; **Aruandegrupi definitsioon** uue aruandegrupi avamiseks vaaturi aknas. Teine võimalus on klõpsata tööriistaribal nuppu **Aruandegrupp** ![Aruandegrupp.](media/report-group.gif "Aruanderühm") tööriistaribal.
3. Klõpsake vahekaarti **Aruandegrupp**. Eraldi aruande definitsioonide teabe tühistamiseks selle aruande loomise puhul märkige ruut **Ettevõtte, üksikasjade ja kuupäeva sätete tühistamine** eraldi aruande definitsioonidest. Ettevõtte nime, üksikasjataseme, tinglikkuse seadistuse ja kuupäeva teave sisestatakse automaatselt, kuid saate endiselt värskendusi teha.
4. Mitme arvestusvaluutasid näitava aruande koostamiseks märkige ruut **Kaasa kõik aruandlusvaluutad**. Seejärel pääsete mitmesse vaatesse, klõpsates aruande vaatamisel veebivaaturis nuppu **Valuuta**.
5. Aruandegruppi kaasatavate aruannete valimiseks klõpsake väljal **Grupi aruanded** valikut **Lisa**. Mitme aruande valimiseks dialoogiboksis **Lisa** hoidke aruannete valimisel all klahvi Ctrl. Kui olete aruannete valimise lõpetanud, klõpsake **OK**.
6. Uue aruandegrupi salvestamiseks klõpsake **Fail** &gt; **Salvesta**.

### <a name="modify-a-report-group"></a>Aruandegrupi muutmine

1. Klõpsake aruandekoosturi navigeerimispaanil valikut **Aruandegrupid**.
2. Aruandegrupi muutmiseks topeltklõpsake.
3. Tehke vahekaardil **Aruandegrupp** soovitud muudatused.
4. Klõpsake menüüs **Fail** käsku **Salvesta** muudetud aruandegrupi salvestamiseks, Teine võimalus on klõpsata tööriistaribal nuppu **Salvesta** ![Salvesta.](media/save.gif "Salvesta") tööriistaribal.

> Kui olete plaaninud aruanded määratud vahemikel koostamiseks, saate need sätted tühistada ja aruande kohe luua.

### <a name="generate-a-report-group-report"></a>Aruandegrupi aruande loomine

1. Klõpsake aruandekoosturi navigeerimispaanil valikut **Aruandegrupid**.
2. Avage loodav aruandegrupp.
3. Klõpsake aruannete loomiseks nuppu **Loo aruanne** ![Loo aruanne.](media/generate-report.gif "Aruande loomine") aruannete loomiseks.

### <a name="delete-a-report-group"></a>Aruandegrupi kustutamine

1. Klõpsake aruandekoosturi navigeerimispaanil valikut **Aruandegrupid**.
2. Paremklõpsake kustutamiseks aruandegruppi ja seejärel tehke valik **Kustuta**.
3. Kui kuvatakse kinnitusteade, klõpsake valikut **Jah**.

## <a name="report-group-tab-controls"></a>Vahekaardi Aruandegrupp juhtelemendid
Järgmises tabelis kirjeldatakse vahekaardi **Aruandegrupp** juhtelemente.

<table>
<thead>
<tr>
<th>Juhtelement</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ettevõtte, üksikasjade ja kuupäeva sätete tühistamine individuaalsetest aruande definitsioonidest</td>
<td>Märkige see ruut selle aruandegrupi aruannete individuaalsete aruande definitsioonide tühistamiseks ainult nende aruannete loomise puhul.</td>
</tr>
<tr>
<td>Ettevõtte nimi</td>
<td>Aruannete puhul kasutatava ettevõtte valimine.</td>
</tr>
<tr>
<td>Üksikasjatase</td>
<td>Määrake aruannete üksikasjatase.
<ul>
<li><strong>Finantsid</strong> – kõrgetasemeline kokkuvõttev aruanne. Te ei saa kontodes ja dimensioonides süvitsi minna, välja arvatud aruandluspuu kaudu lisatud kontode ning dimensioonide puhul.</li>
<li><strong>Rahaline &amp; Konto</strong> − aruanne, mis sisaldab kõrgetasemelist kokkuvõtet ja konto üksikasju.</li>
<li><strong>Rahaline, Konto &amp; Kanne</strong> − aruanne, mis sisaldab kõrgetasemelist kokkuvõtet ja kande üksikasju..</li>
</ul></td>
</tr>
<tr>
<td>Tinglik</td>
<td>Määrake aruannete tegevuste tüübid.
<ul>
<li><strong>Ainult sisestatud toiming</strong> – kaasake ainult finantsandmetes sisestatud kanded ja saldod.</li>
<li><strong>Sisestatud ja sisestamata toiming</strong> – kaasake kõik finantsandmetesse sisestatud ja saadetud kanded ja saldod.</li>
<li><strong>Ainult sisestamata toiming</strong> – kaasake ainult finantsandmetesse sisestatud, kuid veel saatmata kanded.</li>
</ul></td>
</tr>
<tr>
<td>Kõigi aruandlusvaluutade kaasamine</td>
<td>Kui teie Microsoft Dynamicsi ERP-süsteemis on konfigureeritud täiendavaid aruandlusvaluutasid, loetletakse need siin. Märkige see ruut lisaaruannete koostamiseks näidatud valuutades. Aruannete vaatamiseks veebivaaturis klõpsake nuppu <strong>Valuuta</strong> ja valige valuuta.</td>
</tr>
<tr>
<td>Aruande definitsiooni ei salvestatud kuupäevateavet</td>
<td><ul>
<li>Baasperiood</li>
<li>Baasaasta</li>
<li>Ajavahemik</li>
</ul>
Aruande definitsiooni salvestatakse ainult baasperioodi vaikesätted.</td>
</tr>
<tr>
<td>Aruande definitsiooni salvestati kuupäevateave</td>
<td><ul>
<li>Aruande kuupäev</li>
<li>Vaikimisi baasperiood</li>
</ul></td>
</tr>
<tr>
<td>Rühma aruanded</td>
<td>Aruandegrupi aruannete lisamine, eemaldamine ja ümberkorraldamine.
<ul>
<li>Aruandedefinitsioonide lisamiseks aruanderühma topeltklõpsake aruanderühma, et see avada, ning klõpsake seejärel suvandit <strong>Lisa</strong>. Valige aruanderühma kaasatavad aruanded ning klõpsake seejärel <strong>OK</strong>.</li>
<li>Aruande eemaldamiseks aruanderühmast valige see ja klõpsake seejärel käsku <strong>Eemalda</strong>.</li>
<li>Aruannete loomise järjestuse muutmiseks valige loendist aruanne ja seejärel klõpsake valikut <strong>Liigu üles</strong> või <strong>Liigu alla</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Lisaressursid

[Finantsaruandlus](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]