---
title: ER-i sihtkoha tüübi printer
description: Sellest teemast leiate teatevt, kuidas konfigureerida printerit sihtkoha iga väljamineva dokumendi loomiseks konfigureeritud elektroonilise aruandluse (ER) vormingu iga kausta või faili komponendi jaoks kas PDFi või Microsoft Office vormingus (Excel\Word).
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019727"
---
# <a name="PrinterDestinationType"></a>Printeri sihtkoht

[!include [banner](../includes/banner.md)]

Saate loodud dokumendi otse printimiseks otse võrguprinterisse saata.

## <a name="prerequisites"></a>Eeltingimused

Enne alustamist peate installima ja konfigureerima dokumendi marsruudi agendi ning seejärel registreerima võrgu printerid. Lisateavet saate teemast [Dokumendi marsruudivaliku agendi installimine võrguprintimise lubamiseks](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).

## <a name="make-the-printer-destination-available"></a>Printeri sihtkoha kättesaadavaks tegemine

Selleks, et **printeri** sihtkoht oleks saadaval Microsofti Dynamics 365 Finance praeguses eksemplaris, minge **Funktsioonide halduse** tööruumi ja lülitage järgmised funktsioonid sisse selles järjekorras:

1. Teisenda elektroonilise aruandluse väljaminevad dokumendid Microsoft Office'i vormingutest PDF-iks
2. Dokumendi marsruudivaliku agent väljaminevate dokumentide elektroonilise aruandluse sihtkohana

[![ER printeri sihtkoha funktsiooni sisselülitamine funktsioonide halduses](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Kohaldatavus

**Printeri** sihtkoha saab konfigureerida ainult faili komponentide jaoks, mida kasutatakse väljundi loomiseks kas prinditavas PDF-vormingus (PDF-i liitmine või PDF-vormingu elemendid) või Microsoft Office Excel/Word vormingus. Kui väljund luuakse PDF-vormingus, saadetakse see printerisse. Kui väljund luuakse Microsoft Office vormingus, teisendatakse see automaatselt PDF-vormingusse ja seejärel saadetakse printerisse.

### <a name="limitations"></a>Kitsendused

See funktsioon on eelvaate funktsioon ja seda kasutatakse tingimustes, mida on kirjeldatud teemas [Microsoft Dynamics 365 eelvaadete kasutamise täiendavad tingimused](https://go.microsoft.com/fwlink/?linkid=2105274).

**Printeri** sihtkohta rakendatakse ainult pilve juurutamiseks.

### <a name="use-the-printer-destination"></a>Printimise sihtkoha kasutamine

1. Seadke **Lubatud** suvand väärtusele **Jah**, et saata loodud dokument printerisse.
2. Valige väljal **Printeri nimi** vajalik võrguprinter.
3. Seadke suvand **Kas soovite salvestada printimise arhiivi?** väärtusele **Jah**, et salvestada loodud väljund printimise arhiivi, nii et see on edasiseks printimiseks saadaval. Arhiveeritud väljundi juurde pääsemiseks hiljem avage **Organisatsiooni haldus** \> **Päringud ja aruanded** \> **Aruannete arhiiv**.

[![Printimise sihtkoha kasutamine](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Suvand **Teisendamine PDF-iks** ei pea **Printeri** sihtkoha konfigureerimisel olema sisse lülitatud. PDF-i teisendamine printimiseks toimub isegi siis, kui suvand on välja lülitatud.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)
