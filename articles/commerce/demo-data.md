---
title: Demoandmete ekraanipaigutused kaasaegses kassas (MPOS) ja pilve kassas
description: See teema sisaldab teavet ekraanipaigutuste kohta, mis on kaasas Dynamics 365 Commercei kassa demoandmetega.
author: josaw1
manager: AnnBe
ms.date: 10/05/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2017-10-05
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: e55db57089c8ea5bd3def25d79d9c65a3165526c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982711"
---
# <a name="demo-data-screen-layouts-in-modern-pos-mpos-and-cloud-pos"></a>Demoandmete ekraanipaigutused kaasaegses kassas (MPOS) ja pilve kassas

[!include [banner](includes/banner.md)]

See teema sisaldab teavet ekraanipaigutuste kohta, mis on kaasas Dynamics 365 Commercei kassa demoandmetega.

## <a name="overview"></a>Ülevaade

Commerce'i demoandmetega kaasas olevad ekraanipaigutuste näidised hõlmavad sisu, mis on optimeeritud mitmesuguste kaubandussegmentide, kaupluse töötajate rollide ja seadmete jaoks. Üks paigutus võib sisaldada eri suuruses paigutusi ja nupupaneelide kombinatsioone, et tagada ühilduvus, kui kaupluse töötajad kasutavad eri seadmeid ja jaamu. Teemas tõstetakse esile paigutuste erinevused, üldine kasutuskogemus ja nendes saadaolevad operatsioonid.

![Seadmeüleste demoandmete paigutused](../commerce/media/demo-screen-layouts-fig-1-1.png)

## <a name="anatomy-of-a-screen-layout-id"></a>Ekraanipaigutuse ID anatoomia

Ekraanipaigutuste leidmiseks avage jaotis **Jaemüük ja kaubandus** \> **Kanali seadistus** \> **Kassa seadistus** \> **Kassa** \> **Ekraanipaigutused**.

![Ekraanipaigutuste leht](../commerce/media/demo-screen-layouts-fig-2-1.png)

Ekraanipaigutuse ID võib sisaldada kuni 10 märki. ID on string, mis koosneb kolme tüüpi teabest järgmises järjekorras.

1. Ettevõte
2. Paigutuse versioon
3. Isik

### <a name="company"></a>Ettevõte

| Kiri | Ettevõte         |
|--------|-----------------|
| A      | Adventure Works |
| F      | Fabrikam        |
| C      | Contoso         |

### <a name="layout-version"></a>Paigutuse versioon

| Versiooni number | Kirjeldus                                                                                |
|----------------|--------------------------------------------------------------------------------------------|
| 3              | Põhiversioon, mis toetab mitut ekraanisuurust eri seadmete ja kuvasuhete jaoks |
| 3.1            | Põhiversioon, mis hõlmab paneeli **Soovitatud tooted** täiendavat tuge        |
| 4              | Laiendatud Fabrikami värskendatud paigutuse laiendatud versioon                                  |

### <a name="persona"></a>Isik

| Lühend | Isik       | Sisu |
|--------------|---------------|----------|
| CSH          | Kassapidaja       | Kassapidaja paigutused hõlmavad kõiki kannetega seotud toiminguid, nagu klienditellimused, tagastused, allahindlused, tühistamised ja kinkekaardid. Paigutused hõlmavad ka igapäevaseid varude halduse toiminguid, nagu hinnakontrollid, varude otsingud ja laoinventuurid. Samuti on saadaval üldised vahetuste haldamise funktsioonid, nagu algussummad, vahetuste peatamine ja kell. |
| MGR          | Kaupluse juhataja | Kaupluse juhataja paigutused hõlmavad kõiki kannetega seotud operatsioone, mis on saadaval kassapidaja paigutustes, ent sisaldavad ka maksude tühistamise valikuid. Paigutused hõlmavad ka igapäevaseid varude halduse toiminguid, nagu hinnakontrollid, varude otsingud ja laoinventuurid. Vahetuste haldus võimaldab vahetusi alustada, peatada ja sulgeda. Peale selle hõlmavad paigutused sahtliga seotud operatsioone kirjete, eemaldamiste, päevakassade ning seifi ja panka viidava raha haldamiseks. Peale kõige muu annavad paigutused juurdepääsu toimivusaruannetele ja võimaldavad printida X- ja Z-aruandeid. |
| STK          | Kaupade väljapanija   | Kaupade väljapanija paigutused on optimeeritud varude halduse jaoks. Need hõlmavad juurdepääsu igapäevastele toimingutele, nagu hinnakontrollid, varude otsingud, komplekteerimine ja vastuvõtmine, laoinventuurid ja komplektide osadeks jaotamine. Paigutused hõlmavad ka peamisi vahetustega seotud operatsioone, nagu kell ja vahetuste peatamine. Kuigi need paigutused on mõeldud peamiselt kontoris tehtavate toimingute jaoks, on kaupade väljapanijatel kandeekraanidel samad toimingud mis kassapidajatel. |

