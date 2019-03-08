---
title: Ostureskontro konfigureerimine
description: Selles artiklis kirjeldatakse lehti, mida kasutatakse Microsoft Dynamics 365 for Finance and Operationsi mooduli Ostureskontro põhi- ja valikuliste funktsioonide seadistamiseks. Kirjeldatakse ka seadistamistoiminguid, mis tuleb teha enne mooduli Ostureskontro seadistamist.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a832a30870f77578503bae6eea17ad1d0881d91
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "326695"
---
# <a name="configure-accounts-payable"></a><span data-ttu-id="479e4-104">Ostureskontro konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="479e4-104">Configure Accounts payable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="479e4-105">Selles artiklis kirjeldatakse lehti, mida kasutatakse Microsoft Dynamics 365 for Finance and Operationsi mooduli Ostureskontro põhi- ja valikuliste funktsioonide seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="479e4-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="479e4-106">Kirjeldatakse ka seadistamistoiminguid, mis tuleb teha enne mooduli Ostureskontro seadistamist.</span><span class="sxs-lookup"><span data-stu-id="479e4-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

<a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="479e4-107">Ostureskontro seadistamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="479e4-107">Prerequisites for Accounts payable setup</span></span>
----------------------------------------

<span data-ttu-id="479e4-108">Enne ostureskontro seadistamist tuleb teha järgmine seadistus.</span><span class="sxs-lookup"><span data-stu-id="479e4-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="479e4-109">Pearaamatus.</span><span class="sxs-lookup"><span data-stu-id="479e4-109">In General ledger:</span></span>
    -   <span data-ttu-id="479e4-110">Kui kavatsete kasutada maksetöölehti, seadistage maksetöölehed.</span><span class="sxs-lookup"><span data-stu-id="479e4-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="479e4-111">Kui te kavatsete käivitada vahetuskursi korrektsioone, seadistage valuutakoodid lehel Valuutad, seadistage vahetuskursi tüübid lehel Vahetuskursi tüübid ja valuutavahetuskursid lehel Valuutavahetuskursid.</span><span class="sxs-lookup"><span data-stu-id="479e4-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="479e4-112">Seadistage moodulis Sularaha- ja pangahaldus makseviiside korral kasutatavad pangakontod.</span><span class="sxs-lookup"><span data-stu-id="479e4-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="479e4-113">Ostureskontro seadistuslehed</span><span class="sxs-lookup"><span data-stu-id="479e4-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="479e4-114">Kasutage järgmisi lehti iga juriidilise isiku jaoks ostureskontro põhifunktsioonide seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="479e4-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="479e4-115">Lehed on loetletud soovitatavas seadistamise järjekorras.</span><span class="sxs-lookup"><span data-stu-id="479e4-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="479e4-116">Seadistamisprotsessi hõlbustamiseks saate luua malle esimeste loodud kirjete põhjal.</span><span class="sxs-lookup"><span data-stu-id="479e4-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="479e4-117">Mallis sisestatakse tavaliselt paljudele väljadele väärtused, mis kajastavad funktsioone, mida organisatsioon soovib teatud tüüpi hankija korral kasutada.</span><span class="sxs-lookup"><span data-stu-id="479e4-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="479e4-118">Lehel Maksetingimused saate määratleda müügitellimustele, ostutellimustele, klientidele ja hankijatele määratud maksetingimused, mis määravad kindlaks arve tähtajad.</span><span class="sxs-lookup"><span data-stu-id="479e4-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="479e4-119">Lisateavet vt [Hankija käitluslõivude määratlemine](tasks/define-vendor-payment-fees.md).</span><span class="sxs-lookup"><span data-stu-id="479e4-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="479e4-120">Lehel Makseviisid – hankijad saate luua ja hallata andmeid selle kohta, kuidas organisatsioon oma hankijatele maksab.</span><span class="sxs-lookup"><span data-stu-id="479e4-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="479e4-121">Lehel Hankijagrupid saate luua ja hallata hankijagruppe, millel on olulised ühised parameetrid sisestamise, tasakaalustuse ja maksmise, aruandluse ja prognoosimise jaoks.</span><span class="sxs-lookup"><span data-stu-id="479e4-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="479e4-122">Lehel Hankija sisestusreeglid saate määratleda, kuidas hankijakanded pearaamatusse sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="479e4-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="479e4-123">Lehel Ostureskontro parameetrid saate seadistada vaikesätted, mida rakendada, kui täpsemat sätet ei ole määratletud, erinevate funktsioonide parameetrid ja erinevad ostureskontro numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="479e4-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="479e4-124">Lehel Vormi seadistus saate määratleda erinevate dokumentide vormingu, mis on seotud hankijaga ja mida organisatsioon kasutab, et jälgida hankijatelt saadud sissetulekuid ja sisestada hankijate maksevoo põhjusi.</span><span class="sxs-lookup"><span data-stu-id="479e4-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="479e4-125">Lehel Hankijad saate luua ja hallata hankijakontosid ja samuti maksuasutusi, millele teie organisatsioon käibearuandeid esitab.</span><span class="sxs-lookup"><span data-stu-id="479e4-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="479e4-126">Ostureskontro valikulised seadistuslehed</span><span class="sxs-lookup"><span data-stu-id="479e4-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="479e4-127">Lisaks põhifunktsioonidele on moodulil Ostureskontro muid funktsioone, mida saab seadistada.</span><span class="sxs-lookup"><span data-stu-id="479e4-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="479e4-128">Täiendavad seadistuslehed on organiseeritud funktsioonide järgi.</span><span class="sxs-lookup"><span data-stu-id="479e4-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="479e4-129">**Poliitikad**</span><span class="sxs-lookup"><span data-stu-id="479e4-129">**Policies**</span></span>
