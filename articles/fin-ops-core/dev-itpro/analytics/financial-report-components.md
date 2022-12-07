---
title: Finantsaruande komponendid
description: Selles artiklis kirjeldatakse, kuidas aruande definitsiooni komponente (koosteüksusi) finantsaruandluses kasutatakse.
author: aprilolson
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.form: FinancialReports
ms.openlocfilehash: 66430f81bd3d1efe126dfb29fa9c6a093716f90e
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802711"
---
# <a name="financial-report-components"></a>Finantsaruande komponendid

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas aruande definitsiooni komponente (koosteüksusi) finantsaruandluses kasutatakse. Nende koosteüksuste hulka kuuluvad readefinitsioonid, veerudefinitsioonid ja aruandluspuu definitsioonid. Artiklis selgitatakse, kuidas koosteüksusi korraldada ja lukustada.

Finantsaruannete koosturi ülesehituse filosoofia on suunatud teabe jagamisele vähimateks osadeks ehk koosteüksusteks ja siis nende osade segamine ja sobitamine vajalikul viisil. Seepärast on teie aruande vormindamine eraldi  Microsoft Dynamics finantsandmetest ja te saate muuta aruande kujundust ilma finantsandmete muutmiseta 365 finantsandmetes. Selle koosteüksuste lähenemisviisi abil saate vajalike aruannete loomiseks kombineerida teksti, summasid ja arvutusi. Lisaks toetab selline paindlikkus loovust, lihtsustades teil oma tegevuse vaatamist mitmesugusel viisil. Aruande definitsiooni üksikud koosteüksused sarnanevad kolmemõõtmelise arvutustabeliga, kuid on võimsamad. Aruande definitsioon määrab aruande puhul kasutatava readefinitsiooni, veeru definitsiooni ja valikulise aruandluspuu definitsiooni. See hõlmab ka teavet selle kohta, kuhu loodud aruanne salvestada ja kuidas seda vormindada.

## <a name="building-blocks-of-a-report"></a>Aruande koosteüksused

| Koosteüksus            | Kirjeldus | Lisateave |
|---------------------------|-------------|----------------------|
| Rea definitsioon            | Readefinitsioon määratleb kirjeldavad read (näiteks palga või müügi) aruandel. See loetleb ka segmendi väärtused või dimensioonid, mis sisaldavad iga reaüksuse väärtusi, ja hõlmab rea vormindamist ning arvutusi. | [Readefinitsioonid](row-definitions-financial-reporting.md) |
| Veeru määratlus         | Veeru definitsioon määratleb finantsdimensioonidest andmete ekstraktimisel kasutatava perioodi. See hõlmab ka veeru vormindamist ja arvutusi. | [Veeru definitsioonid](column-definitions-financial-reports.md) |
| Aruandluspuu definitsioon | Aruandluspuu definitsioon sarnaneb organisatsiooni skeemiga. See sisaldab üksikuid aruandlusüksusi, mis tähistavad diagrammi igat välja. Üksusteks võivad olla kas finantsandmete üksikud osakonnad või kõrgema taseme üksused, mis koondavad muude aruandlusüksuste andmeid. | [Aruandluspuu definitsioonid](financial-reporting-tree-definitions.md) |
| Aruande definitsioon         | Aruande definitsioon kasutab aruande loomiseks readefinitsiooni, veeru definitsiooni ja valikulist aruandluspuu definitsiooni. See sisaldab ka täiendavaid suvandeid ja sätteid, mida saab aruande kohandamiseks kasutada. | [Aruande definitsioon](design-financial-report-definitions.md) |

Kui te pole varem aruandeid koostanud, võib olla mõistlik kasutada aruandeviisardit kiireks aruande definitsiooni loomiseks, mida saate hiljem kohandada. Kui teil on aruannete koostamisel kogemusi ja soovite paindlikumat aruande ülesehitust, saate uue aruande definitsiooni loomiseks kombineerida uusi või olemasolevaid koosteüksusi. Kvaliteetsete aruannete loomiseks ei pea teil olema kõigist saadaolevatest aruande definitsiooni suvanditest täielikku ülevaadet. Muutudes aruannete kujundamises kogenumaks saate täpsemate funktsioonide kasutamiseks oma aruande definitsioone laiendada. Pärast põhiaruande loomist saate aruande definitsiooni ja selle mis tahes koosteüksusi kohandada.

