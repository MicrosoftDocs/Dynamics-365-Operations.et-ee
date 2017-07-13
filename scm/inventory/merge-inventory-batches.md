---
title: "Varupartiide ühendamine"
description: "Selles artiklis kirjeldatakse kahe või enama varude partii konsolideerimist ühendatud partiisse."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventBatchJournalListPage, InventBatchJournalMerge
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 39782
ms.assetid: 07c5e98b-10fd-4f5c-b471-41d2150f47b0
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: aec97976ef6a2b4c66118289f7f76b14351456f8
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017


---

# <a name="merge-inventory-batches"></a>Varupartiide ühendamine

[!include[banner](../includes/banner.md)]


Selles artiklis kirjeldatakse kahe või enama varude partii konsolideerimist ühendatud partiisse. 

Partiide ühendamisel aitavad arvutused optimeerida ühendatud partii tunnuseid ja partiiatribuute. Kui lähtepartiid on valitud, saab ühendatud partiid enne sisestamist üle vaadata ja muuta. Partii ühendamise saab kinnitamiseks ka varude töölehele edastada. Seejärel saab varud sellelt varude töölehelt otse reserveerida või sisestada. Ühendatud partii sisestamisel korrigeeritakse varud lähtepartiidele ja ühendatud partiile.

## <a name="are-there-any-prerequisites"></a>Kas selleks on eeltingimusi?
Jah, enne kui saate ühendatud partii tööriistu kasutada, peate seadistama paar asja. Eeltingimusi kirjeldatakse järgmises tabelis.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lehekülg</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Töölehe nimed, ladu</td>
<td>Peate looma töölehe nime, mida kasutatakse vaikimisi partiide ühendamiste sisestamisel varude töölehtedele. Valikuline, kuid kohustuslik: saate määrata, et reserveerimised tuleb teha automaatselt, kui partii ühendamine edastatakse varude töölehele. Vastasel juhul on oht, et vabad kaubavarud muutuvad pärast ühendatud partii üksikasjade seadistamist ja töölehe sisestamist. Töölehe nime puhul automaatsete reserveerimiste lubamiseks valige <strong>Automaatne</strong> väljalt <strong><strong>Reserveerimine</strong></strong>.</td>
</tr>
<tr class="even">
<td>Varude ja laohalduse parameetrid</td>
<td>Varude töölehele peate määrama vaikenime.</td>
</tr>
<tr class="odd">
<td>Väljastatud tooted</td>
<td>Siin on kauba soovitatavad sätted.
<ul>
<li>Ühendatud partiide jaoks automaatselt partiinumbrite loomiseks peate partii numbrigrupile määrama vabastatud toote. Ühendatud partii loomiseks saate partiinumbri ka käsitsi sisestada või valida olemasoleva partiinumbri. Olemasoleva partiinumbri valimisel veenduge, et valitud partii ei kuulu ühtegi laokandesse.</li>
<li>Kui kasutate väljastatud toote kõlblikkusaega või parim enne kuupäeva, arvutatakse ühendatud partii kuupäevad väljal <strong>Partii ühendamise kuupäeva arvutamine</strong> tehtud valiku põhjal. Valikud on järgmised:
<ul>
<li><strong>Varaseim</strong> – arvutus põhineb partiide ühendamise jaoks valitud lähtepartiile määratud varaseimal kuupäeval.</li>
<li><strong>Hiliseim</strong> – arvutus põhineb partiide ühendamise jaoks valitud lähtepartiile määratud hiliseimal kuupäeval.</li>
<li><strong>Käsitsi</strong> – arvutamist ei toimu. Kui kuupäev on kõigil lähtepartiidel sama, siis kuupäeva soovitatakse. Seda kuupäeva saate muuta. Kui kuupäev pole lähtepartiidel sama, saate kuupäeva käsitsi sisestada.</li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td>Partiinumbrigrupp</td>
<td>Valikuline: ühendatud partii loomisel partiinumbri loomiseks, peate määrama vabastatud tootele partii numbrigrupi. Muul juhul saate partiinumbri käsitsi sisestada.</td>
</tr>
</tbody>
</table>

## <a name="when-might-i-want-to-merge-batches-of-inventory"></a>Millal tuleks varude partiid ühendada?
Siin on mõned näited stsenaariumidest, mille korral partiide ühendamine võib kasulikuks osutuda.