-   <span data-ttu-id="479e4-130">Lehel Hankija arvepoliitika saate seadistada hankija arvepoliitikaid.</span><span class="sxs-lookup"><span data-stu-id="479e4-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="479e4-131">**Arvete võrdlemine**</span><span class="sxs-lookup"><span data-stu-id="479e4-131">**Invoice matching**</span></span>

-   <span data-ttu-id="479e4-132">Lehel Arvesummade lubatud kõikumised saate seadistada arvesummade lubatud kõikumisi.</span><span class="sxs-lookup"><span data-stu-id="479e4-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="479e4-133">Lehel Vastavusse viimise poliitika saate seadistada kahesuunalisi ja kolmesuunalisi vastavusse viimise poliitikaid.</span><span class="sxs-lookup"><span data-stu-id="479e4-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="479e4-134">Lehel Hinnakõikumised saate seadistada ühikuhindade lubatud kõikumisi.</span><span class="sxs-lookup"><span data-stu-id="479e4-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="479e4-135">Lehel Kauba hinnakõikumisgrupid saate seadistada kauba hinnakõikumisgruppe.</span><span class="sxs-lookup"><span data-stu-id="479e4-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="479e4-136">Lehel Hankija hinnakõikumisgrupid saate seadistada hankija hinnakõikumisgruppe.</span><span class="sxs-lookup"><span data-stu-id="479e4-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="479e4-137">Lehel Tasude kõikumised saate seadistada tasude lubatud kõikumisi.</span><span class="sxs-lookup"><span data-stu-id="479e4-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="479e4-138">**Töövoog**</span><span class="sxs-lookup"><span data-stu-id="479e4-138">**Workflow**</span></span>

-   <span data-ttu-id="479e4-139">Lehel Ostureskontro töövood saate seadistada töövookonfiguratsioone töölehtede kinnituste ja ostutaotluste jaoks.</span><span class="sxs-lookup"><span data-stu-id="479e4-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="479e4-140">**Põhjused**</span><span class="sxs-lookup"><span data-stu-id="479e4-140">**Reasons**</span></span>

-   <span data-ttu-id="479e4-141">Lehel Hankija põhjused saate seadistada põhjusekoode.</span><span class="sxs-lookup"><span data-stu-id="479e4-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="479e4-142">**Tasud**</span><span class="sxs-lookup"><span data-stu-id="479e4-142">**Charges**</span></span>

