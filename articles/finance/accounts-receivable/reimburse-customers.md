---
title: Klientide kulude korvamine
description: Selles artiklis kirjeldatakse, kuidas kliendigrupile korvamiskandeid luua. Kui kliendil on kreeditsaldo, saate kliendile saldosumma hüvitada.
author: JodiChristiansen
ms.date: 09/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransCustPaym, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.custom: 14191
ms.assetid: 53533ee3-470e-458a-ac8b-3815aa4cb502
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd8b32e04743fdde3cc339e1535f8ae58c518aed
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816288"
---
# <a name="reimburse-customers"></a><span data-ttu-id="4bb90-104">Klientide kulude korvamine</span><span class="sxs-lookup"><span data-stu-id="4bb90-104">Reimburse customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bb90-105">Selles artiklis kirjeldatakse, kuidas kliendigrupile korvamiskandeid luua.</span><span class="sxs-lookup"><span data-stu-id="4bb90-105">This article explains how to create reimbursement transactions for a group of customers.</span></span> <span data-ttu-id="4bb90-106">Kui kliendil on kreeditsaldo, saate kliendile saldosumma hüvitada.</span><span class="sxs-lookup"><span data-stu-id="4bb90-106">If a customer has a credit balance, you can reimburse the customer for the amount of the balance.</span></span> 

<span data-ttu-id="4bb90-107">Järgmises tabelis kuvatakse eeltingimused, mis peavad olema asukohakorralduse loomiseks täidetud.</span><span class="sxs-lookup"><span data-stu-id="4bb90-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="4bb90-108">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="4bb90-108">Prerequisite</span></span>                                                            | <span data-ttu-id="4bb90-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="4bb90-109">Description</span></span> |
|-------------------------------------------------------------------------|-------------|
| <span data-ttu-id="4bb90-110">Juriidilise isiku minimaalse tagasimakse summa määramine.</span><span class="sxs-lookup"><span data-stu-id="4bb90-110">Specify the minimum reimbursement amount for the legal entity.</span></span>          | <span data-ttu-id="4bb90-111">Sisestage lehe **Müügireskontro parameetrid** ala **Üldine** väljale **Minimaalne tagasimakse** miinimumsumma, mille saab kliendi ülemaksete puhul tagastada.</span><span class="sxs-lookup"><span data-stu-id="4bb90-111">On the **Accounts receivable parameters** page, in the **General** area, in the **Minimum reimbursement** field, enter the minimum amount that can be reimbursed for customer overpayments.</span></span> |
| <span data-ttu-id="4bb90-112">Valikuline: hankija konto lisamine igale kliendile, kellele saab tagasimakse teha.</span><span class="sxs-lookup"><span data-stu-id="4bb90-112">Optional: Add a vendor account to each customer that can be reimbursed.</span></span> | <span data-ttu-id="4bb90-113">Valige kliendi puhul hankija konto lehe **Kliendid** kiirkaardi **Mitmesugused üksikasjad** väljalt **Hankija konto**.</span><span class="sxs-lookup"><span data-stu-id="4bb90-113">On the **Customers** page, on the **Miscellaneous details** FastTab, in the **Vendor account** field, select the vendor account for the customer.</span></span> |

<span data-ttu-id="4bb90-114">Korvamiskannete loomisel luuakse kreeditsaldo summa kohta hankija arve.</span><span class="sxs-lookup"><span data-stu-id="4bb90-114">When you create reimbursement transactions, a vendor invoice is created for the amount of the credit balance.</span></span> <span data-ttu-id="4bb90-115">Korvamisprotsess eemaldab kreeditsaldo kliendi kontolt ja loob kliendile vastava hankija konto saldo.</span><span class="sxs-lookup"><span data-stu-id="4bb90-115">The reimbursement process removes the credit balance for the customer account and creates a balance due for the vendor account that corresponds to the customer.</span></span>

1. <span data-ttu-id="4bb90-116">Käivitage müügireskontros **Tagasimakse** protsess (**Müügireskontro \> Perioodilised ülesanded \> Tagasimaksed**).</span><span class="sxs-lookup"><span data-stu-id="4bb90-116">In Accounts receivable, run the **Reimbursement** process (**Accounts receivable \> Periodic tasks \> Reimbursement**).</span></span>
2. <span data-ttu-id="4bb90-117">Kõigi kannete rühmitamiseks pearaamatu dimensioonidest sõltumata seadke suvand **Summeeri klient** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="4bb90-117">To group all transactions, regardless of ledger dimensions, set the **Summarize customer** option to **Yes**.</span></span> <span data-ttu-id="4bb90-118">Ainult sarnaste pearaamatu dimensioonidega kannete rühmitamiseks seadke suvandi olekuks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="4bb90-118">To group only transactions that have similar ledger dimensions, set the option to **No**.</span></span>
3. <span data-ttu-id="4bb90-119">Valige käsk **Kaasa laekumata deebetkannetega kliendid**, et valida kliendid, kellel on maksmata deebetsummad.</span><span class="sxs-lookup"><span data-stu-id="4bb90-119">Select **Include customers with outstanding debit transactions** to select customers who have unsettled debit amounts.</span></span>
4. <span data-ttu-id="4bb90-120">Kindlate kliendikontode hüvitamiseks valige kiirkaardil **Kaasatavad kirjed** suvand **Filtreeri** ja seejärel määratlege päringus kliendikontod.</span><span class="sxs-lookup"><span data-stu-id="4bb90-120">To reimburse specific customer accounts, on the **Records to include** FastTab, select **Filter**, and then specify the customer accounts in the query.</span></span>

    <span data-ttu-id="4bb90-121">Kreeditsummad kantakse klientide hankijakontodele ja töödeldakse tavaliste maksetena.</span><span class="sxs-lookup"><span data-stu-id="4bb90-121">The credit amounts are transferred to the vendor accounts of the customers and are processed as ordinary payments.</span></span> <span data-ttu-id="4bb90-122">Kui kliendil ei ole hankija kontot, loob programm kliendi jaoks automaatselt ühekordse hankija konto.</span><span class="sxs-lookup"><span data-stu-id="4bb90-122">If a customer doesn't have a vendor account, a one-time vendor account is automatically created for the customer.</span></span>

5. <span data-ttu-id="4bb90-123">Loodud hüvitamiskannete vaatamiseks kasutage **Tagasimakse** aruannet (**Müügireskontro \> Päringud ja aruanded \> Tagasimakse aruanne**).</span><span class="sxs-lookup"><span data-stu-id="4bb90-123">To view the reimbursement transactions that were created, use the **Reimbursement** report (**Accounts Receivable \> Inquiries and reports \> Reimbursement report**).</span></span>
6. <span data-ttu-id="4bb90-124">Looge ostureskontros korvamisprotsessi tulemusena loodud hankija arvete makse.</span><span class="sxs-lookup"><span data-stu-id="4bb90-124">In Accounts payable, create a payment for the vendor invoices that were created by the reimbursement process.</span></span> <span data-ttu-id="4bb90-125">Lisateavet hankijatele maksmise kohta vt teemast [Hankija maksete ülevaade](../accounts-payable/Vendor-payments-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="4bb90-125">For information about how to pay vendors, see [Vendor payment overview](../accounts-payable/Vendor-payments-workspace.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]