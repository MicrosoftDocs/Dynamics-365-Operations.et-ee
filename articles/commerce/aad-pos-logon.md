---
title: Luba Azure Active Directory kassa sisselogimise autentimine
description: See teema selgitab, kuidas konfigureerida Microsoft Dynamics 365 Commerce'i kassasse (POS) sisselogimise kogemust nii, et see kasutab Azure Active Directory autentimist.
author: boycezhu
manager: annbe
ms.date: 03/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: dfc49585434383385b6b993893d93b95ef888384
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248936"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="073c0-103">Luba Azure Active Directory kassa sisselogimise autentimine</span><span class="sxs-lookup"><span data-stu-id="073c0-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="073c0-104">Paljud kliendid, kes kasutavad Microsoft Dynamics 365 Commerce'i, kasutavad ka teisi Microsoft pilve teenuseid ja võivad Azure Active Directory kasutada (Azure AD) nende teenuste kasutaja mandaadi haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="073c0-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="073c0-105">Sel juhul võivad kliendid soovida kasutada sama Azure AD kontot kõigis rakendustes.</span><span class="sxs-lookup"><span data-stu-id="073c0-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="073c0-106">See teema selgitab, kuidas konfigureerida kaubanduse kassasse (POS) sisselogimise kogemust nii, et see kasutab Azure AD autentimist.</span><span class="sxs-lookup"><span data-stu-id="073c0-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="073c0-107">Autentimise Azure AD konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="073c0-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="073c0-108">Kaupluse Azure AD jaoks kassa sisselogimise autentimise meetodina kättesaadavaks tegemiseks tuleb teil konfigureerida kaupluse funktsionaalsuse profiili sätted ja rakendada need sätted POS klientidele.</span><span class="sxs-lookup"><span data-stu-id="073c0-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="073c0-109">Funktsionaalsuse profiili konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="073c0-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="073c0-110">Avage **Jaemüük ja kaubandus** \> **Kanali seadistus** \> **Kassa seadistus** \> **Kassaprofiilid** \> **Funktsiooniprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="073c0-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="073c0-111">Valige muudetava funktsionaalsuse profiil.</span><span class="sxs-lookup"><span data-stu-id="073c0-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="073c0-112">Muutke FastTab **funktsioonid** jaotises **POS personali sisselogimine** **väärtuseks sisselogimise autentimise meetodi** väljale **personali ID ja parool** **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="073c0-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="073c0-113">Vaikimisi kasutavad kõik funktsionaalsuse profiilid **töötaja ID-d ja parooli** POS-i autentimise meetodina.</span><span class="sxs-lookup"><span data-stu-id="073c0-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="073c0-114">Seega, kui soovite kasutada Azure AD , peate muutma **sisselogimise autentimise meetodi** välja väärtust.</span><span class="sxs-lookup"><span data-stu-id="073c0-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="073c0-115">See muudatus mõjutab kõiki jaekaupluseid, mis on valitud funktsiooniprofiiliga ühendatud.</span><span class="sxs-lookup"><span data-stu-id="073c0-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="073c0-116">Sätete rakendamiseks kassa klientidele tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="073c0-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="073c0-117">Avage **Jaemüük ja kaubandus** \> **Jaemüügi ja kaubanduse IT** \> **Jaotusgraafik**.</span><span class="sxs-lookup"><span data-stu-id="073c0-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="073c0-118">Käivitage **1070** (**Kanali konfiguratsioon**) jaotusgraafik.</span><span class="sxs-lookup"><span data-stu-id="073c0-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="073c0-119">Azure AD autentimine vajab Interneti-ühendust.</span><span class="sxs-lookup"><span data-stu-id="073c0-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="073c0-120">See ei tööta, kui kassa töötab ühenduseta režiimis.</span><span class="sxs-lookup"><span data-stu-id="073c0-120">It won't work when POS is in offline mode.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="073c0-121">Konto Azure AD seostamine töötajaga</span><span class="sxs-lookup"><span data-stu-id="073c0-121">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="073c0-122">Enne kui kaupluse töötaja saab kasutada kontot Azure AD, et sisse logida kassa rakendusse, peab konto Azure AD olema seotud selle töötajaga.</span><span class="sxs-lookup"><span data-stu-id="073c0-122">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="073c0-123">Konto Azure AD seostamiseks töötajaga toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="073c0-123">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="073c0-124">Avage **Jaemüük ja kaubandus** \> **Palgalised** \> **Töötajad**.</span><span class="sxs-lookup"><span data-stu-id="073c0-124">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="073c0-125">Avage töötaja üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="073c0-125">Open the details page for a worker.</span></span>
1. <span data-ttu-id="073c0-126">Valige tegumiriba vahekaardil **Kaubandus** grupis **Välisidentiteet** , valige **Olemasoleva identiteedi seostamine**.</span><span class="sxs-lookup"><span data-stu-id="073c0-126">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="073c0-127">Dialoogiaknas **Kasuta olemasolevat välisidentiteeti** valige **Otsi kasutades e-posti**, sisestage Azure AD e-posti aadress ja seejärel valige **Otsing**.</span><span class="sxs-lookup"><span data-stu-id="073c0-127">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="073c0-128">Valige saadud konto Azure AD ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="073c0-128">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="073c0-129">Täidetakse väljad **Alias**, **UPN**ja **Väline alamidentifikaator** töötaja üksikasjade lehe vahekaardil **Kaubandus** .</span><span class="sxs-lookup"><span data-stu-id="073c0-129">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="073c0-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="073c0-130">Additional resources</span></span>

[<span data-ttu-id="073c0-131">MPOS-i ja pilve kassa laiendatud sisselogimisfunktsiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="073c0-131">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="073c0-132">Jaemüügi funktsiooniprofiili loomine</span><span class="sxs-lookup"><span data-stu-id="073c0-132">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="073c0-133"> Töötaja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="073c0-133">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
