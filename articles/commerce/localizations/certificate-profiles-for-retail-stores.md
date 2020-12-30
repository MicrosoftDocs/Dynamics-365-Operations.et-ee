---
title: Kasutaja määratletud serdiprofiilid jaekaupluste jaoks
description: Selles teemas antakse ülevaade selle kohta, kuidas serte kauplustes kasutatakse.
author: josaw
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 75edc1b683c4ea6c2bac8e509e6f6da8c56c5e6a
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665243"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a><span data-ttu-id="0dffc-103">Kasutaja määratletud serdiprofiilid jaekaupluste jaoks</span><span class="sxs-lookup"><span data-stu-id="0dffc-103">User-defined certificate profiles for retail stores</span></span>

[!include [banner](../includes/banner.md)]


## <a name="overview"></a><span data-ttu-id="0dffc-104">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="0dffc-104">Overview</span></span>

<span data-ttu-id="0dffc-105">Selles teemas antakse ülevaade rakenduses Microsoft Dynamics 365 Commerce saadaolevatest serdiprofiilidest.</span><span class="sxs-lookup"><span data-stu-id="0dffc-105">This topic provides an overview of the certificate profiles that are available in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="0dffc-106">See funktsioon laiendab funktsiooni [Jaemüügikanalite saladuste haldamine](../dev-itpro/manage-secrets.md), lisades kohalike sertide toe.</span><span class="sxs-lookup"><span data-stu-id="0dffc-106">This functionality extends the [Manage secrets for retail channels](../dev-itpro/manage-secrets.md) feature by adding support for local certificates.</span></span>

<span data-ttu-id="0dffc-107">Kui kassa (POS) töötab ühenduseta režiimis, ei pääse see juurde võtmehoidlas talletatud sertidele.</span><span class="sxs-lookup"><span data-stu-id="0dffc-107">While the point of sale (POS) is running in offline mode, it can't access the certificates that are stored in the key vault.</span></span> <span data-ttu-id="0dffc-108">Selle asemel tuleks kasutada kohalikku serti.</span><span class="sxs-lookup"><span data-stu-id="0dffc-108">The local certificate should be used instead.</span></span> <span data-ttu-id="0dffc-109">Toetatud on järgmised võimalused.</span><span class="sxs-lookup"><span data-stu-id="0dffc-109">The following capabilities are supported:</span></span>

- <span data-ttu-id="0dffc-110">Kohalike sertide kasutamine võtmehoidla taandeolekusse laskumise korral</span><span class="sxs-lookup"><span data-stu-id="0dffc-110">Using local certificates in key vault fallback scenarios</span></span>
- <span data-ttu-id="0dffc-111">Kohalike sertide kasutamine võtmehoidlata (nt kohapealse installimise korral)</span><span class="sxs-lookup"><span data-stu-id="0dffc-111">Using local certificates without a key vault (for example in an on-premises installation)</span></span>
- <span data-ttu-id="0dffc-112">Sertide järkjärguline uuendamine, mille korral kasutab mõni kauplus ja terminal serdi uut versiooni, kuid teised kauplused ja terminalid jätkavad eelmise versiooni kasutamist</span><span class="sxs-lookup"><span data-stu-id="0dffc-112">Gradual update of certificates, where some stores and terminals use a new version of the certificate, but other stores and terminals continue to use the previous version</span></span>

<span data-ttu-id="0dffc-113">Serdiprofiilide funktsioon võimaldab määrata vaikeserdi ja seadistada järjekorra, mille alusel serte samas serdiprofiilis otsitakse.</span><span class="sxs-lookup"><span data-stu-id="0dffc-113">The certificate profiles functionality lets you specify a default certificate and set the order that certificates in the same certificate profile are searched in.</span></span> <span data-ttu-id="0dffc-114">See funktsioon pakub ka sarnaseid seadistusvõimalusi kohalike sertide ja võtmehoidla sertide puhul.</span><span class="sxs-lookup"><span data-stu-id="0dffc-114">This functionality also provides a similar setup approach for local certificates and Key Vault certificates.</span></span> <span data-ttu-id="0dffc-115">Saate seadistada serte ettevõttepõhiselt, kuid iga serdi kordumatut ettevõtteülest identifikaatorit on võimalik kasutada Commerce'i kanalites.</span><span class="sxs-lookup"><span data-stu-id="0dffc-115">You can add company-specific settings for certificates, but the unique cross-company identifier for each certificate can be used in the Commerce channels.</span></span>

