---
title: Süsteeminõuded
description: Selles artiklis kirjeldatakse rakenduse Microsoft Dynamics 365 Human Resources nõudeid.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f68b8f642ada1345e7097b5e7220e222b132b1dd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418186"
---
# <a name="system-requirements"></a>Süsteeminõuded

Selles artiklis kirjeldatakse rakenduse Microsoft Dynamics 365 Human Resources nõudeid. Lisaks tuuakse välja riigid ja piirkonnad, kus rakendus Human Resources on saadaval ning teave keelte ja Human Resourcesi andmete lokaliseerimise kohta.

## <a name="supported-web-browsers"></a>Toetatud veebibrauserid

Rakendust Human Resources saab kasutada kõigis järgmistes veebibrauserites, mis töötavad nimetatud operatsioonisüsteemis. 

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
> * Human Resources on mõeldud võrkudele, mille latentsus on kuni 250–300 millisekundit (ms). See on latentsus brauserikliendist Microsoft Azure’i andmekeskusse, mis majutab rakendust Human Resources. Soovitame teilt testida võrgulatentsust veebiaadressil [www.azurespeed.com](https://www.azurespeed.com "Azure’i latentsustest").
> * Ribalaiuse nõuded rakenduse Human Resources puhul sõltuvad teie stsenaariumist. Kõige tüüpilisemad stsenaariumid nõuavad ribalaiust rohkem kui 50 kilobaiti sekundis (KB/s).
> 
> [!WARNING]
> Ärge arvutage ribalaiuse nõudeid kliendi asukohast, korrutades kasutajate arvu minimaalsete ribalaiuse nõuetega. Antud asukoha samaaegset kasutust on väga keeruline arvutada. Ribalaiuse nõuete pärast muret tundvad kliendid peaksid kasutama rakenduse Human Resources eelvaateversiooni.

## <a name="supported-microsoft-office-applications"></a>Toetatud Microsoft Office’i rakendused

* Microsoft Exceli ja Wordi lisandmoodulite käivitamiseks peab teil olema installitud Windowsile või Macile mõeldud Microsoft Office 2016. Versiooninõuete kohta lisateabe saamiseks vaadake teemat [Office’i integratsiooni tõrkeotsing](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office’i integreerimise tõrkeotsing").
* Funktsiooniga Ekspordi Excelisse või Ekspordi Wordi loodud dokumentide vaatamiseks peab teil olema installitud Microsoft Office 2007 või uuem versioon.

## <a name="regional-availability-languages-and-localization"></a>Piirkondlik saadavus, keeled ja lokaliseerimine

Saate alla laadida PDF-faili riikide, piirkondade ja keelte kohta, mida Human Resources toetab teemast [Microsoft Dynamics 365 rahvusvaheline kättesaadavus](https://docs.microsoft.com/dynamics365/get-started/availability). 

> [!NOTE]
> Kui kasutajaliides on lokaliseeritud teistesse keeltesse, talletatakse kõik kasutajaandmed keeles, milles need sisestati. Saate luua e-kirju ja malle teistes keeltes, kuid sellised andmed nagu planeerimise teave on praegu saadaval ainult inglise keeles.

Kui olete arendaja, kes on huvitatud riigi- või piirkonnapõhiste kohanduste loomisest või luua lahendus mõnele riigile või piirkonnale, mida Microsoft praegu ei toeta, vt [Globaliseerumine](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).


[!INCLUDE[footer-include](../includes/footer-banner.md)]