---
title: Sisselogimislingi ümbersuunamised tagasi e-äri saidile
description: See teema pakub tõrkeotsingu juhiseid, mis aitavad teil sisselogimise lingil tagasi e-äri saidile ümber suunata, selle asemel et minna sisselogimislehele.
author: Reza-Assadi
manager: AnnBe
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
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36f10c9f68570a6c67da6b4b6e4155f4634f633a
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585277"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="fda03-103">Sisselogimislingi ümbersuunamised tagasi e-äri saidile</span><span class="sxs-lookup"><span data-stu-id="fda03-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fda03-104">See teema pakub tõrkeotsingu juhiseid, mis aitavad teil sisselogimise lingil tagasi e-äri saidile ümber suunata, selle asemel et minna sisselogimislehele.</span><span class="sxs-lookup"><span data-stu-id="fda03-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="fda03-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="fda03-105">Description</span></span>

<span data-ttu-id="fda03-106">Pärast uue Microsoft Azure Active Directory B2C (Azure AD B2C) rentniku konfigureerimist Commerce'i saidi koostajas, kes valisid **sisselogimise** suunatakse kasutajad tagasi, ilma sisselogimislehele minemata.</span><span class="sxs-lookup"><span data-stu-id="fda03-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="fda03-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="fda03-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="fda03-108">Veenduge, et vastuse URL on Azure AD B2C-rakenduses õigesti konfigureeritud</span><span class="sxs-lookup"><span data-stu-id="fda03-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="fda03-109">Veenduge, et vastuse URL on Azure AD B2C-rakenduses õigesti konfigureeritud, järgides järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="fda03-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="fda03-110">Avage [Azure’i portaalis](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="fda03-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="fda03-111">Valige Azure AD B2C-rakendus, mille lõite oma saidi juurdepääsuks.</span><span class="sxs-lookup"><span data-stu-id="fda03-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="fda03-112">Valige rakendus, mille lõite Azure AD B2C-seadistuse ajal.</span><span class="sxs-lookup"><span data-stu-id="fda03-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="fda03-113">**Vastuse URLi** all veenduge, et loend sisaldab kirjeid nii saidi domeeni URL-i kui e-kaubanduse loodud URL-i kohta, nagu näidatud järgmises illustratsioonis.</span><span class="sxs-lookup"><span data-stu-id="fda03-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![Azure AD B2C-vastuse URL-i kirjed](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="fda03-115">Nii saidi domeeni URL kui ka e-äri loodud URL peavad olema kehtivas URL-vormingus, mis ei sisalda lõpu- või lõpukriipse.</span><span class="sxs-lookup"><span data-stu-id="fda03-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fda03-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="fda03-116">Additional resources</span></span>

[<span data-ttu-id="fda03-117">Ühendatud rakenduse registreerimine Azure Active Directory B2C</span><span class="sxs-lookup"><span data-stu-id="fda03-117">Register a web application in Azure Active Directory B2C</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="fda03-118">B2C-rentniku häälestus Commerce'is</span><span class="sxs-lookup"><span data-stu-id="fda03-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)
