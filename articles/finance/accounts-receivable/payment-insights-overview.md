---
title: Kliendimaksete ülevaated (eelvaade)
description: Selles teemas kirjeldatakse makse ülevaadete võimalust, mis aitab parandada üksikute klientide tüüpiliste maksetavade mõistmist. Funktsioon aitab teil tuvastada asjaolud, mis õigustavad sissenõudmisprotsesside alustamist varem, kui te oleksite seda muidu teinud.
author: ShivamPandey-msft
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: a1b3b6540a03dc85d5dcd813e8c41ac49ab36728
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822391"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="54a83-104">Kliendimaksete ülevaated (eelvaade)</span><span class="sxs-lookup"><span data-stu-id="54a83-104">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="54a83-105">Selles teemas kirjeldatakse makse ülevaadete võimalust, mis aitab parandada üksikute klientide tüüpiliste maksetavade mõistmist.</span><span class="sxs-lookup"><span data-stu-id="54a83-105">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices.</span></span> <span data-ttu-id="54a83-106">Funktsioon aitab teil tuvastada asjaolud, mis õigustavad sissenõudmisprotsesside alustamist varem, kui te oleksite seda muidu teinud.</span><span class="sxs-lookup"><span data-stu-id="54a83-106">The feature can help you identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="54a83-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="54a83-107">Overview</span></span>

<span data-ttu-id="54a83-108">Võib olla raske ennustada, millal kliendid oma arved ära maksavad.</span><span class="sxs-lookup"><span data-stu-id="54a83-108">It can be hard to predict when customers will pay their invoices.</span></span> <span data-ttu-id="54a83-109">Selle ülevaate puudumine toob kaasa vähem täpset likviidsuse planeerimised, liiga hilja algavad kogumisprotsessid ja tellimused, mis väljastatakse kliendile, kes ei pruugi maksta.</span><span class="sxs-lookup"><span data-stu-id="54a83-109">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="54a83-110">Funktsioon Kliendi makse ülevaated (eelversioon) aitab organisatsioonidel ennustada, millal kliendi arve tasutakse.</span><span class="sxs-lookup"><span data-stu-id="54a83-110">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="54a83-111">See teave võib aidata organisatsioonidel luua sissenõudmisstrateegiaid, mis parandavad õigeaegselt maksmise tõenäosust.</span><span class="sxs-lookup"><span data-stu-id="54a83-111">This information can help organizations create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="54a83-112">Ennustused</span><span class="sxs-lookup"><span data-stu-id="54a83-112">Predictions</span></span>

<span data-ttu-id="54a83-113">Makseennustused võimaldavad organisatsioonidel parandada oma äriprotsesse, aidates neil hõlpsasti tuvastada arveid, mis tõenäoliselt makstakse hilja, ja võtta asjakohaseid meetmeid, mis parandavad nende võimalusi saada õigeaegselt tasutud.</span><span class="sxs-lookup"><span data-stu-id="54a83-113">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="54a83-114">Masinõppe mudelit kasutades, mis kasutab varasemaid arveid, makseid ja kliendiandmeid, ennustab kliendimaksete ülevaated (eelvaade) veelgi täpsemalt, millal klient tasumata arve ära maksab.</span><span class="sxs-lookup"><span data-stu-id="54a83-114">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="54a83-115">Funktsioon Kliendi makse ülevaated (eelversioon) ennustab iga avatud arve jaoks kolme maksetõenäosust.</span><span class="sxs-lookup"><span data-stu-id="54a83-115">For each open invoice, Customer payment insights (Preview) can predict three payment probabilities:</span></span>

-   <span data-ttu-id="54a83-116">Õigeaegselt maksmise tõenäosus</span><span class="sxs-lookup"><span data-stu-id="54a83-116">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="54a83-117">Makse hilja tegemise tõenäosus</span><span class="sxs-lookup"><span data-stu-id="54a83-117">Probability of payment being made late</span></span>
-   <span data-ttu-id="54a83-118">Makse väga hilja tegemise tõenäosus</span><span class="sxs-lookup"><span data-stu-id="54a83-118">Probability of payment being made very late</span></span>

<span data-ttu-id="54a83-119">Et aidata organisatsioonidel mõista kogu maksesummat, mida nad võivad kliendilt oodata ühes kolmest vahemikust (õigeaegselt, hilja ja väga hilja), annab Klindi makse ülevaated (eelversioon) ka eeldatavate maksete koondvaate.</span><span class="sxs-lookup"><span data-stu-id="54a83-119">Customer payment insights (Preview) also provides an aggregated view of expected payments, which can help organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late.</span></span>

