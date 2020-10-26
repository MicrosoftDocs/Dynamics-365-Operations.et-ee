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
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 28abef376e8462c9a69dbd8e5033ea799b6a4b3a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977811"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="66f5f-103">Rahvusvahelise pangakonto numbri (IBAN) konto valideerimise haldamine</span><span class="sxs-lookup"><span data-stu-id="66f5f-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66f5f-104">Rahvusvahelise pangakonto numbri (IBAN) valideerimine suurendab valideerimise hulka, mis tehakse IBAN-i lisamisel pangakontole.</span><span class="sxs-lookup"><span data-stu-id="66f5f-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="66f5f-105">Teavet IBAN-i struktuuri kohta talletatakse rakenduses Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="66f5f-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="66f5f-106">See teave laaditakse automaatselt, kui kasutate pangakontodel esmakordselt IBAN-i.</span><span class="sxs-lookup"><span data-stu-id="66f5f-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="66f5f-107">See sisaldab IBAN-i pikkust, pangakonto numbri ja protsessinumbri alguspositsioone ning pangakonto numbri ja protsessinumbri pikkuseid.</span><span class="sxs-lookup"><span data-stu-id="66f5f-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="66f5f-108">IBAN-i struktuuride seadistamine</span><span class="sxs-lookup"><span data-stu-id="66f5f-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="66f5f-109">Minge jaotisse **Sularaha- ja pangahaldus \> Seadistus \> IBAN-i struktuurid**.</span><span class="sxs-lookup"><span data-stu-id="66f5f-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="66f5f-110">Pange tähele, et iga riigi või piirkonna IBAN-i struktuurid on automaatselt seadistatud.</span><span class="sxs-lookup"><span data-stu-id="66f5f-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="66f5f-111">Kui tahate struktuure konkreetse riigi või piirkonna jaoks kohandada, saate neid redigeerida.</span><span class="sxs-lookup"><span data-stu-id="66f5f-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="66f5f-112">Struktuuri definitsioonid on osa igast uuest väljaandest.</span><span class="sxs-lookup"><span data-stu-id="66f5f-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="66f5f-113">Pärast iga uuendust uusimate definitsioonide laadimiseks võite kasutada menüüd **Lähtesta struktuurid**.</span><span class="sxs-lookup"><span data-stu-id="66f5f-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="66f5f-114">IBAN-i struktuuri valideerimine pangakontol</span><span class="sxs-lookup"><span data-stu-id="66f5f-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="66f5f-115">Minge jaotisse **Sularaha- ja pangahaldus \> Pangakontod \> Pangakontod**.</span><span class="sxs-lookup"><span data-stu-id="66f5f-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="66f5f-116">Looge pangakonto.</span><span class="sxs-lookup"><span data-stu-id="66f5f-116">Create a bank account.</span></span>
3. <span data-ttu-id="66f5f-117">Sisestage IBAN kiirkaardile **Lisateave**.</span><span class="sxs-lookup"><span data-stu-id="66f5f-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="66f5f-118">Kui IBAN-i pikkus ei kattu iga riigi või regiooni jaoks määratletud pikkusega, kuvatakse hoiatusteade.</span><span class="sxs-lookup"><span data-stu-id="66f5f-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="66f5f-119">Te ei saa jätkata, kui IBAN-i pikkus ei ühti IBAN-i struktuuris määratletud pikkusega.</span><span class="sxs-lookup"><span data-stu-id="66f5f-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="66f5f-120">Valideerimine kontrollib ka seda, kas pangakonto number ühtib IBAN-i osaga, mis kujutab pangakonto numbrit.</span><span class="sxs-lookup"><span data-stu-id="66f5f-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="66f5f-121">Kui pangakonto number ei ühti, kuvatakse hoiatusteade.</span><span class="sxs-lookup"><span data-stu-id="66f5f-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="66f5f-122">See teade on ainult hoiatus.</span><span class="sxs-lookup"><span data-stu-id="66f5f-122">This message is only a warning.</span></span> <span data-ttu-id="66f5f-123">Saate jätkata, isegi kui pangakonto number ei ühti.</span><span class="sxs-lookup"><span data-stu-id="66f5f-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="66f5f-124">Valideerimine kontrollib ka seda, kas protsessikood ühtib IBAN-i osaga, mis kujutab panga protsessikoodi.</span><span class="sxs-lookup"><span data-stu-id="66f5f-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="66f5f-125">Protsessikood sisaldab panga numbrit ja sageli ka täiendavat panga filiaali.</span><span class="sxs-lookup"><span data-stu-id="66f5f-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="66f5f-126">Kui panga protsessikood ei ühti, kuvatakse hoiatusteade.</span><span class="sxs-lookup"><span data-stu-id="66f5f-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="66f5f-127">See teade on ainult hoiatus.</span><span class="sxs-lookup"><span data-stu-id="66f5f-127">This message is only a warning.</span></span> <span data-ttu-id="66f5f-128">Saate jätkata, isegi kui panga protsessikood ei ühti.</span><span class="sxs-lookup"><span data-stu-id="66f5f-128">You can continue even if the bank routing number doesn't match.</span></span>
