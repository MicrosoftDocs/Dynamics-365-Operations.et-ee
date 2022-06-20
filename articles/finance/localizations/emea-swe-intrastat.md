---
title: Rootsi Intrastat
description: See artikkel sisaldab teavet Intrastat-aruandluse kohta Rootsis.
author: anasyash
ms.date: 8/24/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: a81f0c19923d1a4747c2ecb8ab03dd86b45497ad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886256"
---
# <a name="swedish-intrastat"></a>Rootsi Intrastat

[!include[banner](../includes/banner.md)]

**Intrastat** lehte kasutatakse Euroopa Liidu (EL) riikide vahelise kaubavahetuse aruannete loomiseks ja esitamiseks. Rootsi Inrastati deklaratsioon sisaldab aruandluseks teavet kauplemise kohta.

Rootsi Intrastati deklaratsioonis on kaasatud järgmised väljad:

   - Partneri riigi ISO-kood
   - Kandekood
   - Kaubaartikkel
   - Lisaühik
   - Kaal
   - Arve summa

## <a name="set-up-intrastat"></a>Intrastati seadistamine

Importige järgmiste elektroonilise aruandluse (ER) konfiguratsioonide uusim versioon:

   - Intrastati mudel
   - Intrastat-aruanne
   - Intrastat (SE)

