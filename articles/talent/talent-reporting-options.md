---
title: Talenti aruandlusvõimalused
description: Selles teemas selgitatakse, kuidas lahendada probleemi, mille käigus klient soovib kohandada rakenduse Microsoft Dynamics 365 for Talent aruandeid või luua uusi aruandeid.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304108"
---
# <a name="reporting-options-in-talent"></a>Talenti aruandlusvõimalused

[!include [banner](includes/banner.md)]

**Keskkonna üksikasjad**

Probeem kehtib kõigile keskkondadele.

**Sümptom**

Klient soovib kohandada rakenduse Microsoft Dynamics 365 for Talent aruandeid või luua uusi aruandeid.

**Väljastamine**

Kasutaja ei saa kohandada manustatud Microsoft Power BI aruandeid.

**Lahendus**

- Core HR-i andmete voogu teenusesse Common Data Service for Apps saab esitada rakendusse Power BI Desktop PowerAppsi CDS-konnektori kaudu. Pange tähele, et teenus Common Data Service for Apps sisaldab Core HR-i andmete alamkogumit. Lisateavet Power BI ja armatuurlaudade kohta vt teemast [Power BI aruannete ja armatuurlaudade loomine teenuse PowerApps Common Data Service abil](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).
- Mõnedele aruannetele on Talentis saadaval elektrooniline aruandlus. Kliendi juhitud kohandamisi saab teha ER-i konfiguratsioonivalikute kaudu.
- Andmed saab eksportida Microsoft Excelisse või Microsoft Wordi, kasutades mitmesuguseid andmeüksuseid, mida rakendus Talent pakub Microsoft Office’i integratsiooni kaudu.

**Pikaajaline lahendus**

Saadaval on Power BI lisasuvandid ning teenusesse Common Data Service for Apps kuulub rohkem andmeid ja üksuseid.
