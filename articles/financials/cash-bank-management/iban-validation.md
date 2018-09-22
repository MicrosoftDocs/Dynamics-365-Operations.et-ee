---
title: Rahvusvahelise pangakonto numbri (IBAN) konto valideerimise haldamine
description: Selles teemas selgitatakse, kuidas hallata rahvusvahelise pangakonto numbri (IBAN) konto valideerimist.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: et-ee
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="5abd3-103">Rahvusvahelise pangakonto numbri (IBAN) konto valideerimise haldamine</span><span class="sxs-lookup"><span data-stu-id="5abd3-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5abd3-104">Rahvusvahelise pangakonto numbri (IBAN) konto valideerimine suurendab valideerimise hulka, mis tehakse IBAN-i lisamisel pangakontole.</span><span class="sxs-lookup"><span data-stu-id="5abd3-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="5abd3-105">IBAN-i struktuur salvestatakse rakendusse Microsoft Dynamics 365 for Finance and Operation ja see laaditakse automaatselt, kui IBAN-it esimest korda pangakontodel kasutate.</span><span class="sxs-lookup"><span data-stu-id="5abd3-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="5abd3-106">Pangakonto number on osa IBAN-i numbri jaoks määratud struktuurist.</span><span class="sxs-lookup"><span data-stu-id="5abd3-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="5abd3-107">Selle struktuuri põhjal saate hoiatusteateid, kui kontonumbri asukoht ja pikkus IBAN-is ei ühti struktuuris iga riigi või piirkonna jaoks määratud asukohaga.</span><span class="sxs-lookup"><span data-stu-id="5abd3-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="5abd3-108">IBAN-i struktuuride seadistamine</span><span class="sxs-lookup"><span data-stu-id="5abd3-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="5abd3-109">Minge jaotisse **Sularaha- ja pangahaldus \> Seadistus \> IBAN-i struktuurid**.</span><span class="sxs-lookup"><span data-stu-id="5abd3-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="5abd3-110">Pange tähele, et iga riigi või piirkonna IBAN-i struktuurid on automaatselt seadistatud.</span><span class="sxs-lookup"><span data-stu-id="5abd3-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="5abd3-111">Kui teil on vaja struktuure konkreetse riigi või piirkonna jaoks kohandada, saate neid redigeerida.</span><span class="sxs-lookup"><span data-stu-id="5abd3-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="5abd3-112">Struktuuri definitsioonid on osa igast uuest väljaandest.</span><span class="sxs-lookup"><span data-stu-id="5abd3-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="5abd3-113">Pärast iga uuendust uusimate definitsioonide laadimiseks võite kasutada menüüd **Lähtesta struktuurid**.</span><span class="sxs-lookup"><span data-stu-id="5abd3-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="5abd3-114">IBAN-i struktuuri valideerimine pangakontol</span><span class="sxs-lookup"><span data-stu-id="5abd3-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="5abd3-115">Minge jaotisse **Sularaha- ja pangahaldus \> Pangakontod \> Pangakontod**.</span><span class="sxs-lookup"><span data-stu-id="5abd3-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="5abd3-116">Looge pangakonto.</span><span class="sxs-lookup"><span data-stu-id="5abd3-116">Create a bank account.</span></span>
3. <span data-ttu-id="5abd3-117">Sisestage IBAN kiirkaardile **Lisateave**.</span><span class="sxs-lookup"><span data-stu-id="5abd3-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="5abd3-118">Teile kuvatakse teade, kui kontonumbri asukoht ja pikkus IBAN-is ei ühti struktuuris iga riigi või piirkonna jaoks määratud asukohaga.</span><span class="sxs-lookup"><span data-stu-id="5abd3-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="5abd3-119">Te ei saa jätkata, kui IBAN-i pikkus ei ühti pikkusega IBAN-i struktuuris.</span><span class="sxs-lookup"><span data-stu-id="5abd3-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="5abd3-120">Valideerimine kontrollib ka seda, kas pangakonto number ühtib IBAN-i osaga, mis kujutab pangakonto numbrit.</span><span class="sxs-lookup"><span data-stu-id="5abd3-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="5abd3-121">Kui pangakonto number ei ühti, kuvatakse hoiatusteade.</span><span class="sxs-lookup"><span data-stu-id="5abd3-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="5abd3-122">See teade on ainult hoiatus.</span><span class="sxs-lookup"><span data-stu-id="5abd3-122">This message is only a warning.</span></span> <span data-ttu-id="5abd3-123">Saate jätkata, isegi kui pangakonto number ei ühti.</span><span class="sxs-lookup"><span data-stu-id="5abd3-123">You can continue even if the bank account number doesn't match.</span></span>

