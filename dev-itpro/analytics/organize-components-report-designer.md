---
title: Aruande komponentide korraldamine aruandekoosturis
description: "Kui olete koosteüksused kujundanud ja aruanded koostanud, on abiks nende objektide korraldamine, et kasutajatel oleks neid hõlpsam leida. Selles artiklis kirjeldatakse olemasolevate aruannete,koosteüksuste ja objektide korraldamist aruandekoosturis."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter, Core
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ca6d02d41be67447719819e27fbcf3f615eced63
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="organize-report-components-in-report-designer"></a>Aruande komponentide korraldamine aruandekoosturis

[!include[banner](../includes/banner.md)]


Kui olete koosteüksused kujundanud ja aruanded koostanud, on abiks nende objektide korraldamine, et kasutajatel oleks neid hõlpsam leida. Selles artiklis kirjeldatakse olemasolevate aruannete,koosteüksuste ja objektide korraldamist aruandekoosturis.

Failide korraldamiseks saate aruandekoosturis kaustu, aruandeid, koosteüksusi ja muid objekte ümber nimetada. Ümbernimetatava objekti tüübist olenevalt võib teil olla vaja selle objekti seoseid värskendada.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Aruande kujundaja kausta või koosteüksuse ümbernimetamine
Saate aruande kujundajas ümber nimetada kaustu, aruande definitsioone, readefinitsioone, veerudefinitsioone ja aruandluspuu definitsioone. **Märkus.** Koosteüksuse ümbernimetamisel peate värskendama aruandluse definitsioone, mis seda koosteüksust kasutavad. Vastasel korral ei saa aruannet koostada.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Aruande kujundaja kausta või koosteüksuse ümbernimetamine

1.  Kasutage aruande kujundajas ümbernimetatava kausta või objekti leidmiseks navigeerimispaani.
2.  Paremklõpsake kausta või objekti ja seejärel klõpsake suvandit **Nimeta ümber**. Navigeerimispaani väli **Nimi** muutub aktiivseks.
3.  Sisestage uus nimi ja seejärel vajutage suvandit Sisesta.
4.  Kui koosteüksus on readefinitsioon, veeru definitsioon või aruandluspuu definitsioon, peate värskendama teisi sellega seotud koosteüksusi. Paremklõpsake 3. etapis ümbernimetatud koosteüksust, valige **Seosed** ja seejärel valige element loendist selle värskendamiseks.
5.  Korrake 4. etappi, kuni kõik seotud elemendid on värskendatud.

## <a name="create-and-manage-report-groups"></a>Aruandegruppide loomine ja haldamine
Saate grupeerida aruande definitsioone korraga mitme aruande loomiseks. Aruandegruppide loomiseks, muutmiseks ja kustutamiseks peab teil olema kujundaja või administraatori roll. Looja rolliga kasutajad saavad aruandegruppe luua ja ka aruandegruppide kasutaja aruande definitsiooni seadistust muuta.

### <a name="create-a-report-group"></a>Aruandegrupi loomine

