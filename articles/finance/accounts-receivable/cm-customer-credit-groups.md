---
title: Kliendi krediidigrupid
description: Selles teemas kirjeldatakse kliendi krediidigruppe.
author: mikefalkner
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3cdf4f7e72a55292c64b7a9191974242aab85a90
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835312"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="61b70-103">Kliendi krediidigrupid</span><span class="sxs-lookup"><span data-stu-id="61b70-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61b70-104">Saate määratleda kliendigrupid, kellel on jagatud krediidilimiit.</span><span class="sxs-lookup"><span data-stu-id="61b70-104">You can define groups of customers who have a shared credit limit.</span></span> <span data-ttu-id="61b70-105">Arvestatakse ka kliendiarve kontole määratletud individuaalset krediidilimiiti.</span><span class="sxs-lookup"><span data-stu-id="61b70-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="61b70-106">Kliendi krediidigrupi liikmeid saab valida erinevate juriidiliste isikute seast.</span><span class="sxs-lookup"><span data-stu-id="61b70-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="61b70-107">Kui lisate kliendi krediidigrupi klientide loendisse kliendi, muudetakse iga kliendi krediidilimiidi aegumiskuupäev grupile määratud aegumiskuupäevaks.</span><span class="sxs-lookup"><span data-stu-id="61b70-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="61b70-108">Kliendi krediidigruppe saate seadistada lehel **Kliendi krediidigrupid** (**Krediidihaldus \> Kliendi krediidigrupid \> Kliendi krediidigrupid**).</span><span class="sxs-lookup"><span data-stu-id="61b70-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="61b70-109">Sisestage väljadele **Grupi number** ja **Kirjeldus** grupi identifikaator ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="61b70-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="61b70-110">Sisestage väljadele **Krediidilimiit** ja **Valuuta** see krediidilimiit ja valuuta, mida tuleks kasutada, kui süsteem kontrollib grupi mõne liikme krediidilimiiti.</span><span class="sxs-lookup"><span data-stu-id="61b70-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="61b70-111">Väljale **Krediidilimiit kuupäevani** sisestage krediidilimiidi aegumise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="61b70-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="61b70-112">Kliendi krediidigruppidel peab olema aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="61b70-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="61b70-113">Kui olete kliendi krediidigrupi seadistamise lõpetanud, saate sellele kliente lisada, määratledes nende juriidilise isiku ja kliendi konto ID.</span><span class="sxs-lookup"><span data-stu-id="61b70-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="61b70-114">Kui lisate kliendi krediidigrupile uue kliendi, otsib süsteem kõigi juriidiliste isikute seast sama kliendikonto ja palub teil selle kliendi krediidigruppi lisada.</span><span class="sxs-lookup"><span data-stu-id="61b70-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="61b70-115">Kasutage menüüd **Aegunud saldod**, et vaadata kõigi kliendi krediidigrupi arveklientide aegumissaldo üksikasju.</span><span class="sxs-lookup"><span data-stu-id="61b70-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="61b70-116">Leht **Aegumissaldo** näitab arveklientide kontode aegunud saldosid.</span><span class="sxs-lookup"><span data-stu-id="61b70-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]