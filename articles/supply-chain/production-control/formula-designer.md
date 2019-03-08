---
title: Valemikoostaja
description: Selles teemas kirjeldatakse, kuidas kasutada valemikoostajad valemite analüüsimiseks ja haldamiseks puuvaates.
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31a46230251be3a654092a4acc05a404533001b2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "348499"
---
# <a name="formula-designer"></a>Valemikoostaja

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas kasutada valemikoostajad valemite analüüsimiseks ja haldamiseks puuvaates.

Kui avate lehe **Valemikoostaja** lehelt **Väljastatud tooted**, on vasakul paanil oleval puul näha väljastatud toote kaastoodete loend ja koostisosade hierarhia. Struktuur tuletatakse valitud kauba ja selle koostisosade, kauba tellimise vaikelaoala ja tegeliku kuupäeva puhul aktiivsete ning kinnitatud valemite hierarhiast.

Klõpsake nuppu **Seadistus** erinevate konfiguratsioonide valimiseks ja määramiseks, milline teave puu ridadel ilmub.

Klõpsake suvandit **Filtreeri** vaate algse valiku muutmiseks. Kui määrate kuvamispõhimõtteks **Valitud/aktiivne** või **Valitud**, saate vaadetes kasutamiseks valida üksiku valemi või protsessi versiooni. Saate valida mittekinnitatud ja mitteaktiivseid valemiversioone valemikoostajas kuvamiseks või haldamiseks.  

> [!NOTE]
> Kui avate lehe **Valemikoostaja** loendilehelt **Kooslused**, ei kuva see protsessiteavet. Praegu rakendub valemi või protsessiversiooni valik kõigile valemikoostaja eksemplaridele.  

Järgmistes jaotistes kirjeldatakse funktsionaalsust, mis on koosluse koostajas saadaval.

## <a name="analyze-a-formula-structure-by-using-the-formula-designer"></a>Valemistruktuuri analüüsimine valemikoostaja abil
Valemikoostajal on kaks osa.

-   Valemistruktuuri puuvaade.
-   Üksikasjade osa, mis näitab valitud andmete üksikasju. Kui valite puuvaates sõlme, värskendatakse üksikasjade osa kiirkaarte sõlme alusel.
    -   **Valemi rea üksikasjad** – kuvab puuvaates valitud valemirea üksikasjad.
    -   **Kauba andmed** – kuvab põhikauba või valitud sõlmes kasutatava kauba üksikasjad. Valitud kauba haldamiseks klõpsake suvandit **Väljastatud toote redigeerimine**.
    -   **Valem** – kuvab valitud sõlmega seotud valemi päise.
    -   **Protsess** – kuvab valitud sõlmega seotud protsessi päise.
    -   **Protsessitoimingud** – kuvab protsessitoimingute eelvaate. Kui valitud on konkreetsele toimingule määratud koosluse rida, siis on toiming märkega **Toimingutes vajalik komponent**.

## <a name="select-a-formula-and-route"></a>Valemi ja protsessi valimine
Valemile ja protsessile rakendatud filter kuvatakse valemikoostaja päises. Saate filtrit muuta, kasutades dialoogikasti **Filtreeri**. Järgmises tabelis kirjeldatakse käesoleva dialoogikasti välju.

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
<td>Kui valitud valmistoode on tooteetalon, saate määratleda peamise valiku aktiivsed tootedimensioonid. Pange tähele, et kui avate valemikoostaja toote puhul, mis ei ole tooteetalon, ei saa dialoogiboksis <strong>Filter</strong> ühtegi tootedimensiooni valida.</p></td>
</tr>
<tr class="even">
<td>Sait</td>
<td>Muutke saiti, mille koostisosade puu on kuvatud. Vaikeala on valmistoote vaikelaoala.</td>
</tr>
<tr class="odd">
<td>Kuvamispõhimõte</td>
<td><p>Valige versiooni kuvamise põhimõte, mida rakendada praeguse valemi struktuuri ja praeguse protsessiga.</p>
<ul>
<li>Kui põhimõtteks on määratud <strong>Aktiivne</strong> või <strong>Valitud aktiivne</strong>, otsitakse üles sellel kuupäeval kehtiv valemi või protsessi versioon.</li>
<li>Kui põhimõtteks on määratud <strong>Valitud aktiivne</strong> või <strong>Valitud</strong>, saate valida valemi või protsessi versiooni, klõpsates valikuid <strong>Valem</strong> &gt; <strong>Valemiversioonid</strong> või <strong>Protsess</strong> &gt; <strong>Protsessiversioonid</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Versiooni kuupäev</td>
<td>Sisestage valemi ja protsessi versiooni kuupäev. Versioon tuvastab valemiversiooni seadistuses olevate versiooni kuupäevade põhjal konkreetsel kuupäeval kasutatava valemiversiooni.</td>
</tr>
<tr class="odd">
<td>Alates kogusest</td>
<td>Filtreerige versiooni, valides konkreetse &quot;lähtekoguse&quot;. Kui määrate väärtuse, võidakse valida erinevad valemi ja protsessi versioonid.</td>
</tr>
<tr class="even">
<td>Näita ainult kehtivaid</td>
<td>Kui valite märkeruudu, näitab puustruktuur ainult kehtivate kuupäevadega valemiridu. Paremklõpsake või topeltklõpsake valemirida, et avada leht <strong>Valemirea redigeerimine</strong>, kus näete selle valemirea kehtivuskuupäevi.</td>
</tr>
</tbody>
</table>

