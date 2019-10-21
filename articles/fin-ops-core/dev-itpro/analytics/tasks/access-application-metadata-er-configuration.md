---
title: Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil
description: Selle teema sammud selgitavad, kuidas Regulatory configuration service (RCS) kasutaja saab kujundada uut elektroonilise aruandluse (ER) mudeli kaardistamise, kasutades metaandmeid Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bfe007995c894d6cc86d07ef2b52da65e32e950
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182734"
---
# <a name="access-application-metadata-by-using-er-configuration"></a>Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil

[!include [task guide banner](../../includes/task-guide-banner.md)]

Järgmised etapid selgitavad, kuidas süsteemi administraatori või elektroonilise aruandluse arendaja rolliga lahenduse Regulatory Configuration Service (RCS) kasutaja saab kavandada uue elektroonilise aruandluse (ER) mudelivastenduse kasutades rakenduse metaandmeid. Rakenduse metaandmetele pääseb juurde elektroonilise aruandluse metaandmete konfiguratsiooni abil, mis sisaldab metaandmete nädiskomplekti juurdepääsuks väliskaubanduse kannetele. Etappide lõpuleviimiseks, peate esmalt läbima ECS-is etapid teemas [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md). Seejärel viige lõpuni etapid teemas [(ER) RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine](prepare-application-metadata-rcs.md).

## <a name="prerequisites"></a>Eeltingimused
1. Avage **Kõik tööruumid** > **Elektrooniline aruandlus**. 
2. Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md) toodud juhised. 

## <a name="import-metadata-configuration"></a>Importige metaandmete konfiguratsioon 
1. Klõpsake valikut **Metaandmete konfiguratsioonid**. 
2. Importige ER metaandmete konfiguratsioon, mis sisaldab metaandmeid, mis on konfigureeritud looma elektroonilisi dokumente väliskaubanduse äritegevuse jaoks. See ER metaandmete konfiguratsioon on eksporditud XML-failina, samal ajal kui viiakse läbi protseduurion [(ER) RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine](prepare-application-metadata-rcs.md) etappe. 
3. Klõpsake valikut **Vahetus**. 
4. Klõpsake valikut **Laadi XML-failist**. 
5. Klõpsake **Sirvi** ja valige fail "Väliskaubanduse metaandmed.xml". 
6. Klõpsake valikut **OK**. 
7. Sulgege leht. 

## <a name="create-data-model-configuration"></a>Looge andmemudeli konfiguratsioon
1. Klõpsake valikut **Aruandluse konfiguratsioonid**. 
2. Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog. 
3. Sisestage väljale **Nimi** "Väliskaubanduse mudel". 
4. Klõpsake **Loo konfiguratsioon**. 
5. Klõpsake valikut **Kujundaja**. 
6. Rippdialoogi avamiseks klõpsake valikut **Uus**. 
7. Sisestage väljale **Nimi** "Juur". 
8. Klõpsake käsku **Lisa**. 
9. Rippdialoogi avamiseks klõpsake valikut **Uus**. 
10. Trükkive "Kanne" väljale **Nimi**. 
11. Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**. 
12. Klõpsake käsku **Lisa**. 
13. Rippdialoogi avamiseks klõpsake valikut **Uus**. 
14. Trükkige "Kaubakood" väljale **Nimi**. 
15. Valige väljalt **Üksuse tüüp** suvand **String**. 
16. Klõpsake käsku **Lisa**. 
17. Rippdialoogi avamiseks klõpsake valikut **Uus**. 
18. Trükkige "Arveldatud summa" väljale **Nimi**. 
19. Väljal **Üksuse tüüp** valige **Tegelik**. 
20. Klõpsake käsku **Lisa**. 
21. Rippdialoogi avamiseks klõpsake valikut **Uus**. 
22. Trükkige "Kuupäev" väljale **Nimi**. 
23. Väljalt **Üksuse tüüp** valige **Kuupäev**. 
24. Klõpsake käsku **Lisa**. 
25. Klõpsake nupul **Juure viide**. 
26. Klõpsake valikut **OK**. 
27. Klõpsake valikut **Salvesta**. 
28. Sulgege leht. 
29. Klõpsake valikut **Muuda olekut**. 
30. Klõpsake valikut **Vii lõpule**. 
31. Klõpsake valikut **OK**. 

