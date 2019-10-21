---
title: Hankijamaksete loomine ja eksportimine ISO20022 maksevormingu abil
description: See protseduur näitab, kuidas luua makseridu hankija makse töölehel ja kuidas luua hankija maksefaili, kasutades ISO2022 kreeditülekande näidet.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b70ad94014587ba8e55735192dbe0ab2e4adf4ee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185815"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="a4459-103">Hankijamaksete loomine ja eksportimine ISO20022 maksevormingu abil</span><span class="sxs-lookup"><span data-stu-id="a4459-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a4459-104">See teema selgitab, kuidas luua makseridu hankija makse töölehel ja kuidas luua hankija maksefaili, kasutades ISO2022 kreeditülekande näidet.</span><span class="sxs-lookup"><span data-stu-id="a4459-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="a4459-105">See on viies viiest protseduurist, mis illustreerib hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="a4459-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="a4459-106">Kasutage selle näite lõpuleviimiseks DEMF-i demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="a4459-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="a4459-107">Näide</span><span class="sxs-lookup"><span data-stu-id="a4459-107">Example</span></span>

1.  <span data-ttu-id="a4459-108">Minge jaotisse **Ostureskontro > Maksed > Makse tööleht**.</span><span class="sxs-lookup"><span data-stu-id="a4459-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.  <span data-ttu-id="a4459-109">Klõpsake **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a4459-109">Click **New**.</span></span>
3.  <span data-ttu-id="a4459-110">Sisestage või valige väärtus väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="a4459-110">In the **Name** field, enter or select a value.</span></span>
4.  <span data-ttu-id="a4459-111">Klõpsake valikuid **Read > Maksesoovitus > Loo maksesoovitus**.</span><span class="sxs-lookup"><span data-stu-id="a4459-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.  <span data-ttu-id="a4459-112">Jaotise kaasamiseks laiendage valikut **Kirjed**.</span><span class="sxs-lookup"><span data-stu-id="a4459-112">Expand the **Records to include** section.</span></span>
6.  <span data-ttu-id="a4459-113">Klõpsake käsku **Filtreeri**.</span><span class="sxs-lookup"><span data-stu-id="a4459-113">Click **Filter**.</span></span>
7.  <span data-ttu-id="a4459-114">Valige loendist rida **tabelile Hankijad** ja **väljale Hankija konto**.</span><span class="sxs-lookup"><span data-stu-id="a4459-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.  <span data-ttu-id="a4459-115">Sisestage või valige väärtus väljal **Kriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="a4459-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="a4459-116">Saate rakendada mis tahes kriteeriume makstavate hankija kannete valimiseks, selles näites kasutage hankija kontot DE-001.</span><span class="sxs-lookup"><span data-stu-id="a4459-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12. <span data-ttu-id="a4459-117">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4459-117">Click **OK**.</span></span>
13. <span data-ttu-id="a4459-118">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4459-118">Click **OK**.</span></span>
14. <span data-ttu-id="a4459-119">Klõpsake suvandit **Maksete loomine**.</span><span class="sxs-lookup"><span data-stu-id="a4459-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="a4459-120">Looge ISO20022 maksefail.</span><span class="sxs-lookup"><span data-stu-id="a4459-120">Generate an ISO20022 payment file.</span></span>
    1.  <span data-ttu-id="a4459-121">Klõpsake suvandit **Loo maksed**.</span><span class="sxs-lookup"><span data-stu-id="a4459-121">Click **Generate payments**.</span></span>
    2.  <span data-ttu-id="a4459-122">Valige või sisestage väärtus väljal **Makseviis**.</span><span class="sxs-lookup"><span data-stu-id="a4459-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.  <span data-ttu-id="a4459-123">Sisestage väärtus väljale **Faili nimi**.</span><span class="sxs-lookup"><span data-stu-id="a4459-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="a4459-124">Selles näites on loodud fail euromakse tõttu SEPA-ga ühilduv.</span><span class="sxs-lookup"><span data-stu-id="a4459-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="a4459-125">Maksete loomiseks muudes valuutades saab kasutada ni ISO20022 krediidiedastust kui ka muid hankija maksevorminguid.</span><span class="sxs-lookup"><span data-stu-id="a4459-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.  <span data-ttu-id="a4459-126">Sisestage või valige väärtus väljal **Pangakonto**.</span><span class="sxs-lookup"><span data-stu-id="a4459-126">In the **Bank account** field, enter or select a value.</span></span>

