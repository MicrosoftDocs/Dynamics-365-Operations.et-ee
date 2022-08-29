---
title: Saabumiste ja lähetuste sisestamine Intrastati jaoks
description: See artikkel annab näite, mis näitab, kuidas sisestada Saabumised ja lähetused Intrastati jaoks.
author: AdamTrukawka
ms.date: 08/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: b6d46efd477f526c4bec3515086e10aa8172c579
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280683"
---
# <a name="post-arrivals-and-dispatches-for-intrastat"></a>Saabumiste ja lähetuste sisestamine Intrastati jaoks

[!include [banner](../includes/banner.md)]

See artikkel annab näite, mis näitab, kuidas sisestada Saabumised ja lähetused Intrastati jaoks. Näites kasutatakse **ITCO** juriidilist isikut.

## <a name="setup"></a>Seadistus

1. Importige järgmiste elektroonilise aruandluse (ER) konfiguratsioonide uusim versioon:

    - Intrastati mudel
    - Intrastat-aruanne
    - Intrastat (IT)

    Lisateavet leiate teemast [ER konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

2. Määratlege Microsoft Dynamics 365 Finantsis järgmised numbriseeriad pidevaks: **Gene\_ 397**, **A\_ 16403**, **Gene\_ 407** ja **PUR\_ EL**.

    1. Avage **Organisatsiooni haldus** > **Numbriseeriad** > **Numbriseeriad**.
    2. Valige ruudustikus üks numbriseeria koodidest.
    3. Valige Toimingupaanil nupp **Redigeeri**.
    4. Määrake kiirkaardi **Üldine** jaotises **Seadista** valiku **Pidev** väärtuseks **Jah**.
    5. Valige toimingupaanil nupp **Salvesta**.

3. Lao aadressi seadistamine.

    1. Avage **Laohaldus** &gt; **Seadistus** &gt; **Ladu** &gt; **Laod**.
    2. Valige loendist ladu **11**.
    3. Valige **Aadress** kiirkaardil käsk **Lisa**.
    4. Dialoogiaknas **Uus aadress**, **aadress** **nimi** **või** **kirjeldus** väljal sisestage **Peamine**.
    5. Väljal **Riik/regioon** valige **ITA (Itaalia)**.
    6. Väljal **Linn** valige **Aprilia**.
    7. Valige nupp **OK**.

4. Saate häälestada kandekoode.

    1. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Kandekoodid**.
    2. Valige **uus** ja seadistage kandekood atribuudi ülekannete jaoks.

        - Sisestage väljas **Kandekood** **1**.
        - Väljale **nimi** sisestage **Vara üleandmine**.

    3. Valige **uus** ja seadistage tagastamiseks kandekood.

        - Väljal **Kande** **kood** sisestage väärtus **2**.
        - Väljale **Nimi** sisestage väärtus **Kaupade tagastamine**.

5.  Väliskaubanduse parameetrite häälestamine.

    1. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Väliskaubanduse parameetrid**.
    2. Valige vahekaardil **Intrastat** kiirkaardil **Üldine** väljal **Kande** **kood** väärtus **1**.
    3. Väljal **Kreeditarve** valige **2**.
    4. Valige **Igakuine** väljal **Müügi aruandlusperiood**.
    5. Valige **Igakuine** väljal **Ostude aruandlusperiood**.
    6. Valige kiirkaardi **Elektrooniline aruandlus** väljal **Failivormingu vastendamine** **Intrastat (IT)**.
    7. Sisestage või valige väärtus **Intrastati aruanne** väljal **Aruandevormingu vastendamine**.
    8. Valige kiirkaardi **Kaubaartikli hierarhia** väljal **Kategooriahierarhia** väärtus **Intrastat**.
    9. Seadke kiirkaardi **Statistiline väärtus** suvandi **Prindi ja ekspordi statistilised andmed** väärtuseks **Jah**.
    10. Kontrollige **Riigi/regiooni atribuudid** vahekaardil, et järgmised read on olemas.

        | **Osapoole/riik/regioon** | **Intrastati kood** | **Currency** | **Riigi/regiooni tüüp** |
        |--------------------------|--------------------|--------------|-------------------------|
        | ITA                      | IT                 | EUR          | Kodumaine                |
        | SMR                      | SM                 | EUR          | Spetsiaalne kodumaine        |

    11. Rea loomiseks valige toimingupaanilt suvand **Uus**.

        | **Osapoole/riik/regioon** | **Intrastati kood** | **Currency** | **Riigi/regiooni tüüp** |
        |--------------------------|--------------------|--------------|-------------------------|
        | DNK                      | DK                 | taani kroon          | EL                      |

6. Saate häälestada maksukohuslase numbreid.

    1. Minge jaotisse **Maks** > **Seadistus** > **Käibemaks** > **Maksuvabastuse numbrid**.
    2. Rea loomiseks valige toimingupaanilt suvand **Uus**.

        | **Riik/regioon** | **Maksuvabastuse number** | **Ettevõtte nimi** |
        |--------------------|-----------------------|------------------|
        | DEU                | DE3456789012          | UE HANKIJA        |
        | DNK                | DK0987654321          | Kliendi ER      |

7. Hankija aadressi seadistamine.

    1. Avage **Ostureskontro** &gt; **Hankijad** &gt; **Kõik hankijad**.
    2. Valige ruudustikus **UE hankija**.
    3. Valige **Aadressid** kiirkaardil käsk **Lisa**.
    4. Sisestage dialoogiaknas **Uus aadress** väljale **Kirjelduse nimi**, **Saksamaa**.
    5. Väljal **Riik/regioon** valige **DEU**.
    6. Valige uue aadressi loomiseks **OK**.
    7. Valige kiirkaardi **Arve ja tarne** jaotises **Käibemaks** väljal **Maksukohuslase kood** valik **Kõik** ja siis valige **DE1234567890**.
    8. Valige toimingupaanil nupp **Salvesta**.

8. Seadistage kliendi aadress.

    1. Avage **Müügireskontro** > **Kliendid** > **Kõik kliendid**.
    2. Valige ruudustikus **ITC-O000001**.
    3. Kiirkaardil **Aadressid** valige **Redigeeri**.
    4. Sisestage dialoogiaknas **Uus aadress** väljale **Nimi või kirjeldus**, **San Marino**.
    5. Väljal **Riik/regioon** valige **SMR**.
    6. Valige uue aadressi loomiseks **OK**.
    7. Valige **Arve ja tarne** kiirkaardi jaotise **Arve** väljal **Arve konto** väärrtus **ITCO-000001**.
    8. Valige **Numbriseeria** väljal suvand **IT\_VENDOM**.
    9. Valige tegevuspaanil **Salvesta** ja sulgege lehekülg.
    10. Valige **kõigi klientide** ruudustikus lehel **ITCO-000002**.
    11. Valige **Aadressid** kiirkaardil käsk **Lisa**.
    12. Sisestage dialoogiaknas **Uus aadress** väljale **Nimi või kirjeldus**, **Taani**.
    13. Väljal **Riik/regioon** valige **DNK**.
    14. Valige uue aadressi loomiseks **OK**.
    15. **Müügigeograafia** kiirkaardil väljal **Valuuta** valige **DKK**.
    16. Kiirkaardi **Arve ja tarne** jaotises **Käibemaks** väljal **Käibemaksu grupp** valige **IT\_PUREU**.
    17. Väljal **Maksukohuslase kood** valige **Kõik** ja seejärel valige **DK0987654321**.
    18. Valige toimingupaanil nupp **Salvesta**.

9. Kategooriahierarhia seadistamine.

    1. Minge jaotisse **Tooteteabe haldus** > **Seadistus** > **Kategooriad ja atribuudid** > **Kategooria hierarhiad**.
    2. Valige ruudustikus **Intrastat**.
    3. Valige Toimingupaanil nupp **Uus kategooria sõlm**.
    4. Väljale **Nimi** sisestage suvand **Teenus**.
    5. Sisestage väljal **Kood** **123456**.
    6. Valige toimingupaanil nupp **Salvesta**.

10. Seadistage tooted.

    1. Avage **Toote informatsiooni haldus** > **Tooted** > **Väljastatud tooted**.
    2. Valige ruudustikus **ITEM**.
    3. Valige **ostu** kiirkaardi jaotise **Administreerimine** väljal **Hankija** suvand **ITCO-000001**.
    4. Valige kiirkaardi **Väliskaubandus** jaotise **Intrastat** väljal **Kaup** valige **\[100 200 30\] Spiiker**.
    5. **Päritolu** jaotises **Riik/regioon** väljal valige **DEU**.
    6. Valige väljalt **Osariik/provints** suvand **BE**.
    7. Kiirkaardi **Varude haldamine** jaotise **Neto kaaluühikud** väljale **Netokaal** sisestage **5**.
    8. Valige toimingupaanil nupp **Salvesta**.
    9. Valige **Väljastatud toodete** lehel ruudustikus **Teenusüksus**.
    10. Kiirkaardi **Väliskaubandus** jaotise **Intrastat** väljal **Kaup** valige **\[123456\] Teenus**.
    11. Valige toimingupaanil nupp **Salvesta**.

11. Seadistage transpordimeetodid.

    1. Avage **Maks** > **Seadistus** > **Väliskaubandus** > **Transpordimeetodid**.
    2. Järgmiste transpordi meetodite loomiseks valige toimingupaanilt suvand **Uus**.

        | **Transport** | **Kirjeldus** |
        |---------------|-----------------|
        | 1             | Tee            |
        | 2             | Lennupost             |

12. Seadistage kohaletoimetamise viis.

    1. Minge jaotisse **Ostmine ja hankimine** > **Seadistamine** > **Tarneviis** > **Saatmise mudel**.
    2. Valige toimingupaanil nupp **Uus**.
    3. Väljale **Kättetoimetamisviis** sisestage **1**.
    4. Sisestage väljale **Kirjeldus** väärtus **Veok**.
    5. Kiirkaardi **Väliskaubandus** väljal **Transport** valige **1 Tee**.
    6. Valige toimingupaanil nupp **Salvesta**.

13. Tarnetingimuste seadistamine.

    1. Avage **Ostureskontro** > **Seadistamine** > **Tarnetingimused**.
    2. Loendist valige **CFR**.
    3. Kiirkaardi **Üldine** väljal **Intrastati kood** valige **1**.

## <a name="post-arrivals-for-intrastat"></a>Saabumiste sisestamine Intrastati jaoks

### <a name="purchase-goods-by-using-a-purchase-order"></a>Kaupade ostmine ostutellimuse abil

See näite osa näitab, kuidas kasutada ostutellimust Euroopa Liidu (EL) riikidest kaupade (ühikud) ostmiseks.

1. Avage **Ostureskontro** > **Ostutellimused** > **Kõik ostutellimused**.
2.  Valige toimingupaanil nupp **Uus**.
3.  Valige dialoogiboksi **Müügitellimuse loomine** väljal **Hankija konto** suvand **UE Hankija**.
4.  Valige **Administreerimine** kiirkaardil **Keel** väljal **see**.
5.  Valige nupp **OK**.
6.  Veenduge, et **Päis** vaates **Välis** **Kaubanduse** kiirkaardil **Kande kood** väljal oleks seatud väärtusele **1**.
7.  Kontrollige, et **Riigi lähte-/sihtkoha** väärtuseks on seatud **RM**.
8.  Kiirkaardi **Kohaletoimetamine** jaotise **Kohaletoimetamine** väljal **Tarnerežiim** valige **1**.
9.  Väljal **tarnetingimused** valige **CFR**.
10. Valige **Read** vaates **Müügi tellimuse ridade** kiirkaardil **Kaubakoodi** väärtuseks **Üksus**.
11. Valige väljal **Tegevuskoht** väärtus **1**.
12. Valige väljal **Ladu** väärtus **11**.
13. Sisestage väljale **Kogus** väärtus **10**.
14. Sisestage väljale **Ühiku hind** väärtus **100**.
15. Kiirkaardil **Seadista** jaotises **Käibemaks** väljal **Käibemaksu grupp** valige **22%EL**.
16. Valige toimingupaanil vahekaardi **Ostmine** grupis **Tegevused** suvand **Kinnita**.
17. Valige toimingupaani vahekaardil **Arve** grupis **Loo** suvand **Arve**.
18. Valige tegumiribal suvand **Vaike vorm**.
19. Väljal **Ridade vaikekogus** valige **Tellitud kogus** ja valige **Ok**.
20. Sisestage **hankija arve päise** kiirkaardi jaotise **Arve ID** jaotisse **Number** väljale väärtus **0001**.
21. Jaotise **Arve kuupäevad** väljal **Arve kuupäev** valige **09.07.2021**.
22. Valige arve postitamiseks toimingupaanilt **Postita**.

### <a name="purchase-services-by-using-a-vendor-invoice"></a>Ostuteenused hankija arve abil

See näite osa näitab, kuidas kasutada hankija arvet teenuste ostmiseks ELi riikidest.

1. Avage **Ostureskontro** > **Arved** > **Arve tööleht**.
2. Valige toimingupaanil nupp **Uus**.
3. Väljal **Nimi** valige **VEND\_EUINV**.
4. Toimingupaanil valige nupp **Alused**.
5. Sisestage väljale **Kuupäev** väärtus **07.09.2021**.
6. Tehke väljal **Konto tüüp** valik **Hankija**.
7. Väljal **Konto** tehke valik **UE Hankija**.
8. Sisestage **Arve kuupäev** väljale **07.09.2021**.
9. Sisestage väljal **Arve** **ITA-0004**.
10. Sisestage väljale **Krediit** väärtus **120000**.
11. Väljal **vastaskonto** **tüüp** valige **Pearaamat**.
12. Väljal **vastaskonto** valige **110130**.
13. Valige väljal **Käibemaksugrupp** suvand **IT\_PUREU**.
14. Valige väljal **Käibemaksugrupp** **22%EL**.
15. Vahekaardil **Väliskaubandus** järgige neid samme:

    1. Sisestage väljal **Kandekood** **1**.
    2. Väljal **Transport** valige väärtus **2 Õhutransport**.
    3. Valige väljal **Kaup** **\[123456\] Teenus**.
    4. Väljal **Riik/regioon** valige **ITA**.
    5. Valige väljalt **Osariik/provints** suvand **LAZ**.
    6. Väljal **Lähte-/sihtkoha maakond** valige **LT**.


16. Tehke toimingupaanil valik **Väljastamine**.
17. Koostage saabujatele Intrastati deklaratsioon.

    1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
    2. Valige tegevuste paanil käsk **Insener**.
    3. Dialoogiboksis **Intrastat (ülekanne)** seadke **hankija arve** valikuks **Jah**.
    4. Tehingute ülekandmiseks valige **OK** ja vaadake Intrastati päevikut.

   ![Intrastati töölehe leht, vahekaart Ülevaade.](media/ita_intrastat_journal_vendor_invoice.png)

18. Vaadake üle **Üldine** ostutellimuse vahekaart.

    ![Intrastati töölehe read ostutellimuse jaoks](media/ita_intrastat_journal_purchase_order_line_details.png)

19. Vaadake üle **Üldine** vahekaart hankija arve jaoks.

    ![Hankija arve jaoks Intrastati töölehe rea üksikasjad](media/ita_intrastat_journal_vendor_invoice_line_details.png)

20. Koostage saabujate jaoks Intrastati aruanne.

    1. Toimingupaanil valige suvandid **Väljund** > **Aruanne**.
    2. Valige **Intrastati aruande** dialoogiboksi jaotise **Kuupäev** väljal **Alguskuupäevaks** **07.01.2021**.
    3. Sisestage väljale **Kuni kuupäevani** väärtus **7.31.2021**.
    4. Seadke jaotises **Ekspordi suvandid** **Loo fail** ja **Loo aruanne** väärtuseks **Jah**.
    5. Väljale **Faili nimi** sisestage **Saabumisfail**.
    6. Väljale **Aruande faili nimi** sisestage **Saabumisaruanne**.
    7. Valige **Suund** väljalt **Saabumised**.
    8. Sisestage väljale **Järjekorranumber** väärtus **123456**.
    9. Valige **OK** Intrastat-aruande ja Intrastat-faili loomiseks ning nende läbivaatamiseks.

    Järgmisel joonisel on toodud Intrastati aruande näide.

    ![Intrastati saabumiste aruanne.](media/ita_intrastat_arrivals_report.png)

    Järgmisel joonisel on toodud Intrastati faili näide.

    ![Intrastati saabumiste fail.](media/ita_intrastat_arrivals_file.png)

## <a name="post-dispatches-for-intrastat"></a>Välja saatmine Intrastati jaoks

### <a name="sell-goods-by-using-a-sales-order"></a>Kaupade müümine müügitellimuse abil

See näite osa näitab, kuidas kasutada müügitellimust kaupade müügiks Euroopa Liidu (EL) riikidesse.

1. Avage **Müügireskontro** > **Tellimused** > **Kõik müügitellimused**.
2. Valige toimingupaanil nupp **Uus**.
3. Valige dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvand **ITCO-000002**.
4. Valige nupp **OK**.
5. Valige **Päise** vaates **Tarneviisi** kiirkaardil **Muu kohaletoimetamise info** jaotises **Väljastamisviis** valige **Veok 1**.
6. Väljal **tarnetingimused** valige **CFR**.
7. **Read** vaates **Müügi tellimuse ridade** vahekaardil **Kaubakoodi** väljal valige väärtuseks **ÜKSUS**.
8. Sisestage väljale **Kogus** väärtus **50**.
9. Valige väljal **Tegevuskoht** väärtus **1**.
10. Valige väljal **Ladu** väärtus **11**.
11. Sisestage väljale **Ühiku hind** väärtus **250**.
12. Kiirkaardil **Rea üksikasjad** vahekaardil **Seadista** jaotises **Käibemaks** väljal **Käibemaksu grupp** valige **22%EL**.
13. Valige toimingupaanil nupp **Salvesta**.
14. Seejärel valige tegevuspaani vahekaardil **Arve** grupis **Loo** **Arve**, et luua arve tellimuse jaoks.
15. Valige dialoogiboksi **Arve sisestamine** kiirkaardi **Parameetrid** jaotises **Parameeter** väljal **Kogus** suvand **Kõik**.
16. Kiirkaardi **Seadistus** väljal **Arve** **kuupäev** valige **07.09.2021**.
17. Valige nupp **OK**.
18. Vaadake Intrastati töölehe ridu töölehel .

    1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
    2. Valige tegevuste paanil käsk **Insener**.
    3. Dialoogiboksis **Intrastat (ülekanne)** seadke **Kliendi arve** valikuks **Jah**.
    4. Tehingute ülekandmiseks valige **OK** ja vaadake Intrastati päevikut. Kreeditarve kanne märgitakse parandusena ja selle arvesumma on negatiivne.

        ![Intrastati töölehe lehekülg](media/ita_intrastat_journal_sales_order.png)

        ![Intrastati töölehe read müügitellimuse jaoks](media/ita_intrastat_journal_sales_order_line_details.png)

### <a name="return-goods-by-using-a-credit-note"></a>Tagasta kaubad kreeditarve abil

See näite osa näitab, kuidas kasutada kreeditarvet Euroopa Liidu (EL) riikidest pärit kaupade (ühikud) tagastamiseks.

1. Avage **Müügireskontro** > **Tellimused** > **Kõik müügitellimused**.
2. Valige toimingupaanil nupp **Uus**.
3. Valige dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvand **ITCO-000002**.
4. Valige nupp **OK**.
5. Valige **Päise** vaates **Tarneviisi** kiirkaardil **Muu kohaletoimetamise info** jaotises **Väljastamisviis** valige **Veok 1**.
6. Väljal **tarnetingimused** valige **CFR**.
7. Kiirkaardi **Väliskaubandus** väljal **Kande kood** valige **2**.
8. Valige **Read** vahekaardil **Müügi tellimuse ridade** väljal **Kaubakoodi** väärtuseks **ÜKSUS**.
9. Sisestage väljale **Kogus** number **-10**.
10. Valige väljal **Tegevuskoht** väärtus **1**.
11. Valige väljal **Ladu** väärtus **11**.
12. Sisestage väljale **Ühiku hind** väärtus **250**.
13. Kiirkaardil **Rea üksikasjad** vahekaardil **Seadista** jaotises **Käibemaks** väljal **Käibemaksu grupp** valige **22%EL**.
14. Valige jaotises **Tagastatud tellimus** väljal **Tagastatud partii ID** partii, mille olete varem loonud.
15. Valige toimingupaanil nupp **Salvesta**.
16. Seejärel valige tegevuspaani vahekaardil **Arve** grupis **Loo** **Arve**, et luua arve tellimuse jaoks.
17. Kiirkaardi **Parameetrid** väljal **Parameeter**, valige **Kogus** väljal **Kõik**.
18. Valige **arve sisestamise** dialoogiakna kiirkaardi **Seadistus** väljal **Arve** **kuupäev** valige **07.09.2021**.
19. Klõpsake sissetuleku sisestamiseks nuppu **OK**.
20. Vaadake Intrastati töölehe ridu töölehel .

    1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
    2. Valige tegevuste paanil käsk **Insener**.
    3. Dialoogiboksis **Intrastat (ülekanne)** seadke **Kliendi arve** valikuks **Jah**.
    4. Tehingute ülekandmiseks valige **OK** ja vaadake Intrastati päevikut. Kreeditarve kanne märgitakse parandusena ja selle arvesumma on negatiivne.

    ![Intrastat-töölehe kreeditarve](media/ita_intrastat_journal_credit_note.png)

    ![Intrastati töölehe rea üksikasjad kreeditarve jaoks](media/ita_intrastat_journal_credit_note_line_details.png)

### <a name="sell-goods-to-san-marino-by-using-a-sales-order"></a>Kaupade müümine San Marinosse müügitellimuse abil

See näite osa näitab, kuidas kasutada müügitellimust kaupade müügiks San Marinosse.

1. Avage **Müügireskontro** > **Tellimused** > **Kõik müügitellimused**.
2. Valige toimingupaanil nupp **Uus**.
3. Valige dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvand **ITCO-000001**.
4. Valige nupp **OK**.
5. Valige **Päise** vaates **Tarneviisi** kiirkaardil **Muu kohaletoimetamise info** jaotises **Väljastamisviis** **Veok 1**.
6. Väljal **tarnetingimused** valige **CFR**.
7. Valige **Read** vahekaardil **Müügi tellimuse ridade** väljal **Kaubakoodi** väärtuseks **ÜKSUS**.
8. Sisestage väljale **Kogus** väärtus **30**.
9. Valige väljal **Tegevuskoht** väärtus **1**.
10. Valige väljal **Ladu** väärtus **11**.
11. Sisestage väljale **Ühiku hind** väärtus **200**.
12. Valige toimingupaanil nupp **Salvesta**.
13. Seejärel valige tegevuspaani vahekaardil **Arve** grupis **Loo** **Arve**, et luua arve tellimuse jaoks.
14. Kiirkaardi **Parameetrid** väljal **Parameeter**, valige **Kogus** väljal **Kõik**.
15. Valige **arve sisestamise** dialoogiakna kiirkaardi **Seadistus** väljal **Arve** **kuupäev** valige **07.09.2021**.
16. Klõpsake sissetuleku sisestamiseks nuppu **OK**.
17. Vaadake Intrastati töölehe ridu töölehel .

    1. Avage **Maks** > **Deklaratsioonid** > **Väliskaubandus** > **Intrastat**.
    2. Valige tegevuste paanil käsk **Insener**.
    3. Dialoogiboksis **Intrastat (ülekanne)** seadke **Kliendi arve** valikuks **Jah**.
    4. Tehingute ülekandmiseks valige **OK** ja vaadake Intrastati päevikut.

   ![Intrastati tööleht San Marino jaoks](media/ita_intrastat_journal_sales_order_san_marino.png)

   ![Intrastati töölehe ridade üksikasjad San Marino jaoks](media/ita_intrastat_journal_sales_order_san_marino_line_details.png)

18. Koostage lähetuste jaoks Intrastati deklaratsioon.

    1. Avage **Maks** &gt; **Deklaratsioonid** &gt; **Väliskaubandus** &gt; **Intrastat**.
    2. Toimingupaanil valige suvandid **Väljund** &gt; **Aruanne**.
    3. Valige **Intrastati aruande** dialoogiboksi jaotise **Kuupäev** väljal **Alguskuupäevaks** **07.01.2021**.
    4. Sisestage väljale **Kuni kuupäevani** väärtus **7.31.2021**.
    5. Seadke jaotises **Ekspordi suvandid** **Loo fail** ja **Loo aruanne** väärtuseks **Jah**.
    6. Väljale **Faili nimi** sisestage **Lähetuste fail**.
    7. Väljale **Aruande faili nimi** sisestage **Lähetuste aruanne**.
    8. Valige **Saadetised** väljalt **Suund**.
    9. Sisestage väljale **Viitenumber** väärtus **98754**.
    10. Valige **OK** Intrastat-aruande ja Intrastat-faili loomiseks ning nende läbivaatamiseks.

        Järgmisel joonisel on toodud Intrastati prinditud aruande näide.

        ![Intrastat-aruanne](media/ita_intrastat_report_for_dispatches.png)

        Järgmisel joonisel on toodud Intrastati prinditud faili näide.

        ![Intrastati fail saatmiseks](media/ita_intrastat_file_for_dispatches.png)
