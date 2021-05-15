---
title: Voog ei ole puhastamiseks kõlblik
description: Voog ei ole puhastamiseks kõlblik
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924323"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="c324b-103">Voog ei ole puhastamiseks kõlblik</span><span class="sxs-lookup"><span data-stu-id="c324b-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="c324b-104">Tõrkekood: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="c324b-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="c324b-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="c324b-105">Symptoms</span></span>

<span data-ttu-id="c324b-106">Süsteem näitab järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="c324b-106">The system shows the following error message:</span></span>

> <span data-ttu-id="c324b-107">Voog %1 ei ole puhastamise jaoks sobilik.</span><span class="sxs-lookup"><span data-stu-id="c324b-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="c324b-108">Voo andmeid ei saa puhastada.</span><span class="sxs-lookup"><span data-stu-id="c324b-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="c324b-109">Põhjus</span><span class="sxs-lookup"><span data-stu-id="c324b-109">Cause</span></span>

<span data-ttu-id="c324b-110">Voogu töödeldakse praegu, nagu näitab üks järgmistest tingimustest:</span><span class="sxs-lookup"><span data-stu-id="c324b-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="c324b-111">**Voo staatus** väli on seatud *Teostamisele*.</span><span class="sxs-lookup"><span data-stu-id="c324b-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="c324b-112">Kui valite **Partiitöö** grupis **Voog** vahekaardil **Voog** Tegevuspaanil väli **Olek** ei ole seatud *Lõpetatud*, *Viga* või *Tühistatud*.</span><span class="sxs-lookup"><span data-stu-id="c324b-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="c324b-113">Seetõttu käitatakse praegu pakett-tööd.</span><span class="sxs-lookup"><span data-stu-id="c324b-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="c324b-114">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="c324b-114">Resolution</span></span>

<span data-ttu-id="c324b-115">Tegevuspaani vahekaardil **Laine** grupis **Laine** valige **Pakett töö** ja siis järgige üht nendest sammudest:</span><span class="sxs-lookup"><span data-stu-id="c324b-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="c324b-116">Kui välja **Olek** on määratud *Teostamine*: Valige Action Paanil vahekaardil **Partiitöö** grupis **Partiitöö** valige **Vaata ülesandeid**.</span><span class="sxs-lookup"><span data-stu-id="c324b-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="c324b-117">Edenemist saate jälgida värskendades lehte **Partii ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="c324b-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="c324b-118">Kui välja **Olek** ei ole määratud *Teostamine*: Valige Action Paanil vahekaardil **Partiitöö** grupis **Funktsioonid** valige **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="c324b-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="c324b-119">Valige väljal **Vali uus olek** *Ootamine*.</span><span class="sxs-lookup"><span data-stu-id="c324b-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="c324b-120">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c324b-120">Then select **OK**.</span></span>
