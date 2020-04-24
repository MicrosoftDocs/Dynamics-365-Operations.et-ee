---
title: Kordustellimuste töövoo ülevaade
description: Teema annab ülevaate kordustellimuse töövoost.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0cb8b86ef0e2a1bd90590c8cc2a20e18e82ef9c6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206584"
---
# <a name="subscription-workflow-overview"></a><span data-ttu-id="b1eca-103">Kordustellimuste töövoo ülevaade</span><span class="sxs-lookup"><span data-stu-id="b1eca-103">Subscription workflow overview</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b1eca-104">Olete valgustusfirma kordustellimuste haldur ja teie ettevõte pakub valgustusseadmete teenuslepinguid.</span><span class="sxs-lookup"><span data-stu-id="b1eca-104">You are the subscriptions administrator for a light company that offers subscriptions for lighting rig maintenance.</span></span> <span data-ttu-id="b1eca-105">Klient soovib teie ettevõttelt osta aastase kordustellimuse valgustusseadmete hooldamiseks.</span><span class="sxs-lookup"><span data-stu-id="b1eca-105">A customer contacts your company to purchase a yearly subscription for lighting rig maintenance.</span></span>

## <a name="setting-up-subscriptions"></a><span data-ttu-id="b1eca-106">Kordustellimuste seadistamine</span><span class="sxs-lookup"><span data-stu-id="b1eca-106">Setting up subscriptions</span></span>

<span data-ttu-id="b1eca-107">Kordustellimuste seadistamiseks tuleb kõigepealt luua kordustellimuste grupp uue teenuseleppe jaoks või kontrollida, kas selline kordustellimuste grupp on juba olemas.</span><span class="sxs-lookup"><span data-stu-id="b1eca-107">To set up a subscription, you must first create a subscription group for the new service agreement or verify that a subscription group exists.</span></span> <span data-ttu-id="b1eca-108">Kui kordustellimuste grupp on olemas, tuleb see seadistada, nii et kliendile esitatakse arve kord aastas ja müügitulusid arveldatakse aasta jooksul iga kuu.</span><span class="sxs-lookup"><span data-stu-id="b1eca-108">If a subscription group exists, you must set it up to invoice the customer yearly and to accrue sales revenue every month of the year.</span></span> <span data-ttu-id="b1eca-109">Lisateavet kordustellimuste seadistamise kohta vt teemast [Kordustellimuste gruppide seadistamine](set-up-subscription-groups.md).</span><span class="sxs-lookup"><span data-stu-id="b1eca-109">For more information about how to set up subscriptions, see [Set up subscription groups](set-up-subscription-groups.md).</span></span>

<span data-ttu-id="b1eca-110">Pärast kordustellimuste grupi loomist saate luua kordustellimuse.</span><span class="sxs-lookup"><span data-stu-id="b1eca-110">After the subscription group is created, you can create the subscription.</span></span> <span data-ttu-id="b1eca-111">Lisateavet teenuse kordustellimuste loomise kohta vt teemast [Teenuse kordustellimuste loomine kordustellimuste grupist](create-service-subscriptions-from-subscription-group.md).</span><span class="sxs-lookup"><span data-stu-id="b1eca-111">For more information about how to create service subscriptions, see [Create service subscriptions from a subscription group](create-service-subscriptions-from-subscription-group.md).</span></span>

## <a name="create-and-modify-subscription-transactions"></a><span data-ttu-id="b1eca-112">Kordustellimuste kannete loomine ja muutmine</span><span class="sxs-lookup"><span data-stu-id="b1eca-112">Create and modify subscription transactions</span></span>

