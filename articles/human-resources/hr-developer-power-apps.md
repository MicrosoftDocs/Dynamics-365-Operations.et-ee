---
title: Talenti laiendamine Power Appsi ja Power Automate’iga
description: Selles artiklis kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 Human Resources, mis kasutab Microsoft Power Appsi ja Microsoft Power Automate’i.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: Dynamics 365 Human Resources;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8d4185b958ed35e9d2bc764db8ea77b3a2f53c37
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029861"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Laiendamine Power Appsi ja Power Automate’iga

Selles artiklis kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 Human Resources, mis kasutab Microsoft Power Appsi ja Microsoft Power Automate’i. Saate rakenduse Power Apps keskkonda importida iga näitega seotud lahendusepaketi. Seejärel saate pakette kasutada juhisena või lähtekohana teie organisatsioonile sobivate stsenaariumide rakendamiseks.

> [!IMPORTANT]
> Kui soovite kasutada selles teemas kirjeldatud malle ja rakendusi muutmata kujul, katsetage neid kindlasti veendumaks, et need hõlmaksid kõiki teie juurutusele kehtivaid stsenaariume.

## <a name="prerequisites"></a>Eeltingimused

- Pakettide importimiseks peab kasutajatel olema **keskkonna looja** luba.
- Rakenduste eksportimiseks või importimiseks peab kasutajatel olema Power Appsi plaani 2 litsents või Power Appsi plaani 2 proovilitsents.

## <a name="integration-with-office-365-power-automate"></a>Office 365-ga integreerimine, Power Automate

Rakendust **Office 365-ga integreerimine** saab kasutada sisse logitud kasutajate töörühma teabe ekstraktimiseks Microsoft Office 365-st. See viitab töötajatele rakenduses Human Resources, et hankida töövõtja tuvastustüüpe. Haldurid saavad kontrollida töötaja ID-tüüpide aegumiskuupäevi. Samuti võivad nad saata meeldetuletuse, kui töötaja ID-tüüp on aegumas. Selle meeldetuletuse saatmiseks Power Automate integreerub Power Appsiga. Kui meeldetuletus on saadetus, saadetakse Power Automate’ist tagasi Power Appsi kinnitus. Identifikatsiooni tüübid hõlmavad juhiluba, passi ja teisi aktsepteeritavaid ID vorme.

Saate seda rakendust laiendada teistele stsenaariumidele. Näiteks saate seda kasutada töörühma puhkuste teabe, kalendrisündmuste ja töörühmaga seotud sündmuste näitamiseks.

**Office 365-ga integreerimise, Power Automate** rakenduse allalaadimiseks avage Microsofti allalaadimiskeskuses [Office 365-ga integreerimine](https://go.microsoft.com/fwlink/?linkid=2081787).

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL-i ühendamine ja käivitamine

Mall **Power Automate – SQL-i ühendamine ja käivitamine** loob ühenduse Microsoft SQL Serveriga ja lubab käivitada SQL-i päringuid.

Kuigi see mall loeb ja värskendab SQL-tabeleid, saate seda laiendada ja kasutada seda muude stsenaariumite jaoks. Näiteks saate seda kasutada vahetabeli täitmiseks teenuses Common Data Service kirjetega SQL-serverist ja vahetabeli aeg-ajalt sünkroonimiseks, kasutades SQL-serveri astmelist jaotust.

Täpsem päring on integreeritud Flowga, mis võimaldab andmete teisendamist ja astmelist jaotust.

Malli **Power Automate – SQL-i ühendamine ja käivitamine** allalaadimiseks avage Microsofti allalaadimiskeskuses [Power Automate – SQL-i ühendamine ja käivitamine](https://go.microsoft.com/fwlink/?linkid=2081789).

## <a name="additional-resources"></a>Lisaressursid

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>
[Rakenduse ülekandmine rentnike ja keskkondade vahel](https://docs.microsoft.com/power-platform/admin/environment-and-tenant-migration)
