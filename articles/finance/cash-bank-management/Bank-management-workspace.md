---
title: Pangahalduse tööruum
description: Teema annab teavet pangahalduse tööruumi kohta. See tööruum näitab ettevõtte pangakontodega seotud andmeid ja sisaldab kokkuvõttevaadet ning analüüsi lehte. Kokkuvõttevaade näitab kokkuvõttepaane, pangakonto andmeid, saldodiagrammi ja seotud andmeid. Leht Analüüs kasutab Microsoft Power BI võimalusi pangakonto saldodega seotud visuaalide kuvamiseks.
author: saraschi2
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 262b871a7c35d01283386af6454bb2852197e3b9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818820"
---
# <a name="bank-management-workspace"></a><span data-ttu-id="6796c-106">Pangahalduse tööruum</span><span class="sxs-lookup"><span data-stu-id="6796c-106">Bank management workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6796c-107">Tööruum **Pangahaldus** näitab ettevõtte pangakontodega seotud andmeid.</span><span class="sxs-lookup"><span data-stu-id="6796c-107">The **Bank management** workspace shows information that is related to company bank accounts.</span></span> <span data-ttu-id="6796c-108">See tööruum sisaldab vaadet **Kokkuvõte** ja lehte **Analüüs**.</span><span class="sxs-lookup"><span data-stu-id="6796c-108">This workspace includes a **Summary** view and an **Analytics** page.</span></span> <span data-ttu-id="6796c-109">Vaade **Kokkuvõte** näitab kokkuvõttepaane, pangakonto andmeid, saldodiagrammi ja seotud andmeid.</span><span class="sxs-lookup"><span data-stu-id="6796c-109">The **Summary** view shows summary tiles, bank account information, a balance chart, and related information.</span></span> <span data-ttu-id="6796c-110">Leht **Analüüs** kasutab Microsoft Power BI võimalusi pangakonto saldodega seotud visuaalide kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="6796c-110">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to bank account balances.</span></span>

## <a name="summary-view"></a><span data-ttu-id="6796c-111">Kokkuvõttevaade</span><span class="sxs-lookup"><span data-stu-id="6796c-111">Summary view</span></span>

### <a name="summary"></a><span data-ttu-id="6796c-112">Kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="6796c-112">Summary</span></span>

<span data-ttu-id="6796c-113">Paanid jaotises **Kokkuvõte** annavad ülevaate pangakontodest ja kiire juurdepääsu lehtedele, mida on vaja kõige sagedamini kasutada.</span><span class="sxs-lookup"><span data-stu-id="6796c-113">The tiles in the **Summary** section give an overview of your bank accounts and provide quick access to the pages that you most often have to use.</span></span> <span data-ttu-id="6796c-114">Panga vastavusseviimise teave on täpsema panga vastavusseviimise funktsiooni põhine.</span><span class="sxs-lookup"><span data-stu-id="6796c-114">The bank reconciliation information is specific to the Advanced bank reconciliation functionality.</span></span> <span data-ttu-id="6796c-115">Lisatakse teave ainult nende pangakontode kohta, millel valiku **Täpsem panga vastavusseviimine** on seatud olekusse **Jah** lehel **Pangakonto**.</span><span class="sxs-lookup"><span data-stu-id="6796c-115">Information is included only for those bank accounts that have the **Advanced bank reconciliation** option set to **Yes** on the **Bank account** page.</span></span> <span data-ttu-id="6796c-116">Jaotisest **Kokkuvõte** saate importida elektroonilisi pangafaile pangakontodele kõigi juriidiliste isikute lõikes.</span><span class="sxs-lookup"><span data-stu-id="6796c-116">From the **Summary** section, you can import electronic bank files for bank accounts across all legal entities.</span></span>

### <a name="bank-accounts"></a><span data-ttu-id="6796c-117">Pangakontod</span><span class="sxs-lookup"><span data-stu-id="6796c-117">Bank accounts</span></span>

<span data-ttu-id="6796c-118">Iga pangakonto juriidilises isikus on kajastatud kaardiga jaotises **Pangakontod**.</span><span class="sxs-lookup"><span data-stu-id="6796c-118">Each bank account in the legal entity is represented by a card in the **Bank accounts** section.</span></span> <span data-ttu-id="6796c-119">Kuvatakse jooksev saldo ja saate minna süvitsi kannetesse, millest see koondsaldo summa koosneb.</span><span class="sxs-lookup"><span data-stu-id="6796c-119">The current balance is shown, and you can drill down to the transactions that make up that summary balance amount.</span></span> <span data-ttu-id="6796c-120">Summa **Vahekonto kanded** võimaldab minna süvitsi kannetesse, millest see koondsumma koosneb.</span><span class="sxs-lookup"><span data-stu-id="6796c-120">The **Bridged transactions** amount also lets you drill down to the transactions that make up that summary amount.</span></span> <span data-ttu-id="6796c-121">Vahekonto kanded on kõik ootel kanded, mis on funktsiooni Vahekonto abil sisestatud, kuid mida pole veel sobivaks märgitud.</span><span class="sxs-lookup"><span data-stu-id="6796c-121">Bridged transactions are any pending transactions that have been posted by using bridging functionality, but that haven't yet been cleared.</span></span> <span data-ttu-id="6796c-122">Summa **Ootel saldo** on jooksev saldo, millest on lahutatud vahekonto kanded või ootel kanded.</span><span class="sxs-lookup"><span data-stu-id="6796c-122">The **Pending balance** amount is the current balance minus the bridged, or pending, transactions.</span></span>

