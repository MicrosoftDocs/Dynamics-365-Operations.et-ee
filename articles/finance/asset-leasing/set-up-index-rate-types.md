---
title: Indeksimäärade seadistamine
description: Selles teemas selgitatakse, kuidas seadistada indeksimäärasid. Indeksimäärad on kohustuslikud, kui teie organisatsioon seostab rendimakse summad indeksimäärade kogumiga.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6424248e8d01d04720ad65e80aaa543b42abccc6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823019"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="deaa7-104">Indeksimäärade seadistamine</span><span class="sxs-lookup"><span data-stu-id="deaa7-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="deaa7-105">Kui rendimaksed sõltuvad indeksist, saab süsteemis lisada ja hallata indeksimäära tüüpe.</span><span class="sxs-lookup"><span data-stu-id="deaa7-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="deaa7-106">Rendimaksete ümberhindamiseks lehelt **Indeksimäära tüüp**, kasutab indeksimäära ümberhindamise protsess ümberhindamise kuupäeva kõige viimast indeksimäära.</span><span class="sxs-lookup"><span data-stu-id="deaa7-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="deaa7-107">Indeksimäära tüüpide ja indeksimäärade lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="deaa7-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="deaa7-108">Avage **Vara rentimine \> Seadistus \> Indeksimäära tüüp**.</span><span class="sxs-lookup"><span data-stu-id="deaa7-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="deaa7-109">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="deaa7-109">Select **New**.</span></span>
3. <span data-ttu-id="deaa7-110">Sisestage vastavatele väljadele määra tüüp ja indeksimäära nimi.</span><span class="sxs-lookup"><span data-stu-id="deaa7-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="deaa7-111">Uue indeksimäära väärtuse lisamiseks valige indeksimäära tüüp ja seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="deaa7-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="deaa7-112">Valige määra kehtiv alguskuupäev ja valige määra väärtus.</span><span class="sxs-lookup"><span data-stu-id="deaa7-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="deaa7-113">Peate valima indeksimäära meetodiks kas **Indeksimäära väärtuse erinevus** või **Indeksimäära väärtus**.</span><span class="sxs-lookup"><span data-stu-id="deaa7-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="deaa7-114">Valige alguskuupäeva indeksimäära ja kõige viimase indeksimäära vahel põhinedes uue rendimakse arvutamiseks meetod **Indeksimäära väärtuse erinevus**.</span><span class="sxs-lookup"><span data-stu-id="deaa7-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="deaa7-115">Indeksimäär määratletakse väljal **Indeksimäär (%)**.</span><span class="sxs-lookup"><span data-stu-id="deaa7-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="deaa7-116">Valige meetod **Indeksimäära väärtus**, et arvutada rendimakse väljal **Indeksimäär (%)** määratletud protsendi alusel.</span><span class="sxs-lookup"><span data-stu-id="deaa7-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]