### <a name="scenarios"></a><span data-ttu-id="0dffc-116">Stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="0dffc-116">Scenarios</span></span>

<span data-ttu-id="0dffc-117">Serdiprofiilide funktsioon toetab Commerce'i kanalites järgmisi stsenaariume.</span><span class="sxs-lookup"><span data-stu-id="0dffc-117">The certificate profiles functionality supports the following scenarios in the Commerce channels:</span></span>

- <span data-ttu-id="0dffc-118">Kohaliku serdi kasutamine võtmehoidla taandeolekusse laskumise korral.</span><span class="sxs-lookup"><span data-stu-id="0dffc-118">Use a local certificate in key vault fallback scenarios.</span></span> <span data-ttu-id="0dffc-119">Siin on mõned näited taandeolekusse laskumisest.</span><span class="sxs-lookup"><span data-stu-id="0dffc-119">Here are some examples of these fallback scenarios:</span></span>

    - <span data-ttu-id="0dffc-120">Võtmehoidla salvestusruum ei ole juurdepääsetav.</span><span class="sxs-lookup"><span data-stu-id="0dffc-120">The key vault storage isn't accessible.</span></span>
    - <span data-ttu-id="0dffc-121">Serti ei leitud võtmehoidlast.</span><span class="sxs-lookup"><span data-stu-id="0dffc-121">A certificate isn't found in the key vault storage.</span></span>
    - <span data-ttu-id="0dffc-122">Kassa töötab ühenduseta režiimis.</span><span class="sxs-lookup"><span data-stu-id="0dffc-122">The POS is running in offline mode.</span></span>

- <span data-ttu-id="0dffc-123">Kohalike sertide kasutamine, ilma et neid võtmehoidlas talletataks (nt kohapealse installimise korral).</span><span class="sxs-lookup"><span data-stu-id="0dffc-123">Use local certificates, but without storing them in the key vault (for example, in an on-premises installation).</span></span>
- <span data-ttu-id="0dffc-124">Sertide järkjärguline värskendamine, mille korral kasutatakse serdi uut versiooni ainult kauplustes ja terminalides, kus uus versioon on juba saadaval.</span><span class="sxs-lookup"><span data-stu-id="0dffc-124">Do a gradual update of certificates, where a new version of the certificate is used only in stores or on terminals where the new version is already available.</span></span>
- <span data-ttu-id="0dffc-125">Sama serdi kasutamine mitmes ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="0dffc-125">Use the same certificate in several companies.</span></span>

## <a name="set-up-certificate-profiles"></a><span data-ttu-id="0dffc-126">Serdiprofiilide seadistamine</span><span class="sxs-lookup"><span data-stu-id="0dffc-126">Set up certificate profiles</span></span>

<span data-ttu-id="0dffc-127">Järgmisena selgitatakse, kuidas seadistada serdiprofiile.</span><span class="sxs-lookup"><span data-stu-id="0dffc-127">The following procedure explains how to set up certificate profiles.</span></span> <span data-ttu-id="0dffc-128">Enne kui kasutate Commerce'i kanalites serdiprofiile, järgige sätete konfigureerimiseks järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="0dffc-128">Before you use certificate profiles in the Commerce channels, follow these steps to configure the settings.</span></span>

