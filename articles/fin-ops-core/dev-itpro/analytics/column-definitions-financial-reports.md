---
title: Veerudefinitsioonid finantsaruannetes
description: See artikkel käsitleb veerudefinitsioone. Veeru määratlus on aruande komponent, mis määrab aruande veergude sisu.
author: ShylaThompson
manager: AnnBe
ms.date: 10/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 820604fac96f5c86be3f7206ca88b3eb1fc6c32a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093105"
---
# <a name="column-definitions-in-financial-reports"></a>Veerudefinitsioonid finantsaruannetes

[!include [banner](../includes/banner.md)]

See artikkel käsitleb veerudefinitsioone. Veerudefinitsioon on aruande komponent (koosteüksus), mis määrab aruande veergude sisu. Nagu readefinitsioone, saab ka peamisi veerudefinitsioone kasutada mitmes aruandes.

## <a name="create-and-modify-a-column-definition"></a>Veeru definitsiooni loomine ja muutmine

Veeru definitsioon võib sisaldada 2 kuni 255 veergu.

### <a name="create-a-column-definition"></a>Veeru definitsiooni loomine

1. Klõpsake aruande kujundajas navigeerimispaanil suvandit **Veeru definitsioonid**.
2. Klõpsake menüüs **Fail** suvandit **Uus** ja seejärel klõpsake suvandit **Veeru definitsioon**.
3. Lisage veeru definitsiooni sisu.

### <a name="open-a-column-definition"></a>Veeru definitsiooni avamine

1. Klõpsake aruande kujundajas navigeerimispaanil suvandit **Veeru definitsioonid**.
2. Veeru definitsiooni avamiseks topeltklõpsake seda.

### <a name="add-a-column-to-a-column-definition"></a>Veeru lisamine veerudefinitsiooni

1. Klõpsake aruande kujundajas suvandit **Veeru definitsioonid** ja seejärel avage muutmiseks veeru definitsioon.
2. Valige veerg, kuhu tuleks lisada uus veerg.
3. Klõpsake menüüs **Redigeerimine** suvandit **Lisa veerg**. Uus veerg ilmub valitud veerust vasakule.

### <a name="delete-a-column-from-a-column-definition"></a>Veeru kustutamine veerudefinitsioonist

1. Klõpsake aruandekoosturis suvandit **Veerudefinitsioonid** ja seejärel avage muutmiseks veerudefinitsioon.
2. Valige kustutatav veerg.
3. Klõpsake menüüs **Redigeeri** suvandit **Kustuta veerg**.

## <a name="contents-of-a-column-definition"></a>Veerudefinitsiooni sisu
Veeru definitsioon sisaldab järgmist teavet.

- Readefinitsiooni kirjelduste veerg
- Summa veerud, milles kuvatakse veeru definitsiooni muudel andmetele põhinevate finantsandmete või arvutuste andmed
- Vormingu veerud
- Atribuudi veerud

See teave kuvatakse veeru definitsiooni järgmistes alades.

- Veeru definitsiooni päiste ala sisaldab aruandes kuvatavat päiseteksti ja vormingut. Päis saab rakenduda üksikule andmeveerule, laieneda üle mitme veeru või rakenduda veergudele tingimuslikkuse alusel. Veeru määratlus võib sisaldada nii palju veerupäise ridasid, kui vajate.

    > [!NOTE]
    > Veerupäised rakenduvad igale aruande andmeveerule. Aruande päised rakenduvad kogu aruandele. Saate määratleda aruande päiseid aruande definitsiooni vahekaardil **Päised ja jalused**.

- Veeru üksikasjade read on veeru definitsioonis päiseridade all olevad read. Veeru üksikasjade read määratlevad aruandesse kaasatava teabe. Järgmises tabelis loetletakse ja kirjeldatakse veeru üksikasjade ridu.

    | Veeru üksikasjade rea nimi                                                | Kirjeldus                                                                                            |
    |-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
    | Veeru tüüp                                                           | (Nõutav) Veeru andmete tüübi määramine.                                                     |
    | Konteerimiskood/atribuudi kategooria                                          | Tüüpide **FD** ja **ATTR** veergude finantsandmete teabe määratlemine.                       |
    | Rahandusaasta perioodi hõlmatud perioodid                                    | Tüübi **FD** veergude finantsandmete teabe määratlemine.                                     |
    | Valem                                                               | Arvutusvalemi määramine tüübiga **CALC** veergude puhul.                                        |
    | Veeru laius Lisatühikud enne veergu Vormingu alistamine Prindi kontrollkood | Erivormingu suvandite määramine.                                                                        |
    | Veeru piirangud                                                   | Andmete piiramine.                                                                                         |
    | Aruandlusüksus                                                        | Veeru piiramine nii, et see kuvaks ainult kindla aruandlusüksuse andmeid.                      |
    | Valuuta kuva Valuutafilter                                      | Valuuta vorming.                                                                                       |
    | Dimensioonifilter                                                      | Filtri määramine andmete piiramiseks teatud finantsandmete aruandlusüksustega.                           |
    | Atribuudi filter                                                      | Filtri määramine finantsandmete piiramiseks.                                                       |
    | Alguskuupäev Lõppkuupäev                                                   | Finantsandmete piiramine kindlate kuupäevadega.                                                         |
    | Põhjendus                                                         | Readefinitsioonis määratud kirjelduse teksti vasakjoondamine, keskjoondamine või paremjoondamine. |

## <a name="column-restrictions-in-a-column-definition"></a>Veeru definitsiooni veeru piirangud
Saate kasutada veeru piiranguid määramaks, kuidas veeru definitsioon andmeid kasutab või arvutab. Saate aruandeveeru piirata ka kindlale üksusele või kindlatele kuupäevadele.

> [!NOTE]
> Kood **Veerupiirang** tühistab ükskõik millise readefinitsioonis määratud vastuolulise sätte.

### <a name="column-restrictions-cell"></a>Lahter Veeru piirangud

Lahter **Veeru piirangud** võib sisaldada koode, mis piiravad või peidavad selle veeru puhul teavet, näiteks rea vormingut, üksikasju ja summasid.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Veeru piirangu lisamine veeru definitsioonis

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Topeltklõpsake piiratava veeru puhul lahtrit **Veeru piirangud**.
3. Valige dialoogiboksis **Veeru piirangud** loendist üks või enam koodi ja seejärel klõpsake nuppu **OK**.

### <a name="column-restriction-codes"></a>Veerupiirangu koodid

Järgmises tabelis kirjeldatakse veeru piirangu koode.

