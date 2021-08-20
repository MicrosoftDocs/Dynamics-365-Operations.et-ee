---
title: Kuupäeva ja kellaaja väljade mõistmine
description: Saate teada, mida oodata kuupäeva ja kellaaja väljade kasutamisel rakenduses Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
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
ms.openlocfilehash: cb011ca7b5f4c036b2f49875a256885182564c391c6dd263a0bfa70bbd29f4a7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733536"
---
# <a name="understand-date-and-time-fields"></a>Kuupäeva ja kellaaja väljade ülevaade

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Kuupäeva ja kellaaja** väljad on põhimõiste rakenduses Dynamics 365 Human Resources. Oluline on mõista, kuidas töötada **Kuupäeva ja kellaaja** andmetega rakenduse Dataverse vormidel, teenuses ja välistes allikates.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Kuupäeva ja kuupäeva ning kellaaja andmetüüpide erinevuse mõistmine

**Kuupäeva ja kellaaja** väljad sisaldavad ajavööndi teavet, kuid **kuupäeva** väljad mitte. **Kuupäeva** väljadel kuvatakse sama teave igas asukohas. Kui sisestate **kuupäeva** väljale kuupäeva, kirjutab Human Resources andmebaasi sama kuupäeva.

Kui kuvate andmeid väljal **Kuupäev ja kellaaeg**, kohandab Human Resources kuupäeva ja kellaaja vastavalt kasutaja ajavööndile, mis on seatud vormis **Kasutaja valikud** (**Üldine > Häälestus > Kasutaja valikud**). Väljale sisestatud kuupäeva ja kellaaja teave ei pruugi olla sama, mis andmebaasi kirjutatud teave.

[![Kasutaja valikute vorm.](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Kuupäeva ja kellaaja väljadest arusaamine vormides 

Ekraanil kuvatavad **kuupäev ja kellaaeg** ei ole andmebaasi salvestatud andmetega samad, kui kasutaja ajavööndiks ei ole seatud UTC. **Kuupäeva ja kellaaja** väljade andmed talletatakse alati UTC-s.

[![Töötaja UTC vorm.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Kuupäeva ja kellaaja väljadest arusaamine andmebaasis 

Kui Human Resources kirjutab andmebaasi **kuupäeva ja kellaaja** väärtuse, talletatakse andmed UTC-s. See võimaldab kasutajatel näha mis tahes **kuupäeva ja kellaaja** andmeid võrreldes nende kasutaja valikutes määratletud ajavööndiga.
 
Ülaltoodud näites on algusaeg ajahetk, mitte konkreetne kuupäev. Muutes sisselogitud kasutaja ajavööndit GMT + 12:00 kuni GMT UTC, näitab kirje 05/01/2019 12:00:00 asemel 04/30/2019 12:00:00.
  
Alltoodud näites muutub töötaja 000724 töösuhe aktiivseks samal ajal, sõltumata ajavööndist. Töötaja on aktiivne 04/30/2019 GMT ajavööndis, mis on sama, mis 05/01/2019 GMT + 12:00-ajavöönd. Mõlemad viitavad samale ajale ja mitte kindlale kuupäevale. 

[![Töötaja GMT vorm.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Kuupäeva ja kellaaja andmed andmehaldusraamistikus, Excelis, ühises andmeteenuses Dataverse ja teenuses Power BI. 

Andmete halduse raamistik, Exceli lisandmoodul, Dataverse ja Power BI aruandlus on kõik loodud, et suhelda andmetega otse andmebaasi tasemel. Kuna puudub klient, kelle jaoks **kuupäeva ja kellaaja** andmeid kasutaja ajavööndiga korrigeerida, on kõik **kuupäeva ja kellaaja** väärtused UTC-s, mis võib põhjustada mõningaid valesid oletusi, kui sisestate või vaatate andmeid.  
 
**Kuupäeva ja kellaaja** andmete puhul, mis esitatakse DMFi kaudu, Excelis või teenuses Dataverse, eeldatakse, et andmebaas on UTC-s. See võib tekitada segadust, kui esitatud **kuupäeva ja kellaaja** väärtust ei kuvata ootuspäraselt, kuna andmeid vaataval kasutajal pole kasutaja ajavööndiks seatud UTC. 
 
Sama asi võib juhtuda, kui andmeid eksporditakse vastupidiselt. Eksporditud DMF-üksuse **kuupäeva ja kellaaga** andmed võivad olla erinevad sellest, mis kuvatakse Dynamics clientis. 
 
Kui kasutate välisallikaid, nagu DMF, et vaadata või luua andmeid, pidage meeles, et **kuupäeva ja kellaaja** väärtusi arvestatakse vaikimisi UTC-s, hoolimata kasutaja arvuti või selle praeguse kasutaja ajavööndi sätete ajavööndist. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Erinevates tootepiirkondades kuvatud sama kirje näited 

**Rakenduse Human Resources kasutaja ajavööndiks on seatud UTC**

[![Töötaja vorm seatud UTC-le.](./media/worker-form3.png)](./media/worker-form3.png)

**Rakenduse Human Resources kasutaja ajavööndiks on seatud GMT +12.00** 

[![Töötaja vorm seatud GMT-le.](./media/worker-form4.png)](./media/worker-form4.png)

**Excel OData kaudu**

[![Excel Via OData.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMFi ajastamine**

[![DMFi ajastamine.](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMFi eksport**

[![DMF Eksport.](./media/DMFexport.png)](./media/DMFexport.png)

**Excel läbi Dataverse**

[![Excel läbi rakenduse Dataverse.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Vt ka

[Kuupäev ja kellaaeg](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Kasutaja eelistatud ajavöönd](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]