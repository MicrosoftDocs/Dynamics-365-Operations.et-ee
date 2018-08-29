---
title: "Üksiku kande töölehtede ja valuuta ümberarvutamiste täiendamine"
description: "Mõned organisatsioonid sisestavad töölehti, mis sisaldavad ühte kannet, millel on rohkem kui üks klient või hankija ning nad käivitavad ka müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessi. See teema kirjeldab juhiseid, mida need organisatsioonid peaksid rakenduse Microsoft Dynamics 365 for Operations versiooni 1611 uuendamisel järgima."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 343fa226e1cf9072696082e9ebf0a1629e553ae9
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="dc47e-104">Üksiku kande töölehtede ja valuuta ümberarvutamiste täiendamine</span><span class="sxs-lookup"><span data-stu-id="dc47e-104">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc47e-105">Mõned organisatsioonid sisestavad töölehti, mis sisaldavad ühte kannet, millel on rohkem kui üks klient või hankija ning nad käivitavad ka müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="dc47e-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="dc47e-106">See teema kirjeldab juhiseid, mida need organisatsioonid peaksid rakenduse Microsoft Dynamics 365 for Operations versiooni 1611 uuendamisel järgima.</span><span class="sxs-lookup"><span data-stu-id="dc47e-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="dc47e-107">Järgige neid juhiseid, kui uuendate rakenduse Microsoft Dynamics 365 for Operations versiooni 1611.</span><span class="sxs-lookup"><span data-stu-id="dc47e-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="dc47e-108">Enne rakendusele Dynamics 365 for Operations uuendamist käivitage müügi- ja ostureskontrole välisvaluuta ümberhindamise protsessid.</span><span class="sxs-lookup"><span data-stu-id="dc47e-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="dc47e-109">Seadke välja **Meetod** väärtuseks **Arve kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="dc47e-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="dc47e-110">Luuakse ümberhindamiskanne, mis tühistab viimase välisvaluuta ümberhindamise.</span><span class="sxs-lookup"><span data-stu-id="dc47e-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="dc47e-111">Seetõttu hinnatakse avatud kandeid nende algses arvestusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="dc47e-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="dc47e-112">Uuendage Dynamics 365 for Operationsi versioonile 1611.</span><span class="sxs-lookup"><span data-stu-id="dc47e-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="dc47e-113">Käivitage müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessid uuesti.</span><span class="sxs-lookup"><span data-stu-id="dc47e-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="dc47e-114">Seekord seadke välja **Meetod** väärtuseks **Standard**.</span><span class="sxs-lookup"><span data-stu-id="dc47e-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="dc47e-115">Luuakse uus ümberhindamise kanne, mis põhineb praegustel valuutakurssidel.</span><span class="sxs-lookup"><span data-stu-id="dc47e-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="dc47e-116">See kanne salvestab realiseerimata kasumi/kahjumi ja õige koondpearaamatukonto.</span><span class="sxs-lookup"><span data-stu-id="dc47e-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





