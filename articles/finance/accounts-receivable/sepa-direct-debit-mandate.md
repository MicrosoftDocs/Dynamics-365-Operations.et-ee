---
title: SEPA otsedeebeti loa seadistamine
description: Ühtse euromaksete piirkonna (Single Euro Payment Area, SEPA) otsekorraldus võimaldab kreeditoril võtta vahendeid kliendi pangakontolt eeldusel, et klient on andnud kreeditorile allkirjastatud loa.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aba265e69bde9a9c194147d6ee6a806e9b2bd7c2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442266"
---
# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="454b7-103">SEPA otsedeebeti loa seadistamine</span><span class="sxs-lookup"><span data-stu-id="454b7-103">Set up SEPA direct debit mandate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="454b7-104">Ühtse euromaksete piirkonna (Single Euro Payment Area, SEPA) otsekorraldus võimaldab kreeditoril võtta vahendeid kliendi pangakontolt eeldusel, et klient on andnud kreeditorile allkirjastatud loa.</span><span class="sxs-lookup"><span data-stu-id="454b7-104">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="454b7-105">Kliendi allkirjastatud luba volitab kreeditori makset koguma ja annab kliendi pangale juhise see välja maksta.</span><span class="sxs-lookup"><span data-stu-id="454b7-105">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="454b7-106">See teema on korraldatud nii, et näidata SEPA otsedeebeti mandaatide seadistamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="454b7-106">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="454b7-107">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="454b7-107">Prerequisites</span></span>
<span data-ttu-id="454b7-108">Järgmises tabelis kuvatakse eeltingimused, mis peavad olema asukohakorralduse loomiseks täidetud.</span><span class="sxs-lookup"><span data-stu-id="454b7-108">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="454b7-109">Kategooria</span><span class="sxs-lookup"><span data-stu-id="454b7-109">Category</span></span>       | <span data-ttu-id="454b7-110">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="454b7-110">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="454b7-111">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="454b7-111">Country/region</span></span> | <span data-ttu-id="454b7-112">Juriidilise isiku peamine aadress peab olema järgmistes riikides/regioonides: Austria, Belgia, Saksamaa, Hispaania, Prantsusmaa, Itaalia või Holland.</span><span class="sxs-lookup"><span data-stu-id="454b7-112">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="454b7-113">Seadistage otsedeebeti lubade jaoks numbriseeria. Igal otsedeebeti loal peab olema unikaalne number.</span><span class="sxs-lookup"><span data-stu-id="454b7-113">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="454b7-114">Looge lehel **Numbriseeriad** otsekorralduse lubade numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="454b7-114">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="454b7-115">Selle identifikaatoriga määrate numbriseeria otsekorralduse lubade süsteemile lehel **Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="454b7-115">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="454b7-116">Müügireskontro parameetrite seadistamine otsedeebeti mandaatidele Kasutage lehte **Müügireskontro parameetrid**, et otsedeebeti lubade jaoks parameetreid seadistada.</span><span class="sxs-lookup"><span data-stu-id="454b7-116">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="454b7-117">Parameetrite seadistamiseks muutke vahekaardil **Otsedeebet** muutke vaikeparameetreid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="454b7-117">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="454b7-118">Seejärel vahekaardil **Numbriseeriad** värskendage välja **Otsedeebeti loa ID** varasemalt seadistatud numbriseeriaga.</span><span class="sxs-lookup"><span data-stu-id="454b7-118">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="454b7-119">Otsedeebeti lubade makseviisi seadistamine Peate otsedeebeti lubade jaoks maksemeetodi seadistama.</span><span class="sxs-lookup"><span data-stu-id="454b7-119">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="454b7-120">Selle makseviisiga saate teha päringuid arvete kohta, mille jaoks loote otsekorralduse makseid.</span><span class="sxs-lookup"><span data-stu-id="454b7-120">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="454b7-121">Seadistage lehel **Makseviisid** makseviis.</span><span class="sxs-lookup"><span data-stu-id="454b7-121">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="454b7-122">Otsekorralduse lubadele makseviisi seadistamiseks tuleb järgida makseviisi puhul neid lisajuhiseid.</span><span class="sxs-lookup"><span data-stu-id="454b7-122">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="454b7-123">Tehke väljal **Makse tüüp** valik **Elektrooniline makse**.</span><span class="sxs-lookup"><span data-stu-id="454b7-123">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="454b7-124">Valikuline: kui ootate, et igal kliendil on mitu luba, valige väljal **Periood** suvand **Arve**.</span><span class="sxs-lookup"><span data-stu-id="454b7-124">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="454b7-125">Sel juhul luuakse iga arve kohta eraldi makse ja iga makse kasutab arve jaoks määratud luba.</span><span class="sxs-lookup"><span data-stu-id="454b7-125">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="454b7-126">Valige **Nõua luba** maksete loomiseks otsekorralduse lubadega.</span><span class="sxs-lookup"><span data-stu-id="454b7-126">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="454b7-127">Valik **Nõua luba** on saadaval ainult juhul, kui teete valiku **Elektrooniline makse** väljal **Makse tüüp**.</span><span class="sxs-lookup"><span data-stu-id="454b7-127">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="454b7-128">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="454b7-128">Additional resources</span></span>

[<span data-ttu-id="454b7-129">SEPA otsekorralduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="454b7-129">SEPA direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="454b7-130">Kliendi jaoks otsekorralduse loa loomine</span><span class="sxs-lookup"><span data-stu-id="454b7-130">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 

