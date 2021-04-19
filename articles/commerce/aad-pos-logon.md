---
title: Luba Azure Active Directory kassa sisselogimise autentimine
description: See teema selgitab, kuidas konfigureerida Microsoft Microsoft Dynamics 365 Commerce'i kassasse (POS) sisselogimise kogemust nii, et see kasutab Azure Active Directory autentimist.
author: boycezhu
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 50088aee8c2474708682c9041251d2336e84d971
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796338"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="20f81-103">Azure Active Directory autentimise lubamine kassasse sisselogimiseks</span><span class="sxs-lookup"><span data-stu-id="20f81-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="20f81-104">Paljud kliendid, kes kasutavad Microsoft Microsoft Dynamics 365 Commerce'i, kasutavad ka teisi Microsofti pilveteenuseid ja võivad Azure Active Directory kasutada (Azure AD) nende teenuste kasutaja mandaadi haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="20f81-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="20f81-105">Sel juhul võivad kliendid soovida kasutada sama Azure AD kontot kõigis rakendustes.</span><span class="sxs-lookup"><span data-stu-id="20f81-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="20f81-106">See teema selgitab, kuidas konfigureerida kaubanduse kassasse (POS) sisselogimise kogemust nii, et see kasutab Azure AD autentimist.</span><span class="sxs-lookup"><span data-stu-id="20f81-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="20f81-107">Autentimise Azure AD konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="20f81-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="20f81-108">Kaupluse Azure AD jaoks kassa sisselogimise autentimise meetodina kättesaadavaks tegemiseks tuleb teil konfigureerida kaupluse funktsionaalsuse profiili sätted ja rakendada need sätted POS klientidele.</span><span class="sxs-lookup"><span data-stu-id="20f81-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="20f81-109">Funktsionaalsuse profiili konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="20f81-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="20f81-110">Avage **Jaemüük ja kaubandus** \> **Kanali seadistus** \> **Kassa seadistus** \> **Kassaprofiilid** \> **Funktsiooniprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="20f81-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="20f81-111">Valige muudetava funktsionaalsuse profiil.</span><span class="sxs-lookup"><span data-stu-id="20f81-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="20f81-112">Muutke FastTab **funktsioonid** jaotises **POS personali sisselogimine** **väärtuseks sisselogimise autentimise meetodi** väljale **personali ID ja parool** **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="20f81-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="20f81-113">Vaikimisi kasutavad kõik funktsionaalsuse profiilid **töötaja ID-d ja parooli** POS-i autentimise meetodina.</span><span class="sxs-lookup"><span data-stu-id="20f81-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="20f81-114">Seega, kui soovite kasutada Azure AD , peate muutma **sisselogimise autentimise meetodi** välja väärtust.</span><span class="sxs-lookup"><span data-stu-id="20f81-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="20f81-115">See muudatus mõjutab kõiki jaekaupluseid, mis on valitud funktsiooniprofiiliga ühendatud.</span><span class="sxs-lookup"><span data-stu-id="20f81-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="20f81-116">Sätete rakendamiseks kassa klientidele tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="20f81-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="20f81-117">Avage **Jaemüük ja kaubandus** \> **Jaemüügi ja kaubanduse IT** \> **Jaotusgraafik**.</span><span class="sxs-lookup"><span data-stu-id="20f81-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="20f81-118">Käivitage **1070** (**Kanali konfiguratsioon**) jaotusgraafik.</span><span class="sxs-lookup"><span data-stu-id="20f81-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="20f81-119">Azure AD autentimine vajab Interneti-ühendust.</span><span class="sxs-lookup"><span data-stu-id="20f81-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="20f81-120">See ei tööta, kui kassa töötab ühenduseta režiimis.</span><span class="sxs-lookup"><span data-stu-id="20f81-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="20f81-121">Praegu ei toeta funktsioon **Halduri alistamine** Azure AD-d autentimismeetodina.</span><span class="sxs-lookup"><span data-stu-id="20f81-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="20f81-122">Operaatori ID-d ja parooli nõutakse ka siis, kui Azure AD on konfigureeritud kassa sisselogimise autentimismeetodina.</span><span class="sxs-lookup"><span data-stu-id="20f81-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="20f81-123">Konto Azure AD seostamine töötajaga</span><span class="sxs-lookup"><span data-stu-id="20f81-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="20f81-124">Enne kui kaupluse töötaja saab kasutada kontot Azure AD, et sisse logida kassa rakendusse, peab konto Azure AD olema seotud selle töötajaga.</span><span class="sxs-lookup"><span data-stu-id="20f81-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="20f81-125">Konto Azure AD seostamiseks töötajaga toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="20f81-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="20f81-126">Avage **Jaemüük ja kaubandus** \> **Palgalised** \> **Töötajad**.</span><span class="sxs-lookup"><span data-stu-id="20f81-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="20f81-127">Avage töötaja üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="20f81-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="20f81-128">Valige tegumiriba vahekaardil **Kaubandus** grupis **Välisidentiteet** , valige **Olemasoleva identiteedi seostamine**.</span><span class="sxs-lookup"><span data-stu-id="20f81-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="20f81-129">Dialoogiaknas **Kasuta olemasolevat välisidentiteeti** valige **Otsi kasutades e-posti**, sisestage Azure AD e-posti aadress ja seejärel valige **Otsing**.</span><span class="sxs-lookup"><span data-stu-id="20f81-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="20f81-130">Valige saadud konto Azure AD ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="20f81-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="20f81-131">Täidetakse väljad **Alias**, **UPN** ja **Väline alamidentifikaator** töötaja üksikasjade lehe vahekaardil **Kaubandus** .</span><span class="sxs-lookup"><span data-stu-id="20f81-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="20f81-132">Pärast töötaja kirje uuendamist, näiteks pärast uue Azure AD konto seostamist, parooli muutmist või töövõtja aadressiraamatu uuendamist, soovitatakse käitada jaotusgraafik **1060** (**Personal**), et sünkroonida uusim personaliteave kanaliga.</span><span class="sxs-lookup"><span data-stu-id="20f81-132">After a worker record is updated, for example if a new Azure AD account is associated, a password is changed, or an employee address book is updated, it’s recommended that you run **1060** (**Staff**) distribution schedule to synchronize the latest staff information to the channel.</span></span> <span data-ttu-id="20f81-133">Nii saab kassarakendus tuua õigeid andmeid kasutaja autentimiseks ja autoriseerimise kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="20f81-133">That way, the POS application can fetch the correct data for user authentication and authorization check.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="20f81-134">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="20f81-134">Additional resources</span></span>

[<span data-ttu-id="20f81-135">MPOS-i ja pilve kassa laiendatud sisselogimisfunktsiooni häälestus</span><span class="sxs-lookup"><span data-stu-id="20f81-135">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="20f81-136">Jaemüügi funktsiooniprofiili loomine</span><span class="sxs-lookup"><span data-stu-id="20f81-136">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="20f81-137"> Töötaja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="20f81-137">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)


[!INCLUDE[footer-include](../includes/footer-banner.md)]