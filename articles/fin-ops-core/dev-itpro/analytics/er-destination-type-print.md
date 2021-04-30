---
title: ER-i sihtkoha tüübi printer
description: Selles teemas selgitatakse, kuidas konfigureerida printeri sihtkohta iga elektroonilise aruandluse (ER) vormingu komponendi FOLDER või FILE jaoks.
author: NickSelin
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 7749a458020de664d00e81ccf0e480ae459da617
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894000"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Printeri sihtkoht

[!include [banner](../includes/banner.md)]

Saate loodud dokumendi otse printimiseks otse võrguprinterisse saata.

## <a name="prerequisites"></a>Eeltingimused

Enne alustamist peate installima ja konfigureerima dokumendi marsruudi agendi ning seejärel registreerima võrgu printerid. Lisateavet saate teemast [Dokumendi marsruudivaliku agendi installimine võrguprintimise lubamiseks](./install-document-routing-agent.md).

## <a name="make-the-printer-destination-available"></a>Printeri sihtkoha kättesaadavaks tegemine

Selleks, et **printeri** sihtkoht oleks saadaval Microsofti Dynamics 365 Finance praeguses eksemplaris, minge **Funktsioonide halduse** tööruumi ja lülitage järgmised funktsioonid sisse selles järjekorras:

1. Teisenda elektroonilise aruandluse väljaminevad dokumendid Microsoft Office'i vormingutest PDF-iks
2. Dokumendi marsruudivaliku agent väljaminevate dokumentide elektroonilise aruandluse sihtkohana

[![ER printeri sihtkoha funktsiooni sisselülitamine funktsioonide halduses](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Kohaldatavus

**Printeri** sihtkoha saab konfigureerida ainult faili komponentide jaoks, mida kasutatakse väljundi loomiseks kas prinditavas PDF-vormingus (PDF-i liitmine või PDF-vormingu elemendid) või Microsoft Office Excel/Word vormingus. Kui väljund luuakse PDF-vormingus, saadetakse see printerisse. Kui väljund luuakse Microsoft Office vormingus, teisendatakse see automaatselt PDF-vormingusse ja seejärel saadetakse printerisse.

### <a name="limitations"></a>Kitsendused

**Printeri** sihtkohta rakendatakse ainult pilve juurutamiseks.

### <a name="use-the-printer-destination"></a>Printimise sihtkoha kasutamine

1. Seadke **Lubatud** suvand väärtusele **Jah**, et saata loodud dokument printerisse.
2. Valige väljal **Printeri nimi** vajalik võrguprinter.
3. Seadke suvand **Kas soovite salvestada printimise arhiivi?** väärtusele **Jah**, et salvestada loodud väljund printimise arhiivi, nii et see on edasiseks printimiseks saadaval. Arhiveeritud väljundi juurde pääsemiseks hiljem avage **Organisatsiooni haldus** \> **Päringud ja aruanded** \> **Aruannete arhiiv**.

[![Printimise sihtkoha kasutamine](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Suvand **Teisendamine PDF-iks** ei pea **Printeri** sihtkoha konfigureerimisel olema sisse lülitatud. PDF-i teisendamine printimiseks toimub isegi siis, kui suvand on välja lülitatud.

Kindla [lehe paigutuse](electronic-reporting-destinations.md#SelectPdfPageOrientation) kasutamiseks väljamineva Exceli vormingus dokumendi printimiseks, peate sisse lülitama suvandi **Teisenda PDF-iks**. Kui määrate suvandi **Teisenda PDF-iks** väärtuseks **Jah**, on saadaval väli **Lehe paigutus**. Väljal **Lehe paigutus** saate valida lehe paigutuse.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]