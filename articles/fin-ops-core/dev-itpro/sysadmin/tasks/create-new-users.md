---
title: Uute kasutajate loomine
description: Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.
author: maertenm
manager: AnnBe
ms.date: 02/06/2020
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
ms.openlocfilehash: 9db4b6d355d6499bce6c550b2fbe76b82cf69fd4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143567"
---
# <a name="create-new-users"></a><span data-ttu-id="5d6d1-103">Uute kasutajate loomine</span><span class="sxs-lookup"><span data-stu-id="5d6d1-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d6d1-104">Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to do their jobs.</span></span>

## <a name="associate-a-user-with-a-license-new-license-types-only"></a><span data-ttu-id="5d6d1-105">Kasutaja seostamine litsentsiga (ainult uued litsentsi tüübid)</span><span class="sxs-lookup"><span data-stu-id="5d6d1-105">Associate a user with a license (new license types only)</span></span>
<span data-ttu-id="5d6d1-106">Klientidele, kes on ühes uutest litsentsi tüüpidest, mis lisati oktoobris 2019, peavad kasutajad olema litsentsiga seotud.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-106">For customers who are on one of the new license types that were added in October 2019, users must be associated with a license.</span></span> <span data-ttu-id="5d6d1-107">Kasutajad, kes on seotud litsentsiga, lisatakse automaatselt süsteemi kasutajatele, kellel ei ole esimest korda sisselogimisel rolle.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-107">Users who are associated with a license are automatically added as system users who have no roles the first time that they sign in.</span></span>

<span data-ttu-id="5d6d1-108">Süsteemi administraatorid saavad [litsentse määrata](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)[Microsoft 365-i administreerimiskeskuse](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide) kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-108">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a><span data-ttu-id="5d6d1-109">Välise kasutaja seostamine litsentsiga (ainult uued litsentsi tüübid)</span><span class="sxs-lookup"><span data-stu-id="5d6d1-109">Associate an external user with a license (new license types only)</span></span>
<span data-ttu-id="5d6d1-110">Kasutajad, kes on väljaspool rentnikku, milles keskkond kasutusele on võetud, peavad olema esindatud hosti rentniku kataloogis (Azure Active Directory (Azure AD)), et neile saaks määrata litsentsid.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-110">Users external to the tenant that the environment was deployed into need to be represented in the host tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="5d6d1-111">Need välised kasutajad tuleb lisada Azure AD's rentnikku külaliskasutajatena ja seejärel määrata vastavad litsentsid.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-111">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="5d6d1-112">Lisateavet vt teemast [Azure portaalis Azure Active Directory B2B koostöö kasutajate lisamine](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="5d6d1-112">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="add-a-new-user"></a><span data-ttu-id="5d6d1-113">Lisa uus kasutaja</span><span class="sxs-lookup"><span data-stu-id="5d6d1-113">Add a new user</span></span>
1. <span data-ttu-id="5d6d1-114">Minge jaotisse **Süsteemihaldus \> Kasutajad \> Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-114">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="5d6d1-115">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="5d6d1-116">Väljale **Kasutaja ID** saate sisestada küsimustiku kordumatu koodi.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-116">In the **User ID** field, enter a unique identifier for the user.</span></span> <span data-ttu-id="5d6d1-117">Kasutaja ID on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-117">A user ID is required.</span></span>  
4. <span data-ttu-id="5d6d1-118">Sisestage väljale **Kasutajanimi** kasutaja nimi.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-118">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="5d6d1-119">Sisestage väljale **Domeen** kasutaja domeen.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-119">In the **Domain** field, enter the user's domain.</span></span>  
6. <span data-ttu-id="5d6d1-120">Sisestage väljale **Pseudonüüm** kasutaja pseudonüüm.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-120">In the **Alias** field, enter the user's alias.</span></span>  
7. <span data-ttu-id="5d6d1-121">Väljal **Ettevõte** valige soovitud ettevõte.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-121">In the **Company** field, select the desired company.</span></span> 
8. <span data-ttu-id="5d6d1-122">Valige kiirkaardil **Kasutaja rollid** turberollide määramiseks kasutajatele suvand **Määra rollid**.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-122">On the **User's roles** FastTab, select **Assign roles** to assign users to security roles.</span></span> <span data-ttu-id="5d6d1-123">Lisainfo saamiseks vt [Kasutajatele turberollide määramine](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="5d6d1-123">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span>
9. <span data-ttu-id="5d6d1-124">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-124">Select **OK**.</span></span>
10. <span data-ttu-id="5d6d1-125">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-125">Select **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="5d6d1-126">Impordi kasutajad</span><span class="sxs-lookup"><span data-stu-id="5d6d1-126">Import users</span></span>
1. <span data-ttu-id="5d6d1-127">Toimingupaanil valige **Impordi kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-127">On the Action Pane, select **Import users**.</span></span>
2. <span data-ttu-id="5d6d1-128">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-128">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="5d6d1-129">Valige **Impordi kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-129">Select **Import users**.</span></span>
4. <span data-ttu-id="5d6d1-130">Valige suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="5d6d1-130">Select **Close**.</span></span>