| Veeru piirangu kood | Kirjeldus |
|-------------------------|-------------|
| SU                      | Allkriipsu peitmine veeru puhul, mil readefinitsiooni on sisestatud kas allkriipsu käsk (**---**) või topelt-allkriipsu käsk (**===**). Näiteks ei pruugi te soovida protsendiarvutuse loodud summade allakriipsutamist. |
| ST                      | Kogusummade peitmine nii, et veerus kuvatakse ainult üksikasju (nt statistiline veerg). |
| SD                      | Üksikasjade peitmine nii, et veerus kuvatakse ainult read **TOT** ja **CAL** (readefinitsioonist). |
| DR                      | Veeru **FD** summade piiramine deebetsummadega. |
| CR                      | Veeru **FD** summade piiramine kreeditsummadega. |
| ADJ                     | Veeru summade piiramine perioodi korrigeerimissummadega nende summade olemasolul. |
| XAD                     | Veeru summade piiramine nii, et perioodi korrigeerimissummad välistatakse. |
| Plaanitud üleviimine                      | Veeru summade piiramine nii, et kaasatakse ainult sisestatud kanded, kui need kanded on olemas. |
| UPT                     | Veeru summade piiramine nii, et kaasatakse ainult sisestamata kanded, kui need kanded on olemas.<p><strong>Märkus.</strong> Kõik andmepakkujad ei toeta sisestamata kandeid. </p> |

### <a name="restrict-a-column-to-a-reporting-unit"></a>Veeru piiramine aruandlusüksusega

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Topeltklõpsake piiratava veeru puhul lahtrit **Aruandlusüksus**.
3. Valige aruandluspuu dialoogiboksi **Aruandlusüksuse valimine** loendist **Aruandluspuu**.
4. Laiendage või ahendage üksuste loendit, valige aruandlusüksus ja seejärel klõpsake nuppu **OK**.

## <a name="format-column-headers"></a>Veerupäiste vormindamine
Saate lisada, muuta ja kustutada aruande veergude ülaosas olevaid päiseid. Samuti saate konfigureerida tingimusliku laiendamise veerupäiseid veerudefinitsioonide välja **Periood** ja aruande definitsioonide välja **Baasperiood** põhjal. Baasperioodi funktsioon aitab säästa jooksva eelarve aruannete loomisel aega.

### <a name="create-and-manage-column-headers"></a>Veerupäiste loomine ja haldamine

Saate kasutada dialoogiboksi **Veerupäis** aruande veergude ülaosas olevate päiste lisamiseks, muutmiseks ja kustutamiseks. Järgmises tabelis kirjeldatakse dialoogiboksi **Veerupäis** välju.

| Väli                 | Kirjeldus |
|-----------------------|-------------|
| Veerupäise tekst    | See tekst kuvatakse veerupäises. Saate sisestada teksti otse sellele väljale või klõpsata suvandit **Sisesta automaattekst** suvandi valimiseks, mis värskendab veerupäist iga kord aruande loomisel. Mitme automaatteksti koodi lisamiseks klõpsake suvandit **Sisesta automaattekst** uuesti ja seejärel klõpsake loendis muud koodi. |
| Vormingusuvandid        | Vormingu rakendamine veeru päisele, nt kasti või allakriipsutuse. |
| Algusvahemik Lõppvahemik | Veeru või veergude määramine, millele päisetekst rakendub. |
| Põhjendus         | Saate määrata, kuidas tuleks veeru päisetekst joondada veeru või veergude vahemiku puhul, mis on määratud väljadel **Algusvahemik** ja **Lõppvahemik**. |

### <a name="create-a-column-header"></a>Veerupäise loomine

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Topeltklõpsake päise lahtrit.
3. Sisestage veerupäise tekst dialoogiboksi **Veerupäis**. Teise võimalusena saate klõpsata suvandit **Sisesta automaattekst** ja valida suvandi.
4. Valige väljalt **Vormingusuvandid** päise vorming.
5. Sisestage väljale **Algusvahemik** veeru täht, millest alates tuleks veerupäis kuvada. Sisestage väljale **Lõppvahemik** veeru täht, kuni milleni tuleks veerupäis kuvada.
6. Valige suvandi **Joondus** alt, kas veerupäise tekst peaks olema vasakjoondatud, keskjoondatud või paremjoondatud.
7. Klõpsake nupul **OK**.

### <a name="add-a-column-header-row"></a>Veerupäise rea lisamine

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Valige päisereast lahter.
3. Klõpsake menüüs **Redigeerimine** suvandit **Lisa rida**. Uus rida sisestatakse 2. etapis valitud rea kohale.

> [!NOTE]
> Kui teie aruandes on aruande päiseid neli rida või rohkem ja aruanne eksporditakse Exceli töölehele, siis päised kattuvad. Kõigi päiste kuvamiseks aruandes suurendage aruande definitsioonis ülemist veerist.

### <a name="delete-a-column-header-row"></a>Veerupäise rea kustutamine

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Valige päisereal kustutatav lahter.
3. Klõpsake menüüs **Redigeerimine** suvandit **Kustuta rida**.

### <a name="create-an-automatically-generated-header"></a>Automaatselt loodava päise loomine

Aruandekoostur saab veerupäiseid automaatteksti koodide alusel automaatselt luua. Automaatteksti koodid on muutujad, mida värskendatakse iga kord, kui aruanne luuakse. Veerupäis võib sisaldada neid koode varieeruva aruandeteabe, nagu kuupäevade või perioodinumbrite määramiseks. Seetõttu saate kasutada ühte veeru definitsiooni mitme aruande definitsiooni, ajaperioodi ja aruandluspuu puhul. Kuna automaatteksti koodid sõltuvad veeru definitsiooni üksikasjaridade kalendriteabest, toetavad neid ainult veerud **CALC** ja **FD**. Automaatteksti koodi veerupäise lahtris kuvamise viis mõjutab selle teabe ilmet aruandes. Dialoogiboksis **Veerupäis** kuvatakse automaatteksti koodid erinevate tõstudega. Seega kuvatakse tekst aruandes erinevate tõstudega. Näiteks standardses kalendriaastas on koodi **\@CalMonthLong** järgi **7**. kuu vasteks **juuli**. Kui kuu nimi tuleks aruandes suurte tähtedega (näiteks **JUULI**) kuvada, sisestage automaatteksti kood väljale **Veeru päise tekst** suurte tähtedega. Sisestage näiteks **\@CALMONTHLONG**. Võite koode ja teksti kombineerida. Näiteks saate sisestada järgmise päiseteksti: **Periood \@FiscalPeriod-\@FiscalYear alates \@StartDate kuni \@EndDate**. Loodav aruande pealkiri sarnaneb järgmisega: **Periood 1-02 alates 01/01/02 kuni 01/31/02**.

> [!NOTE]
> Osa teksti, nt pika kuupäeva vorming oleneb teie regioonisätetest serveris. Nende sätete muutmiseks klõpsake nuppu **Start**, klõpsake suvandit **Juhtpaneel** ja seejärel klõpsake suvandit **Regioon ja keel**. Järgmises tabelis loetletakse veerupäiste puhul saadaolevad automaatteksti suvandid.


