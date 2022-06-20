---
title: Testimise automatiseerimine elektroonilise aruandluse abil
description: See artikkel selgitab, kuidas te saate kasutada elektroonilise aruandluse (ER) raamistiku põhifunktsiooni funktsioonide automaatseks testimiseks.
author: NickSelin
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: df2baa988bb634db11d819dd84ef73eaa560bab9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892765"
---
# <a name="automate-testing-with-electronic-reporting"></a>Testimise automatiseerimine elektroonilise aruandluse abil

[!include[banner](../includes/banner.md)]

See artikkel selgitab, kuidas te saate kasutada elektroonilise aruandluse (ER) raamistikku mõne funktsiooni automaatseks testimiseks. Selles veerus toodud näide näitab, kuidas automatiseerida hankija makse töötlemise testimist.

Rakendus kasutab hankija maksetöötluse ajal makseväljade ja vastavate dokumentide loomiseks ER-raamistikku. ER-raamistik koosneb andmemudelist, mudeli vastendustest ja vorminduse komponentidest, mis toetavad makse töötlemist erinevate makseviiside jaoks ja erinevates vormingutes dokumentide loomist. Neid komponente saab alla laadida lahendusest Microsoft Dynamics Lifecycle Services (LCS) ja importida eksemplari.

Samuti saate kohandada igat Microsofti komponenti ja kasutada seda oma kohandatud komponendi põhjana. Kohandatud versiooni loomisega saate teha muudatusi, mis toetavad kindlaid nõudmisi. Näiteks saate korrigeerida ER-andmemudelit ja ER-mudeli vastendamist, et saada juurdepääs kliendipõhistele rakenduse andmetele, või muuta ER-vormingut loodud dokumendi paigutuse muutmiseks.

Saate kasutada oma eksemplaris kohandatud ER-vorminguid, et töödelda maksete faile, mis loovad hankija makseid ja töödelda ka protsessi juhtimise aruandeid. ER-komponentide puhul toetatakse versioonimist. Seetõttu võib Microsoft pakkuda hankija makse töötlemiseks ER-lahenduste värskendatud versioone ja teie saate värskendatud versiooni automaatselt oma kohandatud komponendiga uuele põhjale tuginedes ühendada. Siiski peate uue põhjaga versiooni testima, et veenduda selle ootuspärases toimimises.

ER-andmemudelid ja ER-mudelite vastendused on omased paljudele ER-vormingutele, mida kasutatakse erinevat tüüpi maksete töötlemiseks ja riigi-/piirkonnapõhiste maksedokumentide loomiseks. Seetõttu on ülimalt soovitatav automatiseerida kasutaja vastuvõtu ja integratsiooni testimine nii, et seda tehakse automaatselt mitmes ettevõttes, võttes arvesse iga sihtettevõtte riigi-/piirkonna konteksti, kasutades erinevaid andmekomplekte jne.

Lisateavet konfiguratsiooni pakkujalt saadud vormingul põhineva kohandatud vormingu versiooni loomise kohta leiate jaotisest [Elektrooniline aruandlus. Vormingu täiendamine uue alusversiooni kasutuselevõtuga](./tasks/er-upgrade-format.md).

## <a name="key-concepts"></a>Põhimõisted

Funktsionaalsed lauskasutajad saavad algatada kasutajate aktsepteerimise ja integreerimise testimist ilma, et peaksid lähtekoodi kirjutama.

- Kasutage ER-alusfunktsiooni loodud dokumentide ja põhieksemplaride võrdlemiseks. Lisainfo saamiseks vt [oodud aruandetulemite jälgimine ja nende võrdlemine alusväärtustega](er-trace-reports-compare-baseline.md).
- Kasutage tegevuse salvestajat testjuhtumite kirjendamiseks ja kaasake lähteolukorra hinnang. Lisateavet vt [Tegevuse salvestaja ressursid](../user-interface/task-recorder.md).
- Grupeerige testjuhtumid vajalike teststsenaariumite jaoks. Lisateavet vt [Kasutaja vastuvõtu testide loomine ja automatiseerimine](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).

    - Kasutage LCS-s äriprotsesside modelleerijat (BPM) kasutaja vastuvõtu testimise teekide tegemiseks.
    - Kasutage BPM-i testimise teeke katseplaani ja testkomplektide loomiseks lahenduses Microsoft Azure DevOps Services (Azure DevOps).

