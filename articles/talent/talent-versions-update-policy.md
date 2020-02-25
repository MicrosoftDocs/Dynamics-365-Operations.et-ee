---
title: Rakenduse Talent süsteeminõuded
description: Selles teemas on loetletud rakenduse Dynamics 365 Talent nõuded.
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 509827d5736887f56e7754a0760af7dea76277f7
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006051"
---
# <a name="talent-system-requirements"></a>Rakenduse Talent süsteeminõuded

[!include [banner](includes/banner.md)]

See teema kirjeldab rakendusele Microsoft Dynamics 365 Talent, samuti rakendustele Attract, ja Onboard esitatavaid nõudeid. Tuuakse välja ka riigid ja piirkonnad, kus Talent on saadaval, lisaks teave keelte ja Talenti andmete lokaliseerimise kohta. Lisaks pakub see teema Talenti värskenduspoliitikat.

## <a name="supported-web-browsers"></a>Toetatud veebibrauserid

Microsoft Dynamics 365 Talenti saab kasutada kõigis järgmistes veebibrauserites, mis töötavad nimetatud operatsioonisüsteemis. 

*   Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s
*   Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7
*   Google Chrome (viimane avalikult saadaolev versioon)
*   Apple Safari (viimane avalikult saadaolev versioon)

Iga veebibrauseri uusima versiooni leidmiseks minge tarkvaratootja veebisaidile. 

> [!NOTE]
> * Tegevuse salvestajas loodud piltide jäädvustamiseks ja nende Microsoft Wordi dokumentidesse lisamiseks peab teil olema installitud Chrome’i laiendus. 
> * Töövooredaktor käivitatakse ClickOnce’i rakendusena. Ainult Microsoft Edge ja Internet Explorer (Microsoft Windowsi toetatud versioonis) toetavad ClickOnce’i rakendusi. Töövooredaktori ClickOnce rakendus nõuab ühilduvat 64-bitist operatsioonisüsteemi.
> * PDF-failide eelvaateks soovitame kasutada tänapäevasi brausereid, nagu Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s või Chrome (viimane avalikult saadaolev versioon) Windows 10-s, Windows 8.1-s, Windows 8-s, Windows 7-s või tahvelarvutis Google Nexus 10.
>   Võrgunõuded
> * Dynamics 365 Talent on mõeldud võrkudele, mille latentsus on kuni 250–300 millisekundit (ms). See on latentsus brauserikliendist Microsoft Azure’i andmekeskusse, mis majutab rakendust. Soovitame teilt testida võrgulatentsust veebiaadressil [www.azurespeed.com](https://www.azurespeed.com "Azure’i latentsustest").
> * Ribalaiuse nõuded Talenti puhul sõltuvad teie stsenaariumist. Kõige tüüpilisemad stsenaariumid nõuavad ribalaiust rohkem kui 50 kilobaiti sekundis (KB/s).
> 
> [!WARNING]
> Ärge arvutage ribalaiuse nõudeid kliendi asukohast, korrutades kasutajate arvu minimaalsete ribalaiuse nõuetega. Antud asukoha samaaegset kasutust on väga keeruline arvutada. Ribalaiuse nõuete pärast muret tundvad kliendid peaksid kasutama rakenduse Talent eelvaateversiooni.

## <a name="supported-microsoft-office-applications"></a>Toetatud Microsoft Office’i rakendused

* Microsoft Exceli ja Wordi lisandmoodulite käivitamiseks peab teil olema installitud Windowsile või Macile mõeldud Microsoft Office 2016. Versiooninõuete kohta lisateabe saamiseks vaadake teemat [Office’i integratsiooni tõrkeotsing](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office’i integreerimise tõrkeotsing").
* Funktsiooniga Ekspordi Excelisse või Ekspordi Wordi loodud dokumentide vaatamiseks peab teil olema installitud Microsoft Office 2007 või uuem versioon.

## <a name="regional-availability-languages-and-localization"></a>Piirkondlik saadavus, keeled ja lokaliseerimine

Saate alla laadida PDF-faili riikide, piirkondade ja keelte kohta, mida Talent toetab siit [Microsoft Dynamics 365 rahvusvaheline kättesaadavus](https://docs.microsoft.com/dynamics365/get-started/availability) 

> [!NOTE]
> Kui kasutajaliides on lokaliseeritud teistesse keeltesse, talletatakse kõik kasutajaandmed keeles, milles need sisestati. Saate luua e-kirju ja malle teistes keeltes, kuid sellised andmed nagu planeerimise teave on praegu saadaval ainult inglise keeles.

Kui olete arendaja, kes on huvitatud riigi- või piirkonnapõhiste kohanduste loomisest või luua lahendus mõnele riigile või piirkonnale, mida Microsoft praegu ei toeta, vt [Globaliseerumine](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).