### <a name="example-layout"></a>Näidispaigutus

Siin on ettevõtte Fabrikam ekraanipaigutuse ID, paigutuse 4. versiooni ja kaupluse juhataja isiku näide.

F4MGR

Järgmisel joonisel on Fabrikami kaupluse juhataja tervitusekraani näide.

![Fabrikami kaupluse juhataja tervitusekraan](../commerce/media/demo-screen-layouts-fig-2-2.png)

## <a name="layout-sizes"></a>Paigutuse suurused

### <a name="full-vs-compact-layouts"></a>Täielikud vs. kompaktsed paigutused

Ekraanipaigutus võib sisaldada ka nii täis- kui ka kompaktseadmete konfiguratsioone. Seetõttu saab kasutaja ühele ekraanipaigutusele, mis töötab kaupluses mitmesuguste suuruse ja vormi tegurite lõikes.

- **Modern POS – täispaigutus**: täispaigutused sobivad tavaliselt kõige paremini suurematele ekraanidele, näiteks lauaarvuti kuvaritele või tahvelarvutitele. Kasutajad saavad valida paigutuses saadaolevaid kasutajaliidese elemente, määrata elementide suuruse ja paigutuse ning konfigureerida nende üksikasjalikke atribuute. Täispaigutused toetavad nii vertikaal- kui ka horisontaalkonfiguratsioone.
- **Modern POS – kompaktne**: kompaktsed paigutused sobivad tavaliselt kõige paremini telefonidele või väikestele tahvelarvutitele. Kompaktsete seadmete puhul on kujundusvõimalused piiratud. Kasutajad saavad konfigureerida sissetuleku ja kogusummade paani veerge ja välju.

### <a name="screen-resolutions-that-are-provided"></a>Saadaolevad ekraani eraldusvõimed

Järgmine tabel näitab paigutuste suurusi, mis on saadaval ekraani tüüpiliste eraldusvõimete korral.

| Paigutuse tüüp | Lahendus | Kuvasuhe | Kasutatav kuva          |
|-------------|------------|--------------|-------------------------|
| Tihenda\*   | 480 × 853  | 16 : 9         | Telefonid                  |
| Täielik        | 1024 × 768 | 4 : 3          | Tahvelarvutid                 |
| Täielik\*      | 1280 × 720 | 16 : 9         | Tahvelarvutid                 |
| Täielik        | 1366 × 768 | 16 : 9         | Tahvelarvutid, suuremad ekraanid |
| Täielik        | 1440 × 960 | 3 : 2          | Tahvelarvutid, suuremad ekraanid |
| Täielik\*      | 1536 × 864 | 16 : 9         | Tahvelarvutid, suuremad ekraanid |

\*Need täiendavad suurused on saadaval ainult Adventure Worksi ja Fabrikami paigutustes.

> [!TIP]
> POS valib paigutuste suurused automaatselt olenevalt sellest, milline suurus on lähim rakenduse praeguse akna eraldusvõimele. Praegu kasutatava ekraanipaigutuse ID ja paigutuse eraldusvõime leidmiseks avage kaasaegses kassaas või Retail'i pilve kassas leht **Sätted** ja vaadake jaotist **Seansi teave**. Samuti näete praeguse rakenduse või brauseripaneeli akna tegelikku eraldusvõimet. Pärast selle teabe hankimist võite jaotises Retaili paigutuse sisu allika leidmiseks avada jaotise **Kanali seadistus** \> **Kassa seadistus** \> **Kassa** \> **Ekraanipaigutused**.

