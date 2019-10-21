---
title: Rahvusvahelise pangakonto numbri (IBAN) konto valideerimise haldamine
description: Selles teemas selgitatakse, kuidas hallata rahvusvahelise pangakonto numbri (IBAN) konto valideerimist.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: a4f9bc2a22aabc7b83eb15665f37849d505e1b6b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177376"
---
# <a name="manage-international-bank-account-number-iban-validation"></a><span data-ttu-id="1e0aa-103">Rahvusvahelise pangakonto numbri (IBAN) valideerimise haldamine</span><span class="sxs-lookup"><span data-stu-id="1e0aa-103">Manage International Bank Account Number (IBAN) validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e0aa-104">Rahvusvahelise pangakonto numbri (IBAN) valideerimine suurendab valideerimise hulka, mis tehakse IBAN-i lisamisel pangakontole.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="1e0aa-105">Teavet IBAN-i struktuuri kohta talletatakse rakenduses Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="1e0aa-106">See teave laaditakse automaatselt, kui kasutate pangakontodel esmakordselt IBAN-i.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="1e0aa-107">See sisaldab IBAN-i pikkust, pangakonto numbri ja protsessinumbri alguspositsioone ning pangakonto numbri ja protsessinumbri pikkuseid.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="1e0aa-108">IBAN-i struktuuride seadistamine</span><span class="sxs-lookup"><span data-stu-id="1e0aa-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="1e0aa-109">Minge jaotisse **Sularaha- ja pangahaldus \> Seadistus \> IBAN-i struktuurid**.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="1e0aa-110">Pange tähele, et iga riigi või piirkonna IBAN-i struktuurid on automaatselt seadistatud.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="1e0aa-111">Kui tahate struktuure konkreetse riigi või piirkonna jaoks kohandada, saate neid redigeerida.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="1e0aa-112">Struktuuri definitsioonid on osa igast uuest väljaandest.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="1e0aa-113">Pärast iga uuendust uusimate definitsioonide laadimiseks võite kasutada menüüd **Lähtesta struktuurid**.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="1e0aa-114">IBAN-i struktuuri valideerimine pangakontol</span><span class="sxs-lookup"><span data-stu-id="1e0aa-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="1e0aa-115">Minge jaotisse **Sularaha- ja pangahaldus \> Pangakontod \> Pangakontod**.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="1e0aa-116">Looge pangakonto.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-116">Create a bank account.</span></span>
3. <span data-ttu-id="1e0aa-117">Sisestage IBAN kiirkaardile **Lisateave**.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="1e0aa-118">Kui IBAN-i pikkus ei kattu iga riigi või regiooni jaoks määratletud pikkusega, kuvatakse hoiatusteade.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="1e0aa-119">Te ei saa jätkata, kui IBAN-i pikkus ei ühti IBAN-i struktuuris määratletud pikkusega.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="1e0aa-120">Valideerimine kontrollib ka seda, kas pangakonto number ühtib IBAN-i osaga, mis kujutab pangakonto numbrit.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="1e0aa-121">Kui pangakonto number ei ühti, kuvatakse hoiatusteade.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="1e0aa-122">See teade on ainult hoiatus.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-122">This message is only a warning.</span></span> <span data-ttu-id="1e0aa-123">Saate jätkata, isegi kui pangakonto number ei ühti.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="1e0aa-124">Valideerimine kontrollib ka seda, kas protsessikood ühtib IBAN-i osaga, mis kujutab panga protsessikoodi.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="1e0aa-125">Protsessikood sisaldab panga numbrit ja sageli ka täiendavat panga filiaali.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="1e0aa-126">Kui panga protsessikood ei ühti, kuvatakse hoiatusteade.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="1e0aa-127">See teade on ainult hoiatus.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-127">This message is only a warning.</span></span> <span data-ttu-id="1e0aa-128">Saate jätkata, isegi kui panga protsessikood ei ühti.</span><span class="sxs-lookup"><span data-stu-id="1e0aa-128">You can continue even if the bank routing number doesn't match.</span></span>
