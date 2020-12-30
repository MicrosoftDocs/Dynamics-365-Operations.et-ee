---
title: Automaatsete tasude lubamine ja konfigureerimine kanali kaupa
description: Selles teemas selgitatakse, kuidas lubada ja konfigureerida automaatseid tasusid kanali järgi Microsoft Dynamics 365 Commerce'is.
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 1be07c754e563298d82f6ca54f09ae3aa9118602
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411652"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="edd1d-103">Automaatsete tasude lubamine ja konfigureerimine kanali kaupa</span><span class="sxs-lookup"><span data-stu-id="edd1d-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="edd1d-104">Selles teemas selgitatakse, kuidas lubada ja konfigureerida automaatseid tasusid kanali järgi Microsoft Dynamics 365 Commerce'is.</span><span class="sxs-lookup"><span data-stu-id="edd1d-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="edd1d-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="edd1d-105">Overview</span></span>

<span data-ttu-id="edd1d-106">Teil võib ette tulla olukordi, kus peate rakendama ringlussevõtu tasusid või muid tasusid kindlale tootegrupile, mida müüakse kõikides või osades poodides kindlas osariigis (nt Californias).</span><span class="sxs-lookup"><span data-stu-id="edd1d-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="edd1d-107">Commerce'i funktsioon **Luba automaatsete tasude filtreerimine kanali järgi** võimaldab teil määrata automaatseid tasusid kanali järgi (nt kindel füüsiliste poodide kanal).</span><span class="sxs-lookup"><span data-stu-id="edd1d-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="edd1d-108">See funktsioon on saadaval rakenduses Dynamics 365 Commerce versioonis 10.0.10 ja uuemas.</span><span class="sxs-lookup"><span data-stu-id="edd1d-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="edd1d-109">Automaatsete tasude lubamiseks ja konfigureerimiseks kanali järgi peate lõpule viima järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="edd1d-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="edd1d-110">Lülitage sisse funktsioon **Luba automaatsete tasude filtreerimine kanali järgi**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="edd1d-111">Konfigureerige organisatsiooni hierarhia eesmärk.</span><span class="sxs-lookup"><span data-stu-id="edd1d-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="edd1d-112">Määratlege automaatsed tasud kanali järgi.</span><span class="sxs-lookup"><span data-stu-id="edd1d-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="edd1d-113">Funktsioon **Luba automaatsete tasude filtreerimine kanali järgi** töötab ainult juhul, kui täpsemate automaatsete tasude funktsioon on samuti sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="edd1d-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="edd1d-114">Lisateabe saamiseks täpsemate automaatsete tasude funktsiooni sisselülitamise kohta leiate teemast [Omnikanali täpsemad automaatsed tasud](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="edd1d-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="edd1d-115">Lülitage sisse funktsioon Luba automaatsete tasude filtreerimine kanali järgi</span><span class="sxs-lookup"><span data-stu-id="edd1d-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="edd1d-116">Commerce'is automaatsete tasude lubamiseks kanali järgi toimige järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="edd1d-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="edd1d-117">Minge jaotisse **Süsteemi administraator \> Tööruumid \> Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="edd1d-118">Vahekaardi **Pole lubatud** loendis **Funktsiooni nimi** otsige ja valige **Luba automaatsete tasude filtreerimine kanali järgi**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="edd1d-119">Valige paremas alanurgas **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="edd1d-120">Pärast funktsiooni sisselülitamist kuvatakse see vahekaardi loendis **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="edd1d-121">Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="edd1d-122">Leidke ja valige vasakpoolsel paanil töö **1110** (**Globaalne konfiguratsioon**).</span><span class="sxs-lookup"><span data-stu-id="edd1d-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="edd1d-123">Konfiguratsioonimuudatuste lisamiseks valige tegevuse paanil käsk **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="edd1d-124">Funktsiooni **Luba automaatsete tasude filtreerimine kanali järgi** väljalülitamisel, kui olete seda juba kasutanud, ei kuvata enam jaotises **Automaatsed tasud** välja **Jaemüügikanali seos** ja olemasolevad konfiguratsioonid lähevad kaotsi.</span><span class="sxs-lookup"><span data-stu-id="edd1d-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="edd1d-125">Kui konfiguratsioonide **Jaemüügikanali seos** eemaldamine põhjustab automaatsete tasude reeglite dubleerimise, ei õnnestu funktsiooni välja lülitada.</span><span class="sxs-lookup"><span data-stu-id="edd1d-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="edd1d-126">Enne funktsiooni väljalülitamist vaadake kindlasti üle kõik automaatsete tasude reeglid ja tehke vajalikud muudatused.</span><span class="sxs-lookup"><span data-stu-id="edd1d-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="edd1d-127">Organisatsiooni hierarhia eesmärgi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="edd1d-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="edd1d-128">Uus organisatsiooni hierarhia eesmärk nimega **Jaemüügi automaatsed tasud** on loodud automaatsete tasude hierarhia haldamiseks kanali järgi.</span><span class="sxs-lookup"><span data-stu-id="edd1d-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="edd1d-129">Commerce'is organisatsiooni hierarhia eesmärgi jaoks vaikehierarhia määramiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="edd1d-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="edd1d-130">Minge jaotisse **Organisatsiooni haldus \> Organisatsioonid \> Organisatsiooni hierarhia eesmärgid**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="edd1d-131">Valige vasakpoolsel paanil **Jaemüügi automaatsed tasud**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="edd1d-132">Jaotises **Määratud hierarhiad** valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="edd1d-133">Dialoogiboksis **Organisatsiooni hierarhiad** valige organisatsiooni hierarhia (nt **Jaekauplused piirkonniti**) ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="edd1d-134">Jaotises **Määratud hierarhiad** valige **Määra vaikesätteks**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="edd1d-135">Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="edd1d-136">Leidke ja valige vasakpoolsel paanil töö **1040** (**Tooted**).</span><span class="sxs-lookup"><span data-stu-id="edd1d-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="edd1d-137">Valige tegevuste paanil käsk **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="edd1d-138">Korrake kahte eelmist kahte toimingut tööde **1070** (**Kanali konfiguratsioon**) ja **1110** (**Globaalne konfiguratsioon**) käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="edd1d-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![Jaemüügi automaatsete tasude organisatsiooni hierarhia eesmärgi konfigureerimine](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="edd1d-140">Automaatsete tasude määratlemine kanali järgi</span><span class="sxs-lookup"><span data-stu-id="edd1d-140">Define auto charges by channel</span></span>

