---
title: Elektroonilise aruandluse vormingute täitmise jälitamine jõudlusprobleemide tõrkeotsingu tegemiseks
description: See artikkel annab teavet selle kohta, kuidas kasutada jõudluse jälgimise funktsiooni elektroonilises aruandluses (ER) jõudlusprobleemide tõrkeotsinguks.
author: kfend
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 9f088228b140a42ee097c9e810166550ab0fae81
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289940"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a>ER-vormingute täitmise jälitus jõudluse probleemide tõrkeotsinguks

[!include[banner](../includes/banner.md)]

Üks osa elektroonilise aruandluse (ER) konfiguratsioonide kujundamisest elektrooniliste dokumentide loomise jaoks on määratleda meetod, mida kasutatakse andmete saamiseks rakendusest, ja sisestada see loodud väljundisse. ER-i jõudluse jälituse funktsioon aitab märkimisväärselt vähendada aja- ja rahakulu, mis tekib ER-vormingu täitmise üksikasjade kogumisel ja nende kasutamisel jõudluse probleemide tõrkeotsinguks. Selles õppetükis esitatakse juhised, kuidas jälitada täidetud ER-vormingute jõudlust ja kuidas kasutada jälitusest saadud teavet jõudluse täiustamiseks.

## <a name="prerequisites"></a>Eeltingimused

Selle õppetüki näidete läbimiseks peavad teil olema järgmised juurdepääsuõigused.

- Juurdepääs ühele järgmistest rollidest.

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

- Juurdepääs teenuse Regulatory Configuration Services (RCS) eksemplarile, mis on ette valmistatud sama rentniku jaoks, nagu rakendus, ühe järgmise rolli jaoks:

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

Samuti peate alla laadima ja kohalikult talletama järgmised failid.