-   <span data-ttu-id="479e4-143">Lehel Tasukoodid saate seadistada ostutellimustel kasutatavaid tasukoode.</span><span class="sxs-lookup"><span data-stu-id="479e4-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="479e4-144">Lehel Hankija tasude grupp saate luua ja hallata hankijate tasugruppe.</span><span class="sxs-lookup"><span data-stu-id="479e4-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="479e4-145">Lehel Kauba tasugrupid  saate luua ja hallata kaupade tasugruppe.</span><span class="sxs-lookup"><span data-stu-id="479e4-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="479e4-146">Lehel Automaatsed kulud saate määratleda tellimustele automaatselt määratavad tasud.</span><span class="sxs-lookup"><span data-stu-id="479e4-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="479e4-147">**Lisakaubad**</span><span class="sxs-lookup"><span data-stu-id="479e4-147">**Supplementary items**</span></span>

-   <span data-ttu-id="479e4-148">Lehel Lisakaubagrupid – hankija saate luua ja hallata hankijate lisakaubagruppe.</span><span class="sxs-lookup"><span data-stu-id="479e4-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="479e4-149">Lehel Lisakaubagrupid – varud saate luua ja hallata kaupade lisakaubagruppe.</span><span class="sxs-lookup"><span data-stu-id="479e4-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="479e4-150">**Jaotus**</span><span class="sxs-lookup"><span data-stu-id="479e4-150">**Distribution**</span></span>

-   <span data-ttu-id="479e4-151">Lehel Tarnetingimused saate luua ja hallata kauba müüjalt ostjale tarnimise tingimusi.</span><span class="sxs-lookup"><span data-stu-id="479e4-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="479e4-152">Lehel Tarneviisid saate luua ja hallata transpordiviise, mida kasutatakse tellimuse transportimisel müüjalt ostjale.</span><span class="sxs-lookup"><span data-stu-id="479e4-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="479e4-153">Lehel Sihtkoha koodid saate luua ja hallata sihtkohtade koode ja kirjeldusi.</span><span class="sxs-lookup"><span data-stu-id="479e4-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="479e4-154">**Vormid**</span><span class="sxs-lookup"><span data-stu-id="479e4-154">**Forms**</span></span>

-   <span data-ttu-id="479e4-155">Lehel Vormi märkused saate luua mitmesugustel lehtedel kuvatavat standardteksti.</span><span class="sxs-lookup"><span data-stu-id="479e4-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="479e4-156">Lehel Vormi sortimisparameetrid saate seadistada ostutellimuste, saabunud kaupade loendi, saatelehtede ja arvete sortimisjärjestuse.</span><span class="sxs-lookup"><span data-stu-id="479e4-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="479e4-157">Lehel Prindihalduse seadistus saate seadistada prindihalduse teabe lehtede originaalidele ja koopiatele.</span><span class="sxs-lookup"><span data-stu-id="479e4-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="479e4-158">**Maksed**</span><span class="sxs-lookup"><span data-stu-id="479e4-158">**Payments**</span></span>

-   <span data-ttu-id="479e4-159">Lehel Skontod saate seadistada ja hallata skontode saamise tingimusi.</span><span class="sxs-lookup"><span data-stu-id="479e4-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="479e4-160">Skonto koodid on seotud hankijatega ja neid rakendatakse ostutellimuste korral.</span><span class="sxs-lookup"><span data-stu-id="479e4-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="479e4-161">Lehel Maksegraafikud saate seadistada maksegraafikuid, mida kasutatakse hankijatele osamaksete tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="479e4-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="479e4-162">Lehel Maksepäevad  saate määratleda tähtaegade arvutamiseks kasutatavad maksepäevad ja täpsustada maksepäevaks konkreetse nädalapäeva või kuu.</span><span class="sxs-lookup"><span data-stu-id="479e4-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="479e4-163">Lehel Maksetasu saate luua ja hallata hankijatega seotud maksetasusid.</span><span class="sxs-lookup"><span data-stu-id="479e4-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="479e4-164">Lehel Maksejuhis saate luua ja hallata maksejuhiseid.</span><span class="sxs-lookup"><span data-stu-id="479e4-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="479e4-165">**Statistika**</span><span class="sxs-lookup"><span data-stu-id="479e4-165">**Statistics**</span></span>

