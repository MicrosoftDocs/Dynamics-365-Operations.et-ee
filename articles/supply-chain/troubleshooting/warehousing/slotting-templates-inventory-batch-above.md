---
title: Kättesaadav varu ei ole partiiülesannete puhul arvesse võetud
description: Mõni pilumall ei arvesta partiiülesannete jaoks olemasolevat olemasolevat laoseisu. Partii või seerianumber tuleb määrata nõudlustellimusel.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: df5642b32f5e053144230eab3dbcf633f526279a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476120"
---
# <a name="slotting-templates-dont-consider-on-hand-inventory-for-batch-above-items"></a>Ruumi leidmise mallid ei arvesta partiiüleste kaupade vaba kaubavaru

## <a name="symptoms"></a>Sümptomid

Pesade mallid, mille puhul on kriteerium *Arvesta vaba* pesa, ei arvesta *partiiüleste* kaupade praegust vaba kaubavaru. Nad arvestavad seda ainult juhul, kui partiinumber on müügitellimuse real määratud.

Kui kasutate aga *partiialuseid* kaupu, loetakse praegune vaba kaubavaru nii nagu on.

Lisateavet vt teemast [Laoruumi leidmine](/dynamics365/supply-chain/warehousing/warehouse-slotting).

## <a name="resolution"></a>Lahendus

Pesastatud malli päise saab määrata nõudetrateegiatele *Tellitud*, *Reserveeritud* või *Välja antud*. *Tellitud* nõudlusstrateegia puhul kehtivad samad reserveerimishierarhia nõuded, mis rakenduvad reserveeringutele või laoprotsesside väljaandmisele. Seetõttu peab *partiialuse* või *seeriaaluste* kaupade puhul, mille reserveerimise hierarhiad on partii- või seerianumbrid määratud nõudlustellimusel (müük või ülekanne).

Teise võimalusena saab nõudlusstrateegiat *Reserveeritud* kasutada partii või seerianumbri valimiseks enne lao täitmisnõudluse loomist.