1. <span data-ttu-id="0dffc-129">Lülitage tööruumis **Funktsioonihaldus** sisse funktsioon **Kasutaja määratletud serdiprofiilid jaekaupluste jaoks**.</span><span class="sxs-lookup"><span data-stu-id="0dffc-129">In the **Feature management** workspace, turn on the **User-defined certificate profiles for retail stores** feature.</span></span>
2. <span data-ttu-id="0dffc-130">Avage **Süsteemihaldus \> Seadistus \> Serdiprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="0dffc-130">Go to **System administration \> Setup \> Certificate profiles**.</span></span>
3. <span data-ttu-id="0dffc-131">Looge kirje ja määratlege selle jaoks väljad **Serdiprofiil**, **Nimi** ja **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="0dffc-131">Create a record, and set the **Certificate profile**, **Name**, and **Description** fields for it.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0dffc-132">Serdiprofiil on serdi kordumatu identifikaator kõikides ettevõtetes ja Commerce'i komponentides.</span><span class="sxs-lookup"><span data-stu-id="0dffc-132">The certificate profile is a unique identifier of a certificate across all companies and Commerce components.</span></span>

3. <span data-ttu-id="0dffc-133">Lisage rida vahekaardil **Juriidilised isikud** ja valige juriidiline isik (ettevõte), mille jaoks praegust serdiprofiili tuleks kasutada.</span><span class="sxs-lookup"><span data-stu-id="0dffc-133">On the **Legal entities** tab, add a line, and select the legal entity (company) that the current certificate profile should be used for.</span></span> <span data-ttu-id="0dffc-134">Kui serdiprofiili tuleks kasutada mitme juriidilise isiku puhul, korrake seda sammu iga täiendava juriidilise isiku jaoks rea lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="0dffc-134">If the certificate profile should be used for multiple legal entities, repeat this step to add a line for each additional legal entity.</span></span>
4. <span data-ttu-id="0dffc-135">Valige **Sätted**, et avada leht **Serdiprofiili sätted**, kus saate sisestada serdiprofiilile ettevõttespetsiifilisi sätteid.</span><span class="sxs-lookup"><span data-stu-id="0dffc-135">Select **Settings** to open the **Certificate profile settings** page, where you can enter company-specific settings for the certificate profile.</span></span>

### <a name="certificate-profile-settings"></a><span data-ttu-id="0dffc-136">Serdiprofiili sätted</span><span class="sxs-lookup"><span data-stu-id="0dffc-136">Certificate profile settings</span></span>

<span data-ttu-id="0dffc-137">Kui valite serdiprofiili ridade puhul suvandi **Sätted**, avaneb leht **Serdiprofiili sätted**.</span><span class="sxs-lookup"><span data-stu-id="0dffc-137">When you select **Settings** for certificate profile lines, the **Certificate profile settings** page appears.</span></span> <span data-ttu-id="0dffc-138">See leht võimaldab teil määrata, milliseid serte saab kasutada, kui praegust serdiprofiili Commerce'i kanalites kutsutakse.</span><span class="sxs-lookup"><span data-stu-id="0dffc-138">This page lets you specify which certificates can be used when the current certificate profile is called in the Commerce channels.</span></span> <span data-ttu-id="0dffc-139">Samuti saate määrata, millises järjekorras tuleks serte otsida.</span><span class="sxs-lookup"><span data-stu-id="0dffc-139">You can also specify the order that certificates should be searched in.</span></span>

> [!NOTE]
> <span data-ttu-id="0dffc-140">Väli **Prioriteet** seatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="0dffc-140">The **Priority** field is automatically set.</span></span> <span data-ttu-id="0dffc-141">Väärtus **1** tähistab kõrgeimat prioriteeti.</span><span class="sxs-lookup"><span data-stu-id="0dffc-141">A value of **1** represents the highest priority.</span></span> <span data-ttu-id="0dffc-142">Kui lehel **Serdiprofiili sätted** lisatakse uus rida, seatakse selle prioriteediks arv, mis on eelmise rea prioriteedist ühe võrra suurem.</span><span class="sxs-lookup"><span data-stu-id="0dffc-142">When a new line is added on the **Certificate profile settings** page, its priority is set to a number that is one more than the priority of the previous line.</span></span> <span data-ttu-id="0dffc-143">Konkreetse rea prioriteedi muutmiseks valige rida ja seejärel valige prioriteedi tõstmiseks **Nihuta üles** või prioriteedi langetamiseks **Nihuta alla**.</span><span class="sxs-lookup"><span data-stu-id="0dffc-143">To change the priority of a specific line, select the line, and then select either **Move up** to increase the priority or **Move down** to decrease the priority.</span></span>

