---
title: Ressursi võimsuse sünkroonimine
description: See teema annab teavet ressursi võimsuse sünkroonimise kohta kalendrite ja projektide vahel.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760522"
---
# <a name="synchronize-resource-capacity"></a>Ressursi võimsuse sünkroonimine

[!include [banner](../includes/banner.md)]

Ressursi sünkroonimise protsessid aitavad tagada, et kalendri ja aluskalendri teave arvestab projekti ressursiplaanimisega. Kalendri muutmisel teevad protsessid projektiressursside plaanimises vajalikud värskendused. Protsessid aitavad ka jõudlust parandada, kuna kalendriressursi teave sünkroonitakse eelnevalt. Seetõttu toimub ressursiplaanimise teabe uuendamine kiiremini. Soovitame plaanida protsessid ühekordsete asemel partiina. Vastasel korral on olemas oht, et keegi unustab hõlmavad kuupäevad, millal teavet viimati sünkrooniti. Kui hõlmavaid kuupäevi ei kasutata, võivad kuupäevade sünkroonimisel tekkida vahed.

![Kalendri sünkroonimine](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Ressursi võimsuse kokkuvõtete sünkroonimine

Sünkroonimisprotsess on mõeldud kogu ressursikalendri teabe sünkroonimiseks. See teave sisaldab peamist kalendriteavet kõigi muudatuste kohta projekti ressursikalendri võimsuse tabelis. Kui projektile lisatakse uusi ressursse, aitab sünkroonimine tagada, et värskendatud kalendriteave oleks saadaval. See sünkroonimine võib toimuda igal ajal.

Soovitame kasutada partiid. Need valikud on võimsuse reserveerimiste sünkroonimisel saadaval.

1. Valige **Projektihaldus ja raamatupidamine** &gt; **Perioodiline** &gt; **Võimsuse sünkroonimine** &gt; **Ressursside võimsuse kokkuvõtete sünkroonimine**.
2. Määrake valikud järgmises tabelis.

    | Suvand      | Kirjeldus |
    |-------------|-------------|
    | Perioodi kood | Soovi korral võite valida pearaamatu kuupäevavahemiku koodi ressursi võimsuse kokkuvõtete sünkroonimisprotsessi alguse ja lõpu kuupäevade määramiseks. |
    | Alguskuupäev  | Sisestage ressursi võimsuse kokkuvõtete sünkroonimisprotsessi alguskuupäev. |
    | Lõppkuupäev    | Sisestage ressursi võimsuse kokkuvõtete sünkroonimisprotsessi lõppkuupäev. |

[![Sünkroonimisprotsess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)
