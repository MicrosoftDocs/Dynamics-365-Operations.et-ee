---
title: Vahetuse konfigureerimine ja töötlemine tagastustellimusel
description: Selles teemas selgitatakse, kuidas konfigureerida vahetust tagastusel rakenduses Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5a0a6a060a1b4a4d5a80c797f61b212a828d2f04
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517047"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a><span data-ttu-id="cf3bd-103">Vahetuse konfigureerimine ja töötlemine tagastustellimusel</span><span class="sxs-lookup"><span data-stu-id="cf3bd-103">Configure and process an exchange on a return order</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf3bd-104">Rakenduse Microsoft Dynamics 365 for Retail eelmistes versioonides töödeldi klienditellimuste tagastusi, kasutades programmis Retail Headquarters tagastustellimuse dokumenti.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-104">In previous versions of Microsoft Dynamics 365 for Retail, returns against customer orders were processed by using the return order document in Retail Headquarters.</span></span> <span data-ttu-id="cf3bd-105">Kuid tagastustellimuse dokumenti saab kasutada vaid tagastatavate toodete töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-105">However, the return order document can be used to process only products that are being returned.</span></span> <span data-ttu-id="cf3bd-106">Tagastatud tooted on tagastustellimuse ridadel tähistatud negatiivse kogusega.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-106">The returned products are indicated by a negative quantity on the return order lines.</span></span> <span data-ttu-id="cf3bd-107">Müügid on aga tähistatud positiivse kogusega.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-107">By contrast, sales are indicated by a positive quantity.</span></span> <span data-ttu-id="cf3bd-108">Kuid tagastustellimuse dokument ei toeta positiivseid koguseid.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-108">However, the return order document doesn't support positive quantities.</span></span> <span data-ttu-id="cf3bd-109">Selle piirangu tõttu ei toetanud Retaili varasemad versioonid stsenaariume, kus tootevahetusi tehakse tagastustellimuse dokumenti kasutades.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-109">Because of this limitation, previous versions of Retail didn't support scenarios where product exchanges are done by using the return order document.</span></span>

<span data-ttu-id="cf3bd-110">Kuid nüüd on lisatud funktsioon tagastustellimuste vahetuste stsenaariumide toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-110">However, functionality has been added to support scenarios where exchanges are done on return orders.</span></span> <span data-ttu-id="cf3bd-111">Retail kasutab nüüd seda tüüpi kannete töötlemiseks tagastustellimuse dokumendi asemel müügitellimuse dokumenti.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-111">Retail now uses the sales order document instead of the return order document to process these types of transactions.</span></span>

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a><span data-ttu-id="cf3bd-112">Retaili konfigureerimine vahetuste toetamiseks tagastustellimustel</span><span class="sxs-lookup"><span data-stu-id="cf3bd-112">Configure Retail to support exchanges on return orders</span></span>

<span data-ttu-id="cf3bd-113">Järgige neid etappe süsteemi konfigureerimiseks nii, et see toetaks vahetusi tagastustellimustel.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-113">Follow these steps to configure the system to support exchanges on return orders.</span></span>

1. <span data-ttu-id="cf3bd-114">Valige suvandid **Retail \> Peakontori seadistamine \> Parameetrid \> Retaili parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-114">Go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**.</span></span> <span data-ttu-id="cf3bd-115">Määrake kiirkaardil **Kliendi tellimused** suvand **Töötle tagastustellimusi müügitellimustena** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-115">On the **Customer orders** FastTab, set the **Process return orders as sales orders** option to **Yes**.</span></span>
2. <span data-ttu-id="cf3bd-116">Käivitage töö **Globaalse konfiguratsiooni jaotusgraafik** (**1110**).</span><span class="sxs-lookup"><span data-stu-id="cf3bd-116">Run the **Global configuration distribution schedule** job (**1110**).</span></span>

## <a name="make-an-exchange"></a><span data-ttu-id="cf3bd-117">Vahetuse tegemine</span><span class="sxs-lookup"><span data-stu-id="cf3bd-117">Make an exchange</span></span>