<span data-ttu-id="54a83-120">[![Maksete ennustuste koondvaade](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="54a83-120">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="54a83-121">Lisaks määratakse igale arvele õigeaegse maksmise tõenäosus.</span><span class="sxs-lookup"><span data-stu-id="54a83-121">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="54a83-122">Kui õigeaegselt maksmise tõenäosus on väiksem kui 50%, märgistatakse arved punase ringiga, et näidata need arved võivad vajada kättesaamiseks tähelepanu.</span><span class="sxs-lookup"><span data-stu-id="54a83-122">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="54a83-123">[![Maksetõenäosuste loend](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="54a83-123">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="54a83-124">Kliendi makse ülevaated (eelvaade) pakub ka ennustuse selgitamiseks konteksti puudutavat teavet, näiteks prognoose mõjutanud peamised tegurid, praegune äritegevuse olukord kliendiga ja üksikasjad seoses kliendi ajaloolise maksekäitumisega.</span><span class="sxs-lookup"><span data-stu-id="54a83-124">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="54a83-125">Paljudes ettevõtetes on kogumistoiming reaktiivne tegevus; kogumistoiming ei alga enne, kui saabub arve tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="54a83-125">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="54a83-126">Kliendi makse ülevaadete (eelvaade) abil saavad organisatsioonid olla kogumiste osas palju proaktiivsemad.</span><span class="sxs-lookup"><span data-stu-id="54a83-126">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="54a83-127">Nad ei pea enam kogumisprotsessi alustamiseks ootama, kuni saabub ülekande tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="54a83-127">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="54a83-128">Selle asemel saavad nad kasutada makse prognoosimise võimekust, et teha kindlaks, kas proaktiivne kogumine parandab õigeaegselt tasumise tõenäosust.</span><span class="sxs-lookup"><span data-stu-id="54a83-128">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="54a83-129">Makse ennustus annab ettevõtetele ka teavet, mis on vajalik kogumisprotsessi varakult alustamise õigustamiseks.</span><span class="sxs-lookup"><span data-stu-id="54a83-129">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="54a83-130">Metoodika</span><span class="sxs-lookup"><span data-stu-id="54a83-130">Methodology</span></span>

<span data-ttu-id="54a83-131">Tehisintellektiga lahenduse arendamine ja kasutuselevõtmine on raske.</span><span class="sxs-lookup"><span data-stu-id="54a83-131">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="54a83-132">Selleks on vajalik andmeteadlastest, valdkonna asjatundjatest ja inseneridest koosnevat meeskonda, kes töötavad pikka aega, et sõnastada, arendada, kasutada ja hallata kasutatavat tehisintellekti lahendust.</span><span class="sxs-lookup"><span data-stu-id="54a83-132">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="54a83-133">Me muudame tehisintellektiga lahenduse rakenduses Finance juurutamise ja kasutamise lihtsaks.</span><span class="sxs-lookup"><span data-stu-id="54a83-133">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="54a83-134">Meil on lisame tehisintellektiga lahendused rakendusse Finance, mis on ehitatud Microsoft AI Builderi peale.</span><span class="sxs-lookup"><span data-stu-id="54a83-134">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="54a83-135">Lõppkasutaja saab ühe nupuvajutusega juurutada tehisintellektiga lahenduse ja hakata kaaluma nutikate ennustuste eeliseid.</span><span class="sxs-lookup"><span data-stu-id="54a83-135">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="54a83-136">Kui organisatsioon ei ole ennustuste täpsusega rahul, saab lauskasutaja taas ühe nupuvajutusega siseneda AI Builderi laienduskogemusse ja seejärel valida või tühistada nende väljade valiku, mida kasutatakse ennustuste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="54a83-136">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="54a83-137">Kui valmis, saavad nad treenida ja avaldada muudatused ning uut treenitud mudelit hakatakse automaatselt rakenduses Finance ennustuste jaoks kasutama.</span><span class="sxs-lookup"><span data-stu-id="54a83-137">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="54a83-138">Kuidas hankida funktsioon Kliendi makse ülevaated (eelvaade)</span><span class="sxs-lookup"><span data-stu-id="54a83-138">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="54a83-139">Kui olete huvitatud funktsiooni Kliendi makse ülevaated (eelversioon) proovimisest, saatke meil lahendusele [Kliendi makse ülevaated (eelversioon)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="54a83-139">Send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="54a83-140">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="54a83-140">Privacy Notice</span></span>

<span data-ttu-id="54a83-141">Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus, 2) ei ole hõlmatud selle teenuse teenusetaseme leppes, 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud, ja 4) on piiratud toega.</span><span class="sxs-lookup"><span data-stu-id="54a83-141">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]