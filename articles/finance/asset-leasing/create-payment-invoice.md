---
title: Maksearvete loomine
description: Selles teemas kirjeldatakse igakuiste rendiarvete loomist. Saate luua arved üksikutele rendikirjetele või saate kasutada partiina töötlemist, et luua need mitmele rendikirjele.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 303fb0e70530fdc29cb129736b01c0e0e8d02075
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969574"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="5531a-104">Maksearvete loomine</span><span class="sxs-lookup"><span data-stu-id="5531a-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5531a-105">Saate luua igakuised arved üksikutele rendikirjetele või saate kasutada partiina töötlemist, et luua need mitmele rendikirjele.</span><span class="sxs-lookup"><span data-stu-id="5531a-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="5531a-106">Järgmine toiming näitab, kuidas luua individuaalse rendimakse kanne, kui parameeter **Hankijale tasumine** on lehel **Rendi raamatu häälestus** on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="5531a-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="5531a-107">Valige lehel **Rendi kokkuvõte** rendikirje ja valige seejärel **Raamatud \> Maksegraafik**.</span><span class="sxs-lookup"><span data-stu-id="5531a-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="5531a-108">Valige tehtav makse ja valige seejärel käsk **Loo tööleht**.</span><span class="sxs-lookup"><span data-stu-id="5531a-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="5531a-109">Kuvatakse teade sõnumiga, et valitud makse suhtes loodi tööleht.</span><span class="sxs-lookup"><span data-stu-id="5531a-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="5531a-110">Valige **Arve töölehed** ja valige seejärel arve, mis tuleb tasuda.</span><span class="sxs-lookup"><span data-stu-id="5531a-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="5531a-111">Vahekaardil **Read** vaadake läbi töölehe kirje, enne kui selle pearaamatusse sisestate.</span><span class="sxs-lookup"><span data-stu-id="5531a-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5531a-112">Vaikimisi kasutavad loodavad hankija arveread hankija sisestamise profiili lehelt **Ostureskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="5531a-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="5531a-113">Valige õige tööleht ja valige seejärel arve, mis tuleb tasuda.</span><span class="sxs-lookup"><span data-stu-id="5531a-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="5531a-114">Selle näite puhul on rendi raamatu parameeter **Hankijale tasumine** sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="5531a-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="5531a-115">Seega on arve arve töölehel.</span><span class="sxs-lookup"><span data-stu-id="5531a-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="5531a-116">Jaotises **Ülevaade** kuvatakse töölehe sisestuse kokkuvõte ja jaotises **Read** kuvatakse tegelike töölehe ridade üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="5531a-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5531a-117">Kui parameeter **Hankijale tasumine** on välja lülitatud, loetletakse makse töölehe kanded rendi raamatu lehel **Vara rentimine** ja süsteem loob arve asemel vara rentimise kande.</span><span class="sxs-lookup"><span data-stu-id="5531a-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="5531a-118">Rendimakse kanne sisestatakse töölehe nimele, mis on määratud väljal **Igakuine rendi tööleht**.</span><span class="sxs-lookup"><span data-stu-id="5531a-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="5531a-119">Pärast kande sisestamist saate vaadata kande teavet ja rendikohustise bilansilist väärtust, valides rendi raamatus suvandi **Kohustise tehingud**.</span><span class="sxs-lookup"><span data-stu-id="5531a-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="5531a-120">Maksegraafikus valitakse märkeruut **Tööleht on sisestatud** ja rida kuvab arve töölehe numbri.</span><span class="sxs-lookup"><span data-stu-id="5531a-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="5531a-121">Pärast makse töölehe ja selle töölehe kirje on loodud, peate kirje enne selle uuesti loomist ümber pöörama.</span><span class="sxs-lookup"><span data-stu-id="5531a-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>
