---
title: Piiratud võimsuse planeerimine ja ajastamine
description: Piiratud võimsuse planeerimine ja planeerimine aitab teil mõista, kui palju tööd saab konkreetse perioodi jooksul toota, kui võetakse arvesse erinevate ressursside piiranguid.
author: t-benebo
ms.date: 09/19/2022
ms.topic: article
ms.search.form: ReqParameters, ReqPlanSched, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-19
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 3d116b5f7f456630415378e6cc069907e339068b
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689689"
---
# <a name="finite-capacity-planning-and-scheduling"></a>Piiratud võimsuse planeerimine ja ajastamine

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!--KFM: Preview until 10.0.31 GA -->

Piiratud võimsus on lähenemine, mis aitab teil mõista, kui palju tööd konkreetse perioodi jooksul saab teha, kui võetakse arvesse erinevate ressursside piiranguid. Piiratud võimsuse planeerimise eesmärk on tagada töö laekumine kogu tehases ühtlasel ja efektiivsel ajal.

Piiratud võimsuse planeerimine ja planeerimine loob tootmisprotsessidele realistlikuma graafiku, kui piiramatu laadimise lähenemine loob. Kui ressurssidel pole piisavalt võimsust, siis tarnekuupäev tõugatakse välja ja töö planeeritakse siis, kui võimsus on piisav.

## <a name="planning-optimization-support-for-finite-capacity-planning"></a>Piiratud võimsuse planeerimise planeerimise optimeerimise tugi

Piiratud võimsuse planeerimine ja planeerimine töötab samal viisil, sõltumata sellest, kas kasutate planeerimise optimeerimist või integreeritud plaanimismootorit. Kuid planeerimise optimeerimine ei kasuta kitsaskohaks **olemise ajapiiri** parameetrit. Kui kasutate planeerimise optimeerimist, planeeritakse kitsaskohana vajalikud ressursid alati, kasutades sama ajapiiri kui kitsaskohana väljamineku ressursid (nagu näitab piiratud võimsuse ajapiir).

## <a name="set-up-finite-capacity-functionality"></a>Seadista piiratud võimsuse funktsioon

Piiratud võimsuse funktsiooni kasutamiseks peate lubama võimsuse planeerimise globaalselt ja teil tuleb lubada piiratud võimsuse planeerimine nii koondplaani puhul, kus soovite seda kasutada kui ka iga ressursi puhul, kus see kehtib. Plaanide ja ressursside puhul, kus piiratud võimsus on lubatud, kaalutakse plaanitud tootmistellimuste planeerimisel juba reserveeritud võimsust. Plaanitud tootmistellimused planeeritakse vajaduse kuupäevast tagasi. Kui optimaalse graafiku järgimiseks pole võimsus saadaval, proovib süsteem nõuda komponendi kaupu varasemal kuupäeval. Kui teie võimsus võib vajaduse muutudes muutuda (nt vahetustega töötamisel), ei tohiks kasutada piiratud võimsuse funktsiooni, sest arvutatud töötlemisajad ei ole õiged. Planeerimine võtab arvesse ainult võimsust, mis on juba reserveeritud ressurssidele, kus piiratud võimsus on lubatud. Kui lubate piiratud võimsuse ressursile, on võimalik muuta piiratud võimsuse ajapiiri.

### <a name="activate-master-planning-parameters"></a>Koondplaneerimise parameetrite aktiveerimine

Piiratud võimsuse funktsiooni kasutamiseks peate lubama võimsuse planeerimise koondplaneerimise **parameetrite** lehel.

1. Avage **Koondplaneerimine \> Seadistus \> Koondplaneerimise parameetrid**.
1. Seadke vahekaardi **Plaanitud** tellimused jaotises **Võimsuse plaanimine** valikuks **Jah** *·*.

### <a name="activate-a-master-plan"></a>Koondplaani aktiveerimine

Peate lubama piiratud võimsuse planeerimise ja planeerimise iga koondplaani puhul, kus soovite seda kasutada.

1. Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**.
1. Valige loendi paanil koondplaan, mida soovite seadistada piiratud võimsuse planeerimiseks ja planeerimiseks.
1. Seadke jaotises **Plaanitud** tootmistellimused kiirkaardi **Üldine** väärtuseks **Jah** *·*.
1. Korrake samme 2 ja 3 iga täiendava koondplaani puhul, mida soovite seadistada.

### <a name="activate-resources"></a>Ressursside aktiveerimine

Peate lubama piiratud võimsuse planeerimise ja planeerimise iga ressursi puhul, kus soovite seda kasutada.

1. Valige **Tootmise juhtimine \> Seadistus \> Ressursid \> Ressursid**.
1. Valige loendipaanil ressurss, mida soovite seadistada kasutama piiratud võimsuse plaanimist ja planeerimist.
1. Seadke jaotises **Võimsus** kiirkaardil **Võimsus** valiku Piiratud **võimsus väärtuseks** *Jah*.
1. Korrake samme 2 ja 3 iga täiendava ressursi puhul, mida soovite seadistada.

## <a name="examples"></a>Näited

See jaotis annab järgmised näited, mis näitavad, kuidas töötada nii piiramatu kui piiratud võimsuse planeerimise ja planeerimisega:

- Näide 1 – piiramatu võimsuse planeerimine
- Näide 2: piiratud võimsuse planeerimine ühe päeva ajapiiriga
- Näide 3: piiratud võimsuse planeerimine kahepäevase ajapiiriga

### <a name="preconditions"></a>Eeltingimused

Kõik kolm näidet eeldavad selles jaotises kirjeldatud eeltingimusi.

Tootel *Product1* on protsess, mis sisaldab järgmisi operatsioone.

| Toimingu nr | Toimingu nimi | Ressurss        | Käitusaeg | Protsessi kogus | Edasi |
|---------------|----------------|-----------------|----------|--------------|------|
| 10            | Keevitus        | Liin <a0/&amp    | 1        | 2            | 20   |
| 20            | Koostamine     | Assemblemisrida | 1        | 4            |      |

Teie ettevõtte töötajad töötavad kaheksa tundi ühes vahetuses (8:00–16:00).

Plaanitud tootmistellimus on olemas *24%-le tootele* *1*. Selle tarnekuupäev on Täna *+ 3 päeva*.

Planeerimise tulemusena laadib süsteem ressursse järgmisel viisil:

- **Väljaminev rida:** seda ressurssi laaditakse *tänasest kella 08.00-st* *tänaseni + 1. kell 12.00*.
- **Assemblemisrida: seda** ressurssi laaditakse tänasest *+ 1 kella 12.00-st* *tänaseni + 2 kell 10.00*.

Järgnev illustratsioon näitab tulemuseks saadud Gantti diagrammi (valige see suurema vaate jaoks).

[![Eeltingimusi kuvav Gantti diagramm.](media/finite-examples-conditions-small.png "Eeltingimusi kuvav Gantti diagramm")](media/finite-examples-conditions.png)

### <a name="example-1--infinite-capacity-planning"></a>Näide 1 – piiramatu võimsuse planeerimine

See näide näitab planeerimise tulemusi, kui kasutate piiratud võimsuse planeerimise asemel piiramatut võimsuse planeerimist.

Koondplaanil on järgmine asjakohane säte, mis keelab plaani piiratud võimsuse planeerimise:

- **Piiratud võimsus:** *ei*

Valik **Piiratud võimsus on** samuti seatud valikule Ei *mõlema* asjakohase ressursi jaoks, et keelata piiratud võimsuse planeerimine nende jaoks:

- Liin <a0/&amp
- Assemblemisrida

Nüüd lisate uue müügitellimuse *8%* -le Product1-st *ja* käivitate plaani. Seetõttu laadib süsteem *liinirea tänasest kella 08.00-st* *tänaseni kell 12.00*. Pärast operatsioonide lõpetamist *käsureal laadib süsteem assemblemisrea tänasest kella 12.00-st* *tänaseni kell 14.00*.

Järgnev illustratsioon näitab tulemuseks saadud Gantti diagrammi (valige see suurema vaate jaoks).

