---
title: Finantsaruande komponendid
description: "Selles artiklis kirjeldatakse, kuidas aruande definitsiooni komponente (koosteüksusi) finantsaruandluses kasutatakse. Nende koosteüksuste hulka kuuluvad readefinitsioonid, veerudefinitsioonid ja aruandluspuu definitsioonid. Artikkel selgitab, kuidas koosteüksusi korraldada ja lukustada ning kuidas koosteüksuste gruppidega töötada."
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
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59071
ms.assetid: a201cfcb-1672-45f6-897d-2db2dd181d9a
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: fb857a16f159d28acb129beaf51d2241391b103d
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="financial-report-components"></a>Finantsaruande komponendid

[!include[banner](../includes/banner.md)]


Selles artiklis kirjeldatakse, kuidas aruande definitsiooni komponente (koosteüksusi) finantsaruandluses kasutatakse. Nende koosteüksuste hulka kuuluvad readefinitsioonid, veerudefinitsioonid ja aruandluspuu definitsioonid. Artikkel selgitab, kuidas koosteüksusi korraldada ja lukustada ning kuidas koosteüksuste gruppidega töötada. 

Finantsaruannete koosturi ülesehituse filosoofia on suunatud teabe jagamisele vähimateks osadeks ehk koosteüksusteks ja siis nende osade segamine ja sobitamine vajalikul viisil. Seetõttu on teie aruande vormindamine finantsandmetest eraldi ja saate muuta aruande ülesehitust, muutmata finantsandmeid oma Microsoft Dynamics ERP süsteemis. Selle koosteüksuste lähenemisviisi abil saate vajalike aruannete loomiseks kombineerida teksti, summasid ja arvutusi. Lisaks toetab selline paindlikkus loovust, lihtsustades teil oma tegevuse vaatamist mitmesugusel viisil. Aruande definitsiooni üksikud koosteüksused sarnanevad kolmemõõtmelise arvutustabeliga, kuid on võimsamad. Aruande definitsioon määrab aruande puhul kasutatava readefinitsiooni, veeru definitsiooni ja valikulise aruandluspuu definitsiooni. See hõlmab ka teavet selle kohta, kuhu loodud aruanne salvestada ja kuidas seda vormindada. Paremaks korduvaks kasutamiseks ja jagamiseks saate luua koosteüksuste grupi, mis on olemasoleva aruande definitsioonide, readefinitsioonide, veeru definitsioonide, aruandluspuu definitsioonide ja dimensioonikogumite kollektsioon, mis on ettevõttega seotud.

## <a name="building-blocks-of-a-report"></a> Aruande koosteüksused
| Koosteüksus            | Kirjeldus                                                                                                                                                                                                                                                                              | Lisateave                                                                                                 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Rea definitsioon            | Readefinitsioon määratleb kirjeldavad read (näiteks palga või müügi) aruandel. See loetleb ka segmendi väärtused või dimensioonid, mis sisaldavad iga reaüksuse väärtusi, ja hõlmab rea vormindamist ning arvutusi.                                                    | [Readefinitsioonid](row-definitions-financial-reporting.md)                       |
| Veeru määratlus         | Veeru definitsioon määratleb finantsdimensioonidest andmete ekstraktimisel kasutatava perioodi. See hõlmab ka veeru vormindamist ja arvutusi.                                                                                                                                 | [Veeru definitsioonid](column-definitions-financial-reports.md)         |
| Aruandluspuu definitsioon | Aruandluspuu definitsioon sarnaneb organisatsiooni skeemiga. See sisaldab üksikuid aruandlusüksusi, mis tähistavad diagrammi igat välja. Üksusteks võivad olla kas finantsandmete üksikud osakonnad või kõrgema taseme üksused, mis koondavad muude aruandlusüksuste andmeid. | [Aruandluspuu definitsioonid](financial-reporting-tree-definitions.md) |
| Aruande definitsioon         | Aruande definitsioon kasutab aruande loomiseks readefinitsiooni, veeru definitsiooni ja valikulist aruandluspuu definitsiooni. See sisaldab ka täiendavaid suvandeid ja sätteid, mida saab aruande kohandamiseks kasutada.                                                                    | [Aruande definitsioon](design-financial-report-definitions.md)                  |

