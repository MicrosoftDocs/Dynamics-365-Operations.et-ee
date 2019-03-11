---
title: Koosluse koostaja funktsioon
description: Selles teemas kirjeldatakse seda, kuidas kasutada koosluse koostaja lehte koosluste puhul puustruktuuridega kujundamiseks ja töötamiseks.
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesigner
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3bae68c9daf7aaaee1802e1def64d04ccea01b8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "338149"
---
# <a name="bom-designer-functionality"></a>Koosluse koostaja funktsioon

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse seda, kuidas kasutada koosluse koostaja lehte koosluste puhul puustruktuuridega kujundamiseks ja töötamiseks. Klõpsake nuppu Seadistus erinevate konfiguratsioonide valimiseks ja määramaks, milline teave puu ridadel ilmub.

Kui avate lehe **Koosluse koostaja** lehe **Väljastatud tooted** kaudu, kuvatakse valitud kauba jaoks aktiivsed ja kinnitatud koosluste hierarhia, kauba vaiketellimisleht ning tegelik kuupäev.  

Klõpsake suvandit **Filtreeri** vaate algse valiku muutmiseks. Seadistades kuvamispõhimõtteks **Valitud/aktiivne või valitud**, saate vaadetes kasutamiseks valida üksiku koosluse või protsessi versiooni. Saate valida mittekinnitatud ja mitteaktiivseid koosluse versioone koosluse koostajas kuvamiseks või haldamiseks.  

**Märkus.** Kui avate koosluse koostaja loendilehelt **Kooslused**, ei kuva see protsessiteavet. Praegu on koosluse või protsessi versiooni valik koosluse ja protsessi versiooni atribuut ja see rakendub kõikide koosluse koostaja eksemplaridele.  

Järgmistes jaotistes kirjeldatakse funktsionaalsust, mis on saadaval koosluse koostaja erinevatel vahekaartidel.

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a>Koosluse struktuuri analüüsimine koosluse koostajat kasutades
Koosluse koostajal on kaks osa.

-   Koosluse struktuuri puuvaade.
-   Üksikasjade osa, mis näitab valitud andmete üksikasju. Kui valite puuvaates sõlme, värskendatakse üksikasjade osa kiirkaarte sõlme alusel.
    -   **Koosluse rea üksikasjad** – näitab puuvaates valitud koosluse rea üksikasju.
    -   **Kauba andmed** – näitab põhikauba või valitud sõlmes kasutatava kauba üksikasju. Valitud kauba haldamiseks klõpsake suvandit **Väljastatud toote redigeerimine**.
    -   **Kooslus** – näitab valitud sõlmega seotud koosluse päist.
    -   **Protsess** – näitab valitud sõlmega seotud protsessi päist.
    -   **Protsessi operatsioonid** – näitab protsessi operatsioonide eelvaadet. Kui valitud on konkreetsele operatsioonile määratud koosluse rida, siis on operatsioon märkega **Operatsioonidel vajalik komponent**.

## <a name="selecting-a-bom-and-route"></a>Koosluse ja protsessi valimine
Kooslusele ja protsessile rakendatud filter kuvatakse koosluse koostaja päises. Saate filtrit muuta, kasutades dialoogikasti **Filtreeri**. Järgmises tabelis kirjeldatakse käesoleva dialoogikasti välju.

<table>
<thead>
<tr class="header">
<th>Väli</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tootedimensioonid</td>
<td>Kui valitud valmistoode on tooteetalon, saate määratleda peamise valiku aktiivsed tootedimensioonid. <strong>Märkus.</strong> Kui avate koosluse koostaja toote puhul, mis ei ole tooteetalon, ei saa dialoogiboksis <strong>Filter</strong> ühtegi tootedimensiooni valida.</td>
</tr>
<tr class="even">
<td>Laoala</td>
<td>Muutke saiti, millele koosluse puu kuvatakse. Vaikeala on valmistoote vaikelaoala.</td>
</tr>
<tr class="odd">
<td>Kuvamispõhimõte</td>
<td>Valige versiooni kuvamise põhimõte, mida rakendada praeguse koosluse struktuuri ja praeguse protsessiga.
<ul>
<li>Kui põhimõte on seadistatud valikule <strong>Aktiivne või valitud/aktiivne</strong>, otsitakse sellel kuupäeval kehtiv koosluse või protsessi versioon.</li>
<li>Kui põhimõte on seatud olekusse <strong>Valitud/aktiivne või Valitud</strong>, saate valida koosluse või protsessi versiooni, klõpsates valikuid <strong>Kooslus</strong> &gt; <strong>Koosluse versioonid</strong> või <strong>Protsess</strong> &gt; <strong>Protsessi versioonid</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Versiooni kuupäev</td>
<td>Sisestage koosluse ja protsessi versiooni kuupäeva. Versioon tuvastab koosluse versiooni häälestuses määratud versiooni kuupäevade alusel, millist koosluse versiooni määratud kuupäeval kasutatakse.</td>
</tr>
<tr class="odd">
<td>Alates kogusest</td>
<td>Filtreerige versiooni, valides konkreetse koguse. Kui määrate väärtuse, võidakse valida erinevad koosluse ja protsessi versioonid.</td>
</tr>
<tr class="even">
<td>Näita ainult kehtivaid</td>
<td>Kui valite märkeruudu, näitab puustruktuur ainult kehtivate kuupäevadega koosluseridu. Paremklõpsake või topeltklõpsake koosluse rida, et avada leht <strong>Koosluse rea redigeerimine</strong>, kus näete selle koosluse rea kehtivuskuupäevi.</td>
</tr>
</tbody>
</table>