<span data-ttu-id="edd1d-141">Pärast funktsiooni **Luba automaatsete tasude filtreerimine kanali järgi** sisselülitamist ja organisatsiooni hierarhia eesmärgi **Jaemüügi automaatsed tasud** konfigureerimist saab automaatseid kulusid kanali järgi määratleda kas tellimuse päise või tellimuserea tasemel.</span><span class="sxs-lookup"><span data-stu-id="edd1d-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="edd1d-142">Commerce'is automaatsete tasude määratlemiseks kanali järgi toimige järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="edd1d-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="edd1d-143">Minge jaotisse **Müügireskontro \> Kulude seadistus \> Automaatsed kulud**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="edd1d-144">Valige vasakpoolse paani väljlal **Tase** kas **Päis** või **Rida**, sõltuvalt teie ettevõtte vajadusest.</span><span class="sxs-lookup"><span data-stu-id="edd1d-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="edd1d-145">Valige väljal **Jaemüügikanali kood** sobiv kanali kood (nt **Tabel** või **Grupp**).</span><span class="sxs-lookup"><span data-stu-id="edd1d-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="edd1d-146">Kui kasutate vaikesätet **Kõik**, rakendatakse tasude reeglid kõigile kanalitele.</span><span class="sxs-lookup"><span data-stu-id="edd1d-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="edd1d-147">Kui teete valiku **Grupp**, veenduge, et jaemüügikanali tasude grupp luuakse jaotises **Jaemüük ja kaubandus \> Kanali häälestus \> Tasud \> Jaemüügikanali tasude grupid**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="edd1d-148">Kui teete valiku **Tabel**, saate valida kindla kanali (nt **San Francisco**) väljal **Jaemüügikanali seos**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="edd1d-149">Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="edd1d-150">Leidke ja valige vasakpoolsel paanil töö **1040** (**Tooted**).</span><span class="sxs-lookup"><span data-stu-id="edd1d-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="edd1d-151">Valige tegevuste paanil käsk **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="edd1d-152">Korrake kahte eelmist kahte toimingut tööde **1070** (**Kanali konfiguratsioon**) ja **1110** (**Globaalne konfiguratsioon**) käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="edd1d-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![Kanali järgi määratletud automaatsed tasud](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="edd1d-154">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="edd1d-154">Example scenario</span></span>

