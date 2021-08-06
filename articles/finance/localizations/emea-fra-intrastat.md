---
title: Prantsuse Intrastat
description: See teema sisaldab teavet Prantsusmaa Intrastat deklareerimise kohta.
author: andosip
ms.date: 07/9/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: a0f418aa18db99088db0b75df41f950e67160e3f
ms.sourcegitcommit: 8fb79920bea14746a71551a4456236a6386bfcea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/12/2021
ms.locfileid: "6538874"
---
# <a name="french-intrastat"></a>Prantsuse Intrastat

[!include[banner](../includes/banner.md)]

Prantsusmaal asuvad ettevõtted, mis on registreeritud käibemaksukohustuslasena ja kauplevad teiste Euroopa Liidu (EL) riikidega, peavad deklareerima kaupade ja teenuste vahetamise Prantsusmaale ja Prantsusmaalt. Deklaratsioon d'exchanges de biens (Kaubakaubanduse deklaratsioon või DEB) on kombinatsioon EL käibe- ja Intrastat-aruandest. Te peate selle aruande esitama kord kuus kogu kaupade ühendusesisese müügi puhul.

DEB-aruande saate luua kahes elektroonilises tekstifailivormingus: SAISUNIC 330 või INTRACOM.

Järgmine tabel näitab Prantsuse Intrastati deklaratsioonis sisalduvaid välju SAISUNIC 330 vormingus.

| **Field**                   | **Aruandetase**   |              |
|-----------------------------|--------------------|--------------|
|                             | **4 (lihtsustatud)** | **1 (täielik)** |
| Viiteperiood         | X                  | X            |
| Deklaratsiooni number       | X                  | X            |
| Rea number                 | X                  | X            |
| Riigi ISO-kood (FR)       | X                  | X            |
| Täiendav kood          | X                  | X            |
| Sireeni number                | X                  | X            |
| Kliendi käibemaksukood        | X                  | X            |
| Suunakood              | X                  | X            |
| Kande tüüp            | X                  | X            |
| Kohustuse tase            | X                  | X            |
| Kaubaartikkel              |                    | X            |
| Rahvuslik NGP                |                    | X            |
| Maakond (osakond)         |                    | X            |
| Kande iseloom       |                    | X            |
| Päritoluriik      |                    | X            |
| Päritoluriik - impordid |                    | X            |
| Lõppsihtkoht - ekspordid |                    | X            |
| Arve väärtus               | X                  | X            |
| Statistiline väärtus           |                    | X            |
| Netokaal                  |                    | X            |
| Lisaühikud            |                    | X            |
| Transpordikood              |                    | X            |

Järgmine tabel näitab Prantsuse Intrastati deklaratsioonis sisalduvaid välju INTRACOM vormingus.

| **Field**                   | **Aruandetase**   |              |
|-----------------------------|--------------------|--------------|
|                             | **4 (lihtsustatud)** | **1 (täielik)** |
| Kood                        | X                  | X            |
| Deklaratsiooni number       | X                  | X            |
| Rea arv              | X                  | X            |
| Sireen                       | X                  | X            |
| Maakond (osakond)         |                    | X            |
| Transpordikood              |                    | X            |
| Päritoluriik           |                    | X            |
| Kande iseloom       |                    | X            |
| Arve väärtus               | X                  | X            |
| Tarneviisid           |                    | X            |
| Kande tüüp            | X                  | X            |
| Kohustuse tase            | X                  | X            |
| Kaubaartikkel              |                    | X            |
| Rahvuslik NGP                |                    | X            |
| Netokaal                  |                    | X            |
| Statistiline väärtus           |                    | X            |
| Lisaühikud            |                    | X            |
| Päritoluriik - impordid |                    | X            |
| Lõppsihtkoht - ekspordid |                    | X            |
| Kliendi käibemaksukood        | X                  | X            |
| Täiendav kood          | X                  | X            |
| Viiteperiood         | X                  | X            |

### <a name="set-up-intrastat"></a>Intrastati seadistamine

1.  [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) ühiskasutusega varateegis laadige Intrastati deklaratsiooni jaoks alla järgmiste elektrooniliste aruannete (ER) konfiguratsioonide viimased versioonid:

-   Intrastati mudel

-   Intrastat-aruanne

-   Intrastat INTRACOM (FR)

-   Intrastat SAISUNIC (FR)

