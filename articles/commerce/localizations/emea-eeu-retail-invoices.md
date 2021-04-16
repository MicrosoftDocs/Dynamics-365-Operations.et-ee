---
title: Kliendiarved ja tagastuse müügitellimused Ida-Euroopa riikides
description: See teema kirjeldab, kuidas sedistada teavet kliendiarvete ja tagastatavate müügitellimuste jaoks Ida-Euroopa riikides.
author: epopov
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: f79208b2508ed3879aa626389564b10a1d78c165
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798824"
---
# <a name="customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a><span data-ttu-id="b51d8-103">Kliendiarved ja tagastuse müügitellimused Ida-Euroopa riikides</span><span class="sxs-lookup"><span data-stu-id="b51d8-103">Customer invoices and return sales orders in Eastern European countries</span></span>


[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b51d8-104">See teema kirjeldab, kuidas sedistada teavet kliendiarvete ja tagastatavate müügitellimuste jaoks Ida-Euroopa riikides.</span><span class="sxs-lookup"><span data-stu-id="b51d8-104">This topic describes how to set up information for customer invoices and return sales orders in Eastern European countries.</span></span>

<span data-ttu-id="b51d8-105">Saate seadistada Retail POS-is loodud kliendiarvete ja tagastatavate müügitellimuste järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="b51d8-105">You can set up the following information for customer invoices and return sales orders that are generated in Retail point of sale (POS).</span></span>

- <span data-ttu-id="b51d8-106">Saate tagastatavaid müügitellimusi kasutades kasutada tagastuste käitlemiseks käibemaksugruppe.</span><span class="sxs-lookup"><span data-stu-id="b51d8-106">You can use sales tax groups to process returns by using return sales orders.</span></span> <span data-ttu-id="b51d8-107">Minge jaotisse **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="b51d8-107">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="b51d8-108">Avage vahekaart **Sisestamine \> Arve** ja seejärel määrake suvandi **Kasutage käibemaksugruppi tagastustele** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b51d8-108">Open the **Posting \> Invoice** tab, and then set **Use sales tax group for returns** to **Yes**.</span></span>

    * <span data-ttu-id="b51d8-109">Kliendi tehtud tagastuste jaoks käibemaksugrupi määramiseks valige käibemaksugrupp **Kliendi** lehel **Kaubanduse** kiirkaardil **Tagastuste käibemaksugrupi** väljal.</span><span class="sxs-lookup"><span data-stu-id="b51d8-109">To specify the sales tax group for returns that are made by a customer, on the **Customers** page, on the **Commerce** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="b51d8-110">Kliendile tagastatava müügitellimuse sisestamisel värskendatakse tagastatava müügitellimuse rida koos **Kliendi** vormil määratud tagasutste käibemaksugrupiga.</span><span class="sxs-lookup"><span data-stu-id="b51d8-110">When you post a return sales order for a customer, the return sales order line is updated with the sales tax group for returns that is specified in the **Customers** form.</span></span>
    * <span data-ttu-id="b51d8-111">Retail POS-is kliendi tehtud tagastuste jaoks käibemaksugrupi määramiseks valige **Kaupluste** lehel **Üldisel** kiirkaardil **Tagastuste käibemaksugrupi** väljal käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="b51d8-111">To specify a sales tax group for returns that are made at a retail POS by a customer, on the **Stores** page, on the **General** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="b51d8-112">Tagastatava müügitellimuse sisestamisel kaupluse kliendi jaoks värskendatakse tagastatava müügitellimuse rida **Kaupluste** lehel määratud tagastuste käibemaksugrupiga.</span><span class="sxs-lookup"><span data-stu-id="b51d8-112">When you post a return sales order for a customer of a  store, the return sales order line is updated with the sales tax group for returns that are specified on the **Stores** page.</span></span>

- <span data-ttu-id="b51d8-113">Kui arvel või tagastusel pole müügi vaikekuupäeva, saate arve või tagastuse müügikuupäevana kasutada kliendiarve või tagastatava müügitellimuse sisestuskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="b51d8-113">You can use the posting date of a customer invoice or a return sales order as the sales date of the invoice or return if the invoice or return does not have a default sales date.</span></span> <span data-ttu-id="b51d8-114">Minge jaotisse **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="b51d8-114">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="b51d8-115">Avage vahekaart **Sisestamine \> Arve** ja seejärel määrake suvandi **Kasutage sisestuskuupäeva müügikuupäevana** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b51d8-115">Open the **Posting \> Invoice** tab, and then set **Use posting date as sales date** to **Yes**.</span></span>
- <span data-ttu-id="b51d8-116">Saate Läti ja Leedu kliendiarvete ja tagastatavate müügitellimuste nummerdamiseks kasutada maksuameti esitatud numbrivahemikku.</span><span class="sxs-lookup"><span data-stu-id="b51d8-116">You can use the number range that is provided by the tax authorities to number Latvian and Lithuanian customer invoices and return sales orders.</span></span>

    * <span data-ttu-id="b51d8-117">Valige **Organisatsiooni haldus \> Numbriseeriad \> Loendurite haldamine**.</span><span class="sxs-lookup"><span data-stu-id="b51d8-117">Go to **Organization administration \> Number sequences \> Counters management**.</span></span> <span data-ttu-id="b51d8-118">Olemas peab olema kirje, kus **Moodul** = **Müük** ja **Tüüp** = **Arve**.</span><span class="sxs-lookup"><span data-stu-id="b51d8-118">There should be a record where **Module** = **Sales** and **Type** = **Invoice**.</span></span>
    * <span data-ttu-id="b51d8-119">Valige **Organisatsiooni haldus \> Numbriseeriad \> Arvete numeratsiooni seadistus**.</span><span class="sxs-lookup"><span data-stu-id="b51d8-119">Go to **Organization administration \> Number sequences \> Invoice numbering setup**.</span></span> <span data-ttu-id="b51d8-120">Märkige **Kaubanduse** märkeruut kliendiarvete nummerdamiseks kasutatava numbriseeria real.</span><span class="sxs-lookup"><span data-stu-id="b51d8-120">Select the **Commerce** check box for the number sequence line that is used to number the customer invoices.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]