## <a name="organize-the-building-blocks"></a>Koosteüksuste korraldamine
Kasutage aruande kujundajas koosteüksuste korraldamiseks kaustu. Kõik kaustad on omased neis sisalduva koosteüksuse tüübile. Näiteks kõik readefinitsioone sisaldavad kaustad asuvad aruandekujundaja **paanil** Readefinitsioonid.

### <a name="create-a-folder"></a>Kausta loomine

1. Aruandekujundajas valige koosteüksuse tüüp, mida navigeerimispaanil korraldada. Näiteks readefinitsiooni sortimiseks klõpsake suvandit **Readefinitsioonid**.
2. Valige navigeerimispaanil olemasolev kaust, mille alla luuakse uus kaust ja seejärel tehke üks järgmistest toimingutest.

    - Paremklõpsake emakausta ja klõpsake seejärel käsku **Uus**.
    - Valige emakaust, klõpsake **nuppu Fail** ja seejärel nuppu **Uus**.

3. Uue kausta kuvamisel sisestage uue kausta nimi ja vajutage sisestusklahvi **Enter**.

## <a name="lock-a-building-block"></a> Koosteüksuse lukustamine
Koosteüksuse lukustamiseks ja kaitsmiseks saab luua parooli. Sel viisil saate lisada aruande komponenti turvalisuse taseme, turvamata kogu süsteemi. Parool võib kaitsta koosteüksuse teavet, mis on oluline teie kuulõpu aruandeprotsessi jaoks. Koosteüksuse saab lukustada igasuguses rollis kasutaja. Kuid teistel kasutajatel on alati juurdepääs lukustatud komponendi kirjutuskaitstud versioonile. Kasutajad saavad lukustatud komponenti avada, muuta ja uue nimega salvestada. Administraatori rolliga kasutajal on lukustatud koosteüksusele alati juurdepääs ja ta saab seda muuta.

1. Avage aruandekujundajas aruande komponent lukustamiseks, nt readefinitsioon, veeru definitsioon, aruandedefinitsioon või aruandluspuu definitsioon.
2. Klõpsake menüüs **Tööriistad** valikut **Kaitse / vabasta kaitse**. Võite klõpsata ka tööriistaribal olevat ikooni **Kaitse / vabasta kaitse** (lukustamise ikoon).
3. Sisestage dialoogiboksi **Kaitse** parool ja kinnitage see ning klõpsake siis nuppu **OK**. Avatud koosteüksuse lukustamisel tõstetakse lukuikoon tööriistaribal esile.

Lukustatud koosteüksuse avamiseks avage koosteüksus ja seejärel klõpsake tööriistaribal ikooni **Kaitse/vabasta kaitse**. Teine võimalus on klõpsata menüüs **Tööriistad** valikut **Vabasta kaitse**.

## <a name="building-block-groups"></a>Koosteüksuste grupid

Koosteüksused on aruande puhul loodavad readefinitsioonid, veeru definitsioonid, aruandluspuu definitsioonid ja aruande definitsioonid. Koosteüksuse grupid on definitsioonide ja dimensioonikogumid.

### <a name="view-a-building-block-group"></a>Koosteüksuste rühma vaatamine

Saate vaadata kõiki koosteüksusi, mis on määratud koosteüksuste rühmale. Saate koosteüksuste rühma eksportida või importida.

1. Aruandekujundajas klõpsake menüü Ettevõte **käsku** Blokeeritud gruppide **loomine**.
2. Dialoogiboksis Koosteüksuse **grupid** valige kuvamiseks koosteplokk.
3. Klõpsake **nuppu** Vaata, et avada **dialoogiboks Hooneplokkide** kuvamine, kus saate vaadata koosteüksuse grupi sisu.
4. Klõpsake dialoogibokside sulgemiseks suvandit **Sulge**.

### <a name="export-a-building-block-group"></a>Koosteüksuste rühma eksportimine

Saate koosteüksuste rühma või koosteüksuste rühma kuuluvaid kindlaid aruande koosteüksusi eksportida. Eksporditud koosteüksuste rühma saate kasutada varukoopiana. Saate eksporditud andmeid ka installide vahel kopeerida. Aruandekoostur sisaldab viidatud fondilaade ja dimensioonigruppe koos koosteüksuste grupiga.

