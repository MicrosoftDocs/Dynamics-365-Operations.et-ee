---
title: Dynamics 365 Human Resources infrastruktuuri ühendamise teadaolevad probleemid
description: See artikkel loetleb probleemid, mis võivad Ilmneda Microsofti infrastruktuuri ühendamisel Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f5981801317ad9647f57a0f68f9b67b592256ab
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752686"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>Dynamics 365 Human Resources infrastruktuuri ühendamise teadaolevad probleemid

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>Ühiskasutuses Dataverse keskkonnad

Topeltkirjutuse raamistik ei toeta kahe finantsi ja toimingute rakenduse keskkonna sidumist sama keskkonnaga Dataverse. Kui teil on keskkond Dataverse, mida jagatakse mõlema järgmise üksusega, peate selle kas dubleerima Dataverse või tükeldama:

- Finantside ja toimingute rakendus
- Praegune Inimressursside keskkond

## <a name="environment-type-requirements"></a>Keskkonnatüübi nõuded

Enne migreerimist on nõutavad järgmised keskkonnatüübid:

- Kui teil ei ole kuubokside eraldi keskkondi, peate looma selle migreerimise kinnitamiseks.
- Kui teil on mitu tootmis eraldi keskkonda, saab ühte neist üle siirdada. Pöörduge Microsofti tugiteenuste poole, et märkida teised keskkonnad boksiks.

## <a name="teams-integration"></a>Teamsi integreerimine

Teamsi olemasolevat inimressursside rakendust nihutatakse praegu lahendusele Microsoft Power Platform. Lisateavet vt teemast [Rakendus Human Resources Teamsis](hr-admin-teams-leave-app.md).

