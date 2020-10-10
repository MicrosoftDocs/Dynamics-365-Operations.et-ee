---
title: Talenti laiendamine Power Appsi ja Power Automate’iga
description: Selles artiklis kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 Human Resources, mis kasutab Microsoft Power Appsi ja Microsoft Power Automate’i.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b28480ff584870e931fdc288a2652a5649268576
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893073"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="84311-103">Laiendamine Power Appsi ja Power Automate’iga</span><span class="sxs-lookup"><span data-stu-id="84311-103">Extend with Power Apps and Power Automate</span></span>

<span data-ttu-id="84311-104">Selles artiklis kirjeldatakse laiendatavuse stsenaariume rakenduses Microsoft Dynamics 365 Human Resources, mis kasutab Microsoft Power Appsi ja Microsoft Power Automate’i.</span><span class="sxs-lookup"><span data-stu-id="84311-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="84311-105">Saate rakenduse Power Apps keskkonda importida iga näitega seotud lahendusepaketi.</span><span class="sxs-lookup"><span data-stu-id="84311-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="84311-106">Seejärel saate pakette kasutada juhisena või lähtekohana teie organisatsioonile sobivate stsenaariumide rakendamiseks.</span><span class="sxs-lookup"><span data-stu-id="84311-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="84311-107">Kui soovite kasutada selles teemas kirjeldatud malle ja rakendusi muutmata kujul, katsetage neid kindlasti veendumaks, et need hõlmaksid kõiki teie juurutusele kehtivaid stsenaariume.</span><span class="sxs-lookup"><span data-stu-id="84311-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="84311-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="84311-108">Prerequisites</span></span>

- <span data-ttu-id="84311-109">Pakettide importimiseks peab kasutajatel olema **keskkonna looja** luba.</span><span class="sxs-lookup"><span data-stu-id="84311-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="84311-110">Rakenduste eksportimiseks või importimiseks peab kasutajatel olema Power Appsi plaani 2 litsents või Power Appsi plaani 2 proovilitsents.</span><span class="sxs-lookup"><span data-stu-id="84311-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-microsoft-365-power-automate"></a><span data-ttu-id="84311-111">Integreerimine rakendustega Microsoft 365, Power Automate</span><span class="sxs-lookup"><span data-stu-id="84311-111">Integration with Microsoft 365, Power Automate</span></span>

<span data-ttu-id="84311-112">Rakendust **Microsoft 365-ga integreerimine** saab kasutada sisse logitud kasutajate töörühma teabe ekstraktimiseks Microsoft 365-st.</span><span class="sxs-lookup"><span data-stu-id="84311-112">The **Integration with Microsoft 365** app can be used to extract team information for signed-in users from Microsoft 365.</span></span> <span data-ttu-id="84311-113">See viitab töötajatele rakenduses Human Resources, et hankida töövõtja tuvastustüüpe.</span><span class="sxs-lookup"><span data-stu-id="84311-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="84311-114">Haldurid saavad kontrollida töötaja ID-tüüpide aegumiskuupäevi.</span><span class="sxs-lookup"><span data-stu-id="84311-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="84311-115">Samuti võivad nad saata meeldetuletuse, kui töötaja ID-tüüp on aegumas.</span><span class="sxs-lookup"><span data-stu-id="84311-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="84311-116">Selle meeldetuletuse saatmiseks Power Automate integreerub Power Appsiga.</span><span class="sxs-lookup"><span data-stu-id="84311-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="84311-117">Kui meeldetuletus on saadetus, saadetakse Power Automate’ist tagasi Power Appsi kinnitus.</span><span class="sxs-lookup"><span data-stu-id="84311-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="84311-118">Identifikatsiooni tüübid hõlmavad juhiluba, passi ja teisi aktsepteeritavaid ID vorme.</span><span class="sxs-lookup"><span data-stu-id="84311-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="84311-119">Saate seda rakendust laiendada teistele stsenaariumidele.</span><span class="sxs-lookup"><span data-stu-id="84311-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="84311-120">Näiteks saate seda kasutada töörühma puhkuste teabe, kalendrisündmuste ja töörühmaga seotud sündmuste näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="84311-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="84311-121">Rakenduse **Microsoft 365, Power Automate'iga integreerimine** allalaadimiseks avage Microsofti allalaadimiskeskuses [Microsoft 365-ga integreerimine](https://go.microsoft.com/fwlink/?linkid=2081787).</span><span class="sxs-lookup"><span data-stu-id="84311-121">To download the **Integration with Microsoft 365, Power Automate** app, go to [Integration with Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="84311-122">Power Automate – SQL-i ühendamine ja käivitamine</span><span class="sxs-lookup"><span data-stu-id="84311-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="84311-123">Mall **Power Automate – SQL-i ühendamine ja käivitamine** loob ühenduse Microsoft SQL Serveriga ja lubab käivitada SQL-i päringuid.</span><span class="sxs-lookup"><span data-stu-id="84311-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="84311-124">Kuigi see mall loeb ja värskendab SQL-tabeleid, saate seda laiendada ja kasutada seda muude stsenaariumite jaoks.</span><span class="sxs-lookup"><span data-stu-id="84311-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="84311-125">Näiteks saate seda kasutada vahetabeli täitmiseks teenuses Common Data Service kirjetega SQL-serverist ja vahetabeli aeg-ajalt sünkroonimiseks, kasutades SQL-serveri astmelist jaotust.</span><span class="sxs-lookup"><span data-stu-id="84311-125">For example, you can use it to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="84311-126">Täpsem päring on integreeritud Flowga, mis võimaldab andmete teisendamist ja astmelist jaotust.</span><span class="sxs-lookup"><span data-stu-id="84311-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="84311-127">Malli **Power Automate – SQL-i ühendamine ja käivitamine** allalaadimiseks avage Microsofti allalaadimiskeskuses [Power Automate – SQL-i ühendamine ja käivitamine](https://go.microsoft.com/fwlink/?linkid=2081789).</span><span class="sxs-lookup"><span data-stu-id="84311-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84311-128">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="84311-128">Additional resources</span></span>

[<span data-ttu-id="84311-129">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="84311-129">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>