---
title: Projektiloendi sünkroonimine rakendusest Supply Chain Management rakendusse Field Service
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projektide sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 12708b35be87baf1ad13296b56507f3246f96394
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010868"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Projektiloendi sünkroonimine rakendusest Supply Chain Management rakendusse Field Service

[!include[banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projektide sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.

[![Äriprotsesside sünkroonimine rakenduste Supply Chain Management ja Field Service vahel](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded
Järgmist malli ja aluseks olevaid ülesandeid kasutatakse rakendusest Supply Chain Management rakendusse Field Service projektide sünkroonimise kävitamiseks.

**Mall andmeintegratsioonis**
- Projektid (rakendusest Supply Chain Management rakendusse Field Service)

**Ülesanne andmeintegratsiooni projektis**
- Projektid

Enne projektide loendi sünkroonimist on nõutavad järgmised sünkroonimisülesanded.
- Kontod (rakendusest Müük rakendusse Supply Chain Management) 

## <a name="entity-set"></a>Üksuste komplekt
| Field Service           | Supply Chain Management  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projektid                |

## <a name="entity-flow"></a>Üksuse voog
Projektid luuakse rakenduses Supply Chain Management. Projektid, mille **Projekti tüüp** on **Aeg ja materjal** ja **Projekti etapp** on **Pooleli**, sünkroonitakse rakenduses Field Service üksusse **Väline projekt**, sealhulgas projekti number, projekti nimi, projekti etapp ja kliendikonto andmed. Loendit **Väline projekt** kasutatakse teenuse Field Service töökäskude sidumiseks rakenduse Supply Chain Management projektidega.

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus
Üksus **Väline projekt** toob kõik projektid rakendusest Supply Chain Management. Üksusele **Töökäsk** on lisatud väli **Väline projekt**. See on otsinguväli, nii et kui sildistate oma töökäsu projektiga, ühendatakse müügitellimus rakenduses Supply Chain Management projektiga. Kui **Süsteemi olek** muutub olekust **Avatud – pooleli (690,970,000)** kõrgemasse olekusse, lukustatakse väli **Väline projekt** ja te ei saa väärtust enam lisada, eemaldada ega muuta.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine
### <a name="supply-chain-management"></a>Supply Chain Management
Muudatuste jälgimise lubamine andmeüksuse projektide jaoks.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis


### <a name="projects-supply-chain-management-to-field-service-projects"></a>Projektid (rakendusest Supply Chain Management rakendusse Field Service): projektid

[![Malli vastendamine andmete integratsioonis](./media/FSProject1.png)](./media/FSProject1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]