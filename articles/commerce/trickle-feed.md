---
title: Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks
description: Selles teemas kirjeldatakse vähehaaval toimuvat tellimuse loomist kaupluse kannete jaoks Microsoft Dynamics 365 Commerceis.
author: josaw1
manager: AnnBe
ms.date: 06/08/2020
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
ms.openlocfilehash: 6e097ead7cacb3f71452323656546a4be661457f
ms.sourcegitcommit: 7061a93f9f2b54aec4bc4bf0cc92691e86d383a6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/20/2020
ms.locfileid: "3710279"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="62f4a-103">Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks</span><span class="sxs-lookup"><span data-stu-id="62f4a-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="62f4a-104">Dynamics 365 Retaili versioonis 10.0.4 ja varasemates versioonides on väljavõtte sisestamine päevalõpu toiming ja kõik kanded sisestatakse raamatutesse päeva lõpus.</span><span class="sxs-lookup"><span data-stu-id="62f4a-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="62f4a-105">Mahukaid kandeid tuleb seejärel töödelda piiratud ajavahemikus, mis mõnikord põhjustab suurt koormust, lukustusi ja väljavõtte sisestamise tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="62f4a-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="62f4a-106">Lisaks ei saa jaemüüjad tuvastada päeva jooksul oma raamatutes tulu ega makseid.</span><span class="sxs-lookup"><span data-stu-id="62f4a-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="62f4a-107">Retaili versioonis 10.0.5 kasutusele võetud vähehaaval toimuva tellimuse loomisel töödeldakse kandeid kogu päeva jooksul ja päeva lõpus töödeldakse ainult maksevahendite finantsvastavusseviimist ja muid kassahalduse kandeid.</span><span class="sxs-lookup"><span data-stu-id="62f4a-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="62f4a-108">See funktsioon jaotab müügitellimuste, arvete ja maksete loomise koormuse päeva peale ära, pakkudes suuremat jõudlust ning võimaldades tulu ja makseid kajastada raamatutes peaaegu reaalajas.</span><span class="sxs-lookup"><span data-stu-id="62f4a-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="62f4a-109">Vähehaaval toimuva sisestamise kasutamine</span><span class="sxs-lookup"><span data-stu-id="62f4a-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="62f4a-110">Kannete vähehaaval toimuva sisestamise lubamiseks avage **Süsteemihaldus > Häälestamine > Litsentsi konfiguratsioon** ja keelake võti **Väljavõtted**.</span><span class="sxs-lookup"><span data-stu-id="62f4a-110">To enable trickle feed-based posting of transactions, go to **System administration > Set up > License configuration** and disable the the **Statements** key.</span></span>

2. <span data-ttu-id="62f4a-111">Samal lehel lubage litsentsivõti **Väljavõtted (vähehaaval toimuv) – eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="62f4a-111">On the same page, enable the **Statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="62f4a-112">Kui lubate selle võtme, veenduge, et ükski väljavõte pole sisestamise ootel.</span><span class="sxs-lookup"><span data-stu-id="62f4a-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

    > [!Important]
    > <span data-ttu-id="62f4a-113">Enne kui lubate litsentsivõtme **Väljavõtted (vähehaaval toimuv) – eelvaade**, veenduge, et ükski väljavõte poleks sisestamise ootel.</span><span class="sxs-lookup"><span data-stu-id="62f4a-113">Before you enable the **Statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="62f4a-114">Praegune väljavõttedokument tükeldatakse kaheks eri tüübiks: kandeväljavõte ja finantsaruanne.</span><span class="sxs-lookup"><span data-stu-id="62f4a-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="62f4a-115">Kandeväljavõte kogub kõik sisestamata ja kinnitatud kanded ning loob müügitellimused, müügiarved, maksete ja allahindluste töölehed ning tulu-/kulukanded teie konfigureeritaval sagedusel.</span><span class="sxs-lookup"><span data-stu-id="62f4a-115">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="62f4a-116">Peaksite selle protsessi konfigureerima nii, et seda käitataks suurel sagedusel, et dokumendid loodaks siis, kui kanded laaditakse peakontori P-töö kaudu.</span><span class="sxs-lookup"><span data-stu-id="62f4a-116">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="62f4a-117">Selle kandeväljavõtte korral, mis juba loob müügitellimusi ja müügiarveid, pole tegelikult vaja konfigureerida pakett-tööd **Sisesta varud**.</span><span class="sxs-lookup"><span data-stu-id="62f4a-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="62f4a-118">Saate oma võimalike ärinõuete täitmiseks seda siiski kasutada.</span><span class="sxs-lookup"><span data-stu-id="62f4a-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="62f4a-119">Finantsaruanne on mõeldud loomiseks päeva lõpus ja see toetab ainult sulgemisviisi **Vahetus**.</span><span class="sxs-lookup"><span data-stu-id="62f4a-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="62f4a-120">See aruanne piiratakse finantsvastavusseviimisega ja see loob töölehed ainult loendatud summa ja kandesumma vaheliste erinevuste summade jaoks eri maksevahendite puhul, samuti loob töölehed muude sularahahalduse kannete jaoks.</span><span class="sxs-lookup"><span data-stu-id="62f4a-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="62f4a-121">Kandeväljavõtte arvutamiseks klõpsake valikuid **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT > Kassa sisestamine > Kandeväljavõtete arvutamine partiina**.</span><span class="sxs-lookup"><span data-stu-id="62f4a-121">To calculate the transactional statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="62f4a-122">Kandeväljavõtete sisestamiseks partiina klõpsake valikuid **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT > Kassa sisestamine > Kandeväljavõtete sisestamine partiina**.</span><span class="sxs-lookup"><span data-stu-id="62f4a-122">To post the transactional statement statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="62f4a-123">Finantsaruande arvutamiseks klõpsake valikuid **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT > Kassa sisestamine > Finantsaruande arvutamine partiina**.</span><span class="sxs-lookup"><span data-stu-id="62f4a-123">To calculate the financial statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="62f4a-124">Finantsaruannete partiina sisestamiseks klõpsake valikuid **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT > Kassa sisestamine > Finantsaruande sisestamine partiina**.</span><span class="sxs-lookup"><span data-stu-id="62f4a-124">To post the financial statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="62f4a-125">Menüükäsud **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT > Kassa sisestamine > Väljavõtete arvutamine partiina** ja **Jaemüük ja kaubandus > Jaemüügi ja kaubanduse IT > Kassa sisestamine > Väljavõtete sisestamine partiina** eemaldatakse selle uue funktsiooniga.</span><span class="sxs-lookup"><span data-stu-id="62f4a-125">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="62f4a-126">Lisaks saab kandeväljavõtte ja finantsaruande tüüpe luua käsitsi.</span><span class="sxs-lookup"><span data-stu-id="62f4a-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="62f4a-127">Avage **Jaemüük ja kaubandus > Kanalid > Kauplused** ja klõpsake valikut **Väljavõtted**.</span><span class="sxs-lookup"><span data-stu-id="62f4a-127">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="62f4a-128">Klõpsake valikut **Uus** ja valige, millist tüüpi väljavõtte soovite luua.</span><span class="sxs-lookup"><span data-stu-id="62f4a-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="62f4a-129">Lehel **Väljavõtted** olevad väljad ja lehe jaotises **Väljavõttegrupp** olevad tegevused kuvavad valitud väljavõttetüübi põhjal asjakohased andmed ja tegevused.</span><span class="sxs-lookup"><span data-stu-id="62f4a-129">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