<span data-ttu-id="cf3bd-118">Kui süsteem on eelmises jaotises kirjeldatud viisil konfigureeritud, valib kassa (POS) kasutaja endiselt müügitellimuse või müügiarve tagastuse töötlemiseks, nagu Retaili eelmistes versioonides.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-118">After the system is configured as described in the previous section, the point of sale (POS) user will still select a sales order or sales invoice to process a return, as in previous versions of Retail.</span></span> <span data-ttu-id="cf3bd-119">Kuid pärast tagastuskaupade lisamist korvi saab kasutaja lisada korvi uued müügiread.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-119">However, after the return items are added to the cart, the user will be able to add new sales lines to the cart.</span></span>

<span data-ttu-id="cf3bd-120">Nende müügiridade jaoks peab kasutaja määrama kõik atribuudid, mis on vajalikud kliendi tellimuse rea töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-120">For these new sales lines, the user must define all the attributes that are required in order to process a customer order line.</span></span> <span data-ttu-id="cf3bd-121">Need atribuudid on muu hulgas tarneviis ja täitmisasukoht.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-121">These attributes include the delivery method and fulfillment location.</span></span> <span data-ttu-id="cf3bd-122">Kandeks ootel makse on tagastustellimuse ridade ja müügitellimuse ridade netosumma.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-122">The payment that is due for the transaction will be a net of the return order lines and sales order lines.</span></span> <span data-ttu-id="cf3bd-123">Kui makse kandeks makstakse, postitatakse tagastustellimus programmis Retail Headquarters müügitellimuse dokumendina ja süsteem koostab kohe tagastusridade kohta arve.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-123">When payment is tendered for the transaction, the return order will be posted as a sales order document in Retail Headquarters, and the system will immediately invoice the return lines.</span></span>

<span data-ttu-id="cf3bd-124">Korvi eri summade paremaks nähtavuseks on korvi lisatud kolm uut summa välja.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-124">To provide better visibility into the various amounts for the cart, three new amount fields have been added to the cart.</span></span> <span data-ttu-id="cf3bd-125">Nende väljade kättesaadavaks muutmiseks kassa kasutajaliideses (UI) saate kasutada ekraanikoostajat.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-125">You can use the screen designer to make these new fields available in the POS user interface (UI).</span></span>

- <span data-ttu-id="cf3bd-126">**Rakendatud deposiit** – deposiidi summa, mis on kohaldatud kandele, kui kasutaja teeb kliendi tellimuse pealevõtmise.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-126">**Deposit applied** – The deposit amount that is applied on a transaction when the user does a customer order pickup.</span></span> <span data-ttu-id="cf3bd-127">Kui deposiidi alistamine puudub ja konfigureeritud on 10-protsendine deposiit, on summa selles väljas 90 protsenti kliendi tellimuse kogusummast.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-127">If there is no deposit override, and a 10-percent deposit is configured, the amount in this field is 90 percent of the total amount of the customer order.</span></span>
- <span data-ttu-id="cf3bd-128">**Realiseerimissumma** – kogusumma ridade kohta, kus tarneviis on seatud valikule **Tarne**, kui kliendi tellimus loodi või seda redigeeriti või kliendi tellimuse vahetuse ajal.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-128">**Carry out amount** – The total amount for lines where the delivery mode was set to **Carry out** when the customer order was created or edited, or during a customer order exchange.</span></span> <span data-ttu-id="cf3bd-129">Summa selles väljas sisaldab makse ja tasusid.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-129">The amount in this field includes taxes and charges.</span></span>
- <span data-ttu-id="cf3bd-130">**Tagastussumma** – kogusumma ridade kohta, kus on kliendi tellimuse vahetuse ajal negatiivne kogus.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-130">**Return amount** – The total amount for lines that have negative quantities during the customer order exchange.</span></span> <span data-ttu-id="cf3bd-131">Summa selles väljas sisaldab makse ja tasusid.</span><span class="sxs-lookup"><span data-stu-id="cf3bd-131">The amount in this field includes taxes and charges.</span></span>
