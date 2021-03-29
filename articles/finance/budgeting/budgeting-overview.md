---
title: Eelarvestamise avaleht
description: Teema annab ülevaate eelarvestamise funktsionaalsuse komponentidest, eelarvestamise tööriistadest ja aruandluse võimalustest teenuses Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 08/09/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 106043
ms.assetid: 702f692e-ad1c-4798-8d3e-c3cf8591d3fa
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5222df8ffd3e0cb8759f7c094e5efde97d2ede0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210261"
---
# <a name="budgeting-home-page"></a>Eelarvestamise avaleht

[!include [banner](../includes/banner.md)]

Teema annab ülevaate eelarvestamise funktsionaalsuse komponentidest, eelarvestamise tööriistadest ja aruandluse võimalustest. 

<a name="components-of-budgeting-functionality"></a>Eelarvestamise funktsiooni komponendid
-------------------------------------

Ettevõtte ressursi planeerimistsükkel koosneb tavaliselt plaanimisest, eelarvestamisest ja tegevuste prognoosimisest.

[![Eelarve koostamise funktsiooni komponendid](./media/budgeting-functionality-components.jpg)](./media/budgeting-functionality-components.jpg)

Pikaajalist strateegilist plaanimist ja aastase eelarve plaanimist toetatakse eelarveplaani dokumendi kaudu. Eelarveplaani dokumendid on tugevasti Microsoft Exceliga integreeritud. Kasutajad saavad konfigureerida piiramatu arvu valuuta- ja kvantitatiivseid stsenaariume ning määratleda eelarvestamise organisatsiooni hierarhia nii ülalt-alla kui ka alt-üles eelarvestamise meetodite toetamiseks. Pärast seda, kui eelarve on rakenduses loodud ja kinnitatud, teisendatakse eelarveplaan eelarveregistri kirjeks. Eelarveregistri kirjed pakuvad vahendeid eelarve haldamiseks ja summade jälgitavana hoidmiseks eelarvekoodide kaudu. Eelarve registrikirjed võimaldavad parandada algseid eelarveid, teha ülekandeid ja eelmise aasta eelarvesummasid edasi kanda. Kehtestatud eelarve põhjal saab ettevõte lubada eelarve juhtimise. Kontrolli tase oleneb organisatsiooni kultuurist ja küpsusastmest. Madala küpsusastmega organisatsioonid võivad jätta eelarve muutmata ja olla rohkem reaktiivsed kui proaktiivsed, kui eelarve ootustele ei vasta. Teised organisatsioonid võivad lubada eelarve juhtimise poliitikaid, mis takistavad kasutajatel ostmist, kui eelarvesummasid pole.

Lõpetuseks võivad väga küpsed organisatsioonid kehtestada organisatsiooni kultuuri, kus töötajaid koolitatakse organisatsiooni eesmärkide teemal, ja nad järgivad neid eesmärke poliitikate kaudu, nagu „Kaaluge reisimise asemel veebikoosolekut”. Rakendus sisaldab eelarve juhtimise raamistikku, mis võimaldab ettevõtte juhtkonnal valida ranged juhtimismeetodid (mis takistavad sisestamisi, mis ületataks eelarvet) või leebed juhtimismeetodid (kus kasutajatele edastatakse hoiatus, et nad ületavad olemasolevaid eelarvevahendeid, kuid nad saavad ise otsustada, kuidas jätkata). Lõpuks saab kasutada jooksvaid prognoose. Jooksev prognoos on eelarve regulaarne võrdlemine tegelike näitajatega ja seda kasutatakse määratlemiseks, kui hästi ettevõttel eelarvega võrreldes läheb. Jooksvat prognoosi kasutatakse ka suundumuste tuvastamiseks. Rakenduses Finance and Operations toetatakse jooksvaid prognoose eelarveplaani dokumendi kaudu algse plaanimise tegevustena. Jooksvaid prognoose saab teha paralleelselt tulevase eelarvetsükli plaanimisega.

-   [Eelarve koostamise ülevaade](basic-budgeting-overview-configuration.md)
-   [Eelarve juhtimise ülevaade](budget-control-overview-configuration.md)
-   [Eelarve plaanimise ülevaade](budget-planning-overview-configuration.md)
-   [Ametikoha prognoosimine](position-forecasting.md)
-   [Eelarve planeerimise põhjendusdokumendid](budget-planning-justification-docs.md)
-   [Eelarve planeerimise mallid Exceli jaoks](budget-planning-excel-templates.md)

## <a name="budgeting-tools"></a>Eelarvestamise tööriistad
[![Eelarvestamise tööriistad](./media/budgeting-tools.jpg)](./media/budgeting-tools.jpg) 

Saadaval on täiendavad plaanimis- ja eelarve koostamise võimalused ning need on integreeritud pearaamatu eelarvetega.

-   **Tööjõu eelarved** – tööjõu eelarvestamine hõlmab üksikasjaliku eelarvekulu komponendi plaanimist ametikohtadele, tasugruppidele jne.
-   **Põhivara eelarved** – tuginedes põhivara teabele, saate arvutada plaanitud kulumit ja kajastada muid põhivaraga seotud plaanitud kandeid.
-   **Projekti eelarved** – projektimoodulis saate luua üksikasjalikke projekti prognoose. Projekti prognoosid sisaldavad üksikasju plaanitud tundide, kulude, tasude ja kaupade kohta.
-   **Nõudluse prognoos** – saate hinnata tulevast varude nõudlust ja koostada varasemate kandeandmete põhjal nõudluse prognoose.

Teavet selle kohta, kuidas tuua plaanimisandmeid muudest moodulitest eelarveplaanidesse vt jaotisest [Eelarve plaanimise integreerimine muude moodulitega](budget-planning-integration-other-modules.md).

## <a name="user-interface-and-reporting-capabilities"></a>Kasutajaliides ja aruandluse võimalused
Kasutajad saavad koostada eelarveplaane kas otse kliendis (kasutades konfigureeritavat eelarveplaani dokumendi lehte) või Exceli kaudu. Excel pakub mitut lisavõimalust. Näiteks saab eelarveplaani allikana kasutada väliseid andmeid, teha kohandatud arvutusi ning kasutada Microsofti liigendtabeleid ja diagramme. Enamikku eelarve plaanimise protsessi muutujatest saab konfigureerida. 

Näiteks saate määratleda, kes eelarve koostab, mille kohta eelarve koostatakse ja milline on protsess. Kuigi saate kasutada eelarve plaanimiseks Excelit, jääb rakendus ainsaks tõe allikaks, mis aitab eelarve juhtimise probleeme vältida. Algsete eelarvestamise andmete toomiseks eelarveplaani saab kasutada perioodilisi protsesse. Aruandluse jaoks pakutakse rakenduses standardsete päringulehtede kogumit, mis võimaldab eelarveandmeid vaadata ja analüüsida. Eelarveplaani andmetele pääseb juurde rakenduse [Financial Reporting](../general-ledger/financial-reporting-getting-started.md) kaudu ning eraldi eelarveplaani stsenaariume saab kuvada finantsaruandes veergudena.








[!INCLUDE[footer-include](../../includes/footer-banner.md)]