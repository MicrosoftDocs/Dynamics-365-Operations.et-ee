---
title: Saabuvate kaupade laotoimingute tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada saabuvate kaupade laotoimingutega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f0ea2ee208cdbb8f9fa6668bbcb6e15252a7c1b1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828222"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="39896-103">Saabuvate kaupade laotoimingute tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="39896-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39896-104">Selles teemas kirjeldatakse, kuidas lahendada saabuvate kaupade laotoimingutega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.</span><span class="sxs-lookup"><span data-stu-id="39896-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="39896-105">Kuvatakse järgmine tõrketeade: "Kvaliteetne tellimus %1 on loodud.</span><span class="sxs-lookup"><span data-stu-id="39896-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="39896-106">Kogumiprofiili ei leitud, kontrollige oma konfiguratsiooni."</span><span class="sxs-lookup"><span data-stu-id="39896-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="39896-107">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="39896-107">Issue description</span></span>

<span data-ttu-id="39896-108">See tõrketeade on seotud vastuvõtu protsessiga, kus kvaliteedijuhtimine (QMS) on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="39896-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="39896-109">Sõltuvalt teie keskkonna konfiguratsioonist võib lisateave tõrkesõnumit tekitava tehingu kohta aidata probleemi lahendada.</span><span class="sxs-lookup"><span data-stu-id="39896-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="39896-110">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="39896-110">Issue resolution</span></span>

<span data-ttu-id="39896-111">Esmalt vaadake üle [kogumi komplekteerimise](set-up-cluster-picking.md) seadistus ja veenduge, et teie kogumiprofiilid on õigesti seadistatud.</span><span class="sxs-lookup"><span data-stu-id="39896-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="39896-112">Te ei saa kasutada mobiilse seadme menüükäsku kogumi komplekteerimiseks, kui pole kogumiprofiilid ei ole seadistatud.</span><span class="sxs-lookup"><span data-stu-id="39896-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="39896-113">Sõltuvalt teie keskkonnast võib olla ka võimalik üle vaadata teisi seotud konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="39896-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="39896-114">Kasutatav kombineeritud identifitseerimisnumber ei tööta ühegi likvideerimise koodi, v.a krediidi puhul.</span><span class="sxs-lookup"><span data-stu-id="39896-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="39896-115">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="39896-115">Issue description</span></span>

<span data-ttu-id="39896-116">Kui likvideerimise koodi **Tegevuse** välja väärtuseks on seatud *Krediit* või *Praak*, saate tagastatud kaupade töötlemiseks kasutada ainult [Kombineeritud identifitseerimisnumbri vastuvõtmise](mixed-license-plate-receiving.md) menüükäsku.</span><span class="sxs-lookup"><span data-stu-id="39896-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="39896-117">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="39896-117">Issue resolution</span></span>

<span data-ttu-id="39896-118">Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang.</span><span class="sxs-lookup"><span data-stu-id="39896-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="39896-119">Hetkel toetatakse kombineeritud identifitseerimisnumbri vastuvõtmiseks ainult [likvideerimiskoode](../service-management/set-up-disposition-codes.md), mille puhul on **Tegevuse** välja väärtuseks seatud *Krediit* või *Praak*.</span><span class="sxs-lookup"><span data-stu-id="39896-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="39896-120">Kui ma käitan vastuvõetud toodete perioodilise ülesande värskendamist, kinnitatakse kinnitamata ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="39896-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="39896-121">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="39896-121">Issue description</span></span>

<span data-ttu-id="39896-122">Pärast seda, kui käivitate *Toote sissetulekute uuendamise* perioodilise ülesande, kinnitab süsteem automaatselt kinnitamata ostutellimused, millel on lao kande olek *Registreeritud*.</span><span class="sxs-lookup"><span data-stu-id="39896-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="39896-123">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="39896-123">Issue resolution</span></span>

