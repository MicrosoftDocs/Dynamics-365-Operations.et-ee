---
title: Kliendimaksete ülevaated (eelvaade)
description: Selles teemas kirjeldatakse makse ülevaadete võimalust, mis aitab parandada individuaalse kliendi tüüpilise maksekäitumise mõistmist ja tuvastada olukorrad, mis õigustavad kogumisprotsesside varasemat algatamist kui olete muidu seda teinud.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f9f1e4ae4270380c88069723e768fd44ecf8c113
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773938"
---
# <a name="customer-payment-insights-preview"></a><span data-ttu-id="55996-103">Kliendimaksete ülevaated (eelvaade)</span><span class="sxs-lookup"><span data-stu-id="55996-103">Customer payment insights (Preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="55996-104">Selles teemas kirjeldatakse makse ülevaadete võimalust, mis aitab parandada individuaalse kliendi tüüpilise maksekäitumise mõistmist ja mis saab tuvastada olukorrad, mis õigustavad kogumisprotsesside varasemat algatamist kui oleksite muidu seda teinud.</span><span class="sxs-lookup"><span data-stu-id="55996-104">This topic describes the payment insights capability that helps improve understanding of individual customers' typical payment practices and that can identify circumstances that justify initiating collection processes earlier than you might have done otherwise.</span></span> 

## <a name="overview"></a><span data-ttu-id="55996-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="55996-105">Overview</span></span>

<span data-ttu-id="55996-106">Organisatsioonidel on tihti raske ennustada, millal kliendid oma arved ära maksavad.</span><span class="sxs-lookup"><span data-stu-id="55996-106">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="55996-107">Selle ülevaate puudumine toob kaasa vähem täpset likviidsuse planeerimised, liiga hilja algavad kogumisprotsessid ja tellimused, mis väljastatakse kliendile, kes ei pruugi maksta.</span><span class="sxs-lookup"><span data-stu-id="55996-107">This lack of insight leads to less accurate cash flow forecasts, collections processes that start too late, and orders that are released to customers who may default on their payment.</span></span> <span data-ttu-id="55996-108">Kliendi makse ülevaated (eelvaade) aitab organisatsioonidel ennustada, millal kliendiarve ära makstakse, aidates organisatsioonidel luua kogumisstrateegiaid, mis täiustavad õigel ajal maksmise tõenäosust.</span><span class="sxs-lookup"><span data-stu-id="55996-108">Customer payment insights (Preview) helps organizations predict when a customer invoice will be paid, helping organization create collections strategies that improve the probability of being paid on time.</span></span> 

## <a name="predictions"></a><span data-ttu-id="55996-109">Ennustused</span><span class="sxs-lookup"><span data-stu-id="55996-109">Predictions</span></span>

<span data-ttu-id="55996-110">Makseennustused võimaldavad organisatsioonidel parandada oma äriprotsesse, aidates neil hõlpsasti tuvastada arveid, mis tõenäoliselt makstakse hilja, ja võtta asjakohaseid meetmeid, mis parandavad nende võimalusi saada õigeaegselt tasutud.</span><span class="sxs-lookup"><span data-stu-id="55996-110">Payment predictions will enable organizations to improve their business processes by helping them easily identify the invoices that are likely to be paid late, and to take appropriate measures that improve their chances of getting paid on time.</span></span>

<span data-ttu-id="55996-111">Masinõppe mudelit kasutades, mis kasutab varasemaid arveid, makseid ja kliendiandmeid, ennustab kliendimaksete ülevaated (eelvaade) veelgi täpsemalt, millal klient tasumata arve ära maksab.</span><span class="sxs-lookup"><span data-stu-id="55996-111">Using a machine learning model, which leverages historical invoices, payments and customer data, Customer payment insights (Preview) more accurately predicts when a customer will pay an outstanding invoice.</span></span>

