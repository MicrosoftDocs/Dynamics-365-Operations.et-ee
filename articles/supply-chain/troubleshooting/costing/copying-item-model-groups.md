---
title: Puuduvad väljaseaded kauba mudeligruppide kopeerimisel teise juriidilisse isikusse
description: Väljaseaded puuduvad kauba mudeligruppide kopeerimisel teise juriidilisse isikusse.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 128caead04cf467c65a50bc6cd2f9e76e318f536b7eafa7972ffc1b5da5bceba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738839"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>Puuduvad väljaseaded kauba mudeligruppide kopeerimisel teise juriidilisse isikusse

KB number: 4612800

## <a name="symptoms"></a>Sümptomid

Kui kopeerite kauba mudeligrupid teisele juriidilisele isikule (ettevõttele), kasutades *kauba mudeligrupi laopoliitika üksust*, puuduvad sihtjuriidilise isiku uues mudeligrupis mõned väljasätted (nt laomudel ja kirjeldus).

## <a name="resolution"></a>Eraldusvõime

Kauba mudeligrupi täieliku koopia loomiseks teisele juriidilisele isikule peate valima ka nii kauba mudeligrupi laopoliitikad (`InventInventoryPolicyEntity`) kui ka kauba mudeligrupiga seotud kuluvoo eelduste (`InventCostFlowAssumptionPolicyEntity`) poliitikad, mis on seotud kauba mudeligrupiga.
