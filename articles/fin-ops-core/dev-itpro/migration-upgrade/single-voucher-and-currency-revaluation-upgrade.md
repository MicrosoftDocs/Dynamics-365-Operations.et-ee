---
title: Üksiku kande töölehtede ja valuuta ümberarvutamiste täiendamine
description: Mõned organisatsioonid sisestavad töölehti, mis sisaldavad ühte kannet, millel on rohkem kui üks klient või hankija ning nad käivitavad ka müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessi. See teema kirjeldab juhiseid, mida need organisatsioonid peaksid rakenduse Microsoft Dynamics 365 for Operations versiooni 1611 värskendamisel järgima.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7c06e54c5be8d0a410b9f15f2a89def3076b4638
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681020"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Üksiku kande töölehtede ja valuuta ümberarvutamise täiendus

[!include [banner](../includes/banner.md)]

Mõned organisatsioonid sisestavad töölehti, mis sisaldavad ühte kannet, millel on rohkem kui üks klient või hankija ning nad käivitavad ka müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessi. See teema kirjeldab juhiseid, mida need organisatsioonid peaksid rakenduse Microsoft Dynamics 365 for Operations versiooni 1611 värskendamisel järgima.

Järgige neid juhiseid, kui täiendate rakenduse Microsoft Dynamics 365 for Operations versioonile 1611.

1.  Enne rakendusele Finance and Operations täiendamist käivitage müügi- ja ostureskontrole välisvaluuta ümberhindamise protsessid. Seadke välja **Meetod** väärtuseks **Arve kuupäev**. Luuakse ümberhindamiskanne, mis tühistab viimase välisvaluuta ümberhindamise. Seetõttu hinnatakse avatud kandeid nende algses arvestusvaluutas.
2.  Uuendage versioonile 1611.
3.  Käivitage müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessid uuesti. Seekord seadke välja **Meetod** väärtuseks **Standard**. Luuakse uus ümberhindamise kanne, mis põhineb praegustel valuutakurssidel. See kanne salvestab realiseerimata kasumi/kahjumi ja õige koondpearaamatukonto.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]