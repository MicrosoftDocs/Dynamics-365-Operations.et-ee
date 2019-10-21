---
title: EE-00015 Makseviite loomise tööriist
description: See protseduur juhatab teid läbi makseviidete koostamise protseduuri.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccount, LedgerJournalTable, LedgerJournalTransDaily
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Estonia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ece3940f735f40d5543c15c2ca416e0b8a24320
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183599"
---
# <a name="ee-00015-payment-reference-generation-tool"></a><span data-ttu-id="38b6c-103">EE-00015 Makseviite loomise tööriist</span><span class="sxs-lookup"><span data-stu-id="38b6c-103">EE-00015 Payment reference generation tool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="38b6c-104">See protseduur juhatab teid läbi makseviidete koostamise protseduuri.</span><span class="sxs-lookup"><span data-stu-id="38b6c-104">This procedure walks you through generating the payment references.</span></span> <span data-ttu-id="38b6c-105">Ülesande loomisel kasutati demoettevõtte DEMF, mille juriidilise isiku esmase aadressi riigiks/regiooniks on määratud Eesti, andmeid.</span><span class="sxs-lookup"><span data-stu-id="38b6c-105">This task was created using the demo data company DEMF with the country/region of legal entity primary address updated to be Estonia.</span></span> <span data-ttu-id="38b6c-106">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="38b6c-106">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="specify-a-number-sequence-for-payment-references"></a><span data-ttu-id="38b6c-107">Määratlege viitenumbrite jaoks numbriseeria vorming.</span><span class="sxs-lookup"><span data-stu-id="38b6c-107">Specify a number sequence for payment references</span></span>
1. <span data-ttu-id="38b6c-108">Minge jaotisse Müügireskontro > Seadistus > Müügireskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="38b6c-108">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="38b6c-109">Klõpsake vahekaarti Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="38b6c-109">Click the Number sequences tab.</span></span>
3. <span data-ttu-id="38b6c-110">Viiteveerus.</span><span class="sxs-lookup"><span data-stu-id="38b6c-110">In the Reference column.</span></span> <span data-ttu-id="38b6c-111">Leidke ja valige kirje "Makseviide".</span><span class="sxs-lookup"><span data-stu-id="38b6c-111">find and select 'Payment reference' record.</span></span>
4. <span data-ttu-id="38b6c-112">Sisestage või valige väärtus väljal Numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="38b6c-112">In the Number sequence code field, enter or select a value.</span></span>
    * <span data-ttu-id="38b6c-113">Võite valida eraldi, vastloodud numbrilise ja pideva numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="38b6c-113">You may want to select a dedicated, newly created numeric and continuous number sequence.</span></span> <span data-ttu-id="38b6c-114">Demo eesmärgil kasutage "Acco_18".</span><span class="sxs-lookup"><span data-stu-id="38b6c-114">For demo purposes, you can use  'Acco_18'.</span></span>  
5. <span data-ttu-id="38b6c-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="38b6c-115">Click Save.</span></span>

## <a name="create-payment-reference-numbers"></a><span data-ttu-id="38b6c-116">Loo makse viitenumbrid</span><span class="sxs-lookup"><span data-stu-id="38b6c-116">Create payment reference numbers</span></span>
1. <span data-ttu-id="38b6c-117">Avage Müügireskonto > Perioodilised ülesanded > Viitenumbrite loomine.</span><span class="sxs-lookup"><span data-stu-id="38b6c-117">Go to Accounts receivable > Periodic tasks > Create payment reference numbers.</span></span>
2. <span data-ttu-id="38b6c-118">Väljal Viitenumbrite loomine valige Jah.</span><span class="sxs-lookup"><span data-stu-id="38b6c-118">Select Yes in the Create payment reference numbers field.</span></span>
    * <span data-ttu-id="38b6c-119">Juba klientidele määratud viitenumbrite kustutamiseks valige käsk "Kustuta maksete viitenumbrid".</span><span class="sxs-lookup"><span data-stu-id="38b6c-119">Select 'Delete payment reference numbers' to remove reference numbers already assigned to customers.</span></span> <span data-ttu-id="38b6c-120">Võite piirata klientide hulka, kellelt soovite eemaldada või kellele lisada viitenumbri. Selleks kasutage jaotist "Kirjenda kaasamiseks" ja määrake klientidele või kliendirühmadele kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="38b6c-120">You may limit the customers for which you want to remove or create reference numbers by using 'Record to include' section and applying criteria for customers or customer groups.</span></span>  
3. <span data-ttu-id="38b6c-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="38b6c-121">Click OK.</span></span>