Lisateavet leiate jaotisest [Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

2.  Minge rakenduses Dynamics 365 Finance jaotisesse **Maksud** &gt; **Seadistamine** &gt; **Väliskaubandus** &gt; **Väliskaubanduse parameetrid** ja järgige järgmisi samme.

    1.  Valige **Intrastati** vahekaardil vahekaardil **Elektrooniline aruandluse kiirkaart** väljal **Failivormingu vastendamine** **Intrastat INTRACOM (FR)** või **Intrastat SAISUNIC (FR)**.

    2.  Sisestage või valige väärtus **Intrastati aruanne** väljal **Aruandevormingu vastendamine**.

    3.  Valige kiirkaardi **Kaubaartikli hierarhia** väljal **Kategooriahierarhia** väärtus **Intrastat**.

    4.  Valige kiirkaardi **Üldine** väljal **Kandekood** kauba ülekannetel kasutatav kood.

    5.  Valige väljal **Kreeditarve** kaupade tagastuseks kasutatav kood.

    6.  Sisestage väljal **Ekspordikohustuse tase** ekspordiaruande üksikasjade tase. Teie valitud tase mõjutab aruandes kuvatavaid ridu. Lisateabe saamiseks vt tabeleid käesoleva teema alguses.

3.  Minge **Organisatsiooni haldamine** &gt; **Organisatsioonid** &gt; **Juriidilised isikud** ja valige oma ettevõte, misjärel järgige neid samme.

    1.  Sisestage oma NAF-kood **NAF-koodi** väljale kiirkaardil **Registreerimisnumbrid**. Lisateavet vt [FR-00003 NAF-koodid ja Sireeni numbrid](tasks/fr-00003-naf-codes-siret-numbers.md).

    2.  Seadke kiirkaardi **Väliskaubandus ja logistika** jaotises **Intrastat** väljad **Käibemaksukohuslase koodi eksport**- ja **Käibemaksukohuslase koodi import**.

    3.  Kiirkaardi **Maksu registreerimine** väljal **Maksu registreerimisnumber** sisestage oma ettevõtte maksu registreerimisnumber.

4.  NAF-koodide ja maksukohustuslase koodide määramiseks minge asukohta **Müügireskonto** &gt; **Kliendid** &gt; **Kõik kliendid** ja järgige järgmisi samme.

    1.  Valige klient.

    2.  Sisestage kiirkaardi **Arve ja tarne** jaotise **Käibemaks** väljale **Maksukohuslase kood** kliendi maksukohuslase kood.

    3.  Kiirkaardil **Müügiddemograafia** väljal **Prantsuse siret** sisestage ettevõtte Siret-number.

    4.  Sisestage väljal **NAF-kood** ettevõtte NAF-kood.

    5.  Korrake neid samme teiste klientide puhul.

5.  NAF-koodide ja müüjate maksukohustuslase koodide määramiseks minge asukohta **Võlad** &gt; **Müüjad** &gt; **Kõik müüjad** ja järgige järgmisi samme.

    1.  Valige hankija.

    2.  Sisestage kiirkaardi **Arve ja tarne** jaotise **Käibemaks** väljale **Maksukohuslase kood** müüja maksukohuslase kood.

    3.  Kiirkaardil **Ostudemograafia** väljal **Prantsuse siret** sisestage ettevõtte Siret-number.

    4.  Sisestage väljal **NAF-kood** ettevõtte NAF-kood.

    5.  Korrake neid samme teiste müüjate puhul.

6.  Minge **Maks** &gt; **Seadistamine** &gt; **Väliskaubandus** &gt; **Intrastati kompressioon** ja valige väljad, mida tuleb Intrastati teabe summeerimisel võrrelda. Prantsuse Intrastati puhul valige **Statistika protseduur**, **Päritolu**, **Lähteriik/-regioon**, **Tarnetingimused**, **Transport**, **Parandus**, **Riik/regioon**, **Lähte või sihtriik**. **Suund**, **Saatja riik/regioon**, **Saatja olek**, **Olek**, **Kandekood**, **Kaup**.

7.  Minge **Laohaldus** &gt; **Seadistus** &gt; **Ladu** &gt; **Laod**, valige ladu ja järgige järgmisi samme.

    1.  Kiirkaardil **Aadressid** valige **Lisa** või **Redigeeri**.

    2.  Valige dialoogiboksi väljal **Linn** lao linn. Linna olekut kasutatakse teie DEB-aruande jaoks maakonnana.

### <a name="ngp-codes"></a>NGP-koodid

DEB aruandes koosneb toodete kodifitseerimine järgmistest elementidest.

1.  Kaheksakohaline CN8-kood, mis esindab EL-i tariifi ja statistika nomenklatuuri.

2.  Vajadusel ühekohaline Nomenclature Générale des Produits (NGP) riiklik kaubakood.

2021. aastal rakendub NGP ainult kolmele tootetüübile:

-   mõned tooted lehmalt, lambalt või kitselt

-   Sõjaväevarustus

-   Prantsuse veinid

Peate seadistama NGP-koodid ja määrama need seotud toodetele. Väli **NGP** seatakse seejärel automaatselt **Intrastati töölehe** lehel.

#### <a name="set-up-an-ngp-code"></a>NGP-koodi seadistamine

1.  Avage **Maks** &gt; **Seadistus** &gt; **Väliskaubandus** &gt; **NGP-koodid**.

2.  NGP-koodi loomiseks valige toimingupaanilt suvand **Uus**.

3.  Sisestage väljal **NGP** ühekohaline kood.

4.  Sisestage väljale **Kirjeldus** koodi kirjeldus.

#### <a name="assign-an-ngp-code-to-a-product"></a>NGP-koodi määramine tootele

1.  Avage **Tooteteabe haldus** &gt; **Tooted** &gt; **Väljastatud tooted**.

2.  Valige ruudustikus toode.

3.  Valige kiirkaardi **Väliskaubandus** jaotise **Intrastat** väljal **NGP** sobiv NGP-kood.

## <a name="intrastat-journal"></a>Intrastati tööleht

Minge **Maks** &gt; **Deklaratsioonid** &gt; **Välis** **kaubandus** &gt; **Intrastat**, et hallata oma kandeid, mida saab kasutada väliskaubanduses EL-iga. Lisateavet leiate jaotisest [Intrastati ülevaade](emea-intrastat.md).

Veerg **NGP** on Prantsusmaale omane. See näitab toote NGP-koodi. Kui NGP ei ole toote puhul rakendatav, kuvatakse väärtus **0** (null). Saate NGP-koodi korrigeerida. Valige kanne ja seejärel valige NGP-kood väljal **NGP** jaotises **Koodid** vahekaardil **Üldine**.

### <a name="intrastat-transfer"></a>Intrastati ülekanne

**Intrastati** lehel saate valida tegevuspaanil valiku **Ülekanne**, et edastada automaatselt oma müügitellimuste, vabas vormis arvete, ostutellimuste, hankija arvete, hankija toote sissetulekute, projektiarvete ja üleviimistellimuste teabe automaatne ülekandmine. Edastatakse ainult dokumendid, mille sihtriigiks või -piirkonnaks (lähetamiseks) või saadetiseks (saabumiseks) on ELi riik.

Kuna DEB aruanne on ELi müüginimekirja ja Intrastati aruande kombinatsioon, sisaldab see ka *kolmnurkseid* tehinguid, kus otsetarned tehakse ühest ELi riigist (osapool A) teise ELi riiki (osapool C) ja Prantsusmaa juriidiline isik (osapool B) on kolmnurkse tehingu keskel.

### <a name="generate-a-deb-intrastat-report"></a>DEB (Intrastat) aruande loomine

1.  Avage **Maks** &gt; **Deklaratsioonid** &gt; **Väliskaubandus** &gt; **Intrastat**.

2.  Toimingupaanil valige suvandid **Väljund** &gt; **Aruanne**.

3.  Määrake dialoogiboksis **Intrastati aruanne** järgmised väljad.

| Field            | Kirjeldus                                                                                                                         |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Alates kuupäevast        | Valige aruande alguskuupäev.                                                                                               |
| Lõppkuupäev          | Valige aruande lõppkuupäev.                                                                                                 |
| Loo fail    | Tekstifaili genereerimiseks määrake suvandi väärtuseks **Jah**.                                                                                 |
| Faili nimi        | Sisestage oma Intrastati aruande jaoks .txt-faili nimi.                                                                          |
| Aruande loomine  | XML-faili genereerimiseks määrake suvandi väärtuseks **Jah**.                                                                                |
| Aruandefaili nimi | Sisestage nõutav nimi.                                                                                                            |
| Ainult parandused | Seadistage see suvand olekusse **Jah**, et raporteerida ainult parandused. Seadke väärtuseks **Ei**, et teatada nii tavakannetest kui parandustest.         |
| Direction        | Valige ühendusesiseste saabumiste aruande jaoks **Saabumised**. Valige ühendusesiseste lähetuste aruande jaoks **Lähetused**. |

## <a name="example"></a>Näide

Järgnev näide näitab, kuidas seadistada ja töötada NGP-koodidega. See kasutab **DEMF** juriidilist isikut.

1.  [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) ühiskasutusega varateegis laadige Intrastati deklaratsiooni vormingu jaoks alla järgmiste ER-konfiguratsioonide viimased versioonid:

-   Intrastati mudel

-   Intrastat-aruanne

-   Intrastat INTRACOM (FR)

2.  Seadistage rakenduses Finance kandekood.

    1.  Avage **Maks** &gt; **Seadistus** &gt; **Väliskaubandus** &gt; **Kandekoodid**.

    2.  Valige toimingupaanil nupp **Uus**.

    3.  Sisestage väljas **Kandekood** **11**.

    4.  Välja **Nimi** sisestage väärtus **Ost või müük**.

    5.  Valige toimingupaanil nupp **Salvesta**.

3.  Seadistage jaemüügi tootehierarhia järgmiselt.

    1.  Minge jaotisse **Tooteteabe haldus** &gt; **Seadistus** &gt; **Kategooriad ja atribuudid** &gt; **Kategooriahierarhiad**.

    2.  Valige ruudustikus **Intrastat**. Valige tegumiriba vahekaardi **Kategooria hierarhia** grupis **Halda** suvand **Redigeeri**.

    3.  Valige Toimingupaanil nupp **Uus kategooria sõlm**.

    4.  Välja **Nimi** sisestage väärtus **Autres Libournais**.

    5.  Sisestage väljas **Kood** **2204 21 42**

    6.  Valige toimingupaanil nupp **Salvesta**.

4.  Minge **Maksud** &gt; **Seadistamine** &gt; **Väliskaubandus** &gt; **Väliskaubanduse parameetrid** ja järgige järgmisi samme.

    1.  Valige vahekaardil **Intrastat** kiirkaardil **Üldine** väljal **Kandekood** väärtus **11**.

    2.  Valige kiirkaardi **Elektroonilise aruandlus** väljal **Failivormingu vastendamine** **Intrastat INTRACOM (FR)**.

    3.  Sisestage või valige väärtus **Intrastati aruanne** väljal **Aruandevormingu vastendamine**.

    4.  Valige kiirkaardi **Kaubaartikli hierarhia** väljal **Kategooriahierarhia** väärtus **Intrastat**.

5.  NGP-koodi seadistamine.

    1.  Avage **Maks** &gt; **Seadistus** &gt; **Väliskaubandus** &gt; **NGP-koodid**.

    2.  Valige toimingupaanil nupp **Uus**.

    3.  Sisestage väljale **NGP** väärtus **8**.

    4.  Sisestage väljale **Kirjelduse nimi** väärtus **NGP 8**.

    5.  Valige toimingupaanil nupp **Salvesta**.

6.  NGP-koodi määramine tootele.

    1.  Avage **Tooteteabe haldus** &gt; **Tooted** &gt; **Väljastatud tooted**.

    2.  Valige ruudustikus **0001**.

    3.  Kiirkaardi **Väliskaubandus** väljal **NGP** valige **8**.

    4.  Valige väljal **Kaup** väärtus **2204 21 42**.

    5.  Valige toimingupaanil nupp **Salvesta**.

7.  Looge müügitellimus, mis sisaldab uut toodet.

    1.  Avage **Müügireskontro** &gt; **Tellimused** &gt; **Kõik müügitellimused**.

    2.  Valige toimingupaanil nupp **Uus**.

    3.  Valige dialoogiboksi **Loo** **müügi** **tellimus** jaotises **Klient** väljas **Kliendi** **konto** väärtus **100001**.

    4.  Valige aadressi loomiseks jaotise **Aadress** väljal **Tarneaadress** plussmärk (**+**).

    5.  Sisestage dialoogiaknas **Uus aadress** väljale **Kirjelduse nimi** **Saksamaa**.

    6.  Väljal **Riik/regioon** valige **DEU**.

    7.  Valige nupp **OK**.

    8.  Valige dialoogiaknas **Loo müügiorder** **OK**.

    9.  Valige kiirkaardi **Müügi** **tellimuse ridade** väljal **Kaubakood** väärtus **0001**.

    10. Valige toimingupaanil nupp **Salvesta**.

    11. Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.

    12. Valige dialoogiboksi **Arve sisestamine** kiirkaardi **Parameetrid** jaotises **Parameeter** väljal **Kogus** suvand **Kõik**. Seejärel valige arve esitamiseks **OK**.

8.  DEB-aruande loomine.

    1.  Avage **Maks** &gt; **Deklaratsioonid** &gt; **Väliskaubandus** &gt; **Intrastat**:

    2.  Tegumiribal. valige **Saada**.

    3.  Seadke dialoogiboksi **Intrastat (ülekanne)** jaotises **Parameetrid** valiku **Kliendiarve** väärtuseks **Jah**. Seejärel valige **OK**.

    4.  Sordib kanded välja **Kuupäev** järgi. Ülemine kanne on tulemuse kanne. Väli **NGP** seatakse automaatselt.

    5.  Toimingupaanil valige suvandid **Väljund** &gt; **Aruanne**.

    6.  Valige dialoogiboksi **Intrastat-aruanne** kiirkaardil **Parameetrid** jaotises **Kuupäev** loodud müügitellimuse kuu.

    7.  Seadke jaotises **Ekspordi suvandid** suvandi **Loo fail** väärtuseks **Jah**.

    8.  Sisestage faili nõutav nimi väljale **Faili nimi**.

    9.  Valige **OK** ja vaadake aruanne üle.

