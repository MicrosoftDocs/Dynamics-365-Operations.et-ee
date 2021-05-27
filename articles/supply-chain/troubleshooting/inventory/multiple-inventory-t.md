---
title: Mitu varude tehingut partiinumbritele, kui füüsiline värskendamine on keelatud
description: Pärast ostutellimuse rea korrigeerimist luuakse mitu varude tehingut, kui partii numbrirühma suvand Füüsilisel uuendamisel valikus on seatud Ei.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026453"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="fb295-103">Mitu varude tehingut partiinumbritele, kui füüsiline värskendamine on keelatud</span><span class="sxs-lookup"><span data-stu-id="fb295-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="fb295-104">KB number: 4613390</span><span class="sxs-lookup"><span data-stu-id="fb295-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="fb295-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="fb295-105">Symptoms</span></span>

<span data-ttu-id="fb295-106">Pärast ostutellimuse rea korrigeerimist luuakse mitu varude tehingut, kui partii numbrirühma suvand **Füüsilisel uuendamisel** valikus on seatud *Ei*.</span><span class="sxs-lookup"><span data-stu-id="fb295-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="fb295-107">Kui loote kauba, kus partiinumbri grupi suvand **Füüsilisel uuendamisel** on seatud valikule *Ei*, loob süsteem osturea koguse muutmisel ja ostutellimuse lehe salvestamisel automaatselt uue partiinumbri.</span><span class="sxs-lookup"><span data-stu-id="fb295-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="fb295-108">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="fb295-108">Resolution</span></span>

<span data-ttu-id="fb295-109">Säte **Füüsilisel uuendamisel** partii numbrigruppidele töötab järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="fb295-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="fb295-110">Kui valiku väärtuseks on määratud *Jah* luuakse uued partiinumbrid alles pärast füüsilist uuendamist (nt kaupade tarnimisel või tarnimisel).</span><span class="sxs-lookup"><span data-stu-id="fb295-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="fb295-111">Kui valikuks on määratud *Ei*, luuakse iga kord, kui toimub rakendatav uuendus, uus partiinumber (nt kui ostutellimusele lisatakse uus kogus).</span><span class="sxs-lookup"><span data-stu-id="fb295-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