<span data-ttu-id="edd1d-155">Järgmises näites kirjeldatakse toote konfigureerimiseks vajalikke etappe nii, et ringlussevõtu tasusid võetakse toote müümisel San Francisco füüsilise kaupluse kanali kaudu.</span><span class="sxs-lookup"><span data-stu-id="edd1d-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="edd1d-156">Selles näites kirjeldatakse ka automaatsete tasude kuvamist Commerce'i kassarakenduses.</span><span class="sxs-lookup"><span data-stu-id="edd1d-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="edd1d-157">Organisatsioon määratleb tasude koodi nimega **RINGLUSSEVÕTT**, nagu järgmisel joonisel on näidatud.</span><span class="sxs-lookup"><span data-stu-id="edd1d-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![Tasude kood RINGLUSSEVÕTT](media/Auto-charges-charge-code.png)

<span data-ttu-id="edd1d-159">Automaatne tasu luuakse reatasemel.</span><span class="sxs-lookup"><span data-stu-id="edd1d-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="edd1d-160">Sellel on järgmine konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="edd1d-160">It has the following configuration:</span></span>

- <span data-ttu-id="edd1d-161">Välja **Konto kood** väärtuseks on seatud **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="edd1d-162">Välja **Kaubakood** väärtuseks on seatud **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="edd1d-163">Välja **Kauba seos** väärtuseks on seatud toote ID **91001**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="edd1d-164">Välja **Tarneviisi kood** väärtuseks on seatud **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="edd1d-165">Välja **Jaemüügikanali kood** väärtuseks on seatud **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="edd1d-166">Välja **Jaemüügikanali seos** väärtuseks on seatud kauplus **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="edd1d-167">Automaatsete tasude rida on loodud.</span><span class="sxs-lookup"><span data-stu-id="edd1d-167">An auto charges line is created.</span></span> <span data-ttu-id="edd1d-168">Sellel on järgmine konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="edd1d-168">It has the following configuration:</span></span>

- <span data-ttu-id="edd1d-169">Välja **Valuuta** väärtuseks on seatud **USD**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="edd1d-170">Välja **Tasude kood** väärtuseks on seatud **RINGLUSSEVÕTT**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="edd1d-171">Välja **Kategooria** väärtuseks on seatud **Fikseeritud**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="edd1d-172">Välja **Tasud** väärtuseks on seatud **6,25 $**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-172">The **Charges** field is set to **$6.25**.</span></span>

![Reataseme automaatsete tasude ja automaatsete tasude rea konfigureerimine](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="edd1d-174">Kassarakenduses on loodud müügitellimus kaupluse kanalis **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="edd1d-175">Real **Kulud** kuvatakse ringlussevõtu tasu **6,25 $**.</span><span class="sxs-lookup"><span data-stu-id="edd1d-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="edd1d-176">Valides kassarakenduses **Kande suvandid \> Tasud \> Tasude haldamine** saate vaadata tasude koodi ja ringlussevõtu tasu kirjeldust.</span><span class="sxs-lookup"><span data-stu-id="edd1d-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![Ringlussevõtu tasu kassarakenduses](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="edd1d-178">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="edd1d-178">Additional resources</span></span>

[<span data-ttu-id="edd1d-179">Omnikanali täpsemad automaatsed kulud</span><span class="sxs-lookup"><span data-stu-id="edd1d-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="edd1d-180">Päisekulude proportsionaalselt jaotamine vastavatele müügiridadele</span><span class="sxs-lookup"><span data-stu-id="edd1d-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)
