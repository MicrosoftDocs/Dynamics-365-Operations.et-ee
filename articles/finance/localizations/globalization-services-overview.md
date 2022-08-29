---
title: Dynamics 365 globaliseerimisteenused
description: See artikkel annab ülevaate Microsoft Dynamics 365 globaliseerimisteenustest.
author: kfend
ms.date: 04/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
ms.openlocfilehash: eebf74ab30a544f6561cf5782148d12b58d9c4b7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278228"
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
