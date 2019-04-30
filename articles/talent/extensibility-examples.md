---
title: Talenti laiendamine PowerAppsi ja Microsoft Flow’ga – näidisstsenaariumid
description: Selles teemas kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 for Talent, mis kasutab Microsoft PowerAppsi ja Microsoft Flow’d.
author: negudava
manager: Annbe
ms.date: 03/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 0aa3578047b9397682a7039d0dbcc05cc1b167e4
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/12/2019
ms.locfileid: "949916"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a>Talenti laiendamine PowerAppsi ja Microsoft Flow’ga – näidisstsenaariumid

Selles teemas kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 for Talent, mis kasutab Microsoft PowerAppsi ja Microsoft Flow’d. Saate PowerAppsi keskkonda importida iga näitega seotud lahendusepaketi. Seejärel saate pakette kasutada juhisena või lähtekohana teie organisatsioonile sobivate stsenaariumide rakendamiseks.

> [!IMPORTANT]
> Kui soovite kasutada selles teemas kirjeldatud malle ja rakendust muutmata kujul, katsetage neid kindlasti veendumaks, et need hõlmavad kõiki teie juurutusele kehtivaid stsenaariume.


## <a name="prerequisites"></a>Eeltingimused

- Pakettide importimiseks peab kasutajatel olema **keskkonna looja** luba.
- Rakenduste eksportimiseks või importimiseks peab kasutajatel olema PowerAppsi plaani 2 litsents või PowerAppsi plaani 2 proovilitsents.

## <a name="flow--form-connect"></a>Flow ja Formi ühendamine

Malli **Flow ja Formi ühendamine** saab kasutada andmete lugemiseks Microsoft Formsist ja nende salvestamiseks teenuse Common Data Service üksusesse.

Seda malli saab laiendada, et seda saaks kasutada ka teistes stsenaariumites. Järgmisena on toodud mõned näited.

- Kandidaadi hinnangute jäädvustamine.
- Kursuse küsimustike tulemuste jäädvustamine.
- Töövestluse küsimuste teegi koostamine inimressursside (HR) administraatorite jaoks.
- Kandidaadi hinnangu jäädvustamine vestluse protsessi kohta

Microsoft Dynamics 365: Attractis saab vorme kuvada kandidaadi portaalis ja kandidaadid saavad täita üksikasju. Vorme saab ka tegevustena töömalli manustada.

Kui kandidaat vormi esitab, jäädvustab Microsoft Flow vormi esitamise, loeb andmeid ja salvestab need teenuse Common Data Service üksusesse.

