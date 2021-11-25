---
title: Kuupäeva ja kellaaja väljade ülevaade
description: See teema kirjeldab, mida eeldada, kui kasutate Microsoftis kuupäeva ja kellaaja välju Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 06c783c1e4a2961f1445909ea03d557c0985064e
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728585"
---
# <a name="understand-date-and-time-fields"></a>Kuupäeva ja kellaaja väljade ülevaade

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Kuupäeva ja kellaaja** väljad on Microsofti põhimõisted Dynamics 365 Human Resources. Oluline on mõista, kuidas töötada lehekülgedel, välistes ja välistes allikates kuupäeva ja **·** kellaaja Dataverse andmetega.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Kuupäeva ja kuupäeva ning kellaaja andmetüüpide erinevuse mõistmine

**Kuupäeva- ja** kellaajaväljad sisaldavad ajavööndi teavet, **kuid** kuupäevaväljad seda ei tee. **·** Kuupäevaväljad näitavad sama teavet mis tahes asukohas. Kui sisestate kuupäeva väljale **·** Kuupäev, kirjutatakse andmebaasi sama kuupäev.

Kui andmed on kuvatud väljal Kuupäev ja kellaaeg, korrigeeritakse kuupäeva ja kellaaega vastavalt kasutaja ajavööndile, mis on valitud kasutaja suvandite **·** lehel **·** (Üldine **\> seadistuse \>** kasutajasuvandid). Kuupäeva ja kellaaja teave, mille väljale sisestate, ei pruugi olla sama, mis andmebaasi kirjutatud teave.

[![ Kasutaja suvandite leht.](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>Lehtedel kuupäeva ja kellaaja väljade mõistmine 

Ekraanil kuvatavad **kuupäev ja kellaaeg** ei ole andmebaasi salvestatud andmetega samad, kui kasutaja ajavööndiks ei ole seatud UTC. **Kuupäeva ja kellaaja** väljade andmed talletatakse alati UTC-s.

[![ Töötaja lehekülg UTC.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Kuupäeva ja kellaaja väljadest arusaamine andmebaasis 

Kui andmebaasi **kirjutatakse** kuupäeva ja kellaaja väärtus, talletatakse andmed UTC-ta. Seetõttu saavad kasutajad näha mis tahes kuupäeva ja kellaaja andmeid oma kasutaja valikutes määratletud **·** ajavööndi suhtes.
 
Ülaltoodud näites on algusaeg ajahetk, mitte konkreetne kuupäev. Muutes sisselogitud kasutaja ajavööndit GMT + 12:00 kuni GMT UTC, näitab kirje 05/01/2019 12:00:00 asemel 04/30/2019 12:00:00.

Alltoodud näites 000724 töötaja tööleping muutub aktiivseks samal ajal, vaatamata ajavööndile. Töötaja on aktiivne 04/30/2019 GMT ajavööndis, mis on sama, mis 05/01/2019 GMT + 12:00-ajavöönd. Mõlemad viitavad samale ajale ja mitte kindlale kuupäevale. 

[![ Töötaja lehe GMT](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Kuupäeva ja kellaaja andmed andmehaldusraamistikus, Excelis, ühises andmeteenuses Dataverse ja teenuses Power BI. 

Andmete haldusraamistik (DMF), Exceli lisandmoodul ja aruandlus on kõik loodud suhtlema Dataverse Power BI andmetega vahetult andmebaasi tasemel. Kuna puudub klient, kelle jaoks **kuupäeva ja kellaaja** andmeid kasutaja ajavööndiga korrigeerida, on kõik **kuupäeva ja kellaaja** väärtused UTC-s, mis võib põhjustada mõningaid valesid oletusi, kui sisestate või vaatate andmeid.
 
Kui **kuupäeva ja kellaaja andmed esitatakse** DMF-i, Exceli või exceli kaudu, eeldab andmebaas, et see on Dataverse UTC-s. Kuid kui andmeid vaatavad kasutajad ei sea oma kasutaja ajavööndiks UTC-d, ei kuvata esitatud kuupäeva ja kellaaja väärtus oodatuna ning kasutajad võivad segi **·** ajada. 
 
Sama asi võib juhtuda, kui andmeid eksporditakse vastupidiselt. Eksporditud DMF-üksuse **kuupäeva ja kellaaga** andmed võivad olla erinevad sellest, mis kuvatakse Dynamics clientis. 
 
Kui kasutate välisallikaid, nagu DMF, et vaadata või luua andmeid, pidage meeles, et **kuupäeva ja kellaaja** väärtusi arvestatakse vaikimisi UTC-s, hoolimata kasutaja arvuti või selle praeguse kasutaja ajavööndi sätete ajavööndist. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Erinevates tootepiirkondades kuvatud sama kirje näited 

**Rakenduse Human Resources kasutaja ajavööndiks on seatud UTC**

[![ Utc-le määratud töötaja leht](./media/worker-form3.png)](./media/worker-form3.png)

**Rakenduse Human Resources kasutaja ajavööndiks on seatud GMT +12.00** 

[![ Töötaja lehekülg seatud GMT-le.](./media/worker-form4.png)](./media/worker-form4.png)

**Excel OData kaudu**

[![ Excel Via OData.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMFi ajastamine**

[![ DMFi ajastamine.](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMFi eksport**

[![ DMF Eksport.](./media/DMFExport.png)](./media/DMFExport.png)

**Excel läbi Dataverse**

[![ Excel läbi rakenduse Dataverse.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Vt ka

[Kuupäev ja kellaaeg](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Kasutaja eelistatud ajavöönd](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
