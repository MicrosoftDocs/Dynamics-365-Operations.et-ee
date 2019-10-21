---
title: Uute kasutajate loomine
description: Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.
author: maertenm
manager: AnnBe
ms.date: 08/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a5635f96132b2e52227b569e7e480fa55e82d61
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180940"
---
# <a name="create-new-users"></a><span data-ttu-id="79330-103">Uute kasutajate loomine</span><span class="sxs-lookup"><span data-stu-id="79330-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="79330-104">Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.</span><span class="sxs-lookup"><span data-stu-id="79330-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="79330-105">Kasutaja seostamine litsentsiga (ainult uued litsentsi tüübid)</span><span class="sxs-lookup"><span data-stu-id="79330-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="79330-106">Klientidele, kes on ühes uutest litsentsi tüüpidest, mis lisati oktoobris 2019, peavad kasutajad olema litsentsiga seotud.</span><span class="sxs-lookup"><span data-stu-id="79330-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="79330-107">Kasutajad, kes on seotud litsentsiga, lisatakse automaatselt süsteemi kasutajatele, kellel ei ole esimest korda sisselogimisel rolle.</span><span class="sxs-lookup"><span data-stu-id="79330-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span> <span data-ttu-id="79330-108">Kasutajad, kes ei ole litsentsiga seotud, saavad hoiatusteate.</span><span class="sxs-lookup"><span data-stu-id="79330-108">Users who aren't associated with a licence receive a warning message.</span></span>

<span data-ttu-id="79330-109">Süsteemi administraatorid saavad [litsentse määrata](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)[Microsoft 365-i administreerimiskeskuse](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide) kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="79330-109">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="79330-110">Lisa uus kasutaja</span><span class="sxs-lookup"><span data-stu-id="79330-110">Add a new user</span></span>
1. <span data-ttu-id="79330-111">Minge jaotisse **Süsteemihaldus \> Kasutajad \> Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="79330-111">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="79330-112">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="79330-112">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="79330-113">Väljale **Kasutaja ID** saate sisestada küsimustiku kordumatu koodi.</span><span class="sxs-lookup"><span data-stu-id="79330-113">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="79330-114">Kasutaja ID on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="79330-114">A user ID is required.</span></span>  
4. <span data-ttu-id="79330-115">Sisestage väljale **Kasutajanimi** kasutaja nimi.</span><span class="sxs-lookup"><span data-stu-id="79330-115">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="79330-116">Sisestage väljale **Domeen** kasutaja domeen.</span><span class="sxs-lookup"><span data-stu-id="79330-116">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="79330-117">Sisestage väljale **Pseudonüüm** kasutaja pseudonüüm.</span><span class="sxs-lookup"><span data-stu-id="79330-117">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="79330-118">Väljal **Ettevõte** valige soovitud ettevõte.</span><span class="sxs-lookup"><span data-stu-id="79330-118">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="79330-119">Vahekaardil **Kasutaja rollid** valige käsk **Määra rollid** [kasutajatele turvalisuse rollide määramiseks.](assign-users-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="79330-119">On the **User's roles** FastTab, select **Assign roles** to [assign users to security roles](assign-users-security-roles.md)</span></span>
9. <span data-ttu-id="79330-120">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="79330-120">Select **OK**.</span></span>
10. <span data-ttu-id="79330-121">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="79330-121">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="79330-122">Impordi kasutajad</span><span class="sxs-lookup"><span data-stu-id="79330-122">Import users</span></span>
1. <span data-ttu-id="79330-123">Toimingupaanil valige **Impordi kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="79330-123">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="79330-124">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="79330-124">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="79330-125">Valige **Impordi kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="79330-125">Select **Import users**.</span></span>
4. <span data-ttu-id="79330-126">Valige suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="79330-126">Select **Close**.</span></span>

