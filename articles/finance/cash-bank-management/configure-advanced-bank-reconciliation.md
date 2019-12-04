---
title: Pangakonto täpsema vastavusseviimise seadistusprotsess
description: Täpsem panga vastavusseviimise funktsioon võimaldab elektroonilisi pangaväljavõtteid importida ja neid Microsoft Dynamics 365 Finance'is automaatselt pangakannetega vastavusse viia. See artikkel selgitab vastavusseviimise seadistusprotsesse.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 405af4e3e122953bbfa74e7e91d2feef8f068708
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772624"
---
# <a name="advanced-bank-reconciliation-setup-process"></a><span data-ttu-id="89149-104">Pangakonto täpsema vastavusseviimise seadistusprotsess</span><span class="sxs-lookup"><span data-stu-id="89149-104">Advanced bank reconciliation setup process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89149-105">Täpsem panga vastavusseviimise funktsioon võimaldab elektroonilisi pangaväljavõtteid importida ja neid Microsoft Dynamics 365 Finance'is automaatselt pangakannetega vastavusse viia.</span><span class="sxs-lookup"><span data-stu-id="89149-105">Advanced bank reconciliation allows you to import electronic bank statements and automatically reconcile with bank transactions in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="89149-106">See artikkel selgitab vastavusseviimise seadistusprotsesse.</span><span class="sxs-lookup"><span data-stu-id="89149-106">This article will explain the set up processes for reconciliation.</span></span>  

