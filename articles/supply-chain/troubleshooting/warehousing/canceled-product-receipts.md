---
title: Tühistatud toote kviitungid ei värskenda kande olekut olekusse Registreeritud
description: Kui olete tühistanud toote kviitungid sissetuleval kaubal, uuendab süsteem automaatselt laokande olekut olekust Saadud olekuks Tellitud.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294054"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="c830e-103">Tühistatud toote kviitungid ei värskenda kande olekut olekusse Registreeritud</span><span class="sxs-lookup"><span data-stu-id="c830e-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="c830e-104">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="c830e-104">Symptoms</span></span>

<span data-ttu-id="c830e-105">Kui olete käivitanud toimingu **Tühista toote kviitungid** sissetulevale kaubale, uuendab süsteem automaatselt laokande olekut olekust *Saadud* olekuks *Tellitud*.</span><span class="sxs-lookup"><span data-stu-id="c830e-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="c830e-106">Lahendus</span><span class="sxs-lookup"><span data-stu-id="c830e-106">Resolution</span></span>

<span data-ttu-id="c830e-107">Väljamineva kauba saatelehtede tühistamisel jääb laokannete olekuks *Valitud*.</span><span class="sxs-lookup"><span data-stu-id="c830e-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="c830e-108">Kui sissetulevast kaubast toote sissetulekud tühistatakse, ei taastata laokannete olekuks *Registreeritud*.</span><span class="sxs-lookup"><span data-stu-id="c830e-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="c830e-109">Seetõttu peab laotöötaja pärast sissetulevast kaubast toote sissetuleku tühistamist kaubakogused selle jaoks uuesti registreerima.</span><span class="sxs-lookup"><span data-stu-id="c830e-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="c830e-110">Lisateavet vt jaotisest [Sissetuleva kaubaga saabuvate kaubakoguste registreerimine](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span><span class="sxs-lookup"><span data-stu-id="c830e-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
