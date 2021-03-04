---
title: Talenti laiendamine Power Appsi ja Power Automate’iga
description: Selles artiklis kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 Talent - Attract, mis kasutab Microsoft Power Appsi ja Microsoft Power Automate’i.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: cfdf36e9486aa4853d3bf674afa73ec3a4d1c161
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529630"
---
# <a name="extend-talent-with-power-apps-and-power-automate"></a>Talenti laiendamine Power Appsi ja Power Automate’iga

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles artiklis kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 Talent: Attract, mis kasutab Microsoft Power Appsi ja Microsoft Power Automate’i. Saate rakenduse Power Apps keskkonda importida iga näitega seotud lahendusepaketi. Seejärel saate pakette kasutada juhisena või lähtekohana teie organisatsioonile sobivate stsenaariumide rakendamiseks.

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

Microsoft Dynamics 365: Attractis saab vorme kasutada kandidaadi portaalis, kus kandidaadid täidavad üksikasju. Vorme saate ka tegevustena töömalli manustada.

Kui kandidaat vormi esitab, jäädvustab Microsoft Power Automate vormi esitamise, loeb andmeid ja salvestab need teenuse Common Data Service üksusesse.

Malli **Power Automate’i ja Formi ühendamine** ja kohandatud üksuse struktuuri alla laadimiseks avage Microsofti allalaadimiskeskuses [Power Automate’i ja Formi ühendamine](https://go.microsoft.com/fwlink/?linkid=2081988).

## <a name="power-automate--sharepoint-integration"></a>Power Automate – SharePointiga integreerimine

Malli **Power Automate – SharePointiga integreerimine** saab kasutada andmete lugemiseks Microsoft SharePointi loendist, loendi võrdlemiseks olemi Common Data Service mis tahes üksuse väljaväärtustega ja võrdluse tulemuste saatmiseks teavitusmeilina. 

Organisatsioonil võivad olla oskused, mida tal on tingimata vaja. Neid oskusi saab hoiustada SharePointis SharePointi loendina. Kui kandidaat kandideerib mis tahes tööle, mille kohta on olemas vajalike oskuste loend, ning kandidaadi oskuse ja SharePointi salvestatud oskuste vahel on oluline kokkulangevus, saadetakse selle kohta teavitusmeil. See aitab täita vajaminevad ametikohad kiiremini, kuna teatised aitavad värbajatel värvata kandidaate kogu organisatsioonist.

Seda malli saab laiendada kasutamiseks mis tahes stsenaariumi jaoks, mis hõlmab SharePointi integratsiooni.

Malli **Power Automate – SharePointiga integreerimine** allalaadimiseks avage Microsofti allalaadimiskeskuses [Power Automate – SharePointiga integreerimine](https://go.microsoft.com/fwlink/?linkid=2082109).

## <a name="referral-app"></a>Soovitusrakendus

Saate kasutada soovitusrakendust, et lisada kandidaate jagatud talendipanka. Soovitaja saab kandidaadi esitamisel sisestada **eesnime**, **perekonnanime**, **meiliaadressi** ja **LinkedIni URLi**. Seejärel täidetakse kandidaatallika metaandmed koos soovitaja teabega.

Saate selle rakenduse manustada soovituste esitamiseks töötajate iseteenindusse või kasutada seda ettevõtteportaalis hüperlingina ja kasutada eraldiseisva rakendusena.

**Sooitusrakenduse** allalaadimiseks minge Microsofti allalaadimiskeskuse lehele [Dynamics 365 Talent laiendatavuse lahendus: soovitusrakendus](https://www.microsoft.com/download/details.aspx?id=58497). Seda rakendust saab importida ja kohandada, et lisada täiendavaid funktsioone.

## <a name="additional-resources"></a>Lisaressursid

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[Rakenduse ülekandmine rentnike ja keskkondade vahel](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)


[!INCLUDE[footer-include](../includes/footer-banner.md)]