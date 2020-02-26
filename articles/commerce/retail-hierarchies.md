---
title: Jaemüügihierarhiad
description: Selles artiklis kirjeldatakse Dynamics 365 Commercei jaemüügihierarhiaid.
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
ms.openlocfilehash: cf8db2c828f99dfd4c220966e31894dcd6eda572
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022292"
---
# <a name="retail-hierarchies"></a>Jaemüügihierarhiad

[!include [banner](includes/banner.md)]

Selles artiklis kirjeldatakse rakenduse Dynamics 365 Commerce hierarhiaid.

Saate luua kategooriahierarhia, et korraldada kanalite kaudu müüdavaid tooteid. Tootehierarhiate abil saate tooteid kategoriseerida või grupeerida. Seejärel saate neid tooteid kasutada tootesortimentide ja püsikliendiprogrammide loomiseks. Saate ka määrata toote atribuute ja omadusi, määrata hinnakujunduse struktuuri, kaasata tooteid tootekampaaniatesse ja kasutada tooteid aruandluseks. Saate luua ühe kategooriahierarhia esindama kõiki organisatsiooni tooteid ja kategooriaid ning kasutada seda kategooriahierarhiat mitmel eesmärgil. Teise võimalusena saate luua mitme kategooria hierarhiad eriotstarbeks, näiteks tootekampaaniate jaoks. Tootehierarhia loomisel tuleb määrata kategooria hierarhia tüüp, et tuvastada kategooriahierarhia eesmärk. Näiteks viidatakse toote sirvimisel võrgus või kassas ainult tootehierarhiaid, millele on määratud tüüp **Kaubanduse navigeerimishierarhia**.

## <a name="hierarchy-types"></a>Hierarhia tüübid

Järgmises tabelis on loetletud saadaolevad kategooriahierarhia tüübid ja iga tüübi üldeesmärk.

| Kategooriahierarhia tüüp       | Eesmärk |
|-------------------------------|---------|
| Tootehierarhia      | Kasutage seda hierarhiatüüpi, et määratleda organisatsiooni üldine tootehierarhia. Saate seda hierarhiatüüpi kasutada tootesündmuste, hinnakujunduse ja kampaaniate, aruandluse ning sortimendi planeerimise jaoks. Selle hierarhia tüübi saab määrata ainult ühele tootehierarhiale. |
| Täiendav hierarhia | Kasutage seda hierarhia tüüpi mis tahes täiendavate kategooriahierarhiate puhul, mille soovite luua. Näiteks korraldate kevadel kampaania ujumisriiete müügiks. Seega kaasate ujumisriietest tooted eraldi kategooriahierarhiasse ja rakendate erinevatele tootekategooriatele kampaaniahinnad. |
| Navigeerimishierarhia   | Kasutage seda hierarhiatüüpi toodete grupeerimiseks ja korraldamiseks kategooriatesse, nii et tooteid saab sirvida võrgus või kassas. |

Kategooriahierarhia abil tooteid struktureerides saate seadistada ja hallata toote atribuute ning omadusi kategooria tasemel. Need atribuudid ja omadused hõlmavad tootedimensioonide ja kassasätteid. Kategooriatesse määratud tooted pärivad automaatselt teie määratud atribuudid ja omadused. Samal ajal saate kopeerida ka mis tahes toote atribuudisätted valitud kategoorias mitmele tootele.