-   Laos ringi käies märkab Sammy, et seal on mitu sama kauba partiid, millel on väikesed kogused. Ta ootab mitut uut saadetist ja mõistab, et järelejäänud koguste ühendamisega uude partiisse saab ta põrandaruumi vabastada.
-   Sammy võtab varud vastu ja soovib uue partii ühendada juba vastuvõetud partiiga, et tõsta olemasoleva partii partiiatribuudi väärtust.

## <a name="can-i-merge-batches-across-sites-and-legal-entities"></a>Kas partiisid saab ühendada üle saitide ja juriidiliste isikute?
Ei, saate ühendada ainult neid partiisid, millel on samad laoala ja lao dimensioonid ühes juriidilises isikus. Siiski saab ühendatud partii jaoks määrata muu asukoha ja kaubaaluse ID.

## <a name="can-i-merge-partial-quantities"></a>Kas saan ühendada osalisi koguseid?
Ei, saate ühendada ainult partiide tervikkoguseid. Partii ühendamise funktsioon on mõeldud varude funktsioonina, mitte tootmisfunktsioonina.

## <a name="what-if-the-batches-have-different-batch-attribute-values"></a>Mis juhtub, kui partiidel on erinevad partiiatribuudi väärtused?
Ühendatud partii loomiseks lähtepartiide valimisel kontrollib Finance and Operations, kas kõigil partiidel on omadused või atribuudiväärtused. Kui atribuudi väärtus on sama, soovitatakse ühendatud partiile väärtust. Seda väärtust saate muuta. Mittekattuvad atribuudiväärtused jäetakse ühendatud partii puhul tühjaks ja saate need väärtused käsitsi sisestada. Kui atribuudiväärtuse partiiatribuudi tüüp on täisarv või murdarv ning väärtused pole kõigi lähtepartiide puhul samad, arvutatakse väärtus kaalutud keskmise alusel. Arvutatud väärtus ümardatakse üles või alla lähima täisarvuni. Kui lähtepartii puhul väärtus puudub, siis partiid ja selle kogust arvutusse ei kaasata. **Näide** Järgmine näide kujutab ühendatud partii kaalutud keskmise arvutamist. Kahe lähtepartii partiiatribuudi tüübil, mis on täisarv, on tühi väärtus. Lähtepartiidele määratakse järgmine atribuut.

| Atribuut | Miinimum | Suurenemine | Maksimum |
|-----------|---------|-----------|---------|
| Tase     | 3       | 3         | 30      |

Lähtepartiidel on atribuudi **Taseme partii** puhul järgmised atribuudiväärtused.

| Pakktöötlus | Kogus | Atribuut | Atribuudi väärtus |
|-------|----------|-----------|-----------------|
| B1    | 10       | Tase     | Tühi           |
| B2    | 15       | Tase     | 15              |
| B3    | 20       | Tase     | 20              |
| B4    | 25       | Tase     | Tühi           |
| B5    | 30       | Tase     | 25              |

Kui lisate need partiid lähtepartiidena, määratakse ühendatud partiile järgmised väärtused.

| Pakktöötlus | Kogus | Atribuut | Atribuudi väärtus |
|-------|----------|-----------|-----------------|
| B6    | 100      | Tase     | 21              |

Partiide B1 ja B4 väärtusi ja koguseid ei kaasata kaalutud keskmise arvutamisse. Seetõttu arvutatakse ühendatud partii väärtus järgmiselt.

| Väärtus | Kogus (kaal)                              | Osakaal | Osakaal × väärtus                                               |
|-------|------------------------------------------------|-----------------|-----------------------------------------------------------------------|
| 15    | 15                                             | 0,230769231     | 3,461538462                                                           |
| 20    | 20                                             | 0,307692308     | 6,153846154                                                           |
| 25    | 30                                             | 0,461538462     | 11,53846154                                                           |
|       | **Kokku:** 65, mis on osakaalude summa |                 | **Kokku:** 21,5384615, mis ümardatakse väärtuseks 21 (lähim aste) |

