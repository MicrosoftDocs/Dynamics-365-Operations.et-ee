---
title: Finantsaruande komponendid
description: Selles artiklis kirjeldatakse, kuidas aruande definitsiooni komponente (koosteüksusi) finantsaruandluses kasutatakse.
author: aprilolson
ms.date: 10/27/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8512559ea33f16f3558b277999cc86240ee8277d1b3b0d6bf2aecba32df8e09f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761436"
---
# <a name="financial-report-components"></a>Finantsaruande komponendid

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas aruande definitsiooni komponente (koosteüksusi) finantsaruandluses kasutatakse. Nende koosteüksuste hulka kuuluvad readefinitsioonid, veerudefinitsioonid ja aruandluspuu definitsioonid. Artiklis selgitatakse, kuidas koosteüksusi korraldada ja lukustada.

Finantsaruannete koosturi ülesehituse filosoofia on suunatud teabe jagamisele vähimateks osadeks ehk koosteüksusteks ja siis nende osade segamine ja sobitamine vajalikul viisil. Seetõttu on teie aruande vormindamine finantsandmetest eraldi ja saate muuta aruande ülesehitust, muutmata finantsandmeid oma Microsoft Dynamics ERP süsteemis. Selle koosteüksuste lähenemisviisi abil saate vajalike aruannete loomiseks kombineerida teksti, summasid ja arvutusi. Lisaks toetab selline paindlikkus loovust, lihtsustades teil oma tegevuse vaatamist mitmesugusel viisil. Aruande definitsiooni üksikud koosteüksused sarnanevad kolmemõõtmelise arvutustabeliga, kuid on võimsamad. Aruande definitsioon määrab aruande puhul kasutatava readefinitsiooni, veeru definitsiooni ja valikulise aruandluspuu definitsiooni. See hõlmab ka teavet selle kohta, kuhu loodud aruanne salvestada ja kuidas seda vormindada.

## <a name="building-blocks-of-a-report"></a>Aruande koosteüksused

| Koosteüksus            | Kirjeldus | Lisateave |
|---------------------------|-------------|----------------------|
| Rea definitsioon            | Readefinitsioon määratleb kirjeldavad read (näiteks palga või müügi) aruandel. See loetleb ka segmendi väärtused või dimensioonid, mis sisaldavad iga reaüksuse väärtusi, ja hõlmab rea vormindamist ning arvutusi. | [Readefinitsioonid](row-definitions-financial-reporting.md) |
| Veeru määratlus         | Veeru definitsioon määratleb finantsdimensioonidest andmete ekstraktimisel kasutatava perioodi. See hõlmab ka veeru vormindamist ja arvutusi. | [Veeru definitsioonid](column-definitions-financial-reports.md) |
| Aruandluspuu definitsioon | Aruandluspuu definitsioon sarnaneb organisatsiooni skeemiga. See sisaldab üksikuid aruandlusüksusi, mis tähistavad diagrammi igat välja. Üksusteks võivad olla kas finantsandmete üksikud osakonnad või kõrgema taseme üksused, mis koondavad muude aruandlusüksuste andmeid. | [Aruandluspuu definitsioonid](financial-reporting-tree-definitions.md) |
| Aruande definitsioon         | Aruande definitsioon kasutab aruande loomiseks readefinitsiooni, veeru definitsiooni ja valikulist aruandluspuu definitsiooni. See sisaldab ka täiendavaid suvandeid ja sätteid, mida saab aruande kohandamiseks kasutada. | [Aruande definitsioon](design-financial-report-definitions.md) |

Kui te pole varem aruandeid koostanud, võib olla mõistlik kasutada aruandeviisardit kiireks aruande definitsiooni loomiseks, mida saate hiljem kohandada. Kui teil on aruannete koostamisel kogemusi ja soovite paindlikumat aruande ülesehitust, saate uue aruande definitsiooni loomiseks kombineerida uusi või olemasolevaid koosteüksusi. Kvaliteetsete aruannete loomiseks ei pea teil olema kõigist saadaolevatest aruande definitsiooni suvanditest täielikku ülevaadet. Muutudes aruannete kujundamises kogenumaks saate täpsemate funktsioonide kasutamiseks oma aruande definitsioone laiendada. Pärast põhiaruande loomist saate aruande definitsiooni ja selle mis tahes koosteüksusi kohandada.