<span data-ttu-id="6796c-123">See kaart näitab ka pangakonto viimase vastavusseviimise aega.</span><span class="sxs-lookup"><span data-stu-id="6796c-123">The card also shows when the bank account was last reconciled.</span></span> <span data-ttu-id="6796c-124">See teave kuvatakse ainult juhul, kui pangakontol on täpsem panga vastavusseviimine lubatud.</span><span class="sxs-lookup"><span data-stu-id="6796c-124">This information is shown only if Advanced bank reconciliation is enabled for the bank account.</span></span>

### <a name="balance"></a><span data-ttu-id="6796c-125">Saldo</span><span class="sxs-lookup"><span data-stu-id="6796c-125">Balance</span></span>

<span data-ttu-id="6796c-126">Diagramm **Saldo** näitab varasemat saldoteavet jaotises **Pangakontod** valitud pangakonto kohta või varasemat saldoteavet kõigi juriidilise isiku pangakontode kohta.</span><span class="sxs-lookup"><span data-stu-id="6796c-126">The **Balance** chart shows either historic balance information for the bank account that is selected in the **Bank accounts** section or a summary of historic balance information for all bank accounts in the legal entity.</span></span> <span data-ttu-id="6796c-127">See teave on saadaval mitmesuguste perioodide kohta: jooksev nädal, jooksev kuu, jooksev aasta, viimased viis aastat ja kõik perioodid (pangakonto täielik ajalugu).</span><span class="sxs-lookup"><span data-stu-id="6796c-127">This information is available for various periods: the current week, the current month, the current year, the last five years, and all periods (the full history of the bank account).</span></span> 

<span data-ttu-id="6796c-128">Kui vaatate diagrammi **Saldo** ühe pangakonto kohta, kuvatakse varasemad saldod pangakonto valuutas.</span><span class="sxs-lookup"><span data-stu-id="6796c-128">If you're viewing the **Balance** chart for a single bank account, the historic balances are shown in the bank account currency.</span></span> <span data-ttu-id="6796c-129">Kui vaatate diagrammi kõigi juriidilise isiku pangakontode kohta, kuvatakse varasemad saldod arvestusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="6796c-129">If you're viewing the chart for all bank accounts in the legal entity, the historic balances are shown in the accounting currency.</span></span>

<span data-ttu-id="6796c-130">Teave andmete viimase uuendamise kohta kuvatakse diagrammi ülaosas.</span><span class="sxs-lookup"><span data-stu-id="6796c-130">Information about when the data was last updated appears at the top of the chart.</span></span> <span data-ttu-id="6796c-131">Andmeid saab vajalikul viisil uuendada.</span><span class="sxs-lookup"><span data-stu-id="6796c-131">You can update the data as you require.</span></span>

### <a name="related-information"></a><span data-ttu-id="6796c-132">Seostuv teave</span><span class="sxs-lookup"><span data-stu-id="6796c-132">Related information</span></span>

<span data-ttu-id="6796c-133">Jaotisest **Seotud andmed** saab avada lehe **Päevaraamat** pangaülekannete tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="6796c-133">From the **Related information** section, you can open the **General journal** page to complete bank transfers.</span></span> <span data-ttu-id="6796c-134">Saate avada kiiresti ka lehti **Pangakanded** ja **Vahekonto kanded**.</span><span class="sxs-lookup"><span data-stu-id="6796c-134">You can also quickly open the **Bank transactions** and **Bridged transactions** pages.</span></span>

## <a name="analytics-view"></a><span data-ttu-id="6796c-135">Analüüsivaade</span><span class="sxs-lookup"><span data-stu-id="6796c-135">Analytics view</span></span>

<span data-ttu-id="6796c-136">Lehel **Analüüs** on olulised mõõdikud pangakontode kohta praeguses ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="6796c-136">The **Analytics** page provides important metrics about the bank accounts in the current company.</span></span> <span data-ttu-id="6796c-137">Lehel on saadaval järgmised visualisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="6796c-137">The following visualizations are available on the page:</span></span>

-   <span data-ttu-id="6796c-138">Kogu pangasaldo süsteemi valuutas</span><span class="sxs-lookup"><span data-stu-id="6796c-138">Total bank balance in system currency</span></span>
-   <span data-ttu-id="6796c-139">Saldo juriidilise isiku järgi</span><span class="sxs-lookup"><span data-stu-id="6796c-139">Balance by legal entity</span></span>
-   <span data-ttu-id="6796c-140">Tänane tegelik saldo võrreldes prognoositava saldoga pangakonto valuutas</span><span class="sxs-lookup"><span data-stu-id="6796c-140">Today’s actual vs forecasted balance in bank account currency</span></span>
-   <span data-ttu-id="6796c-141">Saldo pangakonto järgi</span><span class="sxs-lookup"><span data-stu-id="6796c-141">Balance by bank account</span></span>
-   <span data-ttu-id="6796c-142">Saldo valuuta järgi</span><span class="sxs-lookup"><span data-stu-id="6796c-142">Balance by currency</span></span>

<span data-ttu-id="6796c-143">Pangaanalüüsi saab vaadata kõigi ettevõtete lõikes tööruumis **Kassa ülevaade – kõik ettevõtted**.</span><span class="sxs-lookup"><span data-stu-id="6796c-143">You can view bank analytics across all companies from the **Cash overview – all companies** workspace.</span></span> <span data-ttu-id="6796c-144">Lisateabe saamiseks vt [Sularaha ülevaate Power BI sisu](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="6796c-144">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]