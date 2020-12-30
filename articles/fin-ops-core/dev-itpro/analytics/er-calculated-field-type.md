---
title: Arvutatud väljatüübi ER-andmeallikate parameetritega kõned
description: See teema annab teavet selle kohta, kuidas kasutada arvutatud väljatüüpi ER-andmeallikate puhul.
author: NickSelin
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3f21b323ddbf653bf8ca8dd1f879a6bdbddcdefc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681252"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a>Arvutatud väljatüübi ER-andmeallikate parameetritega kõned

[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas saate kujundada elektroonilise aruandluse (ER) andmeallikat, kasutades tüüpi **Arvutatud väli**. See andmeallikas võib sisaldada ER-avaldist, mida käivitamisel saab juhtida seda andmeallikat nimetavas sidumises konfigureeritud parameetriargumentide väärtustega. Sellise andmeallika parameeteriseeritud kõnede konfigureerimisega saate ühte andmeallikat mitmes sidumises uuesti kasutada, mis vähendab ER-mudeli vastendustes või ER-vormingutes konfigureeritavate andmeallikate koguarvu. See lihtsustab ka konfigureeritud ER-komponenti, mis vähendab hoolduskulusid ja teiste tarbijate kasutuskulusid.

## <a name="prerequisites"></a>Eeltingimused
Selles teemas näidete lõpuleviimiseks peavad teil olema järgmised juurdepääsuõigused.

- Juurdepääs ühele neist rollidest:

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

- Juurdepääs teenustele Regulatory Configuration Services (RCS), mis on ette valmistatud sama rentniku jaoks, nagu rakendus Finance and Operations, ühe järgmise rolli jaoks.

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

Samuti peate alla laadima ja kohalikult talletama järgmised failid.

| **Sisu**                           | **Faili nimi**                                        |
|---------------------------------------|------------------------------------------------------|
| ER-i andmemudeli konfiguratsiooni näide    | [Mudel parameetritega calls.version.1.xml õppimiseks](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| ER-i metaandmete konfiguratsiooni näide      | [Metaandmed parameetritega calls.version.1.xml õppimiseks](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| ER-i mudelivastenduse konfiguratsiooni näide | [Vastendamine parameetritega calls.version.1.xml õppimiseks](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| ER-vormingu konfiguratsiooni näide        | [Vorming parameetritega calls.version.1.xml õppimiseks](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a>Logige sisse oma RCS-eksemplari.
Selles näites loote konfiguratsiooni näidisettevõtte Litware, Inc. jaoks. Esmalt peate RCS-is täitma teemas [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md) toodud juhised.

1. Valige vaikimisi armatuurlaual **Elektrooniline aruandlus**.
2. Valige **Aruandluse konfiguratsioonid**.
3. Importige allalaaditud konfiguratsioonid RCS-i järgmises järjestuses: andmemudel, metaandmed, mudeli vastendamine, vorming. Täitke järgmised sammud iga ER-konfiguratsiooni puhul:

    1. Valige **Vaheta**.
    2. Valige **Laadi XML-failist**.
    3. Valige käsk **Sirvi** ja valige nõutav ER-i konfiguratsioon XML-vormingus.
    4. Valige nupp **OK.**

## <a name="review-the-provided-er-solution"></a>Vaadake läbi esitatud ER-lahendus

### <a name="review-model-mapping"></a>Mudeli vastendamise läbivaatamine

1. Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.
2. Valige **Vastendamine parameetritega kõnede õppimiseks**.
3. Valige **Kujundaja**.
4. Valige **Kujundaja**.  
   
    See ER-mudeli vastendus on ette nähtud selleks, et teha järgmist:

    - Tooge sisse maksukoodide loetelu (**Maksu** andmeallikas), mis asub tabelis **TaxTable**.
    - Tooge esile maksukannete loetelu (**Kannete** andmeallikas), mis asub tabelis **TaxTranse**.
    
        - Grupeerida sissetoodud kannete loend (**GR** andmeallikas) maksukoodi alusel.
        - Arvutage grupeeritud kanded koondväärtuste järgi maksukoodi kohta järgnevalt.

            - Maksubaasi väärtuste summa.
            - Maksuväärtuste summa.
            - Kohaldatava maksumäära miinimumväärtus.

    Selle konfiguratsiooni mudeli vastendamine rakendab põhiandmete mudelit selle mudeli jaoks loodud ER-vormingute puhul, mida kasutatakse rakenduses Finance and Operations. Selle tulemusena on **Maksu-** ja **Gr-** andmeallikate sisu avatud ER-vormingute, näiteks abstraktsete andmeallikate puhul.

    ![Mudeli vastendamise kujundaja lehekülg, kus kuvatakse maksu-ja Gr-andmeallikad](media/er-calculated-field-type-01.png)

5.  Sulgege leht **Mudelivastenduse koostaja**.
6.  Sulgege leht **Mudelivastendus**.

### <a name="review-format"></a>Läbivaatuse vorming

1. Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.
2. Valige **Vorming parameetritega kõnede õppimiseks**.
3. Valige **Kujundaja**. See ER-vormingu vastendus on ette nähtud selleks, et teha järgmist.

    - Vastavusseviimiseks väljavõtte loomine.
    - Esitada maksuaruandes järgmised maksustamistasemed: regulaarne, vähendatud ja pole.
    - Esitada igal maksustamistasandil mitu üksikasja, millel on igal tasandil erinev arv üksikasju.

    ![Vormingu koostaja leht](media/er-calculated-field-type-02.png)

4. Valige **Vastendamine**.
5. Laiendage üksusi **Mudel**, **Andmed** ja **Kokkuvõte**. 

    Arvutatud väli **Model.Data.Summary.Level** sisaldab avaldist, mis tagastab maksutaseme koodi (**Regulaarne**, **Vähendatud**, **Pole** või **Muu**) tekstiväärtusena mis tahes maksukoodi jaoks, mida saab **Model.Data.Summary** mudelist tuua andmeallika käitusajal.

    ![Vormingu kujundaja leht, kus kuvatakse andmemudeli Mudeli üksikasjad parameetriliste kõnede õppimiseks](media/er-calculated-field-type-03.png)

6. Laiendage üksust **Model**.**Data2**.
7. Laiendage üksust **Model**.**Data2.Summary2**.
   
    **Model**.**Data2. Summary2** andmeallikas on konfigureeritud grupeerima **Model.Data.Summary** andmeallika kande üksikasjad maksustamise taseme alusel (tagastab **Model.Data.Summary.Level** arvutatud väli) ja arvutama kokkuvõtted.

    ![Vormingu kujundaja leht, kus kuvatakse andmeallika Model.Data2.Summary üksikasjad](media/er-calculated-field-type-04.png)

8. Vaadake üle arvutatud väljad **Model**.**Data2. Level1**, **Model**.**Data2. Level2** ja **Model**.**Data2. level3.** Neid arvutatud välju kasutatakse **Model**.**Data2. Summary2** kirjeteloendi filtreerimiseks ja ainult konkreetse maksustamistaset kajastavate kirjete tagastamiseks.
9. Sulgege **Vormingu koostaja** leht.

## <a name="create-a-derived-format"></a>Tuletatud vormingu loomine
Esitatud vormingut saate parandada, kui lisate ühe arvutatud välja, et filtreerida nõutavat maksustamistaset, mitte kasutada olemasolevaid kolme välja: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** ja **Mudel**.**Data2.Level3**. Nõutavat maksustamistaset saab määrata asukohas, kus seda uut arvutatud välja nimetatakse.

1. Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.
2. Valige **Vorming parameetritega kõnede õppimiseks**.
3. Valige **Konfiguratsiooni loomine**.
4. Valige **Tuletage nimest: vormindage parameetritega kõnede õppimiseks, Microsoft**.
5. Sisestage väljale **Nimi** suvand **Vorming parameetriga (kohandatud) kõnede õppimiseks**.
6. Valige **Konfiguratsiooni loomine.**

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a>Parameetrite arvutatud välja konfigureerimine, mis tagastab kirjete loendi

### <a name="start-adding-a-new-calculated-field"></a>Uue arvutatud välja lisamise alustamine

1. Valige **Kujundaja**.
2. Kõigi vorminguüksuste laiendamiseks valige **Laienda/ahenda**.
3. Valige **Vastendamine**.
4. Laiendage üksust **Mudel**.
5. Valige üksus **Model.Data2**.
6. Valige **Lisa**.
7. Valige **Funktsioonid\\Arvutatud väli**.
8. Väljale **Nimi** sisestage **Tasemed**.
9. Valige **Valemi redigeerimine**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Arvutatud välja lisamise parameetri määratlemine

1. Valige **Parameetrid**.
2. Valige suvand **Uus**.
3. Väljale **Nimi** sisestage väärtus **Maksustamise tase**.
4. Valige väljalt **Tüüp** suvand **String**.

    Parameetri argumendi tüübi määramiseks saab kasutada ainult primitiivseid andmetüüpe. Seetõttu ei saa tüüpe **Kirjeloend**, **Kirje** ja **Loetelu** sel eesmärgil kasutada.

    Ühe arvutatud välja jaoks määratud maksimaalne parameetrite arv on 8.

    ![Parameetrite andmeallika loend](media/er-calculated-field-type-05.png)

5. Valige nupp **OK**.

Selle parameetri lisamisega määratlete tingimuse, mis peab olema kasutusel selle arvutatud välja nimetamiseks. Kui nimetate seda arvutatud välja, peate määrama parameetri **Maksustamistase** argumendi väärtusena vorminguga **String**.

   Veenduge, et määratlete parameetrid ainult nende arvutatud väljade jaoks, mis asuvad konteineris ( **kas kirje loend**, **kirje** või **konteiner**).

   Konfigureeritud parameeter on saadaval selle arvutatud välja andmeallikate loendis. Parameetri lisamiseks konfigureeritud avaldisse Saate klõpsata käsku **lisa andmeallikas.**

   ![Andmeallika väljad](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Arvutatud välja lisamise väljendi määratlemine

1. Sisestage väljale **Valem**: 

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level =**
    
2. Valige andmeallikate loendis **Maksustamistaseme** parameeter.
3. Valige **Andmeallika lisamine**.
4. Väljal **Valem** viimistlege avaldis järgmiselt:  

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**

5. Valige käsk **Salvesta**.

    ![Andmeallika välja teave](media/er-calculated-field-type-07.png)

6. Sulgege **Valemikoostaja** leht.

### <a name="finish-adding-a-new-calculated-field"></a>Uue arvutatud välja lisamise alustamine

- Valige nupp **OK**.

Lehel **Vormingu koostaja** nõuab konfigureeritud parameetritega arvutatud väli **Tasemed** argumenti **String**.

![Arvutatud välja tasemete laiendatud loend](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a>Kasutage siduva vormingu elementide jaoks konfigureeritud arvutatud välja.

1. Valige **Model.Data2.Levels**, et valida konfigureeritud arvutatud väli.
2. Valige **Statement.Taxation.Regular** vormingu element.
3. Valige **Seo**.
4. Valige **Jah**, et kinnitada praegu kasutatava andmeallika **Tase1** asendamist uue andmeallikaga **Tasemed** kõigis valitud vorminguelemendi pesastatud vorminguelementides.

    Rakendatud sidumine on loodud parameetrina arvutatud välja kutsena. Vaikimisi kasutatakse seotud vormingu elemendi nime parameetrina arvutatud välja argumendina järgmistel tingimustel:

      - Arvutatud väli on konfigureeritud kasutama ühte parameetrit.
      - Selle parameetri andmetüüp määratletakse **Stringina**.

    Kui seotud vormingu elemendi nimi on tühi, kasutatakse selle elemendi andmeallika nime rakendatud sidumises.

5. Valige **Statement.Taxation.Reduced** vormingu element.
6. Valige **Seo**.
7. Valige **Jah**, et kinnitada praegu kasutatava andmeallika **Tase2** asendamist uue andmeallikaga **Tasemed** kõigis valitud vorminguelemendi pesastatud vorminguelementides.
8. Valige **Statement.Taxation.None** vormingu element.
9. Valige **Seo**.
10. Valige **Jah**, et kinnitada praegu kasutatava andmeallika **Tase3** asendamist uue andmeallikaga **Tasemed** kõigis valitud vorminguelemendi pesastatud vorminguelementides.

   Kui määrate argumendi parameetri arvutatud välja kohta XML-elemendi jaoks, mis tähistab maksustamistaset (nt **Model.Data2.Levels („Vähendatud”)** teksti väärtusena), ei pea te sama tegema pesastatud XML-atribuutide puhul – nende sidumised pärivad automaatselt ematasemel (**Model.Data2.Levels.aggregated.Base**, mitte **Model.Data2.Levels („Vähendatud”).aggregated.Base**).

Parameetritega arvutatud välja korduvaid kõnesid ei toetata.

Saate valida **Redigeeri valemit** ja muuta valitud sidumise parameetritega arvutatud välja vaikimisi rakendatud argumenti. Kui see argument on puudu, võib see põhjustada tõrkeid käitusajal — kasutajat teavitatakse sellisest olukorrast, kui on kehtiv vorming on kontrollitud.

![Kinnitamise hoiatuse teatis](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a>Parameetritega arvutatud välja konfigureerimine kirje tagastamiseks
Kui parameetritega arvutatud väli tagastab kirje, peate elementide vormindamiseks toetama selle kirje üksikute väljade sidumist. Sellisel juhul puudub ülataseme sidumine, mis sisaldab parameetritega arvutatud välja kutsumise argumendi väärtust – see väärtus tuleb määratleda ühe kirje välja sidumisel.

### <a name="start-adding-a-new-calculated-field"></a>Uue arvutatud välja lisamise alustamine

1. Valige üksus **Model.Data2**.
2. Valige **Lisa**.
3. Valige **Funktsioonid\\Arvutatud väli**.
4. Sisestage väljale **Nimi** suvand **LevelRecord**.
5. Valige **Valemi redigeerimine**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Arvutatud välja lisamise parameetri määratlemine

1. Valige **Parameetrid**.
2. Valige suvand **Uus**.
3. Väljale **Nimi** sisestage väärtus **Maksustamise tase**.
4. Valige väljalt **Tüüp** suvand **String**.
5. Valige nupp **OK**.

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Arvutatud välja lisamise väljendi määratlemine

1. Sisestage väljale **Valem** järgmine tekst.  
    
    **FIRSTORNULL(\@.Levels(**

2. Valige **Maksustamistaseme** parameeter.
3. Valige **Andmeallika lisamine**.
4. Väljale **Valem** lisage **„Maksustamistase”))**, mis on sisestatud juhises 1, et lõpetada avaldis:  
    
    **FIRSTORNULL(\@.Levels('Taxation Level'))**

5. Valige käsk **Salvesta**.
6. Sulgege **Valemikoostaja** leht.

### <a name="finish-adding-a-new-calculated-field"></a>Uue arvutatud välja lisamise alustamine

-   Valige nupp **OK**.

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a>Kasutage siduva vormingu elementide jaoks konfigureeritud arvutatud välja.

1. Laiendage välja **Model.Data2.LevelRecord**, et valida konfigureeritud arvutatud väli.
2. Laiendage välja **Model.Data2.aggregated**, et valida konfigureeritud arvutatud välja ümbris.
3. Valige **Model. Data2. LevelRecord.aggregated.Base** väli.
4. Valige **Statement.Taxation.None** vormingu element.
5. Valige **Tühista sidumine**.
6. Valige **Statement.Taxation.None.Base** vormingu element.
7. Valige **Seo**.
8. Valige **Valemi redigeerimine**.
9. Muutke avaldiseks **Model.Data2.LevelRecord („Pole”).aggregated.Base**.

![Värskendatud avaldis](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a>Eemaldage arvutatud väljad, mida ei kasutata

1. Valige **Model.Data2.Level1**.
2. Valige **Kustuta**.
3. Valige **Model.Data2.Level2**.
4. Valige **Kustuta**.
5. Valige **Model.Data2.Level3**.
6. Valige **Kustuta**.
7. Valige käsk **Salvesta**.

  > [!NOTE]
  > Kasutasite uuesti sama arvutatud välja **Model.Data2.Levels** mitu korda vormingu sidumistes. Mitme sarnase välja asemel on palju lihtsam kasutada ja hallata üksikut arvutatud välja.

8. Sulgege **Vormingu koostaja** leht.

## <a name="complete-adjusted-version-of-a-derived-format"></a>Tuletatud vormingu kohandatud versiooni lõpetamine

1. Vahekaardil **Versioonid** valige **Muuda olekut**.
2. Valige **Lõpeta**.

## <a name="export-completed-version-of-a-derived-format"></a>Tuletatud vormingu lõpuleviidud versiooni eksportimine

1. Valige konfiguratsioonipuus  **Vorminda parameetritega kõnede õppimiseks (kohandatud)**.
2. Vahekaardil **Versioonid** valige lõpule viidud versioon 1.1.1.
3. Valige **Exchange**.
4. Valige **Ekspordi XML-failina**.
5. Salvestage allalaaditud konfiguratsioon kohapeal, XML-vormingus.

## <a name="test-er-formats"></a>Katsetage ER-vorminguid 
Saate käivitada algsed ja täiustatud ER-vormingud veendumaks, et konfigureeritud parameetritega arvutatud väljad töötavad õigesti.

### <a name="import-er-configurations"></a>Elektroonilise aruandluse konfiguratsioonide importimine
Läbivaadatud konfiguratsioone saate RCS-ist importida tüübi **RCS** ER-hoidla abil. Kui te juba läbisite teemas toodud juhised [Elektroonilise aruandluse (ER) konfiguratsioonide importimine teenusest Regulatory Configuration Services (RCS)](rcs-download-configurations.md), kasutage konfigureeritud ER-hoidlat, et importida selles teemas varem arutatud konfiguratsioonid oma keskkonda. Muul juhul toimige järgmiselt.

1. Valige ettevõte **DEMF** ja valige vaikearmatuurlaual **Elektrooniline aruandlus**.
2. Valige **Aruandluse konfiguratsioonid**.
3. Importige konfiguratsioonid Microsofti allalaadimiskeskusest järgmises järjestuses: andmemudel, mudelivastendus, vorming. Täitke järgmised sammud iga ER-konfiguratsiooni puhul:

    1. Valige **Vaheta**.
    2. Valige **Laadi XML-failist**.
    3. Valige käsk **Sirvi**, et valida nõutav ER-i konfiguratsioon XML-vormingus.
    4. Valige nupp **OK**.

4. Importige eksporditud RCS-i lõpule viidud versioon 1.1.1 vormingust **Vorminda parameetritega kõnede õppimiseks (kohandatud)**:

    1. Valige **Vaheta**.
    2. Valige **Laadi XML-failist**.
    3. Valige **Sirvi**, et valida kohalikult salvestatud **Vorminda parameetritega kõnede õppimiseks (kohandatud)** fail XML-vormingus.
    4. Valige nupp **OK**.

### <a name="run-er-formats"></a>ER-vormingute käivitamine

1. Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.
2. Valige **Vorming parameetritega kõnede õppimiseks**.
3. Valige kõige ülemisel ribal **Käivita**.
4. Salvestage kohapeal loodud väljund.
5. Valige üksus **Vorminda parameetritega kõnede õppimiseks (kohandatud)**.
6. Valige kõige ülemisel ribal **Käivita**.
7. Salvestage loodud väljund kohapeal. 
8. Võrrelge loodud väljundite sisu.

## <a name="additional-resources"></a>Lisaressursid

- [Valemikoostaja elektroonilises aruandluses (ER)](general-electronic-reporting-formula-designer.md)
- [Saate parandada ER-lahenduste jõudlust, lisades parameeteriseeritud ARVUTATUD VÄLJA andmeallikad](er-calculated-field-ds-performance.md)

