---
title: MPOS-i ja pilve kassa (CPOS) jaoks laiendatud sisselogimise funktsiooni seadistamine
description: See teema käsitleb võimalusi laiendatud sisselogimise seadistamiseks pilvekassas ja Retail Modern POS-is (MPOS).
author: rubencdelgado
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f9d8889581e2e11fa5261805c866a6014df57611
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027572"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a><span data-ttu-id="da9a3-103">Cloud MPOS ja Cloud POS‑i laiendatud sisselogimisfunktsiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="da9a3-103">Set up extended logon functionality for MPOS and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da9a3-104">See teema käsitleb võimalusi laiendatud sisselogimise seadistamiseks pilvekassas ja Retail Modern POS-is (MPOS).</span><span class="sxs-lookup"><span data-stu-id="da9a3-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

## <a name="setting-up-extended-logon"></a><span data-ttu-id="da9a3-105">Laiendatud sisselogimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="da9a3-105">Setting up extended logon</span></span>

<span data-ttu-id="da9a3-106">Vöötkoodi maskide seadistuse leiate järgmist teed pidi: **Jaemüük ja kaubandus** &gt; **Kanali häälestus** &gt; **Kassa seadistus** &gt;**Kassa profiilid** &gt; **Funktsiooniprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="da9a3-106">You can find the setup for bar code masks at **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="da9a3-107">Kiirkaart **Funktsioonid** sisaldab järgmisi laiendatud sisselogimisega seotud suvandeid.</span><span class="sxs-lookup"><span data-stu-id="da9a3-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="da9a3-108">Personali vöötkoodi sisselogimine</span><span class="sxs-lookup"><span data-stu-id="da9a3-108">Staff bar code logon</span></span>

<span data-ttu-id="da9a3-109">Kui suvand **Personali vöötkoodiga sisselogimine** on lubatud, saavad töötajad, kelle kassa identimisteabele on määratud laiendatud sisselogimine, vöötkoodi kasutades sisse logida.</span><span class="sxs-lookup"><span data-stu-id="da9a3-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="da9a3-110">Personali vöötkoodiga sisselogimisel on nõutav parool</span><span class="sxs-lookup"><span data-stu-id="da9a3-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="da9a3-111">Kui suvand **Personali vöötkoodiga sisselogimisel on nõutav parool** on lubatud, valib personali vöötkoodiga sisselogimine ainult selle töötaja, kellel on määratud esitatud laiendatud sisselogimine.</span><span class="sxs-lookup"><span data-stu-id="da9a3-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="da9a3-112">Kui see suvand on lubatud, peavad töötajad ka parooli sisestama.</span><span class="sxs-lookup"><span data-stu-id="da9a3-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="da9a3-113">Personali kaardi sisselogimine</span><span class="sxs-lookup"><span data-stu-id="da9a3-113">Staff card logon</span></span>

<span data-ttu-id="da9a3-114">Kui suvand **Personali kaardiga sisselogimine** on lubatud, saavad töötajad, kelle kassa identimisteabele on määratud laiendatud sisselogimine, magnetriba kasutades sisse logida.</span><span class="sxs-lookup"><span data-stu-id="da9a3-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="da9a3-115">Personali kaardiga sisselogimisel on nõutav parool</span><span class="sxs-lookup"><span data-stu-id="da9a3-115">Staff card logon requires password</span></span>

<span data-ttu-id="da9a3-116">Kui suvand **Personali kaardiga sisselogimisel on nõutav parool** on lubatud, valib personali kaardiga sisselogimine ainult selle töötaja, kellel on määratud esitatud laiendatud sisselogimine.</span><span class="sxs-lookup"><span data-stu-id="da9a3-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="da9a3-117">Kui see suvand on lubatud, peavad töötajad ka parooli sisestama.</span><span class="sxs-lookup"><span data-stu-id="da9a3-117">Workers must still enter their password when this option is enabled.</span></span>