Lisateavet leiate teemast [ER konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-foreign-trade-parameters"></a>Väliskaubanduse parameetrite häälestamine

1. Finantside Microsoft Dynamics 365 puhul minge **väliskaubanduse** > **maksu** > **seadistamise parameetritele**.
2. Vahekaardil **Intrastat** kiirkaardi **Elektrooniline aruandlus** väljal **Failivormingu vastendamine**, valige **Intrastat (SE)**.
3. Sisestage või valige väärtus **Intrastati aruanne** väljal **Aruandevormingu vastendamine**.
4. Valige kiirkaardi **Kaubaartikli hierarhia** väljal **Kategooriahierarhia** väärtus **Intrastat**.
5. Väljal **Kande kood** valige varaülekannete kandekood. Seda koodi kasutatakse tehingute jaoks, mis põhjustavad vara tegeliku või kavandatud üleandmise hüvitise eest (finantsiline ja muu). Seda kasutatakse ka paranduste puhul. Rootsi ettevõtted kasutavad ühekohalist kandekoodi.
6. Väljal **Kreeditmärge** valige kandekood kaupade tagastamiseks.
7. Vahekaardil **Riigi/regiooni atribuudid** väljal **Riik/regioon**, loetlege kõik riigid või regioonid, millega teie organisatsioonil on ärisuhted. Iga riigi puhul, mis on ELi osa, väljal **Riigi/regiooni tüüp** valige **EL**, et teie riik või regioon ilmuks teie Intrastat-aruandes.

## <a name="set-up-the-product-parameters-for-the-intrastat-declaration"></a>Intrastati deklaratsiooni tooteparameetrite seadistamine

1. Avage **Tooteteabe haldus** > **Tooted** > **Väljastatud tooted**.
2. Valige ruudustikus toode.
3. Kiirkaardi **Väliskaubandus** jaotise **Intrastat** väljal **Kaup** valige sobiv kauba kood.
4. Kiirkaardi **Varude haldamine** jaotise **Kaaluühikud** väljale sisestage toote kaal kilogrammides.
5. Minge **Maks** > **Seadistamine** > **Väliskaubandus** > **Intrastati kompressioon** ja valige väljad, mida tuleb Intrastati teabe summeerimisel võrrelda. Rootsi Intrastati jaoks valige järgmised väljad:

    - Artikkel
    - Kandekood
    - Direction
    - Riik/regioon
    - Parandus
    - Arve

## <a name="intrastat-transfer"></a>Intrastati ülekanne

**Intrastati** lehel saate valida tegevuspaanil valiku **Ülekanne**, et edastada automaatselt oma müügitellimuste, vabas vormis arvete, ostutellimuste, hankija arvete, hankija toote sissetulekute, projektiarvete ja üleviimistellimuste teabe automaatne ülekandmine. Edastatakse ainult dokumendid, mille sihtriigiks või -piirkonnaks (lähetamiseks) või saadetiseks (saabumiseks) on ELi riik.

Teise võimalusena saate kandeid käsitsi sisestada, valides tegevuspaanil valiku **Uus**.

### <a name="generate-an-intrastat-report"></a>Looge Intrastati aruanne

1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
2. Toimingupaanil valige suvandid **Väljund** > **Aruanne**.
3. Määrake dialoogiboksis **Intrastati aruanne** järgmised väljad.

    | Field            | Kirjeldus                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Alates kuupäevast        | Valige aruande alguskuupäev.                                                                                               |
    | Lõppkuupäev          | Valige aruande lõppkuupäev.                                                                                                 |
    | Loo fail    | .txt tekstifaili genereerimiseks Intrastati aruande jaoks määrake suvandi väärtuseks **Jah**.                                                       |
    | Faili nimi        | Sisestage .txt faili nimi.                                                                                                    |
    | Aruande loomine  | .xlsx faili genereerimiseks Intrastati aruande jaoks määrake suvandi väärtuseks **Jah**.                                                     |
    | Aruandefaili nimi | Sisestage .xlsx faili nimi.                                                                                                   |
    | Direction        | Valige ühendusesiseste saabumiste aruande jaoks **Saabumised**. Valige ühendusesiseste lähetuste aruande jaoks **Lähetused**. |

4. Valige **OK** ja vaadake loodud aruanded üle.

## <a name="example"></a>Näide

See näide näitab, kuidas sisestada Intrastati saabumised ja lähetamised. See kasutab **DEMF** juriidilist isikut.

### <a name="preliminary-setup"></a>Esialgne seadistamine

1. Minge **organisatsiooni haldus** > **organisatsioon** > **juriidilised isikud** ja valige **DEMF** juriidiline isik.
2. Valige **aadresside** kiirkaardil käsk **Redigeeri** ja seejärel valige väljal **Riik/regioon** **SWE (Rootsi)**.
3. Importige elektroonilise aruandluse (ER) konfiguratsioonide uusim versioon:

    - Intrastati mudel
    - Intrastat-aruanne
    - Intrastat (SE)

### <a name="create-transaction-codes"></a>Kandekoodi loomine

1. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Kandekoodid**.
2. Valige toimingupaanil nupp **Uus**.
3. Väljal **Kande** **kood** sisestage väärtus **1**.
4. Väljal **Nimi** sisestage väärtus **Tavalised kanded**
5. Valige toimingupaanil nupp **Salvesta**.

### <a name="set-up-foreign-trade-parameters"></a>Väliskaubanduse parameetrite häälestamine

1. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Väliskaubanduse parameetrid**.
2. Valige vahekaardil **Intrastat** kiirkaardil **Üldine** väljal **Kande** **kood** väärtus **1**.
3. Valige kiirkaardi **Elektrooniline aruandlus** väljal **Failivormingu vastendamine** **Intrastat (SE)**.
4. Sisestage või valige väärtus **Intrastati aruanne** väljal **Aruandevormingu vastendamine**.
5. Veenduge, et kiirkaardi **Kaubaartikli hierarhia** väljal **Kategooriahierarhia** oleks valitud väärtus **Intrastat**.
6. Klõpsake vahekaardil **Riigi/regiooni atribuudid** valimiseks **Uus**.
7. Väljal **Riik/regioon** valige **SWE**.
8. Valige väljalt **Riigi/regiooni tüüp** suvand **Kodumaine**.
9. Väljal **Osapoole riik/regioon** valige **DEU** ja seejärel valige väljal **Riigi/regiooni tüüp** suvand **EL**.

### <a name="set-up-product-information"></a>Seadistage tooteteave

1. Avage **Tooteteabe haldus** > **Tooted** > **Väljastatud tooted**.
2. Valige ruudustikus **D0001**.
3. Valige kiirkaardi **Väliskaubandus** jaotise **Intrastat** väljal **Kaup** valige **100 200 30**.
4. Kiirkaardi **Varude haldamine**  jaotise **Kaaluühikud** väljale **Netokaal** sisestage **5**.
5. Valige toimingupaanil nupp **Salvesta**.

### <a name="change-the-site-address"></a>Muutke saidi aadressi

1. Avage jaotis **Warehouse management** > **Seadistus** > **Ladu** > **Saidid**.
2. Valige ruudustikus **1**.
3. Kiirkaardil **Aadressid** valige **Redigeeri**.
4. Dialoogiakna **Aadressi redigeerimine** väljal **Riik/regioon** valige **SWE**.
5. Valige nupp **OK**.

### <a name="create-a-sales-order-with-an-eu-customer"></a>Looge müügitellimus EL-i kliendiga

1. Avage **Müügireskontro** > **Tellimused** > **Kõik müügitellimused**.
2. Valige toimingupaanil nupp **Uus**.
3. Valige dialoogiboksi **Loo müügi tellimus** jaotises **Klient** väljas **Kliendi** jaotises **Kliendi konto** väljal väärtus **De-015**.
4. Valige **Üldine** kiirkaardi jaotise **Ladustamisdimensioonid** väljal **Saidi väärtus** väärtus **1**.
5. Valige väljal **Ladu** väärtus **11**.
6. Valige nupp **OK**.
7. Valige **Read** vahekaardil **Müügi tellimuse ridade** väljal **Kaubakoodi** väärtuseks **D0001**. Sisestage väljale **Kogus** väärtus **10**.
8. **Rea üksikasjade** kiirkaardil **Väliskaubanduse** vahekaardil veenduge, et **Kande koodi** ja **Kaup** väljad oleks automaatselt seatud.
9. Valige toimingupaanil nupp **Salvesta**.
10. Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.
11. Valige dialoogiboksi **Arve sisestamine** kiirkaardi **Parameetrid** jaotises **Parameeter** väljal **Kogus** suvand **Kõik**.
12. Klõpsake sissetuleku sisestamiseks nuppu **OK**.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Kandke kanne üle Intrastati töölehele ja vaadake tulemus üle

1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
2. Valige tegevuste paanil käsk **Insener**.
3. Seadke dialoogiboksi **Intrastat (ülekanne)** jaotises **Parameetrid** valiku **Kliendiarve** väärtuseks **Jah**.
4. Valige **Filter**.
5. Valige **Intrastati filter** esimene rida ja veenduge, et välja **Ulatus** dialoogiboksisväärtuseks oleks seatud **Väli** ja **Kuupäev**.
6. Valige **Kriteeriumid** väljal praegune kuupäev.
7. Valige dialoogiboksi **Intrastat filter** sulgemiseks **OK**.
8. Valige **OK**, et sulgeda **Intrastati (ülekanne)** dialoogiboks ja vaadake tulemus üle. Rida tähistab varem loodud müügitellimust.

    ![Intrastati töölehe read müügitellimuse jaoks](media/swe_intrastat_journal_sales_order.png)

9. Valige kande rida ja seejärel valige vahekaart **Üldine**, et vaadata rohkem üksikasju.

    ![Intrastati töölehe read müügitellimuse jaoks](media/swe_intrastat_journal_sales_order_line_details.png)

10. Toimingupaanil valige suvandid **Väljund** > **Aruanne**.
11. Valige dialoogiboksi **Intrastat-aruanne** kiirkaardil **Parameetrid** jaotises **Kuupäev** loodud müügitellimuse kuu.
12. Seadke jaotises **Ekspordi** **suvandid**, suvandi **Loo fail** väärtuseks **Jah**. Siis sisestage faili nõutav nimi väljale **Faili nimi**.
13. Määrake suvand **Loo aruanne** valikule **Jah**. Siis sisestage nõutav nimi väljale **Aruande faili nimi**.
14. Valige **Saadetised** väljalt **Suund**.
15. Valige **OK** ja vaadake .txt formaadis loodud aruanne üle. Järgmine tabel näitab näidisaruande väärtusi.

    | Partneri riigi ISO-kood | Kandekood | Kaubaartikkel | Lisaühik | Kaal | Arve summa |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 50     | 3290           |

16. Vaadake loodud fail Exceli vormingus üle.

    ![Intrastat-aruanne](media/swe_intrastat_report_for_dispatches.png)

### <a name="create-a-purchase-order"></a>Ostutellimuse loomine

1. Avage **Ostureskontro** > **Ostutellimused** > **Kõik ostutellimused**.
2. Valige toimingupaanil nupp **Uus**.
3. Valige dialoogiboksi **Müügitellimuse loomine** väljal **Hankija konto** suvand **DE-001**.
4. Valige nupp **OK**.
5. Veenduge, **Päis** **Välis** **Kaubanduse** kiirkaardil **Kande kood** väljal oleks seatud väärtusele **1**.
6. Valige **Read** vahekaardil **Müügi tellimuse ridade** väljal **Kaubakoodi** väärtuseks **D0001**. Sisestage väljale **Kogus** väärtus **6**.
7. Valige toimingupaanil vahekaardi **Ostmine** grupis **Tegevused** suvand **Kinnita**.
8. Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.
9. Valige tegumiribal suvand **Vaike vorm**. Valige **Tellitud kogus** väljal **Ridade vaikekogus**. Seejärel valige **OK**.
10. Sisestage **hankija arve päise** kiirkaardi jaotise **Arve ID** jaotisse **Number** väljale väärtus **0001**.
11. Valige arve postitamiseks toimingupaanilt **Postita**.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Intrastati deklaratsiooni loomine saabumiste jaoks

1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
2. Valige tegevuste paanil käsk **Insener**.
3. Dialoogiboksis **Intrastat (ülekanne)** seadke **hankija arve** valikuks **Jah**.
4. Tehingute ülekandmiseks valige **OK** ja vaadake Intrastati päevikut.

    ![Intrastati tööleht ostutellimuse jaoks](media/swe_intrastat_journal_purchase_order.png)

5. Vaadake üle **Üldine** ostutellimuse vahekaart.

    ![Intrastati töölehe read ostutellimuse jaoks](media/swe_intrastat_journal_purchase_order_line_details.png)

6. Toimingupaanil valige suvandid **Väljund** > **Aruanne**.
7. Valige dialoogiboksi **Intrastat-aruanne** kiirkaardil **Parameetrid** jaotises **Kuupäev** loodud müügitellimuse kuu.
8. Seadke jaotises **Ekspordi** **suvandid**, suvandi **Loo fail** väärtuseks **Jah**. Siis sisestage faili nõutav nimi väljale **Faili nimi**.
9. Määrake suvand **Loo aruanne** valikule **Jah**. Siis sisestage nõutav nimi väljale **Aruande faili nimi**.
10. Valige **Suund** väljalt **Saabumised**.
11. Valige **OK** ja vaadake .txt formaadis loodud aruanne üle. Järgmine tabel näitab näidisaruande väärtusi.

    | Partneri riigi ISO-kood | Kandekood | Kaubaartikkel | Lisaühik | Kaal | Arve summa |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 30     | 1714           |

12. Vaadake loodud fail Exceli vormingus üle.

    ![Intrastati saabumiste aruanne](media/swe_intrastat_arrivals_report.png)
