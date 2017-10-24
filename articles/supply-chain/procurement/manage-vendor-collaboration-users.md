---
title: "Hankija koostöö kasutajate haldamine"
description: "See teema kirjeldab, kuidas saate taotleda uue hankija koostöö kasutajate ettevalmistamist ja kuidas lisada uue hankija koostöö kontakte."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7dd5a1d9da4b648f07e87ad7921ac10ea92bb460
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="manage-vendor-collaboration-users"></a><span data-ttu-id="1a713-103">Hankija koostöö kasutajate haldamine</span><span class="sxs-lookup"><span data-stu-id="1a713-103">Manage vendor collaboration users</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1a713-104">See teema kirjeldab, kuidas saate taotleda uue hankija koostöö kasutajate ettevalmistamist ja kuidas lisada uue hankija koostöö kontakte.</span><span class="sxs-lookup"><span data-stu-id="1a713-104">This topic describes how you can request the provisioning of new vendor collaboration users, and how to add new vendor collaboration contacts.</span></span> 

<span data-ttu-id="1a713-105">Hankija koostöö liides rakenduses Microsoft Dynamics 365 for Finance and Operations paljastab teavet ostutellimuste, arvete ja veosevarude kohta välistele hankijatele.</span><span class="sxs-lookup"><span data-stu-id="1a713-105">The vendor collaboration interface in Microsoft Dynamics 365 for Finance and Operations exposes information about purchase orders, invoices, and consignment stock to external vendors.</span></span> <span data-ttu-id="1a713-106">Saate luua uued hankija koostöö kontaktid ja nõuda, et uued kasutajad valmistatakse ette, kui töötate välise hankijana turberolliga **Hankija administraator (väline)** või sarnaste lubadega.</span><span class="sxs-lookup"><span data-stu-id="1a713-106">You can create new vendor collaboration contacts and request that new users are provisioned if you're working as an external vendor with the **Vendor admin (external)** security role, or similar permissions.</span></span> <span data-ttu-id="1a713-107">Samuti saate teha need ülesanded, kui töötate hankeprofessionaalina.</span><span class="sxs-lookup"><span data-stu-id="1a713-107">You can also perform these tasks if you're working as a procurement professional.</span></span> <span data-ttu-id="1a713-108">Selles teemas viitab see roll hankeprofessionaalile, kes töötab selle ettevõtte siseselt, millele kuulub rakenduse Dynamics 365 for Finance and Operations eksemplar.</span><span class="sxs-lookup"><span data-stu-id="1a713-108">In this topic, this role refers to a procurement professional who is working within the company that owns the instance of Finance and Operations.</span></span> <span data-ttu-id="1a713-109">Lisateavet selle kohta, kuidas kasutada hankija koostööd, kui olete väline hankija, vaadake jaotisest [Klientidega hankija](vendor-collaboration-work-customers-dynamics-365-operations.md).</span><span class="sxs-lookup"><span data-stu-id="1a713-109">For more information about how to use vendor collaboration if you're an external vendor, see [Vendor with customers](vendor-collaboration-work-customers-dynamics-365-operations.md).</span></span>  

