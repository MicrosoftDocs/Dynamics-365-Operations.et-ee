---
title: Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK
description: Selles teemas antakse vastused korduma kippuvate küsimustele Microsoft Dynamics 365 Commerce ja Microsoft Teams integratsiooni kohta.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bf9aebb1c8ba7cf4fee3f0471a10872de1e23ce6
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908852"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="c866b-103">Dynamics 365 Commerce ja Microsoft Teams integratsiooni KKK</span><span class="sxs-lookup"><span data-stu-id="c866b-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c866b-104">Selles teemas antakse vastused korduma kippuvate küsimustele Microsoft Dynamics 365 Commerce ja Microsoft Teams integratsiooni kohta.</span><span class="sxs-lookup"><span data-stu-id="c866b-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="c866b-105">Kes poes saab Commerce'i Teamsi ettevalmistamise ajal töörühmade omanikuks?</span><span class="sxs-lookup"><span data-stu-id="c866b-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="c866b-106">Kõik kaupluste juhatajad lisatakse automaatselt vastavasse töörühmagruppi omanikena, et nad saaksid sooritada toiminguid, nagu privaatse kanali lisamine ning liikmete lisamine või kustutamine.</span><span class="sxs-lookup"><span data-stu-id="c866b-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="c866b-107">Kuidas määrata Commerce'i peakontoris töötajale "sidehalduri" roll?</span><span class="sxs-lookup"><span data-stu-id="c866b-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="c866b-108">Kommunikatsioonihaldurid Microsoft Teams rakenduses saavad luua ja avaldada ülesannete loendeid.</span><span class="sxs-lookup"><span data-stu-id="c866b-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="c866b-109">Organisatsiooni töötajatel, kellest saavad kommunikatsioonihaldurid, peab olema Commerce peakontoris määratud jaemüügi ülesandehalduri roll.</span><span class="sxs-lookup"><span data-stu-id="c866b-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="c866b-110">Jaemüügi ülesandehalduri rolli määramiseks töötajale Commerce peakontoris toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="c866b-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="c866b-111">Avage **Jaemüük ja kaubandus \> Töötajad \> Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="c866b-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="c866b-112">Valige töötaja.</span><span class="sxs-lookup"><span data-stu-id="c866b-112">Select an employee.</span></span>
1. <span data-ttu-id="c866b-113">Kiirkaardil **Kasutaja rollid** valige suvand **Määra rollid**.</span><span class="sxs-lookup"><span data-stu-id="c866b-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="c866b-114">Dialoogiboksis **Määra kasutajale rollid** valige roll **Jaemüügi ülesannete haldur** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c866b-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="c866b-115">Kuidas teha konkreetne organisatsiooni hierarhia üleslaadimiseks Microsoft Teams rakenduses kättesaadavaks?</span><span class="sxs-lookup"><span data-stu-id="c866b-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="c866b-116">Commerce peakontoris on iga organisatsiooni hierarhia seostatud ühe või mitme eesmärgiga.</span><span class="sxs-lookup"><span data-stu-id="c866b-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="c866b-117">Veenduge, et hierarhial, kuhu soovite eraldise Microsoft Teams teha, oleks seostatud **jaemüügi aruandluse** eesmärgiga, nagu näha järgmises näitepildis.</span><span class="sxs-lookup"><span data-stu-id="c866b-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![Organisatsiooni hierarhia eesmärgi näide Commerce'i peakontoris](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="c866b-119">Kuidas lubada kaupluse töötajatel Azure Active Directory (Azure AD) kasutades Commerce kassasse sisse logida?</span><span class="sxs-lookup"><span data-stu-id="c866b-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="c866b-120">Teavet Commerce POS-i sisselogimiskogemuse konfigureerimise kohta Azure AD autentimise kasutamiseks vt [Luba Azure Active Directory autentimine POS sisselogimiseks](aad-pos-logon.md).</span><span class="sxs-lookup"><span data-stu-id="c866b-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="c866b-121">Kuidas vastendada kauplusi ja vastavaid meeskondi Commerce peakontoris, kui minu organisatsioon on juba loonud Microsoft Teams meeskonnad?</span><span class="sxs-lookup"><span data-stu-id="c866b-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="c866b-122">Lisateavet kaupluste ja töörühmade vastendamise kohta olemasolevate töörühmade korral vaadake jaotisest [Kaupluste ja vastavate töörühmade vastendamine, kui teie organisatsioonil on olemas eelnevalt olemas olevad meeskonnad rakenduses Microsoft Teams](map-stores-existing-teams.md).</span><span class="sxs-lookup"><span data-stu-id="c866b-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="c866b-123">Kuidas tühjendada seansi talletusse salvestatud Microsoft Graph API tookenit?</span><span class="sxs-lookup"><span data-stu-id="c866b-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="c866b-124">Kasutaja, kes on kassasse sisse loginud Azure Active Directory (Azure AD) kontoga, peaks kassast välja logima või sulgema rakenduse, et seansi ladustamine kustutada.</span><span class="sxs-lookup"><span data-stu-id="c866b-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="c866b-125">Soovitatav on töötajatel kassaterminali alati lukustada või seansist välja logida, kui terminali ei kasutata.</span><span class="sxs-lookup"><span data-stu-id="c866b-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="c866b-126">Mis juhtub, kui kauplusel ei ole kaupluse juhatajaid?</span><span class="sxs-lookup"><span data-stu-id="c866b-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="c866b-127">Kui kauplusel ei ole juhatajaid, siis kaupluse või Teamsi gruppi ei looda.</span><span class="sxs-lookup"><span data-stu-id="c866b-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="c866b-128">Mis juhtub, kui kaupluse juhataja ettevõttest lahkub?</span><span class="sxs-lookup"><span data-stu-id="c866b-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="c866b-129">Kõik omanikurolliga isikud saavad Commerce peakontoris lisada uue kauplusehalduri ja uuesti ette valmistada Teamsi, et uuel halduril oleks Teamsi grupi jaoks vajalikud privileegid.</span><span class="sxs-lookup"><span data-stu-id="c866b-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="c866b-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c866b-130">Additional resources</span></span>

[<span data-ttu-id="c866b-131">Dynamics 365 Commerce ja Microsoft Teams integratsiooni ülevaade</span><span class="sxs-lookup"><span data-stu-id="c866b-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="c866b-132">Dynamics 365 Commerce ja Microsoft Teams integratsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="c866b-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="c866b-133">Microsoft Teams sätted rakendusest Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c866b-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="c866b-134">Ülesannete halduse sünkroonimine Microsoft Teams ja Dynamics 365 Commerce kassade vahel</span><span class="sxs-lookup"><span data-stu-id="c866b-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="c866b-135">Kasutaja rollide haldamine rakenduses Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c866b-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="c866b-136">Kaupluste ja töörühmade vastendamine, kui töörühmad on olemas rakenduses Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="c866b-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
