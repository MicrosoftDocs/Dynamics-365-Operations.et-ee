---
title: Konfigureeri Azure Active Directory autentimise lubamine kassasse sisselogimiseks
description: See teema kirjeldab, kuidas konfigureerida Azure Active Directory müügis Microsoft Dynamics 365 Commerce autentimismeetodina.
author: boycezhu
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 34a7946a56a58655bc9ae23e060fc50ab01f2c6e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937454"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="25583-103">Konfigureeri Azure Active Directory autentimise lubamine kassasse sisselogimiseks</span><span class="sxs-lookup"><span data-stu-id="25583-103">Configure Azure Active Directory authentication for POS sign-in</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="25583-104">Selles peatükis kirjeldatakse, kuidas konfigureerida Azure Active Directory (Azure AD) autentimismeetodina Microsoft Dynamics 365 Commerce kassas (POS).</span><span class="sxs-lookup"><span data-stu-id="25583-104">This topic explains how to configure Azure Active Directory (Azure AD) as the authentication method in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="25583-105">Jaemüüjad, kes kasutavad koos Dynamics 365 Commerce Microsofti pilveteenustega Microsoft Azure (nt Microsoft 365) ja soovivad Microsoft Teams tavaliselt kasutada kasutaja mandaatide tsentraliseeritud haldust turvaliseks ja sujuvaks sisselogimiseks Azure AD rakendustes.</span><span class="sxs-lookup"><span data-stu-id="25583-105">Retailers who use Dynamics 365 Commerce along with other Microsoft cloud services such as Microsoft Azure, Microsoft 365, and Microsoft Teams typically want to use Azure AD for centralized management of user credentials for a secure and seamless sign-in experience across applications.</span></span> <span data-ttu-id="25583-106">Autentimise kasutamiseks Azure AD Commerce POS-i puhul peate esmalt Azure AD konfigureerima autentimismeetodina Commerce headquartersis.</span><span class="sxs-lookup"><span data-stu-id="25583-106">To use Azure AD authentication for Commerce POS, you must first configure Azure AD as the authentication method in Commerce headquarters.</span></span>

## <a name="configure-pos-authentication-method"></a><span data-ttu-id="25583-107">POSi autentimise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="25583-107">Configure POS authentication method</span></span>