<span data-ttu-id="0dffc-144">Uue rea lisamisel lehel **Serdiprofiili sätted** seadke järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="0dffc-144">When you add a new line to the **Certificate profile settings** page, set the following fields:</span></span>

- <span data-ttu-id="0dffc-145">**Asukoha tüüp** – valige asukoht, kus sert on talletatud.</span><span class="sxs-lookup"><span data-stu-id="0dffc-145">**Location type** – Select the location where the certificate is stored.</span></span> <span data-ttu-id="0dffc-146">Sellel väljal on kaks võimalikku väärtust: **kohalik sert** ja **võtmehoidla**.</span><span class="sxs-lookup"><span data-stu-id="0dffc-146">This field has two possible values: **Local certificate** and **Key Vault**.</span></span>
- <span data-ttu-id="0dffc-147">**Võtmehoidla sert** – see väli on kohustuslik, kui seate välja **Asukoha tüüp** väärtuseks **Võtmehoidla**.</span><span class="sxs-lookup"><span data-stu-id="0dffc-147">**Key Vault certificate** – This field is required if you set the **Location type** field to **Key Vault**.</span></span> <span data-ttu-id="0dffc-148">Kasutage seda võtmehoidla serdi saladuse määramiseks.</span><span class="sxs-lookup"><span data-stu-id="0dffc-148">Use it to specify a Key Vault certificate secret.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0dffc-149">Enne võtmehoidla serdi kasutamist serdiprofiilides laadige sert üles võtmehoidla salvestusruumi ja järgige juhiseid, mis on toodud teemas [Azure'i võtmehoidla klientrakenduse seadistamine](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client).</span><span class="sxs-lookup"><span data-stu-id="0dffc-149">Before you use a Key Vault certificate in certificate profiles, be sure to upload a certificate to the key vault storage, and follow the instructions in [Set up the Azure Key Vault client](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client).</span></span>

- <span data-ttu-id="0dffc-150">**Kaupluse nimi** – see väli on valikuline ja on saadaval ainult siis, kui seate välja **Asukoha tüüp** väärtuseks **Kohalik sert**.</span><span class="sxs-lookup"><span data-stu-id="0dffc-150">**Store name** – This field is optional and is available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="0dffc-151">Kasutage seda kaupluse vaikenime määramiseks, mida tuleks kasutada kohalike sertide otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="0dffc-151">Use it to specify a default store name that should be used to search local certificates.</span></span>
- <span data-ttu-id="0dffc-152">**Kaupluse asukoht** – see väli on valikuline ja on saadaval ainult siis, kui seate välja **Asukoha tüüp** väärtuseks **Kohalik sert**.</span><span class="sxs-lookup"><span data-stu-id="0dffc-152">**Store location** – This field is optional and is available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="0dffc-153">Kasutage seda kaupluse vaikeasukoha määramiseks, mida tuleks kasutada kohalike sertide otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="0dffc-153">Use it to specify a default store location that should be used to search local certificates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0dffc-154">Kaupluse vaikenimi ja -asukoht lisatakse, et lihtsustada kohalike sertide otsimist lahenduses Commerce Runtime.</span><span class="sxs-lookup"><span data-stu-id="0dffc-154">The default store name and store location are added to simplify the process of searching local certificates in the Commerce runtime.</span></span> <span data-ttu-id="0dffc-155">X509StoreProvideril on loend kaustadest, kus serte talletatakse.</span><span class="sxs-lookup"><span data-stu-id="0dffc-155">X509StoreProvider has a list of folders where certificates are stored.</span></span> <span data-ttu-id="0dffc-156">Kui kaupluse vaikenimi ja -asukoht on määramata, üritab X509StoreProvider leida serti oma loendi teistest kaustadest.</span><span class="sxs-lookup"><span data-stu-id="0dffc-156">If the default store name and the default store location aren't specified, X509StoreProvider tries to find a certificate in the other folders on its list.</span></span>

