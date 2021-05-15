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
ms.openlocfilehash: 6f6d689c596b4ec924cb50ec3bea8ce907e6dc6b
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920983"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="c6d4e-103">Saabuvate kaupade laotoimingute tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="c6d4e-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6d4e-104">Selles teemas kirjeldatakse, kuidas lahendada saabuvate kaupade laotoimingutega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="c6d4e-105">Kuvatakse järgmine tõrketeade: "Kvaliteetne tellimus %1 on loodud.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="c6d4e-106">Kogumiprofiili ei leitud, kontrollige oma konfiguratsiooni."</span><span class="sxs-lookup"><span data-stu-id="c6d4e-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c6d4e-107">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c6d4e-107">Issue description</span></span>

<span data-ttu-id="c6d4e-108">See tõrketeade on seotud vastuvõtu protsessiga, kus kvaliteedijuhtimine (QMS) on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="c6d4e-109">Sõltuvalt teie keskkonna konfiguratsioonist võib lisateave tõrkesõnumit tekitava tehingu kohta aidata probleemi lahendada.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c6d4e-110">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c6d4e-110">Issue resolution</span></span>

<span data-ttu-id="c6d4e-111">Esmalt vaadake üle [kogumi komplekteerimise](set-up-cluster-picking.md) seadistus ja veenduge, et teie kogumiprofiilid on õigesti seadistatud.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="c6d4e-112">Te ei saa kasutada mobiilse seadme menüükäsku kogumi komplekteerimiseks, kui pole kogumiprofiilid ei ole seadistatud.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="c6d4e-113">Sõltuvalt teie keskkonnast võib olla ka võimalik üle vaadata teisi seotud konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="c6d4e-114">Kasutatav kombineeritud identifitseerimisnumber ei tööta ühegi likvideerimise koodi, v.a krediidi puhul.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c6d4e-115">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c6d4e-115">Issue description</span></span>

<span data-ttu-id="c6d4e-116">Kui likvideerimise koodi **Tegevuse** välja väärtuseks on seatud *Krediit* või *Praak*, saate tagastatud kaupade töötlemiseks kasutada ainult [Kombineeritud identifitseerimisnumbri vastuvõtmise](mixed-license-plate-receiving.md) menüükäsku.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c6d4e-117">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c6d4e-117">Issue resolution</span></span>

<span data-ttu-id="c6d4e-118">Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="c6d4e-119">Hetkel toetatakse kombineeritud identifitseerimisnumbri vastuvõtmiseks ainult [likvideerimiskoode](../service-management/set-up-disposition-codes.md), mille puhul on **Tegevuse** välja väärtuseks seatud *Krediit* või *Praak*.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="c6d4e-120">Kui ma käitan vastuvõetud toodete perioodilise ülesande värskendamist, kinnitatakse kinnitamata ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c6d4e-121">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c6d4e-121">Issue description</span></span>

<span data-ttu-id="c6d4e-122">Pärast seda, kui käivitate *Toote sissetulekute uuendamise* perioodilise ülesande, kinnitab süsteem automaatselt kinnitamata ostutellimused, millel on lao kande olek *Registreeritud*.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c6d4e-123">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c6d4e-123">Issue resolution</span></span>

<span data-ttu-id="c6d4e-124">Uus sissetuleva koorma käitlemise funktsioon *Koorma koguste ülelaekumine* lahendab selle probleemi.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="c6d4e-125">Selle funktsiooni sisselülitamiseks minge [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruum ja lülitage sisse järgmised funktsioonid (samas järjekorras nagu need on loetletud):</span><span class="sxs-lookup"><span data-stu-id="c6d4e-125">To turn on this feature, go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="c6d4e-126">Ostutellimuse varude kannete seostamine koormusega</span><span class="sxs-lookup"><span data-stu-id="c6d4e-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="c6d4e-127">Koorma koguste liigne vastuvõtt</span><span class="sxs-lookup"><span data-stu-id="c6d4e-127">Over receipt of load quantities</span></span>

<span data-ttu-id="c6d4e-128">Lisateavet vt teemast [Registreeritud toodete koguste sisestamine ostutellimuste eest](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="c6d4e-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="c6d4e-129">Sissetulevate tellimuste registreerimisel kuvatakse järgmine tõrketeade: "Kogus on kehtetu".</span><span class="sxs-lookup"><span data-stu-id="c6d4e-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c6d4e-130">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c6d4e-130">Issue description</span></span>

<span data-ttu-id="c6d4e-131">Kui väli **Litsentsiplaadi grupeerimise poliitika** on seatud väärtusele *Kasutaja määratud* mobiilse seadme menüükäsule, mida kasutatakse sissetulevate tellimuste registreerimiseks, saate tõrketeate ("Kogus on kehtetu") ja registreerimist ei saa lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="c6d4e-132">Väljastamise põhjus</span><span class="sxs-lookup"><span data-stu-id="c6d4e-132">Issue cause</span></span>

<span data-ttu-id="c6d4e-133">Kui *kasutaja määratletud* on kasutatud litsentsiplaadi grupeerimispoliitikana, tükeldab süsteem sissetulevad varud eraldi litsentsiplaatideks, nagu näitab ka ühiku seeriagrupp.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="c6d4e-134">Kui vastuvõetava kauba jälgimiseks kasutatakse partii- või seerianumbreid, tuleb iga partii või seerianumbri kogus registreerida registreeritud numbrimärgi kohta.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="c6d4e-135">Kui litsentsiplaadi jaoks määratud kogus ületab koguse, mis praeguste mõõtmete jaoks tuleb veel saada, kuvatakse tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c6d4e-136">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c6d4e-136">Issue resolution</span></span>

<span data-ttu-id="c6d4e-137">Kui registreerite kauba mobiilse seadme menüü-üksuse abil, kus väli **Litsentsiplaadi grupeerimise poliitika** väärtuseks on seatud *Kasutaja määratud*, võib süsteem nõuda litsentsiplaadi numbrite, partii- või seerianumbrite kinnitamist või sisestamist.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="c6d4e-138">Litsentsiplaadi kinnituslehel näitab süsteem praeguse litsentsiplaadi jaoks eraldatud kogust.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="c6d4e-139">Partii- või seeriakinnituse lehtedel näitab süsteem kogust, mis praegusel litsentsiplaadile peab veel laekuma.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="c6d4e-140">See hõlmab ka välja, kus saate sisestada koguse, et registreerida see litsentsiplaadi ja partii- või seerianumbri kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="c6d4e-141">Sel juhul veenduge, et litsentsiplaadile registreeritav kogus ei ületaks vastuvõetud kogust.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="c6d4e-142">Kui sissetuleva tellimuse registreerimisel luuakse liiga palju litsentsiplaate, saab välja **Litsentsiplaadi grupeerimise poliitika** väärtust muuta väärtuseks *Litsentsiplaadi grupeerimine*, määrata kaubale uus ühiku seeriagrupp või üksuse seeriagrupi suvand **litsentsiplaadi grupeerimise** inaktiveerida.</span><span class="sxs-lookup"><span data-stu-id="c6d4e-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