## <a name="organize-the-building-blocks"></a>Koosteüksuste korraldamine
Kasutage aruande kujundajas koosteüksuste korraldamiseks kaustu. Kõik kaustad on omased neis sisalduva koosteüksuse tüübile. Näiteks asuvad kõik readefinitsioone sisaldavad kaustad aruandekoosturi paanil **Readefinitsioonid**.

### <a name="create-a-folder"></a>Kausta loomine

1. Valige aruande kujundajas navigeerimispaanil korraldatava koosteüksuse tüüp. Näiteks readefinitsiooni sortimiseks klõpsake suvandit **Readefinitsioonid**.
2. Valige navigeerimispaanil olemasolev kaust, mille alla luuakse uus kaust ja seejärel tehke üks järgmistest toimingutest.

    - Paremklõpsake põhikausta ja klõpsake siis valikut **Uus kaust**.
    - Valige põhikaust, klõpsake valikut **Fail** ja seejärel klõpsake valikut **Uus kaust**.

3. Uue kausta kuvamisel sisestage uue kausta nimi ja vajutage siis sisestusklahvi.

## <a name="lock-a-building-block"></a> Koosteüksuse lukustamine
Koosteüksuse lukustamiseks ja kaitsmiseks saab luua parooli. Sel viisil saate lisada aruande komponenti turvalisuse taseme, turvamata kogu süsteemi. Parool võib kaitsta koosteüksuse teavet, mis on oluline teie kuulõpu aruandeprotsessi jaoks. Koosteüksuse saab lukustada igasuguses rollis kasutaja. Kuid teistel kasutajatel on alati juurdepääs lukustatud komponendi kirjutuskaitstud versioonile. Kasutajad saavad lukustatud komponenti avada, muuta ja uue nimega salvestada. Administraatori rolliga kasutajal on lukustatud koosteüksusele alati juurdepääs ja ta saab seda muuta.

1. Avage aruande kujundajas lukustatav aruande komponent, näiteks readefinitsioon, veeru definitsioon, aruande definitsioon või aruandluspuu definitsioon.
2. Klõpsake menüüs **Tööriistad** valikut **Kaitse / vabasta kaitse**. Võite klõpsata ka tööriistaribal olevat ikooni **Kaitse / vabasta kaitse** (lukustamise ikoon).
3. Sisestage dialoogiboksi **Kaitse** parool ja kinnitage see ning klõpsake siis nuppu **OK**. Avatud koosteüksuse lukustamisel tõstetakse lukuikoon tööriistaribal esile.

Lukustatud koosteüksuse avamiseks avage koosteüksus ja seejärel klõpsake tööriistaribal ikooni **Kaitse/vabasta kaitse**. Teine võimalus on klõpsata menüüs **Tööriistad** valikut **Vabasta kaitse**.

## <a name="building-block-groups"></a>Koosteüksuste grupid

Koosteüksused on aruande puhul loodavad readefinitsioonid, veeru definitsioonid, aruandluspuu definitsioonid ja aruande definitsioonid. Koosteüksuse grupid on definitsioonide ja dimensioonikogumid.

### <a name="view-a-building-block-group"></a>Koosteüksuste rühma vaatamine

Saate vaadata kõiki koosteüksusi, mis on määratud koosteüksuste rühmale. Saate koosteüksuste rühma eksportida või importida.

1. Klõpsake aruandekoosturis menüü **Ettevõte** suvandit **Koosteüksuste rühmad**.
2. Valige dialoogiboksist **Koosteüksuste grupid** kuvatav koosteüksus.
3. Klõpsake käsku **Kuva** dialoogiboksi **Koosteüksuste grupi kuvamine** avamiseks, kus saate koosteüksuste grupi sisu kuvada.
4. Klõpsake dialoogibokside sulgemiseks suvandit **Sulge**.

### <a name="export-a-building-block-group"></a>Koosteüksuste rühma eksportimine

Saate koosteüksuste rühma või koosteüksuste rühma kuuluvaid kindlaid aruande koosteüksusi eksportida. Eksporditud koosteüksuste rühma saate kasutada varukoopiana. Saate eksporditud andmeid ka installide vahel kopeerida. Aruandekoostur sisaldab viidatud fondilaade ja dimensioonigruppe koos koosteüksuste grupiga.

