---
title: Dynamics 365 globaliseerimisteenused
description: Teema annab ülevaate Microsoft Dynamics 365 globaliseerimisteenustest.
author: JaneA07
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 3fa4d5ea028e4b8bb0981674db2743df40348a9a
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336604"
---
# <a name="dynamics-365-globalization-services"></a>Dynamics 365 globaliseerimisteenused

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 võrguteenuse võimaluste laiendamiseks saab konfigureerida järgmisi globaliseerumisteenuseid.

- **Regulatory Configuration Service (RCS)** toetab erinevat tüüpi elektrooniliste dokumentide ja aruannete konfigureerimist. RCS pakub täiustatud versiooni elektroonilise aruandluse (ER) kujundajast, kus konfiguratsioonihoidla on autonoomne teenus. Lisateavet vt teemast [Regulatory Configuration Service](rcs-overview.md).
- **E-arveldamine** koondab konfigureeritavad vormingud teisendusteks, digitaalallkirjadeks ja konfigureeritavateks integratsioonideks ühenduvuseks väliste veebiteenustega, sealhulgas sertifitseerimiseks ja reageerimiseks. Lisateavet leiate teemast [E-arveldus](e-invoicing-service-overview.md).
- **Maksuarvestus** pakub suuremat paindlikkust, toetades mitut maksu-ID-d, maksukoodi määramist, maksuarvestuse kujundajat ja käitusaja mootorit, et täita keerulisi maksueeskirju kogu maailmas. Lisateavet vt jaotisest [Maksuarvestus](global-tax-calcuation-service-overview.md).

Need globaliseerumisteenused pakuvad out-of-box integratsiooni järgmiste Dynamics 365 võrguteenustega.

| Võrguteenus | RCS | Elektrooniline arveldus | Maksuarvutus (eelversioon) |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | Jah | Jah | Jah | 
| Dynamics 365 Supply Chain Management | Jah | Jah | Jah | 
| Dynamics 365 Project Operations | Jah | Jah | Pole kohaldatav | 
| Dynamics 365 Commerce | Jah | Pole kohaldatav | Pole kohaldatav | 

> [!NOTE]
> RCS-i Azure'i geograafiliste asukohtade (geode) kättesaadavuse erinevuste tõttu võib selle teenuse konfigureerimine põhjustada kliendiandmete edastamise väljaspool rakenduse Dynamics 365 veebiteenuse jaoks valitud geograafilist piirkonda. Lisateavet vt teemast [Dynamics 365 ja Power Platform: saadavus, andmete asukoht, keel ja lokaliseerimine](https://aka.ms/rcs/D365Productavailabilityguide).