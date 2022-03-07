---
title: Koosluse versiooni määramine
description: Nõudluse koostamise ajal, kui kaubal on vaiketellimuse tüüp Tootmine, leiab plaanimismootor laoalal põhineva kehtiva koosluse versiooni.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 370091eed4ee050031d5d135aa7b1d8d0fe82491
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570965"
---
# <a name="determine-the-bom-version"></a>Koosluse versiooni määramine

[!include [banner](../includes/banner.md)]

Nõudluse koostamise ajal, kui kaubal on vaiketellimuse tüüp Tootmine, leiab plaanimismootor laoalal põhineva kehtiva koosluse versiooni. 

Laoala dimensioon on alati teada ja nimetatud nõudluskandes. Kasutatava koosluse versiooni määramiseks kasutatakse järgmist protsessi.

-   Kui nõudelaoalal on kauba jaoks määratud koosluse versioon, kasutatakse seda laoalapõhist kooslust.
-   Kui nõudelaoalal pole kauba jaoks määratud koosluse versiooni, kasutatakse üldkooslust. Üldkooslus ei nimeta laoala ja see kehtib mitme laoala korral. Kui üldkooslus on olemas, siis kasutatakse seda.
-   Kui ei ole ühtegi kasutuselolevat koosluse versiooni, lõpeb siinkohal nõudluse kooslusearvutus.

Kehtiv koosluse versioon, laoalapõhine või üldine, peab vastama nõutavatele kuupäeva ja koguse kriteeriumidele.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]