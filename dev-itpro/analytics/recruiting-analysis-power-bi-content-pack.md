---
title: "Värbamine Power BI sisu"
description: "Teema käsitleb Dynamics 365 toiminguteks - värbamine Power BI sisu. Ta selgitab, kuidas on võimalik saada aruandeid, mis on kaasatud sisu pack ja andmemudel ja üksuste, ehitada sisu pakendi kasutatud teavet."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d307733193b388149f83dd420cc7003edcf7749a
ms.lasthandoff: 03/31/2017


---

# <a name="recruiting-power-bi-content"></a>Värbamine Power BI sisu

Teema käsitleb Dynamics 365 toiminguteks - värbamine Power BI sisu. Ta selgitab, kuidas on võimalik saada aruandeid, mis on kaasatud sisu pack ja andmemudel ja üksuste, ehitada sisu pakendi kasutatud teavet.

<a name="accessing-the-content-pack"></a>Juurdepääsu sisu pakendi
--------------------------

Leiate värbamine sisu pakendi jagatud varade teegi in Microsoft Dynamics elutsükli teenused (LCS). Lae sisu pakendi ja ühendada oma Microsoft Dynamics 365 toimingute andmete kohta lisateabe saamiseks vt [Power BI sisu LCS Microsofti ja oma partnerite](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Aruanded, mis on kaasatud sisu pack
Pärast sisu pakendi oma Dynamics 365 toimingute andmed, aruannetest nähtub teie ettevõtte andmeid. Kui te pole varem Microsoft Power BI enne, saab õppida rohkem sellest on [juhindub õppe lehekülg Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Aruanded, mis on kaasatud sisu pack on graafikuid ja tabeleid, mis sisaldavad täiendavat teavet. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                       | Sisu                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Taotleja analüüs           | Taotlejate tööd, taotleja allikad, taotlejate asukoht ja koguarv           |
| Kandidaadi olek             | Taotleja tüüp staatus ja kandidaadi olek                                                    |
| Taotleja demograafia       | Kandidaatide vanuse ja soo ja haridustaseme ja staatuse taotlejate                             |
| Värbamine analüüs          | Neto rendi suhe, Keskmine päeva palgata, halb palkab ja värbamise kulud                    |
| Värbamine projekti analüüs | Värbamisprojektide, avade poolt värbamisprojekti ja taotlejate poolt värbamisprojekti arv |

Saate filtreerida diagrammid ja plaadid aruannete ja diagrammide ja plaadid armatuurlauale kinnitada. Filter ja Power BI pin kohta lisateabe saamiseks vt [loomine ja konfigureerimine armatuurlaua](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Toimingute andmed Dynamics 365 saab asustada värbamine sisu Pack aruanded. Järgmine tabel näitab üksuste sisu pakendi põhines.

| Üksus                          | Sisu                                                         | Suhted ka teiste                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Värbamine\_taotleja           | Hagejad, renditud kandidaadile, neto rendi suhe ja kulud          | Värbamine\_ApplicantName tööle\_firma tööle\_CalendarOffset Recuriting\_kuupäev tööle\_GeographicLocation tööle\_demograafia tööle\_töö, tööle\_meedia tööle\_RecruitmentProject                                |
| Värbamine\_ApplicantName       | Taotleja eesnimi, perekonnanimi ja täisnimi                   | Värbamine\_hageja tööle\_EmployedApplicant tööle\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_CalendarOffset      | Kalendri tasakaalustab viil aruanded                                | Värbamine\_hageja tööle\_EmployedApplicant tööle\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_firma             | Ettevõtete poolt aruannete filtreerimiseks                                   | Värbamine\_hageja tööle\_EmployedApplicant tööle\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_kuupäev                | Päeva, nädala, kuu ja aasta                                   | Värbamine\_hageja tööle\_EmployedApplicant tööle\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_demograafia        | Sünniaeg, soo, etnilise päritolu ja Perekonnaseis         | Värbamine\_hageja tööle\_EmployedApplicant tööle\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_EmployedApplicant   | Taotleja, jõudluse, alguskuupäev ja taotleja tüüp           | Värbamine\_firma tööle\_CalendarOffset tööle\_kuupäev tööle\_GeographicLocation tööle\_ApplicantName tööle\_tööhõive tööle\_tulemuslikkuse tööle\_töö, tööle\_meedia tööle\_RecruitmentProject          |
| Värbamine\_tööhõive          | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                        | Värbamine\_hageja tööle\_EmployedApplicant tööle\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_GeographicLocation  | Linn, maakond, postiindeks kood ja maakond                 | Värbamine\_hageja tööle\_EmployedApplicant tööle\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_töö                 | Funktsiooni, tüüp ja tiitel                                        | Värbamine\_hageja tööle\_EmployedApplicant tööle\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_Media               | Allikas taotlejate                                             | Värbamine\_hageja tööle\_EmployedApplicant tööle\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_täitmise         | Hinnang, kirjeldus ja hinnang mudel                            | Värbamine\_hageja tööle\_EmployedApplicant tööle\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_RecruitmentProject  | Projekti kirjeldus projekti seisukorra ja avad                | Värbamine\_hageja tööle\_EmployedApplicant tööle\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_TerminatedApplicant | Hagejad, põhjus, täitmise ja lõppemise päev | Värbamine\_firma tööle\_CalendarOffset tööle\_kuupäev tööle\_GeographicLocation tööle\_tulemuslikkuse tööle\_demograafia tööle\_tööhõive tööle\_meedia tööle\_RecruitmentProject tööle\_ApplicantName |

Need üksused olid saab luua arvutatud mõõtmeid. Need arvutatakse meetmed seejärel kasutatakse tulemuslikkuse võtmenäitajate (KPI) ja aruanded, mida kasutatakse sisu Pack. Kui soovite kaasata edasiste arvutuste aruanded ja armatuurlaud, saate alla laadida ja muuta LCS Recruiting.pbix faili. See fail on vaikimisi andmemudel, kust luua sisu pakendi. Kui olete teinud muudatusi, saate luua organisatsiooni sisu pakendi ja armatuurlaud, mis sisaldab lisatud teavet.

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



