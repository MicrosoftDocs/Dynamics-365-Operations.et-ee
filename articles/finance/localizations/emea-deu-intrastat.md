---
title: Saksa Intrastat
description: See teema sisaldab teavet Saksamaa Intrastat deklareerimise kohta.
author: anasyash
ms.date: 09/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 50c412fdfd7118843d285cbb70e8e44847c9d4a5
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/15/2021
ms.locfileid: "7487921"
---
# <a name="german-intrastat"></a>Saksa Intrastat

[!include [banner](../includes/banner.md)]

**Intrastat** lehte kasutatakse Euroopa Liidu (EL) riikide vahelise kaubavahetuse aruannete loomiseks ja esitamiseks. Saksa Intrastati deklaratsioon sisaldab aruandluseks teavet kauplemise kohta. Aruanne on vormindatud vastavalt Saksa ametivõimude juhistele, mis on esitatud [6.2 failideklaratsioonidel INSTAT/XML-vormingus](https://www-idev.destatis.de/idev/doc/intra_en/hilfe6_2.html) lehel.

Järgmine tabel näitab väljasid, mis kuvatakse Saksa Intrastati deklaratsioonil.

| Väljad | Kauba lähetamine | Saabumised |
|-------------------------|-------------------------|-------------------------|
| Viiteperiood | X | X |
| Suunakood | X | X |
| Intrastati deklaratsiooni valuuta</br>**Märkus:** Kumbki valuuta pole <em>arvestusvaluuta</em>. | X | X |
| Kaubaartikkel | X | X |
| Kauba nimi | X | X |
| Lisaühiku kood | X | X |
| Saadetise/sihtkoha riik | X | X |
| Netomass | X | X |
| Kogus valemiühikutes | X | X |
| Päritoluriik |  | X |
| Arve summa | X |  |
| Statistiline väärtus | X | X |
| Kande iseloom | X | X |
| Transpordiliik | X | X |
| Regiooni kood</br>**Märkus.**</br><ul></br><li>Kui päritoluriik või -regioon on Saksamaa ja arve on lähetuste jaoks, kuvatakse päritolumaa Intrastati kood.</li></br><li>Kui päritoluriik või -regioon ei ole Saksamaa ja arve on lähetuste jaoks, kuvatakse kood **99**.</li></br><li>Kui arve on saabumiste jaoks, kuvatakse osariigi Intrastati kood.</li></br></ul> | X | X |
| Sadam/Lennujaam/sisemise sadami kood | X | X |
| Tarnetingimused | X | X |


## <a name="set-up-intrastat"></a>Intrastati seadistamine

1. Ettevõtete koodi seadistus.

    1. Avage **Organisatsiooni haldus** > **Organisatsioonid** > **Juriidilised isikud**.
    2. **Väliskaubanduse ja logistika** kiirkaardil jaotises **Tuvastus** jaotises **DVR** väljale sisestage vahetuselepingu ID. See ID kaasatakse aruandesse.
    3. Sisestage **käibemaksukohuslase koodi ekspordi** väljale oma ettevõtte käibemaksukood (VAT) number ekspordiks.
    4. Sisestage **käibemaksukohuslase koodi impordi** väljale oma ettevõtte käibemaksukoodi (VAT) number impordiks.
    5. Sisestage **intrastati** koodi väljale juriidilisele isikule määratud Intrastati kood.
    6. Kiirkaardi **Maksu registreerimine** väljal **Maksu registreerimisnumber** sisestage oma ettevõtte maksu registreerimisnumber.

    > [!NOTE]
    > Kui te saate luua tütarettevõtete Intrastat-aruande, sisestage väljale **Maksu registreerimisnumber** oma emaettevõtte maksu registreerimisnumber.

2. [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index), ühiskasutusega varateegis laadige Intrastati deklaratsiooni jaoks alla järgmiste elektrooniliste aruannete (ER) konfiguratsioonide viimased deklaratsioonid.

    - Intrastati mudel
    - Intrastat-aruanne
    - INSTAT XML
    - INSTAT XML (DE)

3. Väliskaubanduse parameetrite häälestamine:

    1. Rakenduses Dynamics 365 Finance avage **Maks** > **Seadistus** > **Väliskaubanduse parameetrid**.
    2. Vahekaardil **Intrastat** kiirkaardi **Elektrooniline aruandlus** väljal **Failivormingu vastendamine**, valige **Intrastat XML (DE)**.
    3. Sisestage või valige väärtus **Intrastati aruanne** väljal **Aruandevormingu vastendamine**.
    4. Valige kiirkaardi **Kaubaartikli hierarhia** väljal **Kategooriahierarhia** väärtus **Intrastat**.
    5. Väljal **Kande kood** valige varaülekannete kandekood. Seda koodi kasutatakse tehingute jaoks, mis põhjustavad vara tegeliku või kavandatud üleandmise hüvitise eest (finantsiline ja muu). Seda kasutatakse ka paranduste puhul.
    6. Väljal **Kreeditmärge** valige kandekood kaupade tagastamiseks.
    7. Väljal **Töötaja** valige Intrastat-aruande kontaktisik. Teise võimalusena sisestage või valige väärtused vahekaardil **Kontakt** väljadel **Nimi**, **Telefon**, **Faks**, **Meiliaadress** ja **Interneti-aadress**. Need väljad on aruandesse kaasatud.
    8. Valige väljal **Asutus** Intrastati asutus.
    9. Minge **maksu** > **kaudsete maksude** > **käibemaksu** > **käibemaksuhaldurid** ja sisestage Intrastati maksuametile järgmine teave:

       - Maksuameti ID
       - Aadress
       - Kontaktandmed

    10. Vahekaardil **Riigi/regiooni atribuudid** väljal **Riik/regioon**, loetlege kõik riigid või regioonid, millega teie organisatsioonil on ärisuhted. Valige iga riigi või regiooni jaoks väljal **Riigi/regiooni tüüp** **EU**, et teie riik või regioon ilmuks teie Intrastat-aruandes.

4. Regioonikoodide häälestamine.

    1. Avage **Organisatsioonihaldus** > **Globaalne aadressiraamat** > **Aadress** > **Aadressi seadistus**.
    2. Valige **Osariik/provints** vahekaardi **Riik/regioon** väljal **DEU** ja seejärel valige **Rakenda filter**.
    3. Valige ruudustikus olek. Sisestage väljale **Intrastati kood** väli, sisestage unikaalne Intrastati kood.

5. Saate seadistada toote päritolu aadressi.

    1. Avage **Tooteteabe haldus** > **Tooted** > **Väljastatud tooted**.
    2. Valige ruudustikus toode.
    3. Valige kiirkaardi **Väliskaubandus** jaotise **Intrastat** väljal **Päritoluriik** väljal, valige **DEU**.

6. Minge **Maks** > **Seadistamine** > **Väliskaubandus** > **Intrastati kompressioon** ja valige väljad, mida tuleb Intrastati teabe summeerimisel võrrelda. Saksa Intrastati jaoks valige järgmised väljad:

    - Artikkel
    - Riik/regioon
    - Parandus
    - Direction
    - Tarnetingimused
    - Arve
    - Päritoluriik/-regioon
    - Sadam
    - Saatja riik/regioon
    - Saatja osariik
    - Statistiline protseduur
    - Kandekood
    - Transport
    - Maksuvabastuse number

### <a name="intrastat-transfer"></a>Intrastati ülekanne

**Intrastati** lehel saate valida tegevuspaanil valiku **Ülekanne**, et edastada automaatselt oma müügitellimuste, vabas vormis arvete, ostutellimuste, hankija arvete, hankija toote sissetulekute, projektiarvete **,** ja üleviimistellimuste teabe automaatne ülekandmine. Edastatakse ainult dokumendid, mille sihtriigiks või -piirkonnaks (lähetamiseks) või saadetiseks (saabumiseks) on ELi riik.

Teise võimalusena saate kandeid käsitsi sisestada, valides tegevuspaanil valiku **Uus**.

### <a name="generate-an-intrastat-report"></a>Looge Intrastati aruanne

1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
2. Toimingupaanil valige suvandid **Väljund** > **Aruanne**.
3. Määrake dialoogiboksis **Intrastati aruanne** järgmised väljad.

    | Field | Kirjeldus |
    |-------------------------|-------------------------|
    | Alates kuupäevast | Valige aruande alguskuupäev. |
    | Lõppkuupäev | Valige aruande lõppkuupäev. |
    | Loo fail | XML-faili genereerimiseks määrake suvandi väärtuseks **Jah**. |
    | Faili nimi | Jätke see väli tühjaks. Faili nimi luuakse automaatselt ja see koosneb väärtusest **&lt;ümbrikus&gt;** XML sildist pluss failinime laiendist **.xml**.</br>**&lt;ümbriku&gt;** väärtus on ühendatud järgmiste elementidega, selles järjekorras:</br><ol type="1"></br><li>**&lt;InterchangeAgreementId&gt;** sildi väärtus</li></br><li>Sidekriips (-)</li></br><li>Üksuse **&lt;viiteperiood AAAAKK&gt;** sildil</li></br><li>Sidekriips (-)</li></br><li>**&lt;Ümbriku/kellaaja/kuupäeva väärtus AAAAKKPP&gt;** sildil</li></br><li>Sidekriips (-)</li></br><li>**&lt;Ümbriku/kellaaja/kuupäeva väärtus AAAAKKPP&gt;** sildil</li></br></ol> |
    | Direction | <ul></br><li>Valige ühendusesiseste saabumiste aruande jaoks **Saabumised**.</li></br><li>Valige ühendusesiseste lähetuste aruande jaoks **Lähetused**.</li></br><li>Valige **Mõlemad**, kui soovite aruandesse nii saabumisi kui lähetusi .</li></br></ul> |
    | Maksu registreerimisnumber | Sisestage registreerimisnumber, mida kasutada saatja ID-koodi loomiseks, kui see number erineb juriidilise isiku maksu registreerimisnumbrist. |


## <a name="example"></a>Näide

See näide näitab, kuidas sisestada Intrastati saabumised ja lähetamised. See kasutab **DEMF** juriidilist isikut.

1. [LCS](https://lcs.dynamics.com/Logon/Index), ühiskasutusega varateegis laadige Intrastati deklaratsiooni vormingu jaoks alla järgmiste ER-konfiguratsioonide viimased versioonid:

    - Intrastati mudel
    - Intrastat-aruanne
    - Intrastat XML
    - Intrastat XML (DE)

2. Kandeteksti loomine.

    1. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Kandekoodid**.
    2. Valige toimingupaanil nupp **Uus**.
    3. Väljal **Kande** **kood** sisestage väärtus **21**.
    4. Väljale **Nimi** sisestage väärtus **Kaupade tagastamine**.
    5. Valige toimingupaanil nupp **Salvesta**.

3. Saate seadistada asutuse ID-koodi.

    1. Klõpsake suvandeid **Maks** > **Kaudsed maksud** > **Käibemaks** > **Käibemaksuhaldurid**.
    2. Loendist valige **TA**.
    3. Sisestage väljale **Maksuamet ID** väärtus **123**.

4. Regioonikoodide häälestamine.

    1. Avage **Organisatsioonihaldus** > **Globaalne aadressiraamat** > **Aadress** > **Aadressi seadistus**.
    2. Valige **Osariik/provints** vahekaardi **Riik/regioon** väljal **DEU** ja seejärel valige **Rakenda filter**.
    3. Ruudustikus valige **BE** ja seejärel sisestage **Intrastat-koodi** väljale **11**.
    4. Valige toimingupaanil nupp **Salvesta**.

5. Väliskaubanduse parameetrite häälestamine.

    1. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Väliskaubanduse parameetrid**.
    2. Valige vahekaardil **Intrastat** kiirkaardil **Üldine** väljal **Kande** **kood** väärtus **11**.
    3. Väljal **Kreeditarve** valige **21**.
    4. Väljal **maksuhaldur** valige **TA**.
    5. Valige kiirkaardi **Elektrooniline aruandlus** väljal **Failivormingu vastendamine** **INSTAT XML (DE)**.
    6. Sisestage või valige väärtus **Intrastati aruanne** väljal **Aruandevormingu vastendamine**.
    7. Veenduge, et kiirkaardi **Kaubaartikli hierarhia** väljal **Kategooriahierarhia** oleks valitud väärtus **Intrastat**.
    8. Klõpsake vahekaardil **Riigi/regiooni atribuudid** valimiseks **Uus**.
    9. Väljal **Riik/regioon** valige **FRA**.
    10. Valige väljalt **Riigi/regiooni tüüp** suvand **EL**.

6. Määrake tootele artiklikood ja määrake toote päritolu. Väljad **Kauba kood** **Päritoluriik/regioon** ja **päritolu** seatakse seejärel toote valides automaatselt müügitellimustele ja ostutellimustele.

    1. Avage **Tooteteabe haldus** > **Tooted** > **Väljastatud tooted**.
    2. Valige ruudustikus **D0001**.
    3. Valige kiirkaardi **Väliskaubandus** jaotise **Intrastat** väljal **Kaup** valige **920 20 34**.
    4. **Päritolu** jaotises **Riik/regioon** väljal valige **DEU**.
    5. Kiirkaardi **Varude haldamine**  jaotise **Kaaluühikud** väljale **Netokaal** sisestage **12**.
    6. Valige toimingupaanil nupp **Salvesta**.

7. Määrake transport tarneviisile. Tarneviisi valides lisatakse siis tellimustele transpordikoodid automaatselt.

    1. Minge jaotisse **Ostmine ja hankimine** > **Seadistamine** > **Tarneviis** > **Saatmise mudel**.
    2. Loendist valige **10**.
    3. Kiirkaardi **Väliskaubandus** väljal **Transport** valige **01**.

8. Looge müügitellimus EL-i kliendiga.

    1. Avage **Müügireskontro** > **Tellimused** > **Kõik müügitellimused**.
    2. Valige toimingupaanil nupp **Uus**.
    3. Valige dialoogiboksi **Loo müügi tellimus** jaotises **Klient** väljas **Kliendi** jaotises **Kliendi konto** väljal väärtus **De-012**.
    4. Valige **Üldine** kiirkaardi jaotise **Ladustamisdimensioonid** väljal **Saidi väärtus** väärtus **1**.
    5. Valige väljal **Ladu** väärtus **11**.
    6. Valige nupp **OK**.
    7. Vahekaardil **Päis** kiirkaardil **Väliskaubandus** väljal **Sadam** valige **53**.
    8. Väljal **Statistiline protseduu** valige **31710**.
    9.  Valige **Read** vahekaardil **Müügi tellimuse** **ridade** väljal **Kaubakoodi** väärtuseks **D0001**. Sisestage väljale **Kogus** väärtus **10**.
    10. Väliskaubanduse vahekaardi **Rea üksikasjade** kiirkaardil veenduge, et **Kande koodi** **Transport**, **Kaup**, **Päritoluriik** ja **Riik/regioon** oleks automaatselt seatud.
    11. Valige toimingupaanil nupp **Salvesta**.
    12. Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.
    13. Valige dialoogiboksi **Arve sisestamine** kiirkaardi **Parameetrid** jaotises **Parameeter** väljal **Kogus** suvand **Kõik**.
    14. Klõpsake sissetuleku sisestamiseks nuppu **OK**.

9.  Kandge kanne üle Intrastati töölehele ja vaadake tulemus üle.

    1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
    2. Valige tegevuste paanil käsk **Insener**.
    3. Seadke dialoogiboksi **Intrastat (ülekanne)** jaotises **Parameetrid** valiku **Kliendiarve** väärtuseks **Jah**.
    4. Valige **Filter**.
    5. Valige **Intrastati filter** esimene rida ja veenduge, et välja **Ulatus** dialoogiboksisväärtuseks oleks seatud **Väli** ja **Kuupäev**.
    6. Valige **Kriteeriumid** väljal praegune kuupäev.
    7. Valige dialoogiboksi **Intrastat filter** sulgemiseks **OK**.
    8. Valige **OK**, et sulgeda **Intrastati (ülekanne)** dialoogiboks ja vaadake tulemus üle. Rida tähistab varem loodud müügitellimust.

        ![Rida tähistab Intrastati lehe müügitellimust](media/intrastat_deu_1.png)

10. Valige kande rida ja seejärel valige vahekaart **Üldine**, et vaadata rohkem üksikasju.

    ![Müügitellimuse üksikasjad intrastati lehe vahekaardil Üldine](media/intrastat_deu_2.png)

11. Kreeditarve loomine müügitellimuse abil.

    1. Avage **Müügireskontro** > **Tellimused** > **Kõik müügitellimused**.
    2. Valige toimingupaanil nupp **Uus**.
    3. Valige dialoogiboksi **Loo müügi tellimus** jaotises **Klient** väljas **Kliendi** jaotises **Kliendi konto** väljal väärtus **De-012**.
    4. Valige **Üldine** kiirkaardi jaotise **Ladustamisdimensioonid** väljal **Saidi väärtus** väärtus **1**.
    5. Valige väljal **Ladu** väärtus **11**.
    6. Vahekaardil **Päis** kiirkaardil **Väliskaubandus** väljal **Sadam** valige **53**.
    7. Väljal **Statistiline protseduu** valige **31710**.
    8. Valige **Read** vahekaardil **Müügi tellimuse** **ridade** väljal **Kaubakoodi** väärtuseks **D0001**. Sisestage väljale **Kogus** väärtus **-2**.
    9. Kiirkaardil **Liini üksikasjad** vahekaardil **Väliskaubandus** väljal **Tehingukood** väärtus **21**.
    10. Veenduge, et **Transport**, **Kaup**, ja **Päritoluriik/regioon** oleks automaatselt seadistatud.
    11. Valige toimingupaanil nupp **Salvesta**.
    12. Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.
    13. Valige dialoogiboksi **Arve sisestamine** kiirkaardi **Parameetrid** jaotises **Parameeter** väljal **Kogus** suvand **Kõik**.
    14. Klõpsake sissetuleku sisestamiseks nuppu **OK**.

12. Kandge kanne üle Intrastati töölehele ja vaadake tulemus üle.

    1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
    2. Valige tegevuste paanil käsk **Insener**.
    3. Seadke dialoogiboksi **Intrastat (ülekanne)** jaotises **Parameetrid** valiku **Kliendiarve** väärtuseks **Jah**.
    4. Valige **OK**, et sulgeda **Intrastati (ülekanne)** dialoogiboks ja vaadake tulemus üle. Uus rida, kus **Suund** väli on seadistatud **Saabumistele**, on lisatud.            
        See rida näitab kaupade füüsilist tagastamist.

        ![Kaupade füüsilise tagastuse rida Intrastati lehel](media/intrastat_deu_3.png)

13. Valige kande rida ja seejärel valige vahekaart **Üldine**, et vaadata rohkem üksikasju.

    ![Kaupade füüsilise tagastuse üksikasjad Intrastati lehe vahekaardil Üldine](media/intrastat_deu_4.png)

14. Paranduse loomine müügitellimuse abil:

    1. Avage **Müügireskontro** > **Tellimused** > **Kõik müügitellimused**.
    2. Valige toimingupaanil nupp **Uus**.
    3. Valige dialoogiboksi **Loo müügi tellimus** jaotises **Klient** väljas **Kliendi** jaotises **Kliendi konto** väljal väärtus **De-012**.
    4. Valige **Üldine** kiirkaardi jaotise **Ladustamisdimensioonid** väljal **Saidi väärtus** väärtus **1**.
    5. Valige väljal **Ladu** väärtus **11**.
    6. Vahekaardil **Päis** kiirkaardil **Väliskaubandus** väljal **Sadam** valige **53**.
    7. Väljal **Statistiline protseduu** valige **31710**.
    8. Valige **Read** vahekaardil **Müügi tellimuse** **ridade** väljal **Kaubakoodi** väärtuseks **D0001**. Sisestage väljale **Kogus** väärtus **-3**.
    9. Kiirkaardil **Liini üksikasjad** vahekaardil **Väliskaubandus** väljal **Tehingukood** väärtus **11**.
    10. Veenduge, et **Transport**, **Kaup**, ja **Päritoluriik/regioon** oleks automaatselt seadistatud.
    11. Valige toimingupaanil nupp **Salvesta**.
    12. Veenduge, et välja **Tehingukood** on seatud väärtusele 11.
    13. Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.
    14. Valige dialoogiboksi **Arve sisestamine** kiirkaardi **Parameetrid** jaotises **Parameeter** väljal **Kogus** suvand **Kõik**.
    15. Klõpsake sissetuleku sisestamiseks nuppu **OK**.

15. Kandge kanne üle Intrastati töölehele ja vaadake tulemus üle:

    1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
    2. Valige tegevuste paanil käsk **Insener**.
    3. Seadke dialoogiboksi **Intrastat (ülekanne)** jaotises **Parameetrid** valiku **Kliendiarve** väärtuseks **Jah**.
    4. Valige **OK**, et sulgeda **Intrastati (ülekanne)** dialoogiboks ja vaadake tulemus üle. Uus rida, kuhu on lisatud veerus **Parandus** märge.

        ![Paranduse rida Intrastati lehel](media/intrastat_deu_5.png)

16. Valige kande rida ja seejärel valige vahekaart **Üldine**, et vaadata rohkem üksikasju.

    ![Paranduse üksikasjad lehel Intrastat vahekaardil Üldine](media/intrastat_deu_6.png)

17. Toimingupaanil valige suvandid **Väljund** > **Aruanne**.
18. Valige dialoogiboksi **Intrastat-aruanne** kiirkaardil **Parameetrid** jaotises **Kuupäev** loodud müügitellimuse kuu.
19. Seadke jaotises **Ekspordi** **suvandid**, suvandi **Loo fail** väärtuseks **Jah**.
20. Sisestage faili nõutav nimi väljale **Faili nimi**.
21. Valige **OK** ja vaadake loodud aruanne üle. Järgmine tabel näitab näidisaruande väärtusi.

    | **Nimi**                  | **Müügiarve**  |   **Parandus**   | **Kreeditarve** |
    |---------------------------|--------------------|--------------------|-----------------|
    | declarationId             | 2021-07-D          | 2021-07-A          |                 |
    | Viiteperiood           | 2021-07            | 2021-07            |                 |
    | PSIId                     | 11203/118/12345000 | 11203/118/12345000 |                 |
    | functionCode              | O                  | O                  |                 |
    | Vookood                  | D                  | A                  |                 |
    | CurrencyCode              | EUR                | EUR                |                 |
    | itemNumber                | 0000362            | 0000362            | 0000361         |
    | CN8Code                   | 9202034            | 9202034            | 9202034         |
    | Kauba kirjeldus          | Esineja            | Esineja            | Esineja         |
    | MsConsDestCode            | FR                 | FR                 | FR              |
    | countryOfOriginCode       | \-                 | \-                 | DE              |
    | netomass                   | 120                | -36                | 24              |
    | Arve summa            | 3290               | -987               | \-              |
    | Statistiline väärtus          | 3290               | -987               | 658             |
    | natureOfTransactionACode  | 1                  | 1                  | 2               |
    | natureOfTransactionBCode  | 1                  | 1                  | 1               |
    | modeOfTransportCode       | 1                 | 1                 | 1              |
    | regiooni kood                | 11                 | 11                 | 11              |
    | portAirportInlandportCode | 53                 | 53                 | 53              |

