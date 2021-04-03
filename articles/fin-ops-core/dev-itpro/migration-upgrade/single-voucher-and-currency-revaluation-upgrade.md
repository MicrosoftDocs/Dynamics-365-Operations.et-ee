---
title: Üksiku kande töölehtede ja valuuta ümberarvutamise täiendus
description: Selles teemas kirjeldatakse, kuidas täiendada üksiku kande töölehtede ja valuuta ümberarvutamist.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fb4eca4933716105789d3bbc21dd374395211d1d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559517"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Üksiku kande töölehtede ja valuuta ümberarvutamise täiendus

[!include [banner](../includes/banner.md)]

Mõned organisatsioonid sisestavad töölehti, mis sisaldavad ühte kannet, millel on rohkem kui üks klient või hankija ning nad käivitavad ka müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessi. See teema kirjeldab juhiseid, mida need organisatsioonid peaksid rakenduse Microsoft Dynamics 365 for Operations versiooni 1611 värskendamisel järgima.

Järgige neid juhiseid, kui täiendate rakenduse Microsoft Dynamics 365 for Operations versioonile 1611.

1.  Enne rakendusele Finance and Operations täiendamist käivitage müügi- ja ostureskontrole välisvaluuta ümberhindamise protsessid. Seadke välja **Meetod** väärtuseks **Arve kuupäev**. Luuakse ümberhindamiskanne, mis tühistab viimase välisvaluuta ümberhindamise. Seetõttu hinnatakse avatud kandeid nende algses arvestusvaluutas.
2.  Uuendage versioonile 1611.
3.  Käivitage müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessid uuesti. Seekord seadke välja **Meetod** väärtuseks **Standard**. Luuakse uus ümberhindamise kanne, mis põhineb praegustel valuutakurssidel. See kanne salvestab realiseerimata kasumi/kahjumi ja õige koondpearaamatukonto.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]