---
title: Impordi valuutavahetuskursid.
description: "Kui juriidiline isik on saanud arveid välisvaluutas, on vaja välisvaluuta kohalikku valuutasse teisendada. See tähendab, et vaja on erinevate valuutade ajakohaseid vahetuskursse. Selles teemas antakse ülevaade vajalikest sätetest ja töötlemisest vahetuskursside pakkujate (nt Euroopa Keskpank ja Venemaa Keskpank) Internetis avaldatud vahetuskursside importimiseks."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: df07066371cb7d9c69976c9714b6d2fe456a0308
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="import-currency-exchange-rates"></a>Impordi valuutavahetuskursid.

[!include[banner](../includes/banner.md)]


Kui juriidiline isik on saanud arveid välisvaluutas, on vaja välisvaluuta kohalikku valuutasse teisendada. See tähendab, et vaja on erinevate valuutade ajakohaseid vahetuskursse. Selles teemas antakse ülevaade vajalikest sätetest ja töötlemisest vahetuskursside pakkujate (nt Euroopa Keskpank ja Venemaa Keskpank) Internetis avaldatud vahetuskursside importimiseks.

Järgmised jaotised kirjeldavad teabevoogu, mida kasutatakse vahetuskursside importimise häälestamiseks ja töötlemiseks.

## <a name="configure-an-exchange-rate-provider"></a>Vahetuskursi pakkuja konfigureerimine
Enne vahetuskursside importimist tuleb seadistada andmed, mida nõuavad vahetuskursi pakkujad. Valige vahetuskursi pakkujad lehelt **Vahetuskursi pakkujate konfigureerimine**. Mõned vahetuskursi pakkujad sisalduvad Microsoft Dynamics 365 for Finance and Operationsi demoandmetes. Lehe juhtelementide kirjeldused leiate järgmisest tabelist.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Väli** | **Kirjeldus**                                                                                                                                                                                                             |
| **Nimi**  | Vahetuskursi pakkuja nimi.                                                                                                                                                                                     |
| **Võti**   | Pakkuja nõutud konfiguratsiooniteabe iga osa kordumatu ID. See teave lisatakse automaatselt iga vahetuskursi pakkuja puhul, kelle lisate, klõpsates nuppu **Lisa**. |
| **Väärtus** | Iga nupu teave. See teave lisatakse iga vahetuskursi pakkuja puhul, kelle lisate, klõpsates nuppu **Lisa**.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Impordi valuutavahetuskursid.
Saate importida vahetuskursse vahetuskursi pakkujate allikast ja seadistada neid lehel **Valuutakursid**. Vahetuskursse saab importida lehe **Impordi valuutakursid** kaudu. Järgmises tabelis kirjeldatakse välju, mida on importimisprotsessi edukaks lõpuleviimiseks vaja.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Väli**                              | **Kirjeldus**                                                                                                                                                                                                                                                                                                                                                             |
| **Vahetuskursi tüüp**                 | Vahetuskursi tüüp.                                                                                                                                                                                                                                                                                                                                                      |
| **Vahetuskursi pakkuja**             | Vahetuskursi pakkuja.                                                                                                                                                                                                                                                                                                                                                  |
| **Impordi seisuga**                       | See parameeter juhib seda, kas importida tänase kuupäeva või kuupäevavahemiku seisuga. Kui soovite kasutada kuupäevavahemikku, siis sisestage või valige alguse ja lõpu kuupäevad.                                                                                                                                                                                                                |
| **Loo vajalikud valuutapaarid**    | See märkeruut juhib valuutapaaride automaatset loomist, kui imporditavaid valuutapaare pole. Mõne pakkuja puhul ei pruugi see valik saadaval olla.                                                                                                                                                                                               |
| **Alista olemasolevad vahetuskursid**   | See märkeruut juhib olemasoleva vahetuskursi uuendamist valuutapaari puhul, kui konkreetse kuupäeva kohta on valuutakurss juba olemas. Kui te seda ruutu ei märgi, ei impordita konkreetsete kuupäevade valuutakurssi, kui teine valuutakurss on juba olemas.                                                                                       |
| **Vältida importimist riiklikel pühadel** | See märkeruut juhib valuutakursi importimist kuupäeval, mis on riigipüha. Näiteks kui märgite selle ruudu ja kasutate vahetuskursi pakkujana Euroopa Keskpanka, ei muuda süsteem vahetuskurssi praeguse juriidilise isikuga seotud riigipühal. Mõne pakkuja puhul ei pruugi see valik saadaval olla. |