Kui kasutate koosluse koostajat ühest või mitmest fiktiivse koosluse tasemest koosnevate koosluste ülevaatuseks või redigeerimiseks, siis tavaliselt hõlmab enimmüüdud kaubaga seostatud protsess kogu koosluse hierarhiat. Ülevaate lihtsustamiseks saate lukustada kuval kõrgeima taseme protsessi, klõpsates valikuid **Vaade** &gt; **Lukusta protsess**. Protsessi vabastamiseks klõpsake valikuid **Vaade** &gt; **Vabasta protsess**.

## <a name="adding-and-editing-boms-and-bom-lines"></a>Koosluste ja koosluse ridade lisamine ning redigeerimine
Koosluse ridade ja koosluste muutmiseks kasutage funktsiooni **Koosluseread**või **Kooslus**. Kui valite puus sõlme, määrab sõlme tüüp saadaolevad funktsioonid.

| Funktsioon                            | Kirjeldus                                                                                               | Sõlme tüüp ja tingimused                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Koosluseread &gt; Redigeeri                 | Avage dialoogikast, kus saab redigeerida koosluse rea atribuute.                                             | See funktsioon on saadaval, kui valitud on koosluse rea sõlm.                                                                                                                                                                                                                                   |
| Koosluseread &gt; Kustuta               | Kustutage koosluse rida valitud kooslusest.                                                                  | See funktsioon on saadaval, kui valitud on koosluse rea sõlm ja kooslus ei ole redigeerimiseks lukustatud.                                                                                                                                                                                             |
| Koosluseread &gt; Lisa enne rida      | Avage dialoogikast, kus saate valida enne valitud koosluse rida kaasatava tootevariandi.         | See funktsioon on saadaval, kui valitud on koosluse rea sõlm.                                                                                                                                                                                                                                   |
| Koosluseread &gt; Lisa komponendikooslusele | Avage dialoogikast, kus saate valida tootevariandi, mida kaasata valitud koosluse lõppu.       | See funktsioon on saadaval, kui valitud sõlmel on valitud kooslus. Kui see funktsioon ei ole saadaval, võib valitud kauba variandil puududa koosluse versioon. Sellisel juhul saate klõpsata valikuid **Kooslus** &gt; **Loo versioon** valitud sõlmele puuduva versiooni loomiseks. |
| Koosluseread &gt; Lisa pärast rida       | Avage dialoogikast, kus saate valida pärast valitud koosluse rida kaasatava tootevariandi.          | See funktsioon on saadaval, kui valitud on koosluse rea sõlm.                                                                                                                                                                                                                                   |
| Kooslus &gt; Loo versioon             | Looge valitud sõlme tootevariandile uus koosluse versioon või kooslus.                             | See funktsioon on saadaval, kui valitud koosluse rea sõlm on seotud kaubaga, mille tootmise tüüp on **Kooslus** või **Valem**.                                                                                                                                                  |
| BOM &gt; Arvutamine                | Avage dialoogikast, kus saate käitada valitud tootevariandi oma- või müügihinna arvutamise. | See funktsioon on saadaval, kui valitud sõlm on seotud koosluse versiooniga.                                                                                                                                                                                                         |
| Kooslus &gt; Kontrolli                      | Kinnitage valitud kooslus ja kontrollige seda.                                                                      | See funktsioon on saadaval, kui valitud sõlm on seotud koosluse versiooniga.                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a>Puuvaate konfigureerimine
Klõpsake suvandit **Seadistus**, et kohandada teavet, mida näidatakse koosluse koostaja puuvaates.

| Väljagrupp | Kirjeldus                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kooslus         | Kasutage märkeruute, et valida puustruktuuris näidatud kriteerium. Koosluse koostaja kuvab valitud kriteeriumi mõlema vahekaardi allosas. |
| Marsruut       | Kasutage märkeruute, et valida protsesside puhul näidatav kriteerium.                                                                                    |





