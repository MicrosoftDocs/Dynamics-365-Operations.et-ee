---
title: Ida-Euroopa kannete vaatamine tasakaalustamisel
description: "Selles teemas käsitletakse lehe Kanded tasakaalustamisel teavet klientide ja hankijate kohta."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustVendTransPostingLog_RU
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 270544
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 00c7ae430cbcf92b211a3525ff8b41e042b033e4
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="view-transactions-on-settlement-for-eastern-europe"></a><span data-ttu-id="f6e60-103">Ida-Euroopa kannete vaatamine tasakaalustamisel</span><span class="sxs-lookup"><span data-stu-id="f6e60-103">View transactions on settlement for Eastern Europe</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f6e60-104">Selles teemas käsitletakse lehe Kanded tasakaalustamisel teavet klientide ja hankijate kohta.</span><span class="sxs-lookup"><span data-stu-id="f6e60-104">This topic provides information about the Transactions on settlement page for customers and vendors.</span></span>

<span data-ttu-id="f6e60-105">Kasutage lehte **Kanded tasakaalustamisel** teabe kuvamiseks kliendi või hankija keerukate tasakaalustuskannete kohta.</span><span class="sxs-lookup"><span data-stu-id="f6e60-105">Use the **Transactions on settlement** page to view information about complex settlement transactions for a customer or a vendor.</span></span> <span data-ttu-id="f6e60-106">See funktsioon on saadaval ainult juriidilistele isikutele esmase aadressiga Leedus, Lätis, Eestis, Tšehhi Vabariigis, Ungaris või Poolas.</span><span class="sxs-lookup"><span data-stu-id="f6e60-106">This feature is available only for legal entities that have their primary address in Lithuania, Latvia, Estonia, Czech Republic, Hungary, or Poland.</span></span> <span data-ttu-id="f6e60-107">Leiate lehe **Kanded tasakaalustamisel** järgmistest kohtadest:</span><span class="sxs-lookup"><span data-stu-id="f6e60-107">You can find the **Transactions on settlement** page at the following locations:</span></span>

-   <span data-ttu-id="f6e60-108">**Ostureskontro** &gt; **Hankijad** &gt; **Kõik hankijad**.</span><span class="sxs-lookup"><span data-stu-id="f6e60-108">**Accounts payable** &gt; **Vendors** &gt; **All vendors**.</span></span> <span data-ttu-id="f6e60-109">Klõpsake tegumiriba vahekaardil **Hankija** valikuid **Kanded** &gt; **Kanded**.</span><span class="sxs-lookup"><span data-stu-id="f6e60-109">On the Action Pane, on the **Vendor** tab, click **Transactions** &gt; **Transactions**.</span></span> <span data-ttu-id="f6e60-110">Valige lehelt **Hankija kanded** kanne ja klõpsake siis valikut **Kanded tasakaalustamisel**.</span><span class="sxs-lookup"><span data-stu-id="f6e60-110">On the **Vendor transactions** page, select a transaction, and then click **Transactions on settlement**.</span></span>
-   <span data-ttu-id="f6e60-111">**Müügireskontro** &gt; **Kliendid** &gt; **Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="f6e60-111">**Accounts receivable** &gt; **Customers** &gt; **All customers**.</span></span> <span data-ttu-id="f6e60-112">Klõpsake tegumiriba vahekaardil **Klient** valikut **Kanded**.</span><span class="sxs-lookup"><span data-stu-id="f6e60-112">On the Action Pane, on the **Customer** tab, click **Transactions**.</span></span> <span data-ttu-id="f6e60-113">Valige lehelt **Kliendi kanded** kanne ja klõpsake siis valikut **Kanded tasakaalustamisel**.</span><span class="sxs-lookup"><span data-stu-id="f6e60-113">On the **Customer transactions** page, select a transaction, and then click **Transactions on settlement**.</span></span>

<span data-ttu-id="f6e60-114">Hõivatakse tasakaalustamisega seotud andmed ja need saab kuvada lehel **Kanded tasakaalustamisel** kannete puhul, mis loodi järgmistes stsenaariumides.</span><span class="sxs-lookup"><span data-stu-id="f6e60-114">Settlement-related information is captured and can be shown on the **Transactions on settlement** page for transactions that were created in the following scenarios:</span></span>

-   <span data-ttu-id="f6e60-115">**Valuutakursi korrigeerimine** – arve ja makse tasakaalustamine loob realiseeritud või realiseerimata vahetuskursi erinevuse.</span><span class="sxs-lookup"><span data-stu-id="f6e60-115">**Exchange adjustment** – Settlement of an invoice and a payment generates a realized or unrealized exchange rate difference.</span></span>
-   <span data-ttu-id="f6e60-116">**Sisestusreeglite muutmine** – tasakaalustatakse kaks erinevate sisestusreeglitega kirjet, nt arve ja kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="f6e60-116">**Posting profile change** – Two entries, such as an invoice and a credit memo, that have different posting profiles are settled.</span></span>
-   <span data-ttu-id="f6e60-117">Ettemakse teisendatakse makseks või makse teisendatakse ettemakseks.</span><span class="sxs-lookup"><span data-stu-id="f6e60-117">A prepayment is converted to a payment, or a payment is converted to a prepayment.</span></span>
-   <span data-ttu-id="f6e60-118">**Skonto** – arve tasakaalustatakse maksega, millest on maha arvatud allahindluse summa.</span><span class="sxs-lookup"><span data-stu-id="f6e60-118">**Cash discount** – An invoice is settled with a payment that a discount amount has been deducted from.</span></span>
-   <span data-ttu-id="f6e60-119">**Sendierinevus** – arve tasakaalustatakse maksega, millel on arvest veidi erinev summa.</span><span class="sxs-lookup"><span data-stu-id="f6e60-119">**Penny difference** – An invoice is settled with a payment that has a slightly different amount than the invoice.</span></span>
-   <span data-ttu-id="f6e60-120">**Tingimusliku maksu sisestamine** – arve tasakaalustatakse maksega, millele on rakendatud tingimuslik maks.</span><span class="sxs-lookup"><span data-stu-id="f6e60-120">**Conditional tax posting** – An invoice is settled with a payment that conditional tax has been applied to.</span></span>
-   <span data-ttu-id="f6e60-121">**Ettevõtetevaheline tasakaalustamine** – kontsernisisest funktsiooni kasutatakse arve tasakaalustamiseks organisatsiooni maksega.</span><span class="sxs-lookup"><span data-stu-id="f6e60-121">**Cross-company settlement** – Intercompany functionality is used to settle an invoice with a payment from an organization.</span></span>





