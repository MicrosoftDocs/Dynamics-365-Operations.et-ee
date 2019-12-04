---
title: Talenti aruandlusvõimalused
description: Selles teemas selgitatakse, kuidas lahendada probleemi, mille käigus klient soovib kohandada rakenduse Microsoft Dynamics 365 Talent aruandeid või luua uusi aruandeid.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ecbeb03b535f19131ddc6649d005702876bab65c
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772961"
---
# <a name="reporting-options-in-talent"></a>Talenti aruandlusvõimalused

[!include [banner](includes/banner.md)]

**Keskkonna üksikasjad**

Probeem kehtib kõigile keskkondadele.

**Sümptom**

Klient soovib kohandada rakenduse Microsoft Dynamics 365 Talent aruandeid või luua uusi aruandeid.

**Väljastamine**

Kasutaja ei saa kohandada manustatud Microsoft Power BI aruandeid.

**Lahendus**

- Core HR-i andmete voogu teenusesse Common Data Service saab esitada rakendusse Power Apps Common Data Service’i konnektori kaudu Power BI Desktop. Pange tähele, et teenus Common Data Service sisaldab Core HR-i andmete alamkogumit. Lisateavet Power BI ja armatuurlaudade kohta vt teemast [Loo Power BI aruannete ja armatuurlaudade loomine teenuse Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) abil.
- Mõnedele aruannetele on Talentis saadaval elektrooniline aruandlus. Kliendi juhitud kohandamisi saab teha ER-i konfiguratsioonivalikute kaudu.
- Andmed saab eksportida Microsoft Excelisse või Microsoft Wordi, kasutades mitmesuguseid andmeüksuseid, mida rakendus Talent pakub Microsoft Office’i integratsiooni kaudu.

**Pikaajaline lahendus**

Saadaval on Power BI lisasuvandid ning teenusesse Common Data Service kuulub rohkem andmeid ja üksuseid.
