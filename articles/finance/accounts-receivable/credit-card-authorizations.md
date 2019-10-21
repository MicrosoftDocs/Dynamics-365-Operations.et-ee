---
title: Krediitkaardi seadistamine, autoriseerimine ja hõivamine
description: See artikkel annab ülevaate krediitkaardi autoriseerimisest rakenduses Microsoft Dynamics 365 Finance. See sisaldab teavet makseteenuse seadistamise, krediitkaardi lisamise kohta müügitellimusele ja loa tühistamise kohta.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a06159f3d26cbaddc1417e863d7e665c2bfb424
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177400"
---
# <a name="credit-card-setup-authorization-and-capture"></a><span data-ttu-id="ac1d1-104">Krediitkaardi seadistamine, autoriseerimine ja hõivamine</span><span class="sxs-lookup"><span data-stu-id="ac1d1-104">Credit card setup, authorization, and capture</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="ac1d1-105">See artikkel annab ülevaate krediitkaardi autoriseerimisest rakenduses Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-105">This article provides an overview of credit card authorization in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="ac1d1-106">See sisaldab teavet makseteenuse seadistamise, krediitkaardi lisamise kohta müügitellimusele ja loa tühistamise kohta.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-106">It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.</span></span>

<a name="setting-up-the-credit-card-payment-service"></a><span data-ttu-id="ac1d1-107">Krediitkaardi makseteenuse seadistamine</span><span class="sxs-lookup"><span data-stu-id="ac1d1-107">Setting up the credit card payment service</span></span>
------------------------------------------

<span data-ttu-id="ac1d1-108">Krediitkaartide kasutamiseks tuleb makseteenus lehel Makseteenused seadistada ja aktiveerida.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-108">To use credit cards, you must set up and activate a payment service on the Payment services page.</span></span> <span data-ttu-id="ac1d1-109">Makseteenus toimib sillana teie juriidilise isiku ja kliendi krediitkaarditasusid töötleva panga vahel.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-109">A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges.</span></span> <span data-ttu-id="ac1d1-110">Peaksite töötama väljal Makse ülekandmine loetletud krediitkaardi pakkujaga ja seadistama selle pakkujaga konto.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-110">You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider.</span></span> <span data-ttu-id="ac1d1-111">Seejärel tuleks seadistada teised suvandid lehel Makseteenused, seadistada krediitkaardi tüübid American Expressi, Discoveri, MasterCardi ja Discoveri jaoks leheküljel Krediitkaardi tüübid ning aktiveerida pakkuja vaikepakkujana.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-111">You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider.</span></span> <span data-ttu-id="ac1d1-112">Seadistuse lõpetamiseks peaksite järgima neid samme.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-112">You must also follow these steps to complete your setup:</span></span>
-   <span data-ttu-id="ac1d1-113">Määrake lehel Müügireskontro parameetrid krediitkaardi kasutamise parameetrid.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-113">On the Accounts receivable parameters page, specify parameters for using credit card authorizations.</span></span>
-   <span data-ttu-id="ac1d1-114">Seadistage lehel Maksetingimused krediitkaartide maksetingimused.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-114">On the Terms of payment page, set up payment terms for credit cards.</span></span> <span data-ttu-id="ac1d1-115">Väljal Makse tüüp valige Krediitkaart.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-115">In the Payment type field, select Credit card.</span></span>
-   <span data-ttu-id="ac1d1-116">Sisestage lehele Kliendi krediitkaardid klientide jaoks krediitkaardi teave.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-116">On the Customer credit cards page, enter credit card information for customers.</span></span>