## <a name="assigning-an-extended-logon"></a><span data-ttu-id="da9a3-118">Laiendatud sisselogimise määramine</span><span class="sxs-lookup"><span data-stu-id="da9a3-118">Assigning an extended logon</span></span>

<span data-ttu-id="da9a3-119">Vaikimisi saavad töötajatele laiendatud sisselogimist määrata ainult juhid.</span><span class="sxs-lookup"><span data-stu-id="da9a3-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="da9a3-120">Laiendatud sisselogimise määramiseks avage kassas valik **Laiendatud sisselogimine**.</span><span class="sxs-lookup"><span data-stu-id="da9a3-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="da9a3-121">Seejärel otsige töötajat, sisestades otsinguväljale tema operaatori ID.</span><span class="sxs-lookup"><span data-stu-id="da9a3-121">Then search for a worker by entering the worker's operator ID in the search field.</span></span> <span data-ttu-id="da9a3-122">Valige töötaja ja klõpsake seejärel nuppu **Määra**.</span><span class="sxs-lookup"><span data-stu-id="da9a3-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="da9a3-123">Järgmisel leheküljel tehke töötajale laiendatud sisselogimise määramiseks kaaarditõmme või ‑skann.</span><span class="sxs-lookup"><span data-stu-id="da9a3-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="da9a3-124">Kui kaarditõmme või ‑skann on edukalt loetud, ilmub nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="da9a3-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="da9a3-125">Töötajale laiendatud sisselogimise salvestamiseks klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="da9a3-125">Click **OK** to save the extended logon for that worker.</span></span>

## <a name="deleting-an-extended-logon"></a><span data-ttu-id="da9a3-126">Laiendatud sisselogimise kustutamine</span><span class="sxs-lookup"><span data-stu-id="da9a3-126">Deleting an extended logon</span></span>

<span data-ttu-id="da9a3-127">Töötajale määratud laiendatud sisselogimise kustutamiseks otsige töötajat toimingu **Laiendatud sisselogimine** abil.</span><span class="sxs-lookup"><span data-stu-id="da9a3-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="da9a3-128">Valige töötaja ja klõpsake seejärel nuppu **Eemalda määrang**.</span><span class="sxs-lookup"><span data-stu-id="da9a3-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="da9a3-129">Kõik töötajaga seostatud laiendatud sisselogimise identimisteave eemaldatakse.</span><span class="sxs-lookup"><span data-stu-id="da9a3-129">All extended logon credentials that are associated with that worker are removed.</span></span>

## <a name="extending-extended-logon"></a><span data-ttu-id="da9a3-130">Laiendatud sisselogimine laiendamine</span><span class="sxs-lookup"><span data-stu-id="da9a3-130">Extending extended logon</span></span>

<span data-ttu-id="da9a3-131">Sisselogimisteenust saab laiendada täiendavate laiendatud sisselogimine seadmete nagu käsiskannerid toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="da9a3-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="da9a3-132">Lisateabe saamiseks vt kassa laiendatavuse dokumentatsiooni.</span><span class="sxs-lookup"><span data-stu-id="da9a3-132">For more information, see the POS extensibility documentation.</span></span>

## <a name="using-extended-logon"></a><span data-ttu-id="da9a3-133">Laiendatud sisselogimise kasutamine</span><span class="sxs-lookup"><span data-stu-id="da9a3-133">Using extended logon</span></span>

<span data-ttu-id="da9a3-134">Kui laiendatud sisselogimine on konfigureeritud ja töötajale on määratud vöötkood või magnetriba, peab töötaja kassa sisselogimislehe kuvamisel tegema ainult kaarditõmbe või ‑skanni.</span><span class="sxs-lookup"><span data-stu-id="da9a3-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan the worker's card while the POS logon page is displayed.</span></span> <span data-ttu-id="da9a3-135">Kui sisselogimise jätkamiseks on kohustuslik ka parool, palutakse töötajal sisestada oma parool.</span><span class="sxs-lookup"><span data-stu-id="da9a3-135">If a password is also required before logon can proceed, the worker is prompted to enter the worker's password.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]