<span data-ttu-id="b1eca-113">Pärast kordustellimuse seadistamist looge kordustellimuse tasukanne esimeseks arveldusperioodiks, mis on üks aasta.</span><span class="sxs-lookup"><span data-stu-id="b1eca-113">After you set up the subscription, you create the subscription fee transaction for the first invoicing period, which is one year.</span></span> <span data-ttu-id="b1eca-114">Kanded on tüübiga **Tavaline**.</span><span class="sxs-lookup"><span data-stu-id="b1eca-114">The transactions are of the **Regular** type.</span></span> <span data-ttu-id="b1eca-115">Seega saate luua ainult selliseid kordustellimuste kandeid, mille alates ja kuni kuupäevad vastavad varem vormis **Perioodi tüübid** loodud perioodidele.</span><span class="sxs-lookup"><span data-stu-id="b1eca-115">Therefore, you can only create subscription transactions where the from date and the to date correspond to periods that were previously created in the **Period types** form.</span></span> <span data-ttu-id="b1eca-116">Lisateavet tasukannete kohta vt teemast [Kordustellimuste tasukannete loomine](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="b1eca-116">For more information about fee transactions, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="b1eca-117">Pärast kliendile kordustellimuse seadistamist meenub teile, et oli kokku lepitud 10-protsendine allahindlus kõigist teenuspakkumiste hinnakirja hindadest.</span><span class="sxs-lookup"><span data-stu-id="b1eca-117">After you set up the subscription for your customer, you remember that they have negotiated a 10 percent discount on all list prices for service offerings.</span></span> <span data-ttu-id="b1eca-118">Seepärast tuleb teil vähendada loodud tasukande hinda.</span><span class="sxs-lookup"><span data-stu-id="b1eca-118">Therefore, you must reduce the price of the transaction fee that you created.</span></span>

<span data-ttu-id="b1eca-119">Hiljem samal päeval teatab kliendi kontaktisik, et kuigi nad endiselt soovivad valgusseadmete teenuselepet, soovivad nad hiljem samal aastal paigaldada uue valgusseadme.</span><span class="sxs-lookup"><span data-stu-id="b1eca-119">Later in the day, your customer contact calls to say that, although they still want the service agreement for the lighting rig, they plan to introduce a new lighting rig later in the year.</span></span> <span data-ttu-id="b1eca-120">Seega vajavad hooldusteenust kuni oktoobrini 2013.</span><span class="sxs-lookup"><span data-stu-id="b1eca-120">Therefore, they only need maintenance coverage until October 2013.</span></span> <span data-ttu-id="b1eca-121">Kliendi kordustellimuses kuude arvu vähendamiseks loote uue kordustellimuste tasukande tüübiga **Vähendamispäevad**.</span><span class="sxs-lookup"><span data-stu-id="b1eca-121">To reduce the number of months for the customer’s subscription, you create a new subscription fee transaction of the **Reduction days** type.</span></span> <span data-ttu-id="b1eca-122">Lisateavet päevade vähendamise kohta vt teemast [Kordustellimuste tasude päevade vähendamine](reduce-the-days-on-subscription-fees.md).</span><span class="sxs-lookup"><span data-stu-id="b1eca-122">For more information about how to reduce days, see [Reduce the days on subscription fees](reduce-the-days-on-subscription-fees.md).</span></span>

## <a name="invoice-and-accrue-subscription-transactions"></a><span data-ttu-id="b1eca-123">Arve koostamine ja kordustellimuste kannete kogumine</span><span class="sxs-lookup"><span data-stu-id="b1eca-123">Invoice and accrue subscription transactions</span></span>

<span data-ttu-id="b1eca-124">Olete nüüd lõpetanud kordustellimuse seadistamise ja olete valmis kliendile arvet koostama.</span><span class="sxs-lookup"><span data-stu-id="b1eca-124">You have now finished setting up the subscription, and you are ready to invoice your customer for it.</span></span> <span data-ttu-id="b1eca-125">Lisateavet kordustellimuste arveldamise kohta vt teemast [Kordustellimuste kannete arveldamine](invoice-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="b1eca-125">For more information about how to invoice subscriptions, see [Invoice subscription transactions](invoice-subscription-transactions.md).</span></span>

<span data-ttu-id="b1eca-126">Kaks päeva hiljem helistab klient, et kordustellimuse arve peaks koostama USA dollarites, mitte eurodes.</span><span class="sxs-lookup"><span data-stu-id="b1eca-126">Two days later, your customer calls to say that the subscription should be invoiced in U.S. dollars, not Euros.</span></span> <span data-ttu-id="b1eca-127">Seega loote kreeditarve ja ka uue kordustellimuse kande vajalikus valuutas.</span><span class="sxs-lookup"><span data-stu-id="b1eca-127">Therefore, you create a credit note, and you also create a new subscription transaction in the correct currency.</span></span> <span data-ttu-id="b1eca-128">Lisateavet kordustellimuste kannete krediteerimise kohta vt teemast [Kordustellimuste kannete krediteerimine](credit-subscription-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="b1eca-128">For more information about how to credit subscription transactions, see [Credit subscription transactions](credit-subscription-transactions.md).</span></span>

<span data-ttu-id="b1eca-129">Iga kuu lõpus saate koguda ühe kuu tulu kliendi kordustellimuselt kasumi- ja kahjumikontole ning lõpetamata toodangu kontodele.</span><span class="sxs-lookup"><span data-stu-id="b1eca-129">At the end of each month, one month's revenue can be accrued from the customer's subscription to the profit and loss account and the WIP accounts.</span></span> <span data-ttu-id="b1eca-130">Lisateavet kordustellimuste tulude kogumise kohta vt teemast [Kordustellimuse tulu kogumine](accrue-subscription-revenue.md).</span><span class="sxs-lookup"><span data-stu-id="b1eca-130">For more information about how to accrue revenue for subscriptions, see [Accrue subscription revenue](accrue-subscription-revenue.md).</span></span>

  


