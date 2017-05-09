---
title: "Eelarvestamise kodulehekülg"
description: "Teema annab ülevaate eelarvestamise funktsionaalsuse komponentidest, eelarvestamise tööriistadest ja aruandluse võimalustest Microsoft Dynamics 365 for Operationsis."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: index-page
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: dd17842365e357ecb5cb6034ed8878fcd60be5fc
ms.openlocfilehash: aacce0449c9490c4ab66cacb9945ed64fa40de34
ms.contentlocale: et-ee
ms.lasthandoff: 04/26/2017


---

# <a name="budgeting-home-page"></a>Eelarvestamise kodulehekülg

[!include[banner](../includes/banner.md)]


Teema annab ülevaate eelarvestamise funktsionaalsuse komponentidest, eelarvestamise tööriistadest ja aruandluse võimalustest Microsoft Dynamics 365 for Operationsis. 

<a name="components-of-budgeting-functionality"></a>Eelarve koostamise funktsiooni komponendid
-------------------------------------

Ressursi planeerimistsükkel ettevõttele koosneb tavaliselt plaanimisest, eelarve koostamisest ja tegevuste prognoosimisest.
[![Eelarve koostamise funktsiooni komponendid](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg) Nii pikaajaliste strateegilise plaanimise kui ka aastaeelarve plaanimise protsessi toetatakse eelarve plaanimise dokumendi kaudu. Eelarveplaani dokumendid on tugevasti Microsoft Exceliga integreeritud. Kasutajad saavad konfigureerida piiramatu arvu valuuta- ja kvantitatiivseid stsenaariume ning määratleda eelarve organisatsiooni nii hierarhia ülalt-alla kui ka alt-üles eelarvestamise meetodite toetamiseks. Pärast seda, kui eelarve on Microsoft Dynamics 365 for Operationsis loodud ja kinnitatud, teisendatakse eelarveplaan eelarveregistri kirjeks. Eelarveregistri kirjed pakuvad vahendeid eelarve haldamiseks ja summade jälgitavana hoidmiseks eelarvekoodide kaudu. Eelarve registrikirjed võimaldavad parandada algseid eelarveid, teha ülekandeid ja eelmise aasta eelarvesummasid edasi kanda. Kehtestatud eelarve põhjal saab ettevõte lubada eelarve juhtimise. Kontrolli tase oleneb organisatsiooni kultuurist ja küpsusastmest. Madala küpsusastmega organisatsioonid võivad jätta eelarve muutmata ja olla rohkem reaktiivsed kui proaktiivsed, kui eelarve ootustele ei vasta. Teised organisatsioonid võivad lubada eelarve juhtimise poliitikaid, mis takistavad kasutajatel ostmist, kui eelarvesummasid pole. Ja lõpuks võivad väga küpsed organisatsioonid kehtestada organisatsiooni kultuuri, kus töötajaid koolitatakse organisatsiooni eesmärkide teemal, ja järgida neid eesmärke poliitikate kaudu, nagu „Kaaluge reisimise asemel veebikoosolekut”. Dynamics 365 for Operations sisaldab eelarve juhtimise raamistikku, mis võimaldab ettevõtte juhtkonnal valida ranged juhtimismeetodid (mis takistavad sisestamise, kui eelarvet ületatakse) või leebed juhtimismeetodid (kus kasutajatele edastatakse hoiatus, et nad ületavad olemasolevaid eelarvevahendeid, kuid nad saavad ise otsustada, kuidas jätkata). Lõpuks saab kasutada jooksvaid prognoose. Jooksev prognoos on eelarve regulaarne võrdlemine tegelike näitajatega ja seda kasutatakse määratlemiseks, kui hästi ettevõttel eelarvega võrreldes läheb. Jooksvat prognoosi kasutatakse ka suundumuste tuvastamiseks. Microsoft Dynamics 365 for Operationsis toetatakse jooksvaid prognoose eelarveplaani dokumendi kaudu algse plaanimise tegevustena. Jooksvaid prognoose saab teha paralleelselt tulevase eelarvetsükli plaanimisega.

-   [Põhiline eelarvestamine: ülevaade ja konfigureerimine](basic-budgeting-overview-configuration.md)
-   [Eelarve juhtimine: ülevaade ja konfigureerimine](budget-control-overview-configuration.md)
-   [Eelarve planeerimine: ülevaade ja konfigureerimine](budget-planning-overview-configuration.md)
-   [Ametikoha prognoosimine](position-forecasting.md)
-   [Eelarve planeerimise põhjendusdokumendid](budget-planning-justification-docs.md)
-   [Microsoft Exceli mallid eelarve plaanimise jaoks](budget-planning-excel-templates.md)

## <a name="budgeting-tools-in-dynamics-365-for-operations"></a>Eelarvestustööriistad Dynamics 365 for Operationsis
[![Eelarvestuse tööriistad](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

Kogu Dynamics 365 for Operationsis on olemas täiendavad plaanimis- ja eelarve koostamise võimalused ning need on integreeritud pearaamatu eelarvetega.

-   **Tööjõu eelarved** – tööjõu eelarvete koostamine hõlmab üksikasjaliku eelarvekulu komponendi plaanimist ametikohtadele, tasugruppidele jne.
-   **Põhivara eelarved** – tuginedes põhivara teabele, saate arvutada plaanitud kulumit ja kajastada muid põhivaraga seotud plaanitud kandeid.
-   **Projekti eelarved** – projektimoodulis saate luua üksikasjalikke projekti prognoose. Projekti eelarved sisaldavad üksikasju plaanitud tundide, kulude, tasude ja kaupade kohta.
-   **Nõudluse prognoos** – saate hinnata tulevast varude nõudlust ja koostada varasemate kandeandmete põhjal nõudluse prognoose.

Teavet plaanimisandmete eelarveplaanidesse toomise kohta muudest moodulitest vt jaotist [Eelarve plaanimise integreerimine muude moodulitega](budget-planning-integration-other-modules.md).

## <a name="user-interface-and-reporting-capabilities"></a>Kasutajaliides ja aruandluse võimalused
Microsoft Dynamics 365 for Operationsis saavad kasutajad koostada eelarveplaane kas otse Microsoft Dynamics 365 for Operationsi kliendist (kasutades seadistatavat eelarvedokumendi lehte) või Exceli kaudu. Excel pakub mitut lisavõimalust. Näiteks saab eelarveplaani allikana kasutada väliseid andmeid, teha kohandatud arvutusi ning kasutada Microsofti liigendtabeleid ja diagramme. Enamikku eelarve plaanimise protsessi muutujatest saab konfigureerida. Näiteks saate määratleda, kes eelarve koostab, mille kohta eelarve koostatakse ja milline on protsess. Kuigi saate kasutada eelarve plaanimiseks Excelit, jääb Dynamics 365 for Operations ainsaks tõe allikaks, mis aitab eelarve juhtimise probleeme vältida. Algsete eelarve koostamise andmete toomiseks eelarveplaani saab kasutada perioodilisi protsesse. Aruandluse jaoks pakub Dynamics 365 for Operations standardsete päringulehtede kogumit, mis võimaldab eelarvestamise andmeid vaadata ja analüüsida. Eelarveplaani andmetele pääseb juurde Management Reporteri kaudu ja eraldi eelarveplaani stsenaariume saab kuvada Management Reporteri aruandes veergudena.







