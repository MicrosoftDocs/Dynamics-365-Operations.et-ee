---
title: Mahaarvamiste konfigureerimine
description: Kasutage rakenduses Microsoft Dynamics 365 Human Resources mahaarvamisi, et määrata kui palju, kui üldse, arvatakse maha töövõtja palgast iga soodustuse jaoks.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fac1624ce3a88b9fb4adcf303860e82f9d9165b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055552"
---
# <a name="configure-deductions"></a>Mahaarvamiste konfigureerimine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kasutage rakenduses Microsoft Dynamics 365 Human Resources mahaarvamisi, et määrata kui palju, kui üldse, arvatakse maha töövõtja palgast iga soodustuse jaoks. Mahaarvamised on kuupäevapõhised, nii et saate säilitada mahaarvamise teabe kohta ajaloolise kirje. 

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Mahaarvamised**.

2. Valige suvand **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Mahaarvamine** | Kordumatu ID, mida kasutatakse soodustuse mahaarvamise tuvastamiseks. |
   | **Kirjeldus** | Mahaarvamise kirjeldus. |
   | **Jõustunud** | Alguskuupäev. Vaikeväärtus on praegune süsteemikuupäev. |
   | **Aegumine** | Lõpukuupäev. Vaikeväärtus on 12/31/2154, mis tähendab, et mitte kunagi. |
   | **Pealkiri** | Palgaarvestussüsteemi päise kood, mida kasutatakse palgasoodustuste töötlemisel antud mahaarvamises töövõtja osana mahaarvamisest. Seda kasutatakse, kui kasutate kolmanda osapoole palgaarvestuse pakkujat. |
   | **Töövõtja palga mahaarvamise viide** | Palgaarvestussüsteemi mahaarvamise kood, mida kasutatakse palgasoodustuste töötlemisel antud mahaarvamises töövõtja osana mahaarvamisest. |
   | **Summa päis** | Palgaarvestussüsteemi päise kood, mida see mahaarvamise summa kasutab palgasoodustuste töötlemisel antud mahaarvamises töövõtja osana mahaarvamisest. Seda kasutatakse tavaliselt, kui kasutate kolmanda osapoole palgaarvestuse pakkujat. |
   | **Saab kustutada** | Määrab, kas rakenduse Dynamics 365 for Finance and Operations ekspordiväärtus võib põhjustada väärtuse kustutamise palgaarvestussüsteemist. |
   | **Paarisveerud** | Määrab, kas eksportida päis ja mahaarvamise summa seotud külgnevate veergudena palgaarvestuse süsteemi. |
   | **Jõustumiskuupäeva muutmine** | Soodustuse mahaarvamise muudatuse jõustumise kuupäev, Sellel kuupäeval muudab süsteem automaatselt soodustuste mahaarvamist ja uuendab kõiki selle mahaarvamisega seotud soodustuse plaane, kui käitate **mahaarvamise muutmise uuendamise** töötluse. |
   | **Mahaarvamise muudatus on lõpule viidud** | Kui soodustuse mahaarvamise muudatused on **mahaarvamise muutmise uuendamise** töötlusel lõpule viidud, valitakse automaatselt märkeruut Mahaarvamise muutmine lõpetatud. |
   
4. Soodustuse määra häälestuse muudatuste jälgimiseks ja säilitamiseks valige suvand **Tegevused** ning seejärel valige suvand **Versioonide haldamine**.

5. Valige käsk **Salvesta**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]