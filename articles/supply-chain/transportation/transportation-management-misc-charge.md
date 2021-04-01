---
title: Transpordi halduse lisakulud
description: See teema selgitab, kuidas transpordi loodud tasusid tuleb seostada tasu koodiga.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 4f58db216176832d61bdafbe43831ededd3dd6dc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233411"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="051dd-103">Transpordi halduse lisakulud</span><span class="sxs-lookup"><span data-stu-id="051dd-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="051dd-104">Nii nagu kõigi teiste lisatasude puhul, tuleb transpordi loodud tasusid seostada tasu koodiga.</span><span class="sxs-lookup"><span data-stu-id="051dd-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="051dd-105">Vastasel juhul ei lisata neid tagasi tellimusele lisakuluna.</span><span class="sxs-lookup"><span data-stu-id="051dd-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="051dd-106">**Kulude kood** määratleb, kuidas tasu arvestatakse seoses tellimuse ja tellimuse reaga, kuhu see lisatakse.</span><span class="sxs-lookup"><span data-stu-id="051dd-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="051dd-107">Minge **Transpordi haldus > Seadistus > Hinnang > Lisakulud**, et määratleda kvalifitseeruvad kriteeriumid, mis määravad, millal kindlat **Tasu koodi** rakendatakse tasule.</span><span class="sxs-lookup"><span data-stu-id="051dd-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="051dd-108">Teil peaks olema vähemalt üks seadistus iga vastava **Tasumooduli** sätte jaoks (*Klient* ja *Hankija*), kus **Lisakulude tüüp** on seatud väärtusele *Ei ole*.</span><span class="sxs-lookup"><span data-stu-id="051dd-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="051dd-109">Kui see puudub, siis lisakulu *ei* lisata tellimusele.</span><span class="sxs-lookup"><span data-stu-id="051dd-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]