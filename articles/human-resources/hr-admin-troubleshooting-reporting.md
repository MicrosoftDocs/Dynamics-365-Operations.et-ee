---
title: Aruandlusvalikud
description: Selles artiklis selgitatakse, kuidas lahendada probleemi, mille käigus klient soovib kohandada rakenduse Microsoft Dynamics 365 Human Resources aruandeid või luua uusi aruandeid.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 64a03724d81745373d028d76a8cc64aab66efdbb
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053295"
---
# <a name="reporting-options"></a>Aruandlusvalikud

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Keskkonna üksikasjad**

Probeem kehtib kõigile keskkondadele.

**Sümptom**

Klient soovib kohandada rakenduse Microsoft Dynamics 365 Human Resources aruandeid või luua uusi aruandeid.

**Väljasta**

Kasutaja ei saa manustatud Microsoft Power BI aruandeid kohandada.

**Lahendus**

- Rakenduse Human Resources andmete voogu teenusesse Dataverse saab esitada rakendusse Power Apps Dataverse’i konnektori kaudu Power BI Desktop. Pange tähele, et teenus Dataverse sisaldab rakenduse Human Resources andmete alamkogumit. Lisateavet Power BI ja armatuurlaudade kohta vt teemast [Loo Power BI aruannete ja armatuurlaudade loomine teenuse Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) abil.
- Mõnedele aruannetele on rakenduses Human Resources saadaval elektrooniline aruandlus. Kliendi juhitud kohandamisi saab teha ER-i konfiguratsioonivalikute kaudu.
- Andmed saab eksportida Microsoft Excelisse või Microsoft Wordi, kasutades mitmesuguseid andmeüksuseid, mida rakendus Human Resources pakub Microsoft Office’i integratsiooni kaudu.

**Pikaajaline lahendus**

Saadaval on Power BI lisasuvandid ning teenusesse Dataverse kuulub rohkem andmeid ja üksuseid.


[!INCLUDE[footer-include](../includes/footer-banner.md)]