---
title: Töötellimuste sünkroonimine koos projektiga rakendusest Field Service rakendusse Finance and Operations
description: Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse projekti numbriga töökäskude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service rakendusse Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "329846"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Töötellimuste sünkroonimine koos projektiga rakendusest Field Service rakendusse Finance and Operations

[!include[banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse projekti numbriga töökäskude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service rakendusse Microsoft Dynamics 365 for Finance and Operations.

[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Kasutatud mall **Field Service’i tooted (Finance and Operationsist Field Service’isse)** põhineb lahenduse Potentsiaalne klient sularahaks mallil **Tooted (Finance and Operationsist Salesi) – otse**. Lisateabe saamiseks vt [Tooted (Finance and Operationsist Salesi) – otse](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Selles teemas kirjeldatakse ainult mallide **Field Service’i tooted (Finance and Operationsist Field Service’isse)** ja **Field Service'i tooted (Finance and Operationsist Salesi)** erinevusi.

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

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a>Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderHeader

[![Malli vastendamine andmete integratsioonis](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a>Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderHeaderProject

[![Malli vastendamine andmete integratsioonis](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a>Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderProduct

[![Malli vastendamine andmete integratsioonis](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a>Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderService

[![Malli vastendamine andmete integratsioonis](./media/FSWOP4.png)](./media/FSWOP4.png)
