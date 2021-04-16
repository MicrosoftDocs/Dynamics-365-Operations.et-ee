---
title: Valuutavahetuskursside importimine
description: See teema annab teavet vahetuskursi pakkujate avaldatud vahetuskursside importimise nõuete kohta.
author: EvgenyPopovMBS
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 20b8496bc3074eae6535eea4cfe0b254f2773e6a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823736"
---
# <a name="import-currency-exchange-rates"></a>Valuutavahetuskursside importimine

[!include [banner](../includes/banner.md)]

Kui juriidiline isik on saanud arveid välisvaluutas, tuleb välisvaluuta teisendada kohalikku valuutasse. See tähendab, et vaja on erinevate valuutade ajakohaseid vahetuskursse. Selles teemas antakse ülevaade vajalikest sätetest ja töötlemisest vahetuskursside pakkujate (nt Euroopa Keskpank ja Venemaa Keskpank) avaldatud vahetuskursside importimiseks.

Järgmised jaotised kirjeldavad teabevoogu, mida kasutatakse vahetuskursside importimise häälestamiseks ja töötlemiseks.

## <a name="configure-an-exchange-rate-provider"></a>Vahetuskursi pakkuja konfigureerimine
Enne vahetuskursside importimist tuleb seadistada andmed, mida nõuavad vahetuskursi pakkujad. Valige vahetuskursi pakkujad lehelt **Vahetuskursi pakkujate konfigureerimine**. Mõned vahetuskursi pakkujad sisalduvad Dynamics 365 Financei demoandmetes. Lehe juhtelementide kirjeldused leiate järgmisest tabelist.

| Field | Kirjeldus                   |
|-----------|-----------------------------------|
| **Nimi**  | Vahetuskursi pakkuja nimi.                                                                                                                                                                                     |
| **Võti**   | Pakkuja nõutud konfiguratsiooniteabe iga osa kordumatu ID. See teave lisatakse automaatselt iga vahetuskursi pakkuja puhul, kelle lisate. |
| **Value** | Iga nupu teave. See teave lisatakse iga vahetuskursi pakkuja puhul, kelle lisate.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Valuutavahetuskursside importimine
Saate importida vahetuskursse vahetuskursi pakkujate allikast ja lisada neid lehele **Valuuta vahetuskursi määrad**. Vahetuskursse saab importida lehe **Impordi valuutakursid** kaudu. Järgmises tabelis kirjeldatakse välju, mida on importimisprotsessi edukaks lõpuleviimiseks vaja.

| Field | Kirjeldus                   |
|-----------|-----------------------------------|
| **Vahetuskursi tüüp**                 | Vahetuskursi tüüp.                                                                                                                                                                                                                                                                                                                                                      |
| **Vahetuskursi pakkuja**             | Vahetuskursi pakkuja.                                                                                                                                                                                                                                                                                                                                                  |
| **Impordi seisuga**                       | See parameeter juhib seda, kas importida praeguse kuupäeva või konkreetse kuupäevavahemiku seisuga. Kui soovite kasutada kuupäevavahemikku, siis sisestage või valige algus- ja lõpukuupäevad.                                                                                                                                                                                                                |
| **Loo vajalikud valuutapaarid.**    | See märkeruut juhib valuutapaaride automaatset loomist, kui imporditavaid valuutapaare pole. Mõne pakkuja puhul ei pruugi see valik saadaval olla.                                                                                                                                                                                               |
| **Alista olemasolevad vahetuskursid**   | See märkeruut juhib olemasoleva vahetuskursi uuendamist valuutapaari puhul, kui konkreetse kuupäeva kohta on valuutakurss juba olemas. Kui te seda ruutu ei märgi, ei impordita konkreetsete kuupäevade valuutakurssi, kui teine valuutakurss on juba olemas.                                                                                       |
| **Vältida importimist riiklikel pühadel** | See märkeruut juhib valuutakursi importimist riigipüha kuupäeval. Näiteks kui märgite selle ruudu ja kasutate vahetuskursi pakkujana Euroopa Keskpanka, ei muuda süsteem vahetuskurssi praeguse juriidilise isikuga seotud riigipühal. Mõne pakkuja puhul ei pruugi see valik saadaval olla. |
| **Eelmise päeva kurss** | See märkeruut on saadaval, kui lubate funktsiooni **Praeguse või eelmise kuupäeva valuutavahetuskursi importimine** lehel **Funktsioonihaldus**. See märkeruut on saadaval ainult pakkujale, *Euroopa Keskpangale*. Valige see ruut, et importida valuuta vahetuskurss, mille Euroopa Keskpank avaldas eelmisel tööpäeval umbes kell 16:00 Kesk-Euroopa aja järgi. Vaikimisi on märkeruut valitud. Tühjendage see märkeruut, et importida samal tööpäeval avaldatud valuutavahetuskurss.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]