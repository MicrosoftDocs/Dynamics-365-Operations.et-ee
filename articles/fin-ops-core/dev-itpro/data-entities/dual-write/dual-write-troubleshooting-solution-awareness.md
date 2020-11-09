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
ms.openlocfilehash: 7f1a6e424996201ecae1b624c13cfc573745dc0a
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997274"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="2e143-103">Lahenduse teadlikkusega seotud probleemide tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="2e143-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="2e143-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="2e143-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="2e143-105">Eelkõige annab see tõrkeotsingu teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme.</span><span class="sxs-lookup"><span data-stu-id="2e143-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e143-106">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="2e143-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="2e143-107">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="2e143-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="2e143-108">Tõrge topeltkirjutuse lehel</span><span class="sxs-lookup"><span data-stu-id="2e143-108">Error on the Dual-write page</span></span>

<span data-ttu-id="2e143-109">Teile võidakse kuvada lehel **Topeltkirjutus** tõrketeade, mis sarnaneb järgmisele näitele.</span><span class="sxs-lookup"><span data-stu-id="2e143-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="2e143-110">*Üksust nimega „msdyn\_dualwriteentitymap” koos üksusega namemapping='Logical' ei leitud MetadataCache'is.*</span><span class="sxs-lookup"><span data-stu-id="2e143-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="2e143-111">Probleemi lahendamiseks veenduge, et topeltkirjutuse tuumlahendus on installitud Common Data Service'is.</span><span class="sxs-lookup"><span data-stu-id="2e143-111">To fix the issue, make sure that the dual-write core solution is installed in Common Data Service.</span></span> <span data-ttu-id="2e143-112">Topeltkirjutuse tuumlahendus on lahenduse teadlikkuse eeltingimus.</span><span class="sxs-lookup"><span data-stu-id="2e143-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>
