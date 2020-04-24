---
title: Ohtlikud materjalid
description: See teema annab teavet teie keskkonda talletatud ohtlike materjalide dokumentide ja teabe kohta.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5006f06d90ddcc314a51878e9e21337de7d493e7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208455"
---
# <a name="hazardous-materials"></a><span data-ttu-id="ec6d5-103">Ohtlikud materjalid</span><span class="sxs-lookup"><span data-stu-id="ec6d5-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec6d5-104">Teave ohtlike materjalide kohta on seadistatud toote teabehalduses.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="ec6d5-105">Siit moodulist leiate ka laohalduse kaudu prinditavad dokumendid.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="ec6d5-106">Kui saadate materjale, mis on liigitatud ohtlikeks kaupadeks, tuleb saadetistega kaasa panna täiendavat dokumentatsiooni.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="ec6d5-107">Ohtlike materjalide funktsioon võimaldab klientidel talletada klassifikatsiooni teavet ja siduda seda lähetatavate kaupadega.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="ec6d5-108">Seda teavet saab kasutada saatmisdokumentide ettevalmistamise hõlbustamiseks.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec6d5-109">Selleks et aidata hallata ohtlike kaupade saadetisi, võimaldab Microsoft Dynamics 365 Supply Chain Management teil seadistada tootega seotud viiteteavet.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="ec6d5-110">Samuti saate seadistada täiendavaid tarnedokumente.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="ec6d5-111">Süsteem ei vasta aga automaatselt teie riigi või piirkonna määrustele.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="ec6d5-112">See on tööriist, mis aitab teid üldiselt kogu programmis.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="ec6d5-113">Enne kui saate seda funktsiooni kasutada, on vaja teha järgmised seadistused.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="ec6d5-114">**Toote teabehaldus:** saate seadistada väljastatud toodetele rakendatavaid koode.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="ec6d5-115">**Laohaldus:** saadetise teabe printimiseks saate kasutada täiendavaid tarnedokumente.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="ec6d5-116">Tooteteabe haldus</span><span class="sxs-lookup"><span data-stu-id="ec6d5-116">Product information management</span></span>

<span data-ttu-id="ec6d5-117">Toote teabehalduses on olemas valik seadistustabeleid, kus saate lisada viiteteabe, mis on esitatud ohtlike kaupade loendites maantee-, õhu- ja meretranspordi jaoks.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="ec6d5-118">Siin on mõned määrused, millele sageli viidatakse.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="ec6d5-119">**ADR** – määrused, mis on seotud ohtlike kaupade rahvusvahelise autoveoga</span><span class="sxs-lookup"><span data-stu-id="ec6d5-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="ec6d5-120">**CFR 49** – Ameerika Ühendriikide määrused ohtlike kaupade veo kohta</span><span class="sxs-lookup"><span data-stu-id="ec6d5-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="ec6d5-121">**IMDG** – rahvusvaheline ohtlike kaupade (IMDG) kood</span><span class="sxs-lookup"><span data-stu-id="ec6d5-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="ec6d5-122">**IATA** – Rahvusvahelise Lennutranspordi Assotsiatsiooni (IATA) ohtlike kaupade määrused</span><span class="sxs-lookup"><span data-stu-id="ec6d5-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="ec6d5-123">Kõigis neis määrustes on viitekoode sisaldav ohtlike kaupade loend.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="ec6d5-124">Iga transporditüübi loendid on kombineeritud rahvusvaheliste ühisklassifikaatoritega.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="ec6d5-125">Supply Chain Management pakub nende loendite ühiskasutatavate koodide viitetabeli.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="ec6d5-126">Igal loendil on ka mõned unikaalsed koodid, mida saab määratleda.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="ec6d5-127">Selle teabe konfigureerimise alustamiseks looge määrus, mida saate kasutada algsete parameetrite konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="ec6d5-128">Laohaldus</span><span class="sxs-lookup"><span data-stu-id="ec6d5-128">Warehouse management</span></span>

<span data-ttu-id="ec6d5-129">Kui saadetis on ette valmistatud, saab printida mitu uut aruannet.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="ec6d5-130">Need aruanded kasutavad teavet, mida olete toote teabehalduses seadistanud.</span><span class="sxs-lookup"><span data-stu-id="ec6d5-130">These reports use the information that you set up in Product information management.</span></span>
