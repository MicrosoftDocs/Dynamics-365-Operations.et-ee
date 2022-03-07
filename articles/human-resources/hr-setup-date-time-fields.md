---
title: Kuupäeva ja kellaaja väljade ülevaade
description: See teema selgitab, mida oodata, kui kasutate Microsofti kuupäeva ja kellaaja välju Dynamics 365 Human Resources.
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
ms.openlocfilehash: 7c81155f0c5150af44982f224c8eca2026a78ee7
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060885"
---
# <a name="understand-date-and-time-fields"></a>Kuupäeva ja kellaaja väljade ülevaade

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



**Päev ja aeg** väljad on Microsofti põhikontseptsioon Dynamics 365 Human Resources. On oluline, et mõistaksite, kuidas nendega töötada **Päev ja aeg** andmed lehtedel, sisse Dataverse ja välistest allikatest.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Kuupäeva ja kuupäeva ning kellaaja andmetüüpide erinevuse mõistmine

**Päev ja aeg** väljad sisaldavad ajavööndi teavet, samas **Kuupäev** väljad mitte. **Kuupäev** väljad näitavad sama teavet mis tahes asukohas. Kui sisestate kuupäeva a **Kuupäev** väljale kirjutatakse sama kuupäev andmebaasi.

Kui andmed kuvatakse jaotises a **Päev ja aeg** väljale kohandatakse kuupäeva ja kellaaega vastavalt kasutaja ajavööndile, mis on valitud lehel **Kasutaja valikud** leht (**Levinud \> Seadistamine \> Kasutaja valikud**). Väljale sisestatud kuupäeva ja kellaaja teave ei pruugi olla sama, mis andmebaasi kirjutatakse.

[![Kasutaja valikute leht.](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>Lehtede kuupäeva ja kellaaja väljade mõistmine 

Ekraanil kuvatavad **kuupäev ja kellaaeg** ei ole andmebaasi salvestatud andmetega samad, kui kasutaja ajavööndiks ei ole seatud UTC. **Kuupäeva ja kellaaja** väljade andmed talletatakse alati UTC-s.

[![Töötaja leht UTC.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Kuupäeva ja kellaaja väljadest arusaamine andmebaasis 

Kui **Päev ja aeg** väärtus kirjutatakse andmebaasi, salvestatakse andmed UTC-na. Seetõttu näevad kasutajad mis tahes **Päev ja aeg** kasutaja valikutes määratud ajavööndi andmed.
 
Ülaltoodud näites on algusaeg ajahetk, mitte konkreetne kuupäev. Muutes sisselogitud kasutaja ajavööndit GMT + 12:00 kuni GMT UTC, näitab kirje 05/01/2019 12:00:00 asemel 04/30/2019 12:00:00.

Allolevas näites aktiveerub töötaja 000724 töösuhe olenemata ajavööndist samal ajal. Töötaja on aktiivne 04/30/2019 GMT ajavööndis, mis on sama, mis 05/01/2019 GMT + 12:00-ajavöönd. Mõlemad viitavad samale ajale ja mitte kindlale kuupäevale. 

[![Töötaja leht GMT.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Kuupäeva ja kellaaja andmed andmehaldusraamistikus, Excelis, ühises andmeteenuses Dataverse ja teenuses Power BI. 

Andmehaldusraamistik (DMF), Exceli lisandmoodul,Dataverse, ja Power BI aruandlus on kõik loodud andmetega suhtlemiseks otse andmebaasi tasemel. Kuna puudub klient, kelle jaoks **kuupäeva ja kellaaja** andmeid kasutaja ajavööndiga korrigeerida, on kõik **kuupäeva ja kellaaja** väärtused UTC-s, mis võib põhjustada mõningaid valesid oletusi, kui sisestate või vaatate andmeid.
 
Millal **Päev ja aeg** andmed esitatakse DMF-i, Exceli või Dataverse, eeldab andmebaas, et see on UTC-ajas. Kui aga andmeid vaatavate kasutajate ajavööndiks pole määratud UTC, esitatakse **Päev ja aeg** väärtus ei ilmu ootuspäraselt ja kasutajad võivad segadusse sattuda. 
 
Sama asi võib juhtuda, kui andmeid eksporditakse vastupidiselt. Eksporditud DMF-üksuse **kuupäeva ja kellaaga** andmed võivad olla erinevad sellest, mis kuvatakse Dynamics clientis. 
 
Kui kasutate välisallikaid, nagu DMF, et vaadata või luua andmeid, pidage meeles, et **kuupäeva ja kellaaja** väärtusi arvestatakse vaikimisi UTC-s, hoolimata kasutaja arvuti või selle praeguse kasutaja ajavööndi sätete ajavööndist. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Erinevates tootepiirkondades kuvatud sama kirje näited 

**Rakenduse Human Resources kasutaja ajavööndiks on seatud UTC**

[![Töötaja leht on seatud UTC-le.](./media/worker-form3.png)](./media/worker-form3.png)

**Rakenduse Human Resources kasutaja ajavööndiks on seatud GMT +12.00** 

[![Töötaja leht on seatud GMT-le.](./media/worker-form4.png)](./media/worker-form4.png)

**Excel OData kaudu**

[![Excel Via OData.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMFi ajastamine**

[![DMFi ajastamine.](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMFi eksport**

[![DMF Eksport.](./media/DMFExport.png)](./media/DMFExport.png)

**Excel läbi Dataverse**

[![Excel läbi rakenduse Dataverse.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Vt ka

[Kuupäev ja kellaaeg](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Kasutaja eelistatud ajavöönd](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