[![Gantti diagramm, mis näitab piiramatu võimsuse planeerimise näidet.](media/finite-examples-example1-small.png "Gantti diagramm, mis näitab piiramatu võimsuse planeerimise näidet")](media/finite-examples-example1.png)

### <a name="example-2--finite-capacity-planning-with-a-time-fence-of-one-day"></a>Näide 2: piiratud võimsuse planeerimine ühe päeva ajapiiriga

See näide näitab planeerimise tulemusi, kui kasutate piiratud võimsuse planeerimist ja ajapiiri ühel päeval.

Koondplaanil on järgmised asjakohased sätted, mis võimaldavad piiratud võimsuse planeerimist ja plaani ajapiiri seada:

- **Piiratud võimsus:** *Jah*
- **Piiratud võimsuse ajapiir:** *1*

Piiratud **võimsuse valik on** mõlema vastava ressursi *puhul* seatud väärtusele Jah, et lubada nende jaoks piiratud võimsuse planeerimist:

- Liin <a0/&amp
- Assemblemisrida

Nüüd lisate uue müügitellimuse *8%* -le Product1-st *ja* käivitate plaani. Selle tulemusena laadib süsteem *käsurea praegusest + 1. kella 01.00-st* *tänaseni + 1 kell 12.00*. Pärast operatsioonide lõpetamist *käsureal laadib süsteem assemblemisrea alates tänasest + 1 kella 12.00-st* *tänaseni + 1 kell 14.00*. Süsteem arvestab piiratud võimsust ainult ühel päeval.

Järgnev illustratsioon näitab tulemuseks saadud Gantti diagrammi (valige see suurema vaate jaoks).

[![Gantti diagramm, kus kuvatakse piiratud võimsuse planeerimine ühe päeva ajapiiriga.](media/finite-examples-example2-small.png "Gantti diagramm, kus kuvatakse piiratud võimsuse planeerimine ühe päeva ajapiiriga")](media/finite-examples-example2.png)

### <a name="example-3--finite-capacity-planning-with-a-time-fence-of-two-days"></a>Näide 3: piiratud võimsuse planeerimine kahepäevase ajapiiriga

See näide näitab planeerimise tulemusi, kui kasutate piiratud võimsuse planeerimist ja kahepäevast ajapiiri.

Koondplaanil on järgmised asjakohased sätted, mis võimaldavad piiratud võimsuse planeerimist ja plaani ajapiiri seada:

- **Piiratud võimsus:** *Jah*
- **Piiratud võimsuse ajapiir:** *2*

Piiratud **võimsuse valik on** mõlema vastava ressursi *puhul* seatud väärtusele Jah, et lubada nende jaoks piiratud võimsuse planeerimist:

- Liin <a0/&amp
- Assemblemisrida

Nüüd lisate uue müügitellimuse *8%* -le Product1-st *ja* käivitate plaani. Selle tulemusena laadib *süsteem käsurea praegusest + 1 kella 12.00-st* *tänaseni + 1 kell 16.00*. Pärast operatsioonide lõpetamist *käsureal laadib süsteem assemblemisrea tänasest + 2 kella 8.00-st* *tänaseni + 2 kell 10.00*. Süsteem arvestab piiratud võimsust ainult kahe päeva jooksul.

Järgnev illustratsioon näitab tulemuseks saadud Gantti diagrammi (valige see suurema vaate jaoks).

[![Gantti diagramm, kus kuvatakse piiratud võimsuse planeerimine kahe päeva ajapiiriga.](media/finite-examples-example3-small.png "Piiratud võimsusega plaanimist kuvav Gantti diagramm kahe päeva ajapiiriga")](media/finite-examples-example3.png)

> [!IMPORTANT]
> Seadistage alati piiratud võimsuse ajapiir vastavalt ärivajadustele. Selles artiklis toodud näited illustreerivad lihtsalt funktsiooni. Tegelikult on ühe päeva ajapiir tõenäoliselt liiga väike enamiku tootjate puhul, kes kasutavad piiratud võimsuse planeerimist.
