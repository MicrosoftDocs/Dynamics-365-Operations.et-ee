---
title: ER-vormingu parameetrite seadistamine juriidilise isiku kohta
description: Selles teemas selgitatakse, kuidas seadistada elektroonilise aruandluse (ER) vormingu parameetreid juriidilise isiku kohta.
author: NickSelin
ms.date: 10/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 0fce566bea6340b4016e559b1f5f1764a6881e28
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675389"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>ER-vormingu parameetrite seadistamine juriidilise isiku kohta

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a>Eeltingimused

Nende etappide lõpetamiseks peate kõigepealt läbima etapid teemas [ER-vormingute konfigureerimine juriidilise isiku kohta määratud parameetrite kasutamiseks](er-app-specific-parameters-configure-format.md).

Selles teemas toodud näidete läbimiseks peab teil olema juurdepääs rakendusele Microsoft Dynamics 365 Finance ühega järgmistest rollidest:

- Elektroonilise aruandluse arendaja
- Elektroonilise aruandluse funktsionaalne konsultant
- Süsteemiadministraator

## <a name="import-er-configurations"></a>Elektroonilise aruandluse konfiguratsioonide importimine
ER-i konfiguratsioonide importimiseks järgige järgmisi samme: 

1. Logige oma keskkonda sisse.
2. Valige vaikimisi armatuurlaual **Elektrooniline aruandlus**.
3. Valige **Aruandluse konfiguratsioonid**.
4. Importige Finance’i praegusesse eksemplari konfiguratsioonid, mille eksportisite teenusest Regulatory Configuration Services (RCS), läbides etappe teemas [ER-vormingute konfigureerimine juriidilise isiku kohta määratud parameetrite kasutamiseks](er-app-specific-parameters-configure-format.md). Järgige neid etappe iga [Elektroonilise aruandluse (ER)](general-electronic-reporting.md) konfiguratsiooni jaoks järgmises järjekorras: andmemudel, mudeli vastendamine ja vormingud.

    1. Valige suvandid **Vahetus \> Laadi XML-failist**.
    2. Valige käsk **Sirvi**, et valida nõutava ER-i konfiguratsiooni jaoks XML-vormingus fail.
    3. Valige nupp **OK**.

    Järgmisel joonisel on näha konfiguratsioonid, mis teil lõpetades olema peavad.

    ![ER-i konfiguratsiooni leht.](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>DEMF-i ettevõtte parameetrite seadistamine

Saate kasutada ER-raamistikku rakendusekohaste parameetrite seadistamiseks ER-vormingu jaoks.

1. Valige juriidiline isik **DEMF**.
2. Valige konfiguratsioonipuust vorming **Vorming LE-andmete otsingu õppimiseks**.
3. Tehke tegumiriba vahekaardil **Konfiguratsioonid** grupis **Rakendusekohased parameetrid** valik **Seadistus**.

    ![ER-i rakendusespetsiifiliste parameetrite leht parameetrite häälestamiseks.](./media/GER-AppSpecParms-LookupForm.PNG)

    Lehel **Rakendusekohased parameetrid** saate konfigureerida vormingu **Vorming LE-andmete otsingu õppimiseks** andmeallika **Valija** reeglid.

    Kui ER-vormingu alus sisaldab mitut tüübi **Otsing** andmeallikat, peate valima sobiva andmeallika kiirkaardilt **Otsingud**, enne kui saate alustada andmeallika reeglite konfigureerimist.

    Iga andmeallika jaoks saate konfigureerida eraldi reeglid valitud ER-vormingu iga versiooni kohta.

    ER-vormingu valitud versioonis saadaolevate kõikide otsingu andmeallikate kogu reeglite kogum moodustab ER-vormingu rakendusekohased parameetrid.

4. Valige ER-vormingu versioon **1.1.1**.
5. Valige kiirkaardil **Tingimused** käsk **Lisa**.
6. Uue kirje väljal **Kood** otsingu avamiseks valige ripploendi nool.

    Otsing kujutab valimiseks saadaolevate maksukoodide loendit. See loend tagastatakse andmeallikaga **Model.Data.Tax**, mis on konfigureeritud ER-vormingu aluses. Kuna see andmeallikas sisaldab välja **Nimi**, kuvatakse otsingus iga maksukoodi nimi.

    ![Koodi väli otsib ER-rakendusekohaste parameetrite lehte.](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)

7. Valige maksukood **VAT19**.
8. Uue kirje väljal **Otsingu tulemus** otsingu avamiseks valige ripploendi nool. Otsing kujutab vormingu loetelu TaxationLevel valimiseks saadaolevate väärtuste loendit.

    Pange tähele, et kui sisse logitud kasutaja eelistatud keeleks on valitud saksa keel, kuvatakse otsingu väärtuste sildid saksa keeles, eeldusel, et need on ER-vormingu aluses tõlgitud. Kui otsingu andmeallika silt on tõlgitud, kuvatakse see silt kasutaja eelistatud keeles vahekaardil **Otsingud**.

    ![Otsinguväli on ER-i rakendusespetsiifiliste parameetrite lehel saksa keeleks tõlgitud.](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9. Valige väärtus **Tavaline maksustamine**.

    Selle kirje lisades saate määratleda järgmise reegli: Kui vajalik on otsingu andmeallikas **Valija** ja maksukood **VAT19** edastatakse argumendina, tagastatakse nõutud maksustamistasemena tase **Tavaline maksustamine**.

10. Valige käsk **Lisa** ja tehke järgmist.

    1. Valige väljalt **Kood** maksukood **InVAT19**.
    2. Valige väljalt **Otsingu tulemus** väärtus **Tavaline maksustamine**.

11. Valige käsk **Lisa** ja tehke järgmist.

    1. Valige väljalt **Kood** maksukood **VAT7**.
    2. Valige väljalt **Otsingu tulemus** väärtus **Vähendatud maksustamine**.

12. Valige käsk **Lisa** ja tehke järgmist.

    1. Valige väljalt **Kood** maksukood **InVAT7**.
    2. Valige väljalt **Otsingu tulemus** väärtus **Vähendatud maksustamine**.

13. Valige käsk **Lisa** ja tehke järgmist.

    1. Valige väljalt **Kood** maksukood **THIRD**.
    2. Valige väljalt **Otsingu tulemus** väärtus **Maksustamine puudub**.

14. Valige käsk **Lisa** ja tehke järgmist.

    1. Valige väljalt **Kood** maksukood **InVAT0**.
    2. Valige väljalt **Otsingu tulemus** väärtus **Maksustamine puudub**.

15. Valige käsk **Lisa** ja tehke järgmist.

    1. Valige väljalt **Kood** suvand **\*Mitte tühi\***.
    2. Valige väljalt **Otsingu tulemus** väärtus **Muu**.

    Selle viimase kirje lisades saate määratleda järgmise reegli: alati kui argumendina edastatud maksukood ei täida mõnda eeltoodud tingimustest, tagastab otsingu andmeallikas nõutud maksustamistasemena taseme **Muu**.

    ![Viimane lisatud kirje ER-rakendusekohaste parameetrite lehel.](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)

16. Valige väljalt **Olek** suvand **Lõpule viidud**.

    Kui käitate ER-vormingu versiooni, mille olek on **Lõpule viidud** või **Jagatud**, peab see reeglite kogum olema olekus **Lõpule viidud**. Muidu katkestatakse ER-vormingu aluse käivitamine, kui vorming üritab laadida andmeid sellest reeglite kogumist, kui käitatakse otsingu andmeallikat **Valija**.

    Kui käitate ER-vormingu versiooni, mille olek on **Mustand**, pääseb ER-vormingu alus sellele reeglite kogumile ligi, olenemata selle olekust.

17. Valige käsk **Salvesta**.
18. Sulgege leht **Rakendusekohased parameetrid**.

## <a name="run-the-er-format-in-the-demf-company"></a>ER-vormingu käitamine DEMF-i ettevõttes
ER-vormingu käitamiseks DEMF ettevõttes, järgige neid juhiseid: 

1. Valige konfiguratsioonipuust vorming **Vorming LE-andmete otsingu õppimiseks**.
2. Valige toimingupaanil käsk **Käivita**.
3. Kuvatavas dialoogiboksis tehke valik **OK**.
4. Laadige alla loodud aruanne ja salvestage see lokaalselt.

    Pange tähele, et loodud aruandes on maksukoodi **InVAT7** kokkuvõte pandud tasemele **Vähendatud** ning maksukoodide **VAT19** ja **InVA19** kokkuvõtted on pandud tasemele **Tavaline**. Selle käitumise määrab juriidilisest isikust oleneva reeglite kogumi konfiguratsioon.

5. Valige suvandid **Maks \> Kaudsed maksud \> Käibemaks \> Käibemaksukoodid**.
6. Valige maksukood **InVAT17**.
7. Valige toimingupaani vahekaardilt **Käibemaksu kood** grupis **Päringud** suvand **Sisestatud käibemaks**, et vaadata maksuväärtuse ja kohaldatava maksumäära teavet maksukoodi kohta.

    ![Sisestatud käibemaksu leht.](./media/GER-AppSpecParms-Statement.PNG)

8. Sulgege **sisestatud käibemaksu** leht.

## <a name="set-up-parameters-for-the-usmf-company"></a>USMF-i ettevõtte parameetrite seadistamine
USMF-ettevõtte parameetrite häälestamiseks läbige järgmised sammud: 

1. Valige juriidiline isik **USMF**.
2. Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.
3. Laiendage konfiguratsioonipuus üksust **Mudel parameetritega kõnede õppimiseks**, laiendage üksust **Vorming parameetritega kõnede õppimiseks** ja valige vorming **Vorming LE-andmete otsingu õppimiseks**.
4. Tehke tegumiriba vahekaardil **Konfiguratsioonid** grupis **Rakendusekohased parameetrid** valik **Seadistus**.
5. Valige valitud ER-vormingu versioon **1.1.1**.
6. Valige kiirkaardil **Tingimused** käsk **Lisa**.
7. Uue kirje väljal **Kood** otsingu avamiseks valige ripploendi nool.

    Otsing kujutab nüüd maksukoodide loendit ettevõtte **USMF** valitava maksu kohta.

    ![USMF-ettevõtte maksukoodid.](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)

8. Valige maksukood **EXEMPT**.
9. Valige uue kirje väljalt **Otsingu tulemus** väärtus **Maksustamine puudub**.
10. Valige **Lisa**.
11. Valige uue kirje väljalt **Kood** suvand **\*Mitte tühi\***.
12. Valige uue kirje väljalt **Otsingu tulemus** väärtus **Tavaline maksustamine**.
13. Valige väljalt **Olek** suvand **Lõpule viidud**.
14. Valige käsk **Salvesta**.

    ![ER-rakendusekohaste parameetrite leht.](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)

15. Sulgege leht **Rakendusekohased parameetrid**.

## <a name="run-the-er-format-in-the-usmf-company"></a>ER-vormingu käitamine USMF-i ettevõttes
ER-vormingu käitamiseks USMF ettevõttes, täitke järgmisi juhiseid:

1. Valige konfiguratsioonipuust vorming **Vorming LE-andmete otsingu õppimiseks**.
2. Valige toimingupaanil käsk **Käivita**.
3. Kuvatavas dialoogiboksis tehke valik **OK**.
4. Laadige alla loodud aruanne ja salvestage see lokaalselt.

    Pange tähele, et loodud aruandes olete nüüd uuesti kasutanud sama ER-vormingut teise juriidilise isiku jaoks, aga ER-vormingut korrigeerimata.

## <a name="reuse-legal-entitydependent-parameters"></a>Juriidilisest isikust sõltuvate parameetrite uuesti kasutamine

### <a name="duplicate-existing-parameters"></a>Olemasolevate parameetrite dubleerimine

#### <a name="export-parameters"></a>Ekspordiparameetrid
Parameetrite ekspordiks lõpetage järgmised toimingud:

1. Avage **Organisatsiooni haldamine \> Tööruumid \> Elektrooniline aruandlus**.
2. Valige **Aruandluse konfiguratsioonid**.
3. Valige konfiguratsioonipuust vorming **Vorming LE-andmete otsingu õppimiseks**.
4. Tehke tegumiriba vahekaardil **Konfiguratsioonid** grupis **Rakendusekohased parameetrid** valik **Seadistus**.
5. Valige ER-vormingu versioon **1.1.1**.
6. Valige toimingupaanil käsk **Ekspordi**.
7. Laadige alla loodud fail ja salvestage see lokaalselt.

    Konfigureeritud rakendusekohaste parameetrite kogum on nüüd eksporditud XML-failina.

#### <a name="import-parameters"></a>Parameetrite importimine
Parameetrite impordiks lõpetage järgmised toimingud:

1. Valige ER-vormingu versioon **1.1.2**.
2. Toimingupaanil valige **Impordi**.
3. Valige suvand **Jah** kinnitamaks, et soovite vormingu selle versiooni jaoks üle kirjutada olemasolevad rakendusekohased parameetrid.
4. Valige suvand **Sirvi**, et leida versiooni **1.1.1** jaoks eksporditud rakendusekohaseid parameetreid sisaldav fail.
5. Valige nupp **OK**.

    ER-vormingu versioonil **1.1.2** on nüüd samad rakendusekohased parameetrid kui algselt versiooni **1.1.1** jaoks konfigureeritud.

##### <a name="applicability-considerations"></a>Kohaldatavuse kaalumine

ER-vormingu rakendusekohased parameetrid sõltuvad juriidilisest isikust. Ühe juriidilise isiku jaoks teises juriidilises isikus konfigureeritud rakendusespetsiifiliste parameetrite taaskasutamiseks peate need eksportima, kui olete esimesse juriidilisse isikusse sisse logitud. Seejärel importige need pärast sisselogimist teisele juriidilisele isikule.

Seda ekspordi-impordi lähenemisviisi saate kasutada ka ER-vorminguga seotud rakendusespetsiifiliste parameetrite ülekandmiseks, mis olid algselt konfigureeritud ühes Finance'i eksemplaris, teise Finance'i eksemplari.

Kui konfigureerite rakendusepõhised parameetrid ER-vormingu ühe versiooni jaoks ja impordite seejärel sama vormingu uuema versiooni praegusesse Finance'i eksemplari, ei rakendata olemasolevaid rakendusepõhiseid parameetreid imporditud versioonile, välja arvatud juhul, kui kasutate **Kasutage ER-vormingute eelmiste versioonide rakendusespetsiifilisi parameetreid** funktsioone. Lisateabe saamiseks vaadake teemat [Olemasolevate taaskasutamine](#reuse-existing-parameters).

Pidage ka meeles, et kui valite importimiseks faili, võrreldakse selle faili rakendusekohaseid parameetreid importimiseks valitud ER-vormingu tüübi **Otsing** vastava andmeallika struktuuriga. Vaikimisi viiakse importimine lõpule ainult siis, kui iga rakendusepõhise parameetri struktuur ühtib impordiks valitud ER-vormingus vastava andmeallika struktuuriga. Kui struktuurid ei kattu, kuvatakse hoiatusteade, et importimist ei toimu. Kui sunnite importimise, tühistatakse valitud ER-vormingu olemasolevad rakendusekohased parameetrid ja peate need uuesti algusest peale seadistama.

Alustades Dynamics 365 Finance versioonis 10.0.23 saate muuta vaikekäitumist ja vältida hoiatusteate saamist, lubades  **joondamise ER-rakenduse funktsiooni importimise** parameetrid spetsiifilise **funktsioonihalduse** tööruumis. Kui see funktsioon on lubatud ja imporditavate rakendusepõhiste parameetrite struktuur erineb importimiseks valitud siht-ER-vormingus vastavate andmeallikate struktuurist, õnnestub importimine järgmistel juhtudel.

- Sihtkoha ER-vormingu struktuuri on muudetud, lisades uusi tingimuse veerge mis tahes olemasolevatele **otsingu** tüübi andmeallikatele. Kui import on lõpetatud, uuendatakse rakendusepõhised parameetrid. Kõikides rakendusspetsiifiliste parameetrite imporditud kirjetes lähtestatakse iga lisatud tingimuse veeru väärtused selle veeru vaikeväärtusega [andmetüübi jaoks](er-formula-supported-data-types-primitive.md).
- Sihtkoha ER-vormingu struktuuri on muudetud, eemaldades mõned veerud olemasolevatelt **otsingu** tüübi andmeallikatelt. Kui import on lõpetatud, uuendatakse rakendusepõhised parameetrid. Rakendusespetsiifiliste parameetrite imporditud kirjetes kustutatakse iga eemaldatud tingimuse veeru väärtused.
- Sihtkoha ER-vormingu struktuuri on muudetud, lisades uusi tingimuse veerge, mis tahes olemasolevatele **otsingu** tüübi andmeallikatele. Kui import on lõpetatud, lisatakse lisatud otsingud rakendusepõhistele parameetritele.
- Sihtkoha ER-vormingu struktuuri on muudetud, eemaldades mõned **otsingu** tüübi andmeallikatelt. Kui import on lõpetatud, kustutatakse imporditud rakendusspetsiifilistest parameetritest kõik **Otsingu** tüübiga andmeallikatega seotud artefaktid, mis eemaldatisiht-ER vormingust.

Kui import on lõpule viidud, muudetakse lisaks äsja kirjeldatud muudatustele imporditud rakendusspetsiifiliste parameetrite olekuks **Pooleli**. Hoiatusteade teavitab teid, et automaatselt korrigeeritud rakenduseomased parameetrid tuleb käsitsi redigeerida.

### <a name="reuse-existing-parameters"></a>Olemasolevate parameetrite taaskasutamine

Alates Dynamics 365 Finance versioonist 10.0.23 saate sama vorminguga kõrgema versiooni käivitamisel kasutada uuesti rakenduseomaseid parameetreid, mis on konfigureeritud ER-vormingu ühe versiooni jaoks. Selleks lubage **ER-vormingute eelmiste versioonide rakendusespetsiifiliste parameetrite** kasutamine **funktsioonihalduse** tööruumis. Kui see funktsioon on lubatud ja käivitate ühe versiooni ER-vormingust, mis proovib lugeda rakendusomaseid parameetreid, proovib ER leida rakendusespetsiifilisi parameetreid, mis on konfigureeritud selle vormingu jooksva versiooni jaoks. Või kui need pole saadaval, selle vormingu lähima madalama versiooni jaoks.

> [!NOTE]
> Rakendusepõhiseid parameetreid saate taaskasutada ainult praeguse juriidilise isiku ulatuse puhul.
>
> Käitusajal kuvatakse tõrge, kui käitate ER-vormingu kõrgemat versiooni, mis proovib taaskasutada sama vorminguga alamversiooni jaoks konfigureeritud rakenduseomasi parameetreid ja vähemalt ühe **otsingu** tüübi andmeallika struktuuri on muudetud.

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>Rakendusekohaste parameetrite ja ER-vormingu vaheline seos

ER-vormingu ja selle rakendusekohaste parameetrite seos saavutatakse ER-vormingu eksemplarist sõltuva kordumatu identimiskoodiga. Seega kui eemaldate ER-vormingu Finance’ist, säilitatakse ER-vormingu jaoks konfigureeritud rakendusekohaseid parameetreid praeguses Finance’i eksemplaris. Neile pääseb ligi alati, kui ER-vormingu alus sellesse Finance’i eksemplari uuesti imporditakse.

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>Ligipääs rakendusekohastele parameetritele ER-raamistikku kasutades

Eelnevas näites pääsesite ER-vormingu rakendusekohastele parameetritele ligi ER-raamistikku kasutades. See lähenemine ei lase teil piirata juurdepääsu konkreetse ER-vormingu rakendusekohastele parameetritele. Kui peate niisugused piirangut määrama, tehke järgmist. 

1. Kasutage uuesti olemasolevat menüü-üksust **ERSolutionAppSpecificParametersDesigner** või juurutage oma menüü-üksus **ERSolutionAppSpecificParametersDesigner**.

    ![Üksuse ERSolutionAppSpecificParametersDesigner menüükäsu kuvamine.](./media/GER-AppSpecParms-LookupForm-Access1.PNG)

2. Järgige üht neist sammudest.

    1. Looge uus menüü-üksus nupp ja linkige see vastava kirjega tabelist **ERSolutionTable**, seadistades selle atribuudi **Andmeallikas** väärtusele **ERSolutionTable**.

        ![Uue menüükäsu sätete kuvamine.](./media/GER-AppSpecParms-LookupForm-Access2.PNG)

    2. Looge lihtne nupp ja kirjutage üle meetod **Klõpsatud**, nagu on näidatud järgmises näites.

        Seda lähenemist kasutades saate määrata kordumatu lahenduse ID (määratakse väärtuse **GUID** kaudu), et anda ligipääs ainult konkreetse ER-vormingu rakendusekohastele parameetritele ja sellest tuletatud koopiatele.
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a>Lisaressursid

[Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)

[ER-vormingute konfigureerimine juriidilise isiku kohta määratud parameetrite kasutamiseks](er-app-specific-parameters-configure-format.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
