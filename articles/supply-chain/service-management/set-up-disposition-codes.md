---
title: Saate häälestada likvideerimiskoode.
description: Saate seadistada likvideerimiskoodid, et määrata, kuidas töödeldakse kliendi tagastatavat kaupa.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnDispositionCode
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16f0ddb9ad956367adc66a952bd8d12551da56a5
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983202"
---
# <a name="set-up-disposition-codes"></a><span data-ttu-id="8ae4e-103">Saate häälestada likvideerimiskoode.</span><span class="sxs-lookup"><span data-stu-id="8ae4e-103">Set up disposition codes</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8ae4e-104">Saate seadistada likvideerimiskoodid, et määrata, kuidas töödeldakse kliendi tagastatavat kaupa.</span><span class="sxs-lookup"><span data-stu-id="8ae4e-104">You can set up disposition codes to specify how to process an item that is returned by a customer.</span></span> <span data-ttu-id="8ae4e-105">Näiteks looge likvideerimiskood nimega **Parandamine ja tagastus** näitamaks, et tagastatud kaup parandatakse ja tagastatakse seejärel kliendile.</span><span class="sxs-lookup"><span data-stu-id="8ae4e-105">For example, create a disposition code named **Repair and return** to indicate that the returned item will be repaired and then returned to the customer.</span></span> <span data-ttu-id="8ae4e-106">Rohkem näiteid likvideerimiskoodidest, mida kasutatakse tavaliselt klientide tagastatavate kaupade puhul, vt teemast [Tagastatud kaupade likvideerimise viisi määratlemine](specify-how-to-dispose-of-returned-items.md).</span><span class="sxs-lookup"><span data-stu-id="8ae4e-106">For more examples of disposition codes that are typically used for items that are returned by customers, see [Specify how to dispose of returned items](specify-how-to-dispose-of-returned-items.md).</span></span>

<span data-ttu-id="8ae4e-107">Saate seadistada ka põhjuse koodi, et aidata selgitada, miks kaup tagastati.</span><span class="sxs-lookup"><span data-stu-id="8ae4e-107">You can also set up a reason code to help explain why an item was returned.</span></span> <span data-ttu-id="8ae4e-108">Lisateavet põhjusekoodide kohta vt teemast [Tagastuspõhjuste koodide seadistamine](set-up-return-reason-code.md).</span><span class="sxs-lookup"><span data-stu-id="8ae4e-108">For more information about reason codes, see [Set up return reason codes](set-up-return-reason-code.md).</span></span>

1.  <span data-ttu-id="8ae4e-109">Klõpsake valikuid **Müük ja turundus** \> **Häälestamine** \> **Müügitellimused** \> **Tagastused** \> **Likvideerimiskoodid**.</span><span class="sxs-lookup"><span data-stu-id="8ae4e-109">Click **Sales and marketing** \> **Setup** \> **Sales orders** \> **Returns** \> **Disposition codes**.</span></span>

2.  <span data-ttu-id="8ae4e-110">Klõpsake nuppu **Uus** või vajutage klahve CTRL+N, et luua uus likvideerimiskood.</span><span class="sxs-lookup"><span data-stu-id="8ae4e-110">Click **New** or press CTRL+N to create a new disposition code.</span></span>

3.  <span data-ttu-id="8ae4e-111">Sisestage kordumatu, kirjeldav nimi, valige tegevus ja sisestage likvideerimiskoodi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="8ae4e-111">Enter a unique, descriptive name, select an action, and enter a description for the disposition code.</span></span>

4.  <span data-ttu-id="8ae4e-112">Kui soovite selle likvideerimiskoodiga siduda mingisuguseid kliendikulusid, klõpsake nuppu **Tasud** vormi **Tasude seadistamine** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="8ae4e-112">If you want to associate any customer charges with this disposition code, click the **Charges** button to open the **Set up charges** form.</span></span>

5.  <span data-ttu-id="8ae4e-113">Kui soovite määratleda mõnda välist koodi, et see sobiks ettevõtte enda likvideerimiskoodidega, klõpsake nuppu **Välised koodid** vormi **Välised koodid** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="8ae4e-113">If you want to define any external codes to match with the company's own disposition codes, click the **External codes** button to open the **External codes** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ae4e-114">Vt ka</span><span class="sxs-lookup"><span data-stu-id="8ae4e-114">See also</span></span>

[<span data-ttu-id="8ae4e-115">Klienditagastuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="8ae4e-115">Customer returns overview</span></span>](disposition-and-return-reason-codes.md)

<span data-ttu-id="8ae4e-116">[Likvideerimiskoodid (vorm)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="8ae4e-116">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

<span data-ttu-id="8ae4e-117">[Automaatsed tasud (vorm)](https://technet.microsoft.com/library/aa582856\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="8ae4e-117">[Auto charges (form)](https://technet.microsoft.com/library/aa582856\(v=ax.60\))</span></span>

<span data-ttu-id="8ae4e-118">[Väliskoodid (vorm)](https://technet.microsoft.com/library/aa583814\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="8ae4e-118">[External codes (form)](https://technet.microsoft.com/library/aa583814\(v=ax.60\))</span></span>

  