1.  Klõpsake aruandekoosturi navigeerimispaanil valikut **Aruandegrupid**.
2.  Klõpsake menüüs **Fail** valikuid **Uus** &gt; **Aruandegrupi definitsioon** uue aruandegrupi avamiseks vaaturi aknas. Teine võimalus on klõpsata tööriistaribal nuppu **Aruandegrupp** ![Aruandegrupp](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Aruandegrupp").
3.  Klõpsake vahekaarti **Aruandegrupp**. Individuaalsete aruande definitsioonide teabe tühistamiseks selle aruande loomise puhul valige märkeruut **Ettevõtte, üksikasjade ja kuupäeva sätete tühistamine individuaalsetest aruande definitsioonidest**. Ettevõtte nime, üksikasjataseme, tinglikkuse seadistuse ja kuupäeva teave sisestatakse automaatselt, kuid saate endiselt värskendusi teha.
4.  Mitme arvestusvaluutasid näitava aruande koostamiseks märkige ruut **Kaasa kõik aruandlusvaluutad**. Seejärel pääsete mitmesse vaatesse, klõpsates aruande vaatamisel veebivaaturis nuppu **Valuuta**.
5.  Aruandegruppi kaasatavate aruannete valimiseks klõpsake väljal **Grupi aruanded** valikut **Lisa**. Mitme aruande valimiseks dialoogiboksis **Lisa** hoidke aruannete valimisel all klahvi Ctrl. Kui olete aruannete valimise lõpetanud, klõpsake **OK**.
6.  Uue aruandegrupi salvestamiseks klõpsake **Fail** &gt; **Salvesta**.

### <a name="modify-a-report-group"></a>Aruandegrupi muutmine

1.  Klõpsake aruandekoosturi navigeerimispaanil valikut **Aruandegrupid**.
2.  Aruandegrupi muutmiseks topeltklõpsake.
3.  Tehke vahekaardil **Aruandegrupp** soovitud muudatused.
4.  Klõpsake menüüs **Fail** käsku **Salvesta** muudetud aruandegrupi salvestamiseks. Teine võimalus on klõpsata tööriistaribal nuppu **Salvesta** ![Salvesta](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Salvesta").

**Märkus.** Kui olete plaaninud aruanded määratud vahemikel koostamiseks, saate need sätted tühistada ja aruande kohe luua.

### <a name="generate-a-report-group-report"></a>Aruandegrupi aruande loomine

1.  Klõpsake aruandekoosturi navigeerimispaanil valikut **Aruandegrupid**.
2.  Avage loodav aruandegrupp.
3.  Klõpsake aruannete loomiseks nuppu **Loo aruanne** ![Loo aruanne](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Loo aruanne").

### <a name="delete-a-report-group"></a>Aruandegrupi kustutamine

1.  Klõpsake aruandekoosturi navigeerimispaanil valikut **Aruandegrupid**.
2.  Paremklõpsake kustutamiseks aruandegruppi ja seejärel tehke valik **Kustuta**.
3.  Kui kuvatakse kinnitusteade, klõpsake valikut **Jah**.

## <a name="report-group-tab-controls"></a>Vahekaardi Aruandegrupp juhtelemendid
Järgmises tabelis kirjeldatakse vahekaardi **Aruandegrupp** juhtelemente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Juhtelement</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ettevõtte, üksikasjade ja kuupäeva sätete tühistamine individuaalsetest aruande definitsioonidest</td>
<td>Märkige see ruut selle aruandegrupi aruannete individuaalsete aruande definitsioonide tühistamiseks ainult nende aruannete loomise puhul.</td>
</tr>
<tr class="even">
<td>Ettevõtte nimi</td>
<td>Aruannete puhul kasutatava ettevõtte valimine.</td>
</tr>
<tr class="odd">
<td>Üksikasjatase</td>
<td>Määrake aruannete üksikasjatase.
<ul>
<li><strong>Rahaline</strong>− kõrgetasemeline koondaruanne. Te ei saa kontodes ja dimensioonides süvitsi minna, välja arvatud aruandluspuu kaudu lisatud kontode ja dimensioonide puhul.</li>
<li><strong>Rahaline &amp; Konto</strong> − aruanne, mis sisaldab kõrgetasemelist kokkuvõtet ja konto üksikasju.</li>
<li><strong>Rahaline, Konto &amp; Kanne</strong> − aruanne, mis sisaldab kõrgetasemelist kokkuvõtet ja kande üksikasju..</li>
</ul></td>
</tr>
<tr class="even">
<td>Tinglik</td>
<td>Määrake aruannete tegevuste tüübid.
<ul>
<li><strong>Ainult sisestatud tegevus</strong> − sisaldavad ainult teie finantsandmetesse kirjendatud kandeid ja saldosid.</li>
<li><strong>Sisestatud ja sisestamata tegevus</strong> − sisaldavad kõiki teie finantsandmetesse sisestatud ja kirjendatud kandeid ja saldosid.</li>
<li><strong>Ainult sisestamata tegevus</strong> − sisaldavad ainult teie finantsandmetesse sisestatud, kuid veel kirjendamata kandeid ja saldosid.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kõigi aruandlusvaluutade kaasamine</td>
<td>Kui teie Microsoft Dynamics ERP süsteemis on konfigureeritud täiendavaid aruandlusvaluutasid, loetletakse need siin. Märkige see ruut lisaaruannete koostamiseks näidatud valuutades. Nende aruannete kuvamiseks veebivaaturis klõpsake nuppu <strong>Valuuta</strong> ja valige siis valuuta.</td>
</tr>
<tr class="even">
<td>Aruande definitsiooni ei salvestatud kuupäevateavet</td>
<td><ul>
<li>Baasperiood</li>
<li>Baasaasta</li>
<li>Ajavahemik</li>
</ul>
Aruande definitsiooni salvestatakse ainult baasperioodi vaikesätted.</td>
</tr>
<tr class="odd">
<td>Aruande definitsiooni salvestati kuupäevateave</td>
<td><ul>
<li>Aruande kuupäev</li>
<li>Vaikimisi baasperiood</li>
</ul></td>
</tr>
<tr class="even">
<td>Rühma aruanded</td>
<td>Aruandegrupi aruannete lisamine, eemaldamine ja ümberkorraldamine.
<ul>
<li>Aruande definitsioonide lisamiseks aruandegruppi topeltklõpsake aruandegruppi selle avamiseks ja seejärel klõpsake suvandit <strong>Lisa</strong>. Valige aruandegruppi kaasatavad aruanded ja seejärel klõpsake nuppu <strong>OK</strong>.</li>
<li>Aruande eemaldamiseks aruandegrupist valige see ja seejärel klõpsake suvandit <strong>Eemalda</strong>.</li>
<li>Aruannete loomise järjestuse muutmiseks valige loendist aruanne ja seejärel klõpsake valikut <strong>Liigu üles</strong> või <strong>Liigu alla</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Vt ka
--------

[Finantsaruandlus](financial-reporting-intro.md)




