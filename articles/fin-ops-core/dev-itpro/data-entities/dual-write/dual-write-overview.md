---
title: Reaalaja lähedane teabe integratsioon teenusega Common Data Service
description: Selles teemas antakse ülevaade integratsioonist rakendusega Finance and Operations ja Common Data Service.
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
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019742"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a>Reaalaja lähedane teabe integratsioon teenusega Common Data Service

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Praeguses digitaalmaailmas kasutavad äriökosüsteemid rakenduste Microsoft Dynamics 365 paketti tervikuna. Kuna inimeste, klientide, operatsioonide ja asjade Interneti (IoT) seadmete andmed voog liigub ühte allikasse, on olemas võimalus digitaalseks tagasiside ringiks. Selle kogemuse saavutamiseks on oluline integratsioon rakenduste Finance and Operations ja Dynamics 365 vahel. Mõned rakendused on ehitatud Common Data Service’i peale. Rakenduse Finance and Operations ja Common Data Service andmete integratsioon võimaldab teistel rakendustel sidusalt ja ladusalt Finance and Operationsiga ladusalt suhelda.

Rakendustekomplekt Finance and Operations ja Common Data Service pakuvad reaalajalähedast andmete sünkroonimist rakendustekomplekti Finance and Operations ja teiste Dynamics 365 rakenduste vahel topeltkirjutamise raamistiku kaudu. Katvus on lai ja ulatub 28 rakenduse valdkonnani. Eesmärk on pakkuda "ühtset Dynamics 365" kasutaja kogemust tõrgeteta andmevoos, mis ühendab äriprotsessid rakenduste vahel.

![Ülesehituse ülevaatlik diagramm](media/dual-write-overview.jpg)

Saadaval on järgmised väärtusettepanekud.

+ [Organisatsiooni hierarhia teenusesCommon Data Service](organization-mapping.md)
+ [Ettevõtte kontseptsioon rakendusesCommon Data Service](company-data.md)
+ [Hankija koondandmete haldamine](customer-mapping.md)
+ [Integreeritud pearaamat](ledger-mapping.md)
+ [Ühendatud toote kasutusfunktsionaalsus](product-mapping.md)
+ [Müüja koondandmete haldamine](vendor-mapping.md)
+ [Integreeritu kohad ja laod](sites-warehouses-mapping.md)
+ [Integreeritud maksude koondandmed](tax-mapping.md)

## <a name="system-requirements"></a>Süsteeminõuded

Sünkroonne, kahesuunaline, reaalaja lähedased andmevood nõuavad järgmisi versioone.

+ Rakenduse Microsoft Dynamics 365 for Finance and Operations versioon 10.0.4 (november 2019) platvormivärskendusega 28 või uuem
+ Microsoft Dynamics 365 for Customer Engagementi versioon 9.1 (4.2) või uuem

## <a name="setup-instructions"></a>Seadistusjuhised

Järgige neid etappe rakendustekomplekti Finance and Operations ja Common Data Servicei integratsiooni seadistamiseks.
    
1. Topeltkirjutamise süsteemi sätestamiseks vaadake [üksikasjalikku juhendit](https://aka.ms/dualwrite-docs) topelkirjutamise eelvaate kohta.
2. Laadige alla ja installige lahendus [topeltkirjutuse kaudu Fin Opsi ja CDS/CE integratsioonist](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammeri grupis. Pakett sisaldab viit lahendust:

    + Dynamics365Company
    + Valuuta vahetuskursi määrad
    + Dynamics365FinanceAndOperationsCommon
    + Dynamics365FinanceCommon
    + Dynamics365SupplyChainCommon

3. Järgige täitmistellimust [esialgsete viiteandmete sünkroonimiseks](initial-sync.md).
4. Kui teil esineb topeltkirjutamise sünkroonimisel probleeme, vaadake teemat [Tõrkeotsingu juhend andmete integreerimiseks ](dual-write-troubleshooting.md).

> [!IMPORTANT]
> Te ei saa käivitada topeltkirjutamist [ja raha väljavaadet](../../../../supply-chain/sales-marketing/prospect-to-cash.md) kõrvuti. Kui kasutate raha väljavaate lahendust, peate selle desinstallima. Samuti peate keelama kliendi ja hankija topeltkirjutamise mallid, mis on osa raha väljavaate lahendusest.
