---
title: Aruande komponentide korraldamine aruandekoosturis
description: Selles artiklis kirjeldatakse olemasolevate aruannete,koosteüksuste ja objektide korraldamist aruandekoosturis.
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a94a88114072792243026e441e6c5a62ee80fc56
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802684"
---
# <a name="organize-report-components-in-report-designer"></a>Aruande komponentide korraldamine aruandekoosturis

[!include [banner](../includes/banner.md)]

Kui olete koosteüksused kujundanud ja aruanded koostanud, on abiks nende objektide korraldamine, et kasutajatel oleks neid hõlpsam leida. Selles artiklis kirjeldatakse olemasolevate aruannete,koosteüksuste ja objektide korraldamist aruandekoosturis.

Saate failide korraldamiseks kaustu, aruandeid, koosteüksuseid ja muid aruandekujundaja objekte ümber nimetada. Ümbernimetatava objekti tüübist olenevalt võib teil olla vaja selle objekti seoseid värskendada.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Kausta ümbernimetamine või blokki loomine aruandekujundajas
Aruandekujundajas saate kaustu, aruandedefinitsioone, readefinitsioone, veerudefinitsioone ja aruandluspuu määratlusi ümber nimetada.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Kausta ümbernimetamine või blokki loomine aruandekujundajas

1. Aruandekujundajas kasutage navigeerimispaani kausta või objekti leidmiseks, mida ümber nimetada.
2. Paremklõpsake kausta või objekti ja seejärel klõpsake suvandit **Nimeta ümber**. Navigeerimispaani väli **Nimi** muutub aktiivseks.
3. Sisestage uus nimi ja seejärel vajutage suvandit **Sisesta**.
4. Kui koosteüksus on readefinitsioon, veeru definitsioon või aruandluspuu definitsioon, peate värskendama teisi sellega seotud koosteüksusi. Paremklõpsake 3. etapis ümbernimetatud koosteüksust, valige **Seosed** ja seejärel valige element loendist selle värskendamiseks.
5. Korrake 4. etappi, kuni kõik seotud elemendid on värskendatud.

## <a name="create-and-manage-report-groups"></a>Aruandegruppide loomine ja haldamine
Saate grupeerida aruande definitsioone korraga mitme aruande loomiseks. Aruandegruppide loomiseks, muutmiseks ja kustutamiseks peab teil olema kujundaja või administraatori roll. Looja rolliga kasutajad saavad aruandegruppe luua ja ka aruandegruppide kasutaja aruande definitsiooni seadistust muuta.

### <a name="create-a-report-group"></a>Aruandegrupi loomine

1. Klõpsake navigeerimispaanil aruandekujundajas nuppu **Aruandegrupid**.
2. Klõpsake menüü **Fail** käsku Uus **aruandegrupi** &gt; **definitsioon,** et avada vaaturi aknas uus aruandegrupp. Teise võimalusena klõpsake aruandegrupi **nuppu** Aruandegrupp ![.](media/report-group.gif "Aruanderühm") tööriistaribal.
3. Klõpsake vahekaardil **Aruandegrupp** . Selle aruande loomiseks üksikute aruandedefinitsioonide teabe alistamiseks märkige ruut Alista ettevõte, **üksikasjad ja kuupäevasätted üksikutest aruandemääratlustest** . Ettevõtte nime, üksikasjataseme, tinglikkuse seadistuse ja kuupäeva teave sisestatakse automaatselt, kuid saate endiselt värskendusi teha.
4. Mitme aruande loomiseks, mis kuvavad aruandlusvaluutasid, märkige ruut **Kaasa kõik aruandlusvaluutad** . Seejärel pääsete mitmesse vaatesse, klõpsates aruande vaatamisel veebivaaturis nuppu **Valuuta**.
5. Aruandegruppi kaasatavate aruannete valimiseks klõpsake väljal **Grupi aruanded** valikut **Lisa**. Mitme aruande valimiseks dialoogiboksis **Lisa** hoidke aruannete valimisel all klahvi Ctrl. Kui olete aruannete valimise lõpetanud, klõpsake **OK**.
6. Uue aruandegrupi salvestamiseks klõpsake **Fail** &gt; **Salvesta**.

### <a name="modify-a-report-group"></a>Aruandegrupi muutmine

1. Klõpsake navigeerimispaanil aruandekujundajas nuppu **Aruandegrupid**.
2. Aruandegrupi muutmiseks topeltklõpsake.
3.  **Tehke vahekaardil** Aruandegrupp soovitud muudatused.
4. Klõpsake menüüs **Fail** käsku **Salvesta** muudetud aruandegrupi salvestamiseks, Teine võimalus on klõpsata tööriistaribal nuppu **Salvesta** ![Salvesta.](media/save.gif "Salvesta") tööriistaribal.

> [NOTE] Kui olete aruandeid planeerinud nii, et need luuakse määratud ajavahemike järel, saate need sätted alistada ja luua kohe aruande.

### <a name="generate-a-report-group-report"></a>Aruandegrupi aruande loomine

1. Klõpsake navigeerimispaanil aruandekujundajas nuppu **Aruandegrupid**.
2. Avage loodav aruandegrupp.
3. Klõpsake aruande **loomise nuppu**  ![Aruande loomine.](media/generate-report.gif "Aruande loomine") aruannete loomiseks.

### <a name="delete-a-report-group"></a>Aruandegrupi kustutamine

1. Klõpsake navigeerimispaanil aruandekujundajas nuppu **Aruandegrupid**.
2. Paremklõpsake kustutamiseks aruandegruppi ja seejärel tehke valik **Kustuta**.
3. Kui kuvatakse kinnitusteade, klõpsake valikut **Jah**.

## <a name="report-group-tab-controls"></a>Aruandegrupi vahekaardi juhtelemendid
Järgmises tabelis kirjeldatakse vahekaardi Aruandegrupp **juhtelemente** .

<table>
<thead>
<tr>
<th>Juhtklahv CTRL</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr>
<td>Alista individuaalsetest aruande määratlustest ettevõtte, üksikasjade ja kuupäeva sätted</td>
<td>Märkige see ruut, et alistada selles aruandegrupis üksikud aruandedefinitsioonid ainult nende aruannete loomiseks.</td>
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
<td>Kõik täiendavad aruandlusvaluutad, mis on konfigureeritud teie Microsoft Dynamics 365 Finantssüsteemis, on loetletud siin. Märkige see ruut, et luua näidatud valuutades täiendavad aruanded. Aruannete vaatamiseks veebivaaturis klõpsake nuppu <strong>Valuuta</strong> ja valige valuuta.</td>
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
