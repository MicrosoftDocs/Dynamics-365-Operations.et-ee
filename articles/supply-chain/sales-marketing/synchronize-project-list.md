---
title: Projektiloendi sünkroonimine rakendusest Finance and Operations rakendusse Field Service
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projektide sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 535094821ca7efa33bf40f2057fac8ffc17bb822
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843549"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Projektiloendi sünkroonimine rakendusest Finance and Operations rakendusse Field Service

[!include[banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projektide sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.

[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded
Projektide sünkroonimise käitamiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.

**Mall andmeintegratsioonis**
- Projektid (rakendusest Fin and Ops rakendusse Field Service)

**Ülesanne andmeintegratsiooni projektis**
- Projektid

Enne projektide loendi sünkroonimist on nõutavad järgmised sünkroonimisülesanded.
- Kontod (Salesist Fin and Opsi) 

## <a name="entity-set"></a>Üksuste komplekt
| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projektid                |

## <a name="entity-flow"></a>Üksuse voog
Projektid luuakse rakenduses Finance and Operations. Projektid, mille **Projekti tüüp** on **Aeg ja materjal** ja **Projekti etapp** on **Pooleli**, sünkroonitakse rakenduses Field Service üksusse **Väline projekt**, sealhulgas projekti number, projekti nimi, projekti etapp ja kliendikonto andmed. Loendit **Väline projekt** kasutatakse teenuse Field Service töökäskude sidumiseks rakenduse Finance and Operations projektidega.

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus
Üksus **Väline projekt** toob kõik projektid rakendusest Finance and Operations. Üksusele **Töökäsk** on lisatud väli **Väline projekt**. See on otsinguväli, nii et kui sildistate oma töökäsu projektiga, ühendatakse müügitellimus rakenduses Finance and Operations projektiga. Kui **Süsteemi olek** muutub olekust **Avatud – pooleli (690,970,000)** kõrgemasse olekusse, lukustatakse väli **Väline projekt** ja te ei saa väärtust enam lisada, eemaldada ega muuta.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine
### <a name="finance-and-operations"></a>Finance and Operations
Muudatuste jälgimise lubamine andmeüksuse projektide jaoks.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis


### <a name="projects-fin-and-ops-to-field-service-projects"></a>Projektid (rakendusest Fin and Ops rakendusse Field Service): projektid

[![Malli vastendamine andmete integratsioonis](./media/FSProject1.png)](./media/FSProject1.png)