Kui kasutate valemikoostajat ühest või mitmest fiktiivse valemi tasemest koosnevate valemite ülevaatuseks või redigeerimiseks, siis tavaliselt hõlmab enimmüüdud kaubaga seostatud protsess kogu valemihierarhiat. Ülevaate lihtsustamiseks saate lukustada kuval kõrgeima taseme protsessi, klõpsates valikuid **Vaade** &gt; **Lukusta protsess**. Protsessi vabastamiseks klõpsake valikuid **Vaade** &gt; **Vabasta protsess**.

## <a name="add-and-edit-formulas-and-formula-lines"></a>Valemite ja valemiridade lisamine ja redigeerimine
Valemiridade ja valemi muutmiseks kasutage funktsiooni **Koosluseread** või **Valem**. Kui valite puus sõlme, määrab sõlme tüüp saadaolevad funktsioonid.

| Funktsioon                            | Kirjeldus                                                                                               | Sõlme tüüp ja tingimused |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|--------------------------|
| Koosluseread &gt; Redigeeri                 | Avage dialoogiboks, kus saab redigeerida valemirea atribuute.                                         | See funktsioon on saadaval, kui valitud on valemirea sõlm. |
| Koosluseread &gt; Kustuta               | Kustutage valemirida valitud valemist.                                                          | See funktsioon on saadaval, kui valitud on valemirea sõlm ja valem ei ole redigeerimiseks lukustatud. |
| Koosluseread &gt; Lisa enne rida      | Avage dialoogiboks, kus saate valida enne valitud valemirida kaasatava tootevariandi.     | See funktsioon on saadaval, kui valitud on valemirea sõlm. |
| Koosluseread &gt; Lisa komponendikooslusele | Avage dialoogiboks, kus saate valida tootevariandi, mida kaasata valitud valemi lõppu.   | See funktsioon on saadaval, kui valitud sõlmel on valitud valem. Kui see funktsioon ei ole saadaval, võib valitud kauba variandil puududa valemiversioon. Sellisel juhul võite klõpsata valikuid **Valem** &gt; **Loo versioon** valitud sõlmele puuduva versiooni loomiseks. |
| Koosluseread &gt; Lisa pärast rida       | Avage dialoogiboks, kus saate valida pärast valitud valemirida lisatava tootevariandi.      | See funktsioon on saadaval, kui valitud on valemirea sõlm. |
| Valem &gt; Loo versioon         | Looge valitud sõlme tootevariandile uus valemiversioon või valem.                     | See funktsioon on saadaval, kui valitud valemirea sõlm on seotud kaubaga, mille tootmise tüüp on **Kooslus** või **Valem**. |
| Valemi &gt; arvutamine            | Avage dialoogikast, kus saate käitada valitud tootevariandi oma- või müügihinna arvutamise. | See funktsioon on saadaval, kui valitud sõlm on seotud valemiversiooniga. |
| Valemi &gt; kontrollimine                  | Kinnitage ja kontrollige valitud valemit.                                                                  | See funktsioon on saadaval, kui valitud sõlm on seotud valemiversiooniga. |

## <a name="configuring-the-tree-view"></a>Puuvaate konfigureerimine
Klõpsake suvandit **Seadistus**, et kohandada teavet, mida näidatakse valemikoostaja puuvaates.


| Väljagrupp |                                                                          Kirjeldus                                                                          |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Kooslus     | Kasutage märkeruute, et valida puustruktuuris näidatud kriteerium. Valemikoostaja kuvab valitud kriteeriumi mõlema vahekaardi allosas. |
|    Protsess    |                                           Kasutage märkeruute, et valida protsesside puhul näidatav kriteerium.                                           |

