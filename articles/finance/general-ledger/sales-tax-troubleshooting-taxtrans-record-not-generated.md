---
title: Kirjet TaxTrans ei loodud
description: See teema pakub tõrkeotsingu teavet, mis võib aidata, kui Kirjet TaxTrans ei looda.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0c7414cc39198ff4d5be9b4c41ca62f9c78c9250
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947625"
---
# <a name="taxtrans-record-isnt-generated"></a><span data-ttu-id="80fb3-103">Kirjet TaxTrans ei loodud</span><span class="sxs-lookup"><span data-stu-id="80fb3-103">TaxTrans record isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80fb3-104">Kui valite kandele **Sisestatud käibemaks**, kuid **Sisestatud käibemaks** lehel pole maksuridu või puudub maksurida, ei pruugi kirje **TaxTrans** olla loodud.</span><span class="sxs-lookup"><span data-stu-id="80fb3-104">If you select **Posted sales tax** for a transaction, but the **Posted sales tax** page either shows no tax lines or is missing a tax line, the **TaxTrans** record might not have been generated.</span></span>

<span data-ttu-id="80fb3-105">[![Sisestatud käibemaksuleht, kus pole reaüksusi](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="80fb3-105">[![Posted sales tax page that has no line items](./media/taxtrans-is-not-generated-Picture1.png)](./media/taxtrans-is-not-generated-Picture1.png)</span></span>

<span data-ttu-id="80fb3-106">Selle probleemi tõrkeotsinguks järgige vastavalt järgmistele jaotistele juhiseid.</span><span class="sxs-lookup"><span data-stu-id="80fb3-106">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="check-the-sales-tax-before-you-post-the-transaction"></a><span data-ttu-id="80fb3-107">Kontrollige käibemaksu enne kande sisestamist</span><span class="sxs-lookup"><span data-stu-id="80fb3-107">Check the sales tax before you post the transaction</span></span>

1. <span data-ttu-id="80fb3-108">Enne kande sisestamist valige arvutuse kontrollimiseks **Arve sisestamise** lehel **Käibemaks**.</span><span class="sxs-lookup"><span data-stu-id="80fb3-108">Before you post the transaction, on the **Posting invoice** page, select **Sales tax** to check the calculation.</span></span>

    <span data-ttu-id="80fb3-109">[![Käibemaksu nupp lehel Arve sisestamine](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="80fb3-109">[![Sales tax button on the Posting invoice page](./media/taxtrans-is-not-generated-Picture2.png)](./media/taxtrans-is-not-generated-Picture2.png)</span></span>

2. <span data-ttu-id="80fb3-110">Vaadake **Ajutise käibemaksu kannete** lehel arvutuse tulemus üle.</span><span class="sxs-lookup"><span data-stu-id="80fb3-110">On the **Temporary sales tax transactions** page, review the result of the calculation.</span></span> <span data-ttu-id="80fb3-111">Kui maksu ei arvutata, vt [Maksu ei arvutata või maksusumma on null](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span><span class="sxs-lookup"><span data-stu-id="80fb3-111">If no tax is calculated, see [Tax isn't calculated or the tax amount is zero](sales-tax-troubleshooting-tax-not-calculated-amount-zero.md).</span></span>

## <a name="find-the-taxtrans-record-in-all-posted-sales-tax"></a><span data-ttu-id="80fb3-112">Leia kirje TaxTrans kõigis sisestatud käibemaksudes</span><span class="sxs-lookup"><span data-stu-id="80fb3-112">Find the TaxTrans record in all posted sales tax</span></span>

1. <span data-ttu-id="80fb3-113">Avage **Maks** \> **Päringud ja aruanded** \> **Käibemaksupäringud** > **Sisestatud käibemaks**.</span><span class="sxs-lookup"><span data-stu-id="80fb3-113">Go to **Tax** \> **Inquiries and reports** \> **Sales tax inquiries** > **Posted sales tax**.</span></span>
2. <span data-ttu-id="80fb3-114">Veerupäises **Kviitung** valige filtri sümbol, et leida kirje **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="80fb3-114">In the **Voucher** column heading, select the filter symbol to find the **TaxTrans** record.</span></span>
3. <span data-ttu-id="80fb3-115">Kui leiate otsitava käibemaksukirje, kontrollige kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="80fb3-115">If you find the sales tax records that you're looking for, check the date.</span></span> <span data-ttu-id="80fb3-116">Kui kuupäev erineb päevaraamatu päise kuupäevast, looge lisatoe saamiseks Microsofti teenusetaotlus.</span><span class="sxs-lookup"><span data-stu-id="80fb3-116">If the date differs from the date of the journal header, create a Microsoft service request for additional support.</span></span>

    <span data-ttu-id="80fb3-117">[![Sisestatud käibemaksu leht](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="80fb3-117">[![Posted sales tax page](./media/taxtrans-is-not-generated-Picture4.png)](./media/taxtrans-is-not-generated-Picture4.png)</span></span>

## <a name="debug-to-check-details"></a><span data-ttu-id="80fb3-118">Vigade parandamine üksikasjade kontrolliks</span><span class="sxs-lookup"><span data-stu-id="80fb3-118">Debug to check details</span></span>

1. <span data-ttu-id="80fb3-119">Teabe saamiseks selle kohta, kuidas vigasid parandada ja otsustada, kas **TmpTaxWorkTrans** ja **TaxUncommitted** on õigesti loodud, vaadake [TaxTransi välja väärtus on vale](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span><span class="sxs-lookup"><span data-stu-id="80fb3-119">For information about how to debug and determine whether **TmpTaxWorkTrans** and **TaxUncommitted** are correctly generated, see [Field value in TaxTrans is incorrect](sales-tax-troubleshooting-field-value-taxtrans-incorrect.md).</span></span>
2. <span data-ttu-id="80fb3-120">Kui **TaxTmpWorkTrans** või **TaxUncommitted** on õigesti loodud, lisage katkestuspunkt **TaxPost::SaveAndPost()** ja **Tax::SaveAndPost**, et parandada viga põhjusel, miks **TaxTrans** ei sisestatud.</span><span class="sxs-lookup"><span data-stu-id="80fb3-120">If **TaxTmpWorkTrans** or **TaxUncommitted** is correctly generated, add a breakpoint at **TaxPost::SaveAndPost()** and **Tax::SaveAndPost** to debug the reason why **TaxTrans** isn't inserted.</span></span>

    <span data-ttu-id="80fb3-121">[![Koodi lisatud katkestuspunktid](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="80fb3-121">[![Breakpoints added in code](./media/taxtrans-is-not-generated-Picture5.png)](./media/taxtrans-is-not-generated-Picture5.png)</span></span>

    <span data-ttu-id="80fb3-122">[![Lisatud katkestuspunktide tulemused](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="80fb3-122">[![Results of added breakpoints](./media/taxtrans-is-not-generated-Picture6.png)](./media/taxtrans-is-not-generated-Picture6.png)</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="80fb3-123">Kohanduse olemasolu tuvastamine</span><span class="sxs-lookup"><span data-stu-id="80fb3-123">Determine whether customization exists</span></span>

<span data-ttu-id="80fb3-124">Kui olete eelmistes jaotistes kirjeldatud toimingud teinud, kuid pole probleemi lahendada õnnestunud, tehke kindlaks, kas kohandamine on võimalik.</span><span class="sxs-lookup"><span data-stu-id="80fb3-124">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="80fb3-125">Kui kohandust ei ole, looge Microsofti teenusetaotlus edasise toe saamiseks.</span><span class="sxs-lookup"><span data-stu-id="80fb3-125">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
