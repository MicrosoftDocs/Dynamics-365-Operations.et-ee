---
title: Rakendusekohaste metaandmete ettevalmistamine RCS-i ja ER-i jaoks
description: Selles teemas selgitatakse, kuidas valmistada ette rakendusespetsiifilisi metaandmeid Regulatiivse konfiguratsiooniteenuse (RCS) ja elektroonilise aruandluse (ER) jaoks.
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c036eab38845db8427c447b27cce0be8048669fd
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248650"
---
# <a name="prepare-application-specific-metadata-for-rcs"></a>Rakendusekohaste metaandmete ettevalmistamine RCS-i jaoks

[!include[banner](../includes/banner.md)]

See teema selgitab järgmiste ülesannete näiteid.

- [RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine](#prepare-application-metadata-that-can-be-used-in-rcs)
- [Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil](#access-application-metadata-by-using-an-er-configuration)
- [Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a>RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine

Järgnev protseduur näitab, kuidas kasutaja, kelle rolliks on kas **Süsteemiadministraator** või **Elektroonilise aruandluse arendaja**, saab luua elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab metaandmeid rakendusele ja mida kasutatakse elektroonilises aruandluses mudelivastenduse konfiguratsioonides Regulatory configuration service (RCS). Selles näites loodud elektroonilise aruandluse mudelivastenduse konfiguratsiooni näidist kasutatakse juurdepääsuks väliskaubanduse kannetele.

Selles näites soovite kasutada RCS-i sellise elektroonilise aruandluse lahenduse kavandamiseks rakendusele, mida kasutatakse väliskaubanduse äritegevuse domeeni teavet sisaldavate elektrooniliste dokumentide loomiseks. ER-i andmemudeli ja nõutavate andmete allikate vahelise vastendamise määramiseks peab teil RCS-is olema ligipääs rakenduse metaandmetele. Seega peate ER-lahenduse projekteerimise protsessi osana konfigureerima uue ER-i metaandmete konfiguratsiooni, mis sisaldab kõiki metaandmeid, mis on valitud äridomeeni ER-aruannete genereerimiseks praegu nõutavad.

> [!NOTE]
> Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Neid etappe saab teha mis tahes ettevõttes.

1. Avage **Organisatsiooni haldamine \> Tööruumid \> Elektrooniline aruandlus**.
2. Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**. Kui te ei näe seda konfiguratsioonipakkujat, viige lõpuni toiming [Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Valige **Metaandmete konfiguratsioonid**.
4. Valige **Konfiguratsiooni loomine**.
5. Dialoogiakna ripploendis sisestage nimi väljale **Nimi**. Selle näite puhul sisestage **Väliskaubanduse metaandmed**.
6. Valige **Konfiguratsiooni loomine**.
7. Valige **Kujundaja**.
8. Valige **Lisa**.

    > [!NOTE]
    > Saate valida kas kogu rakenduse või valitud mudelite või moodulite metaandmed. Mõlemal juhul arvestage, et lisatakse automaatselt järgmised metaandmed: kirjete tabelid, loetelud ja laiendatud andmetüübid (EDT-d). Kui on vaja täiendavaid metaandmete tüüpe, tuleb need lisada käsitsi.

Peate lisama metaandmeid, mis on seotud välikaubanduse kannetega ja valima käsitsi metaandmete üksused.

9. Valige **Andmeallika lisamine \> Tabeli kirjed**.
10. Filter väärtusel **Intrastat** väljal **Nimi**.
11. Valige tabeli kirje **Intrastat**.
12. Valige nupp **OK**.

Peate lisama Intrastati kirjetabeli metaandmete teabe.

13. Tehke puul valik **Tabeli kirjete intrastat \> \>Seosed \> Intrastati kaubaartikkel (Tabeli kirjete EcoResCategory)**.
14. Valige **Lisa metaandmed**.

    > [!NOTE]
    > Valitud kirjetabeli nõutavate seoste metaandmed tuleb lisada käsitsi.

15. Valige **Andmeallika lisamine**.
16. Valige **Loetelu**.
17. Filter väärtusel **IntrastatDirection** väljal **Nimi**.
18. Valige loetelu kirje **IntrastatDirection**.
19. Valige nupp **OK**.
20. Valige käsk **Salvesta**.
21. Sulgege leht.
22. Täitke metaandmete konfiguratsiooni mustandversioon.

    1. Valige **Muuda olekut \> Lõpule viidud**.
    2. Valige nupp **OK**.
    3. Valige lõpule viidud versioon 1.

23. Eksportige metaandmete konfiguratsiooni lõpule viidud versioon rakendusest XML-failina.

    1. Valige **Exchange \> Eksporti XML-failina**.
    2. Valige nupp **OK**.

Teie loodud ER-i metaandmete konfiguratsioon salvestatakse failina **Väliskaubanduse metaandmed.xml**. Nüüd saate selle importida RCS-i, nii et seda saab kasutada väliskaubanduse äritegevuse äridomeeni metaandmete allikana. Selle teabe põhjal saate määratleda vastendamise rakenduse metaandmete ja ER-i andmemudeli vahel.

## <a name="access-application-metadata-by-using-an-er-configuration"></a>Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil

Järgmine protseduur näitab, kuidas RCS-i kasutaja, kelle roll on kas **Süsteemiadministraator** või **Elektroonilise aruandluse arendaja**, saab kavandada uue elektroonilise aruandluse mudeli vastenduse, kasutades rakenduse metaandmeid. Rakenduse metaandmetele pääseb juurde elektroonilise aruandluse metaandmete konfiguratsiooni abil, mis sisaldab metaandmete nädiskomplekti juurdepääsuks väliskaubanduse kannetele.

Enne selle protseduuri lõpule viimist peate esmalt viima lõpuni järgmised protseduurid.

- [Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine](#prepare-application-metadata-that-can-be-used-in-rcs)

1. Avage **Kõik tööruumid \> Elektrooniline aruandlus**.
2. Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**. Kui te ei näe seda konfiguratsioonipakkujat, viige lõpuni toiming [Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md). 
3. Importige ER metaandmete konfiguratsioon, mis sisaldab metaandmeid rakendusele ja mis on konfigureeritud looma elektroonilisi dokumente väliskaubanduse äritegevuse domeenile. Lõite selle elektroonilise aruandluse metaandmete konfiguratsiooni ja eksportisite selle XML-failina varem siin teemas olnud protseduuris [RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine](#prepare-application-metadata-that-can-be-used-in-rcs).

    1. Valige **Metaandmete konfiguratsioonid**.
    2. Valige **Exchange**.
    3. Valige **Laadi XML-failist**.
    4. Sirvige ja valige fail **Väliskaubanduse metaandmed.xml**.
    5. Valige nupp **OK**.
    6. Sulgege leht.

4. Looge andmemudeli konfiguratsioon.

    1. Valige **Aruandluse konfiguratsioonid**.
    2. Valige **Konfiguratsiooni loomine**.
    3. Sisestage ripploendi dialoogiaknasse väljale **Nimi** suvand **Väliskaubanduse mudel**.
    4. Valige **Konfiguratsiooni loomine**.
    5. Valige **Kujundaja**.
    6. Rippdialoogi avamiseks valige **Uus**.

        1. Väljale **Nimi** trükkige **Juur**.
        2. Valige **Lisa**.
    
    7. Rippdialoogi avamiseks valige **Uus**.

        1. Väljale **Nimi** trükkige **Kanne**.
        2. Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.
        3. Valige **Lisa**.
 
    8. Rippdialoogi avamiseks valige **Uus**.

        1. Väljale **Nimi** trükkige **Kaubakood**.
        2. Valige väljalt **Üksuse tüüp** suvand **String**.
        3. Valige **Lisa**.

    9. Rippdialoogi avamiseks valige **Uus**.

        1. Trükkige nimeväljale **Arveldatud summa**.
        2. Väljal **Üksuse tüüp** valige **Tegelik**.
        3. Valige **Lisa**.

    10. Rippdialoogi avamiseks valige **Uus**.

        1. Väljale **Nimi** trükkige **Kuupäev**.
        2. Väljalt **Üksuse tüüp** valige **Kuupäev**.
        3. Valige **Lisa**.
 
    11. Valige **Lisa \> Juure viide**.
    12. Valige nupp **OK**.
    13. Valige käsk **Salvesta**.
    14. Sulgege leht.
    15. Valige **Muuda olekut \> Lõpule viidud**.
    16. Valige nupp **OK**.

5. Looge mudelivastenduse konfiguratsioon.

    1. Valige **Konfiguratsiooni loomine**.
    2. Sisestage ripploendi dialoogiaknasse väljale **Uus** suvand **Mudeli vastendamine väliskaubanduse mudeli andmemudeli põhjal**.
    3. Sisestage väljale **Nimi** suvand **Väliskaubanduse vastendamine**.
    4. Valige **Konfiguratsiooni loomine**.
    5. Valige kiirkaardilt **Eeltingimused** suvand **Redigeeri**.
    6. Valige suvand **Uus**.
    7. Valige väljalt **Eeltingimuse komponendi tüüp** suvand **Konfiguratsioon**.
    8. Valige konfiguratsioon **Väliskaubanduse metaandmed**.
    9. Valige käsk **Salvesta**. Pange tähele et viide lisatakse konfiguratsiooni **Väliskaubanduse metaandmed** versioonile 1. Mudeli vastenduse kavandamise ajal pakutakse rakenduse selle konfiguratsiooni metaandmeid.
    10. Sulgege leht.
    11. Valige **Kujundaja**.
    12. Valige **Kujundaja**.
    13. Valige puul väärtus **Dynamics 365 for Operations \> Tabeli kirjed**.
    14. Valige **Lisa juur**.
    15. Sisestage väljale **Nimi** suvand **Intrastat**.
    16. Valige tabeli kirjed **Intrastat**.
    17. Valige nupp **OK**.

        > [!NOTE]
        > Pakutakse ainult kahte tabelit, sest praegu kasutatavale metaandmete komplektile lisati ainult kaks tabelit.

    18. Valige **Seo**.
    19. Tehke puul valik **Intrastat \> AmountMST**.
    20. Tehke puul valik **Kanne = Intrastat \> Arveldatud summa**.
    21. Valige **Seo**.
    22. Tehke puul valik **Intrastat \> TransDate**.
    23. Tehke puul valik **Kanne = Intrastat \> Kuupäev**.
    24. Valige **Seo**.
    25. Tehke puul valik **Intrastat \> \>Seosed \> IntrastatCommodity \> Kood**.
    26. Tehke puul valik **Kanne = Intrastat \> Kaubakood**.
    27. Valige **Seo**.
    28. Valige **Kinnita**.

        > [!NOTE]
        > Pärast kinnitamise lõpuleviimist olete andmemudeli elemendid edukalt sidunud nende andmeallikate üksustega, mida on viidatud elektroonilise aruandluse metaandmete konfiguratsiooni rakenduse metaandmetega kirjeldatud.

    29. Valige käsk **Salvesta**.

Vajadusel saate laiendada rakenduses olemas olevat metaandmete komplekti. Seejärel saate uue lõpule viidud ER metaandmete konfiguratsiooni versiooni eksportida, importida selle RCS-sse ja värskendada konfigureeritud mudeli vastenduse konfiguratsiooni eeltingimusi viitama uuele imporditud metaandmete konfiguratsiooni versioonile.

> [!NOTE]
> See meetod rakenduse metaandmete kohta info saamiseks on ainuke saadaolev meetod rakendustele, mis arendatakse kohapeal (see tähendab, siis kui rakenduse jaoks kasutatakse kohalikke äriandmeid \[LBD\] või asutusesisese juurutuse mudelit.)

## <a name="access-application-metadata-by-using-connected-applications"></a>Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil

Järgmine protseduur näitab, kuidas RCS-i kasutaja, kelle roll on kas **Süsteemiadministraator** või **Elektroonilise aruandluse arendaja**, saab kavandada uue elektroonilise aruandluse mudeli vastenduse, kasutades rakenduse metaandmeid. Rakenduse metaandmete saab online-juurdepääsu RCS-ga ühendatud rakenduse abil. Väliskaubanduse kannetele juurdepääsuks konfigureeritakse elektroonilise aruandluse mudeli vastenduse näidis.

Selle protseduuri lõpuleviimiseks peate esmalt läbima RCS-is protseduuri [Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md). Kui te ei ole protseduuri [Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil](#access-application-metadata-by-using-an-er-configuration) selles teemas varem lõpule viinud, avage leht [Elektroonilise aruandluse tegevusjuhised rakendusele Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739), et laadida eelnevalt alla järgmised elektroonilise aruandluse konfiguratsioonifailid ja salvestada need kohapeal: **Väliskaubanduse metaandmed.xml**, **Väliskaubanduse mudel.xml** ja **Väliskaubanduse vastendamine.xml**.


### <a name="get-required-er-configurations"></a>Vajalike elektroonilise aruandluse konfiguratsioonide hankimine

Kui olete varem selles teemas protseduuri [Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil](#access-application-metadata-by-using-an-er-configuration) lõpule viinud, on teil praeguses RCS-i eksemplaris juba kõik vajalikud elektroonilise aruandluse konfiguratsioonid (väliskaubanduse metaandmete, mudeli ja vastenduse konfiguratsioonid). Sellisel juhul võite selle protseduuri vahele jätta.

1. Avage **Kõik tööruumid \> Elektrooniline aruandlus**.
2. Valige **Aruandluse konfiguratsioonid**.
3. Laadige konfiguratsioonifailid **Väliskaubanduse metaandmed.xml**, **Väliskaubanduse mudel.xml** ja **Väliskaubanduse vastendamine.xml** korrates neist igaühe korral järgmist etappide jada.

    1. Valige **Exchange**.
    2. Valige **Laadi XML-failist**.
    3. Valige **Sirvi** ja valige fail.
    4. Valige nupp **OK**.

### <a name="register-the-connection-with-the-application"></a>Registreerige ühendus rakendusega

1. Avage **Kõik tööruumid \> Elektrooniline aruandlus**.
2. Valige **Ühendatud rakendused**.
3. Veenduge, et konfigureeritud rakendus on Microsoft Azure põhine ja et see on RCS-i kasutajatele üldiselt juurdepääsetav. Praegusel RCSi kasutajal peab olema juurdepääs konfigureeritud rakendusele, mis registreeritakse selle rakenduse kasutajana rollis, mis annab talle õigused rakenduse mataandmetele juurdepääsuks.
4. Valige suvand **Uus**.
5. Sisestage väljale **Nimi** ühendatud rakenduse nimena suvand **MyConnectedApp**.
6. Määratlege väljal **Rakendus** rakenduse URL.
7. Määratlege väljal **Rentnik** rakenduse pakkuja.
8. Valige käsk **Salvesta**. 
9. Kui kontrollite konfigureeritud rakenduse ühendust, valige lehel **Ühenda kaugrakendusega** link **Valige see valitud kaugrakendusega ühendamiseks**. 
10. Valige **Kontrolli ühendust**, et kontrollida juurdepääsu konfigureeritud rakendusele.
11. Valige suvand **Sule**.

Pärast seda, kui olete selle protseduuri lõpule viinud ja ühenduse kontrollimine on edukas, uuendatakse praeguses ruudustikus konfigureeritud rakenduse versioon ja rentniku andmed.

### <a name="review-the-existing-model-mapping-configuration"></a>Olemasoleva mudelivastenduse üle vaatamine

1. Avage **Kõik tööruumid \> Elektrooniline aruandlus**.
2. Valige **Aruandluse konfiguratsioonid**.
3. valige puul väärtus **Väliskaubanduse mudel \> Väliskaubanduse vastendamine**.
4. Valige kiirkaart **Eeltingimused**.

    > [!NOTE]
    > Praegu viitab see vastendamine metaandmete konfiguratsioonile. Selle konfiguratsiooni rakenduse metaandmeid pakutakse selle mudeli vastendamise kavandamise ajal.

4. Valige **Kujundaja**.
5. Valige **Kujundaja**.
6. Valige puul väärtus **Dynamics 365 for Operations \> Tabeli kirjed**.
7. Valige **Lisa juur**.
8. Sisestage või valige väärtus väljalt **Tabel**.

    > [!NOTE]
    > Praegu viitab see vastendamine metaandmete konfiguratsioonile. Selle konfiguratsiooni rakenduse metaandmeid pakutakse selle mudeli vastendamise kavandamise ajal.

9. Valige **Tühista**.

### <a name="assign-the-connected-application-to-a-model-mapping"></a>Määrake ühendatud rakendus mudelivastendusele

1. Valige suvand **Redigeeri**.
2. Valige väljal **Ühendatud rakenduse väli** rakendus **MyConnectedApp**.

    > [!NOTE]
    > See vastendamine viitab valitud ühendatud rakenduse metaandmetele. Kui vastendamine viitab metaandmete konfiguratsioonile ja ühendatud rakendusele samaaegselt, kasutatakse ühendatud rakenduse metaandmeid.

3. Valige **Kujundaja**.
4. Valige **Kujundaja**.
5. Valige puul väärtus **Dynamics 365 for Operations \> Tabeli kirjed**.
6. Valige **Lisa juur**.
7. Sisestage või valige väärtus väljalt **Tabel**.

    > [!NOTE]
    > Sel hetkel pakutakse rohkem kui kahte rakenduse tabelit, sest see vastendamine kasutab kõiki sellele määratud ühendatud rakenduse metaandmeid.

8. Valige **Tühista**.
9. Valige **Kinnita**.

Olete nüüd andmemudeli elemendid edukalt sidunud nende andmeallikate üksustega, mida on kirjeldatud kasutades sellele vastendusele määratud ühendatud rakenduse metaandmete üksikasju.

Kui peate hindama seda mudeli vastendust, kasutades rakenduse teise versiooni metaandmeid, registreerige teine ühendatud rakendus, määrake see mudeli vastendamiseks ja kinnitage see uute metaandmetega.

## <a name="additional-resources"></a>Lisaressursid

Teise võimalusena saate esitada rakenduse ülesande juhise **RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine** ja ka RCS-i ülesande juhised **Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil** ja **Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil**. Need ülesande juhised saab alla laadida lehelt [Elektroonilise aruandluse ülesande juhised rakendusele Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).