| Automaatteksti suvand ja kood                | Kirjeldus |
|-----------------------------------------|-------------|
| Kuu nimi (@CalMonthLong)              | Veerupäise praeguse kuu nime printimine. Kui otsustate ümardada aruandesummad tuhandike, miljonite või miljarditeni või kui seadistate aruande veeru laiuse vähem kui üheksale märgile, lühendatakse kuu nimi esimese kolme märgini. |
| Lühendatud kuu nimi (@CalMonthShort) | Valitud rahandusperioodi kuu lühendatud nime printimine. |
| Perioodi number (@FiscalPeriod)           | Selle veeru puhul määratud rahandusperioodi numbrilise vormi printimine. Kui veerg hõlmab mitut perioodi, prinditakse vahemiku viimane periood. |
| Perioodi kirjeldus (@FiscalPeriodName)  | Finantsandmetes määratud rahandusperioodi kirjelduse printimine. |
| Rahandusaasta (@FiscalYear)               | Rahandusaasta printimine veeru puhul numbrites. |
| Kalendriaasta (@CalYear)                | Kalendriaasta printimine veeru puhul numbrites. |
| Alguskuupäev (@StartDate)                 | Veeru alguskuupäeva printimine. |
| Lõppkuupäev (@EndDate)                     | Veeru lõppkuupäeva printimine. |
| Üksuse nimi puust (@UnitName)         | Üksuse nime printimine veerupäises veeru piiramisel aruandluspuu kindla üksuseni. |
| Üksuse kirjeldus (@UnitDesc)            | Üksuse kirjelduse printimine veerupäises veeru piiramisel aruandluspuu kindla üksuseni. |
| Konteerimiskood (@BookCode)                   | Veerus määratud konteerimiskoodi printimine. |
| Tühi rida (@Blank)                     | Tühja rea lisamine veerupäises. |

### <a name="create-a-conditional-spanning-header"></a>Tingimusliku laiendamise päise loomine

Tingimusliku laiendamise päised võivad hõlmata mitut konkreetse perioodi andmetel põhinevat veergu. Näiteks kui teil on rahandusaasta eelarve aruanne ja soovite kuvada viimaste kuude tegeliku eelarve koos tulevaste kuude prognoositud eelarvetega, saate aruandepäise automaatseks värskendamiseks kasutada tingimusliku laiendamise päist. Pöörake tingimusliku laienduspäise loomisel tähelepanu järgmistele olukordadele.

- Mis tahes peatamise tingimust (väli **Lõppvahemik**), mis on vastavusse viidud enne alustamise tingimust (väli **Lõppvahemik**), eiratakse. Näiteks veeru B laiendamise tingimus on määratletud järgmiselt: BASE+1 kuni BASE, BASE on veerus C ja BASE+1 on veerus D. Sellisel juhul eiratakse peatamise tingimust veerus C ja päise printimine algab veerust D.
- Kattuvate veerupäiste määramisel kattuvad need aruandesse printimisel. Aruanne luuakse, kuid väljal **Aruande järjekorra olek** kuvatakse järgmine hoiatus: „Väärtust Base kasutavad veerupäised ristuvad teiste veerupäistega ja võivad põhjustada teksti kattumist”. Näiteks päise definitsioon veerus B on B kuni BASE+1 ja päise definitsioon veerus D on BASE+1 kuni F. Sellisel juhul prinditakse päised üksteise peale ja pole loetavad. Väärtuse BASE kasutamisel definitsioonis **Algusvahemik/lõppvahemik** veenduge, et vaatate loodavat aruannet, et näha, kas päised kattuvad.
- Kui määrate väärtuse BASE laiendamise definitsiooni veerus Mitteprinditav (**NP**), eiratakse seda olenemata sellest, mis on veeru definitsioonis määratletud. Põhiolemuselt sarnaneb see stsenaarium veerupäise definitsiooni mitteloomisega.
- Tingimusliku printimise veerude puhul (**P&lt;B**, **P&gt;=B**) toimivad tingimusliku laiendamise päised nagu mis tahes tavaline veerupäise definitsioon. Näiteks kui tingimus on väär, alustavad kõik järgnevad laiendamise tingimuse puhul ühtivad veerud päise printimist.

#### <a name="create-a-conditional-spanning-header"></a>Tingimusliku laiendamise päise loomine

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Topeltklõpsake päise lahtrit.
3. Sisestage veerupäise tekst dialoogiboksi **Veerupäis**. Teise võimalusena saate klõpsata suvandit **Sisesta automaattekst** ja valida suvandi.
4. Valige väljalt **Vormingusuvandid** päise vormingu laad.
5. Määrake periood aruande loomisel määratud baasperioodi suhtes. Sisestage väljadele **Algusvahemik** ja **Lõppvahemik** üks järgmistest väärtustest: **BASE**, **BASE-X** või **BASE+X**, kus X on baasperioodi perioodide arv. Näiteks kui sisestate väärtuse **BASE** väljale **Algusvahemik**, algab tingimusliku laiendamise veeru päisetekst veerupäisest, milles aruande definitsiooni väärtus **Baasperiood** ühtib veeru definitsiooni väärtusega **Periood**. See lõpeb väljal **Lõppvahemik** näidatud veerus. Seega kui laiendamine on BASE kuni M ja aruande definitsiooni suvandi **Baasperiood** väärtus on **4**, algab päis veerust, kus periood on seatud väärtusele **4** ja lõpeb veerus M. Päised lõppevad ja algavad ainult prinditavatelt veergudelt.
6. Valige suvandi **Joondus** alt, kas veerupäise tekst peaks olema vasakjoondatud, keskjoondatud või paremjoondatud.
7. Klõpsake valikut **OK**.

#### <a name="example-of-a-conditional-spanning-header"></a>Tingimusliku laiendamise päise näide

Kasutaja loob dünaamilise kuue kuu eelarve aruande. Kasutaja soovib, et tegelikke andmeid sisaldavatele veergudele prinditaks sõna „Tegelik” ja eelarveprognoose sisaldavatele veergudele prinditaks sõna „Eelarve”. Iga kuu, mil aruannet käitatakse, on üks tegelik veerg rohkem ja üks eelarve veerg vähem. Kuigi kasutaja saab veeru definitsiooni päiste korrigeerimiseks aruande loomisel iga kord käsitsi muuta, otsustab ta luua tingimusliku laiendamise päised, mis loovad päised asjakohastele veergudele iga kord aruande käitamisel automaatselt. Kasutaja avab aruande kujundaja, klõpsab navigeerimispaanil suvandit **Veeru definitsioon** ja avab aruande veeru definitsiooni. Seejärel sisestab kasutaja järgmise teabe. Baasperiood aruande definitsioonis on 4.

