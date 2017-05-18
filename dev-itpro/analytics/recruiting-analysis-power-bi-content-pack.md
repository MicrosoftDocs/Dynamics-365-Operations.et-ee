---
title: "Värbamise Power BI sisu"
description: "See teema kirjeldab Dynamics 365 for Operationsi värbamise mooduli Power BI sisu. See selgitab juurdepääsu sisupaketis sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisupaketi loomiseks kasutati."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 15780e7db5867a2f6a484ceb663e617345c033c2
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="recruiting-power-bi-content"></a>Värbamise Power BI sisu

[!include[banner](../includes/banner.md)]


See teema kirjeldab Dynamics 365 for Operationsi värbamise mooduli Power BI sisu. See selgitab juurdepääsu sisupaketis sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisupaketi loomiseks kasutati.

<a name="accessing-the-content-pack"></a>Juurdepääs sisupaketile
--------------------------

Värbamise sisupaketi leiate teenuste Microsoft Dynamics Lifecycle Services (LCS) ühiste vahendite teegist. Lisateavet sisupaketi allalaadimise ja selle ühendamise kohta Microsoft Dynamics 365 for Operationsi andmetega vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Sisupaketti kuuluvad aruanded
Pärast sisupaketi ühendamist Dynamics 365 for Operationsi andmetega näitavad aruanded teie organisatsiooni andmeid. Kui te pole Microsoft Power BI-d varem kasutanud, saate selle kohta lisateavet jaotisest [Power BI juhendatud õpe](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Sisupaketti kuuluvad aruanded sisaldavad nii lisateavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                       | Sisu                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Kandidaadi analüüs           | Kandidaadid töö järgi, kandidaatide allikad, kandidaadid asukoha järgi ja kandidaatide arv kokku           |
| Kandidaadi olek             | Kandidaadid tüübi ja oleku järgi ning kandidaadi olek                                                    |
| Kandidaadi demograafilised näitajad       | Kandidaadid vanuse ja soo järgi ning kandidaadid haridustaseme ja oleku järgi                             |
| Värbamise analüüs          | Palkamise netosuhe, palkamise keskmine päevade arv, halbade palkamiste protsent ja värbamiskulud                    |
| Värbamisprojekti analüüs | Värbamisprojektide arv, vabad ametikohad värbamisprojekti alusel ja kandidaadid värbamisprojekti alusel |

Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt jaotisest [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Värbamise sisupaketi aruannete täitmiseks kasutatakse Dynamics 365 for Operationsi andmeid. Järgmises tabelis on toodud sisupaketi aluseks olevad üksused.

| Üksus                          | Sisu                                                         | Seosed teiste üksustega                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Värbamine\_Kandidaat           | Kandidaadid, palgatud kandidaadid, palkamise netosuhe ja kulud          | Värbamine\_Värbamise ApplicantName\_Värbamise ettevõte\_Värbamise CalendarOffset\_Värbamise kuupäev\_Värbamise GeographicLocation\_Värbamise demograafilised andmed\_Värbamise töö\_Värbamise meedia\_RecruitmentProject                                |
| Värbamine\_ApplicantName       | Kandidaadi eesnimi, perekonnanimi ja täielik nimi                   | Värbamine\_Värbamise kandidaat\_Värbamise EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_CalendarOffset      | Kalendri tasakaalustused aruannete tükeldamiseks                                | Värbamine\_Värbamise kandidaat\_Värbamise EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_Ettevõte             | Ettevõtted, mille alusel aruandeid filtreerida                                   | Värbamine\_Värbamise kandidaat\_Värbamise EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_Kuupäev                | Päevad, nädalad, kuud ja aastad                                   | Värbamine\_Värbamise kandidaat\_Värbamise EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_Demograafilised andmed        | Sünnikuupäev, sugu, etniline päritolu ja perekonnaseis         | Värbamine\_Värbamise kandidaat\_Värbamise EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_EmployedApplicant   | Kandidaat, tulemused, alguskuupäev ja kandidaadi tüüp           | Värbamine\_Värbamise ettevõte\_Värbamise CalendarOffset\_Värbamise kuupäev\_Värbamise GeographicLocation\_Värbamise ApplicantName\_Värbamise töösuhe\_Värbamise tulemused\_Värbamise töö\_Värbamise meedia\_RecruitmentProject          |
| Värbamine\_Töösuhe          | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                        | Värbamine\_Värbamise kandidaat\_Värbamise EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_GeographicLocation  | Linn, maakond, sihtnumber ja osariik või provints                 | Värbamine\_Värbamise kandidaat\_Värbamise EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_Töö                 | Funktsioon, tüüp ja ametinimetus                                        | Värbamine\_Värbamise kandidaat\_Värbamise EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_Meedia               | Kandidaatide allikas                                             | Värbamine\_Värbamise kandidaat\_Värbamise EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_Tulemused         | Hinnang, kirjeldus ja hinnangumudel                            | Värbamine\_Värbamise kandidaat\_Värbamise EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_RecruitmentProject  | Projekti kirjeldus, projekti olek ja vabad ametikohad                | Värbamine\_Värbamise kandidaat\_Värbamise EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Värbamine\_TerminatedApplicant | Lõpetatud kandidaadid, põhjus, tulemused ja lõpetamise kuupäev | Värbamine\_Värbamise ettevõte\_Värbamise CalendarOffset\_Värbamise kuupäev\_Värbamise GeographicLocation\_Värbamise tulemused\_Värbamise demograafia\_Värbamise töösuhe\_Värbamise meedia\_Värbamise RecruitmentProject\_ApplicantName |

Neid üksusi kasutati arvutatud meetmete loomiseks. Seejärel kasutatakse neid arvutatud meetmeid sisupaketis kasutatavate tulemuslikkuse võtmenäitajate (KPI-d) ja aruannete arvutamiseks. Aruannetesse ja armatuurlauale täiendavate arvutuste lisamiseks võite laadida LCS-ist alla ja muuta faili Recruiting.pbix. See fail on vaikeandmemudel, mida kasutati sisupaketi loomiseks. Kui muudatused on tehtud, saate luua organisatsiooni sisupaketi ja armatuurlaua, mis sisaldab teie lisatud teavet.

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





