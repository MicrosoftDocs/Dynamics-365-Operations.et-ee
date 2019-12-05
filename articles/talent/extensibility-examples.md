---
title: Talenti laiendamine Power Appsi ja Power Automate’iga
description: Selles teemas kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 Talent, mis kasutab Microsoft Power Appsi ja Microsoft Power Automate’i.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 3bb61297e294aa3f2d06f542bebe29d7afae9c3b
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832834"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Talenti laiendamine Power Appsi ja Power Automate’iga

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 Talent, mis kasutab Microsoft Power Appsi ja Microsoft Power Automate’i. Saate rakenduse Power Apps keskkonda importida iga näitega seotud lahendusepaketi. Seejärel saate pakette kasutada juhisena või lähtekohana teie organisatsioonile sobivate stsenaariumide rakendamiseks.

> [!IMPORTANT]
> Kui soovite kasutada selles teemas kirjeldatud malle ja rakendust muutmata kujul, katsetage neid kindlasti veendumaks, et need hõlmavad kõiki teie juurutusele kehtivaid stsenaariume.


## <a name="prerequisites"></a>Eeltingimused

- Pakettide importimiseks peab kasutajatel olema **keskkonna looja** luba.
- Rakenduste eksportimiseks või importimiseks peab kasutajatel olema Power Appsi plaani 2 litsents või Power Appsi plaani 2 proovilitsents.

## <a name="power-automate--form-connect"></a>Power Automate’i ja Formi ühendamine

Malli **Power Automate’i ja Formi ühendamine** saab kasutada andmete lugemiseks Microsoft Formsist ja nende salvestamiseks teenuse Common Data Service üksusesse.

Seda malli saab laiendada, et seda saaks kasutada ka teistes stsenaariumites. Järgmisena on toodud mõned näited.

- Kandidaadi hinnangute jäädvustamine.
- Kursuse küsimustike tulemuste jäädvustamine.
- Töövestluse küsimuste teegi koostamine inimressursside (HR) administraatorite jaoks.
- Kandidaadi hinnangu jäädvustamine vestluse protsessi kohta

Microsoft Dynamics 365: Attractis saab vorme kuvada kandidaadi portaalis ja kandidaadid saavad täita üksikasju. Vorme saab ka tegevustena töömalli manustada.

Kui kandidaat vormi esitab, jäädvustab Microsoft Power Automate vormi esitamise, loeb andmeid ja salvestab need teenuse Common Data Service üksusesse.

