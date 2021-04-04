---
title: Lahenduse teadlikkusega seotud probleemide tõrkeotsing
description: Selles teemas antakse tõrkeotsingu teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f9e02a6a5afe965a1707f0b04e1b4daedd4ec1df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566785"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Lahenduse teadlikkusega seotud probleemide tõrkeotsing

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta. Eelkõige annab see tõrkeotsingu teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="error-on-the-dual-write-page"></a>Tõrge topeltkirjutuse lehel

Teile võidakse kuvada lehel **Topeltkirjutus** tõrketeade, mis sarnaneb järgmisele näitele.

*Üksust nimega „msdyn\_dualwriteentitymap” koos üksusega namemapping='Logical' ei leitud MetadataCache'is.*

Probleemi lahendamiseks veenduge, et topeltkirjutuse tuumlahendus on installitud Dataverse'is. Topeltkirjutuse tuumlahendus on lahenduse teadlikkuse eeltingimus.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]