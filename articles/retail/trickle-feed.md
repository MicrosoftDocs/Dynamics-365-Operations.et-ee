---
title: Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks
description: Selles teemas kirjeldatakse vähehaaval toimuvat tellimuse loomist kaupluse kannete jaoks Microsoft Dynamics 365 Retailis.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: deb8399aa401af16b6fe123a433eb21864e178c6
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693085"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a><span data-ttu-id="828a2-103">Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks (avalik eelvaade)</span><span class="sxs-lookup"><span data-stu-id="828a2-103">Trickle feed-based order creation for retail store transactions (Public preview)</span></span>

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="828a2-104">Dynamics 365 Retaili versioonis 10.0.4 ja varasemates versioonides on jaemüügiväljavõtte sisestamine päevalõpu toiming ja kõik kanded sisestatakse raamatutesse päeva lõpus.</span><span class="sxs-lookup"><span data-stu-id="828a2-104">In Dynamics 365 Retail versions 10.0.4 and earlier, retail statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="828a2-105">Mahukaid kandeid tuleb seejärel töödelda piiratud ajavahemikus, mis mõnikord põhjustab suurt koormust, lukustusi ja väljavõtte sisestamise tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="828a2-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="828a2-106">Lisaks ei saa jaemüüjad tuvastada päeva jooksul oma raamatutes tulu ega makseid.</span><span class="sxs-lookup"><span data-stu-id="828a2-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="828a2-107">Retaili versioonis 10.0.5 kasutusele võetud vähehaaval toimuv tellimuse loomise avalikus eelvaates töödeldakse kandeid kogu päeva jooksul ja päeva lõpus töödeldakse ainult maksevahendite finantsvastavusseviimist ja muid kassahalduse kandeid.</span><span class="sxs-lookup"><span data-stu-id="828a2-107">With the public preview of trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="828a2-108">See funktsioon jaotab müügitellimuste, arvete ja maksete loomise koormuse päeva peale ära, pakkudes suuremat jõudlust ning võimaldades tulu ja makseid kajastada raamatutes peaaegu reaalajas.</span><span class="sxs-lookup"><span data-stu-id="828a2-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="828a2-109">Vähehaaval toimuva sisestamise kasutamine</span><span class="sxs-lookup"><span data-stu-id="828a2-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="828a2-110">Jaemüügikannete vähehaaval toimuva sisestamise lubamiseks avage **Süsteemihaldus > Häälestamine > Litsentsi konfiguratsioon** ja keelake võti **Jaemüügi väljavõtted**.</span><span class="sxs-lookup"><span data-stu-id="828a2-110">To enable trickle feed-based posting of retail transactions, go to **System administration > Set up > License configuration** and disable the the **Retail statements** key.</span></span>

2. <span data-ttu-id="828a2-111">Samal lehel lubage litsentsivõti **Jaemüügi väljavõtted (vähehaaval toimuv) – eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="828a2-111">On the same page, enable the **Retail statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="828a2-112">Kui lubate selle võtme, veenduge, et ükski väljavõte pole sisestamise ootel.</span><span class="sxs-lookup"><span data-stu-id="828a2-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