Malli **Power Automate’i ja Formi ühendamine** ja kohandatud üksuse struktuuri alla laadimiseks avage Microsofti allalaadimiskeskuses [Power Automate’i ja Formi ühendamine](https://go.microsoft.com/fwlink/?linkid=2081988).

## <a name="initiate-and-extract-parameters-passed-to-power-apps"></a>Power Appsi edastatud parameetrite käivitamine ja ekstraktimine

Malli **Power Appsi edastatud parameetrite käivitamine ja ekstraktimine** saab kasutada lähtekohana mis tahes rakenduse Power Apps stsenaariumi jaoks, mis on omane Attractile. See sisaldab kõiki vaikeparameetreid, mille Attract edastab, nt **Tööavaldus**, **Kandidaadi ID** ja **Töö ID**.

Seda malli saab kasutada kandidaadi hinnanguvormi leidmiseks, et personalijuht saaks kandidaadi täidetud hinnangut vaadata.

Power Appsiga loodud rakendusi saab manustada Attractis töömalli.

Malli **Power Appsi edastatud parameetrite käivitamine ja ekstraktimine** ja kohandatud üksuse struktuuri allalaadimiseks avage Microsofti allalaadimiskeskuses [Power Appsi edastatud parameetrite käivitamine ja ekstraktimine](https://go.microsoft.com/fwlink/?linkid=2081991).

## <a name="integration-with-office-365"></a>Office 365-iga integreerimine

Rakendust **Office 365-ga integreerimine** saab kasutada sisse logitud kasutajate töörühma teabe ekstraktimiseks Microsoft Office 365-st. See viitab töötajatele Talentis, et ekstraktida sisse- ja väljaregistreerimiste üksikasju ning erandite kirjeid. Sisse- ja väljaregistreerimiste üksikasju salvestatakse teenuse Common Data Service kohandatud üksustes. Eeldus on, et need üksikasjad täidab muude tootjate süsteemid integratsiooni kaudu.

Seda rakendust saab laiendada, et seda saaks kasutada ka teistes stsenaariumites. Näiteks saab seda kasutada töörühma puhkuste teabe, kalendrisündmuste ja töörühmaga seotud sündmuste näitamiseks.

Rakenduse **Office 365-ga integreerimine** ja kohandatud üksuse struktuuri alla laadimiseks minge Microsofti allalaadimiskeskuses lehele [Office 365-ga integreerimine](https://go.microsoft.com/fwlink/?linkid=2081787).

## <a name="power-automate--email-notification"></a>Power Automate – meiliteatis

Malli **Power Automate – meiliteatis** saab kasutada meiliteatise stsenaariumide jaoks. Seda saab kasutada teavitusmeilide saatmiseks kandidaatidele, kelle värbamistöörühm värbamisprotsessi mis tahes etapis tagasi lükkab.

Seda malli saab laiendada, et see jälgiks muudatusi kandidaadi etapis kogu värbamisprotsessi jooksul ning saadaks teatisi värbamistöörühmale ja kandidaadile.

Üldiselt saab lahenduses Common Data Service salvestatud üksuste jaoks voogusid seadistada nii, et need saadavad teatisi rakenduse Core HR, Attract või Onboard sündmuste kohta.

Malli **Power Automate – meiliteatis** allalaadimiseks avage Microsofti allalaadimiskeskuses [Power Automate – meiliteatis](https://go.microsoft.com/fwlink/?linkid=2082103).

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL-i ühendamine ja käivitamine

Mall **Power Automate – SQL-i ühendamine ja käivitamine** loob ühenduse Microsoft SQL Serveriga ja lubab käivitada SQL-i päringuid.

Kuigi see mall on mõeldud lugema ja värskendama SQL-i tabeleid, saab seda laiendada kasutamiseks teistes stsenaariumites. Näiteks saab seda kasutada vahetabeli täitmiseks teenuses Common Data Service kirjetega SQL Serverist ja vahetabeli aeg-ajalt sünkroonimiseks, kasutades SQL Serveri astmelist jaotust.

Malli **Power Automate – SQL-i ühendamine ja käivitamine** allalaadimiseks avage Microsofti allalaadimiskeskuses [Power Automate – SQL-i ühendamine ja käivitamine](https://go.microsoft.com/fwlink/?linkid=2081789).

## <a name="power-automate--sharepoint-integration"></a>Power Automate – SharePointiga integreerimine

Malli **Power Automate – SharePointiga integreerimine** saab kasutada andmete lugemiseks Microsoft SharePointi loendist, loendi võrdlemiseks olemi Common Data Service mis tahes üksuse väljaväärtustega ja võrdluse tulemuste saatmiseks teavitusmeilina. 

Organisatsioonil võivad olla oskused, mida tal on tingimata vaja. Neid oskusi saab hoiustada SharePointis SharePointi loendina. Kui kandidaat kandideerib mis tahes tööle, mille kohta on olemas vajalike oskuste loend, ning kandidaadi oskuse ja SharePointi salvestatud oskuste vahel on oluline kokkulangevus, saadetakse selle kohta teavitusmeil. Nii täidetakse kiiresti vajaminevad ametikohad kiiremini, kuna teatised aitavad värbajatel jõuda kõigi organisatsiooni kandidaatideni ja neid värvata.

Seda malli saab laiendada kasutamiseks mis tahes stsenaariumi jaoks, mis hõlmab SharePointi integratsiooni.

Malli **Power Automate – SharePointiga integreerimine** allalaadimiseks avage Microsofti allalaadimiskeskuses [Power Automate – SharePointiga integreerimine](https://go.microsoft.com/fwlink/?linkid=2082109).

## <a name="referral-app"></a>Soovitusrakendus
Saate kasutada soovitusrakendust, et lisada kandidaate jagatud talendipanka. Soovitaja saab kandidaadi esitamisel sisestada **eesnime**, **perekonnanime**, **meliaadressi** ja **LinkedIni URLi**. Seejärel täidetakse kandidaatallika metaandmed koos soovitaja teabega.

Saate selle rakenduse manustada soovituste esitamiseks töötajate iseteenindusse (ESS) või kasutada seda ettevõtteportaalis hüperlingina ja kasutada eraldiseisva rakendusena.

**Sooitusrakenduse** allalaadimiseks minge Microsofti allalaadimiskeskuse lehele [Dynamics 365 Talent laiendatavuse lahendus: soovitusrakendus](http://www.microsoft.com/downloads/details.aspx?FamilyID=9a59c9d1-f8a1-4d4d-b768-cfc4f4eb9d0d). Seda rakendust saab importida ja kohandada, et lisada täiendavaid funktsioone.

## <a name="additional-resources"></a>Lisaressursid

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[Rakenduse ülekandmine rentnike ja keskkondade vahel](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
