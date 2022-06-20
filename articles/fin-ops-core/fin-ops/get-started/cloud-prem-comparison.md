---
title: Pilvepõhiste ja kohapealsete funktsioonide võrdlus
description: Artikkel näitab, millised funktsioonid on pilves ja valdustes toetatud.
author: sericks007
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-11-29
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: 4096089978032f150bf6d711711a948cf1d3232f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879771"
---
# <a name="comparison-of-cloud-and-on-premises-features"></a>Pilvepõhiste ja kohapealsete funktsioonide võrdlus

[!include [banner](../includes/banner.md)]

See artikkel näitab pilves vs ettevõttes asuvate funktsioonide võrdlust järgmiste rakenduste jaoks:

- [Dynamics 365 Finance](cloud-prem-comparison.md#dynamics-365-finance)
- [Dynamics 365 Supply Chain Management](cloud-prem-comparison.md#dynamics-365-supply-chain-management)
- [Dynamics 365 Commerce](cloud-prem-comparison.md#dynamics-365-commerce)
- [Dynamics 365 Human Resources](cloud-prem-comparison.md#dynamics-365-human-resources)

Lisatud on ka teave [arendus-ja haldamisfunktsioonide](cloud-prem-comparison.md#development-and-administration-features) kohta.

Järgmistes tabelites on loetletud rakendusvaldkonnad. Pilvepõhine ja asutusesisene tugi on loetletud funktsiooni tervikfunktsiooni kohta. Kui konkreetsed funktsioonid valdkonna üldistest funktsioonidest erinevad, loetletakse need eraldi real veerus Funktsioon.

## <a name="dynamics-365-finance"></a>Dynamics 365 Finance

| **Piirkond**             | **Funktsioon**                | **Pilv** | **Asutusesisene** |
|---------------------|-----------------------------|-----------|-----------------|
| Vastavus ja serdid        |                                                                                           | Jah       | Jah             |
|                                      | SOC 1 1. tüübi sert                                                                | Jah       | Ei              |
| Andmete haldus ja integreerimine      |                                                                                           | Jah       | Jah             |
|                                      | Andmete eksportimine oma andmelattu                                                    | Jah       | Jah             |
|                                      | Astmeliste värskenduste eksportimise lubamine andmeüksusse                                 | Jah       | Jah             |
|                                      | Andmeintegratsioon                                                                         | Jah       | Jah             |
| Dokumendihaldus                  |                                                                                           | Jah       | Jah             |
| Finantshaldus                 |                                                                                           | Jah       | Jah             |
| Spikker                                 |                                                                                           | Jah       | Ei              |
| Inimressursid                      |                                                                                           | Jah       | Jah             |
| Teave                         |                                                                                           | Jah       | Jah             |
|                                      | Elektrooniline aruandlus (ER)                                                                 | Jah       | Jah             |
|                                      | ER: LCS-iga integreerimine                                                                  | Jah       | Ei              |
|                                      | ER: SharePointiga integreerimine                                                           | Jah       | Ei              |
|                                      | ER: teenusega Regulatory Configuration Services (RCS) integreerimine                              | Jah       | Ei              |
|                                      | ER: kasutab ER-i hoidlate kaudu juurdepääsetavate ER-i konfiguratsioonide salvestusruumina kohalikku failisüsteemi | Ei        | Jah             |
|                                      | PowerBI.com-iga integreerimine                                                              | Jah       | Ei              |
|                                      | PowerBI Desktopiga integreerimine                                                          | Ei        | Jah             |
|                                      | Analüütikatööruumid                                                                     | Jah       | Ei              |
|                                      | Arukas äriprotsess: soovitused                                             | Jah       | Ei              |
|                                      | Power BI aruannete loomine OData abil, kasutades Power BI Desktopi või Exceli PowerQuery tööriistu    | Jah       | Ei              |
|                                      | SQL Serveri aruandlusteenused (SSRS) toetavad väljamastaapimist                                 | Jah       | Jah             |
|                                      | Telemeetria kantakse üle pilve                                                   | Jah       | Ei              |
| Elutsükli teenused                   |                                                                                           | Jah       | Jah             |
|                                      | Konfigureeritavad äriprotsessid                                                           | Jah       | Ei              |
| Lokaliseerimised                        |                                                                                           | Jah       | Jah             |
| Mobiilirakendus, tööruumid ja platvorm |                                                                                           | Jah       | Jah             |
| Office’i integreerimine                   |                                                                                           | Jah       | Jah             |
| Organisatsiooni haldus          |                                                                                           | Jah       | Jah             |
| Palk                              |                                                                                           | Jah       | Jah             |
|                                      | Otsedeposiit                                                                            | Jah       | Ei              |
| Projektihaldus ja -arvestus    |                                                                                           | Jah       | Jah             |
| Turve                             |                                                                                           | Jah       | Jah             |
| Teenuste haldamine                   |                                                                                           | Jah       | Jah             |
| Veebiklient                           |                                                                                           | Jah       | Jah             |
|                                      | Tegevuse salvestaja – tegevuse salvestiste salvestamine või laadimine BPM-i teegist                         | Jah       | Ei              |
| Tugi                              |                                                                                           | Jah       | Jah             |
|                                      | Juurdepääs toele spikri ja toe menüü kaudu                                             | Jah       | Ei              |
|                                      | Ärisündmused                                                                           | Jah       | Jah (ärisündmuste sisevõrgus saatmiseks / vastu võtmiseks on vajalik kas internetiühendus või kohandatud lõpp-punktid peavad olema rakendatud)              |

## <a name="dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management 

| **Piirkond**                | **Funktsioon**             | **Pilv** | **Asutusesisene** |
|-------------------------|-------------------|-----------|-----------------|
| Varahaldus                     |                                                                                           | Jah       | Jah             |
| Vastavus ja serdid        |                                                                                           | Jah       | Jah             |
|                                      | SOC 1 1. tüübi sert                                                                | Jah       | Ei              |
| Kuluarvestus                      |                                                                                           | Jah       | Jah             |
|                                      | Kuluarvestuse sisupakett Power BI jaoks                                                 | Jah       | Ei              |
|                                      | Kuluarvestuse tööruum mobiilse rakenduse jaoks                                                  | Jah       | Ei              |
| Kuluhaldus                      |                                                                                           | Jah       | Jah             |
|                                      | Kuluhalduse sisupakett Power BI jaoks                                                 | Jah       | Ei              |
| Andmete haldus ja integreerimine      |                                                                                           | Jah       | Jah             |
|                                      | Konfiguratsioonipõhine laiendus                                                            | Jah       | Ei              |
|                                      | Andmete eksportimine oma andmelattu                                                    | Jah       | Jah             |
|                                      | Astmeliste värskenduste eksportimise lubamine andmeüksusse                                 | Jah       | Jah             |
|                                      | Andmeintegratsioon                                                                         | Jah       | Jah             |
| Dokumendihaldus                  |                                                                                           | Jah       | Jah             |
| Spikker                                 |                                                                                           | Jah       | Ei              |
| Teave                         |                                                                                           | Jah       | Jah             |
|                                      | Elektrooniline aruandlus (ER)                                                                 | Jah       | Jah             |
|                                      | ER: LCS-iga integreerimine                                                                  | Jah       | Ei              |
|                                      | ER: SharePointiga integreerimine                                                           | Jah       | Ei              |
|                                      | ER: teenusega Regulatory Configuration Services (RCS) integreerimine                              | Jah       | Ei              |
|                                      | ER: kasutab ER-i hoidlate kaudu juurdepääsetavate ER-i konfiguratsioonide salvestusruumina kohalikku failisüsteemi | Ei        | Jah             |
|                                      | PowerBI.com-iga integreerimine                                                              | Jah       | Ei              |
|                                      | PowerBI Desktopiga integreerimine                                                          | Ei        | Jah             |
|                                      | Analüütikatööruumid                                                                     | Jah       | Ei              |
|                                      | Arukas äriprotsess: soovitused                                             | Jah       | Ei              |
|                                      | Power BI aruannete loomine OData abil, kasutades Power BI Desktopi või Exceli PowerQuery tööriistu    | Jah       | Ei              |
|                                      | SQL Serveri aruandlusteenused (SSRS) toetavad väljamastaapimist                                 | Jah       | Jah             |
|                                      | Telemeetria kantakse üle pilve                                                   | Jah       | Ei              |
| Varud                 |                                                                                           | Jah       | Jah             |
| Elutsükli teenused                   |                                                                                           | Jah       | Jah             |
|                                      | Konfigureeritavad äriprotsessid                                                           | Jah       | Ei              |
| Lokaliseerimised                        |                                                                                           | Jah       | Jah             |
| Tootmine                        |                                                                                           | Jah       | Jah             |
| Koondplaneerimine ja eelarvestamine      |                                                                                           | Jah       | Jah             |
| Planeerimise optimeerimine                |                                                                                           | Jah       | Ei              |
| Mobiilirakendus, tööruumid ja platvorm |                                                                                           | Jah       | Jah             |
| Office’i integreerimine                   |                                                                                           | Jah       | Jah             |
| Organisatsiooni haldus          |                                                                                           | Jah       | Jah             |
| Hanked             |                                                                                           | Jah       | Jah             |
|                                      | Väljaregistreerimine ostutaotlusest väliskataloogi                                   | Jah       | Ei              |
|                                      | Ostu- ja kulutusanalüüsi Power BI aruanded                                                  | Jah       | Ei              |
| Tooteteabe haldus       |                                                                                           | Jah       | Jah             |
| Toote koondandmed                  |                                                                                           | Jah       | Jah             |
| Tootmine                           |                                                                                           | Jah       | Jah             |
|                                      | Tootmisjõudluse Power BI aruanded                                                   | Jah       | Ei              |
| Projektihaldus ja -arvestus    |                                                                                           | Jah       | Jah             |
| Müük                                |                                                                                           | Jah       | Jah             |
|                                      | Müügi ja tulususe jõudluse Power BI aruanded                                      | Jah       | Ei              |
| Turve                             |                                                                                           | Jah       | Jah             |
| Teenuste halduse                   |                                                                                           | Jah       | Jah             |
| Tarneahela haldamine              |                                                                                           | Jah       | Jah             |
| Transpordihaldus            |                                                                                           | Jah       | Jah             |
| Hankija koostöö                 |                                                                                           | Jah       | Ei              |
| Laohaldus                 |                                                                                           | Jah       | Jah             |
|                                      | Mobiilne laorakendus                                                                      | Jah       | Jah             |
|                                      | Ladustamise Power BI aruanded                                                              | Jah       | Ei              |
| Veebiklient                           |                                                                                           | Jah       | Jah             |
|                                      | Tegevuse salvestaja – tegevuse salvestiste salvestamine või laadimine BPM-i teegist                         | Jah       | Ei              |
| Tugi                              |                                                                                           | Jah       | Jah             |
|                                      | Juurdepääs toele spikri ja toe menüü kaudu                                             | Jah       | Ei              |

## <a name="dynamics-365-commerce"></a>Dynamics 365 Commerce 

Kohapeal saadaolevate juurutuste võimaluste loendi nägemiseks vt [Kohapealseks juurutamiseks saadaolevad Commerce’i võimalused](../../../commerce/retail-onprem.md).

## <a name="dynamics-365-human-resources"></a>Dynamics 365 Human Resources 

| **Piirkond**         | **Funktsioon**         | **Pilv** | **Asutusesisene** |
|------------------|---------------------|-----------|-----------------|
| Kõik inimressursside valdkonnad | Kõik inimressursside funktsioonid | Jah       | Ei              |

## <a name="development-and-administration-features"></a>Arendus ja haldamisfunktsioonid

| **Piirkond**                   | **Funktsioon**                               | **Pilv** | **Asutusesisene** |
|----------------------------|-------------------------------------------|-----------|-----------------|
| Koostamine ja testimine             |                                           | Jah       | Jah             |
| Laiendatavus              |                                           | Jah       | Jah             |
| Jälgimine ja telemeetria   |                                           | Jah       | Jah             |
| Platvorm ühilduvus     |                                           | Jah       | Jah             |
| Hooldus                  |                                           | Jah       | Jah             |
|                            | Teeninduskeskkonnad                    | Jah       | Ei              |
| Trace Parser               |                                           | Jah       | Jah             |
| PerfTimer                  |                                           | Jah       | Jah\*           |
| Täiendamine                    |                                           | Jah       | Jah             |
|                            | Täiendamine                                   | Jah       | Ei              |
|                            | Eelmiste versioonide täiendamine ja tugi | Jah       | Ei              |
| Visual Studio arendus  |                                           | Jah       | Jah             |

\*Kohapealsetes keskkondades näitab PerfTimer ainult kliendi tulemusi.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