<span data-ttu-id="55996-112">Funktsioon Kliendi makse ülevaated (eelvaade) ennustab iga avatud arve jaoks kolme maksetõenäosust.</span><span class="sxs-lookup"><span data-stu-id="55996-112">For each open invoice, Customer payment insights (Preview) predicts three payment probabilities:</span></span>

-   <span data-ttu-id="55996-113">Õigeaegselt maksmise tõenäosus</span><span class="sxs-lookup"><span data-stu-id="55996-113">Probability of payment being made on time</span></span> 
-   <span data-ttu-id="55996-114">Makse hilja tegemise tõenäosus</span><span class="sxs-lookup"><span data-stu-id="55996-114">Probability of payment being made late</span></span>
-   <span data-ttu-id="55996-115">Makse väga hilja tegemise tõenäosus</span><span class="sxs-lookup"><span data-stu-id="55996-115">Probability of payment being made very late</span></span>

<span data-ttu-id="55996-116">Et aidata organisatsioonidel mõista kogu maksesummat, mida nad võivad kliendilt oodata ühte kolmest ämbrist (õigel ajal, hilja ja väga hilja), annab Klindi makse ülevaated (eelvaade) ka eeldatavate maksete koondvaate.</span><span class="sxs-lookup"><span data-stu-id="55996-116">To help Organizations understand the total payment amount they can expect from a customer in one of the three buckets, On time, Late and Very late, Customer payment insights (Preview) also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="55996-117">[![Maksete ennustuste koondvaade](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="55996-117">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="55996-118">Lisaks määratakse igale arvele õigeaegse maksmise tõenäosus.</span><span class="sxs-lookup"><span data-stu-id="55996-118">Also, each invoice is assigned a probability of payment on time.</span></span> <span data-ttu-id="55996-119">Kui õigeaegselt maksmise tõenäosus on väiksem kui 50%, märgistatakse arved punase ringiga, et näidata need arved võivad vajada kättesaamiseks tähelepanu.</span><span class="sxs-lookup"><span data-stu-id="55996-119">If the probability of payment on time is less than 50%, the invoices are tagged with a red circle to  indicate that these invoices may require collections attention.</span></span> 

<span data-ttu-id="55996-120">[![Maksetõenäosuste loend](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="55996-120">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="55996-121">Kliendi makse ülevaated (eelvaade) pakub ka ennustuse selgitamiseks konteksti puudutavat teavet, näiteks prognoose mõjutanud peamised tegurid, praegune äritegevuse olukord kliendiga ja üksikasjad seoses kliendi ajaloolise maksekäitumisega.</span><span class="sxs-lookup"><span data-stu-id="55996-121">Customer Payment Insights (Preview) also provides contextual information to explain the prediction, such as the top factors that influenced the predictions, the current state of business with the customer, and details about the historical customer payment behavior.</span></span> <span data-ttu-id="55996-122">Paljudes ettevõtetes on kogumistoiming reaktiivne tegevus; kogumistoiming ei alga enne, kui saabub arve tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="55996-122">In many businesses, the collections process has been a reactive activity; the collections process doesn’t start until invoices come due.</span></span> 

<span data-ttu-id="55996-123">Kliendi makse ülevaadete (eelvaade) abil saavad organisatsioonid olla kogumiste osas palju proaktiivsemad.</span><span class="sxs-lookup"><span data-stu-id="55996-123">With Customer payment insights (Preview), organizations can be more proactive about collections.</span></span> <span data-ttu-id="55996-124">Nad ei pea enam kogumisprotsessi alustamiseks ootama, kuni saabub ülekande tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="55996-124">They no longer have to wait for the transactions to become due to start the collection process.</span></span> <span data-ttu-id="55996-125">Selle asemel saavad nad kasutada makse prognoosimise võimekust, et teha kindlaks, kas proaktiivne kogumine parandab õigeaegselt tasumise tõenäosust.</span><span class="sxs-lookup"><span data-stu-id="55996-125">Instead, they can use the payment prediction capability to determine whether proactive collections will improve the probability of being paid on time.</span></span> <span data-ttu-id="55996-126">Makse ennustus annab ettevõtetele ka teavet, mis on vajalik kogumisprotsessi varakult alustamise õigustamiseks.</span><span class="sxs-lookup"><span data-stu-id="55996-126">Payment prediction also gives businesses the information needed to justify starting the collection process early.</span></span>

## <a name="methodology"></a><span data-ttu-id="55996-127">Metoodika</span><span class="sxs-lookup"><span data-stu-id="55996-127">Methodology</span></span>

<span data-ttu-id="55996-128">Tehisintellektiga lahenduse arendamine ja kasutuselevõtmine on raske.</span><span class="sxs-lookup"><span data-stu-id="55996-128">Developing and deploying an AI solution is hard.</span></span> <span data-ttu-id="55996-129">Selleks on vajalik andmeteadlastest, valdkonna asjatundjatest ja inseneridest koosnevat meeskonda, kes töötavad pikka aega, et sõnastada, arendada, kasutada ja hallata kasutatavat tehisintellekti lahendust.</span><span class="sxs-lookup"><span data-stu-id="55996-129">It takes a team of data scientists, subject matter experts and engineers, working for an extended period of time to formulate, develop, deploy and maintain a usable AI solution.</span></span> <span data-ttu-id="55996-130">Me muudame tehisintellektiga lahenduse rakenduses Finance juurutamise ja kasutamise lihtsaks.</span><span class="sxs-lookup"><span data-stu-id="55996-130">We are making it easy to deploy and use AI solutions in Finance.</span></span> <span data-ttu-id="55996-131">Meil on lisame tehisintellektiga lahendused rakendusse Finance, mis on ehitatud Microsoft AI Builderi peale.</span><span class="sxs-lookup"><span data-stu-id="55996-131">We are prepackaging AI solutions in Finance that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="55996-132">Lõppkasutaja saab ühe nupuvajutusega juurutada tehisintellektiga lahenduse ja hakata kaaluma nutikate ennustuste eeliseid.</span><span class="sxs-lookup"><span data-stu-id="55996-132">An end user, with the single click of button, can deploy the AI solution and start leveraging the benefits of intelligent predictions.</span></span> <span data-ttu-id="55996-133">Kui organisatsioon ei ole ennustuste täpsusega rahul, saab lauskasutaja taas ühe nupuvajutusega siseneda AI Builderi laienduskogemusse ja seejärel valida või tühistada nende väljade valiku, mida kasutatakse ennustuste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="55996-133">If an organization isn't satisfied with the accuracy of predictions, a power user, again using a single click, can enter the AI builder extension experience, and then select or deselect the fields used to generate predictions.</span></span> <span data-ttu-id="55996-134">Kui valmis, saavad nad treenida ja avaldada muudatused ning uut treenitud mudelit hakatakse automaatselt rakenduses Finance ennustuste jaoks kasutama.</span><span class="sxs-lookup"><span data-stu-id="55996-134">Once ready, they can train and publish the changes, and the newly trained model will be automatically picked up for predictions in Finance.</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="55996-135">Kuidas hankida funktsioon Kliendi makse ülevaated (eelvaade)</span><span class="sxs-lookup"><span data-stu-id="55996-135">How to get Customer payment insights (Preview)</span></span>

<span data-ttu-id="55996-136">Kui olete huvitatud funktsiooni Kliendi makse ülevaated (eelvaade) proovimisest, saatke meil [Kliendi makse ülevaated (eelvaade)](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="55996-136">Please send email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in trying the Customer payment insights (Preview).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="55996-137">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="55996-137">Privacy Notice</span></span>

<span data-ttu-id="55996-138">Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus, 2) ei ole hõlmatud selle teenuse teenusetaseme leppes, 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud, ja 4) on piiratud toega.</span><span class="sxs-lookup"><span data-stu-id="55996-138">Previews (1) may utilize less privacy and security measures than the Dynamics 365 Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>


