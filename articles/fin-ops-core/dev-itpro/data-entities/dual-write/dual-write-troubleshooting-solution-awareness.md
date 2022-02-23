---
title: Lahenduse teadlikkusega seotud probleemide tõrkeotsing
description: Selles teemas antakse tõrkeotsingu teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 79b2920b80ce4a8b419c2a146e15babc061cf64d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683556"
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