Funktsionaalsed lauskasutajad saavad teostada kasutajate vastuvõtu ja integreerimise testimist.

- Kasutage soovitud testkomplekti testjuhtumite teostamiseks tööriista Regression suite automation tool (RSAT).
- Teatage testitulemused Azure DevOps-ile ja kasutage seda teenust nende tulemuste uurimiseks.

## <a name="prerequisites"></a>Eeltingimused

Enne kui saate selles artiklis olevad ülesanded lõpule viia, peate lõpule täitma järgmised eeltingimused:

- Rakendage topoloogiat, mis toetab testimise automatiseerimist. **Süsteemi administraatori** rolli jaoks peab teil olema juurdepääs selle topoloogia eksemplarile. See topoloogia peab sisaldama demo andmeid, mida selles näites kasutatakse. Lisateavet vt [Pideva koostamise ja testimise automaatikat toetavate keskkondade juurutamine ja kasutamine](../perf-test/continuous-build-test-automation.md).
- Kasutaja vastuvõtu ja integreerimise testide automaatseks teostamiseks peate paigaldama RSATi topoloogiasse, mida kasutate, ja selle sobivalt konfigureerima. Lisainfot RSATi installimise ja konfigureerimise ning Finance and Operations rakenduste ja Azure DevOps'iga toimimise konfigureerimise kohta vt [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357). Pöörake tähelepanu tööriista kasutamise eeltingimustele. Järgmisel joonisel on näide RSATi seadistuste kohta. Sinine ristkülik ümbritseb parameetrid, mis määravad juurdepääsu Azure DevOps-ile. Roheline ristkülik ümbritseb parameetrid, mis määravad juurdepääsu eksemplarile.

    ![RSAT sätted.](media/GER-Configure.png "RSAT-i sätete dialoogiboksi kuvatõmmis")

