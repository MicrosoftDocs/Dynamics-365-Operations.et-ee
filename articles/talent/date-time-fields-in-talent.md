---
title: Kuupäeva ja kellaajaga töötamine rakenduses Microsoft Dynamics 365 Talent
description: Saate teada, mida oodata kuupäeva ja kellaaja väljade kasutamisel rakenduses Microsoft Dynamics 365 Talent. Saate selgust, mida oodata kuupäeva ja kellaaja andmetega suhtlemisel rakenduses Talent, välises allikas või teenuses Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a1d1a47bfe6bd58b1e1a0d4d46c2133f3bf48ad
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2007963"
---
# <a name="date-and-time-fields-in-talent"></a>Kuupäeva ja kellaaja väljad Talentis

[!include [banner](includes/banner.md)]

**Kuupäeva ja kellaaja** väljad on põhimõiste rakenduses Dynamics 365 Talent. Oluline on mõista, kuidas töötada **kuupäeva ja kellaaja** andmetega rakenduse Dynamics 365 vormil, ühistes andmeteenustes Common Data Service ja välistes allikates.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Kuupäeva ja kuupäeva ning kellaaja andmetüüpide erinevuse mõistmine

**Kuupäeva ja kellaaja** väljad sisaldavad ajavööndi teavet, kuid **kuupäeva** väljad mitte. **Kuupäeva** väljadel kuvatakse sama teave igas asukohas. Kui sisestate **kuupäeva** väljale kuupäeva, kirjutab Talent andmebaasi sama kuupäeva.

Kui kuvate andmeid väljal **Kuupäev ja kellaaeg**, kohandab Talent kuupäeva ja kellaaja vastavalt kasutaja ajavööndile, mis on seatud vormis **Kasutaja valikud** (**Üldine > Häälestus > Kasutaja valikud**). Väljale sisestatud kuupäeva ja kellaaja teave ei pruugi olla sama, mis andmebaasi kirjutatud teave.

[![Kasutaja valikute vorm](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Kuupäeva ja kellaaja väljadest arusaamine vormides 

Andmete sisestamisel väljale **kuupäev ja kellaaeg** ei ole ekraanil kuvatavad andmed andmebaasi salvestatud andmetega samad, kui kasutaja ajavööndiks ei ole seatud UTC. **Kuupäeva ja kellaaja** väljade andmed talletatakse alati UTC-s.

[![Töötaja vorm](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Kuupäeva ja kellaaja väljadest arusaamine andmebaasis 

Kui Talent kirjutab andmebaasi **kuupäeva ja kellaaja** väärtuse, talletatakse andmed UTC-s. See võimaldab kasutajatel näha mis tahes **kuupäeva ja kellaaja** andmeid võrreldes nende kasutaja valikutes määratletud ajavööndiga.
 
Ülaltoodud näites on algusaeg ajahetk, mitte konkreetne kuupäev. Muutes sisselogitud kasutaja ajavööndit GMT + 12:00 kuni GMT UTC, näitab just loodud kirje 05/01/2019 12:00:00 asemel 04/30/2019 12:00:00.
  
Alltoodud näites muutub töötaja 000724 töösuhe aktiivseks samal ajal, sõltumata ajavööndist. Töötaja on aktiivne 04/30/2019 GMT ajavööndis, mis on sama, mis 05/01/2019 GMT + 12:00-ajavöönd. Mõlemad viitavad samale ajale ja mitte kindlale kuupäevale. 

[![Töötaja vorm](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a>Kuupäeva ja kellaaja andmed andmehaldusraamistikus, Excelis, ühises andmeteenuses Common Data Service ja teenuses Power BI. 

Andmete halduse raamistik, Exceli lisandmoodul, Common Data Service ja Power BI aruandlus on kõik loodud, et suhelda andmetega otse andmebaasi tasemel. Kuna puudub klient, kelle jaoks **kuupäeva ja kellaaja** andmeid kasutaja ajavööndiga korrigeerida, on kõik **kuupäeva ja kellaaja** väärtused UTC-s, mis võib põhjustada mõningaid valesid oletusi, kui sisestate või vaatate andmeid.  
 
**Kuupäeva ja kellaaja** andmete puhul, mis esitatakse DMFi kaudu, Excelis või teenuses Common Data Service, eeldatakse, et andmebaas on UTC-s. See võib tekitada segadust, kui esitatud **kuupäeva ja kellaaja** väärtust ei kuvata ootuspäraselt, kuna andmeid vaataval kasutajal pole kasutaja ajavööndiks seatud UTC. 
 
Sama asi võib juhtuda, kui andmeid eksporditakse vastupidiselt. Eksporditud DMF-üksuse **kuupäeva ja kellaaga** andmed võivad olla erinevad sellest, mis kuvatakse Dynamics clientis. 
 
Kui kasutate välisallikaid, nagu DMF, et vaadata või luua andmeid, on oluline meeles pidada, et **kuupäeva ja kellaaja** väärtusi arvestatakse vaikimisi UTC-s, hoolimata kasutaja arvuti või selle praeguse kasutaja ajavööndi sätete ajavööndist. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Erinevates tootepiirkondades kuvatud sama kirje näited 

**Talenti kasutaja ajavööndiks on seatud UTC**

[![Töötaja vorm](./media/worker-form3.png)](./media/worker-form3.png)

**Talenti kasutaja ajavööndiks on seatud GMT +12:00** 

[![Töötaja vorm](./media/worker-form4.png)](./media/worker-form4.png)

**Excel OData kaudu**

[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMFi ajastamine**

[![DMFi ajastamine](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMFi eksport**

[![DMFi ajastamine](./media/DMFexport.png)](./media/DMFexport.png)

**Excel läbi Common Data Service**

[![Excel läbi Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)

### <a name="see-also"></a>Vt ka

[Kuupäev ja kellaaeg](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Kasutaja eelistatud ajavöönd](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
