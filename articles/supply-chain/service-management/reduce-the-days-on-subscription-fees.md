---
title: Kordustellimuste tasude päevade vähendamine
description: Olemasoleva kordustellimuse tasu päevade arvu vähendamiseks saate luua uue kande, milles eemaldate ajaperioodi, mis ei pea enam olema kordustellimuse tasu intervalli osa.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae2486d08e89c06d76ab9945ccce25c5e97f1500
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010557"
---
# <a name="reduce-the-days-on-subscription-fees"></a><span data-ttu-id="f1774-103">Kordustellimuste tasude päevade vähendamine</span><span class="sxs-lookup"><span data-stu-id="f1774-103">Reduce the days on subscription fees</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f1774-104">Olemasoleva kordustellimuse tasu päevade arvu vähendamiseks saate luua uue kande, milles eemaldate ajaperioodi, mis ei pea enam olema kordustellimuse tasu intervalli osa.</span><span class="sxs-lookup"><span data-stu-id="f1774-104">To reduce the number of days of an existing subscription fee, you can create a new transaction in which you remove the period of time that should no longer be part of the subscription fee interval.</span></span>

## <a name="reduce-the-days-on-a-subscription-fee"></a><span data-ttu-id="f1774-105">Päevade vähendamine kordustellimuse tasul</span><span class="sxs-lookup"><span data-stu-id="f1774-105">Reduce the days on a subscription fee</span></span>

1.  <span data-ttu-id="f1774-106">Klõpsake valikuid **Teenuste haldus** \> **Üldine** \> **Teenuse kordustellimused** \> **Kõik teenuse kordustellimused**.</span><span class="sxs-lookup"><span data-stu-id="f1774-106">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span> <span data-ttu-id="f1774-107">Valige teenuse tellimus ja klõpsake tegevuspaanil nuppu **Kordustellimuse tasud**</span><span class="sxs-lookup"><span data-stu-id="f1774-107">Select the service subscription, and on the Action Pane, click **Subscription fees**</span></span>

2.  <span data-ttu-id="f1774-108">Valige väljas **Kordustellimuse tüüp** suvand **Vähendamispäevad**.</span><span class="sxs-lookup"><span data-stu-id="f1774-108">In the **Subscription type** field, select **Reduction days**.</span></span>

3.  <span data-ttu-id="f1774-109">Kasutage välja **Alates kuupäevast** ja välju **Lõppkuupäev** kordustellimuse tasu kuupäevade vahemiku määratlemiseks, mida soovite kordustellimuse tasu perioodist eemaldada, ja klõpsake siis nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="f1774-109">Use the **From date** field and the **To date** fields to define the date interval of the subscription fee that you want to remove from the subscription fee period, and then click **OK**.</span></span>

<span data-ttu-id="f1774-110">Loodud kande vaatamiseks klõpsake välja **Kordustellimus** ja seejärel välja **Tasukanded**.</span><span class="sxs-lookup"><span data-stu-id="f1774-110">To view the transaction that was created, in the **Subscription** form, click **Fee transactions**.</span></span>

## <a name="example"></a><span data-ttu-id="f1774-111">Näide</span><span class="sxs-lookup"><span data-stu-id="f1774-111">Example</span></span>

<span data-ttu-id="f1774-112">Kui kordustellimuse kande periood kestab 1. jaanuarist 31. jaanuarini ja te soovite perioodi vähendada 10 päeva võrra, looge uus kanne, milles vähendamisperiood kestab 1. jaanuarist 10. jaanuarini.</span><span class="sxs-lookup"><span data-stu-id="f1774-112">If a subscription transaction period runs from January 1 to January 31, and you want to reduce the period by 10 days, create a new transaction in which the reduction period is January 1 to January 10.</span></span> <span data-ttu-id="f1774-113">(Vähendamisperiood võib olla ka 5. jaanuarist 15. jaanuarini või muu kümnepäevane periood.)</span><span class="sxs-lookup"><span data-stu-id="f1774-113">(The reduction period could also be January 5 to January 15, or any other ten day period).</span></span>

<span data-ttu-id="f1774-114">Kui väljal **Alates kuupäevast** on vähendusperiood 21. jaanuar (31 miinus 10), saate seadistada välja **Lõppkuupäev** mis tahes kuupäevani pärast 31. jaanuari, kuid tasukandest eemaldatakse ikka 10 päeva.</span><span class="sxs-lookup"><span data-stu-id="f1774-114">Also, if the **From date** on the reduction period is January 21 (31 minus 10), you could set the **To date** to any date after January 31, and 10 days will still be removed from the fee transaction period.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1774-115">Vt ka</span><span class="sxs-lookup"><span data-stu-id="f1774-115">See also</span></span>

[<span data-ttu-id="f1774-116">Vähendamispäevade näide</span><span class="sxs-lookup"><span data-stu-id="f1774-116">Reduction days example</span></span>](reduction-days-example.md)

  


