---
title: Uute kasutajate loomine
description: Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.
author: peakerbl
manager: AnnBe
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f30f6292ed0a4de93ba75341bc917f9205c4e39c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571049"
---
# <a name="create-new-users"></a><span data-ttu-id="eb822-103">Uute kasutajate loomine</span><span class="sxs-lookup"><span data-stu-id="eb822-103">Create new users</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eb822-104">Enne Finance and Operationsi rakenduste avamist peate olema kõigepealt lisatud lehele **Kasutajad** (**Süsteemi administraator \> Kasutajad \> Kasutajad**).</span><span class="sxs-lookup"><span data-stu-id="eb822-104">Before you can access Finance and Operations apps, you must first be added to the **Users** page (**System administration \> Users \> Users**).</span></span> <span data-ttu-id="eb822-105">Kasutajad hõlmavad teie organisatsioonisiseseid töötajaid või väliseid kliente ja hankijaid.</span><span class="sxs-lookup"><span data-stu-id="eb822-105">Users include internal employees of your organization, or external customers and vendors.</span></span> <span data-ttu-id="eb822-106">Kasutajaid saab importida või lisada käsitsi.</span><span class="sxs-lookup"><span data-stu-id="eb822-106">Users can be imported or added manually.</span></span> <span data-ttu-id="eb822-107">Kõik kasutajad peavad ühilduvaks kasutuseks olema õigesti litsentsitud.</span><span class="sxs-lookup"><span data-stu-id="eb822-107">All users must be correctly licensed for compliant use.</span></span>

