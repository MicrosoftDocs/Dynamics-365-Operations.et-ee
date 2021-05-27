---
title: Partiinumber eemaldatakse uue partii ID valimisel
description: Kui valite komplekteerimislehe töölehe rea läbivaatamisel, tühjendatakse partiinumbri välja väärtus, kui valite väljal Saatepartii ID uue väärtuse.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 71977a04adb066a8b51c9bf7b8c5a4e752ca902e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026424"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a><span data-ttu-id="34946-103">Partiinumber eemaldatakse uue partii ID valimisel</span><span class="sxs-lookup"><span data-stu-id="34946-103">Batch number is cleared when a new lot ID is selected</span></span>

<span data-ttu-id="34946-104">KB number: 4613107</span><span class="sxs-lookup"><span data-stu-id="34946-104">KB number: 4613107</span></span>

## <a name="symptoms"></a><span data-ttu-id="34946-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="34946-105">Symptoms</span></span>

<span data-ttu-id="34946-106">Kui valite komplekteerimislehe töölehe rea läbivaatamisel, tühjendatakse **partiinumbri välja** väärtus, kui valite väljal **Saatepartii ID** uue väärtuse.</span><span class="sxs-lookup"><span data-stu-id="34946-106">When you're reviewing a picking list journal line, the value in the **Batch number** field is cleared if you select a new value in the **Lot ID** field.</span></span>

## <a name="resolution"></a><span data-ttu-id="34946-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="34946-107">Resolution</span></span>

<span data-ttu-id="34946-108">Süsteem käitub kavandatud viisil.</span><span class="sxs-lookup"><span data-stu-id="34946-108">The system is behaving as designed.</span></span> <span data-ttu-id="34946-109">Partii ID muutmisel muudate kauba konteksti.</span><span class="sxs-lookup"><span data-stu-id="34946-109">If you change the lot ID, you change the item context.</span></span> <span data-ttu-id="34946-110">Seetõttu lähtestatakse partiinumber.</span><span class="sxs-lookup"><span data-stu-id="34946-110">Therefore, the batch number is reset.</span></span>

<span data-ttu-id="34946-111">Partiinumbri seostamiseks saatepartii ID-ga peate esmalt seadistama saatepartii ID.</span><span class="sxs-lookup"><span data-stu-id="34946-111">To associate the batch number with a lot ID, you must set the lot ID first.</span></span>
