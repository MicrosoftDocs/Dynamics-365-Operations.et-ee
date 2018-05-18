---
title: "Andmete importimis- ja eksportimistööd"
description: "Kasutage andmeimpordi ja -ekspordi tööde jaoks andmehalduse tööruumi."
author: Sunil-Garg
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fc47f6cd9cfe4a850e0959bf89da086ca82f3b69
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="data-import-and-export-jobs"></a>Andmete importimis- ja eksportimistööd

[!include [banner](../includes/banner.md)]

Andmeimpordi ja -ekspordi tööde jaoks rakenduses Microsoft Dynamics 365 for Finance and Operations kasutatakse tööruumi **Andmehaldus**. Vaikimisi loob andmeimpordi ja -ekspordi protsess igale sihtandmebaasi üksusele koondamistabeli. Koondamistabelid võimaldavad andmeid enne teisaldamist kontrollida, puhastada või teisendada.

> [!NOTE]
> Siin teemas eeldatakse, et olete [andmeüksustega](data-entities.md) tuttav.

## <a name="data-importexport-process"></a>Andmete importimis-/eksportimisprotsess
Siin on toimingud andmete importimiseks või eksportimiseks.

1. Looge impordi- või eksporditöö, kus tuleb teha järgmised toimingud.

    - Määratlege projekti kategooria.
    - Näidake ära imporditavad või eksporditavad üksused.
    - Määrake töö andmevorming.
    - Järjestage üksused nii, et neid töödeldaks loogiliste rühmadena ja mõistlikus järjekorras.
    - Määrale, kas kasutada koondamistabeleid.

2. Kontrollige, kas lähte- ja sihtandmed on õigesti vastendatud.
3. Kontrollige impordi- või eksporditöö turvalisust.
4. Käivitage impordi- või eksporditöö.
5. Kontrollige, et töö toimus õigesti, vaadates üle töö ajaloo.
6. Puhastage koondamistabelid.

Selle teema ülejäänud osades on lisateave iga protsessi etapi kohta.

> [!NOTE]
> Andmete importimise/eksportimise vormi värskendamiseks ja uusima edenemise kuvamiseks kasutage vormi värskendamise ikooni. Brauseritasemel värskendamine pole soovitatav, kuna see katkestab kõik impordi- või eksporditööd, mida ei käitata partiidena.

## <a name="create-an-import-or-export-job"></a>Impordi- või eksporditöö loomine
Andmete impordi- või eksporditöö saab käitada ühe korra või palju kordi.

### <a name="define-the-project-category"></a>Projekti kategooria määratlemine
Soovitame võtta aega, et valida impordi- või eksporditööle sobiv projektikategooria. Projektikategooriate abil saate seotud töid hallata.

### <a name="identify-the-entities-to-import-or-export"></a>Imporditavate või eksporditavate üksuste tähistamine
Saate lisada impordi- või eksporditööle konkreetseid üksusi või valida rakendamiseks malli. Mallid täidavad töö üksuste loendiga. Valik **Rakenda mall** on saadaval, kui olete tööle nime andnud ja selle salvestanud.

### <a name="set-the-data-format-for-the-job"></a>Töö andmevormingu määramine
Kui valite üksuse, peate valima eksporditavate või imporditavate andmete vormingu. Vorminguid saab määratleda paani **Andmeallikate seadistus** kaudu. Lähteandmete vorming on **tüübi**, **failivormingu**, **reaeraldaja** ja **veerueraldaja** kombinatsioon. On ka muid atribuute, kuid need on kõige olulisemad. Järgmises tabelis on toodud kehtivad kombinatsioonid.

| **Failivorming**        | **Rea-/veerueraldaja**                   | **XML-i laad**             |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-Pole-                     |
| XML                    | \-Pole-                                      | XML-element XML-atribuut |
| Eraldatud, fikseeritud laius | Koma, semikoolon, vahekaart, vertikaalriba, koolon | \-Pole-                     |



### <a name="sequence-the-entities"></a>Üksuste järjestamine
Üksusi saab järjestada andmemallis või impordi- ja eksporditöödes. Kui käivitate mitut andmeüksust sisaldava töö, peate veenduma, et andmeüksused oleksid õiges järjestuses. Üksused järjestatakse peamiselt nii, et saaksite käsitleda funktsionaalseid sõltuvusi üksuste vahel. Kui üksustel pole ühtegi funktsionaalset sõltuvust, saab need plaanida paralleelseks impordiks või ekspordiks.

