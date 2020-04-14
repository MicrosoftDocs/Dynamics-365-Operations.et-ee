---
title: Mahaarvamiste konfigureerimine
description: Kasutage rakenduses Microsoft Dynamics 365 Human Resources mahaarvamisi, et määrata kui palju, kui üldse, arvatakse maha töövõtja palgast iga soodustuse jaoks.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5287161f352b386ae4e13067f40228d7c1bce62
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092725"
---
# <a name="configure-deductions"></a>Mahaarvamiste konfigureerimine

[!include [banner](includes/preview-feature.md)]

Kasutage rakenduses Microsoft Dynamics 365 Human Resources mahaarvamisi, et määrata kui palju, kui üldse, arvatakse maha töövõtja palgast iga soodustuse jaoks. Mahaarvamised on kuupäevapõhised, nii et saate säilitada mahaarvamise teabe kohta ajaloolise kirje. 

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Mahaarvamised**.

2. Valige suvand **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | Mahaarvamine | Kordumatu ID, mida kasutatakse soodustuse mahaarvamise tuvastamiseks. |
   | Kirjeldus | Mahaarvamise kirjeldus. |
   | Jõustunud | Alguskuupäev. Vaikeväärtus on praegune süsteemikuupäev. |
   | Aegumine | Lõpukuupäev. Vaikeväärtus on 12/31/2154, mis tähendab, et mitte kunagi. |
   | Pealkiri | Palgaarvestussüsteemi päise kood, mida kasutatakse palgasoodustuste töötlemisel antud mahaarvamises töövõtja osana mahaarvamisest. Seda kasutatakse, kui kasutate kolmanda osapoole palgaarvestuse pakkujat. |
   | Töövõtja palga mahaarvamise viide | Palgaarvestussüsteemi mahaarvamise kood, mida kasutatakse palgasoodustuste töötlemisel antud mahaarvamises töövõtja osana mahaarvamisest. |
   | Summa päis | Palgaarvestussüsteemi päise kood, mida see mahaarvamise summa kasutab palgasoodustuste töötlemisel antud mahaarvamises töövõtja osana mahaarvamisest. Seda kasutatakse tavaliselt, kui kasutate kolmanda osapoole palgaarvestuse pakkujat. |
   | Saab kustutada | Määrab, kas rakenduse Dynamics 365 for Finance and Operations ekspordiväärtus võib põhjustada väärtuse kustutamise palgaarvestussüsteemist. |
   | Paarisveerud | Määrab, kas eksportida päis ja mahaarvamise summa seotud külgnevate veergudena palgaarvestuse süsteemi. |
   | Jõustumiskuupäeva muutmine | Soodustuse mahaarvamise muudatuse jõustumise kuupäev, Sellel kuupäeval muudab süsteem automaatselt soodustuste mahaarvamist ja uuendab kõiki selle mahaarvamisega seotud soodustuse plaane, kui käitate mahaarvamise muutmise uuendamise töötluse. |
   | Mahaarvamise muudatus on lõpule viidud | Kui soodustuse mahaarvamise muudatused on mahaarvamise muutmise uuendamise töötlusel lõpule viidud, valitakse automaatselt märkeruut Mahaarvamise muutmine lõpetatud. |
   
4. Soodustuse määra häälestuse muudatuste jälgimiseks ja säilitamiseks valige suvand **Tegevused** ning seejärel valige suvand **Versioonide haldamine**.

5. Valige käsk **Salvesta**. 
