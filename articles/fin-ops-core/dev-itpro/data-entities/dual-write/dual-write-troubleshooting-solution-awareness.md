---
title: Lahenduse teadlikkusega seotud probleemide tõrkeotsing
description: Selles teemas antakse tõrkeotsingu teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme.
author: RamaKrishnamoorthy
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
ms.openlocfilehash: 86dd8803f7560ea337f2452e9722fe0151466daf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748869"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="0bd91-103">Lahenduse teadlikkusega seotud probleemide tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="0bd91-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="0bd91-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="0bd91-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="0bd91-105">Eelkõige annab see tõrkeotsingu teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme.</span><span class="sxs-lookup"><span data-stu-id="0bd91-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bd91-106">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="0bd91-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="0bd91-107">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="0bd91-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="0bd91-108">Tõrge topeltkirjutuse lehel</span><span class="sxs-lookup"><span data-stu-id="0bd91-108">Error on the Dual-write page</span></span>

<span data-ttu-id="0bd91-109">Teile võidakse kuvada lehel **Topeltkirjutus** tõrketeade, mis sarnaneb järgmisele näitele.</span><span class="sxs-lookup"><span data-stu-id="0bd91-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="0bd91-110">*Üksust nimega „msdyn\_dualwriteentitymap” koos üksusega namemapping='Logical' ei leitud MetadataCache'is.*</span><span class="sxs-lookup"><span data-stu-id="0bd91-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="0bd91-111">Probleemi lahendamiseks veenduge, et topeltkirjutuse tuumlahendus on installitud Dataverse'is.</span><span class="sxs-lookup"><span data-stu-id="0bd91-111">To fix the issue, make sure that the dual-write core solution is installed in Dataverse.</span></span> <span data-ttu-id="0bd91-112">Topeltkirjutuse tuumlahendus on lahenduse teadlikkuse eeltingimus.</span><span class="sxs-lookup"><span data-stu-id="0bd91-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]