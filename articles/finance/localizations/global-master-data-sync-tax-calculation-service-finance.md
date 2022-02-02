---
title: Sünkroonige maksuhäälestus maksuarvutuse teenusest kasutajasse Dynamics 365 Finance
description: See teema kirjeldab, kuidas sünkroonida maksu seadistamise koondandmed maksuarvutuse teenusest Microsofti Dynamics 365 Finance.
author: wangchen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegration, TaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d5d994934014a146f825431cb53dfbef8fe20bc8
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/12/2022
ms.locfileid: "7965106"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Sünkroonige maksuhäälestus maksuarvutuse teenusest kasutajasse Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas sünkroonida maksu seadistamise koondandmed maksuarvutuse teenusest Microsofti Dynamics 365 Finance.

Pärast nõutavate seadistusetappide sooritamist jaotises Alusta maksuarvutusega sünkroonitakse maksuarvutuse teenusest finantsid automaatselt [järgmised](global-get-started-with-tax-calculation-service.md) maksu seadistusandmed.

## <a name="sales-tax-code"></a>Käibemaksukood

| Maksuarvutusteenus           | Finance                             |
| --------------------------------- | ----------------------------------- |
| Maksukood                          | Käibemaksukood                      |
| Kirjeldus                       | Nimi                                |
| Kasutaja sisestus                        | Tasakaalustusperiood                   |
| Kasutaja sisestus                        | Pearaamatu sisestusgrupp                |
| Kasutaja sisestus                        | Käibemaksu valuuta                  |
| Negatiivne maksumäär on konfigureeritud | Luba negatiivset käibemaksuprotsenti |

## <a name="tax-value"></a>Maksu väärtus

| Maksuarvutusteenus | Finance                   |
| ----------------------- | ------------------------- |
| Kande kuupäevast   | Alates kuupäevast                 |
| Kande kuupäevani     | Kuni kuupäevani                   |
| Vähim summa          | Alampiir             |
| Maksimaalne summa          | Ülempiir             |
| Maksumäär                | Väärtus                     |
| Mahaarvamatu määr     | Mahaarvamatu protsent |

## <a name="tax-limits"></a>Maksulimiidid

| Maksuarvutusteenus | Finance           |
| ----------------------- | ----------------- |
| Kande kuupäevast   | Alates kuupäevast         |
| Kande kuupäevani     | Kuni kuupäevani           |
| Minimaalne maksusumma      | Minimaalne käibemaks |
| Maksimaalne maksusumma      | Maksimaalne käibemaks |

## <a name="sales-tax-group"></a>Käibemaksugrupp

| Maksuarvutusteenus                         | Finance                                    |
| ----------------------------------------------- | ------------------------------------------ |
| Maksugrupp                                       | Käibemaksugrupp                            |
| Selle maksugrupi maksukoodid                  | Käibemaksukoodid selle käibemaksugrupi all |
| Maksukood on märgitud **maksuvabana**         | Vabastus                                     |
| Maksukood on märgitud **maksuvabana**         | Vabastuse kood                                |
| Maksukood on märgitud kui **Pöördtasu** | Pöördtasu                             |
| Maksukood on märgitud kui **kasutusmaks.**        | Kasutusmaks                                    |

## <a name="item-sales-tax-group"></a>Kauba käibemaksugrupp

| Maksuarvutusteenus             | Finance                                         |
| ----------------------------------- | ----------------------------------------------- |
| Kauba käibemaksugrupp                      | Kauba käibemaksugrupp                            |
| Selle kauba maksugrupi maksukoodid | Käibemaksukoodid selle kauba käibemaksugrupi all |

Pärast sünkroonimise lõpetamist jätkake finantside järelejäänud parameetrite säilitamist sisestamise ja aruandluse eesmärgil.

> [!NOTE]
> Maksu häälestuse sünkroonimist finantsidelt maksuarvutusteenusele ei toetata. Olemasoleva finantskeskkonna jaoks looge esmalt maksuseadistus maksuarvestuse teenuses. Seejärel sünkroonige seadistusandmed tagasi finantskeskkonda.
