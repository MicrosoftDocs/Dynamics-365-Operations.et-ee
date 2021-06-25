---
title: Kliendimaksete prognoosid (eelversioon)
description: Selles teemas kirjeldatakse makse prognooside võimalust, mis aitab klientide tüüpilisi maksetavasid paremini mõista. Funktsioon aitab teil tuvastada asjaolud, mis peaksid kaasa tooma sissenõudmisprotsesside alustamise varem, kui te oleksite seda muidu teinud.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: 84a2342d76dc309fa1fd3de7b2c3de60e62e4d72
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186392"
---
# <a name="customer-payment-predictions-preview"></a><span data-ttu-id="126d7-104">Kliendimaksete prognoosid (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="126d7-104">Customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="126d7-105">Selles teemas kirjeldatakse makse prognooside võimalust, mis aitab klientide tüüpilisi maksetavasid paremini mõista.</span><span class="sxs-lookup"><span data-stu-id="126d7-105">This topic describes the payment predictions capability that can help you better understand a customer's typical payment practices.</span></span> <span data-ttu-id="126d7-106">Funktsioon aitab teil tuvastada asjaolud, mis peaksid kaasa tooma sissenõudmisprotsesside alustamise varem, kui te oleksite seda muidu teinud.</span><span class="sxs-lookup"><span data-stu-id="126d7-106">This feature can also help identify circumstances that should cause you to start collections processes earlier than you might otherwise start them.</span></span>

## <a name="overview"></a><span data-ttu-id="126d7-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="126d7-107">Overview</span></span>

<span data-ttu-id="126d7-108">Organisatsioonidel on tihti raske ennustada, millal kliendid oma arved ära maksavad.</span><span class="sxs-lookup"><span data-stu-id="126d7-108">Organizations often find it challenging to predict when customers will pay their invoices.</span></span> <span data-ttu-id="126d7-109">Ülevaate puudumine võib tuua kaasa järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="126d7-109">This lack of insight can cause the following issues:</span></span>

- <span data-ttu-id="126d7-110">Vähem täpsemad rahavoogude prognoosid</span><span class="sxs-lookup"><span data-stu-id="126d7-110">Less accurate cash flow forecasts</span></span>
- <span data-ttu-id="126d7-111">Sissenõudmise protsessid, mis algavad liiga hilja</span><span class="sxs-lookup"><span data-stu-id="126d7-111">Collections processes that start too late</span></span>
- <span data-ttu-id="126d7-112">Tellimused vabastatakse klientidele, kes ei pruugi maksta</span><span class="sxs-lookup"><span data-stu-id="126d7-112">Orders that are released to customers who might default on their payment</span></span>

<span data-ttu-id="126d7-113">Kliendi makse prognoosid (eelversioon) aitab organisatsioonidel ennustada, millal kliendi arve tasutakse.</span><span class="sxs-lookup"><span data-stu-id="126d7-113">Customer payment predictions (preview) helps organizations predict when a customer invoice will be paid.</span></span> <span data-ttu-id="126d7-114">Seetõttu saavad nad luua sissenõudmisstrateegiaid, mis aitavad suurendada tõenäosust, et neile makstakse õigeaegselt.</span><span class="sxs-lookup"><span data-stu-id="126d7-114">Therefore, they can create collections strategies that help increase the likelihood that they will be paid on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="126d7-115">Ennustused</span><span class="sxs-lookup"><span data-stu-id="126d7-115">Predictions</span></span>

<span data-ttu-id="126d7-116">Makseprognoosid võimaldavad organisatsioonidel oma äriprotsesse parandada, aidates neil tuvastada arveid, mida võidakse maksta hilinemisega.</span><span class="sxs-lookup"><span data-stu-id="126d7-116">Payment predictions let organizations improve their business processes by helping them identify the invoices that are likely to be paid late.</span></span> <span data-ttu-id="126d7-117">Organisatsioon saab seda teavet kasutada selliste toimingute sooritamiseks, mis parandavad õigeaegselt maksmise tõenäosust.</span><span class="sxs-lookup"><span data-stu-id="126d7-117">Organization can use that information to take actions that improve the chances that they will be paid on time.</span></span>

<span data-ttu-id="126d7-118">Kliendi makseprognooside funktsioon kasutab masinõppemudelit, et täpsemalt ennustada, millal klient tasub tasumata arve.</span><span class="sxs-lookup"><span data-stu-id="126d7-118">The Customer payment predictions feature uses a machine learning model to more accurately predict when a customer will pay an outstanding invoice.</span></span> <span data-ttu-id="126d7-119">See masinõppemudel sisaldab ajaloolisi arveid, makseid ja kliendi andmeid.</span><span class="sxs-lookup"><span data-stu-id="126d7-119">This machine learning model includes historical invoices, payments, and customer data.</span></span>

