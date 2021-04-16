---
title: Ettevõtte pangakontode seadistamine ISO20022 kreeditkorralduste jaoks
description: See protseduur näitab, kuidas seadistada ettevõttekohase pangakonto teavet, mis on nõutav maksefaili loomiseks.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a3ddcae4a53fffa07bd386174811c12150f2f162
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819476"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="f9f1b-103">Ettevõtte pangakontode seadistamine ISO20022 kreeditkorralduste jaoks</span><span class="sxs-lookup"><span data-stu-id="f9f1b-103">Set up company bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9f1b-104">See protseduur näitab, kuidas seadistada ettevõttekohase pangakonto teavet, mis on nõutav maksefaili loomiseks.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-104">This procedure shows how to set up company-specific bank account information that is required for payment file generation.</span></span> <span data-ttu-id="f9f1b-105">Saate seadistada teabe, mis on vajalik ISO 20022 kreeditülekande vormingu loomiseks, kuid olenevalt vormingust võib olla vaja muud teavet, nt ettevõtte ID-d või sortimiskoodi.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-105">You set up information required to generate ISO 20022 credit transfer format but depending on the format there might be other information required, such as the Company ID or the Sort code.</span></span> 

<span data-ttu-id="f9f1b-106">Selle protseduuri loomiseks kasutatav demoandmete ettevõte on DEMF.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-106">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="f9f1b-107">See on teine viiest protseduurist, mis illustreerib hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-107">This is the second procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="f9f1b-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-iban-and-swift-code"></a><span data-ttu-id="f9f1b-109">IBAN- ja SWIFT-koodi seadistamine</span><span class="sxs-lookup"><span data-stu-id="f9f1b-109">Set up IBAN and SWIFT code</span></span>
1. <span data-ttu-id="f9f1b-110">Avage Sularaha- ja pangahaldus > Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-110">Go to Cash and bank management > Bank accounts.</span></span>
2. <span data-ttu-id="f9f1b-111">Kasutage kiirfiltrit, et filtrida välja Pangakonto väärtusega DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-111">Use the Quick Filter to filter on the Bank account field with a value of 'DEMF OPER'.</span></span>
3. <span data-ttu-id="f9f1b-112">Klõpsake pangakonto üksikasjade avamiseks valikut DEMF OPER.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-112">Click DEMF OPER to open bank account details.</span></span>
4. <span data-ttu-id="f9f1b-113">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-113">Click Edit.</span></span>
5. <span data-ttu-id="f9f1b-114">Laiendage jaotist Täiendav identifitseerimine.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-114">Expand the Additional identification section.</span></span>
6. <span data-ttu-id="f9f1b-115">Sisestage väljale IBAN väärtus DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-115">In the IBAN field, type 'DE89370400440532013000'.</span></span>
7. <span data-ttu-id="f9f1b-116">Sisestage väljale SWIFT-kood väärtus DEUTDEFF.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-116">In the SWIFT code field, type 'DEUTDEFF'.</span></span>
    * <span data-ttu-id="f9f1b-117">Pange tähele, et SWIFT\BIC pole paljude maksevormingute puhul nõutav, kuid soovitatav on see pangakonto jaoks registreerida.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-117">Note that SWIFT\BIC is not required for many payment formats, however it is recommended to have it registered for a bank account.</span></span>  
8. <span data-ttu-id="f9f1b-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-118">Click Save.</span></span>

## <a name="set-up-bank-account-for-the-legal-entity"></a><span data-ttu-id="f9f1b-119">Juriidilise isiku pangakonto seadistamine</span><span class="sxs-lookup"><span data-stu-id="f9f1b-119">Set up bank account for the legal entity</span></span>
1. <span data-ttu-id="f9f1b-120">Avage Organisatsiooni haldus > Organisatsioonid > Juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-120">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="f9f1b-121">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-121">Click Edit.</span></span>
3. <span data-ttu-id="f9f1b-122">Laiendage jaotist Pangakonto teave.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-122">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="f9f1b-123">Sisestage väärtus väljale Pangakonto või valige see.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-123">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="f9f1b-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f9f1b-124">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]