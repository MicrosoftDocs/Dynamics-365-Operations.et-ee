---
title: Rakenduse Talent süsteeminõuded ja värskenduspoliitika
description: Selles teemas on loetletud rakenduse Dynamics 365 for Talent nõuded. Samuti on välja toodud värskenduspoliitika.
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 0fa2b7c2dc5b88349cb4012b6b0ba9009a361fa0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "303977"
---
# <a name="talent-system-requirements-and-update-policy"></a>Rakenduse Talent süsteeminõuded ja värskenduspoliitika

[!include [banner](includes/banner.md)]

Selles teemas on loetletud rakenduse Microsoft Dynamics 365 for Talent nõuded. Samuti on välja toodud värskenduspoliitika.

## <a name="supported-web-browsers"></a>Toetatud veebibrauserid

Microsoft Dynamics 365 for Talenti veebirakendust saab kasutada kõigis järgmistes veebibrauserites, mis töötavad nimetatud operatsioonisüsteemis. 

*   Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s
*   Internet Explorer 11 operatsioonisüsteemides Windows 10, Windows 8.1 või Windows 7
*   Google Chrome (viimane avalikult saadaolev versioon) operatsioonisüsteemides Windows 10, Windows 8.1, Windows 8, Windows 7 või tahvelarvuti Google Nexus 10
*   Apple Safari (viimane avalikult saadaolev versioon) operatsioonisüsteemides Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) või 10.12 (Sierra) või Apple iPad

Iga veebibrauseri uusima versiooni leidmiseks minge tarkvaratootja veebisaidile. 

> [!NOTE]
> * Tegevuse salvestajas loodud piltide jäädvustamiseks ja nende Microsoft Wordi dokumentidesse lisamiseks peab teil olema installitud Chrome’i laiendus. 
> * Töövooredaktor käivitatakse ClickOnce’i rakendusena. Ainult Microsoft Edge ja Internet Explorer (Microsoft Windowsi toetatud versioonis) toetavad ClickOnce’i rakendusi. Töövooredaktori ClickOnce rakendus nõuab ühilduvat 64-bitist operatsioonisüsteemi.
> * PDF-failide eelvaateks soovitame kasutada tänapäevasi brausereid, nagu Microsoft Edge (viimane avalikult saadaolev versioon) Windows 10-s või Chrome (viimane avalikult saadaolev versioon) Windows 10-s, Windows 8.1-s, Windows 8-s, Windows 7-s või tahvelarvutis Google Nexus 10.
>   Võrgunõuded
> * Dynamics 365 for Talent on mõeldud võrkudele, mille latentsus on kuni 250–300 millisekundit (ms). See on latentsus brauserikliendist Microsoft Azure’i andmekeskusse, mis majutab rakendust Dynamics 365 for Talent. Soovitame teilt testida võrgulatentsust veebiaadressil [www.azurespeed.com](https://www.azurespeed.com "Azure’i latentsustest").
> * Ribalaiuse nõuded Dynamics 365 for Talenti puhul sõltuvad teie stsenaariumist. Kõige tüüpilisemad stsenaariumid nõuavad ribalaiust rohkem kui 50 kilobaiti sekundis (KB/s).
> 
> [!WARNING]
> Ärge arvutage ribalaiuse nõudeid kliendi asukohast, korrutades kasutajate arvu minimaalsete ribalaiuse nõuetega. Antud asukoha samaaegset kasutust on väga keeruline arvutada. Ribalaiuse nõuete pärast muret tundvad kliendid peaksid kasutama rakenduse Dynamics 365 for Talent eelvaateversiooni.

## <a name="supported-microsoft-office-applications"></a>Toetatud Microsoft Office’i rakendused

* Microsoft Exceli ja Wordi lisandmoodulite käivitamiseks peab teil olema installitud Windowsile või Macile mõeldud Microsoft Office 2016. Versiooninõuete kohta lisateabe saamiseks vaadake teemat [Office’i integratsiooni tõrkeotsing](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office’i integratsiooni tõrkeotsing").
* Funktsiooniga Ekspordi Excelisse või Ekspordi Wordi loodud dokumentide vaatamiseks peab teil olema installitud Microsoft Office 2007 või uuem versioon.

## <a name="update-policy"></a>Värskenduspoliitika

Microsoft Dynamics 365 for Talenti pakutakse pilveteenusena. Microsoft värskendab rakendust Dynamics 365 for Talent pidevalt ja automaatselt.

Värskendusi antakse välja regulaarselt ja need tehakse kättesaadavaks kõikides keskkondades.  Dynamics 365 for Talenti tugi põhineb [Microsofti toe elutsükli poliitikal](https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy "Microsofi toe elutükkel"), kust leiate terviklikud ja ennustatavad juhised tootetoe saadavuse kohta.