Kui te pole varem aruandeid koostanud, võib olla mõistlik kasutada aruandeviisardit kiireks aruande definitsiooni loomiseks, mida saate hiljem kohandada. Kui teil on aruannete koostamisel kogemusi ja soovite paindlikumat aruande ülesehitust, saate uue aruande definitsiooni loomiseks kombineerida uusi või olemasolevaid koosteüksusi. Kvaliteetsete aruannete loomiseks ei pea teil olema kõigist saadaolevatest aruande definitsiooni suvanditest täielikku ülevaadet. Muutudes aruannete kujundamises kogenumaks saate täpsemate funktsioonide kasutamiseks oma aruande definitsioone laiendada. Pärast põhiaruande loomist saate aruande definitsiooni ja selle mis tahes koosteüksusi kohandada.

## <a name="organize-the-building-blocks"></a>Koosteüksuste korraldamine
Kasutage aruande kujundajas koosteüksuste korraldamiseks kaustu. Kõik kaustad on omased neis sisalduva koosteüksuse tüübile. Näiteks asuvad kõik readefinitsioone sisaldavad kaustad aruandekoosturi paanil **Readefinitsioonid**.

### <a name="create-a-folder"></a>Kausta loomine

1.  Valige aruande kujundajas navigeerimispaanil korraldatava koosteüksuse tüüp. Näiteks readefinitsiooni sortimiseks klõpsake suvandit **Readefinitsioonid**.
2.  Valige navigeerimispaanil olemasolev kaust, mille alla luuakse uus kaust ja seejärel tehke üks järgmistest toimingutest.
    -   Paremklõpsake põhikausta ja klõpsake siis valikut **Uus kaust**.
    -   Valige põhikaust, klõpsake valikut **Fail** ja seejärel klõpsake valikut **Uus kaust**.

3.  Uue kausta kuvamisel sisestage uue kausta nimi ja vajutage siis sisestusklahvi.

## <a name="lock-a-building-block"></a> Koosteüksuse lukustamine
Koosteüksuse lukustamiseks ja kaitsmiseks saab luua parooli. Sel viisil saate lisada aruande komponenti turvalisuse taseme, turvamata kogu süsteemi. Parool võib kaitsta koosteüksuse teavet, mis on oluline teie kuulõpu aruandeprotsessi jaoks. Koosteüksuse saab lukustada igasuguses rollis kasutaja. Kuid teistel kasutajatel on alati juurdepääs lukustatud komponendi kirjutuskaitstud versioonile. Kasutajad saavad lukustatud komponenti avada, muuta ja uue nimega salvestada. Administraatori rolliga kasutajal on lukustatud koosteüksusele alati juurdepääs ja ta saab seda muuta.
1.  Avage aruande kujundajas lukustatav aruande komponent, näiteks readefinitsioon, veeru definitsioon, aruande definitsioon või aruandluspuu definitsioon.
2.  Klõpsake menüüs **Tööriistad** valikut **Kaitse / vabasta kaitse**. Võite klõpsata ka tööriistaribal olevat ikooni **Kaitse / vabasta kaitse** (lukustamise ikoon).
3.  Sisestage dialoogiboksi **Kaitse** parool ja kinnitage see ning klõpsake siis nuppu **OK**. Avatud koosteüksuse lukustamisel tõstetakse lukuikoon tööriistaribal esile.

Lukustatud koosteüksuse avamiseks avage koosteüksus ja seejärel klõpsake tööriistaribal ikooni **Kaitse/vabasta kaitse**. Teine võimalus on klõpsata menüüs **Tööriistad** valikut **Vabasta kaitse**.

## <a name="building-block-groups"></a>Koosteüksuste grupid

Koosteüksused on aruande puhul loodavad readefinitsioonid, veeru definitsioonid, aruandluspuu definitsioonid ja aruande definitsioonid. Koosteüksuste grupid on ettevõttega seotud definitsioonide ja dimensioonikogumite kogud. Koosteüksuste grupid võivad olla ettevõttepõhised või mitu ettevõtet võivad sama koosteüksuste kogumit jagada. Kui mõnel ettevõtetest on teistsugune kontoplaan, võite kasutada iga ettevõtte puhul erinevat koosteüksuste gruppi. Teise võimalusena võib anda kõigile koosteüksustele nime, mis kajastab ettevõtet, millega need sobivad.
### <a name="create-a-building-block-group"></a>Koosteüksuste grupi loomine

