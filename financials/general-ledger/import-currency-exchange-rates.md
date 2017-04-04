---
title: Impordi valuutavahetuskursid.
description: "Kui juriidiline isik on saanud välisvaluutas, tuleb muuta valuuta kohalikku vääringusse. See tähendab, et uuema vahetuskursiga erinevate valuutade eest nõutakse. Selles teemas antakse ülevaade seadete ja töötlemise importimise internetis avaldatud vahetuskurss rahastajate, näiteks Euroopa ja Venemaa keskpanga valuutakursi viitemääradena."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf66a1b1c9314b454223274810a21913d54b702d
ms.lasthandoff: 03/31/2017


---

# <a name="import-currency-exchange-rates"></a>Impordi valuutavahetuskursid.

Kui juriidiline isik on saanud välisvaluutas, tuleb muuta valuuta kohalikku vääringusse. See tähendab, et uuema vahetuskursiga erinevate valuutade eest nõutakse. Selles teemas antakse ülevaade seadete ja töötlemise importimise internetis avaldatud vahetuskurss rahastajate, näiteks Euroopa ja Venemaa keskpanga valuutakursi viitemääradena.

Järgmistes punktides kirjeldatakse teabe, mida kasutatakse loomiseks ja töötlemiseks valuutakursside import.

## <a name="configure-an-exchange-rate-provider"></a>Konfigureerida vahetuskursi pakkujaga
Valuutakursside importimiseks peate seadistama teenusepakkujad, kes pakuvad vahetuskursside vajalikku teavet. Kasutamine ning **konfigureerida vahetuskursi pakkujaid** lehe vahetuskursi osutajate valimiseks. Mõned vahetuskursi pakkujad on kaasas demo andmeid Microsoft Dynamics 365 toiminguteks. Selle lehe juhtelementide kirjeldused leiate järgmistest tabelitest.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field** | **Description**                                                                                                                                                                                                             |
| **Name**  | Vahetuskursi pakkuja nimi.                                                                                                                                                                                     |
| **Võti**   | Pakkuja nõutud konfiguratsiooniteabe iga osa kordumatu ID. See teave lisatakse automaatselt iga vahetuskursi teenusepakkuja lisada, kui klõpsate selle **lisa** nuppu. |
| **Value** | Iga nupu teave. See teave lisatakse iga vahetuskursi teenusepakkuja lisada, kui klõpsate selle **lisa** nuppu.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Impordi valuutavahetuskursid.
Saate importida vahetuskursside vahetuskursi pakkujad allikas ja ning selle **Valuutavahetuskursid** lehel. Kasutamine ning **importida Valuutavahetuskursid** lehe vahetuskursside importida. Järgnev tabel annab kirjeldused protsessi edukalt täita nõutavad väljad.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**                              | **Description**                                                                                                                                                                                                                                                                                                                                                             |
| **Exchange rate type**                 | Vahetuskurss tüüp.                                                                                                                                                                                                                                                                                                                                                      |
| **Exchange rate provider**             | Vahetuskursi pakkujaga.                                                                                                                                                                                                                                                                                                                                                  |
| **Import as of**                       | See parameeter juhib kas importida tänasel kuupäeval või kuupäevavahemikul. Kui soovite kasutada kuupäevavahemiku, sisestage või valige algus- ja.                                                                                                                                                                                                                |
| **Create necessary currency pairs**    | See ruut haldab automaatse loomise valuutapaaride, kui imporditud valuutapaaride ei ole. See suvand ei pruugi olla saadaval mõned pakkujad.                                                                                                                                                                                               |
| **Override existing exchange rates**   | See ruut kui vahetuskursi konkreetsel kuupäeval juba olemas haldab värskenduse olemasoleva vahetuskursi valuuta paari. Kui valite märkeruudu, vahetuskursi konkreetseteks kuupäevadeks ei impordita kui teise vahetuskurss on juba olemas.                                                                                       |
| **Prevent import on national holiday** | Selle ruudu märkimisel haldab vahetuskursi impordi kuupäeva, mis on riigipüha. Näiteks kui märgite selle ruudu ja kasutada Euroopa Keskpanga vahetuskursi pakkujaga, süsteem ei uuenda vahetuskurss on riigipüha, mis on seotud praeguse juriidilise. See suvand ei pruugi olla saadaval mõned pakkujad. |