-   <span data-ttu-id="479e4-166">Lehel Aegumisperioodi määratlused saate seadistada kasutaja määratletud intervalle, mida kasutatakse hankijakontode tähtajalise jaotuse analüüsimiseks.</span><span class="sxs-lookup"><span data-stu-id="479e4-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="479e4-167">Lehel Tegevusala saate luua tegevusala koode, mis hankijatele määratakse.</span><span class="sxs-lookup"><span data-stu-id="479e4-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="479e4-168">**Maks 1099**</span><span class="sxs-lookup"><span data-stu-id="479e4-168">**Tax 1099**</span></span>

-   <span data-ttu-id="479e4-169">Lehel **1099 väljad** saate kontrollida ja muuta miinimumsummasid, millest tuleb USA Maksuametile (IRS-ile) viimaste IRS-i nõuete alusel aru anda.</span><span class="sxs-lookup"><span data-stu-id="479e4-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="479e4-170">**Valikuline seadistus teiste moodulite puhul**</span><span class="sxs-lookup"><span data-stu-id="479e4-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="479e4-171">**Organisatsiooni haldus**</span><span class="sxs-lookup"><span data-stu-id="479e4-171">**Organization administration**</span></span>

-   <span data-ttu-id="479e4-172">Lehel numbriseeriad saate seadistada arvenumbritele numbriseeriate grupid.</span><span class="sxs-lookup"><span data-stu-id="479e4-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="479e4-173">Saate seadistada järgmistel lehtedel aadressiteabe.</span><span class="sxs-lookup"><span data-stu-id="479e4-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="479e4-174">Aadressi häälestamine</span><span class="sxs-lookup"><span data-stu-id="479e4-174">Address setup</span></span>
    -   <span data-ttu-id="479e4-175">NAF-koodid</span><span class="sxs-lookup"><span data-stu-id="479e4-175">NAF codes</span></span>
    -   <span data-ttu-id="479e4-176">Impordi sihtnumbrid</span><span class="sxs-lookup"><span data-stu-id="479e4-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="479e4-177">**Pearaamat**</span><span class="sxs-lookup"><span data-stu-id="479e4-177">**General ledger**</span></span>

-   <span data-ttu-id="479e4-178">Lehel Finantsdimensioonid saate seadistada finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="479e4-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="479e4-179">Järgmistel lehtedel saate seadistada maksuteavet.</span><span class="sxs-lookup"><span data-stu-id="479e4-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="479e4-180">Käibemaksukoodid</span><span class="sxs-lookup"><span data-stu-id="479e4-180">Sales tax codes</span></span>
    -   <span data-ttu-id="479e4-181">Käibemaksugrupid</span><span class="sxs-lookup"><span data-stu-id="479e4-181">Sales tax groups</span></span>
    -   <span data-ttu-id="479e4-182">Kauba käibemaksugrupid</span><span class="sxs-lookup"><span data-stu-id="479e4-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="479e4-183">Kontogrupp</span><span class="sxs-lookup"><span data-stu-id="479e4-183">Account group</span></span>
    -   <span data-ttu-id="479e4-184">Käibemaksuvabastuse koodid</span><span class="sxs-lookup"><span data-stu-id="479e4-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="479e4-185">Käibemaksu jurisdiktsioonid</span><span class="sxs-lookup"><span data-stu-id="479e4-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="479e4-186">Käibemaksuhaldurid</span><span class="sxs-lookup"><span data-stu-id="479e4-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="479e4-187">Käibemaksu tasakaalustusperioodid</span><span class="sxs-lookup"><span data-stu-id="479e4-187">Sales tax settlement periods</span></span>

<span data-ttu-id="479e4-188">**Sularaha- ja pangahaldus**</span><span class="sxs-lookup"><span data-stu-id="479e4-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="479e4-189">Lehel Makse eesmärgi koodid saate seadistada keskpangamakse eesmärgikoodi.</span><span class="sxs-lookup"><span data-stu-id="479e4-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>