1.  Klõpsake aruandekoosturi menüüs **Ettevõte** valikut **Koosteüksuste grupid**.
2.  Klõpsake dialoogiboksis **Koosteüksuste grupid** valikut **Uus**.
3.  Sisestage koosteüksuste grupi kordumatu nimi ja kirjeldus. Iga väli võib sisaldada kuni 256 märki. (See number sisaldab tühikuid.)
4.  Uue koosteüksuste grupi loomiseks klõpsake nuppu **OK**.

### <a name="assign-a-building-block-group"></a>Koosteüksuste grupi määramine

Pärast üksuste grupi loomist tuleb määrata see vähemalt ühele ettevõttele. Seejärel saate luua aruande, rea, veeru ja aruandluspuu definitsioonid ja need koosteüksuste gruppi salvestada. Enne järgmise protseduuri alustamist peate kõik koosteüksused sulgema.
1.  Klõpsake aruande kujundaja menüüs **Ettevõte** suvandit **Ettevõtted**.
2.  Valige dialoogiboksis **Ettevõtted** ettevõte, millele koosteüksuste grupi määrate.
3.  Klõpsake käsku **Muuda**.
4.  Valige dialoogiboksi **Ettevõtte muutmine** väljalt **Koosteüksuste grupp** ettevõttele määratav koosteüksuste grupp või klõpsake uue koosteüksuste grupi loomiseks suvandit **Uus**.
5.  Koosteüksuste grupi määramiseks klõpsake nuppu **OK**.
6.  Klõpsake käsku **Sule** dialoogiboksi **Ettevõtted** sulgemiseks. Teie valitud koosteüksuste grupp määratakse nüüd ettevõttele. Nüüd kuuluvad kõik loodud uued readefinitsioonid, veeru definitsioonid jm sellele ettevõttele määratud koosteüksuste gruppi. Saate importida ka faili .TDBX või esitada aruande teisest süsteemist.

### <a name="view-a-building-block-group"></a> Koosteüksuste grupi kuvamine

Pärast koosteüksuste grupi loomist ja kasutusele võtmist saate vaadata kõiki sellele määratud koosteüksusi. Samuti saate koosteüksuste gruppi eksportida või importida ja koosteüksuste gruppidele täiendavat hooldust teha.
1.  Klõpsake aruande kujundaja menüüs **Ettevõte** suvandit **Koosteüksuste grupid**.
2.  Valige dialoogiboksist **Koosteüksuste grupid** kuvatav koosteüksus.
3.  Klõpsake käsku **Kuva** dialoogiboksi **Koosteüksuste grupi kuvamine** avamiseks, kus saate koosteüksuste grupi sisu kuvada.
4.  Dialoogibokside sulgemiseks klõpsake käsku **Sule**.

### <a name="save-a-building-block-group-under-a-new-name"></a>Koosteüksuste grupi salvestamine uue nimega

Saate olemasoleva koosteüksuste grupi uue nimega salvestada. Seejärel saate uut koosteüksuste gruppi muuta ilma algset koosteüksuste gruppi muutmata.
1.  Klõpsake aruande kujundaja menüüs **Ettevõte** suvandit **Koosteüksuste grupid**.
2.  Valige dialoogiboksist **Koosteüksuste grupid** uue nimega salvestatav koosteüksuste grupp.
3.  Klõpsake käsku **Salvesta nimega**.
4.  Sisestage koosteüksuste grupi uus nimi ja kirjeldus.
5.  Klõpsake nupul **OK**. Uus koosteüksuste grupp kuvatakse dialoogiboksis **Koosteüksuste grupid**.

### <a name="export-a-building-block-group"></a> Koosteüksuste grupi eksportimine