- Testjuhtumite õige käivitusjärjestuse tagamiseks komplektidesse sorteerimiseks, et saaksite koguda testkäivituste logisid edasiseks aruandluseks ja uurimiseks, peab teil olema rakendatud topoloogiast juurdepääs Azure DevOps-ile.
- Selle artikli näite lõpuleviimiseks on soovitatav RSAT-testide [jaoks alla laadida ER kasutus](https://go.microsoft.com/fwlink/?linkid=874684). See zip-fail sisaldab järgmisi tegevusjuhiseid.

    | Sisu                                           | Faili nimi ja asukoht |
    |---------------------------------------------------|------------------------|
    | Andmete testimiseks ettevalmistamise tegevuse salvestamise näidis | Ettevalmistamine\\Recording.xml |
    | Hankija makse töötlemise tegevuse salvestamise näidis   | Töötlus\\Recording.xml |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a>Valmistage ostureskontro moodul hankija maksete töötlemiseks ette

1. Logige oma eksemplari sisse.
2. Laadige järgmised ER-konfiguratsioonid LCS-ist alla. Juhiste saamiseks vt [Elektroonilise aruande konfiguratsiooni importimine teenusest Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).

    - **Maksemudel** ER-mudeli konfiguratsioon
    - **Maksemudeli vastendamine 1611** ER-mudeli vastendamise konfiguratsioon
    - **BACS (UK)** ER-vormingu konfiguratsioon

    ![Elektroonilise aruandluse konfiguratsioonid.](media/GER-Configurations.png "Elektroonilise aruandluse konfiguratsioonide lehe kuvatõmmis")

3. Valige **GBSI** demo andmete ettevõte, millel on riigi-/piirkonna kontekst Suurbritannias.
4. Ostureskontro parameetrite konfigureerimine.

    1. Avage **Ostureskonto \> Makse seadistus \> Makseviisid**.
    2. Valige **Elektrooniline** makseviis.
    3. Konfigureerige valitud makseviis nii, et see kasutab **BACS (UK)** ER-vormingut, mille varem hankija makse töötlemiseks alla laadisite.

        1. Seadistage kiirkaardil **Failivormingud** suvand **Üldine elektrooniline ekspordivorming** valikule **Jah**.
        2. Valige väljal **Vormingu konfiguratsiooni eksportimine** **BACS (UK)**.

    ![Makseviiside leht.](media/GER-APParameters.png "Makseviiside lehe kuvatõmmis")

    > [!NOTE]
    > Kui teil on selle ER-vormingu tuletatud versioon, mis loodi kohanduste toetamiseks, saate valida selle konfiguratsiooni makseviisi **Elektrooniline** alt.

5. Looge hankija makse näidis.

    1. Avage **Ostureskonto \> Maksed \> Maksete tööleht**.
    2. Veenduge, et te ei ole maksete töölehte sisestanud.

        ![Maksete töölehe leht.](media/GER-APJournal.png "Maksete töölehe lehe kuvatõmmis")

    3. Valige **Read** ja sisestage rida, millel on järgmised andmed.

        | Väli               | Näidisväärtus   |
        |---------------------|-----------------|
        | Hankija nimi         | GB\_SI\_000001  |
        | Debiteeri               | 1,000.00        |
        | Valuuta            | GBP             |
        | Vastaskonto tüüp | Pank            |
        | Vastaskonto      | GBSI OPER       |
        | Makseviis   | Elektrooniline      |

    ![Hankija maksete leht.](media/GER-APJournalLines.png "Hankija maksete lehe kuvatõmmis")

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a>Valmistage ER-raamistik hankija maksete töötlemise testimiseks ette

### <a name="configure-er-parameters"></a>Elektroonilise aruandluse parameetrite konfigureerimine

1. Avage **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Elektroonilise aruandluse parameetrid**.
2. Vali vahekaardi **Manused** väljal **Alus** selleks dokumenditüübiks **Fail**, mida dokumendihalduse (DM) raamistik kasutab DM-manustena alusfunktsiooniga seotud dokumentide hoidmiseks.

    ![Elektroonilise aruandluse parameetrite leht.](media/GER-ERParameters.png "Elektroonilise aruandluse parameetrite lehe kuvatõmmis")

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a>Handkija maksetega seotud dokumentide algkoopiate loomine

1. Avage **Ostureskonto \> Maksed \> Maksete tööleht**.
2. Valige **Read**.
3. Valige **Loo maksed**.
4. Valige **Elektrooniline** makseviis.
5. Valige **GBSI OPER** pangakonto.
6. Seadistage valik **Kontrollaruande printimine** olekusse **Jah**.
7. Laadige loodud väljund zip-failina alla.
8. Avage allalaaditud fail.
9. Ekstraktige allalaaditud failist järgmised failid.

    - **Fail** maksefail tekstivormingus
    - **ERVendOutPaymControlReport** kontrollaruande fail XLSX-vormingus

    ![Ekstraktitud failid.](media/GER-APJournalProcessed.png "Kuvatõmmis ekstraktitud failide nimedest Windows Exploreris")

### <a name="turn-on-the-er-baseline-feature"></a>ER-alusfunktsiooni sisselülitamine

1. Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.
2. Valige tegumiriba **Konfiguratsioonid** vahekaardil **Kasutaja parameetrid**.
3. Määrake suvand **Käivita silumisrežiimis** valikule **Jah**.

Lülitades parameetri **Käivita silumisrežiimis** sisse, sunnite ER-raamistiku pärast mistahes väljuvaid dokumente loova ER-vormingu käivitamist teostama järgmisi tegevusi.

1. Määratlege, kas täidetud ER-vormingu mistahes komponentidele on konfigureeritud algväärtus.
2. Tehke kindlaks, kas iga konfigureeritud algväärtus on kohaldatav praegustele tingimustele (sisselogitud ettevõtte ettevõtte kood, failinimi ja genereeritud väljundi failinime laiend jne).
3. Iga kohaldatava algväärtuse korral tehke järgmised toimingud.

    1. Võrrelge ER-vormingu täitmisel loodud väljundit vastava algväärtusega.
    2. Talletage võrdluse tulemused ER-konfiguratsioonide silumislogis.

### <a name="configure-er-baselines-for-vendor-payment-processing"></a>Hankija maksete töötlemise ER-algväärtuste konfigureerimine

1. Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.
2. Valige suvand **Alused**.
3. Valige suvand **Uus**.
4. Valige väljal **Viide** vorming **BACS (UK)**.
5. Valige suvand **Manused**.
6. Lisage hankija makse failile uus algväärtus.

    1. Valige suvand **Uus**.
    2. Valige väljal **Tüüp** dokumendihalduse dokumendi tüüp **Fail**, mille konfigureerisite algväärtuse artefakti talletamise ER-parameetrites.
    3. Sirvige kohalikult salvestatud **Fail** maksefaili tekstivormingus.
    4. Sisestage väljale **Kirjeldus** **Makse TXT fail**.

7. Lisage hankija makse kontrollaruandele uus algväärtus.

    1. Valige suvand **Uus**.
    2. Valige väljal **Tüüp** dokumendihalduse dokumendi tüüp **Fail**, mille konfigureerisite algväärtuse artefakti talletamise ER-parameetrites.
    3. Sirvige, et valida kohalikult salvestatud **ERVendOutPaymControlReport** kontrollaruanne XLSX vormingus.
    4. Sisestage väljale **Kirjeldus** **Makse XLSX kontrollaruanne**.

    ![Hankija makse faili ja kontrollaruande algväärtused.](media/GER-BaselineAttachments.png "Kuvatõmmis valitud makse XLSX kontrollaruandega konfiguratsioonilehest")

8. Sulgege leht.
9. Valige kiirkaardil **Algväätused** suvand **Uus**, et konfigureerida maksefaili algväärtus.

    1. Pange reale nimeks **Maksefaili alussätted**.
    2. Valige väljal **Faili komponendi nimi** suvand **fail**, et rakendada see algväärtus sellele ER-vormingu väljundile, mis genereerib maksefaili BACS (UK) tekstivormingus.
    3. Valige väljal **Ettevõtted** suvand **GBSI**, et rakendada seda algväärtust siis, kui GBSI ettevõttes kasutatakse **BACS (UK)** ER-vormingut.
    4. Sisestage väljale **Failinime mask** **\*.TXT**, et rakendada seda algväärtust ainule neile vormingu **fail** komponentide väljunditele, mille failinime laiendiks on **.txt**.
    5. Valige väljal **Algväärtus** suvand **Makse TXT fail**, et seda algväärtust kasutataks loodud väljundiga võrdlemiseks.

10. Valige **Uus**, et konfigureerida kontrollaruandele algväärtus.

    1. Pange reale nimeks **Kontrollaruande alussätted**.
    2. Valige väljal **Faili komponendi nimi** suvand **ERVendOutPaymControlReport**, et rakendada see algväärtus sellele ER-vormingu väljundile, mis genereerib kontrollaruande.
    3. Valige väljal **Ettevõtted** suvand **GBSI**, et rakendada seda algväärtust siis, kui GBSI ettevõttes kasutatakse **BACS (UK)** ER-vormingut.
    4. Sisestage väljale **Failinime mask** **\*.XLSX**, et rakendada seda algväärtust ainule neile vormingu **ERVendOutPaymControlReport** komponentide väljunditele, mille failinime laiendiks on **.xslx**.
    5. Valige väljal **Algväärtus** suvand **Makse XLSX kontrollaruanne**, et seda algväärtust kasutataks loodud väljundiga võrdlemiseks.

    ![Kiirkaart Algväärtused konfiguratsioonide lehel.](media/GER-BaselineRules.png "Kuvatõmmis kiirkaardist Väärtused konfiguratsioonide lehel")

## <a name="record-tests-to-validate-vendor-payment-processing"></a>Kirjendab testid hankija maksete töötlemise kinnitamiseks

Funktsionaalse lauskasutajana saate kirjendada oma samme hankija maksete töötlemise testimiseks. Soovitame teil esitada (ja vastavalt vajadusele redigeerida) tegevuse salvestist **Ettevalmistamine\\Recording.xml**, mille varem alla laadisite. Seda salvestust kasutatakse kõiki testimisandmete õigesse olekusse seadistamiseks. See samm on vajalik, sest testimist saab teha mitu korda ja iga katse peab kasutama andmeid, mis on samas olekus.

### <a name="reset-user-settings"></a>Kasutajasätete lähtestamine

1. Avage vaikearmatuurlaud.
2. Valige nupp **Sätted** (hammasratta sümbol).
3. Valige **Kasutaja valikud**.
4. Valige **Kasutusandmed**.
5. Valige **Lähtesta**.
6. Valige **Jah**, et kinnitada, et soovite kasutusandmeid lähtestada.
7. Sulgege leht.

### <a name="record-the-steps-to-prepare-data-for-testing"></a>Kirjendage andmete testimiseks ettevalmistamise sammud

1. Valige nupp **Sätted** (hammasratta sümbol).
2. Valige **Tegevuse salvestaja**.
3. Valige **Salvestise taasesitus**.
4. Valige **Ava sellest arvutist**.
5. Valige **Sirvi** ja valige kohalikult salvestatud **Ettevalmistamine\\Recording.,xml** fail.
6. Valige nupp **Alusta**.
7. Jätkake valiku **Esita järgmine ootel etapp** kuni salvestuse kõik etapid on esitatud.

Selle tegevuse salvestamine sooritab järgmised tegevused.

1. Seadke töödeldud makse rea olek väärtusele **Puudub**.

    ![Tegevuse salvestamise etapid 3 kuni 4.](media/GER-Recording1Review1.png "Kuvatõmmis tegevuse salvestamise etappidest 3 kuni 4")

2. Lülitage elektroonilise aruandluse kasutaja parameeter **Käivita silumisrežiimis** sisse.

    ![Tegevuse salvestamise etapid 9 kuni 10.](media/GER-Recording1Review2.png "Kuvatõmmis tegevuse salvestamise etappidest 9 kuni 10")

3. Puhastage see elektroonilise aruandluse silumislogi, mis sisaldab loodud failide ja algväärtuste võrdluse tulemusi.

    ![Tegevuse salvestamise etapid 13 kuni 15.](media/GER-Recording1Review3.png "Kuvatõmmis tegevuse salvestamise etappidest 13 kuni 15")

### <a name="record-the-steps-to-test-vendor-payment-processing"></a>Kirjendage hankija maksete töötlemise testimise etapid

Soovitame teil esitada (ja vastavalt vajadusele redigeerida) tegevuse salvestist **Töötlus\\Recording.xml**, mille varem alla laadisite. Seda salvestist kasutatakse hankija maksete töötlemiseks ja loodud dokumentide ja vastavate alusväärtuste võrdluse tulemuste kinnitamiseks.

1. Valige nupp **Sätted** (hammasratta sümbol).
2. Valige **Tegevuse salvestaja**.
3. Valige **Salvestise taasesitus**.
4. Valige **Ava sellest arvutist**.
5. Valige **Sirvi** ja valige kohalikult salvestatud **Töötlus\\Recording.,xml** fail.
6. Valige nupp **Alusta**.
7. Jätkake valiku **Esita järgmine ootel etapp** kuni salvestuse kõik etapid on esitatud.

Selle tegevuse salvestamine sooritab järgmised tegevused.

1. Hankija maksete töötlemise käivitamine.
2. Valige õiged käitamisaja parameetrid ja lülitage kontrollaruande loomine sisse.

    ![Tegevuse salvestamise etapid 3 kuni 8.](media/GER-Recording2Review1.png "Kuvatõmmis tegevuse salvestamise etappidest 3 kuni 8")

3. Avage see elektroonilise aruandluse silumislogi, et kirjendada loodud väljundite ja vastavate algväärtuste võrdluse tulemusi.

    Elektroonilise aruandluse silumislogis kuvatakse võrdlustulemusi väljal **Loodud tekst**. Väljad **Vormingu komponent** ja **Logikande põhjustanud vormingutee** viitavad faili komponendile, millele loodud väljundit on võrreldud algväärtusega.

    ![Elektroonilise aruandluse käitamise logide lehe kirjed.](media/GER-ERDebugLog.png "Elektroonilise aruandluse käitamise logide lehe kirjete kuvatõmmis")

4. Praeguse väljundi võrdlemine algväärtusega on kirjendatud kasutades tegevuse salvestaja suvandit **Kinnita** ja valides suvandi **Praegune väärtus**.

    ![Kinnitamise suvandi kasutamine praeguse väärtusega võrdlemiseks.](media/GER-TRRecordValidation.png "Kuvatõmmis kinnitamise suvandi kasutamisest praeguse väärtusega võrdlemiseks")

    Järgmisel joonisel on näha, millised salvestatud kinnitamise etapid tegevuse salvestises välja näevad.

    ![Tegevuse salvestamise etapid 13 ja15.](media/GER-Recording2Review2.png "Kuvatõmmis tegevuse salvestamise etappidest 13 ja 15")

## <a name="add-the-recorded-tests-to-azure-devops"></a>Lisage salvestatud testid Azure DevOps-i

1. Avage Azure DevOps-i keskkond.
2. Valige projekt, mille määratlesite RSATi parameetrites, kui [konfigureerisite tööriista](#prerequisites).
3. Valige katseplaan, mille määratlesite RSATi parameetrites, kui [konfigureerisite tööriista](#prerequisites).
4. Looge valitud katseplaanile uus testjuhtum.

    1. Pange testjuhtumi nimeks **Hankija elektroonilise makse testtöötluseks andmete ettevalmistamine**.
    2. Manustage fail **Recording.xml** kaustast **Ettevalmistamine**, mille varem alla laadisite.

5. Looge valitud katseplaanile uus testjuhtum.

    1. Pane testjuhtumi nimeks **Hankija maksete testtöötlemine kasutades ER-vormingut BACS (UK)**.
    2. Manustage fail **Recording.xml** kaustast **Töötlemine**, mille varem alla laadisite.

    ![Uued testjuhtumid valitud katseplaani jaoks.](media/GER-RSAT-DevOps-Tests-Passed.png "Kuvatõmmis uutest testjuhtumitest valitud katseplaani jaoks")

> [!NOTE]
> Pöörake tähelepanu lisatud testide õigele käivitamisjärjekorrale.

## <a name="prepare-rsat-to-run-the-recorded-tests"></a>Valmistage RSAT ette salvestatud testide käivitamiseks

### <a name="load-the-tests-from-azure-devops-to-rsat"></a>Laadige testid Azure DevOps-ist RSAT-sse

1. Avab kohalik RSATi rakendus praeguses topoloogias.
2. Valige **Lae**, et laadida praegu Azure DevOps-is olevad testid RSAT-sse.

    ![RSAT-sse laetud testid.](media/GER-RSAT-RSAT-Tests-Loaded.png "Kuvatõmmis RSAT-sse laetud testidest")

### <a name="create-automation-and-parameters-files"></a>Automatiseerimise ja parameetrite failide loomine

1. Valige RSAT-is testid, mida soovite Azure DevOps-ist laadida.
2. Valige RSAT-i automatiseerimise ja parameetrite failide loomiseks **Uus**.

    ![RSAT-is loodud RSAT-i automatiseerimise ja parameetrite failid.](media/GER-RSAT-RSAT-Tests-Initiated.png "Kuvatõmmis RSAT-is loodud RSAT-i automatiseerimise ja parameetrite failidest")

### <a name="modify-the-parameters-files"></a>Parameetrite failide muutmine

1. Valige RSATis testjuhtum **Hankija elektroonilise makse testtöötluseks andmete ettevalmistamine**.
2. Valige suvand **Redigeeri**.
3. Muutke Microsoft Excel-i avatud töövihikus töölehel **Üldine** ettevõtte koodiks **GBSI**, sest seda ettevõtted kasutatakse katse teostamiseks.
4. Valige RSAT-is testjuhtum **Hankija maksete testtöötlemine kasutades ER-vormingut BACS (UK)**.
5. Valige suvand **Redigeeri**.
6. Muutke avatud Exceli töövihikus töölehel **Üldine** ettevõtte koodiks **GBSI**.
7. Pange tähele töölehel **ERFormatMappingRunLogTable**, et lahtrid A:3 ja C:3 sisaldavad elektroonilise aruandluse silumislogi tabeli väljade teksti, mida kasutatakse tulemuste kinnitamiseks võrreldes algväärtuse väljundiga. Neid tekste kasutatakse nende elektroonilise aruandluse silumislogi kirjete hindamiseks, mis katse käigus loodi.

    ![ERFormatMappingRunLogTable tööleht.](media/GER-RSAT-RSAT-ExcelParameters.png "Kuvatõmmis ERFormatMappingRunLogTable töölehest")

## <a name="run-the-tests-and-analyze-the-results"></a>Testide teostamine ja tulemuste analüüs

### <a name="run-the-tests-in-rsat"></a>Teostage RSATis testid

1. Valige RSATis laaditud testid.
2. Valige käsk **Käitus**.

Pange tähele, et testjutumid käivitatakse rakenduses automaatselt veebibrauseri abil.

### <a name="analyze-the-results-of-test-execution"></a>Testitulemuste analüüsimine

Testitulemused salvestatakse RSATis. Pange tähele, et mõlemad testid on läbitud.

![RSAT-i läbinud testid.](media/GER-RSAT-RSAT-Tests-Passed.png "Kuvatõmmis RSAT-i läbinud testidest")

Pange tähele, et testitulemused saadetakse ka rakendusse Azure DevOps et saaksite teha edasisi analüüse.

![Testitulemused rakenduses Azure DevOps.](media/GER-RSAT-DevOps-Tests-Added.png "Kuvatõmmis testitulemustest rakenduses Azure DevOps")

### <a name="simulate-a-situation-where-tests-fail"></a>Testide ebaõnnestumise simuleerimine

See testikomplekt peab nurjuma, kui vähemalt üks loodud väljunditest ei vasta vastavale algväärtusele. Selle olukorra saavutamiseks saate kasutada oma tuletatud versiooni **BACS (UK)** vormingust, mis loob makse faili, millel on erinev sisu kui vastaval algväärtusel. Selle olukorra simuleerimiseks saate kasutada sama **BACS (UK)** vormingut, kuid muutke makse summat töödeldud makse real.

1. Avage rakendus ja minge lehele **Makstaolevad arved \> Maksed \> Maksepäevik**.
2. Valige **Read**.
3. Valige makse rida ja seejärel valige **Makse olek \> Puudub**.
4. Muutke välja **Deebet** väärtus **1 000,00** pealt **2 000,00** peale.
5. Oma muudatuste salvestamiseks valige **Salvesta**.

### <a name="run-the-tests-in-rsat"></a>Teostage RSATis testid

1. Valige RSATis laaditud testid.
2. Valige käsk **Käitus**.

Pange tähele, et testjutumid käivitatakse rakenduses automaatselt veebibrauseri abil.

### <a name="analyze-the-results-of-test-execution"></a>Testitulemuste analüüsimine

Testitulemused salvestatakse RSATis. Pange tähele, et teine katse nurjus teise käivitamise ajal.

![Nurjunud testi tulemused RSAT-is.](media/GER-RSAT-RSAT-Tests-Failed.png "Kuvatõmmis nurjunud testi tulemustest RSAT-is")

Pange tähele, et testitulemused saadetakse ka rakendusse Azure DevOps et saaksite teha edasisi analüüse.

![Nurjunud testi tulemused rakenduses Azure DevOps.](media/GER-RSAT-DevOps-Tests-Failed.png "Kuvatõmmis nurjunud testi tulemustest rakenduses Azure DevOps")

Saade juurdepääsu iga testi olekule. Saate juurdepääsu ka käivitamise logile, et saaksite analüüsida mistahes nurjumise põhjuseid. Järgmisel joonisel näitab käivitamis elogi, et tõrge tekkis seetõttu, et loodud makse faili ja selle algväärtuse sisu oli erinev.

![Käivitumise logi rakenduses Azure DevOps nurjumise analüüsimiseks.](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Kuvatõmmis käivituse logist rakenduses Azure DevOps nurjumise analüüsimiseks")

Seetõttu, nagu olete näinud, saab mis tahes ER-vormingu toimimist hinnata automaatselt, kasutades RSAT testimise platvormina ja kasutades tegevuse salvestajal põhinevaid testjuhtumeid, mis kasutavad ER-i algväärtuse funktsiooni.

## <a name="additional-resources"></a>Lisaressursid

- [Tegevuse salvestaja ressursid](../user-interface/task-recorder.md)
- [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357)
- [Kasutaja vastuvõtu testide loomine ja automatiseerimine](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [Pideva koostamise ja testimise automaatikat toetavate keskkondade juurutamine ja kasutamine](../perf-test/continuous-build-test-automation.md)
- [Loodud aruandetulemite jälgimine ja nende võrdlemine alusväärtustega](er-trace-reports-compare-baseline.md)
- [Elektrooniline aruandlus. Vormingu täiendamine uue alusversiooni kasutuselevõtuga](tasks/er-upgrade-format.md)
- [Elektroonilise aruande konfiguratsiooni importimine teenusest Lifecycle Services](tasks/er-import-configuration-lifecycle-services.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]