1. Klõpsake aruandekoosturi menüüs **Ettevõte** valikut **Koosteüksuste grupid**.
2. Dialoogiaknas **Koosteüksuse** grupid valige ekspordimiseks koosteüksuse grupp ja seejärel klõpsake käsku **Ekspordi**.
3. Valige dialoogiboksist **Eksport** eksporditavad aruande definitsioonid.

    - Kõigi oma aruandedefinitsioonide ja nendega seotud koosteplokkide eksportimiseks klõpsake käsku **Vali kõik**.
    - Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite eksportimiseks klõpsake vastavat vahekaarti ja valige eksporditavad üksused. Vahekaardil mitme üksuse valimiseks vajutage ja hoidke all klahvi Ctrl.

    > [!NOTE]
    > Eksporditavate aruannete valimisel valitakse nendega seotud read, veerud, puud ja dimensioonikogumid.

4. Kui olete eksporditavate üksuste valimise lõpetanud, klõpsake käsku **Ekspordi**.
5. Valige dialoogiboksist **Salvesta nimega** koht, kuhu koosteüksuste grupp eksportida.
6.  **Sisestage faili** nimi väljale Faili nimi. Aruandekoostur lisab automaatselt failinime laiendi .tdbx.
7. Klõpsake nuppu **Salvesta**. Koosteüksuste grupp salvestatakse määratud asukohta.

### <a name="import-a-building-block-group"></a> Koosteüksuste grupi importimine

Saate koosteüksuste rühma importida olemasolevasse koosteüksuste rühma. Kõik imporditud koosteüksuste grupid säilitavad algsed fondilaadid ja ettevõtteviited ning sisaldavad vastavaid dimensioonikogumeid.

1. Aruandekujundajas klõpsake menüü Ettevõte **käsku** Blokeeritud gruppide **loomine**.
2. Dialoogiboksis Koosteüksuse **grupid** valige koosteüksused, millega soovite koosteüksuse grupi importida, ja seejärel klõpsake käsku **Impordi**.
3. Valige dialoogiboksis **Avamine** imporditav koosteüksuste rühm ning klõpsake seejärel suvandit **Ava**.
4. Valige dialoogiboksist **Import** imporditavad aruande definitsioonid.

    - Kõigi aruandedefinitsioonide ja toetavad koosteüksused importimiseks klõpsake nuppu **Vali kõik**.
    - Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite importimiseks valige imporditavad aruanded, read, veerud, puud või dimensioonikogumid.

5. Kui olete imporditavate üksuste valimise lõpetanud, klõpsake käsku **Impordi**.

### <a name="undo-a-checkout-of-a-building-block"></a>Koosteüksuse väljaregistreerimise tühistamine

Koosteüksuse avamisel pääsevad teised kasutajad selle koosteüksuse juurde kirjutuskaitstud režiimis. Mõnikord unustavad kasutajad koosteüksuse sulgeda või sulevad süsteemi ilma koosteüksust sulgemata. Sel juhul jääb koosteüksus välja registreerituks ja ükski teine kasutaja ei saa seda avada. Sellistel juhtudel saab finantsaruandluse administraator kasutada dialoogiboksi **Väljaregistreeritud üksused** koosteüksuste sisseregistreerimiseks, mille kasutajad on jätnud väljaregistreeritud olekusse.

> [!NOTE]
> Teil peab olema administraatori roll, et koosteüksusi dialoogiboksi **Välja registreeritud üksused** kasutades registreerida.

1. Aruandekujundaja menüü Tööriistad käsku **Välja** registreeritud. **·**
2. Dialoogiaknas **Välja registreeritud** üksused valige suvand **Kuva üksused kõikidelt kasutajatelt**. Loendit värskendatakse ning see kuvab kõik välja registreeritud koosteüksused ja kasutajad, kes need välja on registreerinud.
3. Valige kooste blokeerida ja seejärel klõpsake Tühista **väljaregistreerimine**.
4. Klõpsake koosteüksuse registreerimiseks suvandit **Jah**.

## <a name="additional-resources"></a>Lisaressursid

[Finantsaruandlus](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