|      Vorming         |  A   | B             | C             | D             | E             | R             | G             | H             | Mina             | J             | K             | L             | E             |
|---------------------|------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Päis 1            |      | Tegelik        | Eelarve        |               |               |               |               |               |               |               |               |               |               |
| Päis 2            |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
| Päis 3            |      |               |               |               |               |               |               |               |               |               |               |               |               |
| Veeru tüüp         | DESC | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            | FD            |
| Konteerimiskood/atribuut |      | ACTUAL        | EELARVE2012    | ACTUAL        | EELARVE2012    | ACTUAL        | EELARVE2012    | ACTUAL        | EELARVE2012    | ACTUAL        | EELARVE2012    | ACTUAL        | EELARVE2012    |
| Finantsaasta         |      | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          |
| Periood              |      | 1             | 1             | 2             | 2             | 3             | 3             | 4             | 4             | 5             | 5             | 6             | 6             |
| Kaetud perioodid     |      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      | PERIODIC      |
| Veeru laius        | 30   | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            |
| Printimise juhtelement       |      | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        |

Kasutaja topeltklõpsab veerus B veerupäise lahtrit dialoogiboksi avamiseks suvandit **Veerupäis** ja sisestab järgmise teabe.

| Field              | Väärtus                 |
|--------------------|-----------------------|
| Veerupäise tekst | Tegelik                |
| Sisesta automaattekst    | Valik puudub. |
| Vormingusuvandid     | Väli                   |
| Põhjendus      | Valik puudub. |
| Algusvahemik        | B                     |
| Lõppvahemik          | BASE                  |

Pärast teabe sisestamist klõpsab kasutaja nuppu **OK**. Seejärel topeltklõpsab kasutaja veerus C veerupäise lahtrit dialoogiboksi **Veerupäis** avamiseks ja sisestab järgmise teabe.

| Field              | Väärtus                 |
|--------------------|-----------------------|
| Veerupäise tekst | Eelarve                |
| Sisesta automaattekst    | Valik puudub. |
| Vormingusuvandid     | Väli                   |
| Põhjendus      | Valik puudub. |
| Algusvahemik        | BASE+1                |
| Lõppvahemik          | E                     |

Nüüd prinditakse iga kord selle aruande loomisel tegelikke andmeid sisaldavatele veergudele sõna „Tegelik” ja eelarveprognoose sisaldavatele veergudele sõna „Eelarve”. Lisaks korrigeeritakse iga kuu veergude arvu.

## <a name="apply-column-justification"></a>Veeru joonduse rakendamine
Lahtrit **Joondus** kasutatakse joonduse rakendamiseks aruande kirjelduse veerule. See suvand mõjutab ainult veeru kirjeldusi, mitte tegelikke väärtusi.

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Topeltklõpsake lahtrit **Joondus**.
3. Valige loendist üks järgmistest väärtustest.

    - **Puudub** – joondust pole rakendatud.
    - **Vasak** – veeru kirjelduste vasakjoondus.
    - **Keskel** – veeru kirjelduste keskjoondus.
    - **Parem** – veeru kirjelduste paremjoondus.

## <a name="add-special-formatting-options"></a>Erivormingu suvandite lisamine
Veeru definitsioonis rakendavad vorminduse veeru üksikasjaread erivormingu valitud veergudele. Kuigi mõni suvand **Prindi kontrollkood** ja **Veeru piirangud** on omased veergudele **FD**, kehtib enamik suvandeid kõigi veergude kohta. Veeru definitsioonis määratud vorming alistab aruande definitsioonis määratud vormingu. Readefinitsioonis määratud vorming aga alistab veeru definitsioonis määratud vormingu. Vormingu ridadeks peetakse järgmisi ridu.

- Veeru laius
- Lisatühikud enne veergu
- Vormingu/valuuta alistamine
- Prindi kontrollkood

### <a name="changing-the-column-width"></a>Veeru laiuse muutmine

Lahter **Veeru laius** määrab prinditud aruandes selle veeru laiuse puhul kasutatava märkide arvu. Veeru laius on oluline summasid sisaldavate veergude (veerud tüübiga **CALC**, **WKS** või **FD**), kirjelduste (veerud tüübiga **DESC**) või täitmise (veerud tüübiga **FILL**) puhul. Vaikimisi valitakse suvand **AutoFit**, nii et iga veeru laiust korrigeeritakse sisu mahutamiseks automaatselt.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>Aruande veeru laiuse määramine

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Sisestage lahtrisse **Veeru laius** tühikute arv veeru laiuse puhul. Iga veeru maksimumlaius on 255 märki (see arv sisaldab sendimärke, komasid ja sulge). Kui aga soovite lubada aruandekoosturil valida veeru jaoks sobiva laiuse lahtri sisu alusel, topeltklõpsake lahtrit **Veeru laius** ja seejärel klõpsake suvandit **Sobita automaatselt**.

### <a name="add-space-between-columns"></a>Tühiku lisamine veergude vahele

Lahter **Lisatühikuid enne veergu** määrab veeru definitsioonis ühe veeru ja külgnevate veergude vahelise eraldaja laiuse. Suvandi **Lisatühikud enne veergu** säte mõjutab kõiki veeru üksikasjaridade ridu, kuid mitte veeru päiseridu. Kasutage seda suvandit veergude gruppide eraldamiseks või mõne tühiku lisamiseks enne kirjeldust, nii et kirjelduse veergu taandatakse aruande vasakjoondatud tiitlitest. Kõigi veergude vaheliste tühikute vaikearv on kaks. Saate seda sätet muuta aruande definitsiooni vahekaardil **Sätted**.

#### <a name="specify-the-space-between-columns"></a>Veergude vahelise tühiku määramine

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Sisestage lahtrisse **Lisatühikud enne veergu** veergude vahele sisestatavate tühikute arv.

### <a name="specify-a-format-currency-override"></a>Vormingu/valuuta alistamise määramine

Vahekaart **Vormingu/valuuta alistamine** määrab kümnend-, valuuta- ja protsendisummade vormingu veerus. Selline vorming alistab veeru definitsioonis või süsteemi vaikesuvandites määratud vormingu.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Vormingu/valuuta alistamise määramine aruande veerule

1. Avage aruandekoosturis muudetav veerudefinitsioon.
2. Topeltklõpsake summaveerus lahtrit **Vormingu/valuuta alistamine**.
3. Valige vormingusuvandid dialoogiboksist **Vormingu alistamine**.

### <a name="add-a-print-control-code"></a>Prindi kontrollkoodi lisamine

Lahter **Prindi kontrollkood** võib sisaldada koode, mis korrigeerivad veeru kuva või printimisomadusi. Prindi kontrollkoode on kahte tüüpi: tavalised prindi kontrollkoodid ja tingimuslikud prindi kontrollkoodid.

#### <a name="regular-print-control-codes"></a>Tavalised prindi kontrollkoodid

