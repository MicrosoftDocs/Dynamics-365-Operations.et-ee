---
title: Arve tükeldamise funktsioon
description: Selles teemas kirjeldatakse arvete tarneaadressi ja maksukonto numbri (TAN) tükeldamise seadistust ja funktsioone.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023183"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="e9fa4-103">Arve tükeldamise funktsioon</span><span class="sxs-lookup"><span data-stu-id="e9fa4-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9fa4-104">Selles teemas kirjeldatakse arvete tarneaadressi ja maksukonto numbri (TAN) tükeldamise seadistust ja funktsioone.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="e9fa4-105">Märkige **Ostureskontro parameetrite** lehel **Üldine** vahekaardil **Toote sissetulek** või **Arve** et sisestada ja tükeldada toote sissetulek või arve, mille tarneaadressid TAN-is on erinevad kui **Ostutellimuse** lehel.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="e9fa4-106">Seejärel tükeldatakse sisestatud arve tarneaadressi ja teenuseaadressi järgi.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="e9fa4-107">Kinnituse, komplekteerimislehe, saatelehe või arve sisestamiseks ja tükeldamiseks seadke **Koondvärskendus** vahekaardil **Tarneteave suvandi** kiirkaardil **Tarneteabe** suvandi **Kinnitus**, **Komplekteerimisleht**, **Saateleht** või **Arve** valik **Jah** kui müügitellimuse lehel on erinevate arveridade jaoks määratud erinevad **tarneaadressid** ja TAN-id.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="e9fa4-108">Seejärel tükeldatakse sisestatud arve tarneaadressi ja teenuseaadressi järgi.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="e9fa4-109">Kui **tarneteabe** valikud ei ole seatud valikule **Jah** sisestatakse arve üksiku arvena.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="e9fa4-110">Arve tükeldamist ei toimu.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="e9fa4-111">Saatelehe tükeldamiseks ja sisestamiseks, kus arve ridadel on erinevad tarneaadressid ja TAN-id, tuleb tarneteabe jaoks **Tarneteabe** **Saatelehe suvandi** väärtuseks seada **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="e9fa4-112">Saatelehe tükeldamiseks ja sisestamiseks, kus arve ridadel on erinevad tarneaadressid ja TAN-id, tuleb **Arve** suvand **Saatelehe teave** väärtuseks seada **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="e9fa4-113">Saatelehe sisestamiseks, kus arve ridadel on erinevad tarneaadressid, aga sama TAN, tuleb **Arve** valik **Tarne teave** suvand seada **Ei**.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="e9fa4-114">Seejärel tükeldatakse sisestatud arve tarneaadressi järgi.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="e9fa4-115">Näide</span><span class="sxs-lookup"><span data-stu-id="e9fa4-115">Example</span></span>

<span data-ttu-id="e9fa4-116">Selles näites on **Arve** valik **Tarne teave** seadistatud **Jah** **Koonduuendamise** vahekaardil **Ostureskontro parameetrite** lehel.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="e9fa4-117">Sisestatakse ostuarve, kus tarneaadresside ja TN-ide ridade seadistus on järgmine:</span><span class="sxs-lookup"><span data-stu-id="e9fa4-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="e9fa4-118">**Kauba rida 1:** Tarneaadress 1, ABCD-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="e9fa4-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="e9fa4-119">**Kauba rida 2:** Tarneaadress 1, ABCD-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="e9fa4-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="e9fa4-120">**Kauba rida 3:** Tarneaadress 2, ABCD-ABCD12345B</span><span class="sxs-lookup"><span data-stu-id="e9fa4-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="e9fa4-121">**Kauba rida 4:** Tarneaadress 3, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="e9fa4-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="e9fa4-122">Sel juhul tükeldatakse esialgne arve kaheks arveks ja sisestatakse järgmisel viisil:</span><span class="sxs-lookup"><span data-stu-id="e9fa4-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="e9fa4-123">Arve 1 sisestatakse kaubareale 1 ja kaubareale 2, kuna mõlemal real on sama tarneaadress ja tagasiarveldmiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="e9fa4-124">Arve 2 sisestatakse kaubareale 3.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="e9fa4-125">Arve 3 sisestatakse kaubareale 4.</span><span class="sxs-lookup"><span data-stu-id="e9fa4-125">Invoice 3 is posted for item line 4.</span></span>
