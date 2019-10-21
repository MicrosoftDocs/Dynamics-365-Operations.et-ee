---
title: Jaemüügihierarhiad
description: Selles artiklis kirjeldatakse Dynamics 365 Retaili jaemüügihierarhiaid.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cb383c5bc5ad5d641db6f30e915ea43ba5980005
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025073"
---
# <a name="retail-hierarchies"></a>Jaemüügihierarhiad

[!include [banner](includes/banner.md)]

Selles artiklis kirjeldatakse Dynamics 365 Retaili jaemüügihierarhiaid.

Saate luua jaemüügi kategooriahierarhia, et korraldada jaemüügikanalite kaudu müüdavaid tooteid. Jaemüügi tootehierarhiate abil saate tooteid kategoriseerida või grupeerida. Seejärel saate neid tooteid kasutada tootesortimentide ja püsikliendiprogrammide loomiseks. Saate ka määrata toote atribuute ja omadusi, määrata hinnakujunduse struktuuri, kaasata tooteid tootekampaaniatesse ja kasutada tooteid aruandluseks. Saate luua ühe jaemüügi kategooriahierarhia esindama kõiki organisatsiooni tooteid ja kategooriaid ning seejärel kasutada seda kategooriahierarhiat mitmel eesmärgil. Samuti on teil võimalik luua mitu jaemüügi kategooriahierarhiat eriotstarbeks, näiteks tootekampaaniate jaoks. Jaemüügi tootehierarhia loomisel tuleb määrata kategooria hierarhia tüüp, et tuvastada kategooriahierarhia eesmärk. Näiteks viidatakse toote sirvimisel võrgus või kassas ainult tootehierarhiaid, millele on määratud tüüp **Jaemüügi navigeerimishierarhia**.

## <a name="retail-hierarchy-types"></a>Jaemüügihierarhia tüübid

Järgmises tabelis on loetletud saadaolevad jaemüügi kategooriahierarhia tüübid ja iga tüübi üldeesmärk.

| Kategooriahierarhia tüüp       | Eesmärk |
|-------------------------------|---------|
| Jaemüügi tootehierarhia      | Kasutage seda hierarhiatüüpi, et määratleda organisatsiooni üldine tootehierarhia. Saate seda hierarhiatüüpi kasutada tootesündmuste, hinnakujunduse ja kampaaniate, aruandluse ning sortimendi planeerimise jaoks. Selle hierarhiatüübe saab määrata ainult ühele jaemüügi tootehierarhiale. |
| Täiendav jaemüügi hierarhia | Kasutage seda hierarhiatüüpi mis tahes täiendavate jaemüügi kategooriahierarhiate puhul, mille soovite luua. Näiteks korraldate kevadel kampaania ujumisriiete müügiks. Seega kaasate ujumisriietest tooted eraldi kategooriahierarhiasse ja rakendate erinevatele tootekategooriatele kampaaniahinnad. |
| Jaemüügi navigeerimishierarhia   | Kasutage seda hierarhiatüüpi toodete grupeerimiseks ja korraldamiseks kategooriatesse, nii et tooteid saab sirvida võrgus või kassas. |

Jaemüügi kategooriahierarhia abil tooteid struktureerides saate seadistada ja hallata tooteatribuute ning omadusi kategooria tasemel. Need atribuudid ja omadused hõlmavad tootedimensioonide ja kassasätteid. Kategooriatesse määratud tooted pärivad automaatselt teie määratud atribuudid ja omadused. Samal ajal saate kopeerida ka mis tahes toote atribuudisätted valitud kategoorias mitmele tootele.
