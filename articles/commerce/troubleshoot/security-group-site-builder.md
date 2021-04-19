---
title: Ärisaidi koostaja turbegruppi ei saa algse juurutamise ajal konfigureerida
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui Microsoft Azure Active Directory (Azure AD) ärisaidi koostaja turvagruppi ei kuvata suvandina, kui loote Lifecycle Services (LCS) e-äri komponente uue e-äri rentniku algsel Microsoft Dynamics juurutamisel.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: aa00e9331693600ced2f4ead399a0c005b77ad08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801503"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="a1be6-103">Ärisaidi koostaja turbegruppi ei saa algse juurutamise ajal konfigureerida</span><span class="sxs-lookup"><span data-stu-id="a1be6-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a1be6-104">See teema annab tõrkeotsingu juhised, mis aitavad, kui Microsoft Azure Active Directory (Azure AD) ärisaidi koostaja turvagruppi ei kuvata suvandina, kui loote Lifecycle Services (LCS) e-äri komponente uue e-äri rentniku algsel Microsoft Dynamics juurutamisel.</span><span class="sxs-lookup"><span data-stu-id="a1be6-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="a1be6-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a1be6-105">Description</span></span>

<span data-ttu-id="a1be6-106">Kui loote e-äri komponendid osana uue e-äri rentniku, sealhulgas Commerce'i saidikonstruktori komponenti juurutamisprotsessist, ei kuvata turbegruppi dialoogiboksi Azure AD suvandina.</span><span class="sxs-lookup"><span data-stu-id="a1be6-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="a1be6-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="a1be6-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="a1be6-108">E-kaubanduse saidi ettevalmistamine õiges rentnikus kasutajaga</span><span class="sxs-lookup"><span data-stu-id="a1be6-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="a1be6-109">Avage [Azure’i portaalis](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="a1be6-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="a1be6-110">Rentniku all, kelle jaoks teie e-äri saidi LCS-projekt oli ette antud, järgige juhiseid jaotises [Põhigrupi loomine ja liikmete lisamine Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="a1be6-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="a1be6-111">Minge [LCS](https://lcs.dynamics.com/) ja logige sisse kontoga, mis jagab äsja loodud turvagrupiga Azure AD sama rentnikku.</span><span class="sxs-lookup"><span data-stu-id="a1be6-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="a1be6-112">Kontol peab olema turvagrupi Azure AD vaatamiseks juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="a1be6-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="a1be6-113">E-äri saidi konfigureerimiseks viige lõpule seadistuse sammud.</span><span class="sxs-lookup"><span data-stu-id="a1be6-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="a1be6-114">Kui te e-äri komponente ette kasutate, peaks turvagrupp olema dialoogiaknas valikuna.</span><span class="sxs-lookup"><span data-stu-id="a1be6-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="a1be6-115">Kindlustamaks, et dialoogiboksi väli täidetakse turvagruppide loendiga, peate valima **Enter** pärast loodud turvagrupi nime Azure AD turvagruppi sisestamist.</span><span class="sxs-lookup"><span data-stu-id="a1be6-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="a1be6-116">Otsingutulemustes loetletakse Azure AD kõik turvagrupid, mis algavad otsingutekstiga ja neile on kasutajal juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="a1be6-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="a1be6-117">Pikema otsingutulemuse võimaldamiseks saate kasutada lühemat otsingusõna.</span><span class="sxs-lookup"><span data-stu-id="a1be6-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1be6-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a1be6-118">Additional resources</span></span>

[<span data-ttu-id="a1be6-119">Looge põhigrupp ja lisage liikmeid, kasutades Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a1be6-119">Create a basic group and add members using Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="a1be6-120">Uue e-kaubanduse rentniku juurutamine</span><span class="sxs-lookup"><span data-stu-id="a1be6-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)
