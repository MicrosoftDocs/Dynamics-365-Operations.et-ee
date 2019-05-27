---
title: Kasutajat ei leitud Attractis või Onboardis inimeste valijast
description: Selles teemas selgitatakse, mida teha, kui ettevõtte rentnikus olevaid kasutajaid ei kuvata rakendustes Dynamics 365 for Talent Attract või Onboard inimeste valijas.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5a2c61fc21578d1db4c1bf0c3dfaf0c7a93298c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517796"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a><span data-ttu-id="614df-103">Azure Active Directory kasutajaid ei leitud inimeste valijast</span><span class="sxs-lookup"><span data-stu-id="614df-103">Azure Active Directory users not found in People Picker</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="614df-104">Väljastamine</span><span class="sxs-lookup"><span data-stu-id="614df-104">Issue</span></span>

<span data-ttu-id="614df-105">Microsoft Azure Active Directorys (Azure AD) ei kuvata rentniku puhul teatud kehtivaid kasutajaid, kui rakenduses Dynamics 365 for Talent Attract või Onboard otsitakse inimeste valijas kasutajaid nime järgi.</span><span class="sxs-lookup"><span data-stu-id="614df-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in the Dynamics 365 for Talent Attract or Onboard applications.</span></span>

## <a name="cause"></a><span data-ttu-id="614df-106">Põhjus</span><span class="sxs-lookup"><span data-stu-id="614df-106">Cause</span></span>

<span data-ttu-id="614df-107">Rakendused Attract ja Onboard ei toeta praegu teatud kasutajatüüpe.</span><span class="sxs-lookup"><span data-stu-id="614df-107">Certain user types are not currently supported in the Attract and Onboard applications.</span></span> <span data-ttu-id="614df-108">Veenduge, et kasutaja ei oleks lahenduse Azure AD Business to Business (B2B) külaliskasutaja.</span><span class="sxs-lookup"><span data-stu-id="614df-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="614df-109">Kasutaja tüübi teabe leiate Azure’i portaalis Azure Active Directory labal.</span><span class="sxs-lookup"><span data-stu-id="614df-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="614df-110">Lisateavet Azure B2B kohta vt teemast [Mis on külaliskasutaja juurdepääs Azure Active Directory B2B-s](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="614df-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="614df-111">Mitte-B2B kasutajate puhul on olemas teatud kasutajad, kellel võib olla objektis **Kasutaja** puudulik atribuut Kasutaja tüüp.</span><span class="sxs-lookup"><span data-stu-id="614df-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="614df-112">Seda saab kontrollida ja parandada Azure AD mooduliga Powershell.</span><span class="sxs-lookup"><span data-stu-id="614df-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="614df-113">Lisateavet vt [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="614df-113">For more information, see [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="614df-114">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="614df-114">Resolution</span></span>

<span data-ttu-id="614df-115">Probleemi lahendamiseks tuleb teha järgmised toimingud ja selleks peavad teil olema Azure Active Directory rentnikus üldadministraatori õigused või õigused **User.ReadWrite.All**.</span><span class="sxs-lookup"><span data-stu-id="614df-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="614df-116">Mõjutatud kasutaja atribuudi Kasutaja tüüp kontrollimine.</span><span class="sxs-lookup"><span data-stu-id="614df-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="614df-117">Käsk tagastab järgmise teabe.</span><span class="sxs-lookup"><span data-stu-id="614df-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="614df-118">Vaadake kasutaja atribuuti **Kasutaja tüüp**.</span><span class="sxs-lookup"><span data-stu-id="614df-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="614df-119">Kui atribuut **Kasutaja tüüp** on tühi, olemata näiteks Liige või Külaline, värskendage atribuuti **Kasutaja tüüp** järgmist käsku kasutades.</span><span class="sxs-lookup"><span data-stu-id="614df-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