Malli **Flow ja Formi ühendamine** ja kohandatud üksuse struktuuri alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Flow ja Formi ühendamine](https://go.microsoft.com/fwlink/?linkid=2081988).

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a>Powerappsi edastatud parameetrite käivitamine ja ekstraktimine

Malli **Powerappsi edastatud parameetrite käivitamine ja ekstraktimine** saab kasutada lähtekohana mis tahes PowerAppsi stsenaariumi jaoks, mis on omane Attractile. See sisaldab kõiki vaikeparameetreid, mille Attract edastab, nt **Tööavaldus**, **Kandidaadi ID** ja **Töö ID**.

Seda malli saab kasutada kandidaadi hinnanguvormi leidmiseks, et personalijuht saaks kandidaadi täidetud hinnangut vaadata.

PowerAppsiga loodud rakendusi saab manustada Attractis töömalli.

Malli **Powerappsi edastatud parameetrite käivitamine ja ekstraktimine** ja kohandatud üksuse struktuuri alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Powerappsi edastatud parameetrite käivitamine ja ekstraktimine](https://go.microsoft.com/fwlink/?linkid=2081991).

## <a name="integration-with-office-365"></a>Office 365-iga integreerimine

Rakendust **Office 365-ga integreerimine** saab kasutada sisse logitud kasutajate töörühma teabe ekstraktimiseks Microsoft Office 365-st. See viitab töötajatele Talentis, et ekstraktida sisse- ja väljaregistreerimiste üksikasju ning erandite kirjeid. Sisse- ja väljaregistreerimiste üksikasju salvestatakse teenuse Common Data Service kohandatud üksustes. Eeldus on, et need üksikasjad täidab muude tootjate süsteemid integratsiooni kaudu.

Seda rakendust saab laiendada, et seda saaks kasutada ka teistes stsenaariumites. Näiteks saab seda kasutada töörühma puhkuste teabe, kalendrisündmuste ja töörühmaga seotud sündmuste näitamiseks.

Rakenduse **Office 365-ga integreerimine** ja kohandatud üksuse struktuuri alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Office 365-ga integreerimine](https://go.microsoft.com/fwlink/?linkid=2081787).

## <a name="flow--email-notification"></a>Flow – meiliteatis

Malli **Flow – meiliteatis** saab kasutada meiliteatise stsenaariumide jaoks. Seda saab kasutada teavitusmeilide saatmiseks kandidaatidele, kelle värbamistöörühm värbamisprotsessi mis tahes etapis tagasi lükkab.

Seda malli saab laiendada, et see jälgiks muudatusi kandidaadi etapis kogu värbamisprotsessi jooksul ning saadaks teatisi värbamistöörühmale ja kandidaadile.

Üldiselt saab lahenduses Common Data Service salvestatud üksuste jaoks voogusid seadistada nii, et need saadavad teatisi rakenduse Core HR, Attract või Dynamics 365 Talent: Onboard sündmuste kohta.

Malli **Flow – meiliteatis** alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Flow – meiliteatis](https://go.microsoft.com/fwlink/?linkid=2082103).

## <a name="flow--sql-connect-and-execute"></a>Flow – SQL-i ühendamine ja käivitamine

Mall **Flow – SQL-i ühendamine ja käivitamine** loob ühenduse Microsoft SQL Serveriga ja lubab käivitada SQL-i päringuid.

Kuigi see mall on mõeldud lugema ja värskendama SQL-i tabeleid, saab seda laiendada kasutamiseks teistes stsenaariumites. Näiteks saab seda kasutada vahetabeli täitmiseks teenuses Common Data Service kirjetega SQL Serverist ja vahetabeli aeg-ajalt sünkroonimiseks, kasutades SQL Serveri astmelist jaotust.

Malli **Flow – SQL-i ühendamine ja käivitamine** alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Flow – SQL-i ühendamine ja käivitamine](https://go.microsoft.com/fwlink/?linkid=2081789).

## <a name="flow--sharepoint-integration"></a>Flow – SharePointi integreerimine

Malli **Flow – SharePointi integreerimine** saab kasutada andmete lugemiseks Microsoft SharePointi loendist, loendi võrdlemiseks teenuse Common Data Service mis tahes üksuse väljaväärtustega ja võrdluse tulemuste saatmiseks teavitusmeilina. 

Organisatsioonil võivad olla oskused, mida tal on tingimata vaja. Neid oskusi saab hoiustada SharePointis SharePointi loendina. Kui kandidaat kandideerib mis tahes tööle, mille kohta on olemas vajalike oskuste loend, ning kandidaadi oskuse ja SharePointi salvestatud oskuste vahel on oluline kokkulangevus, saadetakse selle kohta teavitusmeil. Nii täidetakse kiiresti vajaminevad ametikohad kiiremini, kuna teatised aitavad värbajatel jõuda kõigi organisatsiooni kandidaatideni ja neid värvata.

Seda malli saab laiendada kasutamiseks mis tahes stsenaariumi jaoks, mis hõlmab SharePointi integratsiooni.

Malli **Flow – SharePointi integratsioon** alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Flow – SharePointi integratsioon](https://go.microsoft.com/fwlink/?linkid=2082109).



## <a name="additional-resources"></a>Lisaressursid

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Rakenduse ülekandmine rentnike ja keskkondade vahel](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