Saate koosteüksuste grupi või selle kindla aruande koosteüksused eksportida. Eksporditud koosteüksuste gruppi saab kasutada varundamiseks. Saate eksporditud andmeid ka koosteüksuse gruppide või rakenduse Dynamics 365 for Operations seadmete vahel kopeerida. Aruandekoostur sisaldab viidatud fondilaade ja dimensioongruppe koos koosteüksuste grupiga.
1.  Klõpsake aruande kujundaja menüüs **Ettevõte** suvandit **Koosteüksuste grupid**.
2.  Valige dialoogiboksist **Koosteüksuste grupid** eksporditav koosteüksuste grupp ja klõpsake seejärel käsku **Ekspordi**.
3.  Valige dialoogiboksist **Eksport** eksporditavad aruande definitsioonid.
    -   Kõikide aruande definitsioonide ja seotud koosteüksuste eksportimiseks klõpsake suvandit **Vali kõik**.
    -   Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite eksportimiseks klõpsake vastavat vahekaarti ja valige eksporditavad üksused. Vahekaardil mitme üksuse valimiseks vajutage ja hoidke all klahvi Ctrl. **Märkus.** Eksporditavate aruannete valimisel valitakse seotud read, veerud, puud ja dimensioonikogumid.

4.  Kui olete eksporditavate üksuste valimise lõpetanud, klõpsake käsku **Ekspordi**.
5.  Valige dialoogiboksist **Salvesta nimega** koht, kuhu koosteüksuste grupp eksportida.
6.  Sisestage faili nimi väljale **Faili nimi**. Aruandekoostur lisab automaatselt failinime laiendi .tdbx.
7.  Klõpsake nuppu **Salvesta**. Koosteüksuste grupp salvestatakse määratud asukohta.

### <a name="import-a-building-block-group"></a> Koosteüksuste grupi importimine

Saate importida koosteüksuste grupi olemasolevasse koosteüksuste gruppi või luua andmetele uue koosteüksuste grupi. Kõik imporditud koosteüksuste grupid säilitavad algsed fondilaadid ja ettevõtteviited ning sisaldavad vastavaid dimensioonikogumeid.
1.  Klõpsake aruande kujundaja menüüs **Ettevõte** suvandit **Koosteüksuste grupid**.
2.  Valige dialoogiboksist **Koosteüksuste grupid** koosteüksus, kuhu koosteüksuste grupp importida ja klõpsake seejärel käsku **Impordi**.
3.  Valige dialoogiboksist **Avatud** imporditav koosteüksuste grupp ja seejärel klõpsake suvandit **Avatud**.
4.  Valige dialoogiboksist **Import** imporditavad aruande definitsioonid.
    -   Kõikide aruande definitsioonide ja seotud koosteüksuste importimiseks klõpsake valikut **Vali kõik**.
    -   Kindlate aruannete, ridade, veergude, puude või dimensioonikogumite importimiseks valige imporditavad aruanded, read, veerud, puud või dimensioonikogumid.

5.  Kui olete imporditavate üksuste valimise lõpetanud, klõpsake käsku **Impordi**.

### <a name="undo-a-checkout-of-a-building-block"></a>Koosteüksuse väljaregistreerimise tühistamine

Koosteüksuse avamisel pääsevad teised kasutajad selle koosteüksuse juurde kirjutuskaitstud režiimis. Mõnikord unustavad kasutajad koosteüksuse sulgeda või sulevad süsteemi ilma koosteüksust sulgemata. Sel juhul jääb koosteüksus välja registreerituks ja ükski teine kasutaja ei saa seda avada. Sellistel juhtudel saab finantsaruandluse administraator kasutada dialoogiboksi **Väljaregistreeritud üksused** koosteüksuste sisseregistreerimiseks, mille kasutajad on jätnud väljaregistreeritud olekusse. **Märkus.** Koosteüksuste sisseregistreerimiseks dialoogiboksist **Väljaregistreeritud üksused** peab teil olema administraatori roll.
1.  Valige aruande kujundaja menüüst **Tööriistad** suvand **Väljaregistreeritud üksused**.
2.  Valige dialoogiboksist **Väljaregistreeritud üksused** suvand **Kuva kõikide kasutajate üksused**. Loendit värskendatakse kuvama kõiki väljaregistreeritud koosteüksusi ja need välja registreerinud kasutajaid.
3.  Valige koosteüksus ja seejärel klõpsake suvandit **Tühista väljaregistreerimine**.
4.  Koosteüksuse sisseregistreerimiseks klõpsake **Jah**.

# <a name="see-also"></a>Vt ka

[Finantsaruandlus](financial-reporting-intro.md)