<span data-ttu-id="39896-124">Uus sissetuleva koorma käitlemise funktsioon *Koorma koguste ülelaekumine* lahendab selle probleemi.</span><span class="sxs-lookup"><span data-stu-id="39896-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="39896-125">Lülitage see funktsioon sisse, minge [Funktsioonihaldusesse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lülitage sisse järgmised funktsioonid (samas järjekorras nagu need on loetletud):</span><span class="sxs-lookup"><span data-stu-id="39896-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="39896-126">Ostutellimuse varude kannete seostamine koormusega</span><span class="sxs-lookup"><span data-stu-id="39896-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="39896-127">Koorma koguste liigne vastuvõtt</span><span class="sxs-lookup"><span data-stu-id="39896-127">Over receipt of load quantities</span></span>

<span data-ttu-id="39896-128">Lisateavet vt teemast [Registreeritud toodete koguste sisestamine ostutellimuste eest](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="39896-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="39896-129">Sissetulevate tellimuste registreerimisel kuvatakse järgmine tõrketeade: "Kogus on kehtetu".</span><span class="sxs-lookup"><span data-stu-id="39896-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="39896-130">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="39896-130">Issue description</span></span>

<span data-ttu-id="39896-131">Kui väli **Litsentsiplaadi grupeerimise poliitika** on seatud väärtusele *Kasutaja määratud* mobiilse seadme menüükäsule, mida kasutatakse sissetulevate tellimuste registreerimiseks, saate tõrketeate ("Kogus on kehtetu") ja registreerimist ei saa lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="39896-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="39896-132">Väljastamise põhjus</span><span class="sxs-lookup"><span data-stu-id="39896-132">Issue cause</span></span>

<span data-ttu-id="39896-133">Kui *kasutaja määratletud* on kasutatud litsentsiplaadi grupeerimispoliitikana, tükeldab süsteem sissetulevad varud eraldi litsentsiplaatideks, nagu näitab ka ühiku seeriagrupp.</span><span class="sxs-lookup"><span data-stu-id="39896-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="39896-134">Kui vastuvõetava kauba jälgimiseks kasutatakse partii- või seerianumbreid, tuleb iga partii või seerianumbri kogus registreerida registreeritud numbrimärgi kohta.</span><span class="sxs-lookup"><span data-stu-id="39896-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="39896-135">Kui litsentsiplaadi jaoks määratud kogus ületab koguse, mis praeguste mõõtmete jaoks tuleb veel saada, kuvatakse tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="39896-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="39896-136">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="39896-136">Issue resolution</span></span>

<span data-ttu-id="39896-137">Kui registreerite kauba mobiilse seadme menüü-üksuse abil, kus väli **Litsentsiplaadi grupeerimise poliitika** väärtuseks on seatud *Kasutaja määratud*, võib süsteem nõuda litsentsiplaadi numbrite, partii- või seerianumbrite kinnitamist või sisestamist.</span><span class="sxs-lookup"><span data-stu-id="39896-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="39896-138">Litsentsiplaadi kinnituslehel näitab süsteem praeguse litsentsiplaadi jaoks eraldatud kogust.</span><span class="sxs-lookup"><span data-stu-id="39896-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="39896-139">Partii- või seeriakinnituse lehtedel näitab süsteem kogust, mis praegusel litsentsiplaadile peab veel laekuma.</span><span class="sxs-lookup"><span data-stu-id="39896-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="39896-140">See hõlmab ka välja, kus saate sisestada koguse, et registreerida see litsentsiplaadi ja partii- või seerianumbri kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="39896-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="39896-141">Sel juhul veenduge, et litsentsiplaadile registreeritav kogus ei ületaks vastuvõetud kogust.</span><span class="sxs-lookup"><span data-stu-id="39896-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="39896-142">Kui sissetuleva tellimuse registreerimisel luuakse liiga palju litsentsiplaate, saab välja **Litsentsiplaadi grupeerimise poliitika** väärtust muuta väärtuseks *Litsentsiplaadi grupeerimine*, määrata kaubale uus ühiku seeriagrupp või üksuse seeriagrupi suvand **litsentsiplaadi grupeerimise** inaktiveerida.</span><span class="sxs-lookup"><span data-stu-id="39896-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
