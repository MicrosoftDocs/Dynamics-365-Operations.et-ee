---
title: Hankija arve kirjendamine arvete töölehele
description: Selles tegevuse juhises näitlikustatakse, kuidas salvestada hankija arveid, mis ei ole seostatud ostutellimustega.
author: abruer
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a60a5959046ca9e953bac80aaeb382d07a267643
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227132"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="c2839-103">Hankija arve kirjendamine arvete töölehele</span><span class="sxs-lookup"><span data-stu-id="c2839-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c2839-104">Selles tegevuse juhises näitlikustatakse, kuidas salvestada hankija arveid, mis ei ole seostatud ostutellimustega.</span><span class="sxs-lookup"><span data-stu-id="c2839-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="c2839-105">Selle arve tüübi näited sisaldavad varude või teenuste kulusid.</span><span class="sxs-lookup"><span data-stu-id="c2839-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="c2839-106">Salvestamisel kasutatakse demoettevõtte USMF-i.</span><span class="sxs-lookup"><span data-stu-id="c2839-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="c2839-107">Avage **Navigeerimispaan > Moodulid > Ostureskontro > Tööruumid > Müüja arve kanne**.</span><span class="sxs-lookup"><span data-stu-id="c2839-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="c2839-108">Klõpsake **tegumiribal** valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c2839-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="c2839-109">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c2839-109">Click **New**.</span></span>
4. <span data-ttu-id="c2839-110">Sisestage töölehe nimi väljale **Nimi** või klõpsake otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c2839-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="c2839-111">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="c2839-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="c2839-112">Klõpsake **Toimingupaanil** valikut **Read**.</span><span class="sxs-lookup"><span data-stu-id="c2839-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="c2839-113">Sisestage sisestuskuupäev, mis ühtlasi värskendab pearaamatut, väljale **Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="c2839-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="c2839-114">Täpsustage **Hankija kontot** väljal **Konto**.</span><span class="sxs-lookup"><span data-stu-id="c2839-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="c2839-115">Sisestage arve number väljale **Arve**.</span><span class="sxs-lookup"><span data-stu-id="c2839-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="c2839-116">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="c2839-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="c2839-117">Sisestage number väljale **Kreedit**.</span><span class="sxs-lookup"><span data-stu-id="c2839-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="c2839-118">Sisestage kontonumber väljale **Vastaskonto** või klõpsake otsingu avamiseks ripploendi nuppu</span><span class="sxs-lookup"><span data-stu-id="c2839-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="c2839-119">**Käibemaksugrupp** pärineb vaikimisi hankija kontolt.</span><span class="sxs-lookup"><span data-stu-id="c2839-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="c2839-120">**Kauba käibemaksugrupp** pärineb vaikimisi väljal **Vastaskonto** määratud põhikontolt.</span><span class="sxs-lookup"><span data-stu-id="c2839-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="c2839-121">**Tähtaeg** arvutatakse maksetingimuste alusel.</span><span class="sxs-lookup"><span data-stu-id="c2839-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="c2839-122">**Sularaha allahindlus** vaikimisi kehtib müüjakontolt.</span><span class="sxs-lookup"><span data-stu-id="c2839-122">The **Cash discount** will default from the Vendor account.</span></span>
12. <span data-ttu-id="c2839-123">Kui olete hankija arve töölehe töövoo lubanud, klõpsake valikul **Töövoog > Esita**.</span><span class="sxs-lookup"><span data-stu-id="c2839-123">If you have enabled Vendor invoice journal workflow, click **Workflow > Submit**.</span></span>
    * <span data-ttu-id="c2839-124">Kui teie esildis on kinnitatud, edastatakse kuupäev järgmise avatud perioodi esimesele päevale, kui kande sisestuskuupäev jääb perioodi, mis on ootel või pearaamatu sisestusteks suletud.</span><span class="sxs-lookup"><span data-stu-id="c2839-124">When your submission is approved, the date will be advanced to the first day of the next open period, if the transaction posting date falls within a period that is On hold or Closed for ledger posting.</span></span>
12. <span data-ttu-id="c2839-125">Klõpsake käsku **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="c2839-125">Click **Post**.</span></span>
13. <span data-ttu-id="c2839-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c2839-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]