![Ekraanipaigutused ja paigutuste eraldusvõimed/suurused Commerce'is ja kassas](../commerce/media/demo-screen-layouts-fig-3-1.png)

## <a name="companies-and-brands"></a>Ettevõtted ja kaubamärgid

Iga fiktiivne ettevõte sihib eri jaemüügisegmenti ja hõlmab tootekatalooge, mis on häälestatud ettevõtte turu jaoks. Igal ettevõtte toodetel on kordumatu visuaalne kaubamärk. Kaubamärgi elemendid hõlmavad rõhuvärvi, tumedat või heledat teemat ja kaasnevaid fotosid, mis loovad realistliku kogemuse.

### <a name="company-segment-and-visual-characteristics"></a>Ettevõtte segment ja visuaalsed omadused

| Ettevõte         | Koht | Segment        | Rõhuvärv | Kujundus |
|-----------------|----------|----------------|--------|-------|
| Adventure Works | Seattle  | Sporditarbed | Sinine   | Tume  |
| Fabrikam        | San Francisco  | Mood        | Roheline  | Hele |
| Contoso         | Boston   | Elektroonika    | Punane    | Tume  |

> [!NOTE]
> Adventure Works ja Fabrikam on kaks juhtivat kaubamärki. Contoso on saadaval, ent see ei hõlma kõiki paigutusi.

Järgmised joonised hõlmavad kolme fiktiivse ettevõtte tervituslehe ja kandelehe näiteid.

### <a name="adventure-works"></a>Adventure Works

![Adventure Worksi tervituslehe demoandmed](../commerce/media/demo-screen-layouts-fig-4-1a.png)

![Adventure Worksi kandelehe demoandmed](../commerce/media/demo-screen-layouts-fig-4-1b.png)

### <a name="fabrikam"></a>Fabrikam

![Fabrikami tervituslehe demoandmed](../commerce/media/demo-screen-layouts-fig-4-2a.png)

![Fabrikami kandelehe demoandmed](../commerce/media/demo-screen-layouts-fig-4-2b.png)

### <a name="contoso"></a>Contoso

![Contoso demoandmete paigutused](../commerce/media/demo-screen-layouts-fig-4-3.png)

## <a name="user-sign-in-matrix"></a>Kasutaja sisselogimise maatriks

Ekraanipaigutuste jaoks on lisatud kasutajad. Järgmise tabeli abil peaksite saama juurdepääsu kõikidele ekraanidele. Kasutage lihtsalt sisselogimiseks sobivat operaatori ID-d.

| Ettevõte         | Ekraani paigutuse ID | Isik       | Operaatori ID-d           |
|-----------------|------------------|---------------|------------------------|
| Adventure Works | A3MGR            | Kaupluse juhataja | 000154, 000137, 000073 |
| Adventure Works | A3CSH            | Kassapidaja       | 000150, 000175, 000165 |
| Adventure Works | A3STK            | Kaupade väljapanija   | 000155, 000181, 000152 |
| Fabrikam        | F4MGR            | Kaupluse juhataja | 000160, 000713         |
| Fabrikam        | F3CSH            | Kassapidaja       | 000161, 000113, 000114 |
| Fabrikam        | F3STK            | Kaupade väljapanija   | 000164, 000112, 000123 |
| Contoso         | C3MGR            | Kaupluse juhataja | 000100, 000111         |
| Contoso         | C3CSH            | Kassapidaja       | 000110, 000120         |
| Contoso         | Pole kohaldatav   | Kaupade väljapanija   | Pole kohaldatav         |

> [!TIP]
> Parimate tulemuste saavutamiseks aktiveerige kaupluse asukohas kassaaparaat ja seejärel valige sisselogimiseks kasutatava isiku ettevõte. See aitab tagada, et visuaalne profiil ja kaubamärgi pildid oleksid keskkonnas järjepidevad. Näiteks kui soovite näha Fabrikami kassapidaja paigutust, tuleb teil aktiveerida kassaaparaat Houstoni kaupluses.

<!-- Hiding until the content page is available on CustomerSource -->

<!-- ## Reference icons and images -->

<!-- The screen layouts, button grids, and visual profiles were created using images and icons that can be found in **Retail and Commerce \> Channel setup \> POS setup \> POS \> Images**. -->

<!-- ![Images in Dynamics 365 Commerce](../commerce/media/demo-screen-layouts-fig-5-1.png) -->

<!-- Use the [POS Icon and Image Mapping](../commerce/media/POS_Icon_and_Image_Mapping.xlsx) reference spreadsheet to locate operation icons, reference photos, swap logos, or provide new images of your own that can be referenced in custom designs. -->

<!-- END HIDDEN CONTENT -->