1. Klõpsake aruande kujundaja menüüs **Ettevõte** suvandit **Koosteüksuste grupid**.
2. Valige dialoogiboksis **Koosteüksuste rühmad** eksporditav koosteüksuste rühm ning klõpsake seejärel suvandit **Ekspordi**.
3. Valige dialoogiboksist **Eksport** eksporditavad aruande definitsioonid.

    - Kõikide aruande definitsioonide ja seotud koosteüksuste eksportimiseks klõpsake suvandit **Vali kõik**.
    - Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite eksportimiseks klõpsake vastavat vahekaarti ja valige eksporditavad üksused. Vahekaardil mitme üksuse valimiseks vajutage ja hoidke all klahvi Ctrl.

    > [!NOTE]
    > Eksporditavate aruannete valimisel valitakse nendega seotud read, veerud, puud ja dimensioonikogumid.

4. Kui olete eksporditavate üksuste valimise lõpetanud, klõpsake käsku **Ekspordi**.
5. Valige dialoogiboksist **Salvesta nimega** koht, kuhu koosteüksuste grupp eksportida.
6. Sisestage faili nimi väljale **Faili nimi**. Aruandekoostur lisab automaatselt failinime laiendi .tdbx.
7. Klõpsake nuppu **Salvesta**. Koosteüksuste grupp salvestatakse määratud asukohta.

### <a name="import-a-building-block-group"></a> Koosteüksuste grupi importimine

Saate koosteüksuste rühma importida olemasolevasse koosteüksuste rühma. Kõik imporditud koosteüksuste grupid säilitavad algsed fondilaadid ja ettevõtteviited ning sisaldavad vastavaid dimensioonikogumeid.

1. Klõpsake aruande kujundaja menüüs **Ettevõte** suvandit **Koosteüksuste grupid**.
2. Valige dialoogiboksis **Koosteüksuste rühmad** koosteüksuste rühm, millesse soovite teise koosteüksuste rühma importida, ning klõpsake seejärel suvandit **Impordi**.
3. Valige dialoogiboksis **Avamine** imporditav koosteüksuste rühm ning klõpsake seejärel suvandit **Ava**.
4. Valige dialoogiboksist **Import** imporditavad aruande definitsioonid.

    - Kõikide aruande definitsioonide ja seotud koosteüksuste importimiseks klõpsake valikut **Vali kõik**.
    - Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite importimiseks valige imporditavad aruanded, read, veerud, puud või dimensioonikogumid.

5. Kui olete imporditavate üksuste valimise lõpetanud, klõpsake käsku **Impordi**.

### <a name="undo-a-checkout-of-a-building-block"></a>Koosteüksuse väljaregistreerimise tühistamine

Koosteüksuse avamisel pääsevad teised kasutajad selle koosteüksuse juurde kirjutuskaitstud režiimis. Mõnikord unustavad kasutajad koosteüksuse sulgeda või sulevad süsteemi ilma koosteüksust sulgemata. Sel juhul jääb koosteüksus välja registreerituks ja ükski teine kasutaja ei saa seda avada. Sellistel juhtudel saab finantsaruandluse administraator kasutada dialoogiboksi **Väljaregistreeritud üksused** koosteüksuste sisseregistreerimiseks, mille kasutajad on jätnud väljaregistreeritud olekusse.

> [!NOTE]
> Teil peab olema administraatori roll, et koosteüksusi dialoogiboksi **Välja registreeritud üksused** kasutades registreerida.

1. Valige aruande kujundaja menüüst **Tööriistad** suvand **Väljaregistreeritud üksused**.
2. Valige dialoogiboksis **Välja registreeritud üksused** suvand **Kuva kõikide kasutajate üksused**. Loendit värskendatakse ning see kuvab kõik välja registreeritud koosteüksused ja kasutajad, kes need välja on registreerinud.
3. Valige koosteüksus ja klõpsake seejärel suvandit **Tühista väljaregistreerimine**.
4. Klõpsake koosteüksuse registreerimiseks suvandit **Jah**.

## <a name="additional-resources"></a>Lisaressursid

[Finantsaruandlus](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]