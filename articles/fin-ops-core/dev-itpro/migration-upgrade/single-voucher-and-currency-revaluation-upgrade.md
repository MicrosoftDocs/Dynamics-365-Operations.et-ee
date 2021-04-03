---
title: Üksiku kande töölehtede ja valuuta ümberarvutamise täiendus
description: Selles teemas kirjeldatakse, kuidas täiendada üksiku kande töölehtede ja valuuta ümberarvutamist.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: fb4eca4933716105789d3bbc21dd374395211d1d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559517"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="0e2e4-103">Üksiku kande töölehtede ja valuuta ümberarvutamise täiendus</span><span class="sxs-lookup"><span data-stu-id="0e2e4-103">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e2e4-104">Mõned organisatsioonid sisestavad töölehti, mis sisaldavad ühte kannet, millel on rohkem kui üks klient või hankija ning nad käivitavad ka müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="0e2e4-104">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="0e2e4-105">See teema kirjeldab juhiseid, mida need organisatsioonid peaksid rakenduse Microsoft Dynamics 365 for Operations versiooni 1611 värskendamisel järgima.</span><span class="sxs-lookup"><span data-stu-id="0e2e4-105">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="0e2e4-106">Järgige neid juhiseid, kui täiendate rakenduse Microsoft Dynamics 365 for Operations versioonile 1611.</span><span class="sxs-lookup"><span data-stu-id="0e2e4-106">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="0e2e4-107">Enne rakendusele Finance and Operations täiendamist käivitage müügi- ja ostureskontrole välisvaluuta ümberhindamise protsessid.</span><span class="sxs-lookup"><span data-stu-id="0e2e4-107">Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="0e2e4-108">Seadke välja **Meetod** väärtuseks **Arve kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="0e2e4-108">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="0e2e4-109">Luuakse ümberhindamiskanne, mis tühistab viimase välisvaluuta ümberhindamise.</span><span class="sxs-lookup"><span data-stu-id="0e2e4-109">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="0e2e4-110">Seetõttu hinnatakse avatud kandeid nende algses arvestusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="0e2e4-110">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="0e2e4-111">Uuendage versioonile 1611.</span><span class="sxs-lookup"><span data-stu-id="0e2e4-111">Upgrade to version 1611.</span></span>
3.  <span data-ttu-id="0e2e4-112">Käivitage müügi- ja ostureskontro välisvaluuta ümberarvutamise protsessid uuesti.</span><span class="sxs-lookup"><span data-stu-id="0e2e4-112">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="0e2e4-113">Seekord seadke välja **Meetod** väärtuseks **Standard**.</span><span class="sxs-lookup"><span data-stu-id="0e2e4-113">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="0e2e4-114">Luuakse uus ümberhindamise kanne, mis põhineb praegustel valuutakurssidel.</span><span class="sxs-lookup"><span data-stu-id="0e2e4-114">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="0e2e4-115">See kanne salvestab realiseerimata kasumi/kahjumi ja õige koondpearaamatukonto.</span><span class="sxs-lookup"><span data-stu-id="0e2e4-115">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]