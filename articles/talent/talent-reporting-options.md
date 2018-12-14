---
title: "Talenti aruandlusvõimalused"
description: "Selles teemas selgitatakse, kuidas lahendada probleemi, mille käigus klient soovib kohandada rakenduse Microsoft Dynamics 365 for Talent aruandeid või luua uusi aruandeid."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a>Talenti aruandlusvõimalused

[!include [banner](includes/banner.md)]

**Keskkonna üksikasjad**

Probeem kehtib kõigile keskkondadele.

**Sümptom**

Klient soovib kohandada rakenduse Microsoft Dynamics 365 for Talent aruandeid või luua uusi aruandeid.

**Probleem**

Kasutaja ei saa kohandada manustatud Microsoft Power BI aruandeid.

**Lahendus**

- Core HR-i andmete voogu teenusesse Common Data Service for Apps saab esitada rakendusse Power BI Desktop PowerAppsi CDS-konnektori kaudu. Pange tähele, et teenus Common Data Service for Apps sisaldab Core HR-i andmete alamkogumit. Lisateavet Power BI ja armatuurlaudade kohta vt jaotisest [Power BI aruannete ja armatuurlaudade loomine PowerAppsi teenusega Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).
- Mõnedele aruannetele on Talentis saadaval elektrooniline aruandlus. Kliendi juhitud kohandamisi saab teha ER-i konfiguratsioonivalikute kaudu.
- Andmed saab eksportida Microsoft Excelisse või Microsoft Wordi kasutades eri andmeüksuseid, mida rakendus Talent pakub Microsoft Office’i integratsiooni kaudu.

**Pikaajaline lahendus**

Saadaval on Power BI lisavalikud ning teenusesse Common Data Service for Apps kuulub rohkem andmeid ja üksuseid.