| Prindi kontrollkood | Teisendamine                                     | Kirjeldus |
|--------------------|-------------------------------------------------|-------------|
| NP                 | Mitteprinditav                                     | Selle veeru summade välistamine prinditavast aruandest ja arvutustest. Mitteprinditava veeru kaasamiseks arvutusse viidake veerule otse arvutusvalemis. Näiteks on mitteprinditav veerg C kaasatud järgmisse arvutusse: **B+C+D**. Mitteprinditav veerg C pole kaasatud järgmisse arvutusse: **B:D**. |
| XCR                | Märgi muutmine, kui rea tavaline saldo on kreedit | Eelarve või võrdlusaruande loomine, kui soovimatu hälve (nt tulu puudujääk või ülekulu) on alati negatiivne. Rakendage see kood veerule **CALC** veeru summa märgi muutmiseks, kui antud rea tavaline saldo on kreedit (määratud tähega **C** readefinitsiooni veerus **Normaalsaldo**).<p><strong>Märkus.</strong> Veenduge ridade <strong>TOT</strong> ja </strong>CAL</strong> puhul, mis tavaliselt sisaldavad kreeditsaldot, et sisestaksite <strong>C</strong> readefinitsiooni veergu <strong>Normaalsaldo</strong>.</p> |
| X0                 | Veeru peitmine, kui kõik on nullid või tühjad          | Veeru **FD** välistamine aruandest, kui kõik selle veeru lahtrid on kas tühjad või sisaldavad nulle. |
| SR                 | Peida ümardamine                               | Selle veeru summade ümardamise takistamine. |
| XR                 | Ümberarvestuse peitmine                                 | Ümberarvestuse peitmine. Kui aruanne kasutab aruandluspuud, ei koondata selle veeru summasid järgnevatesse emasõlmedesse. |
| RP                 | Korda veergu igal lehel                      | Määratud veeru kordamine aruande igal lehel. Näiteks saate kasutada prindi kontrollkoodi **RP** tüüpi **ROW** veeru kaasamiseks, mis tõmbab rea koodid igale lehele. |
| WT                 |  Murra tekst                                      |  Kui veeru tekst on ruumi mahtumiseks liiga pikk, murdke tekst kogu teksti säilitamiseks veerus. |

#### <a name="conditional-print-control-codes"></a>Tingimuslikud prindi kontrollkoodid

| Tingimuslik prindi kontrollkood | Kirjeldus                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (puudub)                         | Tingimusliku prindi suvandi tühjendamine.                                                  |
| P&lt;B                         | Kindla veeru kuvamine ainult siis, kui periood on baasperioodist lühem.             |
| P&gt;B                         | Kindla veeru kuvamine ainult siis, kui periood on baasperioodist pikem.             |
| P=B                            | Kindla veeru kuvamine ainult siis, kui periood on baasperioodiga võrdne.              |
| P&lt;=B                        | Kindla veeru kuvamine ainult siis, kui periood on baasperioodist lühem või sellega võrdne. |
| P&gt;=B                        | Kindla veeru kuvamine ainult siis, kui periood on baasperioodist pikem või sellega võrdne. |

#### <a name="add-print-control-codes-to-a-report-column"></a>Prindi kontrollkoodide lisamine aruande veergu

1. Avage aruandekoosturis muudetav veerudefinitsioon.
2. Topeltklõpsake lahtrit **Printimise juhtelement**.
3. Valige dialoogiboksis **Prindi kontrollkood** kood loendist **Prindi kontrollkoodi suvandite valimine**. Rohkem kui ühe koodi valimiseks hoidke koodide valimisel all klahvi Ctrl.
4. Valige suvand väljalt **Tingimuslikud prindi suvandid**. Vaikimisi on valitud säte **(puudub)**. Korraga saate valida ainult ühe tingimusliku prindi kontrollkoodi.
5. Klõpsake nuppu **OK**.

> [!TIP]
> Saate prindi kontrollkoodid sisestada ka otse lahtrisse **Prindi kontrollkood**. Eraldage mitu prindi kontrollkoodi komadega.

## <a name="column-types"></a>Veerutüübid
Teabe tüüp, mida iga aruande veerg sisaldab, määratakse väärtusega veeru definitsiooni real **Veeru tüüp**. Iga veerudefinitsioon peab sisaldama vähemalt ühte kirjelduse (**DESC**) veergu ja ühte summa (**FD**, **WKS** või **CALC**) veergu.

> [!NOTE]
> Veeru tüübi koodid ei rakendu kõigile raamatupidamissüsteemidele. Valides tüübi, mis teie raamatupidamissüsteemi puhul ei kehti, on see veerg aruandes tühi.

### <a name="specify-a-column-type"></a>Veeru tüübi määramine

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Topeltklõpsake asjakohases veerus lahtrit real **Veeru tüüp**.
3. Valige loendist veeru tüüp. Järgmises tabelis kirjeldatakse eri veeru tüüpe.

    <table>
    <thead>
    <tr>
    <th>Veeru tüübi kood</th>
    <th>Kirjeldus</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>FD</td>
    <td>Kui kasutate rea definitsioonis veergu <strong>Link finantsdimensioonidele</strong>, kuvatakse finantsandmed. Kui valite <strong>FD</strong>‑tüüpi veeru, määratakse järgmistel ridadel automaatselt vaikesätted. <ul>
    <li><strong>Arvestuskood/atribuudikategooria:</strong> TEGELIK</li>
    <li><strong>Arvestuskood/atribuudikategooria:</strong> TEGELIK</li>
    <li><strong>Finantsaasta:</strong> BAAS</li>
    <li><strong>Periood:</strong> BAAS</li>
    <li><strong>Kaetud perioodid:</strong> PERIOODILINE</li>
    <li><strong>Veeru laius:</strong> 14</li>
    </ul>
Saate neid vaikesätteid muuta.</td>
    </tr>
    <tr>
    <td>CALC</td>
    <td>Lahtris <strong>Valem</strong> määratletud lihtsa või keeruka arvutuse tulemuse kuvamine. Lisateabe saamiseks vt jaotist <a href="advanced-formatting-options-financial-reporting.md">Finantsaruandluse täpsemad vormingusuvandid</a>.</td>
    </tr>
    <tr>
    <td>DESC</td>
    <td>Rea kirjelduse kuvamine readefinitsioonist. Kuigi kirjelduse veerg on sageli aruande esimene veerg, võib see olla mis tahes kohas.</td>
    </tr>
    <tr>
    <td>ROW</td>
    <td>Finantsridade üksiku rea koodide kuvamine readefinitsiooni veerult <strong>Rea kood</strong>. Lisateabe saamiseks vt jaotist <a href="row-definitions-financial-reporting.md">Finantsaruandluse readefinitsioonid</a>.</td>
    </tr>
    <tr>
    <td>ACCT (kontokoodid)</td>
    <td>Finantsandmete segmendi väärtuste või dimensiooniväärtuste kuvamine, mida rakendatakse igale reale. Konto ja kande üksikasjade aruannete puhul prinditakse täielik konto (näiteks <strong>110140-070-0101</strong>). Kui vahemikud on määratud seonduva reamääratluse veerus <strong>Link finantsdimensioonidele</strong>, pannakse vahemik nurksulgudesse ja seda käsitletakse üksiku väärtusena (näiteks <strong>[110140:110700]‑070‑[0101:0200]</strong>). Finantsaruannete ja kõrgetasemeliste aruannete puhul, mis on mitmete kontode kombinatsioonid, prinditakse finantsandmete link reamääratlusest (näiteks <strong>1100:1200</strong>).</td>
    </tr>
    <tr>
    <td>FILL</td>
    <td>Lahtri täitmine märgiga, mille panete üksisjutumärkidesse. Kui te märki ei sisesta, on veerg tühi. Näiteks veeru täitmiseks kolmikpunktiga (...) sisestage <strong>FILL</strong> <strong>'.'</strong>.</td>
    </tr>
    <tr>
    <td>PAGE</td>
    <td>Vertikaalse lehepiiri sisestamine aruandesse. Veerust <strong>LEHT</strong> paremal olevad veerud ilmuvad muul lehel.</td>
    </tr>
    <tr>
    <td>ATTR</td>
    <td>Konto või kande atribuudi kuvamine veerus, kui teie raamatupidamissüsteem atribuute toetab. Atribuut, mis tuleb rakendada ühele täielikule kontole, ekstrakdib aluseks oleva konto või kande teabe finantsandmetest. Konto taseme atribuudid kuvavad andmeid kontolt ja kande taseme atribuudid kuvavad kande postitamise ajal ilmnenud andmeid. Kui valite <strong>ATTR</strong>‑tüüpi veeru, määrake atribuudikategooria veeru määratluse üksikasjade real <strong>Arvestuskood/atribuudikategooria</strong>.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Veerg Finantsdimensioonid

