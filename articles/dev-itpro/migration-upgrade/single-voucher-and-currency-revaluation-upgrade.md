---
title: "Ühe kande ja valuuta ümberhindamise täiendus"
description: "Mõned organisatsioonid sisestavad töölehti, mis sisaldavad ühte kannet, millel on rohkem kui üks klient või hankija ning nad käivitavad ka müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessi. See teema kirjeldab juhiseid, mida need organisatsioonid peaksid rakenduse Microsoft Dynamics 365 for Operations versiooni 1611 uuendamisel järgima."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7e0cd0c96ad0f30d56eefdc46a0a69160d864175
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a>Ühe kande ja valuuta ümberhindamise täiendus

[!include [banner](../includes/banner.md)]

Mõned organisatsioonid sisestavad töölehti, mis sisaldavad ühte kannet, millel on rohkem kui üks klient või hankija ning nad käivitavad ka müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessi. See teema kirjeldab juhiseid, mida need organisatsioonid peaksid rakenduse Microsoft Dynamics 365 for Operations versiooni 1611 uuendamisel järgima.

Järgige neid juhiseid, kui uuendate rakenduse Microsoft Dynamics 365 for Operations versiooni 1611.

1.  Enne rakendusele Dynamics 365 for Operations uuendamist käivitage müügi- ja ostureskontrole välisvaluuta ümberhindamise protsessid. Seadke välja **Meetod** väärtuseks **Arve kuupäev**. Luuakse ümberhindamiskanne, mis tühistab viimase välisvaluuta ümberhindamise. Seetõttu hinnatakse avatud kandeid nende algses arvestusvaluutas.
2.  Uuendage Dynamics 365 for Operationsi versioonile 1611.
3.  Käivitage müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessid uuesti. Seekord seadke välja **Meetod** väärtuseks **Standard**. Luuakse uus ümberhindamise kanne, mis põhineb praegustel valuutakurssidel. See kanne salvestab realiseerimata kasumi/kahjumi ja õige koondpearaamatukonto.





