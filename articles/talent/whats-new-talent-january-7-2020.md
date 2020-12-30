---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (7. jaanuar 2020)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460931"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="a27d3-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (7. jaanuar 2020)</span><span class="sxs-lookup"><span data-stu-id="a27d3-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="a27d3-104">Selles artiklis kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="a27d3-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="a27d3-105">Muutused Attractis</span><span class="sxs-lookup"><span data-stu-id="a27d3-105">Changes in Attract</span></span>

<span data-ttu-id="a27d3-106">See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="a27d3-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="a27d3-107">Muutused Onboardis</span><span class="sxs-lookup"><span data-stu-id="a27d3-107">Changes in Onboard</span></span>

<span data-ttu-id="a27d3-108">See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="a27d3-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="a27d3-109">Core HR-i muudatused</span><span class="sxs-lookup"><span data-stu-id="a27d3-109">Changes in Core HR</span></span>

<span data-ttu-id="a27d3-110">Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2697.</span><span class="sxs-lookup"><span data-stu-id="a27d3-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="a27d3-111">Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a27d3-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="a27d3-112">Ei saa kustutada töötajaid, kellel puuduvad tööhõivekirjed – (386157)</span><span class="sxs-lookup"><span data-stu-id="a27d3-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="a27d3-113">See muudatus lisab vormi **Ilma töösuhteta töötajad** kustutamisvõimaluse.</span><span class="sxs-lookup"><span data-stu-id="a27d3-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="a27d3-114">Töötajad kuvatakse sellel vormil, kui töötajaga pole ühtegi tulevast, aktiivset või ajaloolist töösuhet.</span><span class="sxs-lookup"><span data-stu-id="a27d3-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="a27d3-115">Selles versioonis on kustutamine lubatud ainult süsteemiadministraatoritele.</span><span class="sxs-lookup"><span data-stu-id="a27d3-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="a27d3-116">Samas järgmise nädala väljalaskes turvalisust täiendatakse, et lubada kõikidel personaliassisteni rolliga kasutajatel eemaldada ilma töösuhteta töötajaid.</span><span class="sxs-lookup"><span data-stu-id="a27d3-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="a27d3-117">Samuti saate teha neid muudatusi käsitsi, järgides järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="a27d3-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="a27d3-118">Avage suvand **Turvakonfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="a27d3-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="a27d3-119">Vahekaardil **Privileegid** filtreerige loendit **Privileegid** suvandi **Töötajate haldamine** alusel.</span><span class="sxs-lookup"><span data-stu-id="a27d3-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="a27d3-120">Valige veerus **Viited** suvand **Kuvamenüü üksused**.</span><span class="sxs-lookup"><span data-stu-id="a27d3-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="a27d3-121">Valige veerus **Kuvamenüü üksused** suvand **HcmWOrkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="a27d3-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="a27d3-122">Määrake luba **Kustuta** olekusse Luba.</span><span class="sxs-lookup"><span data-stu-id="a27d3-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="a27d3-123">Valige vahekaart **Avaldamata objektid**.</span><span class="sxs-lookup"><span data-stu-id="a27d3-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="a27d3-124">Valige **Avalda kõik**.</span><span class="sxs-lookup"><span data-stu-id="a27d3-124">Select **Publish all**.</span></span>
