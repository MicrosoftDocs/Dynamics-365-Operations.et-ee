---
title: Soodustuste haldamise parameetrite konfigureerimine ettevõtte kohta
description: Konfigureerige soodustuste halduse parameetreid ettevõtte kohta rakenduses Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 31f30c3d268132327074e931b714b5b2ee3ec5ac
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466636"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="47d8b-103">Soodustuste haldamise parameetrite konfigureerimine ettevõtte kohta</span><span class="sxs-lookup"><span data-stu-id="47d8b-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="47d8b-104">Iga soodustust pakkuva organisatsiooni jaoks peate konfigureerima soodustuste kinnitusmeilide sätted.</span><span class="sxs-lookup"><span data-stu-id="47d8b-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="47d8b-105">Kinnitusmeilide sätete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="47d8b-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="47d8b-106">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Human Resourcesi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="47d8b-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="47d8b-107">Määrake vahekaardil **Soodustuste haldus** järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="47d8b-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="47d8b-108">Field</span><span class="sxs-lookup"><span data-stu-id="47d8b-108">Field</span></span> | <span data-ttu-id="47d8b-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="47d8b-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="47d8b-110">**Saada kinnitusmeil**</span><span class="sxs-lookup"><span data-stu-id="47d8b-110">**Send confirmation email**</span></span> | <span data-ttu-id="47d8b-111">Kui see funktsioon on sisse lülitatud, saadetakse töövõtjatele kinnitusmeili, kui nad registreerivad soodustuste registreerimise töövõtja iseteeninduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="47d8b-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="47d8b-112">**Kinnitusmeili mall**</span><span class="sxs-lookup"><span data-stu-id="47d8b-112">**Confirmation email template**</span></span> | <span data-ttu-id="47d8b-113">Valige organisatsiooni meilisõnumi mall, mida kasutada registreerimise kinnituse saatmisel.</span><span class="sxs-lookup"><span data-stu-id="47d8b-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="47d8b-114">Kui te malli ei vali, saadetakse järgmine üldine meilisõnum.</span><span class="sxs-lookup"><span data-stu-id="47d8b-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="47d8b-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="47d8b-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="47d8b-116">Õnnitleme!</span><span class="sxs-lookup"><span data-stu-id="47d8b-116">Congratulations!</span></span> <span data-ttu-id="47d8b-117">Olete soodustuste registreerimise edukalt lõpule viinud.</span><span class="sxs-lookup"><span data-stu-id="47d8b-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="47d8b-118">Suur tänu!</span><span class="sxs-lookup"><span data-stu-id="47d8b-118">Thank you,</span></span><br><span data-ttu-id="47d8b-119">Ettevõtte <Company/Org name> soodustused.</span><span class="sxs-lookup"><span data-stu-id="47d8b-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="47d8b-120">**Vaikimisi meilisõnumi saatja aadress**</span><span class="sxs-lookup"><span data-stu-id="47d8b-120">**Default email sender address**</span></span> | <span data-ttu-id="47d8b-121">Meiliaadress, mida kasutada kinnitusmeili saatmisel.</span><span class="sxs-lookup"><span data-stu-id="47d8b-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="47d8b-122">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="47d8b-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]