<span data-ttu-id="126d7-120">Iga avatud arve puhul määrab funktsioon kolm makse tõenäosust.</span><span class="sxs-lookup"><span data-stu-id="126d7-120">For each open invoice, the feature assigns three payment probabilities:</span></span>

- <span data-ttu-id="126d7-121">Tõenäosus, et makse tehakse õigeaegselt</span><span class="sxs-lookup"><span data-stu-id="126d7-121">The probability that the payment will be made on time</span></span>
- <span data-ttu-id="126d7-122">Tõenäosus, et makse tehakse hilinemisega</span><span class="sxs-lookup"><span data-stu-id="126d7-122">The probability that the payment will be made late</span></span>
- <span data-ttu-id="126d7-123">Tõenäosus, et makse tehakse suure hilinemisega</span><span class="sxs-lookup"><span data-stu-id="126d7-123">The probability that the payment will be made very late</span></span>

<span data-ttu-id="126d7-124">Funktsioon sisaldab ka oodatavate maksete summeeritud vaadet.</span><span class="sxs-lookup"><span data-stu-id="126d7-124">The feature also provides an aggregated view of expected payments.</span></span>

<span data-ttu-id="126d7-125">[![Maksete ennustuste koondvaade](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span><span class="sxs-lookup"><span data-stu-id="126d7-125">[![Aggregated view of payment predictions](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)</span></span>

<span data-ttu-id="126d7-126">Igale arvele määratakse õigeaegselt maksmise tõenäosus.</span><span class="sxs-lookup"><span data-stu-id="126d7-126">Each invoice is assigned a probability of on-time payment.</span></span> <span data-ttu-id="126d7-127">Arved, mille õigeaegselt maksmise tõenäosus on väiksem kui 50%, märgistatakse punase ringiga näitamaks, et arved võivad vajada inkassaatori tähelepanu.</span><span class="sxs-lookup"><span data-stu-id="126d7-127">Invoices that have a probability of on-time payment that is less than 50 percent are tagged with a red circle to indicate that they might require attention from a collections agent.</span></span>

<span data-ttu-id="126d7-128">[![Maksetõenäosuste loend](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span><span class="sxs-lookup"><span data-stu-id="126d7-128">[![List of payment probabilities](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)</span></span>

<span data-ttu-id="126d7-129">Kliendimaksete prognooside funktsioon pakub ka kontekstilist teavet prognoosi selgitamiseks.</span><span class="sxs-lookup"><span data-stu-id="126d7-129">The Customer payment predictions feature also provides contextual information to explain the prediction.</span></span> <span data-ttu-id="126d7-130">See teave sisaldab peamisi tegureid, mis mõjutasid prognoosi, praegust äritegevuse seisu kliendiga ja üksikasju kliendi ajaloolise maksekäitumise kohta.</span><span class="sxs-lookup"><span data-stu-id="126d7-130">This information includes the top factors that influenced the prediction, the current state of business with the customer, and details about the customer's historical payment behavior.</span></span>

<span data-ttu-id="126d7-131">Paljudes ettevõtetes on sissenõudmisprotsess olnud reaktiivne tegevus.</span><span class="sxs-lookup"><span data-stu-id="126d7-131">In many businesses, the collections process has been a reactive activity.</span></span> <span data-ttu-id="126d7-132">Teisisõnu ei käivitu sissenõudmisprotsess enne arvete maksetähtaja saabumist.</span><span class="sxs-lookup"><span data-stu-id="126d7-132">In other words, the collections process doesn't start until invoices become due.</span></span> <span data-ttu-id="126d7-133">Kliendi maksete prognooside abil saavad organisatsioonid olla sissenõudmise osas palju proaktiivsemad.</span><span class="sxs-lookup"><span data-stu-id="126d7-133">Customer payment predictions let organizations be more proactive about collections.</span></span> <span data-ttu-id="126d7-134">Nad ei pea enam sissenõudmisprotsessi alustamiseks ootama, kuni saabub ülekande tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="126d7-134">They no longer have to wait for a transaction to become due to start the collections process.</span></span> <span data-ttu-id="126d7-135">Selle asemel saavad nad kasutada makse prognoosimise võimekust, et teha kindlaks, kas proaktiivne sissenõudmine parandab õigeaegselt tasumise tõenäosust.</span><span class="sxs-lookup"><span data-stu-id="126d7-135">Instead, they can use the payment predictions capability to determine whether proactive collections will improve the probability that they will be paid on time.</span></span>

## <a name="methodology"></a><span data-ttu-id="126d7-136">Metoodika</span><span class="sxs-lookup"><span data-stu-id="126d7-136">Methodology</span></span>

<span data-ttu-id="126d7-137">Minevikus on tehisintellektiga (AI) lahendust olnud keeruline arendada ja kasutusele võtta.</span><span class="sxs-lookup"><span data-stu-id="126d7-137">In the past, it has typically been difficult to develop and deploy an artificial intelligence (AI) solution.</span></span> <span data-ttu-id="126d7-138">Selleks protsessiks on olnud vaja meeskonda andmeteadlastest, valdkonna asjatundjatest ja inseneridest, kes teevad ületunde, et sõnastada, arendada, kasutada ja hallata kasutatavat tehisintellekti lahendust.</span><span class="sxs-lookup"><span data-stu-id="126d7-138">The process has required a team that includes data scientists, subject matter experts (SMEs), and engineers, who work over time to formulate, develop, deploy, and maintain a usable AI solution.</span></span> <span data-ttu-id="126d7-139">Kliendi maksete prognoosid hõlbustavad AI lahenduse rakendamist ja kasutamist lahenduses Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="126d7-139">Customer payment predictions makes it easy to deploy and use an AI solution in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="126d7-140">Microsoft paneb kaasa AI lahendused, mis on ehitatud Microsoft AI Builderi peale.</span><span class="sxs-lookup"><span data-stu-id="126d7-140">Microsoft is prepackaging AI solutions that are built on top of Microsoft AI Builder.</span></span> <span data-ttu-id="126d7-141">Seetõttu saavad kasutajad kasutada AI lahendust ühe hiireklõpsuga, et kasutada ära intelligentsete prognooside eeliseid.</span><span class="sxs-lookup"><span data-stu-id="126d7-141">Therefore, users can deploy the AI solution in a single mouse click to take advantage of the benefits of intelligent predictions.</span></span> <span data-ttu-id="126d7-142">Kui te ei ole ennustuste täpsusega rahul, saab lauskasutaja taas ühe nupuvajutusega siseneda AI Builderi laienduskogemusse ja seejärel valida või tühistada nende väljade valiku, mida kasutatakse ennustuste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="126d7-142">If you aren't satisfied with the accuracy of predictions, a power user can (again, in a single mouse click) enter the AI Builder extension experience, and then select or clear the fields that are used to generate predictions.</span></span> <span data-ttu-id="126d7-143">Kui olete valmis, saate mudelit "koolitada" ja muudatused avaldada.</span><span class="sxs-lookup"><span data-stu-id="126d7-143">When you're ready, you can "train" the model and publish the changes.</span></span> <span data-ttu-id="126d7-144">Äsja koolitatud prognoosimismudel võetakse kasutusele lahenduses Dynamics 365 Finance prognooside loomiseks.</span><span class="sxs-lookup"><span data-stu-id="126d7-144">The newly trained model will automatically be picked up to generate predictions in Dynamics 365 Finance.</span></span>

## <a name="release-details"></a><span data-ttu-id="126d7-145">Väljastuse üksikasjad</span><span class="sxs-lookup"><span data-stu-id="126d7-145">Release details</span></span>

<span data-ttu-id="126d7-146">Finantsülevaadete avalik eelversioon on kasutuselevõtu proovimiseks saadaval Ameerika Ühendriikides, Euroopas ja Ühendkuningriigis.</span><span class="sxs-lookup"><span data-stu-id="126d7-146">Finance Insights public preview is available to try for deployments in the United States of America, Europe, and United Kingdom.</span></span> <span data-ttu-id="126d7-147">Microsoft lisab astmeliselt juurde täiendavate piirkondade tuge.</span><span class="sxs-lookup"><span data-stu-id="126d7-147">Microsoft is incrementally adding support for additional regions.</span></span>

<span data-ttu-id="126d7-148">Avaliku eelvaate funktsioone saab ja tuleb sisse lülitada ainult Järgu 2 liivakasti keskkondades.</span><span class="sxs-lookup"><span data-stu-id="126d7-148">Public preview features should be turned on only in Tier 2 sandbox environments.</span></span> <span data-ttu-id="126d7-149">Liivakasti keskkonnas loodud seadistust ja AI mudeleid ei pruugi saada migreerida töökeskkonda.</span><span class="sxs-lookup"><span data-stu-id="126d7-149">Setup and AI models that are created in a sandbox environment might not be migrated to the production environment.</span></span> <span data-ttu-id="126d7-150">Lisateavet leiate teemast [Microsoft Dynamics 365 eelversioonide täiendavad kasutustingimused](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="126d7-150">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