<span data-ttu-id="1a713-110">Lisateavet selle kohta, kuidas kasutada hankija koostööd, kui olete väline hankija, vaadake jaotisest [Hankija koostöö väliste hankijatega](vendor-collaboration-work-external-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="1a713-110">For more information about how to use vendor collaboration if you're a procurement professional, see [Vendor collaboration to with external vendors](vendor-collaboration-work-external-vendors.md).</span></span>

## <a name="add-new-vendor-collaboration-contacts"></a><span data-ttu-id="1a713-111">Uue hankija koostöö kontaktide lisamine</span><span class="sxs-lookup"><span data-stu-id="1a713-111">Add new vendor collaboration contacts</span></span>
<span data-ttu-id="1a713-112">Kui soovite, et kellelgi oleks juurdepääs hankija koostööle, tuleb nad esmalt lisada hankija koostöö kontaktina.</span><span class="sxs-lookup"><span data-stu-id="1a713-112">If you want someone to have access to vendor collaboration they first have to be added as a vendor collaboration contact.</span></span> <span data-ttu-id="1a713-113">Võite soovi korral lisada kontakte oma ettevõtte töötajatele, kes ei kasuta hankija koostööd.</span><span class="sxs-lookup"><span data-stu-id="1a713-113">You may also want to add contacts for employees in your company who won't use vendor collaboration.</span></span> <span data-ttu-id="1a713-114">Näiteks võivad nad olla kontaktpunktiks teist tüüpi hanketeabele.</span><span class="sxs-lookup"><span data-stu-id="1a713-114">For example, they could be the point of contact for other kinds of procurement information.</span></span> <span data-ttu-id="1a713-115">Uued kontaktid lisatakse lehel **Kõik kontaktid** millele on juurdepääs menüüst **Hankija koostöö** &gt; **Kontaktid**.</span><span class="sxs-lookup"><span data-stu-id="1a713-115">New contacts are added on the **All contacts** page, which is accessed from the **Vendor collaboration** &gt; **Contacts** menu.</span></span> <span data-ttu-id="1a713-116">Uue kontakti lisamiseks:</span><span class="sxs-lookup"><span data-stu-id="1a713-116">To add a new contact:</span></span>

1.  <span data-ttu-id="1a713-117">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1a713-117">Click **New.**</span></span>
2.  <span data-ttu-id="1a713-118">Sisestage kontaktisiku üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="1a713-118">Enter the contact person details.</span></span>
3.  <span data-ttu-id="1a713-119">Valige, millist juriidilist isikut nad teie ettevõttes tähistavad ja millise juriidilise isikuga nad töötavad ettevõttes, millega nad koostööd teevad.</span><span class="sxs-lookup"><span data-stu-id="1a713-119">Choose which legal entity they're representing in your company, and which legal entity they'll work with in the company that they'll collaborate with.</span></span> <span data-ttu-id="1a713-120">Selleks valite paari **Juriidiline isik minu ettevõttes**/**Juriidiline isik kliendi ettevõttes**.</span><span class="sxs-lookup"><span data-stu-id="1a713-120">You do this by selecting a **Legal entity in my company**/**Legal entity in customer company** pair.</span></span>
4.  <span data-ttu-id="1a713-121">Klõpsake valikut **Loo**.</span><span class="sxs-lookup"><span data-stu-id="1a713-121">Click **Create.**</span></span>

<span data-ttu-id="1a713-122">Kui soovite kontakti kustutada, siis on võimalik kustutada ainult need, mille olete loonud.</span><span class="sxs-lookup"><span data-stu-id="1a713-122">If you want to delete a contact, it's only possible to delete the ones that you've created.</span></span>

## <a name="vendor-collaboration-user-requests"></a><span data-ttu-id="1a713-123">Hankija koostöö kasutajataotlused</span><span class="sxs-lookup"><span data-stu-id="1a713-123">Vendor collaboration user requests</span></span>
<span data-ttu-id="1a713-124">Hankija koostöö kasutajataotlused saab tõstada hankeprofessionaal või väline hankija administraator.</span><span class="sxs-lookup"><span data-stu-id="1a713-124">Vendor collaboration user requests can be raised by a procurement professional, or by an external vendor administrator.</span></span>

-   <span data-ttu-id="1a713-125">Kui olete väline hankija, edastate taotlusi lehelt **Kõik kontaktid** mooduli **Hankija koostöö** siseselt.</span><span class="sxs-lookup"><span data-stu-id="1a713-125">If you're an external vendor, you submit requests from the **All contacts** page within the **Vendor collaboration** module.</span></span>
-   <span data-ttu-id="1a713-126">Kui olete hankeprofessionaal, edastate taotlusi lehelt **Kuva kontaktid**.</span><span class="sxs-lookup"><span data-stu-id="1a713-126">If you're a procurement professional, you submit requests from the **View contacts** page.</span></span> <span data-ttu-id="1a713-127">Selleks tehke hankija kirjel tegumiriba jaotises **Seadistus** valikud **Kontaktid** &gt; **Kuva kontaktid**.</span><span class="sxs-lookup"><span data-stu-id="1a713-127">To do this, on the vendor record, in the **Setup** section in the Action pane, select **Contacts** &gt; **View contacts**.</span></span>

<span data-ttu-id="1a713-128">Saate teha taotluse kasutaja ettevalmistamiseks, kasutaja inaktiveerimiseks või turberollide modifitseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="1a713-128">You can make a request to provision a user, to inactivate a user, or to modify security roles.</span></span> <span data-ttu-id="1a713-129">Kui olete välise hankija administraator, peate olema registreeritud selliste hankijakontode kontaktisikuna, mille jaoks soovite kasutajataotlusi teha, ja teil peab olema juurdepääs hankija koostöö liidesele nende hankijakontode puhul.</span><span class="sxs-lookup"><span data-stu-id="1a713-129">If you're an external vendor administrator, you must be registered as a contact person for the vendor accounts that you want to make user requests for, and you must have access to the vendor collaboration interface for those vendor accounts.</span></span>  

<span data-ttu-id="1a713-130">Taotluse edastamisel lisatakse see mooduli **Hankija koostöö** loendisse **Hankija koostöö kasutajataotlused** ja mooduli **Hanked** loendisse **Hankija koostöö kasutajataotlus** (hangete moodul ei ole välistele kasutajatele juurdepääsetav).</span><span class="sxs-lookup"><span data-stu-id="1a713-130">When a request is submitted it is added to the **Vendor collaboration user requests** list in the **Vendor collaboration** module, and to the **Vendor collaboration user request** list in the **Procurement and sourcing** module (the Procurement and sourcing module is not accessible to external users).</span></span>

### <a name="provision-a-user"></a><span data-ttu-id="1a713-131">Kasutaja ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="1a713-131">Provision a user</span></span>

<span data-ttu-id="1a713-132">Enne kui saate taotleda uue kasutaja ettevalmistamist, tuleb see isik seadistada kontaktina ühe või mitme hankijakonto jaoks.</span><span class="sxs-lookup"><span data-stu-id="1a713-132">Before you can request that a new user is provisioned, that person must be set up as a contact for one or more vendor accounts.</span></span> <span data-ttu-id="1a713-133">Uue hankija koostöö kasutaja jaoks taotluse loomiseks:</span><span class="sxs-lookup"><span data-stu-id="1a713-133">To create a request for a new vendor collaboration user:</span></span>

1.  <span data-ttu-id="1a713-134">Lehel **Kõik kontaktid** klõpsake valikut **Valmista ette hankija-kasutaja**.</span><span class="sxs-lookup"><span data-stu-id="1a713-134">On the **All contacts** page, click **Provision vendor user**.</span></span>
2.  <span data-ttu-id="1a713-135">Sisestage kasutaja meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="1a713-135">Enter an email address for the user.</span></span> <span data-ttu-id="1a713-136">Seda aadressi kasutab kasutaja, et logida sisse rakendusse Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1a713-136">This address will be used by the user to log onto Finance and Operations.</span></span> <span data-ttu-id="1a713-137">Kui meiliaadress kuulub domeenile, mis on registreeritud Microsoft Azure'iga üürnikuna, siis peab meiliaadress olema olemasolev Azure Active Directory (ADD) konto, et ettevalmistamise protsessi saaks edukalt lõpuke viia.</span><span class="sxs-lookup"><span data-stu-id="1a713-137">If the email address belongs to a domain registered as a tenant with Microsoft Azure, then the email address has to be an existing Azure Active Directory (ADD) account in order for the provisioning process to complete successfully.</span></span> <span data-ttu-id="1a713-138">Kui meiliaadress ei kuulu Microsoft Azure'iga registreeritud domeenile, luuakse ADD konto osana ettevalmistamise protsessit ja uus kasutaja saab kutsemeili.</span><span class="sxs-lookup"><span data-stu-id="1a713-138">If the email address does not belong to a domain registered with Microsoft Azure, an ADD account will be created as part of the provisioning process and the new user will receive an invitation mail.</span></span> <span data-ttu-id="1a713-139">Laiatarbemeiliaadresse, mis on selliste domeenidega nagu @hotmail.com, @gmail.com või @comcast.net, ei saa kasutada rakenduse Dynamics 365 for Finance and Operations kasutaja registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="1a713-139">Consumer email addresses with domains such as @hotmail.com, @gmail.com, or @comcast.net cannot be used to register a Finance and Operations user.</span></span>
3.  <span data-ttu-id="1a713-140">Seadke suvand **Hankija koostöö juurdepääs on lubatud** valikule **Jah** kõikide juriidiliste isikute puhul, millele kasutaja vajab juurdepääsu.</span><span class="sxs-lookup"><span data-stu-id="1a713-140">Set the **Vendor collaboration access allowed** option to **Yes** for all the legal entities that the user needs access to.</span></span>
4.  <span data-ttu-id="1a713-141">Jaotises **Kasutaja rollide määramine** valige märkeruut **Määra** turberollidele, mis uuel kasutajal peaks olema.</span><span class="sxs-lookup"><span data-stu-id="1a713-141">In the **Assign user roles** section, select the **Assign** check box for the security roles that the new user should have.</span></span>
5.  <span data-ttu-id="1a713-142">Klõpsake **Edasta**.</span><span class="sxs-lookup"><span data-stu-id="1a713-142">Click **Submit**.</span></span>

<span data-ttu-id="1a713-143">Hankija-kasutaja taotluse edastamisel seatakse valitud hankija konto väli **Hankija koostöö juurdepääs on lubatud** olekusse **Jah** ja käivitatakse kasutajataotluse töövoog.</span><span class="sxs-lookup"><span data-stu-id="1a713-143">When the vendor user request is submitted, the **Vendor collaboration access allowed** field is set to **Yes** for the selected vendor account and a user request workflow is started.</span></span> <span data-ttu-id="1a713-144">Osana töövoost luuakse rakenduses Dynamics 365 for Finance and Operations uus kasutaja ja määratakse turberollid.</span><span class="sxs-lookup"><span data-stu-id="1a713-144">As part of the workflow, a new user is created in Finance and Operations, and security roles are assigned.</span></span> <span data-ttu-id="1a713-145">Lisaks aktiveeritakse Azure B2B teenus, mis käivitab suhtluse Azure'i portaaliga ja seostab uut või olemasolevat AAD kontot rakenduse Dynamics 365 for Finance and Operations kasutajakontoga.</span><span class="sxs-lookup"><span data-stu-id="1a713-145">In addition, an Azure B2B service is activated which initiates interaction with Azure portal and associates a new or existing AAD account with the Finance and Operations user account.</span></span>

### <a name="inactivate-a-user"></a><span data-ttu-id="1a713-146">Kasutaja inaktiveerimine</span><span class="sxs-lookup"><span data-stu-id="1a713-146">Inactivate a user</span></span>

<span data-ttu-id="1a713-147">On kaks viisi, kuidas eemaldada kasutaja juurdepääs hankija koostööle:</span><span class="sxs-lookup"><span data-stu-id="1a713-147">There are two ways to remove access to vendor collaboration for a user:</span></span>

-   <span data-ttu-id="1a713-148">Hankija lehel **Kontaktid** määrake suvandi **Hankija koostöö juurdepääs on lubatud** sätteks kontakti puhul **Ei**.</span><span class="sxs-lookup"><span data-stu-id="1a713-148">On the **Contacts** page for the vendor, set the **Vendor collaboration access allowed** option to **No** for the contact.</span></span> <span data-ttu-id="1a713-149">Seda saab teha individuaalselt juriidilise isiku järgi, millele isik kontakt on.</span><span class="sxs-lookup"><span data-stu-id="1a713-149">This can be done individually per legal entity that the person is a contact for.</span></span> <span data-ttu-id="1a713-150">Seda suvandit saavad kasutada ainult hankeprofessionaalid.</span><span class="sxs-lookup"><span data-stu-id="1a713-150">This option can only be used by procurement professionals.</span></span>
-   <span data-ttu-id="1a713-151">Inaktiveerige kogu kasutajakonto, edastades taotluse **Hankija-kasutaja inaktiveerimine**.</span><span class="sxs-lookup"><span data-stu-id="1a713-151">Inactivate the entire user account, by submitting an **Inactivate vendor user** request.</span></span>

<span data-ttu-id="1a713-152">Kasutaja inaktiveerimise taotlemiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="1a713-152">To request that a user is inactivated:</span></span>

1.  <span data-ttu-id="1a713-153">Klõpsake lehel **Kõik kontaktid** valikut **Inaktiveeri** **hankija-kasutaja**.</span><span class="sxs-lookup"><span data-stu-id="1a713-153">On the **All contacts** page, click **Inactivate** **vendor user**.</span></span>
2.  <span data-ttu-id="1a713-154">Kirjutage kommentaar väljale **Äripõhjendus**.</span><span class="sxs-lookup"><span data-stu-id="1a713-154">Write a comment in the **Business justification** field.</span></span>
3.  <span data-ttu-id="1a713-155">Klõpsake **Edasta**.</span><span class="sxs-lookup"><span data-stu-id="1a713-155">Click **Submit**.</span></span>

### <a name="modify-security-roles"></a><span data-ttu-id="1a713-156">Turberollide modifitseerimine</span><span class="sxs-lookup"><span data-stu-id="1a713-156">Modify security roles</span></span>

<span data-ttu-id="1a713-157">Leht **Säilita hankija-kasutaja rollid** on sama mis leht **Valmista ette hankija-kasutaja**, välja arvatud see, et turberollide loendit saab redigeerida.</span><span class="sxs-lookup"><span data-stu-id="1a713-157">The **Maintain vendor user roles** page is the same as the **Provision vendor user** page except that the list of security roles can be edited.</span></span>  

<span data-ttu-id="1a713-158">Kasutaja turberollide muutmise taotlemiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="1a713-158">To request that the security roles are modified for a user:</span></span>

1.  <span data-ttu-id="1a713-159">Klõpsake lehel **Kõik kontaktid** valikut **Halda** **hankija-kasutaja rolle**.</span><span class="sxs-lookup"><span data-stu-id="1a713-159">On the **All contacts** page, click **Maintain** **vendor user roles**.</span></span>
2.  <span data-ttu-id="1a713-160">Kirjutage kommentaar väljale **Äripõhjendus**.</span><span class="sxs-lookup"><span data-stu-id="1a713-160">Write a comment in the **Business justification** field.</span></span>
3.  <span data-ttu-id="1a713-161">Jaotises **Säilita kasutajarollid** valige turberollid, mida soovite määrata, või tühjendage need, mida soovite eemaldada.</span><span class="sxs-lookup"><span data-stu-id="1a713-161">In the **Maintain user roles** section, select the security roles that you want to assign, or clear the ones that you want to remove.</span></span>
4.  <span data-ttu-id="1a713-162">Klõpsake **Edasta**.</span><span class="sxs-lookup"><span data-stu-id="1a713-162">Click **Submit**.</span></span>