- <span data-ttu-id="0dffc-157">**Sõrmejälg** – see väli on kohustuslik ja saadaval ainult siis, kui seate välja **Asukoha tüüp** väärtuseks **Kohalik sert**.</span><span class="sxs-lookup"><span data-stu-id="0dffc-157">**Thumbprint** – This field is required and available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="0dffc-158">Kasutage seda serdi sõrmejälje määramiseks.</span><span class="sxs-lookup"><span data-stu-id="0dffc-158">Use it to specify the certificate thumbprint.</span></span>
- <span data-ttu-id="0dffc-159">**Kommentaarid** – see väli on valikuline ja võimaldab kasutajatel sisestada märkmeid.</span><span class="sxs-lookup"><span data-stu-id="0dffc-159">**Comments** – This field is optional and lets users enter notes.</span></span>

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a><span data-ttu-id="0dffc-160">Töövoog: sertide otsimine lahenduses Commerce Runtime</span><span class="sxs-lookup"><span data-stu-id="0dffc-160">Workflow: Searching certificates in the Commerce runtime</span></span>

<span data-ttu-id="0dffc-161">Siin on põhiline töövoog, mida kasutatakse serdi otsimiseks serdiprofiili kutsumise korral Commerce Runtime'is.</span><span class="sxs-lookup"><span data-stu-id="0dffc-161">Here is the basic workflow that is used to search for a certificate when a certificate profile is called in the Commerce runtime.</span></span>

1. <span data-ttu-id="0dffc-162">Süsteem tuvastab, kas serdiprofiilil on praeguse juriidilise isiku jaoks ettevõttespetsiifilisi sätteid.</span><span class="sxs-lookup"><span data-stu-id="0dffc-162">The system identifies whether the certificate profile has company-specific settings for the current legal entity.</span></span>
1. <span data-ttu-id="0dffc-163">Süsteem püüab leida serti, kasutades lehel **Serdiprofiili sätted** toodud sellise rea väärtusi, mille väli **Prioriteet** väärtuseks on seatud **1**.</span><span class="sxs-lookup"><span data-stu-id="0dffc-163">The system tries to find the certificate by using the values on the **Certificate profile settings** page for the line where the **Priority** field is set to **1**.</span></span>

    - <span data-ttu-id="0dffc-164">Kui välja **Asukoha tüüp** väärtuseks on seatud **Võtmehoidla**, kasutatakse välja **Võtmehoidla serdi saladus** väärtust, et otsida serti lehel **Võtmehoidla parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="0dffc-164">If the **Location type** field is set to **Key Vault**, the value of the **Key Vault certificate secret** field is used to search for the certificate on the **Key vault parameters** page.</span></span> <span data-ttu-id="0dffc-165">Seejärel otsitakse serti võtmehoidla salvestusruumist.</span><span class="sxs-lookup"><span data-stu-id="0dffc-165">The certificate is then searched for in the key vault storage.</span></span>
    - <span data-ttu-id="0dffc-166">Kui välja **Asukoha tüüp** väärtuseks on seatud **Kohalik sert**, otsib X509StoreProvider esiteks serti kaupluse vaikenime ja -asukoha põhjal, kui need parameetrid on määratud.</span><span class="sxs-lookup"><span data-stu-id="0dffc-166">If the **Location type** field is set to **Local certificate**, X509StoreProvider first searches for the certificate by using the default store name and store location, if these parameters are specified.</span></span> <span data-ttu-id="0dffc-167">Seejärel otsib see oma kaustaloendi kõigist muudest kaustadest.</span><span class="sxs-lookup"><span data-stu-id="0dffc-167">It then searches in all other folders on its list of folders.</span></span>

1. <span data-ttu-id="0dffc-168">Kui serti ei leita, korratakse protsessi rea puhul, mille välja **Prioriteet** väärtuseks on seatud **2** jne.</span><span class="sxs-lookup"><span data-stu-id="0dffc-168">If the certificate isn't found, the process is repeated for the line where the **Priority** field is set to **2**, and so on.</span></span>