Järgmised rea **Veeru definitsioon** definitsioonid rakenduvad veergudele, mille veeru tüüp on **FD** (finantsdimensioonide summad).

#### <a name="book-codeattribute-category-cell"></a>Lahter Konteerimiskood/atribuudi kategooria

Lahter **Konteerimiskood/atribuudi kategooria** määratleb konteerimiskoodi veeru **FD** andmete puhul. Veeru definitsioon võib sisaldada mitut tegelikku, eelarve ja statistilist veergu. Veeru definitsioon võib kuvada ka eri perioode, nagu praegune või aasta algusest praeguse kuupäevani, ja eri summasid. Konteerimiskoodide loend kajastab teie ettevõtte andmetes loodud tegelikke, eelarve ja statistilisi (mitterahalisi) suvandeid.

#### <a name="fiscal-year-cell"></a>Lahter Rahandusaasta

Lahter **Rahandusaasta** määratleb rahandusaasta, mis tuleks veergu kaasata. Aasta võib olla aruande loomisel määratud baasperioodile vastav. Saadaval on järgmised suvandid.

| Suvand  | Kirjeldus                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| BASE    | Aruande ajal määratud aasta kasutamine.                                                                          |
| BASE+\# | Aasta kasutamine, mis on \# aastat pärast baasaastat. Näiteks baasaastale järgneva kolmanda aasta kasutamiseks sisestage **BASE+3**. |
| BASE-\# | Aasta kasutamine, mis on \# aastat enne baasaastat. Näiteks eelmise aasta kasutamiseks sisestage **BASE-1**.                 |
| \#      | Tegeliku rahandusaasta sisestamine.                                                                                                |

#### <a name="period-cell"></a>Lahter Periood

Lahter **Periood** määratleb rahandusperioodid, mis tuleks veergu kaasata. Periood võib olla aruande loomisel määratud baasperioodile vastav. Saadaval on järgmised suvandid.

| Suvand          | Kirjeldus |
|-----------------|-------------|
| BASE            | Baasperioodi kasutamine. |
| BASE+\#         | Perioodi kasutamine, mis on \# perioodi pärast baasperioodi. Näiteks baasperioodile järgneva kolmanda perioodi kasutamiseks sisestage **BASE+3**. |
| BASE-\#         | Perioodi kasutamine, mis on \# perioodi enne baasperioodi. Näiteks eelmise perioodi kasutamiseks sisestage **BASE-1**. |
| BASE-\#:BASE    | Mitme perioodi kasutamine alates mitmest perioodist enne alusperioodi kuni baasperioodini. Näiteks kolme eelmise perioodi ja baasperioodi kasutamiseks sisestage **BASE-3:BASE**. |
| BASE:BASE+\#    | Mitme perioodi kasutamine alates baasperioodist kuni mitme perioodini pärast baasperioodi. Näiteks baasperioodi ja kahe järgmise perioodi kasutamiseks sisestage **BASE:BASE+2**. |
| BASE-\#:BASE+\# | Mitme perioodi kasutamine alates mitmest perioodist enne baasperioodi kuni mitme perioodini pärast baasperioodi. Näiteks kolme eelmise perioodi, baasperioodi ja kahe järgmise perioodi kasutamiseks sisestage **BASE-3:BASE+2**. |
| 1:BASE          | Mitme perioodi kasutamine alates esimesest perioodist kuni baasperioodini. |
| \#              | Alati kindla perioodi koodi kasutamine. Selle suvandi kasutamine pole soovitatav, kuna see vähendab veeru definitsiooni paindlikkust. |
| \#                                      : \#           | Alati kindla perioodide vahemiku kasutamine. Selle suvandi kasutamine pole soovitatav, kuna see vähendab veeru definitsiooni paindlikkust. |

Saate rahandusaasta piire ületada mis tahes perioodi spetsifikatsioonis ja kombineerida perioodide vahemiku aastaid. Näiteks saate määrata perioodid kui **BASE-5** (viimase kuue perioodi tähistamiseks) ja käivitada aruande, mille baasperiood on 2. Sellisel juhul kuvatakse aruandes määratud rahandusaasta kahe esimese perioodi ja eelmise rahandusaasta nelja viimase perioodi andmed.

### <a name="specify-the-periods-for-an-fd-column"></a>Perioodide määratlemine veeru FD jaoks

