---
title: Tagastatud kauba osaliste tarnete vastu võtmine
description: Osatarned määratakse tagastustellimuse ridade, mitte tagastustellimuse saadetistena.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31db10ad820bf049192ba0446b59da16cab3c553
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010593"
---
# <a name="receive-partial-deliveries-of-returned-items"></a><span data-ttu-id="eadb8-103">Tagastatud kauba osaliste tarnete vastu võtmine</span><span class="sxs-lookup"><span data-stu-id="eadb8-103">Receive partial deliveries of returned items</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="eadb8-104">Osatarned määratakse tagastustellimuse ridade, mitte tagastustellimuse saadetistena.</span><span class="sxs-lookup"><span data-stu-id="eadb8-104">Partial deliveries are defined in terms of return order lines, not return order shipments.</span></span>

<span data-ttu-id="eadb8-105">See tähendab, et kui saate täiskoguse, mis on näidatud ühel tagastustellimuse real, kuid ei saa midagi teistelt tagastustellimuse ridadelt, siis ei ole tarne osatarne.</span><span class="sxs-lookup"><span data-stu-id="eadb8-105">This means that if you receive the full quantity that is indicated on one return order line, but you receive nothing from the other lines in the return order, the delivery is not a partial delivery.</span></span> <span data-ttu-id="eadb8-106">Kui tagastustellimuse rida nõuab aga konkreetse kauba kümne ühiku tagastamist, kuid teie saate ainult neli, on tegu osatarnega.</span><span class="sxs-lookup"><span data-stu-id="eadb8-106">However, if a return order line requires 10 units of a particular item to be returned, but you receive only four, it is a partial delivery.</span></span>

<span data-ttu-id="eadb8-107">Kui tagastussaadetise kogus on väiksem kui tagastustellimuse rea täiskogus, saate saadetise kõrvale panna ja oodata ülejäänud tagastatud koguse saabumist või saate registreerida ja sisestada osakoguse.</span><span class="sxs-lookup"><span data-stu-id="eadb8-107">If a return shipment contains less than the full quantity of a return order line, you can set the shipment aside and wait for the rest of the returned quantity to arrive, or you can register and post the partial quantity.</span></span>

## <a name="register-and-post-a-partial-quantity"></a><span data-ttu-id="eadb8-108">Osaline koguse registreerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="eadb8-108">Register and post a partial quantity</span></span>

1.  <span data-ttu-id="eadb8-109">Kui olete valinud saabumisel tagastustellimuse vormil **Saabumise ülevaade – Ladu: %1, Ala: %2, Töölehe nimi: %3**, klõpsake käsku **Alusta saabumistöölehte**, et luua saabumistööleht, ja klõpsake valikuid **Töölehed** \> **Kuva sissetulekute saabumistöölehed**, et avada vorm **Asukoha tööleht**.</span><span class="sxs-lookup"><span data-stu-id="eadb8-109">After you select a return order for arrival on the **Arrival overview - Warehouse: %1, Dock: %2, Journal name: %3** form, click **Start arrival** to create the arrival journal, and then click **Journals** \> **Show arrivals from receipts** to open the **Location journal** form.</span></span>

2.  <span data-ttu-id="eadb8-110">Valige töölehe rida, mida soovite kasutada, ja klõpsake seejärel nuppu **Read**, et avada vormi **Töölehe read, asukohad**.</span><span class="sxs-lookup"><span data-stu-id="eadb8-110">Select the line of the journal that you want to work with, and then click **Lines** to open the **Journal lines, locations** form.</span></span>

3.  <span data-ttu-id="eadb8-111">Valige kaubakoodi rida, millele on saabunud ainult osakogus, ja seejärel klõpsake käske **Funktsioonid** \> **Tükelda** vormi **Tükelda** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="eadb8-111">Select the line of the item number for which only a partial quantity has arrived, and then click **Functions** \> **Split** to open the **Split** form.</span></span>

4.  <span data-ttu-id="eadb8-112">Väljale **Tükeldatud kogus** sisestage saadud kaubakoguse koguarv ja seejärel klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="eadb8-112">In the **Split quantity** field, enter the quantity for the total number of items that have been received, and then click **OK**.</span></span>

5.  <span data-ttu-id="eadb8-113">Valige vormil **Töölehe read, asukohad** saabunud kaubakoguse rida ja seejärel klõpsake käsku **Postita**.</span><span class="sxs-lookup"><span data-stu-id="eadb8-113">On the **Journal lines, locations** form, select the line for the quantity of items that has arrived, and then click **Post**.</span></span> <span data-ttu-id="eadb8-114">Täiendava koguse saate reale sisestada pärast kaupade saabumist.</span><span class="sxs-lookup"><span data-stu-id="eadb8-114">You can post the line for the additional quantity after the items have arrived.</span></span>




