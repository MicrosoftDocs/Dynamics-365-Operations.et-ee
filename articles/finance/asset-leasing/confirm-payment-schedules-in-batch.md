---
title: Vara rentimise maksegraafikute hulgikinnitamine
description: Selles teemas selgitatakse, kuidas mitu maksegraafikut hulgikinnitada.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9c680ea16e9f64107fde081c7e7763697356dcc1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971374"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="70751-103">Vara rentimise maksegraafikute hulgikinnitamine</span><span class="sxs-lookup"><span data-stu-id="70751-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70751-104">Selles teemas selgitatakse, kuidas mitu maksegraafikut hulgikinnitada.</span><span class="sxs-lookup"><span data-stu-id="70751-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="70751-105">Maksegraafikud kinnitatakse kas rendikirje põhiselt või hulgikinnitamise protsessi kaudu.</span><span class="sxs-lookup"><span data-stu-id="70751-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="70751-106">Töölehe kirje saab sisestada ainult kinnitatud maksegraafikuga rendikirjele.</span><span class="sxs-lookup"><span data-stu-id="70751-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="70751-107">Maksegraafiku kinnitamine toimib rentimise finantsteabe lõpliku kinnitamisena.</span><span class="sxs-lookup"><span data-stu-id="70751-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="70751-108">Kõik rendikirje finantsteabe tulevased muudatused (nt maksed ja rendiperiood), moodustavad rendi korrigeerimise ja tuleks sel viisil töödelda.</span><span class="sxs-lookup"><span data-stu-id="70751-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="70751-109">Mitme maksegraafiku kinnitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="70751-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="70751-110">Avage suvand **Vara rentimine \> Perioodiline \> Kinnitamise partii**.</span><span class="sxs-lookup"><span data-stu-id="70751-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="70751-111">Valige lehel **Kinnitamise partii** suvand **Kinnitamise partii**.</span><span class="sxs-lookup"><span data-stu-id="70751-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="70751-112">Kuvatavas dialoogiaknas filtreerige raamatud, mille soovite kinnitada.</span><span class="sxs-lookup"><span data-stu-id="70751-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="70751-113">Kõigi kindlas rendirühmas olevate raamatute kinnitamiseks valige grupp väljal **Rendigrupp**.</span><span class="sxs-lookup"><span data-stu-id="70751-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="70751-114">Konkreetsete raamatute kinnitamiseks valige raamatud väljal **Raamatu ID**.</span><span class="sxs-lookup"><span data-stu-id="70751-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="70751-115">Kõigi raamatute kinnitamiseks lülitage sisse parameeter **Kõigi raamatute jaoks**.</span><span class="sxs-lookup"><span data-stu-id="70751-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="70751-116">Teave äsja kinnitatud raamatute kohta kuvatakse lehel **Kinnitatud raamatud**.</span><span class="sxs-lookup"><span data-stu-id="70751-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="70751-117">Pärast maksegraafikute kinnitamist saab algse tuvastamise töölehtede kirjed sisestada vastavate rendikirjete suhtes.</span><span class="sxs-lookup"><span data-stu-id="70751-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>
