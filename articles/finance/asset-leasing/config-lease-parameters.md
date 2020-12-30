---
title: Rentimise parameetrite konfigureerimine (eelversioon)
description: See teema kirjeldab varade rentimise konfiguratsiooni seadistusi, nagu turbeteave ja raamatupidamise sätteid.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f71006570cd8f2bdc0385388eae0800cd29d3ec8
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442567"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="ac2d7-103">Rentimise parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ac2d7-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac2d7-104">Varade rentimise käitumist mõjutavad mitu konfiguratsiooni sätet.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="ac2d7-105">Need sätted hõlmavad töölehe nimesid, üldisi parameetreid ja sisestusreeglite sätteid.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="ac2d7-106">Avage **Vara rentimine \> Seadistus \> Vara rentimise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="ac2d7-107">Valige vahekaardil **Rendikirjed** kiirkaart **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="ac2d7-108">Parameeter **Luba käsitsi klassifitseerimise alistamise** määratleb, kas rendi klassifikatsiooni saab alistada enne maksegraafiku kinnitamist.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="ac2d7-109">Parameeter **Ristolemi partii** määratleb, kas saate sisestada praegusest juriidilisest isikust teistesse juriidilistesse isikutesse.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="ac2d7-110">Kui see parameeter on sisse lülitatud, saate luua töölehe kandeid juriidilistele isikutele, millele teil on juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="ac2d7-111">Määrake suvandi **Luba kinnitatud rendilepingute kustutamine** väärtusele **Jah**, et lubada rendikirjed, milles sisalduvad kustutamiseks kinnitatud maksegraafikuid.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="ac2d7-112">Rendikirjeid saab kustutada, kui nendega on seostatud sisestatud või sisestamata kanded, olenemata selle valiku sättest.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="ac2d7-113">Rendikirjet ei saa pärast kustutamist taastada.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="ac2d7-114">Kui laadite mõne kustutatud rendikirjetest (käsitsi või andmeolemite), käsitletakse üleslaaditud teavet uuena, mitte olemasoleva rendikirje värskendusena.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="ac2d7-115">Kui valite selle suvandi väärtuseks **Jah** ja raamatu kande tüüp on **Kumulatiivse järelkulu valik A või B**, määrab süsteem välja **Alternatiivne laenuintressimäär** suvandi **Ülemineku alternatiivne laenuintressimäär** väärtuseks **Raamatu häälestus**.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="ac2d7-116">Kui selle suvandi väärtuseks on määratud **Ei**, seatakse põhirendi määr välja **Alternatiivne laenuintressimäär** väärtusele lehel **Raamatu üksikasjad**, sõltumata raamatu ülekande tüübist.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="ac2d7-117">Määrake suvandi **Luba suletud raamatu versiooni suvand kulumiarvestused** väärtuseks **Jah**, et lubada kulumiarvestuse kannete ümberpööramine.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="ac2d7-118">Kulukanded saab pöörata ümber isegi siis, kui raamatu versioon on suletud.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac2d7-119">Soovitame jätta selle suvandi väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="ac2d7-120">Selle suvandi valikut kasutatakse kontrollimiseks ja juhtimiseks, et takistada suletud raamatu versiooni juhuslikku amortiseerimist.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="ac2d7-121">Kui hoiate suvandi väärtusel **Ei**, saate hoida raamatu netoväärtuse ja tulevased kulumiarvutused täpsena.</span><span class="sxs-lookup"><span data-stu-id="ac2d7-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>
