---
title: Kliendiportaali kohandamine ja kasutamine
description: Selles teemas selgitatakse, kuidas kohandada kliendiportaali pärast teie süsteemi lisamist.
author: dasani-madipalli
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 16d5c13c0fbff8c5033b0d1e9dd0d07851521126
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840769"
---
# <a name="customize-and-use-the-customer-portal"></a><span data-ttu-id="76027-103">Kliendiportaali kohandamine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="76027-103">Customize and use the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="76027-104">Selles teemas kirjeldatakse erinevaid lehti, mis on valmiskujul kliendiportaalis saadaval.</span><span class="sxs-lookup"><span data-stu-id="76027-104">This topic describes the different pages that available in the Customer portal out of the box.</span></span> <span data-ttu-id="76027-105">Selles seletatakse, mida lehed teevad ja kuidas saate neid kohandada.</span><span class="sxs-lookup"><span data-stu-id="76027-105">It explains what the pages do and how you can customize them.</span></span>

<span data-ttu-id="76027-106">Kliendiportaal pakub valmiskujul mõningaid veebilehti ja toiminguid.</span><span class="sxs-lookup"><span data-stu-id="76027-106">The Customer portal offers a few webpages and actions out of the box.</span></span> <span data-ttu-id="76027-107">Järgmine saidikaart annab ülevaate nendest veebisaitidest ja toimingutest ning samuti rollidest, mis saavad nimetatud toiminguid teha.</span><span class="sxs-lookup"><span data-stu-id="76027-107">The following site map provides an overview of those webpages and actions, and the roles that can perform the actions.</span></span>

<span data-ttu-id="76027-108">![Kliendiportaali saidikaart](media/customer-portal-site-map.png "Kliendiportaali saidikaart")</span><span class="sxs-lookup"><span data-stu-id="76027-108">![Customer portal site map](media/customer-portal-site-map.png "Customer portal site map")</span></span>

## <a name="typical-customizations"></a><span data-ttu-id="76027-109">Tavalised kohandused</span><span class="sxs-lookup"><span data-stu-id="76027-109">Typical customizations</span></span>

<span data-ttu-id="76027-110">Järgmised teemad aitavad teil õppida Power Appsi portaalide põhitõdesid ning portaalide kohandamise viise.</span><span class="sxs-lookup"><span data-stu-id="76027-110">The following topics will help you learn the basics about Power Apps portals and how you can customize portals:</span></span>

