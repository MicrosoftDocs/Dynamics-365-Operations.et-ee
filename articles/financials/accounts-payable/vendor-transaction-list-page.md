---
title: Hankija kannete loendi leht
description: See teema sisaldab teavet rakenduse Microsoft Dynamics 365 for Finance and Operations hankija kannete loendi lehe kohta.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 1ef7d97f059801f2fb2c0d451546b57055208f81
ms.contentlocale: et-ee
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-transaction-list-page"></a><span data-ttu-id="bfa5b-103">Hankija kannete loendi leht</span><span class="sxs-lookup"><span data-stu-id="bfa5b-103">Vendor transaction list page</span></span>

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a><span data-ttu-id="bfa5b-104">Kuva tasakaalustused</span><span class="sxs-lookup"><span data-stu-id="bfa5b-104">View settlements</span></span>

<span data-ttu-id="bfa5b-105">Vahekaart **Kuva tasakaalustused** toimingupaanil annab kiire juurdepääsu tasakaalustuste ajaloole ja lisateavet kogu tasakaalustuskande kohta.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-105">The **View settlements** tab on the action pane provides quick access to settlement history and more information about the whole settlement transaction.</span></span> <span data-ttu-id="bfa5b-106">Saate ka kuvada lisakandeid, mis on seotud valitud kandega kas seetõttu, et need olid osa samast tasakaalustusest või kuna need on maksed, mis loodi samas makse töölehes.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-106">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

1. <span data-ttu-id="bfa5b-107">Valige suvandid **Ostureskontro \> Kõik hankijad**.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-107">Select **Accounts payable \> All vendors**.</span></span>
2. <span data-ttu-id="bfa5b-108">Valige hankija, kellel on kanded, ja seejärel valige suvandid **Hankija \> Kanded**.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-108">Select a vendor that has transactions, and then select **Vendor \> Transactions**.</span></span>
3. <span data-ttu-id="bfa5b-109">Valige uurimiseks kanne.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-109">Select a transaction to research.</span></span>
4. <span data-ttu-id="bfa5b-110">Valige toimingupaanilt vahekaart **Kuva tasakaalustused**.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-110">Select the **View settlements** tab on the action pane.</span></span>

    <span data-ttu-id="bfa5b-111">Avaneb dialoogiboks **Kuva tasakaalustused** ja kuvab valitud kande ning kõik dokumendid, mis on selle suhtes tasakaalustatud.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-111">The **View settlements** dialog box opens and shows the selected transaction and all documents that are settled against it.</span></span> <span data-ttu-id="bfa5b-112">See dialoogiboks meenutab tasakaalustuste ajaloo vaadet, aga sisaldab kõiki seotud dokumente.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-112">This dialog box resembles the settlement history view, but it includes all related documents.</span></span>

5. <span data-ttu-id="bfa5b-113">Sellest dialoogiboksist saate teha mitmesuguseid toiminguid.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-113">You can perform various tasks from this dialog box.</span></span> <span data-ttu-id="bfa5b-114">Valige üks või mitu kannet ja seejärel valige üks järgmistest menüüdest:</span><span class="sxs-lookup"><span data-stu-id="bfa5b-114">Select one or more vouchers, and then select one of the following menus:</span></span>

   - <span data-ttu-id="bfa5b-115">**Kuva raamatupidamine** – kuvatakse kõik valitud dokumentidega seotud kanded.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-115">**View accounting** – All vouchers that are related to the selected documents appear.</span></span> <span data-ttu-id="bfa5b-116">Valige dialoogiboksi sulgemiseks suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-116">Select **Close** to close the dialog box.</span></span>
   - <span data-ttu-id="bfa5b-117">**Ekspordi** – ekspordi valitud kanded Microsoft Excelisse.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-117">**Export** – Export the selected vouchers to Microsoft Excel.</span></span>
   - <span data-ttu-id="bfa5b-118">**Kuva seotud maksed** – kuvatakse kõik valitud dokumendiga seotud makse töölehes loodud töölehekanded.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-118">**View related payments** – All the payment journal transactions that were created in the payment journal that is related to the selected document appear.</span></span> <span data-ttu-id="bfa5b-119">Peale selle kuvatakse kõik nende maksetega seotud tasakaalustused.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-119">In addition, all the settlements that are related to those payments appear.</span></span> <span data-ttu-id="bfa5b-120">Selle menüü silt muutub sildiks **Kuva tasakaalustused**.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-120">The label of this menu also changes to **View settlements**.</span></span> <span data-ttu-id="bfa5b-121">Valige suvand **Kuva tasakaalustused**, et kuvada ainult need kanded, mis kuvati dialoogiboksi **Kuva tasakaalustused** esimesel avamisel.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-121">Select **View settlements** to show only the transactions that were shown when you first opened the  **View settlements** dialog box.</span></span>
    - <span data-ttu-id="bfa5b-122">**Kannete tasakaalustamine** – see menüü ilmub, kui valitud algdokument ei olnud täielikult tasakaalustatud.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-122">**Settle transactions** – This menu appears if the original document that was selected wasn't fully settled.</span></span> <span data-ttu-id="bfa5b-123">Kui selle valite, ilmub dialoogiboks **Kannete tasakaalustamine**, kus saate valida tasakaalustamiseks kanded.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-123">When you select it, the **Settle transactions** dialog box appears, where you can select transactions for settlement.</span></span>
    - <span data-ttu-id="bfa5b-124">**Tasakaalustamise tühistamine** – see menüü ilmub, kui valitud algdokument oli täielikult tasakaalustatud.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-124">**Undo settlements** – This menu appears if the original document that was selected was fully settled.</span></span> <span data-ttu-id="bfa5b-125">Kui selle valite, ilmub dialoogiboks **Tasakaalustamise tühistamine**, kus saate tühistada selle dokumendi tasakaalustamised.</span><span class="sxs-lookup"><span data-stu-id="bfa5b-125">When you select it, the **Undo settlements** dialog box appears, where you can undo the settlements that were done for that document.</span></span>

