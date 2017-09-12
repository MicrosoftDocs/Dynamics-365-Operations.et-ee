---
title: "Ühe kande ja valuuta ümberhindamise täiendus"
description: "Mõned organisatsioonid sisestavad töölehti, mis sisaldavad ühte kannet, millel on rohkem kui üks klient või hankija ning nad käivitavad ka müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessi. See teema kirjeldab juhiseid, mida need organisatsioonid peaksid rakenduse Microsoft Dynamics 365 for Operations versiooni 1611 uuendamisel järgima."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 13ad43cc77731727525aae1edc4d405c166acbc1
ms.contentlocale: et-ee
ms.lasthandoff: 07/18/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a><span data-ttu-id="c21e8-104">Ühe kande ja valuuta ümberhindamise täiendus</span><span class="sxs-lookup"><span data-stu-id="c21e8-104">Single voucher and currency revaluation upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c21e8-105">Mõned organisatsioonid sisestavad töölehti, mis sisaldavad ühte kannet, millel on rohkem kui üks klient või hankija ning nad käivitavad ka müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="c21e8-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="c21e8-106">See teema kirjeldab juhiseid, mida need organisatsioonid peaksid rakenduse Microsoft Dynamics 365 for Operations versiooni 1611 uuendamisel järgima.</span><span class="sxs-lookup"><span data-stu-id="c21e8-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="c21e8-107">Järgige neid juhiseid, kui uuendate rakenduse Microsoft Dynamics 365 for Operations versiooni 1611.</span><span class="sxs-lookup"><span data-stu-id="c21e8-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="c21e8-108">Enne rakendusele Dynamics 365 for Operations uuendamist käivitage müügi- ja ostureskontrole välisvaluuta ümberhindamise protsessid.</span><span class="sxs-lookup"><span data-stu-id="c21e8-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="c21e8-109">Seadke välja **Meetod** väärtuseks **Arve kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="c21e8-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="c21e8-110">Luuakse ümberhindamiskanne, mis tühistab viimase välisvaluuta ümberhindamise.</span><span class="sxs-lookup"><span data-stu-id="c21e8-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="c21e8-111">Seetõttu hinnatakse avatud kandeid nende algses arvestusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="c21e8-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="c21e8-112">Uuendage Dynamics 365 for Operationsi versioonile 1611.</span><span class="sxs-lookup"><span data-stu-id="c21e8-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="c21e8-113">Käivitage müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessid uuesti.</span><span class="sxs-lookup"><span data-stu-id="c21e8-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="c21e8-114">Seekord seadke välja **Meetod** väärtuseks **Standard**.</span><span class="sxs-lookup"><span data-stu-id="c21e8-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="c21e8-115">Luuakse uus ümberhindamise kanne, mis põhineb praegustel valuutakurssidel.</span><span class="sxs-lookup"><span data-stu-id="c21e8-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="c21e8-116">See kanne salvestab realiseerimata kasumi/kahjumi ja õige koondpearaamatukonto.</span><span class="sxs-lookup"><span data-stu-id="c21e8-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