- <span data-ttu-id="76027-111">[Töö mallidega](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) – selles teemas antakse üldine ülevaade sellest, kuidas Power Appsi portaalid toimivad ja kuidas saate teha portaalides lihtsamaid kohandusi.</span><span class="sxs-lookup"><span data-stu-id="76027-111">[Work with templates](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) – This topic provides a general overview of how Power Apps portals works and how you can do simple customizations of portals.</span></span>
- <span data-ttu-id="76027-112">[Portaali sisu haldamine](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) – selles teemas selgitatakse, kuidas saate hallata ja kohandada sisu, mida oma portaalis kasutate.</span><span class="sxs-lookup"><span data-stu-id="76027-112">[Manage portal content](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) – This topic explains how you can manage and customize the content that you surface in your portal.</span></span>
- <span data-ttu-id="76027-113">[CSS-i redigeerimine](https://docs.microsoft.com/powerapps/maker/portals/edit-css) – see teema aitab teil teha oma portaali kasutajaliidese keerukamaid kohandusi.</span><span class="sxs-lookup"><span data-stu-id="76027-113">[Edit CSS](https://docs.microsoft.com/powerapps/maker/portals/edit-css) – This topic helps you make more complex customizations to the user interface (UI) of your portal.</span></span>
- <span data-ttu-id="76027-114">[Portaali jaoks teema loomine](https://docs.microsoft.com/dynamics365/portals/create-theme) – selles teemas aidatakse teil luua oma portaali kasutajaliidese teema.</span><span class="sxs-lookup"><span data-stu-id="76027-114">[Create a theme for your portal](https://docs.microsoft.com/dynamics365/portals/create-theme) – This topic helps you create a UI theme for your portal.</span></span>
- <span data-ttu-id="76027-115">[Portaali sisu lihtne loomine ja esitamine](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) – selles teemas aidatakse teil hallata alusandmeid ja -tabeleid, mida oma portaalis kasutate.</span><span class="sxs-lookup"><span data-stu-id="76027-115">[Create and expose portal content easily](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) – This topic helps you manage the underlying data and tables that you use for your portal.</span></span>
- <span data-ttu-id="76027-116">[Kontakti konfigureerimine portaalis kasutamiseks](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) – selles teemas selgitatakse, kuidas luua ja kohandada kasutajarolle ning kuidas toimivad Power Appsi portaalide turve ja autentimine.</span><span class="sxs-lookup"><span data-stu-id="76027-116">[Configure a contact for use on a portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) – This topic explains how to create and customize user roles, and how security and authentication work in Power Apps portals.</span></span>
- <span data-ttu-id="76027-117">[Teadete konfigureerimine portaalide tabeli- ja veebivormide jaoks](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) – selles teemas selgitatakse, kuidas lisada portaali dokumente ja täiendavat mäluruumi.</span><span class="sxs-lookup"><span data-stu-id="76027-117">[Configure notes for table forms and web forms on portals](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) – This topic explains how to add documents and additional storage to your portal.</span></span>
- <span data-ttu-id="76027-118">[Portaali veebisaidi tõrketöötlus](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) – selles teemas selgitatakse, kuidas kuvada portaali tõrkelogisid ja salvestada neid oma Microsoft Azure'i bloobimälu kontol.</span><span class="sxs-lookup"><span data-stu-id="76027-118">[Error handling for portal website](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) – This topic explains how to view portal error logs and store them in your Microsoft Azure Blob storage account.</span></span>

## <a name="customize-the-order-creation-process"></a><span data-ttu-id="76027-119">Tellimuse loomise protsessi kohandamine</span><span class="sxs-lookup"><span data-stu-id="76027-119">Customize the order creation process</span></span>

<span data-ttu-id="76027-120">Kui kasutaja esitab kliendiportaali kasutades tellimuse, siis sünkroonitakse tellimus automaatselt asjakohase Dynamics 365 Supply Chain Managementi keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="76027-120">When a user submits an order by using the Customer portal, the order is automatically synced to the corresponding Dynamics 365 Supply Chain Management environment.</span></span> <span data-ttu-id="76027-121">Kuna kasutaja on välisklient, siis on osa nõutavast teabest tema eest tahtlikult peidetud.</span><span class="sxs-lookup"><span data-stu-id="76027-121">Because the user is an external customer, some required information is intentionally hidden from him or her.</span></span> <span data-ttu-id="76027-122">See teave täidetakse automaatselt vormi esitamisel.</span><span class="sxs-lookup"><span data-stu-id="76027-122">This information will automatically be filled in when the form is submitted.</span></span>

<span data-ttu-id="76027-123">Selles jaotises näidatakse, kuidas peaksite seadistama kontakte, et vältida tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="76027-123">This section shows how you should set up contacts to avoid errors.</span></span> <span data-ttu-id="76027-124">See selgitab automaatselt määratud väljasid ning seda, kuidas saate vajadusel nende väljade väärtusi muuta.</span><span class="sxs-lookup"><span data-stu-id="76027-124">It explains fields that are automatically set and how you can modify the value of those fields if you must.</span></span>

### <a name="the-out-of-box-order-creation-process"></a><span data-ttu-id="76027-125">Valmiskujul tellimuse loomise protsess</span><span class="sxs-lookup"><span data-stu-id="76027-125">The out-of-box order creation process</span></span>

<span data-ttu-id="76027-126">Siit leiate standardetapid tellimuse esitamiseks kliendiportaali kaudu.</span><span class="sxs-lookup"><span data-stu-id="76027-126">Here are the standard steps for submitting an order from the Customer portal.</span></span>

1. <span data-ttu-id="76027-127">Valige avalehel viisardi **Tellimuse loomine** avamiseks paan **Tellimuse loomine**.</span><span class="sxs-lookup"><span data-stu-id="76027-127">On the home page, select the **Create order** tile to open the **Create Order** wizard.</span></span>
1. <span data-ttu-id="76027-128">Seadistage lehel **Tellimuse teave** järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="76027-128">On the **Order Information** page, set the following fields:</span></span>

    - <span data-ttu-id="76027-129">**Nõutav sissetulekukuupäev** – täpsustage tarnekuupäev.</span><span class="sxs-lookup"><span data-stu-id="76027-129">**Requested receipt date** – Specify the date of delivery.</span></span>
    - <span data-ttu-id="76027-130">**Tarneaadress** – sisestage aadress, kuhu tellimus tuleks tarnida.</span><span class="sxs-lookup"><span data-stu-id="76027-130">**Delivery address** – Enter the address that the order should be delivered to.</span></span>
    - <span data-ttu-id="76027-131">**Ettevõte** – valige kliendi ettevõtte nimi.</span><span class="sxs-lookup"><span data-stu-id="76027-131">**Company** – Select the name of the customer company.</span></span> <span data-ttu-id="76027-132">See väli määratakse mitteadministraatorist kasutajate jaoks automaatselt.</span><span class="sxs-lookup"><span data-stu-id="76027-132">This field is automatically set for non-admin users.</span></span>
    - <span data-ttu-id="76027-133">**Ostutellimuse number** – sisestage tellimuse ostutellimuse number.</span><span class="sxs-lookup"><span data-stu-id="76027-133">**Requisition number** – Enter the requisition number of the order.</span></span> <span data-ttu-id="76027-134">See väli ei ole kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="76027-134">This field isn't required.</span></span>
    - <span data-ttu-id="76027-135">**Tarni riiki/piirkonda** – sisestage riik või piirkond, kuhu kaubad tarnitakse.</span><span class="sxs-lookup"><span data-stu-id="76027-135">**Ship to country/region** – Enter the country or region that the items will be delivered to.</span></span> <span data-ttu-id="76027-136">See väli määratakse mitteadministraatorist kasutajate jaoks automaatselt.</span><span class="sxs-lookup"><span data-stu-id="76027-136">This field is automatically set for non-admin users.</span></span>

    <span data-ttu-id="76027-137">![Tellimuse teabeleht](media/customer-portal-order-information.png "Tellimuse teabeleht")</span><span class="sxs-lookup"><span data-stu-id="76027-137">![Order Information page](media/customer-portal-order-information.png "Order Information page")</span></span>

1. <span data-ttu-id="76027-138">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="76027-138">Select **Next**.</span></span>
1. <span data-ttu-id="76027-139">Valige lehel **Kaubad** suvand **Lisa kaup**.</span><span class="sxs-lookup"><span data-stu-id="76027-139">On the **Items** page, select **Add Item**.</span></span>

    <span data-ttu-id="76027-140">![Kaupade leht](media/customer-portal-items.png "Kaupade leht")</span><span class="sxs-lookup"><span data-stu-id="76027-140">![Items page](media/customer-portal-items.png "Items page")</span></span>

1. <span data-ttu-id="76027-141">Määrake dialoogiboksis **Kauba teave** järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="76027-141">In the **Item Information** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="76027-142">**Toote nimi** – otsige ja valige toode, mida tellimusele lisada.</span><span class="sxs-lookup"><span data-stu-id="76027-142">**Product Name** – Find and select a product to add to the order.</span></span>
    - <span data-ttu-id="76027-143">**Kogus** – sisestage valitud toote kogus.</span><span class="sxs-lookup"><span data-stu-id="76027-143">**Quantity** – Enter the quantity of the selected product.</span></span>
    - <span data-ttu-id="76027-144">**Ühik** – määrake mõõtühik (nt **ea.**, **kg** või **kast**).</span><span class="sxs-lookup"><span data-stu-id="76027-144">**Unit** – Specify the unit of measure (for example, **ea.**, **kgs**, or **box**).</span></span>
    - <span data-ttu-id="76027-145">**Eeldatav netosumma** – väärtus arvutatakse kauba eeldatava hinna ja valitud üksuse koguse korrutisena.</span><span class="sxs-lookup"><span data-stu-id="76027-145">**Estimated net amount** – The value is calculated as the estimated price of the item × the quantity for the selected unit.</span></span>

    <span data-ttu-id="76027-146">![Kauba teabe dialoogiboks](media/customer-portal-item-information.png "Kauba teabe dialoogiboks")</span><span class="sxs-lookup"><span data-stu-id="76027-146">![Item Information dialog box](media/customer-portal-item-information.png "Item Information dialog box")</span></span>

1. <span data-ttu-id="76027-147">Kauba tellimusele lisamiseks valige **Esita**.</span><span class="sxs-lookup"><span data-stu-id="76027-147">Select **Submit** to add the item to the order.</span></span>
1. <span data-ttu-id="76027-148">Korrake samme 4–6, kuni olete lisanud kõik kaubad, mida soovite tellida.</span><span class="sxs-lookup"><span data-stu-id="76027-148">Repeat steps 4 through 6 until you've added all the items that you want to order.</span></span>
1. <span data-ttu-id="76027-149">Kui olete kaupade lisamise lõpetanud, klõpsake lehel **Kaubad** nuppu **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="76027-149">When you've finished adding items, select **Next** on the **Items** page.</span></span>
1. <span data-ttu-id="76027-150">Lehel **Tellimuse teave** esitatakse tellimuse kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="76027-150">The **Order Information** page provides a summary of the order.</span></span> <span data-ttu-id="76027-151">Vaadake üle tellimuse sisu ja tarne üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="76027-151">Review the order contents and delivery details.</span></span> <span data-ttu-id="76027-152">Kui kõik tundub õige, siis valige tellimuse esitamiseks suvand **Esita**.</span><span class="sxs-lookup"><span data-stu-id="76027-152">If everything looks correct, select **Submit** to submit the order.</span></span>

    <span data-ttu-id="76027-153">![Tellimuse teabeleht](media/customer-portal-order-submit.png "Tellimuse teabeleht")</span><span class="sxs-lookup"><span data-stu-id="76027-153">![Order Information page](media/customer-portal-order-submit.png "Order Information page")</span></span>

### <a name="standard-data-setup"></a><span data-ttu-id="76027-154">Standardandmete seadistus</span><span class="sxs-lookup"><span data-stu-id="76027-154">Standard data setup</span></span>

<span data-ttu-id="76027-155">Sujuva kasutajakogemuse tagamise otstarbel täidab kliendiportaal mitme nõutava välja väärtused automaatselt.</span><span class="sxs-lookup"><span data-stu-id="76027-155">To help ensure a smooth user experience, the Customer portal automatically fills in values for several required fields.</span></span> <span data-ttu-id="76027-156">Need väärtused põhinevad tellimust esitava kliendi kontaktikirjes toodud teabel.</span><span class="sxs-lookup"><span data-stu-id="76027-156">These values are based on information in the contact record of the customer who is submitting the order.</span></span>

<span data-ttu-id="76027-157">Kliendiportaali tellimuste esitamiseks kasutava kliendi iga [kontaktirida](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) kohta tuleb täpsustada järgmiste nõutud väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="76027-157">For each [contact row](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) that belongs to a customer who will use the Customer portal to submit orders, values must be specified for the following required fields.</span></span> <span data-ttu-id="76027-158">Vastasel juhul ilmnevad tõrked.</span><span class="sxs-lookup"><span data-stu-id="76027-158">Otherwise, errors will occur.</span></span>

- <span data-ttu-id="76027-159">**Ettevõte** – juriidiline isik, kellele tellimus kuulub</span><span class="sxs-lookup"><span data-stu-id="76027-159">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="76027-160">**Potentsiaalne klient** – tellimusega seotud kliendikonto</span><span class="sxs-lookup"><span data-stu-id="76027-160">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="76027-161">**Hinnakiri** – kliendi jaoks kohandatud hinnakiri</span><span class="sxs-lookup"><span data-stu-id="76027-161">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="76027-162">**Valuuta** – hinna valuuta</span><span class="sxs-lookup"><span data-stu-id="76027-162">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="76027-163">**Tarni riiki/piirkonda** – riik või piirkond, kuhu kaubad tarnitakse</span><span class="sxs-lookup"><span data-stu-id="76027-163">**Ship to country/region** – The country or region that the items will be delivered to</span></span>

<span data-ttu-id="76027-164">Müügitellimuse tabeli jaoks on automaatselt täidetud järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="76027-164">The following fields are automatically set for the sales order table:</span></span>

- <span data-ttu-id="76027-165">**Keel** – tellimuse keel (väärtus võetakse vaikimisi kontaktikirjest).</span><span class="sxs-lookup"><span data-stu-id="76027-165">**Language** – The language of the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="76027-166">**Tarni riiki/piirkonda** – riik või piirkond, kuhu kaubad tarnitakse (väärtus võetakse vaikimisi kontaktikirjest).</span><span class="sxs-lookup"><span data-stu-id="76027-166">**Ship to country/region** – The country or region that the items will be delivered to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="76027-167">**Kontaktisik** – kasutaja, kelle poole pöörduda tellimuse kohta käiva teabe puhul (väärtus võetakse vaikimisi kontaktikirjest).</span><span class="sxs-lookup"><span data-stu-id="76027-167">**Contact person** – The user who can be contacted for information about the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="76027-168">**Ettevõte** – juriidiline isik, kellele tellimus kuulub (väärtus võetakse vaikimisi kontaktikirjest).</span><span class="sxs-lookup"><span data-stu-id="76027-168">**Company** – The legal entity that the order belongs to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="76027-169">**Potentsiaalne klient** – tellimusega seotud kliendikonto (väärtus võetakse vaikimisi kontaktikirjest).</span><span class="sxs-lookup"><span data-stu-id="76027-169">**Potential customer** – The customer account that is associated with the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="76027-170">**Arve klient** – tellimuse arvelduskonto (vaikeväärtus on kontaktikirjes toodud potentsiaalne klient).</span><span class="sxs-lookup"><span data-stu-id="76027-170">**Invoice customer** – The billing account of the order (The default value is the potential customer from the contact record.)</span></span>
- <span data-ttu-id="76027-171">**Müügitellimuse nimi** – müügitellimuse nimi (vaikeväärtus on **müügitellimus**).</span><span class="sxs-lookup"><span data-stu-id="76027-171">**Sales order name** – The name of the sales order (The default value is **sales order**.)</span></span>
- <span data-ttu-id="76027-172">**Valuuta** – hinna valuuta (väärtus võetakse vaikimisi kontaktikirjest).</span><span class="sxs-lookup"><span data-stu-id="76027-172">**Currency** – The currency of the price (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="76027-173">**Hinnakiri** – kliendi jaoks kohandatud hinnakiri (väärtus võetakse vaikimisi kontaktikirjest).</span><span class="sxs-lookup"><span data-stu-id="76027-173">**Price list** – The custom price list for the customer (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="76027-174">**Tarneaadressi kirjeldus** – müügitellimuse tarneaadress (vaikeväärtus on **tarneaadressi kirjeldus**).</span><span class="sxs-lookup"><span data-stu-id="76027-174">**Delivery address description** – The delivery address of the sales order (The default value is **delivery address description**.)</span></span>

### <a name="modify-the-order-creation-process"></a><span data-ttu-id="76027-175">Tellimuse loomise protsessi muutmine</span><span class="sxs-lookup"><span data-stu-id="76027-175">Modify the order creation process</span></span>

<span data-ttu-id="76027-176">Te saate vabalt muuta kliendiportaali välimust ja kasutajaliidest, kui te ei muuda tellimuse loomise põhiprotsessi.</span><span class="sxs-lookup"><span data-stu-id="76027-176">You can freely modify the appearance and UI of the Customer portal if you don't change the basic order creation process.</span></span> <span data-ttu-id="76027-177">Kui soovite muuta tellimuse loomise protsessi, siis tuleb meeles pidada mõned asjad.</span><span class="sxs-lookup"><span data-stu-id="76027-177">If you want to change the order creation process, there are a few points that you must keep in mind.</span></span>

<span data-ttu-id="76027-178">Ärge eemaldage Microsoft Dataverse’is müügitellimuse tabelist järgmisi veerge, kuna need on vajalikud müügitellimuse loomisel topeltkirjutuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="76027-178">Don't remove the following columns from the sales order table in Microsoft Dataverse, because they are required to create a sales order in dual-write:</span></span>

- <span data-ttu-id="76027-179">**Ettevõte** – juriidiline isik, kellele tellimus kuulub</span><span class="sxs-lookup"><span data-stu-id="76027-179">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="76027-180">**Nimi** – müügitellimuse nimi</span><span class="sxs-lookup"><span data-stu-id="76027-180">**Name** – The name of the sales order</span></span>
- <span data-ttu-id="76027-181">**Valuuta** – hinna valuuta</span><span class="sxs-lookup"><span data-stu-id="76027-181">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="76027-182">**Hinnakiri** – kliendi jaoks kohandatud hinnakiri</span><span class="sxs-lookup"><span data-stu-id="76027-182">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="76027-183">**Tarni riiki/piirkonda** – riik või piirkond, kuhu kaubad tarnitakse</span><span class="sxs-lookup"><span data-stu-id="76027-183">**Ship to country/region** – The country or region that the items will be delivered to</span></span>
- <span data-ttu-id="76027-184">**Potentsiaalne klient** – tellimusega seotud kliendikonto</span><span class="sxs-lookup"><span data-stu-id="76027-184">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="76027-185">**Keel** – tellimuse keel (tavaliselt on see potentsiaalse kliendi keel).</span><span class="sxs-lookup"><span data-stu-id="76027-185">**Language** – The language of the order (Typically, this language is the language of the potential customer.)</span></span>
- <span data-ttu-id="76027-186">**Tarneaadressi kirjeldus** – müügitellimuse tarneaadress</span><span class="sxs-lookup"><span data-stu-id="76027-186">**Delivery address description** – The delivery address of the sales order</span></span>

<span data-ttu-id="76027-187">Kaupade puhul on järgmised veerud kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="76027-187">For items, the following columns are required:</span></span>

- <span data-ttu-id="76027-188">**Toode** – tellitav toode</span><span class="sxs-lookup"><span data-stu-id="76027-188">**Product** – The product to order</span></span>
- <span data-ttu-id="76027-189">**Kogus** – valitud toote kogus</span><span class="sxs-lookup"><span data-stu-id="76027-189">**Quantity** – The quantity of the selected product</span></span>
- <span data-ttu-id="76027-190">**Ühik** – mõõtühik (nt **ea.**, **kg** või **kast**)</span><span class="sxs-lookup"><span data-stu-id="76027-190">**Unit** – The unit of measure (for example, **ea.**, **kgs**, or **box**)</span></span>
- <span data-ttu-id="76027-191">**Tarni riiki/piirkonda** – tarneriik või -piirkond</span><span class="sxs-lookup"><span data-stu-id="76027-191">**Ship to country/region** – The country or region of delivery</span></span>
- <span data-ttu-id="76027-192">**Tarneaadressi kirjeldus** – tellimuse tarneaadress</span><span class="sxs-lookup"><span data-stu-id="76027-192">**Delivery address description** – The delivery address of the order</span></span>

<span data-ttu-id="76027-193">Peate veenduma, et kliendiportaal esitaks kuidagi kõigi nende veergude väärtused.</span><span class="sxs-lookup"><span data-stu-id="76027-193">You must make sure that your Customer portal somehow submits values for all these columns.</span></span>

<span data-ttu-id="76027-194">Kui soovite lehele veerge lisada või neid eemaldada, vt teemat [Kiirloomise vormide loomine või redigeerimine sujuvaks andmesisestuseks](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span><span class="sxs-lookup"><span data-stu-id="76027-194">If you want to add columns to the page, or remove columns, see [Create or edit quick create forms for a streamlined data entry experience](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span></span>

<span data-ttu-id="76027-195">Kui soovita muuta veergude eelseadistust ning seda, kuidas väärtused lehe salvestamisel seadistatakse, siis tutvuge Power Appsi portaalide dokumentatsioonis järgmise teabega.</span><span class="sxs-lookup"><span data-stu-id="76027-195">If you want to change how columns are preset and how values are set when the page is saved, see the following information in the Power Apps portals documentation:</span></span>

- [<span data-ttu-id="76027-196">Välja eeltäitmine</span><span class="sxs-lookup"><span data-stu-id="76027-196">Prepopulate field</span></span>](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [<span data-ttu-id="76027-197">Määra väärtus salvestamisel</span><span class="sxs-lookup"><span data-stu-id="76027-197">Set Value On Save</span></span>](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a><span data-ttu-id="76027-198">Avalehe kohandamine</span><span class="sxs-lookup"><span data-stu-id="76027-198">Customize the home page</span></span>

<span data-ttu-id="76027-199">Kõik kliendiportaali juhtelemendid on Power Appsi portaalide sisseehitatud juhtelemendid.</span><span class="sxs-lookup"><span data-stu-id="76027-199">All the controls in the Customer portal are built-in Power Apps portals controls.</span></span> <span data-ttu-id="76027-200">Te saate neid kohandada, järgides Power Appsi portaalide dokumentatsiooni jaotist [Lehe koostamine](https://docs.microsoft.com/powerapps/maker/portals/compose-page).</span><span class="sxs-lookup"><span data-stu-id="76027-200">You can customize them by following the steps in [Compose a page](https://docs.microsoft.com/powerapps/maker/portals/compose-page) in the Power Apps portals documentation.</span></span>

<span data-ttu-id="76027-201">Ainus kliendiportaali malli kaasatud kohandatud juhtelement on mõeldud avalehel paanide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="76027-201">The only custom control that is included in the Customer portal template is used to create the tiles on the home page.</span></span>

<span data-ttu-id="76027-202">![Avalehe paanid](media/customer-portal-home-page-tiles.png "Avalehe paanid")</span><span class="sxs-lookup"><span data-stu-id="76027-202">![Tiles on the home page](media/customer-portal-home-page-tiles.png "Tiles on the home page")</span></span>

<span data-ttu-id="76027-203">Paanide muutmiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="76027-203">To modify the tiles, follow these steps.</span></span>

1. <span data-ttu-id="76027-204">Avage [portaalihalduse rakendus](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal).</span><span class="sxs-lookup"><span data-stu-id="76027-204">Open the [Portal Management app](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal).</span></span>
1. <span data-ttu-id="76027-205">Valige navigeerimispaanilt vasakult suvand **Lehe mallid**.</span><span class="sxs-lookup"><span data-stu-id="76027-205">In the navigation pane on the left, select **Page Templates**.</span></span>

    <span data-ttu-id="76027-206">![Portaalihalduse navigeerimispaan](media/customer-portal-nav.png "Portaalihalduse navigeerimispaan")</span><span class="sxs-lookup"><span data-stu-id="76027-206">![Portal Management navigation pane](media/customer-portal-nav.png "Portal Management navigation pane")</span></span>

1. <span data-ttu-id="76027-207">Valige lehe mall, mille nimi on **Avaleht**.</span><span class="sxs-lookup"><span data-stu-id="76027-207">Select the page template that is named **Home**.</span></span>
1. <span data-ttu-id="76027-208">Valige väljal **Veebimall** link **Avaleht**, et avada selle lehe lähtekood.</span><span class="sxs-lookup"><span data-stu-id="76027-208">In the **Web Template** field, select the **Home** link to open the source code for that page.</span></span>

    <span data-ttu-id="76027-209">![Veebimalli väli](media/customer-portal-web-template.png "Veebimalli väli")</span><span class="sxs-lookup"><span data-stu-id="76027-209">![Web Template field](media/customer-portal-web-template.png "Web Template field")</span></span>

1. <span data-ttu-id="76027-210">Nüüd peaksite nägema kogu avalehe lähtekoodi ja saate seda vajaduse järgi muuta.</span><span class="sxs-lookup"><span data-stu-id="76027-210">You should now see all the source code for the home page and can modify it as you require.</span></span>

## <a name="resources"></a><span data-ttu-id="76027-211">Ressursid</span><span class="sxs-lookup"><span data-stu-id="76027-211">Resources</span></span>

<span data-ttu-id="76027-212">Lisateavet kliendiportaali seadistamise ja kohandamise kohta leiate järgmistest allikatest.</span><span class="sxs-lookup"><span data-stu-id="76027-212">To learn more about how you can set up and customize the Customer portal, see the following resources:</span></span>

- [<span data-ttu-id="76027-213">Power Appsi portaalide dokumentatsioon</span><span class="sxs-lookup"><span data-stu-id="76027-213">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="76027-214">Topeltkirjutuse dokumentatsioon</span><span class="sxs-lookup"><span data-stu-id="76027-214">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [<span data-ttu-id="76027-215">Portaali töötsükkel</span><span class="sxs-lookup"><span data-stu-id="76027-215">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="76027-216">Portaali uuendamine</span><span class="sxs-lookup"><span data-stu-id="76027-216">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="76027-217">Portaali konfiguratsiooni migreerimine</span><span class="sxs-lookup"><span data-stu-id="76027-217">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="76027-218">Lahenduse töötsükli haldus: Dynamics 365 for Customer Engagementi rakendused</span><span class="sxs-lookup"><span data-stu-id="76027-218">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]