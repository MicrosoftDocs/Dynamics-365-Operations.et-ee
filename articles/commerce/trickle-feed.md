---
title: Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks
description: Selles teemas kirjeldatakse vähehaaval toimuvat tellimuse loomist kaupluse kannete jaoks Microsoft Dynamics 365 Commerce'is.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0fdb1f636183e8365729ab8947a50614a77eaeac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211041"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="af724-103">Vähehaaval toimuv tellimuse loomine kaupluse kannete jaoks</span><span class="sxs-lookup"><span data-stu-id="af724-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="af724-104">Dynamics 365 Retaili versioonis 10.0.4 ja varasemates versioonides on väljavõtte sisestamine päevalõpu toiming ja kõik kanded sisestatakse raamatutesse päeva lõpus.</span><span class="sxs-lookup"><span data-stu-id="af724-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="af724-105">Mahukaid kandeid tuleb seejärel töödelda piiratud ajavahemikus, mis mõnikord põhjustab suurt koormust, lukustusi ja väljavõtte sisestamise tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="af724-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="af724-106">Lisaks ei saa jaemüüjad tuvastada päeva jooksul oma raamatutes tulu ega makseid.</span><span class="sxs-lookup"><span data-stu-id="af724-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="af724-107">Retaili versioonis 10.0.5 kasutusele võetud vähehaaval toimuva tellimuse loomisel töödeldakse kandeid kogu päeva jooksul ja päeva lõpus töödeldakse ainult maksevahendite finantsvastavusseviimist ja muid kassahalduse kandeid.</span><span class="sxs-lookup"><span data-stu-id="af724-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="af724-108">See funktsioon jaotab müügitellimuste, arvete ja maksete loomise koormuse päeva peale ära, pakkudes suuremat jõudlust ning võimaldades tulu ja makseid kajastada raamatutes peaaegu reaalajas.</span><span class="sxs-lookup"><span data-stu-id="af724-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="af724-109">Vähehaaval toimuva sisestamise kasutamine</span><span class="sxs-lookup"><span data-stu-id="af724-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="af724-110">Jaemüügikannete vähehaaval toimuva sisestamise lubamiseks lubage funktsioonihalduse abil funktsioon **Retaili väljavõtted – vähehaaval toimuv**.</span><span class="sxs-lookup"><span data-stu-id="af724-110">To enable trickle feed-based posting of retail transactions, enable the feature named **Retail statements - Trickle feed** using Feature management.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="af724-111">Enne funktsiooni lubamist veenduge, et ükski väljavõte pole sisestamise ootel.</span><span class="sxs-lookup"><span data-stu-id="af724-111">Before you enable the feature, make sure that no pending statements are waiting to be posted.</span></span>

2. <span data-ttu-id="af724-112">Praegune väljavõttedokument tükeldatakse kaheks tüübiks: kandeväljavõte ja finantsaruanne.</span><span class="sxs-lookup"><span data-stu-id="af724-112">The current statement document will be split into two types: transactional statement and financial statement.</span></span>

      - <span data-ttu-id="af724-113">Kandeväljavõte kogub kõik sisestamata ja kinnitatud kanded ning loob müügitellimused, müügiarved, maksete ja allahindluste töölehed ning tulu-/kulukanded teie konfigureeritaval sagedusel.</span><span class="sxs-lookup"><span data-stu-id="af724-113">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="af724-114">Peaksite selle protsessi konfigureerima nii, et seda käitataks suurel sagedusel, et dokumendid loodaks siis, kui kanded laaditakse peakontori P-töö kaudu.</span><span class="sxs-lookup"><span data-stu-id="af724-114">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="af724-115">Selle kandeväljavõtte korral, mis juba loob müügitellimusi ja müügiarveid, pole tegelikult vaja konfigureerida pakett-tööd **Sisesta varud**.</span><span class="sxs-lookup"><span data-stu-id="af724-115">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="af724-116">Saate oma võimalike ärinõuete täitmiseks seda siiski kasutada.</span><span class="sxs-lookup"><span data-stu-id="af724-116">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="af724-117">Finantsaruanne on mõeldud loomiseks päeva lõpus ja see toetab ainult sulgemisviisi **Vahetus**.</span><span class="sxs-lookup"><span data-stu-id="af724-117">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="af724-118">See aruanne piiratakse finantsvastavusseviimisega ja see loob töölehed ainult loendatud summa ja kandesumma vaheliste erinevuste summade jaoks eri maksevahendite puhul, samuti loob töölehed muude sularahahalduse kannete jaoks.</span><span class="sxs-lookup"><span data-stu-id="af724-118">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

3. <span data-ttu-id="af724-119">Kandeväljavõtte arvutamiseks avage **Retail ja Commerce > Retaili ja Commerce'i IT > Kassa sisestamine > Kandeväljavõtete arvutamine partiina**.</span><span class="sxs-lookup"><span data-stu-id="af724-119">To calculate the transactional statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="af724-120">Kandeväljavõtete sisestamiseks partiina valige **Retail ja Commerce > Retaili ja Commerce'i IT > Kassa sisestamine > Kandeväljavõtete sisestamine partiina**.</span><span class="sxs-lookup"><span data-stu-id="af724-120">To post the transactional statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

4. <span data-ttu-id="af724-121">Finantsaruande arvutamiseks valige **Retail ja Commerce > Retaili ja Commerce'i IT > Kassa sisestamine > Finantsaruande arvutamine partiina**.</span><span class="sxs-lookup"><span data-stu-id="af724-121">To calculate the financial statement, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="af724-122">Finantsaruannete partiina sisestamiseks valige **Retail ja Commerce > Retaili ja Commerce'i IT > Kassa sisestamine > Finantsaruande sisestamine partiina**.</span><span class="sxs-lookup"><span data-stu-id="af724-122">To post the financial statements in batch, go to **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="af724-123">Menüükäsud **Retail ja Commerce > Retaili ja Commerce'i IT > Kassa sisestamine > Väljavõtete arvutamine partiina** ja **Retail ja Commerce > Retaili ja Commerce'i IT > Kassa sisestamine > Väljavõtete sisestamine partiina** eemaldatakse selle uue funktsiooniga.</span><span class="sxs-lookup"><span data-stu-id="af724-123">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="af724-124">Lisaks saab kandeväljavõtte ja finantsaruande tüüpe luua käsitsi.</span><span class="sxs-lookup"><span data-stu-id="af724-124">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="af724-125">Avage **Retail ja Commerce > Kanalid > Kauplused** ja klõpsake valikut **Väljavõtted**.</span><span class="sxs-lookup"><span data-stu-id="af724-125">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="af724-126">Klõpsake valikut **Uus** ja valige, millist tüüpi väljavõtte soovite luua.</span><span class="sxs-lookup"><span data-stu-id="af724-126">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="af724-127">Lehel **Väljavõtted** olevad väljad ja lehe jaotises **Väljavõttegrupp** olevad tegevused kuvavad valitud väljavõttetüübi põhjal asjakohased andmed ja tegevused.</span><span class="sxs-lookup"><span data-stu-id="af724-127">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]