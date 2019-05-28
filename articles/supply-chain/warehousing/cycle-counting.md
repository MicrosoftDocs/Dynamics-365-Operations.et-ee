---
title: Tsükliline inventuur
description: See artikkel kirjeldab, kuidas kasutada tsüklilist inventuuri laohalduse moodulis oleva ladustamislahendusega. See artikkel ei kehti moodulis Varude haldus oleva ladustamislahenduse puhul.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a76082a7aa375424e6f118744e2f63600a8cbda
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560653"
---
# <a name="cycle-counting"></a>Tsükliline inventuur

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas kasutada tsüklilist inventuuri laohalduse moodulis oleva ladustamislahendusega. See artikkel ei kehti moodulis Varude haldus oleva ladustamislahenduse puhul.

Tsükliline inventuur on laoprotsess, mida saate kaupade laovaru kontrollimiseks kasutada. Tsüklilise inventuuri protsessi saab kirjeldada kolme etapina.

1.  **Tsüklilise inventuuri töö loomine** – tsüklilise inventuuri töö saab luua automaatselt, tuginedes kaupade läveparameetritele või kasutades tsüklilise inventuuri plaani. Teine võimalus on luua tsüklilise inventuuri töö käsitsi, kasutades lehel **Tsüklilise inventuuri töö kauba alusel** või lehel **Tsüklilise inventuuri töö asukoha alusel** olevaid kauba või lao parameetrid.
2.  **Tsüklilise inventuuri töötlemine** – pärast tsüklilise inventuuri töö loomist saab teha tsüklilise inventuuri töö, loendades lao asukohas olevad kaubad ja sisestades tulemuse mobiilse seadme abil Microsoft Dynamics 365 for Finance and Operationsisse. Teise võimalusena saate lugeda kaupu lao asukohas, tsüklilise inventuuri tööd loomata. Seda protsessi nimetatakse *punkttsükliliseks inventuuriks*.
3.  **Tsüklilise inventuuri väärtuse erinevuse lahendamine** – pärast tsüklilist inventuuri on vormil **Kogu töö** kaupadel, mille inventuuri käigus saadud väärtuses on erinevusi, tööolek **Ülevaatuse ootel**. Need erinevused saab lahendada lehel **Ülevaatuse ootel tsüklilise inventuuri töö**.