<span data-ttu-id="eb822-108">Lisateavet Finance and Operationsi rakendust ostmise ja litsentsimise kohta vt [Microsoft Dynamics 365 litsentsimise juhend](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span><span class="sxs-lookup"><span data-stu-id="eb822-108">For information about how to buy and license for Finance and Operations apps, see [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).</span></span>

## <a name="assign-a-license-to-a-user"></a><span data-ttu-id="eb822-109">Kasutajale litsentsi määramine</span><span class="sxs-lookup"><span data-stu-id="eb822-109">Assign a license to a user</span></span>
<span data-ttu-id="eb822-110">Süsteemi administraatorid saavad [litsentse määrata](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide)[Microsoft 365-i administreerimiskeskuse](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide) kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="eb822-110">System admins can [assign licenses to users](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in the [Microsoft 365 admin center](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).</span></span>

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a><span data-ttu-id="eb822-111">Azure AD-s välise kasutaja lisamine ja litsentsi määramine</span><span class="sxs-lookup"><span data-stu-id="eb822-111">Add an external user in Azure AD and assign a license</span></span> 
<span data-ttu-id="eb822-112">Litsentside määramiseks peavad välised kasutajad olema teie rentniku teegis esindatud (Azure Active Directory (Azure AD)).</span><span class="sxs-lookup"><span data-stu-id="eb822-112">External users must be represented in your tenant directory (Azure Active Directory (Azure AD)) so that they can be assigned licenses.</span></span> <span data-ttu-id="eb822-113">Need välised kasutajad tuleb lisada Azure AD's rentnikku külaliskasutajatena ja seejärel määrata vastavad litsentsid.</span><span class="sxs-lookup"><span data-stu-id="eb822-113">Those external users should be added to the tenant in Azure AD as guest users and then assigned the appropriate licenses.</span></span> <span data-ttu-id="eb822-114">Finance and Operationsi rakenduste nõue on, et külaliskasutaja ettevõte peab kasutama teenust Azure AD.</span><span class="sxs-lookup"><span data-stu-id="eb822-114">A requirement for Finance and Operations apps is that the guest user's company must use Azure AD.</span></span> <span data-ttu-id="eb822-115">Lisateavet vt teemast [Azure portaalis Azure Active Directory B2B koostöö kasutajate lisamine](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span><span class="sxs-lookup"><span data-stu-id="eb822-115">For more information, see [Add Azure Active Directory B2B collaboration users in the Azure portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator).</span></span>

## <a name="import-new-users-from-azure-ad"></a><span data-ttu-id="eb822-116">Uute kasutajate importimine teenusest Azure AD</span><span class="sxs-lookup"><span data-stu-id="eb822-116">Import new users from Azure AD</span></span> 
1. <span data-ttu-id="eb822-117">Avage **Süsteemihaldud** \> **Kasutaja** \> **Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="eb822-117">Go to **System administration** \> **User** \> **Users**.</span></span>
2. <span data-ttu-id="eb822-118">Toimingupaanil valige **Impordi kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="eb822-118">On the Action Pane, select **Import users**.</span></span>
3. <span data-ttu-id="eb822-119">Valige imporditavad failid.</span><span class="sxs-lookup"><span data-stu-id="eb822-119">Select the users to be imported.</span></span> <span data-ttu-id="eb822-120">Loend hõlmab Azure AD kasutajaid, kes pole praegu selles keskkonnas kasutajad.</span><span class="sxs-lookup"><span data-stu-id="eb822-120">The list includes Azure AD users that are currently not users in this environment.</span></span>
4. <span data-ttu-id="eb822-121">Valige **Impordi kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="eb822-121">Select **Import users**.</span></span>
5. <span data-ttu-id="eb822-122">Valige suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="eb822-122">Select **Close**.</span></span>

> [!NOTE]
> <span data-ttu-id="eb822-123">Välja **Ettevõte** väärtus määratakse administraatori praeguse seansi ettevõtte põhjal. Pärast importimist peate määrama vastavalt vajadusele rollid ja organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="eb822-123">The value for the **Company** field will be set based on the current session company for the admin. After import, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="eb822-124">Lisainfo saamiseks vt [Kasutajatele turberollide määramine](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="eb822-124">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="eb822-125">Tingimuslikult võib olla nõutav ka kasutaja seostamine **isikuga** ja kasutaja valikute uuendamine, nt keel.</span><span class="sxs-lookup"><span data-stu-id="eb822-125">Conditionally, it might also be required to associate the user with a **Person** and to update user options such as language.</span></span>

## <a name="manually-add-a-new-user"></a><span data-ttu-id="eb822-126">Uue kasutaja käsitsi lisamine</span><span class="sxs-lookup"><span data-stu-id="eb822-126">Manually add a new user</span></span>
1. <span data-ttu-id="eb822-127">Avage **Süsteemihaldus** \> **Kasutajad** \> **Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="eb822-127">Go to **System administration** \> **Users** \> **Users**.</span></span>
2. <span data-ttu-id="eb822-128">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="eb822-128">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="eb822-129">Väljale **Kasutaja ID** saate sisestada küsimustiku kordumatu koodi.</span><span class="sxs-lookup"><span data-stu-id="eb822-129">In the **User ID** field, enter a unique identifier for the user.</span></span>   
4. <span data-ttu-id="eb822-130">Sisestage väljale **Kasutajanimi** kasutaja nimi.</span><span class="sxs-lookup"><span data-stu-id="eb822-130">In the **User name** field, enter the user's name.</span></span>  
5. <span data-ttu-id="eb822-131">Väljal **Pakkuja** tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="eb822-131">In the **Provider** field:</span></span>
 - <span data-ttu-id="eb822-132">Sisemiste kasutajate puhul kasutage vaikeväärtust.</span><span class="sxs-lookup"><span data-stu-id="eb822-132">For internal users, use the defaulted value.</span></span> <span data-ttu-id="eb822-133">Näiteks teie Azure AD rentnik koos eesliitega https://sts.windows.net/.</span><span class="sxs-lookup"><span data-stu-id="eb822-133">For example, your Azure AD tenant prefixed with https://sts.windows.net/.</span></span>  
 - <span data-ttu-id="eb822-134">Mitte-Azure AD kasutajate jaoks, näiteks teenustevahelised kontod, sisestage põhiteksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="eb822-134">For non-Azure AD users, such as Service-2-Service accounts, enter a basic text value.</span></span> <span data-ttu-id="eb822-135">Näiteks, NA.</span><span class="sxs-lookup"><span data-stu-id="eb822-135">For example, NA.</span></span> <span data-ttu-id="eb822-136">See väärtus aitab vältida valesid autentimiskutseid, mis võivad põhjustada tõrkeid, kui kasutatakse kehtivat identiteedipakkuja väärtust.</span><span class="sxs-lookup"><span data-stu-id="eb822-136">This value will help avoid incorrect authentication calls that might result in errors if a valid identity provider value is used.</span></span>  
 - <span data-ttu-id="eb822-137">Väliste või külaliskasutajate jaoks lisage nende Azure AD rentniku nimi aadressi https://sts.windows.net/ järel.</span><span class="sxs-lookup"><span data-stu-id="eb822-137">For external or guest users, add their Azure AD tenant name after https://sts.windows.net/.</span></span>
6. <span data-ttu-id="eb822-138">Sisestage väljale **Meil** kasutaja täispikk meil / kasutaja üldnimi.</span><span class="sxs-lookup"><span data-stu-id="eb822-138">In the **Email** field, enter the user's full Email/User Principle Name.</span></span>  
7. <span data-ttu-id="eb822-139">Valige väljal **Ettevõte** kasutaja vaikimisi avatav ettevõte.</span><span class="sxs-lookup"><span data-stu-id="eb822-139">In the **Company** field, select the default startup company for the user.</span></span> 
8. <span data-ttu-id="eb822-140">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="eb822-140">Select **Save**.</span></span>

<span data-ttu-id="eb822-141">Identiteedipakkuja ja telemeetria ID väärtusi värskendatakse [Microsofti graafiku](https://docs.microsoft.com/graph/overview) kutse põhjal, kui kasutajakirje salvestatakse.</span><span class="sxs-lookup"><span data-stu-id="eb822-141">The values for Identity provider and Telemetry ID will be updated based on a [Microsoft graph](https://docs.microsoft.com/graph/overview) call, when the user record is saved.</span></span> <span data-ttu-id="eb822-142">Telemeetria ID põhineb kasutaja objekti ID-l / turbeidentifikaatoril (SID) Azure AD-s.</span><span class="sxs-lookup"><span data-stu-id="eb822-142">The Telemetry ID is based on the user's Object ID/Security Identifier (SID) in Azure AD.</span></span>

> [!NOTE]
> <span data-ttu-id="eb822-143">Pärast kasutaja lisamist peate määrama vastavalt vajadusele rollid ja organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="eb822-143">After you add a user, you must assign roles and organizations as applicable.</span></span> <span data-ttu-id="eb822-144">Lisainfo saamiseks vt [Kasutajatele turberollide määramine](assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="eb822-144">For more information, see [Assign users to security roles](assign-users-security-roles.md).</span></span> <span data-ttu-id="eb822-145">Tingimuslikult võib olla nõutav ka kasutaja seostamine **isikuga** ja **kasutaja valikute** uuendamine, nt keel.</span><span class="sxs-lookup"><span data-stu-id="eb822-145">Conditionally, it might also be required to associate the user with a **Person** and to update **User options** such as language.</span></span>

## <a name="change-a-user-id"></a><span data-ttu-id="eb822-146">Kasutaja ID muutmine</span><span class="sxs-lookup"><span data-stu-id="eb822-146">Change a user ID</span></span>
<span data-ttu-id="eb822-147">Kasutaja ID muutmiseks peate võtme andmebaasis ümber nimetama.</span><span class="sxs-lookup"><span data-stu-id="eb822-147">To change a user ID, you must rename the key in the database.</span></span> <span data-ttu-id="eb822-148">Kui muudate seda protseduuri kasutades kasutaja ID, muudetakse kõiki seotud kasutajasätteid, et kasutada uut kasutaja ID-d.</span><span class="sxs-lookup"><span data-stu-id="eb822-148">When you change a user ID by using this procedure, all related user settings are modified to use the new user ID.</span></span> <span data-ttu-id="eb822-149">Näiteks tabeli **SysLastValue** kasutusteavet värskendatakse, et see viitaks uuele kasutaja ID-le.</span><span class="sxs-lookup"><span data-stu-id="eb822-149">For example, the usage information in the **SysLastValue** table is updated to reference the new user ID.</span></span>

> [!NOTE]
> <span data-ttu-id="eb822-150">Kasutaja ID on kasutajateabe tabeli primaarvõti.</span><span class="sxs-lookup"><span data-stu-id="eb822-150">The user ID is the primary key of the user information table.</span></span> <span data-ttu-id="eb822-151">Primaarvõtme ümbernimetamine võib olemasoleva kasutaja puhul võtta aega, kuna kõiki võtme viiteid värskendatakse ka andmebaasis.</span><span class="sxs-lookup"><span data-stu-id="eb822-151">Renaming the primary key can take some time for existing users because all references to the key are also updated in the database.</span></span> 

1. <span data-ttu-id="eb822-152">Minge jaotisse **Süsteemihaldus \> Kasutajad \> Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="eb822-152">Go to **System administration \> Users \> Users**.</span></span>
2. <span data-ttu-id="eb822-153">Valige loendist kasutaja ja valige **Suvandid\> Kirje teave**.</span><span class="sxs-lookup"><span data-stu-id="eb822-153">Select a user in the list and select **Options\> Record info**.</span></span>
3. <span data-ttu-id="eb822-154">Valige nupp **Nimeta ümber**.</span><span class="sxs-lookup"><span data-stu-id="eb822-154">Select **Rename**.</span></span>
4. <span data-ttu-id="eb822-155">Sisestage kasutaja ID uus ja ainulaadne väärtus ning valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb822-155">Enter a new and unique value for the User ID, and then select **OK**.</span></span> 
5. <span data-ttu-id="eb822-156">Kinnitamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="eb822-156">Select **Yes** to confirm.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb822-157">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="eb822-157">Additional resources</span></span>

<span data-ttu-id="eb822-158">Lisateavet B2B kasutajate juurutamiseks vt [B2B kasutajate eksportimine Azure AD-sse](../implement-b2b.md).</span><span class="sxs-lookup"><span data-stu-id="eb822-158">For more options to implement B2B users, see [Export B2B users to Azure AD](../implement-b2b.md).</span></span>

<span data-ttu-id="eb822-159">Lisateavet eelkonfigureeritud süsteemikontode kohta vt [Eelkonfigureeritud süsteemikontod](../pre-configured-system-accounts.md)</span><span class="sxs-lookup"><span data-stu-id="eb822-159">For information about preconfigured system accounts, see [Preconfigured system accounts](../pre-configured-system-accounts.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]