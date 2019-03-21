---
title: Töötellimuste sünkroonimine koos projektiga rakendusest Field Service rakendusse Finance and Operations
description: Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse projekti numbriga töökäskude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service rakendusse Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2019
ms.locfileid: "836438"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Töötellimuste sünkroonimine koos projektiga rakendusest Field Service rakendusse Finance and Operations

[!include[banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse projekti numbriga töökäskude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service rakendusse Microsoft Dynamics 365 for Finance and Operations.

[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Kasutatud mall **Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations)** põhineb lahenduse mallil **Töötellimused (rakendusest Field Service rakendusse Finance and Operations)**. Lisateavet vt jaotisest [Rakenduse Field Service töötellimuste sünkroonimine rakenduse Finance and Operations müügitellimustega](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Selles teemas kirjeldatakse ainult kahe malli vahelisi erinevusi:
- **Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations)**
- **Töötellimused (rakendusest Field Service rakendusse Finance and Operations)**

Peamine erinevus seisneb selles, et see mall sisaldab töötellimusele rakenduses Field Service määratud projektinumbri vastendust, mis tagab, et rakenduses Finance and Operations loodud müügitellimus sisaldab projekti numbrit ja saab toimuda seotud projekti arveldus. Peale selle kasutab mall suvandit Täpsem päring ja filtreerimine.

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

**Malli nimi andmete integratsioonis:**

- Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations)

**Ülesande nimi andmete integratsiooni projektis:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus
**Välise projekti** väli on lisatud üksusele Töökäsk. See väli otsimine, mis märgistades teie Töökäsu Müügitellimuse projektiga ühendatakse seejärel Projektiga rakenduses Finance and Operations. Kui **Süsteemi olek** muutub Avatud – Pooleli(690,970,000) pealt kõrgema oleku peale, lukustatakse väli  **Väline projekt** ja te ei saa selle väärtusele lisada, seda eemaldada ega muuta.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a>Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderHeader

[![Malli vastendamine andmete integratsioonis](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a>Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderHeaderProject

[![Malli vastendamine andmete integratsioonis](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a>Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderProduct

[![Malli vastendamine andmete integratsioonis](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a>Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderService

[![Malli vastendamine andmete integratsioonis](./media/FSWOP4.png)](./media/FSWOP4.png)