Järgmine illustratsioon näitab tsüklilise inventuuri protsessi. ![Tsüklilise inventuuri protsessivoog](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a>Tsüklilise inventuuri eeltingimused
Järgmises tabelis kuvatakse eeltingimused, mis peavad olema olemas, enne kui saate tsüklilist inventuuri kasutada.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eeltingimus</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kaup</td>
<td>Kauba puhul peavad olema lubatud laohaldusprotsessid.</td>
</tr>
<tr class="even">
<td>Ladu</td>
<td>Laos peavad olema lubatud laohaldusprotsessid. Laohaldusprotsesside lubamiseks laos valige ladu lehelt <strong>Laod</strong> ja märkige seejärel valik <strong>Kasuta laohaldusprotsesse</strong>. Kui soovite, et töötajad saaksid tsüklilise inventuuri käigus aluseid teisaldada, märkige kiirkaardil <strong>Laohaldus</strong> ruut <strong>Luba kaubaaluse teisaldamine tsüklilises inventuuris</strong>.</td>
</tr>
<tr class="odd">
<td>Töökaustad</td>
<td>Valikuline: saate luua töökausta laotöö eraldamiseks töö (praegusel juhul tsüklilise inventuuri töö) tüübi alusel.</td>
</tr>
<tr class="even">
<td>Asukohad</td>
<td>Tsüklilise inventuuri lubamine asukohtades. Tsüklilise inventuuri lubamiseks lao asukoha puhul tehke lehel <strong>Asukohaprofiilid</strong> valik <strong>Luba tsükliline inventuur</strong>.</td>
</tr>
<tr class="odd">
<td>Laohalduse parameetrid</td>
<td>Tsüklilise inventuuri parameetrite häälestamine. Määrake tsüklilisele inventuurile lehel <strong>Laohalduse parameetrid</strong> vaikimisi korrigeerimistüübi kood, tööklassi ID ja töö prioriteet.</td>
</tr>
<tr class="even">
<td>Mobiilne seade</td>
<td><ul>
<li>Looge ühele järgmistest meetoditest menüü-üksus lehel <strong>Mobiilse seadme menüü-üksused</strong>.
<ul>
<li>Kasutaja juhitud tsükliline inventuur</li>
<li>Süsteemi juhitud tsükliline inventuur</li>
<li>Tsüklilise inventuuri rühmitamine</li>
<li>Punkttsükliline inventuur</li>
</ul>
</li>
<li>Menüü seadistamine mobiilsele seadmele.</li>
<li>Töö kasutajakonto loomine ja mobiilse seadme menüü määramine töö kasutaja ID-le.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Seostuv seadistustoiming</td>
<td>Tsüklilise inventuuri plaani seadistamine lao asukohale.</td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a>Automaatne tsüklilise inventuuri loomine
Korduvaks tsüklilise inventuuri töö loomiseks on kaks võimalust: seadistada tsüklilise inventuuri läved või seadistada tsüklilise inventuuri plaanid.

-   Tsüklilise inventuuri lävi näitab laokaupade koguse või protsendi piirangut. Tsüklilise inventuuri töö luuakse lävepiirini jõudmisel automaatselt.
-   Tsüklilise inventuuri plaan loob tsüklilise inventuuri töö kohe või perioodiliselt pakett-töö kaudu. Kui tsüklilise inventuuri töö on loodud, sisaldab inventuuri töö rida teavet inventuuri asukoha kohta. Selle asukohaga seostatud vaba kaubavaru on blokeeritud ja on seetõttu reserveerimise ning väljamineva töötluse isegi siis, kui on olemas avatud inventuuri töö.

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a>Tsüklilise inventuuri töö loomine kaupade läveparameetrite põhjal

Tsüklilise inventuuri töö saab luua, kui kaupade arv langeb asukohas alla konkreetse läveväärtuse. Näiteks on 60 kaupa asukohas, mille tsüklilise inventuuri läve kogus on 40. Müügitellimuse kande käigus komplekteeritakse asukohast 25 kaupa ja need paigutatakse vaheasukohta. Kuna uus kaupade arv 35 on lävekogusest väiksem, luuakse asukohas automaatselt tsüklilise inventuuri töö.

### <a name="schedule-cycle-counting-work"></a>Tsüklilise inventuuri töö plaanimine

Saate ajastada tsüklilise inventuuri plaane tsüklilise inventuuri töö loomiseks kohe või perioodiliselt. Tsüklilise inventuuri plaanide seadistamisega saate kontrollida töökausta, mille jaoks tsüklilise inventuuri töö luuakse, maksimaalset tsükliliste inventuuride arvu, mis kaupadele erinevates asukohtades luuakse, ja päevade arvu enne lao asukohas uue inventuuri läbiviimist. Näiteks on kaup laos saadaval kolmes asukohas ja maksimaalseks tsükliliste inventuuride arvuks on määratud **2**. Sellisel juhul luuakse tsüklilise inventuuri plaani käivitamisel kaks tsüklilist inventuuri kahes asukohas, kus kaup olemas on. Teine näide: määrate tsükliliste inventuuride vaheliseks päevade arvuks **5**. Sel juhul luuakse tsüklilise inventuuri töö iga viie päeva järel. Kuid kui tsüklilise inventuuri töö töödeldakse 3. päeval, luuakse järgmine tsüklilise inventuuri töö viis päeva pärast viimase tsüklilise inventuuri töö töötlemist, 8. päeval.

## <a name="create-cycle-counting-work-manually"></a>Tsüklilise inventuuri loomine käsitsi
Tsüklilise inventuuri töö loomiseks käsitsi võite kasutada lehte **Tsükliline inventuur kauba alusel** või **Tsükliline inventuur asukoha alusel**. Saate määrata loodavate tsükliliste inventuuride maksimumarvu. Näiteks kui laojuhataja määrab väärtuse **5**, luuakse tsüklilise inventuuri töö viiele asukohale, isegi kui kaup on 10-s asukohas olemas. Saate valida ka töökausta ID, kuhu loodavate tsüklilise inventuuri tööde ID-d määratakse. Töökausta ID töötlemisel tsüklilise inventuuri jaoks töödeldakse sellesse töökausta määratud tsüklilise inventuuri tööde ID-d grupina.

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a>Tsüklilise inventuuri läbiviimine mobiilse seadmega
Tsüklilise inventuuri töö tegemiseks mobiilses seadmes on Finance and Operationsis mitu võimalust.

-   **Kasutaja juhitud** – töötaja saab määrata tsüklilise inventuuri töö ID, mille olek on **Avatud**.
-   **Süsteemi juhitud** – Finance and Operations määrab töötajale tsüklilise inventuuri töö ID.
-   **Tsüklilise inventuuri rühmitamine** – töötaja saab rühmitada teatud asukoha, tsooni või töökausta tsüklilise inventuuri töö ID-d.
-   **Punkttsükliline inventuur** – valikuline: töötaja saab loendada kaupu lao asukohas igal ajal, tsüklilise inventuuri tööd loomata, sisestades asukoha ID. Punkttsüklilise inventuuri läbiviimiseks asukohas sisestab töötaja asukoha ID.

Järgmine näide illustreerib, kuidas saate mobiilse seadme abil punkttsüklilist inventuuri teha. Juhised, mida töötaja seadmel näeb, erinevad, olenevalt punkttsüklilise inventuuri menüü-üksuse seadistusest.

1.  Valige mobiilsel seadmel menüüelement punkttsüklilise inventuuri töö töötlemiseks.
2.  Registreerige asukoht, millele punkttsüklilist inventuuri teha.
3.  Registreerige ja kinnitage kaubakood ja loendatud kaupade kogus. **Märkus:** tsüklilise inventuuri olekuks määratakse **Ülevaatuse ootel** või **Suletud** lehel **Kogu töö**,olenevalt lehel **Töötaja** määratud parameetritest.
4.  Valikuline: korrake 3. sammu asukoha ülejäänud kaupade puhul ja kinnitage, et pole rohkem loendatavaid kaupu.

## <a name="resolve-cycle-counting-differences"></a>Tsüklilise inventuuri erinevuste lahendamine
Tsüklilise inventuuri erinevus ilmneb järgmistes stsenaariumides, kui valiku **On tsüklilise inventuuri ülevaataja** väärtuseks on töö kasutaja ID puhul määratud **Ei**.

-   Loendatud väärtus jääb lehe **Töö kasutajad** väljadel **Maksimaalne protsendi piirang** või **Maksimaalse koguse piirang** määratletud hälbepiiridest välja. Näiteks on asukohas vaba kaubavaru kogus 50 ja töö kasutaja hälbepiir on 10. Kui töö kasutaja sisestab väärtuse, mis ei ole vahemikus 40–60, tekib erinevus.
-   Tsüklilise inventuuri väärtus erineb vaba kaubavaru kogusest ja kindlaid hälbepiire pole määratud.

Saate korrigeerida loendatud väärtuse erinevusi ja kinnitada siis loendatud väärtuse lehel **Ülevaatuse ootel tsükliline inventuur**. Kauba muudetud kogust saab kontrollida lehel **Vaba varu asukoha järgi**. Loendatud väärtus lükatakse tagasi, kui erinevust ei saa kinnitada.

## <a name="additional-resources"></a>Lisaressursid
[Mobiilsete seadmete konfigureerimine lao töö jaoks](configure-mobile-devices-warehouse.md)