1. Avage aruandekoosturis muudetav veerudefinitsioon.
2. Topeltklõpsake veeru **FD** rea lahtrit **Periood** ja seejärel valige suvand loendist.
3. Lõpetage valem navigeerimispaani kohal valemiribal või lahtris **Periood**. Asendage numbrimärk (\#) sobiva väärtusega.

#### <a name="periods-covered-cell"></a>Lahter Hõlmatud perioodid

Lahter **Hõlmatud perioodid** määratleb summa, mis tuleks veerus kuvada. See summa on seotud väärtusega veeru lahtrites **Rahandusaasta** ja **Periood**. Saadaval on järgmised suvandid.

| Suvand      | Kirjeldus                                                                 |
|-------------|-----------------------------------------------------------------------------|
| PERIODIC    | Praeguse perioodi või perioodide vahemiku tegevuse summa kuvamine. |
| PERIODIC/BB | Praeguse perioodi või perioodide vahemiku algsaldo kuvamine.   |
| YTD         | Kumulatiivse tegevuse summa kuvamine.                               |
| YTD/BB      | Aasta algsaldo kuvamine.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>Veeru FD puhul hõlmatud perioodide määramine

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Topeltklõpsake veeru **FD** rea lahtrit **Hõlmatud perioodid** ja valige suvand loendist.

### <a name="attribute-filter-in-a-column-definition"></a>Veeru definitsiooni atribuudi filter

Atribuudid on finantsandmete väärtused konto või kande täpsemaks määratlemiseks. Konto atribuudid sisaldavad suvandeid **Vara**, **Kohustus**, **Tulu** ja **Kulu**. Kande atribuudid sisaldavad suvandeid **Kande kirjeldus** ja **Kande rakendamise kuupäev**. Atribuudi tugi võib Microsoft Dynamicsi ERP süsteemide lõikes erineda. Lahter **Atribuudi filter** piirab andmed veergudes **FD** atribuudikategooriate konkreetsetele väärtustele või vahemikele. Kuigi seda funktsiooni saab kasutada koos veeruga **ATTR**, pole veerg **ATTR** nõutav. Veerus **FD** on aruande atribuudi filtrist kaasatavad kontod või kanded piiratud.

> [!NOTE]
> Nägemaks, milliseid atribuute ERP-süsteem toetab, vaadake süsteemi integratsioonijuhendit.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Atribuudi filtri rakendamine aruande veerule FD

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Topeltklõpsake veeru **FD** jaoks lahtrit **Atribuudifilter**.
3. Topeltklõpsake dialoogiboksis **Atribuudifilter** mõnd veeru **Atribuut** lahtrit ning valige seejärel filtri tüüp.
4. Tulemuste edasiseks piiramiseks sisestage vahemik veergudesse **Alates** ja **Kuni**. Lahter **Alates** peab sisaldama väärtust.
5. Klõpsake nupul **OK**.

#### <a name="example-of-an-attribute-filter"></a>Atribuudi filtri näide

Järgmises näites kuvatakse veeru kirjelduse osa, mille konto atribuut on real **Konteerimiskood/atribuudi kategooria**. Selle veeru atribuudi filter määrab aruandesse kaasatavate väärtuste vahemiku.

|      Filtreeri                  | A    | B                   |
|------------------------------|------|---------------------|
| Veeru tüüp                  | DESC | FD                  |
| Arvestuskood/atribuudikategooria |      | TEGELIK              |
| Finantsaasta                  |      | BASE                |
| Periood                       |      | 1:BASE              |
| Kaetud perioodid              |      | PERIODIC            |
| ...                          |      |                     |
| Veeru laius                 | 30   |                     |
| ...                          |      |                     |
| Atribuudi filter             |      | Viide=\[01:10\] |

### <a name="dimension-filter-in-a-column-definition"></a>Veeru definitsiooni dimensioonifilter

Dimensiooni filtrit kasutatakse veeru **FD** piiramiseks teatud dimensiooniväärtusteni. Filter võib hõlmata üksikut dimensiooni, dimensioonide vahemikku või dimensioonide gruppi. Filter võib sisaldada ka dimensiooni väärtuste kogumit. Kuna dimensiooniväärtused võivad olla erinevad, ei pea ..\\finantsdimensioonid\\dimensioonipõhine süsteem täpsele pikkusele vastama. Filtrit rakendatakse olenemata sellest, kas aruanne sisaldab aruandluspuud või mitte. Saate kasutada metamärki (\* või ?) kõigis kohtades. Kui määrate mitu kontot, pange kontode vahele koma, nagu järgmises näites: +konto=\[1200\], +konto=\[1100\], osakond=\[01?\] Kõigi konkreetse konto osakondade saamiseks võite dimensioonifiltrist dimensiooni Osakond välja jätta. Näiteks käsitletakse mõlemat järgmist dimensioonifiltrit samamoodi.

- +Konto=\[1100\],Osakond
- +Konto=\[1100\]

Täpseks vastendamiseks saate kasutada ka mis tahes kirjamärkide kombinatsiooni ja määratleda osalised dimensioonid. Näiteks **Asukoht = \[10\*\]** sisaldab kõiki asukoha dimensiooniväärtusi, mis algavad numbriga 10.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Dimensioonifiltri rakendamine aruande veerule

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Topeltklõpsake lahtrit **Dimensioonifilter** veeru **FD** puhul.
3. Sisestage dialoogiboksi **Dimensioonid** rakendatavad filtrid.
4. Klõpsake nupul **OK**.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Mitme valuutaga aruande vormindamine veeru definitsioonis

Mitme valuutaga aruanne võib kuvada summasid pearaamatu arvestusvaluutas, pearaamatu aruandlusvaluutas, algses kandevaluutas või teisendatud aruandlusvaluutas. Ettevõtte arvestusvaluuta on määratud pearaamatu seadistuses. Ärge ajage seda sätet segamini operatsioonisüsteemi piirkonnavalikute sättega, milles saate konfigureerida aruannetest kasutatavaid vaikevaluutatähiseid. Veeru definitsioonis on saadaval järgmised valuutaga seotud lahtrid.

- **Valuuta kuvamine** – saate määrata kannetes kuvatava valuuta tüübi (arvestusvaluuta, aruandlusvaluuta, kandevaluuta või teisendatud aruandlusvaluuta). Aruandlusvaluutaks teisendamise funktsiooni nimetatakse mõnikord valuuta teisendamiseks. Valuuta teisendamine on võimalus esitada pearaamatu summasid valuutas, mis ei ole ettevõtte tegevus- või aruandlusvaluuta või sisestatud kande valuuta.
- **Valuutafilter** – valuuta filtri määramine. Aruandes kuvatakse ainult valitud valuutas sisestatud kanded.

> 
Ettevõtte arvestusvaluuta määramiseks toimige allpool kirjeldatud viisil.

1. Klõpsake aruandekoosturis menüü **Ettevõte** suvandit **Ettevõtted**.
2. Valige ettevõte dialoogiboksist **Ettevõtted** ja seejärel klõpsake käsku **Kuva**..
3. Dialoogiboksi **Ettevõtte kuvamine** suvandi **Piirkonnavalikud** all saate vaadata valitud ettevõtte puhul määratud valuutat.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>Valuuta määramine mitme valuutaga aruandel

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Topeltklõpsake asjakohases veerus **FD** olevat lahtrit **Valuutakuva** ja seejärel valige valuutateabe kuvamise suvand: **Pearaamatu arvestusvaluuta**, **Pearaamatu aruandlusvaluuta**, kandevaluuta või muuks aruandlusvaluutaks teisendamine.
3. Topeltklõpsake lahtrit **Valuutafilter** asjakohases veerus **FD** ja seejärel valige loendist sobiv valuutakood. Aruandes kuvatakse ainult selles valuutas sisestatud kanded.


### <a name="example-for-currency-display-and-currency-filter-cells"></a>Lahtrite Kuva valuuta ja Valuutafilter näide

Kasutaja tegi oma veeru definitsioonis järgmised valuuta valikud.

- **Valuutafilter:** jeen
- **Valuutakuva:** pearaamatu arvestusvaluuta (USA dollarid)

Valitud valuutafiltri tõttu sisaldab aruanne ainult kandeid, mis sisestati Jaapani jeenides (JPY). Valitud valuutakuva tõttu kuvatakse need kanded aruandes arvestusvaluutas, USA dollarites (USD).

#### <a name="currency-filter-and-currency-display-combinations"></a>Kombinatsioonid Valuutafilter ja Valuuta kuva

Järgmises tabelis kuvatakse aruande tulemused, mis võivad ilmneda suvandite eri kombinatsioonide puhul lahtrites **Valuuta kuva** ja **Valuutafilter** tehtud valikute tõttu. Ametlik valuuta on USD.


| Lahter Valuuta kuva                        | Lahter Valuutafilter | Aruande tulemus |
|----------------------------------------------|----------------------|---------------|
| Kande valuuta                 | **YEN**              | **Y6,000** – tulemus kuvab ainult valuutas JPY sisestatud kanded. |
| Pearaamatu arvestusvaluuta | **YEN**              |**$60** – tulemus kuvab ainult need kanded, mis sisestati valuutas JPY ja kuvab need kanded valuutas USD.<p><strong>Märkus.</strong> Vahetuskurss on umbes 100 JPY USD kohta.</p> |
| Pearaamatu arvestusvaluuta | Tühi                | **2310 $** – kõik andmed kuvatakse pearaamatus määratud arvestusvaluutas.<p><strong>Märkus.</strong> See summa on kõigi kannete summa arvestusvaluutas.</p> |
| Kande valuuta                 | Tühi                | **$2,250** – tulemus kuvab kõik summad valuutas, milles kanne tehti. See tähendab, et kogusummaks liidetakse kokku eri valuutade summad. |

### <a name="calculation-column-in-a-column-definition"></a>Veeru definitsiooni arvutuse veerg

Veeru definitsiooni veeru tüüp **CALC** toetab keerukaid arvutusi lahtris **Valem** ning võib sisaldada tehtemärke **+**, **-**, **\**_ ja _*/** ning ka lauseid **IF/THEN/ELSE**. Arvutuse veerg võib viidata ka mis tahes muule veerule, sh järgnevatele veergudele. Lisaks võib arvutuse veerg veeru päiste toetamiseks sisaldada ka rahandusaastat ja perioodi. Arvutusvalem võib olla kuni 1024 märki pikk. Arvutustulemuse väljendamiseks protsendina kasutage kindla vormingu alistamist.

> [!NOTE]
> Arvutusvalemite tulemused ei hõlma mitteprinditavate veergude vahemikes olevaid väärtusi. Näiteks **A:D** prindib **0** (null), samas kui **A+B+C** arvutab mitteprinditavate väärtuste puhul väärtuse.

#### <a name="operators-in-calculation-columns"></a>Arvutusveergude tehtemärgid

Veergude liitmiseks, lahutamiseks, korrutamiseks või jagamiseks sisestage veeru tähed arvutamise järjekorras ja kasutage seejärel iga veeru tähe eraldamiseks asjakohast tehtemärki. Järgmises tabelis selgitatakse tehtemärke, mida saate arvutusveerus kasutada.

| Operaator | Arvutuse näide | Kirjeldus |
|----------|---------------------|-------------|
| +        | A+C                 | Veeru A summa liitmine veeru C summale. |
| :        | A:C A:C-D           | Järjestikuste veergude vahemiku liitmine. Näiteks valem **A:C** liidab veergude A kuni C summad ja valem **A:C-D** liidab veergude A kuni C summad ja lahutab seejärel veeru D summa. |
| -        | A-C                 | Lahutage veerus A olev summa veerus C olevast summast.<p><strong>Märkus.</strong> Veerus märkide ümberpööramiseks võite kasutada miinusmärki (-). Näiteks kasutage valemit <strong>-A+B</strong> veeru A summa pöördmärgi liitmiseks veeru B summale.</p> |
| \*       | A\*C                | Veeru A summa korrutamine veeru C summaga. |
| /        | A/C                 | Veeru A summa jagamine veeru C summaga. |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Arvutusvalemi kasutamine veeru definitsioonis

1. Avage aruande kujundajas muudetav veeru definitsioon.
2. Sisestage valem asjakohase veeru **CALC** lahtrisse **Valem**.

#### <a name="complex-calculations"></a>Keerukad arvutused

Keerukas arvutus võib sisaldada lahtri viidete, tehtemärkide, väärtuste ja pesastatud sulgude tasemete mis tahes kombinatsioone. Näiteks kasutage veergude A ja B keskmise arvutamiseks arvutusvalemit **((A+B)/2)**.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Aruande lahtrite määramine veeru arvutuses

Saate viidata kindlale aruande lahtrile, sisestades veeru tähe ja rea koodi. Näiteks **B.100** viitab rea koodile 100 veerus B. Saate kogu veeru jagada kindla aruande samas veerus oleva lahtri summaga. Näiteks arvutus **B/B.100** tähendab, et veeru B summa tuleks jagada veeru B rea koodi 100 väärtusega. Kui arvutus viitab veerule, mis sõltub teisest veerust, lahendatakse esmalt sõltuv veerg. Veeru viitamisel teisele veerule, mis viitab taas esimesele veerule põhjustate ringviite tõrke.

> [!NOTE]
> Arvutus võib vale olla, kui aruande arvutamise prioriteeti muudate. Saate seadistada arvutamise prioriteedi aruande definitsiooni vahekaardil **Sätted**.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Veeru korrutamine või jagamine baasreaga

Saate luua veeru, mis kuvaks määratud veerus kõik väärtused baasarvu protsendina. Seega saate kuvada ridadevahelised seosed, nagu müügi rea protsendi või kogukulude rea protsendi. Iga konkreetse veeru rea korrutamiseks või jagamiseks baasreaga sisestage arvutamisel kasutatav veerg ja seejärel sisestage **\*BASEROW** või **/BASEROW**. Näiteks sisestage **C\*BASEROW** või **C/BASEROW**.

> [!NOTE]
> Kui kasutate veerudefinitsioonis baasrea arvutust, veenduge, et kõik selle veerudefinitsiooniga kasutatavad readefinitsioonid sisaldavad arvutamiseks vähemalt üht baasrida.

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Veeru summa jagamine perioodide arvuga

Saate veeru summa jagada määratud perioodide arvuga. Näiteks valem **B/Periods** jagab veeru B väärtuse veerus B olevate perioodide arvuga. Kui arvutus hõlmab mitut veergu, määrake arvutamisel kasutatavate perioodide arv. Näiteks valem **(B+C)/Periods** liidab veeru B ja veeru C summad ja jagab seejärel tulemuse perioodi väärtusega.

## <a name="additional-resources"></a>Lisaressursid

[Readefinitsioonid finantsaruande koosturis](row-definitions-financial-reporting.md)

[Täpsemad vormingusuvandid finantsaruandluses](advanced-formatting-options-financial-reporting.md)
