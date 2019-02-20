---
title: Jaemüügikande süsteemsuskontroll
description: Selles teemas kirjeldatakse jaemüügikande süsteemsuskontrolli funktsiooni teenuses Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "302179"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="3ff6b-103">Jaemüügikande süsteemsuskontroll</span><span class="sxs-lookup"><span data-stu-id="3ff6b-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="3ff6b-104">Selles teemas kirjeldatakse jaemüügikande süsteemsuskontrolli funktsiooni, mis lasti välja teenuse Microsoft Dynamics 365 for Finance and Operations versioonis 8.1.3.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-104">This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="3ff6b-105">Süsteemsuskontroll tuvastab ja isoleerib vastuolulised kanded enne, kui väljavõtte sisestuse protsess need peale võtab.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="3ff6b-106">Retailis võib väljavõtte sisestamine nurjuda, kuna jaemüügikannete tabelites on vastuolulised andmed.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="3ff6b-107">Andmete probleemi võivad põhjustada ettenägematud probleemid kassarakenduses (POS) või kolmanda osapoole kassasüsteemidest valesti imporditud kanded.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-107">The data issue may be caused by by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="3ff6b-108">Need vastuolud võivad ilmuda näiteks järgmistel juhtudel.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-108">Examples of how these inconsistencies may appear include:</span></span> 

  - <span data-ttu-id="3ff6b-109">Päisetabelis olev kande kogusumma ei kattu kande ridade kogusummaga.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
  - <span data-ttu-id="3ff6b-110">Päisetabeli ridade arv ei kattu kandetabeli ridade arvuga.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
  - <span data-ttu-id="3ff6b-111">Päisetabeli maksud ei kattu ridade maksusummaga.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 
  
<span data-ttu-id="3ff6b-112">Kui väljavõtte sisestamise protsess laadib vastuolulised kanded, luuakse vastuolulised müügiarved ja maksetöölehed ning kogu väljavõtte sisestamise protsess nurjub.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="3ff6b-113">Sellises olekus väljavõtete taastamine hõlmab keerukaid andmeparandusi mitmes kandetabelis.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="3ff6b-114">Jaemüügikande süsteemsuskontroll takistab selliseid probleeme.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="3ff6b-115">Järgmine diagramm illustreerib kande süsteemsuskontrolliga sisestusprotsessi.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="3ff6b-116">![Väljavõtte sisestamise protsess jaemüügikande süsteemsuskontrolliga](./media/validchecker.png "Väljavõtte sisestamise protsess jaemüügikande süsteemsuskontrolliga")</span><span class="sxs-lookup"><span data-stu-id="3ff6b-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transsaction consistency checker")</span></span>

<span data-ttu-id="3ff6b-117">Pakktöötluse funktsioon **Kinnita kaupluse kanded** kontrollib jaemüügi kandetabelite järjepidevust järgmiste stsenaariumite suhtes.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="3ff6b-118">Kliendi konto: kontrollib, kas jaemüügi kandetabelites märgitud kliendi konto on peakontori kliendi koondandmetes olemas.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-118">Customer account - Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="3ff6b-119">Ridade arv: kontrollib, kas kande päsietabelis märgitud ridade arv kattub müügikande tabeli ridade arvuga.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-119">Line count - Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="3ff6b-120">Süsteemsuskontrolli seadistamine</span><span class="sxs-lookup"><span data-stu-id="3ff6b-120">Set up the consistency checker</span></span>
<span data-ttu-id="3ff6b-121">Seadistage pakktöötluse funktsiooni „Kontrolli kaupluse kandeid” regulaarne käitamine jaotises **Jaemüük \> Jaemüügi IT \> Kassa sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-121">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="3ff6b-122">Pakett-tööd saab ajastada kaupluse organisatsiooni hierarhia alusel, sarnaselt protsesside „Väljavõtte arvutamine partiina” ja „Väljavõtte sisestamine partiina” seadistamisega.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-122">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="3ff6b-123">Soovitame konfigureerida pakktöötluse nii, et seda käitataks mitu korda päevas, ja ajastada käitamise iga P-töö lõpus.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-123">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="3ff6b-124">Kontrollimisprotsessi tulemused</span><span class="sxs-lookup"><span data-stu-id="3ff6b-124">Results of validation process</span></span>
<span data-ttu-id="3ff6b-125">Pakktöötluse kontrolli tulemused märgistatakse sobivas jaemüügikandes.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-125">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="3ff6b-126">Jaemüügikande kirje väljal **Kinnitamise olek** on märge **Õnnestus** või **Tõrge** ning viimase kontrollimise kuupäev kuvatakse väljal **Viimase kinnitamise aeg**.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-126">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="3ff6b-127">Kontrollimistõrkega seotud täpsema tõrketeksti vaatamiseks valige asjakohane jaemüügikande kirje ja seejärel klõpsake nuppu **Valideerimistõrked**.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-127">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="3ff6b-128">Kandeid, mille kontroll nurjub või mis ei ole veel kontrollitud, ei lisata väljavõtetesse.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-128">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="3ff6b-129">Protsessi „Väljavõtte arvutamine” ajal teavitatakse kasutajaid, kui teatud kandeid ei saanud väljavõttesse kaasata.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-129">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="3ff6b-130">Ainus viis valideerimistõrke lahendamiseks on võtta ühendust Microsofti toega.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-130">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="3ff6b-131">Tulevases versioonis lisatakse funktsioonid, mis võimaldavad kasutajatel nurjunud kirjeid kasutajaliidese kaudu parandada.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-131">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="3ff6b-132">Samuti tulevad saadavale logimise ja auditeerimise funktsioonid, mis võimaldavad muudatuste ajalugu jälgida.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-132">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="3ff6b-133">Tulevases versioonis lisatakse täiendavad kinnitusreeglid, mis toetavad rohkem stsenaariume.</span><span class="sxs-lookup"><span data-stu-id="3ff6b-133">Additional validation rules to support more scenarios will be added in a future release.</span></span>
