---
title: Töökäskude sünkroonimine projektiga rakendusest Field Service rakendusse Supply Chain Management
description: Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse projekti numbriga töökäskude sünkroonimiseks rakendusest Dynamics 365 Field Service rakendusse Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 03/12/2019
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
ms.openlocfilehash: 3ee512c2814b45a0bf35d1bee718b1ce37867bbb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010800"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>Töökäskude sünkroonimine projektiga rakendusest Field Service rakendusse Supply Chain Management

[!include[banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse projekti numbriga töökäskude sünkroonimiseks rakendusest Dynamics 365 Field Service rakendusse Dynamics 365 Supply Chain Management.

[![Äriprotsesside sünkroonimine rakenduste Supply Chain Management ja Field Service vahel](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Kasutatud mall **Töötellimused koos projektiga (rakendusest Field Service rakendusse Supply Chain Management)** põhineb mallil **Töötellimused (rakendusest Field Service rakendusse Supply Chain Management)**. Lisateavet vt jaotisest [Rakenduse Field Service töötellimuste sünkroonimine rakenduse Supply Chain Management müügitellimustega](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Selles teemas kirjeldatakse ainult kahe malli vahelisi erinevusi:
- **Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management)**
- **Töötellimused (rakendusest Field Service rakendusse Supply Chain Management)**

Peamine erinevus seisneb selles, et see mall sisaldab töötellimusele rakenduses Field Service määratud projektinumbri vastendust, mis tagab, et rakenduses Supply Chain Management loodud müügitellimus sisaldab projekti numbrit ja saab toimuda seotud projekti arveldus. Peale selle kasutab mall suvandit Täpsem päring ja filtreerimine.

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

**Malli nimi andmete integratsioonis:**

- Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management)

**Ülesande nimi andmete integratsiooni projektis:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus
**Välise projekti** väli on lisatud üksusele Töökäsk. See on otsinguväli, nii et kui sildistate oma töökäsu projektiga, ühendatakse müügitellimus rakenduses Supply Chain Management projektiga. Kui **Süsteemi olek** muutub Avatud – Pooleli(690,970,000) pealt kõrgema oleku peale, lukustatakse väli **Väline projekt** ja te ei saa selle väärtusele lisada, seda eemaldada ega muuta.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management): WorkOrderHeader

[![Malli vastendamine andmete integratsioonis](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management): WorkOrderHeaderProject

[![Malli vastendamine andmete integratsioonis](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management): WorkOrderProduct

[![Malli vastendamine andmete integratsioonis](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management): WorkOrderService

[![Malli vastendamine andmete integratsioonis](./media/FSWOP4.png)](./media/FSWOP4.png)
