---
title: Täpsema laohalduse kasutuselevõtmine ja sellesse migreerumine
description: Selles teemas kirjeldatakse, kuidas lahendada täpsema laohalduse kasutuselevõtul ja sellesse migreerumisel tekkivaid probleeme.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d50c6d75ec7cc98109cf81c38ff42b4d2b105b0c
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645813"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="263d9-103">Täpsema laohalduse kasutuselevõtmine ja sellesse migreerumine</span><span class="sxs-lookup"><span data-stu-id="263d9-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="263d9-104">Selles teemas kirjeldatakse, kuidas lahendada täpsema laohalduse kasutuselevõtul ja sellesse migreerumisel tekkivaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="263d9-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="263d9-105">Kuvatakse järgmine tõrketeade: "java.security.cert.certPathValidatorException: usaldusankru sertifitseerimise teed ei leitud."</span><span class="sxs-lookup"><span data-stu-id="263d9-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="263d9-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="263d9-106">Issue description</span></span>

<span data-ttu-id="263d9-107">See tõrketeade kuvatakse laorakenduses, kuna iseseisvalt allkirjastatud sertifikaate ei usaldata Android 8+ asutusesiseses keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="263d9-107">You receive this error message in the warehouse app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="263d9-108">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="263d9-108">Issue resolution</span></span>

<span data-ttu-id="263d9-109">Kasutage välist (avaliku) sertifitseerimiskeskust (CA).</span><span class="sxs-lookup"><span data-stu-id="263d9-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="263d9-110">Selle probleemi parandus on saadaval laorakenduse versioonis 1.9.0.0.</span><span class="sxs-lookup"><span data-stu-id="263d9-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="263d9-111">Lisateavet selle probleemi ja lahendamise kohta vt teemast [Laorakenduse ühenduse probleemide tõrkeotsing](troubleshoot-warehouse-app-connection.md).</span><span class="sxs-lookup"><span data-stu-id="263d9-111">For more information about this issue and how to fix it, see [Troubleshoot warehouse app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="263d9-112">Mis on kinnitatud protsess baaslaost täpsemale laole liikumiseks?</span><span class="sxs-lookup"><span data-stu-id="263d9-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="263d9-113">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="263d9-113">Issue description</span></span>

<span data-ttu-id="263d9-114">Töötate praegu laos/laohalduses ja kasutate põhivoogude funktsiooni ning soovite migreeruda täpsemasse lattu mobiilsete seadmete, voogude ja töö kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="263d9-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="263d9-115">Kuid teil esineb probleeme, kui proovite seda käiku teha.</span><span class="sxs-lookup"><span data-stu-id="263d9-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="263d9-116">Näiteks ei saa te oma tooteid muuta nii, et need kasutaksid ladustamise dimensioone (sait, ladu ja asukoht), sest toodetel on nende vastu kanded.</span><span class="sxs-lookup"><span data-stu-id="263d9-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="263d9-117">Seetõttu peate õppima kinnitatud protsessi baaslaost täpsemale laole liikumiseks.</span><span class="sxs-lookup"><span data-stu-id="263d9-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="263d9-118">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="263d9-118">Issue resolution</span></span>

<span data-ttu-id="263d9-119">Lisateavet protsessi kohta, kuidas liikuda baaslaost täpsemasse lattu, leiate järgmistest blogipostitustest ja dokumentatsioonist:</span><span class="sxs-lookup"><span data-stu-id="263d9-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="263d9-120">Võimalda olemasolevate kaupadele ja ladudele laohaldusprotsessid</span><span class="sxs-lookup"><span data-stu-id="263d9-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="263d9-121">Microsoft Dynamics AX WMS-i migratsioon uutele R3 lao ja transpordi funktsioonidele</span><span class="sxs-lookup"><span data-stu-id="263d9-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="263d9-122">WMSI/WMS2 kauba migreerimine</span><span class="sxs-lookup"><span data-stu-id="263d9-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="263d9-123">Laohalduse uuendamine rakendusest Microsoft Dynamics AX 2012 rakendusse Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="263d9-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)
