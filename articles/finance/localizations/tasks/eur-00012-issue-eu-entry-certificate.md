---
title: EUR-00012 EL-i kandesertifikaadi väljastamine
description: See protseduur selgitab EL-i kandesertifikaadi lubamist, kliendikonto konfigureerimist kandesertifikaatide kasutamiseks ja sertifikaadi väljastamist.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustTable, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustEntryCertificateJour_W, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b20f7d498439f2b2064d52ab621225f3c35ca8b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4984788"
---
# <a name="eur-00012-issue-an-eu-entry-certificate"></a>EUR-00012 EL-i kandesertifikaadi väljastamine

[!include [banner](../../includes/banner.md)]
See protseduur selgitab EL-i kandesertifikaadi lubamist, kliendikonto konfigureerimist kandesertifikaatide kasutamiseks ja sertifikaadi väljastamist. Protseduuri loomisel kasutati demoettevõtte DEMF andmeid.


## <a name="enable-entry-certificate-management"></a>Luba kandesertifikaadi haldamine
1. Minge jaotisse Müügireskontro > Seadistus > Müügireskontro parameetrid.
2. Klõpsake vahekaarti Saadetised.
3. Laiendage jaotist Kandesertifikaat.
4. Valige väljal Luba kandesertifikaadi haldus suvand Jah.
5. Valige väljal Luba kandesertifikaadi väljastamine suvand Jah.
6. Klõpsake vahekaarti Numbriseeriad.
7. Leidke ja valige loendist rida Kandesertifikaat.
8. Sisestage või valige väärtus väljal Numbriseeria kood.

## <a name="set-up-a-customer"></a>Kliendi seadistamine
1. Avage Müügireskontro > Kliendid > Kõik kliendid.
2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja Konto väärtuse DE-015 järgi.
3. Avage kliendi konto üksikasjad.
4. Klõpsake nuppu Redigeeri.
5. Laiendage jaotist Arve ja tarne.
6. Valige väljal Kandesertifikaat on nõutav suvand Jah.
7. Valige väljal Väljasta kandesertifikaat suvand Jah.
8. Klõpsake nuppu Salvesta.

## <a name="create-an-eu-entry-certificate-automatically"></a>EL-i kandesertifikaadi automaatne loomine
1. Avage Müügireskontro > Tellimused > Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Valige või sisestage väärtus väljal Kliendi konto.
4. Klõpsake nuppu OK.
5. Sisestage või valige väärtus väljal Kaubakood.
6. Klõpsake nuppu Salvesta.
7. Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.
8. Klõpsake valikut Saatelehe sisestamine.
9. Laiendage jaotist Parameetrid.
10. Valige väljal Kogus väärtus Kõik.
11. Tühjendage ruut Väljasta kandesertifikaat.
    * Kandesertifikaadi saab väljastada saatelehe sisestamise või tellimuse arveldamise ajal. Hiljem väljastamiseks jätke ruut Väljasta kandesertifikaat tühjaks.  
12. Klõpsake nuppu OK.
13. Klõpsake nuppu OK.
14. Klõpsake toimingupaanil valikut Arve.
15. Klõpsake valikut Arve.
    * Kontrollige, kas ruudud Kandesertifikaat on nõutav ja Väljasta kandesertifikaat jaotises Ülevaade on märgitud.  Saate valida ka ruudu Prindi kandesertifikaat, et lubada sertifikaadi printimine.  
16. Klõpsake nuppu OK.
17. Klõpsake nuppu OK.
18. Klõpsake toimingupaanil valikut Arve.
19. Klõpsake valikut Arve.
20. Klõpsake toimingupaanil valikut Arve.
21. Klõpsake suvandit Kuva väljastatud kandesertifikaadid.
22. Klõpsake Prindi.
23. Sulgege leht.
24. Klõpsake valikut Muuda olekut.
25. Valige suvand väljal Uus olek.
26. Klõpsake nuppu OK.
27. Sulgege leht.

## <a name="create-an-eu-entry-certificate-manually"></a>EL-i kandesertifikaadi käsitsi loomine
1. Klõpsake toimingupaanil valikut Arve.
2. Klõpsake suvandit Loo kandesertifikaat.
3. Klõpsake nuppu OK.
4. Klõpsake toimingupaanil valikut Arve.
5. Klõpsake suvandit Kuva väljastatud kandesertifikaadid.