## <a name="what-if-the-batches-have-different-batch-dates"></a>Mis juhtub, kui partiidel on erinevad partiikuupäevad?
Kui partiide kuupäevad on erinevad, arvutatakse mõned neist kuupäevadest grupi **Partii kuupäevad** põhjal kiirkaardil **Ühendatud partii** lehel **Partii ühendamine**. Süsteem arvutab grupi **Partii kuupäevad** väljade väärtused. Väärtused hõlmavad tootmiskuupäeva, aegumiskuupäeva, säilivusaviisi kuupäeva ja parim-enne kuupäeva. Kuupäevad arvutatakse kauba sätete põhjal väljagrupis **Kauba andmed** lehel **Väljastatud toote üksikasjad**. Saate neid väärtusi muuta või need käsitsi sisestada. Kõigi muude kuupäevade puhul arvutusi ei tehta. Sama põhimõtet kasutatakse partii atribuudiväärtuste puhul. Kui kuupäev on kõigi lähtepartiide puhul sama, siis soovitatakse seda kuupäeva ühendatud partii puhul. Kui kuupäev ei ole kõigi lähtepartiide puhul sama, jääb ühendatud partii puhul kuupäevaväli tühjaks ja saate selle käsitsi sisestada.

## <a name="what-if-the-dimensions-are-different-on-the-batches-that-i-want-to-merge"></a>Mis juhtub, kui ühendatavate partiide dimensioonid on erinevad?
Tootedimensioone, jälgimisdimensioone ja laoala dimensioone käsitletakse järgmiselt.

-   **Tootedimensioonid** – kõik valitud kauba tootedimensioonid peavad olema samad. Partiisid ei saa tootedimensioonide lõikes ühendada.
-   **Jälgimisdimensioonid** – uus partiinumber luuakse automaatselt, kui kauba jaoks on määratud partii numbrigrupp. Kui kaubale pole partii numbrigruppi määratud, saate valige olemasoleva partii või numbri käsitsi sisestada. Seerianumbrid edastatakse lähtepartiist ühendatud partii varude tööleheridadele.
-   **Laoala dimensioonid** – tegevuskoha ja lao laoala dimensioonid peavad olema kõigi lähtepartiide ja ühendatud partii puhul samad. Siiski saate ühendatud partii jaoks määrata uue asukoha ja kaubaaluse ID.

## <a name="how-does-posting-work"></a>Kuidas toimub sisestamine?
Sisestamine toimub kahel viisil olenevalt sellest, kas kasutate töölehtede jaoks kinnitusprotsessi või mitte. Ühendatud partii saate toimingute **Kanna töölehele** ja **Sisesta partii ühendamine** abil üle kanda töölehele, kus saate selle kinnitada ja sisestada, kuid võite ühendatud partii ka otse sisestada. Peamine erinevus nende kahe tegevuse vahel on see, et ülekandmine töölehele ei sisesta partii ühendamist. Mõlemad tegevused loovad uue partii, kui olemasolevat partiid pole valitud, värskendavad kõiki partii üksikasju ja atribuudiväärtusi ning loovad varude töölehe.

-   **Kanna töölehele** – partiide ühendamise üksikasjad kantakse uuele varude töölehele. Kui olete seadistanud automaatsed reserveeringuid, reserveeritakse kogused lähtepartiides. Partii ühendamise üksikasju ei saa muuta. Partii ühendamise muutmiseks peate töölehe kustutama. Töölehte saab kasutada ülesandena, mille teine töötaja peab hiljem täitma. Partii koguse reserveerimine töölehe reale on kinnitatud. See eraldamine võimaldab kvaliteediplaanijal või laojuhatajal oma töötajatele ülesandeid luua.
-   **Sisesta partii ühendamine** – sisestab partiide ühendamise otse. Selle toimingu saab teha pärast füüsilise ühendamise toimumist.

Varude töölehe saate partiide ühendamiseks kinnitada loendilehelt **Kõik partii ühendamised**. Klõpsake valikuid **Tööleht** &gt; **Sisesta**. Kui tööleht on sisestatud, ei saa ühendatud partii üksikasju muuta. Pärast ühendatud partii ülekandmist varude töölehele saate muuta üksikasju ainult töölehe kustutamisel.

## <a name="after-i-merged-a-catchweight-item-why-cant-i-see-the-catchweight-information-in-the-inventory-journal"></a>Miks ma ei näe pärast tegeliku kaaluga kauba ühendamist tegeliku kaalu teavet varude töölehel?
Tegeliku kaaluga kaupade partiisid saate ühendada samamoodi kui kõiki teisi kaupu. Kuid tegeliku kaalu teavet varude töölehel ei kuvata. Soovitame teil enne ühendatud partii ülekandmist varude töölehele tegeliku kaalu teavet kontrollida.