## <a name="adding-a-new-credit-card"></a><span data-ttu-id="ac1d1-117">Uue krediitkaardi lisamine</span><span class="sxs-lookup"><span data-stu-id="ac1d1-117">Adding a new credit card</span></span>
<span data-ttu-id="ac1d1-118">Uusi krediitkaardi kirjeid saate luua lehel Kliendid, kasutades välju Klient, Hääletamine, Krediitkaart.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-118">You can create new credit card records on the Customers page by using Customer, Set up, Credit card.</span></span> <span data-ttu-id="ac1d1-119">Krediitkaardi kirjeid saate luua ka müügitellimusi lehel Müügitellimus sisestades, kasutades välju Haldamine, Klient, Krediitkaart, Registreerimine.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-119">You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.</span></span>

<a name="adding-a-credit-card-to-a-sales-order"></a><span data-ttu-id="ac1d1-120">Müügitellimusele krediitkaardi lisamine</span><span class="sxs-lookup"><span data-stu-id="ac1d1-120">Adding a credit card to a sales order</span></span>
-------------------------------------

<span data-ttu-id="ac1d1-121">Krediitkaardi lisamiseks müügitellimusele valige krediitkaart krediitkaardi otsingust lehe Müügitellimus vahekaardil Hinnad ja allahindlused.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-121">You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page.</span></span> <span data-ttu-id="ac1d1-122">Autoriseerimisprotsessi käivitamiseks avage tegevuspaani vahekaart Haldamine, kus valige Krediitkaart ja Autoriseerimine.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-122">To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.</span></span>

<a name="authorizing-a-credit-card"></a><span data-ttu-id="ac1d1-123">Krediitkaardi autoriseerimine</span><span class="sxs-lookup"><span data-stu-id="ac1d1-123">Authorizing a credit card</span></span>
-------------------------

<span data-ttu-id="ac1d1-124">Kui krediitkaardi autoriseerimisel kontrollitakse kaardi numbrit ja kaardiomaniku nime ning olemasolev kreeditsaldo kinnitatakse.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-124">When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed.</span></span> <span data-ttu-id="ac1d1-125">Alternatiivina võib kontrollida kaardi kontrollnumbrit ja kaardiomaniku aadressi.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-125">Optionally, the card verification value and the cardholder’s address are verified.</span></span> <span data-ttu-id="ac1d1-126">Seejärel vähendatakse kliendi olemasolevat kreeditsaldot arve summa võrra.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-126">The customer's available credit balance is then reduced by the amount of the invoice.</span></span> <span data-ttu-id="ac1d1-127">Makseteenus annab teada, kas krediitkaart on kinnitatud või tagasi lükatud.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-127">The payment service sends information that the credit card has been approved or declined.</span></span> <span data-ttu-id="ac1d1-128">Kui müügitellimus on arveldatud, võetakse krediitkaardilt tasu (hõivatakse) arve summa väärtuses.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-128">When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.</span></span>

### <a name="card-verification-value"></a><span data-ttu-id="ac1d1-129">Kaardi tõendamise väärtus</span><span class="sxs-lookup"><span data-stu-id="ac1d1-129">Card verification value</span></span>

<span data-ttu-id="ac1d1-130">Saate nõuda kaardi kontrollnumbrit, millele mõnikord on viidatud ka kui kaardi turvakoodile.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-130">You can require the card verification value, which is sometimes referred to as the card's security code.</span></span> <span data-ttu-id="ac1d1-131">American Expressi puhul on see neljakohaline.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-131">For American Express, this is a four-digit value.</span></span> <span data-ttu-id="ac1d1-132">Discoveri, MasterCardi ja Visa puhul on see kolmekohaline.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-132">For Discover, MasterCard, and Visa, it is a three-digit value.</span></span>

### <a name="address-verification"></a><span data-ttu-id="ac1d1-133">Aadressi tõendamine</span><span class="sxs-lookup"><span data-stu-id="ac1d1-133">Address verification</span></span>

