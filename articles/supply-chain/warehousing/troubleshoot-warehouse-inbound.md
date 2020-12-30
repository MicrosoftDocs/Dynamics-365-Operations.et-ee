---
title: Saabuvate kaupade laotoimingute tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada saabuvate kaupade laotoimingutega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 60b6e37ec9d716f635c2d25374ac25a82286660e
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645968"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="62527-103">Saabuvate kaupade laotoimingute tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="62527-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62527-104">Selles teemas kirjeldatakse, kuidas lahendada saabuvate kaupade laotoimingutega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.</span><span class="sxs-lookup"><span data-stu-id="62527-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="62527-105">Kuvatakse järgmine tõrketeade: "Kvaliteetne tellimus %1 on loodud.</span><span class="sxs-lookup"><span data-stu-id="62527-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="62527-106">Kogumiprofiili ei leitud, kontrollige oma konfiguratsiooni."</span><span class="sxs-lookup"><span data-stu-id="62527-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="62527-107">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="62527-107">Issue description</span></span>

<span data-ttu-id="62527-108">See tõrketeade on seotud vastuvõtu protsessiga, kus kvaliteedijuhtimine (QMS) on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="62527-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="62527-109">Sõltuvalt teie keskkonna konfiguratsioonist võib lisateave tõrkesõnumit tekitava tehingu kohta aidata probleemi lahendada.</span><span class="sxs-lookup"><span data-stu-id="62527-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="62527-110">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="62527-110">Issue resolution</span></span>

<span data-ttu-id="62527-111">Esmalt vaadake üle [kogumi komplekteerimise](set-up-cluster-picking.md) seadistus ja veenduge, et teie kogumiprofiilid on õigesti seadistatud.</span><span class="sxs-lookup"><span data-stu-id="62527-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="62527-112">Te ei saa kasutada mobiilse seadme menüükäsku kogumi komplekteerimiseks, kui pole kogumiprofiilid ei ole seadistatud.</span><span class="sxs-lookup"><span data-stu-id="62527-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="62527-113">Sõltuvalt teie keskkonnast võib olla ka võimalik üle vaadata teisi seotud konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="62527-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="62527-114">Kasutatav kombineeritud identifitseerimisnumber ei tööta ühegi likvideerimise koodi, v.a krediidi puhul.</span><span class="sxs-lookup"><span data-stu-id="62527-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="62527-115">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="62527-115">Issue description</span></span>

<span data-ttu-id="62527-116">Kui likvideerimise koodi **Tegevuse** välja väärtuseks on seatud *Krediit* või *Praak*, saate tagastatud kaupade töötlemiseks kasutada ainult [Kombineeritud identifitseerimisnumbri vastuvõtmise](mixed-license-plate-receiving.md) menüükäsku.</span><span class="sxs-lookup"><span data-stu-id="62527-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="62527-117">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="62527-117">Issue resolution</span></span>

<span data-ttu-id="62527-118">Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang.</span><span class="sxs-lookup"><span data-stu-id="62527-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="62527-119">Hetkel toetatakse kombineeritud identifitseerimisnumbri vastuvõtmiseks ainult [likvideerimiskoode](../service-management/set-up-disposition-codes.md), mille puhul on **Tegevuse** välja väärtuseks seatud *Krediit* või *Praak*.</span><span class="sxs-lookup"><span data-stu-id="62527-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="62527-120">Kui ma käitan vastuvõetud toodete perioodilise ülesande värskendamist, kinnitatakse kinnitamata ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="62527-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="62527-121">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="62527-121">Issue description</span></span>

<span data-ttu-id="62527-122">Pärast seda, kui käivitate *Toote sissetulekute uuendamise* perioodilise ülesande, kinnitab süsteem automaatselt kinnitamata ostutellimused, millel on lao kande olek *Registreeritud*.</span><span class="sxs-lookup"><span data-stu-id="62527-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="62527-123">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="62527-123">Issue resolution</span></span>

<span data-ttu-id="62527-124">Uus sissetuleva koorma käitlemise funktsioon *Koorma koguste ülelaekumine* lahendab selle probleemi.</span><span class="sxs-lookup"><span data-stu-id="62527-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="62527-125">Lülitage see funktsioon sisse, minge [Funktsioonihaldusesse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lülitage sisse järgmised funktsioonid (samas järjekorras nagu need on loetletud):</span><span class="sxs-lookup"><span data-stu-id="62527-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="62527-126">Ostutellimuse varude kannete seostamine koormusega</span><span class="sxs-lookup"><span data-stu-id="62527-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="62527-127">Koorma koguste liigne vastuvõtt</span><span class="sxs-lookup"><span data-stu-id="62527-127">Over receipt of load quantities</span></span>

<span data-ttu-id="62527-128">Lisateavet vt teemast [Registreeritud toodete koguste sisestamine ostutellimuste eest](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="62527-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>
