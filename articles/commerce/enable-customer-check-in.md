---
title: Luba kliendi sisseregistreerimise teatised kassas (POS)
description: See teema kirjeldab, kuidas lubada kliendi sisseregistreerimise teatisi Microsoft Dynamics 365 Commerce kassas (POS).
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e4defc15d9ef198a361934d51e31016747dbb5ab
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937576"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="6d4db-103">Luba kliendi sisseregistreerimise teatised kassas (POS)</span><span class="sxs-lookup"><span data-stu-id="6d4db-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="6d4db-104">See teema kirjeldab, kuidas lubada kliendi sisseregistreerimise teatisi Microsoft Dynamics 365 Commerce kassas (POS).</span><span class="sxs-lookup"><span data-stu-id="6d4db-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="6d4db-105">Oma "komplekt kasutamiseks valmis olevas tellimuses" võivad organisatsioonid anda lingi või nupu, mis lubab klientidel teavitada kauplust, et nad on valdustes ja ootavad oma paketi välja tuua.</span><span class="sxs-lookup"><span data-stu-id="6d4db-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="6d4db-106">Kliendid saavad seejärel sisseregistreerimise kinnituse ja kauplus saab kassarakenduses ülesandena teatise.</span><span class="sxs-lookup"><span data-stu-id="6d4db-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="6d4db-107">See ülesanne on viip müügipartnerile tellimuse tarnimiseks kliendi sõidukisse.</span><span class="sxs-lookup"><span data-stu-id="6d4db-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="6d4db-108">Seetõttu ei pea klient kauplust sisestama.</span><span class="sxs-lookup"><span data-stu-id="6d4db-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="6d4db-109">Kliendi sisseregistreerimise töövoogu saab konfigureerida ka klientidelt lisateabe kogumiseks, nt klientide parkimise punktinumber, sõiduki tootja, mudel ja värv ning tarnejuhised.</span><span class="sxs-lookup"><span data-stu-id="6d4db-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="6d4db-110">Kaupluse töötaja saab seda teavet tellimuse täitmise hõlbustamiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="6d4db-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="6d4db-111">Kliendi sisseregistreerimise lubamine</span><span class="sxs-lookup"><span data-stu-id="6d4db-111">Enable customer check-in</span></span>

<span data-ttu-id="6d4db-112">Kui kliendi sisseregistreerimise funktsioon on sisse lülitatud, loob Commerce tellimuse kinnituse ID (tuntud ka kui kanaliviite ID).</span><span class="sxs-lookup"><span data-stu-id="6d4db-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="6d4db-113">Samuti loob see tellimuse kinnitus ID-d tellimustele, mis luuakse kassa (POS) või kõnekeskuse kanalite kaudu.</span><span class="sxs-lookup"><span data-stu-id="6d4db-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="6d4db-114">Kliendi sisseregistreerimise funktsiooni sisselülitamiseks Commerce'i peakontoris toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="6d4db-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6d4db-115">Avage **Tööruumid \> Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="6d4db-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="6d4db-116">Otsige kanali funktsiooni **Ühtse kanaliviite ID-vormingu loomine üle kanalite**.</span><span class="sxs-lookup"><span data-stu-id="6d4db-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="6d4db-117">Valige funktsioon ja seejärel valige atribuutide paanil nupp **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="6d4db-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="6d4db-118">Sisseregistreerimise kinnituslehe loomine</span><span class="sxs-lookup"><span data-stu-id="6d4db-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="6d4db-119">Oma e-kaubanduse saidil peate looma uue lehekülje, mis toimib sisseregistreerimise kinnituse kogemusena.</span><span class="sxs-lookup"><span data-stu-id="6d4db-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="6d4db-120">Täiendava konfiguratsiooni abil võib leht sisaldada ka vormi, mis kogub klientidelt tellimuse täitmise hõlbustamiseks täiendavat teavet.</span><span class="sxs-lookup"><span data-stu-id="6d4db-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="6d4db-121">Teavet selle kohta, kuidas seadistada lehekülge ja moodulit, vt [kliendi sisseregistreerimise moodulit](check-in-pickup-module.md).</span><span class="sxs-lookup"><span data-stu-id="6d4db-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="6d4db-122">Kande meilimalli konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6d4db-122">Configure the transactional email template</span></span>

<span data-ttu-id="6d4db-123">Peate lisama siia lingi **Olen siin** või nupu mallile kandemeilide jaoks, mille kliendid saavad, kui nende tellimus on valmis peale võtma.</span><span class="sxs-lookup"><span data-stu-id="6d4db-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="6d4db-124">Kliendid kasutavad seda linki või nuppu, et teavitada kauplust, et nad on saabunud tellimust kätte saama.</span><span class="sxs-lookup"><span data-stu-id="6d4db-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="6d4db-125">Lisage mallile link või nupp, mis on vastendatud **lõpuleviidud pakkimise** teatise tüübiga ja tarneviisiga, mida kasutate tellimuse täitmise curbside'i täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="6d4db-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="6d4db-126">Looge mallis HTML-link või nupp, mis viitab teie loodud sisseregistreerimise kinnituslehe URL-ile.</span><span class="sxs-lookup"><span data-stu-id="6d4db-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="6d4db-127">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="6d4db-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="6d4db-128">Lisateavet e-kirjade mallide konfigureerimise kohta vt [Kande e-kirjade kohandamine tarneviisi alusel](customize-email-delivery-mode.md).</span><span class="sxs-lookup"><span data-stu-id="6d4db-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="6d4db-129">Kassas luuakse sisseregistreerimise kinnitusülesanne</span><span class="sxs-lookup"><span data-stu-id="6d4db-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="6d4db-130">Pärast seda, kui klient teavitab kauplust, et nad on vastuvõtmiseks kohal, saavad nad sisseregistreerimise kinnituse teatise ja ülesanne luuakse müügikoha ülesannete loendis kaupluses, kus klient tellimuse peale võtab.</span><span class="sxs-lookup"><span data-stu-id="6d4db-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="6d4db-131">Ülesanne sisaldab kogu kliendi ja tellimuse teavet, mis on tellimuse täitmiseks vajalik.</span><span class="sxs-lookup"><span data-stu-id="6d4db-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="6d4db-132">Ülesandes näitab juhiste väli kogu teavet, mis koguti kliendilt täiendava teabe vormi kaudu.</span><span class="sxs-lookup"><span data-stu-id="6d4db-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="6d4db-133">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6d4db-133">Additional resources</span></span>

[<span data-ttu-id="6d4db-134">Pealevõtmismooduli sisseregistreerimine</span><span class="sxs-lookup"><span data-stu-id="6d4db-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