> [!NOTE]
> <span data-ttu-id="0dffc-169">Kui serdiprofiilil pole praeguse juriidilise isiku jaoks ühtki sätet või kui serdiotsing ebaõnnestub kõikide lehel **Serdiprofiili sätted** toodud ridade puhul, jääb sert leidmata.</span><span class="sxs-lookup"><span data-stu-id="0dffc-169">If the certificate profile has no settings for the current legal entity, or if the certificate search is unsuccessful for all lines on the **Certificate profile settings** page, the certificate isn't found.</span></span>

#### <a name="caching-the-results-of-certificate-searches"></a><span data-ttu-id="0dffc-170">Serdiotsingute tulemuste salvestamine vahemällu</span><span class="sxs-lookup"><span data-stu-id="0dffc-170">Caching the results of certificate searches</span></span>

<span data-ttu-id="0dffc-171">Serdiotsingute tulemused salvestatakse vahemällu.</span><span class="sxs-lookup"><span data-stu-id="0dffc-171">The results of certificate searches are cached.</span></span> <span data-ttu-id="0dffc-172">Vahemälu vaikeaegumisaeg on üks tund.</span><span class="sxs-lookup"><span data-stu-id="0dffc-172">The default expiration time for a cache is one hour.</span></span> <span data-ttu-id="0dffc-173">Seda aega saab aga kohandada ja selle väärtuseks saab seadistada maksimaalselt 24 tundi.</span><span class="sxs-lookup"><span data-stu-id="0dffc-173">However, this time can be customized and can be set to a maximum value of 24 hours.</span></span>

### <a name="gradual-update"></a><span data-ttu-id="0dffc-174">Järkjärguline värskendamine</span><span class="sxs-lookup"><span data-stu-id="0dffc-174">Gradual update</span></span>

<span data-ttu-id="0dffc-175">Kui kasutusele võetakse serdi uus versioon, kuid seda ei saa värskendada samal ajal kõikides kauplustes, võimaldab serdiprofiilide funktsioon serti järk-järgult värskendada.</span><span class="sxs-lookup"><span data-stu-id="0dffc-175">If a new version of the certificate is introduced, but it can't be updated in all stores at the same time, the certificate profiles functionality enables the certificate to be updated gradually.</span></span>

1. <span data-ttu-id="0dffc-176">Leidke serdiprofiil ja rida, mida tuleks värskendada, ning seejärel valige **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="0dffc-176">Find a certificate profile and the line that should be updated, and then select **Settings**.</span></span>
1. <span data-ttu-id="0dffc-177">Lisage rida ja määrake sätted, mis on seotud serdi uusima versiooniga.</span><span class="sxs-lookup"><span data-stu-id="0dffc-177">Add a line, and specify settings that are related to the latest version of the certificate.</span></span>
1. <span data-ttu-id="0dffc-178">Suurendage uue rea välja **Prioriteet** väärtust.</span><span class="sxs-lookup"><span data-stu-id="0dffc-178">Increase the **Priority** value of the new line.</span></span> <span data-ttu-id="0dffc-179">Kasutage nuppu **Nihuta üles**, et liigutada rida nii, et see oleks sama serdi eelmise versiooni rea kohal.</span><span class="sxs-lookup"><span data-stu-id="0dffc-179">Use the **Move up** button to move the line so that it's above the line for the previous version of the same certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="0dffc-180">Commerce Runtime'is kutsutakse serdi uut versiooni esimesena.</span><span class="sxs-lookup"><span data-stu-id="0dffc-180">In the Commerce runtime, the new version of the certificate will be called first.</span></span> <span data-ttu-id="0dffc-181">Kui serti ei olda veel kindlas poes või terminalis värskendatud, kutsutakse eelmist versiooni.</span><span class="sxs-lookup"><span data-stu-id="0dffc-181">If the certificate hasn't yet been updated in a specific store or on a specific terminal, the previous version will be called.</span></span>