#### <a name="execution-units-levels-and-sequences"></a>Käivitamise ühikud, tasemed ja järjestused
Üksuse käivitamise ühik, tase käivitamise ühikus ja järjekord aitavad juhtida andmete eksportimise või importimise järjekorda.

- Erinevate käivitamise ühikute üksusi töödeldakse paralleelselt.
- Igas käivitamise ühikus töödeldakse üksusi paralleelselt, kui neil on sama tase.
- Igal tasemel töödeldakse üksusi nende järjekorranumbri alusel sellel tasemel.
- Kui üks tase on töödeldud, töödeldakse järgmine tase.

#### <a name="resequencing"></a>Ümberjärjestamine
Üksusi võib olla vaja ümber järjestada järgmistes olukordades.

- Kui kõigi muudatuste jaoks kasutatakse ainult ühte andmetööd, võite kasutada ümberjärjestamise valikuid terve töö läbiviimise aja optimeerimiseks. Nendel juhtudel võite kasutada käivitamise ühikut mooduli tähistamiseks, taset mooduli funktsiooniala tähistamiseks ja järjekorda üksuse tähistamiseks. Selle lähenemisega saate töötada moodulite lõikes paralleelselt, kuid mooduli sees ikka järjekorras. Tagamaks, et paralleelsed toimingud õnnestuksid, tuleb arvestada kõiki sõltuvusi.
- Kui kasutatakse mitut andmetööd (näiteks ühte tööd iga mooduli jaoks), võite optimaalseks läbiviimiseks kasutada järjestust, mis mõjutab üksuste taset ja järjekorda.
- Kui sõltuvusi polegi, võite maksimaalseks optimeerimiseks järjestada üksused erinevatel käivitamise ühikutel.

Menüü **Ümberjärjestamine** on saadaval, kui valitud on mitu üksust. Ümber saab järjestada käivitamise ühiku, taseme või järjekorravalikute alusel. Saate määrata vahemiku valitud üksuste ümberjärjestamiseks. Igale üksusele valitud ühikut, taset ja/või järjekorranumbrit muudetakse määratud vahemiku võrra.

#### <a name="sorting"></a>Sortimine
Valikut **Sortimisalus:** saab kasutada üksuste loendi vaatamiseks järjekorras.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Kontrollimine, kas lähte- ja sihtandmed on õigesti vastendatud
Vastendamine on funktsioon, mida rakendatakse nii impordi- kui ka eksporditööde puhul.

- Imporditöö kontekstis kirjeldab vastendus, millistest lähtefaili veergudest saavad koondamistabeli veerud. Seetõttu saab süsteem määratleda, millised lähtefaili veeruandmed tuleb kopeerida millisesse koondamistabeli veergu.
- Eksporditöö kontekstis kirjeldab vastendus, millistest koondamistabeli (st allika) veergudest saavad sihtfaili veerud.

Kui koondamistabeli ja faili veergude nimed ühtivad, loob süsteem nimede põhjal automaatselt vastenduse. Kuid kui nimed erinevad, ei vastendata veerge automaatselt. Sellistel juhtudel tuleb teha vastendamine, tehes valiku **Kuva kaart** andmetöö üksusel.

Vastendamisvaateid on kaks: **Vastendamise visualiseering**, mis on vaikevaade, ja **Vastendamise üksikasjad**. Punane tärn (\*) tähistab üksuse kohustuslikke välju. Need väljad tuleb vastendada, enne kui saate üksusega töötada. Teiste väljade vastendusi saab üksusega töötades soovi kohaselt tühistada. Välja vastenduse tühistamiseks valige väli veerust **Üksus** või veerust **Allikas** ja valige siis **Kustuta valik**. Valige **Salvesta** muudatuste salvestamiseks ja sulgege siis leht projekti juurde naasmiseks. Sama protsessi abil saab redigeerida välja vastendust lähtetabelist koondamistabelisse pärast importimist.

Lehel saab luua vastenduse, valides **Allika vastendamise loomine**. Loodud vastendus toimib nagu automaatne vastendus. Seega tuleb vastendamata väljad käsitsi vastendada.