| Fail                                  | Sisu                               |
|---------------------------------------|---------------------------------------|
| Performance trace model.version.1 (Jõudluse jälituse mudel, versioon 1)     | [ER-i andmemudeli konfiguratsiooni näide](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| Performance trace metadata.version.1 (Jõudluse jälituse metaandmed, versioon 1)  | [ER-i metaandmete konfiguratsiooni näide](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| Performance trace mapping.version.1.1 (Jõudluse jälituse vastendus, versioon 1.1) | [ER-i mudelivastenduse konfiguratsiooni näide](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| Performance trace format.version.1.1 (Jõudluse jälituse vorming, versioon 1.1)  | [ER-vormingu konfiguratsiooni näide](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a>Elektroonilise aruandluse parameetrite konfigureerimine

Iga ER-i jõudluse jälg, mis luuakse rakenduses, salvestatakse käivituslogi kirje manusena. Nende manuste haldamiseks kasutatakse dokumendihalduse raamistikku. Peate konfigureerima ER-i parameetreid varem, et määrata dokumendihalduse dokumendi tüüp, mida tuleks kasutada jõudluse jälgede manustamiseks. Tööruumis **Elektrooniline aruandlus** valige **Elektroonilise aruandluse parameetrid**. Seejärel valige lehe **Elektroonilise aruandluse parameetrid** vahekaardi **Manused** väljal **Muud** dokumendihalduse dokumendi tüüp, mida tuleks kasutada jõudluse jälitusteks.

![Elektroonilise aruandluse parameetrite leht.](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

Selleks, et dokumendihalduse dokumenditüüp oleks otsinguväljal **Muud** saadaval, peab dokumendihalduse dokumenditüüp olema lehel **Dokumenditüübid** konfigureeritud järgmisel viisil (**Organisatsiooni haldus \> Dokumendihaldus \> Dokumenditüübid**).

- **Klass:** manusfail
- **Grupp:** fail

![Dokumenditüüpide leht.](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> Valitud dokumenditüüp peab olema eksemplari igas ettevõttes saadaval, kuna dokumendihalduse manused on ettevõttekohased.

### <a name="configure-rcs-parameters"></a>RCS-i parameetrite konfigureerimine

Loodud ER-i jõudluse jäled imporditakse analüüsimiseks RCS-i, kasutades ER-vormingu kujundajat ja ER-i mudelivastenduse kujundajat. Kuna ER-i jõudluse jäljed salvestatakse ER-vorminguga seotud käivituslogi kirje manustena, peate konfigureerima RCS-i parameetreid ette, et määrata dokumendihalduse dokumenditüüp, mida tuleks kasutada jõudluse jälje manustamiseks. Valige RCS-i eksemplari, mis on teie ettevõtte jaoks ette valmistatud, tööruumis **Elektrooniline aruandlus** suvand **Elektroonilise aruandluse parameetrid**. Seejärel valige lehe **Elektroonilise aruandluse parameetrid** vahekaardi **Manused** väljal **Muud** dokumendihalduse dokumendi tüüp, mida tuleks kasutada jõudluse jälitusteks.

![Elektroonilise aruandluse parameetrite leht RCS-is.](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

Selleks, et dokumendihalduse dokumenditüüp oleks otsinguväljal **Muud** saadaval, peab dokumendihalduse dokumenditüüp olema lehel **Dokumenditüübid** konfigureeritud järgmisel viisil (**Organisatsiooni haldus \> Dokumendihaldus \> Dokumenditüübid**).

- **Klass:** manusfail
- **Grupp:** fail

## <a name="design-an-er-solution"></a>ER-i lahenduse kujundamine

Oletame, et olete alustanud uue ER-i lahenduse kujundamist, et luua uus hankija kandeid esitav aruanne. Praegu leiate valitud hankija kanded lehel **Hankija kanded** (avage **Ostureskontro \> Hankijad \> Kõik hankijad**, valige hankija ja seejärel valige toimingupaanil vahekaardi **Hankija** grupis **Kanded** suvand **Kanded**). Kuid teil on vaja, et kõik hankija kanded oleksid samal ajal ühes elektroonilises dokumendis XML-vormingus. See lahendus koosneb mitmest ER-i konfiguratsioonist, mis sisaldavad nõutud andmemudelit, metaandmeid, mudelivastendust ja vormingu komponente.

1. Logige sisse RCS-i eksemplari, mis on teie ettevõtte jaoks ette valmistatud.
2. Selles õppetükis loote näidisettevõtte **Litware, Inc** jaoks konfiguratsioonid ja muudate neid. Seetõttu veenduge, et see konfiguratsiooni pakkuja oleks RCS-i lisatud ja aktiivsena valitud. Juhiste saamiseks vaadake teemat [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Tööruumis **Elektrooniline aruandlus** valige paan **Aruandluse konfiguratsioonid**.
4. Importige lehel **Konfiguratsioonid** ER-i konfiguratsioonid, mille eeltingimusena RCS-i alla laadisite, järgmises järjestuses: andmemudel, metaandmed, mudelivastendus, vorming. Toimige iga konfiguratsiooni puhul järgmiselt.

    1. Valige toimingupaanil suvand **Rahavahetus \> Laadi XML-failist**.
    2. Valige käsk **Sirvi**, et valida nõutava ER-i konfiguratsiooni jaoks sobiv fail XML-vormingus.
    3. Valige nupp **OK**.

    ![Konfiguratsioonide leht RCS-s.](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a>ER-i lahenduse kasutamine täitmise jälituseks

Oletame, et olete lõpetanud ER-i lahenduse esimese versiooni kujundamise. Nüüd soovite seda testida oma eksemplaris ja analüüsida täitmise jõudlust.

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a> ER-konfiguratsiooni importimine RCS-st finantsidesse ja toimingutesse

1. Logige sisse oma rakenduse eksemplari.
2. Selles õppetükis impordite konfiguratsioonid RCS-i eksemplarist (kus kujundate ER-i komponente) oma eksemplari (kus testite ja lõpuks neid kasutate). Seega peate veenduma, et kõik nõutud artefaktid oleksid ette valmistatud. Juhised leiate teemast [Elektroonilise aruandluse (ER) konfiguratsioonide importimine teenusest Regulatory Configuration Services (RCS)](rcs-download-configurations.md).
3. Järgige neid samme, et importida konfiguratsioonid RCS-ist rakendusse.

    1. Valige tööruumi **Elektrooniline aruandlus** konfiguratsiooni pakkuja **Litware, Inc.** paanilt valik **Hoidlad**.
    2. Valige lehel **Konfiguratsioonihoidla** hoidla tüübiga **RCS** ja seejärel valige käsk **Ava**.
    3. Valige kiirkaardil **Konfiguratsioonid** konfiguratsioon **Jõudluse jälituse vorming**.
    4. Valige kiirkaardil **Versioonid** valitud konfiguratsiooni versioon **1.1** ja seejärel käsk **Impordi**.

    ![Konfiguratsioonihoidla leht.](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

Andmemudeli ja mudelivastenduse vastavate versioonide konfiguratsioonid imporditakse eeltingimustena automaatselt imporditud ER-vormingu konfiguratsioonile.

### <a name="turn-on-the-er-performance-trace"></a>ER-i jõudluse jälituse sisselülitamine

1. Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Toimige dialoogiboksi **Kasutaja parameetrid** jaotises **Täitmise jälitus** järgmiselt.

    1. Määrake väljal **Täitmise jälituse vorming** loodud jõudluse jäljele vorming, milles talletatakse täitmise üksikasjad ER-vormingu ja vastendamise elementide jaoks.

        - **Silumise jälgimisvorming** – valige see väärtus, kui plaanite interaktiivselt käitada lühikese täitmisajaga ER-vormingu. Siis käivitatakse ER-vormingu käivitamise üksikasjade kogum. Kui see väärtus on valitud, kogub jõudluse jälitus teavet järgmistele toimingutele kulutatud aja kohta.

            - Iga andmeallika käitamine mudelivastendusel, mida kutsutakse andmeid tooma
            - Iga vormingu üksuse töötlemine andmete sisestamiseks loodavasse väljundisse

            Kui valite **silumisjälje vormingu** väärtuse, saate analüüsida jälje sisu ER-toimingu kujundajas. Seal saate vaadata jäljes mainitud ER-vormingut või vastendamise elemente.

        - **Kokkuvõtlik jälgimisvorming** – valige see väärtus, kui plaanite käitada pika täitmisajaga ER-vormingu partiirežiimis. Siis käivitatakse ER-vormingu käivitamise kokkuvõtlik üksikasjade kogum. Kui see väärtus on valitud, kogub jõudluse jälitus teavet järgmistele toimingutele kulutatud aja kohta.

            - Iga andmeallika käitamine mudelivastendusel, mida kutsutakse andmeid tooma
            - Iga andmeallika käitamine vormingu vastendusel, mida kutsutakse andmeid tooma
            - Iga vormingu üksuse töötlemine andmete sisestamiseks loodavasse väljundisse

            Agregad **jälgimise vormingu** väärtus on saadaval Microsoft Dynamics versioonis 365 Finance versioonis 10.0.20 ja uuemas versioonis.

            ER-vormingu kujundajas ja ER-mudeli vastendamise kujundajas saate vaadata üksiku komponendi kogu täitmisaega. Lisaks sisaldab jälg käivitamise üksikasju, nt teostamiste arvu ning üksiku käivitamise minimaalset ja maksimaalset aega.

            > [!NOTE]
            > See jälg kogutakse jälgitud komponentide tee põhjal. Seetõttu võib statistika olla vale, kui üksik vanemkomponent sisaldab mitut nimetamata alamkomponenti või kui mitme alamkomponendi nimi on sama.

    2. Määrake järgmiste suvandite olekuks **Jah**, et koguda kindlaid üksikasju ER-i mudelivastenduse ja ER-vormingu komponentide täitmise kohta.

        - **Päringustatistika sissenõudmine** – kui see valik on sisse lülitatud, kogub jõudluse jälitus järgmist teavet.

            - Andmeallikate tehtud andmebaasi kutsete arv
            - Korduvate kutsete arv andmebaasi
            - Andmebaasi kutsete tegemiseks kasutatud SQL-i lausete üksikasjad

        - **Jälita vahemälule juurdepääsu** – kui see valik on sisse lülitatud, kogub jõudluse jälitus teavet ER-i mudelivastenduse vahemälu kasutuse kohta.
        - **Jälita andmete juurdepääsu** – kui see valik on sisse lülitatud, kogub jõudluse jälitus teavet andmebaasi kutsete arvu kohta, mis on tehtud kirjeloendi tüüpi täidetud andmeallikate jaoks.
        - **Jälita loendi loetelu** – kui see valik on sisse lülitatud, kogub jõudluse jälitus teavet kirjete arvu kohta, mis on taotletud kirjeloendi tüüpi andmeallikatest.

    > [!NOTE]
    > Dialoogiboksi **Kasutaja parameetrid** parameetrid kehtivad konkreetsele kasutajale ja praegusele ettevõttele.

    ![Kasutaja parameetrite dialoogiaken.](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a>ER-vormingu käivitamine

1. Valige ettevõte **DEMF**.
2. Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.
3. Valige lehe **Konfiguratsioonid** konfiguratsioonipuult üksus **Jõudluse jälituse vorming**.
4. Valige toimingupaanil käsk **Käivita**.

Pange tähele, et loodud fail esitab teavet kuue hankija 265 kande kohta.

## <a name="review-the-execution-trace"></a>Täitmise jälje läbivaatus

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a>Eksportige loodud jälg rakendusest

Jõudluse jäljed lahutatakse ER-vormingu allikast ja neid saab järjestada välisele ZIP-failile.

1. Minge jaotisse **Organisatsiooni haldamine\> Elektrooniline aruandlus \>Konfiguratsiooni silumislogid**.
2. Valige lehe **Elektroonilise aruandluse käivituslogid** vasakpoolsel paanil **Konfiguratsiooni nimi** valik **Jõudluse jälituse vorming**, et leida logi kirjed, mis on loodud konfiguratsiooni **Jõudluse jälituse vorming** täitmisega.
3. Valige lehe paremas ülanurgas nupp **Manused** (kirjaklambrisümbol) või vajutage klahve **Ctrl + Shift + A**.

    ![Lehe Elektroonilise aruandluse käitamise logid nupp Manused.](./media/GER-PerfTrace-GER-DebugLog.png)

4. Valige lehe **Elektroonilise aruandluse käitamise logide manused** toimingupaanil käsk **Ava**, et saada jõudluse jälg ZIP-failina ja seda kohalikult talletada.

    ![Elektroonilise aruandluse logide manused.](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> Loodud jäljel on viide allika ER-i aruandele kordumatu aruande identifikaatori kaudu ainult **GUID**-vormingus. Vormingu versiooni nummerdamist ei arvestata.

Pange tähele, et täidetud ER-vormingu jaoks loodud jõudluse jälje ja ER-i mudelivastenduse vaheline seos põhineb kasutatud juurdeskriptoril ning üldisel andmemudelil. Vormingu ja mudelivastenduse versiooni nummerdamist ei arvestata. Samuti ei arvestata mudelivastenduse lipu **Mudelivastenduse vaikeväärtus** sätet.

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a>Loodud jälje importimine RCS-i

1. Valige RCS-i tööruumis **Elektrooniline aruandlus** paan **Aruandluse konfiguratsioonid**.
2. Laiendage lehe **Konfiguratsioonid** konfiguratsioonipuul üksust **Jõudluse jälituse mudel** ja valige üksus **Jõudluse jälituse vorming**.
3. Valige toimingupaanil valik **Koostaja**.
4. Valige lehe **Vormingu koostaja** toimingupaanil **Jõudluse jälitus**.
5. Valige dialoogiaknas **Jõudluse jälituse tulemuste sätted** valik **Impordi jõudluse jälg**.
6. Valige nupp **Sirvi**, et valida varem eksporditud zip fail.
7. Valige nupp **OK**.

    ![Jõudluse jälituse tulemuse sätete dialoogiboks RCS-s.](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a>Jõudluse jälituse kasutamine analüüsiks RCS-is – vormingu täitmine

1. Valige RCS-is lehel **Vormingu koostaja** käsk **Laienda/ahenda**, et laiendada kõigi vormingu üksuste sisu.

    Pange tähele, et praeguse vormingu mõne üksuse kohta kuvatakse lisateavet.

    - Tegelik aeg, mis kulus andmete sisestamiseks loodud väljundisse kasutades vormingu üksust
    - Sama aeg väljendatuna protsendina koguajast, mis kulutati kogu väljundi loomiseks

    ![Vormingu koostaja leht RCS-s.](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. Sulgege **Vormingu koostaja** leht.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a>Jõudluse jälituse kasutamine analüüsiks RCS-is – mudelivastendus

1. Valige RCS-is lehe **Konfiguratsioonid** konfiguratsioonipuult üksus **Jõudluse jälituse vastendus**.
2. Valige toimingupaanil valik **Koostaja**.
3. Valige **Kujundaja**.
4. Valige lehe **Mudelivastenduse koostaja** toimingupaanil **Jõudluse jälitus**.
5. Valige jälg, mille varem importisite.
6. Valige nupp **OK**.

Pange tähele, et praeguse mudelivastenduse mõne andmeallika üksuse kohta muutub kättesaadavaks uus teave.

- Tegelik aeg, mis kulus andmeallika abil andmete toomisele
- Sama aeg väljendatuna protsendina koguajast, mis kulutati kogu mudelivastenduse käitamise peale

Pange tähele, et ER annab teile teate, et praegune mudelivastendus dubleerib andmebaasi taotlusi ajal, mil andmeallikat VendTable/\<Relations/VendTrans.VendTable\_AccountNum käitatakse. Dubleerimine toimub seetõttu, et hankija kannete loendit kutsutakse iga itereeritud hankija kirje puhul kaks korda.

- Üks kutse tehakse, et sisestada andmemudelis iga kande üksikasjad konfigureeritud sidumiste alusel.
- Teine kutse tehakse, et sisestada andmemudelis iga hankija kohta arvutatud kannete arv.

![Teade dubleeritud andmebaasi taotluste kohta mudelivastenduse koostaja lehel RCS-s.](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

Väärtus **\[Q:530\]** näitab, et tabelit VendTrans kutsuti 530 korda, et tagastada sellest tabelist kirje andmeallikasse VendTable/\<Relations/VendTrans.VendTable\_AccountNum. Väärtus **\[530\]** näitab, et andmeallikat VendTable/\<Relations/VendTrans.VendTable\_AccountNum kutsuti 530 korda, et tagastada kirje sellest andmeallikast ja sisestada selle üksikasjad andmemudelisse.

Soovitame kasutada andmeallika VendTable/\<Relations/VendTrans.VendTable\_AccountNum jaoks vahemällusalvestust, et vähendada kutsete arvu, mida tehakse 265 kande üksikasjade saamiseks, ja aidata parandada mudelivastenduse jõudlust.

Samuti võib see olla kasulik. et vähendada andmeallikale LedgerTransTypeList tehtud kutsumiste arvu. Seda andmeallikat kasutatakse **LedgerTransType**-i nummerdamise iga väärtuse seostamiseks oma sildiga. Seda andmeallikat kasutades saate leida sobiva sildi ja seda andmeallikasse iga hankija kande jaoks sisestada. Praegune kutsete arv sellele andmeallikale (9027) on 265 kande kohta üsna kõrge.

![Mudelivastenduse koostaja leht RCS-s, mis näitab 9027 kutset andmeallikale.](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Mudelivastenduse parandamine täitmise jälitusest saadud teabe põhjal

### <a name="modify-the-logic-of-the-model-mapping"></a>Mudelivastenduse loogika muutmine

1. Järgige vahemälu kasutamiseks järgmisi samme, et vältida andmebaasi dubleeritud kutseid.

    1. Valige RCS-is lehe **Mudelivastenduse koostaja** paanil **Andmeallikad** üksus **VendTable**.
    2. Valige suvand **Vahemälu**.
    3. Laiendage üksust **VendTable**, laiendage andmeallika VendTable üks-mitmele seoste loendit (üksus **\<Seosed**) ja valige üksus **VendTrans.VendTable\_AccountNum**.
    4. Valige suvand **Vahemälu**.

    ![Vahemälu häälestus, mis aitab vältida dubleeritud kutseid.](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. Järgige neid samme, et tuua andmeallikas LedgerTransTypeList andmeallika VendTable ulatusse.

    1. Laiendage paanil **Andmeallika tüübid** üksust **Funktsioonid** ja valige üksus **Arvutatud väli**.
    2. Valige paanil **Andmeallikad** üksus **VendTable**.
    3. Valige **Lisa**.
    4. Sisestage väljale **Nimi** tekst **\$TransType**.
    5. Valige **Valemi redigeerimine**.
    6. Sisestage väljale **Valem** tekst **LedgerTransTypeList**.
    7. Valige käsk **Salvesta**.
    8. Sulgege leht **Valemiredaktor**.
    9. Klõpsake valikut **OK**.

3. Järgige neid samme, et kasutada vahemällusalvestust välja **\$TransType** jaoks.

    1. Valige üksus **LedgerTransTypeList**.
    2. Valige suvand **Vahemälu**.
    3. Valige üksus **VendTable.\$TransType**.
    4. Valige suvand **Vahemälu**.

    ![Vahemällusalvestuse seadistamine välja $TransType jaoks.](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. Järgige neid samme, et muuta välja **\$TransTypeRecord** nii, et see hakkaks kasutama vahemällu salvestatud välja **\$TransType.**

    1. Laiendage paanil **Andmeallikad** üksust **VendTable**, üksust **\<Seosed**, üksust **VendTrans.VendTable\_AccountNum** ja valige üksus **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.
    2. Valige suvand **Redigeeri**.
    3. Valige **Valemi redigeerimine**.
    4. Leidke väljal **Valem** järgmine avaldis.

        FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))

    5. Sisestage väljale **Valem** järgmine avaldis.

        FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).

    6. Valige käsk **Salvesta**.
    7. Sulgege leht **Valemiredaktor**.
    8. Valige nupp **OK**.

5. Valige käsk **Salvesta**.
6. Sulgege leht **Mudelivastenduse koostaja**.
7. Sulgege leht **Mudelivastendused**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>ER-i mudelivastenduse muudetud versiooni lõpetamine

1. Valige RCS-is lehe **Konfiguratsioonid** kiirkaardil **Versioonid** konfiguratsiooni **Jõudluse jälituse vastendus** versioon **1.2**.
2. Valige käsk **Muuda olekut**.
3. Valige **Lõpeta**.

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a>Muudetud ER-i mudelivastenduse konfiguratsiooni importimine RCS-ist rakendusse

Korrake [selles artiklis varasemas jaotises RCS-ilt](#import-configuration) ER-i konfiguratsiooni importimiseks selles artiklis toodud etappe, et importida jõudlusjälje vastenduse konfiguratsiooni versioon 1.2 **·**.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Muudetud ER-i lahenduse kasutamine täitmise jälituseks

### <a name="run-the-er-format"></a>ER-vormingu käivitamine

Korrake selle artikli varasema [ER-vormingu](#run-format) sektsiooni samme uue jõudluse jälituse loomiseks.

## <a name="work-with-the-execution-trace"></a>Töö käivitamise jäljega

### <a name="export-the-generated-trace-from-the-application"></a>Eksportige loodud jälg rakendusest

Korrake selle artikli varasemas [jaotises Loodud jälituse](#export-trace) eksportimine, et salvestada uus jõudluse jälitus kohalikult.

### <a name="import-the-generated-trace-into-rcs"></a>Loodud jälje importimine RCS-i

Korrake selle artikli varasemas [jaotises "Impordi loodud jälitus" toodud RCS-i](#import-trace), et importida uus jõudluse jälitus RCS-i.

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a>Jõudluse jälituse kasutamine analüüsiks RCS-is – mudelivastendus

Korrake viimase jõudluse [jälituse analüüsimiseks RCS-i –](#use-trace) mudeli vastendamise jaotises toodud etappe selles artiklis.

Pange tähele, et kohandused, mida tegite mudelivastendusele, on eemaldanud dubleeritud päringud andmebaasile. Vähendatud on ka selle mudelivastenduse kutsete arvu andmebaasi tabelitele ja andmeallikatele. See on paranenud kogu ER-i lahenduse jõudlus.

![Jälje teave andmeallika VendTable kohta RCS-i mudelivastenduse koostaja lehel.](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

Jälje teabes näitab andmeallika VendTable väärtus **\[12\]**, et seda andmeallikat kutsuti 12 korda. Väärtus **\[Q:6\]** näitab, et kuus kutset teisendati andmebaasi kutseteks andmeallika VendTable tabelile. Väärtus **\[C:6\]** näitab, et andmebaasist toodud kirjed salvestati vahemällu ja kuus muud kõnet töödeldi vahemälu abil.

Pange tähele, et kutsete arv andmeallikale LedgerTransTypeList on vähendatud 9027-lt 240-le.

![Jälje teave andmeallika LedgerTransTypeList kohta RCS-i mudelivastenduse koostaja lehel.](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a>Kontrollige käivitamise jälge rakenduses

Peale RCS-i võivad mõned versioonid pakkuda võimalusi ER-i raamistiku koostaja kogemuse jaoks. Nendel versioonidel on olemas suvand **Luba kujundusrežiim**, mida saab sisse lülitada. Selle suvandi leiate lehe **Elektroonilise aruandluse parameetrid** vahekaardilt **Üldine**, mille saate avada tööruumist **Elektrooniline aruandlus**.

![Disainimise režiimi suvandi lubamine elektroonilise aruandluse parameetrite lehel.](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

Kui kasutate ühte neist versioonidest, saate analüüsida loodud jõudluse jälje üksikasju otse rakenduses Finance and Operations. Te ei pea neid eksportima rakendusest ning importima RCS-i.

## <a name="review-the-execution-trace-by-using-external-tools"></a>Täitmise jälje läbivaatus väliste tööriistade abil

### <a name="configure-user-parameters"></a>Kasutaja parameetrite konfigureerimine

1. Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Valige dialoogiboksi **Kasutaja parameetrid** jaotises **Täitmise jälitus** väljal **Täitmise jälje vorming** valik **PerfView XML.**

### <a name="run-the-er-format"></a>ER-vormingu käivitamine

Korrake selle artikli varasema [ER-vormingu](#run-format) sektsiooni samme uue jõudluse jälituse loomiseks.

Pange tähele, et veebibrauser pakub allalaadimiseks ZIP-faili. See fail sisaldab jõudluse jälge PerfView-vormingus. Seejärel saate kasutada PerfView jõudluse analüüsi tööriista, et analüüsida ER-vormingu täitmise üksikasju.

![Jõudluse jälje teave PerfView-vormingus.](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a>Väliste tööriistade kasutamine täitmise jälje läbivaatamiseks, mis hõlmab andmebaasi päringuid

Tänu ER-raamistiku täiustustele pakub PerfView'is loodud jõudluse jälitus nüüd üksikasjalikumat teavet ER-i vormingu käivitamise kohta. Finantside Microsoft Dynamics versioonis 365 10.0.4 (juuli 2019) võib see jälitada ka rakenduse andmebaasi tehtud SQL-päringute üksikasju.

### <a name="configure-user-parameters"></a>Kasutaja parameetrite konfigureerimine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Seadke dialoogiboksi **Kasutaja parameetrid** jaotises **Täitmise jälitus** järgmised parameetrid.

    - Valige väljal **Täitmise jälituse vorming** suvand **PerfView XML**.
    - Seadistage **Päringustatistika sissenõudmise** väärtuseks **Jah**.
    - Määrake suvand **Jälituse päring** olekule **Jah**.

    ![Täitmise jälituse jaotis, kasutaja parameetri dialoogiboks.](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a>ER-vormingu käivitamine

Korrake selle artikli varasema [ER-vormingu](#run-format) sektsiooni samme uue jõudluse jälituse loomiseks.

Pange tähele, et veebibrauser pakub allalaadimiseks ZIP-faili. See fail sisaldab jõudluse jälge PerfView-vormingus. Seejärel saate kasutada PerfView jõudluse analüüsi tööriista, et analüüsida ER-vormingu täitmise üksikasju. See jälg sisaldab nüüd SQL-i andmebaasi juurdepääsu üksikasju ER-vormingu käivitamise ajal.

![Käivitatud ER-vormingu jälitusteave PerfView'is.](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)
- [Saate parandada ER-lahenduste jõudlust, lisades parameeteriseeritud ARVUTATUD VÄLJA andmeallikad](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

