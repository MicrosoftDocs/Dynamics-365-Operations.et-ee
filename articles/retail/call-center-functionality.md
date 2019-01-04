---
title: "Kõnekeskuse müügifunktsioonid"
description: "Selles teemas antakse ülevaade kõnekeskuse müügifunktsioonidest rakenduses Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 8b78762ce70b318e1f77e1e49ffaa7b72f01667f
ms.contentlocale: et-ee
ms.lasthandoff: 01/04/2019

---

# <a name="call-center-sales-functionality"></a><span data-ttu-id="23ab6-103">Kõnekeskuse müügifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="23ab6-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="23ab6-104">Rakenduse Dynamics 365 for Retail kõnekeskus on sellist tüüpi jaemüügikanal, mille saab määrata rakenduses.</span><span class="sxs-lookup"><span data-stu-id="23ab6-104">In Dynamics 365 for Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="23ab6-105">Kõnekeskuse üksustele kindla kanali määramine võimaldab süsteemil kindlate andmete ja tellimuse töötlemise vaikesätted kõnekeskuse kanali kasutaja loodud müügitellimustega siduda.</span><span class="sxs-lookup"><span data-stu-id="23ab6-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="23ab6-106">Kõnekeskus sisaldab selliseid funktsioone nagu täpsem jaemüügihind ja kampaaniad, kataloogid, kinkekaardid, püsikliendi programmid ja kupongid.</span><span class="sxs-lookup"><span data-stu-id="23ab6-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="23ab6-107">Kõnekeskuse tellimusi kasutatakse ka kassarakenduses, et toetada kanalite vahelisi tellimuse täitmise stsenaariume.</span><span class="sxs-lookup"><span data-stu-id="23ab6-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="23ab6-108">Siinkohal on oluline märkida, et kuigi kõnekeskuse moodulit saab kasutada teistes valdkondades väljaspool Retaili, pole Dynamics 365 for Retaili praeguse versiooni kõnekeskuse rakendus optimeeritud kasutamiseks ettevõtete vaheliste (B2B) tellimuste töötlemise stsenaariumide jaoks ega selliste stsenaariumide jaoks, kus tellimustel on palju müügiridu.</span><span class="sxs-lookup"><span data-stu-id="23ab6-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Dynamics 365 for Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="23ab6-109">Kasutajatel, kes soovivad kasutada kõnekeskuse tellimuste töötlemise funktsioone väljapool tavapärast vahetult tarbijaga seotud kannete töötlemist, on soovitatav võtta piisavalt aega, et testida ja veenduda, et kõnekeskuse funktsionaalsuse lubamine vastaks funktsionaalsuse ja jõudluse vajadustele.</span><span class="sxs-lookup"><span data-stu-id="23ab6-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="23ab6-110">Lisaks tellimuste loomise toele pakub kõnekeskuse moodul kasutajasõbralikku klienditeenindusrakendust, mis hõlbustab kasutajatel kliendikontode leidmist ja kõigi seonduvate klienditellimuste andmete ja atribuutide ülevaatamist.</span><span class="sxs-lookup"><span data-stu-id="23ab6-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="23ab6-111">Klienditeeninduse ekraan on mõeldud pakkuma kasutajale kiiret juurdepääsu tellimusega seotud andmetele, mis võimaldab klientide kõige levinumatele tellimusega seotud küsimustele kiiresti vastata.</span><span class="sxs-lookup"><span data-stu-id="23ab6-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="23ab6-112">Sellelt leheküljelt leiate lingid asjakohasele Dynamics 365 for Retaili kõnekeskuse seadistuse, konfiguratsiooni ja kasutamise dokumentatsioonile.</span><span class="sxs-lookup"><span data-stu-id="23ab6-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Dynamics 365 for Retail.</span></span>

## <a name="configure-the-call-center"></a><span data-ttu-id="23ab6-113">Kõnekeskuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="23ab6-113">Configure the call center</span></span>

[<span data-ttu-id="23ab6-114">Tellimuse töötlemise suvandite seadistamine</span><span class="sxs-lookup"><span data-stu-id="23ab6-114">Set up order processing options</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="23ab6-115">Tellimuse töötlemise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="23ab6-115">Configure order processing</span></span>

[<span data-ttu-id="23ab6-116">Pettuseteatiste seadistamine</span><span class="sxs-lookup"><span data-stu-id="23ab6-116">Set up fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="23ab6-117">Tellimuste ooteloleku haldamine</span><span class="sxs-lookup"><span data-stu-id="23ab6-117">Manual Order Holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="23ab6-118">Makse töötlemise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="23ab6-118">Configure payment processing</span></span>

[<span data-ttu-id="23ab6-119">Makseviisid kõnekeskuses</span><span class="sxs-lookup"><span data-stu-id="23ab6-119">Payment methods in a call center</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="23ab6-120">Tarneviiside konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="23ab6-120">Configure delivery modes</span></span>

[<span data-ttu-id="23ab6-121">Kõnekeskuse tarneviiside ja -tasude konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="23ab6-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="23ab6-122">Otseturustamise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="23ab6-122">Configure direct marketing</span></span>

[<span data-ttu-id="23ab6-123">Kõnekeskuse kataloogid</span><span class="sxs-lookup"><span data-stu-id="23ab6-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="23ab6-124">RFM-analüüsi seadistamine</span><span class="sxs-lookup"><span data-stu-id="23ab6-124">Set up RFM analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="23ab6-125">Järjepidevusprogrammide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="23ab6-125">Configure continuity programs</span></span>

[<span data-ttu-id="23ab6-126">Kõnekeskuse järjepidevusprogrammi seadistamine</span><span class="sxs-lookup"><span data-stu-id="23ab6-126">Set up a continuity program for a call center</span></span>](set-up-continuity-program.md)

