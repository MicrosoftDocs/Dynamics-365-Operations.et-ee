---
title: Töökäskude sünkroonimine projektiga rakendusest Field Service rakendusse Supply Chain Management
description: See artikkel käsitleb malle ja aluseks olevat ülesannet, mida kasutatakse töötellimuste sünkroonimiseks projekti numbriga alates Dynamics 365 Field Service kuni Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: a43a7f7e900205bdb23fb9a35ca1518369683a42
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860489"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>Töökäskude sünkroonimine projektiga rakendusest Field Service rakendusse Supply Chain Management

[!include[banner](../includes/banner.md)]

See artikkel käsitleb malle ja aluseks olevat ülesannet, mida kasutatakse töötellimuste sünkroonimiseks projekti numbriga alates Dynamics 365 Field Service kuni Dynamics 365 Supply Chain Management.

[![Äriprotsesside sünkroniseerimine rakenduste Supply Chain Management ja Field Service vahel.](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Kasutatud mall **Töötellimused koos projektiga (rakendusest Field Service rakendusse Supply Chain Management)** põhineb mallil **Töötellimused (rakendusest Field Service rakendusse Supply Chain Management)**. Lisateavet vt jaotisest [Rakenduse Field Service töötellimuste sünkroonimine rakenduse Supply Chain Management müügitellimustega](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

See artikkel kirjeldab ainult erinevusi kahe malli vahel:
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

[![Mallide kaardistamine andmete integreerimisel, töötellimused projektiga (Field Service kuni Supply Chain Management): WorkOrderHeader.](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management): WorkOrderHeaderProject

[![Mallide kaardistamine andmete integreerimisel, töötellimused projektiga (Field Service kuni Supply Chain Management): WorkOrderHeaderProject.](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management): WorkOrderProduct

[![Mallide kaardistamine andmete integreerimisel, töötellimused projektiga (Field Service kuni Supply Chain Management): WorkOrderProduct.](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management): WorkOrderService

[![Mallide kaardistamine andmete integreerimisel, töötellimused projektiga (Field Service kuni Supply Chain Management): WorkOrderService.](./media/FSWOP4.png)](./media/FSWOP4.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]