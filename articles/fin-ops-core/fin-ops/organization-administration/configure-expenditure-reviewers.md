---
title: Kulu ülevaatajate konfigureerimine
description: See teema kirjeldab, kuidas kasutada kulu ülevaatajad dünaamiliselt kasutaja valimiseks, kellele on määratud töövoo ülesanne, kinnitamine või käsitsi otsus.
author: rachel-profitt
ms.date: 06/25/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2021-06-24
ms.openlocfilehash: ad980889247e0239ad743078cb013c1c5839f676
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070142"
---
# <a name="configure-expenditure-reviewers"></a>Kulu ülevaatajate konfigureerimine
[!include[banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Saate seadistada kulude dünaamilise ülevaataja konfiguratsioonid, et suunata kulusid ülevaatamiseks kasutaja põhjal, kes on määratud projekti rollile või finantsdimensioonile, kus kulu tekib. Töövooprotsess kasutab määratud projektirolli või finantsdimensiooni omanikku määramaks, kellele tuleb kulu suunata.

Saate määratleda ühe või mitu kulude ülevaataja konfiguratsiooni ja seejärel valida töövoo loomisel konfiguratsiooni. Saate konfigureerida kulude ülevaataja väärtused igale organisatsiooni juriidilise isikule. Pärast kulude ülevaataja konfiguratsioonide määratlemist saate määrata oma töövooülesandele konfiguratsiooni. Kulu ülevaatajad saab määrata töövoo ülesannetele, kinnitamistele ja käsitsi otsustele.

> [!NOTE]
> Kuigi kulude ülevaatajad ei ole kohustuslikud, võivad need aidata lihtsustada teie töövoo konfigureerimist. Näiteks ei pea te iga kulukeskuse dimensiooni määramiseks looma ühte tingimuslikku otsustamist ning looma seejärel uue elemendi, et määrata kinnitus või ülesanne kindlale kasutajale või kasutajagruppidele. Selle asemel saate konfigureerida kulukeskuse dimensiooni omaniku ja kasutada kulu ülevaataja abil dünaamiliselt õiget kasutajat. Sel viisil, kui kulukeskuste omand või määramine muutub, peate lihtsalt värskendama **Omaniku** finantsdimensiooni välja.

## <a name="types-of-expenditure-reviewers"></a>Kulude ülevaatajate tüüpide seadistamine

Kõik töövood ei toeta kulu ülevaatajate kontseptsiooni. Vaikimisi saate konfigureerida ostutaotluste, ostutellimuste, hankija arvete ja kuluaruannete kulu ülevaatajad. Iga töövoo tüüp nõuab kulu ülevaatajate konfigureerimist eraldi lehel, mis on omane funktsioonile ja moodulile. Iga toetatud dokumendi puhul saab kulu ülevaatajad kasutada kas päise taseme töövoogude või rea taseme töövoogudega.

Järgmine tabel näitab, kuhu te minge iga toetatud dokumendi kulu ülevaataja konfigureerimiseks.

| Dokument  | Navigeerimispaan |
|----------|-----------------|
| Kuluaruanded | Kuluhalduse \> häälestus \> poliitika \> kulude ülevaatajad |
| Ostutellimused | Ostutellimused ja hanke \> häälestuse \> poliitikad \> Ostutellimuse kulu ülevaatajad |
| Ostutaotlused | Ostutellimused ja hanke \> häälestuse \> poliitikad \> Ostutellimuse registreerija kulu ülevaatajad |
| Hankijaarved | Avage Ostureskontro \> Poliitika seadistus \> Hankija arve kulu ülevaatajad |

## <a name="expenditure-reviewer-assignments"></a>Kulu ülevaataja määramised

Iga kulu ülevaataja jaoks on saadaval kahte tüüpi määramised: *projekti jaotised* ja *organisatsiooni jaotised*. Projekti jaotuse jaoks saate valida projekti asutused ja finantsdimensioonid. Organisatsiooni jaotuse jaoks saate valida finantsdimensioone.

Projektihaldurite hulka kuuluvad projektihaldur, projektikontroller ja projekti müügijuht. Määrate need asutused otse oma projektil, valides töötaja asjakohastel väljadel.

Finantsdimensioone juhitakse iga juriidilise isiku kontostruktuuridega. Iga juriidilise isiku jaoks saate valida, milliseid finantsdimensioone kulu ülevaatajaga kasutatakse. Dimensioonid võivad tulla kas projektist (sellisel juhul valite dimensioonid **Projekti jaotused** vahekaardil) või dokumendist (sellisel juhul valite **Organisatsiooni jaotused** dimensioonid vahekaardil). Välja **Omanik** lehel **Finantsdimensioonide väärtused** saate valida töötaja iga finantsdimensiooni jaoks.

## <a name="example-1-expenditure-reviewers-based-on-organization-distributions"></a>Näide 1: organisatsiooni jaotustel põhinevad kulu ülevaatajad

Töötate Contoso Appliancesis ja teie organisatsioonil on kuus osakonda ja 10 kulukeskust. Uue ostutaotluse esitamise korral peab kinnitus tulema esmalt osakonnajuhatajalt ja seejärel kulukeskuse juhilt.

Selles näites konfigureerite kaks *ostutaotluse kulu ülevaatajat*:

- Esimese ülevaataja korral peate osakonnale nime lisama ja seejärel valima **Osakonna** finantsdimensioonis **Organisatsiooni jaotus** vahekaardil. 
- Teise ülevaataja korral peate kõnekeskusele nime lisama ja seejärel valima **Kulukeskus** finantsdimensioonis **Organisatsiooni jaotus** vahekaardil.

Töövoo konfigureerimisel loote kaks kinnitus astet. Esimene on osakonnale ja teine kulukeskusele. Iga kinnituseelemendi jaoks valige **osaleja** väljal **Osaleja** vahekaardil **Rollipõhine**, valige **Osaleja tüüp** **Kulu osalejad** väljal ja seejärel valige soovitud osaleja **Osaleja** väljal.

Kui ostutaotlus on loodud, määratakse osakond ja kulukeskuse finantsdimensioonid ostutaotluse ridadele. Kui töövoog on esitatud, hindab süsteem kõigepealt ostutaotluse osakonda ja määrab kinnituselemendi kasutajale, kes on seotud osakonna jaoks valitud töötajaga. Pärast esimese kinnitamisetapi lõppu hindab süsteem teist heakskiitmise sammu ja määrab teise kinnituselemendi kasutajale, kes on seotud kulukeskusesse valitud töötajaga.

## <a name="example-2-expenditure-reviewers-based-on-project-distributions"></a>Näide 2: projekti jaotustel põhinevad kulu ülevaatajad

Te töötate Contoso Appliancesi teenuste osakonnas. Organisatsioon nõuab, et iga ostutellimuse projektijuht peab kulu kinnitama. Lisaks peab projekti kulukeskuse haldur selle kinnitama. Kinnitusi saab teha samaaegselt. Igal juhul peavad mõlemad kasutajad ostutellimuse kinnitama, enne kui töövoog saab jätkata.

Selles näites loote *ostutellimuse kulu ülevaataja* nimega **PM ja kulukeskus**. Märgistate **Projektihaldur** kasti ja seate **kulukeskuse dimensiooni** väärtuseks **Jah** **Projekti jaotamised** vahekaardil **Ostutellimuse kulu ülevaataja** lehel. Osana konfiguratsioonist peate tagama, et **projektijuhi** väli on seadistatud kõigile projektidele ja et omanik on määratud kõigile kulukeskustele **Finantsdimensiooni väärtused** lehel.

Töövoo konfigureerimisel on teil vaja ühte kinnituse elementi. Valite **osaleja** väljal **Määrangu tüüp** välja. Seejärel valite **rollipõhisel** vahekaardil **osalejatüübi osalejad** **Osaleja tüüp** väljal, ja valite projektijuhi ja kulukeskuse **Osaleja** väljal. Kindlustamaks, et töövooga ei saa jätkata enne, kui nii projektihaldur kui ka kulukeskuse omanik on töövoo kinnitanud, seate välja **Lõpetamispoliitika** väärtuseks **Kõik kinnitajad**.

Ostutellimuse loomisel peab väli **Projekt** olema määratud. Kui te ei nõua kõigi ostutellimuste jaoks projekti, peate enne kinnitussammu käivitamist projekti kontrolliks lisama töövoole tingimusliku otsuse. Süsteem hindab siis ostutellimuse jaoks määratud projekti ja määrab kinnituselemendi kasutajale, kes on seotud väljal **Projektijuht** määratud töötajaga. Lisaks loob süsteem ülesande ja määrab selle kasutajale, kes on seotud projektist valitud töötajaga väljal **Omanik**. Pange tähele, et selles näites kasutatakse projekti kulukeskust, mitte ostutellimuse kulukeskust.

## <a name="set-up-expenditure-reviewers"></a>Kulude ülevaatajate seadistamine

Selles näites näidatakse, kuidas konfigureeritakse ostutaotluse kulu ülevaatajat. Teist tüüpi kulu ülevaatajate konfigureerimiseks asendage navigeerimistee sammus 1 vastava teega tabelist [kulu ülevaatajate tüüpide](configure-expenditure-reviewers.md#types-of-expenditure-reviewers) jaotises, nagu varasemas teemas.

1. Minge **Ostutellimused ja hanke \> häälestuse \> poliitikad \> Ostutellimuse registreerija kulu ülevaatajad**.
2. Valige **ostutaotluse kulu ülevaatajate** lehel **uus**.
3. Sisestage **nimi** väljale kulu ülevaataja konfiguratsiooni nimi, nt **kulukeskus**.
4. Valige **kulu ülevaatajatel juriidilise isiku** kiirkaart konfigureerimiseks juriidiline isik.
5. Projekti jaotuse jaoks märkige ruut iga projekti asutusele ja valige **jah** iga finantsdimensiooni puhul, mida soovite lubada. 
6. Organisatsiooni jaotuse jaoks valige **Organisatsiooni jaotused** vahekaardil suvand **jah** iga finantsdimensiooni puhul, mida soovite lubada.
7. Korrake samme 4–6 iga järgmise juriidilise isiku jaoks.

## <a name="assign-owners-to-financial-dimensions"></a>Omanike määramine finantsdimensioonidesse

Omanikule finantsdimensiooni määramiseks tehke järgmist.

1. Avage **Pearaamat \> Kontoplaan \> Dimensioonid \> Finantsdimensioonid**.
2. Valige loendist omanikele määratav finantsdimensioon.
3. **Dimensiooniväärtuste** valimine.
4. Dimensiooniväärtuste muutmiseks klõpsake nuppu **Redigeeri**.
5. Valige loendist omanikele määratav finantsdimensioon.
6. Väljal **Omanik** valige töötaja, kellele dimensiooniväärtus määrata.

## <a name="configure-project-distributions"></a>Projekti jaotuste konfigureerimine

Projektiametite määramiseks projektile tehke järgmist.

1. Avage **Projektihaldus ja raamatupidamine \> Projektid \> Kõik projektid**.
2. Valige projekt, mille asutusele määrata.
3. Klõpsake nuppu **Redigeeri** et muuta projekti.
4. Kiirkaardil **Üldine** jaotises **Vastutav**, valige töötaja vastavalt vajadusele **müügijuhi**, **projektijuhi**, ja **projektikontrolleri** väljadele.
5. Valige **finantsdimensioonide** kiirkaardil projekti jaoks nõutavad finantsdimensioonid.

## <a name="assign-expenditure-reviewers-to-a-workflow-task"></a>Kulude ülevaatajate määramine töövoo ülesandele

See näide näitab, kuidas konfigureerida ostutaotluse töövoogu nii, et see kasutab ostutaotluse kulu ülevaataja. Teist tüüpi töövoogude konfigureerimiseks võib töövoo leht, mille peate avama sammus 1, olla moodulis **Kuluhaldus** või **Ostureskontr** moodul **Ostutellimuse ja hankemooduli** asemel.

Ostutellimuse täitmise kulude ülevaatajate määramiseks töövoo ülesandele toimige järgmiselt.

1. Valige seaded **Hanked \>, Seadistus, \> Hangete töövood**.
2. Topeltpuudutage (või topeltklõpsake) olemasolevat töövoogu või looge uus töövoog.
3. Valige töövoo redaktori **Töövoog** paanil ülesanne, mille konfiguratsioonile kulu ülevaataja määrata. Siis **Tegevuspaanil** grupis **Näita** valige **Atribuudid**.
4. Lehe **Atribuudid** vasakul paanil valige **Määrang**.
5. Vahekaardil **Määrangu tüüp** valige **Osaleja**.
6. Valige **rollipõhise** vahekaardi väljal **Osaleja tüüp** suvand **Kulu osalejad**. Siis **Osaleja** väljal valige kulude ülevaataja konfiguratsioon, mida soovite kasutada töövoo ülesande jaoks.