<span data-ttu-id="25583-108">Commerce headquarters\`is kassa autentimise meetodi redigeerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="25583-108">To configure the POS authentication method in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="25583-109">Valige suvandid **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa profiilid \> Funktsiooniprofiilid** ja valige funktsionaalsuse profiil, mida soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="25583-109">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**, and select a functionality profile to change.</span></span>
1. <span data-ttu-id="25583-110">**Funktsiooni** kiirkaardi jaotises **Kassa personali sisselogimine** valige soovitud autentimismeetodi suvand **sisselogimise** autentimismeetodi ripploendist.</span><span class="sxs-lookup"><span data-stu-id="25583-110">In the **POS staff logon** section of the **Functions** FastTab, select a desired authentication method option from the **Logon authentication method** drop-down list.</span></span>

    <span data-ttu-id="25583-111">Sisselogimise **autentimismeetodil** on kolm valikut:</span><span class="sxs-lookup"><span data-stu-id="25583-111">The **Logon authentication method** has three options:</span></span>
    
    - <span data-ttu-id="25583-112">**Personali ID ja parool** – see vaikesuvand nõuab kassa kasutajatelt personali ID ja parooli sisestamist, et kassasse sisse logida ja pääseda juurde halduri alistamisfunktsioonile.</span><span class="sxs-lookup"><span data-stu-id="25583-112">**Personnel ID and Password** - This default option requires POS users to enter a personnel ID and password to sign in to the POS and to access manager override functionality.</span></span>
    - <span data-ttu-id="25583-113">**Azure AD ilma ühekordse sisselogimiseta** – see valik nõuab kassa kasutajatelt mandaatide kasutamist kassasse ja juurdepääsuhalduri Azure AD alistamisfunktsioonile sisse logimiseks.</span><span class="sxs-lookup"><span data-stu-id="25583-113">**Azure AD without single sign-on** - This option requires POS users to use Azure AD credentials to sign in to the POS and access manager override functionality.</span></span> <span data-ttu-id="25583-114">Kui müügikoha klienti värskendatakse või taasavatakse, peab kassa kasutaja Azure AD sisestama mandaadid uuesti sisse logimiseks.</span><span class="sxs-lookup"><span data-stu-id="25583-114">When the POS client is refreshed or reopened, the POS user must provide Azure AD credentials to sign in again.</span></span>
    - <span data-ttu-id="25583-115">**Azure AD ühekordse sisselogimisega** – selle suvandi valimisel saavad kassa kasutajad sisse logida Pilve kassasse (CPOS), kasutades aktiivseid Azure AD mandaate, mida kasutavad teised veebirakendused samas veebibrauseris, või logida Sisse Modern POS-i (MPOS) Azure AD mandaatide abil, mis on Windowsi sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="25583-115">**Azure AD with single sign-on** - When this option is selected, POS users are able to sign in to Cloud POS (CPOS) using active Azure AD credentials that are being used by other web applications in the same web browser, or sign in to Modern POS (MPOS) using Azure AD credentials signed in to Windows.</span></span> <span data-ttu-id="25583-116">Mõlemad meetodid võimaldavad sisselogimist ilma kassa sisselogimise ekraanile mandaate Azure AD sisestamata.</span><span class="sxs-lookup"><span data-stu-id="25583-116">Both methods allow sign-in without needing to enter Azure AD credentials on the POS sign-in screen.</span></span> <span data-ttu-id="25583-117">Kuid kassahalduri alistamisfunktsiooni poole pöördumine nõuab siiski sisselogimist Azure AD mandaatide abil.</span><span class="sxs-lookup"><span data-stu-id="25583-117">However, accessing the POS manager override functionality will still require sign-in using Azure AD credentials.</span></span>

1. <span data-ttu-id="25583-118">Minge jaemüügi ja äri > jaemüügi ja äri IT > jaotusgraafikusse **ja käitage** **1070 (kanali konfiguratsioon), et sünkroonida uusimad funktsiooniprofiili sätted** müügikoha klientidele.</span><span class="sxs-lookup"><span data-stu-id="25583-118">Go to **Retail and Commerce > Retail and Commerce IT > Distribution schedule** and run the **1070 (Channel configuration)** job to synchronize the latest functionality profile settings to POS clients.</span></span>

> [!NOTE]
> - <span data-ttu-id="25583-119">**Azure AD Autentimismeetodi ühekordse** sisselogimiseta suvand asendab Commerce'i versiooni **Azure Active Directory** 10.0.18 ja varasema variandi.</span><span class="sxs-lookup"><span data-stu-id="25583-119">The **Azure AD without single sign-on** authentication method option replaces the **Azure Active Directory** option in Commerce version 10.0.18 and earlier.</span></span>
> - <span data-ttu-id="25583-120">Azure AD autentimine nõuab aktiivset Interneti-ühendust ja see ei toimi, kui kassa on ühenduseta.</span><span class="sxs-lookup"><span data-stu-id="25583-120">Azure AD authentication requires an active internet connection, and won't function when the POS is offline.</span></span>

## <a name="associate-azure-ad-accounts-with-pos-users"></a><span data-ttu-id="25583-121">Kontode Azure AD seostamine müügikoha kasutajatega</span><span class="sxs-lookup"><span data-stu-id="25583-121">Associate Azure AD accounts with POS users</span></span>

<span data-ttu-id="25583-122">Kassa Azure AD autentimismeetodina kasutamiseks peate kontod seostama Azure AD rakenduse Commerce headquarters kassa kasutajatega.</span><span class="sxs-lookup"><span data-stu-id="25583-122">To use Azure AD as the POS authentication method, you must associate Azure AD accounts with POS users in Commerce headquarters.</span></span> 

<span data-ttu-id="25583-123">Kontode Azure AD seostamiseks müügikoha kasutajatega Commerce Headquartersis järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="25583-123">To associate Azure AD accounts with POS users in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="25583-124">Valige **jaemüük ja äri > Töötajad > Töötajad** ja avage töötajakirje.</span><span class="sxs-lookup"><span data-stu-id="25583-124">Go to **Retail and Commerce > Employees > Workers** and open a worker record.</span></span>
1. <span data-ttu-id="25583-125">Valige tegumiriba vahekaardil **Kaubandus** grupis **Välisidentiteet**, valige **Olemasoleva identiteedi seostamine**.</span><span class="sxs-lookup"><span data-stu-id="25583-125">On the Action Pane, select the **Commerce** tab, then under **External identity** select **Associate existing identity**.</span></span> 
1. <span data-ttu-id="25583-126">Dialoogiaknas **Kasuta olemasolevat välisidentiteeti** valige **Otsi kasutades e-posti**, sisestage Azure AD e-posti aadress ja seejärel valige **Otsing**.</span><span class="sxs-lookup"><span data-stu-id="25583-126">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="25583-127">Valige saadud konto Azure AD ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="25583-127">Select the Azure AD account that is returned, then select **OK**.</span></span>

<span data-ttu-id="25583-128">Pärast ülaltoodud konfiguratsioonisamme täidetakse väljad **Alias**, **UPN** ja **Väline alamidentifikaator** töötaja üksikasjade lehe vahekaardil **Kaubandus**.</span><span class="sxs-lookup"><span data-stu-id="25583-128">After the configuration steps above, the **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

<span data-ttu-id="25583-129">Peate käitama **1060 (Personal)** töö käskudes **Retail ja Commerce > Retail ja Commerce IT > Distribution Schedule** viimase kassa kasutaja ja Azure AD konto andmete kanalisse sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="25583-129">You must run the **1060 (Staff)** job in **Retail and Commerce > Retail and Commerce IT > Distribution schedule** to synchronize the latest POS user and Azure AD account data to the channel.</span></span>

> [!NOTE]
> <span data-ttu-id="25583-130">Hea tava on pärast töötajateabe, nt parooli, kassa loa, seotud konto või töötaja aadressiraamatu värskendamist Commerce Headquartersis käitada Azure AD **1060 (Personal) töö, et sünkroonida värskeim töötaja teave** kanalisse.</span><span class="sxs-lookup"><span data-stu-id="25583-130">As a best practice, after worker information such as password, POS permission, associated Azure AD account, or employee address book is updated in Commerce headquarters, it is highly recommended to run the **1060 (Staff)** job to synchronize the latest worker information to the channel.</span></span> <span data-ttu-id="25583-131">Kassarakendus saab siis tuua õigeid andmeid kasutaja autentimiseks ja autoriseerimise kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="25583-131">The POS client can then fetch the correct data for user authentication and authorization checks.</span></span>

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a><span data-ttu-id="25583-132">Kassaluku register ja autentimine välja Azure AD logimine</span><span class="sxs-lookup"><span data-stu-id="25583-132">POS lock register and sign-out with Azure AD authentication</span></span>

<span data-ttu-id="25583-133">Kui kassa on konfigureeritud autentimismeetodit kasutama, Azure AD ilmneb järgmine:</span><span class="sxs-lookup"><span data-stu-id="25583-133">The following occurs when POS is configured to use the Azure AD authentication method:</span></span>

- <span data-ttu-id="25583-134">**Lukustamisregistri funktsioon ei ole kassa rakenduses** saadaval.</span><span class="sxs-lookup"><span data-stu-id="25583-134">The **Lock register** function will not be available in the POS application.</span></span> 
- <span data-ttu-id="25583-135">Funktsioon **Lukusta** automaatselt täidetakse sama funktsiooniga **Automaatne väljalogimine**.</span><span class="sxs-lookup"><span data-stu-id="25583-135">The **Automatically lock** function will behave the same as the **Automatically logoff** function.</span></span>
- <span data-ttu-id="25583-136">Kui müügikoha kasutaja valib **väljalogimise**, palutakse kasutajal järgmisel müügikoha käivitamisel  Azure AD mandaatidega sisse logida, olenemata sellest, kas üks sisselogimine on lubatud.</span><span class="sxs-lookup"><span data-stu-id="25583-136">If the POS user selects **Log off**, the user will be asked to sign in with Azure AD credentials the next time the POS launches, regardless of whether single sign-in is enabled.</span></span>

## <a name="manager-override-functionality-with-azure-ad-authentication"></a><span data-ttu-id="25583-137">Juhi alistamisfunktsioon Azure AD autentimisega</span><span class="sxs-lookup"><span data-stu-id="25583-137">Manager override functionality with Azure AD authentication</span></span>

<span data-ttu-id="25583-138">Kui müügikoht on autentimise kasutamiseks konfigureeritud, avab halduri alistamisfunktsioon dialoogiboksi, kus küsitakse halduri Azure AD kasutaja Azure AD mandaate.</span><span class="sxs-lookup"><span data-stu-id="25583-138">When the POS is configured to use Azure AD authentication, the manager override functionality will open a dialog box that prompts for the manager user's Azure AD credentials.</span></span> <span data-ttu-id="25583-139">Kui juhatajana sisselogimine on kinnitatud, loobutakse juhataja Azure AD mandaatidest ja eelmise kasutaja Azure AD mandaate kasutatakse järgmisteks kassatoiminguteks.</span><span class="sxs-lookup"><span data-stu-id="25583-139">After manager sign-in is approved, the manager's Azure AD credentials will be dropped and the previous user's Azure AD credentials will be used for subsequent POS operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="25583-140">Commerce'i versioonides 10.0.18 ja varasemas pole halduri alistamisfunktsioon Azure AD toetatud.</span><span class="sxs-lookup"><span data-stu-id="25583-140">In Commerce versions 10.0.18 and earlier, the manager override function does not support Azure AD.</span></span> <span data-ttu-id="25583-141">Personali ID-d ja parooli nõutakse ka siis, kui kassa on konfigureeritud kasutama Azure AD autentimismeetodina.</span><span class="sxs-lookup"><span data-stu-id="25583-141">A personnel ID and password are required even if the POS is configured to use the Azure AD authentication method.</span></span>
> - <span data-ttu-id="25583-142">Kui kasutate CPOS-i Microsofti veebibrauserigaUdu iOS-seadmes, peate **blokeerimise hüpikmenüüd** Azure AD autentimisfunktsiooni funktsionaalsuse halduri sätetes välja lülitama.</span><span class="sxs-lookup"><span data-stu-id="25583-142">When using CPOS with the Safari web browser on an Apple iOS device, you must first turn off **Block Pop-ups** in Safari settings for the manager override functionality to work with Azure AD authentication.</span></span> 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a><span data-ttu-id="25583-143">Ühiskasutusega seadmete Azure AD kassapõhise autentimise turbe head tavad</span><span class="sxs-lookup"><span data-stu-id="25583-143">Security best practices for Azure AD-based POS authentication on shared devices</span></span>

<span data-ttu-id="25583-144">Paljud jaemüüjad seadistavad oma kaupluse keskkonna viisil, et mitu kasutajat peavad kassa rakendusele juurde pääsema ühiskasutusega füüsilisest seadmest.</span><span class="sxs-lookup"><span data-stu-id="25583-144">Many retailers set up their retail store environment in a way that multiple users need to access the POS application from a shared physical device.</span></span> <span data-ttu-id="25583-145">Selles kontekstis võib see, kui üks sisselogimine pakub mugavat ja sujuvat autentimise kogemust, luua ka turbekontsessi, kus praegune kassa kasutaja ei pruugi realiseerida, et kassas kannete või toimingute tegemiseks kasutatakse teise kasutaja mandaate.</span><span class="sxs-lookup"><span data-stu-id="25583-145">In that context, while single sign-in provides a convenient and seamless authentication experience, it may also create a security loophole where the current POS user may not realize that another user's credentials are being used to perform transactions or operations in the POS.</span></span> <span data-ttu-id="25583-146">Enne kassa konfigureerimist autentimismeetodi kasutamiseks on soovitatav oma turvapoliitika ja jagatud seadme sisselogimissätted üle vaadata, et otsustada, milline valik Azure AD on parim.</span><span class="sxs-lookup"><span data-stu-id="25583-146">Before you configure the POS to use the Azure AD authentication method, it is highly recommended to review your security policy and the shared device's sign-in settings to decide which option is the best fit.</span></span>

- <span data-ttu-id="25583-147">Kui teie jaemüügikeskkond kasutab füüsilise seadmega sisselogimiseks ühiskasutatavaid kontosid (nt kohalikku kontot), on soovitatav kasutada valikut ilma ühekordse **Azure AD** sisselogimiseta.</span><span class="sxs-lookup"><span data-stu-id="25583-147">If your retail environment uses a shared account (for example, a local account) for physical device sign-in, it's recommended to use the **Azure AD without single sign-on** option.</span></span> <span data-ttu-id="25583-148">See tagab, et iga kassa kasutaja annab eraldi Azure AD mandaadid kassasse sisselogimiseks.</span><span class="sxs-lookup"><span data-stu-id="25583-148">This ensures that each POS user explicitly provides Azure AD credentials to sign in to the POS.</span></span>
- <span data-ttu-id="25583-149">Kui teie jaemüügikeskkond nõuab töötajatelt oma Azure AD kontode kasutamist, et kassasse sisse logida ja see majutab füüsilist seadet, on soovitatav kasutada **Azure AD ühekordse sisselogimisega** suvandit.</span><span class="sxs-lookup"><span data-stu-id="25583-149">If your retail environment requires employees to use their own Azure AD accounts to sign in to the POS and its hosting physical device, it's recommended to use the **Azure AD with single sign-on** option.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25583-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="25583-150">Additional resources</span></span>

[<span data-ttu-id="25583-151"> Töötaja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="25583-151">Configure a worker</span></span>](tasks/worker.md)

[<span data-ttu-id="25583-152">Jaemüügi funktsiooniprofiili loomine</span><span class="sxs-lookup"><span data-stu-id="25583-152">Create a retail functionality profile</span></span>](retail-functionality-profile.md)


[<span data-ttu-id="25583-153">MPOS-i ja pilve kassa laiendatud sisselogimisfunktsiooni häälestus</span><span class="sxs-lookup"><span data-stu-id="25583-153">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="25583-154">Pilve kassa turbe head tavad ühiskasutusega keskkondades</span><span class="sxs-lookup"><span data-stu-id="25583-154">Security best practices for Cloud POS in shared environments</span></span>](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