## <a name="create-model-mapping-configuration"></a>Looge mudelivastenduse konfiguratsioon 
1. Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog. 
2. Sisestage väljale **Uus** suvand „Mudelivastendus, mis põhineb väliskaubanduse mudeli andmemudelil". 
3. Trükkige "Väliskaubanduse vastendamine" väljale **Nimi**. 
4. Klõpsake **Loo konfiguratsioon**. 
5. Laiendage jaotist **Eeltingimused**. 
6. Klõpsake valikut **Redigeeri**. 
7. Klõpsake valikut **Uus**. 
8. Märkige loendis valitud rida. 
9. Valige väljalt **Eeltingimuse komponendi tüüp** suvand **Konfiguratsioon**. 
10. Valige konfiguratsioon **Väliskaubanduse metaandmed**. 
11. Klõpsake valikut **Salvesta**. 
12. Lisasime viite konfiguratsiooni "Väliskaubanduse metaandmed" versioonile 1. Selle konfiguratsiooni rakenduse metaandmeid pakutakse selle mudeli vastendamise kavandamise ajal. 
13. Sulgege leht. 
14. Klõpsake valikut **Kujundaja**. 
15. Klõpsake valikut **Kujundaja**. 
16. Valige puul väärtus **Dynamics 365 for Operations\Tabeli kirjed**. 
17. Klõpsake suvandil **Juure lisamine**. 
18. Trükkige "Intrastat" väljale **Nimi**. 
19. Valige tabeli kirjed **Intrastat**. 
20. Klõpsake valikut **OK**. 

> [!NOTE]
> Pakutakse ainult kahte tabelit, sest praegu kasutatavale metaandmete komplektile lisati ainult kaks tabelit. 

21. Klõpsake valikult **Seo**. 
22. Laiendage puul valikut **Intrastat** . 
23. Tehke puul valik **Intrastat\AmountMST**. 
24. Laiendage puul valikut **Kanne = Intrastat** . 
25. Tehke puul valik **Kanne = Intrastat\Arveldatud summa**. 
26. Klõpsake valikult **Seo**. 
27. Tehke puul valik **Intrastat\TransDate**. 
28. Tehke puul valik **Kanne = Intrastat\Kuupäev**. 
29. Klõpsake valikult **Seo**. 
30. Laiendage puul valikut **Intrastat\>Seosed**. 
31. Laiendage puul valikut **Intrastat\>Seosed\IntrastatCommodity**. 
32. Tehke puul valik **Intrastat\>Seosed\IntrastatCommodity\Kood**. 
33. Tehke puul valik **Kanne = Intrastat\Kaubakood**. 
34. Klõpsake valikult **Seo**. 
35. Klõpsake valikut **Kinnita**. 

> [!NOTE]
> Oleme andmemudeli elemendid edukalt sidunud nende andmeallikate üksustega, mida on viidatud elektroonilise aruandluse metaandmete konfiguratsiooni rakenduse metaandmetega kirjeldatud. 
36. Klõpsake valikut **Salvesta**. 
37. Sulgege leht. 
38. Sulgege leht. 
39. Vajadusel saate olemasolevat metaandmete kogumit laiendada ja seejärel eksportida ER metaandmete konfiguratsiooni uue lõpule viidud versiooni. Seejärel saate importida selle RCS-i ja värskendada konfigureeritud mudeli vastendamise konfiguratsiooni eeltingimused, mis viitavad imporditud metaandmete konfiguratsiooni uuele versioonile. 

> [!NOTE]
> Selline rakenduste metaandmete info hankimine on ainuke saadaolev meetod kohapeal juurutatud rakendustele (kui kasutatakse kohalikke äriandmeid (LBD) või asutusesisese juurutuse mudelit).
        
