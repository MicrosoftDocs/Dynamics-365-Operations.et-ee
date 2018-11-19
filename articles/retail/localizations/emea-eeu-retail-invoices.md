---
title: "Retaili kliendiarved ja tagastuse müügitellimused Ida-Euroopa riikides"
description: "See teema kirjeldab, kuidas sedistada teavet kliendiarvete ja tagastatavate müügitellimuste jaoks Ida-Euroopa riikides."
author: epopov
manager: annbe
ms.date: 10/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 01239f0eff3e59f62188fca64f99e93be843d2e2
ms.openlocfilehash: 20ae19fb03acb075b6553b95808779c905bcd31b
ms.contentlocale: et-ee
ms.lasthandoff: 10/24/2018

---

# <a name="retail-customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a><span data-ttu-id="1aae9-103">Retaili kliendiarved ja tagastuse müügitellimused Ida-Euroopa riikides</span><span class="sxs-lookup"><span data-stu-id="1aae9-103">Retail customer invoices and return sales orders in Eastern European countries</span></span>


[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1aae9-104">See teema kirjeldab, kuidas sedistada teavet kliendiarvete ja tagastatavate müügitellimuste jaoks Ida-Euroopa riikides.</span><span class="sxs-lookup"><span data-stu-id="1aae9-104">This topic describes how to set up information for customer invoices and return sales orders in Eastern European countries.</span></span>

<span data-ttu-id="1aae9-105">Saate seadistada Retail POS-is loodud kliendiarvete ja tagastatavate müügitellimuste järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="1aae9-105">You can set up the following information for customer invoices and return sales orders that are generated in Retail point of sale (POS).</span></span>

- <span data-ttu-id="1aae9-106">Saate tagastatavaid müügitellimusi kasutades kasutada tagastuste käitlemiseks käibemaksugruppe.</span><span class="sxs-lookup"><span data-stu-id="1aae9-106">You can use sales tax groups to process returns by using return sales orders.</span></span> <span data-ttu-id="1aae9-107">Avage **Jaemüük > Haldamise seadistamine > Parameetrid > Jaemüügi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1aae9-107">Go to **Retail > Headquarters setup > Parameters > Retail parameters**.</span></span> <span data-ttu-id="1aae9-108">Avage **Sisestamine > Arve** vahekaart ning seejärel määrake **Käibemaksugruppide kasutamine tagastusteks** olekuks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1aae9-108">Open the **Posting > Invoice** tab, and then set **Use sales tax group for returns** to **Yes**.</span></span> 

  * <span data-ttu-id="1aae9-109">Kliendi tehtud tagastuste jaoks käibemaksugrupi määramiseks valige käibemaksugrupp **Kliendi** lehel **Jaemüügi** kiirkaardil **Tagastuste käibemaksugrupi** väljal.</span><span class="sxs-lookup"><span data-stu-id="1aae9-109">To specify the sales tax group for returns that are made by a customer, on the **Customers** page, on the **Retail** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="1aae9-110">Kliendile tagastatava müügitellimuse sisestamisel värskendatakse tagastatava müügitellimuse rida koos **Kliendi** vormil määratud tagasutste käibemaksugrupiga.</span><span class="sxs-lookup"><span data-stu-id="1aae9-110">When you post a return sales order for a customer, the return sales order line is updated with the sales tax group for returns that is specified in the **Customers** form.</span></span>
  
  * <span data-ttu-id="1aae9-111">Retail POS-is kliendi tehtud tagastuste jaoks käibemaksugrupi määramiseks valige **Kaupluste** lehel **Üldisel** kiirkaardil **Tagastuste käibemaksugrupi** väljal käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="1aae9-111">To specify a sales tax group for returns that are made at a retail POS by a customer, on the **Stores** page, on the **General** FastTab, in the **Sales tax group for returns** field, select a sales tax group.</span></span> <span data-ttu-id="1aae9-112">Tagastatava müügitellimuse sisestamisel kaupluse kliendi jaoks värskendatakse tagastatava müügitellimuse rida **Kaupluste** lehel määratud tagastuste käibemaksugrupiga.</span><span class="sxs-lookup"><span data-stu-id="1aae9-112">When you post a return sales order for a customer of a retail store, the return sales order line is updated with the sales tax group for returns that are specified on the **Stores** page.</span></span>

- <span data-ttu-id="1aae9-113">Kui arvel või tagastusel pole müügi vaikekuupäeva, saate arve või tagastuse müügikuupäevana kasutada jaemüügi kliendiarve või tagastatava müügiarve sisestuskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="1aae9-113">You can use the posting date of a retail customer invoice or a return sales order as the sales date of the invoice or return if the invoice or return does not have a default sales date.</span></span> <span data-ttu-id="1aae9-114">Avage **Jaemüük > Haldamise seadistamine > Parameetrid > Jaemüügi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1aae9-114">Go to **Retail > Headquarters setup > Parameters > Retail parameters**.</span></span> <span data-ttu-id="1aae9-115">Avage **Sisestamine > Arve** vahekaart ning seejärel määrake **Sisestuskuupäeva kasutamine müügikuupäevana** olekuks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1aae9-115">Open the **Posting > Invoice** tab, and then set **Use posting date as sales date** to **Yes**.</span></span>

- <span data-ttu-id="1aae9-116">Saate Läti ja Leedu kliendiarvete ja tagastatavate müügitellimuste nummerdamiseks kasutada maksuameti esitatud numbrivahemikku.</span><span class="sxs-lookup"><span data-stu-id="1aae9-116">You can use the number range that is provided by the tax authorities to number Latvian and Lithuanian customer invoices and return sales orders.</span></span> 

  * <span data-ttu-id="1aae9-117">Avage **Organisatsiooni haldus > Numbriseeriad > Loendurite haldamine**.</span><span class="sxs-lookup"><span data-stu-id="1aae9-117">Go to **Organization administration > Number sequences > Counters management**.</span></span> <span data-ttu-id="1aae9-118">Olemas peab olema kirje, kus **Moodul** = **Müük** ja **Tüüp** = **Arve**.</span><span class="sxs-lookup"><span data-stu-id="1aae9-118">There should be a record where **Module** = **Sales** and **Type** = **Invoice**.</span></span>

  * <span data-ttu-id="1aae9-119">Avage **Organisatsiooni haldus > Numbriseeriad > Arvete numeratsiooni seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="1aae9-119">Go to **Organization administration > Number sequences > Invoice numbering setup**.</span></span> <span data-ttu-id="1aae9-120">Märkige **Jaemüügi** märkeruut kliendiarvete nummerdamseks kasutatava numbriseeria real.</span><span class="sxs-lookup"><span data-stu-id="1aae9-120">Select the **Retail** check box for the number sequence line that is used to number the customer invoices.</span></span>
