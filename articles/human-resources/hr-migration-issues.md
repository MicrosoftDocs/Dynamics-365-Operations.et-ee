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
ms.openlocfilehash: 28c2c10a9293d00e26dfcc80ab08b89a122a6135
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2022
ms.locfileid: "9732763"
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

## <a name="licensing"></a>Litsentsimine

Litsentsimises ei ole muudatusi Dynamics 365 Human Resources järgmistel aladel: 

- **Litsentsi ostunõude miinimumarv**
- **Tootmiskeskkonna** litsentsid ja sisendkausta keskkond – kui teil on olemas autonoomsed inimressursside litsentsid, mis sisaldavad ühte tootmiskeskkonda ja ühte kausta keskkonda, on finantside ja toimingute infrastruktuuris saadaval sama arv litsentse.
- **Täiendavad rakenduslitsentsid** – kui olete ostnud eraldiseisev inimressursid rakenduse jaoks täiendavaid ruutlitsentsisid, on finantside ja toimingute infrastruktuuris märkeruutukeskkondades saadaval sama arv litsentse. 