> [!Important]
> <span data-ttu-id="828a2-113">Enne kui lubate litsentsivõtme **Jaemüügi väljavõtted (vähehaaval toimuv) – eelvaade**, veenduge, et ükski väljavõte poleks sisestamise ootel.</span><span class="sxs-lookup"><span data-stu-id="828a2-113">Before you enable the **Retail statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="828a2-114">Praegune väljavõttedokument tükeldatakse kaheks eri tüübiks: kandeväljavõte ja finantsaruanne.</span><span class="sxs-lookup"><span data-stu-id="828a2-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="828a2-115">Kandeväljavõte kogub kõik sisestamata ja kinnitatud jaemüügikanded ning loob müügitellimused, müügiarved, maksete ja allahindluste töölehed ning tulu-/kulukanded teie konfigureeritaval sagedusel.</span><span class="sxs-lookup"><span data-stu-id="828a2-115">The transactional statement will pick up all unposted and validated retail transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="828a2-116">Peaksite selle protsessi konfigureerima nii, et seda käitataks suurel sagedusel, et dokumendid loodaks siis, kui jaemüügikanded laaditakse programmi Retail Headquarters P-töö kaudu.</span><span class="sxs-lookup"><span data-stu-id="828a2-116">You should configure this process to run at a high frequency so that documents are created when the retail transactions are uploaded into Retail Headquarters through the P-job.</span></span> <span data-ttu-id="828a2-117">Selle kandeväljavõtte korral, mis juba loob müügitellimusi ja müügiarveid, pole tegelikult vaja konfigureerida pakett-tööd **Sisesta varud**.</span><span class="sxs-lookup"><span data-stu-id="828a2-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="828a2-118">Saate oma võimalike ärinõuete täitmiseks seda siiski kasutada.</span><span class="sxs-lookup"><span data-stu-id="828a2-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="828a2-119">Finantsaruanne on mõeldud loomiseks päeva lõpus ja see toetab ainult sulgemisviisi **Vahetus**.</span><span class="sxs-lookup"><span data-stu-id="828a2-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="828a2-120">See aruanne piiratakse finantsvastavusseviimisega ja see loob töölehed ainult loendatud summa ja kandesumma vaheliste erinevuste summade jaoks eri maksevahendite puhul, samuti loob töölehed muude kassahalduse kannete jaoks.</span><span class="sxs-lookup"><span data-stu-id="828a2-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="828a2-121">Kandeväljavõtte arvutamiseks klõpsake valikuid **Jaemüük > Jaemüügi IT > Kassa sisestamine > Kandeväljavõtete arvutamine partiina**.</span><span class="sxs-lookup"><span data-stu-id="828a2-121">To calculate the transactional statement, click **Retail > Retail IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="828a2-122">Kandeväljavõtete sisestamiseks partiina klõpsake valikuid **Jaemüük > Jaemüügi IT > Kassa sisestamine > Kandeväljavõtete sisestamine partiina**.</span><span class="sxs-lookup"><span data-stu-id="828a2-122">To post the transactional statement statements in batch, click **Retail > Retail IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="828a2-123">Finantsaruande arvutamiseks klõpsake valikuid **Jaemüük > Jaemüügi IT > Kassa sisestamine > Finantsaruannete arvutamine partiina**.</span><span class="sxs-lookup"><span data-stu-id="828a2-123">To calculate the financial statement, click **Retail > Retail IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="828a2-124">Finantsaruannete sisestamiseks partiina klõpsake valikuid **Jaemüük > Jaemüügi IT > Kassa sisestamine > Finantsaruannete sisestamine partiina**.</span><span class="sxs-lookup"><span data-stu-id="828a2-124">To post the financial statements in batch, click **Retail > Retail IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="828a2-125">Menüükäsud **Jaemüük > Jaemüügi IT > Kassa sisestamine > Väljavõtete arvutamine partiina** ja **Jaemüük > Jaemüügi IT > Kassa sisestamine > Väljavõtete sisestamine partiina** eemaldatakse selle uue funktsiooniga.</span><span class="sxs-lookup"><span data-stu-id="828a2-125">The menu items **Retail > Retail IT > POS Posting > Calculate statements in batch** and **Retail > Retail IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="828a2-126">Lisaks saab kandeväljavõtte ja finantsaruande tüüpe luua käsitsi.</span><span class="sxs-lookup"><span data-stu-id="828a2-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="828a2-127">Avage **Jaemüük > Kanalid > Kauplused** ja klõpsake valikut **Jaemüügi väljavõtted**.</span><span class="sxs-lookup"><span data-stu-id="828a2-127">Go to **Retail > Channels > Retail stores** and click **Retail statements**.</span></span> <span data-ttu-id="828a2-128">Klõpsake valikut **Uus** ja valige, millist tüüpi väljavõtte soovite luua.</span><span class="sxs-lookup"><span data-stu-id="828a2-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="828a2-129">Lehel **Jaemüügi väljavõtted** olevad väljad ja lehe jaotises **Väljavõttegrupp** olevad tegevused kuvavad valitud väljavõttetüübi põhjal asjakohased andmed ja tegevused.</span><span class="sxs-lookup"><span data-stu-id="828a2-129">Fields on the **Retail statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
