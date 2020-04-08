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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5277081d9f7adcc43c30d30208d13c7e39d76118
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140371"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="b8453-103">Hankija arve kirjendamine arvete töölehele</span><span class="sxs-lookup"><span data-stu-id="b8453-103">Record a vendor invoice in the invoice journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8453-104">Selles tegevuse juhises näitlikustatakse, kuidas salvestada hankija arveid, mis ei ole seostatud ostutellimustega.</span><span class="sxs-lookup"><span data-stu-id="b8453-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="b8453-105">Selle arve tüübi näited sisaldavad varude või teenuste kulusid.</span><span class="sxs-lookup"><span data-stu-id="b8453-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="b8453-106">Salvestamisel kasutatakse demoettevõtte USMF-i.</span><span class="sxs-lookup"><span data-stu-id="b8453-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="b8453-107">Avage **Navigeerimispaan > Moodulid > Ostureskontro > Tööruumid > Müüja arve kanne**.</span><span class="sxs-lookup"><span data-stu-id="b8453-107">Go to **Navigation pane > Modules > Accounts payable > Workspaces > Vendor invoice entry**.</span></span>
2. <span data-ttu-id="b8453-108">Klõpsake **tegumiribal** valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b8453-108">On the **Action pane**, click **New invoice journal**.</span></span>
3. <span data-ttu-id="b8453-109">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b8453-109">Click **New**.</span></span>
4. <span data-ttu-id="b8453-110">Sisestage töölehe nimi väljale **Nimi** või klõpsake otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b8453-110">In the **Name** field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="b8453-111">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="b8453-111">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="b8453-112">Klõpsake **Toimingupaanil** valikut **Read**.</span><span class="sxs-lookup"><span data-stu-id="b8453-112">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="b8453-113">Sisestage sisestuskuupäev, mis ühtlasi värskendab pearaamatut, väljale **Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="b8453-113">In the **Date** field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="b8453-114">Täpsustage **Hankija kontot** väljal **Konto**.</span><span class="sxs-lookup"><span data-stu-id="b8453-114">In the **Account** field, specify the **Vendor account**.</span></span>
8. <span data-ttu-id="b8453-115">Sisestage arve number väljale **Arve**.</span><span class="sxs-lookup"><span data-stu-id="b8453-115">In the **Invoice** field, enter the invoice number.</span></span>
9. <span data-ttu-id="b8453-116">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="b8453-116">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="b8453-117">Sisestage number väljale **Kreedit**.</span><span class="sxs-lookup"><span data-stu-id="b8453-117">In the **Credit** field, enter a number.</span></span>
11. <span data-ttu-id="b8453-118">Sisestage kontonumber väljale **Vastaskonto** või klõpsake otsingu avamiseks ripploendi nuppu</span><span class="sxs-lookup"><span data-stu-id="b8453-118">In the **Offset account** field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="b8453-119">**Käibemaksugrupp** pärineb vaikimisi hankija kontolt.</span><span class="sxs-lookup"><span data-stu-id="b8453-119">The **Sales tax group** will be default from the vendor account.</span></span>  
    * <span data-ttu-id="b8453-120">**Kauba käibemaksugrupp** pärineb vaikimisi väljal **Vastaskonto** määratud põhikontolt.</span><span class="sxs-lookup"><span data-stu-id="b8453-120">The **Item sales tax group** will be default from the main account specified in the **Offset account** field.</span></span>  
    * <span data-ttu-id="b8453-121">**Tähtaeg** arvutatakse maksetingimuste alusel.</span><span class="sxs-lookup"><span data-stu-id="b8453-121">The **Due date** will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="b8453-122">**Sularaha allahindlus** vaikimisi kehtib müüjakontolt.</span><span class="sxs-lookup"><span data-stu-id="b8453-122">The **Cash discount** will default from the Vendor account.</span></span>  
12. <span data-ttu-id="b8453-123">Klõpsake käsku **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="b8453-123">Click **Post**.</span></span>
13. <span data-ttu-id="b8453-124">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b8453-124">Close the page.</span></span>

