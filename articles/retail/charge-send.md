---
title: "Tellimuse lähetamine muust kauplusest"
description: Selles teemas kirjeldatakse tasu saatmise funktsiooni.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 797058bdbbdb63a08eb35034ffe3c913307f38df
ms.openlocfilehash: 41434614b01f9a00f2b8a56765ecb90ee07e3d90
ms.contentlocale: et-ee
ms.lasthandoff: 03/05/2018

---

# <a name="ship-an-order-from-a-different-store"></a><span data-ttu-id="07952-103">Tellimuse lähetamine muust kauplusest</span><span class="sxs-lookup"><span data-stu-id="07952-103">Ship an order from a different store</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="07952-104">Dynamics 365 for Retaili tasu saatmise funktsiooniga saate teha klienditellimuse ühes kaupluses ja lähetada selle teisest kauplusest.</span><span class="sxs-lookup"><span data-stu-id="07952-104">With the Charge send feature in Dynamics 365 for Retail, customer orders can be placed in one store and shipped from another store.</span></span> <span data-ttu-id="07952-105">Kassas vormistatavad klienditellimused toetavad mitmesuguseid täitmisvalikuid.</span><span class="sxs-lookup"><span data-stu-id="07952-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="07952-106">Täitmisvalikud on muuhulgas järgmised.</span><span class="sxs-lookup"><span data-stu-id="07952-106">Some examples of fulfillment options include:</span></span>
-   <span data-ttu-id="07952-107">Kättesaamine samast kauplusest muul kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="07952-107">Pick up from the same store on a different date.</span></span>
-   <span data-ttu-id="07952-108">Kättesaamine muust kauplusest samal või muul kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="07952-108">Pick up from a different store on the same date or a different date.</span></span>
-   <span data-ttu-id="07952-109">Lähetamine kauplusele määratud vaikelaost ja tarnimine konkreetsel kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="07952-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="07952-110">Tasu saatmise funktsioon kasutab järgmisi kassa operatsioone: Läheta kõik tooted ja Läheta valitud tooted.</span><span class="sxs-lookup"><span data-stu-id="07952-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="07952-111">See võimaldab kassapidajal valida lähtekoha, kust saab tellimuse või selle rea täita.</span><span class="sxs-lookup"><span data-stu-id="07952-111">This allows the store clerk to select the “ship from” location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="07952-112">Vaikimisi on lähtekoht kauplusega seotud lähetav ladu.</span><span class="sxs-lookup"><span data-stu-id="07952-112">By default, the “ship from” location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="07952-113">Müüja saab siiski asukohta muuta ja valida mis tahes kaupluse, mis on määratletud kauplusele määratud kaupluselokaatori grupis.</span><span class="sxs-lookup"><span data-stu-id="07952-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span> 

<span data-ttu-id="07952-114">See ei mõjuta sihtaadresside valimise võimalust.</span><span class="sxs-lookup"><span data-stu-id="07952-114">The ability to select “ship to” addresses remains unchanged.</span></span> 

<span data-ttu-id="07952-115">Tarneviisid, mida saab tellimuse rea täitmiseks kasutada, põhinevad toodete ja aadresside jaoks sobivatel tarneviisidel.</span><span class="sxs-lookup"><span data-stu-id="07952-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="07952-116">Kuna sobivate tarneviiside reegleid talletatakse ainult kaupluse halduses (HQ), teeb kassaklient reaalajas kõne tarnerea jaoks sobivate tarneviiside toomiseks.</span><span class="sxs-lookup"><span data-stu-id="07952-116">Because the rules about valid of modes of delivery are maintained only in the Retail headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span> 


