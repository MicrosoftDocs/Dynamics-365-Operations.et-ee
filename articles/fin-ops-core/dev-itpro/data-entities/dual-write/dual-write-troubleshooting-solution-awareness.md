---
title: Lahenduse teadlikkusega seotud probleemide tõrkeotsing
description: Selles teemas antakse tõrkeotsingu teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: ec5afd92a71c8b12c913de78a513abb0959df88a
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782057"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Lahenduse teadlikkusega seotud probleemide tõrkeotsing

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta. Eelkõige annab see tõrkeotsingu teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="error-on-the-dual-write-page"></a>Tõrge topeltkirjutuse lehel

Teile võidakse kuvada lehel **Topeltkirjutus** tõrketeade, mis sarnaneb järgmisele näitele.

*Üksust nimega „msdyn\_ dualwriteentitymap” koos üksusega namemapping='Logical' ei leitud MetadataCache'is.*

Probleemi lahendamiseks veenduge, et topeltkirjutuse tuumlahendus on installitud Dataverse'is. Topeltkirjutuse tuumlahendus on lahenduse teadlikkuse eeltingimus.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]