<span data-ttu-id="ac1d1-134">Aadressi tõendamise teave saadetakse alati maksepakkujale.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-134">Address verification information is always sent to the payment provider.</span></span> <span data-ttu-id="ac1d1-135">Saate määrata kande aktseptimiseks nõutava teabe hulga.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-135">You can decide how much information is required for a transaction to be accepted.</span></span> <span data-ttu-id="ac1d1-136">Kindlasti kontrollige oma pakkujalt, kas ta aktseptib seda teavet.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-136">Be sure to check with your provider to determine whether it accepts this information.</span></span> <span data-ttu-id="ac1d1-137">Siin on aadressi tõendamise võimalused.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-137">Here are the options for address verification:</span></span>
-   <span data-ttu-id="ac1d1-138">**Luba kanne alati** – kanne aktseptitakse aadressi tõendamise tulemustest olenemata.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-138">**Always accept transaction** – Accept the transaction, regardless of address verification results.</span></span>
-   <span data-ttu-id="ac1d1-139">**Kontoomanik** – kandel olevat kaardiomaniku nime võrreldakse krediitkaardi ettevõtte teabega.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-139">**Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="ac1d1-140">**Arveldusaadress** – kaardiomaniku nime ja arveldusaadressi kandel võrreldakse krediitkaardi ettevõtte teabega.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-140">**Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="ac1d1-141">**Arve sihtnumber** – kaardiomaniku nime, arveldusaadressi ja arve sihtnumbrit kandel võrreldakse krediitkaardi ettevõtte teabega.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-141">**Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.</span></span>

## <a name="data-support"></a><span data-ttu-id="ac1d1-142">Andmete tugi</span><span class="sxs-lookup"><span data-stu-id="ac1d1-142">Data support</span></span>
<span data-ttu-id="ac1d1-143">Igale toetatud krediitkaardile saate määrata andmete toe taseme.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-143">For each credit card type that is supported, you can specify the level of data support.</span></span> <span data-ttu-id="ac1d1-144">Tase kontrollib kande kohta makseteenusele ülekantava teabe hulka.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-144">The level controls how much information about a transaction is transferred to the payment service.</span></span> <span data-ttu-id="ac1d1-145">Kindlasti kontrollige oma pakkujalt, kas ta saab seda teavet anda.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-145">Be sure to check with your provider to determine whether it can provide this information.</span></span> <span data-ttu-id="ac1d1-146">Siin on andmete toe taseme võimalused.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-146">Here are the options for the level of data support:</span></span>
-   <span data-ttu-id="ac1d1-147">**1. tase** – üle kantakse kande kuupäev, summa ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-147">**Level 1** – Transfer the transaction date, transaction amount, and description.</span></span>
-   <span data-ttu-id="ac1d1-148">**2. tase** – üle kantakse 1. taseme teave ja lisaks tarne- ja kaupmehe aadressid ning maksuteave.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-148">**Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.</span></span>
-   <span data-ttu-id="ac1d1-149">**3. tase** – üle kantakse 2. taseme ja lisaks tellimuse rea teave.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-149">**Level 3** – Transfer all Level 2 information, plus order line information.</span></span>

## <a name="partial-payments"></a><span data-ttu-id="ac1d1-150">Osalised maksed</span><span class="sxs-lookup"><span data-stu-id="ac1d1-150">Partial payments</span></span>
<span data-ttu-id="ac1d1-151">Kui lähetate tellimuse osaliselt, hõivatakse osaline summa ja kogu tellimuse summale tehtud autoriseerimine suletakse.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-151">If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed.</span></span> <span data-ttu-id="ac1d1-152">Seejärel tehakse järelejäänud lähetamata tellimuse summale uus autoriseerimine.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-152">A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.</span></span>

## <a name="voiding-an-authorization"></a><span data-ttu-id="ac1d1-153">Autoriseerimise tühistamine </span><span class="sxs-lookup"><span data-stu-id="ac1d1-153">Voiding an authorization</span></span>
<span data-ttu-id="ac1d1-154">Krediitkaardi autoriseerimise tühistamiseks saate muuta makseviisi teise meetodi vastu, millel ei ole tüüpi Krediitkaart.</span><span class="sxs-lookup"><span data-stu-id="ac1d1-154">To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.</span></span>





