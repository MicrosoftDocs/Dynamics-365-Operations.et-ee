---
title: Peaaegu reaalaja andmete integreerimine Finance and Operationsi ja Common Data Service’i vahel.
description: Selles teemas antakse ülevaade integratsioonist rakendusega Microsoft Dynamics 365 for Finance and Operations ja Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797224"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a>Peaaegu reaalaja andmete integreerimine Finance and Operationsi ja Common Data Service’i vahel.

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Praeguses digitaalmaailmas kasutavad äriökosüsteemid rakenduse Microsoft Dynamics 365 paketti tervikuna. Kuna inimeste, klientide, operatsioonide ja asjade Interneti (IoT) seadmete andmed voog liigub ühte allikasse, on olemas võimalus digitaalseks tagasiside ringiks. Selle kogemuse saavutamiseks on oluline integratsioon rakenduste Dynamics 365 for Finance and Operations ja Dynamics 365 for Customer Engagementi rakenduste vahel. Customer Engagementi rakendused on ehitatud Common Data Service’i peale. Finance and Operationsi andmete integreermine Common Data Service’iga võimaldab Customer Engagementi rakendustel ühtselt ja ladusalt suhelda Finance and Operationsis.

Finance and Operations ja Common Data Service pakuvad reaalajalähedast andmete sünkroonimist Finance and Operationsi ja Customer Engagementi rakenduste vahel topeltkirjutamise raamistiku kaudu. Katvus on lai ja ulatub 28 Finance and Operationsi valdkonnani. Eesmärk on pakkuda "ühtset Dynamics 365" kasutaja kogemust tõrgeteta andmevoos, mis ühendab äriprotsessid rakenduste vahel.

![Ülesehituse ülevaatlik diagramm](media/dual-write-overview.jpg)

Klientide jaoks on saadaval järgmised väärtusettepanekud.

+ [Organisatsiooni hierarhia teenusesCommon Data Service](dual-write-organization.md)
+ [Ettevõtte kontseptsioon rakendusesCommon Data Service](dual-write-company.md)
+ [Hankija koondandmete haldamine](dual-write-customer.md)
+ [Müüja koondandmete haldamine](dual-write-vendor.md)
+ Ühendatud tooteetalon

## <a name="system-requirements"></a>Süsteeminõuded

Sünkroonne, kahesuunaline, reaalaja lähedased andmevood nõuavad järgmisi versioone.

+ Rakenduse Microsoft Dynamics 365 for Finance and Operations versioon 10.0.4 (november 2019) platvormivärskendusega 28 või uuem
+ Microsoft Dynamics 365 for Customer Engagementi versioon 9.1 (4.2) või uuem

## <a name="setup-instructions"></a>Seadistusjuhised

Seadistage rakenduste Finance and Operations ja Common Data Service vaheline integratsioon.
    
1. Topeltkirjutamise süsteemi sätestamiseks vaadake [üksikasjalikku juhendit](https://aka.ms/dualwrite-docs) topelkirjutamise eelvaate kohta.
2. Laadige alla ja installige lahendus rakenduste [Finance and Operations, Common Data Service ja Customer Engagementi integreerimise](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096)Yammer rühmast. Pakett sisaldab viit lahendust:

    + Dynamics365Company
    + Valuuta vahetuskursi määrad
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Järgige täitmistellimust [esialgsete viiteandmete sünkroonimiseks](dual-write-initial.md).
4. Kui teil esineb topeltkirjutamise sünkroonimisel probleeme, vaadake teemat [Tõrkeotsingu juhend andmete integreerimiseks ](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Te ei saa käivitada topeltkirjutamist [ja raha väljavaadet](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) kõrvuti. Kui kasutate raha väljavaate lahendust, peate selle desinstallima. Samuti peate keelama kliendi ja hankija topeltkirjutamise mallid, mis on osa raha väljavaate lahendusest.
