---
title: Klientide kulude korvamine
description: Selles artiklis kirjeldatakse, kuidas kliendigrupile korvamiskandeid luua. Kui kliendil on kreeditsaldo, saate kliendile saldosumma hüvitada.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97982dec140ed440682ae507f40557670ebccd3e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177397"
---
# <a name="reimburse-customers"></a><span data-ttu-id="a80a9-104">Klientide kulude korvamine</span><span class="sxs-lookup"><span data-stu-id="a80a9-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a80a9-105">Selles artiklis kirjeldatakse, kuidas kliendigrupile korvamiskandeid luua.</span><span class="sxs-lookup"><span data-stu-id="a80a9-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="a80a9-106">Kui kliendil on kreeditsaldo, saate kliendile saldosumma hüvitada.</span><span class="sxs-lookup"><span data-stu-id="a80a9-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="a80a9-107">Järgmises tabelis kuvatakse eeltingimused, mis peavad olema asukohakorralduse loomiseks täidetud.</span><span class="sxs-lookup"><span data-stu-id="a80a9-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="a80a9-108">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="a80a9-108">Prerequisite</span></span>                                                            | <span data-ttu-id="a80a9-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a80a9-109">Description</span></span>                                                                                                                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a80a9-110">Juriidilise isiku minimaalse tagasimakse summa määramine.</span><span class="sxs-lookup"><span data-stu-id="a80a9-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="a80a9-111">Sisestage lehe **Müügireskontro parameetrid** ala **Üldine** väljale **Minimaalne tagasimakse** miinimumsumma, mille saab kliendi ülemaksete puhul tagastada.</span><span class="sxs-lookup"><span data-stu-id="a80a9-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="a80a9-112">Valikuline: hankija konto lisamine igale kliendile, kellele saab tagasimakse teha.</span><span class="sxs-lookup"><span data-stu-id="a80a9-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="a80a9-113">Valige kliendi puhul hankija konto lehe **Kliendid** kiirkaardi **Mitmesugused üksikasjad** väljalt **Hankija konto**.</span><span class="sxs-lookup"><span data-stu-id="a80a9-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span>                                           |

<span data-ttu-id="a80a9-114">Korvamiskannete loomisel luuakse kreeditsaldo summa kohta hankija arve.</span><span class="sxs-lookup"><span data-stu-id="a80a9-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="a80a9-115">Korvamisprotsess eemaldab kreeditsaldo kliendi kontolt ja loob kliendile vastava hankija konto saldo.</span><span class="sxs-lookup"><span data-stu-id="a80a9-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1.  <span data-ttu-id="a80a9-116">Käivitage müügireskontros protsess **Korvamine**.</span><span class="sxs-lookup"><span data-stu-id="a80a9-116">In Accounts receivable, run the **Reimbursement** process.</span></span>
2.  <span data-ttu-id="a80a9-117">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="a80a9-117">Follow one of these steps:</span></span>
    -   <span data-ttu-id="a80a9-118">Kindlate kliendikontode korvamiseks klõpsake käsku **Vali** ja määrake päringus kliendikontod.</span><span class="sxs-lookup"><span data-stu-id="a80a9-118">To reimburse specific customer accounts, click **Select**, and specify the customer accounts in the query.</span></span>
    -   <span data-ttu-id="a80a9-119">Kõigi kliendikontode korvamiseks klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="a80a9-119">To reimburse all customer accounts, click **OK**.</span></span>

    <span data-ttu-id="a80a9-120">Kreeditsummad kantakse klientide hankijakontodele ja töödeldakse tavaliste maksetena.</span><span class="sxs-lookup"><span data-stu-id="a80a9-120">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="a80a9-121">Kui kliendil ei ole hankija kontot, loob programm kliendi jaoks automaatselt ühekordse hankija konto.</span><span class="sxs-lookup"><span data-stu-id="a80a9-121">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>
3.  <span data-ttu-id="a80a9-122">Loodud korvamiskannete vaatamiseks kasutage lehte **Korvamine**.</span><span class="sxs-lookup"><span data-stu-id="a80a9-122">To view the reimbursement transactions that were created, use the **Reimbursement** page.</span></span>
4.  <span data-ttu-id="a80a9-123">Looge ostureskontros korvamisprotsessi tulemusena loodud hankija arvete makse.</span><span class="sxs-lookup"><span data-stu-id="a80a9-123">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span>



