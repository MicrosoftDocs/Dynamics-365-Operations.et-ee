---
title: Kohaldatavate hindade ja allahindluste otsimine
description: See protseduur näitab, kuidas leida kindlale kliendile kehtivat toote hinda ja/või allahindlust ilma müügitellimust loomata.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba95e651898da0e0fbd1221f61436ffac59db09e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "359861"
---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="93a1a-103">Kohaldatavate hindade ja allahindluste otsimine</span><span class="sxs-lookup"><span data-stu-id="93a1a-103">Look up applicable prices and discounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93a1a-104">See protseduur näitab, kuidas leida kindlale kliendile kehtivat toote hinda ja/või allahindlust ilma müügitellimust loomata.</span><span class="sxs-lookup"><span data-stu-id="93a1a-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="93a1a-105">Protseduur selgitab konkreetse näite kaudu, kuidas valida vajalikud väärtused, kasutades demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="93a1a-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="93a1a-106">Kohalduva hinna leidmine</span><span class="sxs-lookup"><span data-stu-id="93a1a-106">Find the applicable price</span></span>
1. <span data-ttu-id="93a1a-107">Avage Müük ja turundus > Hinnad ja allahindlused > Hindade otsimine.</span><span class="sxs-lookup"><span data-stu-id="93a1a-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="93a1a-108">Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="93a1a-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="93a1a-109">Leidke ja valige loendist klient US-001.</span><span class="sxs-lookup"><span data-stu-id="93a1a-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="93a1a-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="93a1a-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="93a1a-111">Sisestage väljale Kaubakood tüüp T0004.</span><span class="sxs-lookup"><span data-stu-id="93a1a-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="93a1a-112">Vaikimisi on välja Kogus väärtuseks määratud 1.</span><span class="sxs-lookup"><span data-stu-id="93a1a-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="93a1a-113">Kui aga teate, kui suurt tellimust soovib klient kõnealusele tootele teha, sisestage see väärtus.</span><span class="sxs-lookup"><span data-stu-id="93a1a-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="93a1a-114">See teave on oluline, kui kliendiga sõlmitud kaubanduslepetel on kogusekatkestusi, mis tähendab, et toote hind sõltub minimaalsest ostetud kogusest.</span><span class="sxs-lookup"><span data-stu-id="93a1a-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="93a1a-115">Sisestage väljale Kuupäev see kuupäev, millal klient soovib tellimuse esitada.</span><span class="sxs-lookup"><span data-stu-id="93a1a-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="93a1a-116">Kuupäev võib olla täna või millal tahes tulevikus.</span><span class="sxs-lookup"><span data-stu-id="93a1a-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="93a1a-117">Süsteem tagastab nüüd hinna, mis kehtib valitud tootele, kui valitud klient on selle ostnud valitud kuupäeval ja määratud koguses.</span><span class="sxs-lookup"><span data-stu-id="93a1a-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="93a1a-118">Selles näites: kui klient US-001 ostis täna 1 ühiku toodet T0004, peab ta maksma 350 Kanda dollarit ühiku eest.</span><span class="sxs-lookup"><span data-stu-id="93a1a-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="93a1a-119">Hind tuleneb kliendiga sõlmitud olemasolevast ja aktiivsest kaubandusleppest.</span><span class="sxs-lookup"><span data-stu-id="93a1a-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="93a1a-120">Lehe muud väljad pakuvad lisateavet toote hinna ja toote kulu kohta (kui need on tooteetalonis seadistatud) ning arvutatud tulususe.</span><span class="sxs-lookup"><span data-stu-id="93a1a-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="93a1a-121">Kui valitud on suvand Kuva seotud tootevariandid, tähendab see, et toote variantide kohta on olemas täiendavad kaubanduslepped.</span><span class="sxs-lookup"><span data-stu-id="93a1a-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="93a1a-122">Märkige ruut Kuva seotud tootevariandid.</span><span class="sxs-lookup"><span data-stu-id="93a1a-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="93a1a-123">Kuvatakse tootevariantide loend koos teabega nende dimensioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="93a1a-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="93a1a-124">Märkige loendis valget värvi tähistav rida.</span><span class="sxs-lookup"><span data-stu-id="93a1a-124">In the list, mark the line representing color White.</span></span>
    * <span data-ttu-id="93a1a-125">Pange tähele, et toote hind erineb nüüd varem kuvatust, kui see polnud veel dimensiooni kohta määratud.</span><span class="sxs-lookup"><span data-stu-id="93a1a-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="93a1a-126">Klõpsake suvandit Kuva müügihinnad.</span><span class="sxs-lookup"><span data-stu-id="93a1a-126">Click View sales prices.</span></span>
    * <span data-ttu-id="93a1a-127">Lehel Hind (müük) kuvatakse kõik toote, k.a selle variantide puhul kehtivad kaubanduslepped.</span><span class="sxs-lookup"><span data-stu-id="93a1a-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="93a1a-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="93a1a-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="93a1a-129">Kohalduva allahindluse leidmine</span><span class="sxs-lookup"><span data-stu-id="93a1a-129">Find the applicable discount</span></span>
    * <span data-ttu-id="93a1a-130">Veenduge, et väli Kliendi konto sisaldab kliendinumbrit US-001. </span><span class="sxs-lookup"><span data-stu-id="93a1a-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="93a1a-131">Sisestage väljale Kaubakood tüüp T0012.</span><span class="sxs-lookup"><span data-stu-id="93a1a-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="93a1a-132">Veenduge, et välja Kogus väärtuseks oleks määratud 1.</span><span class="sxs-lookup"><span data-stu-id="93a1a-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="93a1a-133">Järgmised toote T0012 kohta kuvatavad hinnakujunduse üksikasjad pärinevad ühest või mitmest kaubandusleppest. Ühiku hind on 1000 Kanada dollarit ja allahindlusprotsent 5.</span><span class="sxs-lookup"><span data-stu-id="93a1a-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="93a1a-134">Määrake koguse väärtuseks 20.</span><span class="sxs-lookup"><span data-stu-id="93a1a-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="93a1a-135">Tellimuse koguse suurendamisel pakutakse kliendile rea allahindlust 5 protsendilt 7-le.</span><span class="sxs-lookup"><span data-stu-id="93a1a-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="93a1a-136">Netosumma arvutatakse ühiku hinna, allahindluse ja lõpliku koguse alusel.</span><span class="sxs-lookup"><span data-stu-id="93a1a-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="93a1a-137">Klõpsake suvandit Kuva rea allahindlus.</span><span class="sxs-lookup"><span data-stu-id="93a1a-137">Click View line discount.</span></span>
    * <span data-ttu-id="93a1a-138">Tootel T0012 on kaks rea allahindluse lepet, mis määrab 5-protsendise allahindluse tellimuserea kogusele 1 kuni 10 ja 7-protsendise allahindluse tellimuse kogustele üle 10.</span><span class="sxs-lookup"><span data-stu-id="93a1a-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="93a1a-139">Pange tähele, et allahindlused rakenduvad tootegrupile, siinses näiteks grupile koodiga 01, millesse toode T0012 kuulub.</span><span class="sxs-lookup"><span data-stu-id="93a1a-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="93a1a-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="93a1a-140">Close the page.</span></span>

