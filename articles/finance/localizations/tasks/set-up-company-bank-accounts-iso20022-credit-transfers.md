---
title: Ettevõtte pangakontode seadistamine ISO20022 kreeditkorralduste jaoks
description: See protseduur näitab, kuidas seadistada ettevõttekohase pangakonto teavet, mis on nõutav maksefaili loomiseks.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e121ce7d87ee50a4e6b367a170eea4375d64fb3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442288"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="8792c-103">Ettevõtte pangakontode seadistamine ISO20022 kreeditkorralduste jaoks</span><span class="sxs-lookup"><span data-stu-id="8792c-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8792c-104">See protseduur näitab, kuidas seadistada ettevõttekohase pangakonto teavet, mis on nõutav maksefaili loomiseks.</span><span class="sxs-lookup"><span data-stu-id="8792c-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="8792c-105">Saate seadistada teabe, mis on vajalik ISO 20022 kreeditülekande vormingu loomiseks, kuid olenevalt vormingust võib olla vaja muud teavet, nt ettevõtte ID-d või sortimiskoodi.</span><span class="sxs-lookup"><span data-stu-id="8792c-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="8792c-106">Selle protseduuri loomiseks kasutatav demoandmete ettevõte on DEMF.</span><span class="sxs-lookup"><span data-stu-id="8792c-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="8792c-107">See on teine viiest protseduurist, mis illustreerib hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="8792c-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="8792c-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="8792c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="8792c-109">IBAN- ja SWIFT-koodi seadistamine</span><span class="sxs-lookup"><span data-stu-id="8792c-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="8792c-110">Avage Sularaha- ja pangahaldus > Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="8792c-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="8792c-111">Kasutage kiirfiltrit, et filtrida välja Pangakonto väärtusega DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="8792c-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="8792c-112">Klõpsake pangakonto üksikasjade avamiseks valikut DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="8792c-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="8792c-113">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="8792c-113">Click Edit.</span></span>
5. <span data-ttu-id="8792c-114">Laiendage jaotist Täiendav identifitseerimine.</span><span class="sxs-lookup"><span data-stu-id="8792c-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="8792c-115">Sisestage väljale IBAN väärtus DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="8792c-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="8792c-116">Sisestage väljale SWIFT-kood väärtus DEUTDEFF.</span><span class="sxs-lookup"><span data-stu-id="8792c-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="8792c-117">Pange tähele, et SWIFT\BIC pole paljude maksevormingute puhul nõutav, kuid soovitatav on see pangakonto jaoks registreerida.</span><span class="sxs-lookup"><span data-stu-id="8792c-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="8792c-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="8792c-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="8792c-119">Juriidilise isiku pangakonto seadistamine</span><span class="sxs-lookup"><span data-stu-id="8792c-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="8792c-120">Avage Organisatsiooni haldus > Organisatsioonid > Juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="8792c-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="8792c-121">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="8792c-121">Click Edit.</span></span>
3. <span data-ttu-id="8792c-122">Laiendage jaotist Pangakonto teave.</span><span class="sxs-lookup"><span data-stu-id="8792c-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="8792c-123">Sisestage väärtus väljale Pangakonto või valige see.</span><span class="sxs-lookup"><span data-stu-id="8792c-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="8792c-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="8792c-124">Click Save.</span></span>