<span data-ttu-id="89149-107">Enne pangakonto täpsema vastavusseviimise funktsiooni kasutamist tuleb seadistada mitmed parameetrid.</span><span class="sxs-lookup"><span data-stu-id="89149-107">There are a number of pieces that must be set up before using the advanced bank reconciliation functionality.</span></span> <span data-ttu-id="89149-108">Lisateavet pangaväljavõtete impordi seadistamise kohta leiate jaotisest [Täpsema panga vastavusseviimise impordiprotsessi seadistamine](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="89149-108">For more information about setting up bank statement import, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>  <span data-ttu-id="89149-109">Vastavusseviimise protsessi seadistamise nõudeid on üksikasjalikult kirjeldatud allpool.</span><span class="sxs-lookup"><span data-stu-id="89149-109">Requirements for set up of the reconciliation process are detailed below.</span></span>

## <a name="transaction-codes"></a><span data-ttu-id="89149-110">Kandekoodid</span><span class="sxs-lookup"><span data-stu-id="89149-110">Transaction codes</span></span>
<span data-ttu-id="89149-111">Kandekoode saab kasutada osana pangakonto vastavusseviimise vastendusreeglitest.</span><span class="sxs-lookup"><span data-stu-id="89149-111">Transaction codes can be used as part of the bank reconciliation matching rules.</span></span> <span data-ttu-id="89149-112">Kandekoodid aitavad vastendada Finance'i ja teie pangaväljavõtte vahel sama tüüpi kanded.</span><span class="sxs-lookup"><span data-stu-id="89149-112">Transaction codes will help to match only the same types of transactions between Finance and your bank statement.</span></span> <span data-ttu-id="89149-113">Seda tüüpi vastendamiseks peate esmalt määratlema Finance'ist tehtavate pangakannete jaoks kasutatavad kandetüübid ja seejärel vastendama need tüübid teie panga kasutatavate väljavõtte kandekoodidega.</span><span class="sxs-lookup"><span data-stu-id="89149-113">In order to do this type of matching, you must first define transaction types used for bank transactions from Finance, then map those types to statement transaction codes used by your bank.</span></span> <span data-ttu-id="89149-114">Pangakannete kandekoodid määratletakse lehel **Pankakande tüüp**.</span><span class="sxs-lookup"><span data-stu-id="89149-114">Transaction types for bank transactions are defined on the **Bank transaction type** page.</span></span> <span data-ttu-id="89149-115">See on ka koht, kus saate määratleda kõnealuse kandetüübiga seostatud sisestuste jaoks kasutatava meilikonto.</span><span class="sxs-lookup"><span data-stu-id="89149-115">This is also where you define the main account to be used for postings associated with that transaction type.</span></span> 

<span data-ttu-id="89149-116">Kui teie pangakandekoodid on määratletud, vastendage need oma elektroonilistel pangaväljavõtetel kasutatavate kandekoodidega.</span><span class="sxs-lookup"><span data-stu-id="89149-116">Once your bank transaction codes are defined, you then map those to the transaction codes used in your electronic bank statements.</span></span> <span data-ttu-id="89149-117">Vastendamine toimub lehel **Kandekoodide vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="89149-117">This mapping process is done using the **Transaction code mapping** page.</span></span> <span data-ttu-id="89149-118">Kandekoodide vastendamine tuleb teha iga pangakonto puhul eraldi.</span><span class="sxs-lookup"><span data-stu-id="89149-118">Transaction code mapping is completed separately for each bank account.</span></span>

## <a name="matching-rules-and-matching-rule-sets"></a><span data-ttu-id="89149-119">Vastendusreeglid ja vastendusreeglite kogumid</span><span class="sxs-lookup"><span data-stu-id="89149-119">Matching rules and matching rule sets</span></span>
<span data-ttu-id="89149-120">Vastendusreeglid võimaldavad määratleda Finance'i pangakannete ja pangaväljavõtte kannete vahelisel automaatse vastavusseviimise kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="89149-120">Matching rules allow you to define criteria for automatic reconciliation between Finance bank transactions and bank statement transactions.</span></span> <span data-ttu-id="89149-121">Vastendusreeglid saate määratleda lehel **Vastavusseviimise vastendusreeglid**.</span><span class="sxs-lookup"><span data-stu-id="89149-121">Setup of matching rules is done on the **Reconciliation matching rules** page.</span></span> <span data-ttu-id="89149-122">Lisateavet vt teemast [Panga vastavusseviimise vastendusreeglite seadistamine](set-up-bank-reconciliation-matching-rules.md).</span><span class="sxs-lookup"><span data-stu-id="89149-122">For more information, see [Set up bank reconciliation matching rules](set-up-bank-reconciliation-matching-rules.md).</span></span> 

<span data-ttu-id="89149-123">Vastendusreeglistikuga määratletakse vastendusreeglite grupp, mis käivitatakse järjest pangakonto vastavusseviimise protsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="89149-123">Matching rule sets are used to define a group of matching rules that are run in sequence during the bank reconciliation process.</span></span>  <span data-ttu-id="89149-124">Vastendusreeglistiku saate konfigureerida lehel **Vastavusseviimise vastendusreeglistikud**.</span><span class="sxs-lookup"><span data-stu-id="89149-124">Matching rule sets are configured on the **Reconciliation matching rule sets** page.</span></span>

## <a name="cash-and-bank-management-parameters"></a><span data-ttu-id="89149-125">Sularaha- ja pangahalduse parameetrid</span><span class="sxs-lookup"><span data-stu-id="89149-125">Cash and bank management parameters</span></span>
<span data-ttu-id="89149-126">Lehel **Sularaha- ja pangahalduse parameetrid** leiate mitmed pangakonto täpsema vastavusseviimise protsessile kohased parameetrid.</span><span class="sxs-lookup"><span data-stu-id="89149-126">There are a number of parameters specific to the advanced bank reconciliation process on the **Cash and bank management parameters** page.</span></span>  <span data-ttu-id="89149-127">Valik **Kuva väljavõtterea summa deebetis/kreeditis** muudab summade vaadet lehel **Pangaväljavõte**.</span><span class="sxs-lookup"><span data-stu-id="89149-127">The **Show statement line amount in debit/credit** changes the view of amounts on the **Bank statement** page.</span></span> <span data-ttu-id="89149-128">Selle valiku korral kuvatakse pangaväljavõtte kandesummad eraldi deebeti- ja kreeditiveergudes.</span><span class="sxs-lookup"><span data-stu-id="89149-128">If this option is selected, the bank statement transaction amounts will be shown in separate debit and credit columns.</span></span> <span data-ttu-id="89149-129">Kui seda suvandit ei valita, kuvatakse pangaväljavõtte kandesummad üksiku summa veerus koos vastava märgiga.</span><span class="sxs-lookup"><span data-stu-id="89149-129">If not selected, the bank statement transaction amounts will be shown in a single amount column with the appropriate sign.</span></span> 

<span data-ttu-id="89149-130">Parameetrite lehel määratud kontrollimisvalikud alistavad vastendusreeglites määratud valikud.</span><span class="sxs-lookup"><span data-stu-id="89149-130">The validation options set on the parameters page override the selections set on matching rules.</span></span> <span data-ttu-id="89149-131">Näiteks ei saa te käsitsi ega automaatselt vastendada dokumente, mis jäävad parameetrite lehel määratud kuupäevavahemikust väljapoole.</span><span class="sxs-lookup"><span data-stu-id="89149-131">For example, you cannot manually or automatically match documents beyond the date difference set on the parameters page.</span></span> <span data-ttu-id="89149-132">Samuti, kui on tehtud valik **Kontrolli kandetüübi vastendust**, tuleb kandetüübid Finance'i pangakannete ja pangaväljavõtte kannete vahel vastendada, et kandeid saaks käsitsi või automaatselt vastendada.</span><span class="sxs-lookup"><span data-stu-id="89149-132">Also, if the option to **Validate transaction type mapping** is selected, the transaction types must be mapped between the Finance bank transaction and bank statement transaction in order for the transactions to be manually or automatically matched.</span></span> 

<span data-ttu-id="89149-133">Peale selle peate konfigureerima lehel **Sularaha- ja pangahalduse parameetrid** vajalikud numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="89149-133">You also must configure the necessary number sequences on the **Cash and bank management parameters** page.</span></span>  <span data-ttu-id="89149-134">Määrake vahekaardil **Numbriseeriad** numbriseeriate koodid **Allalaadimise ID, Väljavõtte ID, Vastavusseviimise ID ja Pangakonto vastavusseviimise** viidetele.</span><span class="sxs-lookup"><span data-stu-id="89149-134">On the **Number sequences** tab, set number sequence codes for the Download **ID, Statement ID, Reconcile ID, and Bank reconciliation** references.</span></span>

## <a name="bank-account-reconciliation-options"></a><span data-ttu-id="89149-135">Pangakonto vastavusseviimise valikud</span><span class="sxs-lookup"><span data-stu-id="89149-135">Bank account reconciliation options</span></span>
<span data-ttu-id="89149-136">Esmalt peate lubama pangakonto täpsema vastavusseviimise pangakonto puhul.</span><span class="sxs-lookup"><span data-stu-id="89149-136">You must first enable Advanced bank reconciliation for the bank account.</span></span> <span data-ttu-id="89149-137">Lehel **Pangakonto** on saadaval mitu lisavalikut, kui funktsioon Pangakonto täpsem vastavusseviimine on lubatud.</span><span class="sxs-lookup"><span data-stu-id="89149-137">A number of additional options are available on the **Bank account** page once the Advanced bank reconciliation functionality is enabled.</span></span> 

<span data-ttu-id="89149-138">Funktsioon **Kasuta pangaväljavõtteid elektroonilise makse kinnitusena** integreerib pangakonto vastavusseviimise funktsiooni elektrooniliste maksete olekutega.</span><span class="sxs-lookup"><span data-stu-id="89149-138">**Use bank statements as confirmation of electronic payment** functionality integrates the bank reconciliation functionality with electronic payment statuses.</span></span> <span data-ttu-id="89149-139">Kui see on lubatud, luuakse pangadokument automaatselt, kui elektroonilise makse olek on **Saadetud**.</span><span class="sxs-lookup"><span data-stu-id="89149-139">When this is enabled, a bank document will automatically be created for the electronic payment status is set to **Sent**.</span></span> <span data-ttu-id="89149-140">Peale selle värskendatakse elektroonilise makse olek väärtuselt **Saadetud** väärtusele **Vastu võetud**, kui makse on vastendatud, vastavusse viidud ja sisestatud.</span><span class="sxs-lookup"><span data-stu-id="89149-140">In addition, the status of an electronic payment will be updated from **Sent** to **Received** after the payment is matched, reconciled, and posted.</span></span> 

<span data-ttu-id="89149-141">Väli **Pangakonto nimi väljavõtetel** on nimi, mida kasutatakse teie elektroonilistel pangaväljavõtetel pangakonto kohta.</span><span class="sxs-lookup"><span data-stu-id="89149-141">The **Bank account name in statements** field is the name used for the bank account on your electronic bank statements.</span></span> <span data-ttu-id="89149-142">Seda nime kasutatakse määramisel, milliseid kandeid importida pangakonto puhul väljavõttest, milles võivad olla mitme pangakonto andmed.</span><span class="sxs-lookup"><span data-stu-id="89149-142">This name is used when determining what transactions to import for a bank account from a statement that may contain information for multiple bank accounts.</span></span> 

<span data-ttu-id="89149-143">Valik **Vii vastavusse pärast importimist** kontrollib automaatselt pangaväljavõtet, loob uue pangakonto vastavusseviimise ja töölehe ning käivitab vaike-vastendamisreeglistiku.</span><span class="sxs-lookup"><span data-stu-id="89149-143">The option to **Reconcile after import** will automatically validate the bank statement, create a new bank reconciliation and worksheet, and run the Default matching rule set.</span></span> <span data-ttu-id="89149-144">See funktsioon automatiseerib protsessi kuni punktini, kus tehingud tuleb käsitsi vastendada.</span><span class="sxs-lookup"><span data-stu-id="89149-144">This functionality automates the process up to the point of the transactions that must be manually matched.</span></span> <span data-ttu-id="89149-145">Säte pangakontol muutub importimisel vaikesätteks.</span><span class="sxs-lookup"><span data-stu-id="89149-145">The setting on the bank account will default when importing.</span></span>