![Andmetüüpide vastendamine](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>Impordi- või eksporditöö turvalisuse kontrollimine
Juurdepääsu tööruumile **Andmehaldus** saab piirata, et mitte-administraatorist kasutajad pääseksid juurde ainult konkreetsetele andmetöödele. Juurdepääs andmetööle tähendab täielikku juurdepääsu selle töö läbiviimise ajaloole ja juurdepääsu koondamistabelitele. Seetõttu tuleb veenduda, et andmetöö loomisel oleksid paigas sobivad juurdepääsu kontrollimismehhanismid.

### <a name="secure-a-job-by-roles-and-users"></a>Töö kaitsmine rollide ja kasutajatega
Menüü **Rakendatavad rollid** abil saate piirata töö ühe või mitme turberolliga. Ainult nende rollidega kasutajad pääsevad tööle juurde.

Samuti saab töö teha kättesaadavaks ainult konkreetsetele kasutajatele. Kui töö turve põhineb kasutajatel, mitte rollidel, on kontroll suurem, kui ühele rollile on määratud mitu kasutajat.

### <a name="secure-a-job-by-legal-entity"></a>Töö turve juriidilise isiku alusel
Andmetööd on olemuselt globaalsed. Seetõttu, kui juriidilises isikus loodi andmetöö ja seda kasutati seal, on see töö süsteemi teistes juriidilistes isikutes näha. Mõnes rakenduse stsenaariumis võib see vaikekäitumine eelistatud olla. Näiteks organisatsioonis, kus arveid imporditakse andmeüksuste abil, võib olla tsentraalne arveid töötlev töörühm, mis vastutab kõigi organisatsiooni divisjonide arvetel olevate vigade eest. Selles stsenaariumis on abiks, kui tsentraalne arveid töötlev töörühm pääseb juurde kõigi juriidiliste isikute arvete imporditöödele. Seetõttu vastab vaikekäitumine juriidilise isiku vaatepunktist vajadustele.

Kuid organisatsioon võib soovida, et arvete töötlemise töörühmad oleksid juriidilise isiku põhised. Sel juhul peaks juriidilise isiku töörühmal olema juurdepääs ainult oma juriidilise isiku arve imporditööle. Selle nõude täitmiseks võite konfigureerida juriidilise isiku põhise juurdepääsukontrolli andmetöödele, kasutades andmetöös menüüd **Kohaldatavad juriidilised isikud**. Pärast konfigureerimist näevad kasutajad ainult töid, mis on saadaval selles juriidilises isikus, kuhu nad parajasti on sisse logitud. Teise juriidilise isiku tööde vaatamiseks peavad kasutajad minema sellesse juriidilisse isikusse.

Töö saab kaitsta korraga rollide, kasutajate ja juriidiliste isikute kaudu.

## <a name="run-the-import-or-export-job"></a>Impordi- või eksporditöö käivitamine
Töö saab käivitada ühe korra, valides pärast töö määratlemist nupu **Impordi** või **Ekspordi**. Korduva töö seadistamiseks valige **Korduva andmetöö loomine**.

## <a name="validate-that-the-job-ran-as-expected"></a>Kontrollimine, et töö toimus õigesti
Töö ajalugu on tõrkeotsinguks ja uurimiseks saadaval nii impordi- kui ka eksporditööde puhul. Varasemad töötsüklid on korraldatud ajavahemike alusel.

![Töö ajaloo vahemikud](./media/dixf-job-history.md.png)

Iga töötsükli puhul kuvatakse järgmised andmed.

- Käivitamise üksikasjad
- Käivituslogi

Käivitamise üksikasjad näitavad iga töös töödeldud andmeüksuse olekut. Seetõttu leiate kiiresti järgmise teabe.

- Milliseid üksusi töödeldi
- Üksuse puhul – mitu kirjet töödeldi edukalt ja mitu ebaõnnestus
- Iga üksuse koondamiskirjed

Koondamisandmed saab laadida eksporditööde puhul alla failina või impordi- ja eksporditööde puhul paketina.

Käivitamise üksikasjadest saab avada ka käivituslogi.

## <a name="clean-up-the-staging-tables"></a>Koondamistabelite puhastamine
Koondamistabelid saab puhastada, kasutades funktsiooni **Koondamise puhastamine** tööruumis **Andmehaldus**. Järgmiste valikute abil saate valida, millised kirjed millisest koondamistabelist kustutada tuleks.

- **Üksus** – kui antud on ainult üksus, kustutatakse kõik selle üksuse kirjed koondamistabelist. Selle valiku abil saate kustutada kõik üksuse andmed kõigi andmeprojektide ja kõigi tööde lõikes.
- **Töö ID** – kui antud on ainult töö ID, kustutatakse kõigi üksuste kõik kirjed valitud töös vastavatest koondamistabelitest.
- **Andmeprojektid** – kui valitud on ainult andmeprojekt, kustutatakse valitud andmeprojekti kõigi üksuste kõik kirjed kõigi tööde lõikes.

Kustutatava kirjekogumi täiendavaks piiramiseks saab valikuid ka kombineerida.

