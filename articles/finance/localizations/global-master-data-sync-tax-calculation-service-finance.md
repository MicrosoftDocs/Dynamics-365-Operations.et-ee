---
title: Sünkroonige maksuhäälestus maksu arvutamise teenusest Dynamics 365 finance-ga
description: See teema kirjeldab, kuidas sünkroonida maksu seadistamise koondandmeid maksu arvutamise teenusest Microsoft Dynamics 365 Finantsid.
author: wangchen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegration, TaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3a9c11a6f5946d56b9e58a02c37f18adec155661
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687782"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Sünkroonige maksuhäälestus maksu arvutamise teenusest Dynamics 365 finance-ga

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas sünkroonida maksu seadistamise koondandmeid maksu arvutamise teenusest Microsoft Dynamics 365 Finantsid.

Pärast nõutavate seadistusetappide lõpule viimist [jaotises](global-get-started-with-tax-calculation-service.md) Alusta maksuarvutusega sünkroonitakse maksuarvutuse teenusest finantsid automaatselt järgmised maksu seadistusandmed.

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
| Kande kuupäevast   | Kehtivuse alguskuupäev                 |
| Kande kuupäevani     | Lõppkuupäev                   |
| Vähim summa          | Alampiir             |
| Maksimaalne summa          | Ülempiir             |
| Maksumäär                | Väärtus                     |
| Mahaarvamatu määr     | Mahaarvamatu protsent |

## <a name="tax-limits"></a>Maksulimiidid

| Maksuarvutusteenus | Finance           |
| ----------------------- | ----------------- |
| Kande kuupäevast   | Kehtivuse alguskuupäev         |
| Kande kuupäevani     | Lõppkuupäev           |
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
| Maksukood on märgitud kui kasutusmaks **.**        | Kasutusmaks                                    |

## <a name="item-sales-tax-group"></a>Kauba käibemaksugrupp

| Maksuarvutusteenus             | Finance                                         |
| ----------------------------------- | ----------------------------------------------- |
| Kauba maksugrupp                      | Kauba käibemaksugrupp                            |
| Selle kauba maksugrupi maksukoodid | Käibemaksukoodid selle kauba käibemaksugrupi all |

Pärast sünkroonimise lõpetamist jätkake finantside järelejäänud parameetrite säilitamist sisestamise ja aruandluse eesmärgil.

> [!NOTE]
> Maksu häälestuse sünkroonimist finantsidelt maksuarvutusteenusele ei toetata. Olemasoleva finantskeskkonna jaoks looge esmalt maksuseadistus maksuarvestuse teenuses. Seejärel sünkroonige seadistusandmed tagasi finantskeskkonda.
